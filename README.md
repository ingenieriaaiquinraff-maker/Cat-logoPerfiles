# Catálogos de perfiles

Proyecto en Python para procesar un catálogo de perfiles estructurales desde un archivo Excel.

El notebook calcula, según la familia del perfil (`I`, `RHS`, `SHS`, `C` o `L`):

- Área de la sección.
- Perímetro.
- Peso calculado.
- Diferencia respecto al peso del catálogo.
- Área de pintura por metro y por tonelada.

El resultado se guarda en un nuevo archivo Excel.

## Requisitos

- Python 3.
- Jupyter Notebook o JupyterLab.

## Instalación

Desde la carpeta del proyecto, crea y activa un entorno virtual:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

Instala las dependencias:

```powershell
pip install -r requirements.txt
```

Si Windows no permite activar el entorno, ejecuta PowerShell como usuario y configura la política para tu usuario:

```powershell
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

## Uso

1. Coloca `Perfiles.xlsx` en la carpeta del proyecto.
2. Abre `CatálogoV1.ipynb` en VS Code, Jupyter Notebook o JupyterLab.
3. Ejecuta las celdas en orden.
4. Se generará `Perfiles_Post.xlsx` con los cálculos.

El archivo de entrada debe contener una hoja llamada `Hoja1` y las columnas geométricas utilizadas por el notebook, como `Familia`, `h (mm)`, `b (mm)`, `tw (mm)`, `tf (mm)` y `W (kg/m)`.

## Nota

En el mapa de funciones del notebook, la familia `I` apunta actualmente a `calcular_W`, pero la función definida se llama `calcular_I`. Para procesar perfiles `I`, cambia esa referencia a `calcular_I`.
