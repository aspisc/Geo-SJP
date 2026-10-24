# Memoria de análisis geoespacial — PMF San Juan de los Potreros

**Fecha:** 2026-10-23
**Predio:** Comunidad Indígena de San Juan de los Potreros, Chimaltitán, Jalisco (RAN clave 14031001)
**CRS de trabajo:** EPSG:32613 (WGS84 UTM 13N)
**Norma:** NOM-152-SEMARNAT-2023

## Superficies de referencia verificadas

- Polígono RAN (comunal): **16,126.72 ha** (1 polígono, geometría válida).
- Zonificación (`zonif_final`): **16,126.70 ha**. Cubre el RAN completo, incluida la fracción en Zacatecas (RAN no cubierto por la zonificación = 6.43 ha de astillas de borde). *Corrige el supuesto de que la zonificación era solo de Jalisco.*
- Cobertura SAMOF 2020 (`Superficies.xlsx`): **15,986.60 ha**. Es producto estatal de Jalisco; el faltante de 140.13 ha (0.87 %) corresponde a la franja en Zacatecas, sin polígono SAMOF. Es cobertura/vegetación, **no** la clasificación legal.

## Cuadro 2 — Clasificación y cuantificación de superficies (4.7), escala comunal

Fuente: zonificación. Franja ribereña reclasificada como subclase 1c (clase I). Pendientes >45° recortadas de producción y restauración hacia la clase I.

| Clase NOM-152 | ha | % |
|---|---|---|
| I. Conservación y aprovechamiento restringido | 1,387.42 | 8.60 |
| &nbsp;&nbsp;a) Áreas naturales protegidas | 0.00 | 0.00 |
| &nbsp;&nbsp;Áreas de conservación comunitaria | 375.86 | 2.33 |
| &nbsp;&nbsp;c) Franja protectora de vegetación ribereña (subclase 1c) | 1,007.58 | 6.25 |
| &nbsp;&nbsp;d) Pendientes mayores al 100 % (45°) | 3.98 | 0.02 |
| &nbsp;&nbsp;e) Altitud mayor a 3,000 msnm | 0.00 | 0.00 |
| &nbsp;&nbsp;f) Manglar y bosque mesófilo | 0.00 | 0.00 |
| II. Producción | 8,507.67 | 52.76 |
| III. Restauración (incl. 118.65 de saneamiento) | 4,608.01 | 28.57 |
| IV. Protección forestal declarada por la Secretaría | 0.00 | 0.00 |
| V. Otros usos | 1,623.60 | 10.07 |
| **Total** | **16,126.70** | **100.00** |

## Relieve y pendientes (4.8.2) — DEM INEGI 15 m

Fuente: `DEM-15m.tif` del repositorio (EPSG:6365), reproyectado a EPSG:32613 a 15 m; pendiente por algoritmo de Horn.

- Altitud en el predio: mínima 1,676 m, media 2,108 m, mediana 2,119 m, máxima 2,412 m. Ninguna celda supera 3,000 msnm.
- Pendiente media 13.6°, máxima 72.7°.
- Distribución Van Zuidam (% de pendiente): 0–2: 290.1 ha; 2–7: 1,993.6; 7–15: 3,251.9; 15–30: 4,872.8; 30–70: 5,582.2; 70–140: 132.0; >140: 3.9.
- Pendiente >45° (100 %): 12.5 ha totales; 8.53 ya en clase I (ribereña/conservación), 3.98 recortadas (1.55 de producción + 2.43 de restauración).

## Vegetación (4.8.5.1) — INEGI Serie VII (fuente normativa), recorte al RAN

| Tipo (Serie VII) | ha | % |
|---|---|---|
| Bosque de encino (BQ) | 4,204.16 | 26.07 |
| Bosque de pino-encino (BPQ) | 3,888.84 | 24.11 |
| Bosque de encino-pino (BQP) | 3,572.04 | 22.15 |
| Pastizal inducido (PI) | 2,119.97 | 13.14 |
| Agricultura de temporal anual (TA) | 1,647.15 | 10.21 |
| Veg. secundaria arbustiva de pastizal (VSa/PN) | 438.52 | 2.72 |
| Veg. secundaria arbustiva de selva baja (VSa/SBC) | 255.93 | 1.59 |
| **Total** | **16,126.61** | **100.00** |

Forestal (BQ+BPQ+BQP) = 11,665.04 ha (72.3 %). La Serie VII cubre el predio completo, Zacatecas incluido, por lo que las 140 ha de SAMOF quedan subsumidas (sin faltante).

## Hidrología (4.8.5) — Red hidrográfica recortada al RAN

- Región Hidrológica 12 Lerma-Santiago, subregión Río Santiago, cuenca RH12-K Río Bolaños; subcuencas RH12Kd y RH12Ke.
- 433.60 km de cauces en 1,075 tramos; densidad de drenaje 2.69 km/km².
- Predominio intermitente (418.23 km) sobre perenne (15.17 km). Orden máximo 6 (Strahler).

## Clima, suelo y fisiografía (contexto, 4.8)

- Clima dominante templado subhúmedo C(w); temperatura media anual 18.1 °C; precipitación media anual 743 mm (IIEG 2018, base CONABIO). Pendiente de refinar con la carta de climas y/o estaciones representativas (excluyendo la estación del cañón de Bolaños por >1,000 m de diferencia altitudinal).
- Suelos dominantes a nivel municipal: Cambisol, Litosol/Leptosol, Luvisol, Feozem (IIEG 2018). A nivel predio: intersectar carta edafológica INEGI 1:50,000 (`Edafologia-50k-SJP.gpkg`).
- Geología dominante: toba y roca extrusiva ácida (vulcanismo de la Sierra Madre Occidental).
- Provincia fisiográfica: Sierra Madre Occidental (Cañón de Bolaños).

## Insumos geoespaciales en el repositorio

gpkg: CI San Juan, Caminos, Clima, Edafologia-50k, Edaf-SII, Red hídica, USV-Serie7, USV-Conafor 5000, Zonificacion-2020-CONAFOR, Zonificación Preliminar, UMAs Preliminar (sjp_um_siplafor, 157 UM), Geo-SJP. Rásters: DEM-15m (EPSG:6365), DEM (EPSG:4326). Zips: erosión eólica/hídrica, precipitación/temperatura media anual, provincias/subprovincias fisiográficas.

## Herramientas y métodos

geopandas / shapely / pyproj (vector, EPSG:32613, make_valid); rasterio (reproyección bilineal a 15 m); pendiente por método de Horn; clasificación de pendientes de Van Zuidam. Superficies por geometría, no por el campo HAS.

## Pendientes

- Fusionar la actualización 4.8.2 y 4.8.5 al 4.8 maestro (`PMF_SJP_Cap_4-8_Diagnostico_Fisico_completo.docx`, no disponible en la sesión).
- Subclase a/b de producción: tras cerrar la rodalización y correr SIPLAFOR.
- Restauración por bajas existencias: tras el inventario/SIPLAFOR.
- Umbral de generalización de la zonificación (25,044 fragmentos) antes del llenado cartográfico fino.
- Confirmación en laboratorio de *Phytophthora cinnamomi* sobre encino del predio.
- Verificar susceptibilidad de *Pinus lumholtzii*, *P. oocarpa*, *P. devoniana* al patógeno antes de comprometer la reconversión (4.11 y 4.17).
- SIPLAFOR: memoria y propuesta de texto por generar e ingresar.
