# Swiss Grid Styleguide

## 1. Charakter stylu

Swiss Grid to styl dla produktów, raportów i prezentacji, które mają wyglądać technicznie, wiarygodnie i spokojnie. Nie opiera się na dekoracji, lecz na rytmie siatki, mocnej typografii, cienkich liniach konstrukcyjnych, dużej ilości białej przestrzeni i jednym świadomym kolorze akcentowym.

Ten wariant jest inspirowany aktualną prezentacją ReplayFlow: białe tło, czarny tekst, czerwony akcent, techniczne etykiety, 12-kolumnowy układ, poziome reguły i precyzyjne wykresy.

Styl ma sprawiać wrażenie:

- analitycznego, a nie marketingowo-ozdobnego,
- nowoczesnego, ale nie startupowo-gradientowego,
- oszczędnego, ale nie pustego,
- technicznego, ale nadal zrozumiałego dla odbiorcy biznesowego.

## 2. Zasady nadrzędne

1. Informacja jest dekoracją.
2. Każdy element musi mieć powód: tytuł, dane, reguła, wykres, etykieta albo podział.
3. Kolor akcentowy służy do znaczenia, nie do ozdabiania.
4. Jedna plansza lub ekran powinien mieć jeden główny komunikat.
5. Układ ma być wyrównany do siatki, nawet jeśli kompozycja jest asymetryczna.
6. Tekst nie może walczyć z kontenerem. Jeśli treść się nie mieści, skróć tekst albo zmień układ.
7. Wykresy i tabele są pełnoprawnymi obiektami projektowymi, nie zrzutami z Excela.
8. Unikaj cieni, gradientów, zaokrąglonych kart i ozdobnych ilustracji, jeśli nie niosą informacji.

## 3. Paleta kolorów

Paleta jest prawie monochromatyczna. Czerwony akcent ma działać jak marker redakcyjny: wskazuje decyzję, ryzyko, lukę, ważny punkt lub aktywny stan.

| Token | Hex | Rola |
|---|---:|---|
| `--color-bg` | `#FFFFFF` | główne tło slajdów i ekranów |
| `--color-ink` | `#0B0B0B` | główny tekst, osie, reguły wysokiego priorytetu |
| `--color-muted` | `#5F6673` | tekst drugorzędny, opisy, podpisy |
| `--color-subtle` | `#9AA0AA` | metadane, numery stron, osie pomocnicze |
| `--color-line` | `#E8E8E8` | delikatne separatory, siatka, granice tabel |
| `--color-soft` | `#F5F5F5` | podświetlenie wiersza, lekkie tło panelu |
| `--color-accent` | `#FF3B30` | najważniejszy akcent semantyczny |
| `--color-positive` | `#10B981` | wzrost, przychód, pozytywny wynik |
| `--color-positive-dark` | `#087B4E` | tekst lub etykieta pozytywna na jasnym tle |

Zalecane proporcje:

- 80-90% biel i jasne neutralne tło,
- 8-15% czarny tekst i linie,
- 2-5% czerwony akcent,
- zieleń tylko na wykresach finansowych lub statusach pozytywnych.

Nie używaj:

- gradientów jako tła,
- fioletowo-niebieskich palet SaaS,
- wielu kolorów kategorii naraz,
- szarych tekstów o zbyt niskim kontraście,
- czerwieni dla wszystkiego, co jest po prostu ozdobą.

## 4. Typografia

### Fonty

Rekomendowany zestaw:

- UI i tekst główny: `Plus Jakarta Sans`, `Inter`, `Helvetica Neue`, `Arial`, sans-serif.
- Etykiety techniczne i dane: `Space Grotesk`, `IBM Plex Mono`, `Roboto Mono`, monospace.

W prezentacji aktualny klimat najlepiej oddaje:

```css
font-family: "Plus Jakarta Sans", Arial, sans-serif;
font-family: "Space Grotesk", monospace;
```

### Hierarchia UI

