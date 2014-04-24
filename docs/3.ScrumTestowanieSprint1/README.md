3. Scrum: Testowanie sprint 1
===

* Michał Miszczyszyn (137347)
* Bartłomiej Płotka (137378)
* Marcin Piątkowski (137371)

1. O projekcie i sprincie
---

### O produkcie

Przedmiotem projektu jest przeglądarka internetowa Firesocks.

Produkt umożliwiać będzie szybkie, bezpieczne i ekfektywne przeglądanie zasobów internetowych z pełną obsługą multimediów, stanowiąc doskonałe rozwiązanie dla wszystkich internautów bez względu na stopień ich zaawansowania czy wiek.

### Zakres sprintu

Stworzenie wersji MVP produktu (Minimum viable product).

2. Środowisko testowe
---

* **Komputer**: MacBook Pro 13-inch, Late 2011
* **System Operacyjny**: OS X 10.9.2
* **Procesor**: 2.8 GHz Intel Core i7
* **Pamięć RAM**: 8 GB 1333 MHz DDR3
* **Karta graficzna**: Intel HD Graphics 3000 512 MB
* **Kompilator**: Apple LLVM version 5.1 (clang-503.0.40) (based on LLVM 3.4svn)

3. Przypadki testowe
---

| ID        | Funkcja testowana           | Nazwa testu  | 
| :------------:|:-------------:| :-----:| 
| 50   | Est: 8h - Wykonanie podstawowego interfejsu użytkownika - walidacja inputów- Parent: #9  | Test: Sprawdznie walidatora dla inputów - pole wpisania lokalizacji instalacji |
<table>
    <thead>
        <tr>
            <th>Opis testu</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
            1) Starting situation:<br/>
Brak zainstalowanego programu na systemie, pobrany instalator<br/>
2) Test Steps:<br/>
<br/>
- Włączenie aplikacji instalacyjnej<br/>
- Postępowanie zgodnie z krokami<br/>
- Wybranie prostej, domyślnej instalacji<br/>
- Wybranie miejsca zapisu programu na dysku (ale użycue inputu)<br/>
- Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki)<br/>
- Próba zostawienia pustego inputu<br/>
- Próba wpisania samych cyfr "3242"<br/>
- Próba wpisania "Programs" (względną ścieżka - błędna)<br/>
- Próba wpisania "D://Programs" (instniejącej ścieżki)<br/>
- Śledzenie paska postępu<br/>
- Po zakończeniu, sprawdzenie czy aplikacja zapisała się w wybranym miejscu<br/>
- Sprawdzenie, czy zainstalowały się tylko wybrane moduły<br/>
- Włączenie aplikacji<br/>
3) Expected situation:<br/>
Instalor się otwiera, pozwala na wpisanie lokalizacji.
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki) -> komunikat "nie ma takiej ściezki"
Próba zostawienia pustego inputu -> komunikat "wpisz lokalizacje!"
Próba wpisania samych cyfr "3242" -> komunikat "nie ma takiej ściezki"
Próba wpisania "Programs" (względną ścieżka - błędna) -> komunikat "nie ma takiej ścieżki"
Próba wpisania "D://Programs" (instniejącej ścieżki) -> brak komunikatu aplikacja przechodzi do instalacji Aplikacja zapisana w poprawnym miejscu na dysku, otwiera się poprawnie.. Pasek postępu płynnie pokazywał postęp instalacji
            </td>
        </tr>
    </tbody>
</table>

---

| ID        | Funkcja testowana           | Nazwa testu  | 
| :------------:|:-------------:| :-----:| 
| 49   | Est: 8h - Wykonanie podstawowego interfejsu użytkownika - walidacja inputów- Parent: #9  | Test: Sprawdznie walidatora dla inputów - pole wpisania adresu http/https |
<table>
    <thead>
        <tr>
            <th>Opis testu</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
            1) Starting situation:<br/>
