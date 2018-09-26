---
title: Datastructuren
title_long: Datastructuren
permalink: data/datastructures/
---

# Datacollecties

### Array
Een array is een collectie welke bestaat uit een vast aantal elementen van hetzelfde datatype.
Elk element in de collectie is een variabele en heeft een adres of ook wel index genoemd.
Doormiddel van de index kan je een waarde toekennen of opvragen.

Snelle toegang via een nummer. Grootte staat vooraf vast, resizen is duur. Een tweedimensionale array (toegang via twee nummers) heet een matrix.

Aanpassen van de grootte is moeilijk.

#### Een dimensionale array
Toegang via single index in een lineaire vorm.

{% highlight cs linenos %}
// Array met bedragen (double datatype), grootte van de array is 10.
double[] bedragen = new double[10];
// Array met getallen (int datatype), grootte van de array is 5.
int[] getallen = new int[5] { 1, 2, 3, 4, 5 };
// Opvragen van het 2de getal van de array getallen.
Console.WriteLine("Het 2de getal van de array getallen: {0}", getallen[1]);
// Waarde opgeven voor de 1ste en 2de plek in de array bedragen.
bedragen[0] = 2.50;
bedragen[1] = 4.12;
// Uitlezen van het 2de getal van de array bedragen.
Console.WriteLine("Het 2de getal van de array bedragen: {0}", bedragen[1]);
{% endhighlight %}


#### Multidimensionale array
Matrix van waarden van hetzelfde type men spreekt ook wel eens van arrays van arrays.

{% highlight cs linenos %}
// 2 dimensionale array
string[,] 2darray = new string[3, 2] { { "BMW", "520" }, { "Golf", "1,9 TDI" },
                                        { "Mercedes-Benz", "E 200" } };
// Afdrukken type van de Golf.
Console.WriteLine(2darray[1, 1]);
// 3 dimensionale array
int[, ,] getallen = new int[2, 2, 3] { { { 1, 2, 3 }, { 4, 5, 6 } }, 
                                       { { 7, 8, 9 }, { 10, 11, 12 } } };
{% endhighlight %}


[Referentie multidimensionale array](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/arrays/multidimensional-arrays)


