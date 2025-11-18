<img width="563" height="380" alt="Screenshot 2025-11-18 174353" src="https://github.com/user-attachments/assets/1518e506-c031-4a75-9740-c22a3e053954" />

# 🌟 Caratteristiche Principali


## 🚀 1. Motore Fisico e Simulazione
Il cuore del progetto si basa su una simulazione fisica robusta per garantire un'esperienza di volo realistica.
* **Gravità N-Body (Semplificata):** Simulazione dell'attrazione gravitazionale esercitata da più corpi celesti contemporaneamente (Sole, Mercurio, Terra, Marte, Giove).
* **Integratore Runge-Kutta 4 (RK4):** Algoritmo utilizzato per calcolare con precisione la posizione futura della nave e disegnare le linee di traiettoria predittiva, visualizzando **Periapside (Pe)** e **Apoapside (Ap)**.
* **Time Warp:** Sistema di accelerazione temporale (fino a `256x`) per ridurre i tempi di attesa durante i viaggi interplanetari mantenendo la stabilità della simulazione.

## 🧭 2. Avionica e Controlli di Volo (SAS)
**Sistema SAS (Stability Assist System):** Un autopilota avanzato in grado di orientare automaticamente la nave.
* 🔴 **Target:** Punta verso il corpo celeste selezionato.
* 🟢 **Prograde / Retrograde:** Allineamento col vettore velocità (ottimale per accelerare o frenare).
* 🔵 **Normal / Antinormal:** Essenziale per i cambi di inclinazione orbitale.

<img width="448" height="220" alt="image" src="https://github.com/user-attachments/assets/aaf8a372-dce6-487d-b72e-7164089f1c23" />


> **Strumentazione:** Include una **NavBall** funzionante (orizzonte artificiale su Canvas) che ruota in tempo reale mostrando Pitch, Roll e i vettori di manovra.

## ⚡ 3. Gestione Risorse e Sistemi
La gestione delle risorse è critica per la sopravvivenza della missione.

<img width="442" height="177" alt="image" src="https://github.com/user-attachments/assets/312688e8-8208-40b2-86c0-ff92b898e6f7" />

### Sistema Elettrico (EC)
* Generazione tramite pannelli solari basata sulla distanza dalla stella (Inverse Square Law).
* **Raycasting per Eclissi:** I pannelli smettono di caricare se un pianeta oscura il Sole.
* Consumo dinamico basato sull'uso del SAS e degli esperimenti.

  <img width="202" height="141" alt="image" src="https://github.com/user-attachments/assets/0b97caf0-be6c-4e8f-b6c6-e465cbf5b3b7" />

### Propulsione
* **Fisica a Massa Variabile:** Il consumo di carburante riduce la massa totale della nave, influenzando il Delta-V e l'accelerazione.
* Spegnimento automatico dei motori all'esaurimento del propellente liquido.

## 🔬 4. Modulo Scientifico (Novità v15)
Un pannello interattivo per l'esecuzione di esperimenti *in-situ*.
* **Tipologie:** Rilevamento Temperatura, Pressione, Radiazioni e Qualità dell'aria.
* **Logica Contestuale:** I risultati cambiano in base all'altitudine (es. vuoto dello spazio vs atmosfera) e alla vicinanza al Sole.
* **Log:** Un registro scorrevole storico dei dati raccolti.

## 🎨 Interfaccia Utente (UI/UX)
Stile **"Retrò-Tech"** scuro con font *Orbitron*, ispirato ai display LCD delle vere strumentazioni spaziali.
* **HUD Modulare:** Pannelli semitrasparenti con bordi luminosi per Telemetria, Risorse e Controlli.
* **Minimappa Radar:** Visualizzazione tattica della posizione relativa dei pianeti.
* **Feedback Visivo:** Effetti particellari per i motori e gradienti dinamici per le barre delle risorse.

## 🛠 Stack Tecnologico
Il progetto è costruito senza engine grafici pesanti, utilizzando tecnologie web native.

| Componente | Tecnologia | Utilizzo |
| :--- | :--- | :--- |
| **Rendering** | `HTML5 Canvas` | Rendering del gioco e della strumentazione complessa (NavBall). |
| **Logica** | `JavaScript (ES6)` | Moduli nativi, loop di gioco, calcoli vettoriali e fisica. |
| **Styling** | `CSS3` | Layout Flexbox/Grid per l'overlay dell'interfaccia (HUD). |

## 🎮 Comandi

| Tasto | Azione |
| :--- | :--- |
| `W` / `S` | Spinta massima momentanea / Taglio motore (Cutoff) |
| `A` / `D` | Rotazione nave (Yaw) |
| `Cursore` | Imposta Throttle fisso (Manetta) |
| `Click (UI)` | Attiva modalità SAS |
| `<` / `>` | Diminuisce / Aumenta il Time Warp |
| `Rotella Mouse` | Zoom In / Out |

---
**Stato del progetto:** 🟢 Funzionante (v15) - UI Stabile e Modulo Scientifico implementato.
