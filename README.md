# ML - Clasificador de Regresión Logística  

Este proyecto implementa un modelo de **regresión logística** utilizando la biblioteca **Scikit-Learn** en Python. El objetivo es predecir si un cliente incumplirá el pago de un préstamo (`default_Yes`), utilizando como características el saldo (`balance`), los ingresos (`income`) y el estado de estudiante (`student_Yes`).

## Estructura del proyecto  

El proyecto incluye el archivo `Default.csv`, que contiene 10,000 registros con las siguientes columnas:  
- **default**: Indica si el cliente incumplió el pago (`Yes` o `No`).  
- **student**: Indica si el cliente es estudiante (`Yes` o `No`).  
- **balance**: Saldo del cliente.  
- **income**: Ingresos del cliente.  

## Proceso  

### 1. **Importación y exploración de datos**  
- Se utiliza la biblioteca **pandas** para cargar y explorar los datos.  
- Se realizan inspecciones iniciales con `data.head()` y `data.info()`.  

### 2. **Preprocesamiento de datos**  
- Las columnas categóricas (`default`, `student`) se convierten en variables dummy usando `pd.get_dummies`.  
- Las nuevas columnas binarias (`default_Yes`, `student_Yes`) se aseguran como enteros para facilitar su procesamiento.  

### 3. **Separación de datos**  
- Las características seleccionadas son: `balance`, `income`, `student_Yes`.  
- La variable objetivo es `default_Yes`.  
- Se dividen los datos en conjuntos de entrenamiento y validación, usando un 70% para entrenamiento y un 30% para validación mediante `train_test_split`.  

### 4. **Entrenamiento del modelo**  
- Se entrena un modelo de **Regresión Logística** con los datos de entrenamiento.  

### 5. **Evaluación del modelo**  
- Se generan predicciones con el conjunto de validación.  
- Se evalúa el modelo utilizando:  
  - **Matriz de confusión** (visualización incluida).  
  - **Exactitud (accuracy)**: Métrica principal del modelo.  

## Ejecución  

### Requisitos  
- **Python 3.x**  
- Bibliotecas: `pandas`, `scikit-learn`

### Pasos  
1. Clona este repositorio e incluye el archivo `Default.csv` en el mismo directorio que el código.  
2. Ejecuta el script de Python proporcionado.  

### Resultado esperado  
Al final de la ejecución, se mostrará:  
1. La matriz de confusión para evaluar el desempeño del modelo.  
2. La exactitud (`accuracy`) del modelo en la predicción del conjunto de validación.  

## Contacto  
Para preguntas o sugerencias, puedes abrir un **issue** en este repositorio. ¡Gracias por explorar este proyecto! 🚀
