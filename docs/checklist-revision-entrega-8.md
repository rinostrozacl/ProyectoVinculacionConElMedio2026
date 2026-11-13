# Checklist de revisión — Entrega 8

| Campo | Valor |
|-------|-------|
| Entrega | 8 — Producto terminado (entrega final) |
| Fecha de revisión | Miércoles 25 de noviembre de 2026 |
| Presentación ante el jurado | Jueves 26 de noviembre de 2026 |
| Nota | Entrega 8, que pondera 100 % de la EVA 5 |
| Criterios | 35. Cada fallo resta 2 décimas |
| Orden | App Android, web y cierre de la entrega |
| Base | [Planificación, entrega 8](planificacion.md#entrega-8--producto-terminado-entrega-final), [requisitos base](requerimientos-base.md) |

Cada criterio se marca **cumple** o **no cumple**. No hay puntaje intermedio. Se demuestra con cuentas de prueba del grupo (no hay emprendedoras de la contraparte en la sala).

## Cómo se calcula la nota

Se parte de **7,0**. Cada criterio en fallo resta **2 décimas** (0,2).

**Nota = 7,0 − 0,2 × (criterios en fallo)**

Tope **7,0**. Piso **1,0** (desde 30 fallos la nota queda en 1,0).

| Fallos | Nota | Fallos | Nota |
|:------:|:----:|:------:|:----:|
| 0 | 7,0 | 8 | 5,4 |
| 1 | 6,8 | 10 | 5,0 |
| 2 | 6,6 | 15 | 4,0 |
| 3 | 6,4 | 20 | 3,0 |
| 4 | 6,2 | 25 | 2,0 |
| 5 | 6,0 | 30 o más | 1,0 |

Con 15 fallos la entrega queda en 4,0. Ejemplo: fallan el APK (A01), la matriz (C08) y el README (C11). Son 3 fallos: 7,0 − 0,6 = **6,4**.

---

## 1. App Android

Producto instalable y flujos principales vivos. Celular con la versión mínima definida por el grupo.

| ID | Criterio | No cumple si… | Sustento |
|:--:|----------|----------------|----------|
| A01 | El APK firmado (o la build de prueba en Play) se instala en un celular con la versión mínima de Android definida. | No hay APK firmado, no se instala, o no hay versión mínima definida. | Entregable 6; RNF-CPT-01; criterio 1 |
| A02 | Al abrir, se distinguen el modo comprador y el modo emprendedora, y ambos entran a su flujo. | Falta un modo, o uno de los dos no abre. | RF-ACC-05 |
| A03 | Con una cuenta de prueba de emprendedora, inicia sesión, edita un dato de su tienda y el cambio se conserva. | No entra, o la tienda no guarda. | RF-ACC-01; RF-TIE-01 |
| A04 | Con esa cuenta, crea o edita un producto con foto y lo publica. | No puede crear ni editar, o no publica. | RF-PRO-01; RF-PRO-04 |
| A05 | Registra una venta y el stock o la pieza única se actualiza en el catálogo público. | La venta no se registra, o el catálogo no cambia. | RF-VEN-01; RF-VEN-02 |
| A06 | En modo comprador ve directorio, una tienda y la ficha de una feria. | Falta alguna de esas tres vistas. | RF-CMP-01; RF-CMP-02; RF-CMP-04 |
| A07 | Con una cuenta de comprador, sigue una tienda o asociación y, al confirmar esa tienda una feria (desde otra cuenta de prueba), llega una notificación push. | No puede seguir, o el push no llega. | RF-CMP-06; RF-CMP-07 |
| A08 | Con el tamaño de texto del sistema aumentado, las pantallas de acceso y tienda se siguen usando. | El layout se rompe o el texto queda ilegible. | RNF-USA-03 |
| A09 | Con la red cortada, informa el estado de la conexión y no pierde un dato que estaba ingresando (por ejemplo, al crear un producto o una venta). | No avisa, o al volver la red el dato desapareció. | RNF-REN-02 |
| A10 | La interfaz está en español de Chile. | Hay pantallas en otro idioma o con términos sin traducir. | RNF-IDI-01 |
| A11 | Firebase App Check está activo y rechaza (o marca) una solicitud que no proviene de la app legítima, o el grupo lo demuestra en la consola. | No hay App Check, o no se puede mostrar. | RNF-SEG-06 |

**Subtotal: 11**

---

## 2. Web

URL pública en Firebase Hosting. Computador y teléfono.

| ID | Criterio | No cumple si… | Sustento |
|:--:|----------|----------------|----------|
| W01 | La web abre desde su URL pública en un computador. | No hay URL pública, o no carga. | Entregable 6; criterio 1 |
| W02 | La misma URL se puede usar en el navegador del teléfono: directorio y una tienda se recorren sin quedar cortados. | En el teléfono no se puede navegar lo básico. | RNF-CPT-02; criterio 1 |
| W03 | El administrador inicia sesión y completa una operación de feria (publicar, invitar o marcar asistencia). | No entra, o no puede operar ferias. | RF-FER-01; RF-FER-02; RF-FER-07 |
| W04 | Con una cuenta de prueba de emprendedora, gestiona desde la web al menos un cambio de tienda, un producto o una venta, y el cambio se ve en la vitrina. | No puede operar su tienda desde la web. | RF-TIE-02 |
| W05 | Un visitante sin sesión recorre directorio, tienda y ficha de feria. | Alguna de esas vistas exige sesión. | RF-ACC-07; RF-CMP-01; RF-FER-10 |
| W06 | Una cuenta de emprendedora o de comprador con correo y contraseña puede recuperar su contraseña. | No hay recuperación, o no llega el correo de restablecimiento. | RF-ACC-10 |
| W07 | El administrador gestiona otra cuenta de administrador (crear, editar o desactivar). | No hay gestión de otros administradores. | RF-ADM-04 |
| W08 | Las acciones del administrador sobre cuentas, asociaciones o ferias quedan registradas (quién, qué y cuándo) y se pueden consultar. | No hay registro consultable. | RNF-SEG-07 |
| W09 | Solo son públicos los datos configurados como visibles en la tienda de prueba; hay un aviso o política de datos personales accesible desde la web. | Se exponen datos no publicados, o no hay aviso de datos personales. | RNF-PRI-03; RNF-PRI-01 |
| W10 | Siguiendo solo el manual del administrador, una persona del curso ajena al grupo publica o cancela una feria sin que el grupo le dicte los pasos. | No hay manual usable, o no logra la operación. | RNF-OPE-01 |
| W11 | La interfaz de la web está en español de Chile. | Hay pantallas en otro idioma o sin traducir. | RNF-IDI-01 |

**Subtotal: 11**

---

## 3. Cierre de la entrega

Documentos en `docs/` del repositorio del grupo, etiqueta `entrega-8` y demostración.

| ID | Criterio | No cumple si… | Sustento |
|:--:|----------|----------------|----------|
| C01 | La entrega está etiquetada `entrega-8` sobre el commit usado en la demo. | No hay etiqueta, o la demo no sale de ese commit. | RNF-MAN-04 |
| C02 | Demuestran la plataforma completa en la revisión (app y web) solo con cuentas de prueba del grupo, sin usuarias de la contraparte. | La demo depende de una emprendedora real, o no cubre app y web. | Entregable 8 |
| C03 | Un paso del manual de la emprendedora y un paso del manual del administrador se pueden seguir en la demo con las cuentas de prueba. | Los manuales no calzan con lo que se ve, o no se pueden seguir. | Entregable 7; RNF-OPE-01 |
| C04 | El informe de seguridad actualizado incluye pruebas de reglas con el emulador; el comando del README corre y pasa. | No hay pruebas, el comando falta o falla. | RNF-SEG-04; RNF-SEG-08 |
| C05 | El informe de seguridad incluye análisis de vulnerabilidades (app, web y dependencias) con gravedad y corrección o justificación de cada hallazgo. | Falta el análisis, o un hallazgo sin gravedad ni cierre. | RNF-SEG-05; RNF-SEG-08 |
| C06 | Ese informe cubre el producto completo, incluidas ferias, seguidores y mapas. | Solo revisa un subconjunto anterior a la entrega 7. | Entregable 3 |
| C07 | Existen casos de prueba de los criterios de aceptación de todos los requisitos Esenciales, cada uno con su resultado. | Faltan Esenciales sin caso, o casos sin resultado. | Entregable 4; criterio 2 |
| C08 | Hay una matriz de requisitos con el estado final de cada uno: cumplido, parcial o pendiente. | No hay matriz, o faltan requisitos base. | Entregable 5 |
| C09 | En la matriz, todos los Esenciales figuran como "cumplido" y cada uno apunta a su caso de prueba. | Algún Esencial está pendiente o sin caso. | Criterio 2 |
| C10 | Los Importantes no construidos figuran como pendientes, con justificación. | Un Importante falta sin justificación, o aparece como cumplido sin poder demostrarlo. | Criterio 2 |
| C11 | El README permite a una persona ajena al grupo clonar y ejecutar app y web desde cero, sin instrucciones orales del grupo. | El README está incompleto, o hace falta ayuda del grupo para arrancar. | RNF-MAN-01; criterio 3 |
| C12 | Hay manual breve orientado al perfil emprendedora y manual breve para el administrador. | Falta uno de los dos. | Entregable 7 |
| C13 | Hay una descripción de cómo se incorporaría la IA como módulo desacoplado, sin rehacer el flujo de creación de productos. | No está, o implica rehacer el flujo de productos. | RNF-MAN-02 |

**Subtotal: 13**

---

## Totales

| Bloque | Criterios |
|--------|:---------:|
| 1. App Android | 11 |
| 2. Web | 11 |
| 3. Cierre de la entrega | 13 |
| **Total** | **35** |

## Orden sugerido en la demo

1. Instalar el APK y recorrer acceso, tienda, producto, venta, comprador y push (A01–A07). Probar texto grande y corte de red (A08–A09).
2. Abrir la URL pública en computador y teléfono (W01–W05). Pendientes Importantes: recuperación, otros admins y bitácora (W06–W08).
3. Privacidad, idioma y una operación del administrador hecha por alguien ajeno con el manual (W09–W11).
4. Etiqueta, demo completa con cuentas de prueba y manuales seguibles (C01–C03).
5. Informe de seguridad: comando del emulador y hallazgos (C04–C06).
6. Casos de prueba, matriz y README ejecutado por alguien ajeno (C07–C11).
7. Manuales e IA desacoplada (C12–C13). Presentación ante el jurado el 26 sobre el commit `entrega-8`.

## Hoja por grupo

Marcar F en cada criterio en fallo. **Nota = 7,0 − 0,2 × F**, con piso 1,0.

| ID | ALERCEIS7 | BORA | SurCode | Fixmol |
|:--:|:---------:|:----:|:-------:|:------:|
| A01 | | | | |
| A02 | | | | |
| A03 | | | | |
| A04 | | | | |
| A05 | | | | |
| A06 | | | | |
| A07 | | | | |
| A08 | | | | |
| A09 | | | | |
| A10 | | | | |
| A11 | | | | |
| W01 | | | | |
| W02 | | | | |
| W03 | | | | |
| W04 | | | | |
| W05 | | | | |
| W06 | | | | |
| W07 | | | | |
| W08 | | | | |
| W09 | | | | |
| W10 | | | | |
| W11 | | | | |
| C01 | | | | |
| C02 | | | | |
| C03 | | | | |
| C04 | | | | |
| C05 | | | | |
| C06 | | | | |
| C07 | | | | |
| C08 | | | | |
| C09 | | | | |
| C10 | | | | |
| C11 | | | | |
| C12 | | | | |
| C13 | | | | |
| **Fallos** | | | | |
| **Nota** | | | | |
