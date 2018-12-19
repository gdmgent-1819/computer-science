---
title: Dataformaten
title_long: Dataformaten
permalink: data/dataformats/
published: false
---

Wat is een dataformaat?
-----------------------
Een dataformaat is de manier waarop gegevens of informatie worden gecodeerd en opgeslagen. 
Een gegevensformaat (of bestandsformaat) geeft informatie over het verwerken van de gegevens.

# De meest voorkomende dataformaten:
- JSON
- XML
- CSV

# JSON of voluit JavaScript Object Notation.

JSON is uitgevonden in 2001 en werd populair vanwege Yahoo en Google in 2005 - 2006, en is een alternatief voor XML. Net als XML kan je een hiërarchische gegevensstructuur hanteren met behulp van komma's, accolades en haakjes.

Voorbeeld van lijst bomem in JSON-formaat:

{% highlight json linenos %} 
{“naam”:”eik”,”vruchten”:”eikels″},
{“name”:”kastanje”,”vruchten”:”kastanjes″}
{% endhighlight %}

## Voordeel
- JSON is een dataformaat dat een hiërarchische gegevensstructuur ondersteunt terwijl ze kleiner zijn dan het XML-formaat.
- Zoals de naam aangeeft is JSON ook gemaakt om eenvoudig te gebruiken in native Javscript-objecten, waardoor we zeer nuttig zijn voor webtoepassingen.
- JSON is het beste van beide werelden met betrekking tot XML en CSV.
Het is eenvoudig en compact zoals CSV maar ondersteunt een hiërarchische gegevensstructuur zoals XML. 
- In tegenstelling tot XML zijn JSON-formaten slechts ongeveer even groot als CSV-formaten.

## Nadeel
Het JSON dataformaat had vroeger iets minder ondersteuning dan XML. Omdat JSON relatief jonger is dan XML, waren er minder API's om JSON automatisch te converteren naar native datastructuren. Dit is nu veel minder het geval doordat nieuwere API's zowel XML als JSON ondersteunen.

# XML of voluit Extensible Markup Language.
XML is ontstaan in 1996 en is officieel een W3C standaard geworden in 1998. XML is ontwikkeld om dataformaten met een hiërarchische structuur weer te geven.

Voorbeeld van lijst van bomen in XML-formaat:

{% highlight xml linenos %} 
<boom>
<naam>eik</naam>
<vruchten>eikels</vruchten
<maxHoogte>30</maxHoogte>
</boom>
<boom>
<naam>kastanje</naam>
<vruchten>kastanjes</vruchten>
<maxHoogte>35</maxHoogte>
</boom>
{% endhighlight %}

## Voordeel
- Het XML-formaat ondersteunt hiërarchische gegevensstructuren en is geschikt voor het ontvangen van complexe gegevens als reactie.
- Het XML-formaat is perfect leesbaar voor mensen.
- Browsers hebben ingebouwde XML lezers waarmee je XML-bestanden kan inspecteren.
- XML was de eerste standaard voor hiërarchische gegevensindeling waardoor de meeste API's ingebouwde functionaliteit hadden om data automatisch te converteren naar native datastructuren.

## Nadeel
- Het XML-formaat is drie keer wo groot als een CSV-formaat.
Dit komt omdat elk element verpakt zit in een bijhorende tag (open- en sluittag van het element).

# CSV of voluit Comma Separated Values.
Zoals de naam doet vermoeden bestaat dit dataformaat uit een lijst van elementen die gescheiden zijn door een komma.

Voorbeeld van lijst van bomen in CSV-formaat:
``` csv
eik,kastanje,linde,beuk

## Voordeel
Dit formaat is de meest compacte van de drie formaten.
Algemeen kunnen beschouwen dat de CSV-indeling ongeveer de helft van grootte is dan de XML- en/of JSON-indeling.
Dit is dan ook het grootste voordeel van CSV omdat het inderdaad kan helpen voor het verminderen van de bandbreedte.

## Nadeel
- De CSV is het minst veelzijdige formaat van de drie.
Dit komt doordat je een zelfgemaakte parser nodig hebt om de gegevens uit de CSV om te zetten in een eigen gegevensstructuur. Indien er dan iets wijzigt aan de gegevensstructuur is er sprake van een overhead vanwege het terug wijzigen of opnieuw ontwerpen van de parser.
Men dient hierna ook het programma aan te passen op de verschillende plaatsen zodat er geen incompatibiliteitsproblemen voorkomen.

- CSV ondersteunt geen hiërarchie in de data.
Wat als je per boom extra attributen wenst door te geven?
In dat geval zal je moeten voorzien in een complexere parser die weet welke elementen van de CSV overeenkomen met een bomen en welke elementen overeenkomen met attributen van bomen.
Een mogelijke oplossing om dan gebruik te maken van een ander scheidingsteken zoals een puntkomma (;) om elk attribuut van een boom te scheiden.

Voorbeeld van lijst van bomen met attributen in CSV-formaat:
``` csv
eik;eikels;30,kastanje;kastanjes;35,linde,beuk;beukennoten;22

//[Referentie voorbeelden code repo.](https://github.com/gdmgent/1718-csse-code/tree/master/week02)