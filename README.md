# Proyecto: Red Neuronal - Equipo 8

Este es el repositorio central para nuestro proyecto académico de redes neuronales. Aquí se encuentra todo el código, los entornos y los datos necesarios para trabajar de forma síncrona.

## Estructura del Proyecto

* **`data/`**: Contiene los datasets (datos) exactos que estamos utilizando para entrenar y probar la red neuronal.
* **`notebooks/`**: Archivos de Jupyter (`.ipynb`) para exploración de datos, pruebas rápidas, visualización y experimentación.
* **`src/`**: Archivos de Python (`.py`) con el código fuente definitivo (arquitectura de la red, scripts de entrenamiento, etc.).
* **`requirements.txt`**: Lista de todas las librerías exactas que el proyecto necesita para funcionar.

---

## 🚀 Guía de inicio rápido para el equipo

Para empezar a trabajar en tu computadora sin romper el código de los demás, sigue estos pasos al pie de la letra:

### 1. Clonar el repositorio
Abre tu terminal, ve a la carpeta donde quieras guardar el proyecto y ejecuta:
```bash
git clone <AQUÍ_PON_EL_ENLACE_QUE_TE_DA_GITHUB>
cd red_neuronal_8
```

### 2. Crear el entorno virtual (venv)
Esto nos asegura a los 3 trabajar con las mismas versiones de las librerías. Dentro de la carpeta del proyecto, ejecuta:
```bash
python -m venv venv
```

### 3. Activar el entorno virtual
* **En Windows (PowerShell):** ```powershell
  .\venv\Scripts\Activate.ps1
  ```
  *(Si te da un error de permisos en Windows, ejecuta `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`, dile que sí, y vuelve a intentar activar).*

* **En Mac/Linux:** ```bash
  source venv/bin/activate
  ```
Sabrás que funcionó porque verás un `(venv)` verde al inicio de tu terminal.

### 4. Instalar las librerías del proyecto
Con el entorno activado, instala todo lo necesario ejecutando:
```bash
python -m pip install -r requirements.txt
```

### 5. Configurar Jupyter Notebook en VS Code
1. Abre VS Code en la carpeta del proyecto (`code .`).
2. Ve a la carpeta `notebooks/` y abre o crea un archivo `.ipynb`.
3. En la esquina superior derecha, haz clic en el botón **"Select Kernel"** (o en la versión de Python que aparezca).
4. Elige **"Python Environments"**.
5. Selecciona el que dice **`venv`**. 

¡Listo! Ya puedes empezar a programar.