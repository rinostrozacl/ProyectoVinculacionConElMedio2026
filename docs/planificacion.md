# Planificación de entregas — Emprendedores Puerto Montt

| Campo | Valor |
|-------|-------|
| Versión | 1.2 |
| Fecha | 2026-10-05 |
| Período | 5 de octubre al 23 de noviembre de 2026 |
| Entregas | 8 (los lunes, salvo la entrega 2, que se presenta en la visita a terreno) |
| Entrega final | Lunes 23 de noviembre de 2026 |

Base: [ficha de proyecto v1.1](ficha-proyecto.md), [requisitos base](requerimientos-base.md) y [pauta de levantamiento](pauta-levantamiento.md).

---

## 1. Calendario de entregas

| N.º | Fecha | Entrega | Nota |
|-----|-------|---------|------|
| 1 | Lunes 5 de octubre | Diseño conceptual | EVA 2 |
| 2 | **Miércoles 14 de octubre** | Propuesta para la visita y base técnica (se presenta en la visita a la asociación de Alerce) | EVA 2 |
| 3 | Lunes 19 de octubre | Levantamiento, requisitos completos y diseño detallado | EVA 3 |
| 4 | Lunes 26 de octubre | Acceso, administración y tienda | EVA 3 |
| 5 | Lunes 2 de noviembre | Catálogo, productos y ventas | EVA 3 |
| 6 | Lunes 9 de noviembre | Vitrina, modo comprador, difusión y mapas | EVA 4 |
| 7 | Lunes 16 de noviembre | Ferias, seguidores y notificaciones | EVA 4 |
| 8 | **Lunes 23 de noviembre** | Producto terminado (entrega final) | EVA 5 |

## 2. Notas de la asignatura

Las notas se organizan según las entregas del proyecto (la EVA 1 corresponde a la Unidad 1 y queda fuera del proyecto). Cada entrega se califica con sus criterios de aceptación, y la nota de cada EVA pondera sus entregas.

| Nota | Nombre | Entregas y ponderación | Contenidos de la asignatura que incluye |
|------|--------|------------------------|------------------------------------------|
| **EVA 2** | Diseño y propuesta | Entrega 1: 40 % · Entrega 2: 60 % | Prototipo de la propuesta y puesta en marcha del repositorio con flujo de Git |
| **EVA 3** | Especificación y construcción base | Entrega 3: 30 % · Entrega 4: 35 % · Entrega 5: 35 % | Estudio de caso: presentación de la app por Git (entrega 3) · Presentación y conexión a la base de datos (entrega 4) · Elementos de seguridad: informe de pruebas y detección (entrega 5) |
| **EVA 4** | Vitrina, mapas y ferias | Entrega 6: 50 % · Entrega 7: 50 % | Prototipo de GPS y mapas (entrega 6) |
| **EVA 5** | Producto final | Entrega 8: 100 % | Proyecto de app: presentación final |

### 2.1 Contenidos de la asignatura y requisitos asociados

Cada contenido se evalúa dentro de la entrega indicada y se apoya en requisitos del proyecto.

| Contenido | Entrega (nota) | Qué se evalúa | Requisitos |
|-----------|----------------|---------------|------------|
| Estudio de caso: presentación de la app por Git | 3 (EVA 3) | El grupo presenta su proyecto a través del repositorio: flujo de ramas, *pull requests* revisados, *issues* de requisitos, etiquetas por entrega y contribución de cada integrante. | RNF-MAN-03, RNF-MAN-04, RNF-MAN-05 |
| Presentación y conexión a la base de datos | 4 (EVA 3) | Modelo de datos en Firestore y su justificación; conexión desde la app y la web mediante la capa de datos; datos de prueba cargados. | RNF-DAT-01, RNF-DAT-02, RNF-DAT-04, RNF-SEG-01 |
| Elementos de seguridad: informe de pruebas y detección | 5 (EVA 3) | Pruebas automatizadas de las reglas de seguridad, análisis de vulnerabilidades y mecanismos de detección, reunidos en un informe. | RNF-SEG-04, RNF-SEG-05, RNF-SEG-06, RNF-SEG-07, RNF-SEG-08 |
| Prototipo de GPS y mapas | 6 (EVA 4) | Ubicación de ferias en el mapa, mapa de próximas ferias con la posición del usuario y manejo del permiso de ubicación. | RF-MAP-01 a RF-MAP-04, RNF-PRI-04 |
| Proyecto de app: presentación final | 8 (EVA 5) | Plataforma completa, probada y documentada. | Todos los Esenciales |

