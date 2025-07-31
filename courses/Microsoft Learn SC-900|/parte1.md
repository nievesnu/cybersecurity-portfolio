# Introducción a los conceptos de seguridad, cumplimiento e identidad

## Capas de seguridad

Entre las capas de seguridad de ejemplo se pueden incluir:

* **Seguridad física**: limitar el acceso a un centro de datos solo al personal autorizado.
* **Controles de seguridad de identidad y acceso**: como la **autenticación multifactor (MFA)** o el **acceso basado en condiciones**, para controlar la infraestructura y el control de cambios.
* **Seguridad perimetral de red**: incluye protección contra ataques DDoS.
* **Seguridad de red**: segmentación y controles de acceso para limitar la comunicación entre recursos.
* **Seguridad de la capa de proceso**: proteger acceso a máquinas locales o en la nube, cerrando puertos.
* **Seguridad de la capa de aplicación**: asegurar que las aplicaciones estén libres de vulnerabilidades.
* **Seguridad de la capa de datos**: controlar el acceso y cifrar datos empresariales y de clientes.

---

## Modelo CIA: **Confidencialidad, Integridad, Disponibilidad**

---

## Modelo de **Confianza Cero (Zero Trust)**

**Supone que toda red es abierta y no confiable.**
**Principio clave**: *"No confíes en nadie, comprueba todo."*

### Principios rectores:

1. **Comprobación explícita**: autenticación y autorización basadas en identidad, ubicación, dispositivo, datos, etc.
2. **Acceso con privilegios mínimos**: JIT, JEA, políticas adaptativas y protección de datos.
3. **Asunción de infracción**: segmentación, cifrado, análisis y acciones defensivas ante amenazas.


## Seis pilares fundamentales del modelo Zero Trust:

1. **Identidades**: usuarios, servicios o dispositivos deben autenticarse y seguir el principio de menor privilegio.
2. **Dispositivos**: supervisar su estado y cumplimiento.
3. **Aplicaciones**: detectar Shadow IT, controlar permisos y accesos.
4. **Datos**: deben clasificarse, etiquetarse y cifrarse.
5. **Infraestructura**: evaluar configuración, acceso JIT, telemetría, bloqueo automático.
6. **Redes**: segmentación, microsegmentación, cifrado E2E, supervisión y análisis en tiempo real.

---

## Cifrado y código hash

### **Cifrado**

Proceso de hacer que los datos sean ilegibles sin la clave secreta.
**Tipos:**

* **Simétrico**: misma clave para cifrar y descifrar.
* **Asimétrico**: par de claves (pública y privada).

### **Cifrado de datos en reposo**

Datos almacenados físicamente.
**Ejemplo**: si un atacante accede a un disco cifrado sin la clave, **no podrá leer los datos.**

### **Cifrado de datos en tránsito**

Datos en movimiento (por Internet o redes privadas).
**Ejemplo**: uso de **HTTPS**.
**Protege frente a observadores externos**.

### **Cifrado de datos en uso**

Protección de datos en memoria volátil (**RAM, CPU**).
**Ejemplo**: enclaves protegidos en la CPU.

### **Algoritmo Hash**

* **Hash**: valor de longitud fija único.
* **No es cifrado**: no se puede revertir.
* **Uso común**: almacenamiento de contraseñas.

**Salting**: agregar un valor aleatorio al texto antes de aplicar el hash → dificulta ataques de diccionario.

---

## Conceptos de **Gobernanza, Riesgo y Cumplimiento (GRC)**

### **Gobernanza**

Conjunto de reglas y procesos para dirigir y controlar una organización.
**Ejemplo**: políticas de acceso, privilegios administrativos, etc.

![Gobernanza](https://github.com/user-attachments/assets/f2c55c42-022e-475d-a7f7-63adf627efe4)

### **Riesgo**

Evaluación y respuesta ante amenazas (internas o externas).

* **Externos**: clima, pandemias, ciberataques.
* **Internos**: filtraciones, fraude, acceso no autorizado.

### **Cumplimiento normativo**

Cumplimiento de leyes, regulaciones nacionales e internacionales.

**Cumplimiento no equivale a seguridad**, pero la seguridad forma parte del cumplimiento.

#### Conceptos clave de cumplimiento:

* **Residencia de datos**: lugar físico donde se almacenan los datos.
* **Soberanía de datos**: sujeción de los datos a las leyes del lugar de recogida o almacenamiento.
* **Privacidad de los datos**: transparencia en recopilación, uso y compartición de datos personales.


> Todas las organizaciones deben **comprender y aplicar correctamente los conceptos de cumplimiento**, ya que están obligadas a **cumplir estándares mínimos legales.**


### Resultado evaluacion:

![Resultado](https://github.com/user-attachments/assets/31735f6d-0278-4e99-bf3b-715bda27e541)
