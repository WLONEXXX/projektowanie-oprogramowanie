Elektro-Bud, analiza wymagań
Analiza wymagań dla systemu zarządzania magazynem hurtowni materiałów elektrycznych i budowlanych, opracowana na podstawie nagrania rozmowy z klientem oraz dokumentu z opisem potrzeb klienta.
1. Wymagania funkcjonalne
1. FR-01 Logowanie użytkownika. System powinien umożliwiać użytkownikowi zalogowanie się przy użyciu indywidualnych danych dostępowych.
2. FR-02 Logowanie kartą identyfikacyjną. System powinien umożliwiać logowanie za pomocą karty lub numeru ID pracownika.
3. FR-03 Indywidualne konta użytkowników. Każdy pracownik powinien posiadać własne konto. System nie powinien dopuszczać współdzielenia jednego konta przez wiele osób.
4. FR-04 Zarządzanie kontami. Administrator powinien móc tworzyć, edytować i dezaktywować konta użytkowników.
5. FR-05Nadawanie ról i uprawnień. Administrator powinien móc przypisać użytkownikowi rolę określającą jego uprawnienia.
6. FR-06Reset hasła. Administrator powinien móc zresetować hasło użytkownika.
7. FR-07 Dodawanie produktu. Kierownik powinien móc dodać produkt, podając: kod EAN, nazwę, kategorię, cenę oraz miejsce przechowywania.
8. FR-08 Edycja produktu. Kierownik powinien móc zmienić dane produktu.
9. FR-09 Wyszukiwanie po kodzie EAN. System powinien umożliwiać wyszukanie produktu po kodzie EAN.
10. FR-10 Wyszukiwanie po nazwie. System powinien umożliwiać wyszukanie produktu po nazwie lub jej fragmencie.
11. FR-11 Wyszukiwanie po innych kryteriach. System powinien umożliwiać wyszukanie produktu także po kategorii oraz lokalizacji.
12. FR-12 Wyświetlanie lokalizacji i ceny. System powinien wyświetlać dla produktu jego miejsce przechowywania oraz cenę.
13. FR-13 Podgląd stanu magazynowego. System powinien przechowywać aktualną ilość każdego produktu w magazynie, a kierownik powinien móc przeglądać stany magazynowe.
14. FR-14 Rejestracja przyjęcia towaru. Magazynier powinien móc zarejestrować przyjęcie towaru. Przyjęcie zwiększa stan magazynowy.
15. FR-15 Rejestracja wydania towaru. Magazynier powinien móc zarejestrować wydanie towaru. Wydanie zmniejsza stan magazynowy.
16. FR-16 Blokada wydania ponad stan. System nie powinien pozwolić na wydanie większej liczby sztuk produktu, niż jest dostępne w magazynie.
17. FR-17 Obsługa równoczesnych operacji. System powinien poprawnie obsłużyć sytuację, gdy dwóch pracowników wykonuje operację na tym samym produkcie w tym samym czasie. Stan magazynowy musi pozostać prawidłowy.
18. FR-18 Historia operacji. System powinien zapisywać każdą operację magazynową wraz z informacją: jaki produkt, w jakiej ilości, kto ją wykonał i kiedy.
19. FR-19 Przeglądanie historii. Kierownik powinien móc przeglądać historię operacji magazynowych.
20. FR-20 Raporty magazynowe. Kierownik powinien móc generować raporty dotyczące magazynu. Dokładny zakres raportów nie został jeszcze ustalony przez klienta i wymaga doprecyzowania.
21. FR-21 Kontrola uprawnień. System powinien udostępniać funkcje zgodnie z rolą użytkownika. Kierownik nie ma dostępu do administracji kontami, a magazynier nie dodaje produktów, nie przegląda stanów, historii ani raportów.
2. Wymagania niefunkcjonalne
1. NFR-01 Wydajność, wyszukiwanie. System powinien zwracać wynik wyszukiwania produktu wraz z lokalizacją i ceną w czasie nie dłuższym niż 2 sekundy w typowych warunkach pracy. Oczekiwany czas reakcji to około 1 do 2 sekund, bez długiego oczekiwania.
2. NFR-02 Wydajność, operacje magazynowe. Zapis przyjęcia lub wydania towaru powinien trwać nie dłużej niż 2 sekundy.
3. NFR-03 Bezpieczeństwo, konta. Każdy użytkownik powinien posiadać unikalne konto. System nie może pozwalać na pracę kilku osób na jednym koncie.
4. NFR-04 Bezpieczeństwo, hasła. Hasła powinny być przechowywane w postaci zaszyfrowanej, a ich minimalna długość powinna wynosić 8 znaków.
5. NFR-05 Kontrola dostępu. System powinien rozróżniać 3 role. Uprawnienia muszą być sprawdzane po stronie serwera, a nie tylko ukrywane w interfejsie.
6. NFR-06 Spójność danych. Operacje zmieniające stan magazynowy powinny być wykonywane niepodzielnie, tak aby stan produktu nigdy nie był ujemny ani niezgodny z historią operacji, także przy równoczesnej pracy co najmniej 3 użytkowników.
7. NFR-07 Dostępność. System powinien być dostępny w godzinach pracy magazynu, z dostępnością co najmniej 99% w tym czasie.
8. NFR-08 Sposób korzystania. Interfejs powinien być prosty i czytelny: układ prostych bloków z opisem, a podstawowe operacje powinny być osiągalne w maksymalnie 3 kliknięciach. Użytkownicy nie są informatykami.
9. NFR-09 Śledzenie operacji. Historia operacji nie może być edytowana ani usuwana przez zwykłych użytkowników.
10. NFR-10 Dostęp spoza magazynu. Kierownik powinien mieć dostęp do informacji o magazynie także poza stanowiskiem w magazynie, na przykład z innego komputera przez sieć. Dostęp ten wymaga uwierzytelnienia i kontroli uprawnień jak w wymaganiach dotyczących kont i kontroli dostępu.
Wartości liczbowe w wymaganiach niefunkcjonalnych to założenia analityka, ponieważ klient nie podał konkretnych liczb. Należy je potwierdzić z klientem. Zakres raportów również wymaga doprecyzowania.
3. Aktorzy
Magazynier. Rola: Pracownik magazynu, na co dzień obsługujący towar. Działania: Logowanie, wyszukiwanie produktów, sprawdzanie lokalizacji i ceny, rejestrowanie przyjęć i wydań towaru.
Kierownik. Rola: Osoba nadzorująca magazyn, ma szersze uprawnienia niż magazynier. Działania: Wszystko, co magazynier, a dodatkowo: przeglądanie stanów magazynowych, dodawanie i edycja produktów, przeglądanie historii operacji, korzystanie z raportów. Nie zarządza kontami.
Administrator. Rola: Osoba odpowiedzialna za konta i dostęp do systemu. Działania: Logowanie, tworzenie i dezaktywacja kont, nadawanie ról i uprawnień, resetowanie haseł.
