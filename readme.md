# 🚛 FL-FPersV-EG-VO

Lenk- und Ruhezeiten Datenbank für die FL-Mastery-App

## Gesetze

- **FPersV** (Fahrpersonalverordnung)
  - Quelle: https://www.gesetze-im-internet.de/fpersv/
  - Nationale Regelungen
  
- **VO (EG) 561/2006** (EU-Sozialvorschriften)
  - Quelle: https://eur-lex.europa.eu/eli/reg/2006/561/oj/deu
  - EU-weite Grundlage

## Wichtig für Fahrlehrer

⚠️ **Auch Klasse B kann Kontrollgerätpflicht haben!**

Beispiele:
- 🏆 Fußballturnier mit Sachpreis = entgeltlich
- 🐴 Pferdetransport mit Aufwandsentschädigung = entgeltlich
- 🥨 Brötchen holen gegen Spritgeld = entgeltlich
- 📅 56-Tage-Nachweispflicht beachten!

## Struktur
```json
{
  "paragraphen": [
    {
      "nummer": "§ 1 FPersV",
      "titel": "Geltungsbereich",
      "gesetzestext": "...",
      "quelle": "https://...",
      "praxisbeispiele": [
        {
          "titel": "...",
          "klasse": "B/BE/C/etc.",
          "beschreibung": "...",
          "wichtigkeit": "CRITICAL/HIGH/BANAL"
        }
      ]
    }
  ],
  "metadata": {
    "lastUpdated": "...",
    "totalParagraphen": 0
  }
}
```

## Verwendung

Diese Datenbank wird über die **fpersv-eg-master.html** Editor-Datei bearbeitet und automatisch mit GitHub synchronisiert.

Die **FL-Mastery-App** (https://fl-mastery-app.vercel.app) lädt die Daten direkt von diesem Repository.

## Updates

- 27.12.2025: Initiale Struktur erstellt
- Geplant 2026: Anpassung an neue EU-Verordnung

## Lizenz

Für Fahrlehrer-Ausbildung nach FahrlG
```

---

## 🚀 **TEIL 3: Schritt-für-Schritt Anleitung**

### **SCHRITT 1: GitHub Repository erstellen**

1. **Gehe zu:** https://github.com/new
2. **Repository name:** `FL-FPersV-EG-VO`
3. **Description:** "Lenk- und Ruhezeiten Datenbank für FL-Mastery-App"
4. **Public** ✅ (wichtig für App-Zugriff!)
5. **Initialize with README:** ❌ NEIN (machen wir selbst)
6. **Create repository**

### **SCHRITT 2: Dateien auf PC vorbereiten**

Erstelle auf deinem PC einen Ordner:
```
C:\Users\[DeinName]\FL-FPersV-EG-VO\
```

Lege dort diese Dateien rein:

**A) data.json** (kopiere den JSON-Code von oben)
**B) README.md** (kopiere den Markdown-Code von oben)

### **SCHRITT 3: GitHub Desktop nutzen**

1. **Öffne GitHub Desktop**
2. **File → Add Local Repository**
3. **Wähle den Ordner:** `C:\Users\[DeinName]\FL-FPersV-EG-VO\`
4. **"Create Repository"** klicken
5. **Publish Repository** klicken
   - ✅ Name: `FL-FPersV-EG-VO`
   - ✅ Keep this code **public**
   - Publish!

### **SCHRITT 4: GitHub Token erstellen**

1. **Gehe zu:** https://github.com/settings/tokens/new
2. **Note:** "FPersV EG-VO Master Editor"
3. **Expiration:** 90 days (oder länger)
4. **Permissions:**
   - ✅ **repo** (alle Sub-Checkboxen werden automatisch ausgewählt)
5. **Generate token**
6. **Token KOPIEREN** (sieht aus wie: `ghp_xxxxxxxxxxxxx`)
7. **WICHTIG:** Token irgendwo sicher speichern (Passwort-Manager!)

### **SCHRITT 5: HTML-Editor testen**

1. **Öffne:** `fpersv-eg-master.html` im Browser (z.B. Chrome)
2. **GitHub Token eingeben** (den Token von Schritt 4)
3. **"Mit GitHub verbinden"** klicken
4. ✅ **Sollte zeigen:** "Mit GitHub verbunden! Repository geladen."

### **SCHRITT 6: Ersten Paragraph erstellen (Test)**

1. **Klicke:** "➕ Neuer Paragraph"
2. **Trage ein:**
   - Nummer: `§ 1 FPersV`
   - Titel: `Geltungsbereich`
   - Gesetzestext: `(TEST) Diese Verordnung gilt für...`
   - Quelle: `https://www.gesetze-im-internet.de/fpersv/__1.html`
3. **Klicke:** "§ 1 FPersV - Typische Fälle" (Vorlage lädt Beispiele)
4. **Klicke:** "💾 Speichern"
5. ✅ **Sollte zeigen:** "GitHub Sync erfolgreich!"

### **SCHRITT 7: In GitHub prüfen**

1. **Gehe zu:** https://github.com/710Deckel/FL-FPersV-EG-VO
2. **Öffne:** `data.json`
3. ✅ **Sollte jetzt deinen Test-Paragraph enthalten!**

---

## 📋 **TEIL 4: Die wichtigsten Gesetze eintragen**

Jetzt kannst du die Gesetze eintragen:

### **FPersV von:** https://www.gesetze-im-internet.de/fpersv/

**Wichtigste Paragraphen:**
- § 1 - Geltungsbereich (CRITICAL!)
- § 2 - Kontrollgerät
- § 3 - Mitführungspflichten

### **VO (EG) 561/2006 von:** https://eur-lex.europa.eu/eli/reg/2006/561/oj/deu

**Wichtigste Artikel:**
- Art. 3 - Anwendungsbereich
- Art. 6 - Lenkzeiten (CRITICAL!)
- Art. 7 - Pausen (CRITICAL!)
- Art. 8 - Ruhezeiten (CRITICAL!)
- Art. 9 - Ausnahmen

**Workflow:**
1. Gehe zur Gesetzesseite
2. Kopiere den Paragraphen/Artikel-Text
3. Füge in HTML-Editor ein
4. Lade passende Praxisbeispiele (Vorlagen-Buttons!)
5. Speichern → Auto-Sync!

---

## 🎯 **TEIL 5: Integration in FL-Mastery-App**

Sobald du einige Paragraphen eingetragen hast, kann Google AI die Integration in deine FL-Mastery-App machen.

**Die App wird dann:**
1. Daten von GitHub laden: `https://raw.githubusercontent.com/710Deckel/FL-FPersV-EG-VO/main/data.json`
2. FPersV/EG-VO Modul anzeigen
3. Praxisbeispiele prominent zeigen
4. Suchfunktion bereitstellen
5. Filter nach Klassen (B, BE, C, etc.)

---

## ✅ **CHECKLISTE - Hast du alles?**
```
□ GitHub Repository erstellt: FL-FPersV-EG-VO
□ data.json hochgeladen
□ README.md hochgeladen
□ GitHub Token erstellt & gespeichert
□ fpersv-eg-master.html funktioniert
□ Test-Paragraph erfolgreich gespeichert
□ In GitHub sichtbar
