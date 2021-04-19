---
title: Debitorentreuekarten und Belohnungspunkte
description: In diesem Thema wird die Integration von Daten zu Kundenbindungskarten und Prämienpunkten mit dualem Schreiben beschrieben.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: d2c3845c1a7371d9e992495246e8dd0eb8631020
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747986"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Debitorentreuekarten und Belohnungspunkte

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Unternehmen klassifizieren Kunden und bieten anspruchsvolle Dienstleistungen basierend auf Kundeneinkaufs- und Ausgabenmustern. Beispielsweise verfügt Dynamics 365 Commerce über die Infrastruktur und Funktionen zur Erleichterung und Verwaltung von Kundenbindungskarten, Prämienpunkten, loyalitätsbasierten Preisen und belohnungsbasierten Einkaufserlebnissen. Wenn Daten zu Kundenbindungskarten und Prämienpunkten in Commerce mit Dataverse synchronisiert werden, können Customer Engagement-Apps diese Daten verwenden. Beispielsweise können Benutzer des Dynamics 365 Customer Service die Daten verwenden, um über den Helpdesk dieselben anspruchsvollen Dienste bereitzustellen.

## <a name="templates"></a>Vorlagen

| Finance and Operations Apps | Modellgesteuerte Anwendungen in Dynamics 365 | Beschreibung |
|-----------------------------|-----------------------------------|-------------|
| Treuekarte                | msdyn\_loyaltycards               | Diese Vorlage synchronisiert Informationen über Treukarten von Debitoren. |
| Treuebelohnungspunkte       | msdyn\_loyaltyrewardpoints        | Diese Vorlage synchronisiert Informationen über Belohnungspunkte von Debitoren. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]