

Eerste kop | Tweede kop
--- | ---
Inhoudsel | Inhoudsel
Inhoudsel | Inhoudsel

![Citadel](https://vignette.wikia.nocookie.net/masseffect/images/d/d7/MassEffect2Citadel.jpg/revision/latest?cb=20100721191415)

Links gerig | Sentrum gerig | Regs gerig
:-- | :-: | --:
kol 3 is | een of ander woordryke teks | **$ 1600**
kol 2 is | gesentreer | $ 12
sebra strepe | netjies is | ~~ $ 1 ~~

Dillinger is 'n wolk-geaktiveerde, selfoongereed, AngularJS-aangedrewe HTML5 Markdown-redakteur wat op die regte pad beskikbaar is.

- Tik 'n bietjie Markdown aan die linkerkant
- Sien HTML regs
- towerkuns

# waar

- Voer 'n HTML-lêer in en kyk hoe dit op 'n magiese manier na Markdown omgeskakel word
- Sleep en plaas prente (vereis dat u Dropbox-rekening gekoppel is)

Jy kan ook:

- Voer lêers in vanaf GitHub, Dropbox, Google Drive en One Drive
- Sleep en afteken en HTML-lêers in Dillinger
- Voer dokumente uit as Markdown, HTML en PDF

Markdown is 'n ligte opmaaktaal wat gebaseer is op die opmaakkonvensies wat mense van nature in e-pos gebruik. Soos [John Gruber] op die [Markdown-werf] [df1] skryf

> Die belangrikste doel van die ontwerpsintaksis van Markdown is om dit so leesbaar as moontlik te maak. Die idee is dat 'n Markdown-geformatteerde dokument soos dit is, as gewone teks gepubliseer moet word, sonder om te lyk asof dit gemerk is met etikette of opmaakinstruksies.

Hierdie teks wat u hier sien, is *eintlik* in Markdown geskryf! Om 'n aanvoeling vir die sintaksis van Markdown te kry, tik 'n bietjie teks in die linkervenster en kyk na die resultate regs.

### onwaar

Dillinger gebruik 'n aantal oopbronprojekte om behoorlik te werk:

- [AngularJS] - HTML verbeter vir webprogramme!
- [Ace Editor] - wonderlike webgebaseerde teksredigeerder
- [markdown-it] - Markdown-ontleder word reg gedoen. Vinnig en maklik om uit te brei.
- [Twitter Bootstrap] - 'n uitstekende UI-ketel vir moderne webprogramme
- [node.js] - ek / O vir die backend
- [Express] - vinnige netwerk.raamwerk vir node.js [@tjholowaychuk]
- [Gulp] - die streaming-bou-stelsel
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML na Markdown-omskakelaar
- [jQuery] - duh

En natuurlik is Dillinger self 'n open source met 'n [openbare bewaarplek] [dille] op GitHub.

### Installasie

![Ilos](https://lh3.googleusercontent.com/proxy/DDV8a7sLIWurhJtW8Ego9bq-JlwpfFFoR0tkLJQKKYXEXoWHB6ZUP5jGKD2VcYt3z1QVsgcn6L3GoU1ns8m9fvi3U51GzddA70ZUMHgzHvjl4-i7YOJY9cShBPrfjUhMQhxaJ97WFBp612XmjMXVGypfGkiBarN4PWxhiHkiYYNW7HGbtTpOcyt9GQ4Q23C2noxLTWFXZMcQZhRpQA_qzu2n6_H6CPViBnhSHpEl4JZAPaGCSJqgZg)

Dillinger vereis dat [Node.js](https://nodejs.org/) v4 + moet werk.

Installeer die afhanklikhede en afhanklikhede en begin die bediener.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

Vir produksie-omgewings ...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Inproppe

Dillinger word tans uitgebrei met die volgende inproppe. Instruksies oor hoe om dit in u eie toepassing te gebruik, word hieronder gekoppel.

Inprop | LEES
--- | ---
Dropbox | [plugins / dropbox / README.md] [PlDb]
GitHub | [plugins / github / README.md] [PlGh]
Google Drive | [plugins / googledrive / README.md] [PlGd]
OneDrive | [plugins / onedrive / README.md] [PlOd]
Medium | [plugins / medium / README.md] [PlMe]
Google Analytics | [plugins / googleanalytics / README.md] [PlGa]

### Ontwikkeling

Wil u bydra? Groot!

Dillinger gebruik Gulp + Webpack om vinnig te ontwikkel. Maak 'n verandering in u lêer en sien dadelik u opdaterings!

Maak u gunsteling terminal oop en voer hierdie opdragte uit.

Eerste oortjie:

```sh
$ node app
```

Tweede oortjie:

```sh
$ gulp watch
```

(opsioneel) Derde:

```sh
$ karma test
```

#### Gebou vir bron

Vir produksie vrystelling:

```sh
$ gulp build --prod
```

Genereer vooraf geboude zip-argiewe vir verspreiding:

```sh
$ gulp build dist --prod
```

### Docker

Dillinger is baie maklik om te installeer en in 'n Docker-houer te implementeer.

Standaard sal die Docker poort 8080 blootlê, so verander dit indien nodig in die Dockerfile. Gebruik die Dockerfile om die beeld te bou as u gereed is.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version} .
```

Dit sal die dillinger-beeld skep en die nodige afhanklikhede intrek. Verander seker `${package.json.version}` met die werklike weergawe van Dillinger.

Sodra u klaar is, voer die Docker-beeld uit en karteer die poort na alles wat u gasheer wil hê. In hierdie voorbeeld karteer ons poort 8000 van die gasheer eenvoudig na poort 8080 van die Docker (of watter poort ook al in die Dockerfile blootgestel is):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Verifieer die implementering deur na u bedieneradres te gaan in u blaaier.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

Sien [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)

### Todos
