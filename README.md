# **Red neuronal convolucional para el diagnóstico de nódulos tiroideos según la clasificación EU-TIRADS**

## Por Alejandro Martínez Hernández

Especialización en analítica y ciencia de datos
Universidad de Antioquía
Medellín 
2024

Este proyecto tiene como objetivo desarrollar un modelo capaz de clasificar imágenes de ultrasonido de nódulos tiroideos según la EU-TIRADS, con el fin de crear una solución accesible y aplicable en una amplia variedad de entornos clínicos, incluidos aquellos con limitaciones tecnológicas.

Se utilizó una base de datos abierta de imágenes ecográficas de tiroides, enriquecida con anotaciones clínicas (DDTI versión 2023), proporcionada por el grupo de investigación Computer Imaging and Medical Applications Laboratory (CIM@LAB) de la Universidad Nacional de Colombia y el Instituto de Diagnóstico Médico (IDIME). Estas imágenes se emplearon para evaluar modelos clásicos como máquinas de vectores de soporte (SVM), bosques aleatorios (Random Forest) y Naive Bayes, así como modelos preentrenados de redes neuronales convolucionales (CNN) mediante transferencia de aprendizaje, incluyendo MobileNetV3 (versiones Small y Large), ResNet50, ResNet101, VGG16, VGG19, Xception y DenseNet121.

Este proyecto consta de cinco notebooks. En el primero, se realiza un análisis exploratorio de los datos. En el segundo, se procesan y organizan los datos. En el tercero, se utilizan estos datos para clasificarlos en dos categorías mediante modelos clásicos de inteligencia artificial. En el cuarto notebook, se clasifican nuevamente las imágenes en dos categorías, pero utilizando redes neuronales convolucionales. Finalmente, en el quinto notebook, se repite el proceso del cuarto, implementando además un aumento de datos.

Una vez ejecutado todo el proyecto se tendrá la siguiente estructura de directorios:

```
nodulos_tiroideos/
├─ .gitignore
├─ 1_exploracion_datos.ipynb
├─ 2_procesamiento_datos.ipynb
├─ 3_modelos_simples.ipynb
├─ 4_modelos_CNN.ipynb
├─ 5_modelos_CNN_Datos_Aumentados.ipynb
├─ README.md
├─ df_actualizado.csv
├─ df_agrupado.csv
├─ requirements.txt
├─ us_images_backup/
│  ├─ DDTI_V1.zip
│  ├─ DDTI_V2.zip
│  └─ cropped.zip
├─ db_unal/
│  ├─ organized/
│  │  ├─ images/
│  │  │  ├─ cropped/
│  │  │  │  ├─ high/
│  │  │  │  │  ├─ 1_1.jpg
│  │  │  │  │  ├─ 1_2.jpg
│  │  │  │  │  └─ ...
│  │  │  │  ├─ low/
│  │  │  │  │  ├─ 4_1.jpg
│  │  │  │  │  ├─ 6_1.jpg
│  │  │  │  │  └─ ...
│  │  │  ├─ raw/
│  │  │  │  ├─ high/
│  │  │  │  │  ├─ 1_1.jpg
│  │  │  │  │  ├─ 1_2.jpg
│  │  │  │  │  └─ ...
│  │  │  │  ├─ low/
│  │  │  │  │  ├─ 4_1.jpg
│  │  │  │  │  ├─ 6_1.jpg
│  │  │  │  │  └─ ...
│  ├─ originals/
│  │  ├─ DDTI_V1/
│  │  │  ├─ 1.xml
│  │  │  ├─ 1_1.jpg
│  │  │  ├─ 1_2.jpg
│  │  │  ├─ ...
│  │  ├─ DDTI_V2/
│  │  │  ├─ RadiologistSegmentations/
│  │  │  │  ├─ Segmentations_1/
│  │  │  │  │  ├─ 1_1.nii
│  │  │  │  │  ├─ 1_2.nii
│  │  │  │  │  ├─ ...
│  │  │  │  │  └─ clasificación.xlsx
│  │  │  ├─ ResidentSegmentations/
│  │  │  │  ├─ Segmentations_1/
│  │  │  │  │  ├─ 1_1.nii
│  │  │  │  │  ├─ 1_2.nii
│  │  │  │  │  ├─ ...
│  │  │  │  ├─ Segmentations_2/
│  │  │  │  │  ├─ 1_2.nii
│  │  │  │  │  ├─ 2_1.nii
│  │  │  │  │  ├─ ...
```