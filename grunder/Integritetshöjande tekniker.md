Att pseudonymisera och anonymisera personuppgifter, särskilt känsliga sådana som hälsodata, är viktiga tekniker för att kunna använda data för forskning och produktutveckling samtidigt som man skyddar den personliga integriteten. På senare tid har även syntetisering blivit ett kraftfullt alternativ. Men dessa metoder skiljer sig tydligt åt – både tekniskt och juridiskt.

## **Vad innebär pseudonymisering?**

När personuppgifter pseudonymiseras ersätter man direkta identifierare (som namn och personnummer) med en kod eller pseudonym. Eftersom det fortfarande finns en nyckel som gör det möjligt att koppla tillbaka uppgifterna till individen, anses det normalt att pseudonymiserade uppgifter fortfarande är personuppgifter enligt GDPR. Men bedömningen kan påverkas av vem som tar emot uppgifterna och vilka faktiska och rättsliga möjligheter mottagaren har att identifiera personerna. Pseudonymisering räknas som en effektiv teknisk skyddsåtgärd som avsevärt minskar risken för integritetsintrång.

## **Hur fungerar pseudonymisering i praktiken?**

Principen är att identiteten skiljs från hälsodatan genom att namn och andra identifierare ersätts med en kod. Nyckeln som länkar koden till den faktiska individen lagras separat, mycket säkert, och med stränga begränsningar kring åtkomst.  

Ett exempel kan vara en hälsoapp som samlar in data från användare. I appens analysdatabas är varje individ representerad av en kod, t.ex. ”anv-XY45-B2Z9”. Namn, e-post och kod lagras separat med hög säkerhet och strikt åtkomstkontroll. Utvecklarna som analyserar hälsodatan ser endast koden, inte vem individen är. Vid behov kan man använda nyckeln för att koppla tillbaka datan till individen.

## **Vad innebär anonymisering?**

Anonymisering går ett steg längre och innebär att man helt och permanent tar bort alla möjligheter att identifiera en individ i en befintlig datamängd. När anonymisering lyckas, upphör informationen att vara personuppgifter och faller därför utanför GDPR:s krav. Det ger större frihet att använda data i exempelvis forskning och statistik.

## **Utmaningar med anonymisering av hälsodata**

Att uppnå anonymisering av hälsodata på individnivå är mycket svårt. Det räcker nämligen inte att bara ta bort namn eller personnummer, eftersom en unik kombination av andra uppgifter (till exempel ålder, ort och ovanlig sjukdom) fortfarande kan göra att en individ identifieras. För att anonymisera måste man därför ofta använda tekniker som:

* Maskering: ta bort detaljerad information som namn, adresser, personnummer och exakta datum.  
* Generalisering: göra information mindre exakt, exempelvis ändra ”47 år” till ”åldersgrupp 40–50 år” eller ”Kalmar” till ”södra Sverige”.  
* Brusning: lägga till slumpmässiga avvikelser i numeriska värden, till exempel något justerade blodtrycksvärden.

Problemet med anonymisering är alltså att processen kan misslyckas. I vissa fall går det ändå att identifiera personer trots anonymiseringsåtgärder. Dessutom minskar datans användbarhet om viktig information i den ursprungliga datan tas bort eller förvrängs.

## **Vad innebär syntetisering?**

Ett tredje, alltmer populärt angreppssätt är syntetisering. Till skillnad från anonymisering, som modifierar befintlig data, innebär syntetisering att man skapar helt ny, konstgjord data med utgångspunkt från en given datamängd. Denna syntetiska data är utformad för att efterlikna de statistiska egenskaperna, mönstren och strukturen hos den ursprungliga datamängden, men den innehåller ingen information om verkliga individer.

## **Hur fungerar syntetisering i praktiken?**

Processen involverar ofta avancerade maskininlärningsmodeller, så kallade generativa modeller (exempelvis GANs – Generative Adversarial Networks). Dessa modeller tränas på den verkliga mikrodatan i en datamängd för att lära sig dess fördelning och variabelsamband. När modellen är tränad kan den generera syntetisk mikrodata som statistiskt liknar originalet, men som är helt fiktiva.  

Om syntetiseringen är korrekt utförd betraktas datan som anonym och faller därmed utanför GDPR, eftersom den då inte är kopplad till identifierbara personer.

## **Fördelar och utmaningar med syntetisk data**

Den stora fördelen är förmågan att balansera högt integritetsskydd med hög användbarhet. Till skillnad från traditionell anonymisering behöver man inte försämra datan genom generalisering eller brusning. Datan kan behålla en hög detaljnivå och komplexitet, vilket är särskilt värdefullt för djupanalys och träning av AI-modeller.  

Utmaningarna ligger i kvaliteten och säkerheten. Högkvalitativ syntetisk data måste korrekt återspegla originaldatan för att vara användbar, men det finns en risk att sällsynta fall (*outliers*) eller subtila nyanser missas. Överinlärning (*overfitting*) är en särskild risk. När modellen anpassas för hårt till träningsdatan kan den memorera mönster på individnivå och sedan generera poster som liknar verkliga personer. Att skapa högkvalitativ och säker syntetisk data kräver därför avancerad teknisk expertis.

## **Sammanfattning av skillnaderna**

| Aspekt | Pseudonymisering | Anonymisering (Klassisk) | Syntetisering |
| :---- | :---- | :---- | :---- |
| Metod | Ersätter identifierare med kod. | Modifierar/tar bort data för att hindra identifiering. | Skapar ny, konstgjord data baserat på mönster. |
| Är data fortfarande personuppgifter? | Ja, omfattas av GDPR. | Nej, faller utanför GDPR (om lyckad). | Nej, faller utanför GDPR (om lyckad). |
| Kan man identifiera individen? | Ja, med nyckel som förvaras separat. | Nej, kopplingen är permanent bruten (om lyckad). | Nej, datan är konstgjord (om lyckad). |
| Datakvalitet och användbarhet | Hög, datans kvalitet behålls. | Lägre, data försämras medvetet. | Potentiellt hög, men kan missa sällsynta fall. Kräver validering. |
| Juridisk frihet att använda data | Begränsad, GDPR gäller fortfarande. | Hög, GDPR gäller ej. | Hög, GDPR gäller ej. |
| Krav på expertis | Medel (säker nyckelhantering). | Hög (svårt att garantera anonymitet). | Hög (kräver expertis inom AI/ML och integritet). |

Sammanfattningsvis är pseudonymisering ofta det praktiska förstahandsvalet när exakt datakvalitet och möjlighet till uppföljning behövs, men den lämnar uppgifterna inom GDPR och kräver därför robusta skyddsåtgärder. 

Anonymisering ger stor regulatorisk frihet om den verkligen uppnås, men det är svårt för komplex hälsodata och leder ofta till en betydande försämring av datans användbarhet.  

Syntetisering erbjuder en modern medelväg, som potentiellt kan ge både regulatorisk frihet och hög datanytta, vilket gör det till ett intressant alternativ för innovation och AI-utveckling. Det ställer dock höga krav på teknisk kompetens för att säkerställa att datan är både korrekt representativ och säker ur integritetssynpunkt.
