---
title: Datatypen
title_long: Datatypen
permalink: data/datatypes/
published: true
---

## Wat is data?

Data is een gegevensverzameling, ook wel dataset genoemd welke in de meeste gevallen gepresenteerd is in een tabelvorm.

Waarbij de rijen, ook wel records genoemd, in de tabel overeenstemt met een lid uit de gegevensverzameling.

De kolom stemt overeen met een variabele.
Elke rij bevat een waarde voor de verschillende variabelen of attributen.

Voorbeelden van variabelen: datum, tijdstip, getal, tekst,...

Een dataset heeft verschillende kenmerken welke de eigenschappen en structuur bepalen zoals onder andere het datatype van de variabelen, het aantal variabelen

Andere vormen van datasets welke geen tabelvorm zijn: XML, JSON,...

De waarden kunnen getallen zijn, maar ook gegevens van nominaal of ordinaal niveau zijn. Voor elke variable zullen normaal gesproken de waarden van hetzelfde niveau zijn, al kunnen er wel gegevens ontbreken, wat op een of andere manier dient te worden aangegeven.


# Datatypes

Een datatype of gegevenstype is een specifieke soort van data, het datatype bepaalt welke waarde de variabele kan bevatten.

De datatypes kan je verdelen in primitieve, enkelvoudige en samengestelde datatypes.

## Primitieve datatypes.

Een primitief datatype is gedefinieerd door de programmeertaal zelf.

Meest voorkomende primitieve datatypes:
- Boolean
- Char
- Integer
- Double
- Decimal

Overzicht
---------

| Verkorte naam | .NET Class en type | Bereik | Grootte | Standaardwaarde |
|:---------|:--------:|:--------:|:--------:|---------:|
|Gehele getallen |  |  |  |
|----------|----------|----------|----------|----------|
| byte     | Byte, unsigned integer | 0 tot 255 | 8 | 0 |
| sbyte    | SByte, signed integer | -128 tot 127 | 8 | 0 |
| int      | Int32, signed integer | -2.147.483.648 tot 2.147.483.647 | 32 | 0 |
| uint     | UInt32, unsigned integer | 0 tot 4.294.967.295 | 32 | 0 |
| short    | Int16, signed integer | -32.768 tot 32.767 | 16 | 0 |
| ushort   | UInt16, unsigned integer | 0 tot 65535 | 16 | 0 |
| long     | Int64, signed integer | -9.223.372.036.854.775.808 tot 9.223.372.036.854.775.807 | 64 | 0 |
| ulong    | UInt64, unsinged integer | 0 tot 18.446.744.073.709.551.615 | 64 | 0 |
| =========|==========|==========|==========|==========|
|Reële getallen |  |  |  |  |
|----------|----------|----------|----------|----------|
| float    | Single, single-precision floating point type | -3,402823e38 tot 3,402823e38 | 32 | 0.0F |
| double   | Double, double-precision floating point type | -1,79769313486232e308 tot 1,79769313486232e308 | 64 | 0.0D |
| decimal  | Decimal, Precise fractional or integral type that can represent decimal numbers with 29 significant digits | ±1.0 × 10e−28 tot ±7.9 × 10e28 | 128 | 0.0M |
| =========|==========|==========|==========|==========|
|Tekst     |  |  |  |  |
|----------|----------|----------|----------|----------|
| string   | String, tekenreeks |  |  |  |
| =========|==========|==========|==========|==========|
|Andere types |  |  |  |  |
|----------|----------|----------|----------|----------|
| char     | Char, 1 unicode karakter | U +0000 tot U +ffff | 16 | '\0' |
| bool     | Boolean, True (1) of False (0) | True (1) of False (0) | 8 | False (0) |
| object   | Object, basistype van alle andere types |  | | 
| =========|==========|==========|==========|==========|
{:.table.table-bordered}

{% include shared/figure.html src="https://raw.githubusercontent.com/krisra/gdmgent-1819-csse1/master/images/datatypes.png" alt="Datatypes" caption="Datatypes"%}

## Enkelvoudige datatypes.

Is een primitief datatype, ook wel simpel datatype genoemd, of een datatype gedefinieerd op basis van een primitief datatype. De voorwaarde is dat een enkelvoudig datatype enkel als geheel kan worden uitgelezen en/of gemanipuleerd.

## Samengestelde datatypes.

Samengestelde datatypes of complexe datatypes bestaan uit meerdere simpele types die afzonderlijk kunnen worden gemanipuleerd en uitgelezen. 

Deze structuren welke resulteren in arrays, klasse, lijsten,... die samengesteld zijn uit elementen die op zichzelf ook kunnen bestaan uit samengestelde datatypes zoals lijsten van lijsten, geneste structuren,...

### String
Is een reeks van karakters.

### Conversie
Converteren van datatype wil eigenlijk zeggen dat je het huidige datatype wil wijzigen in een ander datatype.

#### Convert klasse.
Uitvoeren van een conversie kan je doen via de Convert klasse.
Je kan bijvoorbeeld een double waarde in een sbyte datatype steken.

{% highlight cs linenos %}
    sbyte csb = Convert.ToSByte(2.41255);
    Console.WriteLine("Converteren van double naar sbyte: {0}", csb);
{% endhighlight %}

[Referentie Convert klasse](https://msdn.microsoft.com/en-us/library/system.convert.aspx)
[Referentie Convert methodes](https://msdn.microsoft.com/en-us/library/system.convert_methods.aspx)

#### Impliciete en expliciete conversie.
{% highlight cs linenos %}
int r = 5.0; // Geen impliciete conversie voor double naar int.
int s = (int)5.0; // Expliciete conversie.
{% endhighlight %}