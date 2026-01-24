---
id: 019bf231-775d-76e6-ae82-584c0e79cafa
title: Zmiana nazwy repozytoriów
slug: zmiana-nazwy-repozytoriw
draft: false
links:
- "[Git i GitHub](/git-github/index.pl.md?label=parent)"
---

# Zmiana nazwy repozytoriów

## Przegląd

Zmiana nazwy repozytorium obejmuje zarówno zmianę nazwy lokalnego repozytorium Git, jak i w razie potrzeby - zdalnego repozytorium na platformach takich jak GitHub. Proces ten wymaga starannej koordynacji, aby uniknąć zerwania istniejących odnośników i URL-i do klonowania.

## Zmiana nazwy lokalnego repozytorium Git

Aby zmienić nazwę lokalnego repozytorium Git, wystarczy zmienić nazwę katalogu zawierającego folder `.git`:

```bash
mv stara-nazwa-repo nowa-nazwa-repo
```

Ta operacja jest bezpieczna i nie wpływa na historię Git ani konfigurację. Należy jednak zaktualizować wszelkie skrypty lub konfiguracje odwołujące się do starej ścieżki.

## Zmiana nazwy repozytorium GitHub

### Kroki

1. **Przejdź do ustawień repozytorium**
   - Otwórz repozytorium na GitHub
   - Kliknij zakładkę "Settings" (Ustawienia)
   - Znajdź pole "Repository name" (Nazwa repozytorium) w sekcji General (Ogólne)

2. **Wprowadź nową nazwę**
   - Wpisz nową nazwę repozytorium
   - Kliknij przycisk "Rename" (Zmień nazwę)

3. **Ważne uwagi**
   - GitHub automatycznie przekierowuje żądania ze starej nazwy na nową
   - Jednak to przekierowanie może nie działać w nieskończoność
   - Wszystkie istniejące klony, forki i pull requesty będą nadal działać
   - Linki do issue i odniesienia są automatycznie aktualizowane

### Aktualizacja lokalnych klonów

Po zmianie nazwy repozytorium na GitHub, zaktualizuj URL zdalnego repozytorium w lokalnym repozytorium:

```bash
# Sprawdź aktualny URL zdalnego repozytorium
git remote -v

# Zaktualizuj URL zdalnego repozytorium
git remote set-url origin https://github.com/uzytkownik/nowa-nazwa-repo.git

# Lub dla SSH
git remote set-url origin git@github.com:uzytkownik/nowa-nazwa-repo.git

# Zweryfikuj zmianę
git remote -v
```

### Aktualizacja ze starej nazwy repozytorium

Jeśli sklonowałeś repozytorium przed zmianą nazwy, możesz również zaktualizować nazwę lokalnego katalogu:

```bash
# Zmień nazwę lokalnego katalogu
cd ..
mv stara-nazwa-repo nowa-nazwa-repo
cd nowa-nazwa-repo

# Zaktualizuj URL zdalnego repozytorium (jak pokazano powyżej)
git remote set-url origin https://github.com/uzytkownik/nowa-nazwa-repo.git
```

## Dobre praktyki

1. **Komunikacja**: Poinformuj członków zespołu i współpracowników przed zmianą nazwy
2. **Dokumentacja**: Zaktualizuj całą dokumentację odwołującą się do starej nazwy
3. **Pipeline CI/CD**: Zaktualizuj konfiguracje ciągłej integracji i wdrażania
4. **Zależności**: Sprawdź, czy inne projekty odwołują się do tego repozytorium i zaktualizuj je
5. **Lokalne klony**: Upewnij się, że wszyscy członkowie zespołu zaktualizowali swoje lokalne klony
6. **Zakładki**: Zaktualizuj zakładki w przeglądarce i konfiguracje projektów w IDE

## Typowe problemy

### Zerwane linki
- Linki do konkretnych plików lub commitów używające starej nazwy repozytorium mogą przestać działać
- Zaktualizuj odpowiednio linki w dokumentacji i wiki

### Submoduły
Jeśli zmienione repozytorium jest używane jako submoduł w innych projektach:
```bash
# Zaktualizuj plik .gitmodules
vim .gitmodules  # Zmień URL na nową nazwę repozytorium

# Zsynchronizuj i zaktualizuj
git submodule sync
git submodule update --init --recursive
```

### Chronione gałęzie
Reguły chronionych gałęzi są zachowywane podczas zmiany nazwy, ale wszelkie systemy zewnętrzne odwołujące się do nazw gałęzi przez pełną ścieżkę repozytorium będą wymagały aktualizacji.

## Źródła

- Oficjalna dokumentacja Git: https://git-scm.com/docs
- Dokumentacja GitHub o zmianie nazwy repozytoriów: https://docs.github.com/en/repositories/creating-and-managing-repositories/renaming-a-repository