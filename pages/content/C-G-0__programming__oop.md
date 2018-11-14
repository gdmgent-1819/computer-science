---
title: OOP
title_long: Object geÖrienteerd Programeren
permalink: programming/oop/
---

# Wat is een object?
Een object is een exemplaar van een bepaalde klasse en bestaat uit de waarden van alle velden of attributen waarmee we een object definiëren. Objecten van dezelfde klassen beschikken steeds over dezelfde velden. De waarden van de velden kan per object verschillen.

De naam van een object start altijd met een kleine letter.

# Wat is een klasse?
Een klasse beschrijft de algemene kenmerken en een aantal algemene methodes van objecten van een bepaalde soort.
Men kan een instantie maken van een klasse welke men een object noemt.

De naam van een start altijd met een hoofdletter.
Uit een klasse kunnen we oneindig veel objecten maken.

Een klasse bestaat uit:
- velden (instance variables, variabele van alle types kunnnen hierbij)
- properties (voor bewerkingen uit te voeren op de velden)
- constructors (startwaarden voor de velden, initialisatie)
    - Een constructor is een methode waarvan de naam dezelfde is als de naam van de klasse.
    - De signatuur van de methode bevat enkel de methodenaam en de lijst van parameters, er is geen returntype aanwezig.
    - Een constructor heeft altijd de naam van de klasse.
    - Je kan meerdere constructors maken voor je klasse.
    - Een defaultconstructor is een constructor zonder parameters.
    - Telkens je een instantie maakt van een klasse zal de constructor uitgevoerd worden.
    - Het hangt ervan af hoeveel parameters je meegeeft om uit te maken welke constructor uitgevoerd zal worden.

{% highlight cs linenos %}
    public Person()
    {
    }
{% endhighlight %}    

{Referentie](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/constructors)

- methodes

{% highlight cs linenos %}
// Met onderstaande code maak je een klasse, 
// voorbeeld: Person.
public class Person
{
    // Fields
    // Defaultconstructor
    // Hieronder een voorbeeld van een defaultconstructor
    public Person()
    {
    }
    // Properties
    // Methods,...
}
{% endhighlight %}

# Overerving
Een klasse kan eigenschappen overnemen vanuit een andere klasse dit noemen we overerving.
Men spreekt dan van een basisklasse en een superklasse.

De basisklasse/superklasse is de hoogste klasse en de subklasse of afgeleide klasse bevat dan alle attributen en methodes van de superklasse.

[Referentie](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/inheritance)

# Polymorfisme
Een object kan voorkomen in meerdere gedaantes.
Het komt erop neer dat een object van een subklasse kan gezien worden als een element van een superklasse en dus ook de eigenschappen en methoden kan gebruiken van die superklasse of basisklasse.
Polymorfisme betekent letterlijk veelvormigheid.

[Referentie](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/polymorphism)

# Inkapsulatie of inkapseling
Bij inkapseling wil men ervoor zorgen dat men een of meer items gaat insluiten in een fysieke of logische package.
Hierbij ga je er voor zorgen dat er geen toegang is tot de details van de implementatie.

Encapsulation of inkapseling in OO ga je toepassen door gebruik te maken van access specifiers.
Een access specifier gaat definiëren wat de scope en visibiliteit is van een klasse member.

Volgende access specifiers zijn van toepassing:

- public, overal
- private, enkel in dezelfde klasse.
- protected, in dezelfde klasse of elke klasse die overerft van de klasse.
- internal, in dezelfde assembly, maar niet van een andere assembly.
- protected internal, in de assembly waar die gedeclareerd is of van een overervende klasse in een andere assembly.

# Wat is een struct?

Een struct is qua syntax hetzelfde als een klasse maar structs zijn beperkter dan klasses.
Even een overzicht van de verschillen:

- Structs zijn value types en klasses zijn reference types.
- Binnen een struct declaratie kunnen de velden of fields niet geintialiseerd worden tenzij deze gedeclareerd zijn als const of als static.
- Binnen een struct kan je geen default constructor declareren of een finalizer.
- Structs kunnen constructors bevatten met parameters.
- Als je een struct toewijst aan een nieuwe variabele dan zal alle data gekopieerd worden.
Bij wijziging van de nieuwe kopie zal de data in de originele kopie niet veranderen.
Dit belangrijk om weten wanneer je gebruik gaat maken van collections van value types zoals Dictionary<string, myStruct>.
- Je dient geen new te gebruiken zoals bij klassen wanneer je een instantie maakt van een struct.
- Je kan niet overerven van een andere struct of klasse, en het kan ook niet de basisklasse zijn van een klasse. Elke struct erft over van System.ValueType welke overerft van System.Object.
- Een struct kan interfaces implementeren.
- Een struct kan gebruikt worden als een nullable type and kan null waarde toegewezen worden.

{% highlight cs linenos %}
// Met onderstaande code maak je een struct, 
// voorbeeld: Postcode.
public struct Postcode
{
    // Fields
    // Properties
    // Methods,...
}
{% endhighlight %}

[Referentie](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/access-modifiers)