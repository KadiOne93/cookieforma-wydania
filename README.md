# cookieforma — aktualizacje

Aktualizacje programu cookieforma dla Windows. **Pakiet aktualizacji działa tylko na zainstalowanym programie** — bez niego kończy się komunikatem i niczego nie instaluje.

Zainstalowana cookieforma sprawdza to repozytorium raz na dobę. Gdy jest nowsza wersja, w nagłówku programu pojawia się odnośnik „Nowa wersja · Pobierz”, który otwiera stronę wydania.

## Jak zaktualizować

1. Zamknij cookieformę.
2. Pobierz `cookieforma-<wersja>-aktualizacja.exe` z [najnowszego wydania](../../releases/latest) i uruchom go.
3. Pakiet nie jest podpisany certyfikatem, więc Windows może pokazać okno **„System Windows ochronił ten komputer”** → **„Więcej informacji”** → **„Uruchom mimo to”**. Sumę SHA-256 pliku możesz porównać z podaną w opisie wydania: `Get-FileHash .\cookieforma-<wersja>-aktualizacja.exe` w PowerShellu.

Aktualizacja wymienia tylko program. Projekty, ustawienia, ComfyUI i modele zostają. Jeśli nowa wersja korzysta z nowszych plików do generowania z opisu, program przy pierwszym uruchomieniu zaproponuje dociągnięcie tylko tego, co się zmieniło.
