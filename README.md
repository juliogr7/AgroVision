<img width="800" height="300" alt="Banner_Agrovision_800x300" src="https://github.com/user-attachments/assets/87ab898a-dcca-4014-8410-d96064d0a6c1" />

# AgroVision: Clasificación de enfermemdades en mazorcas de maíz mediante redes neuronales densas y convolucionales
Autores: Luis Toscano, Daniel Badillo, Julio Gutiérrez

Objetivo: Desarrollar un sistema automatizado de diagnóstico agrícola basado en IA que identifique y clasifique con precisión enfermedades en mazorcas de maíz para mejorar la eficiencia y objetividad de dicho análisis.

Dataset: En este dataset hay disponibles 39 clases diferentes de imágenes de hojas de plantas y fondos, conteniendo 61,486 imágenes. Se utilizaron seis técnicas diferentes de aumento de datos para incrementar el tamaño del conjunto. Las técnicas son: volteo de imágenes, corrección de gamma, inyección de ruido, aumento de color mediante PCA, rotación y escalado. Link de descarga: https://data.mendeley.com/datasets/tywbtsjrjv/1
En base a este, se escogieron únicamente las 4 clases de hojas de maíz (las clases 9, 10, 11 y 12 en la página): Mancha gris, roya (u óxido) común, tizón norteño y maíz sano.

Se evaluaron 5 modelos en total: 
- DNN: GELU, regularización L2, Dropout, Softmax, AdamW, ReduceLROnPlateau, EarlyStopping
- CNN: ReLU, BatchNorm, Dropout, Softmax, AdamW, Sparse Categorical Crossentropy, ReduceLROnPlateau, EarlyStopping
- Transfer Learning: ResNet50 y EfficientNetB0 (Preentrenadas en el dataset ImageNet)
- Denoising CNN Autoencoder
