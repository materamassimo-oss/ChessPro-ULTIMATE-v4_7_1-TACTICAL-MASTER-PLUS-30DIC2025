<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chess Pro Ultimate v4.7.1 - Help Guide / Guida Completa</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.3);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 30px;
            text-align: center;
        }

        .header h1 {
            font-size: 2rem;
            margin-bottom: 10px;
        }

        .header .version {
            font-size: 1.2rem;
            opacity: 0.9;
        }

        .lang-switch {
            text-align: center;
            padding: 15px;
            background: #f8f9fa;
            border-bottom: 2px solid #667eea;
        }

        .lang-btn {
            background: white;
            border: 2px solid #667eea;
            color: #667eea;
            padding: 8px 20px;
            margin: 0 5px;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s;
        }

        .lang-btn:hover {
            background: #667eea;
            color: white;
        }

        .lang-btn.active {
            background: #667eea;
            color: white;
        }

        .content {
            padding: 30px;
        }

        .lang-section {
            display: none;
        }

        .lang-section.active {
            display: block;
        }

        h2 {
            color: #667eea;
            margin-top: 30px;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 3px solid #667eea;
            font-size: 1.8rem;
        }

        h3 {
            color: #764ba2;
            margin-top: 25px;
            margin-bottom: 12px;
            font-size: 1.4rem;
        }

        h4 {
            color: #555;
            margin-top: 15px;
            margin-bottom: 8px;
            font-size: 1.1rem;
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }

        .feature-card {
            background: #f8f9fa;
            padding: 15px;
            border-radius: 10px;
            border-left: 4px solid #667eea;
        }

        .feature-card h4 {
            color: #667eea;
            margin-top: 0;
        }

        .shortcut-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background: white;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }

        .shortcut-table th {
            background: #667eea;
            color: white;
            padding: 12px;
            text-align: left;
            font-weight: 600;
        }

        .shortcut-table td {
            padding: 12px;
            border-bottom: 1px solid #e0e0e0;
        }

        .shortcut-table tr:hover {
            background: #f8f9fa;
        }

        .key {
            display: inline-block;
            background: #e9ecef;
            border: 2px solid #ced4da;
            border-radius: 4px;
            padding: 4px 10px;
            font-family: 'Courier New', monospace;
            font-weight: 600;
            font-size: 0.9rem;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        .pattern-list {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 12px;
            margin: 20px 0;
        }

        .pattern-item {
            background: #f8f9fa;
            padding: 12px;
            border-radius: 8px;
            border-left: 3px solid #28a745;
        }

        .pattern-item.advanced {
            border-left-color: #ffc107;
        }

        .pattern-item.master {
            border-left-color: #dc3545;
        }

        .tip-box {
            background: #fff3cd;
            border-left: 4px solid #ffc107;
            padding: 15px;
            margin: 20px 0;
            border-radius: 6px;
        }

        .tip-box strong {
            color: #856404;
        }

        .warning-box {
            background: #f8d7da;
            border-left: 4px solid #dc3545;
            padding: 15px;
            margin: 20px 0;
            border-radius: 6px;
        }

        .info-box {
            background: #d1ecf1;
            border-left: 4px solid #17a2b8;
            padding: 15px;
            margin: 20px 0;
            border-radius: 6px;
        }

        code {
            background: #f4f4f4;
            padding: 2px 6px;
            border-radius: 3px;
            font-family: 'Courier New', monospace;
        }

        ul {
            margin-left: 20px;
            margin-bottom: 15px;
        }

        li {
            margin-bottom: 8px;
        }

        .footer {
            background: #f8f9fa;
            padding: 20px;
            text-align: center;
            color: #666;
            margin-top: 30px;
        }

        @media print {
            body {
                background: white;
                padding: 0;
            }
            .lang-switch {
                display: none;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>♔ Chess Pro Ultimate ♚</h1>
            <div class="version">Version 4.7.1 TACTICAL MASTER+</div>
            <div style="margin-top: 15px; font-size: 0.9rem;">
                Complete User Guide / Guida Completa Utente
            </div>
        </div>

        <div class="lang-switch">
            <button class="lang-btn active" onclick="switchLang('it')">🇮🇹 Italiano</button>
            <button class="lang-btn" onclick="switchLang('en')">🇬🇧 English</button>
        </div>

        <div class="content">
            <!-- ITALIAN VERSION -->
            <div id="lang-it" class="lang-section active">
                <h2>📖 Guida Completa - Chess Pro Ultimate v4.7.1</h2>
                
                <div class="info-box">
                    <strong>Benvenuto!</strong> Questa è la guida completa alla versione 4.7.1 TACTICAL MASTER+ del Chess Pro Ultimate.
                    Questa versione include 13 pattern tattici avanzati, supporto Stockfish locale/online, integrazione Lichess API,
                    scorciatoie da tastiera complete e controlli touch ottimizzati.
                </div>

                <h3>🎮 Controlli e Input</h3>

                <h4>⌨️ Scorciatoie da Tastiera (Novità v4.7.1!)</h4>
                <p>Controllo rapido e completo da tastiera per utenti PC:</p>
                
                <table class="shortcut-table">
                    <tr>
                        <th>Tasto</th>
                        <th>Funzione</th>
                        <th>Descrizione</th>
                    </tr>
                    <tr>
                        <td><span class="key">Z</span> o <span class="key">Ctrl+Z</span></td>
                        <td>Annulla</td>
                        <td>Annulla l'ultima mossa (tua + AI)</td>
                    </tr>
                    <tr>
                        <td><span class="key">N</span></td>
                        <td>Nuova Partita</td>
                        <td>Inizia una nuova partita</td>
                    </tr>
                    <tr>
                        <td><span class="key">H</span></td>
                        <td>Aiuto/Hint</td>
                        <td>Mostra suggerimento mossa migliore</td>
                    </tr>
                    <tr>
                        <td><span class="key">F</span></td>
                        <td>Capovolgi</td>
                        <td>Capovolgi la scacchiera</td>
                    </tr>
                    <tr>
                        <td><span class="key">R</span></td>
                        <td>Abbandona</td>
                        <td>Abbandona la partita corrente</td>
                    </tr>
                    <tr>
                        <td><span class="key">Space</span></td>
                        <td>Auto Play</td>
                        <td>Attiva/disattiva modalità automatica</td>
                    </tr>
                    <tr>
                        <td><span class="key">A</span></td>
                        <td>Analizza</td>
                        <td>Analizza la partita completa</td>
                    </tr>
                    <tr>
                        <td><span class="key">T</span></td>
                        <td>Analisi Tattica</td>
                        <td>Mostra/nascondi pattern tattici</td>
                    </tr>
                    <tr>
                        <td><span class="key">S</span></td>
                        <td>Toggle Stockfish</td>
                        <td>Passa tra Stockfish locale/online</td>
                    </tr>
                    <tr>
                        <td><span class="key">?</span></td>
                        <td>Guida Rapida</td>
                        <td>Mostra elenco scorciatoie</td>
                    </tr>
                </table>

                <div class="tip-box">
                    <strong>💡 Suggerimento:</strong> Usa le scorciatoie da tastiera per un controllo velocissimo! 
                    Ogni volta che usi una scorciatoia, vedrai un toast di conferma verde in basso.
                </div>

                <h4>📱 Controlli Touch Mobile (Ottimizzati v4.7.1!)</h4>
                <div class="feature-grid">
                    <div class="feature-card">
                        <h4>Tap</h4>
                        <p>Seleziona e muovi i pezzi</p>
                    </div>
                    <div class="feature-card">
                        <h4>Double Tap</h4>
                        <p>Richiedi suggerimento rapido</p>
                    </div>
                    <div class="feature-card">
                        <h4>Swipe Left (Fuori scacchiera)</h4>
                        <p>Annulla ultima mossa</p>
                    </div>
                    <div class="feature-card">
                        <h4>Drag & Drop</h4>
                        <p>Trascina pezzi sulla scacchiera</p>
                    </div>
                </div>

                <div class="warning-box">
                    <strong>🎯 FIX v4.7.1:</strong> Lo swipe ora è DISABILITATO sulla scacchiera! 
                    Non farai più undo accidentale quando muovi i pezzi. Lo swipe funziona solo sui pannelli laterali.
                </div>

                <h3>🧠 Motore AI e Stockfish</h3>

                <h4>Due Modalità Stockfish</h4>
                <div class="feature-grid">
                    <div class="feature-card">
                        <h4>🏠 Stockfish Locale</h4>
                        <p><strong>Pro:</strong> Funziona offline, privacy totale</p>
                        <p><strong>Contro:</strong> Più lento su mobile</p>
                    </div>
                    <div class="feature-card">
                        <h4>☁️ Stockfish Online</h4>
                        <p><strong>Pro:</strong> Velocissimo, calcolo cloud</p>
                        <p><strong>Contro:</strong> Richiede connessione internet</p>
                    </div>
                </div>

                <p><strong>Come cambiare:</strong> Clicca il bottone "Stockfish" nella sidebar o premi <span class="key">S</span></p>

                <h4>⚙️ Livelli Difficoltà AI</h4>
                <ul>
                    <li><strong>Facile:</strong> Depth 1, perfetto per principianti</li>
                    <li><strong>Medio:</strong> Depth 3, giocatore intermedio</li>
                    <li><strong>Difficile:</strong> Depth 5, giocatore avanzato</li>
                    <li><strong>Esperto:</strong> Depth 7, molto forte</li>
                    <li><strong>Master:</strong> Depth 10+, livello maestro</li>
                </ul>

                <h3>🌐 Integrazione Lichess API</h3>

                <h4>📖 Opening Explorer</h4>
                <p>Quando la partita ha ≥20 pezzi (fase di apertura), il sistema consulta automaticamente il database Lichess per mostrarti:</p>
                <ul>
                    <li>Mosse più giocate in questa posizione</li>
                    <li>Statistiche vittorie/patte/sconfitte</li>
                    <li>Frequenza delle mosse</li>
                    <li>Teoria delle aperture</li>
                </ul>

                <h4>🎯 Tablebase (Finali Perfetti)</h4>
                <p>Quando restano ≤7 pezzi, il sistema consulta le tablebase Lichess per calcoli perfetti:</p>
                <ul>
                    <li>Mossa ottimale garantita</li>
                    <li>Valutazione precisa (Vince/Patta/Perde)</li>
                    <li>Numero di mosse alla vittoria</li>
                    <li>Gioco perfetto nei finali</li>
                </ul>

                <h3>⚡ Sistema Analisi Tattica (13 Pattern!)</h3>

                <p>Attiva con il bottone "Analisi Tattica" o premi <span class="key">T</span></p>

                <h4>📊 Pattern Base (v4.4.0)</h4>
                <div class="pattern-list">
                    <div class="pattern-item">
                        <strong>🔱 FORK</strong><br>
                        Un pezzo attacca 2+ pezzi nemici contemporaneamente
                    </div>
                    <div class="pattern-item">
                        <strong>📌 PIN</strong><br>
                        Pezzo inchiodato non può muoversi senza esporre pezzo più prezioso
                    </div>
                    <div class="pattern-item">
                        <strong>🎯 SKEWER</strong><br>
                        Attacco penetrante: pezzo costretto a muoversi, esponendo quello dietro
                    </div>
                </div>

                <h4>🎪 Pattern Fondamentali (v4.5.0)</h4>
                <div class="pattern-list">
                    <div class="pattern-item">
                        <strong>🎪 HANGING</strong><br>
                        Pezzo non difeso, facilmente catturabile
                    </div>
                    <div class="pattern-item">
                        <strong>👑 BACK RANK</strong><br>
                        Re intrappolato sulla prima traversa, vulnerabile a matto
                    </div>
                    <div class="pattern-item">
                        <strong>🔄 OVERLOADED</strong><br>
                        Pezzo che difende troppe cose contemporaneamente
                    </div>
                    <div class="pattern-item">
                        <strong>⚡ DOUBLE CHECK</strong><br>
                        Scacco da due pezzi simultaneamente (devastante!)
                    </div>
                </div>

                <h4>🔥 Pattern Avanzati (v4.6.0)</h4>
                <div class="pattern-list">
                    <div class="pattern-item advanced">
                        <strong>💥 DISCOVERED</strong><br>
                        Pezzo si muove scoprendo attacco del pezzo dietro
                    </div>
                    <div class="pattern-item advanced">
                        <strong>🚫 TRAPPED</strong><br>
                        Pezzo intrappolato senza vie di fuga sicure
                    </div>
                    <div class="pattern-item advanced">
                        <strong>🔍 X-RAY</strong><br>
                        Attacco attraverso un pezzo verso il bersaglio dietro
                    </div>
                </div>

                <h4>🎖️ Pattern MASTER (v4.7.0 - Novità!)</h4>
                <div class="pattern-list">
                    <div class="pattern-item master">
                        <strong>🎣 DEFLECTION</strong><br>
                        Forza un difensore a lasciare una posizione critica con sacrificio
                    </div>
                    <div class="pattern-item master">
                        <strong>🚧 INTERFERENCE</strong><br>
                        Blocca una linea difensiva nemica piazzando un pezzo
                    </div>
                    <div class="pattern-item master">
                        <strong>🔓 CLEARANCE</strong><br>
                        Sgombera una linea per permettere attacco devastante
                    </div>
                </div>

                <div class="info-box">
                    <strong>ℹ️ Come funziona:</strong> I pattern tattici vengono evidenziati sulla scacchiera con emoji animate.
                    Ogni pattern mostra la severità (Critical/High/Medium) e il materiale minacciato.
                </div>

                <h3>📊 Sistema Analisi Partita</h3>

                <h4>Metriche Disponibili</h4>
                <ul>
                    <li><strong>Precisione:</strong> % di mosse buone/eccellenti</li>
                    <li><strong>Classificazione mosse:</strong> Eccellenti, Buone, Imprecise, Errori, Blunder</li>
                    <li><strong>Statistiche fase:</strong> Apertura, Mediogioco, Finale</li>
                    <li><strong>Valutazione posizione:</strong> Centipawn per ogni mossa</li>
                    <li><strong>Probabilità vittoria:</strong> Grafico in tempo reale</li>
                    <li><strong>Tempo speso:</strong> Per ogni mossa</li>
                </ul>

                <h4>Export Disponibili</h4>
                <ul>
                    <li><strong>PGN:</strong> Standard chess notation</li>
                    <li><strong>PGN Annotato:</strong> Con commenti e valutazioni</li>
                    <li><strong>JSON:</strong> Dati completi analisi</li>
                    <li><strong>HTML Report:</strong> Report completo visualizzabile</li>
                </ul>

                <h3>🎯 Suggerimenti per Giocare al Meglio</h3>

                <div class="tip-box">
                    <strong>💡 Per Principianti:</strong>
                    <ul>
                        <li>Usa difficoltà Facile o Media</li>
                        <li>Attiva Analisi Tattica per imparare i pattern</li>
                        <li>Usa Hint (<span class="key">H</span>) quando sei bloccato</li>
                        <li>Studia i suggerimenti Opening Explorer</li>
                    </ul>
                </div>

                <div class="tip-box">
                    <strong>💡 Per Giocatori Intermedi:</strong>
                    <ul>
                        <li>Gioca Difficile o Esperto</li>
                        <li>Analizza le partite per capire gli errori</li>
                        <li>Prova a trovare i pattern tattici prima di attivarli</li>
                        <li>Usa Stockfish Online per analisi veloce</li>
                    </ul>
                </div>

                <div class="tip-box">
                    <strong>💡 Per Esperti:</strong>
                    <ul>
                        <li>Master level con Stockfish Online</li>
                        <li>Sperimenta con i pattern MASTER (Deflection, Interference, Clearance)</li>
                        <li>Analizza profondità Multi-PV per varianti alternative</li>
                        <li>Usa keyboard shortcuts per velocità massima</li>
                    </ul>
                </div>

                <h3>❓ FAQ - Domande Frequenti</h3>

                <h4>Q: Come evito l'undo accidentale su mobile?</h4>
                <p><strong>A:</strong> Con la v4.7.1 il problema è risolto! Lo swipe è disabilitato sulla scacchiera. 
                Puoi muovere i pezzi senza preoccuparti. Lo swipe funziona solo sui pannelli laterali.</p>

                <h4>Q: Quale Stockfish usare?</h4>
                <p><strong>A:</strong> Su PC usa quello che preferisci. Su mobile, Stockfish Online è molto più veloce.</p>

                <h4>Q: Posso giocare offline?</h4>
                <p><strong>A:</strong> Sì! Usa Stockfish Locale. Le API Lichess (Opening Explorer e Tablebase) richiedono connessione.</p>

                <h4>Q: Come migliorare velocemente?</h4>
                <p><strong>A:</strong> Attiva sempre Analisi Tattica, studia i pattern dopo ogni partita, e analizza gli errori.</p>

                <h4>Q: I pattern tattici rallentano il gioco?</h4>
                <p><strong>A:</strong> L'analisi tattica è leggera e non influisce sulle prestazioni. Si aggiorna ogni 2 secondi.</p>

                <h3>🔧 Risoluzione Problemi</h3>

                <h4>La scacchiera non appare</h4>
                <ul>
                    <li>Ricarica la pagina (F5)</li>
                    <li>Verifica la console browser per errori</li>
                    <li>Controlla che JavaScript sia abilitato</li>
                </ul>

                <h4>Stockfish è lento</h4>
                <ul>
                    <li>Passa a Stockfish Online (pulsante o <span class="key">S</span>)</li>
                    <li>Riduci la difficoltà AI</li>
                    <li>Chiudi altre tab del browser</li>
                </ul>

                <h4>API Lichess non funziona</h4>
                <ul>
                    <li>Verifica connessione internet</li>
                    <li>Controlla che lichess.org sia raggiungibile</li>
                    <li>A volte le API hanno rate limits, riprova dopo un minuto</li>
                </ul>

                <h3>📝 Note sulla Versione</h3>

                <h4>v4.7.1 TACTICAL MASTER+ (30 Dicembre 2025)</h4>
                <ul>
                    <li>✅ <strong>FIX:</strong> Swipe disabilitato sulla scacchiera (no più undo accidentale)</li>
                    <li>✅ <strong>NUOVO:</strong> Sistema completo keyboard shortcuts (10 scorciatoie)</li>
                    <li>✅ <strong>NUOVO:</strong> Feedback visivo toast per shortcuts</li>
                    <li>✅ Migliorata gestione touch events</li>
                    <li>✅ Aggiunta guida help bilingue (IT/EN)</li>
                </ul>

                <h4>v4.7.0 TACTICAL MASTER (29 Dicembre 2025)</h4>
                <ul>
                    <li>✅ 3 Pattern tattici MASTER: Deflection, Interference, Clearance</li>
                    <li>✅ Algoritmi multi-mossa per pattern avanzati</li>
                    <li>✅ Analisi sacrifici e valutazione tattica</li>
                </ul>

                <div class="footer">
                    <p><strong>Chess Pro Ultimate v4.7.1 TACTICAL MASTER+</strong></p>
                    <p>Sviluppato con ❤️ | Data: 30 Dicembre 2025</p>
                    <p>Powered by Stockfish, Chess.js, Chessboard.js, Lichess API</p>
                </div>
            </div>

            <!-- ENGLISH VERSION -->
            <div id="lang-en" class="lang-section">
                <h2>📖 Complete Guide - Chess Pro Ultimate v4.7.1</h2>
                
                <div class="info-box">
                    <strong>Welcome!</strong> This is the complete guide to Chess Pro Ultimate version 4.7.1 TACTICAL MASTER+.
                    This version includes 13 advanced tactical patterns, local/online Stockfish support, Lichess API integration,
                    complete keyboard shortcuts, and optimized touch controls.
                </div>

                <h3>🎮 Controls and Input</h3>

                <h4>⌨️ Keyboard Shortcuts (New in v4.7.1!)</h4>
                <p>Fast and complete keyboard control for PC users:</p>
                
                <table class="shortcut-table">
                    <tr>
                        <th>Key</th>
                        <th>Function</th>
                        <th>Description</th>
                    </tr>
                    <tr>
                        <td><span class="key">Z</span> or <span class="key">Ctrl+Z</span></td>
                        <td>Undo</td>
                        <td>Undo last move (yours + AI)</td>
                    </tr>
                    <tr>
                        <td><span class="key">N</span></td>
                        <td>New Game</td>
                        <td>Start a new game</td>
                    </tr>
                    <tr>
                        <td><span class="key">H</span></td>
                        <td>Hint</td>
                        <td>Show best move suggestion</td>
                    </tr>
                    <tr>
                        <td><span class="key">F</span></td>
                        <td>Flip</td>
                        <td>Flip the board</td>
                    </tr>
                    <tr>
                        <td><span class="key">R</span></td>
                        <td>Resign</td>
                        <td>Resign current game</td>
                    </tr>
                    <tr>
                        <td><span class="key">Space</span></td>
                        <td>Auto Play</td>
                        <td>Toggle automatic play mode</td>
                    </tr>
                    <tr>
                        <td><span class="key">A</span></td>
                        <td>Analyze</td>
                        <td>Analyze complete game</td>
                    </tr>
                    <tr>
                        <td><span class="key">T</span></td>
                        <td>Tactical Analysis</td>
                        <td>Show/hide tactical patterns</td>
                    </tr>
                    <tr>
                        <td><span class="key">S</span></td>
                        <td>Toggle Stockfish</td>
                        <td>Switch between local/online Stockfish</td>
                    </tr>
                    <tr>
                        <td><span class="key">?</span></td>
                        <td>Quick Guide</td>
                        <td>Show shortcuts list</td>
                    </tr>
                </table>

                <div class="tip-box">
                    <strong>💡 Tip:</strong> Use keyboard shortcuts for lightning-fast control! 
                    Each time you use a shortcut, you'll see a green confirmation toast at the bottom.
                </div>

                <h4>📱 Mobile Touch Controls (Optimized v4.7.1!)</h4>
                <div class="feature-grid">
                    <div class="feature-card">
                        <h4>Tap</h4>
                        <p>Select and move pieces</p>
                    </div>
                    <div class="feature-card">
                        <h4>Double Tap</h4>
                        <p>Request quick hint</p>
                    </div>
                    <div class="feature-card">
                        <h4>Swipe Left (Outside board)</h4>
                        <p>Undo last move</p>
                    </div>
                    <div class="feature-card">
                        <h4>Drag & Drop</h4>
                        <p>Drag pieces on the board</p>
                    </div>
                </div>

                <div class="warning-box">
                    <strong>🎯 FIX v4.7.1:</strong> Swipe is now DISABLED on the chessboard! 
                    No more accidental undo when moving pieces. Swipe only works on side panels.
                </div>

                <h3>🧠 AI Engine and Stockfish</h3>

                <h4>Two Stockfish Modes</h4>
                <div class="feature-grid">
                    <div class="feature-card">
                        <h4>🏠 Local Stockfish</h4>
                        <p><strong>Pro:</strong> Works offline, total privacy</p>
                        <p><strong>Con:</strong> Slower on mobile</p>
                    </div>
                    <div class="feature-card">
                        <h4>☁️ Online Stockfish</h4>
                        <p><strong>Pro:</strong> Very fast, cloud computing</p>
                        <p><strong>Con:</strong> Requires internet connection</p>
                    </div>
                </div>

                <p><strong>How to switch:</strong> Click "Stockfish" button in sidebar or press <span class="key">S</span></p>

                <h4>⚙️ AI Difficulty Levels</h4>
                <ul>
                    <li><strong>Easy:</strong> Depth 1, perfect for beginners</li>
                    <li><strong>Medium:</strong> Depth 3, intermediate player</li>
                    <li><strong>Hard:</strong> Depth 5, advanced player</li>
                    <li><strong>Expert:</strong> Depth 7, very strong</li>
                    <li><strong>Master:</strong> Depth 10+, master level</li>
                </ul>

                <h3>🌐 Lichess API Integration</h3>

                <h4>📖 Opening Explorer</h4>
                <p>When the game has ≥20 pieces (opening phase), the system automatically consults Lichess database to show you:</p>
                <ul>
                    <li>Most played moves in this position</li>
                    <li>Win/draw/loss statistics</li>
                    <li>Move frequency</li>
                    <li>Opening theory</li>
                </ul>

                <h4>🎯 Tablebase (Perfect Endgames)</h4>
                <p>When ≤7 pieces remain, the system consults Lichess tablebases for perfect calculations:</p>
                <ul>
                    <li>Guaranteed optimal move</li>
                    <li>Precise evaluation (Win/Draw/Loss)</li>
                    <li>Number of moves to win</li>
                    <li>Perfect endgame play</li>
                </ul>

                <h3>⚡ Tactical Analysis System (13 Patterns!)</h3>

                <p>Activate with "Tactical Analysis" button or press <span class="key">T</span></p>

                <h4>📊 Base Patterns (v4.4.0)</h4>
                <div class="pattern-list">
                    <div class="pattern-item">
                        <strong>🔱 FORK</strong><br>
                        One piece attacks 2+ enemy pieces simultaneously
                    </div>
                    <div class="pattern-item">
                        <strong>📌 PIN</strong><br>
                        Pinned piece cannot move without exposing more valuable piece
                    </div>
                    <div class="pattern-item">
                        <strong>🎯 SKEWER</strong><br>
                        Penetrating attack: piece forced to move, exposing the one behind
                    </div>
                </div>

                <h4>🎪 Fundamental Patterns (v4.5.0)</h4>
                <div class="pattern-list">
                    <div class="pattern-item">
                        <strong>🎪 HANGING</strong><br>
                        Undefended piece, easily capturable
                    </div>
                    <div class="pattern-item">
                        <strong>👑 BACK RANK</strong><br>
                        King trapped on back rank, vulnerable to mate
                    </div>
                    <div class="pattern-item">
                        <strong>🔄 OVERLOADED</strong><br>
                        Piece defending too many things at once
                    </div>
                    <div class="pattern-item">
                        <strong>⚡ DOUBLE CHECK</strong><br>
                        Check from two pieces simultaneously (devastating!)
                    </div>
                </div>

                <h4>🔥 Advanced Patterns (v4.6.0)</h4>
                <div class="pattern-list">
                    <div class="pattern-item advanced">
                        <strong>💥 DISCOVERED</strong><br>
                        Piece moves discovering attack from piece behind
                    </div>
                    <div class="pattern-item advanced">
                        <strong>🚫 TRAPPED</strong><br>
                        Piece trapped with no safe escape routes
                    </div>
                    <div class="pattern-item advanced">
                        <strong>🔍 X-RAY</strong><br>
                        Attack through a piece to the target behind
                    </div>
                </div>

                <h4>🎖️ MASTER Patterns (v4.7.0 - New!)</h4>
                <div class="pattern-list">
                    <div class="pattern-item master">
                        <strong>🎣 DEFLECTION</strong><br>
                        Force defender to leave critical position with sacrifice
                    </div>
                    <div class="pattern-item master">
                        <strong>🚧 INTERFERENCE</strong><br>
                        Block enemy defensive line by placing a piece
                    </div>
                    <div class="pattern-item master">
                        <strong>🔓 CLEARANCE</strong><br>
                        Clear a line to enable devastating attack
                    </div>
                </div>

                <div class="info-box">
                    <strong>ℹ️ How it works:</strong> Tactical patterns are highlighted on the board with animated emojis.
                    Each pattern shows severity (Critical/High/Medium) and threatened material.
                </div>

                <h3>📊 Game Analysis System</h3>

                <h4>Available Metrics</h4>
                <ul>
                    <li><strong>Accuracy:</strong> % of good/excellent moves</li>
                    <li><strong>Move classification:</strong> Excellent, Good, Inaccurate, Mistakes, Blunders</li>
                    <li><strong>Phase statistics:</strong> Opening, Middlegame, Endgame</li>
                    <li><strong>Position evaluation:</strong> Centipawns for each move</li>
                    <li><strong>Win probability:</strong> Real-time graph</li>
                    <li><strong>Time spent:</strong> For each move</li>
                </ul>

                <h4>Available Exports</h4>
                <ul>
                    <li><strong>PGN:</strong> Standard chess notation</li>
                    <li><strong>Annotated PGN:</strong> With comments and evaluations</li>
                    <li><strong>JSON:</strong> Complete analysis data</li>
                    <li><strong>HTML Report:</strong> Complete viewable report</li>
                </ul>

                <h3>🎯 Tips for Best Play</h3>

                <div class="tip-box">
                    <strong>💡 For Beginners:</strong>
                    <ul>
                        <li>Use Easy or Medium difficulty</li>
                        <li>Enable Tactical Analysis to learn patterns</li>
                        <li>Use Hint (<span class="key">H</span>) when stuck</li>
                        <li>Study Opening Explorer suggestions</li>
                    </ul>
                </div>

                <div class="tip-box">
                    <strong>💡 For Intermediate Players:</strong>
                    <ul>
                        <li>Play Hard or Expert</li>
                        <li>Analyze games to understand mistakes</li>
                        <li>Try to find tactical patterns before activating them</li>
                        <li>Use Online Stockfish for fast analysis</li>
                    </ul>
                </div>

                <div class="tip-box">
                    <strong>💡 For Experts:</strong>
                    <ul>
                        <li>Master level with Online Stockfish</li>
                        <li>Experiment with MASTER patterns (Deflection, Interference, Clearance)</li>
                        <li>Analyze Multi-PV depth for alternative variations</li>
                        <li>Use keyboard shortcuts for maximum speed</li>
                    </ul>
                </div>

                <h3>❓ FAQ - Frequently Asked Questions</h3>

                <h4>Q: How to avoid accidental undo on mobile?</h4>
                <p><strong>A:</strong> With v4.7.1 the problem is solved! Swipe is disabled on the chessboard. 
                You can move pieces without worry. Swipe only works on side panels.</p>

                <h4>Q: Which Stockfish to use?</h4>
                <p><strong>A:</strong> On PC use whichever you prefer. On mobile, Online Stockfish is much faster.</p>

                <h4>Q: Can I play offline?</h4>
                <p><strong>A:</strong> Yes! Use Local Stockfish. Lichess APIs (Opening Explorer and Tablebase) require connection.</p>

                <h4>Q: How to improve quickly?</h4>
                <p><strong>A:</strong> Always enable Tactical Analysis, study patterns after each game, and analyze mistakes.</p>

                <h4>Q: Do tactical patterns slow down the game?</h4>
                <p><strong>A:</strong> Tactical analysis is lightweight and doesn't affect performance. Updates every 2 seconds.</p>

                <h3>🔧 Troubleshooting</h3>

                <h4>Chessboard doesn't appear</h4>
                <ul>
                    <li>Reload the page (F5)</li>
                    <li>Check browser console for errors</li>
                    <li>Verify JavaScript is enabled</li>
                </ul>

                <h4>Stockfish is slow</h4>
                <ul>
                    <li>Switch to Online Stockfish (button or <span class="key">S</span>)</li>
                    <li>Reduce AI difficulty</li>
                    <li>Close other browser tabs</li>
                </ul>

                <h4>Lichess API not working</h4>
                <ul>
                    <li>Check internet connection</li>
                    <li>Verify lichess.org is reachable</li>
                    <li>Sometimes APIs have rate limits, try again after a minute</li>
                </ul>

                <h3>📝 Version Notes</h3>

                <h4>v4.7.1 TACTICAL MASTER+ (December 30, 2025)</h4>
                <ul>
                    <li>✅ <strong>FIX:</strong> Swipe disabled on chessboard (no more accidental undo)</li>
                    <li>✅ <strong>NEW:</strong> Complete keyboard shortcuts system (10 shortcuts)</li>
                    <li>✅ <strong>NEW:</strong> Visual toast feedback for shortcuts</li>
                    <li>✅ Improved touch events handling</li>
                    <li>✅ Added bilingual help guide (IT/EN)</li>
                </ul>

                <h4>v4.7.0 TACTICAL MASTER (December 29, 2025)</h4>
                <ul>
                    <li>✅ 3 MASTER tactical patterns: Deflection, Interference, Clearance</li>
                    <li>✅ Multi-move algorithms for advanced patterns</li>
                    <li>✅ Sacrifice analysis and tactical evaluation</li>
                </ul>

                <div class="footer">
                    <p><strong>Chess Pro Ultimate v4.7.1 TACTICAL MASTER+</strong></p>
                    <p>Developed with ❤️ | Date: December 30, 2025</p>
                    <p>Powered by Stockfish, Chess.js, Chessboard.js, Lichess API</p>
                </div>
            </div>
        </div>
    </div>

    <script>
        function switchLang(lang) {
            // Hide all sections
            document.querySelectorAll('.lang-section').forEach(section => {
                section.classList.remove('active');
            });
            
            // Show selected section
            document.getElementById('lang-' + lang).classList.add('active');
            
            // Update buttons
            document.querySelectorAll('.lang-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            event.target.classList.add('active');
        }
    </script>
</body>
</html>
