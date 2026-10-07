# *A Dark Room*: un estudio técnico narrativo sobre ingeniería inversa ligera, manipulación del estado y análisis de aplicaciones web

## Introducción

Durante mis años en la universidad, en una de mis clases más aburridas di con un juego que paliaba la lectura de diapositivas y así, jugué por primera vez a *A Dark Room*.

Es un juego minimalista que comienza como un idle/clicker, evoluciona hacia la supervivencia, se transforma en un RPG de exploración y termina rozando la ciencia ficción existencial. 
Este verano, y con muchos más conocimientos, decidí volver a él, y en esa segunda partida obtuve una puntuación de **3.990.770**, suficiente para desbloquear el mensaje:

> *expanded story alternate ending behind the scenes commentary*

Ese mensaje fue el detonante. En lugar de limitarme a repetir la experiencia, la curiosidad me pudo y quise comprender el juego desde dentro: cómo estaba construido, cómo gestionaba su estado, qué dependencias internas tenía y hasta qué punto era posible manipularlo. 

Este artículo es una narración técnica de ese proceso.

---

## El ritmo del juego y la necesidad de comprender su arquitectura

*A Dark Room* es deliberadamente lento en sus primeras fases. Avivar el fuego, recoger madera, construir cabañas… todo está diseñado para que el jugador avance de forma gradual. Pero esa lentitud, combinada con mi curiosidad técnica, me llevó a preguntarme cómo funcionaba realmente el juego.

La estructura interna mezcla lógica, estado y UI en un conjunto de scripts que, aunque accesibles, requieren paciencia para recorrerlos. No es tu código, no conoces las convenciones del desarrollador original y muchas funciones dependen de otras partes del motor. 
  La experiencia inicial es la de un explorador que avanza a tientas: inspeccionando scripts, probando comandos en la consola, buscando referencias en internet y reconstruyendo mentalmente, y con papel y boli, la arquitectura del juego.

Poco a poco, esa exploración se convierte en comprensión.

---

## El descubrimiento del State Manager: `$SM`

El primer hallazgo significativo fue el **State Manager**, accesible desde la consola como `$SM`. Este módulo centraliza el estado del juego y permite modificar prácticamente cualquier variable interna. La primera manipulación fue sencilla:

```js
$SM.add('stores["item"]', cantidad);
```

Con este comando es posible alterar recursos sin haber desbloqueado aún la brújula ni el mapa. La madera, los dientes, la piel, las escamas, el hierro, el acero… todos los elementos del almacén pueden generarse de forma inmediata.

Mi configuración inicial para acelerar el comienzo del juego fue:

```js
$SM.add('stores["wood"]', 100000);
$SM.add('stores["teeth"]', 1000);
$SM.add('stores["fur"]', 1000);
$SM.add('stores["scales"]', 1000);
$SM.add('stores["iron"]', 1000);
$SM.add('stores["steel"]', 1000);
$SM.add('stores["bait"]', 1000);
$SM.add('stores["cured meat"]', 1000);
$SM.add('stores["medicine"]', 100);
$SM.add('stores["alien alloy"]', 100000);
```

Este conjunto de comandos elimina la fase inicial del juego y abre la puerta a un análisis más profundo.

---

## La estructura del código fuente: una arquitectura accesible

La navegación por los archivos del juego revela una estructura sorprendentemente clara:

```
/scripts/
  ├── state-manager.js
  ├── world.js
  ├── path.js
  ├── events.js
  ├── fabricator.js
  ├── ship.js
  └── perks.js
```

Cada archivo cumple una función específica: gestión del estado, lógica del mundo, rutas y peso de objetos, eventos, fabricación de objetos avanzados, sistema de la nave y definición de perks. Esta claridad facilita la ingeniería inversa y permite comprender cómo se relacionan las distintas partes del juego.

---

## El Fabricator: acceso directo a objetos avanzados

Uno de los descubrimientos más interesantes fue el **fabricator**, un módulo que permite fabricar objetos avanzados sin necesidad de explorar el mapa. Con `alien alloy` infinito, cualquier objeto especial está al alcance:

```js
Craftables: {
  'energy blade': { ... },
  'fluid recycler': { ... },
  'cargo drone': { ... },
  'kinetic armour': { ... },
  'disruptor': { ... },
  'hypo': { ... },
  'stim': { ... },
  'plasma rifle': { ... },
  'glowstone': { ... }
}
```

Este hallazgo revela una característica importante del juego: su lógica interna está completamente expuesta al cliente.

