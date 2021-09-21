---
title: Abonnieren zum Verwenden von Bewertungen und Prüfungen
description: In diesem Thema wird erläutert, wie Sie sich für die Verwendung von Bewertungen und Prüfungen auf Ihrer Microsoft Dynamics 365 Commerce-Website anmelden.
author: gvrmohanreddy
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9fe8e9403ccbdc1e26620ae33c6a3866af06b23c
ms.sourcegitcommit: 81bc42551e6c9af6ad38908afb606ee1f8d3c44b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473428"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Nutzung von Bewertungen und Prüfungen aktivieren

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie sich für die Verwendung von Bewertungen und Prüfungen auf Ihrer Microsoft Dynamics 365 Commerce-Website anmelden.

Die Bewertungs- und Prüfungslösung ist eine Omnikanal-Lösung, die Sie in Dynamics 365 Commerce zur Verfügung stellen können, indem Sie Microsoft Dynamics Lifecycle Services (LCS) verwenden. LCS ist ein Verwaltungsportal, über das Einzelhändler ihre Umgebungen von der Bereitstellung bis zur Außerbetriebnahme verwalten.

Wenn Sie die Bewertungs- und Überprüfungslösung auf Ihrer Commerce-Website verwenden möchten, müssen Sie sich für Bewertungen und Überprüfungen während der Bereitstellung Ihrer E-Commerce-Website auf anmelden Dynamics 365 Commerce.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Abonnieren zum Verwenden von Bewertungen und Prüfungen

Führen Sie die folgenden Schritte aus, um die Verwendung von Bewertungen und Prüfungen auf Ihrer Site zu aktivieren.

1. Befolgen Sie die Schritte in [Eine neue E-Commerce-Webseite bereitstellen](deploy-ecommerce-site.md).
1. Navigieren Sie, während Sie sich noch im LCS befinden, zu **Einrichtung der Retail-Bereitstellung \> Andere Einstellungen**.
1. Legen Sie die Option **Bewertungs- und Prüfungsdienst aktivieren** auf **Ja** fest.
1. Geben Sie im Feld **AAD-Sicherheitsgruppe für Bewertungs- und Prüfungsmoderator** die ID der Microsoft Azure Active Directory-Sicherheitsgruppe (Azure AD) ein, die Bewertungs- und Prüfungsmoderatoren enthält.

    ![Nutzung von Bewertungen und Prüfungen aktivieren.](media/LCS_RnR_Preference.png)

1. Schließen Sie den E-Commerce-Initialisierungsprozess ab.

> [!NOTE] 
> Wenn Sie ein bestehender Dynamics 365 Commerce Kunde sind, der bereits eine E-Commerce-Website bereitgestellt hat, ohne sich für Bewertungen und Beurteilungen entschieden zu haben, und der jetzt Bewertungen und Beurteilungen vom Dynamics 365 Commerce-Paket verwenden möchte, sendet bitte eine Serviceanfrage. Informationen zum Senden einer Serviceanforderung finden Sie unter [Prozess zur Übermittlung von Serviceanfragen](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Bewertungen und Prüfungen](ratings-reviews-overview.md)

[Verwalten von Bewertungen und Prüfungen](manage-reviews.md)

[Konfigurieren von Bewertungen und Prüfungen](configure-ratings-reviews.md)

[Synchronisieren von Produktbewertungen in Dynamics 365 Commerce](sync-product-ratings.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
