# MLOps Projekt

Numer albumu: 99789

## Porównanie narzędzi do zarządzania środowiskiem i danymi

| Narzędzie | Zmierzony czas instalacji | Plik definicji | Sposób odtworzenia środowiska | Kiedy stosować / Różnice |
| --- | --- | --- | --- | --- |
| venv | ~10-20 s | requirements.txt | python -m venv .venv && .venv\Scripts\activate && pip install -r requirements.txt | Standardowe, lekkie projekty w Pythonie. |
| uv | ~4-8 s | pyproject.toml / requirements.txt | uv venv && uv pip install -r requirements.txt | Szybka, codzienna praca w Pythonie. |
| conda | ~30-60 s | environment.yml | conda env create -f environment.yml | Złożone projekty, pakiety C/C++ i CUDA. |
| DVC | N/A | .dvc (np. housing.csv.dvc) | dvc pull | Wersjonuje duże dane i modele. Git odpowiada za kod, DVC za pliki danych. |


## Ćwiczenie nr 3 - Odtworzenie repozytorium partnera

Sklonowano repozytorium: `https://github.com/Nela-cat/mlops-projekt`

### Wymagane komendy:
1. `git clone https://github.com/Nela-cat/mlops-projekt`
2. `uv venv`
3. `.venv\Scripts\activate`
4. `uv pip install -r requirements.txt`
5. `dvc pull`

### Napotkane problemy:
- Odtworzenie środowiska za pomocą `uv` przebiegło bezproblemowo dzięki plikowi `requirements.txt`.
- W przypadku DVC, pobranie danych zależy od konfiguracji remote (wymagany dostęp do lokalnego storage lub chmury).