---

## Eventos, triggers y control del flujo narrativo

El juego incluye eventos que afectan al estado del mundo: tormentas que destruyen edificios, encuentros con personajes, fragmentos del mapa, ventajas temporales. Desde la consola es posible desencadenarlos manualmente:

```js
Events.useShield($('#wanderer'));
```

Esto permite alterar el flujo narrativo del juego y acceder a contenido que normalmente requeriría exploración.

---

## El mapa: exploración sin restricciones

La exploración del mapa es el núcleo del juego. Sin embargo, es posible recorrerlo de una sola vez si se manipulan ciertas variables:

- capacidad de mochila,
- peso de los objetos,
- agua disponible,
- vida base,
- perks de combate y supervivencia.

```js
Path.Weight['cured meat'] = 0;
Path.DEFAULT_BAG_SPACE = 10000;
World.setHp(10000);
World.BASE_WATER = 10000;
```

La cadena de perks más interesante es la que convierte los puños en el arma más poderosa:

```js
boxer → martial artist → unarmed master
```

Esta progresión, normalmente lenta, puede acelerarse:

```js
var perks = [...];
for (var i = 0; i < perks.length; i++) {
    $SM.addPerk(perks[i]);
}
```

---

## La nave: un idle dentro del idle

La nave espacial es, en esencia, un idle dentro del idle. Aunque es posible obtener materiales infinitos, las mejoras requieren clics repetidos. Para evitarlo:

```js
for (let i = 0; i < 1000; i++) {
  Ship.reinforceHull();
  Ship.upgradeEngine();
}
```

La interfaz no está preparada para cambios tan bruscos, así que es necesario refrescarla manualmente:

```js
$('#hullRow .row_val').text($SM.get('game.spaceShip.hull'));
$('#engineRow .row_val').text($SM.get('game.spaceShip.thrusters'));
```

---

## Huts infinitas: el exploit definitivo

En cierto punto descubrí una configuración que generaba **huts infinitas**. Esto implica:

- población infinita,  
- producción ilimitada de recursos,  
- crecimiento exponencial del score.

El equilibrio del juego desaparece y la partida se convierte en un experimento matemático.

Mis puntuaciones fueron:

- **3.990.770**
- **186.150.207**
- **1.591.024.024**
- **1.446.451.315**
- **3.263.351.856** (final)

La multiplicación total fue de **817×**.

---

## Conceptos de seguridad aplicados

Aunque *A Dark Room* es un juego, su arquitectura permite practicar conceptos reales de seguridad en aplicaciones web:

### **1. Confianza en el cliente (client-side trust)**  
El juego delega toda la lógica en el navegador. Esto permite manipular cualquier variable sin restricciones.

### **2. Ausencia de validación**  
No existen límites, rangos ni tipos validados. El usuario puede crear estados imposibles.

### **3. Exposición de API interna**  
Funciones críticas están accesibles desde la consola, lo que equivale a una API sin protección.

### **4. Ingeniería inversa ligera**  
La lectura de scripts y reconstrucción de dependencias es un ejercicio real de ingeniería inversa.

### **5. Manipulación del DOM**  
La interfaz depende del DOM, no del estado real, lo que permite inconsistencias visuales.

### **6. Explotación de lógica**  
Crear rutas alternativas, saltarse requisitos o generar recursos infinitos es explotación de lógica en sentido técnico.

---

## Lecciones aprendidas

Explorar *A Dark Room* desde dentro me permitió comprender cómo se comporta una aplicación web cuando su arquitectura confía plenamente en el cliente. La ausencia de validación, la exposición de funciones internas y la dependencia del DOM son patrones que aparecen en aplicaciones reales y que pueden generar vulnerabilidades.

Este proyecto personal me permitió practicar:

- análisis de código ajeno  
- reconstrucción de arquitectura  
- pensamiento ofensivo  
- manipulación del estado  
- identificación de puntos débiles  
- explotación de lógica

---

## Conclusión

Lo que empezó como una partida más terminó siendo un estudio técnico completo. *A Dark Room* se convirtió en un entorno seguro para experimentar con ingeniería inversa ligera, análisis de seguridad y manipulación del estado. Esta experiencia me permitió reforzar mi capacidad para comprender sistemas complejos, identificar vulnerabilidades lógicas y analizar aplicaciones desde una perspectiva técnica y crítica.

Es, en definitiva, un ejemplo de cómo la curiosidad puede transformar un juego minimalista en un laboratorio de aprendizaje.

---