## 3. Reglas comunes a todas las entregas

Además de los entregables propios, **cada entrega** incluye:

- **Etiqueta en el repositorio del grupo** (`entrega-1`, `entrega-2`, …) sobre el commit entregado, creada antes del inicio de la clase (en la entrega 2, antes de la visita).
- **Informe breve** (una o dos páginas, en `docs/`): lo realizado, requisitos cubiertos (por ID), lo pendiente y su plan, y el reparto de trabajo dentro del grupo.
- **Demostración** en clase de 5 a 10 minutos, desde el commit etiquetado (en la entrega 2, la propuesta se prueba con las emprendedoras en la visita).

Desde la entrega 3, la app compila e instala, la web está publicada con lo construido hasta esa semana y lo entregado antes sigue funcionando. Los documentos se entregan en `docs/` del repositorio del grupo.

---

## 4. Entregas

### Entrega 1 — Diseño conceptual

**Fecha:** lunes 5 de octubre · **Nota:** EVA 2 (40 %)

**Objetivo:** definir la visión del grupo sobre la plataforma a partir de la ficha y los requisitos base: quiénes la usan, qué hacen en ella, cómo navegan y qué información maneja, dejando explícito lo que hay que confirmar en terreno.

**Entregables:**

1. **Identidad:** nombre comercial propuesto con su justificación, logo o bosquejo, paleta de colores y tipografía.
2. **Propuesta de valor** para cada perfil: emprendedora, comprador y administrador.
3. **Fichas de usuario tipo** (*personas*), una por perfil, marcando los supuestos que se deben confirmar en la visita.
4. **Historias de usuario de los flujos principales**, en formato "Como… quiero… para…" y con el ID del requisito que cubren:
   - Emprendedora: entrar a la app con huella, crear un producto, registrar una venta, responder una invitación a feria y compartir su tienda.
   - Comprador: encontrar una tienda, ver sus productos y contactar a la emprendedora.
   - Administrador: registrar una emprendedora, y crear una feria e invitar participantes.
5. **Mapa de navegación** de la app (modo emprendedora y modo comprador) y de la web (vitrina, administración de la tienda y administración de la plataforma).
6. **Modelo conceptual del dominio:** diagrama de entidades y relaciones, con cardinalidades.
7. **Hipótesis de tipos de producto:** tabla con los tipos de la ficha (sección 5.11) y, para cada uno, los campos, variantes, modalidad y manejo de stock que el grupo supone.
8. **Supuestos a validar:** lista de lo que el grupo supone y cómo lo averiguará en la visita (pregunta o tarea de la pauta).

**Criterios de aceptación:**

1. Cada flujo principal tiene al menos una historia de usuario, y cada historia cita el ID del requisito que cubre (por ejemplo, "RF-PRO-01").
2. Cada flujo principal se puede recorrer de principio a fin en el mapa de navegación, y las entidades que usa están en el modelo conceptual.
3. Cada supuesto de la lista tiene asociada una pregunta o tarea concreta para la visita.

---

### Entrega 2 — Propuesta para la visita y base técnica

**Fecha:** miércoles 14 de octubre, en la visita a la asociación de Alerce · **Nota:** EVA 2 (60 %)

**Objetivo:** llegar a terreno con una propuesta concreta que las emprendedoras puedan usar y comentar, con todo lo necesario para levantar información, y dejar el proyecto técnico listo para empezar a construir.

**Entregables:**

1. **Prototipo navegable** de baja o media fidelidad (Figma u otra herramienta), usable en un celular, con estos flujos de la emprendedora:
   1. Entrar a la app (modo emprendedora, con huella).
   2. Crear un producto con el flujo guiado (foto, datos, variantes, disponibilidad).
   3. Registrar una venta.
   4. Responder una invitación a feria.
   5. Compartir la tienda por WhatsApp o QR.

   Incluye además una o dos pantallas de lo que vería un comprador (tienda y producto), con ejemplos de productos plausibles de la zona y sin datos personales reales.
