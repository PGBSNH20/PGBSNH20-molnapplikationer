---
layout: lecture
title: Filer i molnet
lectureDate: Onsdag den 29:e September 2021
permalink: /cloud-lectures/files
---

Lektion 8 av 12

Dom flesta applikation handtera i något mån filar eller data om inte hör hemma i en databas, denna lektion handlar om dissa filar och data, hur vi ska förhålla os till dom, och hur vilka lösningar som finns i Azure för att handtera dissa.

## Lektionsplan

Förre lektion ({{site.data.schedule.weeks[3].days[0].activities[1].number}}): <a href="{{site.data.schedule.weeks[3].days[0].activities[1].slug | prepend: site.baseurl }}">{{site.data.schedule.weeks[3].days[0].activities[1].title}}</a>

{% include lectureplan.html lectureWeek=3 lectureDay=2 lectureCaption="Lektion från kl. 8:30 till kl. 16:30" %}

Nästa lektion ({{site.data.schedule.weeks[4].days[0].activities[1].number}}): <a href="{{site.data.schedule.weeks[4].days[0].activities[1].slug | prepend: site.baseurl }}">{{site.data.schedule.weeks[4].days[0].activities[1].title}}</a> 

## Lektionslitteratur
*Detta är material (artiklar, videoer, blogs, podcasts etc) som är den teoretiska bas för denna lektion, det antas att du har läst/set/lystnad detta innan lektionen starter.*


Estimerat samlat "läs"-tid för lektionslittertur är **{{site.data.lecture_filer_i_molnet.contentTimeTotal.literatureTime}} min** (för den frivilliga fördjupningslitteratur gäller {{site.data.lecture_filer_i_molnet.contentTimeTotal.optionalLiteratureTime}} min)

{% include lecturenontopics.html lectureData="lecture_filer_i_molnet" %}
{% include lecturetopics.html lectureData="lecture_filer_i_molnet" %}

# Indviduella övningsuppgifter

Gå igennom kursen [Store data in Azure](https://docs.microsoft.com/en-us/learn/paths/store-data-in-azure/) (3h 40min)

Och denna övning [Azure Storage CRUD Operations In MVC Using C# - Azure Table Storage - Part One](https://www.c-sharpcorner.com/article/azure-storage-crud-operations-in-mvc-using-c-sharp-azure-table-storage-part-one/) 

# Övningsuppgift

Göras ensamt eller fler tillsammans. Målet är altid en fungerande applikation, och det rekomenderas därför att börja med brons och sen gå på silver och på slutet guld (men det är såklart möjligt att gå på silver eller guld direkt). Silver och guld är frivilliga, hellere en fungerende brons än en ofungerende silver. VG är möjligt på alla nivåer.

Gör en .NET-konsol applikation med C# som kan ladda upp ett bild till en Azure blob storage. När man har laddat upp bilden ska applikationen visa URLen till bilden i bloben.

Hints:

* [Azure Blob Storage using a .NET Core Console Application](https://medium.com/@rammonzito/azure-blob-storage-using-a-net-core-console-application-106a0c2e6de5)

**Brons (enkel): Konsol applikation**

Testa lokalt med en storage emulator (välj själv emellam [The Microsoft Azure Storage Emulator](https://docs.microsoft.com/en-us/azure/storage/common/storage-use-emulator?toc=/azure/storage/blobs/toc.json) och [Azurite](https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azurite?toc=/azure/storage/blobs/toc.json)), innan ni ansluttar mot Azure.

**Silver (meddel):**
Skåpa en web app som läser bilderna som finns i eran blob och visa dom.

Lokalt ska webb applikationen jobba mot eran storage emulator.

**Hints**:

* Artikel: [Azure Storage CRUD Operations In MVC Using C# - Azure Blob Storage - Part Two](https://www.c-sharpcorner.com/article/azure-storage-crud-operations-in-mvc-using-c-sharp-part-two/)
* Video: [How to create a storage account and upload a blob](https://www.youtube.com/watch?v=UJG6viKU_A8)

**Guld (avancerat):**
Bygg som i *silver* en web app som läser av era filer i blob storage. **Lägg till** automatisk deploy med GitHub actions till Azure.


# Individuell inlämningsuppgift
## Blogg 08: Filer i molnet

Gör ett nytt inlägg på din blog som du gjorde i samband med dom förra lektioner. Det rekomenderas att skriva på samma språk som din första blogg post.

Deadline på PingPong, fredag den 01:e oktober kl 23:55. Posta ett länk till dagens blog post.

Skriv ett blogg post som följer denna lektion, detta post ska innehålla en text som svara på dissa frågor:
* Beskriv kort applikationen, vad gör den? 
* Gör en diagram (använn eg [draw.io](https://draw.io)) som visar hur data flyter.
* Beskriv koden
* Vad skulle det kosta att driva en applikation som spara och läser filer i Azure? Låt oss säga att man ska bygga en applikation som [shutterstock](https://shutterstock.com). Vad skulle hända med kostnad över tid om du har 1000 använder som var isär lägger upp 100 MB nya bilder varje dag (med din konsoll app), och alla bilder som finns i din blob laddas ner tre gångar per dag (med ditt web UI).
* Explain with your own words what Microsoft does to secure your blob data ([hint](https://cloudacademy.com/blog/how-does-azure-encrypt-data/))
* För guld: Hur har du/ni fått den din applikation köra i Azure? Screenshots, scrips, pipelines

Om du vill kan du nu välja att dela denna blogpost på sociala media (Linked, Twitter, Facebook etc.) kom ihåg att använda lämpliga hashtags som: #1 #2