# Timbre-Transfer-Pitch-Detectiong-With-ML

ste proyecto utiliza el modelo DDSP (Differentiable Digital Signal Processing) para la síntesis de audio de alta fidelidad. Proporciona una comparación con el modelo WaveRNN y presenta resultados detallados en términos de métricas de resíntesis y capacidades del modelo.

## Contenido

- [Introducción](#introducción)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Resultados](#resultados)
- [Requisitos](#requisitos)
- [Cómo Usar](#cómo-usar)
- [Contribuciones](#contribuciones)
- [Licencia](#licencia)

## Introducción

Este proyecto se centra en la síntesis de audio de alta fidelidad utilizando el modelo DDSP, una técnica que permite el procesamiento de señales digitales de manera diferenciable. Exploramos las capacidades del modelo en comparación con el estado del arte representado por WaveRNN. La síntesis de audio es un área emocionante en la que la inteligencia artificial ha demostrado ser eficaz, y DDSP ofrece un enfoque prometedor.

## Estructura del Proyecto

- **/data:** Contiene los conjuntos de datos utilizados para entrenar y evaluar el modelo.
- **/models:** Almacena los modelos preentrenados y los checkpoints.
- **/results:** Archivos y visualizaciones de los resultados obtenidos durante la experimentación.
- **/src:** Código fuente del proyecto, organizado en módulos y scripts.

## Resultados

### Resíntesis Comparativa

En la siguiente tabla, se comparan las métricas de resíntesis entre DDSP y WaveRNN:

\ Begin {Table} [H]
\ Centering
\ Rowcolors {2} {gray! 25} {White}
\ begin {tabular} {| c | c | c | c |}
\ hline
Modelo & Loudness (L1) & F0 (L1) & F0 Outliers \\
\ hline
WAVERNN & 0.10 & 1.00 & 0.07 \\
DDSP Autoencoder & 0.04 & 1.29 & 0.02 \\
\ hline
\ end {tabular}
\ capt
\ end {table}

### Interpolación de Características

Las siguientes métricas se obtuvieron durante las interpolaciones:

\ Begin {Table} [H]
\ Centering
\ Rowcolors {2} {gray! 25} {White}
\ begin {tabular} {| c | c |}
\ hline
Task & Loudness (L1) & F0 (L1) \\
\ hline
Reconstruction & 0.042 & 0.060 \\
Loudness l(t) interp. & 0.061 & 0.060 \\
F0 f(t) interp. & 0.048 & 0.070 \\
Z z(t) interp. & 0.063 & 0.065 \\
\ hline
\ end {tabular}
\ capt
\ end {table}

## Requisitos

- Python 3.9
- Bibliotecas Python: !sudo apt-get install portaudio19-dev
!pip install sounddevice
!apt install -y ffmpeg
!pip install --upgrade librosa
-  Use los 3 codigos proporcionados en el orden indicado para empezar primero con la identificaciond e Audio, Luego el entrenamiento del modelo con los datasets descargados, Y al final el proceso de Timbre Transfer

## Cómo Usar

1. Clona el repositorio: `git clone [URL del repositorio]`
2. Navega al directorio del proyecto: `cd ddsp-audio-synthesis`
3. Instala las dependencias: `pip install -r requirements.txt`
4. Ejecuta el script principal: `python main.py`

## Contribuciones

¡Contribuciones bienvenidas! Si deseas contribuir al proyecto, sigue estos pasos:
1. Haz un fork del repositorio.
2. Crea una rama para tu contribución: `git checkout -b feature/nueva-funcionalidad`
3. Realiza tus cambios y commitea: `git commit -m "Agrega nueva funcionalidad"`
4. Haz un push a tu rama: `git push origin feature/nueva-funcionalidad`
5. Abre una solicitud de extracción.

## Autores

William Garzon 
David Casa
