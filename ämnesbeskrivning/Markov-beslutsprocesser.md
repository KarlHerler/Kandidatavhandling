25.1.2012

<br />

#Markov-beslutsprocesser i Scala
Karl Herler, 34067


<br />&nbsp;

##Referat
---

Markov-beslutsprocesser är en typ av planeringsalgoritm innom artficiell intelligens som ofta används för att planera i situationer som innehåller en viss slump och osäkerhet (stochastisitet), t.ex. för att styra en robot i verkliga värden (där osäkerhet kan komma från störningar i sensorer eller handlingar som inte nödvändigtvis lyckas). Markov-beslutsprocesser har sin basis i Dolda markovmodeller och bayesisk sannolikhet. Målet med algorimen är att skapa en optimal "policy" för agenten* att agera efter för varje stadie den kan vara i. D.v.s. Att oberoende av vilket stadie agenten är i så har den en (optimal) "regel" för att agera för att förbättra sin situation, detta optimeringsproblem kan lösas antingen med hjälp av dynamisk programmering eller linjär programmering.

Scala är ett rätt så nytt programmeringspråk (första versionen lanserades 2003), som har fått sitt namn från orden "Scalable" (skalbar) och "Language" (språk). Språket i sig innehåller inslag från både funktionella och imperativa språk och är implementerat för att köras i antingen Java Virtual Machine (JVM) eller Microsoft .NET platform, jag kommer dock bara att se på JVM implementationen. Språket är mycket flexibelt och stöder många funktioner som är relevanta för 
modern AI programmering.

<br />


##Innehållsförteckning
---

1.  Inledning

2.  Markov-beslutsprocesser

	2.1. Varför Markov-beslutsprocesser (var används de?)

	2.2. Förkunskaper

	2.3. Markov-beslutsprocess algoritmen
	
	2.4. Varianter

3.  Scala

	3.1. Historia

	3.2. Grundläggande syntax


4.  Makrov-beslutsprocesser implementerade i Scala

	4.1. Naiv implementation

	4.2. Funkionell implementation

	4.3. Actor-concurrency


<br />

##2. Markov-beslutsprocesser
---

