# Tecnológico de Software
## Materia: Sistemas Operativos
## Alumno: Michelle Cámara, Carlos Llanes, Noe Euan
## Actividad: Simulador HTML

-----
# Introducción

En este proyecto se realizó un simulador interactivo diseñado para visualizar y comprender cómo el Sistema Operativo gestiona la memoria mediante **particiones fijas** y **particiones variables**. El objetivo de este simulador es observar cómo los procesos son asignados, cómo se genera la fragmentación y cómo se optimiza el espacio según el algoritmo de ajust (First-Fit, Worst-Fit, Best-Fit).

# Instrucciones de uso

1. **Configurar la Memoria**: Define el tamaño total de la memoria RAM y la unidad de medida en el panel de configuración.
2. **Gestionar Procesos**: Agrega procesos manualmente indicando su nombre y tamaño. 
3. **Ejecutar simulación**: Pulsar *"Ejecutar"* para ver una comparación automática y simultánea entre los algoritmos.
4. **Interactuar con el mapa**: Haz click en cualquier bloque asignado en el mapa de memoria para liberarlo manualmente y observar cómo los espacios libres se juntan. 
5. **Pruebas de estrés**: Utiliza el botón *"Fragmentar"* para crear un escenario de memoria dispersa y luego intenta *"Probar acceso grande

--- 

# ¿Qué va a observar? 

* *Mapas de memoria dinámicos*: Dos columnas que representan la RAM, donde los bloques de colores son procesos activos y los bloques claros son espacios libres.
* *Log de Acciones*: Un registro en tiempo real de cada asignación, fallo o liberación realizada.
* *Indicadores visualeS*: Los bloques se colorean al ser seleccionados por el algoritmo antes de la asignación.

---

# Resultados

* *Utilización (%)*: Indica qué porcentaje de la memoria total está ocupada por preocesos.

* *Fragmentación externa*: Suma de todos los espacios libros no contiguos. Si un proceso grande no cabe a pesar de haber suficiente espacio, es por este problema.

* *Compactación*: Solución a la fragmentación externa.

---

# Algoritmos

* **Best-Fit**: El algoritmo recorre la memoria y elige el hueco más pequeño sea suficiente para el proceso. 

* **Worst-Fit**: El algoritmo busca el hueco más grande disponible en toda la memoria.

---
# Reflexión

Este simulador nos ayudó a entender un poco mejor cómo se divide la memoria con respecto a los procesos. Ademas, del uso de los algoritmos vistos en clases, como el best-fit que aprovecha el mejor espacio con procesos de tamaños variados, mientras que el worst-fit intenta prevenir la fragmentación externa. La simulación nos muestra como se genera este problema y cómo es el principal enemigo de la partición dinámica. 

---
# Referencias
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Wiley.

Tanenbaum, A. S., & Bos, H. (2014). Modern Operating Systems. Pearson.

----

# Cláusula de Uso de IA

**Nombre del estudiante**: Michelle Cámara González

**IA utilizada**: Gemini AI

**Propósito**: Diseño de interfaz de usuario mediante CSS.

**Prompt**: Podrías ayudarme en la implementación del CSS, quiero que se vea mejor, podrías darle un formato bonito

**Archivos adjuntos**: N/A

**Respuesta**: Claro Michelle 💙✨
Vamos a convertir tu simulador en algo que se vea más profesional, limpio y moderno, como proyecto de Sistemas Operativos 👩🏻‍💻🔥

Te voy a dar:

✅ Diseño tipo dashboard
✅ Tarjetas (cards)
✅ Botones modernos
✅ Colores agradables
✅ Memoria con animación
✅ Mejor tipografía
✅ Fragmentación destacada

🎨 NUEVO CSS (Reemplaza completamente tu <style>)

Sustituye todo tu bloque <style> por este:

<style>

body{
    margin:0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #1e3c72, #2a5298);
    color:#fff;
    display:flex;
    flex-direction:column;
    align-items:center;
    padding:30px;
}

h2{
    margin-bottom:20px;
    font-weight:600;
    letter-spacing:1px;
}

.container{
    display:flex;
    gap:40px;
    flex-wrap:wrap;
    justify-content:center;
    align-items:flex-start;
}

.card{
    background:white;
    color:#333;
    padding:20px;
    border-radius:15px;
    box-shadow:0 15px 30px rgba(0,0,0,0.3);
    width:350px;
}

.card h3{
    margin-top:0;
    text-align:center;
}

input, select{
    width:100%;
    padding:10px;
    margin:8px 0;
    border-radius:8px;
    border:1px solid #ccc;
    font-size:14px;
}

