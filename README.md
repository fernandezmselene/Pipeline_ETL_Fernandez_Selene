# Pipeline_ETL_Fernandez_Selene

Este entregable aborda la extracción, transformación y carga (ETL) de datos comerciales en Power BI Desktop. El objetivo principal es garantizar la calidad de los datos, estandarizar tipos, resolver inconsistencias y estructurar un modelo de datos analítico eficiente.


## Principales Transformaciones Aplicadas

1. **Gestión de duplicados y Claves Primarias**: Eliminación de registros duplicados en `id_cliente` e `id_producto` para asegurar la unicidad en las tablas dimensionales (`Dim_Clientes`, `Dim_Productos`).
2. **Tratamiento y asignación de valores nulos**:
   * **Clientes**: Asignación del valor `"Sin Dato"` en atributos opcionales (`email`, `ciudad`) para preservar las ventas históricas asociadas sin descartar registros.
   * **Productos**: Asignación de la categoría basada en la jerarquía del catálogo y del atributo `precio` para garantizar la continuidad en el cálculo de métricas financieras.
3. **Estandarización y Modelado**:
   * Conversión de tipos de datos (`Date`, `Decimal Number`, `Whole Number`, `Text`).
   * Enriquecimiento de la tabla de hechos (`Fact_Ventas`) mediante operaciones de `Merge` con la dimensión de productos para incorporar el nombre y la categoría del producto sin duplicar tablas.


## Documentación en Lenguaje M
Las consultas principales contienen comentarios integrados en el **Editor Avanzado** que justifican algunos pasos del pipeline de transformación.
