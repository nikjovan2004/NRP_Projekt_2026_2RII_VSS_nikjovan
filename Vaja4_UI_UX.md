# 🧪 Vaja 4 – UX/UI zasnova aplikacije DomServices

## 🎯 Namen vaje

Cilj vaje je oblikovati **UX in UI zasnovo** za DomServices – AI platformo za povezavo med strankami (lastniki domov/stanovanj) in ponudniki lokalnih storitev (popravila, čiščenje, vzdrževanje).  
Osredotoči se na to:

- kako uporabnik **potuje** skozi aplikacijo (flow),
- kakšen je **namen vsakega zaslona**,
- kateri **UI elementi** so na posamezni strani,
- kako **navigacija** povezuje zaslone med seboj.

Na koncu lahko na podlagi tega opisa izdelaš skice ali končni UI (Figma, Canva, Google Stitch …).

---

## 1️⃣ Seznam vseh zaslonov aplikacije

### A) Kupec (lastnik doma / najemnik)

1. Onboarding / Welcome
2. Prijava (Login)
3. Registracija (Sign up)
4. Pozabljeno geslo (Forgot password)
5. Domov (Customer Home / Dashboard)
6. Izbira lokacije (Location picker)
7. Iskanje storitve (AI + kategorije)
8. Rezultati ponudnikov (Search results)
9. Filter & sort (modal)
10. Profil ponudnika (Provider profile)
11. Izbira termina (Time selection)
12. Povzetek naročila & plačilo (Order summary & payment)
13. Potrditev naročila (Booking confirmation)
14. Moja naročila (Bookings list)
15. Podrobnosti naročila (Booking detail / tracking)
16. Chat s ponudnikom (Customer chat)
17. Ocena in mnenje (Rating & review)
18. Račun / Invoice (view invoice)
19. Obvestila (Notifications – customer)
20. Profil in nastavitve (Customer profile & settings)
21. Shranjeni naslovi (Saved addresses)
22. Priljubljeni ponudniki (Favourites)
23. Pomoč & FAQ (Help & FAQ)
24. Pravna obvestila (Terms & Privacy)
25. Napaka / prazno stanje (Error & empty state zasloni)

### B) Ponudnik (obrtnik, čistilec, vrtnar)

26. Prijava ponudnika (isti login, druga vloga)
27. Onboarding ponudnika (Onboarding checklist)
28. Nastavitev profila ponudnika (Provider profile setup)
29. Verifikacija / KYC upload
30. Dashboard ponudnika (Provider dashboard)
31. Upravljanje urnika (Schedule management)
32. Upravljanje storitev in cen (Services & pricing)
33. Podrobnosti naročila – ponudnik (Job detail)
34. Chat s stranko (Provider chat)
35. Zgodovina naročil & zaslužki (Earnings & history)
36. Izplačila (Payouts)
37. Obvestila ponudnika (Notifications – provider)
38. Nastavitve ponudnika (Provider settings)

---

## 2️⃣ UX struktura – kaj se dogaja na posamezni strani

Za vsak zaslon je spodaj:

- **Glavni namen**
- **Glavne akcije uporabnika**
- **Navigacija (kam vodijo gumbi)**

### 2.1 Onboarding / Welcome

- **Namen:** Na kratko razloži, kaj DomServices počne (hitro iskanje lokalnih mojstrov, AI filtriranje, varno plačilo).
- **Akcije:** Swipe med 2–3 informativnimi zasloni, klik na “Začni”, “Prijava”, “Registracija”.
- **Navigacija:**  
  “Začni” → Registracija ali Domov (če je uporabnik že prijavljen)  
  “Prijava” → Login  
  “Registracija” → Sign up

### 2.2 Prijava (Login)

- **Namen:** Uporabnik dostopa do svojega računa.
- **Akcije:** Vnos email/telefona in gesla, prijava, skok na “Pozabljeno geslo”.
- **Navigacija:**  
  “Log in” →  
  - če je kupec → Domov (Home)  
  - če je ponudnik → Provider dashboard  
  “Create account” → Registracija  
  “Forgot password?” → Pozabljeno geslo

