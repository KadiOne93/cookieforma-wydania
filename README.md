# cookieforma — wydania

Program do projektowania foremek i stempli do ciastek do druku 3D. Z obrazu, napisu albo opisu słownego powstaje komplet: **foremka**, która wycina kształt ciastka, i **stempel z ogranicznikiem**, który odciska w cieście detale na zadaną głębokość. Wynik to ZIP z plikami STL i 3MF gotowymi do Bambu Studio.

To repozytorium zawiera tylko wydania programu dla Windows. **Pobieranie:** [najnowsze wydanie](../../releases/latest) → plik `cookieforma-<wersja>-instalator.exe`.

## Wymagania

| | Minimum | Zalecane |
|---|---|---|
| System | Windows 10 22H2 / Windows 11, 64-bit | Windows 11 |
| Karta graficzna (do generowania z opisu) | NVIDIA, 12 GB VRAM (generowanie wolniejsze) | NVIDIA, 16 GB VRAM |
| Sterownik NVIDIA | 580 lub nowszy | najnowszy |
| RAM | 16 GB | 32 GB |
| Dysk | ok. 40 GB wolnego | SSD |

Bez karty NVIDIA program działa w całości poza zakładką „Generuj”, czyli poza generowaniem z opisu. Obrazy, napisy, podgląd 3D, eksport i biblioteka projektów działają na każdym komputerze.

## Instalacja

1. Pobierz instalator z [najnowszego wydania](../../releases/latest) i uruchom go. Program instaluje się tylko dla Twojego konta i nie wymaga uprawnień administratora.
2. Instalator nie jest podpisany certyfikatem, więc Windows może pokazać okno **„System Windows ochronił ten komputer”**. Kliknij **„Więcej informacji”**, a potem **„Uruchom mimo to”**.
3. Jeśli chcesz sprawdzić, że plik jest tym z wydania, porównaj jego sumę SHA-256 z sumą podaną w opisie wydania (i w pliku `.sha256` obok instalatora). W PowerShellu:

   ```
   Get-FileHash .\cookieforma-0.2.0-instalator.exe
   ```

4. Przy pierwszym uruchomieniu program sprawdza kartę graficzną i wolne miejsce, a potem pobiera ComfyUI, Ollamę i modele do generowania z opisu: ok. 30 GB z ich oficjalnych źródeł (GitHub, Hugging Face, rejestr Ollamy). Pobieranie można przerwać i wznowić. Model FLUX.1 [dev] ma licencję niekomercyjną — kreator pokazuje ją przed pobraniem.

Po instalacji program działa bez internetu. Połączenia z siecią wymaga tylko wczytanie obrazu z adresu w internecie.

## Gdzie są pliki

| Co | Gdzie |
|---|---|
| program | `%LOCALAPPDATA%\Programs\cookieforma` |
| projekty | `Dokumenty\cookieforma\projekty` |
| ComfyUI, Ollama i modele | folder wybrany w kreatorze, domyślnie `%LOCALAPPDATA%\cookieforma\dane` |
| logi | `%LOCALAPPDATA%\cookieforma\logi` (menu „Program” → „Otwórz folder logów”) |

## Odinstalowanie

Ustawienia Windows → **Aplikacje** → cookieforma → Odinstaluj. Dezinstalator pyta, czy usunąć też ComfyUI, Ollamę i modele. **Projektów nie usuwa nigdy** — na koniec podaje folder, w którym zostały.