| Element | Rozmiar | Line-height | Waga | Uwagi |
|---|---:|---:|---:|---|
| Display | 48-64px | 0.98-1.06 | 800 | tylko na widok startowy lub duży nagłówek |
| Page title | 32-44px | 1.05-1.12 | 800 | tytuł ekranu aplikacji |
| Section title | 22-28px | 1.15 | 800 | nagłówek sekcji |
| Card title | 16-20px | 1.2 | 700-800 | krótki, bez łamania na wiele linii |
| Body | 14-16px | 1.45-1.6 | 400-500 | opis, formularze, treść |
| Small / meta | 11-13px | 1.35-1.5 | 500-700 | etykiety, statusy, numery |
| Kicker | 10-12px | 1.2 | 700 | uppercase, letter-spacing 1.5-2px |

### Hierarchia prezentacji 16:9

| Element | Rozmiar | Line-height | Waga |
|---|---:|---:|---:|
| H1 cover | 72-84px | 0.95-1.0 | 800 |
| H2 slide title | 48-56px | 1.04-1.08 | 800 |
| H3 claim | 34-40px | 1.08-1.12 | 800 |
| H4 module title | 18-22px | 1.15 | 800 |
| Body | 14-16px | 1.45-1.6 | 400-500 |
| Table text | 11-13px | 1.25-1.4 | 500 |
| Axis label | 10-12px | 1.2 | 500 |

### Reguły typograficzne

- Nie stosuj ujemnego letter-spacingu.
- Nie centruj długich bloków tekstu.
- Nagłówki mogą być masywne, ale tekst pomocniczy musi oddychać.
- Kicker jest zawsze mały, czerwony, techniczny i pisany uppercase.
- Monospace stosuj do liczb, metadanych, osi wykresów, etykiet typu `M1`, `BEP`, `SOM 12M`.
- Nie mieszaj więcej niż dwóch rodzin fontów.

## 5. Siatka i spacing

### Prezentacja

Format bazowy:

- canvas: `1280 x 720`,
- margines poziomy: `80px`,
- margines pionowy: `60px`,
- grid: 12 kolumn,
- gutter: `32px`,
- tło opcjonalne: delikatna siatka `80px x 80px` na slajdach otwierających.

Tokeny:

```css
:root {
  --slide-w: 1280px;
  --slide-h: 720px;
  --slide-x: 80px;
  --slide-y: 60px;
  --grid-gap: 32px;
  --grid-unit: 80px;
}
```

Układy prezentacyjne:

```css
.slide {
  width: 1280px;
  height: 720px;
  padding: 60px 80px;
}

.cols-12 {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 32px;
  align-items: center;
}

.two { display: grid; grid-template-columns: 1fr 1fr; gap: 56px; }
.three { display: grid; grid-template-columns: repeat(3, 1fr); gap: 32px; }
.four { display: grid; grid-template-columns: repeat(4, 1fr); gap: 24px; }
```

### UI

Desktop:

- outer margin: `32px`,
- content max width: `1180-1280px`,
- grid: 12 kolumn,
- gutter: `24-32px`,
- section spacing: `48-72px`,
- component spacing: wielokrotności `8px`.

Tablet:

- outer margin: `24px`,
- grid: 8 kolumn,
- gutter: `20-24px`.

Mobile:

- outer margin: `16px`,
- grid: 4 kolumny lub jedna kolumna,
- gutter: `16px`,
- redukuj liczbę kolumn, nie zmniejszaj tekstu agresywnie.

Skala spacingu:

| Token | Wartość | Użycie |
|---|---:|---|
| `--space-1` | `4px` | drobne korekty |
| `--space-2` | `8px` | odstęp ikona-tekst, małe grupy |
| `--space-3` | `12px` | pola formularza, małe paddingi |
| `--space-4` | `16px` | standardowy padding komponentu |
| `--space-5` | `24px` | odstęp między modułami |
| `--space-6` | `32px` | gutter, duży padding |
| `--space-7` | `48px` | sekcje |
| `--space-8` | `64px` | hero, rozdziały |
| `--space-9` | `80px` | margines prezentacji |

## 6. Linie, reguły i separatory

