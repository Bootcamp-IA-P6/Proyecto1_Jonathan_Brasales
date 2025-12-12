# 🚕 Taxímetro en Python

Este proyecto es un simulador de taxímetro desarrollado en Python. La aplicación, controlada por la línea de comandos (CLI) y también a través de una Interfaz Gráfica de Usuario (GUI), no solo calcula la tarifa de un viaje en tiempo real, sino que también incluye un sistema de **logs**, **tests unitarios**, un **historial de trayectos** y **tarifas configurables**. El programa guía al usuario desde el inicio, permite gestionar múltiples trayectos y guarda un registro persistente de cada viaje.

El código fue refactorizado siguiendo principios de **Programación Orientada a Objetos (OOP)**, lo que permite que la misma lógica de negocio funcione tanto para la versión de consola como para la gráfica.

> 📖 **Artículo Detallado del Desarrollo**
> Si quieres conocer el proceso de creación paso a paso (dividido en niveles Esencial, Medio y Avanzado), puedes leer el artículo completo aquí: **[Notion 🌐](https://www.notion.so/Project-1-De-Cero-a-Aplicaci-n-de-Consola-Creando-un-Simulador-de-Tax-metro-en-Python-2c4abdea458e80f4bb6ad935b3e3906a?source=copy_link)**

---
## ✨ Características Principales
*   **Doble Interfaz**: Funciona tanto por línea de comandos (CLI) como con una interfaz gráfica (GUI).
*   **Cálculo de Tarifas Dinámico**: Calcula automáticamente la tarifa diferenciando entre el tiempo en movimiento y el tiempo en parada.
*   **Tarifas Configurables**: Permite ajustar los precios por segundo para adaptarse a diferentes condiciones o tarifas.
*   **Gestión de Múltiples Trayectos**: Inicia un nuevo viaje inmediatamente después de finalizar uno, sin necesidad de reiniciar el programa.
*   **Historial de Viajes**: Guarda un registro detallado de todos los trayectos finalizados en un archivo de texto.
*   **Sistema de Logs**: Incorpora un sistema de logging para facilitar la depuración y la trazabilidad de las operaciones.
*   **Tests Unitarios**: Incluye una suite de pruebas para garantizar la precisión de los cálculos y el correcto funcionamiento del sistema.
*   **Interfaz de Comandos Clara**: Guía al usuario con instrucciones claras sobre cómo operar el taxímetro.
---

## 🛠️ Entorno de Desarrollo y Tecnologías

Este proyecto se ha desarrollado con el siguiente conjunto de herramientas y tecnologías.

*   **Control de versiones**: Git y GitHub 
*   **Lenguaje**: [**Python 3.13.5**](https://www.python.org/ )
*   **Gestor de Entorno**: [**Anaconda**](https://www.anaconda.com/ ) fue utilizado para gestionar las dependencias y el entorno virtual.
*   **Editor de Código**: El desarrollo se realizó en [**Visual Studio Code**](https://code.visualstudio.com/ ).
*   **Librerías Principales**:
    *   `time`: Para la gestión del tiempo y el cálculo de las tarifas.
    *   `logging`: Usado para rastrear los eventos que ocurren cuando se ejecuta el programa.
    *   `datetime`: El módulo datetime proporciona clases para manipular fechas y horas.
    *   `pytest`: Usado para la escritura de pruebas pequeñas y legibles, aunque puede permitir pruebas funcionales complejas para aplicaciones y bibliotecas.
    *   `CustomTkinter`: Biblioteca de Python basada en Tkinter que proporciona widgets modernos, personalizables para crear interfaces gráficas de usuario (GUI) de escritorio.

---

## ⚙️ Instalación y Funcionamiento

Sigue estos pasos para poner en marcha el proyecto en tu máquina local.

### 1. Clona el Repositorio

```bash
git clone https://github.com/Bootcamp-IA-P6/Proyecto1_Jonathan_Brasales.git
cd C:\Users\under\Documents\F5\projects\taximetro\main.py
```

### 2. Configura el Entorno Virtual

Tienes dos opciones para instalar las dependencias. Elige la que prefieras.

#### Opción A: Usando conda (Recomendado)

Este método utiliza el archivo **environment.yml** para recrear el entorno de desarrollo exacto.

```bash
# Crea el entorno a partir del archivo
conda env create -f environment.yml

# Activa el nuevo entorno
conda activate vTaxi
```
#### Opción B: Usando pip y venv

Este es el método estándar de Python si no usas Anaconda.

```bash
# Crea un entorno virtual
python -m venv venv

# Actívalo
# En Windows:
venv\Scripts\activate
# En macOS/Linux:
source venv/bin/activate

# Instala las dependencias
pip install -r requirements.txt
```

### 3. ¡Ejecuta el Programa! ▶️

Una vez que el entorno esté activado y las dependencias instaladas, puedes iniciar el taxímetro con el siguiente comando:
```bash
python main.py
```
O iniciar la GUI:
```bash
python app_gui.py
```
---

## 🚀 Guía de Uso (Versión CLI)

Una vez que el programa está en ejecución, te dará la bienvenida y mostrará los comandos disponibles. El flujo de operación es el siguiente:

1.  **Iniciar un Viaje (`start`)**: Comienza un nuevo trayecto. El taxímetro empezará a contar el tiempo en estado "parado".
2.  **Poner en Movimiento (`move`)**: Cambia al estado "en movimiento" para aplicar la tarifa correspondiente.
3.  **Detener el Taxi (`stop`)**: Vuelve al estado "parado". Puedes alternar entre `move` y `stop` tantas veces como sea necesario.
4.  **Finalizar el Viaje (`finish`)**: Termina el trayecto, calcula la tarifa total y la muestra en pantalla. El viaje se guardará en el historial.
5.  **Salir del Programa (`exit`)**: Cierra la aplicación.

---

## 📒 Metodología de Desarrollo y Aprendizaje
Más allá de ser un simple proyecto de software, este taxímetro fue concebido como un ejercicio práctico para afianzar conceptos clave de Python y, sobre todo, para dominar un flujo de trabajo profesional con Git y GitHub.

### El Flujo de Trabajo con Git y GitHub  

Todo el desarrollo se gestionó siguiendo una metodología basada en ramas, *Pull Requests* y gestión de proyectos, simulando un entorno de equipo.

1.  **Gestión con GitHub Projects:** Se utilizó un tablero de Proyectos en GitHub para organizar las tareas. Cada funcionalidad o bug se convirtió en un *Issue*.
2.  **Desarrollo en Ramas (`feature-branches`):** Ningún cambio se hizo directamente en la rama principal (`main`). Para cada *Issue*, se creaba una nueva rama descriptiva (ej. `feature/add-logging`).
3.  **Commits Atómicos:** Se procuró hacer *commits* pequeños y enfocados en un solo cambio, con mensajes claros que explicaban el "qué" y el "porqué".
4.  **Pull Requests (PRs) para Revisión:** Una vez que una funcionalidad estaba completa en su rama, se abría un *Pull Request* hacia la rama `esencial, medio o avanzado`. El PR servía como un punto de revisión de código (aunque fuera auto-revisión) y enlazaba directamente al *Issue* que resolvía.
5.  **Merge y Cierre:** Tras la "aprobación" del PR, los cambios se fusionaban (`merge`) a la rama principal, cerrando automáticamente el *Issue* asociado.

### Estructura del Desarrollo por Fases

El proyecto se construyó de manera incremental, siguiendo una hoja de ruta clara dividida en tres fases principales. Cada fase se desarrolló en su propia rama de trabajo antes de integrarse a la rama `main`.

*   **🟢 Fase 1: `rama-esencial`**
    *   Creación de la estructura básica del programa CLI.
    *   Implementación de la bienvenida y las instrucciones.
    *   Lógica para `iniciar` y `finalizar` un trayecto.
    *   Cálculo de tarifas diferenciadas para `mover` y `detener`.
    *   Capacidad para encadenar múltiples viajes.

*   **🟡 Fase 2: `rama-medio`**
    *   Implementación de un sistema de `logging` para la trazabilidad.
    *   Creación de `tests unitarios` para validar los cálculos.
    *   Desarrollo de un `historial` de viajes en un archivo de texto.
    *   Externalización de las tarifas a un `archivo de configuración`.

*   **🟠 Fase 3: `rama-avanzado`**
    *   `Refactorización` completa a un diseño Orientado a Objetos (OOP).
    *   Desarrollo de una `Interfaz Gráfica de Usuario (GUI)` con CustomTkinter.

*   **🔵 Rama `main`**
    *   Versión estable del proyecto que integra todas las funcionalidades de las fases/ramas anteriores.

#### Diagrama de Flujo de Ramas (Vertical)

```txt
        main
          |
          ●──> [🟢 feature/esencial] ──> feature/[bienvenida, calculos]
          |
          ●──> [🟡 feature/medio] ──>feature/[logging, históricos]
          |
          ●──> [🟠 feature/avanzado] ──> feature/[Refactorizar, GUI]
          |
        main
```


### Desafíos y Aprendizajes 🧠

*   **El Reto de la Refactorización a OOP:** El mayor desafío técnico fue pasar del código funcional inicial a una arquitectura Orientada a Objetos. Requirió varias iteraciones para lograr una clara separación de responsabilidades.
*   **La Disciplina de los Commits:** Al principio, es tentador hacer un solo `commit` gigante con muchos cambios. Forzarme a hacer commits pequeños y atómicos fue un reto de disciplina, pero el resultado fue un historial de Git fácil de seguir y afianzar los comandos mas utilizados.

Esta metodología no solo resultó en un código más limpio y un historial organizado, sino que también fue una experiencia de aprendizaje inmensamente valiosa sobre cómo se construyen y mantienen los proyectos de software en el mundo real.

## 🐛 Bugs Conocidos y Posibles Mejoras

### Bugs Conocidos
*   Actualmente, no hay bugs conocidos. ¡Si encuentras alguno, no dudes en reportarlo!

### Posibles Mejoras
*   **Exportar Recibos Individuales**: Añadir una función para guardar el resumen de un viaje específico en un archivo PDF o de texto como si fuera un recibo.
*   **Modo noche**: Implementar tarifas nocturnas que se activen automáticamente según la hora del sistema.


---