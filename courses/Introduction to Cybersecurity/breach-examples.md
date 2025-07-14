## Caso 1: Brecha de datos de Qantas (julio 2025)

### What was taken?
- Datos personales de ~5,7 millones de clientes: nombres, emails, teléfonos, fechas de nacimiento y direcciones (~1,7 M registros más sensibles).

### What exploit did attackers use?
- Acceso a una plataforma de atención al cliente de terceros en Filipinas mediante ingeniería social. Posible grupo implicado: "Scattered Spider".

### Actions recommended to prevent recurrence:
- Revisar y reforzar seguridad de tercerizados (acceso remoto, concienciación).
- Aplicar autenticación multifactor (MFA).
- Monitorizar actividad anómala en plataformas externas.
- Implementar formación continua y auditorías de seguridad en proveedores.

---

## Caso 2: TalentHook – Contenedor Azure mal configurado

### What was taken?
- ~26 millones de CVs expuestos: nombres, emails, historial profesional y educativo.

### What exploit did attackers use?
- Configuración pública de un Azure Blob Storage sin restricciones de acceso.

### Actions recommended to prevent recurrence:
- Revisar configuraciones de almacenamiento en la nube (no exponer contenedores).
- Implementar políticas de acceso mínimo y control RBAC.
- Auditorías periódicas de entornos y monitorización de logs.

---

## Caso 3: Mega filtración de credenciales (Cybernews)

### What was taken?
- 16 000 millones de credenciales (usuarios/contraseñas) recientes recopiladas por infostealers.

### What exploit did attackers use?
- Malware tipo infostealer que extrajo credenciales directamente de dispositivos infectados.

### Actions recommended to prevent recurrence:
- Forzar políticas de contraseñas robustas y únicas.
- Implementar MFA siempre que sea posible.
- Detectar usos de credenciales via Threat Detection y monitorización del dark web.
