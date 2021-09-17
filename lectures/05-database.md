---
layout: lecture
title: Databaser i molnet
lectureDate: Måndag den 20:e September 2021
permalink: /cloud-lectures/databases
---

Lektion 5 av 12

Oftast när vi bygger en applikation har vi ett behov att ha data på ett strukturerat sätt, vanligvis i någon sort av databas. Denna lektion introducera någon av dom databas funktioner som finns i Azure.

## Lektionsplan

{% include lectureplan.html lectureWeek=2 lectureDay=0 lectureCaption="Lektion från kl. 8:30 till kl. 16:30" %}

## Lektionslitteratur
*Detta är material (artiklar, videoer, blogs, podcasts etc) som är den teoretiska bas för denna lektion, det antas att du har läst/set/lystnad detta innan lektionen starter.*

Estimerat samlat "läs"-tid för lektionslittertur är **{{site.data.lecture_databaser_i_molnet.contentTimeTotal.literatureTime}} min** (för den frivilliga fördjupningslitteratur gäller {{site.data.lecture_databaser_i_molnet.contentTimeTotal.optionalLiteratureTime}} min)

{% include lecturenontopics.html lectureData="lecture_databaser_i_molnet" %}
{% include lecturetopics.html lectureData="lecture_databaser_i_molnet" %}

# Indviduella övningsuppgifter

Gå igennom dissa tre övningar, som är en del av kursen [Work with NoSQL data in Azure Cosmos DB](https://docs.microsoft.com/en-us/learn/paths/work-with-nosql-data-in-azure-cosmos-db/):
* [Create an Azure Cosmos DB database built to scale](https://docs.microsoft.com/en-us/learn/modules/create-cosmos-db-for-scale/), 35 min
* [Insert and query data in your Azure Cosmos DB database](https://docs.microsoft.com/en-us/learn/modules/access-data-with-cosmos-db-and-sql-api/)
* [Build a .NET Core app for Azure Cosmos DB in Visual Studio Code](https://docs.microsoft.com/en-us/learn/modules/build-cosmos-db-app-with-vscode/), 54 min
# Övningsuppgift

Ensamt eller fler tillsammans. Det rekomenderas att börja med bronze och sen gå på silver och på slutet guld. Silver och guld är frivilliga.

Skriv ett enkelt Azure Functions API som kan hämta och spara data i en databas som kör i molnet.

Du får välja vad APIet gör så länga dett involvera en databas, där finns möjlighet att bygge videre på denna applikation under resten av kursen.

Ett förslag är ett API som har en POST som kan lägga till en item till en lista som spara i databasen, och en GET som hämter ut alla värden i databasen.




**Brons (enkel):**
Azure function
sql server serverless

**Silver (meddel):**
Azure function
cosmos db

**Guld (avancerat):**
Azure funtion
cosmos db
build and deploy github actions

# Individuell inlämningsuppgift
## Blogg 05: Databaser i molnet

Gör ett nytt inlägg på din blog som du gjorde i samband med dom förra lektioner. Det rekomenderas att skriva på samma språk som din första blogg post.

Deadline på PingPong, tisdag den 21:e september kl 23:55. Posta ett länk till dagens blog post.

Skriv ett blogg post som följer denna lektion ska innehålla en text som svara på dissa frågor:
* 1
* 2

Om du vill kan du nu välja att dela denna blogpost på sociala media (Linked, Twitter, Facebook etc.) kom ihåg att använda lämpliga hashtags som: #1 #2