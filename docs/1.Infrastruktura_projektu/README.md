Opis projektu i produktu
====



1. Infrastruktura projektu
----

###Projekt:

Przedmiotem projektu jest przeglądarka internetowa `NAZWA`.

###Cel projektu i obszar zastosowania:

Produkt umożliwiać będzie szybkie, bezpieczne i ekfektywne przeglądanie zasobów internetowych z pełną obsługą multimediów, stanowiąc doskonałe rozwiązanie dla wszystkich internautów bez względu na stopień ich zaawansowania. 
Zarówno dla osób starszych jak i młodych interfejs będzie intuicyjny i przejrzysty, oferując przy tym cieszący oko wygląd.
Dzięki obsłudze szerokiej gamy multimediów i rozmaitych plików przeglądarka zadowoli najbardziej wymagających klientów.
Dodatkowym zadaniem projektu jest dostarczenie klientom przeglądarki, która będzie kompatybilna z najnowszymi technologiami (tj. najnowsze jQuery czy w przyszłości html6).

###Rynek:

Klientami naszego produktu są wszyscy, ktorzy pragną bezpiecznie i efektywnie przeglądać zasoby internetowe. 
Jedynymi wymaganiami są:
* podstawowa umiejętność obsługi komputera.
* umiejętność czytania. 
* znajomość języka angielskiego lub polskiego.
* sprawny wzrok. (nie przwidujemy wersji dla niewidomych)

###Współpracujące systemy:

Nasz produkt współpracuje z większością popularnych systemów operacyjnych takich jak:
* Mac OS
* Windows
* Linux Ubuntu/Fedora/RedHat/CentOS

2. Organizacja zespołu projektu
----

Prace prowadzone są w wynajętym biurze w jednym miejscu. W razie potrzeb jest możliwa także praca zdalna.

Osoby, które tworzą ten projekt:

| Pseudonim     | Rola          | Doświadczenie   | Praca Zdalna |  
|:-------------:|:-------------:|:---------------:|:-------:|
| mmiszy   | programista | Duże | Nie |
| Bplotka     | programista      |   Średnie | Nie |
| nicra | programista      |  Duże | Nie |
| klayer88 | programista | Małe | Nie |
| graficzex | frontend | Duże | Nie |
| @itgg2 | analityk IT | Średnie | Tak | 


3. Komunikacja w zespole
----

###Organizacja spotkań:

Jako że projekt jest wytwarzany metodyką `zwinną` (agile) to krótkie spotkania występują codziennie o 10:00 w systemie "scrum".

Co tydzień spotykamy się także na tzw. `Architecture meeting`, aby uzgodnić sprawy dotyczące architektury produktu, czy nowych rozwiązań.

Wszystkie spotkania odbywają się w biurze, jednak możliwe jest dołączenie do nich za pomocą wideokonferencji.

###Komunikacja:

Komunikacja może odbywać się na wiele różnych sposobów. W zależności od priorytetu rozmowy oraz sytuacji:
* Komunikacja osobista w biurze
* Komunikator 
* Mail
* Telefonicznie (Tylko w razie nagłych spraw)

###Komunikacja z klientem:

Projekt jest produktem typu OpenSource istniejącym na serwisie [GitHub] (https://github.com/RPI-2014/RPI_2014_projekt), zatem klienci i użytkownicy mogą bardzo łatwo zgłaszać sprawy, problemy lub defekty dotyczące projektu na: [GitHub issues](https://github.com/RPI-2014/RPI_2014_projekt/issues)

###Kontakt:

Aby skontaktować się z osobą z tego zespołu wystarczy znaleźć jej profil na serwisie GitHub: `https://github.com/pseudonim`

W tym miejszu znajduje się sposób komunikacji z daną osobą.

4. Dokumentacja
----

###Schemat nazewnictwa plików

Pliki dokumentacji znajdują się w katalogu `docs`.

Każdy kolejny raport powinien znaleźć się w osobnym podfolderze w pliku `README.md`, zgodnie z szablonem dokumentu projektu.

Jeżeli informacje, które mają znaleźć się w danym raporcie są zbyt obszerne dopuszczalne jest przeniesienie ich do osobnych plików w tym samym katalogu, pod warunkiem dodania bezpośrednich odnośników do nich w pliku `README.md`.

Przykładowe drzewo projektu:

```
/
├── README.md
├── docs
│   ├── 1.Infrastruktura_projektu
│   │   ├── README.md
│   │   └── instrukcja_rebase.md
│   ├── 2.Rejestr_produktu_i_rejestr_sprintu
│   │   └── README.md
│   └── ...
└── src
    └── ...
```

###Szablon dokumentu projektu

Przykładowy szablon dokumentu (formatowanie Markdown):

```
Tytuł raportu
===

Część 1. raportu
---

###Nagłówek pierwszy

Treść akapitu...

[odnośnik](http://example.com/)

Lista:

* jeden
* dwa
  * 2,5
* trzy


###Nagłówek drugi

Dalsza treść...


Część 2. raportu
---

Dalsza treść...

```

###Sposób tworzenia nowych wersji plików

Do tworzenia nowych wersji plików wykorzystywany jest system wersjonowania (VCS) GIT. Repozytorium trzymane jest na GitHubie, więcej informacji o sposobie pracy z nim znajduje się [tutaj](#5-wspo%CC%81%C5%82dzielenie-dokumento%CC%81w-i-kodu).

Osobą odpowiedzialną za porządek w dokumentacji jest **Michał Miszczyszyn**.


5. Współdzielenie dokumentów i kodu
----

###Repozytorium

Kod źródłowy oraz dokumentacja trzymane są w repozytorium na git na GitHubie: https://github.com/RPI-2014/RPI_2014_projekt

Projekt jest Open Source, a więc każda osoba ma możliwość przeglądania zawartości repozytorium.

Osobą odpowiedzialną za konfigurację i utrzymanie głównego repozytorium jest **Michał Miszczyszyn**.

###Wprowadzania zmian

**Aby pracować nad projektem trzeba wykonać fork tego repozytorium na swoje konto.**

Poleca się pracę lokalnie na osobnym branchu:

```
git remote add upstream git@github.com:RPI-2014/RPI_2014_projekt.git`
git checkout master
git pull --rebase upstream master
git checkout -b NAZWA_BRANCHA
```

Po zakończeniu wprowadzania zmian lokalnie, należy wykonać commit i push do swojego forka, a następnie wystawić pull-request do odpowiedniego brancha głównego repozytorium. **Ważne jest, aby pull request składał się wyłącznie z jednego commita i zawierał krótki, ale tręściwy opis wprowadzanych zmian.** [Instrukcja łączenia commitów w gicie](instrukcja_rebase.md).


6. Narzędzia
----

Aby usprawnić proces tworzenia oprogramowania wykorzystujemy w naszym projekcie następujące narzędzia: 

###Narzędzia wspomagające komunikacje:

* Komunikator (np. Skype)
* e-mail
* serwis GitHub (m.in. GitHub issues)

###Narzędzia wspomagające modelowanie:

* MS Visio

###Narzędzia wspomagające tworzenie kodu:

* Eclipse 
* Git

###Narzędzia wspomagające testowanie i kontrole nad defektami:

* Bugzilla
* Google Test Framework (Unit testy)

###Narzędzia wspomagające tworzenie dokumentacji:

* MS Office
* Edytory tekstu
* PDF Reader