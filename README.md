Il core del progetto si basa su un motore fisico personalizzato che calcola la gravità newtoniana e prevede le traiettorie orbitali.

🌟 Caratteristiche Principali
1. Motore Fisico e Simulazione
Gravità N-Body (Semplificata): Simulazione dell'attrazione gravitazionale esercitata da più corpi celesti (Sole, Mercurio, Terra, Marte, Giove).

Integratore Runge-Kutta 4 (RK4): Utilizzato per calcolare con precisione la posizione futura della nave e disegnare le linee di traiettoria predittiva, mostrando visivamente Periapside (Pe) e Apoapside (Ap).

Time Warp: Sistema di accelerazione temporale (fino a 256x) per ridurre i tempi di attesa durante i viaggi interplanetari senza perdere stabilità nella simulazione.

2. Avionica e Controlli di Volo (SAS)
Sistema SAS (Stability Assist System): Autopilota in grado di orientare automaticamente la nave verso vettori specifici:

🔴 Target: Punta verso il corpo celeste selezionato.

🟢 Prograde/Retrograde: Allineamento col vettore velocità (per accelerare o frenare).

🔵 Normal/Antinormal: Per cambi di inclinazione orbitale.

NavBall Funzionante: Orizzonte artificiale disegnato su Canvas che ruota in tempo reale mostrando Pitch, Roll e i vettori di manovra.

Controllo Manetta: Slider analogico per la spinta continua e controlli da tastiera (W/S) per impulsi rapidi.

3. Gestione Risorse e Sistemi
Sistema Elettrico (EC): Gestione realistica della carica elettrica.

I pannelli solari generano energia in base alla distanza dal Sole.

Implementazione del Raycasting per simulare le eclissi (i pannelli non caricano se un pianeta oscura il Sole).

Il consumo aumenta usando il SAS o eseguendo esperimenti.

Propellente Liquido: Il carburante si consuma in base alla spinta; l'esaurimento porta allo spegnimento dei motori e alla riduzione della massa della nave (fisica a massa variabile).

4. Modulo Scientifico (Novità v15)
Un pannello dedicato all'esecuzione di esperimenti scientifici in base alla posizione della nave:

Tipologie: Rilevamento Temperatura, Pressione, Radiazioni e Qualità dell'aria.

Logica: I risultati variano in base all'altitudine e al pianeta (es. rilevare "Vuoto" nello spazio profondo o alte temperature vicino al Sole).

Costo Energetico: Ogni esperimento consuma batteria e richiede tempo per essere completato.

Log Risultati: Un registro scorrevole mostra lo storico dei dati raccolti.

🎨 Interfaccia Utente (UI/UX)
L'interfaccia è progettata con uno stile "Retrò-Tech" scuro, utilizzando il font Orbitron per richiamare i display LCD delle strumentazioni spaziali.

HUD Modulare: Pannelli semitrasparenti con bordi luminosi per Telemetria, Risorse, Missione e Controlli.

Minimappa Radar: Visualizzazione tattica della posizione relativa dei pianeti e della nave.

Feedback Visivo: Effetti particellari per la scia del motore, gradienti dinamici per le barre delle risorse e indicatori di stato colorati.

🛠 Stack Tecnologico
HTML5 Canvas: Utilizzato sia per il rendering del gioco (#game), sia per la strumentazione complessa (NavBall, Minimappa).

JavaScript (ES6 Modules): Logica di gioco pura senza framework esterni. Gestione del loop di gioco, input handling e calcoli matematici vettoriali.

CSS3: Layout flessibile (Flexbox/Grid) per posizionare i pannelli dell'interfaccia sopra il canvas (Overlay).

🎮 Comandi
W / S: Spinta massima momentanea / Taglio motore.

A / D: Rotazione nave (Yaw).

Cursore Throttle: Imposta una spinta fissa.

Click su SAS: Attiva le modalità di autopilota.

< / >: Diminuisce/Aumenta il Time Warp.

Rotella Mouse: Zoom In/Out.

Stato del progetto: Funzionante, versione 15 (UI Stabile e Modulo Scientifico implementato).
