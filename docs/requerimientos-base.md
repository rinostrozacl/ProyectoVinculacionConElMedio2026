# Requisitos base — Emprendedores Puerto Montt

Requisitos **mínimos** propuestos por el equipo docente a partir de la [ficha de proyecto v1.1](ficha-proyecto.md). Son el punto de partida común para todos los grupos.

Incluyen los contenidos de las evaluaciones de la asignatura: Git (RNF-MAN-03 a 05), base de datos (RNF-DAT), seguridad (RNF-SEG-04 a 08) y GPS y mapas (RF-MAP, RNF-PRI-04). La entrega y la nota (EVA) en que se evalúa cada uno están en la [planificación](planificacion.md#2-notas-de-la-asignatura).

**Cada grupo debe completarlos** con lo que obtenga del levantamiento con la contraparte ([pauta de levantamiento](pauta-levantamiento.md)): requisitos nuevos, campos específicos por tipo de producto, criterios de aceptación y detalle de flujos (ver sección 5).

---

## 1. Convenciones

### 1.1 Identificadores

Categorías de requisitos no funcionales: USA (usabilidad), CPT (compatibilidad), REN (rendimiento), SEG (seguridad), PRI (privacidad), DAT (datos), OPE (operación), MAN (mantenibilidad) e IDI (idioma).

| Prefijo | Tipo |
|---------|------|
| `RF-XXX-nn` | Requisito funcional del módulo `XXX` |
| `RN-nn` | Regla de negocio |
| `RNF-XXX-nn` | Requisito no funcional de la categoría `XXX` |

Los requisitos que agregue cada grupo continúan la numeración del módulo (por ejemplo, después de `RF-PRO-12` viene `RF-PRO-13`) o crean un módulo nuevo si corresponde.

### 1.2 Prioridad

| Prioridad | Significado |
|-----------|-------------|
| **Esencial** | Obligatorio en la entrega final de todos los grupos. |
| **Importante** | Esperado en una solución completa; se considera en la evaluación y en la selección de la solución ganadora. |
| **Condicionado** | Depende de conseguir financiamiento (IA). No se exige; el diseño debe dejarlo preparado. |

### 1.3 Perfiles

- **Administrador:** administrador de plataforma.
- **Emprendedora:** usuaria que vende, registrada por el administrador.
- **Comprador:** usuario con cuenta (Google en la app; cualquier medio en la web).
- **Visitante:** persona que navega sin iniciar sesión.

## 2. Reglas de negocio

| ID | Regla |
|----|-------|
| RN-01 | El registro de emprendedoras y asociaciones **no es libre**: solo lo realiza el administrador. |
| RN-02 | Solo el administrador crea, edita y cancela ferias o eventos. La emprendedora nunca crea ferias. |
| RN-03 | La participación en ferias es **solo por invitación** del administrador (o incorporación directa por él). |
| RN-04 | Las asociaciones son administradas solo por el administrador; no son un perfil de usuario. |
| RN-05 | Una emprendedora puede pertenecer a cero, una o varias asociaciones. |
| RN-06 | Seguir, pedir alertas y calificar requieren una cuenta de comprador. |
| RN-07 | En la app, el comprador solo puede autenticarse con cuenta de Google. |
| RN-08 | Una pieza única vendida sale del catálogo público y no vuelve a aparecer. |
| RN-09 | Un producto marcado "no disponible" no aparece en el catálogo público, pero se conserva en la tienda de la emprendedora. |
| RN-10 | El historial de ventas es privado: solo lo ve su emprendedora; el administrador no tiene acceso. |
| RN-11 | En la primera versión, los seguidores reciben avisos solo cuando una tienda o asociación que siguen confirma su participación en una feria. |
| RN-12 | La plataforma cubre solo la comuna de Puerto Montt. |
| RN-13 | La plataforma debe funcionar completa sin IA. |

## 3. Requisitos funcionales

### 3.1 Acceso (ACC)

| ID | Requisito | Prioridad |
|----|-----------|-----------|
| RF-ACC-01 | La emprendedora inicia sesión con el usuario y la contraseña entregados por el administrador, en la app y en la web. | Esencial |
| RF-ACC-02 | En la app, la emprendedora puede activar el acceso con huella digital después de su primer ingreso, y desactivarlo cuando quiera. | Esencial |
| RF-ACC-03 | En la app, el comprador inicia sesión con su cuenta de Google. | Esencial |
| RF-ACC-04 | En la web, el comprador puede registrarse e iniciar sesión con Google o con correo y contraseña. | Esencial |
| RF-ACC-05 | La app muestra desde la primera pantalla una separación clara entre el modo comprador y el modo emprendedora. | Esencial |
| RF-ACC-06 | La app aplica la configuración de navegación anónima definida por el administrador: (a) permitir, (b) invitar a iniciar sesión con opción de omitir, (c) obligar el inicio de sesión al abrir. | Esencial |
| RF-ACC-07 | La web permite navegar sin iniciar sesión. | Esencial |
| RF-ACC-08 | Si un visitante intenta seguir, pedir alertas o calificar, el sistema le pide iniciar sesión o registrarse y, una vez autenticado, completa la acción que intentaba. | Esencial |
| RF-ACC-09 | Todo usuario autenticado puede cerrar sesión. | Esencial |
| RF-ACC-10 | Emprendedoras y compradores con correo y contraseña pueden recuperar su contraseña. | Importante |

### 3.2 Tienda (TIE)

| ID | Requisito | Prioridad |
|----|-----------|-----------|
| RF-TIE-01 | La emprendedora edita la ficha de su tienda: nombre, foto o logo, descripción, tipo de emprendimiento, sector de Puerto Montt y datos de contacto. | Esencial |
| RF-TIE-02 | La emprendedora puede administrar su tienda, productos y ventas también desde la web. | Importante |

### 3.3 Catálogo y productos (PRO)

| ID | Requisito | Prioridad |
|----|-----------|-----------|
| RF-PRO-01 | La emprendedora crea un producto mediante un flujo guiado paso a paso: foto (cámara o galería), datos básicos, variantes (si tiene), disponibilidad y publicación. | Esencial |
| RF-PRO-02 | La ficha de producto tiene los datos comunes: fotos, nombre, descripción, categoría, precio y tipo de producto. | Esencial |
| RF-PRO-03 | La ficha de producto incluye los campos específicos de su tipo de producto, definidos a partir del levantamiento. | Importante |
| RF-PRO-04 | La emprendedora edita y elimina sus productos. | Esencial |
| RF-PRO-05 | Un producto puede tener variantes (talla, color, tamaño, etc.), cada una con su propio precio, foto y stock. | Esencial |
| RF-PRO-06 | La emprendedora define la modalidad de cada producto: regular, a pedido o pieza única. | Esencial |
| RF-PRO-07 | La emprendedora define si un producto maneja stock o no. | Esencial |
| RF-PRO-08 | Para productos con stock, la emprendedora define qué ocurre al agotarse: mostrar "agotado", ocultar del catálogo o pasar a "a pedido". | Esencial |
| RF-PRO-09 | La emprendedora marca un producto como disponible o no disponible. | Esencial |
| RF-PRO-10 | La emprendedora aplica una configuración de disponibilidad a varios productos a la vez: selección, categoría o catálogo completo. | Importante |
| RF-PRO-11 | La emprendedora define los valores por defecto con que nace cada producto nuevo en su tienda. | Importante |
| RF-PRO-12 | El catálogo público muestra cada producto según su configuración (modalidad, stock, comportamiento al agotarse y visibilidad). | Esencial |

### 3.4 Ventas (VEN)

| ID | Requisito | Prioridad |
|----|-----------|-----------|
| RF-VEN-01 | La emprendedora registra una venta indicando producto, variante (si tiene) y cantidad; si el producto maneja stock, se descuenta. | Esencial |
| RF-VEN-02 | Al registrar la venta de una pieza única, el producto sale del catálogo público. | Esencial |
| RF-VEN-03 | Si la emprendedora tiene activo el historial, cada venta guarda además precio, fecha y lugar (feria de la plataforma u otro lugar). | Importante |
| RF-VEN-04 | La emprendedora consulta su historial de ventas filtrando por fecha, feria y producto. | Importante |
| RF-VEN-05 | Al registrar una venta el mismo día de una feria en que está confirmada, la app sugiere esa feria como lugar. | Importante |

### 3.5 Compartir (COM)

| ID | Requisito | Prioridad |
|----|-----------|-----------|
| RF-COM-01 | Desde la app se puede compartir una tienda, un producto, una asociación o una feria mediante el menú nativo de Android (WhatsApp, redes sociales, etc.), con un enlace a su página web. | Esencial |
| RF-COM-02 | La app genera el código QR de una tienda, asociación o feria, y permite guardarlo o compartirlo como imagen. | Esencial |
| RF-COM-03 | Cada enlace o QR abre la página web correspondiente, visible sin iniciar sesión. | Esencial |

### 3.6 Ferias y eventos (FER)

| ID | Requisito | Prioridad |
|----|-----------|-----------|
| RF-FER-01 | El administrador crea, edita, publica y cancela ferias con: nombre, descripción, imagen, lugar y ubicación en el mapa (ver RF-MAP-01), fecha, horario y organizador. | Esencial |
| RF-FER-02 | El administrador invita emprendedoras y asociaciones a una feria. | Esencial |
| RF-FER-03 | El administrador agrega directamente una emprendedora o asociación a una feria, sin invitación. | Importante |
| RF-FER-04 | El administrador ve el checklist de cada feria con el estado de cada participante: invitada, confirmada, rechazada o agregada por el administrador. | Esencial |
| RF-FER-05 | El checklist permite buscar y filtrar por estado, tipo de emprendimiento y asociación. | Importante |
| RF-FER-06 | Desde el checklist, el administrador envía recordatorios a quienes no han respondido y avisos a las confirmadas. | Importante |
| RF-FER-07 | El administrador registra la asistencia real (asistió / no asistió) el día de la feria. | Importante |
| RF-FER-08 | La emprendedora recibe la invitación como notificación en la app y responde "Participo" o "No participo" con un toque. | Esencial |
| RF-FER-09 | La emprendedora ve en la app el calendario de ferias a las que está invitada o confirmada. | Esencial |
| RF-FER-10 | Cada feria tiene una ficha pública (web y modo comprador) con sus datos, los participantes confirmados y una muestra del catálogo público de cada uno. | Esencial |

### 3.7 Comprador (CMP)

| ID | Requisito | Prioridad |
|----|-----------|-----------|
| RF-CMP-01 | El comprador o visitante ve un directorio de emprendedoras y asociaciones, con búsqueda y filtros por tipo de emprendimiento, sector y asociación. | Esencial |
| RF-CMP-02 | El comprador o visitante ve la tienda, el detalle de producto y la ficha de asociación. | Esencial |
| RF-CMP-03 | En el detalle de producto, al seleccionar una variante se muestran su foto y su precio. | Esencial |
| RF-CMP-04 | El comprador o visitante ve el calendario de próximas ferias y la ficha de cada una. | Esencial |
| RF-CMP-05 | El comprador o visitante contacta a la emprendedora según la forma que ella configuró: WhatsApp, formulario o ambos. | Esencial |
| RF-CMP-06 | El comprador sigue y deja de seguir una tienda o asociación. | Esencial |
| RF-CMP-07 | En la app, el comprador recibe una notificación push cuando una tienda o asociación que sigue confirma su participación en una feria. | Esencial |
| RF-CMP-08 | En la web, el comprador recibe ese aviso como notificación del navegador (previo permiso) o por correo. | Importante |
| RF-CMP-09 | El comprador califica la tienda y sus productos, si la emprendedora tiene activas las calificaciones. | Importante |

### 3.8 Configuración de la tienda (CFG)

| ID | Requisito | Prioridad |
|----|-----------|-----------|
| RF-CFG-01 | La emprendedora define si sus precios se muestran; si no, se muestra "consultar precio". | Esencial |
| RF-CFG-02 | La emprendedora define la forma de contacto: WhatsApp, formulario o ambos. | Esencial |
| RF-CFG-03 | La emprendedora ve en la app los contactos recibidos por formulario. | Esencial |
| RF-CFG-04 | La emprendedora activa o desactiva las notificaciones de contacto y define su horario; fuera de horario el contacto se guarda sin notificar. | Importante |
| RF-CFG-05 | La emprendedora activa o desactiva las calificaciones de su tienda. | Importante |
| RF-CFG-06 | La emprendedora activa o desactiva el historial de ventas. | Importante |

### 3.9 Asociaciones (ASO)

| ID | Requisito | Prioridad |
|----|-----------|-----------|
| RF-ASO-01 | El administrador crea, edita y desactiva asociaciones con su ficha: nombre, logo, descripción, sector y contacto. | Esencial |
| RF-ASO-02 | El administrador asigna y quita emprendedoras de una asociación. | Esencial |
| RF-ASO-03 | Cada asociación tiene una vista pública con sus integrantes y acceso a sus tiendas. | Esencial |

### 3.10 Administración de la plataforma (ADM)

| ID | Requisito | Prioridad |
|----|-----------|-----------|
| RF-ADM-01 | El administrador crea, edita y desactiva cuentas de emprendedora y entrega sus credenciales. | Esencial |
| RF-ADM-02 | El administrador configura la navegación anónima de la app (ver RF-ACC-06). | Esencial |
| RF-ADM-03 | El administrador mantiene los tipos de emprendimiento, tipos de producto y categorías. | Esencial |
| RF-ADM-04 | El administrador gestiona otras cuentas de administrador. | Importante |
| RF-ADM-05 | El administrador habilita o deshabilita la asistencia de IA. | Condicionado |

### 3.11 Asistencia con IA (IA)

| ID | Requisito | Prioridad |
|----|-----------|-----------|
| RF-IA-01 | Con la IA habilitada, al crear o editar un producto se sugieren título, descripción, categoría y observaciones sobre la calidad de la foto. | Condicionado |
| RF-IA-02 | La emprendedora acepta, edita o descarta cada sugerencia. | Condicionado |
| RF-IA-03 | La IA no sugiere precios. | Condicionado |

### 3.12 Mapas y ubicación (MAP)

| ID | Requisito | Prioridad |
|----|-----------|-----------|
| RF-MAP-01 | Al crear o editar una feria, el administrador fija su ubicación marcando un punto en un mapa o buscando la dirección. | Esencial |
| RF-MAP-02 | La ficha de la feria muestra un mapa con su ubicación, en la app y en la web, con la opción "Cómo llegar", que abre la aplicación de mapas del celular. | Esencial |
| RF-MAP-03 | En el modo comprador, la app muestra en un mapa las próximas ferias; si la persona autoriza el uso de su ubicación (GPS), el mapa se centra en su posición y las ferias se ordenan por distancia. | Esencial |
| RF-MAP-04 | La emprendedora puede indicar, si lo desea, un punto de venta o de retiro (por ejemplo, su local) marcándolo en un mapa; si lo indica, se muestra en su tienda. | Importante |
| RF-MAP-05 | Al registrar una venta, si la emprendedora autorizó su ubicación y se encuentra en una feria en curso en la que está confirmada, la app sugiere esa feria como lugar de la venta (complementa RF-VEN-05). | Importante |

## 4. Requisitos no funcionales

| ID | Categoría | Requisito | Prioridad |
|----|-----------|-----------|-----------|
| RNF-USA-01 | Usabilidad | La interfaz de la emprendedora está pensada para baja alfabetización digital: lenguaje simple, íconos acompañados de texto, un objetivo por pantalla y confirmaciones claras. | Esencial |
| RNF-USA-02 | Usabilidad | Los elementos táctiles tienen un tamaño mínimo de 48 dp, según las pautas de accesibilidad de Android. | Esencial |
| RNF-USA-03 | Usabilidad | La app respeta el tamaño de texto configurado en el celular sin romper las pantallas. | Esencial |
| RNF-USA-04 | Usabilidad | Si la emprendedora sale o es interrumpida al crear un producto, no pierde lo ya ingresado. | Importante |
| RNF-USA-05 | Usabilidad | Los flujos principales de la emprendedora se validan con usuarias de la contraparte antes de la entrega final. | Importante |
| RNF-CPT-01 | Compatibilidad | La app funciona en la versión mínima de Android que se defina según los celulares observados en el levantamiento. | Esencial |
| RNF-CPT-02 | Compatibilidad | La web es adaptable y funciona en computador y en teléfono, en las versiones actuales de los navegadores principales. | Esencial |
| RNF-REN-01 | Rendimiento | Las imágenes se comprimen antes de subirlas, para funcionar con planes de datos limitados. | Esencial |
| RNF-REN-02 | Rendimiento | La app tolera conexiones inestables: informa el estado de la conexión y no pierde datos ingresados cuando la red falla. | Importante |
| RNF-SEG-01 | Seguridad | El acceso a datos se controla por perfil en el backend: cada emprendedora solo modifica su tienda; solo el administrador gestiona ferias, asociaciones y cuentas. | Esencial |
| RNF-SEG-02 | Seguridad | La huella se implementa con la API biométrica del sistema; la app no almacena datos biométricos. | Esencial |
| RNF-SEG-03 | Seguridad | Credenciales, claves de API y archivos de configuración sensibles no se suben al repositorio. | Esencial |
| RNF-SEG-04 | Seguridad | Las reglas de seguridad de Firestore y Storage tienen pruebas automatizadas (con Firebase Emulator Suite) que verifican, para cada perfil, qué operaciones se permiten y cuáles se rechazan. | Esencial |
| RNF-SEG-05 | Seguridad | Se analiza la app, la web y sus dependencias en busca de vulnerabilidades (por ejemplo, con las reglas de seguridad de Android Lint, revisión de dependencias y MobSF), y cada hallazgo se corrige o se justifica. | Esencial |
| RNF-SEG-06 | Seguridad | La app y la web usan Firebase App Check para detectar y rechazar solicitudes que no provienen de la aplicación legítima. | Importante |
| RNF-SEG-07 | Seguridad | Las acciones del administrador sobre cuentas, asociaciones y ferias quedan registradas (quién, qué y cuándo) y pueden consultarse. | Importante |
| RNF-SEG-08 | Seguridad | Se elabora un informe de pruebas de seguridad con los casos probados, las vulnerabilidades detectadas, su gravedad y cómo se corrigieron (reúne los resultados de RNF-SEG-04 a RNF-SEG-07). | Esencial |
| RNF-PRI-01 | Privacidad | Los datos personales se tratan según la normativa chilena de protección de datos personales. | Esencial |
| RNF-PRI-02 | Privacidad | El comprador da consentimiento explícito para recibir notificaciones y puede dejar de seguir o darse de baja en cualquier momento. | Esencial |
| RNF-PRI-03 | Privacidad | Solo son públicos los datos que la emprendedora elige mostrar en su tienda. | Esencial |
| RNF-PRI-04 | Privacidad | La ubicación del celular se pide solo al usar una función que la necesita, explicando para qué; si se rechaza, la app sigue funcionando (mapa sin posición, ferias ordenadas por fecha). La ubicación de la persona no se guarda en el servidor. | Esencial |
| RNF-DAT-01 | Datos | El modelo de datos en Firestore está documentado (colecciones, documentos, campos, relaciones e índices) y justificado según las consultas que realiza la plataforma. | Esencial |
| RNF-DAT-02 | Datos | La app y la web acceden a la base de datos solo mediante una capa de datos (repositorios), sin consultas directas desde las pantallas. | Esencial |
| RNF-DAT-03 | Datos | La app usa la persistencia local de Firestore: la emprendedora puede consultar su catálogo sin conexión, y los cambios se sincronizan al volver la red. | Importante |
| RNF-DAT-04 | Datos | Existe un procedimiento para cargar datos de prueba ficticios (emprendedoras, asociaciones, productos y ferias) en un proyecto de Firebase de desarrollo, separado del de producción. | Importante |
| RNF-OPE-01 | Operación | Las herramientas del administrador son operables por personal no técnico (pensando en el traspaso a la Municipalidad). | Importante |
| RNF-MAN-01 | Mantenibilidad | La app se desarrolla en Kotlin con Android Studio, con una arquitectura en capas documentada, y el código se versiona en git con un README de ejecución. | Esencial |
| RNF-MAN-02 | Mantenibilidad | La asistencia de IA se diseña como un módulo desacoplado que puede habilitarse después sin rehacer el flujo de creación de productos. | Importante |
| RNF-MAN-03 | Mantenibilidad | El grupo trabaja con un flujo de Git definido y documentado: rama principal protegida, ramas por funcionalidad, integración mediante *pull requests* revisados por otro integrante y mensajes de commit descriptivos. | Esencial |
| RNF-MAN-04 | Mantenibilidad | Cada entrega queda marcada con una etiqueta (`entrega-N`), y el historial del repositorio muestra la contribución de todos los integrantes. | Esencial |
| RNF-MAN-05 | Mantenibilidad | Los requisitos y tareas se gestionan como *issues* del repositorio, enlazados desde los *pull requests* que los resuelven. | Importante |
| RNF-IDI-01 | Idioma | Toda la interfaz está en español de Chile. | Esencial |

## 5. Lo que completa cada grupo

Estos requisitos base **no son la especificación completa**. Cada grupo debe:

1. **Levantar los tipos de producto** con la contraparte y definir los campos específicos de cada uno (detalle de RF-PRO-03).
2. **Agregar requisitos nuevos** derivados del levantamiento, cada uno trazado a un hallazgo del informe (H01, H02…).
3. **Escribir criterios de aceptación** para cada requisito base Esencial e Importante.
4. **Detallar los flujos principales** (casos de uso o historias de usuario) y prototipar las pantallas.
5. **Decidir de forma fundamentada** si se incluyen servicios, según lo que muestre el levantamiento.
6. **Fijar la versión mínima de Android** (RNF-CPT-01) según los celulares observados.
7. **Proponer el nombre comercial** e identidad visual de la plataforma.

Los grupos pueden proponer ajustes a los requisitos base si el levantamiento lo justifica; esos ajustes se conversan con el docente antes de aplicarlos.

## 6. Plantilla para requisitos nuevos

| Campo | Contenido |
|-------|-----------|
| ID | RF-XXX-nn / RNF-XXX-nn |
| Requisito | Qué debe hacer el sistema, en una oración, desde el punto de vista del usuario. |
| Perfil | Administrador / Emprendedora / Comprador / Visitante |
| Origen | Hallazgo del levantamiento (H__) o requisito base que detalla (RF-___) |
| Prioridad | Esencial / Importante |
| Criterios de aceptación | Condiciones verificables, idealmente en formato "Dado… cuando… entonces…". |

### Ejemplo de criterios de aceptación (RF-PRO-08)

> **RF-PRO-08:** Para productos con stock, la emprendedora define qué ocurre al agotarse: mostrar "agotado", ocultar del catálogo o pasar a "a pedido".

1. **Dado** un producto con stock configurado para "mostrar agotado", **cuando** su stock llega a cero, **entonces** sigue apareciendo en el catálogo público con la etiqueta "Agotado".
2. **Dado** un producto con stock configurado para "ocultar", **cuando** su stock llega a cero, **entonces** deja de aparecer en el catálogo público, pero sigue visible en la tienda de la emprendedora.
3. **Dado** un producto con stock configurado para "pasar a pedido", **cuando** su stock llega a cero, **entonces** aparece en el catálogo público identificado como "A pedido".
4. **Dado** un producto sin manejo de stock, **entonces** la opción "al agotarse" no se muestra.
