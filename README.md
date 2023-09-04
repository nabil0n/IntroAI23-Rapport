# Introduktion till AI - AI23
## Uppgift - Arbetsflöde för AI-projekt

### Ett projekt där maskininlärning eller djupinlärning är inblandat kräver oftast ett visst antal steg i arbetsflödet. Syftet med den här uppgiften är att få en teoretisk överblick över de vanliga stegen i arbetsflödet av en maskininlärningsapplikation.

### I den här uppgiften ska du teoretiskt beskriva dessa steg för ett scenario med maskininlärningsalgoritmen linjär regression. Scenariot är att förutspå huspriser baserat på olika ”features” såsom antalet rum, geografiska läget, storlek på huset med mera.

---
- 500-1000 ord

- källhänvisa allt
---

- [ ]  beskriv hur man kan göra för att samla in datan, vilka format, vart kan man spara datan?

Sidor så som svensk mäklarstatistik och booli hushåller och uppdaterar bostadsmarknadsdata i api-form, vilket är enkelt att hämta och ställa upp i tabeller eller liknande genom json-manipulering i allt från excel till kod-språk.

- [ ]  beskriv hur man kan visualisera datan?

Förutom dagens väldigt automatiserade och enkla lösningar i excel eller google sheets finns andra mer kodbaserade lösningar. Exempel på detta i Python är Pandas, Matplotlib, Seaborn eller Plottly, som ställer upp data i lättlästa grafer och tabeller.

- [ ]  beskriv hur man kan göra för att bearbeta datan till rätt format?

Förhoppningsvis kan datan samlas in i rätt format redan från början, men ytterligare skulle man kunna "rena" datan genom att undersöka om datan innehåller tomma värden eller data som verkar vara långt utanför vad som är rimligt. 

- [x]  beskriv hur linjär regression fungerar.

Linjär regression är ett sätt att förutspå en utveckling av något utifrån flera variabler genom att matematiskt undersöka och värdera värden mot varandra. Om vi till exempel skulle vilja förutspå hur huspriser skiljer sig kan nog de flesta tänka sig att ett stort hus i stan är dyrare än ett litet hus i skogen. Men är detta alltid sant, och spelar det någon roll om huset har många rum, eller kanske vem som bott i huset tidgare? Genom att använda oss av linjär regression kan vi jämföra insamlad data, och på så vis rita upp och jämföra modeller som kollar på korrelationer mellan de olika modellerna. Fungerar modellen bra kan den sedan göra en kvalificerad gissning om ytterligare tillagda hus om ny husdata skulle tillsättas.

Nedan följer ett enkelt exempel:

| Hus | Kostnad | Plats | Antal rum | 
| -------- | -------- | -------- | -------- |
| 1 | 300 000 | Haparanda | 8 |
| 2 | 400 000 | Borås | 5 |
| 3 | 1 800 000 | Göteborg | 5 |
| 4 | 1 600 000 | Stockholm | 3 |

Vi kan direkt se att det är dyrare och mindre "värt" att bo i stora städer, men låt oss för tillfället enbart jämföra Kostnad och Antal rum. Se grafer.

![exempel graf prickar](exempelgraf1.jpg)

I grafen ovan kan vi se hur de fyra husen förhåller sig till varandra, och nedan kan vi trenden i form av en linje som är uträknad med linjär regression utifrån angiven data. Detta är ett exempel på enkel linjär regression, men multiopel eller polymial regression hade kanske vart mer aktuell för vårt exempel långsiktigt.

![exempel graf prickar](exempelgraf2.jpg)

- [x]  beskriv hur man kan göra för att driftsätta modellen?

I detta exempel skulle man kunna utveckla en app som utifrån användarens önskemål och budgeterade tidslinje kunna gissa sig till ungefär vilket sorts hus användaren har råd med, var någonstans i Sverige bostaden skulle kunna ligga samt när användaren skulle kunna ha råd med det. Eller varför inte en implementering för byggkoncerner där företag kan se vilken mark som är bäst att bygga på utefter vilka sorts bostäder människor i Sverige verkar söka efter, där storlek, område och prisområden skulle kunna får avgöra vad som byggs i framtiden. 

- [ ]  vilka teknologier kan man använda i de olika stegen i maskininlärningsprocessen?



Källor
- https://learn.microsoft.com/en-us/training/modules/understand-regression-machine-learning/
- https://docs.google.com/spreadsheets/
- https://www.maklarstatistik.se/svensk-maklarstatistiks-api-aggregerad-statistik/
- https://www.booli.se/p/api