# Animazioni principali

Il progetto gestisce diverse animazioni:

## 1. Lampadine
- Tre modalità:
  - **Random**: accende da 3 a 10 lampadine casuali.
  - **Even**: lampeggiano solo lampadine pari.
  - **Odd**: lampeggiano solo lampadine dispari.
- Ciclo continuo, transizione automatica tra le modalità.
- Controllo stato con `alternateState` per alternare lampeggio.

## 2. Tappo
- Movimento lungo una traiettoria SVG.
- Rotazione con easing e rumore casuale.
- Al termine parte la sequenza dello **zampillio**.

## 3. Zampillio e schiuma
- Sequenza a 5 step per mostrare skizzo e schiuma.
- Gestito da `zampillio(cicli, intervallo)`.
- Alla fine: mano e smile visibili, occhi del gatto chiusi.

## 4. Bollicine
- Funzione `avviaBollicine(prefixId, numero)`:
  - Evita accumulo di timer.
  - Ciclo ricorsivo controllato da `animazioneInCorso`.
  - Sicuro contro memory leak.

## 5. Testo
- Funzione `mostraTesto()`.
- Appare in fade-in al termine della sequenza.

---

### Navigazione
- [Torna all’indice](00_index.md)
- [Architettura](architecture.md)
- [Guida all’uso](usage.md)
