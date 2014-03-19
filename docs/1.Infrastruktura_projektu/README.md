Opis projektu i produktu
====



1. Infrastruktura projektu
----
(nazwa projektu/produktu, adresowany problem, obszar zastosowania, rynek, użytkownicy i ich problemy, cel i zakres produktu, inne współpracujące systemy)


2. Organizacja zespołu projektu
----
(kto jest w zespole, role, doświadczenie, umiejętności, praca w rozproszeniu czy w jednym miejscu, można dodać fikcyjne osoby do zespołu, ale zespół nie powinien być większy niż 7 osób)


3. Komunikacja w zespole
----
(sposoby komunikacji, środki komunikacji, organizacja spotkań, komunikacja z otoczeniem projektu – z klientem, użytkownikami, dane kontaktowe osób w zespole)


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
(narzędzia wspierające obszary z punktów 3, 4 i 5, narzędzia wspomagające organizację projektu, modelowanie, tworzenie dokumentów, wytwarzanie i testowanie systemu)