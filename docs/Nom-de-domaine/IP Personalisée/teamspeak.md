---
sidebar_position: 2
title: TeamSpeak
---

Dans ce tutoriel je vais vous montrer comment avoir une ip personnalisée pour votre serveur TeamSpeak.

:::caution Cloudflare

Toute aux long de ce tutoriel je vais utiliser Cloudflare, si vous ne savez comment relier votre nom de domaine a Cloudflare, vous pouvez aller voir le tutoriel suivant <a href="../../Nom-de-domaine/cloudflare" target="_blank">Cloudflare</a>.

:::

:::note

Avant de commencez je précise que les étapes suivante fonctionne si vous avez un VPS/Dedié.<br/>
Si vous avez un serveur spécial teampspeak (pas de full access) le manipulation peuvent etre différente

:::

## IP personnalisée Teamspeak

1. Rendez vous sur le dashboard de votre compte Cloudflare, et cliquer sur votre site.

![](https://media.tutorapide.xyz/ihhkqqfqpa16.png)

2. Sur le panneau de gauche, cliquer sur le bouton **DNS**.

![](https://media.tutorapide.xyz/fl3fgbg6wn6o.png)

Dans cette nouvelle étape nous crée 2 type de zone DNS, **A** et **SRV**.

Dans la fenétre **Gestion DNS pour votresite.Com**. Cliquer sur **Ajouter un engregistrement**.

3. Creation de la zone DNS **A**.

  - Type: A
  - Nom: ts
  - Adresse IPv4: IP de votre serveur TeamSpeak ex. 192.168.1.1
  - TTL: Automatic TLL (default)

![](https://media.tutorapide.xyz/7fzpvxvt248s.png)

Puis faites engregistrer.

4. Creation de la zone DNS **SRV**.

  - Type: SRV
  - Nom: ts
  - Service: _ts3
  - Protocols: UDP
  - Durée TTL: Automatic
  - Priorité: 0
  - Poids: 5
  - Port: 9987
  - Cible: ts.votredomaine.com.

  ![](https://media.tutorapide.xyz/t1b3cxzhlxqd.png)

  Puis faites engregistrer.

  La creation de votre ip pour votre serveur TeamSpeak est terminé.