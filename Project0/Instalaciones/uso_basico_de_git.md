<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Uso básico de Git

# Primeros pasos con Git

Git es un sistema de control de versiones distribuido que permite a los desarrolladores colaborar de manera eficiente en proyectos de software. Con Git, puedes rastrear los cambios en tu código, revertir a versiones anteriores y trabajar simultáneamente en múltiples características o correcciones sin interferencias. Esta guía está diseñada para proporcionar una comprensión clara y práctica de las operaciones básicas en Git, adecuada para aquellos que lo utilizan por primera vez.

## ¿Por qué es importante entender Git?

---

1. **Colaboración Eficiente**: Git facilita el trabajo en equipo, permitiendo que múltiples desarrolladores colaboren en el mismo proyecto sin conflictos.
2. **Historial de Cambios**: Mantén un registro detallado de todos los cambios realizados, lo que facilita la revisión y auditoría del código.
3. **Trabajo en Paralelo**: Crea ramas para trabajar en nuevas características o correcciones sin afectar la rama principal del proyecto.
4. **Integración Continua y Despliegue (CI/CD)**: Automatiza pruebas y despliegues, integrando Git con otras herramientas de desarrollo y operaciones.

A continuación, exploraremos los conceptos y comandos básicos de Git para ayudarte a empezar.

## Configuración Básica

---

### Configuración del Nombre de Usuario o Email

Antes de comenzar a usar Git, debes configurar tu identidad para que todos los cambios realizados queden correctamente atribuidos a ti.

```bash
git config --global user.name "nombre"
git config --global user.email "email@email.com"
```

Configurar tu nombre y correo electrónico es crucial para mantener un historial de cambios claro y atribuir correctamente cada contribución.

### Activar el Marco de Colorización de Comandos

Para mejorar la legibilidad de los comandos y la salida de Git, puedes activar la colorización.

```bash
git config --global color.ui auto
```

La colorización ayuda a distinguir entre diferentes tipos de información (como nombres de archivos, ramas, y mensajes de error), facilitando la lectura y comprensión de los comandos y resultados.

### Consultar la Configuración Actual

Para verificar la configuración actual de Git, puedes listar todas las configuraciones establecidas.

```bash
git config --list
```

Consultar la configuración actual te permite asegurarte de que Git esté configurado correctamente y verificar tus ajustes.

### Establecer Alias

Para ahorrar tiempo y esfuerzo al escribir comandos frecuentes, puedes definir alias personalizados.

```bash
git config --global alias.ci "commit"
```

Los alias te permiten utilizar abreviaciones para comandos largos o frecuentemente utilizados, mejorando la eficiencia.

### Activar el Completado Predictivo

El completado predictivo ayuda a corregir errores tipográficos automáticamente.

```bash
git config --global help.autocorrect 1
```

El completado predictivo es útil para evitar errores tipográficos en los comandos, especialmente en nombres largos o complejos.

En el README de Git, Linus Torvalds incluyó varias definiciones humorísticas y autocríticas sobre el nombre "Git".

1. **"Stupid. Contemptible and despicable. Simple. Take your pick from the dictionary of slang."**
    - "Estúpido. Despreciable y despreciado. Simple. Elige una entre estas jergas."
2. **"Global Information Tracker"**
    - El nombre oficial si todo funciona a la perfección. Cuando sale todo bien dices: "¡Estoy usando el Global Information Tracker!"
3. **"Goddamn Idiotic Truckload of sh*t"**
    - Una definición autocrítica para cuando Git no funciona como esperabas.


## Contenido asociado
---
- [Video: Uso Básico de Repositorios - Parte 1](https://vimeo.com/918306353/28883d8c86)
- [Video: Uso Básico de Repositorios - Parte 2](https://vimeo.com/918293982/4742a105e4)
