---
sidebar_position: 3
title: ip peronnalisée
---
Dans ce tutoriel je vais vous montrer comment avoir une ip personnalisée pour vos serveur de jeux ou serveur vocaux.

:::caution Cloudflare

Toute aux long de ce tutoriel je vais utiliser Cloudflare, si vous ne savez comment relier votre nom de domaine a Cloudflare, vous pouvez aller voir le tutoriel suivant <a href="cloudflare" target="_blank">Cloudflare</a>.

:::

## IP personnalisée minecraft

Une version vidéo est disponible.

:::note

Avant de commencez je précise que les étapes suivante fonctionne si vous avez un VPS/Dedié.<br/>
Si vous avez un serveur de jeux (pas de full access) le manipulation peuvent etre différente

:::

<iframe width="560" height="315" src="https://www.youtube.com/embed/DM70XFo95oM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

1. Rendez vous sur le dashboard de votre compte Cloudflare, et cliquer sur votre site.

![](https://media.tutorapide.xyz/ihhkqqfqpa16.png)

2. Sur le panneau de gauche, cliquer sur le bouton **DNS**.

![](https://media.tutorapide.xyz/fl3fgbg6wn6o.png)

Dans cette nouvelle étape nous crée 2 type de zone DNS, **A** et **SRV**.

Dans la fenétre **Gestion DNS pour votresite.Com**. Cliquer sur **Ajouter un engregistrement**.

3. Creation de la zone DNS **A**.

  - Type: A
  - Nom: play
  - Adresse IPv4: IP de votre serveur minecraft ex. 192.168.1.1
  - TTL: Automatic TLL (default)

![](https://media.tutorapide.xyz/8mg8nl6k6162.png)

Puis faites engregistrer.

4. Creation de la zone DNS **SRV**.

  - Type: SRV
  - Nom: play
  - Service: _minecraft
  - Protocols: _tcp
  - Durée TTL: Automatic
  - Priorité: 0
  - Poid: 0
  - Port: 25565
  - Cible: play.votredomaine.com.

  ![](https://media.tutorapide.xyz/k5hfi53bctwm.png)

  Puis faites engregistrer.

  La creation de votre ip pour votre serveur minecraft est terminé.

## IP personnalisée Teamspeak

## IP personnalisée Valheim