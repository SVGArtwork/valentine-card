# Architettura del progetto

Questa applicazione è una **Progressive Web App** basata su SVG inline e JavaScript.  

## Componenti principali

1. **SVG interattivo**
   - Contiene tutti gli elementi grafici: tappo, lampadine, bollicine, mani, smile, occhi del gatto, ecc.
   - Gli elementi hanno ID specifici per permettere l’interazione e l’animazione via JS.

2. **Gestione pannello info**
   - Associato agli elementi SVG tramite `svgInfoMap`.
   - Mostra un pannello con titolo e testo quando un elemento è cliccato.

3. **Zoom e Panning**
   - Implementato con la libreria `svgPanZoom`.
   - Permette zoom in/out, pan e ridimensionamento responsivo.
   - Include slider e pulsanti di controllo opzionali.

4. **Animazioni lampadine**
   - Tre modalità: random, lampadine pari, lampadine dispari.
   - Ciclo automatico con intervalli definiti.
   - Funzioni principali:
     - `setLampState()` – accende/spegne singole lampadine
     - `turnOffAllLamps()` – spegne tutte le lampadine
     - `randomLamps()` e `fastAlternateLamps()` – gestione animazioni

5. **Animazione tappo e bollicine**
   - Movimento lungo la traiettoria definita da SVG.
   - Bollicine animate in modo sicuro per evitare memory leak.
   - Funzioni principali:
     - `anima()` – animazione tappo
     - `zampillio()` – sequenza bollicine e schiuma
     - `avviaBollicine()` – gestione ricorsiva delle bollicine
   - Include easing e rotazione casuale per un effetto realistico.

6. **State Machine**
   - Stati: `LOADING`, `INTRO`, `ANIMATION`, `IDLE`.
   - Transizioni controllate tramite `setState()`.
   - Garantisce ordine e sincronizzazione di animazioni e interazioni.

---

### Navigazione
- [Torna all’indice](00_index.md)
- [Sezione Animazioni](animation.md)
