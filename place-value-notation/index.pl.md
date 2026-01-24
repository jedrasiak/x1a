---
id: 019b9fd7-9af1-71e7-a96b-1c265cb93705
title: Systemy pozycyjne
slug: systemy-pozycyjne
draft: false
links:
- "[Systemy liczbowe](/numeral-systems/index.pl.md?label=parent)"
---

# Systemy pozycyjne

// metafora z licznikiem kilometrów

Systemy pozycyjne (dziesiętny, binarny, ósemkowy, szesnastkowy) różnią się od siebie zestawem cyfr, których używa się do zapisywania liczb:
- dziesiętny: od 0 do 9 (10 cyfr),
- binarny: 0 lub 1 (2 cyfry),
- ósemkowy: od 0 do 7 (8 cyfr),
- szesnastkowy: od 0 do 9 plus A, B, C, D, E, F (16 cyfr).

> Ilość cyfr wykorzystywanych w danym systemie nazywa się **podstawą systemu**.

W systemach pozycyjnych wartość zapisanej liczby zależy nie tylko od wartości znaków użytych do jej zapisu, ale także od umiejscowienia poszczególnych cyfr w ciągu znaków. Cyfra leżąca najbardziej na lewo jest najbardziej znacząca (ma największą wartość).

### Przekształcanie liczb na system dziesiętny

Aby obliczyć wartość liczby zapisanej w różnych systemach (przekształcić na znany nam system dziesiętny) należy:
- określić pozycję danej cyfry w liczbie ($n$)
- każdą cyfrę pomnożyć przez podstawę podniesioną do potęgi $n-1$
- zsumować wyniki

_Formalny wzór:_

...

_Przykłady:_

Widoczne przy każdej liczbie indeksy w nawiasach wskazują na podstawę, która została wybrana do zapisu. Jeśli w jednym dokumencie występują różne systemy liczbowe to podawanie podstaw jest konieczne - jak widać, ta sama liczba w różnych systemach reprezentuje zupełnie inną wartość.

$5342_{(10)} = 5\times10^3 + 3\times10^2 + 4\times10^1 + 2\times10^0$

$5342_{(8)} = 5\times8^3 + 3\times8^2 + 4\times8^1 + 2\times8^0 = 2786_{(10)}$

$5342_{(16)} = 5\times16^3 + 3\times16^2 + 4\times16^1 + 2\times16^0 = 21314_{(10)}$

### Przekształcanie liczb dziesiętnych na inne systemy

...