Linie są ważnym elementem stylu. Zastępują karty, cienie i dekoracyjne ramki.

Typy linii:

- `2px #0B0B0B` dla głównych reguł modułu,
- `1px #0B0B0B` dla osi, ramek i silnych podziałów,
- `1px #E8E8E8` dla siatki, tabel i sekcji pomocniczych,
- `4px #FF3B30` dla pionowego akcentu lub krytycznej notatki.

Przykład:

```css
.rule-box {
  border-top: 2px solid var(--color-ink);
  padding-top: 16px;
}

.rule-box.is-accent {
  border-top-color: var(--color-accent);
}

.note {
  border-left: 4px solid var(--color-accent);
  padding-left: 18px;
}
```

Nie używaj linii jako ozdoby, jeśli niczego nie grupują.

## 7. Komponenty UI

### Shell aplikacji

Układ aplikacji powinien być spokojny i użytkowy.

- Górny pasek: biały, bez gradientu, z cienką dolną linią.
- Sidebar: tylko jeśli nawigacja ma więcej niż 5-6 pozycji.
- Aktywny stan: czarny tekst + mały czerwony marker, nie duże kolorowe tło.
- Breadcrumbs: monospace lub small text, neutralny szary.

```css
.app-shell {
  min-height: 100vh;
  background: #fff;
  color: var(--color-ink);
  font-family: "Plus Jakarta Sans", Arial, sans-serif;
}

.topbar {
  height: 64px;
  border-bottom: 1px solid var(--color-line);
  display: flex;
  align-items: center;
  padding: 0 32px;
}
```

### Panele i sekcje

W tym stylu panel nie musi być kartą z cieniem. Preferowany jest moduł z górną regułą.

```css
.panel {
  border-top: 2px solid var(--color-ink);
  padding-top: 16px;
}

.panel-title {
  font-size: 20px;
  line-height: 1.15;
  font-weight: 800;
}

.panel-copy {
  margin-top: 10px;
  font-size: 15px;
  line-height: 1.55;
  color: var(--color-muted);
}
```

Używaj kart tylko dla:

- powtarzalnych rekordów,
- modalnych obiektów,
- list wyników,
- narzędzi wymagających ramy.

Nie wkładaj kart w karty.

### Przyciski

Przyciski mają być proste, prostokątne i czytelne.

```css
.button {
  min-height: 40px;
  padding: 0 16px;
  border: 1px solid var(--color-ink);
  background: var(--color-ink);
  color: #fff;
  font-weight: 700;
  cursor: pointer;
}

.button.secondary {
  background: #fff;
  color: var(--color-ink);
}

.button.danger,
.button.accent {
  border-color: var(--color-accent);
  background: var(--color-accent);
  color: #fff;
}
```

Reguły:

- border radius `0-4px`, maksymalnie `6px`,
- ikona + krótki tekst dla głównych akcji,
- sama ikona dla narzędzi powtarzalnych,
- tooltip dla ikon nieoczywistych,
- nie używaj dużych, miękkich pill buttonów jako głównego języka UI.

### Formularze

Formularze powinny wyglądać technicznie i spokojnie.

```css
.field label {
  display: block;
  margin-bottom: 8px;
  font-family: "Space Grotesk", monospace;
  font-size: 11px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: var(--color-muted);
}

.input {
  width: 100%;
  min-height: 42px;
  border: 1px solid var(--color-line);
  padding: 0 12px;
  background: #fff;
  color: var(--color-ink);
}

.input:focus {
  outline: 2px solid var(--color-ink);
  outline-offset: 1px;
}
```

Stany:

- błąd: cienka czerwona linia i krótki opis,
- sukces: zielony tekst lub marker, bez dużego zielonego tła,
- disabled: `#F5F5F5`, tekst `#9AA0AA`.

### Tabele

Tabele są jednym z najlepszych nośników tego stylu.

