---
id: 019b8b41-fc6c-768d-b2a8-e04e88418f50
title: Systemy liczbowe
slug: systemy-liczbowe
draft: false
links:
- "[Matematyka](/mathematics/index.pl.md?label=parent)"
---

# Systemy liczbowe

**System liczbowy to zbiór reguł zapisywania liczb. Korzystając z różnych systemów liczbowych tę samą wartość można zapisać na wiele sposobów, korzystając z różnych zestawów symboli (cyfr) i zasad ich stosowania.**

Aby lepiej zobrazować różnice pomiędzy systemami liczbowymi spróbujmy na kilka sposobów zapisać odpowiedź na wielkie pytanie o życie, wszechświat i całą resztę:
- system jedynkowy: ||||\ ||||\ ||||\ ||||\ ||||\ ||||\ ||||\ ||||\ ||
- system rzymski: XLII
- system dziesiętny: 42
- system binarny: 101010
- system ósemkowy: 52
- system szesnastkowy: 2A

## Systemy addytywne

W systemach addytywnych liczby tworzy się poprzez dodawanie kolejnych symboli do ciągu znaków. Najlepiej obrazuje to system jedynkowy, w którym każdy dodany "patyczek" zwiększa zapisaną liczbę o 1. Zestaw dostępnych znaków składa się wyłącznie z pionowej kreski. Czasami - dla łatwiejszego liczenia - 4 następujące po sobie pionowe kreski przedziela się piątą.

## Systemy pozycyjne

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