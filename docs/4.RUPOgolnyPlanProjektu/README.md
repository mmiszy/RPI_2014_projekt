4. Metodyka RUP: Ogólny plan projektu 
===


* Michał Miszczyszyn (137347)
* Bartłomiej Płotka (137378)
* Marcin Piątkowski (137371)

1. O projekcie
---

Przedmiotem projektu jest przeglądarka internetowa Firesocks.

Produkt umożliwiać będzie szybkie, bezpieczne i efektywne przeglądanie zasobów internetowych z pełną obsługą multimediów, stanowiąc doskonałe rozwiązanie dla wszystkich internautów bez względu na stopień ich zaawansowania czy wiek.

2. Założenia planu
---

###Termin:
Projekt zaplanowano na wykonanie w ciągu kolejnych 35 tygodni, czas ten rozdysponowany jest na kolejne fazy RUP.

###Zespół:
| Imię i nazwisko     | Pseudonim | Rola        | Doświadczenie | Praca Zdalna |
|:-------------------:|:---------:|:-----------:|:-------------:|:------------:|
| Bartłomiej Koder    | Bplotka   | team lead   | Duże          | Nie          |
| Michał Koderski     | mmiszy    | programista | Duże          | Nie          |
| Marcin Kodoklep     | nicra     | programista | Duże          | Nie          |
| Kszysztof Lajer     | klayer88  | design & UX | Średnie       | Tak          |
| Jan Fotoszopski     | graficzex | front-end   | Duże          | Nie          |
| Sebastian Rynkowski | @itgg2    | analityk IT | Średnie       | Tak          | 

###Wyjściowy produkt:
Produktem wyjściowym będzie w pełni funkcjonalna przeglądarka internetowa dostępna dla użytkownika w postaci instalatora umożliwiającego instalację produktu na dysku.

3. Organizacja zespołu
---

| Rola                     | Imię i nazwisko                      |
|:------------------------:|:------------------------------------:|
| Kierownik projektu       | Bartłomiej Koder                     |
| Architekt oprogramowania | Michał Koderski                      |
| Analityk biznesowy       | Sebastian Rynkowski                  |
| Analityk systemowy       | Marcin Kodoklep                      |
| Specyfikujący wymagania  | Bartłomiej Koder                     |
| Projektant               | Kszysztof Lajer                      |
| Programista              | Marcin Kodoklep, Michał Koderski     |
| Integrator               | Michał Koderski                      |
| Kierownik testów         | Bartłomiej Koder                     |
| Analityk testów          | Marcin Kodoklep, Sebastian Rynkowski |
| Projektant testów        | Bartłomiej Koder                     |
| Tester                   | Marcin Kodoklep, Michał Koderski     |
| Grafik                   | Jan Fotoszopski, Kszysztof Lajer     |
| Inżynier procesu         | Michał Koderski                      |
| Specjalista ds. narzędzi | Marcin Kodoklep                      |
| Kontrolerzy jakości      | Michał Koderski, Bartłomiej Koder    |

4. Przebieg projektu (omówienie struktury projektu w czasie oraz przebiegu pracy realizowanej w projekcie) 
---

###Fazy i iteracje (podział na fazy zgodne z RUP oraz iteracje tych faz, dla każdej iteracji określenie celów i głównych produktów – artefaktów, kryteria akceptacji produktów danej fazy umożliwiające przejście do następnej fazy) 

* Inception
  * I1
    * Zdefiniowanie wizji
	* Zdefiniowanie zasięgu projektu
	* Zdefiniowanie architektury i narzędzi
	* Stworzenie biznesowych przypadków użycia (use case)
	* Stworzenie planu tworzenia oprogramowania
	* Przewidziane artefakty:
	  * Wizja systemu
	  * Przypadki użycia
	  * Lista przewidzianych ryzyk
	  * Plan tworzenia oprogramowania
	  * Plan iteracji
	* Kryteria akceptacji:
	  * Wizja jak i przypadki użycia pokrywają przewidywaną funkcjonalność
	  * Plan tworzenia oprogramowania pokrywa funkcjonalność i jest możliwy do zrealizowania
	  * Lista ryzyk pokrywa większość dających się przewidzieć problemów
	  * Wybrana jest architektura i narzędzia umożliwiające zrealizowanie projektu