### 2.3 Registracija (Sign up)

- **Namen:** Ustvari nov račun (kupec ali ponudnik).
- **Akcije:** Vnos osebnih podatkov, označitev “Sem ponudnik”, sprejem pogojev.
- **Navigacija:**  
  “Create account” →  
  - brez “Sem ponudnik” → Domov + onboarding tooltipi  
  - z “Sem ponudnik” → Onboarding ponudnika

### 2.4 Pozabljeno geslo

- **Namen:** Obnovi dostop do računa.
- **Akcije:** Vnos emaila, potrditev.
- **Navigacija:**  
  “Send reset link” → info zaslon → “Back to login”

---

### 2.5 Domov (Customer Home / Dashboard)

- **Namen:** Hiter vstop v iskanje storitev.
- **Akcije:**  
  - vnos problema v AI-iskalno polje (npr. “pušča pipa v kuhinji”),  
  - izbor kategorije (Popravila, Čiščenje, Vrt …),  
  - izbor predlaganih hitrih iskanj,  
  - klik na “Priporočeni ponudniki”.
- **Navigacija:**  
  Iskanje / kategorija → Rezultati ponudnikov  
  Ikona lokacije → Izbira lokacije  
  Spodnji meni:  
  - Home → Domov  
  - Bookings → Moja naročila  
  - Notifications → Obvestila  
  - Profile → Profil in nastavitve

### 2.6 Izbira lokacije (Location picker)

- **Namen:** Določi lokacijo storitve.
- **Akcije:** “Use my location”, ročni vnos naslova, izbira na zemljevidu, izbor shranjenega naslova.
- **Navigacija:**  
  “Confirm location” → nazaj na Domov ali Rezultate z novo lokacijo

### 2.7 Iskanje storitve (AI + kategorije)

- **Namen:** Uporabnik natančneje opiše svoj problem.
- **Akcije:** Vnos besedila, nastavitve datuma (danes, ta teden), osnovni filtri (cenovni razpon).
- **Navigacija:**  
  “Najdi ponudnike” → Rezultati ponudnikov

### 2.8 Rezultati ponudnikov

- **Namen:** Prikaz seznama najbolj ustreznih ponudnikov.
- **Akcije:** Pregled kartic, filtriranje, sortiranje, izbor ponudnika.
- **Navigacija:**  
  Klik kartice → Profil ponudnika  
  “Filter” → Filter & sort modal  
  “Nazaj” → Domov / Iskanje

### 2.9 Filter & sort (modal)

- **Namen:** Ožanje rezultatov.
- **Akcije:** Nastavitev min. ocene, cene, razdalje, “samo verificirani”, “dostopen danes”.
- **Navigacija:**  
  “Apply” → nazaj na Rezultate s posodobljenim seznamom  
  “Reset” → ponastavi filtre

### 2.10 Profil ponudnika

- **Namen:** Zgraditi zaupanje (ocene, reference, slike, cene).
- **Akcije:** Pregled informacij, storitev, ocen, galerije; klik na “Rezerviraj termin”; “Dodaj med priljubljene”.
- **Navigacija:**  
  “Rezerviraj termin” → Izbira termina  
  “Nazaj” → Rezultati  
  “Dodaj med priljubljene” → Priljubljeni

### 2.11 Izbira termina (Time selection)

- **Namen:** Izbira dneva in ure.
- **Akcije:** klik na datum, izbira časovnega termina, vnos opombe.
- **Navigacija:**  
  “Naprej na plačilo” → Povzetek & plačilo  
  “Nazaj” → Profil ponudnika

### 2.12 Povzetek naročila & plačilo

- **Namen:** Pregled naročila + izvedba plačila.
- **Akcije:** pregled podatkov, vklop/izklop “Garancija kvalitete” in “Priority booking”, vnos podatkov kartice.
- **Navigacija:**  
  “Plačaj in rezerviraj” → Potrditev naročila  
  “Nazaj” → Izbira termina

