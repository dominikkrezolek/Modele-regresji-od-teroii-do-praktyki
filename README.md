
# Instalacja i uruchomienie pakietów w R

Ten projekt zawiera przykładowy kod do instalacji i uruchamiania popularnych pakietów R wykorzystywanych w analizie danych, uczeniu maszynowym oraz analizie przestrzennej.

## 📦 Lista pakietów

Poniższe pakiety zostaną zainstalowane, jeśli nie są jeszcze obecne w systemie:

- `caret` – modelowanie i walidacja
- `dplyr`, `tidyr`, `tidyverse` – manipulacja i analiza danych
- `ggplot2` – wizualizacja
- `glmnet` – modele regresyjne i klasyfikacyjne z regularyzacją
- `KernSmooth`, `mgcv` – metody nieparametryczne i gładzenie
- `quantmod` – dane finansowe i rynkowe
- `readxl`, `reshape2` – import i przekształcanie danych
- `sf`, `spdep`, `spatialreg` – analiza danych przestrzennych

## 🔧 Instalacja pakietów

Aby zainstalować wszystkie wymagane pakiety (jeśli nie są jeszcze obecne):

```r
packages <- c(
  "caret", "dplyr", "ggplot2", "glmnet", "KernSmooth",
  "mgcv", "quantmod", "readxl", "reshape2", "sf",
  "spatialreg", "spdep", "tidyr", "tidyverse"
)

installed <- rownames(installed.packages())
for (p in packages) {
  if (!(p %in% installed)) {
    install.packages(p, dependencies = TRUE)
  }
}
```

> 💡 **Uwaga**: Pakiety przestrzenne (`sf`, `spatialreg`, `spdep`) mogą wymagać dodatkowych bibliotek systemowych (np. `gdal`, `proj`, `geos`) w systemach Linux/macOS.

## ▶️ Ładowanie pakietów

Aby rozpocząć pracę z pakietami, załaduj je przy użyciu `library()`:

```r
library(caret)
library(dplyr)
library(ggplot2)
library(glmnet)
library(KernSmooth)
library(mgcv)
library(quantmod)
library(readxl)
library(reshape2)
library(sf)
library(spatialreg)
library(spdep)
library(tidyr)
library(tidyverse)
```

> ℹ️ **Uwaga**: `tidyverse` automatycznie ładuje niektóre pakiety (np. `dplyr`, `ggplot2`, `readr`, `tidyr`, `tibble`, `stringr`, `forcats`), ale **nie obejmuje** pakietów takich jak `caret`, `sf`, `spdep`.

## 📁 Licencja

Ten skrypt może być swobodnie wykorzystywany do celów edukacyjnych i badawczych.
