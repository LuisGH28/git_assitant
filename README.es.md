# 🤖 GitGPT - Asistente Inteligente de Commits

📄 Este README también está disponible en: [English](README.md)

GitGPT es una herramienta inteligente que sugiere automáticamente **mensajes de commit** y también proporciona una **plantilla básica para pull requests**, combinando heurísticas, estructura del proyecto y un modelo de Machine Learning. Es perfecto para desarrolladores que quieren mantener sus commits consistentes y claros sin perder tiempo.

---

## 🚀 Características principales

- Detecta cambios en archivos **staged**, **unstaged** y **untracked**.
- Sugiere mensajes de commit basados en:
  - El contenido del diff (`git diff`)
  - El nombre de la rama actual
  - El tipo de archivo (código, documentación, estilo, test, etc.)
  - Un modelo de **Machine Learning** entrenado con ejemplos comunes.
- Soporta múltiples enfoques para sugerencias de mensajes:
  - 🔬 Modelo ML
  - ⚙️ Enfoque heurístico
  - 🎯 Enfoque temático
  - 🔍 Enfoque descriptivo
- Opción para crear una nueva rama antes de hacer commit.
- Interfaz de línea de comandos limpia y fácil de usar.

---

## 📌 Requisitos

- Python 3.7 o superior
- Git instalado y configurado
- Dependencias de Python (instalar vía pip):

```bash
pip install -r requirements.txt
```

---

## 🛠 Instalación

Clona el repositorio y copia `git_assistant` en el repositorio del proyecto en el que estás trabajando:

```
https://github.com/LuisGH28/git_assitant.git
cd git_assitant
```

Luego ejecuta el asistente:

```
python3 git_gpt.py
```

También puedes instalar desde PyPI:

```bash
pip install ai-git-assistant
```

---

## 📁 Estructura del Proyecto

```
├── README.md
├── README.es.md
└── git_assistant
    ├── git_gpt.py
    ├── gitgpt_model.pkl
    └── requirements.txt
```

---

## 🧠 Cómo funciona

1. Detecta archivos modificados en el repositorio usando `git status`.
2. Clasifica los archivos por tipo (documentación, código, tests, etc.).
3. Extrae diffs (`git diff`) y palabras clave relevantes.
4. Genera varias sugerencias de commit usando diferentes estrategias.
5. Permite seleccionar el mensaje más adecuado o escribir uno propio.
6. Crea un archivo `.md` con una plantilla básica de sugerencia para PR.

---

## 💬 Ejemplo

```
$ ./gitgpt.py

¿Deseas crear una nueva rama? (Y/y): n
ℹ️ Continuarás trabajando en la rama actual: fix/login-issue

Agregando archivos:
+ login.py
Archivos agregados correctamente.

💡 Sugerencia de commit #1:

fix: problema resuelto en login.py

¿Usar este mensaje? (Y/y), (N/n) para otra opción, o presiona enter para escribir tu propio mensaje: n

💡 Sugerencia de commit #2:

fix(login): error de autenticación corregido

¿Usar este mensaje? (Y/y), (N/n) para otra opción, o presiona enter para escribir tu propio mensaje: y

✅ Commit creado correctamente.
```

---

## 🧪 Entrenamiento del modelo

El modelo ML está basado en Naive Bayes con vectorización TF-IDF. Puedes reentrenarlo manualmente si lo deseas:

```
python3 -c "import gitgpt; gitgpt.train_model()"
```

Esto generará el archivo `gitgpt_model.pkl`.

> El modelo se entrena automáticamente si no existe o está corrupto.

---

## 🛠️ Desarrollo

1. Clona el repositorio
2. Crea un entorno virtual:

```
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

3. Instala dependencias:

```
pip install -e ".[dev]"
```

4. Ejecuta tests:

```
pytest
```

---

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! No dudes en abrir un issue o un pull request con mejoras, nuevas estrategias o mejoras al modelo.

---

## 📄 Licencia

Este proyecto está licenciado bajo la Licencia MIT. Úsalo, modifícalo y contribuye libremente.

---

## 🧑‍💻 Autor

Creado con ❤️ por [Luigi](https://github.com/LuisGH28)

---

## 🌟 ¿Te gusta este proyecto?

Dale una ⭐ en GitHub y compártelo con tu equipo!
