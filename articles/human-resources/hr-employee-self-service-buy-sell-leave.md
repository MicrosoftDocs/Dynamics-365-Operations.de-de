---
title: Urlaub kaufen und verkaufen
description: In Dynamics 365 Human Resources können Sie Anfragen zum Kauf und Verkauf von Urlaub auf der Grundlage der von Ihrem Unternehmen eingerichteten Richtlinien für den Kauf und Verkauf von Urlaub stellen.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271483"
---
# <a name="buy-and-sell-leave"></a>Urlaub kaufen und verkaufen

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

Wenn ein Workflow für eine Kauf- oder Verkaufsabwesenheitsanforderung fehlschlägt, können Benutzer mit der Berechtigung **EssLeaveBuySellRequestApprover** das Nachrichtenprotokoll für alle Kauf- und Verkaufsabwesenheitsanforderungen überprüfen. Gehen Sie dazu auf **Urlaub und Abwesenheit > Link > Urlaubskäufe und -verkäufe > Meldungsprotokoll** (links oben). Das **Meldungsprotokoll** zeigt dem Benutzer, wie die Transaktionen verarbeitet wurden und die dazugehörige Workflow-Historie.


## <a name="see-also"></a>Siehe auch

[Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)</br>
[Kauf- und Verkaufsurlaubsrichtlinien verwalten](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
