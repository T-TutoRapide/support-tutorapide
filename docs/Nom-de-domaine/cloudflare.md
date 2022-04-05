---
sidebar_position: 2
title: Cloudflare
description: Ajouter son site au cdn de Cloudflare.
tags:
  - cloudflare
  - CDN
Author: Samuel*#7455 (Discord)
---


Dans ce tutoriel je vais vous montrer comment configurer Cloudflare pour votre site web.

:::note Information

Attention quand vous allez changer les dns de votre nom de domaine pour ceux de **Cloudflare** , c'est changement peuvent prendre entre 24h/48h.
Mais vous pouvez suivre cette propagation sur [whatmydns](https://www.whatsmydns.net/).

:::

:::info Cloudflare (source)

**Combien de temps faut-il pour qu’un changement de DNS soit effectif ?**

Le Time-To-Live (TTL) par défaut du DNS Cloudflare est de 300 secondes (5 minutes).<br/>
Tous les changements ou suppléments réalisés sur votre fichier de zone Cloudflare seront effectifs en 5 minutes ou moins.<br/>
Notez que le cache de votre DNS local peut prendre plus de temps pour se mettre à jour. <br/>
La propagation complète peut donc prendre plus de 5 minutes.<br/>

:::

Une version vidéo est disponible.

<iframe width="560" height="315" src="https://www.youtube.com/embed/mKki2xuD_k4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# Creation d'un compte Cloudflare {#create-account}

*Si vous avez déjà un compte Cloudflare, vous pouvez utiliser le compte existant, et passer à l'étape [suivante](#site)*

Rendez vous sur le [dashboard](https://dash.cloudflare.com/sign-up).<br/>

Remplissez le formulaire suivant :


![register](https://media.tutorapide.xyz/h61alzxn0kv4.png)

Lors de votre premier connexion il vous sera demandé d'ajoutez votre premier site.<br/>Puis faite **add site**.

*Pensez à confirmer votre adresse email*

### Ajoutez son site {#site}

![add_site](https://media.tutorapide.xyz/to7elxu8467e.png)

Il vas vous demander de choisir un plan. Nous allons selecionner le plan **Free**.<br/>Et faite **Continue**.

![free-plan](https://media.tutorapide.xyz/dopkrtq331at.png)

Un petit scan de votre site vous sera fait.<br/>

![scan](https://media.tutorapide.xyz/ch7byhuct0zn.png)

Une page avec des informations sur votre site vous sera affiché.<br/>Il ce peut que vous n'ayez pas de DNS.<br/>Faite **Continue**.<br/>

![dns](https://media.tutorapide.xyz/sxsota40h10f.png)

Si comme moi vous n'avez pas de DNS, une nouvelle fenetre va apparaitre pour vous dire que vous n'avez de dns.<br/>
Sois vous pouvez crée un zone DNS de type **A** avec l'ip de votre **serveur**.<br/>Sinon faites **Confirm**.<br/>

![vide](https://media.tutorapide.xyz/w4weglt7hkl0.png)

La parti la plus importante du processus est de changer les serveur DNS de **registra** de domaine par ceux de cloudflare.<br/>
Pour ce faire vous allez devoir vous rendre sur le pannel de votre registra de domaine pour changer c'est dns.<br/>
Vous allez touvez tout les informations que vous devrez renseignez chez votre registra sur la page suivate.<br/>
![](https://media.tutorapide.xyz/xhtrfnrkhqtz.png)

La ou vous avez marquez **Remove the following nameservers**.<br/> Il s'agit des serveurs DNS de votre registra de domaine.<br/>Que vous allez devoir remplacer par ceux de **Cloudflare** qui ce trouve juste au dessous.<br/>

Une fois que vous avez modifier les serveur DNS vous devriez avoir quelque chose qui resemble a ceci :

![registra_domaine](https://media.tutorapide.xyz/qwwd1o2cotxp.png)

Une fois que vous avez fait ceci, cliquer sur **Done, check nameservers**.<br/>

Une nouvelle page s'affiche , vous pouvez si vous les souhaitez cliquer que le bouton **Configuration Recommendations**, sinon faite **Skip Recommendations**.<br/>

Une fois que vous avez fait votre choix, vous allez arriver sur la page suivante.<br/>

![over](https://media.tutorapide.xyz/24txv6z4tlc8.png)

Une fois vos DNS de valider vous recevez un email de confirmation.<br/>

Le résulat une fois le domaine de valider.<br/>

![valide](https://media.tutorapide.xyz/pupmuk9xf60k.png)

Félicitation vous avez fini le processus de configuration de votre domaine.<br/>

Dernière mise à jour le **05/04/2022** par **Samuel*#7455 (Discord)**