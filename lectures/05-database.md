---
layout: lecture
title: Databaser i molnet
lectureDate: Måndag den 20:e September 2021
permalink: /cloud-lectures/databases
---

Lektion 5 av 12

Oftast när vi bygger en applikation har vi ett behov att ha data på ett strukturerat sätt, vanligvis i någon sort av databas. Denna lektion introducera någon av dom databas funktioner som finns i Azure.

## Lektionsplan

Förre lektion ({{site.data.schedule.weeks[1].days[2].activities[1].number}}): <a href="{{site.data.schedule.weeks[1].days[2].activities[1].slug | prepend: site.baseurl }}">{{site.data.schedule.weeks[1].days[2].activities[1].title}}</a>

{% include lectureplan.html lectureWeek=2 lectureDay=0 lectureCaption="Lektion från kl. 8:30 till kl. 16:30" %}

Nästa lektion ({{site.data.schedule.weeks[2].days[2].activities[1].number}}): <a href="{{site.data.schedule.weeks[2].days[2].activities[1].slug | prepend: site.baseurl }}">{{site.data.schedule.weeks[2].days[2].activities[1].title}}</a> 

## Lektionslitteratur
*Detta är material (artiklar, videoer, blogs, podcasts etc) som är den teoretiska bas för denna lektion, det antas att du har läst/set/lystnad detta innan lektionen starter.*

Där finns till denna lektion inte så mycket matrial, men se till att göra dom indviduella övningsuppgifter.

Estimerat samlat "läs"-tid för lektionslittertur är **{{site.data.lecture_databaser_i_molnet.contentTimeTotal.literatureTime}} min** (för den frivilliga fördjupningslitteratur gäller {{site.data.lecture_databaser_i_molnet.contentTimeTotal.optionalLiteratureTime}} min)

{% include lecturenontopics.html lectureData="lecture_databaser_i_molnet" %}
{% include lecturetopics.html lectureData="lecture_databaser_i_molnet" %}

# Indviduella övningsuppgifter

Gå igennom dissa tre övningar, som är en del av kursen [Work with NoSQL data in Azure Cosmos DB](https://docs.microsoft.com/en-us/learn/paths/work-with-nosql-data-in-azure-cosmos-db/):
* [Create an Azure Cosmos DB database built to scale](https://docs.microsoft.com/en-us/learn/modules/create-cosmos-db-for-scale/), 35 min
* [Insert and query data in your Azure Cosmos DB database](https://docs.microsoft.com/en-us/learn/modules/access-data-with-cosmos-db-and-sql-api/), 58 min
* [Build a .NET Core app for Azure Cosmos DB in Visual Studio Code](https://docs.microsoft.com/en-us/learn/modules/build-cosmos-db-app-with-vscode/), 54 min

Det primäre fokus på dissa är på Cosmos DB, primärt för att det är nytt, att få en SQL server upp att köra i molnet är inte så mycket annonlunda än vad vi är vanvid lokalt, största skildnad är att konfiguration och pris. Och är vad gäller utveckling är det enbart en fråga om connectionstring.

# Övningsuppgift

Göras ensamt eller fler tillsammans. Målet är altid en fungerande applikation, och det rekomenderas därför att börja med brons och sen gå på silver och på slutet guld (men det är såklart möjligt att gå på silver eller guld direkt). Silver och guld är frivilliga, hellere en fungerende brons än en ofungerende silver. VG är möjligt på alla nivåer.

Skriv ett enkelt Azure Functions API som kan hämta och spara data i en databas som kör i molnet.

Du får välja vad APIet gör, bara detta involvera en databas (läs och skiv data till databasen), där finns möjlighet att bygge vidre på denna applikation under resten av kursen.

Ett förslag är ett API som har en POST som kan lägga till en item till en lista som spara i databasen, och en GET som hämter ut alla värden i databasen. Detta kunna vara en typ av chat eller mini blogg. Men du har säkkert en egen ide.

Målet är att bygga en första applikation som enbart lever i molnet, och som även är serverless. Bygg applikationen lokalt, och se till att ha koden i GitHub.

**Brons (enkel):**
Bygg som beskrivet ett REST API med Azure function, använn en [SQL Server Serverless](https://docs.microsoft.com/en-us/azure/azure-sql/database/serverless-tier-overview) till att hålla data.

Hints:
* [Getting started with Azure SQL Serverless](https://laptrinhx.com/getting-started-with-azure-sql-serverless-2968233992/)
* [Azure SQL Database Serverless – Facts!!](https://sqlworldwide.com/azure-sql-database-serverless-facts/)

**Silver (meddel - rekomenderat):**
Bygg som beskrivet ett REST API med Azure function, använn CosmosDB Serverless till att hålla data.

Hints:
* Step 1:[Reading Azure Cosmos DB Data In Azure Functions](http://dontcodetired.com/blog/post/Reading-Azure-Cosmos-DB-Data-In-Azure-Functions)
* Step 2:[Writing Azure Cosmos DB Data from Azure Functions](http://dontcodetired.com/blog/post/Writing-Azure-Cosmos-DB-Data-from-Azure-Functions)
* [Rapid API Development with Azure Functions](https://markheath.net/post/azure-functions-rest-csharp-bindings)
* [Building and Deploying a REST API using Azure Functions and Azure DevOps Pipelines](https://cloudskills.io/blog/azure-functions-rest-api)


Förslag till hur man kan komma på gång med silver (och också Guld för den del):
1. Skåpa en konsol applikation som jobbar (skriv och läs) med data i en CosmosDb (se [Using Azure CosmosDB With .NET Core](https://dotnetcoretutorials.com/2020/05/02/using-azure-cosmosdb-with-net-core/))
1. Skåpa en Azure function, med ett GET och ett POST endpoint, testa att det "funkar"
1. Kopiera kode från konsol appliktion till Azure Funtions projektet, testa att det funkar lokalt

**Guld (avancerat):**
Bygg som i *silver* ett REST API med Azure function, använn CosmosDB Serverless till att hålla data. **Lägg till** automatisk deploy med GitHub actions till Azure.

Hints:
* [Azure Functions Action](https://github.com/marketplace/actions/azure-functions-action)

# Individuell inlämningsuppgift
## Blogg 05: Databaser i molnet

Gör ett nytt inlägg på din blog som du gjorde i samband med dom förra lektioner. Det rekomenderas att skriva på samma språk som din första blogg post.

Deadline på PingPong, onsdag den 22:e september kl 23:55. Posta ett länk till dagens blog post.

Skriv ett blogg post som följer denna lektion ska innehålla en text som svara på dissa frågor:
* Beskriv kort applikationen, vad gör den?
* Beskriv koden
* Beskriv databasen
* Hur har du/ni fått den att köra i Azure functions? Screenshots, scrips, pipelines
* Hur har du tänkt runt uppdatring av databsen ifall scheman ändras? Migrations?
* Vad skulle det kosta att driva detta? Tänk gärna två scenarier: Nästan ingen använadere och jätte jätte mycket användere
    * Använd [Azure Calculator](https://azure.microsoft.com/en-us/pricing/calculator/) till att ta fram kostnad

Om du vill kan du nu välja att dela denna blogpost på sociala media (Linked, Twitter, Facebook etc.) kom ihåg att använda lämpliga hashtags som: #1 #2