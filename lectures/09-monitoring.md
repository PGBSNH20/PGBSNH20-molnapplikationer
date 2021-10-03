---
layout: lecture
title: Monitorering av moln applikationer
lectureDate: Måndag den 4:e Oktober 2021
permalink: /cloud-lectures/monitoring
---

Lektion 9 av 12

När en appliktion lever i molnet är det lätt händt att man tappar kontakten till appliktionen, där för är det viktigt att vi har en bra bild av vilka verktyg vi kan använda för att kunna övervaka vår applikation.

## Lektionsplan

Förre lektion ({{site.data.schedule.weeks[3].days[2].activities[1].number}}): <a href="{{site.data.schedule.weeks[3].days[2].activities[1].slug | prepend: site.baseurl }}">{{site.data.schedule.weeks[3].days[2].activities[1].title}}</a>

{% include lectureplan.html lectureWeek=4 lectureDay=0 lectureCaption="Lektion från kl. 8:30 till kl. 16:30" %}

Nästa lektion ({{site.data.schedule.weeks[4].days[2].activities[1].number}}): <a href="{{site.data.schedule.weeks[4].days[2].activities[1].slug | prepend: site.baseurl }}">{{site.data.schedule.weeks[4].days[2].activities[1].title}}</a> 

## Lektionslitteratur
*Detta är material (artiklar, videoer, blogs, podcasts etc) som är den teoretiska bas för denna lektion, det antas att du har läst/set/lystnad detta innan lektionen starter.*

Estimerat samlat "läs"-tid för lektionslittertur är **{{site.data.lecture_monitorering_av_moln_applikationer.contentTimeTotal.literatureTime}} min** (för den frivilliga fördjupningslitteratur gäller {{site.data.lecture_monitorering_av_moln_applikationer.contentTimeTotal.optionalLiteratureTime}} min)

{% include lecturenontopics.html lectureData="lecture_monitorering_av_moln_applikationer" %}
{% include lecturetopics.html lectureData="lecture_monitorering_av_moln_applikationer" %}

# Indviduella övningsuppgifter

Gå igennom dissa fem övningar:
* [Introduction to Azure Monitor](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-monitor/), 49 min
* [Analyze your Azure infrastructure by using Azure Monitor logs](https://docs.microsoft.com/en-us/learn/modules/analyze-infrastructure-with-azure-monitor-logs/), 36 min
* [Capture and view page load times in your Azure web app with Application Insights](https://docs.microsoft.com/en-us/learn/modules/capture-page-load-times-application-insights/), 45 min
* [Instrument server-side web application code with Application Insights](https://docs.microsoft.com/en-us/learn/modules/instrument-web-app-code-with-application-insights/), 34 min
* [Implement logging in a .NET Framework ASP.NET web application](https://docs.microsoft.com/en-us/learn/modules/aspnet-logging/), 24 min

# Övningsuppgift

Göras ensamt eller fler tillsammans. Målet är altid en fungerande applikation, och det rekomenderas därför att börja med brons och sen gå på silver och på slutet guld (men det är såklart möjligt att gå på silver eller guld direkt). Silver och guld är frivilliga, hellere en fungerende brons än en ofungerende silver. VG är möjligt på alla nivåer.

Ta en av dina webbapplikationer, detta kunna vara webb applikation som du/ni byggd i [lektion 6](https://pgbsnh20.github.io/PGBSNH20-molnapplikationer/cloud-lectures/webapplications#övningsuppgift).

Implementera logging och konfigura så att loggen hamnar i Application Insights. Deploya applikationen till Azure App Service. 

Ta frem minst två [Kusto](https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/) "queries" (förfrågningar) som viser data om din applikation, eksampler på queries:
* En som visar alla *Errors* och *Warnings* i applikationen
* En som visar tiden det tar att inläsa en websida

Hints:
* [Application Insights for ASP.NET Core applications](https://docs.microsoft.com/en-us/azure/azure-monitor/app/asp-net-core)

# Individuell inlämningsuppgift
## Blogg 09: Monitorering av molnapplikationer

Gör ett nytt inlägg på din blog som du gjorde i samband med dom förra lektioner. Det rekomenderas att skriva på samma språk som din första blogg post.

Deadline på PingPong, onsdag den 6:e oktober kl 23:55. Posta ett länk till dagens blog post.

Skriv ett blogg post som följer denna lektion, detta post ska innehålla en text som svara på dissa frågor:
* Beskriv kort applikationen, vad gör den? 
* Gör en diagram (använn eg [draw.io](https://draw.io)) hur den applikation är förbundet andra tjäster
* Beskriv koden, med fokus på den del som rör din log implementation
* Fundera på och beskriv hur logging av din applikation kan kan avhjälpa säkerhetsproblem i din applikation
* Förklara dina queries; vad gör dom? varför är dissa data som tas fram interesanta? 

Om du vill kan du nu välja att dela denna blogpost på sociala media (Linked, Twitter, Facebook etc.) kom ihåg att använda lämpliga hashtags som: #1 #2