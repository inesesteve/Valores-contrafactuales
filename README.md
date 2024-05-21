# Valores y experimentos contrafactuales
**Autoras**: *iesmom@alumni.uv.es* y *anrome2@alumni.uv.es*

## Motivación del trabajo y objetivos
El propósito principal de este trabajo es explorar el uso de valores contrafactuales en el contexto del machine learning. Buscamos comprender cómo estos valores pueden aprovechar el conocimiento recogido en modelos de aprendizaje automático para mejorar su interpretabilidad y capacidad de generalización.

## Descripción
A través de la implementación de métodos específicos en la librería Alibi Explain, buscamos proporcionar una plataforma para calcular y explorar estos valores en diversos conjuntos de datos y escenarios de aplicación.

## Definición
Un **contrafactual** trata de responder a la pregunta "¿Por qué el modelo hizo esta predicción?" a través de la exploración de cómo una instancia de entrada podría haber sido modificada mínimamente para que el modelo emitiera una predicción diferente. Su valor asociado mide el impacto que tendría un suceso determinado diferente al observado

## Métodos para obtener contrafactuales
La librería Alibi Explain expone cuatro métodos para la búsqueda de contrafactuales, los cuales hemos integrado en este proyecto junto con diversos ejemplos de uso de la propia libería donde, cada uno de estos métodos aborda la interpretabilidad de manera ligeramente diferente.

1. **Instancias contrafactuales (CFI)**: genera instancias alternativas o contrafactuales modificando las características de una instancia de entrada, manteniendo la clase de salida igual o cambiándola según sea necesario. Es útil para comprender cómo pequeños cambios en las características de entrada afectan las predicciones del modelo.
   
2. **Explicaciones contrastivas (CEM)**: genera explicaciones locales basadas en instancias para modelos de clasificación en términos de Positivos Pertinentes (PP) y Negativos Pertinentes (PN), siendo estos dos tipos de explicaciones contrastivas. Estas explicaciones contrastivas ayudan a entender por qué una instancia se clasifica de una manera específica y qué cambios serían necesarios para cambiar esa clasificación.
   
3. **Contrafactuales guiados por prototipos (CFP)** : utiliza prototipos de clases para guiar la generación de instancias contrafactuales. Se enfoca en crear instancias que sean similares a los prototipos de una clase diferente a la clase de la instancia original, lo que puede proporcionar información sobre cómo el modelo distingue entre diferentes clases.
   
4. **Contrafactuales con aprendizaje por refuerzo (CFRL)**: se utiliza un enfoque basado en aprendizaje por refuerzo para generar instancias contrafactuales. El modelo aprende a modificar las características de entrada de manera que maximice una recompensa definida, como la probabilidad de clasificación correcta o la similitud con otras instancias de la misma clase.

## Conclusión
En conclusión, este proyecto ofrece una visión profunda y práctica sobre el uso de valores contrafactuales en el aprendizaje automático. Hemos explorado varios métodos para obtener valores contrafactuales utilizando la librería Alibi Explain, y hemos proporcionado ejemplos de aplicación que ilustran su utilidad en diversos escenarios. Comparando los siguientes aspectos para cada método: la necesidad de interpretabilidad, eficiencia computacional y  adaptabilidad a diferentes modelos. Esto nos ayuda a la elección del método adecuado según el contexto y de las prioridades específicas. 

Los métodos más interpretables son CEM y CFP, proporcionando explicaciones claras sobre los cambios necesarios para alterar una predicción. Sin embargo, CFP y CFRL sobresalen en generar contrafactuales de alta calidad. Con respecto a la eficiencia, los más eficientes son CFP y CFRL, reduciendo significativamente el coste computacional. Y por último, CFRL es el más adaptable, seguido de CFP, permitiendo su uso en una amplia variedad de modelos y datos.

El estudio de valores contrafactuales no solo mejora nuestra comprensión de cómo funcionan los modelos de aprendizaje automático, sino que también abre nuevas oportunidades para mejorar su interpretabilidad y robustez. Al comprender cómo pequeñas modificaciones en las características de entrada afectan las predicciones del modelo, podemos tomar decisiones más informadas sobre cómo mejorar y ajustar nuestros modelos para diferentes aplicaciones.