Włączona aplikacja<br/>
2) Test Steps:<br/>
- Wpisujemy adres "dziwny adres"<br/>
- Wpisujemy adres "http://dziwny adres"<br/>
- Wpisujemy adres "http://dziwny_adres"<br/>
- Wpisujemy adres "10.122.34.123"<br/>
- Wpisujemy adres "10.122.34.270"<br/>
<br/>
3) Expected situation:<br/>
- adres "dziwny adres"  -> ten napis zostanie wpisany do domyślnej wyszukiwarki<br/>
- adres "http://dziwny adres" -> ten napis zostanie wpisany do domyślnej wyszukiwarki<br/>
- adres "http://dziwny_adres" -> po tym adresie pójdzie request.(strona not found)<br/>
- adres "10.122.34.123" -> po tym adresie pójdzie request (strona not found)<br/>
- adres "10.122.34.270" -> ten napis zostanie wpisany do domyślnej wyszukiwarki (nie ma takiego adresu ip)<br/>
            </td><br/>
        </tr>
    </tbody>
</table>

---

| ID        | Funkcja testowana           | Nazwa testu  | 
| :------------:|:-------------:| :-----:| 
| 48   | Est: 5h - Wykonanie możliwości ściągania plików - zarządzanie plikami - Parent: #32  |Test: Sprawdzenie modułu ściągania plików, zbyt duży plik |
<table>
    <thead>
        <tr>
            <th>Opis testu</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
            1) Starting situation:<br/>
Włączona aplikacja, brak plików ściąganych wcześniej, miejsce na dysku jest ograniczone do 3GB<br/>
2) Test Steps:<br/>
- Wpisz istniejący adres strony, który ściągnie duży plik (powyżej 4GB). Miejsca na dysku jest 3GB.<br/>
- Po przeczytaniu komunikatu że plik sie nie miesci wybierz inną lokalizacje dla pliku (tam gdzie sie zmieści)<br/>
- W momencie postępu 100% spróbuj otworzyć plik<br/>
- Wejdź do zarządzania pobieranymi plikami<br/>
- Sprawdź plik.<br/>
<br/>
3) Expected situation:<br/>
Przy rozpoczęciu pobierania (!) program zauważy że nie ma miejsca odpowiedniego na ten plik. Pokaże interfejst, w którym można wpisać nową lokalizacje. Element zacznie się ściągać, po dłuższym czasie będzie możliwość jego otwarcia., W module zarządznia plikami będzie data pobrania, jego wielkość i nazwa.
            </td>
        </tr>
    </tbody>
</table>

---

| ID        | Funkcja testowana           | Nazwa testu  | 
| :------------:|:-------------:| :-----:| 
| 50   | Est: 8h - Wykonanie podstawowego interfejsu użytkownika - walidacja inputów- Parent: #9  | Test: Sprawdznie walidatora dla inputów - pole wpisania lokalizacji instalacji |
<table>
    <thead>
        <tr>
            <th>Opis testu</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
            1) Starting situation:<br/>
Brak zainstalowanego programu na systemie, pobrany instalator<br/>
2) Test Steps:<br/>
<br/>
Włączenie aplikacji instalacyjnej<br/>
Postępowanie zgodnie z krokami<br/>
Wybranie prostej, domyślnej instalacji<br/>
Wybranie miejsca zapisu programu na dysku (ale użycue inputu)<br/>
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki)<br/>
Próba zostawienia pustego inputu<br/>
Próba wpisania samych cyfr "3242"<br/>
Próba wpisania "Programs" (względną ścieżka - błędna)<br/>
Próba wpisania "D://Programs" (instniejącej ścieżki)<br/>
Śledzenie paska postępu<br/>
Po zakończeniu, sprawdzenie czy aplikacja zapisała się w wybranym miejscu<br/>
Sprawdzenie, czy zainstalowały się tylko wybrane moduły<br/>
Włączenie aplikacji<br/>
3) Expected situation:<br/>
Instalor się otwiera, pozwala na wpisanie lokalizacji.
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki) -> komunikat "nie ma takiej ściezki"
Próba zostawienia pustego inputu -> komunikat "wpisz lokalizacje!"
Próba wpisania samych cyfr "3242" -> komunikat "nie ma takiej ściezki"
Próba wpisania "Programs" (względną ścieżka - błędna) -> komunikat "nie ma takiej ścieżki"
Próba wpisania "D://Programs" (instniejącej ścieżki) -> brak komunikatu aplikacja przechodzi do instalacji Aplikacja zapisana w poprawnym miejscu na dysku, otwiera się poprawnie.. Pasek postępu płynnie pokazywał postęp instalacji
            </td>
        </tr>
    </tbody>
</table>

---

