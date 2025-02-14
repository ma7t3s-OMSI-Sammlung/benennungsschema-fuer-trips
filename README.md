# **🚏 OMSI 2 Benennungsschema für Trips**  

## **🔹 Allgemeine Struktur:**  
`[Liniennummer]_[Start][Steig]-[Ziel][Steig][_vZwischenhalt][_SM/SN]`  

- **Liniennummer** → Immer **drei Ziffern** (z. B. `270`)  
- **Betriebsfahrten** (Leerfahrten ohne Fahrgäste) → Statt einer Liniennummer wird **"X"** verwendet (`X_SEB-SWB`)  
- **Start/Ziel** → **Dreistellige Haltestellenkürzel**  
- **Steigbezeichnung** → Falls nötig, direkt an das Kürzel anhängen (`SEW1`, `RFM2`)  
- **via-Zwischenhalt** → Falls alternative Routen existieren, mit `_vXXX` angeben (z. B. `_vSWB`)  
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
| Seestedt, Weiher | `SEW` |
| Seestedt, Markt | `SEM` |
| Rosenfeld, Markt | `RFM` |
| Schönwalde, Bahnhof/ZOB | `SWB` |

Falls eine Haltestelle mehrere Bussteige hat, wird die **Steigbezeichnung direkt angehängt**:  
- **Seestedt, Weiher, Steig 1** → `SEW1`  
- **Rosenfeld, Markt, Steig 2** → `RFM2`  
- **Schönwalde, Bahnhof, Steig 3** → `SWB3`  

---

## **🔹 Beispiele für Trip-Namen:**  

### **🚍 Normale Fahrten (ohne Steigangabe, ohne via, ohne Schulbezug)**  
| Linienweg  | Trip-Name  |
|------------|-----------|
| **279** von *Seestedt, Weiher* nach *Rosenfeld, Markt*  | `279_SEW-RFM`  |
| **271** von *Seestedt, Markt* nach *Schönwalde, Bahnhof/ZOB*  | `271_SEM-SWB`  |

---

### **🚏 Fahrten mit Steigangabe**  
| Linienweg  | Trip-Name  |
|------------|-----------|
| **270** von *Stein, Bahnhof, Steig 6* nach *Rosenfeld, Markt, Steig 2*  | `270_STB1-RFM2`  |
| **271** von *Seestedt, Markt, Steig A* nach *Schönwalde, Bahnhof/ZOB, Steig 3*  | `271_SEMA-SWB3`  |

---

### **🛤 Fahrten mit via-Angabe (alternative Streckenführungen)**  
| Linienweg  | Trip-Name  |
|------------|-----------|
| **279** von *Seestedt, Weiher* nach *Rosenfeld, Markt* via *Strackdorf, Ort*  | `279_SEW-RFM_vSTO`  |
| **271** von *Seestedt, Markt* nach *Schönwalde, Bahnhof/ZOB* via *Rosenfeld, Markt*  | `271_SEM-SWB_vRFM`  |

---

### **🏫 Schulfahrten (SM = morgens zur Schule, SN = nachmittags zurück)**  
| Linienweg  | Trip-Name  |
|------------|-----------|
| **279** von *Seestedt, Weiher* nach *Rosenfeld, Markt* (Schulfahrt morgens)  | `279_SEW-RFM_SM`  |
| **271** von *Seestedt, Markt* nach *Schönwalde, Bahnhof/ZOB* (Schulfahrt nachmittags)  | `271_SEM-SWB_SN`  |

---

### **🔀 Kombinierte Fahrten (via, Steig & Schulfahrten gleichzeitig)**  
| Linienweg  | Trip-Name  |
|------------|-----------|
| **279** von *Seestedt, Weiher, Steig 1* nach *Rosenfeld, Markt, Steig 2*, via *Seestedt, Schule* (Schulfahrt morgens)  | `279_SEW1-RFM2_vSES_SM`  |
| **271** von *Seestedt, Markt, Steig A* nach *Schönwalde, Bahnhof/ZOB, Steig 3*, via *Rosenfeld, Markt* (Schulfahrt nachmittags)  | `271_SEMA-SWB3_vRFM_SN`  |

---

### **⚙ Betriebsfahrten (Leerfahrten ohne Fahrgäste)**  
| Linienweg  | Trip-Name  |
|------------|-----------|
| **Betriebsfahrt** von *Seestedt Betriebshof* nach *Schönwalde, Bahnhof/ZOB*  | `X_SEB-SWB`  |
| **Betriebsfahrt** von *Rosenfeld, Markt, Steig 3* nach *Seestedt, Betriebshof*  | `X_RFM3-SEB`  |

---

## **📌 Zusätzliche Regeln zur Einheitlichkeit:**  
✔ **Alles in Großbuchstaben** → Einheitlich und gut lesbar  
✔ **Keine Leerzeichen oder Sonderzeichen** → Kompatibilität mit allen Dateisystemen  
✔ **Unterstriche `_` zur Trennung von Modifikationen**  
✔ **Steigbezeichnungen direkt am Haltestellenkürzel**  
✔ **Betriebsfahrten immer mit "X" als Liniennummer**  
