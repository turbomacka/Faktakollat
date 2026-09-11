# Faktakollat

**Faktakollat** är ett öppet experiment i AI assisterad faktagranskning.

Den första granskningen gäller SVT:s **Statsministermötet den 9 september 2026**. Hela sändningens undertextspår har bearbetats till ett tidskodat transkript. Generativ AI har därefter använts för att identifiera kontrollerbara sakpåståenden, hitta relevanta källor och föreslå bedömningar. De publicerade fynden har källor och tidskoder så att de går att kontrollera i efterhand.

## Principer

* Samma metod används oavsett vem som uttalar sig.
* Primärkällor och originalstatistik prioriteras.
* Värderingar, prognoser och politiska löften skiljs från kontrollerbara sakpåståenden.
* Ett felaktigt påstående kallas inte automatiskt en lögn. Avsikt kräver egna belägg.
* Rättelser ska vara synliga och motiverade.

## Filer

`index.html` innehåller den publicerbara webbplatsen och faktagranskningen.

`data.json` innehåller granskningsresultaten i maskinläsbart format.

`transkript.html` är en läsbar webbsida som hämtar hela transkriptet.

`transkript/del-01.txt` till `transkript/del-08.txt` innehåller den rengjorda tidskodade versionen av SVT:s undertextning.

`.nojekyll` gör att GitHub Pages serverar innehållet utan Jekyll bearbetning.

## Metod i korthet

1. SVT:s undertextspår hämtades i WebVTT format.
2. Formateringskod togs bort och tidskoder behölls.
3. AI gick igenom hela transkriptet och identifierade kontrollerbara sakpåståenden.
4. Kandidaterna kontrollerades mot i första hand myndigheter, riksdagen, regeringen, OECD och annan originaldata.
5. Resultaten klassificerades som **felaktigt**, **missvisande** eller **obestyrkt** när underlaget motiverade det.
6. Varje publicerad bedömning har tidskod och källhänvisning.

## Begränsningar

SVT:s undertextning kan vara lätt redigerad jämfört med exakt ordagrant tal. AI kan missa relevanta påståenden och kan göra fel i både källsökning och tolkning. Materialet är därför byggt för att kunna granskas och rättas, inte för att behandlas som en ofelbar automatisk domare.

## Rättelser

Om du hittar ett fel, öppna gärna ett issue i repot och ange vilken rad eller tidskod det gäller samt den källa som motsäger bedömningen.

## Publicering

Sajten är byggd som statisk HTML och kan publiceras direkt med GitHub Pages från `main` och repository root.

## Licens och källmaterial

Webbplatsens analys och kod kan återanvändas med källhänvisning. Transkriptet bygger på SVT:s publicerade undertextning och är inkluderat här som granskningsunderlag. Projektet är inte producerat av eller knutet till SVT.