| ID        | Funkcja testowana           | Nazwa testu  | 
| :------------:|:-------------:| :-----:| 
| 50   | Est: 8h - Wykonanie podstawowego interfejsu użytkownika - walidacja inputów- Parent: #9  | Test: Sprawdznie walidatora dla inputów - pole wpisania lokalizacji instalacji |
<table>
    <thead>
        <tr>
            <th>Opis testu</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
            1) Starting situation:<br/>
Brak zainstalowanego programu na systemie, pobrany instalator<br/>
2) Test Steps:<br/>
<br/>
Włączenie aplikacji instalacyjnej<br/>
Postępowanie zgodnie z krokami<br/>
Wybranie prostej, domyślnej instalacji<br/>
Wybranie miejsca zapisu programu na dysku (ale użycue inputu)<br/>
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki)<br/>
Próba zostawienia pustego inputu<br/>
Próba wpisania samych cyfr "3242"<br/>
Próba wpisania "Programs" (względną ścieżka - błędna)<br/>
Próba wpisania "D://Programs" (instniejącej ścieżki)<br/>
Śledzenie paska postępu<br/>
Po zakończeniu, sprawdzenie czy aplikacja zapisała się w wybranym miejscu<br/>
Sprawdzenie, czy zainstalowały się tylko wybrane moduły<br/>
Włączenie aplikacji<br/>
3) Expected situation:<br/>
Instalor się otwiera, pozwala na wpisanie lokalizacji.
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki) -> komunikat "nie ma takiej ściezki"
Próba zostawienia pustego inputu -> komunikat "wpisz lokalizacje!"
Próba wpisania samych cyfr "3242" -> komunikat "nie ma takiej ściezki"
Próba wpisania "Programs" (względną ścieżka - błędna) -> komunikat "nie ma takiej ścieżki"
Próba wpisania "D://Programs" (instniejącej ścieżki) -> brak komunikatu aplikacja przechodzi do instalacji Aplikacja zapisana w poprawnym miejscu na dysku, otwiera się poprawnie.. Pasek postępu płynnie pokazywał postęp instalacji
            </td>
        </tr>
    </tbody>
</table>

---

| ID        | Funkcja testowana           | Nazwa testu  | 
| :------------:|:-------------:| :-----:| 
| 50   | Est: 8h - Wykonanie podstawowego interfejsu użytkownika - walidacja inputów- Parent: #9  | Test: Sprawdznie walidatora dla inputów - pole wpisania lokalizacji instalacji |
<table>
    <thead>
        <tr>
            <th>Opis testu</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
            1) Starting situation:<br/>
Brak zainstalowanego programu na systemie, pobrany instalator<br/>
2) Test Steps:<br/>
<br/>
Włączenie aplikacji instalacyjnej<br/>
Postępowanie zgodnie z krokami<br/>
Wybranie prostej, domyślnej instalacji<br/>
Wybranie miejsca zapisu programu na dysku (ale użycue inputu)<br/>
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki)<br/>
Próba zostawienia pustego inputu<br/>
Próba wpisania samych cyfr "3242"<br/>
Próba wpisania "Programs" (względną ścieżka - błędna)<br/>
Próba wpisania "D://Programs" (instniejącej ścieżki)<br/>
Śledzenie paska postępu<br/>
Po zakończeniu, sprawdzenie czy aplikacja zapisała się w wybranym miejscu<br/>
Sprawdzenie, czy zainstalowały się tylko wybrane moduły<br/>
Włączenie aplikacji<br/>
3) Expected situation:<br/>
Instalor się otwiera, pozwala na wpisanie lokalizacji.
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki) -> komunikat "nie ma takiej ściezki"
Próba zostawienia pustego inputu -> komunikat "wpisz lokalizacje!"
Próba wpisania samych cyfr "3242" -> komunikat "nie ma takiej ściezki"
Próba wpisania "Programs" (względną ścieżka - błędna) -> komunikat "nie ma takiej ścieżki"
Próba wpisania "D://Programs" (instniejącej ścieżki) -> brak komunikatu aplikacja przechodzi do instalacji Aplikacja zapisana w poprawnym miejscu na dysku, otwiera się poprawnie.. Pasek postępu płynnie pokazywał postęp instalacji
            </td>
        </tr>
    </tbody>
</table>

---

