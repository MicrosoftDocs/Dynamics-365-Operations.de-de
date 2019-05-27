---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent (14. Februar 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518060"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a>Neuerungen oder Änderungen in Dynamics 365 for Talent (14. Februar 2019)

[!include [banner](includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Talent entweder neu oder geändert sind.

## <a name="changes-in-attract"></a>Änderungen in Attract
Es gibt kleinere Fehlerkorrekturen in dieser Version.

## <a name="changes-in-onboarding"></a>Änderungen in Onboarding
Es gibt kleinere Fehlerkorrekturen in dieser Version.
 
## <a name="changes-in-core-hr"></a>Core HR-Änderungen 
**Build 8.1.2146**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>Die Entität für feste Mitarbeitervergütung exportiert nicht alle Datensätze
Mit dieser Änderung exportiert die Entität **Feste Mitarbeitervergütung** nun alle Datensätze. Die Entität kann verwendet werden, um vorhandene Datensätze mit fester Vergütung für Mitarbeiter zu erstellen und zu aktualisieren. 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>Das Enddatum der Beschäftigung berücksichtigt keine bevorzugten Zeitzoneneinstellungen für Mitarbeiter
Das Enddatum der Beschäftigung berücksichtigt nun bevorzugte Zeitzonen von Mitarbeitern beim Erstellen oder Beenden einer Beschäftigung.
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>Adressenanzeige für das Vereinigte Königreich in Analytics als Adressen der Ost-Schweiz angezeigt
In dieser Version wurde eine Änderung vorgenommen, um falsche Adressen in der **Personalführung** im Bericht „Mitarbeiterzahl nach Abteilung“ zu korrigieren.
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>Kündigungscode wird im Arbeitskraftpositions-Zuweisungsdatensatz nicht ausgefüllt, wenn die Position beendet wird
Eine Änderung am Standardcode für den Kündigungsgrund wurde vorgenommen, wenn die Mitarbeiterpositionszuweisung beendet wird.

### <a name="new-entity-created-for-job-compensation-levels"></a>Neue Entität für Stellenvergütungsstufen erstellt
Eine neue Datenverwaltungsframework (DMF)-Entität wurde erstellt. Die Entität stellt Erstellung und Aktualisierungen der Vergütungsstufen, Marktwerte und Umfrageinformationen zu den im System definierten Stellen bereit.
