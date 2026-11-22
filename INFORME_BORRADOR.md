# SISTEMA DE GESTIÓN DE INFORMACIÓN PARA UN CENTRO MÉDICO

## Evidencia GA6-220501096-AA3-EV02 — Borrador de Informe Escrito

---

## 1. PORTADA ESTRUCTURADA

| Campo | Contenido |
|-------|-----------|
| **Institución** | SENA — Servicio Nacional de Aprendizaje |
| **Programa** | Análisis y Desarrollo de Software / Desarrollo de Aplicaciones Web |
| **Código de evidencia** | GA6-220501096-AA3-EV02 |
| **Título del proyecto** | Sistema de Gestión de Información para un Centro Médico |
| **Fase de entrega** | Maquetación de interfaces — HTML5 y CSS3 |
| **Autor** | [Nombre del aprendiz] |
| **Instructor** | [Nombre del instructor] |
| **Fecha de entrega** | [DD/MM/AAAA] |
| **Versión** | 1.0 |

---

## 2. INTRODUCCIÓN

El presente documento constituye el informe escrito de la evidencia GA6-220501096-AA3-EV02, correspondiente a la maquetación de las interfaces del "Sistema de Gestión de Información para un Centro Médico". El sistema tiene como propósito digitalizar y ordenar los procesos administrativos y clínicos de un centro de salud, permitiendo el registro y consulta de pacientes, médicos, empleados, citas médicas, consultorios, medicamentos y tratamientos.

El desarrollo se realizó utilizando tecnologías frontend estándar: HTML5 para la estructura semántica de las 11 pantallas y CSS3 para la guía visual, con un diseño basado en barra lateral fija y área de contenido principal.

---

## 3. OBJETIVOS

### Objetivo General
Diseñar y maquetar la interfaz gráfica de usuario (GUI) del Sistema de Gestión de Información para un Centro Médico, cubriendo los 8 procesos clave mediante 11 pantallas interconectadas con una guía visual uniforme.

### Objetivos Específicos
1. Establecer una paleta de colores institucional y tipografía consistente en todas las pantallas.
2. Implementar un layout con sidebar fijo de navegación y área de contenido principal.
3. Crear la pantalla de dashboard con resumen de métricas y accesos rápidos.
4. Maquetar el módulo de gestión de citas (consulta, registro y cancelación).
5. Maquetar los formularios de registro de personas (pacientes, médicos y empleados).
6. Maquetar los formularios de registro de recursos clínicos (consultorios, medicamentos y tratamientos).
7. Garantizar navegación bidireccional entre todas las pantallas mediante el menú lateral.
8. Aplicar principios de usabilidad y accesibilidad WCAG en el diseño de formularios y tablas.

---

## 4. DESCRIPCIÓN DEL CENTRO MÉDICO Y LOS 8 PROCESOS CLAVE

### Centro Médico
Institución de salud de nivel ambulatorio que brinda servicios de consulta médica general y especializada, programación de citas, dispensación de medicamentos y procedimientos de tratamiento.

### Los 8 Procesos Clave

| # | Proceso | Pantalla(s) asociada(s) |
|---|---------|------------------------|
| 1 | Gestión de Citas Médicas | `citas.html`, `registrar-cita.html`, `cancelar-cita.html` |
| 2 | Registro de Pacientes | `registrar-paciente.html` |
| 3 | Registro de Médicos | `registrar-medico.html` |
| 4 | Registro de Empleados | `registrar-empleado.html` |
| 5 | Registro de Consultorios | `registrar-consultorio.html` |
| 6 | Registro de Medicamentos | `registrar-medicamento.html` |
| 7 | Registro de Tratamientos | `registrar-tratamiento.html` |
| 8 | Panel de Control / Dashboard | `index.html` |

---

## 5. REQUISITOS FUNCIONALES Y PERFILES DE USUARIO

### Perfiles de Usuario

| Perfil | Descripción | Accesos principales |
|--------|-------------|---------------------|
| Recepción / Administración | Gestiona citas, pacientes y empleados | Todas las pantallas de registro y citas |
| Médico | Consulta su agenda de citas y pacientes asignados | `citas.html`, dashboard |
| Administrador del sistema | Configura consultorios, medicamentos y tratamientos | Formularios de recursos clínicos |

### Requisitos Funcionales

| ID | Requisito | Pantalla |
|----|-----------|----------|
| RF-01 | Visualizar resumen de métricas del centro | `index.html` |
| RF-02 | Consultar listado de citas con filtros | `citas.html` |
| RF-03 | Registrar nueva cita médica | `registrar-cita.html` |
| RF-04 | Cancelar cita con motivo justificado | `cancelar-cita.html` |
| RF-05 | Registrar datos de un paciente | `registrar-paciente.html` |
| RF-06 | Registrar datos de un médico | `registrar-medico.html` |
| RF-07 | Registrar datos de un empleado administrativo | `registrar-empleado.html` |
| RF-08 | Registrar consultorio con estado | `registrar-consultorio.html` |
| RF-09 | Registrar medicamento con stock inicial | `registrar-medicamento.html` |
| RF-10 | Registrar tratamiento con costo sugerido | `registrar-tratamiento.html` |