```css
.table {
  width: 100%;
  border-collapse: collapse;
  font-family: "Space Grotesk", monospace;
  font-size: 12px;
}

.table th {
  text-align: left;
  padding: 12px 10px 12px 0;
  border-bottom: 2px solid var(--color-ink);
  text-transform: uppercase;
}

.table td {
  padding: 16px 10px 16px 0;
  border-bottom: 1px solid var(--color-line);
  vertical-align: top;
}

.table tr.is-emphasis td {
  background: var(--color-soft);
  border-bottom: 1px solid var(--color-ink);
  font-weight: 800;
}
```

Reguły:

- liczby wyrównuj do prawej,
- tekst kategorii wyrównuj do lewej,
- nie stosuj zebra stripingu, jeśli tabela jest krótka,
- podświetl maksymalnie jeden wiersz jako wniosek.

### Statusy i badge

Status nie powinien wyglądać jak kolorowa etykieta z dashboardu SaaS. Lepiej użyć tekstu monospace i punktu.

```css
.status {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  font-family: "Space Grotesk", monospace;
  font-size: 12px;
}

.status::before {
  content: "";
  width: 8px;
  height: 8px;
  background: currentColor;
  border-radius: 50%;
}
```

### Timeline

Timeline w stylu Swiss Grid jest najlepiej pokazać jako rząd modułów z oznaczeniami `M1`, `M2`, `M3`.

- Każdy etap ma krótki tytuł i maksymalnie 1-2 zdania.
- Czerwień oznacza aktywny lub kluczowy milestone.
- Linie poziome mogą łączyć etapy, ale nie powinny dominować nad treścią.

## 8. Wykresy i dane

Wykresy muszą być czyste i podpisane tak, aby dało się je wyjaśnić w 20 sekund.

### Zasady

- Osie czarne, `1-2px`.
- Linie pomocnicze jasnoszare.
- Jedna linia akcentowa na wykres, maksymalnie dwie, jeśli porównanie tego wymaga.
- Czerwony punkt tylko dla decyzji, progu, ryzyka albo BEP.
- Etykiety nie mogą nachodzić na linie ani punkty.
- Legenda jest zbędna, jeśli linie są opisane bezpośrednio.
- Unikaj napisu typu "zysk/strata", jeśli opowiadasz to głosem i wykres jest już zrozumiały.

### Kolory wykresów

| Obiekt | Kolor |
|---|---:|
| Przychody / pozytywny wynik | `#10B981` |
| Koszty / linia bazowa | `#0B0B0B` |
| Próg / akcent / alarm | `#FF3B30` |
| Siatka pomocnicza | `#E8E8E8` |
| Opisy osi | `#5F6673` |

### Wykres BEP

Minimalny standard:

- `S` = sprzedaż / przychody,
- `Ks` = koszty stałe,
- `Kc` = koszty całkowite,
- punkt BEP leży na przecięciu `S` i `Kc`,
- jeśli pokazujesz `Ks`, opisz je jako linię referencyjną, nie punkt przecięcia.

## 9. Wzorce slajdów

### Cover

Układ:

- duży tytuł po lewej,
- krótki opis pod tytułem,
- mały czerwony element lub techniczna etykieta,
- opcjonalna delikatna siatka w tle.

Nie dodawaj:

- autora jako wielkiego elementu,
- logotypu w każdym rogu,
- rozbudowanego footera,
- ozdobnych gradientów.

### Slajd problemu

Najlepszy układ:

- duża teza na górze,
- po prawej krótkie wyjaśnienie,
- na dole 3-4 moduły z regułą,
- ostatni moduł może mieć czerwoną linię jako "luka".

### Slajd procesu

Stosuj sekwencję:

```text
01 NAGRANIE -> 02 SOP -> 03 REPLAY
```

Każdy krok:

- numer jako duży jasnoszary element,
- tytuł mocny,
- opis krótki,
- najważniejszy krok może mieć czerwoną regułę.

### Slajd architektury

Układ:

- lewa część: diagram procesu,
- prawa część: teza lub ograniczenie,
- małe moduły pod diagramem dla doprecyzowania.

Diagram powinien być prosty:

```text
Capture -> SOP -> Replay + Evidence
```

### Slajd rynku

Układ:

