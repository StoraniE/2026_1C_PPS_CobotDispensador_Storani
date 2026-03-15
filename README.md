![Logo Institucional](https://github.com/JonatanBogadoUNLZ/PPS-Jonatan-Bogado/blob/9952aac097aca83a1aadfc26679fc7ec57369d82/LOGO%20AZUL%20HORIZONTAL%20-%20fondo%20transparente.png)

# UNLZ — Facultad de Ingeniería (Plantilla de Proyecto)
## Ingeniería Mecatrónica — README + estructura estándar

Este repositorio es una **PLANTILLA**.  
Los estudiantes deben **usar este repo como base** (fork o “Use this template”) y **reemplazar los textos entre corchetes** `[ ... ]` con la información real de su proyecto.

---

2) Editar este archivo `README.md` completando todos los campos `[ ... ]`.

3) Subir archivos a las carpetas correspondientes:
   - Código en `CODIGO/`
   - Planos y esquemas en `PLANOS/`
   - Fotos / videos en `MULTIMEDIA/`
   - Datasheets en `DATASHEET/`
   - Informes en `INFORMES/`

---

## ✅ Checklist de entrega
- [ ] Brief completo (one-liner + pitch + problema + solución + alcance + estado)
- [ ] Instrucciones de uso reproducibles (otro puede correrlo)
- [ ] Lista de componentes con cantidades y modelos
- [ ] Esquemáticos/planos adjuntos en `PLANOS/`
- [ ] Fotos / video demostración en `MULTIMEDIA/`
- [ ] Informe PDF en `INFORMES/` (si aplica)

---

# [Cobot dispensador de piezas]

2026_1C_PPS_CobotDispensador_Storani

**Tipo:** [PPS]  
**Año:** [2026] — **Cuatrimestre:** [1C ]  

**Carrera:** Ingeniería Mecatrónica  
**Materia / Curso:** [NOMBRE_DE_LA_MATERIA]  
**Docente / Cátedra:** [NOMBRE_DOCENTE]  
**Autor/es:** [Storani Ezequiel]

---

**Introducción:**
Debe automatizarse una inyectora de plástico, a la cual se le coloca en un molde un filtro y se le realiza una sobreinyeción de plástico, luego se retira la pieza inyectada

**Contexto:**  
Actualmente se realiza una operación de pick and place para abastecer a la inyectora de plástico de unos filtros (llamados "mantas") a los cuales se los sobreinyecta con polipropilento coloreado para rigidizarlos y se los retira del molde de la inyectora una vez finalizado el proceso de inyección y se los coloca en una caja.

**Problema a resolver:**  
Bajo los nuevos lineaminetos de la empresa se desea automatizar la mayor cantidad de tareas posibles, permitiendo que una persona pueda controlar varias inyectoras de plástico a la vez, en lo particular este proyecto cuenta con una problematica destacada, ya que los objetos que deben colocarse en la matriz de la inyectora ("mantas") son objetos porosos, comprimibles, vienen pegados en ocaciones unos con otros, poseen "pelos" tipo abrojo y no deben mancharse, romperse o rasgarse. Y tienen orientación.

**Objetivo general:**  
Realizar una automatización que coloque estas mantas en la matriz de la inyectora sin dañarlas controlando su orientación y retirando las mismas una vez inyectadas.

**Objetivos específicos (opcional):**
- Separar las mantas individualmente controlando su orientación
- Transladarlas hasta la matriz
- Retirarlas una vez inyectadas
---

