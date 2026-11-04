# Checklist de revisión — Entrega 4

| Campo          | Valor                                                                                                                                                                                                        |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Entrega        | 4 — Acceso, administración y tienda                                                                                                                                                                          |
| Fecha Revisión | Miércoles 4 de noviembre de 2026                                                                                                                                                                             |
| Nota           | Entrega 4, que pondera 35 % de la EVA 3                                                                                                                                                                      |
| Orden          | Por aplicación: web, app Android, backend / repositorio; al final, adicionales por problemáticas                                                                                                             |
| Base           | [Planificación, entrega 4](planificacion.md#entrega-4--acceso-administración-y-tienda), [requisitos base](requerimientos-base.md), [ficha de proyecto](ficha-proyecto.md), [problemáticas](problematicas.md) |

Cada ítem se marca **cumple** o **no cumple**. No hay puntaje intermedio.

## Premisas

1. **El administrador de plataforma usa solo la web**, no la app. Está en la [ficha de proyecto](ficha-proyecto.md#4-actores-y-perfiles-de-usuario): canal del administrador = Web. En la app no debe haber panel de administración de plataforma.
2. **La emprendedora escribe la ficha de su tienda en la app** (RF-TIE-01). En esta entrega la web debe **mostrar** esa ficha. Editarla desde la web es de la entrega 6 (RF-TIE-02).
3. **Cómo se clasifica un ítem**

- **Obligatorio:** todo lo que viene de los [requisitos base](requerimientos-base.md) (Esencial o Importante) y entra en el alcance de esta revisión (acceso, administración, tienda, reglas, capa de datos y reglas comunes de entrega), más lo que fija la ficha o los entregables de la entrega 4. Si falta, resta.
- **Adicional** (solo estas tres vías; si está, suma; si no, no resta):

1. Requisito o capacidad **de otra entrega** (incluido un Esencial o Importante que la planificación deja para después).
2. Un **plus** sobre algo que ya es obligatorio (más cómodo, más pulido, no un RF distinto).
3. Una **mitigación de** [problemáticas](problematicas.md) **que el grupo implementó y que no está cubierta por un RF/RNF** de los requisitos base.
4. No se usa “es Importante” como motivo para dejar un requisito base en adicionales.

## Cómo se calcula la nota

Se parte de **7,0**.

| Tipo                 | Efecto                    |
| -------------------- | ------------------------- |
| Obligatorio en fallo | Resta **1 décima** (−0,1) |
| Adicional cumplido   | Suma **1 décima** (+0,1)  |

**Nota = 7,0 − 0,1 × (obligatorios en fallo) + 0,1 × (adicionales cumplidos)**

Tope **7,0**. Piso **1,0**.

Los adicionales solo suman si se demostraron en la revisión. Pueden recuperar décimas hasta el tope 7,0, no más.

Ejemplo: 8 obligatorios en fallo y 3 adicionales cumplidos → 7,0 − 0,8 + 0,3 = **6,5**.

---

## 1. Web

Canal de administración de la plataforma, acceso de emprendedora y comprador, y lectura pública de lo ya guardado.

### 1.1 Obligatorios — web

| ID  | Ítem                                                                                                                       | Sustento                            |
| --- | -------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| W01 | El administrador inicia sesión en la web.                                                                                  | Ficha §4; RNF-SEG-01                |
| W02 | Tras iniciar sesión, el administrador llega a la administración de la plataforma (cuentas, asociaciones o catálogos).      | Entrega 4, entregable 3             |
| W03 | No existe (o no es usable) un panel de administración de plataforma en la app: la operación del administrador es solo web. | Ficha §4, canal Web                 |
| W04 | El administrador crea una cuenta de emprendedora.                                                                          | RF-ADM-01                           |
| W05 | Quedan definidas las credenciales (usuario y contraseña) para entregárselas a la emprendedora.                             | RF-ADM-01                           |
| W06 | El administrador edita un dato de esa cuenta (por ejemplo el nombre o el correo de contacto).                              | RF-ADM-01                           |
| W07 | Tras editar, el cambio se conserva al recargar la página.                                                                  | RF-ADM-01                           |
| W08 | El administrador desactiva la cuenta de emprendedora.                                                                      | RF-ADM-01                           |
| W09 | Con la cuenta desactivada, el ingreso con esas credenciales es rechazado en la web.                                        | RF-ADM-01; RNF-SEG-01               |
| W10 | El administrador crea una asociación.                                                                                      | RF-ASO-01                           |
| W11 | La ficha de la asociación guarda el nombre.                                                                                | RF-ASO-01                           |
| W12 | La ficha de la asociación guarda el logo.                                                                                  | RF-ASO-01                           |
| W13 | La ficha de la asociación guarda la descripción.                                                                           | RF-ASO-01                           |
| W14 | La ficha de la asociación guarda el sector.                                                                                | RF-ASO-01                           |
| W15 | La ficha de la asociación guarda el contacto.                                                                              | RF-ASO-01                           |
| W16 | El administrador edita la asociación y el cambio se conserva.                                                              | RF-ASO-01                           |
| W17 | El administrador desactiva la asociación.                                                                                  | RF-ASO-01                           |
| W18 | El administrador asigna una emprendedora a una asociación.                                                                 | RF-ASO-02                           |
| W19 | El administrador quita a esa emprendedora de la asociación.                                                                | RF-ASO-02                           |
| W20 | El administrador crea o edita un tipo de emprendimiento.                                                                   | RF-ADM-03                           |
| W21 | El administrador crea o edita un tipo de producto.                                                                         | RF-ADM-03                           |
| W22 | El administrador crea o edita una categoría.                                                                               | RF-ADM-03                           |
| W23 | El administrador gestiona otras cuentas de administrador (crear, editar o desactivar).                                     | RF-ADM-04                           |
| W24 | Listados de administración con búsqueda o filtro (cuentas, asociaciones o catálogos).                                      | RNF-OPE-01                          |
| W25 | La emprendedora inicia sesión en la web con las credenciales creadas por el administrador.                                 | RF-ACC-01                           |
| W26 | La emprendedora cierra sesión en la web.                                                                                   | RF-ACC-09                           |
| W27 | Emprendedora o comprador con correo y contraseña pueden recuperar su contraseña.                                           | RF-ACC-10                           |
| W28 | El comprador inicia sesión en la web con Google.                                                                           | RF-ACC-04                           |
| W29 | El comprador se registra en la web con correo y contraseña.                                                                | RF-ACC-04                           |
| W30 | El comprador inicia sesión en la web con ese correo y contraseña.                                                          | RF-ACC-04                           |
| W31 | El comprador cierra sesión en la web.                                                                                      | RF-ACC-09                           |
| W32 | Un visitante recorre al menos una pantalla pública de la web sin iniciar sesión.                                           | RF-ACC-07                           |
| W33 | La web muestra el nombre de la tienda tal como lo guardó la emprendedora en la app.                                        | RF-TIE-01; criterio de aceptación 2 |
| W34 | La web muestra el logo o la foto de la tienda.                                                                             | RF-TIE-01                           |
| W35 | La web muestra la descripción de la tienda.                                                                                | RF-TIE-01                           |
| W36 | La web muestra el tipo de emprendimiento de la tienda.                                                                     | RF-TIE-01                           |
| W37 | La web muestra el sector de la tienda.                                                                                     | RF-TIE-01                           |
| W38 | La web muestra los datos de contacto de la tienda.                                                                         | RF-TIE-01                           |
| W39 | La interfaz de la web está en español de Chile.                                                                            | RNF-IDI-01                          |
| W40 | Las pantallas de la web no consultan Firestore de forma directa: el acceso pasa por repositorios (capa de datos).          | RNF-DAT-02                          |

**Subtotal obligatorios web: 40**

### 1.2 Adicionales — web

Solo **otra entrega** o **plus**. No restan.

| ID  | Ítem                                                                                                                       | Tipo         | Motivo                                                                         |
| --- | -------------------------------------------------------------------------------------------------------------------------- | ------------ | ------------------------------------------------------------------------------ |
| WA1 | La emprendedora edita la ficha de su tienda también desde la web.                                                          | Otra entrega | RF-TIE-02; planificación, entrega 6.                                           |
| WA2 | La web se ve usable en el navegador del teléfono (administración o ficha sin romper el layout).                            | Otra entrega | RNF-CPT-02; planificación, entrega 6.                                          |
| WA3 | Las acciones del administrador sobre cuentas o asociaciones quedan registradas (quién, qué, cuándo) y se pueden consultar. | Otra entrega | RNF-SEG-07; contenido de seguridad en entrega 5 (o 8).                         |
| WA4 | Confirmación explícita antes de desactivar una cuenta o una asociación.                                                    | Plus         | Desactivar (W08, W17) ya es obligatorio.                                       |
| WA5 | Las credenciales de una emprendedora nueva se pueden copiar o enviar sin anotarlas a mano.                                 | Plus         | Que existan (W05) ya es obligatorio.                                           |
| WA6 | Tras desactivar una asociación, deja de mostrarse como activa donde el grupo ya exponga asociaciones.                      | Plus         | Desactivar (W17) ya es obligatorio; la vitrina pública completa es de después. |

**Subtotal adicionales web: 6**

---

## 2. App Android

Acceso de emprendedora y comprador, y escritura de la ficha de la tienda. Sin administración de plataforma.

### 2.1 Obligatorios — app

| ID  | Ítem                                                                                                                                                                       | Sustento                            |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| A01 | Desde la primera pantalla se distingue el modo comprador del modo emprendedora.                                                                                            | RF-ACC-05                           |
| A02 | La emprendedora inicia sesión en la app con las credenciales creadas en la web.                                                                                            | RF-ACC-01                           |
| A03 | Credenciales incorrectas son rechazadas (no abre sesión).                                                                                                                  | RF-ACC-01; RNF-SEG-01               |
| A04 | Tras el primer ingreso, la emprendedora puede activar el acceso con huella.                                                                                                | RF-ACC-02                           |
| A05 | Con la huella activada, el ingreso siguiente es solo con la huella (sin volver a escribir la contraseña).                                                                  | RF-ACC-02; criterio de aceptación 1 |
| A06 | La huella usa la API biométrica del sistema; la app no almacena datos biométricos.                                                                                         | RNF-SEG-02                          |
| A07 | La emprendedora puede desactivar la huella.                                                                                                                                | RF-ACC-02                           |
| A08 | Tras desactivar la huella, el ingreso vuelve a pedir usuario y contraseña.                                                                                                 | RF-ACC-02                           |
| A09 | El comprador inicia sesión en la app con Google.                                                                                                                           | RF-ACC-03                           |
| A10 | En la app, el comprador no tiene como vía principal el correo y contraseña (solo Google).                                                                                  | RF-ACC-03; RN-07                    |
| A11 | La emprendedora cierra sesión en la app.                                                                                                                                   | RF-ACC-09                           |
| A12 | El comprador cierra sesión en la app.                                                                                                                                      | RF-ACC-09                           |
| A13 | Con la cuenta desactivada en la web (W08), el ingreso en la app también es rechazado.                                                                                      | RF-ADM-01; RNF-SEG-01               |
| A14 | La emprendedora edita el nombre de su tienda.                                                                                                                              | RF-TIE-01                           |
| A15 | La emprendedora edita la descripción de su tienda.                                                                                                                         | RF-TIE-01                           |
| A16 | La emprendedora elige el tipo de emprendimiento de su tienda.                                                                                                              | RF-TIE-01                           |
| A17 | La emprendedora elige el sector de Puerto Montt de su tienda.                                                                                                              | RF-TIE-01                           |
| A18 | La emprendedora edita los datos de contacto de su tienda.                                                                                                                  | RF-TIE-01                           |
| A19 | La emprendedora sube la foto o el logo de su tienda.                                                                                                                       | RF-TIE-01                           |
| A20 | Tras cerrar la app por completo y volver a abrirla, los datos de texto de la tienda se conservan.                                                                          | RF-TIE-01; criterio de aceptación 2 |
| A21 | Tras cerrar y volver a abrir, el logo o la foto se conserva.                                                                                                               | RF-TIE-01                           |
| A22 | La interfaz de la app está en español de Chile.                                                                                                                            | RNF-IDI-01                          |
| A23 | Las pantallas de la app no consultan Firestore de forma directa: el acceso pasa por repositorios.                                                                          | RNF-DAT-02                          |
| A24 | En los flujos de emprendedora revisados, el lenguaje es simple y los íconos van acompañados de texto (un objetivo por pantalla o confirmaciones claras donde corresponda). | RNF-USA-01                          |
| A25 | Los elementos táctiles principales del flujo de acceso y tienda tienen tamaño mínimo de 48 dp.                                                                             | RNF-USA-02                          |
| A26 | La app respeta el tamaño de texto del sistema en las pantallas de acceso y tienda sin romper el layout.                                                                    | RNF-USA-03                          |

**Subtotal obligatorios app: 26**

### 2.2 Adicionales — app

Solo **otra entrega** o **plus**. No restan.

| ID  | Ítem                                                                                         | Tipo         | Motivo                                                          |
| --- | -------------------------------------------------------------------------------------------- | ------------ | --------------------------------------------------------------- |
| AA1 | Compresión de la imagen del logo antes de subirla.                                           | Otra entrega | RNF-REN-01; planificación, entrega 5.                           |
| AA2 | Mensaje claro cuando falla el ingreso (credenciales, red o Google).                          | Plus         | El rechazo (A03) ya es obligatorio.                             |
| AA3 | La huella se demuestra en dispositivo real (no solo emulador).                               | Plus         | Activar, reingresar y desactivar (A04–A08) ya son obligatorios. |
| AA4 | La emprendedora ve en la app a qué asociación(es) la asignó el administrador (solo lectura). | Plus         | Asignar y quitar en la web (W18–W19) ya son obligatorios.       |

**Subtotal adicionales app: 4**

---

## 3. Backend y repositorio

Aplica a ambos clientes: reglas, modelo, datos de prueba y forma de entregar.

### 3.1 Obligatorios — backend y repositorio

| ID  | Ítem                                                                                                                               | Sustento                             |
| --- | ---------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------ |
| B01 | Las reglas de seguridad de Firestore están publicadas.                                                                             | Entrega 4, entregable 5; RNF-SEG-01  |
| B02 | Las reglas de seguridad de Storage están publicadas.                                                                               | Entrega 4, entregable 5; RNF-SEG-01  |
| B03 | Una emprendedora no puede modificar la tienda de otra (simulador de reglas o segunda cuenta).                                      | RNF-SEG-01; criterio de aceptación 3 |
| B04 | Una emprendedora no puede escribir archivos de Storage de otra tienda.                                                             | RNF-SEG-01                           |
| B05 | Solo el administrador puede crear o desactivar cuentas de emprendedora.                                                            | RNF-SEG-01; RF-ADM-01                |
| B06 | Solo el administrador puede crear o desactivar asociaciones.                                                                       | RNF-SEG-01; RF-ASO-01                |
| B07 | Solo el administrador puede mantener tipos de emprendimiento, tipos de producto y categorías.                                      | RNF-SEG-01; RF-ADM-03                |
| B08 | Presentan el modelo de Firestore: colecciones, documentos y relaciones.                                                            | RNF-DAT-01                           |
| B09 | El modelo incluye o justifica los índices que usan.                                                                                | RNF-DAT-01                           |
| B10 | El modelo presentado coincide con lo que se ve en la consola de Firebase durante la demo.                                          | Criterio de aceptación 4             |
| B11 | Existe un procedimiento documentado para cargar datos de prueba ficticios en el proyecto de desarrollo.                            | RNF-DAT-04                           |
| B12 | El procedimiento (o el README) deja claro un proyecto de Firebase de desarrollo separado del de producción.                        | RNF-DAT-04                           |
| B13 | Demuestran lectura y escritura reales por perfil (administrador, emprendedora y, al menos, comprador o visitante) contra Firebase. | Entrega 4, contenido evaluado        |
| B14 | Credenciales, claves de API y archivos sensibles no están en el repositorio.                                                       | RNF-SEG-03                           |
| B15 | README con pasos para ejecutar la app y la web.                                                                                    | RNF-MAN-01                           |
| B16 | La app está en Kotlin con Android Studio y hay arquitectura en capas documentada (dónde viven los repositorios).                   | RNF-MAN-01                           |
| B17 | La entrega está marcada con la etiqueta `entrega-4` (o la acordada) sobre el commit revisado.                                      | Reglas comunes; RNF-MAN-04           |
| B18 | El historial del repositorio muestra contribución de los integrantes del grupo.                                                    | RNF-MAN-04                           |
| B19 | Hay un informe breve en `docs/` con lo realizado, requisitos cubiertos, pendiente y reparto de trabajo.                            | Reglas comunes de la planificación   |
| B20 | Los requisitos o tareas de esta entrega están como _issues_, enlazados desde los _pull requests_ que los resuelven.                | RNF-MAN-05                           |

**Subtotal obligatorios backend: 20**

### 3.2 Adicionales — backend y repositorio

Solo **plus**. No restan.

| ID  | Ítem                                                                              | Tipo | Motivo                                                                      |
| --- | --------------------------------------------------------------------------------- | ---- | --------------------------------------------------------------------------- |
| BA1 | Justificación escrita del modelo (por qué esas colecciones), además del diagrama. | Plus | Presentar el modelo y que calce con la consola (B08–B10) ya es obligatorio. |

**Subtotal adicionales backend: 1**

---

## 4. Adicionales por problemáticas (sin RF/RNF propio)

Mitigaciones de [problematicas.md](problematicas.md) que el grupo **demostró** en acceso, administración o tienda, y que **no** están ya cubiertas por un requisito base. Cada una cumplida suma **+0,1**. No restan.

Si la medida es exactamente un RF/RNF (por ejemplo solo “íconos con texto” = RNF-USA-01), no cuenta aquí: eso ya es obligatorio.

| ID   | Ítem (ejemplos de lo que sí suma)                                                                                                                                                                       | Problemática | Por qué no es requisito base                                                                                          |
| ---- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------- |
| P01a | Al subir el logo o foto de la tienda, hay guía concreta (luz, encuadre, fondo) o una ayuda que mejore la foto **sin** depender de IA.                                                                   | P01          | No hay RF de tips o asistencia de foto de tienda; RF-IA-01 es de producto y está condicionado.                        |
| P02a | Ayuda a redactar la descripción de la tienda (plantilla, ejemplos o dictado) **sin** depender de IA.                                                                                                    | P02          | No hay RF de plantillas de descripción de tienda.                                                                     |
| P04a | La ficha de tienda en la web, abierta desde el teléfono sin instalar la app, se entiende sola (qué vende y cómo contactar) más allá del mínimo de W33–W38.                                              | P04          | Compartir/QR y vitrina completa son de entregas posteriores; aquí solo cuenta un plus demostrable en la ficha actual. |
| P05a | Vista previa o confirmación clara antes de dejar la tienda visible, de modo que publicar no se sienta irreversible.                                                                                     | P05          | RNF-USA-01 pide confirmaciones; esto es una mitigación específica de “miedo a publicar” en la ficha de tienda.        |
| P08a | Vocabulario y flujo de acceso/tienda sin jerga técnica, comprobado con una persona poco habituada (o evidencia equivalente del grupo).                                                                  | P08          | Más allá de RNF-USA-01/02/03 ya obligatorios.                                                                         |
| P09a | Desde la ficha de tienda, un camino simple para llevar el enlace o el aviso a WhatsApp/redes **que no sea** solo el RF-COM-01 de entregas posteriores (si aún no lo tienen, puede ser un atajo propio). | P09          | RF-COM-01 es de otra entrega; cuenta si resolvieron parte de P09 sin ese entregable.                                  |
| Pxx  | Cualquier otra mitigación demostrable de P01–P09 en acceso, administración o tienda, **no** cubierta por un RF/RNF.                                                                                     | P01–P09      | Abierto: el grupo indica la problemática y muestra la función.                                                        |

**Cómo anotar Pxx:** en la hoja del grupo escribir, por ejemplo, `P03a: acceso offline a ficha de tienda` — solo si no existe ya como RNF-DAT-03 u otro requisito (RNF-DAT-03 es de catálogo en la entrega 5).

**Subtotal adicionales por problemáticas:** según lo demostrado (hasta 7 en la tabla de ejemplos; Pxx puede agregar más, con tope de nota 7,0).

---

## Totales

| Bloque                        | Obligatorios | Adicionales            |
| ----------------------------- | ------------ | ---------------------- |
| 1. Web                        | 40           | 6                      |
| 2. App Android                | 26           | 4                      |
| 3. Backend y repositorio      | 20           | 1                      |
| 4. Problemáticas (sin RF/RNF) | —            | según demo             |
| **Total fijo**                | **86**       | **11 + problemáticas** |

Máximo descuento por obligatorios: la nota queda en el piso **1,0**.  
Los adicionales (otra entrega, plus y problemáticas) solo suben hasta el tope **7,0**.

---

## Orden sugerido en la demo

1. **Web, administrador:** W01–W24.
2. **App, emprendedora:** A01–A08, A14–A21, A24–A26, A11.
3. **Web, lectura y otros perfiles:** W33–W38, W25–W32, W39–W40.
4. **App, comprador y desactivación:** A09–A10, A12; luego W08–W09 y A13.
5. **Backend:** B01–B20 con la consola a la vista.
6. **Adicionales** si el grupo los ofrece: WA*, AA*, BA*, y mitigaciones P*.

---

## Hoja por grupo

Anotar fallos obligatorios (F) y adicionales cumplidos (+).  
**Nota = 7,0 − 0,1×F + 0,1×(+)** , acotada entre 1,0 y 7,0.

| Bloque            | Grupo |
| ----------------- | ----- |
| Web (W / WA)      | /     |
| App (A / AA)      | /     |
| Backend (B / BA)  | /     |
| Problemáticas (P) | — /   |
| **Total F**       |       |
| **Total +**       |       |
| **Nota**          |       |