---

## 6. GUÍA VISUAL DEL SISTEMA

### Paleta de Colores (HEX)

| Componente | Color HEX | Uso |
|------------|-----------|-----|
| Color principal | `#1E3A5F` | Sidebar, encabezados, texto de valor en tarjetas |
| Color secundario/acento | `#4299E1` | Botones primarios, enlaces activos |
| Fondo general | `#F5F7FA` | Fondo del cuerpo (`body`) |
| Fondo tarjetas | `#FFFFFF` | Tarjetas de métricas, contenedores de formularios |
| Éxito | `#276749` | Estados positivos, iconos de confirmación |
| Advertencia | `#D69E2E` | Estados de advertencia |
| Error | `#C53030` | Botones de eliminación, estados de error, cancelaciones |

### Tipografía

- **Familia:** Arial, sans-serif
- **Tamaño base:** 16px
- **Títulos H1:** Tamaño relativo al base, negrita
- **Etiquetas de formulario:** `font-weight: 600`, bloque

### Componentes Visuales

| Componente | Clase CSS | Descripción |
|------------|-----------|-------------|
| Botón primario | `.btn-primario` | Fondo `#4299E1`, texto blanco |
| Botón secundario | `.btn-secundario` | Fondo gris claro, texto oscuro |
| Botón error/advertencia | `.btn-advertencia` | Fondo `#C53030`, texto blanco |
| Etiqueta | `label` | Bloque, negrita, color `#2D3748` |
| Tabla | `table` | Bordes colapsados, encabezado en color principal |
| Tarjeta métrica | `.tarjeta` | Fondo blanco, sombra suave, valor en color principal |
| Modal | `.modal` | Fondo oscuro semitransparente, contenido centrado |
| Layout | `.layout` | Flex con sidebar fijo (250px) y contenido principal |

---

## 7. MAPA GENERAL DE NAVEGACIÓN

```
                    +------------------+
                    |   index.html     |
                    |   Dashboard      |
                    +------------------+
                           |
    +----------------------+----------------------+
    |                      |                      |
+--v--+                +--v--+                +--v--+
|citas|                |paciente|             |medico |
|html |                |.html   |             |.html  |
+--v--+                +--v--+                +--v--+
   |                      |                      |
+--v--+                +--v--+                +--v--+
|registrar|         |registrar|         |registrar|
|-cita.html |         |-paciente|         |-medico|
+--v--+                +--v--+                +--v--+
   |                      |                      |
+--v--+                +--v--+                +--v--+
|cancelar-|         +--v--+                +--v--+
|-cita.html |         |empleado|         |consultorio|
+-----------+         |-html   |         |-html    |
                      +--v--+                +--v--+
                       |                      |
                      +--v--+                +--v--+
                      |medicamento|         |tratamiento|
                      |-html    |         |-html    |
                      +--v--+                +--v--+

Nota: Todas las pantallas incluyen el sidebar con enlaces a las 11 páginas del sistema.
```

### Flujo de navegación principal

1. **index.html** → Acceso rápido a "Registrar Cita" y "Registrar Paciente"
2. **citas.html** → Botón "+ Registrar Nueva Cita" → `registrar-cita.html`; fila de acciones → `cancelar-cita.html`
3. **registrar-cita.html** → Botón "Cancelar" → `citas.html`; modal éxito → `citas.html`
4. **cancelar-cita.html** → Botón "Volver" → `citas.html`; confirmación → `citas.html`
5. Todos los formularios de registro → Botón "Volver al Panel" / "Volver" → `index.html`

---

## 8. DESCRIPCIÓN DE LAS 11 PANTALLAS Y GUÍA DE CAPTURAS

A continuación se describe cada pantalla con la indicación exacta de qué captura de pantalla tomar y dónde pegarla en el informe.

### 8.1 index.html — Panel de Control Administrativo

**Descripción:** Pantalla de inicio con resumen de métricas y accesos rápidos.

**Elementos principales:**
- Sidebar con logo "Centro Médico" y menú de los 8 procesos
- Header con usuario "Recepción / Administración" y fecha actual
- H1: "Panel de Control Administrativo"
- 4 tarjetas: Citas del Día (12), Pacientes Registrados (145), Médicos Disponibles (8), Consultorios Activos (6)
- Botones: "Registrar Cita" (primario) y "Registrar Paciente" (secundario)

