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

## 🔀 Guía de Trabajo Colaborativo (Flujo Git)

Para trabajar los 3 al mismo tiempo de forma asíncrona y sin pisarnos los talones, usaremos el flujo de trabajo basado en **Ramas (Branches)** y **Pull Requests**.

🚨 **Regla de oro:** NADIE trabaja ni sube cambios directamente a la rama `main`. La rama `main` es sagrada y solo contiene código que ya funciona perfectamente.

### El flujo de trabajo paso a paso:

#### 1. Actualizar tu computadora (Antes de empezar)
Antes de escribir una sola línea de código, asegúrate de tener lo último que hayan hecho los demás:
```bash
git checkout main
git pull origin main
```

#### 2. Crear tu propia Rama
Crea una rama aislada para tu tarea específica (ejemplo: `juan-limpieza-datos` o `maria-arquitectura-red`):
```bash
git checkout -b tu-nombre-tarea
```
*(Ahora estás en tu propia rama, aislado de `main`).*

#### 3. Trabajar y hacer Commits
Modifica los archivos en VS Code. Cuando termines una parte importante, guarda tus cambios:
```bash
git add .
git commit -m "Descripción clara de lo que hiciste"
```

#### 4. Subir tu Rama a GitHub
Cuando tu tarea esté lista y quieras que el equipo la una al proyecto principal, sube **tu rama** a la nube:
```bash
git push origin tu-nombre-tarea
```

#### 5. El "Pull Request" (PR)
1. Ve a la página del repositorio en GitHub.
2. Verás un botón verde que dice **"Compare & pull request"**. Haz clic en él.
3. Deja un comentario de lo que hiciste y crea el Pull Request.
4. Otro miembro del equipo debe revisar el código en GitHub y presionar **"Merge pull request"** para fusionarlo con `main`.

#### 6. Sincronizar de nuevo
Una vez que tu código fue aceptado y fusionado en GitHub, regresa a tu terminal y actualiza tu computadora para tu siguiente tarea:
```bash
git checkout main
git pull origin main
```

---

### 💡 3 Consejos de oro para evitar problemas:

1. **Repártanse los archivos:** Para evitar "Conflictos de Fusión" (Merge Conflicts), eviten que dos personas editen *exactamente la misma línea del mismo archivo* al mismo tiempo. Divídanse por archivos o módulos.
2. **Cuidado con Jupyter Notebooks:** Los archivos `.ipynb` cambian internamente con solo ejecutarlos. Es mejor que cada quien tenga su propio notebook para experimentar (ej. `notebook_juan.ipynb`) y pasen el código final y limpio a los archivos `.py` en la carpeta `src/`.
3. **Commits descriptivos:** No usen mensajes como "cambios" o "actualización". Usen descripciones útiles como "Agregué la carga del dataset" o "Corregí error de dimensiones en la capa oculta".