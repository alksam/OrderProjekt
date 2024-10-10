# OrderProjekt
## Problemformulering

Dette projekt sigter mod at anvende moderne Business Intelligence (BI) og kunstig intelligens (AI) metoder til at analysere og optimere ordredata. Formålet er at:

- Forudsige fremtidige ordrer baseret på historiske kundedata, produkttyper og geografiske faktorer.
- Evaluere effekten af rabatstrategier for at finde en optimal balance mellem øget salg og opretholdelse af fortjeneste.
- Optimere lagerstyring ved hjælp af præcise salgsprognoser for at sikre, at lagerbeholdningen matcher efterspørgslen.
- Identificere geografiske salgsområder med højt potentiale og tilpasse markedsførings- og distributionsstrategier i overensstemmelse hermed.

Projektet skal give en brugbar løsning, der kombinerer dataanalyse, maskinlæring og interaktiv visualisering for at understøtte beslutningstagning. Den forventede positive effekt er øget salgspræcision, effektiv lagerstyring og bedre kundeindsigt.

## Teoretisk Grundlag og Baggrund

I dette projekt anvendes både superviseret og usuperviseret maskinlæring til at analysere ordredata. Følgende metoder anvendes:

- **Random Forest**: Random Forest er en ensemblemetode, der bygger på flere beslutningstræer for at forbedre modellens præcision og reducere risikoen for overfitting. Ved at kombinere forudsigelser fra mange forskellige træer opnås en mere robust og nøjagtig model. Random Forest blev valgt til klassifikationsopgaven på grund af dens evne til at håndtere komplekse og ikke-lineære sammenhænge i dataene.

- **K-means Clustering**: K-means er en usuperviseret læringsmetode, der bruges til at gruppere data i forskellige klynger baseret på ligheder i dataene. Metoden opdeler data i et forudbestemt antal klynger og tildeler hvert datapunkt til den nærmeste klyngecenter. K-means blev anvendt til at segmentere kunder baseret på deres købsmønstre, hvilket gjorde det muligt at identificere forskellige kundesegmenter og tilpasse markedsføringsstrategier.

## Evalueringsmetrikker

- **Accuracy**: Måler andelen af korrekte forudsigelser ud af det samlede antal forudsigelser. Velegnet, når klasserne er nogenlunde balancerede.
- **Precision**: Angiver, hvor mange af de forudsagte positive tilfælde, der faktisk er positive. Dette er særligt vigtigt, når det er nødvendigt at minimere falske positive.
- **Recall**: Måler, hvor mange af de faktiske positive tilfælde, der blev korrekt forudsagt som positive. Dette er vigtigt, når det er nødvendigt at fange så mange positive tilfælde som muligt.
- **ROC AUC**: ROC AUC (Receiver Operating Characteristic - Area Under Curve) viser modellens evne til at skelne mellem positive og negative klasser. En højere AUC-værdi indikerer en bedre præstation.

## Dataforberedelse og Datakvalitet

Data blev indsamlet fra `Orders.csv` og gennemgik en række dataforberedelses- og rensningsprocesser for at sikre kvaliteten. Dette omfattede:

- **Håndtering af manglende værdier**:
  - Numeriske kolonner blev udfyldt med gennemsnittet for at undgå påvirkning af manglende data.
  - Kategoriske variabler blev udfyldt med den mest almindelige værdi for at sikre konsistens.

- **Fjernelse af Outliers**:
  - Outliers blev identificeret og fjernet ved hjælp af boksplot-metoden, hvor data uden for 1,5 gange interkvartilområdet (IQR) blev fjernet.

- **Datatransformation**:
  - Datoformater blev konverteret til `datetime`-format for at muliggøre tidsbaserede analyser.
  - Kategoriske variabler blev omkodet ved brug af one-hot encoding for at forberede dataene til maskinlæringsmodellerne.

- **Datakvalitet**:
  - Inkonsekvenser i dataene, såsom duplikerede rækker og manglende værdier, blev håndteret ved at fjerne dubletter og udfylde manglende data. Ubalancerede klasser blev adresseret ved hjælp af stratificeret sampling til opdeling af data i trænings- og testdatasæt.

## Modelleringsprocessen

- **Valg af Algoritmer**: Random Forest blev valgt til klassifikationsopgaven på grund af dens evne til at håndtere komplekse ikke-lineære sammenhænge i dataene. K-means clustering blev anvendt til at gruppere kunder i segmenter baseret på købsmønstre.

- **Hyperparameter Tuning**: Grid Search blev anvendt til at finde de optimale hyperparametre for Random Forest ved at søge på tværs af forskellige kombinationer af parametre. Dette hjalp med at forbedre modellernes præcision ved at vælge de bedste parametre, såsom `n_estimators`, `max_depth`, `min_samples_split`, og `min_samples_leaf`.

- **Modelvalidering**: Data blev opdelt i trænings- og testdatasæt (70/30), og k-fold krydsvalidering blev brugt på træningsdatasættet for at vurdere modellernes generaliserbarhed.

## Klyngeanalyse og A/B Tests

- **Klyngeanalyse**: K-means clustering blev brugt til at gruppere data i klynger baseret på lignende mønstre. Klyngernes kvalitet blev vurderet ved brug af silhuetkoefficienten, som måler, hvor godt datapunkterne passer til deres respektive klynger.

- **A/B Tests**: A/B tests blev udført for at sammenligne effekten af forskellige rabatstrategier på salgsvolumen. En statistisk t-test blev brugt til at vurdere, om der var en signifikant forskel mellem grupperne.

## Konklusion

Dette projekt kombinerer dataanalyse, maskinlæring og interaktiv visualisering for at understøtte beslutningstagning i virksomheden. Ved at anvende Random Forest til forudsigelser og K-means clustering til segmentering har projektet skabt en løsning, der forbedrer salgsprognoser, lagerstyring og kundeindsigt. De opnåede resultater giver mulighed for at tilpasse markedsføring, optimere lagerbeholdning og øge virksomhedens effektivitet.
