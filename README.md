# 🎿 SkiExplorer – Napredne baze podataka (Neo4j + Cassandra)

## 📌 Opis projekta

**SkiExplorer** je full-stack web aplikacija razvijena kao projekat iz predmeta *Napredne baze podataka*.

Cilj projekta je demonstracija rada sa **graf bazom (Neo4j)** i **distribuiranom NoSQL bazom (Cassandra)** u okviru jedne aplikacije, uz backend implementiran u ASP.NET Web API i frontend u React-u.

Aplikacija omogućava upravljanje podacima o skijalištima, stazama, aktivnostima, obaveštenjima i vremenskim uslovima, kao i funkcionalnost preporuke staza na osnovu nivoa skijanja korisnika.

---

## 🏗️ Arhitektura sistema

Aplikacija je realizovana kao client-server sistem:

- 🔹 Backend: ASP.NET Web API
- 🔹 Frontend: React (JS)
- 🔹 Graf baza: Neo4j
- 🔹 Distribuirana baza: Cassandra

### 📊 Podela odgovornosti baza

**Neo4j** je korišćen za:
- modelovanje relacija između skijališta i staza
- implementaciju funkcionalnosti preporuke staza
- graf analizu i povezivanje entiteta

**Cassandra** je korišćena za:
- skladištenje strukturiranih podataka o:
  - skijalištima
  - stazama
  - aktivnostima
  - obaveštenjima
  - vremenskoj prognozi
- demonstraciju rada sa distribuiranim NoSQL sistemom

---

## 🚀 Funkcionalnosti aplikacije

- Upravljanje skijalištima i stazama
- Evidencija aktivnosti i obaveštenja
- Demonstracija vremenske prognoze
- Preporuka staza na osnovu nivoa skijanja korisnika

### 🎯 Preporuka staza

Na osnovu unetog nivoa skijanja:

- **nizak nivo** → plava staza  
- **srednji nivo** → crvena staza  
- **visok nivo** → crna staza  

Logika preporuke realizovana je kroz graf relacije u Neo4j bazi.

---

## 🌦️ Vremenska prognoza (Demonstracija)

Sistem sadrži modul za prikaz vremenske prognoze.

⚠️ Napomena:  
Vremenska prognoza je simulirana i služi kao demonstracija funkcionalnosti sistema. Aplikacija nije povezana sa realnom meteorološkom stanicom niti eksternim API servisom.

Podaci se generišu u okviru sistema radi testiranja rada sa bazom i prikaza promena vremenskih parametara.

---

## 🧰 Tehnologije

- C#
- ASP.NET Web API
- React (JavaScript)
- Neo4j
- Cassandra
- REST arhitektura

---

## ⚙️ Pokretanje aplikacije (lokalno)

### 1️⃣ Pokretanje baza

Potrebno je pokrenuti:
- Cassandra
- Neo4j

### 2️⃣ Backend

```bash
cd SkiExplorer
dotnet run
```
### 3️⃣ Frontend

```bash
npm install
npm start
```

---

## 📈 Buduća unapređenja
- Interaktivna ski mapa sa grafičkim prikazom staza
- Integracija sa realnim meteorološkim API servisom
- Napredniji sistem preporuka
- Optimizacija performansi pri radu sa većim skupovima podataka