2. **Guion de revisión del prototipo:** el Guion C de la pauta adaptado a las pantallas del grupo, con las tareas y preguntas que se harán a cada emprendedora.
3. **Material de la visita:** los dos encargados del trabajo con la emprendedora y sus roles ([pauta de la actividad](pauta-actividad-visita.md)), preguntas propias agregadas a la pauta y material impreso (fichas de registro de producto, hojas de observación de uso, hojas de revisión del prototipo, hoja de consentimiento y QR de prueba).
4. **Decisiones técnicas:** framework web elegido con su justificación y diagrama preliminar de la arquitectura en capas.
5. **Proyecto base:** app Android (Kotlin y Jetpack Compose) y web en el repositorio del grupo, conectadas a Firebase, con README de ejecución y `.gitignore` que excluya credenciales. Desde aquí el grupo trabaja con ramas por funcionalidad y *pull requests* (RNF-MAN-03).
6. **Primer incremento ejecutable:** pantalla inicial de la app con la separación entre modo comprador y modo emprendedora (RF-ACC-05) y web publicada en Firebase Hosting (URL en el README).

**Criterios de aceptación:**

1. Una persona ajena al grupo, en un celular, completa las cinco tareas del prototipo de principio a fin sin encontrar pantallas sin salida ni botones que no lleven a ninguna parte.
2. Al llegar a la visita, el grupo asiste completo, con el prototipo cargado en un celular (funciona sin depender del wifi del lugar), sus dos encargados con roles definidos y el material impreso completo.
3. La app se instala en un dispositivo o emulador y muestra la pantalla inicial con los dos modos; la web abre desde su URL pública; el repositorio no contiene `google-services.json`, claves ni contraseñas.

---

### Entrega 3 — Levantamiento, requisitos completos y diseño detallado

**Fecha:** lunes 19 de octubre · **Nota:** EVA 3 (30 %)

**Objetivo:** convertir lo observado en la visita en una especificación cerrada y en un diseño listo para construir.

**Entregables:**

1. **Informe de levantamiento** según la sección 10 de la pauta, con sus anexos (fichas de producto, hojas de observación y hojas de revisión del prototipo).
2. **Tipos de emprendimiento y de producto reales:** tabla con campos específicos, variantes, modalidad y manejo de stock de cada tipo, comparada con las hipótesis de la entrega 1.
3. **Documento de requisitos completo:** requisitos base más requisitos nuevos (con la plantilla de los requisitos base, trazados a hallazgos H01…), historias de usuario de todos los requisitos Esenciales (completando las de los flujos principales de la entrega 1), criterios de aceptación para todos los Esenciales e Importantes, y decisiones fundamentadas sobre la versión mínima de Android y la inclusión de servicios.
4. **Prototipo de alta fidelidad** corregido con lo observado en la visita (flujos de la emprendedora y pantallas principales del comprador y del administrador), con un registro de los cambios realizados.
5. **Guía visual:** colores, tipografía, componentes, íconos con texto y tamaños mínimos de 48 dp (RNF-USA-01, RNF-USA-02).
6. **Modelo de datos en Firestore:** colecciones, documentos, campos y relaciones, incluidos los campos específicos por tipo de producto.
7. **Arquitectura en capas definitiva** y borrador de las reglas de seguridad por perfil (RNF-SEG-01).
8. **Contenido evaluado — Estudio de caso: presentación de la app por Git:** presentación del proyecto a través del repositorio: flujo de trabajo documentado (ramas, *pull requests* y revisión), requisitos cargados como *issues*, etiquetas `entrega-1` a `entrega-3` y contribución de cada integrante (RNF-MAN-03 a 05).

**Criterios de aceptación:**

1. El informe incluye todas las tablas de consolidación de la pauta (sección 9) completas, con las emprendedoras identificadas solo por código (E01, E02…).
2. Cada requisito nuevo cita el hallazgo que lo origina; cada requisito Esencial está cubierto por al menos una historia de usuario; y todos los Esenciales e Importantes tienen criterios de aceptación en formato "Dado… cuando… entonces…".
3. Cada cambio anotado en la tabla de retroalimentación (sección 9.6 de la pauta) se ve reflejado en el prototipo, y cada tipo de producto levantado tiene sus campos en el modelo de datos.
4. La rama principal está protegida, todo cambio desde la entrega 2 entró por un *pull request* revisado por otro integrante, y cada integrante tiene commits propios en el historial.

---

### Entrega 4 — Acceso, administración y tienda

**Fecha:** lunes 26 de octubre · **Nota:** EVA 3 (35 %)

