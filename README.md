# ABO výpis → HTML / PDF konvertor

Tento projekt umožňuje **načíst a zobrazit bankovní výpis ve formátu ABO (GPC 074/075/078/079)** přímo v prohlížeči – bez nutnosti instalace.  
Soubor `.abo` nebo `.gpc` stačí přetáhnout do stránky a zobrazí se přehledná tabulka s transakcemi.  
Výsledek lze poté **uložit jako PDF** pomocí běžné funkce tisku v prohlížeči.

---

## 🧩 Funkce

- ✅ Načtení výpisu ve formátu **ABO / GPC** (typické exporty z českých a slovenských bank)  
- ✅ Podpora záznamů **074** (hlavička), **075** (položka), **078/079** (AV texty)  
- ✅ Automatická detekce kódování (`cp1250`, `ISO-8859-2`, `UTF-8`)  
- ✅ Přehledná tabulka s částkami, VS/KS/SS, názvy protistran a daty  
- ✅ Spočítané obraty a kontrola zůstatku  
- ✅ Uložení jako **PDF** nebo export zpracované stránky jako **HTML**  
- ✅ Funguje **offline** – vše běží přímo v prohlížeči, bez serveru

---

## 📦 Jak použít

1. Stáhni nebo zkopíruj soubor [`abo-vypis.html`](./abo-vypis.html) a nebo využij GitHub pages https://doctor-bohlav.github.io/abo-statement-preview/abo-vypis.html
2. Otevři ho v prohlížeči (Chrome, Edge, Firefox…)  
3. Přetáhni nebo vyber svůj soubor s výpisem (`.abo`, `.gpc`, `.txt`)  
4. Zobrazí se přehled výpisu s položkami  
5. Pomocí **Tisk → Uložit jako PDF** vytvoř přehledný soubor s výpisem

---

## 🧠 Jak to funguje

Parser je napsán v čistém JavaScriptu podle veřejné **specifikace ABO/GPC formátu**:  
- Záznamy `074` (hlavička výpisu)  
- Záznamy `075` (obratová položka)  
- Záznamy `078` / `079` (AV texty k položkám)

Podporovány jsou základní pole:
- číslo účtu a název majitele  
- protiúčet, VS, KS, SS  
- částka a směr pohybu (debet/kredit)  
- data a volné texty  
- výpočet obratů a kontrola zůstatku

---

## 🖨 Export do PDF

PDF vytvoříš jednoduše pomocí:
Soubor → Tisk → Uložit jako PDF

Vše je naformátováno pro tisk na šířku A4 s přehlednými tabulkami.

---

## 💡 Tipy

- Projekt funguje plně **offline** – můžeš ho použít i na interních datech.  
- Pokud narazíš na formát z jiné banky (s mírně jinými poli), otevři issue nebo pošli ukázkový řádek.  
- V HTML kódu je i **„demo“ tlačítko**, které zobrazí syntetický výpis pro testování.

---

## 🪪 Licence

MIT License © 2025

---

# English version 🇬🇧

## ABO Statement → HTML / PDF Converter

This project lets you **load and visualize Czech/Slovak ABO (GPC) bank statements** directly in your browser — no installation or server required.  
Simply drag and drop your `.abo` or `.gpc` file, and it will render a clean table of transactions.  
You can then **save the result as a PDF** via your browser’s print dialog.

---

## 🧩 Features

- ✅ Reads **ABO / GPC** statements (formats 074/075/078/079)  
- ✅ Automatic character set detection (`cp1250`, `ISO-8859-2`, `UTF-8`)  
- ✅ Clear transaction table with amounts, account numbers, VS/KS/SS codes, and dates  
- ✅ Calculates totals and checks balances  
- ✅ Export as **PDF** or **self-contained HTML**  
- ✅ Works **fully offline** — no backend or data upload

---

## 📦 How to Use

1. Download or copy the file [`abo-vypis.html`](./abo-vypis.html)  or use GitHub pages https://doctor-bohlav.github.io/abo-statement-preview/abo-vypis.html
2. Open it in your browser (Chrome, Edge, Firefox, etc.)  
3. Drag & drop your `.abo` or `.gpc` file into the page  
4. View the formatted statement  
5. Use **Print → Save as PDF** to export it

---

## 🧠 How It Works

The parser is implemented in plain JavaScript and follows the official **ABO/GPC record specification**:
- `074` – Statement header  
- `075` – Transaction record  
- `078` / `079` – Additional information (AV text)

Extracted fields include:
- account number, owner name  
- counter-account, VS, KS, SS  
- amount, direction (debit/credit)  
- dates and free text notes  
- turnover totals and balance validation

---

## 🖨 Export to PDF

You can export by printing:
File → Print → Save as PDF

The layout is optimized for landscape A4 pages.

---

## 💡 Tips

- The app works entirely **offline**, so it’s safe for internal or confidential data.  
- If your bank uses a slightly different ABO variant, open an issue and include a sample record.  
- There’s also a built-in **demo button** for testing without real data.

---

## 🪪 License

MIT License © 2025