**Captura de pantalla requerida:**
- Tomar captura completa de `index.html` mostrando las 4 tarjetas de métricas y los botones de acceso rápido.
- **Pegar en:** Sección 8.1 del informe, bajo el título "Pantalla 1: Dashboard".

---

### 8.2 citas.html — Gestión de Citas Médicas

**Descripción:** Listado tabular de citas con filtro de búsqueda y botón de registro.

**Elementos principales:**
- Filtro de búsqueda por número de documento del paciente
- Botón "+ Registrar Nueva Cita" (redirige a `registrar-cita.html`)
- Tabla con columnas: Código, Paciente, Médico, Consultorio, Fecha/Hora, Estado, Acciones
- Acciones por fila: Editar y Cancelar

**Captura de pantalla requerida:**
- Tomar captura completa de `citas.html` mostrando la tabla con al menos 3 filas de datos y el filtro de búsqueda visible.
- **Pegar en:** Sección 8.2 del informe, bajo el título "Pantalla 2: Gestión de Citas".

---

### 8.3 registrar-cita.html — Registrar Nueva Cita

**Descripción:** Formulario para programar una cita médica con modal de confirmación.

**Elementos principales:**
- Campos: Paciente (desplegable), Médico, Consultorio, Fecha, Hora, Motivo de consulta
- Botón "Guardar Cita" (envía y muestra modal)
- Botón "Cancelar" (regresa a `citas.html`)
- Modal con mensaje "¡Cita registrada con éxito!" y botón Aceptar

**Captura de pantalla requerida:**
- Tomar captura de `registrar-cita.html` mostrando el formulario completo y el modal de éxito abierto (activar modal con JavaScript o editar para mostrarlo).
- **Pegar en:** Sección 8.3 del informe, bajo el título "Pantalla 3: Registrar Cita".

---

### 8.4 cancelar-cita.html — Cancelar Cita Médica

**Descripción:** Formulario para cancelar una cita activa por documento del paciente.

