# Raport projektu:

# 1. Wyniki Testowe i Treningowe: Prezentacja Osiągniętych Wyników

## Wprowadzenie
W raporcie przedstawiono wyniki analizy czterech modeli klasyfikacyjnych: Random Forest, Logistic Regression, Gradient Boosting oraz XGBoost, oraz najlepszy model uzyskany za pomocą GridSearchCV. Analiza obejmuje metryki takie jak dokładność, precyzja, recall i F1-score dla poszczególnych klas.

## Wyniki Modeli

### Random Forest
**Classification Report:**

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 1     | 0.78      | 0.81   | 0.79     | 141     |
| 2     | 0.49      | 0.44   | 0.46     | 59      |

- **Accuracy:** 0.70

### Logistic Regression
**Classification Report:**

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 1     | 0.75      | 0.87   | 0.81     | 141     |
| 2     | 0.50      | 0.32   | 0.39     | 59      |

- **Accuracy:** 0.705

### Gradient Boosting
**Classification Report:**

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 1     | 0.78      | 0.87   | 0.82     | 141     |
| 2     | 0.57      | 0.41   | 0.48     | 59      |

- **Accuracy:** 0.735

### XGBoost
**Classification Report:**

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.78      | 0.79   | 0.79     | 141     |
| 1     | 0.49      | 0.47   | 0.48     | 59      |

- **Accuracy:** 0.70

### Random Forest z GridSearchCV
**Classification Report:**

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.78      | 0.84   | 0.81     | 141     |
| 1     | 0.53      | 0.42   | 0.47     | 59      |

- **Accuracy:** 0.72

## Metryki

- **Precision (Precyzja)**: Odsetek prawidłowo klasyfikowanych pozytywnych przypadków spośród wszystkich przypadków zaklasyfikowanych jako pozytywne.
- **Recall (Czułość)**: Odsetek prawidłowo klasyfikowanych pozytywnych przypadków spośród wszystkich rzeczywistych pozytywnych przypadków.
- **F1-Score**: Średnia harmoniczna precyzji i czułości, która łączy te dwie metryki w jedną wartość.
- **Accuracy (Dokładność)**: Odsetek prawidłowo klasyfikowanych przypadków spośród wszystkich przypadków.

## Wnioski
- **Gradient Boosting** uzyskał najwyższą dokładność wynoszącą 0.735, co wskazuje na najlepszą ogólną wydajność modelu.
- **Logistic Regression** i **XGBoost** osiągnęły niższą dokładność, ale warto zwrócić uwagę na ich precyzję i recall w kontekście klasy 2.

# 2. Uzasadnienie Wyboru Techniki/Modelu

## Wybrane Techniki i Modele

### Random Forest
**Opis:**
Random Forest jest algorytmem ensamble, który buduje wiele drzew decyzyjnych podczas treningu i łączy ich wyniki, aby uzyskać bardziej stabilne i dokładne prognozy. Model ten jest znany z odporności na overfitting i zdolności do pracy z danymi o różnych właściwościach.

**Przewagi:**
- **Odporność na overfitting:** Random Forest jest mniej podatny na overfitting w porównaniu do pojedynczych drzew decyzyjnych.
- **Robustness:** Działa dobrze z dużymi zbiorami danych i jest odporny na szumy w danych.
- **Automatyczne ustalanie cech ważnych:** Model automatycznie ocenia ważność cech, co może pomóc w selekcji cech.

### Logistic Regression
**Opis:**
Logistic Regression jest prostym modelem liniowym używanym do klasyfikacji binarnej. Pomimo swojej prostoty, jest często skuteczny w zadaniach klasyfikacyjnych i może być stosowany jako punkt odniesienia do bardziej zaawansowanych modeli.

**Przewagi:**
- **Interpretowalność:** Wyniki są łatwe do zrozumienia, a współczynniki modelu bezpośrednio wskazują na wpływ cech na przewidywaną klasę.
- **Efektywność obliczeniowa:** Model jest szybki do trenowania i prognozowania, nawet na dużych zbiorach danych.
- **Podstawowe założenia:** Działa dobrze, gdy dane są liniowo separowalne.

### Gradient Boosting
**Opis:**
Gradient Boosting jest algorytmem ensamble, który buduje modele sekwencyjnie, gdzie każdy kolejny model koryguje błędy poprzedniego. Jest znany ze swojej wysokiej dokładności i skuteczności w różnych problemach klasyfikacyjnych.

**Przewagi:**
- **Wysoka dokładność:** Gradient Boosting często osiąga wyższe wyniki dokładności w porównaniu do innych modeli.
- **Elastyczność:** Może modelować złożone zależności między cechami.
- **Wykrywanie interakcji:** Skutecznie radzi sobie z interakcjami między cechami.

### XGBoost
**Opis:**
XGBoost (Extreme Gradient Boosting) jest ulepszoną wersją Gradient Boosting, która optymalizuje proces trenowania poprzez zaawansowane techniki, takie jak przycinanie drzew i regularyzacja. Jest szczególnie ceniony w nauce o danych.