button{
    width:100%;
    padding:10px;
    margin-top:10px;
    border:none;
    border-radius:8px;
    background:#2a5298;
    color:white;
    font-weight:bold;
    cursor:pointer;
    transition:0.3s;
}

button:hover{
    background:#1e3c72;
    transform:scale(1.03);
}

#memory{
    width:300px;
    height:500px;
    border-radius:15px;
    overflow:hidden;
    box-shadow:0 15px 30px rgba(0,0,0,0.4);
    display:flex;
    flex-direction:column-reverse;
    background:white;
}

.block{
    width:100%;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:12px;
    font-weight:bold;
    transition:0.4s ease;
}

.free{
    background:#e0e0e0;
    color:#333;
}

.fragmentation-box{
    margin-top:15px;
    padding:10px;
    background:#ff6b6b;
    border-radius:10px;
    text-align:center;
    font-weight:bold;
    color:white;
    box-shadow:0 5px 15px rgba(0,0,0,0.2);
}

footer{
    margin-top:20px;
    font-size:12px;
    opacity:0.8;
}

</style>

🧱 También debes envolver tu HTML así:

Reemplaza tu estructura actual por esta dentro del <body>:

<h2>Simulador de Memoria RAM</h2>

<div class="container">

    <div class="card">
        <h3>Configuración</h3>

        <label>Memoria Total (KB)</label>
        <input type="number" id="totalMemory" value="1000">
        <button onclick="initMemory()">Inicializar Memoria</button>

        <hr>

        <label>Tamaño del Proceso (KB)</label>
        <input type="number" id="processSize">

        <label>Algoritmo</label>
        <select id="algorithm">
            <option value="best">Best-Fit</option>
            <option value="worst">Worst-Fit</option>
        </select>

        <button onclick="addProcess()">Asignar Proceso</button>
        <button onclick="resetMemory()">Resetear</button>

        <div class="fragmentation-box">
            Fragmentación Externa:
            <span id="fragmentation">0</span> KB
        </div>
    </div>

    <div id="memory"></div>

</div>

<footer>
Proyecto Sistemas Operativos - Simulación de Gestión de Memoria
</footer>

💎 ¿Qué mejoras visuales tiene ahora?

✔ Fondo degradado elegante
✔ Tarjetas tipo aplicación moderna
✔ Botones con hover animado
✔ Sombra en memoria
✔ Fragmentación resaltada en rojo
✔ Diseño limpio y profesional

🔥 Si quieres hacerlo aún MÁS pro puedo agregar:

🎨 Colores distintos para cada proceso (sin repetir)

📊 Barra de porcentaje de uso

💾 Botón para liberar procesos

🧠 Comparador Best vs Worst lado a lado

✨ Animación cuando se asigna memoria

📑 Tabla detallada abajo

🌙 Modo oscuro / claro

Si quieres que quede nivel proyecto final para entregar, lo dejamos estilo:

🖥 Simulador tipo sistema operativo real
con bloques horizontales tipo Windows/Linux

¿Lo hacemos versión premium? 😏💙


**Nombre del estudiante**: Carlos Alfonso Llanes Rodríguez

**IA utilizada**: Chat-GPT

**Propósito**: Realizar el simulador html.

**Prompt**: Ayúdame a realizar un simulador html para la división de memoria RAM donde pueda observar la fragmentación, y los algoritmos best fit y worst fit.

**Archivos adjuntos**: N/A

**Respuesta**: Perfecto Carlos 👩🏻‍💻✨
Te voy a dar un simulador completo en HTML + CSS + JavaScript que:

✅ Permite definir tamaño de memoria
✅ Agregar procesos dinámicamente
✅ Elegir algoritmo: Best-Fit o Worst-Fit
✅ Visualizar bloques en forma gráfica
✅ Ver fragmentación externa
✅ Reiniciar memoria

Lo puedes abrir directamente en tu navegador.

📌 ¿Qué simula?

Memoria representada como bloques verticales

Procesos asignados con colores

Espacios libres en gris

Cálculo de fragmentación externa

Comparación visual entre Best-Fit y Worst-Fit

🧠 Recordatorio rápido

Best-Fit: asigna al bloque libre más pequeño posible que quepa.

Worst-Fit: asigna al bloque libre más grande disponible.

Aquí observaremos fragmentación externa.

💻 SIMULADOR COMPLETO

Copia esto en un archivo llamado:

simulador_memoria.html

<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Simulador de Memoria RAM</title>
<style>
body{
    font-family: Arial;
    text-align:center;
}

#memory{
    width:300px;
    height:500px;
    border:3px solid black;
    margin:20px auto;
    display:flex;
    flex-direction:column-reverse;
}

