---
title: Fundamenten
title_long: Fundamenten
permalink: programming/fundamentals/
published: true
---
## Commentaar plaatsen

Het is aanbevolen je broncode altijd te voorzien van commentaar zodat je later gemakkelijk wijzigingen kunt uitvoeren en de broncode ook leesbaar/begrijpbaar is voor anderen.

Commentaar in C# kunnen we doen door volgende tekencombinatie // voorop onze commentaar te plaatsen.

Je kan kiezen voor 1 regel commentaar of voor meerdere regels commentaar:

{% highlight cs linenos %}
// 1 regel commentaar

/*
    Meerdere
    regels
    commentaar.
*/
{% endhighlight %}

## Operatoren

In code worden er dikwijls veel berekeningen uitgevoerd, elementen met elkaar vergelijken of logische keuzes gemaakt worden.
Hieronder kan je de operatoren vinden in groep.


Overzicht rekenkundige operatoren
---------------------------------

| Operator | Omschrijving             |
|:---------|:------------------------:|
| ++       | waarde verhogen met 1    |
| --       | waarde verminderen met 1 |
| x + y    | som                      |
| x - y    | verschil                 |
| x / y    | delen                    |
| x * y    | vermenigvuldigen         |
| x % y    | rest na deling           |
| +x, -x   | veranderen van teken     |
|==========|==========================|
{:.table.table-striped}


Overzicht tekenreeks operatoren
-------------------------------

| Operator | Omschrijving                             |
|:---------|:----------------------------------------:|
| +        | tekenreeksen worden hiermee samengevoegd |
|==========|==========================================|
{:.table.table-striped}


Overzicht logische operatoren
--------------------------------

| Operator | Omschrijving |
|:---------|:------------:|
| !        | NOT          |
| &&       | AND          |
| ||       | OR           |
|==========|==============|
{:.table.table-striped}


Overzicht relationele operatoren
--------------------------------

| Operator | Omschrijving                 |
|:---------|:----------------------------:|
| x == y   | is gelijk aan                |
| x != y   | is niet gelijk aan           |
| x > y    | is groter dan                |
| x < y    | is kleiner dan               |
| x >= y   | is groter dan of gelijk aan  |
| x <= y   | is kleiner dan of gelijk aan |
|==========|==============================|
{:.table.table-striped}


## Sequentie/opeenvolging

Een sequentie is een opeenvolging van instructies die een voor een uitgevoerd worden in de volgorde waarin ze geschreven zijn.

Hieronder een voorbeeld van een sequentie:

{% highlight cs linenos %}
getValue();
checkValue();
saveValue();
{% endhighlight %}


## Keuze/selectie

### Intro tot keuze

Een selectie of keuze wordt meestal uitgevoerd door gebruik te maken van het “if-statement”. 
Afhankelijk van het resultaat van het "if-statement" zal de handeling tussen de accolades {}, na de if, al dan niet uitgevoerd worden.

We kunnen dus een keuze coderen door middel van een voorwaarde:

*if* voorwaarde
*then* handeling uitvoeren als aan voorwaarde voldaan is
*else* else-component
*endif*

Als er aan de voorwaarde voldaan is dan zal code uitgevoerd worden dus in het then deel aanwezig is, tussen de accolades {} na de voorwaarde.
Indien niet aan de voorwaarde is voldaan dan zullen de handelingen aanwezig in het else deel uitgevoerd worden.
De voorwaarde van het "if-statement" kan zowel bestaaan uit een enkelvoudige als uit een samengestelde logische formulering, zie relationele en logische operatoren.

### If-statement

{% highlight cs linenos %}
int getal = 0;
Console.WriteLine("Geef een getal in tussen 0 en 5");
getal = Convert.ToInt32(Console.ReadLine());

if (getal > 0)// conditie of voorwaarde
{
    // statements
    Console.WriteLine("Het getal is groter dan 0!");
}
{% endhighlight %}

De conditie of voorwaarde is een logische formulering (true of false als resultaat) waaraan voldaan dient te worden (true als resultaat van de conditie), om de statements tussen accolades uit te voeren, is dat de waarde van de integer variabele getal groter dient te zijn dan 0.
Als de conditie een true oplevert dan zal het statement uitgevoerd worden om volgende lijn af te drukken in de console: Het getal is groter dan 0!
Als de conditie een false oplevert zal het programma de lijnen code uitvoeren na de accolade van het if-statement.

### IfElse-statement

{% highlight cs linenos %}
int getal = 0;
Console.WriteLine("Geef een getal in tussen 0 en 5");
getal = Convert.ToInt32(Console.ReadLine());

if (getal > 0)// conditie of voorwaarde
{
    // statements
    Console.WriteLine("Het getal is groter dan 0!");
}
else
{
    // statements
    Console.WriteLine("Het getal is niet groter dan 0!");
}
{% endhighlight %}

