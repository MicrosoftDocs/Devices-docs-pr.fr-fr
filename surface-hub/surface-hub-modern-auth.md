---
title: Authentification moderne sur SurfaceHub
description: Cette page décrit l’utilisation de l’authentification moderne sur Surface Hub par opposition à l’authentification de base héritée.
keywords: séparer les valeurs par des virgules
ms.prod: surface-hub
ms.sitesec: library
author: greg-lindsay
ms.author: greglin
manager: laurawi
audience: Admin
ms.topic: article
ms.date: 12/10/2020
ms.localizationpriority: Medium
appliesto:
- Surface Hub 2S 2020 Update
ms.openlocfilehash: 1674b7abd74a666e2ab1040f66d9ea548ab3c201
ms.sourcegitcommit: 7e1b351024e33926901ddbdc562ba12aea0b4196
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "11385162"
---
# <a name="modern-authentication-on-surface-hub"></a>Authentification moderne sur SurfaceHub

Windows 10 Team 2020 Update ajoute la prise en charge de l’authentification moderne du compte d’appareil Hub dans certains scénarios. Une fois que vous avez installé la mise à jour 2020, vous pouvez migrer de l’authentification de base héritée pour utiliser les dernières améliorations de sécurité si le compte d’appareil s’authentifier via Azure Active Directory et que la boîte aux lettres du compte est hébergée dans Exchange Online. Avec la mise à jour 2020, le Surface Hub prend en charge les protocoles des services web Exchange (EWS) et l’authentification basée sur la bibliothèque d’authentification Active Directory (ADAL) lors de la synchronisation du compte d’appareil avec Exchange Online.

Pour les nouveaux comptes basés sur le cloud, le Surface Hub utilise automatiquement l’authentification moderne pour se connecter à Exchange Online sans nécessiter de configuration supplémentaire au-delà de la simple création de comptes d’appareil au format [alias@contoso.com](mailto:alias@contoso.com). N’utilisez pas le format hérité : Contoso\alias, qui n’est pas pris en charge pour l’authentification moderne. Pour plus d’informations, voir [Créer un compte d’appareil Surface Hub 2S.](https://docs.microsoft.com/surface-hub/surface-hub-2s-account)

> [!NOTE]
> Le Surface Hub ne prend pas en charge l’authentification moderne pour les comptes locaux. Les comptes doivent être créés dans le cloud.

