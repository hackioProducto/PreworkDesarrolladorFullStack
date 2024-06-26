<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Crear ramas

Las ramas en Git permiten trabajar en diferentes funcionalidades o correcciones de manera aislada. Esto facilita el desarrollo paralelo y la gestión de código sin interferir con la rama principal.

## Crear una nueva rama en Git

---

**1. Clonar el Repositorio desde GitHub (si aún no lo tienes localmente):**

```bash
git clone https://github.com/tuusuario/mi-repositorio.git
```

**2. Crear una nueva rama y cambiar a ella:**

1. **Crear una nueva rama**:
    
    ```bash
    git branch nombre_de_la_rama
    ```
    
2. **Cambiar a la nueva rama**:
    
    ```bash
    git checkout nombre_de_la_rama
    ```
    

**Alternativamente, puedes crear y cambiar a una nueva rama en un solo comando:**

```bash
git checkout -b nombre_de_la_rama
```

## Realizar cambios en la nueva rama

---

1. **Crear o modificar archivos** (puedes usar Visual Studio Code para esto):
    - Crear un archivo nuevo:
        
        ```bash
        echo "Contenido del nuevo archivo" > nuevo_archivo.txt
        ```
        
    - Modificar un archivo existente utilizando Visual Studio Code:
        - Abre Visual Studio Code y navega a tu proyecto.
        - Realiza los cambios necesarios en los archivos y guarda los cambios.
2. **Añadir los cambios al área de staging**:
    
    ```bash
    git add .
    ```
    
3. **Hacer un commit de los cambios**:
    
    ```bash
    git commit -m "Descripción de los cambios realizados"
    ```
    

## Subir cambios a la rama en GitHub

---

1. **Subir la rama al repositorio remoto**:
    
    ```bash
    git push origin nombre_de_la_rama
    ```
    
    ### Tip
    
    Si quieres comprobar en qué rama te encuentras en cualquier momento puedes hacer uso de `git status` en la terminal para obtener toda la información sobre tu trabajo en Git.
    