Algemene referentie: [https://docs.microsoft.com/nl-nl/dotnet/api/system.array?view=netframework-4.7](https://docs.microsoft.com/nl-nl/dotnet/api/system.array?view=netframework-4.7)


#### BitArray
Een BitArray is een array bestaande uit bit waarden welke bestaan uit booleans. 

Referentie: [https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.bitarray?view=netframework-4.7](https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.bitarray?view=netframework-4.7)

{% highlight cs linenos %}
 bool[] booleans = new bool[5] { true, false, true, true, false };
 BitArray ba = new BitArray( booleans );
 Console.WriteLine("Aantal: {0}", booleans.Count );
 Console.WriteLine("Lengte: {0}", booleans.Length );
 {% endhighlight %}

### ArrayList
Is een datacollectie van een bepaalde object die geordend is.
Opvragen van een item kan via zijn index.
Het verschil met een array is dat je items kan toevoegen en verwijderen zonder de grootte aan te passen.
Sorteren, zoeken zijn ook mogelijk via methodes.

Referentie: [https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.arraylist?view=netframework-4.7](https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.arraylist?view=netframework-4.7)

{% highlight cs linenos %}
// Aanmaak arraylist met toevoeging van 3 elementen.
ArrayList al = new ArrayList();
al.Add("Hello");
al.Add("World");
al.Add("!");
// Opvragen van het 2de element.
Console.WriteLine("2de waarde:  {0}", al[1]);
// Het aantal, de capaciteit en de elementen opvragen.
Console.WriteLine("Aantal: {0}", al.Count );
Console.WriteLine("Capaciteit: {0}", al.Capacity );
{% endhighlight %}


### Lijst
Een lijst, list in C#, is een collectie welke bestaat uit een x aantal elementen van een bepaald object.
Elk element is toegankelijk via zijn index.
Zoeken, sorteren en manipuleren is mogelijk via voorziene methodes.

Referentie: [https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.generic.list-1?view=netframework-4.7](https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.generic.list-1?view=netframework-4.7)

{% highlight cs linenos %}
// Aanmaak van een lijst met strings.
List<string> namen = new List<string>();
// Toevoegen van namen tot de lijst.
namen.Add("Bart");
namen.Add("Geert");
namen.Add("Kristof");
Console.WriteLine();
foreach (string naam in namen)
{
    Console.WriteLine(naam);
}
Console.WriteLine("");
Console.WriteLine("Capaciteit: {0}", namen.Capacity);
Console.WriteLine("Aantal: {0}", namen.Count);
// Een elment verwijderen.
namen.Remove("Bart");
// Ledigen van lijst.
namen.Clear();
{% endhighlight %}

### Sortedlist
Dit is een datacollectie waarbij je gebruik kan maken van de key of de index om elementen op te vragen in de lijst.
Een SortedList is een combinatie van een hashtable (key) en een arraylist (index).
De collectie is gesorteerd via zijn key waarde.

Referentie: [https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.sortedlist?view=netframework-4.7](https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.sortedlist?view=netframework-4.7)

{% highlight cs linenos %}
 SortedList sl = new SortedList();
 sl.Add("B", "World");
 sl.Add("C", "!");
 sl.Add("A", "Hello");
 Console.WriteLine("Count:    {0}", mySL.Count );
 Console.WriteLine("Capacity: {0}", mySL.Capacity );
 Console.WriteLine("Key van 2de element: {0}", myList.GetKey(1));
 Console.WriteLine("Value van 2de element: {0}", myList.GetByIndex(1));
{% endhighlight %}

### Hashtable
Hashtable is een datacollectie die bestaat uit elementen van een bepaald datatype welke toegankelijk zijn via hun key.
Dit gebruik je best als je elementen wenst op te vragen aan de hand van een key.
Elk element in de hashtable bestaat uit een key/value paar.

Referentie: [https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.hashtable?view=netframework-4.7](https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.hashtable?view=netframework-4.7)

{% highlight cs linenos %}
Hashtable openenMet = new Hashtable();
openenMet.Add("rtf", "wordpad.exe");
openenMet.Add("jpg", "paint.exe");
openenMet.Add("txt", "notepad.exe");
openenMet.Add("pdf", "AcroRd32.exe");
openenMet["jpg"] = "Illustrator.exe";
Console.WriteLine("Opvragen waarde voor key jpg, waarde: {0}", openenMet["jpg"]);
Remove("pdf");
{% endhighlight %}

### Queue
Een queue is een FIFO collectie van een bepaald object, waarbij FIFO staat voor first-in, first-out.
Is handig als je een de items in de collectie wil raadplegen volgens het FIFO principe.
Wanneer je een item toevoegt tot de queue dan dien je enqueue uit te voeren, wanneer je een item wist van de queue dan dien je dit te doen via deque.

Referentie: [https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.queue?view=netframework-4.7](https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.queue?view=netframework-4.7)

{% highlight cs linenos %}
Queue q = new Queue();
q.Enqueue("Hello");
q.Enqueue("World");
q.Enqueue("!");
Console.WriteLine("Aantal: {0}", q.Count);
Console.WriteLine("Een element uitlezen: " + q.Dequeue(););
q.Enqueue("!");
{% endhighlight %}

### Stack
Een stack is een LIFO collectie van een bepaald object, waarbij LIFO staat voor last-in, first-out.
Wanneer je een item toevoegt tot de stack dan zal push moeten uitvoeren, wanneer je een item van de lijst wist dan zal je pop moeten uitvoeren (popping).

Referentie: [https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.stack?view=netframework-4.7](https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.stack?view=netframework-4.7)

{% highlight cs linenos %}
Stack st = new Stack();
st.Push("Hello");
st.Push("World");
st.Push("!");
Console.WriteLine("Aantal: {0}", st.Count );
Console.WriteLine( "Weergeven element, (Pop): {0}", st.Pop() );
Console.WriteLine( "Weergeven element, (Peek): {0}", st.Peek() );
{% endhighlight %}

### Associatieve array
Dictionary in C#; elementen in de datacollectie kan je zoeken via hun unieke key.

Referentie: 
- [Dictionary](https://msdn.microsoft.com/en-us/library/xfhwa508.aspx)
- [Dictionary Base](https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.dictionarybase?view=netframework-4.7)

{% highlight cs linenos %}
Dictionary<string, string> openenMet = new Dictionary<string, string>();
openenMet.Add("rtf", "wordpad.exe");
openenMet.Add("jpg", "paint.exe");
openenMet.Add("txt", "notepad.exe");
openenMet.Add("pdf", "AcroRd32.exe");
openenMet["jpg"] = "Illustrator.exe";
Console.WriteLine("Opvragen waarde voor key jpg, waarde: {0}", openenMet["jpg"]);
{% endhighlight %}

### HashSet
Je kan elementen in de hashset opzoeken doormiddel van hun unieke key.

Referentie: 
 - [HashSet](https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.generic.hashset-1?view=netframework-4.7)


{% highlight cs linenos %}
 HashSet<int> hs = new HashSet<int>();
 hs.Add(1);
 hs.Add(3);
 hs.Add(5);
 hs.Add(7);
 Console.WriteLine("Aantal: {0}", hs.Count);
 Console.Write("Elementen: ");
 Console.Write("{");
 foreach (int i in hs)
 {
     Console.Write(" {0}", i);
 }
 Console.WriteLine(" }");
{% endhighlight %}

### ConcurrentBag
Een concurrentbag is een datacollectie met waarden waar je resultaten kunt toevoegen en uitpikken.

Referentie: [https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.concurrent.concurrentbag-1?view=netframework-4.7](https://docs.microsoft.com/nl-nl/dotnet/api/system.collections.concurrent.concurrentbag-1?view=netframework-4.7)

{% highlight cs linenos %}
ConcurrentBag<int> cb = new ConcurrentBag<int>();
cb.Add(1);
cb.Add(3);
cb.Add(5);
cb.Add(7);
int element;
while (!cb.IsEmpty)
{
    if (cb.TryTake(out element))
        Console.WriteLine(element);
}
{% endhighlight %}