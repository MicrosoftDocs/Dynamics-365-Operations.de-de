---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (31. Januar 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fbbecd4e0f205c2f09ec30548756ff1a43872644
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899104"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (31. Januar 2019)

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

**Build 8.1.2128**

## <a name="core-hr-changes"></a>Core HR Änderungen

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Freizeit auf Urlaub genommen Leute Karte berücksichtigt nicht Urlaubsplan Daten
Für diejenigen, die Urlaubspläne haben, die nicht auf einem Kalenderjahr laufen, zeigt die Karte **Genommen** jetzt Urlaub an, der im planmäßig definierten Urlaubsjahr genommen wurde. Wenn beispielsweise das Urlaubsjahr eines Unternehmens vom 1. Juni bis zum 30. Mai dauert und ein Mitarbeiter im Dezember 3 Tage frei genommen hat, wird die **Genommen**-Karte am 15. Januar 3 Tage anzeigen. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Abgrenzungsbeträge, die nicht der Tier-Datumsbasis entsprechen.
Es wurden neue Urlaubs- und Abwesenheitsoptionen (**Personalparameter**) hinzugefügt, damit Kunden feststellen können, wann die Dienstzeit der Mitarbeiter wirksam ist. Für einige Unternehmen ist das Datum das Ende des Monats, für andere kann es der Beginn des nächsten Monats sein. So kann beispielsweise ein Unternehmen am 31. Dezember Urlaub gewähren, während ein anderes am 1. Januar Urlaub gewähren kann. Mit dieser Option können Sie wählen, wann der Award stattfinden soll. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Aktionen zur Einstellung von Arbeitnehmern sind im Zustand "Workflow abgeschlossen" stecken geblieben.
Es wurden Änderungen vorgenommen, um ein Problem zu beheben, bei dem eine kleine Anzahl von Workflows mit dem Status "Workflow abgeschlossen" beendet wurde. Neue Workflows sollten nun nach Beendigung des Workflows in den Zustand "Abgeschlossen" übergehen. Alle Workflows in einem abgeschlossenen Workflow-Status werden in einen Fehlerstatus überführt, um bei Bedarf eine Aktualisierung oder Entfernung zu ermöglichen. 
