# Checklist de revisión — Entrega 5

| Campo | Valor |
|-------|-------|
| Entrega | 5 — Catálogo, productos y ventas |
| Fecha planificada | Lunes 2 de noviembre de 2026 |
| Nota | Entrega 5, que pondera 35 % de la EVA 3 |
| Criterios | 35, solo funcionales. Cada fallo resta 2 décimas |
| Orden | App Android y web |
| Base | [Planificación, entrega 5](planificacion.md#entrega-5--catálogo-productos-y-ventas), [requisitos base](requerimientos-base.md) |

Cada criterio se marca **cumple** o **no cumple**. No hay puntaje intermedio. Se comprueba usándolo, en el celular o en el navegador.

## Premisas

1. **App:** la emprendedora crea productos, configura el catálogo y registra ventas.
2. **Web:** un visitante, sin instalar la app y sin iniciar sesión, ve el catálogo público de esa tienda y el efecto de lo que ella configuró o vendió. Crear y vender desde la web es de la entrega 6.
3. Entran solo comportamientos que se pueden mostrar. Informes, pruebas del emulador, Lint, MobSF, App Check, etiquetas de git y documentos no se califican aquí; quedan para la revisión final.
4. No entran directorio, filtros, QR, mapas ni contacto. Eso es la entrega 6. Sugerir la feria del día al vender es la entrega 7.

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

Con 15 fallos la entrega queda en 4,0. Ejemplo: fallan la galería (A03), la pieza única en la web (W12) y el filtro por feria (A22). Son 3 fallos: 7,0 − 0,6 = **6,4**.

---

## 1. App Android

La emprendedora, con su sesión.

### 1.1 Crear un producto

| ID | Criterio | No cumple si… | Sustento |
|:--:|----------|----------------|----------|
| A01 | El alta es un flujo guiado, paso a paso: foto, datos, variantes si tiene, disponibilidad y publicación. | Es un solo formulario sin guía, o falta uno de esos pasos. | RF-PRO-01 |
| A02 | La foto se toma con la cámara. | No hay captura desde la cámara. | RF-PRO-01 |
| A03 | La foto se elige desde la galería. | No hay selección desde la galería. | RF-PRO-01 |
| A04 | Guarda nombre, descripción, categoría, precio y tipo de producto, además de las fotos. | Falta uno de esos datos al reabrir el producto. | RF-PRO-02 |
| A05 | Al elegir el tipo de producto, aparecen los campos específicos definidos en el levantamiento. | El tipo no cambia los campos. | RF-PRO-03 |
| A06 | Una variante guarda su propio precio, su propia foto y su propio stock. | Comparte precio, foto o stock con otra variante. | RF-PRO-05 |
| A07 | Elige la modalidad: regular, a pedido o pieza única. | Falta alguna de las tres. | RF-PRO-06 |
| A08 | Define si el producto maneja stock o no. | No se puede dejar un producto sin control de stock. | RF-PRO-07 |
| A09 | Si maneja stock, elige qué pasa al agotarse: mostrar "agotado", ocultar o pasar a "a pedido". | Falta alguna de las tres opciones. | RF-PRO-08 |
| A10 | Lo marca disponible o no disponible. El no disponible sigue en su tienda. | No se puede marcar, o desaparece también de su tienda. | RF-PRO-09; RN-09 |
| A11 | Si cierra la app a mitad de la creación y vuelve a abrirla, encuentra lo ya ingresado. | El flujo interrumpido parte de cero. | RNF-USA-04 |

**Subtotal: 11**

### 1.2 Catálogo y ventas

| ID | Criterio | No cumple si… | Sustento |
|:--:|----------|----------------|----------|
| A12 | Edita un producto y, al volver a abrirlo, el cambio sigue. | La edición no se guarda. | RF-PRO-04 |
| A13 | Elimina un producto y deja de verse en su catálogo. | No se puede eliminar, o reaparece en su tienda. | RF-PRO-04 |
| A14 | Cambia la disponibilidad de varios productos a la vez (selección, categoría o catálogo completo). | Solo puede cambiar de a uno. | RF-PRO-10 |
| A15 | Un producto nuevo nace con los valores por defecto que ella definió. | Cada alta parte sin esos valores. | RF-PRO-11 |
| A16 | La vista previa del catálogo en la app muestra cada producto según su modalidad, stock, "al agotarse" y visibilidad. | La vista previa ignora alguna de esas configuraciones. | RF-PRO-12 |
| A17 | Sin red consulta su catálogo. Al volver la conexión, lo que cambió sin red queda guardado. | Sin red no ve el catálogo, o esos cambios se pierden. | RNF-DAT-03 |
| A18 | Registra una venta con producto, variante (si tiene) y cantidad. | Falta alguno de esos datos. | RF-VEN-01 |
| A19 | La venta descuenta solo el stock de la variante vendida. | Descuenta otra, todas, o ninguna. | RF-VEN-01 |
| A20 | El historial de ventas se activa o se desactiva en la configuración. | No hay interruptor. | RF-CFG-06 |
| A21 | Con el historial activo, la venta guarda precio, fecha y lugar (feria de la plataforma u otro lugar). | Falta precio, fecha o lugar. | RF-VEN-03 |
| A22 | Consulta el historial filtrando por fecha, por feria y por producto. | Falta uno de los tres filtros. | RF-VEN-04 |

**Subtotal: 11**

---

## 2. Web

Visitante sin sesión, en la página pública de la tienda. Los datos los cargó la emprendedora en la app.

| ID | Criterio | No cumple si… | Sustento |
|:--:|----------|----------------|----------|
| W01 | Ve el nombre del producto publicado. | El producto publicado en la app no aparece en la web. | RF-PRO-12 |
| W02 | Ve la foto del producto. | La ficha web no muestra la foto. | RF-PRO-02 |
| W03 | Ve la descripción. | La ficha web no muestra la descripción. | RF-PRO-02 |
| W04 | Ve el precio. | La ficha web no muestra el precio. | RF-PRO-02 |
| W05 | Ve la categoría o el tipo de producto. | No se distingue qué tipo de producto es. | RF-PRO-02 |
| W06 | Al elegir una variante, ve el precio de esa variante. | Sigue mostrando el precio de otra variante. | RF-PRO-05 |
| W07 | Al elegir una variante, ve la foto de esa variante. | Sigue mostrando la foto de otra variante. | RF-PRO-05 |
| W08 | Un producto marcado no disponible no aparece. Sigue en la tienda de la emprendedora, en la app. | Aparece en la web, o también desapareció de su app. | RF-PRO-09; RN-09 |
| W09 | Con "mostrar agotado", al llegar el stock a cero el producto sigue en la web con la indicación de agotado. | Desaparece, o sigue como si hubiera stock. | RF-PRO-08 |
| W10 | Con "ocultar", al llegar el stock a cero el producto deja de aparecer en la web. | Sigue visible para el visitante. | RF-PRO-08 |
| W11 | Con "pasar a pedido", al llegar el stock a cero el producto sigue en la web identificado como a pedido. | Desaparece, o no se distingue de uno con stock. | RF-PRO-08 |
| W12 | Una pieza única vendida no aparece en la web y, al recargar más tarde, sigue sin aparecer. | Sigue publicada, o vuelve a publicarse sola. | RF-VEN-02; RN-08 |
| W13 | Un producto editado en la app (nombre o precio) se ve actualizado en la web al recargar. | La web muestra el dato anterior. | RF-PRO-04; RF-PRO-12 |

**Subtotal: 13**

---

## Totales

| Bloque | Criterios |
|--------|:---------:|
| 1. App Android | 22 |
| 2. Web | 13 |
| **Total** | **35** |

## Orden sugerido en la demo

1. En la app, crear un producto con foto, tipo, variante y stock (A01–A11). Cerrar a mitad y retomar.
2. Editar, borrar, cambio masivo, valores por defecto y vista previa (A12–A16). Cortar la red y volver (A17).
3. En la web, abrir la tienda sin sesión y recorrer W01–W07.
4. En la app, marcar no disponible, agotar con cada opción y vender una pieza única. En la web, comprobar W08–W12.
5. Activar el historial, anotar precio, fecha y lugar, y filtrar (A20–A22). Editar el precio y recargar la web (W13).

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
| A12 | | | | |
| A13 | | | | |
| A14 | | | | |
| A15 | | | | |
| A16 | | | | |
| A17 | | | | |
| A18 | | | | |
| A19 | | | | |
| A20 | | | | |
| A21 | | | | |
| A22 | | | | |
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
| **Fallos** | | | | |
| **Nota** | | | | |
