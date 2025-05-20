# README.es.md

---



# AI Git Assistant 🤖📦

[![PyPI version](https://img.shields.io/pypi/v/ai-git-assistant)](https://pypi.org/project/ai-git-assistant/)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

Asistente inteligente para Git que automatiza la creación de commits semánticos y genera plantillas para Pull Requests, con soporte para análisis de cambios y sugerencias basadas en IA.

## ✨ Características principales

- 🧠 **Sugerencias de commits inteligentes** usando ML (Naive Bayes + TF-IDF)
- 📝 **Generación automática de mensajes** con múltiples enfoques:
  - Basado en tipo de archivo
  - Basado en cambios realizados
  - Basado en temática del código
- 🔍 **Detección automática** de archivos modificados (staged/unstaged/untracked)
- 📊 **Análisis de cambios** por tipo de archivo (código, docs, tests, etc.)
- 📑 **Plantilla de PR** con:
  - Listado organizado de archivos modificados
  - Sección para consideraciones de testing
  - Tabla de aplicaciones compatibles
- 🛠️ **Soporte para SQL** con detección especial de archivos .sql
- 🌍 **Interfaz en español** (fácil de internacionalizar)

---

## 📦 Instalación

```bash
pip install ai-git-assistant
```

O instala desde el código fuente:

```bash
https://github.com/LuisGH28/git_assitant.git
cd git_assitant
pip install .
```

---

<<<<<<< HEAD
## 🏗️ Estructura del proyecto

```
ai-git-assistant/
├── __init__.py
├── __main__.py            # Lógica principal
├── requirements.txt       # Dependencias
tests/
├── tests_cli.py           # Tests de interfaz
└── tests_git_utils.py     # Tests de funcionalidad Git
=======
## 🛠 Instalación

Clona el repositorio y agrega el archivo git_assistant a tu repositorio en el que estas trabajando

```
https://github.com/LuisGH28/git_assitant.git
cd git_assitant
```

Luego ejecuta el asistente

```
python3 git_gpt.py
```

---

## 🧠 Cómo funciona

1. Detecta los archivos modificados en el repositorio usando `git status`.
2. Clasifica los archivos por tipo (documentación, código, pruebas, etc.).
3. Extrae las diferencias (`git diff`) y palabras clave.
4. Genera varias sugerencias de commit usando diferentes enfoques.
5. Permite seleccionar la sugerencia que más se ajuste o escribir una personalizada.
6. Crea un archivo .md de sugerencia para un posible PR

---

## 💬 Ejemplo de uso

$ ./gitgpt.py

¿Quieres crear una nueva rama? (S/s): n
ℹ️ Continuarás trabajando en la rama actual: fix/login-issue

Agregando archivos:

+ login.py
  Archivos agregados exitosamente.

💡 Sugerencias de commit #1:

fix: solucionado error en login.py

¿Deseas usar este mensaje? (S/s), (O/o) para otra opcion o enter para ingresar tu propio commit: o

💡 Sugerencias de commit #2:

 fix(login): corrección de error en autenticación

¿Deseas usar este mensaje? (S/s), (O/o) para otra opcion o enter para ingresar tu propio commit: s

✅ Commit realizado con éxito.

---

## 🧪 Entrenamiento del Modelo

El modelo de ML está basado en Naive Bayes con vectorización TF-IDF. Puedes entrenarlo tú mismo si lo deseas:

```
python3 -c "import gitgpt; gitgpt.train_model()"

```

Esto generará el archivo `gitgpt_model.pkl`.

> El modelo también se entrena automáticamente si no existe o si está dañado.

---

## 📁 Estructura del Proyecto

```
├── README.md
├── README.es.md
└── git_assistant
    ├── git_gpt.py
    ├── gitgpt_model.pkl
    └── requirements.txt
>>>>>>> 42c9f6a2e09320e2a599f6881b8dad5ace57232c

```

---

## 📌 Requisitos

* Python 3.8+
* Git instalado y configurado
* Dependencias:
  * scikit-learn
  * joblib

---

## 🛠️ Desarrollo

1. Clona el repositorio
2. Crea un entorno virtual:


3. Instala dependencias:

```
pip install -e ".[dev]"
```


4. Ejecuta tests:

```
pytest
```


---



## 🤖 Roadmap

* Soporte para más lenguajes (i18n)
* Integración con APIs de GitHub/GitLab
* Modo no-interactivo para CI/CD
* Plugin para editores (VSCode, PyCharm)

---



## 🎉 ¡Disponible en PyPI!


```
pip install ai-git-assistant
```
