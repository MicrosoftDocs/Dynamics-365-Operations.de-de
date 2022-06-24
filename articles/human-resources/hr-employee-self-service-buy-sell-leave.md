---
title: Urlaub kaufen und verkaufen
description: In diesem Artikel wird beschrieben, wie Sie Anfragen zum Kaufen und Verkaufen von Urlaub in Dynamics 365 Human Resources übermitteln.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a6d38a69a73ce14f099beb6b6b560bf6c5686b0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875712"
---
# <a name="buy-and-sell-leave"></a>Urlaub kaufen und verkaufen


>[!Important]
>Die in diesem Artikel beschriebene Funktionalität ist derzeit für Kunden der eigenständigen Version von Dynamics 365 Human Resources verfügbar. Einige oder die gesamten Funktionen werden in einem zukünftigen Release der Finance-Infrastruktur nach Finance-Version 10.0.26 verfügbar sein.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In Dynamics 365 Human Resources können Sie Anfragen zum Kauf und Verkauf von Urlaub auf der Grundlage der von Ihrem Unternehmen eingerichteten Richtlinien für den Kauf und Verkauf von Urlaub stellen.  

## <a name="request-to-buy-leave"></a>Antrag auf Urlaub kaufen

1. In dem **Mitarbeiter Selbstservice** Arbeitsbereich wählen Sie **Antrag auf Urlaub kaufen** in der Kachel **Freizeitguthaben**. 

2. Fügen Sie **Urlaubstyp** hinzu und geben Sie einen **Menge** für die Menge an Urlaub ein, die Sie kaufen möchten. 

3. Wählen **einreichen**, wenn Sie bereit sind, Ihre Anfrage einzureichen. 

Ihre Guthaben werden entweder automatisch aktualisiert oder durchlaufen vor der Aktualisierung einen Genehmigungsprozess. Dies hängt davon ab, wie die Kaufrichtlinie konfiguriert wurde.

## <a name="request-to-sell-leave"></a>Antrag, Urlaub zu verkaufen

1. Wählen Sie im Arbeitsbereich **Employee Self-Service** die Option **Urlaubsanforderung verkaufen** in der Kachel **Salden arbeitsfreier Zeiten**. 

2. Fügen Sie einen **Urlaubstyp** hinzu und geben Sie eine **Menge** für die Menge an Urlaub ein, die Sie verkaufen möchten. 

3. Wählen **einreichen**, wenn Sie bereit sind, Ihre Anfrage einzureichen.

Ihre Guthaben werden entweder automatisch aktualisiert oder durchlaufen vor der Aktualisierung einen Genehmigungsprozess. Dies hängt davon ab, wie die Kaufrichtlinie konfiguriert wurde.


## <a name="troubleshooting"></a>Problembehandlung 

Wenn ein Workflow für eine Kauf- oder Verkaufsabwesenheitsanforderung fehlschlägt, können Benutzer mit der Berechtigung **EssLeaveBuySellRequestApprover** das Nachrichtenprotokoll für alle Kauf- und Verkaufsabwesenheitsanforderungen überprüfen. Gehen Sie hierfür zu **Urlaub und Abwesenheit > Links > Urlaubskäufe und -verkäufe > Meldungsprotokoll** (links oben). Das **Meldungsprotokoll** zeigt dem Benutzer, wie die Transaktionen verarbeitet wurden und die dazugehörige Workflow-Historie.


## <a name="see-also"></a>Siehe auch

[Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)</br>
[Kauf- und Verkaufsurlaubsrichtlinien verwalten](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
