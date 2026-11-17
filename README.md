# Mapa de parroquias y concellos de la provincia de Lugo

Mapa interactivo con las **1.271 parroquias** y los **67 concellos** de la provincia de Lugo, dibujados con los **límites oficiales** de la Xunta de Galicia sobre una ortofoto o un mapa de carreteras.

👉 **Ver el mapa:** https://adry2342.github.io/mapa-parroquias-lugo/

Funciona en el ordenador y en el móvil, sin instalar nada.

---

## Cómo se usa

1. **Abre el enlace** de arriba en el navegador (Chrome, Safari, Firefox o Edge). La primera vez tarda unos segundos en descargar los límites; las siguientes veces abre casi al instante.
2. **Busca** una parroquia o un concello en la caja de búsqueda. No hace falta escribir tildes ni el nombre completo: con escribir `lanz`, `fonsa` o `san martino` ya salen las coincidencias. Toca el resultado y el mapa va hasta allí.
3. **Toca una parroquia** en el mapa para ver su ficha: concello al que pertenece, superficie exacta, puesto por tamaño dentro de su concello, nombre oficial y código.
4. **Cambia el fondo** con los botones de arriba a la derecha:
   - **Satélite:** foto aérea del Plan Nacional de Ortofotografía Aérea (PNOA), con carreteras, ríos y nombres de lugares.
   - **Carreteras:** Mapa Base del Instituto Geográfico Nacional.
5. **Elige cómo colorear** en el apartado *Colores*:
   - **Por parroquia:** cada parroquia de un color distinto al de sus vecinas, para distinguirlas.
   - **Por superficie:** naranja claro = parroquia pequeña, naranja oscuro = parroquia grande (con leyenda en km²).
   - **Por concello:** cada concello de un color.
6. **Elige qué concellos ver** en *Concellos visibles*: márcalos o desmárcalos, pulsa *Todos* o *Ninguno*, **Ir** para centrar uno o **Solo** para dejar únicamente ese.
7. **Exportar:** el botón *Descargar KML* guarda los concellos visibles con el máximo detalle oficial para abrirlos en Google Earth o importarlos en Google My Maps.

**En el móvil:** el panel está abajo. Toca o desliza hacia arriba la barra para abrirlo y hacia abajo para cerrarlo. El botón **?** muestra una ayuda rápida.

### Sin conexión o descargado

También puedes descargar el archivo `index.html` (botón verde *Code → Download ZIP* en GitHub) y abrirlo con doble clic. Necesita conexión a internet para descargar los límites y los fondos de mapa.

---

## Datos y fuentes

| Qué | Fuente | Licencia |
|---|---|---|
| Límites de parroquias y concellos | Instituto de Estudos do Territorio (IET), Xunta de Galicia — servicio *Límites administrativos*, edición de febrero de 2026 | Compatible con CC BY 4.0 |
| Nombres oficiales (para el contraste) | Nomenclátor de Galicia 2026 (Decreto 27/2026), portal Abert@s de la Xunta | Datos abiertos con atribución |
| Ortofoto | PNOA — Instituto Geográfico Nacional | CC BY 4.0 scne.es |
| Carreteras, ríos y nombres; Mapa Base | Instituto Geográfico Nacional | CC BY 4.0 ign.es |
| Librería de mapas | [Leaflet](https://leafletjs.com) | BSD-2-Clause |

Los límites **no están copiados en este repositorio**: el mapa los descarga en directo del servicio oficial de la Xunta cada vez que se actualiza la caché (como mucho cada 30 días), así que siempre muestra la edición vigente. Al acercarte a un concello se cargan sus límites a máximo detalle.

### Contraste realizado (17/11/2026)

- Las **1.271 parroquias** y los **67 concellos** del servicio de límites coinciden **uno a uno**, con el mismo nombre y advocación, con el Nomenclátor oficial de Galicia 2026.
- En cada concello, **la suma de las superficies de sus parroquias coincide con la del concello** (diferencia máxima: 0,002 %).
- Superficie provincial calculada: **9.862,6 km²** (cifra oficial publicada: 9.856 km²; diferencia del 0,07 % por el método de cálculo y la línea de costa). Concello de Lugo: 329,94 km² (IGE: 329,78 km²).
- Ejemplo de caso dudoso resuelto: en Vilalba hay **dos parroquias distintas** llamadas Lanzós — *Lanzós (San Martiño)*, 27,30 km², y *Lanzós (San Salvador)*, 2,15 km², formada por dos trozos separados.

Las superficies se calculan sobre el elipsoide a partir del límite oficial a máximo detalle.

---

## Aviso

Proyecto **personal y no oficial**. No está hecho, revisado ni avalado por la Xunta de Galicia ni por el Instituto Geográfico Nacional; solo utiliza sus datos abiertos citando la fuente, tal como piden sus licencias. Para cualquier trámite legal o administrativo, consulta siempre la fuente oficial ([mapas.xunta.gal](https://mapas.xunta.gal), [ign.es](https://www.ign.es)).

**Privacidad:** la página no usa cookies, publicidad ni sistemas de seguimiento. Solo guarda una copia de los límites en tu propio navegador para abrir más rápido.

---

## Detalles técnicos

- Una sola página (`index.html`) sin compilación ni servidor propio; se publica con GitHub Pages.
- Dibujo en *canvas* para mover con fluidez las 1.271 parroquias; nombres sin solaparse y que aparecen según el zoom.
- Vista general con límites simplificados (~10 m) y carga del máximo detalle (~0,5 m) solo de los concellos que se están mirando.
- Copia local de los datos en IndexedDB durante 30 días (se puede forzar la recarga en *Fuentes y verificación*).

## Licencia

El código de este proyecto se publica con licencia [MIT](LICENSE). Los datos y fondos de mapa pertenecen a sus autores y se usan según sus licencias (ver tabla de fuentes).
