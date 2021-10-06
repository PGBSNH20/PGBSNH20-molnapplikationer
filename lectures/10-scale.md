---
layout: lecture
title: Skalning, upp och ut
lectureDate: Onsdag den 6:e Oktober 2021
permalink: /cloud-lectures/scaling
---

Lektion 10 av 12

En av styrkorna vid molnet är möjligheten till at enkelt skala sin applikation, men innan vi kan det måste vi säkerställa oss att vår applikation kan skala. Ett vikitigt ord för att lyckas med en applikation som kan skala är stateless.

## Lektionsplan

Förre lektion ({{site.data.schedule.weeks[4].days[0].activities[1].number}}): <a href="{{site.data.schedule.weeks[4].days[0].activities[1].slug | prepend: site.baseurl }}">{{site.data.schedule.weeks[4].days[0].activities[1].title}}</a>

{% include lectureplan.html lectureWeek=4 lectureDay=2 lectureCaption="Lektion från kl. 8:30 till kl. 16:30" %}

Nästa lektion ({{site.data.schedule.weeks[5].days[0].activities[1].number}}): <a href="{{site.data.schedule.weeks[5].days[0].activities[1].slug | prepend: site.baseurl }}">{{site.data.schedule.weeks[5].days[0].activities[1].title}}</a> 

## Lektionslitteratur
*Detta är material (artiklar, videoer, blogs, podcasts etc) som är den teoretiska bas för denna lektion, det antas att du har läst/set/lystnad detta innan lektionen starter.*


Estimerat samlat "läs"-tid för lektionslittertur är **{{site.data.lecture_skalning_upp_och_ut.contentTimeTotal.literatureTime}} min** (för den frivilliga fördjupningslitteratur gäller {{site.data.lecture_skalning_upp_och_ut.contentTimeTotal.optionalLiteratureTime}} min)

{% include lecturenontopics.html lectureData="lecture_skalning_upp_och_ut" %}
{% include lecturetopics.html lectureData="lecture_skalning_upp_och_ut" %}

# Indviduella övningsuppgifter

Gå igennom dissa två övningar, som är en del av kursen [Architect migration, business continuity, and disaster recovery in Azure](https://docs.microsoft.com/en-us/learn/paths/architect-migration-bcdr/):
* [Scale apps in Azure App Service](https://docs.microsoft.com/en-us/learn/modules/scale-apps-app-service/), 21 min
* [Scale an App Service web app to efficiently meet demand with App Service scale up and scale out](https://docs.microsoft.com/en-us/learn/modules/app-service-scale-up-scale-out/), 46 min


# Övningsuppgift

Göras ensamt eller fler tillsammans. Målet är altid en fungerande applikation, och det rekomenderas därför att börja med brons och sen gå på silver och på slutet guld (men det är såklart möjligt att gå på silver eller guld direkt). Silver och guld är frivilliga, hellere en fungerende brons än en ofungerende silver. VG är möjligt på alla nivåer.

Målet med dagens övning är att se hur man kan sätt upp ett last-test med <loader.io> och samtidigt se att en Azure Function automatisk börjar att skala när där kommer tillräckligt med last.

Hint: [Load-Testing Azure Functions with Loader.io](https://mikhail.io/2019/07/load-testing-azure-functions-with-loaderio/)

* Se till att ha en Azure function, eller lägg upp en ny.
* Skåpa en konto på <loader.io> 
* Lägg till den azure function host i Loader
* När du ska verficera din azure funtion är det enklaste att lägga upp en Function Proxy.
* Verificera din function i Loader och lägg upp dit första test

![Proxy example]({{ "/images/azureproxy.png" | prepend: site.baseurl }})

# Individuell inlämningsuppgift
## Blogg 10: Skalning, upp och ut

Gör ett nytt inlägg på din blog som du gjorde i samband med dom förra lektioner. Det rekomenderas att skriva på samma språk som din första blogg post.

Deadline på PingPong, fredag den 08:e oktober kl 23:55. Posta ett länk till dagens blog post.

Skriv ett blogg post som följer denna lektion, detta post ska innehålla en text som svara på dissa frågor:
* Förklara skildnad på att skala en applikation horisontalt och vertikalt
* Hur påverker det kostnad att ha en applikation Azure som skalar horisontalt vs vertikalt?
    * För en app service
    * En en virtuell maskin

Att prata om vertikal skalning ger mest mening på virtelle maskiner eftersom där finns fler typer av instanser att välja på. Men kan också vara relevant för App Services.

Om du vill kan du nu välja att dela denna blogpost på sociala media (Linked, Twitter, Facebook etc.) kom ihåg att använda lämpliga hashtags som: #1 #2