# 🧠 Clasificador de Depresión Estudiantil

Este proyecto es una aplicación de escritorio desarrollada en Python que utiliza un modelo de Machine Learning para clasificar el estado de salud mental de un estudiante, específicamente orientado a la detección de riesgo de depresión. La aplicación cuenta con una interfaz gráfica donde el usuario puede ingresar diversa información personal, académica y de estilo de vida, y obtener una predicción basada en los datos proporcionados.

## 📜 Descripción

El objetivo principal de este proyecto es proporcionar una herramienta simple e intuitiva que sirva como una primera aproximación para evaluar el estado de salud mental, sin reemplazar en ningún caso el diagnóstico de un profesional. El sistema utiliza un modelo pre-entrenado de **Random Forest** para realizar las clasificaciones.

## ✨ Características

- **Interfaz Gráfica Intuitiva**: Creada con `Tkinter` para facilitar la entrada de datos.
- **Modelo Predictivo**: Utiliza un clasificador `RandomForestClassifier` de Scikit-learn entrenado con el dataset "Student Depression Dataset".
- **Formulario Completo**: Recopila 12 características clave del usuario, incluyendo:
    - Información personal (género, edad).
    - Datos académicos (nivel educativo, promedio, presión académica).
    - Estilo de vida (calidad del sueño, hábitos alimenticios, horas de trabajo/estudio).
    - Historial de salud mental (pensamientos suicidas, historial familiar).
- **Resultados Claros**: Muestra la predicción de manera sencilla, junto con una advertencia sobre la naturaleza no médica de la herramienta.

## 📂 Estructura del Proyecto

El repositorio está organizado de la siguiente manera para mantener el código, los datos y otros recursos de manera ordenada:

```
.
├── data/
│   ├── raw/              # Datasets originales sin procesar
│   └── processed/        # Datasets limpios y listos para el modelo
├── notebooks/            # Jupyter Notebooks para exploración y pruebas
├── src/                  # Código fuente de la aplicación (.py)
│   ├── gui.py            # Lógica de la interfaz gráfica
│   ├── preproces.py      # Script para limpieza y preprocesamiento de datos
│   └── models_tests.py   # Script para entrenar y evaluar modelos
├── .gitignore            # Archivos a ignorar por Git
├── README.md             # Este archivo
├── requirements.txt      # Dependencias del proyecto
└── rf_model.pkl          # Modelo de Random Forest serializado
```

## 💾 Dataset

El modelo fue entrenado con el **Student Depression Dataset**. Los datos originales y procesados se encuentran en la carpeta `data/`. El preprocesamiento incluye la codificación de variables categóricas a numéricas y el manejo de valores faltantes.

## 🚀 Instalación y Uso

Sigue estos pasos para ejecutar la aplicación en tu máquina local.

### Prerrequisitos

- Python 3.6 o superior.
- `pip` para instalar las dependencias.

### 1. Clona el repositorio

```bash
git clone <URL-DEL-REPOSITORIO>
cd <NOMBRE-DEL-REPOSITORIO>
```

### 2. (Opcional) Crea un entorno virtual

Es una buena práctica crear un entorno virtual para aislar las dependencias del proyecto.

```bash
# Para Windows
python -m venv venv
venv\Scripts\activate

# Para macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Instala las dependencias

Instala todas las librerías necesarias que se encuentran en `requirements.txt`.

```bash
pip install -r requirements.txt
```

### 4. Ejecuta la aplicación

Una vez instaladas las dependencias, puedes iniciar la interfaz gráfica con el siguiente comando:

```bash
python src/gui.py
```

Se abrirá una ventana donde podrás completar el formulario y obtener una clasificación.

## ⚠️ Descargo de Responsabilidad

Este proyecto es una herramienta con fines educativos y de demostración. **Las predicciones no constituyen un diagnóstico médico**. Si tienes preocupaciones sobre tu salud mental, por favor, consulta a un profesional de la salud.
