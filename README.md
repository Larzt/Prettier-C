# Tutorial PRETTIER C++: Configuración de .clang-format en Visual Studio Code

## Prerrequisitos
Tener instalado Visual Studio Code.
Tener instalada la extensión C/C++ en VSC

## Paso 1: Crear el archivo .clang-format
Navega al directorio raíz de tu proyecto.
Crea un archivo llamado .clang-format en este directorio con el siguiente contenido, basado en la guía de estilo de Google:
```
### Archivo .clang-format basado en la guía de estilo de Google
BasedOnStyle: Google
IndentWidth: 2               # Usa una indentación de 2 espacios, como en la guía de Google
TabWidth: 2                  # El tamaño del tabulador es de 2 espacios
UseTab: Never                # Usa espacios en lugar de tabs (Google recomienda espacios)

### Reglas específicas
BreakBeforeBraces: Attach     # Las llaves se abren en la misma línea
AllowShortFunctionsOnASingleLine: Inline # Permite funciones cortas en una sola línea
ColumnLimit: 80               # Límite de 80 caracteres por línea según la guía de Google
PointerAlignment: Right       # Los punteros se alinean a la derecha ('int *ptr' en lugar de 'int* ptr')
SpaceBeforeParens: ControlStatements  # Espacio antes de paréntesis solo en sentencias de control
SpacesInParentheses: false    # No agrega espacios dentro de paréntesis
SpaceAfterCStyleCast: false   # No deja un espacio después de un cast estilo C
SpaceBeforeRangeBasedForLoopColon: false # No deja espacio antes de los dos puntos en for-ranged loops

### Opciones de formateo adicional
AlignConsecutiveAssignments: false     # No alinea asignaciones consecutivas (Google no lo exige)
AlignConsecutiveDeclarations: false    # No alinea declaraciones consecutivas de variables

### Estilo de funciones y argumentos
AlignAfterOpenBracket: DontAlign       # No alinea los argumentos de funciones
BinPackArguments: true                 # Empaqueta múltiples argumentos en una línea si es posible
BinPackParameters: true                # Empaqueta múltiples parámetros en una línea si es posible

### Espacios en torno a operadores
SpaceBeforeAssignmentOperators: true   # Deja un espacio antes de los operadores de asignación
SpacesInAngles: false                  # No hay espacios dentro de ángulos <>
SpacesInSquareBrackets: false          # No hay espacios dentro de corchetes []
SpaceAfterTemplateKeyword: false       # No deja espacio después de la palabra clave 'template'

### Comportamiento de alineación
AlignTrailingComments: true            # Alinea los comentarios de final de línea
```

Guarda el archivo .clang-format en el directorio raíz de tu proyecto.
## Paso 2: Configurar clang-format en Visual Studio Code
Abre Visual Studio Code.
Ve a Settings (Configuración):
Haz clic en el ícono de engranaje en la esquina inferior izquierda o usa Ctrl + ,.
En el campo de búsqueda, escribe *C_Cpp: Formatting: ClangFormat Style.
Asegúrate de que el valor de esta configuración esté configurado como file:
Esto indica que Visual Studio Code debe usar el archivo .clang-format que colocaste en el directorio raíz del proyecto.*

## Paso 3: Habilitar el formato al guardar
En Settings, busca Format On Save.
Marca la casilla de Editor: Format On Save para habilitar el formato automático cuando guardes los archivos.
## Paso 4: Verificar la configuración
Abre un archivo C++ en Visual Studio Code.
Haz cualquier cambio en el archivo y guarda el documento (Ctrl + S).
Visual Studio Code debería formatear automáticamente el archivo según las reglas especificadas en el archivo .clang-format.
