# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Pitagoras Go!** - edukacyjna strona internetowa do nauki matematyki dla 8 klasy szkoły podstawowej.
Autor: Adam Kasprzak, 8C, Społeczna Jedynka im. św. Urszuli Ledóchowskiej w Poznaniu.

## Development

Otwórz `index.html` w przeglądarce - brak zależności i procesu budowania.

## Project Structure

```
pitagorasgo/
├── index.html              # Strona główna (hub nawigacyjny)
├── gra.html                # Gra edukacyjna (samodzielny plik)
├── uklad-wspolrzednych.html
├── os-liczbowa.html
├── podzielnosc-liczb.html
├── zaokraglanie.html
├── css/
│   └── style.css           # Wspólne style dla strony i podstron
└── CLAUDE.md
```

## Architecture

### Strona główna (index.html)
- Hub z 4 kafelkami tematycznymi
- Link do gry
- Responsywny design (mobile-friendly)

### Podstrony tematyczne
Każda podstrona (`uklad-wspolrzednych.html`, `os-liczbowa.html`, `podzielnosc-liczb.html`, `zaokraglanie.html`) zawiera:
- Sekcję teorii (4-5 paragrafów)
- Przykładowe zadania z rozwiązaniami
- System quizów (3 poziomy trudności × 5 pytań)

Quiz system:
- Pytania jednokrotnego wyboru (4 odpowiedzi)
- Natychmiastowy feedback (✅/❌)
- Wynik + losowy komentarz na końcu

### Gra (gra.html)
Samodzielny plik HTML (~4000 linii) z wbudowanymi stylami i JavaScript:
- 3 poziomy trudności (EASY, MEDIUM, HARD)
- System pytań matematycznych z diagramami SVG
- Power-upy i Hall of Fame (localStorage)

## Styling

Wspólne style w `css/style.css`:
- Kolorystyka: niebieski/turkusowy (#2980b9, #1a5276, #5dade2)
- CSS variables dla kolorów i akcentów
- Responsywność: breakpointy 768px i 480px

## Language

Cała treść po polsku. Kod mieszany (polskie komentarze, angielskie nazwy zmiennych).
