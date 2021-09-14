---
layout: lecture
title: Serverless
lectureDate: Onsdag den 15:e September 2021
permalink: /cloud-lectures/serverless 
---
Lektion 4 av 12

Termen serverless gör det extremt enkelt att börja att använda sig av molnet, vi kan skriva kod lokalt och med få steg få det att köra i Azure vid hjälp av Azure Functions.

## Lektionsplan

{% include lectureplan.html lectureWeek=1 lectureDay=2 lectureCaption="Lektion från kl. 8:30 till kl. 16:30" %}

## Lektionslitteratur
*Detta är material (artiklar, videoer, blogs, podcasts etc) som är den teoretiska bas för denna lektion, det antas att du har läst/set/lystnad detta innan lektionen starter.*

Estimerat samlat "läs"-tid för lektionslittertur är **{{site.data.lecture_severless_applikationer.contentTimeTotal.literatureTime}} min** (för den frivilliga fördjupningslitteratur gäller {{site.data.lecture_severless_applikationer.contentTimeTotal.optionalLiteratureTime}} min)

{% include lecturenontopics.html lectureData="lecture_severless_applikationer" %}
{% include lecturetopics.html lectureData="lecture_severless_applikationer" %}


# Indviduella övningsuppgifter
<br />

## Azure konto

Vi kommer under denna kurs att jobba med Azure, och därför behöver ni en Azure konto.

**Azure for Students**

Som en del av student erbjudande från Microsoft, ska ni har tillgång till [Azure for Students](https://azure.microsoft.com/en-us/free/students/), tyvärr kommer denna med en viktig begränsning, men får 100$ och dom är aktiva i 12 månad från start. Så om man aktiverade sin Azure konto i starten av utbildningen är denna nu gått ut på tid, dock borde ni ha fått en mail om reaktivering.

Använn eran *plushogskolan.se* epost.

**Azure free account**

Om Azure for Students inte är en möjligt kan man skåpa en [Azure free account](https://azure.microsoft.com/en-us/free/?ref=VSDevEssentials), här får man 200$ men dom är enbart aktiva i 30 dagar från start

När du har fått din konto att funka, titta runt i Azure och få en känsla av dom möjligheter som finns i Azure.

### Azure CLI, frivillig

För utom det grafiska webb-gränssnitt i Azure, är det även möjligt kontrollera Azure gennom kommando förtolkeren (ett CLI) och även ett [REST api](https://docs.microsoft.com/en-us/rest/api/azure/).

Detta är en liten frivillig övning till att göra klar Azure CLI
* Ladda ner och installera: [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli-windows)
* Logga in med: `az login`

## Microsoft Learn övningar

Gå igennom dissa tre övningar, som är en del av kursen [Create serverless applications](https://docs.microsoft.com/en-us/learn/paths/create-serverless-applications/):
* [Choose the best Azure service to automate your business processes](https://docs.microsoft.com/en-us/learn/modules/choose-azure-service-to-integrate-and-automate-business-processes) (44 min)
* [Create serverless logic with Azure Functions](https://docs.microsoft.com/en-us/learn/modules/create-serverless-logic-with-azure-functions) (36 min)
* [Execute an Azure Function with triggers](https://docs.microsoft.com/en-us/learn/modules/execute-azure-function-with-triggers/) (83 min)


# Övningsuppgift

Ensamt eller fler tillsammans.

Bygga en Azure Functions application, denna ska vara en mini-kalkylator som kan ta två input och addera dom.

Det rekomenderas att börja med bronze och sen gå på silver och på slutet guld. Silver och guld är frivilliga.

**Brons (enkel):**

Den enkla lösning är att bygga den direkt i Azures webgränssnitt. Men du kan även utveckla functions lokalt med [Visual Studio Code](https://docs.microsoft.com/en-us/azure/azure-functions/functions-develop-vs-code?tabs=csharp) eller [Visual Studio](https://docs.microsoft.com/en-us/azure/azure-functions/functions-develop-vs?tabs=in-process).

**Silver (meddel):**
Det är även möjligt att deploya sin function direkt från GitHub: [Create a function app in Azure that is deployed from GitHub](https://docs.microsoft.com/en-us/azure/azure-functions/scripts/functions-cli-create-function-app-github-continuous). Detta ska förstås på det sätt att koden ligger i ett GitHub repo och när man skåper applikationen via CLIen kan man beträtta att den ska dra koden from detta Git-repo.

**Guld (mycket avancerat):**
Slutligen finns där möjligheten att deploya en azure funtion app från GitHub actions med hjälp av [Azure Functions Action](https://github.com/marketplace/actions/azure-functions-action).



# Individuell inlämningsuppgift

Inlämnas via PingPong, men sparas i GitHub
## Blogg 04: Severless applikationer

Gör ett nytt inlägg på din blog som du gjorde i samband med dom förra lektioner. Det rekomenderas att skriva på samma språk som din första blogg post.

Deadline på PingPong, torsdag den 16:e september kl 23:55. Posta ett länk till dagens blog post.

Skriv ett blogg post som följer denna lektion ska innehålla en text som svara på dissa frågor:
* Vad är Serverless och Function As A Service (FaaS)?
* Beskriv din/eran kalkylator.
    * Koden?
    * Hur har du/ni fått den att köra i Azure functions? Screenshots, scrips, pipelines

Du ska **inte** beskriva hur du har satt upp din Azure konto.

**Akta** att din blogg + kod + scripts + screenshots inte innehåller någon användernamn, lösenord, api nycklar etc.

Om du vill kan du nu välja att dela denna blogpost på sociala media (Linked, Twitter, Facebook etc.) kom ihåg att använda lämpliga hashtags som: #1 #2