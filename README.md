# Outreach CRM

Jednostavan CRM za praćenje outreach kontakata, poruka i poziva. Radi u browseru,
bez servera i baze — svi podaci se čuvaju lokalno (localStorage) u tvom browseru.

## Kako se koristi

Otvori `index.html` u browseru (dupli klik na fajl ili preko web servera).

### Mogućnosti

- **Kontakti** — ime, firma, telefon, email, izvor, status i napomena.
- **Statusi** — Nov → Kontaktiran → Zainteresovan → Dogovoreno → Odbijen.
- **Aktivnosti** — za svaki kontakt beležiš pozive, poruke, mejlove, sastanke i beleške
  (datum/vreme, ishod, napomena). Kad dodaš prvu aktivnost kontaktu koji je "Nov",
  status automatski prelazi u "Kontaktiran".
- **Follow-up** — zakaži datum sledećeg kontakta; dospeli i današnji se ističu i broje na vrhu.
- **Dashboard** — brojači: ukupno, dospeli follow-up, zainteresovani, dogovoreno.
- **Pretraga i filteri** — po tekstu, statusu, "samo dospeli", i sortiranje.
- **Backup** — izvoz/uvoz svih podataka kao JSON, plus CSV izveštaj za Excel.

## Važno o podacima

Podaci žive u localStorage tog konkretnog browsera i uređaja. Ako obrišeš podatke
browsera ili menjaš uređaj, koristi dugme **Backup** (JSON) da sačuvaš/preneseš podatke.

## Bez zavisnosti

Ceo CRM je jedan `index.html` fajl (HTML + CSS + JS), bez eksternih biblioteka.
