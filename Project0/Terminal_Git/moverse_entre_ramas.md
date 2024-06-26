<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Moverse entre ramas

Moverse entre ramas en Git es esencial para trabajar en diferentes funcionalidades o correcciones sin interferir con la rama principal. Cambiar de rama te permite aislar tu trabajo y mantener un flujo de trabajo organizado.

## Listar todas las ramas en un repositorio

---

**1. Clonar el Repositorio desde GitHub (si aún no lo tienes localmente):**

```bash
git clone https://github.com/tuusuario/mi-repositorio.git
cd mi-repositorio
```

**2. Listar todas las ramas locales:**

```bash
git branch
```

**3. Listar todas las ramas, incluidas las remotas:**

```bash
git branch -a
```

## Cambiar entre diferentes ramas

---

**1. Cambiar a una rama existente:**

```bash
git checkout nombre_de_la_rama
```

**2. Crear y cambiar a una nueva rama:**

```bash
git checkout -b nueva_rama
```

## Gestionar cambios no confirmados al cambiar de rama

---

1. **Si tienes cambios no confirmados y deseas cambiarlos a otra rama**:
    - Añadir los cambios al área de staging:
        
        ```bash
        git add .
        ```
        
    - Hacer un commit de los cambios:
        
        ```bash
        git commit -m "Guardando cambios antes de cambiar de rama"
        ```
        
2. **Si prefieres mantener los cambios sin hacer commit**:
    - Stash los cambios no confirmados:
        
        ```bash
        git stash
        ```
        
    - Cambiar a la nueva rama:
        
        ```bash
        git checkout nombre_de_la_rama
        ```
        
    - Aplicar los cambios stasheados:
        
        ```bash
        git stash apply
        ```