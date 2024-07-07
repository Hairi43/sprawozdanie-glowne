Główna baza danych
------------------

Model fizyczny głównej bazy danych
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: main_database_file.png

Główna baza danych przechowuje dane o zarejestrowanych klientach, ich adresach (każdy klient może mieć więcej niż jeden dom/mieszkanie), adresach pocztowych oznaczających miasta i kody pocztowe,liczniku, który jest przypisany do każdego adresu (liczniki są w relacji jeden do jednego z adresami klientów, tzw. jeden licznik może być przypisany pod jeden adres), odczytach z danego licznika (jest to relacja jeden do wielu, ponieważ każdy licznik ma swoją historię odczytów), domokrążców, którzy te liczniki sprawdzają oraz historię miejsc liczników, w których przebywały.
