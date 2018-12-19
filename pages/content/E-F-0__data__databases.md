---
title: Databases
title_long: Databases
permalink: data/databases/
---

# Wat is een databank?

Een databank is een digitale verzameling van data welke je kan vergelijken met een bestand waarin gegevens opgeslagen en met elkaar verbonden worden.

Binnen een hogeschool kan men gebruik maken van een database die alle data bijhoudt die belangrijk zijn voor de onderwijsactiviteiten van de hogeschool. Denk daarbij aan de gegevens van de studenten, lectoren, lessen, lokalen, studiegelden,...

# Voordelen
- Je kan eemvoudig gegevens in de databank toevoegen.
- Het is eenvoudig om gegevens te wijzigen en verwijderen in de databank.
- Je kan snel gegevens opzoeken in de databank.
- Je kan filteren op gegevens.

# Onderdelen

Als je gegevens gaat bijhouden van specifieke objecten kan je dit gelijkstellen aan tabellen.
Elke eigenschap van het object komt dan overeen met een kolom.
En elk element van het type object zal dan overeenkomen met een rij in de tabel men noemt dit ook een record.

# RDBMS
RDBMS staat voor relational database management system en wijst op het relationele model van de data.
Meest gekende RDBMS is MySQL, Microsoft SQL Server, SQLite, Oracle,...

{% include shared/figure.html src="https://raw.githubusercontent.com/krisra/gdmgent-1819-csse1/master/images/RDBMS.png" alt="RDBMS" caption="RDBMS"%}


[Voorbeelden van RDBMS.](https://en.wikipedia.org/wiki/List_of_relational_database_management_systems)

# NoSQL
Een NoSQL databank verwijst naar een "niet-SQL" of "niet-relationele database".
Een NoSQL databank gaat voor het opslaan en ophalen van gegevens niet werken met tabellarische relaties zoals in een relationele databank

[Voorbeelden van NoSQL databanken](https://bigdata-madesimple.com/18-free-and-widely-used-open-source-nosql-databases/)

## Key-/Value-Stores
Bestaat uit een grote tabel van KV pairs.

Voorbeeld: 
- Amazon’s Dynamo

## Document Databases

Deze databank slaat documenten op welke samengesteld zijn door tagged elementen.

Voorbeelden:
- MongoDB
- Apache CouchDB

# Column-Oriented Databases
Elk blok bestaat uit gegevens afkomstig uit slechts één kolom.

Voorbeel:
- Google’s Bigtable

[Exploring the different types of NoSQL databases.](https://www.3pillarglobal.com/insights/exploring-the-different-types-of-nosql-databases)
[NoSQL explained.](https://www.mongodb.com/nosql-explained)