* Elaboration
  * E1
    * Instalacja i testowanie architektury
	* Instalacja i testowanie narzędzi
	* Zweryfikowanie szczegółów wymagań
	* Przynajmniej częściowe zaimplementowanie przypadków użycia z wysokim priorytetem
	* Przewidziane artefakty:
	  * Zweryfikowana architektura i narzędzia
	  * Lista funkcjonalności zweryfikowana pod kątem możliwości architektury i narzędzi
	  * Częściowo zaimplementowane przypadki użycia z wysokim priorytetem
	* Kryteria akceptacji:
	  * Wybrane środki do stworzenia projektu są właściwe pod kątem planowanej funkcjonalności, bezpieczeństwa, łatwości używania jak i stabilności
	  * Dotychczasowa implementacja nie budzi zastrzeżeń i pozwala na rozwinięcie do pełnej funkcjonalności 
  * E2
    * Zmniejszenie ryzyka związanego z wybraną architekturą
	* Zakończenie instalacji i testów architektury oraz narzędzi
	* Przynajmniej częściowa implementacja dodatkowych przypadków użycia
	* Przewidziane artefakty:
	  * Gotowa architektura wraz z narzędziami, zminimalizowane ryzyko związane z ich użyciem
	  * Częściowo zaimplementowane dodatkowe przypadki użycia
	* Kryteria akceptacji:
	  * Architektura i narzędzia są gotowe do dalszych etapów, ich użycie nie wiąże się ze zbędnym ryzykiem
	  * Dotychczasowa implementacja nie budzi zastrzeżeń i pozwala na rozwinięcie do pełnej funkcjonalności 
* Construction
  * C1
    * Opisanie dodatkowych przypadków użycia
	* Zaprojektowanie dodatkowych podsystemów
	* Implementacja przypadków użycia i podsystemów
	* Integracja produktu i zweryfikowanie funkcjonalności i wymagań
	* Zaprojektowanie, wykonanie i analiza testów
	* Przewidziane artefakty:
	  * Kolejna wersja developerska oprogramowania
	  * Testy zaimplementowanych funkcjonalności
	* Kryteria akceptacji:
	  * Implementacja zaplanowanych przypadków użycia jest poprawna i pokrywa zaplanowaną funkcjonalność
	  * Przeprowadzone testy nie wykazują błędów bądź niedoróbek
  * C2 
    * Opisanie dodatkowych przypadków użycia
	* Implementacja przypadków użycia
	* Integracja produktu i zweryfikowanie funkcjonalności i wymagań
	* Zaprojektowanie, wykonanie i analiza testów
	* Przewidziane artefakty:
	  * Kolejna wersja developerska oprogramowania
	  * Testy zaimplementowanych funkcjonalności
	* Kryteria akceptacji:
	  * Implementacja zaplanowanych przypadków użycia jest poprawna i pokrywa zaplanowaną funkcjonalność
	  * Przeprowadzone testy nie wykazują błędów bądź niedoróbek
  * C3
    * Opisanie dodatkowych przypadków użycia
	* Implementacja przypadków użycia
	* Integracja produktu i zweryfikowanie funkcjonalności i wymagań
	* Zaplanowanie wersji beta projektu
	* Zaplanowanie i zaprojektowanie systemów pomocy
	* Zaprojektowanie, wykonanie i analiza testów
	* Przewidziane artefakty:
	  * Wersja beta oprogramowania
	  * Testy zaimplementowanych funkcjonalności
	* Kryteria akceptacji:
	  * Implementacja zaplanowanych przypadków użycia jest poprawna i pokrywa zaplanowaną funkcjonalność
	  * Przeprowadzone testy nie wykazują błędów bądź niedoróbek
	  * Wersja beta jest gotowa do dostarczenia do klienta
* Transition
  * T1
    * Dostarczenie wersji beta do klientów
	* Analiza feedbacku
	* Poprawianie błędów i niedoróbek
	* Dokończenie systemu pomocy i systemów pobocznych
	* Przygotowanie wersji do wydania
	* Dostarczenie do klienta
	* Przewidziane artefakty:
	  * Wersja beta poprawiona na podstawie feedbacku klientów
	  * Wersja gotowa do wydania
	* Kryteria akceptacji:
	  * Wszystkie błędy zauważone przez klientów zostały poprawione
	  * Aplikacja jest dostępna dla potencjalnych klientów
* Evolution
  * En
    * Analiza zauważonych błędów przez klientów bądź testerów
	* Poprawienie błędów
	* Przygotowanie kolejnej wersji
	* Dodanie aktualnej wersji do systemu aktualizacji
	* Przewidziane artefakty:
	  * Kolejna wersja poprawiona o zauważone błędy
	* Kryteria akceptacji:
	  * Wszystkie błędy zauważone przez klientów zostały poprawione
	  * Aplikacja jest dostępna dla potencjalnych klientów

### Wydania (lista wydań oprogramowania, zakładana data, typ wydania (demo, beta itp.)) 

### Harmonogram (określenie terminu rozpoczęcia i zakończenia faz i iteracji, diagram Gantta faz i iteracji projektu wykonany w narzędziu do harmonogramowania)