- trzy kolumny: `TAM`, `SAM`, `SOM 12M`,
- każda kolumna ma liczbę, definicję i interpretację,
- czerwony akcent tylko przy najważniejszym celu.

### Slajd konkurencji

Najlepszy format to tabela, nie rozrzucone logotypy.

Kolumny:

- kategoria,
- przykłady,
- mocna strona,
- słabość,
- luka / odpowiedź.

ReplayFlow lub własne rozwiązanie powinno być ostatnim wierszem, z lekkim tłem i mocniejszym tekstem.

### Slajd pozycjonowania

Układ:

- lewa część: macierz 2x2 lub prosty wykres,
- prawa część: interpretacja.

Osie muszą opisywać realne kryteria:

- nie "lepsze/gorsze",
- tylko mierzalne lub obronne cechy, np. adaptacja UI, ślad audytu, koszt wdrożenia, prywatność.

### Slajd 4P

Układ:

- cztery równe moduły,
- każdy moduł ma kicker: `Product`, `Price`, `Promotion`, `Place`,
- tekst w module to maksymalnie 2-3 linie.

Szczegóły opowiada się głosem, nie upycha na slajdzie.

### Slajd kosztów

Najlepszy format:

- tabela kosztów,
- suma wyróżniona mocniejszą linią,
- pod tabelą jedno krytyczne założenie.

### Slajd harmonogramu

Układ:

- sześć modułów `M1-M6`,
- każdy moduł ma jeden outcome,
- na dole kryterium sukcesu.

### Slajd SWOT

Układ:

- 2x2,
- każda ćwiartka ma kod `S/W/O/T`, tytuł i jedno zdanie,
- zagrożenie lub najważniejsze ryzyko może mieć czerwoną regułę.

### Slajd końcowy

Powinien domykać tezę, nie być generycznym "Dziękuję".

Struktura:

- jednozdaniowa konkluzja,
- kwota lub decyzja,
- co finansowanie / decyzja umożliwia,
- krótki finał.

## 10. UI layout patterns

### Dashboard operacyjny

Dobry dla narzędzi QA, B2B, analityki i monitoringu.

Struktura:

- topbar z nazwą produktu i statusem środowiska,
- lewa kolumna: filtry lub lista scenariuszy,
- prawa większa część: szczegóły, tabela, wykres, logi,
- brak hero sekcji.

### Widok szczegółu

Struktura:

- tytuł + metadane,
- pozioma reguła,
- 2-kolumnowy układ: treść główna + panel statusu,
- audit trail jako tabela lub timeline.

### Widok raportu

Struktura:

- nagłówek z identyfikatorem raportu,
- sekcja summary,
- tabela kroków,
- dowody jako miniatury lub linki,
- statusy bez kolorowego chaosu.

## 11. Motion i interakcje

Animacje powinny być krótkie i użytkowe.

- Hover: zmiana koloru tekstu lub linii, nie duży ruch.
- Focus: wyraźny outline.
- Loading: prosta linia, spinner tylko jeśli musi być.
- Przejścia: `120-180ms`.
- Nie używaj parallaxu, pływających kształtów ani dużych mikroanimacji w narzędziach roboczych.

```css
:root {
  --motion-fast: 120ms;
  --motion-base: 180ms;
}

.interactive {
  transition:
    color var(--motion-fast) ease,
    border-color var(--motion-fast) ease,
    background-color var(--motion-fast) ease;
}
```

## 12. Dostępność

Minimalne reguły:

- Tekst główny minimum `14px` w UI.
- Kontrast tekstu głównego na bieli minimum WCAG AA.
- Czerwony nie może być jedynym nośnikiem znaczenia.
- Focus states muszą być widoczne.
- Tabele muszą mieć nagłówki.
- Wykresy powinny mieć podpis lub alternatywny opis.
- Nie używaj tekstu w obrazach, jeśli ma być edytowalny albo dostępny.

## 13. Checklist dla UI

Przed oddaniem ekranu sprawdź:

