# **🚏 OMSI 2 Benennungsschema für Trips**  

## **🔹 Allgemeine Struktur:**  
`[Liniennummer]_[Start][Steig]-[Ziel][Steig][_vZwischenhalt][_SM/SN]`  

- **Liniennummer** → Immer **drei Ziffern** (z. B. `270`)  
- **Betriebsfahrten** (Leerfahrten ohne Fahrgäste) → Statt einer Liniennummer wird **"X"** verwendet (`X_STB-BSH`)  
- **Start/Ziel** → **Dreistellige Haltestellenkürzel**  
- **Steigbezeichnung** → Falls nötig, direkt an das Kürzel anhängen (`STB1`, `RFM2`)  
- **via-Zwischenhalt** → Falls alternative Routen existieren, mit `_vXXX` angeben (z. B. `_vHBF`)  
- **Schulfahrten**:  
  - `_SM` → Schülerfahrt **morgens zur Schule**  
  - `_SN` → Schülerfahrt **nachmittags von der Schule**  

---

## **🔹 Aufbau der Haltestellenkürzel**  
Jede Haltestelle hat ein **dreistelliges Kürzel**, das nach folgendem Schema aufgebaut ist:  

🔹 **Die ersten zwei Zeichen** stehen für die **Ortschaft oder den Stadtteil**  
🔹 **Das dritte Zeichen** steht für die **Haltestelle innerhalb der Ortschaft**  

### **🛑 Beispiele für Haltestellenkürzel**  
| Haltestelle  | Kürzel  |
|--------------|---------|
| Seestedt, Schule | `SES` |
| Rosenfeld, Markt | `RFM` |
| Stein, Bahnhof | `STB` |
| Neumarkt, Theater | `NMT` |

Falls eine Haltestelle mehrere Bussteige hat, wird die **Steigbezeichnung direkt angehängt**:  
- **Stein, Bahnhof, Steig 1** → `STB1`  
- **Rosenfeld, Markt, Steig 2** → `RFM2`  

---

## **🔹 Beispiele für Trip-Namen:**  

### **🚍 Normale Fahrten (ohne Steigangabe, ohne via, ohne Schulbezug)**  
| Linienweg  | Trip-Name  |
|------------|-----------|
| **270** von *Stein Bahnhof* nach *Rosenfeld Markt*  | `270_STB-RFM`  |
| **015** von *Altstadt* nach *Neumarkt*  | `015_ALT-NMT`  |

---

### **🚏 Fahrten mit Steigangabe**  
| Linienweg  | Trip-Name  |
|------------|-----------|
| **270** von *Stein Bahnhof, Steig 1* nach *Rosenfeld Markt, Steig 2*  | `270_STB1-RFM2`  |
| **015** von *Altstadt, Steig A* nach *Neumarkt, Steig B*  | `015_ALTA-NMTB`  |

---

### **🛤 Fahrten mit via-Angabe (alternative Streckenführungen)**  
| Linienweg  | Trip-Name  |
|------------|-----------|
| **270** von *Stein Bahnhof* nach *Rosenfeld Markt* via *Hauptbahnhof*  | `270_STB-RFM_vHBF`  |
| **015** von *Altstadt* nach *Neumarkt* via *Schulzentrum*  | `015_ALT-NMT_vSCH`  |

---

### **🏫 Schulfahrten (SM = morgens zur Schule, SN = nachmittags zurück)**  
| Linienweg  | Trip-Name  |
|------------|-----------|
| **270** von *Stein Bahnhof* nach *Rosenfeld Markt* (Schulfahrt morgens)  | `270_STB-RFM_SM`  |
| **015** von *Altstadt* nach *Neumarkt* (Schulfahrt nachmittags)  | `015_ALT-NMT_SN`  |

---

### **🔀 Kombinierte Fahrten (via, Steig & Schulfahrten gleichzeitig)**  
| Linienweg  | Trip-Name  |
|------------|-----------|
| **270** von *Stein Bahnhof, Steig 1* nach *Rosenfeld Markt, Steig 2*, via *Hauptbahnhof* (Schulfahrt morgens)  | `270_STB1-RFM2_vHBF_SM`  |
| **015** von *Altstadt, Steig A* nach *Neumarkt, Steig B*, via *Schulzentrum* (Schulfahrt nachmittags)  | `015_ALTA-NMTB_vSCH_SN`  |

---

### **⚙ Betriebsfahrten (Leerfahrten ohne Fahrgäste)**  
| Linienweg  | Trip-Name  |
|------------|-----------|
| **Betriebsfahrt** von *Stein Betriebshof* nach *Hauptbahnhof*  | `X_BSH-HBF`  |
| **Betriebsfahrt** von *Neumarkt Steig 3* nach *Stein, Betriebshof*  | `X_NMT3-STB`  |
| **Betriebsfahrt mit via-Angabe** (*über Rosenfeld Markt*)  | `X_BSH-HBF_vRFM`  |

---

## **📌 Zusätzliche Regeln zur Einheitlichkeit:**  
✔ **Alles in Großbuchstaben** → Einheitlich und gut lesbar  
✔ **Keine Leerzeichen oder Sonderzeichen** → Kompatibilität mit allen Dateisystemen  
✔ **Unterstriche `_` zur Trennung von Modifikationen**  
✔ **Steigbezeichnungen direkt am Haltestellenkürzel**  
✔ **Betriebsfahrten immer mit "X" als Liniennummer**  