| ID        | Funkcja testowana           | Nazwa testu  | 
| :------------:|:-------------:| :-----:| 
| 50   | Est: 8h - Wykonanie podstawowego interfejsu użytkownika - walidacja inputów- Parent: #9  | Test: Sprawdznie walidatora dla inputów - pole wpisania lokalizacji instalacji |
<table>
    <thead>
        <tr>
            <th>Opis testu</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
            1) Starting situation:<br/>
Brak zainstalowanego programu na systemie, pobrany instalator<br/>
2) Test Steps:<br/>
<br/>
Włączenie aplikacji instalacyjnej<br/>
Postępowanie zgodnie z krokami<br/>
Wybranie prostej, domyślnej instalacji<br/>
Wybranie miejsca zapisu programu na dysku (ale użycue inputu)<br/>
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki)<br/>
Próba zostawienia pustego inputu<br/>
Próba wpisania samych cyfr "3242"<br/>
Próba wpisania "Programs" (względną ścieżka - błędna)<br/>
Próba wpisania "D://Programs" (instniejącej ścieżki)<br/>
Śledzenie paska postępu<br/>
Po zakończeniu, sprawdzenie czy aplikacja zapisała się w wybranym miejscu<br/>
Sprawdzenie, czy zainstalowały się tylko wybrane moduły<br/>
Włączenie aplikacji<br/>
3) Expected situation:<br/>
Instalor się otwiera, pozwala na wpisanie lokalizacji.
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki) -> komunikat "nie ma takiej ściezki"
Próba zostawienia pustego inputu -> komunikat "wpisz lokalizacje!"
Próba wpisania samych cyfr "3242" -> komunikat "nie ma takiej ściezki"
Próba wpisania "Programs" (względną ścieżka - błędna) -> komunikat "nie ma takiej ścieżki"
Próba wpisania "D://Programs" (instniejącej ścieżki) -> brak komunikatu aplikacja przechodzi do instalacji Aplikacja zapisana w poprawnym miejscu na dysku, otwiera się poprawnie.. Pasek postępu płynnie pokazywał postęp instalacji
            </td>
        </tr>
    </tbody>
</table>

---

| ID        | Funkcja testowana           | Nazwa testu  | 
| :------------:|:-------------:| :-----:| 
| 50   | Est: 8h - Wykonanie podstawowego interfejsu użytkownika - walidacja inputów- Parent: #9  | Test: Sprawdznie walidatora dla inputów - pole wpisania lokalizacji instalacji |
<table>
    <thead>
        <tr>
            <th>Opis testu</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
            1) Starting situation:<br/>
Brak zainstalowanego programu na systemie, pobrany instalator<br/>
2) Test Steps:<br/>
<br/>
Włączenie aplikacji instalacyjnej<br/>
Postępowanie zgodnie z krokami<br/>
Wybranie prostej, domyślnej instalacji<br/>
Wybranie miejsca zapisu programu na dysku (ale użycue inputu)<br/>
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki)<br/>
Próba zostawienia pustego inputu<br/>
Próba wpisania samych cyfr "3242"<br/>
Próba wpisania "Programs" (względną ścieżka - błędna)<br/>
Próba wpisania "D://Programs" (instniejącej ścieżki)<br/>
Śledzenie paska postępu<br/>
Po zakończeniu, sprawdzenie czy aplikacja zapisała się w wybranym miejscu<br/>
Sprawdzenie, czy zainstalowały się tylko wybrane moduły<br/>
Włączenie aplikacji<br/>
3) Expected situation:<br/>
Instalor się otwiera, pozwala na wpisanie lokalizacji.
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki) -> komunikat "nie ma takiej ściezki"
Próba zostawienia pustego inputu -> komunikat "wpisz lokalizacje!"
Próba wpisania samych cyfr "3242" -> komunikat "nie ma takiej ściezki"
Próba wpisania "Programs" (względną ścieżka - błędna) -> komunikat "nie ma takiej ścieżki"
Próba wpisania "D://Programs" (instniejącej ścieżki) -> brak komunikatu aplikacja przechodzi do instalacji Aplikacja zapisana w poprawnym miejscu na dysku, otwiera się poprawnie.. Pasek postępu płynnie pokazywał postęp instalacji
            </td>
        </tr>
    </tbody>
</table>

---

