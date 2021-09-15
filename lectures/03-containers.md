---
layout: lecture
title: Containrar och orkestrering
lectureDate: Måndag den 13:e September 2021
permalink: /cloud-lectures/containers
---

Lektion 3 av 12

Vi har tidigere pratat om containere och Docker ([Webbutveckling backend: lektion 2](https://pgbsnh20.github.io/PGBSNH20-backendweb/lectures/docker)), denna lektion kommer att bli litet repitaion på denna snak. Men med fokus på hur vi själv kan bygga en ett docker image och använda det,

## Lektionsplan

{% include lectureplan.html lectureWeek=1 lectureDay=0 lectureCaption="Lektion från kl. 8:30 till kl. 16:30" %}

## Lektionslitteratur
*Detta är material (artiklar, videoer, blogs, podcasts etc) som är den teoretiska bas för denna lektion, det antas att du har läst/set/lystnad detta innan lektionen starter.*

Estimerat samlat "läs"-tid för lektionslittertur är **{{site.data.lecture_containrar_och_orkestrering.contentTimeTotal.literatureTime}} min** (för den frivilliga fördjupningslitteratur gäller {{site.data.lecture_containrar_och_orkestrering.contentTimeTotal.optionalLiteratureTime}} min)

{% include lecturenontopics.html lectureData="lecture_containrar_och_orkestrering" %}
{% include lecturetopics.html lectureData="lecture_containrar_och_orkestrering" %}


# Indviduella övningsuppgifter

Gå igennom detta lab på GitHub:
* [GitHub Actions: Publish to github packages](https://lab.github.com/githubtraining/github-actions:-publish-to-github-packages)


# Övningsuppgifter i grupp (eller ensamt)

Dissa övningar är bygger på varandra
## Övning 1: Hello World i Docker

**Mål med denna övning**: Bygg en container som kan hålla Hello World webb applikationen (samma om vi använda i förra lektion). Och få applikationen att köra i Docker, så att du kan komma åt den med webbläsare: localhost:80.

1. Installera Docker på din dator: [Get Docker](https://docs.docker.com/get-docker/) (du borde ha detta)
2. Starta om din dator
3. Klona ner ["Hello world" .NET Core webb applikationen](https://github.com/skjohansen/SimpleWebHalloWorld) 
4. Lägg till en "Dockerfile"
   * Tutorial: [Getting Started With ASP.NET Core & Docker](https://morioh.com/p/5414a74be39d) 
   * Tutorial: [How YOU can Dockerize a .Net Core app](https://softchris.github.io/pages/dotnet-dockerize.html)
5. Bygg din container
6. Kör din container

Hints:

* Ni kan behöva att se över port mapningen
* Ni kan behöva att byta base-image i förhållande till tutorials
* Mindre kod ändringar kan behövas

Blogg:

* Se till att beskriva dom olika delar av container filen i eran indviduella blogg

## Övning 2: Hello World med Docker Compose

Ni har nu en Docker container som innehåller vår Hello World applikation

**Mål med denna övning**: Gör en Docker compose fil som kan köra din nya Hello World-Docker container 

1. Skåpa en `docker-compose.yml` fil som beskivar hur eran docker container ska köras
	* [Get started with Docker Compose](https://docs.docker.com/compose/gettingstarted/)
	* [A Practical Introduction to Docker Compose](https://hackernoon.com/practical-introduction-to-docker-compose-d34e79c4c2b6)
2. Starta eran applikation med `docker-compose up`

Docker Compose är speciellt smidigt för lokala utvecklingsmiljö vart man har behov av flera containers (services) jobbar ihop i en applikation. I detta exempel är där endast en service så där finns inte ett jätte behov av en compose fil, men så fort applikationen växer blir den relevant.

**OBS**: Ni kommer inte att använda denna compose fil mer i denna övning

## Övning 3: Publicera Hello World container image

Ni har nu en Docker container som innehåller vår Hello World applikation (och en Docker Compose definition).

**Mål med denna övning**: Är att skåpa ett Docker image och publicera det till "GitHub packages" med GitHub Actions. Ni väljer själv vilken av dom två system ni vill använda.

1. Skåpa en GitHub pipeline som bygger eran applikation (som [lektion 2](/cloud-lectures/ci))
2. Utök denna pipeline med ett *step* som bygger eran container och pusher den till ert GitHub package storage
   * Där finns en GitHub action som man med fördel kan använda: [Build-Push Action](https://github.com/docker/build-push-action)
   * AKTA: API nycklar, användernamn, lösenord etc får **inte** finnas in eran pipline, använn GitHub secrets till detta: [Encrypted secrets](https://docs.github.com/en/actions/reference/encrypted-secrets)
3. Information om login till [GitHub Container Registry](https://github.com/docker/login-action#github-container-registry)
4. Skåpa en Personal Access Token (PAT) på Github: [Create a GitHub Personal Access Token](https://itnext.io/build-ship-github-container-registry-kubernetes-aa06029b3f21#0075)
5. Lägg till denna PAT som en secret i ditt repo


Så här kan eran jobs-section i action workflowen se ut, se till att ersätta, med rätt info:
* PROJECT_DIR
* DITT_USER_NAME
* PROJECT
* OBS där är gjort ett extra mellanslag emellan { och { som inte ska vara där, men är det inte där tolker GitHub det som den parameter
* Där är här två tags, försök i din blogg att förklara varför


```yaml
jobs:
  build-and-push-api:
    runs-on: ubuntu-latest
    env: 
      working-directory: ./Source
    steps:
    - name: Checkout code
      uses: actions/checkout@v2.3.4
    - name: Login to GitHub Container Registry
      uses: docker/login-action@v1.10.0
      with:
         registry: ghcr.io
         username: ${ { github.actor } };
         password: ${ { secrets.GITHUB_PAT } }
    - name: Build and push
      id: docker_build
      uses: docker/build-push-action@v2.7.0
      with:
        push: true
        context: ${ {env.working-directory} }/PROJECT_DIR
        tags: |
          ghcr.io/DITT_USER_NAME/PROJECT:latest
          ghcr.io/DITT_USER_NAME/PROJECT:${ { github.run_number } }
```

Hints:

* GitHub: [Packages](https://github.com/features/packages)
* [Publishing and installing a package with GitHub Actions](https://docs.github.com/en/packages/managing-github-packages-using-github-actions-workflows/publishing-and-installing-a-package-with-github-actions)

Ni kan nu logga in på eran GitHub packages med docker och hämta ut er container och gör en pull på det med `docker pull`

* Starta en ny instans
* Pull ert image från Github Package
* Kör ert image och testa det


# Individuell inlämningsuppgift

Inlämnas via PingPong, men sparas i GitHub
## Blogg 03: Containrar och orkestrering

Gör ett nytt inlägg på din blogg som du gjorde i samband med lektion 1+2. Det rekomenderas att skriva på samma språk som din första blogg post.

Deadline på PingPong, tisdag den 14:e september kl 23:55. Posta ett länk till dagens blog post.

Skriv ett blogg post som följer denna lektion ska innehålla en text som svara på dissa frågor:
* Vad har in installerat lokalt / Github
* Hur har ni fått applikationen att kör i en container
* Beskriv din docker fil
* Beskriv din github pipeline
* Hur har ni gjort med hemliser?


Om du vill kan du nu välja att dela denna blogpost på sociala media (Linked, Twitter, Facebook etc.) kom ihåg att använda lämpliga hashtags som: #1 #2

