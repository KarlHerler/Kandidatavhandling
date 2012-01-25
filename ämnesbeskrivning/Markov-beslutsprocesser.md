25.1.2012

<br />

#Markov-beslutsprocesser i Scala
Karl Herler, 34067


<br />&nbsp;

##Referat
---

Markov-beslutsprocesser är en typ av planeringsalgoritm inom artficiell intelligens som ofta används för att planera i situationer som innehåller en viss slump och osäkerhet (stokastisitet), t.ex. för att styra en robot i verkliga världen, där osäkerhet kan komma från störningar i sensorer eller handlingar som inte nödvändigtvis lyckas. Markov-beslutsprocesser har sin basis i dolda markovmodeller och bayesisk sannolikhet. Målet med algoritmen är att skapa en optimal "policy" för agenten* att agera efter för varje stadie den kan vara i. D.v.s. Att oberoende av vilket stadie agenten är i så har den en (optimal) "regel" att agera efter för att förbättra sin situation.

Scala är ett rätt så nytt programmeringspråk (första versionen lanserades 2003). namnet Scala kommer från orden "Scalable" (skalbar) och "Language" (språk). Språket i sig innehåller inslag av både funktionella och imperativa språk och är implementerat för att köras i antingen Java Virtual Machine (JVM) eller Microsoft .NET platform. Språket är mycket flexibelt och stöder många principer som är relevanta för modern AI-programmering.


*) Agent = den artificella intelligensen samt dess "sensorer" och "aktuatorer"

<br />


##Innehållsförteckning
---

1.  Inledning

2.  Markov-beslutsprocesser

	2.1. Varför Markov-beslutsprocesser (var används de?)

	2.2. Förkunskaper

	2.3. Markov-beslutsprocessalgoritmen
	
	2.4. Varianter

3.  Scala

	3.1. Historia

	3.2. Grundläggande syntax


4.  Markov-beslutsprocesser implementerade i Scala

	4.1. Naiv implementation

	4.2. Funktionell implementation

	4.3. Actor-concurrency


<br />

##Litteraturlista
---

[1] LaValle, M. Steven, Planning Algorithms. Cambridge University Press 2009

[2] Luger, F. George, Artificial Intelligence: Structures and strategies for complex problem solving, Sixth Edition. Pearsons 2009

[3] Luger, F. George, Stubblefield, A. William, AI Algorithms, Data structures, and Idioms in Prolog, List, and Java. Pearsons 2009

[4] Odersky, Martin, Spoon, Lex, Venners, Bill, Programming in Scala, Second Edition. Artima 2010

[5] Russell, Stuart, Norvig, Peter, Artificial Intelligence: A Modern Approach, Second Edition. Pearsons 2003

[6] Scala Standard Library 2.9.1.final. [http://www.scala-lang.org/api/current/index.html](http://www.scala-lang.org/api/current/index.html). Hämtad 25.1.2012

