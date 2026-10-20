# Specyfikacja: Edytor map i fal (Tower Defense)

## 1. Metadane
- Wersja: 0.0,1
- Status: Wersja robocza
- Data modyfikacji: 20-10-2026

## 2. Kontekst i cel 
Moduł edytora pozwala graczom na tworzenie własnych plansz oraz definiowanie fal przeciwników. Utworzone poziomy następnie trafiają do bazy danych poziomów utworzonych przez graczy.

## 3. Cele i antycele
Cele:
- Graficzny kreator bazowany na siatce
- Interfejs do konfigurowania fal przeciwników i odstępów czasowych
- Walidacja ciągłości ścieżki od spawnera do bazy
- Eksport mapy do pliku o prostej strukturze
Antycele:
- Edytor statystyk i wyglądu wież i przeciwników dla gracza (te elementy są z góry ustalone w kodzie gry)

## 4. 
- Gracz wybiera docelowy rozmiar mapy, stawia elementy "Spawner" i "Baza", łączy je ścieżką, która musi być ciągła. Gracz dodaje dodatkowe przeszkody.
- Gracz dodaje wybraną ilość fal oraz je definiuje. Każda fala musi mieć określone ilości danych przeciwników, czas między przeciwnikami i nagrodę. Gracz ustawia czas między falami oraz ilość zdrowia gracza i ilość początkową złota.
- Gracz klika przycisk "Testuj" i system sprawdza czy "Spawner" i "Baza" są połączone ścieżką, jeśli nie to zwracany jest błąd.

## 5. Wymagania funkcjonalne
1. System wymusza istnienie dokładnie jednego Spawnera i jednej Bazy
2. Każda fala definiuje: rodzaj przeciwników, ilość, czas między spawnem i nagrodę.
3. Poziom definiuje ilość zdrowia, złoto początkowe i czas między falami
4. Mapa nie zostanie zapisana jeżeli walidacja ścieżki się nie powiedzie.

## 6. Wymagania niefunkcjonalne
1. Przejście z trybu edycji do trybu testowania musi zająć mniej niż 2 sekundy