### 2.13 Potrditev naročila (Booking confirmation)

- **Namen:** Potrdi uspešno rezervacijo in pojasni naslednje korake.
- **Akcije:** Ogled naročila, vrnitev na Domov.
- **Navigacija:**  
  “Poglej naročilo” → Podrobnosti naročila  
  “Nazaj na Domov” → Domov

### 2.14 Moja naročila (Bookings list)

- **Namen:** Pregled vseh rezervacij.
- **Akcije:** Pregled kartic po statusu (prihodnja, pretekla), klik na naročilo.
- **Navigacija:**  
  Klik kartice → Podrobnosti naročila

### 2.15 Podrobnosti naročila (Booking detail)

- **Namen:** Prikaz statusa in vseh podrobnosti.
- **Akcije:** Sledenje statusu, odpiranje chata, preklic (če še možno), ogled računa po zaključku.
- **Navigacija:**  
  “Chat” → Chat s ponudnikom  
  “Poglej račun” → Račun  
  “Oceni storitev” → Ocena in mnenje  
  “Nazaj” → Moja naročila

### 2.16 Chat s ponudnikom (Customer chat)

- **Namen:** Komunikacija o detajlih storitve.
- **Akcije:** Pošiljanje sporočil, slik (slika poškodbe), dogovor o detajlih.
- **Navigacija:**  
  “Nazaj” → Podrobnosti naročila

### 2.17 Ocena in mnenje (Rating & review)

- **Namen:** Zbiranje verodostojnih ocen.
- **Akcije:** Dati oceno (zvezdice), izbrati tage, napisati komentar, poslati oceno.
- **Navigacija:**  
  “Pošlji oceno” → Podrobnosti naročila / Moja naročila  
  “Preskoči za zdaj” → Podrobnosti naročila

### 2.18 Račun / Invoice

- **Namen:** Pregled računa in prenos.
- **Akcije:** Ogled podatkov, prenos PDF, pošiljanje na email.
- **Navigacija:**  
  “Download PDF” → prenos  
  “Send to email” → pošlje račun  
  “Nazaj” → Podrobnosti naročila

### 2.19 Obvestila (Notifications – customer)

- **Namen:** Seznam vseh pomembnih dogodkov.
- **Akcije:** Klik na obvestilo.
- **Navigacija:**  
  Nova rezervacija → Podrobnosti naročila  
  Sprememba termina → Podrobnosti naročila  
  Nova ocena → Podrobnosti naročila / Ocena

### 2.20 Profil in nastavitve (Customer profile)

- **Namen:** Upravljanje računa.
- **Akcije:** Urejanje podatkov, naslovi, plačilne metode, jezik, odjava.
- **Navigacija:**  
  “Saved addresses” → Shranjeni naslovi  
  “Payment methods” → upravljanje kartic  
  “Help & FAQ” → Pomoč  
  “Legal” → Pravna obvestila  
  “Log out” → Login

### 2.21 Shranjeni naslovi (Saved addresses)

- **Namen:** Hitro izbiranje lokacije.
- **Akcije:** Dodajanje, urejanje, brisanje naslovov.
- **Navigacija:**  
  Izbira naslova pri naročilu → uporaba tega naslova

### 2.22 Priljubljeni ponudniki (Favourites)

- **Namen:** Hitro ponovno naročanje od istih ponudnikov.
- **Akcije:** pregled seznamov, klik na ponudnika.
- **Navigacija:**  
  Klik kartice → Profil ponudnika

### 2.23 Pomoč & FAQ (Help & FAQ)

- **Namen:** Odgovori na najpogostejša vprašanja.
- **Akcije:** pregled kategorij, klik na članek, kontakt podpore.
- **Navigacija:**  
  “Kontaktiraj podporo” → email / chat

