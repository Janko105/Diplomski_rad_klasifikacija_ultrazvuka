# Razlikovanje benignih i malignih lezija na ultrazvučnim snimcima dojke

Kod uz diplomski rad. Sistem razlikuje benigne od malignih lezija na
ultrazvučnim snimcima dojke pomoću konvolucione neuronske mreže sa
separabilnim konvolucijama, obučen nad tri javno dostupna skupa
(BUSI, BUS-BRA, BUS-UCLM).

Autor: Janko Joksimović
Mentor: prof. dr Danijela Milošević
Fakultet tehničkih nauka u Čačku, Univerzitet u Kragujevcu, 2026.

## Sadržaj repozitorijuma

- `diplomski_final.ipynb` — kompletan radni tok: priprema podataka,
  obučavanje, eksperimenti i evaluacija (poglavlja 4 i 5 rada).
- `requirements.txt` — verzije korišćenih biblioteka.
- `README.md` — ovaj fajl.

## Okruženje

Rad je izrađen u okruženju **Kaggle Notebooks** (Python 3.12.13,
GPU NVIDIA Tesla T4). Sve verzije biblioteka odgovaraju Kaggle
Docker image-u navedenom u `requirements.txt`.

Pokretanje van Kaggle-a moguće je uz iste verzije biblioteka i
CUDA-kompatibilan GPU, uz izmenu putanja do podataka.

## Podaci

Skupovi podataka **nisu** deo repozitorijuma zbog uslova korišćenja.
Preuzimaju se sa zvaničnih izvora:

- **BUSI** — ____ (link ka izvoru)
- **BUS-BRA** — ____ (link ka izvoru)
- **BUS-UCLM** — ____ (link ka izvoru)

Na Kaggle-u se skupovi dodaju kao *Input datasets*; putanje se podešavaju
u prvoj ćeliji sveske (odeljak „1. Priprema okruženja").

## Pokretanje

1. Otvoriti `diplomski_final.ipynb` u Kaggle Notebooks.
2. Dodati tri skupa kao ulazne skupove (Add Input).
3. Uključiti GPU (Settings → Accelerator → GPU T4).
4. Pokrenuti ćelije redom, odozgo (Run All).

Svaka celina sveske označena je naslovom koji odgovara poglavlju rada:
priprema podataka, model i obučavanje, eksperimenti (šum, uticaj podele,
generalizacija) i završna evaluacija.

## Napomene o reprodukciji

- Nasumičnost je fiksirana inicijalizatorom (`seed`), pa su rezultati
  ponovljivi u granicama opisanim u poglavlju 5.3.
- Konačni model je ansambl osam nezavisnih inicijalizacija (poglavlje 5.5).
