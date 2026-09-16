# Outreach CRM

Lični sales/outreach CRM za freelancere i agencije koji prave web sajtove. Prati
outreach putem poruka (Instagram, Facebook, email…) i cold calling (firme sa Google Maps-a),
sve do zatvorene prodaje. Radi u browseru, bez servera — svi podaci se čuvaju lokalno
(localStorage) i ostaju sačuvani nakon refresh-a.

## Kako se koristi

Otvori `index.html` u browseru (dupli klik ili preko web servera). Aplikacija odmah
učita nekoliko testnih (demo) prospekata i leadova da vidiš kako radi — možeš ih obrisati
jednim klikom u **Settings → Obriši testne**.

## Sekcije

- **Dashboard** — kombinovani pregled: ukupno leadova, outreach pokušaji, pozivi, ponude,
  prodaje, **Total Revenue** i **Average Deal Value**, plus Message i Cold Calling metrike,
  conversion rate-ovi i levci (funnel).
- **Message Outreach** — ručno editable KPI kartice (Poslate poruke, Odgovori, Prihvatili sajt,
  Pozitivni utisci, Zakazani/Održani pozivi, Prodaje). Dugme **✏️ Edit Metrics** za ručnu izmenu.
  Automatski conversion rate-ovi (Reply, Website Acceptance, Positive Feedback, Call Booking,
  Call Show, Close, Overall Outreach-to-Sale). Ispod je tabela leadova (dodaj/izmeni/obriši,
  pretraga, filteri po statusu/platformi, sortiranje).
  - **Manual / Iz leadova** — podrazumevano je *Manual* (brojevi se vode ručno, nezavisno od
    pojedinačnih leadova). Prebaci na *Iz leadova* da se metrike računaju iz tabele.
- **Cold Calling** — KPI kartice se automatski računaju iz prospekata (Ukupno, Kontaktirani,
  Zainteresovani, Poslate ponude, Won, Odbijeni) + Contact/Interest/Offer/Close rate.
  **Kanban pipeline** sa drag & drop (Prospekt → Kontaktiran → Zainteresovan → Poslata ponuda
  → Won → Odbijen) i brzim akcijama na svakoj kartici.
- **Prospekti** — baza firmi. Pretraga po nazivu/telefonu/lokaciji, filter po statusu i periodu,
  sortiranje. Na svakom prospektu: otvori Google Maps, otvori sajt, kopiraj telefon, izmeni, obriši.
- **Settings** — tema (tamna/svetla), valuta, Export (JSON/CSV), Import (JSON), brisanje testnih
  podataka i reset svih podataka (uz potvrdu).

## Revenue

Kod svakog **Won** klijenta (lead ili prospekt) uneseš vrednost posla. Dashboard onda
prikazuje ukupan **Total Revenue** i **Average Deal Value**.

## Podaci i migracija

Podaci žive u `localStorage` (`outreach_crm_v2`) tog browsera/uređaja. Struktura je čist
JSON (`settings`, `messageMetrics`, `leads[]`, `prospects[]`) pa lako može kasnije da se
prebaci na pravi online database/server. Koristi **Export (JSON)** za backup i prenos.

## Bez zavisnosti

Cela aplikacija je jedan `index.html` (HTML + CSS + JS), bez eksternih biblioteka.
