# Agile Testing 1-3

Godt, kort og let forståeligt link, som forklarer om [Test driven development og Continiuous integration](https://www.agiledeveloper.com/articles/TDDPartIII.pdf) 

- Explain about Test Driven Development and how to use it with Continuous integration

Test driven development er en metode som går ud på, at man skriver sine tests før man skriver sin kode. Når man har skrevet testen, implementerer man koden lige akkurat så testen passer. Når testen passer, refaktorerer man designet, men uden at ændre det opstillede design. 

![](/week-9-11/ttd-illustration.jpg)

Fremgangsmåden er således: 

1. Skriv testen. 
2. Implementer koden således, at testen akkurat er grøn. 
3. Refactor.

Test driven development bygges op omkring tests, og i særdeleshed unit tests - automatiserede unit tests. Essensen for, at continious integration kan fungere er, at man har nogle gode, solide og stabile tests, som hjælper med, at man ikke pusher kode til produktion som ikke virker. Derfor fungerer TDD godt som med CI, da man her fra start af definerer de tests, som skal fungerer med ens CI system. 

--- 

- Explain Continuous Integration and principles/tools involved

Continuous integration bygger på princippet om, at man pusher små releases til produktionen hele tiden. 
I stedet for at lave få store ændringer i koden, releaser man så snart, at man er færdig med én task/feature. 
Dette gøres (som regel) ved brug af en bygge server, for eksempel Travis. Bygge serveren har til formål, at teste, alle tests og tjek er grønne, således, at man ikke pusher fejl/bugs til produktionen. Hermed også sagt, at det er nødvendigt med nogle gode test, da man ellers ofte vil komme til, at pushe noget til produktion, som eventuelt har ødelagt noget andet. 

* Unit tests. 
* Maven
* NPM
* Code reviews. 
* Dependency managers: Maven, Node/NPM.
* Shared code repository - Github. 
* Travis (build server). 
* Teamcity (build server)

--- 

- Explain why Maven (or similar tools) is a "great" match for CI via a Build Server, and elaborate on the properties we can take advantage of.



- Explain how to use separate test phases for Unit Tests and Integration Tests with Maven.
- Demonstrate CI, using Travis (or a similar build server), on a system involving, as a minimum:
	- Building the project
	- Running all Unit Tests 
	- Running all Integrations test, involving a real database
	- Creating Project Reports (Code Coverage, Test Results etc.)

Semester projektet. 

[Travis](https://travis-ci.org/hilleer/semester-project)
 
- Explain about Test-Driven Development  and its role as a design tool

Test driven development er en metode som går ud på, at man skriver sine tests før man skriver sin kode. Når man har skrevet testen, implementerer man koden lige akkurat så testen passer. Når testen passer, refaktorerer man designet, men uden at ændre det opstillede design. 

![](/week-9-11/ttd-illustration.jpg)

Fremgangsmåden er således: 

1. Skriv testen. 
2. Implementer koden således, at testen akkurat er grøn. 
3. Refactor.

Det er en avanceret teknik hvor man bruger automatiserede unit tests til, at drive designet af ens software og tvinge lav kobling mellem afhængigheder. 
Resultatet er, at man får en omfattende gruppe af unit tests, som kan til hver en tid kan gøre, og få feedback på, om systemet fungerer som det skal. 

Udover den overordnede fremgangsmåde, kan man også opstille det således:

1. **Rød:** Lav en test og få den til at fejle.
2. **Grøn:** Få testen til at pass, hvor alle midler er tilladte. 
3. **Refactor:** Optimer koden - optimer designet - sikre dig, at alle testene stadig passer. 

For at kunne arbejde med TTD, bliver man nødt til, at opbygge små let testlige funktioner/metoder, som iøvrigt har lav kobling, og som ofte ikke har nogen intern logik, således at de er lette at teste. 

Derudover er pointen, at man splitter ansvaret ud mellem funktionerne/metoderne, så der ikke er få funktioner/metoder som har for meget ansvar eller gør for mange ting. 

TTD hjælper også med, at abstrahere over usecasen på det absolut minimale niveau for, at den kan implementeres. Dette hjælper os med, at skrive kode som består af små simple kode fragmenter, som ikke er afhængige af hinanden, og som ikke bliver påvirket af, at vi andre et andet kode fragment. 

--- 

- Explain how agile development and testing differ from traditional approaches
- Explain the test activities in agile projects, including when which test activities are initiated
- Explain how risk is coped with in agile project as compared to traditional approaches
- Explain the roles and skills of a tester in agile projects
- Explain agile development and testing in the context of the Agile Manifesto’s 4 statements of values
	- Individuals and interactions 	over processes and tools 
	- Working software 		over comprehensive documentation 
	- Customer collaboration 		over contract negotiation 
	- Responding to change 		over following a plan

- Explain the Agile Testing Quadrants:

![the agile testing quadrants](/week-9-11/the-agile-testing-quadrant.png)