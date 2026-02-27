# 📌 Versionshantering med Git  
En introduktion till hur Git används för att spara, följa och organisera förändringar i kod och filer.

---

## 🧩 Vad är Git?  
Git är ett distribuerat versionshanteringssystem som hjälper dig att:

- gå tillbaka till tidigare versioner av ett projekt  
- spara tydliga “ögonblicksbilder” av filers tillstånd  
- samarbeta med andra utan att skriva över varandras arbete  
- få en historik över hur projektet utvecklats över tid  

Git används i allt från små skolprojekt till stora professionella kodbaser.

---

## 🗂️ Stage – att förbereda ändringar  
När du har skapat en fil, exempelvis `index.html`, behöver du lägga till den i Git:s “staging area” innan du kan spara den som en version.

```bash
git add index.html
```

Du kan kontrollera vilka filer som ändrats med:

```bash
git status
```

---

## 💾 Commit – att spara en version  
En commit är en sparad version av projektet. Varje commit bör ha ett tydligt meddelande som beskriver vad som ändrats.

Skapa din första commit:

```bash
git commit --message "Skapat index.html"
```

Gör sedan en ändring i filen (t.ex. lägg till eller ta bort text) och spara den nya versionen:

```bash
git add index.html
git commit --message "Lagt till innehåll i HEAD"
```

---

## 📜 Git log – se historiken  
`git log` visar alla commits som gjorts i projektet. Här kan du se:

- vem som gjort commit  
- datum  
- commit‑meddelande  
- commit‑hash (unik identifierare)

```bash
git log
```

För en mer kompakt vy:

```bash
git log --pretty=oneline
```

---

## 🔍 Visa ändringar mellan versioner  
Vill du se exakt vad som ändrats i filerna kan du använda:

```bash
git log --patch -2
```

Det visar skillnaderna i de två senaste commitsen. Navigera med piltangenterna och avsluta med `q`.

---

## ⏪ Återgå till en tidigare version  
Varje commit har en unik hash. Du kan använda hela hashen eller de första fem tecknen för att gå tillbaka till en tidigare version av en specifik fil:

```bash
git checkout <hash> index.html
```

Filen öppnas då i det skick den hade vid den commit du valt.

---

## 🔄 Återställ senaste versionen  
Om du vill gå tillbaka till den senaste versionen igen:

1. Kör `git log` och kopiera hash för den senaste committen.  
2. Kör:

```bash
git checkout <senaste-hash> index.html
```
---
