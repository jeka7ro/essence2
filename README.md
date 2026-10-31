# Simulator Circuit Sală (35.3m × 21.6m) — 800 Persoane Față în Față

Simulator interactiv dezvoltat în HTML5 Canvas & Vanilla JavaScript pentru configurarea, vizualizarea și analiza fluxului a **800 de participanți** (400 perechi față în față) într-o sală de **35.30 m lungime × 21.60 m lățime**.

---

## Caracteristici Principale

- **9 Culoare Drepte & 8 Bucle U**: împărțite exact pe cele 3 compartimente ale sălii:
  - **C3 (6.6 m)**: Culoarele 1, 2, 3
  - **C2 (6.7 m)**: Culoarele 4, 5, 6
  - **C1 (6.6 m)**: Culoarele 7, 8, 9
- **40 de Asistenți (A1 la A40)**: poziționați exclusiv pe tronsoanele drepte, aliniați în 5 rânduri regulate pe lățimea sălii (niciun asistent pe viraje).
- **START & END**:
  - **START**: Culoarul 1 (Sus-Stânga), orientat în jos.
  - **END**: Culoarul 9 (Jos-Dreapta), orientat în jos spre ieșire.
- **Deplasare în Contrasens (Pas la Dreapta)**: participanții stau față în față timp de 10 secunde (configurabil), apoi fac 1 pas lateral la dreapta.

---

## 4 Soluții Geometrice pentru Păstrarea a 800 de Persoane (Fără Reducere)

Pe liniile drepte ($9 \times 29.4\text{ m} = 264.6\text{ m}$), cei 800 de oameni au **73.4 cm/om** (lejer, umerii au 46 cm). Înghesuiala apărea doar pe interiorul celor 8 viraje U dacă se păstra lățimea de 1.20 m peste tot (unde raza strânsă reducea spațiul la 35.1 cm).

1. ** Soluția 1 (Recomandată): Culoar Conic 0.70 m pe Viraje (și 1.20 m pe Drept)**
   - Lățimea pe viraj este redusă la 0.70 m.
   - Raza interioară crește la 0.80 m $\rightarrow$ spațiul dintre participanți devine **51.0 cm** (> 46 cm umeri). **Zero zone roșii!**
2. ** Soluția 2: Viraje de Tranzit Fluid (Staționare doar pe Drept)**
   - Toate cele 400 de perechi stau față în față pe liniile drepte (**66.1 cm/om**).
   - Virajele U sunt zone de tranzit continuu (fără oprire pe viraj).
3. ** Soluția 3: Dispunere în Șah (Decalaj 20 cm pe Viraj)**
   - Rândul din interior este decalat cu 20 cm în lungul arcului.
   - Umerii nu se mai ating lateral, ci se suprapun în spațiul toracic liber (adâncime corp 24 cm).
4. ** Soluția 4: Traseu Maxim la Pereți (0.60 m) + Viraj 0.75 m**
   - Circuit extins la 304.5 metri în sală, cu 76 cm pe drept și 52 cm pe viraj.

---

## Acces Online (GitHub Pages)

Aplicația este configurată pentru deploy automat pe GitHub Pages:
 **[https://jeka7ro.github.io/essence2/](https://jeka7ro.github.io/essence2/)**

---

## Utilizare pe Mobil și Desktop

- **Mobil:** 
  - Butoane rapide de navigare: ` Plan Sală & Animație` (ecran complet) vs ` Setări & Calcule (800)`.
  - Suport tactil nativ: tragere cu un deget pentru pan / deplasare și pinch cu 2 degete pentru zoom in/out.
- **Desktop:**
  - Panou lateral complet cu parametri, distanțe reglabile față de pereți, cronometru 2s - 60s, pas înainte (+1) și pas înapoi (-1).
  - Comutator instant între cele 4 soluții geometrice deasupra planului.

---

## Rulare Locală

Deschide direct `index.html` în orice browser modern sau pornește un server HTTP local:

```bash
python3 -m http.server 8000
```

Accesează în browser:
`http://localhost:8000`

