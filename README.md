# OrderProjekt
## Problemformulering

Dette projekt har til formål at analysere og optimere ordredata ved hjælp af Business Intelligence (BI)-værktøjer og maskinlæringsmodeller. Målet er at forudsige fremtidige ordrer, analysere effekten af rabatstrategier og optimere lagerstyring. Dataene fra **Orders.csv** omfatter flere dimensioner såsom kundedetaljer, produktkategorier, geografisk placering og prisfastsættelse, som vil blive brugt til at løse følgende spørgsmål:

1. **Forudsigelse af fremtidige ordrevolumener**: Hvilke faktorer påvirker sandsynligheden for fremtidige ordrer baseret på kundens tidligere købsadfærd, produktkategorier og geografiske områder?
2. **Effekt af rabatter**: Hvordan påvirker forskellige rabatniveauer den samlede ordremængde og indtægt? Er der en optimal rabatstrategi, der kan maksimere omsætningen uden at reducere fortjenesten væsentligt?
3. **Geografisk optimering**: Hvilke geografiske områder genererer de højeste salgsvolumener, og hvilke produkter er mest populære i disse områder? Hvordan kan virksomheden målrette markedsføring og distribution for at maksimere salget?

## Metode

### 1. Dataindsamling og -forberedelse
- **Dataintegration**: Ordredata fra **Orders.csv** blev indlæst og inspiceret for at identificere manglende værdier og outliers.
- **Datatransformation**: Konvertering af datoformater og håndtering af tekstvariabler (f.eks. kundens navn og by) samt omkodning af kategoriske variabler som produktkategori og land.
- **Deskriptiv statistik**: Anvendt til at udforske centrale tendenser som gennemsnit, median og standardafvigelse på tværs af produktkategorier, geografiske områder og rabatniveauer.
- **Visualisering**: Diagrammer som søjlediagrammer og tidsserier blev oprettet for at vise ordretendenser over tid og på tværs af geografiske regioner.

### 2. Feature Engineering og Udvælgelse
- **Feature Engineering**: Nye variable blev oprettet, såsom "samlet rabat pr. ordre" og "gennemsnitligt antal ordrer pr. kunde".
- **Feature Selection**: Brug af korrelationsanalyse og *Recursive Feature Elimination* (RFE) til at udvælge de mest informative variable til forudsigelse.

### 3. Modeller til forudsigelse af ordrevolumener
- **Maskinlæring**: Algoritmer som *Random Forest* og *Logistic Regression* blev anvendt til at forudsige sandsynligheden for, at en kunde afgiver en ordre baseret på historiske data.
- **Modelvalidering**: Data blev opdelt i trænings- og testdatasæt, og præstationen af modellerne blev evalueret ved hjælp af metrikker som *accuracy*, *precision*, *recall* og *ROC AUC*.
- **Hyperparameter tuning**: Modellerne blev optimeret ved hjælp af *Grid Search* for at finde de bedste parametre.

### 4. Analyse af rabatstrategier
- **Klyngeanalyse (Clustering)**: *K-means clustering* blev anvendt til at gruppere kunder baseret på deres købsmønstre og rabatniveauer for at identificere mønstre i kundeadfærd.
- **A/B test**: A/B tests blev anvendt til at evaluere, hvordan forskellige rabatniveauer påvirker kundernes købsadfærd og den samlede indtjening.

### 5. Præsentation af resultater
- **Datavisualisering**: Der blev udviklet interaktive dashboards til at visualisere forudsigelser, rabatanalyse og salgsprognoser. Værktøjer som *Tableau* og *Power BI* blev brugt til at præsentere resultaterne.
- **Brugerinterface**: En simpel brugergrænseflade blev implementeret for at give adgang til analyserne og gøre resultaterne tilgængelige for beslutningstagere.
