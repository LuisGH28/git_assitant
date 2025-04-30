# README.es.md (versión en español)

---

# 🤖 GitGPT - Asistente Inteligente de Commits

📄 Este README también está disponible en: [English](README.md)

GitGPT es una herramienta inteligente que sugiere mensajes de **commit** automáticamente, además de proponer una plantilla básica para la generación de PR, combinando heurísticas, estructura del proyecto y un modelo de Machine Learning. Es ideal para desarrolladores que buscan mantener consistencia y claridad en sus commits sin perder tiempo.

---

## 🚀 Características

- Detecta cambios en archivos **staged**, **unstaged** y **untracked**.
- Sugiere mensajes de commit basados en:
  - El contenido del cambio (`git diff`)
  - La rama actual
  - El tipo de archivo (código, documentación, estilo, test, etc.)
  - Un modelo de **Machine Learning** entrenado con ejemplos comunes.
- Soporta múltiples enfoques para generar sugerencias:
  - 🔬 Modelo ML
  - ⚙️ Enfoque heurístico
  - 🎯 Enfoque temático
  - 🔍 Enfoque descriptivo
- Permite crear una nueva rama antes del commit (opcional).
- Interfaz por consola clara y fácil de usar.

---

## 📦 Requisitos

- Python 3.7 o superior
- Git instalado y configurado
- Dependencias de Python (instalable vía pip):

```bash
pip install -r requirements.txt
```

---

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

```

---

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Puedes abrir un issue o hacer un pull request con mejoras, nuevos enfoques o ajustes al modelo.

---

## 📄 Licencia

Este proyecto está bajo la licencia MIT. ¡Úsalo, modifícalo y contribuye!

---

## 🧑‍💻 Autor

Desarrollado con ❤️ por [Luigi](https://github.com/LuisGH28)

---

## 🌟 ¿Te gusta el proyecto?

¡Dale una ⭐ en GitHub y compártelo con tus colegas!
