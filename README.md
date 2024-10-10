# OrderProjekt
## Problemformulering

Dette projekt sigter mod at anvende moderne Business Intelligence (BI) og kunstig intelligens (AI) metoder til at analysere og optimere ordredata. Formålet er at:
1. Forudsige fremtidige ordrer baseret på historiske kundedata, produkttyper og geografiske faktorer.
2. Evaluere effekten af rabatstrategier for at finde en optimal balance mellem øget salg og opretholdelse af fortjeneste.
3. Optimere lagerstyring ved hjælp af præcise salgsprognoser for at sikre, at lagerbeholdningen matcher efterspørgslen.
4. Identificere geografiske salgsområder med højt potentiale og tilpasse markedsførings- og distributionsstrategier i overensstemmelse hermed.

Projektet skal give en brugbar løsning, der kombinerer dataanalyse, maskinlæring og interaktiv visualisering for at understøtte beslutningstagning. Den forventede positive effekt er øget salgspræcision, effektiv lagerstyring og bedre kundeindsigt.




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
