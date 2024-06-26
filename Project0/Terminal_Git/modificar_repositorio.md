<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# ¿Qué es el desarrollo web?
## Actualizar o subir nuevos ficheros

---

**1. Clonar el Repositorio desde GitHub (si aún no lo tienes localmente):**

```bash
git clone https://github.com/tuusuario/mi-repositorio.git
cd mi-repositorio
```

**2. Subir nuevos ficheros al repositorio:**

1. **Crear un nuevo archivo**:
    - Puedes crear un archivo nuevo en la terminal:
        
        ```bash
        echo "Contenido del nuevo archivo" > nuevo_archivo.txt
        ```
        
    - O puedes crear un archivo nuevo utilizando Visual Studio Code:
        - Abre Visual Studio y navega a tu proyecto.
        - Haz clic derecho en el explorador y selecciona `Add > New File`.
        - Elige el tipo de archivo que deseas crear y dale un nombre.
        - Añade el contenido deseado al archivo y guarda los cambios.
2. **Añadir el archivo al área de staging**:
    
    ```bash
    git add nuevo_archivo.txt
    ```
    
3. **Hacer un commit del archivo**:
    
    ```bash
    git commit -m "Añadido nuevo archivo nuevo_archivo.txt"
    ```
    
4. **Enviar los cambios al repositorio remoto en GitHub**:
    
    ```bash
    git push origin main
    ```
    

## **Actualizar ficheros existentes en el repositorio**

---

1. **Modificar un archivo existente**:
    - Puedes modificar un archivo utilizando Visual Studio Code:
        - Abre el archivo que deseas modificar desde el explorador.
        - Realiza los cambios necesarios en el archivo y guarda los cambios.
2. **Añadir el archivo modificado al área de staging**:
    
    ```bash
    git add archivo_existente.txt
    ```
    
3. **Hacer un commit del archivo modificado**:
    
    ```bash
    git commit -m "Actualizado archivo archivo_existente.txt"
    ```
    
4. **Enviar los cambios al repositorio remoto en GitHub**:
    
    ```bash
    git push origin main
    ```
    

### Tip:

Practica estos comandos regularmente para mejorar tu fluidez en el uso de la terminal, aunque puedes optar por empezar a utilizar Visual Studio Code para gestionar los archivos, ya que debido al volumen de contenido lo haremos a través de nuestro IDE y no la terminal.

## Reto coding

---

1. **Clonar el repositorio** desde GitHub (si aún no lo tienes localmente) que hayas creado:
    
    ```bash
    git clone https://github.com/tuusuario/mi-ejemplo.git
    cd mi-ejemplo
    ```
    
2. **Subir un nuevo archivo**:
    - Crear un archivo llamado `nueva_funcionalidad.txt` en Visual Studio:
        - Haz clic derecho en el explorador y crea uno nuevo.
        - Nombra el archivo `nueva_funcionalidad.txt` y añadelo.
        - Añade el texto "Esta es una nueva funcionalidad" y guarda los cambios.
    - Añade el archivo al área de staging:
    - Haz un commit del archivo:
    - Envia los cambios al repositorio remoto en GitHub:
3. **Actualizar un archivo existente**:
    - Crea y modificar el archivo de texto en Visual Studio:
        - Abrelo desde el explorador de soluciones.
        - Añade el contenido "Actualización de funcionalidad" y guarda los cambios.
    - Añade el archivo modificado al área de staging:
    - Haz un commit del archivo modificado:
    - Envia los cambios al repositorio remoto en GitHub: