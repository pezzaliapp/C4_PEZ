
# 🕹️ C64_PEZ – Retro Price Calculator

> Una rielaborazione in chiave moderna della **mia prima app scritta in BASIC nel settembre 1983**, oggi trasformata in una Progressive Web App minimale, in puro stile Commodore 64.

---

## 📜 Descrizione

**C64_PEZ** è una web app retro-futurista che calcola:

- ✅ Il prezzo netto dopo due sconti percentuali sequenziali
- ✅ Il prezzo di vendita con applicazione di un margine percentuale
- ✅ Il tutto su un'interfaccia ispirata ai colori, ai font e all’estetica del **Commodore 64**

L’obiettivo? Unire la logica funzionale dei primi anni ’80 con l’accessibilità moderna dei browser e degli smartphone.

---

## ⚙️ Funzionalità

- Inserisci il **prezzo lordo**
- Applica **Sconto 1 (%)** e **Sconto 2 (%)**
- Aggiungi un **Margine di Vendita (%)**
- Visualizza:
  - 💰 Prezzo Netto
  - 📈 Prezzo di Vendita

---

## 📲 Compatibilità

- ✅ iPhone (consigliato SE in verticale)
- ✅ Android
- ✅ Browser desktop (Chrome, Safari, Firefox, Edge)

Può essere **installata come PWA** per funzionare offline, a tutto schermo.

---

## 🖼️ Design

- 🎨 Colori: **#0400A0** (sfondo blu), **#80FF80** (testo verde)
- 🖼️ Immagine finale in bianco e nero **in stile Commodore 64**
- ✍️ Frase commemorativa:  
  > *A rielaborazione della mia prima app scritta in BASIC – Settembre 1983*

---

## 💾 Come usarla su iPhone o Android

1. Apri `https://tuonomeutente.github.io/C64_PEZ/` in Safari o Chrome
2. Tocca **"Condividi" → "Aggiungi a schermata Home"**
3. Lancia l'app come se fosse nativa

---

## 📁 Contenuto della repo

- `index.html` – Codice dell'app in HTML + JS + stile C64
- `portrait_c64.png` – Immagine finale retro stile Commodore
- `manifest.json` – File PWA per installazione su smartphone
- `README.md` – Questo documento
- *(opzionale)* `service-worker.js` – Per abilitare la modalità offline

---

## 📟 Versione originale (BASIC – Commodore 64, Settembre 1983)

```basic
10 PRINT "CALCOLATRICE PREZZO NETTO+MARGINE"
20 INPUT "PREZZO LORDO";P
30 INPUT "SCONTO 1 (%)";S1
40 INPUT "SCONTO 2 (%)";S2
50 INPUT "MARGINE VENDITA (%)";M
60 N1 = P * (1 - S1 / 100)
70 N2 = N1 * (1 - S2 / 100)
80 VENDITA = N2 / (1 - M / 100)
90 PRINT "NETTO = ";N2;" EURO"
100 PRINT "VENDITA = ";VENDITA;" EURO"
110 END

🧠 Tutto gestito da tastiera. Solo logica e numeri. Niente grafica, solo funzionalità.

⸻

🧾 Seconda elaborazione per C65 (cross-compiler cc65)

#include <stdio.h>

void main() {
    float prezzo, s1, s2, margine, netto1, netto2, vendita;

    printf("CALCOLATRICE NETTO + MARGINE\n");
    printf("PREZZO LORDO: "); scanf("%f", &prezzo);
    printf("SCONTO 1 (%%): "); scanf("%f", &s1);
    printf("SCONTO 2 (%%): "); scanf("%f", &s2);
    printf("MARGINE (%%): "); scanf("%f", &margine);

    netto1 = prezzo * (1 - s1 / 100);
    netto2 = netto1 * (1 - s2 / 100);
    vendita = netto2 / (1 - margine / 100);

    printf(">>> NETTO: %.2f EURO\n", netto2);
    printf(">>> VENDITA: %.2f EURO\n", vendita);
}

🛠️ Compilabile con cc65 per Commodore 64
📺 Output su terminale identico alla versione BASIC

⸻

✍️ Autore

Alessandro Pezzali
🧠 pezzaliAPP.com | 🔧 pezzalistack | ☕ patreon.com/pezzaliAPP

⸻

📘 Licenza

Open source – per uso personale, didattico o nostalgico.
Nessun utilizzo commerciale senza autorizzazione scritta.

---
