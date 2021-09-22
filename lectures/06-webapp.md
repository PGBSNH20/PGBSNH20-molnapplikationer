---
layout: lecture
title: Webb applikationer i molnet
lectureDate: Onsdag den 22:e September 2021
permalink: /cloud-lectures/webapplications
---

Lektion 6 av 12

Det vi oftast som udviklare är att använda molnet till att göra vår webbappliktion tillgänglig i molnet. Denna lektion handlar om någon av dom möjlighet vi har till att servicera en webbapplikation med Azure.

## Lektionsplan

Förre lektion ({{site.data.schedule.weeks[2].days[0].activities[1].number}}): <a href="{{site.data.schedule.weeks[2].days[0].activities[1].slug | prepend: site.baseurl }}">{{site.data.schedule.weeks[2].days[0].activities[1].title}}</a>

{% include lectureplan.html lectureWeek=2 lectureDay=2 lectureCaption="Lektion från kl. 8:30 till kl. 16:30" %}

Nästa lektion ({{site.data.schedule.weeks[3].days[0].activities[1].number}}): <a href="{{site.data.schedule.weeks[3].days[0].activities[1].slug | prepend: site.baseurl }}">{{site.data.schedule.weeks[3].days[0].activities[1].title}}</a> 

## Lektionslitteratur
*Detta är material (artiklar, videoer, blogs, podcasts etc) som är den teoretiska bas för denna lektion, det antas att du har läst/set/lystnad detta innan lektionen starter.*

Estimerat samlat "läs"-tid för lektionslittertur är **{{site.data.lecture_webb_applikationer_i_molnet.contentTimeTotal.literatureTime}} min** (för den frivilliga fördjupningslitteratur gäller {{site.data.lecture_webb_applikationer_i_molnet.contentTimeTotal.optionalLiteratureTime}} min)

{% include lecturenontopics.html lectureData="lecture_webb_applikationer_i_molnet" %}
{% include lecturetopics.html lectureData="lecture_webb_applikationer_i_molnet" %}

# Indviduella övningsuppgifter

Gå igennom dissa fyre övningar, som är en del av kursen [Architect modern applications in Azure](https://docs.microsoft.com/en-us/learn/paths/architect-modern-apps/):
* [Explore Azure App Service](https://docs.microsoft.com/en-us/learn/modules/introduction-to-azure-app-service/), 39 min
* [Host a web application with Azure App Service](https://docs.microsoft.com/en-us/learn/modules/host-a-web-app-with-azure-app-service/), 31 min
* [Build and store container images with Azure Container Registry](https://docs.microsoft.com/en-us/learn/modules/build-and-store-container-images/), 49 min
* [Deploy and run a containerized web app with Azure App Service](https://docs.microsoft.com/en-us/learn/modules/deploy-run-container-app-service/), 46 min

# Övningsuppgift

Göras ensamt eller fler tillsammans. Målet är altid en fungerande applikation, och det rekomenderas därför att börja med brons och sen gå på silver och på slutet guld (men det är såklart möjligt att gå på silver eller guld direkt). Silver och guld är frivilliga, hellere en fungerende brons än en ofungerende silver. VG är möjligt på alla nivåer.

I förre lektion gjorde du/ni en databas som höll en data struktur efter ditt eget val. Målet i denna övning är att du ska bygga en liten webapplikation som i princip kan samma som det API du gjorde.

Webbapplikationen ska vara skriven med Razor Pages och det ska vara möjligt att få präsenterat data från databasen och lägga till nytt data. Tanken är **inte** att du ska använda ditt API men att göra alla anrop direkt från din razor page model. Det viktiga mål är att denna webbapplikation ska du få att köra i Azure App Service.

**Brons (enkel):**
Bygg webbapplikationen med Razor Pages och publish den till Azure App Services med [Visual Studio](https://docs.microsoft.com/en-US/visualstudio/deployment/quickstart-deploy-to-azure?view=vs-2019) eller [Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azureappservice)

**Silver (meddel - rekomenderat):**
Bygg webbapplikationen med Razor Pages, lägg till en **dockerfile** så att du kan bygga ett image, [push detta image till ACR](https://blog.hildenco.com/2020/10/pushing-docker-images-to-azure.html).

När ditt image är i ACR konfigurera en ny Azure App Services så att den hämtar och kör ditt docker image.

Hints:
* [Deploy docker image to Azure App Service using Visual Studio Code](https://code.visualstudio.com/docs/containers/app-service)

**Guld (avancerat):**
Bygg webbapplikationen med Razor Pages, lägg till en **dockerfile** så att du kan bygga ett image, push alt till ett GitHub repo.

Configurera GitHub actions så att ett docker image byggs till GitHub packages (som i lektion 2), konfigurera en ny Azure App Services så att den hämtar och kör ditt docker image från GitHub packages.

Hints:
* [How to deploy docker image from Github Package Registry to Azure Web Apps](https://stackoverflow.com/questions/64853326/how-to-deploy-docker-image-from-github-package-registry-to-azure-web-apps)

**Platina (mycket avancerat)**
Bygg webbappliktionen som en statisk web applikation, som hämter data via Azure Functions. Ett förslag är att använda React som frontend ramverk.

Deploy till **Azure Static Web Apps** från GitHub.

Hints:
* [Building Single Page App with Azure Functions and improving cold start time](https://itnext.io/building-single-page-app-with-azure-functions-and-improving-cold-start-time-79a0faec9913)
* [Building An React App With Azure Static Web Apps Service](https://medium.com/bb-tutorials-and-thoughts/building-an-react-app-with-azure-static-web-apps-service-4e3e23e9870c)

# Individuell inlämningsuppgift
## Blogg 06: Webbapplikationer i molnet

Gör ett nytt inlägg på din blog som du gjorde i samband med dom förra lektioner. Det rekomenderas att skriva på samma språk som din första blogg post.

Deadline på PingPong, fredag den 24:e september kl 23:55. Posta ett länk till dagens blog post.

Skriv ett blogg post som följer denna lektion ska innehålla en text som svara på dissa frågor:
* Beskriv kort applikationen, vad gör den?
* Beskriv koden
* Hur har du/ni fått den att köra i Azure App Service? Screenshots, scrips, pipelines
* Vad skulle det kosta att driva detta? Tänk gärna två scenarier: Nästan ingen använadere och jätte jätte mycket användere
    * Använd [Azure Calculator](https://azure.microsoft.com/en-us/pricing/calculator/) till att ta fram kostnad

Om du vill kan du nu välja att dela denna blogpost på sociala media (Linked, Twitter, Facebook etc.) kom ihåg att använda lämpliga hashtags som: #1 #2