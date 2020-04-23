---
title: Debitorentreuekarten und Belohnungspunkte
description: Dieses Thema beschreibt die Integration von Daten zu Kundenbindungskarten und Prämienpunkten zwischen Finance and Operations-Apps und Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172968"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Debitorentreuekarten und Belohnungspunkte

[!include [banner](../../includes/banner.md)]



Unternehmen klassifizieren Kunden und bieten anspruchsvolle Dienstleistungen basierend auf Kundeneinkaufs- und Ausgabenmustern. In der Microsoft Dynamics 365-Anwendungssuite verfügt Dynamics 365 Commerce über die Infrastruktur und Funktionen zur Erleichterung und Verwaltung von Kundenbindungskarten, Prämienpunkten, loyalitätsbasierten Preisen und belohnungsbasierten Einkaufserlebnissen. Wenn Daten zu Kundenbindungskarten und Prämienpunkten in Commerce mit dem Common Data Service synchronisiert werden, können modellgesteuerte Apps in Dynamics 365 diese Daten verwenden. Beispielsweise können Benutzer des Dynamics 365 Customer Service die Daten verwenden, um über den Helpdesk dieselben anspruchsvollen Dienste bereitzustellen.

## <a name="templates"></a>Vorlagen

| Finance and Operations Apps | Modellgesteuerte Anwendungen in Dynamics 365 | Beschreibung |
|-----------------------------|-----------------------------------|-------------|
| Treuekarte                | msdyn\_loyaltycards               | Diese Vorlage synchronisiert Informationen über Treukarten von Debitoren. |
| Treuebelohnungspunkte       | msdyn\_loyaltyrewardpoints        | Diese Vorlage synchronisiert Informationen über Belohnungspunkte von Debitoren. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]