| ID        | Funkcja testowana           | Nazwa testu  | 
| :------------:|:-------------:| :-----:| 
| 50   | Est: 8h - Wykonanie podstawowego interfejsu użytkownika - walidacja inputów- Parent: #9  | Test: Sprawdznie walidatora dla inputów - pole wpisania lokalizacji instalacji |
<table>
    <thead>
        <tr>
            <th>Opis testu</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
            1) Starting situation:<br/>
Brak zainstalowanego programu na systemie, pobrany instalator<br/>
2) Test Steps:<br/>
<br/>
Włączenie aplikacji instalacyjnej<br/>
Postępowanie zgodnie z krokami<br/>
Wybranie prostej, domyślnej instalacji<br/>
Wybranie miejsca zapisu programu na dysku (ale użycue inputu)<br/>
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki)<br/>
Próba zostawienia pustego inputu<br/>
Próba wpisania samych cyfr "3242"<br/>
Próba wpisania "Programs" (względną ścieżka - błędna)<br/>
Próba wpisania "D://Programs" (instniejącej ścieżki)<br/>
Śledzenie paska postępu<br/>
Po zakończeniu, sprawdzenie czy aplikacja zapisała się w wybranym miejscu<br/>
Sprawdzenie, czy zainstalowały się tylko wybrane moduły<br/>
Włączenie aplikacji<br/>
3) Expected situation:<br/>
Instalor się otwiera, pozwala na wpisanie lokalizacji.
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki) -> komunikat "nie ma takiej ściezki"
Próba zostawienia pustego inputu -> komunikat "wpisz lokalizacje!"
Próba wpisania samych cyfr "3242" -> komunikat "nie ma takiej ściezki"
Próba wpisania "Programs" (względną ścieżka - błędna) -> komunikat "nie ma takiej ścieżki"
Próba wpisania "D://Programs" (instniejącej ścieżki) -> brak komunikatu aplikacja przechodzi do instalacji Aplikacja zapisana w poprawnym miejscu na dysku, otwiera się poprawnie.. Pasek postępu płynnie pokazywał postęp instalacji
            </td>
        </tr>
    </tbody>
</table>

---

| ID        | Funkcja testowana           | Nazwa testu  | 
| :------------:|:-------------:| :-----:| 
| 50   | Est: 8h - Wykonanie podstawowego interfejsu użytkownika - walidacja inputów- Parent: #9  | Test: Sprawdznie walidatora dla inputów - pole wpisania lokalizacji instalacji |
<table>
    <thead>
        <tr>
            <th>Opis testu</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
            1) Starting situation:<br/>
Brak zainstalowanego programu na systemie, pobrany instalator<br/>
2) Test Steps:<br/>
<br/>
Włączenie aplikacji instalacyjnej<br/>
Postępowanie zgodnie z krokami<br/>
Wybranie prostej, domyślnej instalacji<br/>
Wybranie miejsca zapisu programu na dysku (ale użycue inputu)<br/>
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki)<br/>
Próba zostawienia pustego inputu<br/>
Próba wpisania samych cyfr "3242"<br/>
Próba wpisania "Programs" (względną ścieżka - błędna)<br/>
Próba wpisania "D://Programs" (instniejącej ścieżki)<br/>
Śledzenie paska postępu<br/>
Po zakończeniu, sprawdzenie czy aplikacja zapisała się w wybranym miejscu<br/>
Sprawdzenie, czy zainstalowały się tylko wybrane moduły<br/>
Włączenie aplikacji<br/>
3) Expected situation:<br/>
Instalor się otwiera, pozwala na wpisanie lokalizacji.
Próba wpisania znaków "X://Programs" ("nie istniejącej ścieżki) -> komunikat "nie ma takiej ściezki"
Próba zostawienia pustego inputu -> komunikat "wpisz lokalizacje!"
Próba wpisania samych cyfr "3242" -> komunikat "nie ma takiej ściezki"
Próba wpisania "Programs" (względną ścieżka - błędna) -> komunikat "nie ma takiej ścieżki"
Próba wpisania "D://Programs" (instniejącej ścieżki) -> brak komunikatu aplikacja przechodzi do instalacji Aplikacja zapisana w poprawnym miejscu na dysku, otwiera się poprawnie.. Pasek postępu płynnie pokazywał postęp instalacji
            </td>
        </tr>
    </tbody>
</table>


4. Wyniki testów
---

![](1.png)
![](2.png)
![](3.png)
![](4.png)
![](5.png)
![](6.png)
