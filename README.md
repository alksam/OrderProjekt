# OrderProjekt
## Problemformulering

Dette projekt sigter mod at anvende moderne Business Intelligence (BI) og kunstig intelligens (AI) metoder til at analysere og optimere ordredata. Formålet er at:
1. Forudsige fremtidige ordrer baseret på historiske kundedata, produkttyper og geografiske faktorer.
2. Evaluere effekten af rabatstrategier for at finde en optimal balance mellem øget salg og opretholdelse af fortjeneste.
3. Optimere lagerstyring ved hjælp af præcise salgsprognoser for at sikre, at lagerbeholdningen matcher efterspørgslen.
4. Identificere geografiske salgsområder med højt potentiale og tilpasse markedsførings- og distributionsstrategier i overensstemmelse hermed.

Projektet skal give en brugbar løsning, der kombinerer dataanalyse, maskinlæring og interaktiv visualisering for at understøtte beslutningstagning. Den forventede positive effekt er øget salgspræcision, effektiv lagerstyring og bedre kundeindsigt.



### Teoretisk grundlag og baggrund

I dette projekt anvendes både superviseret og usuperviseret maskinlæring til at analysere ordredata. Følgende metoder anvendes:

1. **Random Forest:** 
   Random Forest er en ensemblemetode, der bygger på flere beslutningstræer for at forbedre modellens præcision og reducere risikoen for overfitting. Ved at kombinere forudsigelser fra mange forskellige træer opnås en mere robust og nøjagtig model. Random Forest er velegnet til klassifikationsopgaver, hvor der er behov for at håndtere komplekse og ikke-lineære sammenhænge i dataene.

2. **K-means Clustering:** 
   K-means er en usuperviseret læringsmetode, der bruges til at gruppere data i forskellige klynger baseret på ligheder i dataene. Metoden opdeler data i et forudbestemt antal klynger og tildeler hvert datapunkt til den nærmeste klyngecenter. K-means anvendes til at finde mønstre i data, såsom segmentering af kunder baseret på deres købsmønstre.

#### Evalueringsmetrikker:
- **Accuracy:** Måler andelen af korrekte forudsigelser ud af det samlede antal forudsigelser. Velegnet, når klasserne er nogenlunde balancerede.
- **Precision:** Angiver, hvor mange af de forudsagte positive tilfælde, der faktisk er positive. Bruges især, når det er vigtigt at minimere falske positive.
- **Recall:** Måler, hvor mange af de faktiske positive tilfælde, der blev korrekt forudsagt som positive. Bruges, når det er vigtigt at fange så mange positive tilfælde som muligt.
- **ROC AUC:** ROC AUC (Receiver Operating Characteristic - Area Under Curve) viser modellens evne til at skelne mellem positive og negative klasser. En højere AUC-værdi indikerer en bedre præstation.
### Dataforberedelse og datakvalitet

Data blev indsamlet fra `Orders.csv` og gennemgik en række dataforberedelses- og rensningsprocesser for at sikre kvaliteten. Dette omfattede:

1. **Håndtering af manglende værdier:**
   - Numeriske kolonner blev udfyldt med gennemsnittet for at undgå påvirkning af manglende data. 
   - Kategoriske variabler blev udfyldt med den mest almindelige værdi for at sikre konsistens.

2. **Fjernelse af outliers:**
   - Outliers blev identificeret og fjernet ved hjælp af boksplot-metoden, hvor data uden for 1,5 gange interkvartilområdet (IQR) blev fjernet.

3. **Datatransformation:**
   - Datoformater blev konverteret til datetime-format for at muliggøre tidsbaserede analyser.
   - Kategoriske variabler blev omkodet ved brug af one-hot encoding for at forberede dataene til maskinlæringsmodellerne.

#### Datakvalitet:
Der var nogle inkonsekvenser i dataene, såsom duplikerede rækker og manglende værdier, som blev håndteret ved at fjerne dubletter og udfylde manglende data. Der var også ubalancerede klasser, hvilket blev adresseret ved at bruge stratificeret sampling til at opdele data i trænings- og testdatasæt.