**Przewagi:**
- **Wydajność:** XGBoost jest szybki zarówno w trenowaniu, jak i w prognozowaniu.
- **Skuteczność:** Często osiąga najlepsze wyniki w zawodach związanych z uczeniem maszynowym.
- **Zaawansowane funkcje:** Oferuje różne techniki regularyzacji, które pomagają w unikaniu overfittingu.

## Random Forest z GridSearchCV

Chociaż Gradient Boosting osiągnął nieco wyższą dokładność (0.735), model Random Forest z GridSearchCV również okazał się skuteczny, osiągając dokładność na poziomie 0.72. Dzięki optymalizacji hiperparametrów, model Random Forest został lepiej dostosowany do danych, co czyni go stabilnym i solidnym wyborem do pracy z danymi o złożonej strukturze. Wybór między tymi modelami może zależeć od dalszych czynników, takich jak interpretowalność wyników lub czas trenowania.
## Podsumowanie

- **Random Forest** i **Gradient Boosting** wyróżniły się wysoką dokładnością, ale Random Forest był bardziej stabilny.
- **Logistic Regression** i **XGBoost** oferują inne zalety, takie jak interpretowalność i wydajność, ale nie przewyższyły wyników Random Forest.
- **GridSearchCV** umożliwił znalezienie najlepszego modelu Random Forest, co potwierdziło, że technika ta była najbardziej efektywna w tym przypadku.

Wybór Random Forest z GridSearchCV jako najlepszego modelu opierał się na jego wysokiej dokładności oraz odporności na overfitting, co czyni go solidnym wyborem dla mojego zadania klasyfikacyjnego.


# 3. Strategia Podziału Danych

## Podział Danych

### Zestaw Treningowy (Training Set)
**Opis:**
Zestaw treningowy to część danych używana do nauki modelu. Model jest trenowany na podstawie tych danych, co oznacza, że parametry modelu są dostosowywane w celu minimalizacji błędu na tym zestawie. 

**Cel:**
- Umożliwienie modelowi nauki i dostosowania swoich parametrów do danych.
- Zapewnienie, że model jest w stanie znaleźć wzorce i zależności w danych.

### Zestaw Walidacyjny (Validation Set)
**Opis:**
Zestaw walidacyjny to część danych używana do optymalizacji hiperparametrów modelu i wyboru najlepszego modelu spośród kilku kandydatów. Model nie jest trenowany na tym zestawie, ale jest testowany, aby sprawdzić, jak dobrze radzi sobie z nowymi danymi.

**Cel:**
- Pomoc w doborze najlepszych hiperparametrów modelu.
- Monitorowanie wydajności modelu w celu uniknięcia overfittingu (dopasowania do danych treningowych).

### Zestaw Testowy (Test Set)
**Opis:**
Zestaw testowy to część danych, która nie jest używana podczas treningu ani walidacji modelu. Jest to ostateczny zbiór danych używany do oceny wydajności modelu po zakończeniu trenowania i optymalizacji.

**Cel:**
- Ostateczna ocena wydajności modelu na nieznanych danych.
- Sprawdzenie, jak dobrze model generalizuje do nowych, nieznanych przypadków.

## Strategia Podziału w Projekcie

W moim projekcie dane zostały podzielone na zestawy treningowy i testowy. Proces ten wyglądał następująco:

1. **Podział na Zestawy Treningowy i Testowy:**
   - **Zestaw Treningowy:** 80% danych. Używany do trenowania modeli i dostosowywania hiperparametrów.
   - **Zestaw Testowy:** 20% danych. Używany do ostatecznej oceny modeli.



 ```python
 from sklearn.model_selection import train_test_split

 X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
 ```

2. **Brak Zestawu Walidacyjnego:**
W tym projekcie nie został zastosowany osobny zestaw walidacyjny. Optymalizacja hiperparametrów oraz wybór najlepszego modelu zostały przeprowadzone przy użyciu techniki GridSearchCV w ramach zestawu treningowego.

  ```python
  from sklearn.model_selection import GridSearchCV

  grid_search_rf = GridSearchCV(pipeline_rf, param_grid, cv=5, scoring='accuracy')
  grid_search_rf.fit(X_train, y_train)

  ```


GridSearchCV wykorzystuje kroswalidację do oceny modeli na podstawie danych treningowych, co pozwala na optymalizację hiperparametrów bez potrzeby posiadania osobnego zestawu walidacyjnego.

# 4. Opis Danych Wejściowych

## 1. Tytuł
**Nazwa zbioru danych:** German Credit Data

## 2. Źródło Informacji
- **Autor:** Professor Dr. Hans Hofmann
- **Instytut:** Institut für Statistik und Ökonometrie
- **Uniwersytet:** Universität Hamburg
- **Wydział:** FB Wirtschaftswissenschaften
- **Adres:** Von-Melle-Park 5, 2000 Hamburg 13, Niemcy

## 3. Liczba Instancji
- **Liczba instancji:** 1000

## 4. Opis Zbioru Danych

### Oryginalny Zbiór Danych
- **Nazwa pliku:** `german.data`
- **Typ danych:** Categorical/Symbolic
- **Opis:** Zbiór danych zawiera atrybuty kategoryczne, które są w formie oryginalnej dostarczonej przez Prof. Hofmann. 

