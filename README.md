# Transformer-From-Scratch (PyTorch)

To repozytorium to mój własny, „ręcznie robiony” silnik Transformera, zbudowany w PyTorchu. Zamiast korzystać z gotowych bibliotek, postanowiłem zbudować każdy element architektury od podstaw, żeby zrozumieć, jak to wszystko faktycznie działa pod maską.

## O co w tym chodzi?

Większość ludzi używa bibliotek typu transformers od HuggingFace, nie wiedząc, co dzieje się w środku. Ten projekt to moja próba rozłożenia tej technologii na części pierwsze. Zaimplementowałem tutaj:

* Multi-Head Attention: Mechanizm, dzięki któremu model „patrzy” na zdanie z kilku różnych perspektyw naraz.
* Residual Connections: „Skróty”, dzięki którym informacje nie zanikają po przejściu przez wiele warstw.
* Layer Normalization: Stabilizator, który sprawia, że matematyka modelu nie „odlatuje w kosmos” przy głębszym przetwarzaniu.
* Architektura modułowa: Cały model jest zamknięty w czytelnej strukturze danych (tabeli), co ułatwia zarządzanie wagami.

## Jak to działa?

Model składa się z 5 warstw, z których każda posiada własne wagi (macierze Wq, Wk, Wv). Dane wędrują przez model w ten sposób:

1. Attention: Model wyciąga kontekst ze słów.
2. Add & Norm: Dodajemy wynik do oryginalnych danych i wyrównujemy wartości (stabilizacja).
3. Powtórka: Proces powtarza się 5 razy, czyniąc model coraz „mądrzejszym” w kontekście analizowanego zdania.

## Technologie

* Python 3.x
* PyTorch

## Jak uruchomić?

1. Sklonuj repozytorium.
2. Upewnij się, że masz zainstalowany PyTorch.
3. Odpal główny skrypt.

Ten projekt jest częścią mojej nauki fundamentów Deep Learningu.
