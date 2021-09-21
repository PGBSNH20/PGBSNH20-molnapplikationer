---
layout: lecture
title: Nätverk i molnet
lectureDate: Måndag den 27:e September 2021
permalink: /cloud-lectures/network
---

Lektion 7 av 12

Att ha en ensam appliktion i molnet räcker oftast inte, ofta måste vi ha flera applikationer att prata ihop. Denna lektion är om hur vi får detta till och dom möjlighetter som finns i Azure till att bygga privata netvärk.

## Lektionsplan

Förre lektion ({{site.data.schedule.weeks[2].days[2].activities[1].number}}): <a href="{{site.data.schedule.weeks[2].days[2].activities[1].slug | prepend: site.baseurl }}">{{site.data.schedule.weeks[2].days[2].activities[1].title}}</a>

{% include lectureplan.html lectureWeek=3 lectureDay=0 lectureCaption="Lektion från kl. 8:30 till kl. 16:30" %}

Nästa lektion ({{site.data.schedule.weeks[3].days[2].activities[1].number}}): <a href="{{site.data.schedule.weeks[3].days[2].activities[1].slug | prepend: site.baseurl }}">{{site.data.schedule.weeks[3].days[2].activities[1].title}}</a> 

## Lektionslitteratur
*Detta är material (artiklar, videoer, blogs, podcasts etc) som är den teoretiska bas för denna lektion, det antas att du har läst/set/lystnad detta innan lektionen starter.*

Estimerat samlat "läs"-tid för lektionslittertur är **{{site.data.lecture_naetverk_i_molnet.contentTimeTotal.literatureTime}} min** (för den frivilliga fördjupningslitteratur gäller {{site.data.lecture_naetverk_i_molnet.contentTimeTotal.optionalLiteratureTime}} min)

{% include lecturenontopics.html lectureData="lecture_naetverk_i_molnet" %}
{% include lecturetopics.html lectureData="lecture_naetverk_i_molnet" %}

# Indviduella övningsuppgifter


Gå igennom kursen [Connect your services together](https://docs.microsoft.com/en-us/learn/paths/connect-your-services-together/) (4h 4min)

Och denna övning [Introduction to Azure virtual networks](https://docs.microsoft.com/en-us/learn/modules/introduction-to-azure-virtual-networks/), 78 min


# Individuell inlämningsuppgift
## Blogg 07: Nätverk i molnet

Gör ett nytt inlägg på din blog som du gjorde i samband med dom förra lektioner. Det rekomenderas att skriva på samma språk som din första blogg post.

Deadline på PingPong, onsdag den 29:e september kl 23:55. Posta ett länk till dagens blog post.

*Denna övning är av teoretisk karaktär*

Ni jobbar i ett företag som har en intern applikation som ni gärna vill modernisera, denna interna applikation använder tillgång till interna server och resurser, och jobbar med klassificerade data som inte får öppet skickas via nätat, och därför är det i följa din CTO inte möjligt att använda en PaaS moln-lösning.

Ett viktigt punkt i modernisering är att implementera en enterprise bus, och ni vill gärna använda er av Azure Service Bus, men tyvär säger eran CTO säger "nej", på grund av data inte får skickas öppet.

Skriv (i eran blogg) ett argument till eran CTO som förklara och övertyga hen om att ni med hjälp av ett Azure Private Link kan använda Azure Service Bus i eran interna applikation. Förklara begrepp som Virtual Private Cloud i eran förklaring.

Om ni lyckas att övertyga eran CTO till att tillåta att ni använder Azure Service Bus, kommer ni i framtiden att kunna använda andra Azure PaaS tjänster (vilket gör livet som utvecklare mycket bättre) :-)

Fakta om eran CTO, hen är:

* inte så svår att övertyga, om bara ni använder fakta
* visuell och älskar därför diagram och ritningar (men se till att göra egna, använd t.ex. draw.io)
* fan av teknisk, så var inte rädd om att använda tekniska termer

**Hints**:

* [Connect an on-premises network to a Microsoft Azure virtual network](https://docs.microsoft.com/en-us/microsoft-365/enterprise/connect-an-on-premises-network-to-a-microsoft-azure-virtual-network?view=o365-worldwide)

Om du vill kan du nu välja att dela denna blogpost på sociala media (Linked, Twitter, Facebook etc.) kom ihåg att använda lämpliga hashtags som: #1 #2

# Frivillig övelse

Om man saknar litet kod, kan man göra denna övelse. 

Skåpa en konsol applikation som använder Azure Service Bus : [Get started with Service Bus queues](https://docs.microsoft.com/en-us/azure/service-bus-messaging/service-bus-dotnet-get-started-with-queues)

Denna övning ska **inte** vara i eran blog.