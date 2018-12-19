---
title: Documenteren
title_long: Documenteren
permalink: programming/documenting/
---

Documenteren van code.
----------------------

Het is aanbevolen je broncode altijd te documenteren, door te voorzien in commentaarlijnen zodat je later gemakkelijk wijzigingen kunt uitvoeren (onderhoudbaarheid) en de broncode ook leesbaar/begrijpbaar is voor anderen.

Ondanks een veelvoorkomend misverstand wordt het documenteren van code niet gebruikt om te beschrijven wat de code doet maar wel hoe dit gebeurt.

## Commentaar (single line en multi line) in C#.

Het plaatsen van commentaar in C# kunnen we doen door volgende tekencombinatie // (2 slashes) voor onze commentaartekst te plaatsen.

Je kan kiezen voor 1 regel commentaar of voor meerdere regels commentaar:

{% highlight cs linenos %}
// 1 regel commentaar

/*
    Meerdere
    regels
    commentaar.
*/
{% endhighlight %}

## Commentaar ter documentatie (XML).

Een stap verder is XML commentaar ter documentatie en ziet er bijna hetzelfde uit als gewone commentaar, maar dan met embedded XML. Hierbij kan je ook zowel single line als multi line commentaar gebruiken. 
Je schrijft ze op dezelfde manier als gewone commentaar, maar met een extra karakter. 
Single line XML commentaar ter documentatie gebruikt 3 slashes (///) in plaats van 2. 
De multi line variant gebruikt een extra asterisk (*). 

{% highlight cs linenos %}
class Gebruiker
{
    /// <summary>
    /// De Naam van de Gebruiker.
    /// </summary>
    public string Naam { get; set; }

    /**
    * <summary>De Leeftijd van de Gebruiker.</summary>
    */
    public string Leeftijd { get; set; }
}
{% endhighlight %}

Hierboven zie je beide vormen. De eerste variant met gebruik van 3 slashes (///) wordt meestal gebruikt voor commentaar ter documentatie.

{% include shared/figure.html src="https://raw.githubusercontent.com/krisra/gdmgent-1819-csse1/master/images/documentatie-gebruiker0.png" alt="Voorbeeld XML documentatie van broncode." caption="Voorbeeld XML documentatie van broncode."%}


{% include shared/figure.html src="https://raw.githubusercontent.com/krisra/gdmgent-1819-csse1/master/images/documentatie-gebruiker1.png" alt="Voorbeeld IntelliSense." caption="Voorbeeld IntelliSense."%}


Hierbij een overzicht van de best pratices:
- Omwille van de consistentie dien je alle publiek zichtbare types en members te documenteren. Als je het moet doen, doe het dan voor alles.
- Private members kunnen ook gedocumenteerd worden via XML commentaar.
Dit zorgt er wel voor dat de innerlijke (mogelijk vertrouwelijke) werking vrijgegeven wordt van uw code.
- Een echt minimum moet zijn dat types en hun members een <summary>-tag hebben omdat die informatie nodig is voor de IntelliSense.
- De tekst in documentatie dient te bestaan uit volledige zinnen en eindigen met een punt.
- Gedeeltelijke klassen worden volledig ondersteund en documentatie wordt samengevoegd tot één item voor dat type.
- De compiler verifieert de syntax van de <exception>, <include>, <param>, <see>, <seealso> en <typeparam> tags.
- De compiler valideert de parameters die bestandspaden en verwijzingen naar andere delen van de code.

[Referentie XML documentation comments.](https://docs.microsoft.com/en-us/dotnet/csharp/codedoc)

## Takenlijst via commentaar.

Je kan een takenlijst samenstellen door in commentaar deze items toe te voegen, je dient deze lijn wel te starten met de single line commentaar als startsequentie direct gevolgd door TODO, FIXME, NOTE, HACK.

Hieronder een voorbeeld:
{% highlight cs linenos %}
    Gebruiker g = new Gebruiker();
    //TODO: het instellen van de naam van de gebruiker...
    //FIXME: eventueel een constructor voorzien in de klasse Gebruiker...
{% endhighlight %}

In de Todo view, als je gebruik maakt van de Todo+ extensie in Visual Studio Code, krijg je dan een overzicht van de items volgens categorie en dit per bestand.

{% include shared/figure.html src="https://raw.githubusercontent.com/krisra/gdmgent-1819-csse1/master/images/documentatie-gebruiker3.png" alt="Voorbeeld takenlijst in broncode via Todo+." caption="Voorbeeld takenlijst in broncode via Todo+."%}

{% include shared/figure.html src="https://raw.githubusercontent.com/krisra/gdmgent-1819-csse1/master/images/documentatie-gebruiker2.png" alt="Voorbeeld takenlijst in broncode via TODO Highlight." caption="Voorbeeld takenlijst in broncode via TODO Highlight."%}

[Referentie extensie TODO Highlight.](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight)
[Referentie extensie Todo+.](https://marketplace.visualstudio.com/items?itemName=fabiospampinato.vscode-todo-plus)