## 5. Liczba Atrybutów

### Zbiór Oryginalny
- **Liczba atrybutów:** 20
  - **Atrybuty numeryczne:** 7
  - **Atrybuty kategoryczne:** 13

## 6. Atrybuty

### Oryginalne Atrybuty
- **Atrybuty numeryczne:** Zawierają atrybuty takie jak saldo konta, historia kredytowa, cel kredytu, itp.
- **Atrybuty kategoryczne:** Zawierają atrybuty takie jak stan cywilny, długość zatrudnienia, posiadane oszczędności, itp.

## 7. Przykłady Atrybutów

### Oryginalne Atrybuty
- **Saldo konta:** (kategoryczny)
- **Historia kredytowa:** (kategoryczny)
- **Cel kredytu:** (kategoryczny)
- **Długość zatrudnienia:** (kategoryczny)
- **Posiadane oszczędności:** (kategoryczny)

### Atrybuty Numeryczne
- **Saldo konta:** (numeryczny)
- **Historia kredytowa:** (numeryczny)
- **Cel kredytu:** (numeryczny)
- **Długość zatrudnienia:** (numeryczny)
- **Posiadane oszczędności:** (numeryczny)

## 8. Uwagi
- **Zastosowanie:** Zbiór danych jest szeroko używany w analizie kredytów i ocenie ryzyka kredytowego. Jest to klasyczny zbiór danych używany do porównań metod klasyfikacji i algorytmów uczenia maszynowego.

# 5. Analiza Wyników

### Random Forest

- **Cross-Validation Accuracy Scores:** [0.675, 0.72, 0.74, 0.715, 0.7]
- **Mean Cross-Validation Accuracy:** 0.71
- **Classification Report:**
  - **Precision:** 0.78 (0), 0.49 (1)
  - **Recall:** 0.81 (0), 0.44 (1)
  - **F1-Score:** 0.79 (0), 0.46 (1)
  - **Accuracy:** 0.70

### Logistic Regression

- **Cross-Validation Accuracy Scores:** [0.675, 0.705, 0.73, 0.685, 0.73]
- **Mean Cross-Validation Accuracy:** 0.705
- **Classification Report:**
  - **Precision:** 0.75 (0), 0.50 (1)
  - **Recall:** 0.87 (0), 0.32 (1)
  - **F1-Score:** 0.81 (0), 0.39 (1)
  - **Accuracy:** 0.70

### Gradient Boosting

- **Cross-Validation Accuracy Scores:** [0.675, 0.695, 0.735, 0.71, 0.73]
- **Mean Cross-Validation Accuracy:** 0.709
- **Classification Report:**
  - **Precision:** 0.78 (0), 0.57 (1)
  - **Recall:** 0.87 (0), 0.41 (1)
  - **F1-Score:** 0.82 (0), 0.48 (1)
  - **Accuracy:** 0.73

### XGBoost

- **Cross-Validation Accuracy Scores:** [0.675, 0.66, 0.73, 0.715, 0.715]
- **Mean Cross-Validation Accuracy:** 0.699
- **Classification Report:**
  - **Precision:** 0.78 (0), 0.49 (1)
  - **Recall:** 0.79 (0), 0.47 (1)
  - **F1-Score:** 0.79 (0), 0.48 (1)
  - **Accuracy:** 0.70

### Random Forest z GridSearchCV

- **Cross-Validation Accuracy Scores:** [0.69, 0.705, 0.745, 0.745, 0.735]
- **Mean Cross-Validation Accuracy:** 0.724
- **Classification Report:**
  - **Precision:** 0.78 (0), 0.53 (1)
  - **Recall:** 0.84 (0), 0.42 (1)
  - **F1-Score:** 0.81 (0), 0.47 (1)
  - **Accuracy:** 0.72

## 4. Wnioski

- **Gradient Boosting** osiągnął najwyższą dokładność w walidacji krzyżowej (0.735) i pokazuje silne wyniki na zestawie testowym.
- **Logistic Regression** i **Random Forest** pokazują podobną średnią dokładność w walidacji krzyżowej, ale Random Forest osiągnął nieco wyższą dokładność na zbiorze testowym.
- **XGBoost** miało niższą dokładność w walidacji krzyżowej i na zbiorze testowym, co może sugerować, że ten model wymaga dalszej optymalizacji.

## 5. Propozycje Dalszych Kroków

- **Optymalizacja Hyperparametrów:** Możliwość dalszego dostrajania hyperparametrów dla modeli XGBoost i Gradient Boosting w celu poprawy wyników.
- **Analiza Atrybutów:** Badanie wpływu poszczególnych atrybutów na wyniki modeli, aby lepiej zrozumieć, które cechy są najbardziej informacyjne.
- **Zbieranie Większej Ilości Danych:** Rozważenie rozszerzenia zbioru danych, co może poprawić jakość modelu i jego dokładność.

Ten raport prezentuje wyniki walidacji krzyżowej oraz oceny klasyfikacji dla różnych modeli, oferując wszechstronny obraz ich efektywności.