**Objetivo:** que existan los tres perfiles con acceso seguro y que el administrador pueda poblar la plataforma con asociaciones y emprendedoras.

**Entregables:**

1. **App — acceso:** ingreso de la emprendedora con las credenciales entregadas por el administrador, activación y desactivación de la huella, ingreso del comprador con Google y cierre de sesión.
2. **App — tienda:** edición de la ficha de la tienda (nombre, foto o logo, descripción, tipo de emprendimiento, sector y contacto).
3. **Web — administración de la plataforma:** crear, editar y desactivar cuentas de emprendedora; crear, editar y desactivar asociaciones; asignar y quitar emprendedoras de asociaciones; mantener tipos de emprendimiento, tipos de producto y categorías.
4. **Web — acceso:** ingreso del comprador con Google o con correo y contraseña, y navegación sin iniciar sesión.
5. **Reglas de seguridad** de Firestore y Storage por perfil, publicadas.
6. **Capa de datos:** repositorios en la app y en la web por los que pasa todo acceso a Firestore, y procedimiento para cargar datos de prueba ficticios en un proyecto de Firebase de desarrollo.
7. **Contenido evaluado — Presentación y conexión a la base de datos:** presentación del modelo de datos en Firestore (colecciones, documentos, relaciones e índices) y su justificación, y demostración de la conexión desde la app y la web: lectura y escritura de datos reales por perfil.

**Requisitos que cubre:** RF-ACC-01, 02, 03, 04, 07, 09 · RF-ADM-01, 03 · RF-ASO-01, 02 · RF-TIE-01 · RNF-SEG-01, 02 · RNF-DAT-01, 02, 04.

**Criterios de aceptación:**

1. **Dado** que el administrador creó una cuenta de emprendedora en la web, **cuando** ella ingresa en la app con esas credenciales y activa la huella, **entonces** en su siguiente ingreso entra solo con la huella.
2. **Dado** una emprendedora con sesión iniciada, **cuando** edita los datos de su tienda, **entonces** los cambios se conservan al cerrar y volver a abrir la app, y se ven también desde la web.
3. **Dado** una emprendedora con sesión iniciada, **cuando** intenta modificar la tienda de otra emprendedora (por ejemplo, desde el simulador de reglas de Firebase), **entonces** la operación es rechazada.
4. Ninguna pantalla consulta Firestore directamente (todo pasa por los repositorios), y el modelo presentado coincide con los datos que se ven en la consola de Firebase durante la demostración.

---

### Entrega 5 — Catálogo, productos y ventas

**Fecha:** lunes 2 de noviembre · **Nota:** EVA 3 (35 %)

**Objetivo:** que la emprendedora administre su catálogo completo, a su manera, y registre sus ventas.

**Entregables:**

1. **Flujo guiado de creación de producto:** foto desde cámara o galería (comprimida antes de subir), datos comunes, campos específicos según el tipo de producto, variantes con precio, foto y stock propios, configuración de disponibilidad y publicación. Si se interrumpe, conserva lo ingresado.
2. **Gestión del catálogo:** editar y eliminar productos; configurar modalidad, manejo de stock, comportamiento al agotarse y visibilidad por producto o de forma masiva (selección, categoría o catálogo completo); valores por defecto para productos nuevos.
3. **Registro de ventas:** producto, variante y cantidad, con descuento de stock y retiro de piezas únicas.
4. **Historial de ventas** opcional (se activa en la configuración), con precio, fecha y lugar, y consulta filtrando por fecha, feria y producto.
5. **Vista previa del catálogo público** en la app, que muestra cada producto según su configuración.
6. **Catálogo sin conexión:** la emprendedora consulta su catálogo sin red y los cambios se sincronizan al volver la conexión.
7. **Contenido evaluado — Elementos de seguridad: informe de pruebas y detección:**
   - Pruebas automatizadas de las reglas de seguridad con Firebase Emulator Suite, para cada perfil.
   - Análisis de vulnerabilidades de la app, la web y sus dependencias (Android Lint, revisión de dependencias y MobSF).
   - Mecanismos de detección: Firebase App Check y registro de las acciones del administrador (Importantes).
   - Informe de pruebas de seguridad con los casos probados, las vulnerabilidades detectadas, su gravedad y su corrección.