De conditie of voorwaarde is een logische formulering (true of false als resultaat) waaraan voldaan dient te worden (true als resultaat van de conditie), om de statements tussen accolades uit te voeren, is dat de waarde van de integer variabele getal groter dient te zijn dan 0.
Als de conditie een true oplevert dan zal het statement uitgevoerd worden om volgende lijn af te drukken in de console: Het getal is groter dan 0!
Als de conditie een false oplevert zal het programma de lijnen code uitvoeren na de accolade van het else-statement.

### IfElseIfElse-statement

{% highlight cs linenos %}
int getal = 0;
Console.WriteLine("Geef een getal in tussen 0 en 5");
getal = Convert.ToInt32(Console.ReadLine());

if (getal > 0)// conditie of voorwaarde
{
    // statements
    Console.WriteLine("Het getal is groter dan 0!");
}
else if (getal == 5)
{
    // statements
    Console.WriteLine("Het getal is gelijk aan 5!");
}
else
{
    // statements
    Console.WriteLine("Het getal is niet groter dan 0!");
}
{% endhighlight %}

Zoals in bovenstaand voorbeeld is te zien kan men ook nog opteren om de ifelse uit te breiden met een elseif zodat je hierbij een extra keuze kan toevoegen tot je klassieke ifelse-structuur.

### Geneste IfElse-structuur

Bij een geneste IfElse-structuur is het zo dat je meerdere controlestructuren gaat hebben op verschillende niveaus.
Hieronder kan je een voorbeeld vinden van een geneste IfElse-structuur.

{% highlight cs linenos %}
int getal = 0;
Console.WriteLine("Geef een getal in tussen 0 en 5");
getal = Convert.ToInt32(Console.ReadLine());

if (getal > 0)// conditie of voorwaarde
{
    // statements
    if (getal < 5)
    {
        // statements
        if(getal >= 1 && getal < 4)
        {
            Console.WriteLine("Het getal is kleiner dan 5!");    
        } 
    }
    else if(getal == 5)
    {
        Console.WriteLine("Het getal is gelijk aan 5!");
    }
    else
    {
        // statements
        Console.WriteLine("Het getal is groter dan 0!");
    }
}
{% endhighlight %}


### Switch-statement

Vanaf je meer dan 2 keuzemogelijkheden dient in te bouwen is de switch-structuur efficiënter. 

De switch-opdracht heeft de algemene structuur:

{% highlight cs linenos %}
            switch (getal) // integer expressie
            {
                case 1: // constant expressie
                    Console.WriteLine("Het getal is 1."); //statement
                    break; //jump statement
                case 2:
                    Console.WriteLine("Het getal is 2.");
                    break;
                case 3:
                case 4:
                    Console.WriteLine("Het getal is 3 of 4.");
                    break;
                case 5:
                    Console.WriteLine("Het getal is 5.");
                    break;
                default:
                    Console.WriteLine("Het getal is een ander getal... :-(");
                    break;
                    
            }
{% endhighlight %}

De expressie, welke achter switch staat, van de switch-structuur is meestal een variabele.
De waarde van de variabele gaat dan vergeleken worden met de constant expressie.
Als de waarde overeenstemt met een bepaalde constant expressie, voorbeeld case 5, dan zal het statement na de constant expressie uitgevoerd worden.
Elke mogelijkheid, case x dus, eindigt met het jump-statement waar men break; plaatst.
break; zal er voor zorgen dat er geen code meer zal uitgevoerd worden van de switch-structuur na de break; indien de case in kwestie uitvoerbaar is.

Goed om weten:
- Bij een een switch kan je geen rekenkundige of logische operatoren gebruiken.
- Bij case kan je enkel waarden meegeven.
- Een case werkt niet met bereiken, voorbeeld: 5-8.
- Je kan wel een case definieren voor 2 mogelijkheden, zoals bij het voorbeeld hierboven waarbij hetzelfde mag uitgevoerd worden voor case 3 en 4.


