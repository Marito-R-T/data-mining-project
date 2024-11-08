
# Análisis de datos de estudiantes de educación formal (2023)

## Documentación técnica

Para el análisis se utilizaron las siguientes bibliotecas en R:

- **haven**: Para importar datos en formato SPSS (.sav).
- **arules**: Para ejecutar el algoritmo Apriori.
- **ggplot2 y ggalt**: Para la visualización de gráficos.
- **kmeans**: Algoritmo de agrupamiento utilizado para la segmentación de datos.

```r
# Ejemplo de cómo cargar bibliotecas en R
install.packages("haven")
library("arules")
library("haven")
library("ggplot2")
library("ggalt")
```

---

## 1. Análisis de Reglas de Asociación Apriori
### Se realizo en base a la población de básico

Las reglas de asociación Apriori ayudan a identificar patrones entre variables en los datos educativos.
Las cuatro reglas más importantes encontradas son:

1. **Regla 1**: Si el área es urbana, es más probable que el sector no sea público.
   **Interpretación**: Esta relación sugiere que los estudiantes en áreas urbanas tienen mayor acceso a instituciones privadas.

2. **Regla 2**: La jornada no matutina tiene una relación significativa con el sector privado.
   **Interpretación**: Esto podría deberse a la flexibilidad horaria en instituciones privadas.

3. **Regla 3**: Si el estudiante es de origen mestizo/ladino, es más probable que su jornada no sea matutina aunque no es crucial.
   **Interpretación**: Refleja posibles preferencias o limitaciones culturales o económicas en horarios de estudio.

4. **Regla 4**: Los estudiantes mestizo/ladinos generalmente no pertenecen al sector público.
   **Interpretación**: Muestra un posible sesgo hacia el acceso a instituciones privadas para la población maya, garifuna y Xinca.

---

## 2. Reglas de Asociación FP-Growth
### Se realizo en base a la población de diversificado

FP-Growth es una alternativa eficiente para el análisis de patrones frecuentes. Las cuatro reglas clave encontradas con FP-Growth son:

1. **Regla 1**: Los estudiantes de determinados departamentos (como Guatemala y El Progreso) son menos propensos a pertenecer al sector público.
   **Interpretación**: Podría reflejar una mayor disponibilidad de opciones privadas en estos departamentos.

2. **Regla 2**: Si el sector no es público, existe una alta probabilidad de que el estudiante pertenezca a una población ladina.
   **Interpretación**: Es posible que estudiantes de la población ladina prefieran el sector privado.

3. **Regla 3**: El sector privado tiende a ofrecer más jornadas no matutinas.
   **Interpretación**: Podría ser una estrategia para atraer estudiantes con necesidades de horario flexible.

4. **Regla 4**: Es probable que los estudiantes de jornadas matutinas pertenezcan a la población mestiza/ladina.
   **Interpretación**: Esto puede ser indicativo de un sesgo cultural en cuanto a las preferencias de horario.

---

## 3. Análisis de Clustering (K-means)
### Se realizo en base a la población en general

El clustering K-means permite identificar grupos de estudiantes con características similares. A continuación, se presentan los segmentos principales relacionados con una problemática identificada:

1. **Idea 1**: Estudiantes del sector público en áreas rurales.
   **Correlación**: Este grupo tiene limitaciones en acceso a recursos.

2. **Idea 2**: Estudiantes en áreas urbanas con preferencia por el sector privado.
   **Correlación**: Relacionado con un acceso socioeconómico superior.

3. **Idea 3**: Estudiantes en jornadas no matutinas del sector privado.
   **Correlación**: Posible conexión con actividades extracurriculares o empleo.

4. **Idea 4**: Estudiantes de origen maya en áreas rurales.
   **Correlación**: Indica una brecha en acceso y calidad educativa comparado con áreas urbanas.

4. **Idea 5**: Estudiantes dependiendo del departamento al que pertenecen están segmentados en regiones, y cada región tiene más ingerencia ya sea en el un sector u otro, como también en un área u otra área.
   **Correlación**: Indica una diferencia entre regiones y su acceso y pertenencia de los estudiantes a sectores o áreas mayoritariamente dependiendo de la región a la que pertenezcan. Por ejemplo la región central tiene mayor diferencia en que tienen mayor presencia en el sector privado y pertenecen mayoritariamente a áreas urbanas.

**Interpretación de los Resultados**:  
La segmentación permite entender diferentes factores que afectan a cada grupo, proporcionando una base para estrategias educativas adaptadas.

---

## 4. Propuestas para Abordar la Problemática Identificada

Basadas en los resultados del análisis de datos y en la investigación realizada, se proponen estrategias concretas para abordar los problemas identificados:

1. **Propuesta 1**: Implementación de programas de becas y subsidios para estudiantes en áreas rurales.
   - **Justificación**: Mejoraría el acceso a instituciones de mayor calidad y reduciría la brecha urbano-rural.

2. **Propuesta 2**: Flexibilidad en horarios de estudio para estudiantes del sector público en áreas rurales.
   - **Justificación**: Beneficiaría a aquellos que deben trabajar o tienen responsabilidades familiares.

3. **Propuesta 3**: Fomento de la inclusión educativa para poblaciones mayas mediante programas específicos.
   - **Justificación**: Facilitaría el acceso en el sistema educativo y mayor igualdad en este acceso.

3. **Propuesta 4**: Alternativas entre departamentos para entregar planes de estudios más orientadas a la región a la que pertenece el establecimiento y dar mejores oportunidades a regiones más exteriores a la capital.
   - **Justificación**: Facilitaría el acceso en el sistema educativo y mayor igualdad en este acceso a nivel regiones.

**Investigación de Contexto Guatemalteco**:  
Estas propuestas es necesario verlas desde el contexto Guatemalteco, lo que se realizó en este análisis, considerando factores culturales, económicos y sociales. Aún así no se encontrarón factores completamente determinantes y extremos,

---

**Referencias**  
1. `Documentación científica sobre inclusión y acceso a la educación en zonas rurales`
2. `Estudios de contexto guatemalteco sobre el sector educativo y brechas socioeconómicas`
