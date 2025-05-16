# Clasificador_de_imagenes

---

## 🎯 Objetivo

Entrenar una red neuronal convolucional que sea capaz de distinguir si una imagen corresponde a un **perro** o a un **gato**.

---

## 🧠 Modelo utilizado

El modelo es una CNN compuesta por:

- 3 capas convolucionales con `ReLU` + MaxPooling
- Capa `Flatten` + `Dense` con 512 neuronas
- `Dropout` para evitar sobreajuste
- Salida con activación `sigmoid` para clasificación binaria

Además, se utilizó:

- `ImageDataGenerator` con data augmentation
- `EarlyStopping` para evitar entrenamiento excesivo

---

## 🗂️ Dataset

Se utilizó el dataset **PetImages**, que contiene aproximadamente 25.000 imágenes:

- 12.500 de gatos (`Cat/`)
- 12.500 de perros (`Dog/`)

Las imágenes fueron reorganizadas en carpetas `train/` (80%) y `validation/` (20%).

---

## 🔍 Resultados

Tras el entrenamiento del modelo con 10–20 épocas y early stopping:

- **Precisión en entrenamiento**: ~97%
- **Precisión en validación**: ~75–80%
- Curvas de `accuracy` y `loss` estables, con señales de ligera sobreajuste controlado por `Dropout` y `EarlyStopping`.

---

## 🖼️ Ejemplos de predicción

A continuación se muestran predicciones reales del modelo sobre imágenes no vistas:

| Imagen Gato | Imagen Perro |
|-------------|---------------|
| ![](./predicciones_demo/cat_1.png) | ![](./predicciones_demo/dog_1.png) |
| ![](./predicciones_demo/cat_2.png) | ![](./predicciones_demo/dog_2.png) |
| ![](./predicciones_demo/cat_3.png) | ![](./predicciones_demo/dog_3.png) |
1. Clona este repositorio:


