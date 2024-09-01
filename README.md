# Ocena Ryzyka Kredytowego - Prognozowanie Zdolności Kredytowej Klientów Banku

## Opis Projektu

Celem tego projektu jest prognozowanie zdolności kredytowej klientów banku na podstawie danych ze zbioru **German Credit Data**. Zdolność kredytowa jest kluczowym wskaźnikiem używanym przez banki do oceny ryzyka związanego z udzielaniem kredytów. Poprawne prognozowanie tej zdolności pozwala na minimalizowanie ryzyka finansowego i poprawę decyzji kredytowych.

W projekcie zastosowano kilka popularnych algorytmów klasyfikacyjnych:
- **RandomForestClassifier**: Wybrany jako model bazowy ze względu na jego zdolność do radzenia sobie z dużą ilością cech oraz na tendencję do unikania przeuczenia dzięki zastosowaniu techniki "ensemble learning".
- **Logistic Regression**: Szybki i prosty algorytm klasyfikacyjny, który dobrze radzi sobie z binarnymi problemami.
- **Gradient Boosting Classifier**: Skuteczny algorytm, który tworzy silny model klasyfikacyjny z szeregu słabych klasyfikatorów.
- **XGBoost Classifier**: Zaawansowana wersja Gradient Boosting, zoptymalizowana pod kątem szybkości i wydajności.

## Zawartość Repozytorium

- `credit_risk_analysis.ipynb` - Główny notebook Jupyter zawierający pełną analizę danych, przetwarzanie danych, trening modelu, cross-validation oraz ocenę wyników.
- `german.data` - Zbiór danych użyty w projekcie, zawierający informacje o klientach banku. [Link do zbioru danych](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data)
- `README.md` - Plik zawierający opis projektu, jego cel oraz sposób uruchomienia.
- `requirements.txt` - Plik zawierający wszystkie zależności projektu.

## Wymagania

Aby uruchomić projekt, potrzebujesz następujących narzędzi i bibliotek:

- Python 3.x
- `pandas`
- `numpy`
- `scikit-learn`
- `xgboost`

Możesz zainstalować wymagane pakiety za pomocą polecenia:

```bash
pip install -r requirements.txt
```





## Instrukcje Uruchomienia

### Klonowanie repozytorium

Aby rozpocząć, sklonuj repozytorium na swoją lokalną maszynę. Użyj poniższych poleceń:

```bash
git clone <URL do Twojego repozytorium>
cd <nazwa folderu repozytorium>
```

### Instalacja zależności
Następnie zainstaluj wszystkie wymagane pakiety za pomocą pip. Wystarczy wykonać poniższe polecenie:

```bash
pip install -r requirements.txt
```

### Uruchomienie Jupyter Notebook
Aby rozpocząć analizę, otwórz plik notebooka credit_risk_analysis.ipynb:

```bash
jupyter notebook credit_risk_analysis.ipynb
```

### Trenowanie modeli
W notebooku przejdź przez kolejne komórki, aby:

- Załadować i przetworzyć dane.
- Wytrenować modele klasyfikacyjne.
- Ocenić ich wyniki.
## Przykłady Użycia

Po uruchomieniu projektu i wytrenowaniu modelu, możesz użyć go do prognozowania zdolności kredytowej dla nowych danych. Oto przykład:

```bash
# Załóżmy, że masz nowe dane w formie DataFrame
new_data = pd.DataFrame({
    'feature1': [value1],
    'feature2': [value2],
    ...
})

# Przewidywanie zdolności kredytowej
prediction = best_model.predict(new_data)
print(f"Predykcja zdolności kredytowej: {prediction}")
```