### 2.24 Pravna obvestila (Terms & Privacy)

- **Namen:** prikaz pogojev uporabe in politike zasebnosti.
- **Akcije:** branje, sprejem ob registraciji.
- **Navigacija:**  
  “Nazaj” → Profil / Registracija

### 2.25 Error & empty state zasloni

- **Namen:** Prijazno obveščanje o napakah ali praznih seznamih.
- **Akcije:** “Retry”, “Adjust filters”, “Back to home”.

---

### 2.26–38 UX za ponudnika (na kratko)

- **Onboarding ponudnika:** checklist (profil, storitve, urnik, Stripe).
- **Nastavitev profila:** poslovni podatki, opis, področje dela.
- **Verifikacija:** upload dokumentov, status.
- **Dashboard:** današnja naročila, statistika.
- **Urnik:** tedenski pregled, nastavljanje razpoložljivosti.
- **Storitve & cene:** dodajanje/urejanje storitev.
- **Podrobnosti naročila (ponudnik):** potrdi/ zavrni, “na poti”, “zaključeno”, chat.
- **Chat s stranko:** podobno kot customer chat.
- **Zgodovina & zaslužki:** pregled prihodkov.
- **Izplačila:** seznam payoutov, povezava na Stripe.
- **Obvestila ponudnika:** nova naročila, spremembe, ocene.
- **Nastavitve ponudnika:** notification settings, jezik, odjava.

---

## 3️⃣ UI postavitev – ključni elementi na izbranih zaslonih

Spodaj so glavne smernice za vizualno razporeditev.

### 3.1 Domov (kupec)

- **Naslov:** “Kaj želite urediti danes?”
- **Elementi:**
  - Velik search bar z AI oznako.
  - Čipi kategorij (ikone + tekst).
  - Predlagana iskanja v obliki čipov.
  - “Priporočeni ponudniki” – horizontalni seznam kartic.
- **Navigacija:** spodnji tab bar (Home, Bookings, Notifications, Profile).

### 3.2 Rezultati ponudnikov

- **Header:** besedilo iskanja ali izbrana kategorija.
- **Elementi:**
  - vrstica s filtri (ikona Filter, Sort).
  - vertikalni seznam kartic ponudnikov (slika, ime, rating, cena, oznake).
- **CTA:** tap na kartico → Profil ponudnika.

### 3.3 Profil ponudnika

- **Header:** foto, ime, rating, “Verified”.
- **Body:** zavihki/sekcije (About, Services, Reviews, Gallery).
- **Sticky bottom bar:** cena od, gumb “Rezerviraj termin”.

### 3.4 Izbira termina

- **Zgoraj:** indikator korakov (1 Izbira mojstra, 2 Termin, 3 Plačilo).
- **Levo/center:** koledar.
- **Desno/spodaj:** seznam prostih slotov.
- **Spodaj:** gumb “Naprej na plačilo”.

### 3.5 Plačilo

- **Zgoraj:** kartica s povzetkom naročila.
- **V sredini:** opcijski toggle-i (garancija, priority).
- **Spodaj:** forma za kartico + gumb “Plačaj in rezerviraj”.

### 3.6 Rating screen

- **Zgoraj:** naslov + ime izvajalca.
- **Sredina:** velike zvezdice, čipi tagov, textarea.
- **Spodaj:** gumbi “Pošlji oceno” (primarni), “Preskoči za zdaj” (sekundarni).

### 3.7 Dashboard ponudnika

- **Zgoraj:** povzetek (današnji / tedenski prihodki).
- **Sredina:** seznam današnjih jobov (kartice z akcijami).
- **Spodaj / top nav:** zavihki (Naročila, Urnik, Storitve, Zaslužki).

---

## 4️⃣ Prompt za Google Stitch (za generiranje UI)

Ta blok lahko kopiraš v `.md` ali direktno v Google Stitch:

