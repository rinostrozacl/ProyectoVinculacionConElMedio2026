# Checklist de revisión — Entrega 6

| Campo | Valor |
|-------|-------|
| Entrega | 6 — Vitrina, modo comprador, difusión y mapas |
| Fecha de revisión | Miércoles 18 de noviembre de 2026 |
| Nota | Entrega 6, que pondera 50 % de la EVA 4 |
| Criterios | 35, solo funcionales. Cada fallo resta 2 décimas |
| Orden | Web y app Android |
| Base | [Planificación, entrega 6](planificacion.md#entrega-6--vitrina-modo-comprador-difusión-y-mapas), [requisitos base](requerimientos-base.md) |

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

Con 15 fallos la entrega queda en 4,0. Ejemplo: fallan el filtro por sector (W02), el QR de la feria (A10) y el mapa sin permiso (A14). Son 3 fallos: 7,0 − 0,6 = **6,4**.

---

## 1. Web

### 1.1 Vitrina pública

Visitante sin sesión. En el computador y, donde se indica, en el teléfono.

| ID | Criterio | No cumple si… | Sustento |
|:--:|----------|----------------|----------|
| W01 | Ve un directorio de emprendedoras y de asociaciones. | Falta uno de los dos listados, o exige iniciar sesión para verlos. | RF-CMP-01 |
| W02 | Busca en el directorio y filtra por tipo de emprendimiento, por sector y por asociación. | No hay búsqueda, o falta uno de los tres filtros. | RF-CMP-01 |
| W03 | Abre la tienda y ve su catálogo público. | La tienda no muestra los productos publicados. | RF-CMP-02 |
| W04 | En el detalle de un producto, al elegir una variante ve la foto y el precio de esa variante. | La foto o el precio no cambian con la variante. | RF-CMP-03 |
| W05 | Abre una asociación y ve a sus integrantes, con acceso a la tienda de cada una. | No lista integrantes, o no se llega a sus tiendas. | RF-ASO-03 |
| W06 | Contacta a la emprendedora por la vía que ella dejó: WhatsApp, formulario o ambos. | Ofrece una vía que ella no configuró, o no ofrece la que sí configuró. | RF-CMP-05; RF-CFG-02 |
| W07 | Si ella ocultó los precios, se ve "Consultar precio" y no el monto. | El precio sigue visible. | RF-CFG-01 |
| W08 | El directorio y la tienda se pueden usar en el navegador del teléfono, sin que el contenido quede cortado o inaccesible. | En el teléfono no se puede recorrer o no se puede tocar lo necesario. | RNF-CPT-02 |

**Subtotal: 8**

### 1.2 Administración

| ID | Criterio | No cumple si… | Sustento |
|:--:|----------|----------------|----------|
| W09 | La emprendedora edita la ficha de su tienda en la web y el cambio se ve en la tienda pública. | No puede editarla, o la vitrina sigue con el dato anterior. | RF-TIE-02 |
| W10 | La emprendedora crea o edita un producto en la web y el resultado se ve en el catálogo público. | No puede hacerlo desde la web, o el catálogo no cambia. | RF-TIE-02 |
| W11 | La emprendedora registra una venta en la web y el catálogo público refleja el stock descontado o la pieza única retirada. | La venta no se puede registrar, o el catálogo no cambia. | RF-TIE-02 |
| W12 | El administrador elige la navegación anónima de la app: permitir, invitar con opción de omitir, u obligar el ingreso con Google. La opción elegida queda guardada. | Falta una de las tres opciones, o al recargar vuelve a la anterior. | RF-ADM-02 |
| W13 | El administrador crea una feria con nombre, descripción, imagen, lugar, fecha, horario y organizador. | Falta uno de esos datos. | RF-FER-01 |
| W14 | Al crear o editar la feria, fija la ubicación marcando un punto en el mapa o buscando la dirección. | No hay mapa ni búsqueda de dirección. | RF-MAP-01 |
| W15 | Edita la feria y, al volver a abrirla, los cambios siguen. | La edición no se guarda. | RF-FER-01 |
| W16 | La ficha pública de la feria muestra un mapa con su ubicación. | No hay mapa, o el punto no corresponde al lugar fijado. | RF-MAP-02 |
| W17 | "Cómo llegar" abre la aplicación de mapas del celular en ese lugar. | El control no está, o abre un mapa sin la ubicación de la feria. | RF-MAP-02 |

**Subtotal: 9**

---

## 2. App Android

### 2.1 Modo comprador

| ID | Criterio | No cumple si… | Sustento |
|:--:|----------|----------------|----------|
| A01 | Ve el directorio de emprendedoras y de asociaciones. | Falta uno de los dos listados. | RF-CMP-01 |
| A02 | Busca y filtra por tipo de emprendimiento, por sector y por asociación. | No hay búsqueda, o falta uno de los tres filtros. | RF-CMP-01 |
| A03 | Abre la tienda y ve su catálogo público. | La tienda no muestra los productos publicados. | RF-CMP-02 |
| A04 | Al elegir una variante ve su foto y su precio. | La foto o el precio no cambian con la variante. | RF-CMP-03 |
| A05 | Abre una asociación, ve a sus integrantes y entra a la tienda de una de ellas. | No lista integrantes, o no se llega a una tienda. | RF-ASO-03 |
| A06 | Contacta por la vía configurada: WhatsApp, formulario o ambos. | No respeta la configuración de la emprendedora. | RF-CMP-05 |
| A07 | Con los precios ocultos, ve "Consultar precio" y no el monto. | El precio sigue visible. | RF-CFG-01 |
| A08 | Sin sesión, la app obedece la opción guardada por el administrador: deja entrar, invita a Google con posibilidad de omitir, u obliga el ingreso con Google. Se prueban las tres. | Alguna de las tres no cambia el comportamiento al abrir. | RF-ACC-06 |

**Subtotal: 8**

### 2.2 Difusión, configuración y mapas

| ID | Criterio | No cumple si… | Sustento |
|:--:|----------|----------------|----------|
| A09 | Comparte tienda, producto y asociación con el menú nativo de Android. El enlace, abierto sin sesión, muestra la página web correspondiente. | Falta uno de los tres, o el enlace no abre esa página sin sesión. | RF-COM-01; RF-COM-03 |
| A10 | Genera el QR de una tienda, de una asociación y de una feria, y lo guarda o lo comparte como imagen. Al abrirlo se ve la página web sin sesión. | Falta un QR, no se puede guardar ni compartir, o no abre la web. | RF-COM-02; RF-COM-03 |
| A11 | En la ficha de una feria ve el mapa con su ubicación y "Cómo llegar" abre la aplicación de mapas. | No hay mapa, o "Cómo llegar" no lleva a ese lugar. | RF-MAP-02 |
| A12 | En el modo comprador, un mapa muestra las próximas ferias. | No hay mapa de ferias, o no aparecen las creadas. | RF-MAP-03 |
| A13 | Si autoriza la ubicación, el mapa se centra en su posición y las ferias quedan de la más cercana a la más lejana. | No muestra su posición, o el orden no es por distancia. | RF-MAP-03 |
| A14 | Si rechaza el permiso, el mapa sigue disponible y las ferias se ordenan por fecha, sin error que impida usarlo. | La pantalla falla, o no muestra las ferias. | RF-MAP-03; RNF-PRI-04 |
| A15 | El permiso de ubicación se pide al abrir el mapa, no al iniciar la app. | Lo pide al abrir la app, antes de entrar al mapa. | RNF-PRI-04 |
| A16 | La emprendedora define si los precios se muestran y elige el contacto: WhatsApp, formulario o ambos. El visitante ve ese resultado. | No puede cambiar precios o contacto, o el visitante no ve el cambio. | RF-CFG-01; RF-CFG-02 |
| A17 | Ve en la app los contactos que llegaron por el formulario. | El formulario en la vitrina no deja un mensaje consultable en la app. | RF-CFG-03 |
| A18 | Puede marcar en un mapa un punto de venta o de retiro. Si lo marca, el visitante lo ve en la tienda. | No puede marcarlo, o al marcarlo la tienda no lo muestra. | RF-MAP-04 |

**Subtotal: 10**

---

## Totales

| Bloque | Criterios |
|--------|:---------:|
| 1. Web | 17 |
| 2. App Android | 18 |
| **Total** | **35** |

## Orden sugerido en la demo

1. Web, sin sesión: directorio, búsqueda, filtros, tienda, variante, asociación y contacto (W01–W08).
2. Web, emprendedora: editar tienda, producto y una venta (W09–W11).
3. Web, administrador: navegación anónima, crear feria con mapa, editarla y abrir "Cómo llegar" (W12–W17).
4. App, comprador: las mismas vistas y las tres opciones de entrada (A01–A08).
5. App: compartir, QR, mapa de ferias con permiso y sin permiso (A09–A15).
6. App, emprendedora: ocultar precios, dejar solo formulario, revisar la bandeja y marcar un punto de retiro (A16–A18).

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
| A18 | | | | |
| **Fallos** | | | | |
| **Nota** | | | | |