**Requisitos que cubre:** RF-PRO-01 a 12 · RF-VEN-01 a 04 · RF-CFG-06 · RNF-REN-01 · RNF-USA-04 · RNF-DAT-03 · RNF-SEG-04, 05, 08 (y 06, 07 si alcanza; si no, en la entrega 8).

**Criterios de aceptación:**

1. **Dado** un producto con variantes que maneja stock, **cuando** la emprendedora registra la venta de una variante, **entonces** se descuenta solo el stock de esa variante; y si llega a cero, el catálogo público aplica la opción "al agotarse" configurada.
2. **Dado** una pieza única publicada, **cuando** la emprendedora registra su venta, **entonces** desaparece del catálogo público y no vuelve a aparecer.
3. **Dado** que la emprendedora está creando un producto, **cuando** cierra la app a mitad del flujo y vuelve a abrirla, **entonces** encuentra lo que ya había ingresado.
4. Las pruebas de reglas se ejecutan con un comando documentado en el README y pasan, e incluyen al menos un caso rechazado por perfil; cada vulnerabilidad del informe tiene su gravedad y su corrección o justificación.

---

### Entrega 6 — Vitrina, modo comprador, difusión y mapas

**Fecha:** lunes 9 de noviembre · **Nota:** EVA 4 (50 %)

**Objetivo:** que cualquier persona pueda conocer a las emprendedoras desde la web o la app, llegar a ellas por un enlace o un código QR, y ubicar en un mapa las ferias donde estarán.

**Entregables:**

1. **Web pública adaptable** (computador y teléfono): directorio de emprendedoras y asociaciones con búsqueda y filtros (tipo de emprendimiento, sector y asociación), vista de tienda, detalle de producto con variantes, vista de asociación y contacto según la configuración de cada emprendedora.
2. **App — modo comprador:** las mismas vistas del directorio, tienda, producto y asociación, aplicando la configuración de navegación anónima.
3. **Compartir y QR:** compartir tienda, producto y asociación con el menú nativo de Android, y generar, guardar o compartir el QR; cada enlace abre la página web correspondiente.
4. **Configuración de la tienda:** mostrar u ocultar precios, forma de contacto (WhatsApp, formulario o ambos) y bandeja de contactos recibidos en la app.
5. **Web — administración de la tienda:** la emprendedora gestiona su tienda, productos y ventas desde la web.
6. **Web — administración de la plataforma:** configuración de la navegación anónima de la app, y creación y edición de ferias con su ubicación marcada en un mapa.
7. **Contenido evaluado — Prototipo de GPS y mapas:**
   - Mapa con la ubicación de cada feria y opción "Cómo llegar", en la app y en la web.
   - Mapa de próximas ferias en el modo comprador; con permiso de ubicación (GPS), centrado en la posición de la persona y con las ferias ordenadas por distancia.
   - Punto de venta o retiro opcional de la emprendedora, marcado en un mapa (Importante).
   - Solicitud del permiso de ubicación solo cuando se necesita, con la app funcionando si se rechaza.

**Requisitos que cubre:** RF-CMP-01, 02, 03, 05 · RF-COM-01 a 03 · RF-ASO-03 · RF-ACC-06 · RF-ADM-02 · RF-CFG-01 a 03 · RF-TIE-02 · RF-FER-01 · RF-MAP-01 a 04 · RNF-CPT-02 · RNF-PRI-03, 04.

**Criterios de aceptación:**

1. **Dado** el enlace de una tienda compartido por WhatsApp o su código QR, **cuando** se abre en un teléfono sin sesión iniciada, **entonces** se ve la página web de esa tienda con su catálogo público.
2. **Dado** una emprendedora con "mostrar precios" desactivado, **cuando** un visitante ve sus productos en la web o en la app, **entonces** aparece "Consultar precio" en lugar del precio.
3. **Dado** que el administrador elige una de las tres opciones de navegación anónima, **cuando** se abre la app en modo comprador sin sesión, **entonces** la app se comporta según esa opción (permitir, invitar con opción de omitir u obligar el ingreso con Google).
4. **Dado** un comprador que autoriza su ubicación, **cuando** abre el mapa de ferias, **entonces** ve su posición y las ferias ordenadas de la más cercana a la más lejana; y si rechaza el permiso, ve el mapa con las ferias ordenadas por fecha, sin errores.

---

### Entrega 7 — Ferias, seguidores y notificaciones

**Fecha:** lunes 16 de noviembre · **Nota:** EVA 4 (50 %)

