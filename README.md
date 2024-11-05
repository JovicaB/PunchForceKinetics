# Punch Force Kinetics

**PunchForceKinetics** je projekat koji primenjuje mašinsko učenje za analizu i merenje snage udarca i dinamike pokreta tokom udaranja bokserske vreće. Pored toga, projekat pruža zbirne statističke podatke o trening sesijama, uključujući potrošene kalorije, intenzitet treninga, brzinu udaraca i energetsku efikasnost.

Fokusira se na prepoznavanje udaraca rukom ili nogom, kao i na precizno merenje ključnih trenutaka u pokretu, poput trenutka početka udarca, kontakta sa vrećom i prenosa sile.

## Karakteristike

- **Detekcija udarca** – Prepoznavanje trenutka početka udarca i kontakta sa vrećom.
- **Analiza snage udarca** – Merenje vremena i brzine udarca pomoću video okvira za procenu prenosa sile.
- **Klasifikacija pokreta** – Prepoznavanje da li je pokret iniciran rukom ili nogom, omogućavajući korišćenje specifičnog modela za svaku vrstu pokreta.
- **Kinetička analiza** – Procena kinetičke i potencijalne energije u ključnim trenucima udarca.
- **Open-Source i Prilagodljivo** – Kod je dizajniran tako da se može kalibrisati prema fizičkim karakteristikama različitih korisnika.

## Tehnologije

- **Python** – Glavni programski jezik za obradu video podataka i primenu modela.
- **OpenCV** – Biblioteka za računski vid, korišćena za obradu i analizu video okvira u realnom vremenu.
- **Deep Learning modeli** – Modeli za prepoznavanje ključnih tačaka (pose estimation) kao što su MediaPipe ili OpenPose, korišćeni za praćenje pokreta ruku i nogu.
- **GoPro** – Kamera koja snima video zapise visoke frekvencije i služi kao izvor podataka za analizu.

## Instalacija

1. Klonirajte repozitorijum:

   ```bash
   git clone https://github.com/korisnicko-ime/PunchForceKinetics.git
   cd PunchForceKinetics

2. Instalirajte potrebne zavisnosti:

bash
pip install -r requirements.txt

3. Podesite GoPro kameru i osigurajte Wi-Fi konekciju da biste mogli da prenosite uživo video stream u Python za dalju analizu i kalibraciju modela.

Upotreba
1. Faza: Snimanje i Priprema Podataka

Pokrenite skriptu za snimanje videa pomoću GoPro kamere. Snimljeni video se deli u okvire koji se potom ručno označavaju (početak i kraj svakog udarca) kako bi se stvorio set podataka za treniranje.
2. Faza: Treniranje i Real-Time Analiza

    Trenira se model za prepoznavanje udaraca rukom i nogom koristeći video okvire.
    Nakon klasifikacije, koristi se model za procenu energije i prenos sile za svaki udarac.

## Budući Razvoj

    Automatska kalibracija za personalizovano merenje snage udarca na osnovu fizičkih karakteristika korisnika.
    Dalja optimizacija klasifikacije pokreta za efikasnije prepoznavanje udaraca rukom ili nogom.
    Višekanalna analiza – Korišćenje dodatnih senzora (ako su dostupni) za precizniju procenu pritiska i sile.

## Licenca

Projekat je licenciran pod GNU GPLv3 licencom – zadržava prava autora i obavezuje da sve izmene ostanu otvorene.