.block{
    width:100%;
    border-top:1px solid black;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:12px;
    color:white;
}

.free{
    background:#ccc;
    color:black;
}

.controls{
    margin:10px;
}
</style>
</head>
<body>

<h2>Simulador de División de Memoria RAM</h2>

<div class="controls">
Memoria Total (KB):
<input type="number" id="totalMemory" value="1000">
<button onclick="initMemory()">Inicializar</button>
</div>

<div class="controls">
Tamaño Proceso (KB):
<input type="number" id="processSize">
<select id="algorithm">
<option value="best">Best-Fit</option>
<option value="worst">Worst-Fit</option>
</select>
<button onclick="addProcess()">Asignar</button>
<button onclick="resetMemory()">Reset</button>
</div>

<h3>Fragmentación Externa: <span id="fragmentation">0</span> KB</h3>

<div id="memory"></div>

<script>

let memoryBlocks = [];
let totalMemory = 1000;

function initMemory(){
    totalMemory = parseInt(document.getElementById("totalMemory").value);
    memoryBlocks = [{size: totalMemory, free: true}];
    renderMemory();
}

function resetMemory(){
    initMemory();
}

function addProcess(){
    let size = parseInt(document.getElementById("processSize").value);
    let algo = document.getElementById("algorithm").value;

    let index = -1;

    if(algo === "best"){
        let minDiff = Infinity;
        for(let i=0;i<memoryBlocks.length;i++){
            if(memoryBlocks[i].free && memoryBlocks[i].size >= size){
                let diff = memoryBlocks[i].size - size;
                if(diff < minDiff){
                    minDiff = diff;
                    index = i;
                }
            }
        }
    }

    if(algo === "worst"){
        let maxSize = -1;
        for(let i=0;i<memoryBlocks.length;i++){
            if(memoryBlocks[i].free && memoryBlocks[i].size >= size){
                if(memoryBlocks[i].size > maxSize){
                    maxSize = memoryBlocks[i].size;
                    index = i;
                }
            }
        }
    }

    if(index === -1){
        alert("No hay espacio suficiente");
        return;
    }

    let block = memoryBlocks[index];

    if(block.size > size){
        memoryBlocks.splice(index,1,
            {size:size, free:false},
            {size:block.size-size, free:true}
        );
    } else {
        memoryBlocks[index].free = false;
    }

    renderMemory();
}

function calculateFragmentation(){
    let freeSpaces = memoryBlocks.filter(b => b.free);
    let totalFree = freeSpaces.reduce((sum,b)=>sum+b.size,0);
    let largestFree = 0;

    freeSpaces.forEach(b=>{
        if(b.size > largestFree) largestFree = b.size;
    });

    return totalFree - largestFree;
}

function renderMemory(){
    let container = document.getElementById("memory");
    container.innerHTML = "";

    memoryBlocks.forEach(block=>{
        let div = document.createElement("div");
        div.classList.add("block");

        let heightPercent = (block.size / totalMemory)*100;
        div.style.height = heightPercent + "%";

        if(block.free){
            div.classList.add("free");
            div.innerText = "Libre ("+block.size+" KB)";
        } else {
            div.style.background = randomColor();
            div.innerText = "Proceso ("+block.size+" KB)";
        }

        container.appendChild(div);
    });

    document.getElementById("fragmentation").innerText =
        calculateFragmentation();
}

function randomColor(){
    return "#"+Math.floor(Math.random()*16777215).toString(16);
}

initMemory();

</script>

</body>
</html>

🎯 Cómo usarlo

Inicializa memoria (ej. 1000 KB)

Agrega procesos con diferentes tamaños

Cambia entre Best-Fit y Worst-Fit

Observa cómo cambia la fragmentación externa

Compara visualmente

🔬 Qué puedes probar para tu examen

Ejemplo:

Memoria = 1000
Procesos = 200, 300, 100, 150

Luego agrega uno de 250 KB.

👉 Verás cómo Best-Fit y Worst-Fit generan diferente distribución.

🚀 Si quieres versión más avanzada puedo agregarte:

❌ Botón para liberar procesos

📊 Gráfica comparativa automática

🧠 First-Fit también

📈 Cálculo de eficiencia

📑 Tabla detallada de asignaciones

🎨 Visualización horizontal tipo SO real

💾 Simulación de compactación

Si quieres, te hago una versión tipo proyecto final para Sistemas Operativos más profesional con:

Diseño moderno

Explicación teórica integrada

Comparador automático Best vs Worst

Reporte imprimible

¿La hacemos más pro? 😏💙

Yo, Noé Guillermo Euan Herrera, no utilicé IA para la implemetación de el README.md, y tengo información que avala mi trabajo.