**Objetivo:** completar la gestión centralizada de ferias y los avisos a seguidores. Es la **última entrega con funcionalidades nuevas**; después solo se prueba, corrige y documenta.

**Entregables:**

1. **Web — gestión de ferias:** publicar y cancelar ferias (la creación con ubicación se entrega en la 6); invitar o agregar directamente emprendedoras y asociaciones; checklist con estados, búsqueda y filtros; envío de recordatorios y avisos; registro de asistencia.
2. **App — ferias de la emprendedora:** invitación como notificación, respuesta "Participo" o "No participo" con un toque, calendario de sus ferias y sugerencia de la feria al registrar una venta, según la fecha y, si autorizó la ubicación, según dónde está.
3. **Ficha pública de la feria** en la web y en el modo comprador, con los participantes confirmados, una muestra de su catálogo público, el mapa de la entrega 6, y opción de compartir y QR.
4. **Seguidores:** seguir y dejar de seguir tiendas y asociaciones (con inicio de sesión si es visitante); aviso por notificación push en la app y por notificación del navegador o correo en la web cuando confirman su participación en una feria.
5. **Configuraciones restantes de la tienda:** notificaciones de contacto con horario, y calificaciones activables por la emprendedora.

**Requisitos que cubre:** RF-FER-02 a 10 · RF-CMP-04, 06 a 09 · RF-ACC-08 · RF-VEN-05 · RF-MAP-05 · RF-CFG-04, 05 · RNF-PRI-02.

**Criterios de aceptación:**

1. **Dado** una feria creada por el administrador, **cuando** invita a una emprendedora, **entonces** ella recibe una notificación en la app, responde "Participo" con un toque y el checklist del administrador muestra su estado como "Confirmada".
2. **Dado** un comprador que sigue a esa emprendedora, **cuando** ella confirma su participación, **entonces** el comprador recibe una notificación push con el nombre de la feria.
3. **Dado** un visitante sin sesión, **cuando** intenta seguir una tienda, **entonces** se le pide iniciar sesión y, al volver, ya queda siguiéndola sin repetir la acción.

---

### Entrega 8 — Producto terminado (entrega final)

**Fecha:** lunes 23 de noviembre · **Nota:** EVA 5 (100 %)

**Objetivo:** entregar una plataforma estable, probada con usuarias reales y documentada, lista para presentarse a las emprendedoras.

**Entregables:**

1. **Informe de la prueba de uso** con emprendedoras (RNF-USA-05), realizada entre la entrega 7 y la final: tareas realizadas, problemas detectados y correcciones aplicadas.
2. **Funcionalidades pendientes:** requisitos Importantes que no alcanzaron en su semana (por ejemplo, RF-ACC-10, RF-ADM-04, RNF-SEG-06 y RNF-SEG-07) y verificación de los no funcionales transversales (RNF-USA-03, RNF-CPT-01, RNF-REN-02, RNF-PRI-01, RNF-OPE-01, RNF-IDI-01).
3. **Informe de seguridad actualizado** (RNF-SEG-08): pruebas de reglas y análisis de vulnerabilidades repetidos sobre el producto completo, incluidas ferias, seguidores y mapas.
4. **Pruebas:** casos de prueba de los criterios de aceptación de todos los requisitos Esenciales, con su resultado.
5. **Matriz de requisitos** con el estado final de cada uno (cumplido, parcial o pendiente, con su justificación).
6. **Producto publicado:** APK firmado (o publicación de prueba en Google Play) y web publicada en Firebase Hosting.
7. **Documentación:** README de ejecución, manual breve para la emprendedora, manual breve para el administrador y descripción de cómo se incorporaría la IA como módulo desacoplado (RNF-MAN-02).
8. **Contenido evaluado — Proyecto de app: presentación final:** presentación y demostración de la plataforma completa.

**Criterios de aceptación:**

1. El APK se instala en un celular Android con la versión mínima definida, y la web funciona desde su URL pública en computador y en teléfono.
2. En la matriz de requisitos, todos los Esenciales figuran como "cumplido", cada uno con su caso de prueba y resultado; los Importantes no construidos figuran como pendientes, con su justificación.
3. Una persona ajena al grupo puede ejecutar el proyecto desde cero siguiendo solo el README, y el informe de la prueba de uso muestra qué se corrigió a partir de lo observado con las emprendedoras.