## Índice
- [Brief](#brief)
- [Descripción técnica](#descripción-técnica)
- [Arquitectura del sistema](#arquitectura-del-sistema)
- [Instrucciones de uso](#instrucciones-de-uso)
- [Tecnologías utilizadas](#tecnologías-utilizadas)
- [Listado de componentes](#listado-de-componentes)
- [Esquemáticos / Planos](#esquemáticos--planos)
- [Fotos / Videos](#fotos--videos)
- [Estructura del repositorio](#estructura-del-repositorio)
- [Autor](#autor)
- [Licencia](#licencia)

---

## Brief
Pick and place de una tela porosa para una empresa de filtros automatizando un puesto de trabajo.

**Elevator pitch:**  
Este proyecto **Cobot dispoensador de mantas** (tipo **[PPS]**, **[2026] [C1]**) independiza **la inyección de mantas de la intervensión constante de un operario** mediante **la implementación de un brazo antropomorfico colaborativo "cobot"**.
Está orientado a **[una empresa de filtros]** y permite **[independizar al colaborador del proceso, permitiendo que el mismo realize varias tareas y no una sola]**.
Se implementa con **[brazo robótico y un dispositivo dispensador de mantas]** y se valida mediante **[producción automática]**.

### Problema
- **Contexto:** [Industria]
- **Dolor principal:** [Operario unicamente abocado a poner y sacar piezas]
- **Impacto:** [Horas hombre/ piezas fabricadas]

### Solución propuesta
- **Qué hace (features):**
  - Separa uno en uno los filtros.
  - Coloca los filtros en la inyectora.
  - Retira las piezas sobreinyectadas.
- **Cómo lo hace (alto nivel):** Dispositivo dispenzador de filtros → Cobot → inyección → Cobot → Pieza final
- **Valor diferencial:** Al contrario de las propuestas realizadas por distintos proveedores (Argentina y China) esta garantiza la separación unitaria de los filtros, evitando posibles roturas de la matriz de inyección.

### Alcance
**Incluye:**
- Separación de filtros
- Colocación de los mismos
- Retiro de piezas inyectadas
- Verificación y autorización de inyección evitando faltantes de piezas o piezas en posiciones erroneas.

**No incluye (por ahora):**
- Verificación de orientación de filtros (no se encontró método alguno para realizar esta tarea)
- Verificación de pieza correctamente inyectada (Si se cumplen los lineamientos previos no se tiene registro de pieza no conforme)

### Estado del proyecto
- **Madurez:** [en validación]
- **Qué funciona hoy:**
     - Dispenzador de filtros.
     - Colocado de filtros en matrices.
     - Retiro de piezas inyectadas (7 de 8 piezas).
- **Próximos pasos:**
     - Asegurar el retiro exitoso de las 8 piezas inyectadas. (fin de automatización planeada)
- **Oportunidad de mejora:** 
     - Reducción de tiempo de ciclo.
     - Reducción de tiempo de llenado de dispensador de filtros.
     - Implementar el cobot para más procesos.
     - Mejora general de automatización: Mejorar cableado, mejorar dispensador (hoy prototipo de aluminio, a futuro de Acero Inox. con guia lineal)
     - Implementar control de orientacicón de filtros.
     - Implementar control por visión artificial de piezas inyectadas.

### Demo rápida
- **Video / GIF:** [link o ruta en MULTIMEDIA]
- **Instrucciones express (2 minutos):**
  1) [Paso 1]
  2) [Paso 2]
  3) [Paso 3]

---

## Descripción técnica

   - Separación de filtros:
        Al inicio se trato de implementar que el agarre del filtro y la separación uno a uno se realice de forma conjunta por el mismo gripper, esta idea viene de la mano de proveedores de automatización local(Argentina) e internacional(China) los cuales rápidamente sugirieron un agarre por ventosas o por clavado de agujas, ambos sistemas no resultaron satisfactorios en la práctica, ya que tomaban más de un filtro, lo que puede casuar una rotura de la matriz por una inyección descontrolada del material, por lo que fueron descartados rapidamente.
     En paralelo investigué una tecnología poco explotada industrialmente como lo son los SoftGrippers, existiendo una empresa que se dedica a fabricar estos agarres para el mundo de la inyección de plástico y telas [https://www.softroboticgripper.com/], estos por lo visto en videos parecían la solución perfecta, por lo que se decidío comprar un kit base de la marca para realizar pruebas, sin embargo estas pruebas no resultaron satisfactorias y siendo este un recurso solo disponible en china con tiempos de entrega grandes y con la fecha de cierre de proyecto acercandose se decidío descartarlos.
     No obstante a día de hoy sigo pensando que debe existir una configuración que satisfasga la necesidad planteada, siendo superior al sistema implementado, solo que no pudimos conseguirla.
     También se descartó una opción muy interesante que imita a las patas de un Gecko, [https://schunk.com/de/en/gripping-systems/adhesive-grippers/adheso/c/PGR_5510?csot0=downloads&cspt0=tctc&cspc0=seriesTabComponent&cspt1=tcsc&cspc1=categoryVariants&cspfs1=PGR_5510], siendo esta descartada por su elevado costo.
     Con todos los resultados puestos sobre la mesa se decidió avanzar con un dispositivo que separe uno a uno los filtros, el cuál se basa en el principio del funcionamiento de una mandolina (utensillo culinario), este posee una cuchilla con un escalón del espesor de un filtro, por lo que con un movimiento se puede "cortar", en realidad es separar, por cada filtro, recordar que este material es poroso y una de sus superficies es similar a la de un velcro (posee pelos) por lo que se necesita de ese filo para separarlos.
   - Orientación de filtros:
        Desde un comienzo se probaron sistemas de rodillos, actuadores, velcros, cámaras de visión artificail, sensores de colores y sensores opticos para tratar de diferenciar el lado del filtro, ya que esto es importante porque si se inyecta del lado equivocado el filtro no sirve, ya que puede taparse con el uso doméstico con los años, generando un inconveniente que surge con el tiempo, por lo que no es posible validarlo en una etapa posterior de los procesos de la fábrica. Dadas estas condiciones se decide continuar con el ordenamiento de los mismos mediante un operario, como se lo hace actualmente.
   - Agarre de filtros:
        Una vez separados los filtros uno a uno parecería resolverse el problema del agarre, ya que está comprobado que las ventosas por vacío pueden agarrar estos filtros; sin embargo el que sea posible no quiere decir que sea fácil, ya que si tomamos el principio de funcionamiento de la ventosa se intuye que mientras mayor sea la superficie de agarre, sea mayor el caudal de vacío y sea mayor la presión de vacío mejor se va a agarrar la pieza.
        Bueno, no esta vez, ya que es un material poroso; por lo que a mayor área, mayor lugar por donde se pierde vacío, por lo que resulta en que no se agarre a la ventosa, a mayor presión se abren más los poros de la tela, resultando en lo mismo.
        La solución fue, y contra toda lógica, reducir lo máximo el punto de aplicación del vacío, aplicando el mayor caudal posible en ese punto para la presión de entrada, lo que resultó en una "ventosa" de 4mm de diam de superficie de vacío efectivo.
   - Operación del sistema:
        Se analizaron distintos métodos para realizar el pick and place, como lo fueron los robots cartesianos (comunes en inyección de plástico), desplazamientos lineales neumaticos y los brazos antropomórficos, resultando este último el seleccionado ya que no implica modificar estructuralmente a la inyectora, permitiendo retirarlo con un apilador hidráulico para utilizar a la inyectora de forma manual.
   - Funcionamiento del dispensador de filtros (tipo "mandolina"):
        El operario debe colocar en orden y bien orientados los filtros en un tubo cargador, el mismo es encastrado en una posición única sobre el dispositivo separador, el cual bajo el comando del cobot retrae la cuchilla para separar una manta utilizando un pistón neumático para efectuar este movimiento, una vez separado el filtro se lo posiciona con otro pistón neumático para que el cobot pueda tomarlo.
   - Agarre de piezas inyectadas:
        Esta es la parte más sencilla de la automatización, ya que se trata de pienzas neumáticas estándar en el mundo de la inyección de plástico.
     
---

## Arquitectura del sistema

**Entradas (sensores / señales):**
- Sensores del tipo magnéticos reed switch para detectar posiciones.
- Sensores de presión de vacío para detectar si se tomó un filtro de manera exitosa

**Procesamiento / Control:**
- Realizado por el Robot Colaborativo (C5 de AuboRobotics) el mismo puede levantar hasta 5 kilos de carga y cuenta con 16 entradas y 16 salidas.

**Salidas (actuadores / señales):**
- Pinzas neumáticas AA-22 de Gimatic
- Eyectores de vacío de la marcha Schmalz
- Pistones para el movimiento del dispenzador de filtros

**Interfaz (si aplica):**
- [Pantalla / dashboard / app / web]

> (Opcional) Insertar diagrama:
![Diagrama de bloques](PLANOS/diagrama_bloques.png)

---

## Instrucciones de uso

### Requisitos previos
- [Software / IDE]
   - Integrado en el Cobot, no es necesario descargar nada.
- [Drivers / librerías]
   - Idem anterior.
- [Hardware mínimo]
   - Contando con el cobot ya es posible simular el funcionamineto, luego debe implmentarse el gripper para tomar las piezas inyectadas, por último debe colocarse el dispensador para automatizarlo.

### Instalación / Puesta en marcha
1) [Armado de dispensador y estación del robot]
2) [Instalar sensores y señales]
3) [Programación previa, antes de la integración en máquina]
4) [Puesta apunto en inyectora]
5) [Validar funcionamiento]

### Uso
- **Modo normal:**
     Se coloca el Robot colaborativo en el puesto de operación de la inyectora de plástico, se lo asegura a la misma mediante dos tornillos para evitar desfaces y se vinculan mediente la conexión de un cable, con el mismo el robot recibe las señales que le permiten comenzar a moverse dentro de la inyectora.
     La inyectora debe colocarse en modo semi-automático ya que el cobot enviará la confirmación de cuando terminó la tarea de pick and place para que la mesa rotativa de la inyectora intercambie matrices.
     Debe reponerse periodicamente (estimado 1 hora) los filtros en su cargador para que el ciclo no se detenga, al igual que retirar cada 4 horas la caja donde caen las piezas inyectadas a granel.
- **Calibración (si aplica):**
     Al instalarse el conjunto pueden existir desfasajes a los puntos referidos por programa previamente, por ello una vez asegurado a la inyectora con los tornillos de posición se debe calibrar:
     1. Debe referenciarse el centro de la matriz con 4 piezas inyectadas en el, esto debe realizarse sobre el punto del programa llamado "matriz".
     2. Deben referenciarse ambos puntos donde se dejarán los filtros, para esto se debe actualizar el punto de programa llamado "matriz_matas1" y "matriz_matas2".

### Troubleshooting (opcional)
- **Problema:** [Fallo tomar piezas inyectadas] → **Solución:** [Realizar calibración 1]
- **Problema:** [Fallo tomar mantas] → **Solución:** [Revisar estado de ventosas]
- **Problema:** [Fallo cuchilla] → **Solución:** [Retirar la presión del aire del sistema y destabar cuchilla de "mandolina", conectar al aire y reiterar funcionamiento del proegrama]

---

## Tecnologías utilizadas
- **Robótica / Control:** [Robot colaborativo C5 Aubo]
- **Electrónica:** [sensores  / drivers / etc.]
     - Vacuostatos electricos regulables
     - Sensores magneticos tipo Reed Switch
     - Relés 24VDC (aislamiento entre sensores(PNP), inyectora(PNP), controlador del robor(NPN))
- **Programación:** [Online Program en controlador de Cobot]

---

## Listado de componentes

| Componente | Cantidad | Modelo / Especificación | Función |
|---|---:|---|---|
| [Componente 1] | [1] | [Modelo] | [Función] |
| [Componente 2] | [2] | [Modelo] | [Función] |
| [Componente 3] | [1] | [Modelo] | [Función] |

---

## Esquemáticos / Planos
- [Plano/Esquemático 1] → `PLANOS/[archivo]`
- [Plano/Esquemático 2] → `PLANOS/[archivo]`

---

## Fotos / Videos
- Foto 1 → `MULTIMEDIA/[archivo]`
- Foto 2 → `MULTIMEDIA/[archivo]`
- Video demo → https://youtube.com/shorts/cSWNZMFp7aM?feature=share

---

## Estructura del repositorio
- `CODIGO/` — Código fuente del proyecto.
- `MULTIMEDIA/` — Imágenes y videos.
- `PLANOS/` — Esquemáticos y diagramas.
- `DATASHEET/` — Hojas de datos y especificaciones.
- `INFORMES/` — Informes, Gantt, manuales, PDFs.

---

## Autor
**[Storani, Ezequiel]** — [Legajo]  
Contacto: [estorani23@gmial.com / www.linkedin.com/in/ezequiel-storani-5a57673b1]

---

## Licencia
[Definir según la cátedra: MIT / uso académico / etc.]

---

## About (descripción corta del repositorio)
Automatización con robot colaborador para tareas de Pick and Place de materiales porosos.
Usar este texto (o similar) en el campo **About** de GitHub:

**[PPSF] — [CobotDispensador] — FI-UNLZ — [2026] [1C] — [Storani]**
