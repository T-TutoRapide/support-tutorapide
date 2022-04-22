---
sidebar_position: 3
title: Valheim
description: Création du ip personalisé pour son serveur Valheim.
tags:
  - Valheim
  - ip personalisée
Author: Samuel*#7455 (Discord)
---

Dans ce tutoriel je vais vous montrer comment avoir une ip personnalisée pour votre serveur Valheim.

:::caution Cloudflare

Toute aux long de ce tutoriel je vais utiliser Cloudflare, si vous ne savez comment relier votre nom de domaine a Cloudflare, vous pouvez aller voir le tutoriel suivant <a href="../../Nom-de-domaine/cloudflare" target="_blank">Cloudflare</a>.

:::

:::note

Avant de commencer, je précise que les étapes suivantes fonctionnent si vous avez un VPS/Dedié.<br/>
Si vous avez un serveur de jeux (pas de full access) le manipulation peuvent être différente.

:::


## IP personnalisée Valheim

1. RRendez-vous sur le dashboard de votre compte Cloudflare, et cliquer sur votre site.

![](https://media.tutorapide.xyz/ihhkqqfqpa16.png)

2. Sur le panneau de gauche, cliquer sur le bouton **DNS**.

![](https://media.tutorapide.xyz/fl3fgbg6wn6o.png)

Dans cette nouvelle étape, nous allons créer 2 types de zone DNS, **A** et **SRV**.

Dans la fenêtre **Gestion DNS** pour votresite.Com. Cliquer sur **Ajouter un enregistrement**.

3. Creation de la zone DNS **A**.

  - Type: A
  - Nom: vlh
  - Adresse IPv4: IP de votre serveur Valheim ex. 192.168.1.1
  - TTL: Automatic TLL (default)

![](https://media.tutorapide.xyz/h3366rsaz8rr.png)

Puis faites enregistrer.

4. Creation de la zone DNS **SRV**.

  - Type: SRV
  - Nom: vlh
  - Service: _valheim
  - Protocols: TCP
  - Durée TTL: Automatic
  - Priorité: 0
  - Poids: 0
  - Port: 2456
  - Cible: vlh.votredomaine.com.

  ![](https://media.tutorapide.xyz/fb6mpljxgz6p.png)

Puis faites enregistrer.

  La création de votre ip pour votre serveur Valheim est terminé.

  Dernière mise à jour le **05/04/2022** par **Samuel*#7455 (Discord)**