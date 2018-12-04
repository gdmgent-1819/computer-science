---
title: Fundamenten
title_long: Fundamenten
permalink: programming/fundamentals/
published: true
---
## Commentaar plaatsen.

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


### Overzicht rekenkundige operatoren.

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


### Overzicht tekenreeks operatoren.

| Operator | Omschrijving                             |
|:---------|:----------------------------------------:|
| +        | tekenreeksen worden hiermee samengevoegd |
|==========|==========================================|
{:.table.table-striped}


### Overzicht logische operatoren.

| Operator | Omschrijving |
|:---------|:------------:|
| !        | NOT          |
| &&       | AND          |
| \|\|       | OR           |
|==========|==============|
{:.table.table-striped}


### Overzicht relationele operatoren.

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


## Sequentie/opeenvolging.

Een sequentie is een opeenvolging van instructies die een voor een uitgevoerd worden in de volgorde waarin ze geschreven zijn.

Hieronder een voorbeeld van een sequentie:

{% highlight cs linenos %}
getValue();
checkValue();
saveValue();
{% endhighlight %}


## Keuze/selectie.

### Intro tot keuze.

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

### If-statement.

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

### IfElse-statement.

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

### IfElseIfElse-statement.

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

### Geneste IfElse-structuur.

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


### Switch-statement.

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

## Herhaling/iteratie.

Een iteratie zorgt ervoor dat je een opeenvolging van instructies een x aantal keren kunt herhalen.
Men spreekt ook wel van een lus of een herhaling.

Enkele voorbeelden: 
- Overlopen van een lijst.
- Vermenigvuldigingstafel opstellen.

### For loop.

Een for loop of ook wel begrensde herhaling is er op voorhand vastgelegd hoeveel keren de instructies herhaald moeten worden.

{% highlight cs linenos %}
    for (int i = 0; i < length; i++)
    {
        // instructie     
    }
{% endhighlight %}

### While loop.

{% highlight cs linenos %}
    while (true)
    {
            
    }
{% endhighlight %}

### Do While loop.

Met behulp van een Do While loop ga je ...

{% highlight cs linenos %}
    do
    {
            
     } while (true);
{% endhighlight %}

### ForEach loop.

Door middel van een ForEach loop ga je alle elementen in collectie overlopen.

{% highlight cs linenos %}
    foreach (var item in collection)
    {
            
    }
{% endhighlight %}

[Referentie](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/index)

