Vad är skillnaden mellan mikrodata, individdata och aggregerad data?
Enkelt uttryckt är skillnaden att mikrodata/individdata handlar om enskilda enheter (en person, ett föremål, en händelse), medan aggregerad data handlar om grupper.

## **Mikrodata och individdata**  
Mikrodata är data som beskriver egenskaper hos en enskild enhet. Om den enheten är en person kallas det ofta individdata. Om enheten är något annat (ett företag, en bil, en transaktion) är mikrodata en vanligare allmän term. Här är några exempel på individdata:

  * En rad i ett patientregister som visar: `Personnummer: 700101-1234, Besöksdatum: 2025-10-23, Diagnos: Hypertoni (I10), Mätt blodtryck: 145/92`.  
  * Data från en hälsoapp: `Användare: anna@epost.se, Datum: 2025-10-22, Steg: 8 450, Vilopuls: 62`.  
  * En post i ett nationellt register: `Individ-ID: 9876, Vaccination: Ja, Dos 1 (Pfizer), Datum: 2024-03-10`.

Individdata som är hälsodata är nästan alltid personuppgifter, eftersom det är mycket svårt att [anonymisera hälsodata](https://github.com/PaulJohannesson/hds-data-toolbox/blob/main/grunder/Integritetsh%C3%B6jande%20tekniker.md).

## **Aggregerad data**  
Aggregerad data är information där mikrodata har slagits samman på gruppnivå (till exempel per region, kön eller månad) för att ge en översikt. Aggregerad data kan exempelvis uttryckas i antal, andelar, medelvärden, medianer eller percentiler. Datan beskriver alltså en grupp, inte en individ. Här är exempel på aggregerade data (relaterade till individdata ovan):

* Statistik från en vårdcentral: ”12 % av våra listade patienter över 65 år hade diagnosen hypertoni under 2024.” (Man kan inte se vad patient 700101-1234 hade.)  
* En trendrapport från en hälso-app: ”Våra svenska användare gick i genomsnitt 6 200 steg per dag förra månaden.” (Man kan inte se vad `anna@epost.se` gjorde.)  
* Statistik från Folkhälsomyndigheten: ”Vaccinationstäckningen för dos 1 i riket är 88 %.” (Man kan inte se Individ 9876:s status.)


Observera att aggregering inte alltid är anonymisering—för små grupper kan återidentifiering fortfarande vara möjlig.

## **Översikt**

| Egenskap | Mikrodata / Individdata | Aggregerad data |
| :---- | :---- | :---- |
| Visar | Detaljer om en enhet (till exempel en person). | Sammanfattning om en grupp (till exempel alla personer i Malmö). |
| Granularitet | Mycket hög (den lägsta nivån). | Låg (en högre nivå). |
| Syfte | Detaljerad analys, förstå enskilda fall. | Se övergripande trender, mönster, helheter. |
| Identifierbarhet | Kan ofta identifiera enheten (särskilt individdata). | Enheter kan oftast inte identifieras. |
| Process | Råmaterialet som samlas in. | Produkten man får efter bearbetning av individdata. |
| Exempel | "Den här patienten har blodtryck 140/90." | "15 % av patienterna har högt blodtryck." |

