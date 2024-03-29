---
layout: lecture
title: Moln-säkerhet
lectureDate: Måndag den 11:e Oktober 2021
permalink: /cloud-lectures/security
---

Lektion 11 av 12

Vi kommer att prata om någon av dom säkerhets lösningar som finns i Azure som kan hjälpa oss utvecklare med att hålla vår applikation sikker.

## Lektionsplan

Förre lektion ({{site.data.schedule.weeks[4].days[2].activities[1].number}}): <a href="{{site.data.schedule.weeks[4].days[2].activities[1].slug | prepend: site.baseurl }}">{{site.data.schedule.weeks[4].days[2].activities[1].title}}</a>

{% include lectureplan.html lectureWeek=5 lectureDay=0 lectureCaption="Lektion från kl. 8:30 till kl. 16:30" %}

Nästa lektion ({{site.data.schedule.weeks[5].days[2].activities[1].number}}): <a href="{{site.data.schedule.weeks[5].days[2].activities[1].slug | prepend: site.baseurl }}">{{site.data.schedule.weeks[5].days[2].activities[1].title}}</a> 

## Lektionslitteratur
*Detta är material (artiklar, videoer, blogs, podcasts etc) som är den teoretiska bas för denna lektion, det antas att du har läst/set/lystnad detta innan lektionen starter.*


Estimerat samlat "läs"-tid för lektionslittertur är **{{site.data.lecture_moln-saekerhet.contentTimeTotal.literatureTime}} min** (för den frivilliga fördjupningslitteratur gäller {{site.data.lecture_moln-saekerhet.contentTimeTotal.optionalLiteratureTime}} min)

{% include lecturenontopics.html lectureData="lecture_moln-saekerhet" %}
{% include lecturetopics.html lectureData="lecture_moln-saekerhet" %}

# Indviduella övningsuppgifter

Gå igennom dissa 3 övningar, som är en del av kursen [Secure your cloud applications in Azure](https://docs.microsoft.com/en-us/learn/paths/secure-your-cloud-apps/):
* [Top 5 security items to consider before pushing to production](https://docs.microsoft.com/en-us/learn/modules/top-5-security-items-to-consider/), 45 min
* [Manage secrets in your server apps with Azure Key Vault](https://docs.microsoft.com/en-us/learn/modules/manage-secrets-with-azure-key-vault/), 46 min
* [Control authentication for your APIs with Azure API Management](https://docs.microsoft.com/en-us/learn/modules/control-authentication-with-apim/), 50 min

Dissa 2 kan också vara bra:
* [Protect against security threats on Azure](https://docs.microsoft.com/en-us/learn/modules/protect-against-security-threats-azure/), 28 min
* [Secure and isolate access to Azure resources by using network security groups and service endpoints](https://docs.microsoft.com/en-us/learn/modules/secure-and-isolate-with-nsg-and-service-endpoints/), 43 min

# Övningsuppgift
Bygg en Azure fuction eller en konsol applikation som använder data från en Azure Key Vault.

Tanken är att ni har en hemlighet som ni ligger i Azure Key Valut och denna ska ni läsa i applikation och använda på något sätt.

Förslag: Bygg en quiz vart svar och fråga ligge i Azure Key Valut. Frågan läsa och presenteras till användern (GET) och använderen svara (POST) och det valideras mot svaret i Key Valut.

Hints:
* [Storing and using secrets in Azure](https://devblogs.microsoft.com/dotnet/storing-and-using-secrets-in-azure/)