- Czy layout trzyma 8px spacing i kolumny?
- Czy główna akcja jest oczywista bez dekoracji?
- Czy czerwony akcent oznacza coś konkretnego?
- Czy nie ma kart w kartach?
- Czy tabele i formularze mają czytelne stany?
- Czy na mobile układ redukuje kolumny zamiast ściskać tekst?
- Czy tekst mieści się w kontenerach?
- Czy focus keyboard jest widoczny?
- Czy komponenty wyglądają jak narzędzie pracy, a nie landing page?

## 14. Checklist dla prezentacji

Przed eksportem sprawdź:

- Czy każdy slajd ma jeden główny komunikat?
- Czy żaden tekst nie wychodzi poza pole?
- Czy wszystkie wykresy mają poprawne punkty przecięcia i etykiety?
- Czy footery są dyskretne i nie powtarzają zbędnego brandingu?
- Czy tabele są czytelne na zrzucie 1280x720?
- Czy czerwony akcent występuje oszczędnie?
- Czy źródła, podpisy i metadane nie dominują nad treścią?
- Czy slajdy mają różny rytm: cover, proces, tabela, wykres, timeline, SWOT?
- Czy prezentacja działa fullscreen bez elementów nawigacji?

## 15. Minimalny CSS startowy

```css
:root {
  --color-bg: #ffffff;
  --color-ink: #0b0b0b;
  --color-muted: #5f6673;
  --color-subtle: #9aa0aa;
  --color-line: #e8e8e8;
  --color-soft: #f5f5f5;
  --color-accent: #ff3b30;
  --color-positive: #10b981;

  --font-sans: "Plus Jakarta Sans", "Inter", Arial, sans-serif;
  --font-mono: "Space Grotesk", "IBM Plex Mono", monospace;

  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 24px;
  --space-6: 32px;
  --space-7: 48px;
  --space-8: 64px;
  --space-9: 80px;
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  background: var(--color-bg);
  color: var(--color-ink);
  font-family: var(--font-sans);
}

h1, h2, h3, h4, p {
  margin: 0;
}

h1 {
  font-size: clamp(44px, 6vw, 76px);
  line-height: 0.98;
  font-weight: 800;
  letter-spacing: 0;
}

h2 {
  font-size: clamp(32px, 4vw, 52px);
  line-height: 1.06;
  font-weight: 800;
  letter-spacing: 0;
}

p {
  font-size: 15px;
  line-height: 1.55;
  color: var(--color-muted);
}

.kicker {
  font-family: var(--font-mono);
  font-size: 12px;
  letter-spacing: 2px;
  color: var(--color-accent);
  text-transform: uppercase;
  font-weight: 700;
}

.grid-12 {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: var(--space-6);
}

.rule-box {
  border-top: 2px solid var(--color-ink);
  padding-top: var(--space-4);
}

.rule-box.is-accent {
  border-top-color: var(--color-accent);
}
```

## 16. Czego unikać

- Gradientowych hero sekcji.
- Dekoracyjnych kropek, blobów i orbów bez funkcji.
- Nadmiaru cieni i kart.
- Długich akapitów na slajdzie.
- Kolorowych badge'y dla każdej kategorii.
- Zbyt małych tabel.
- Wykresów bez jasnego progu, osi lub tezy.
- Slajdów będących screenshotem zamiast edytowalnej treści.
- Powtarzania logotypu lub nazwy projektu w każdym możliwym miejscu.
- Dopisywania źródeł i podpisów większych niż właściwa treść.

## 17. Szybki wzorzec decyzyjny

Jeśli nie wiesz, jak zaprojektować element, wybierz najpierw:

1. Czy to informacja, akcja, status czy dekoracja?
2. Jeśli dekoracja, usuń.
3. Jeśli informacja, wyrównaj do siatki.
4. Jeśli akcja, daj prosty przycisk lub ikonę z tooltipem.
5. Jeśli status, użyj tekstu monospace i małego markera.
6. Jeśli dane, użyj tabeli lub prostego wykresu.
7. Jeśli nadal wygląda pusto, zwiększ hierarchię typograficzną zamiast dodawać ozdobę.

