##1. Inledning
---


En Markov-beslutsprocess är en planeringsalgoritm som tillhör ämnet artificiell intelligens. 
För att förstå en Markov-beslutsprocess behöver man först förstå de problem som Markov-beslutsprocesserna strävar efter att lösa, men man behöver även förstå varför man använder just denna algoritm för det och var det inte lönar sig att använda algoritmen. 

<br />

Artificiell intelligens är ett ämne som är känt för att vara mycket svårdefinierat. Detta kan delvis förklaras av att intelligens i sig inte är lätt att definiera. En tidig definition som försöker undvika problemet med att definiera intelligens är den som gavs av Alan Turing[7]. Turing föreslog att man, istället för att strikt försöka definiera termerna, skulle kunna definiera en maskin som intelligent om maskinens beteende inte kan urskiljas från beteendet hos något som vi definierar som intelligent (en människa). Även om denna definition undviker problemen med att definiera intelligens så har den vissa problem. Specifikt begränsar Turings definition den artificiella intelligensens prestanda till det man jämför den med. T.ex. skulle en maskin som är snabbare än en människa på att räkna relativt lätt kunna urskiljas från en människa och därmed inte vara intelligent. John McCarthy, som för övrigt var den som myntade uttrycket artificell intelligens, ger en enklare definition av det: _"The science and engineering of making intelligent machines, especially intelligent computer programs. It is related to the similar task of using computers to understand human intelligence, but AI does not have to confine itself to methods that are biologically observable."_

<br />

För artificiell intelligens, precis som för annan problemlösning, är det oftast relevant att veta vissa saker om miljön där intelligensen agerar. Russell och Norvig[5] definierar de fem faktorer som beskriver en problemmiljö: Fullt observerbar vs partiellt observerbar, deterministisk vs stokastisk, statisk vs dynamisk, diskret vs kontinuerlig och harmlös vs fientlig [min översättning]. Planeringsalgoritmer för kombinationen fullt observerbar, deterministisk, statisk, diskret och harmlös är mycket välundersökta och problem men den kombinationen av faktorer löses ofta av grafsökningsalgoritmer. Grafsökning har även tillämpats mycket framgångsrikt i partiellt observerbara och fientliga miljöer. Grafsökning blir dock problematiskt i miljöer med stokasticitet och dynamik, både på grund av att graferna lätt blir för stora för att hantera och för att det är svårt att med säkerhet minska på dem.

<br />

Markov-beslutsprocesser används i områden fullt observerbar, stokastisk, dynamisk, diskret och harmlös eller fientlig. Det finns även en variant av Markov-beslutsprocesser som kallas partiellt observerbara Markov-beslutsprocesser som kan användas i partiellt observerbara miljöer. Kombinationen stokastisk och dynamisk är intressant eftersom mycket i den verkliga världen har sådana parametrar. T.ex. en robots rörelser där stokasticitet kan uppstå på grund av hjulens bristande grepp, sensordata där stokasticiteten kan komma från misstolkningar eller störningar i mätningarna, eller planering där stokasticiteten kan orsakas av att miljön förändras mellan planeringsfasen och genomförandefasen. Eftersom stokastiska och dynamiska miljöer är så vanliga är det nödvändigt att det finns algoritmer för att artificiella intelligenser skall kunna funktionera i verkligheten.

<br />

För att implementera markov-beslutsprocesser effektivt så krävs det en del specifika hjälpmedel och vissa programmeringspråk är bättre lämpade än andra för detta ändamål. Jag har valt att undersöka programmeringspråket Scalas lämplighet genom att undersöka hur implementationer av Markov-beslutsprocesser i Scala ser ut. Jag valde Scala efter som det till ytan verkar som ett mycket lämpligt språk för artificiell intelligens programmering, och Markov-beslutsprocesser är ett intressant exempel på modern artificiell intelligens och därmed ett passande exempel för att illustrera de kraven som sätts på modern artificiell intelligensprogrammering. Scala har dessutom, så vitt jag vet inte använts till detta ändamål förr, i alla fall inte i allmän kännedom.

<br />

Programmeringsspråket Scala är ett nytt programmeringspråk vars första version lanserades år 2003. Namnet Scala kommer från orden "Scalable" (skalbar) och "Language" (språk), med skalbar menar Odersky att språket kan användas till både små och stora projekt. Språket i sig innehåller inslag av både det funktionella och det imperativa paradigmet och är implementerat för att köras i främst Java Virtual Machine (JVM) men det finns även en implementation av Scala för Microsofts .NET platform.[4].

<br />

Scalas fördelar för artificiell intelligens och speciellt markov-beslutsprocesser kommer troligen att ses bland annat i stödet för olika programmeringsparadigm, Akörmodell-samtidighet (Actor model concurrency) samt Scalas interoperabilitet med Java och dess rika programbibliotek och kompabilitet med existerande system.