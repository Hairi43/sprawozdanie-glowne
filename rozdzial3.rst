Opis funkcji pobierających informacje z bazy danych
---------------------------------------------------

Wstęp
~~~~~
Poniżej opisane funkcje są dostępne dla użytkowników z uprawnieniami administratora. Można z nich skorzystać po uruchomieniu pliku aplikacja_administratora.py oraz wybraniu odpowiednich opcji.

Pobieranie użytkowników z bazy danych
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
W celu sprawdzenia danych o konkretnej osobie możemy po uruchomieniu pliku aplikacja_administratora.py użyć opcji 3. podpisanej jako wyszukiwanie danych o wybranej osobie. 
Po wpisaniu imienia, nazwiska oraz peselu zapytanie SQL wyszukuje wszystkie informacje zapisane poniżej o konkretnej osobie i wypisuje je na ekranie. 

Zapytanie łączy kilka tabel:
klienci: zawiera podstawowe informacje o kliencie (imię, nazwisko, PESEL).
adres_klienta: zawiera szczegóły adresu klienta (ulica, numer budynku, numer mieszkania).
adres_pocztowy: zawiera kod pocztowy i miejscowość.
liczniki: zawiera informacje o licznikach przypisanych do klienta.
historia_licznika: zawiera informacje o historii liczników (data założenia, data usunięcia).
odczyty_licznika: zawiera odczyty liczników (zużycie, data odczytu).

Plik wykonujący opisaną funkcję nazywa się "wyszukiwanie_w_bazie.py".

Raport o domokrążcach
~~~~~~~~~~~~~~~~~~~~~
Generuje raport w postaci wykresu o ilości sprawdzonych liczników przez każdego z domokrążców.
Aby wygenerować wykres trzeba użyć opcji 2 w menu admnistratora.

Poniżej przedstawione jest działanie trzech funkcji odpowiedzialnych za pobieranie, przetwarzanie danych dotyczących domokrążców oraz generowanie raportu graficznego ich wydajności.

Pierwsza z nich:

1. Pobiera imię i nazwisko domokrążcy.
2. Liczy liczbę wpisów dokonanych przez każdego domokrążcę (count(odczyty_licznika.id_domokrazcy)).
3. Grupuje wyniki według imienia i nazwiska.
4. Sortuje wyniki malejąco według liczby wpisów.

Druga:
Przekształca dane pobrane z bazy w bardziej przystępną formę do generowania wykresu.
Tworzy listę ilość wpisów, zawierającą liczbę wpisów dla każdego domokrążcy oraz krotkę z przetworzonymi danymi.

Trzecia:
Zmienia ustawienia wykresu tak, żeby był najczytelniejszy oraz na podstawie danych dostarczonych z drugiej funkcji generuje wykres słupkowy, który przedstawia liczbę wpisów dokonanych przez domokrążców.
