# MLOps Projekt

Numer albumu: 99789

## Porównanie narzêdzi do zarz¹dzania œrodowiskiem i danymi

| Narzêdzie | Zmierzony czas instalacji | Plik definicji zale¿noœci | Sposób odtworzenia œrodowiska | Kiedy stosowaæ / Ró¿nice |
|---|---|---|---|---|
| **venv** | ~10-20 s | equirements.txt | python -m venv .venv <br> .venv\Scripts\activate <br> pip install -r requirements.txt | Standardowe, lekkie projekty w Pythonie bez z³o¿onych zale¿noœci C/C++. |
| **uv** | ~4-8 s (bardzo szybki) | pyproject.toml / equirements.txt | uv venv <br> uv pip install -r requirements.txt | Nowoczesny, ekstremalnie szybki mened¿er do codziennej pracy w Pythonie. |
| **conda** | ~30-60 s | environment.yml | conda env create -f environment.yml | Projekty wymagaj¹ce pakietów C/C++, bibliotek CUDA oraz z³o¿onego stosu naukowego. |
| **DVC** | N/A (zarz¹dzanie danymi) | .dvc (np. housing.csv.dvc) | dvc pull | **Co wersjonuje:** Du¿e pliki danych, artefakty i modele ML.<br>**Ró¿nica vs Git:** Git przechowuje kod Ÿród³owy i lekkie pliki-wskaŸniki (.dvc), natomiast DVC przechowuje w³aœciwe, ciê¿kie pliki w zewnêtrznym magazynie (remote). |