**Elementos principales:**
- Campo de texto: Número de documento del paciente
- Campo obligatorio: Motivo de la cancelación (textarea)
- Botón "Confirmar Cancelación" (color error #C53030)
- Botón "Volver" (regresa a `citas.html`)
- Modal de confirmación antes de cancelar

**Captura de pantalla requerida:**
- Tomar captura de `cancelar-cita.html` mostrando el formulario con el campo de motivo y el botón de confirmación.
- **Pegar en:** Sección 8.4 del informe, bajo el título "Pantalla 4: Cancelar Cita".

---

### 8.5 registrar-paciente.html — Registro de Pacientes

**Descripción:** Formulario para registrar datos personales de un paciente.

**Elementos principales:**
- Campos: Tipo de Documento, Número de Documento, Nombres, Apellidos, Fecha de Nacimiento, Teléfono, Correo Electrónico, Dirección
- Botones: "Guardar Paciente" y "Limpiar Formulario"

**Captura de pantalla requerida:**
- Tomar captura completa de `registrar-paciente.html` mostrando todos los campos del formulario.
- **Pegar en:** Sección 8.5 del informe, bajo el título "Pantalla 5: Registro de Pacientes".

---

### 8.6 registrar-medico.html — Registro de Médicos

**Descripción:** Formulario para registrar datos del cuerpo médico.

**Elementos principales:**
- Campos: Documento, Nombres, Apellidos, Registro Médico/Tarjeta Profesional, Especialidad, Teléfono, Correo, Consultorio Asignado
- Botones: "Guardar Médico" y "Volver al Panel"

**Captura de pantalla requerida:**
- Tomar captura completa de `registrar-medico.html` mostrando todos los campos del formulario.
- **Pegar en:** Sección 8.6 del informe, bajo el título "Pantalla 6: Registro de Médicos".

---

### 8.7 registrar-empleado.html — Registro de Empleados

**Descripción:** Formulario para registrar personal administrativo.

**Elementos principales:**
- Campos: Documento, Nombres, Apellidos, Cargo Administrativo (Recepción/Facturación/Servicios), Teléfono, Turno de Trabajo (Mañana/Tarde/Noche)
- Botones: "Guardar Empleado" y "Volver"

**Captura de pantalla requerida:**
- Tomar captura completa de `registrar-empleado.html` mostrando todos los campos del formulario.
- **Pegar en:** Sección 8.7 del informe, bajo el título "Pantalla 7: Registro de Empleados".

---

### 8.8 registrar-consultorio.html — Registro de Consultorios

**Descripción:** Formulario para registrar consultorios médicos.

**Elementos principales:**
- Campos: Número/Código de Consultorio, Ubicación/Piso, Especialidad Asignada, Estado (Disponible/Mantenimiento)
- Botón: "Guardar Consultorio"

**Captura de pantalla requerida:**
- Tomar captura completa de `registrar-consultorio.html` mostrando todos los campos del formulario.
- **Pegar en:** Sección 8.8 del informe, bajo el título "Pantalla 8: Registro de Consultorios".

---

### 8.9 registrar-medicamento.html — Registro de Medicamentos

**Descripción:** Formulario para registrar medicamentos en el inventario.

**Elementos principales:**
- Campos: Nombre Comercial, Principio Activo, Presentación (Tabletas/Jarabe/Inyectable), Concentración, Stock Inicial
- Botón: "Guardar Medicamento"

**Captura de pantalla requerida:**
- Tomar captura completa de `registrar-medicamento.html` mostrando todos los campos del formulario.
- **Pegar en:** Sección 8.9 del informe, bajo el título "Pantalla 9: Registro de Medicamentos".

---

### 8.10 registrar-tratamiento.html — Registro de Tratamientos

**Descripción:** Formulario para registrar tratamientos médicos.

**Elementos principales:**
- Campos: Nombre del Tratamiento, Descripción del Procedimiento, Duración Estimada, Costo Sugerido
- Botón: "Guardar Tratamiento"

**Captura de pantalla requerida:**
- Tomar captura completa de `registrar-tratamiento.html` mostrando todos los campos del formulario.
- **Pegar en:** Sección 8.10 del informe, bajo el título "Pantalla 10: Registro de Tratamientos".

---

### 8.11 Resumen de Capturas por Pantalla

| Pantalla | Archivo | Qué capturar | Dónde pegar |
|----------|---------|--------------|-------------|
| 1 | `index.html` | Dashboard con 4 tarjetas de métricas | Sección 8.1 |
| 2 | `citas.html` | Tabla de citas + filtro de búsqueda | Sección 8.2 |
| 3 | `registrar-cita.html` | Formulario + modal de éxito abierto | Sección 8.3 |
| 4 | `cancelar-cita.html` | Formulario + campo motivo de cancelación | Sección 8.4 |
| 5 | `registrar-paciente.html` | Formulario completo (8 campos) | Sección 8.5 |
| 6 | `registrar-medico.html` | Formulario completo (8 campos) | Sección 8.6 |
| 7 | `registrar-empleado.html` | Formulario completo (6 campos) | Sección 8.7 |
| 8 | `registrar-consultorio.html` | Formulario completo (4 campos) | Sección 8.8 |
| 9 | `registrar-medicamento.html` | Formulario completo (5 campos) | Sección 8.9 |
| 10 | `registrar-tratamiento.html` | Formulario completo (4 campos) | Sección 8.10 |

---

## 9. LISTA DE CHEQUEO DE USABILIDAD Y ACCESIBILIDAD WCAG

| Criterio | Estado | Observación |
|----------|--------|-------------|
| Etiquetas `<label>` asociadas a cada input | ✅ | Todos los formularios incluyen `<label>` |
| Contrast ratio mínimo 4.5:1 en texto normal | ✅ | Colores institucional sobre fondos claros |
| Navegación por teclado (Tab) | ✅ | Elementos focables en orden lógico |
| Texto alternativo en imágenes | ⚠️ | No hay imágenes; logo es texto |
| Títulos jerárquicos (H1, H2, H3) | ✅ | H1 por pantalla, H3 en tarjetas |
| Mensajes de error claros | ⚠️ | Validación nativa del navegador (HTML5 required) |
| Estados de boton (hover, focus) | ✅ | Transiciones CSS en botones |
| Formularios con validación obligatoria | ✅ | Atributo `required` en campos críticos |
| Idioma del documento declarado | ✅ | `<html lang="es">` |
| Viewport móvil configurado | ✅ | `<meta name="viewport">` |

---

## 10. CONCLUSIONES Y REFERENCIAS

### Conclusiones

Se ha completado la maquetación de las 11 pantallas del Sistema de Gestión de Información para un Centro Médico, cubriendo los 8 procesos clave definidos. El sistema cuenta con una guía visual uniforme basada en la paleta institucional (#1E3A5F, #4299E1, #F5F7FA), tipografía Arial y componentes reutilizables (botones, tarjetas, tablas, modales). Todas las pantallas comparten el layout con sidebar de navegación y header, garantizando consistencia y navegabilidad entre módulos.

### Referencias

1. SENA — Guía de evidencia GA6-220501096-AA3-EV02
2. W3C — HTML5 Specification. https://www.w3.org/TR/html52/
3. W3C — CSS3 Specification. https://www.w3.org/Style/CSS/
4. WCAG 2.1 — Web Content Accessibility Guidelines. https://www.w3.org/WAI/WCAG21/quickref/
5. MDN Web Docs — HTML y CSS reference. https://developer.mozilla.org/

---

**Fin del borrador del informe escrito.**

*Nota: Reemplazar los campos entre corchetes [] con la información real del aprendiz, instructor y fecha antes de entregar el documento final en formato Word o PDF.*