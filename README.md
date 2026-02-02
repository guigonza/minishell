# minishell

Autor: guigonza (Guillermo González)  
Coautor: carbon (https://github.com/GranCAM)

Resumen
-------
minishell es una implementación de un intérprete de comandos minimalista siguiendo los requisitos de la proyecto 42. Proporciona parsing, ejecución de redirecciones y tuberías, manejo de señales y builtins básicos.

Estado
------
Rama estable: `main` (esta rama contiene la versión aprobada y limpia).

Requisitos
---------
- cc / gcc / clang
- make
- libft (incluida en el repo)
- readline (se recomienda instalar via Homebrew en macOS):
  - macOS: `brew install readline`
  - Debian/Ubuntu: `sudo apt install libreadline-dev`

Instalación / Compilación
-------------------------
Desde la raíz del repo:
```bash
make fclean
make
```
Si hay problemas con readline en macOS, asegúrate de que el Makefile apunte al prefix de Homebrew:
```bash
export LDFLAGS="-L$(brew --prefix readline)/lib"
export CPPFLAGS="-I$(brew --prefix readline)/include"
```

Uso
---
Ejecutar:
```bash
./minishell
```
Comandos soportados (no exhaustivo): builtins (cd, echo, export, unset, env, pwd, exit), ejecución externa, tuberías, redirecciones básicas, heredoc.

Estructura del repositorio
--------------------------
- src/           : código fuente (.c)
- obj/           : objetos generados por la compilación
- includes/      : cabeceras públicas del proyecto
- libft/         : biblioteca auxiliar
- Makefile       : reglas de compilación

Normas y estilo
---------------
- Cumple con las normas de 42 (norminette). Mantener & revisar estilo antes de push.
- Evitar funciones no permitidas según enunciado del proyecto.
- Documentar funciones complejas y gestionar correctamente memoria y errores.

Pruebas y debugging
-------------------
- Usar `make` y ejecutar binario.
- Comprobar comportamiento de señales y heredoc en terminal interactivo.
- Para reproducibilidad usar Docker (opcional, ver Dockerfile en repo si existe).

Aprendizajes y objetivos
------------------------
- Parsing de shell y manejo de tokens
- Gestión de procesos y pipes en Unix
- Manejo de señales y de la biblioteca readline
- Corrección de errores y escritura de Makefiles portables

Créditos
--------
Trabajo realizado por Guille y revisado/colaborado por carbon — https://github.com/GranCAM

Licencia
--------
Proyecto para evaluación académica (consultar reglas de reparto de código de 42).