```markdown
## Prompt za Google Stitch – DomServices UI (full)

Design a complete, modern **web + mobile UI** for an on‑demand **home services marketplace** called **DomServices** (similar to “Uber for home repairs and cleaning” in Slovenia).

There are **two roles**:  
1) Customers (home owners / tenants, 25–65)  
2) Service providers (independent pros and small businesses).

Focus on a clean, trustworthy experience, with AI‑based search, real‑time availability and secure payments.

### CUSTOMER FLOWS AND SCREENS

1. **Onboarding / welcome**
   - 2–3 intro slides: “Find trusted local pros”, “Real‑time availability”, “Secure payment & quality guarantee”.
   - Buttons: “Get started”, “Log in”, “Sign up”.

2. **Authentication**
   - **Login:** Email/phone + password, links “Create account”, “Forgot password”.
   - **Sign up:** First name, Last name, Email, Password, checkbox “I am a service provider”, checkbox “I agree to Terms & Privacy”.
   - **Forgot password:** Email field + “Send reset link”.

3. **Customer Home dashboard**
   - Top: greeting and question “What do you need fixed today?”.
   - Large AI search bar (users can type natural language like “my kitchen sink is leaking”), with a small “AI” badge.
   - Chips for categories with icons: Repairs, Cleaning, Garden, Other.
   - Suggested quick queries as chips (e.g. “Fix leaking pipe”, “Deep clean apartment”, “Mow the lawn”).
   - Section “Recommended pros near you” with horizontal scroll of provider cards.
   - Bottom navigation bar: Home, Bookings, Notifications, Profile.

4. **Location picker**
   - “Use my location” button, address input with suggestions, small map with draggable pin.
   - Option to select from saved addresses (Home, Work, Other).
   - Primary button: “Confirm location”.

5. **Search results**
   - Header with query text or selected category and location.
   - Filter & sort bar at the top.
   - Provider cards show: photo, name, rating + number of reviews, starting price, distance, badges “Verified”, “Available today 14:00–16:00”.
   - Tap card → Provider profile.

6. **Filter & sort modal**
   - Controls: minimum rating slider, price range, distance, toggles “Only verified”, “Available today”.
   - Buttons: “Reset”, “Apply”.

7. **Provider profile**
   - Large header: photo, name, rating, “Verified” badge, number of completed jobs.
   - Sections or tabs:
     - About (bio, experience, service area),
     - Services & prices,
     - Reviews,
     - Gallery (before/after photos).
   - Sticky footer: price from, primary button “Book time”.
   - Secondary actions: “Save to favourites”, “Share”.

8. **Time selection**
   - Step indicator: 1) Select pro, 2) Time, 3) Payment.
   - Calendar for date selection.
   - List of available time slots for the chosen day.
   - Notes field: “Add notes for your pro…”.
   - Button: “Continue to payment”.

9. **Order summary & payment**
   - Summary card: service, provider, date, time, address, price breakdown.
   - Optional toggles:
     - “Quality guarantee (+€2)”
     - “Priority booking (+€0.50)”.
   - Payment form with card fields (Stripe‑style), option to save card.
   - Trust indicators: lock icon, “Secure payment”, Stripe logo.
   - Primary button: “Pay and book”.

10. **Booking confirmation**
    - Big checkmark, booking ID, date & time.
    - Text explaining “The provider will confirm your booking and you’ll receive updates here.”
    - Buttons: “View booking”, “Back to home”.

11. **Bookings list**
    - Tabs: Upcoming | Past.
    - Booking cards with service, provider, date, time, price, and status chip (Pending, Confirmed, On the way, Completed, Cancelled).
    - Tap card → Booking detail.

12. **Booking detail**
    - Status timeline (Pending → Confirmed → On the way → Completed).
    - Summary of service and price.
    - Buttons:
      - “Chat with provider”
      - “Cancel booking” (if allowed)
      - “View invoice” (after completion).
    - Link to “Rate service” when completed.

13. **Customer chat**
    - Chat UI with message bubbles, timestamps.
    - Input field with attachment icon to upload photos of the problem.
    - Header: provider photo, name, status (Online / Last seen).

14. **Rating & review screen**
    - Title: “How satisfied were you with this service?”
    - Subtitle with provider name and service.
       - Large 1–5 star rating.
    - Quick-tag chips: “On time”, “Friendly”, “High quality”, “Great value”, “Poor communication”, “Late arrival”.
    - Multiline text area for an optional comment.
    - Info text: “Your review helps others choose the right pro.”
    - Buttons: primary “Submit review”, secondary “Skip for now”.

15. **Invoice / receipt**
    - Invoice-style page:
      - Invoice ID, date, Paid status.
      - Provider details, customer details.
      - Line items with service, quantity, unit price, subtotal, taxes if any, total.
      - Payment method (“Paid with card via Stripe”).
    - Buttons: “Download PDF”, “Send to email”.

16. **Notifications (customer)**
    - List of notifications: new booking status, provider messages, reminders, review prompts.
    - Each item leads to Booking detail, Chat, or Rating screen.

17. **Customer profile & settings**
    - Sections:
      - Personal info
      - Saved addresses
      - Payment methods
      - Notifications preferences (push/email/SMS)
      - Language
      - Help & FAQ
      - Legal (Terms & Privacy)
      - Log out.

18. **Favourites**
    - List of saved providers with same card design as search results.

19. **Help & FAQ**
    - Categories and searchable articles about payments, cancellations, quality guarantee, account.
    - Button “Contact support”.

20. **Terms & Privacy**
    - Scrollable legal text, linkable from registration and profile.

21. **Empty and error states**
    - No results state with friendly message, buttons “Adjust filters” and “Show all in your city”.
    - Network/server error state with “Retry” and “Back to home”.

### PROVIDER FLOWS AND SCREENS

22. **Provider onboarding checklist**
    - After choosing “I am a service provider”.
    - Steps: 1) Complete profile, 2) Add services & prices, 3) Set availability, 4) Connect payouts (Stripe).
    - Progress indicator and CTA buttons for each step.

23. **Provider profile setup**
    - Business name, contact info, service areas, description, profile photo/logo.

24. **Verification / KYC**
    - Upload ID and business documents.
    - Status: Pending / Verified / Rejected.

25. **Provider dashboard**
    - Today’s jobs list with times, addresses, status.
    - Summary of today’s and this week’s earnings.
    - Quick filters by status (New, Accepted, On the way, Completed).

26. **Schedule management**
    - Weekly calendar where providers mark available slots.
    - Ability to set recurring availability.

27. **Services & pricing**
    - List of services with price and duration.
    - “Add service” form with name, description, price type (fixed/hourly).

28. **Job detail (provider)**
    - Customer name, address with small map, date/time, notes.
    - Buttons: “Accept”, “Decline”, “On the way”, “Mark as completed”.
    - Shortcut to chat with the customer.

29. **Provider chat**
    - Same layout as customer chat, separate role.

30. **Earnings & payouts**
    - Earnings overview graph.
    - List of payouts with date, amount, status.
    - Button “Connect Stripe account”.

31. **Notifications (provider)**
    - New bookings, changes, cancellations, new reviews.
    - Tapping items leads to Job detail or Reviews.

32. **Provider settings**
    - Notification preferences, language/region, account details, log out.

### VISUAL STYLE

- Light theme, lots of white space, rounded cards and buttons.
- Friendly, “home services” look and feel.
- Main accent color: calming blue or teal; primary CTA color: contrasting warm orange.
- Clear typography hierarchy and large tap targets for mobile.
- Strong emphasis on trust: verified badges, star ratings, secure payment labels, clear statuses.

### OUTPUT

- Provide responsive layouts for both **mobile and desktop** for key screens (Home, Search results, Provider profile, Booking flow, Customer dashboard, Provider dashboard).
- Make navigation flows clear and intuitive, minimizing steps to book a service.
- Highlight elements that build **trust and reliability** at every step.