Referentie: [https://nl.wikibooks.org/wiki/Programmeren,_de_basis/De_controlestructuren](https://nl.wikibooks.org/wiki/Programmeren,_de_basis/De_controlestructuren)

## Herhaling/iteratie

Een iteratie zorgt ervoor dat je een opeenvolging van instructies een x aantal keren kunt herhalen.
Men spreekt ook wel van een lus of een herhaling.

Enkele voorbeelden: 
- Overlopen van een lijst.
- Vermenigvuldigingstafel opstellen.

### For loop

Een for loop of ook wel begrensde herhaling is er op voorhand vastgelegd hoeveel keren de instructies herhaald moeten worden.

{% highlight cs linenos %}
    for (int i = 0; i < length; i++)
    {
        // instructie     
    }
{% endhighlight %}

### While loop

{% highlight cs linenos %}
    while (true)
    {
            
    }
{% endhighlight %}

### Do While loop

{% highlight cs linenos %}
    do
    {
            
     } while (true);
{% endhighlight %}

### ForEach loop

{% highlight cs linenos %}
    foreach (var item in collection)
    {
            
    }
{% endhighlight %}

[Referentie](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/index)

# Wat is een methode?
Een methode of procedure is een reeks van commando's welke in volgorde uitgevoerd worden. Een methode geeft geen returnwaarde terug.

Elk C# programma bestaat ten minste uit 1 klasse met een methode Main.

# Wat is een functie?
Hetzelfde als een methode met dat verschil dat een functie wel een waarde teruggeeft wel spreken in dat geval van een return.

# Argumenten

De argumenten van een procedure kunnen By Value of By Reference doorgegeven worden.

- By Value (ByVal): hierbij is de waarde (inhoud) van de variabele doorgegeven en niet de varibele zelf. De procedure kan de inhoud van de variabele niet wijzigen.
- By Reference (ByRef): de referentie (of verwijzing) naar de waarde is hierbij doorgegeven. De waarde van de variabele kan hierbij aangepast worden in de functie.

Standaard worden variabelen doorgegeven By Value. 
Het is uitzonderlijk om variabelen By Reference door te geven.
Voor de performantie te verhogen kunnen we wel opteren om variabelen By Reference door te geven.

# Signatuur
De signatuur van een methode of functie bestaat uit de naam, het aantal en het type van argumenten.

# Overloading
Methodes met dezelfde naam maar verschil in aantal of types argumenten.


# Waaruit bestaat een methode/functie:
- Access specifier
    Men spreekt ook wel van access modifiers.
    - public, overal
    - private, enkel in dezelfde klasse
    - protected, in dezelfde klasse of elke klasse die overerft van de klasse
    - internal, in dezelfde assembly, maar niet van een andere assembly.
    - protected internal, in de assembly waar die gedeclareerd is of van een overervende klasse in een andere assembly.
Referentie:    [https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/access-modifiers](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/access-modifiers)
- Return type
    - void => in dit geval spreken we van een methode.
    - int, string,... als returntype => in dit geval spreken we van een functie.
- Methodenaam
- Parameters
    - Tussen de (), type, volgorde, aantal.
- Inhoud van de methode
    - Volgorde van instructies om uit te voeren.

### Interfaces

Een interface bevat de definities van een groep van gerelateerde functionaliteiten die een klasse of een struct kan implementeren.

Voor een interface dien je het keyword interface te gebruiken.
De naam van de interface dient te starten met een hoofdletter I.
De interface in het voorbeeld hieronder voorziet in een definitie van een functie accountActive.

{% highlight cs linenos %}
interface IAccount
{
    bool accountActive(Account a);
}
{% endhighlight %}

Wat is het verschil tussen een interface en een abstract klasse?
Wat is het voordeel van een interface bij overerving?

[Referentie](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/interfaces/)

### Exceptions
Een exception is een fout die gegooid wordt via keyword [throw](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/throw).
De type exception hangt af van de fout die opgetreden is.

Je kan zelf een exception gooien op volgende manier:
{% highlight cs linenos %}
throw new NotImplementedException();
throw new IndexOutOfRangeException
{% endhighlight %}

### Try-catch
Je kan een exception opvangen door rond de code die je wenst uit te voeren een [try-catch](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/try-catch) te zetten.

De code dient dus in de try te komen en het opvangen van eventuele exceptions dien je in het catch blok te behandelen.
Wil je verschillende types van exceptions opvangen dan kan je opteren voor verschillende catches te schrijven ofwel geef je geen argument mee tussen de haakjes en dan vang je alle exceptions op.

{% highlight cs linenos %}
object o = null;  
try  
{  
    int i = (int)o;   // Error  
}
catch (InvalidCastException e)   
{  
    Console.WriteLine(e.);
}
{% endhighlight %}

### Try-finally

Als je bepaalde handelingen wenst uit te voeren die niet geïmpacteerd mogen geraken door een exception, dan opteer je voor een finally blok te plaatsen.

{% highlight cs linenos %}
int i = 123;
string s = "tekst";
object obj = s;

try
{
    i = (int)obj;
    Console.WriteLine("Einde van try.");
}
finally
{
    Console.WriteLine("Uitvoeren van finally blok na het optreden van een exception.");
    Console.WriteLine("i: {0}", i);
}
{% endhighlight %}

### Try-catch-finally
Als je de combinatie van alle 3 wenst dien je de 3 blokken toe te voegen.

{% highlight cs linenos %}
int i = 123;
string s = "tekst";
object obj = s;

try
{
    i = (int)obj;
    Console.WriteLine("Einde van try.");
}
catch
{
    Console.WriteLine("!EXCEPTION!");
}
finally
{
    Console.WriteLine("Uitvoeren van finally blok na het optreden van een exception.");
    Console.WriteLine("i: {0}", i);
}
{% endhighlight %}



Referenties:
[Exception handling](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/exception-handling-statements)

- Waarvoor dient een exception?
- Van welke klasse dien je over te erven om een custom Exception aan te maken?
- Hoe vang je een exception op?
- Het verschil tussen een try-catch en een try-finally?