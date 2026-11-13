# Checklist de revisión — Entrega 7

| Campo | Valor |
|-------|-------|
| Entrega | 7 — Ferias, seguidores y notificaciones |
| Fecha de revisión | Lunes 23 de noviembre de 2026 |
| Nota | Entrega 7, que pondera 50 % de la EVA 4 |
| Criterios | 35, solo funcionales. Cada fallo resta 2 décimas |
| Orden | Web y app Android |
| Base | [Planificación, entrega 7](planificacion.md#entrega-7--ferias-seguidores-y-notificaciones), [requisitos base](requerimientos-base.md) |

Cada criterio se marca **cumple** o **no cumple**. No hay puntaje intermedio. Se comprueba usándolo, en el navegador o en el celular.

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

Con 15 fallos la entrega queda en 4,0. Ejemplo: fallan el recordatorio (W09), el push (A13) y el horario de contacto (A15). Son 3 fallos: 7,0 − 0,6 = **6,4**.

---

## 1. Web

### 1.1 Gestión de ferias

Administrador, con una feria ya creada desde la entrega 6.

| ID | Criterio | No cumple si… | Sustento |
|:--:|----------|----------------|----------|
| W01 | Publica la feria. Tras publicarla, queda visible para quien navega sin sesión. | No hay publicación, o tras publicarla un visitante no la ve. | RF-FER-01 |
| W02 | Cancela la feria. Tras cancelarla, deja de ofrecerse como feria activa. | No se puede cancelar, o sigue apareciendo como activa. | RF-FER-01 |
| W03 | Invita a una emprendedora a la feria. | No hay invitación a emprendedoras. | RF-FER-02 |
| W04 | Invita a una asociación a la feria. | No hay invitación a asociaciones. | RF-FER-02 |
| W05 | Agrega directamente una emprendedora o una asociación, sin pasar por invitación. | Solo puede invitar, no agregar. | RF-FER-03 |
| W06 | El checklist muestra los estados: invitada, confirmada, rechazada y agregada por el administrador. | Falta alguno de esos estados. | RF-FER-04 |
| W07 | Cuando la emprendedora responde "Participo" en la app, el checklist pasa a "Confirmada". | El checklist no cambia, o cambia a otro estado. | RF-FER-04; criterio 1 |
| W08 | En el checklist busca y filtra por estado, tipo de emprendimiento y asociación. | Falta la búsqueda o uno de los tres filtros. | RF-FER-05 |
| W09 | Envía un recordatorio a quienes aún no han respondido. | No hay envío a las pendientes. | RF-FER-06 |
| W10 | Envía un aviso a las confirmadas. | No hay envío a las confirmadas. | RF-FER-06 |
| W11 | El día de la feria registra la asistencia: asistió o no asistió. | No se puede marcar la asistencia real. | RF-FER-07 |

**Subtotal: 11**

### 1.2 Ficha pública, calendario y seguidores

| ID | Criterio | No cumple si… | Sustento |
|:--:|----------|----------------|----------|
| W12 | La ficha pública de la feria lista a las participantes confirmadas. | No muestra confirmadas, o muestra también a quien rechazó. | RF-FER-10 |
| W13 | En esa ficha se ve una muestra del catálogo público de cada confirmada. | No hay muestra de productos, o muestra productos no públicos. | RF-FER-10 |
| W14 | Un visitante ve el calendario de próximas ferias y abre la ficha de una. | No hay calendario, o no se puede abrir la ficha. | RF-CMP-04 |
| W15 | Un comprador con sesión sigue una tienda o una asociación. | No se puede seguir. | RF-CMP-06 |
| W16 | Un visitante sin sesión intenta seguir: se le pide iniciar sesión y, al volver, ya queda siguiendo sin repetir la acción. | No pide sesión, o tras entrar hay que volver a pulsar seguir. | RF-ACC-08; criterio 3 |
| W17 | Deja de seguir esa tienda o asociación. | No se puede dejar de seguir. | RF-CMP-06 |
| W18 | Cuando una tienda o asociación que sigue confirma su participación, recibe el aviso por notificación del navegador (si dio permiso) o por correo. | No llega ningún aviso en la web. | RF-CMP-08 |

**Subtotal: 7**

---

## 2. App Android

### 2.1 Ferias de la emprendedora

| ID | Criterio | No cumple si… | Sustento |
|:--:|----------|----------------|----------|
| A01 | Recibe la invitación a la feria como notificación en la app. | La invitación no llega, o solo aparece si ella abre la app por su cuenta. | RF-FER-08 |
| A02 | Responde "Participo" con un toque. | La respuesta pide varios pasos, o no queda registrada. | RF-FER-08 |
| A03 | Responde "No participo" con un toque. El checklist web pasa a "Rechazada". | No puede rechazar, o el checklist no refleja el rechazo. | RF-FER-08; RF-FER-04 |
| A04 | Ve un calendario de las ferias a las que está invitada o confirmada. | No hay calendario, o no aparecen esas ferias. | RF-FER-09 |
| A05 | Al registrar una venta el mismo día de una feria en que está confirmada, la app sugiere esa feria como lugar. | No sugiere la feria, o sugiere una en la que no está confirmada. | RF-VEN-05 |
| A06 | Si autorizó la ubicación y está en una feria en curso en la que está confirmada, la app sugiere esa feria al vender. | Con permiso y en el lugar, no sugiere esa feria. | RF-MAP-05 |

**Subtotal: 6**

### 2.2 Ficha pública, seguidores, avisos y configuración

| ID | Criterio | No cumple si… | Sustento |
|:--:|----------|----------------|----------|
| A07 | En el modo comprador, la ficha de la feria muestra a las confirmadas y una muestra de su catálogo público. | Falta la lista o la muestra de productos. | RF-FER-10 |
| A08 | Comparte la feria con el menú nativo o genera su QR. El enlace o el QR abre la ficha web sin sesión. | No se puede compartir ni generar el QR, o no abre la web. | RF-COM-01; RF-COM-02; RF-COM-03 |
| A09 | El comprador sigue una tienda. | No se puede seguir desde la app. | RF-CMP-06 |
| A10 | El comprador sigue una asociación. | No se puede seguir una asociación. | RF-CMP-06 |
| A11 | Deja de seguir una tienda o una asociación. | No se puede dejar de seguir. | RF-CMP-06 |
| A12 | Sin sesión, al intentar seguir se le pide iniciar sesión con Google y, al volver, ya queda siguiendo sin repetir la acción. | No pide sesión, o tras entrar hay que volver a pulsar seguir. | RF-ACC-08 |
| A13 | Cuando una tienda o asociación que sigue confirma su participación, recibe una notificación push con el nombre de la feria. | No llega el push, o llega sin identificar la feria. | RF-CMP-07; criterio 2 |
| A14 | Antes de recibir avisos, da un consentimiento explícito, y puede dejar de seguir o darse de baja. | Los avisos llegan sin consentimiento, o no hay forma de cortarlos. | RNF-PRI-02 |
| A15 | Activa o desactiva las notificaciones de contacto y define un horario. Fuera de horario, el contacto del formulario se guarda sin notificar. | No hay horario, o fuera de horario igual notifica. | RF-CFG-04 |
| A16 | Activa o desactiva las calificaciones de su tienda. | No hay interruptor de calificaciones. | RF-CFG-05 |
| A17 | Con las calificaciones activas, el comprador califica la tienda o un producto. Con ellas desactivadas, no puede calificar. | No se puede calificar estando activas, o se puede calificar estando desactivadas. | RF-CMP-09; RF-CFG-05 |

**Subtotal: 11**

---

## Totales

| Bloque | Criterios |
|--------|:---------:|
| 1. Web | 18 |
| 2. App Android | 17 |
| **Total** | **35** |

## Orden sugerido en la demo

1. Web, administrador: publicar, invitar, agregar, checklist y filtros (W01–W08).
2. App, emprendedora: notificación, "Participo" / "No participo" y calendario (A01–A04). Volver al checklist web (W07).
3. Web: recordatorios, avisos a confirmadas y asistencia (W09–W11).
4. Web y app, ficha pública: confirmadas y muestra de catálogo (W12–W14, A07–A08).
5. Seguir sin sesión y con sesión, en web y app; dejar de seguir (W15–W17, A09–A12).
6. Confirmar participación y comprobar push y aviso web (A13, W18). Consentimiento (A14).
7. Venta con sugerencia de feria por fecha y por ubicación (A05–A06).
8. Horario de contactos y calificaciones (A15–A17).

## Hoja por grupo

Marcar F en cada criterio en fallo. **Nota = 7,0 − 0,2 × F**, con piso 1,0.

| ID | ALERCEIS7 | BORA | SurCode | Fixmol |
|:--:|:---------:|:----:|:-------:|:------:|
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
| W12 | | | | |
| W13 | | | | |
| W14 | | | | |
| W15 | | | | |
| W16 | | | | |
| W17 | | | | |
| W18 | | | | |
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
| A12 | | | | |
| A13 | | | | |
| A14 | | | | |
| A15 | | | | |
| A16 | | | | |
| A17 | | | | |
| **Fallos** | | | | |
| **Nota** | | | | |
