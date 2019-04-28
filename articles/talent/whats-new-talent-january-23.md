---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (23. Januar 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f27698c257301f52e5c77eaa8a04ca13a0315825
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "859614"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a>Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (23. Januar 2019)

[!include [banner](includes/banner.md)]

**Build 8.1.2121**

In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.

## <a name="changes"></a>Änderungen

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a>Import von nicht funktionierenden Mitarbeiter-Festvergütungen beim Anlegen neuer Festvergütungssätze
Es wurde eine Änderung an der festen Vergütungseinheit vorgenommen, um die Vergütungshöhe beim Import abzurufen. Vor dieser Freigabe wurde eine Meldung angezeigt, die angab, dass der Level erforderlich war.

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a>Entfernen Sie das Feld Mindestguthaben aus dem Dialogfenster Urlaubsantrag.
Das Feld **Mindestguthaben** wurde aus dem Dialogfenster **Urlaubsantrag** entfernt. Diese Änderung betrifft alle Bereiche, in denen eine Freistellung beantragt werden kann.

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a>Datenaktualisierung für Vergütungsstufen, die nicht in allen Szenarien aktualisiert werden.
Es wurde eine Änderung vorgenommen, um die Vergütungshöhe bei festen Vergütungsplänen zu aktualisieren. Diese Änderung füllt die Vergütungsstufe bei festen Plänen für die dem Mitarbeiter zugeordnete Stelle.

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a>Abrechnungsinformationen auf der Seite Änderungen verwalten sind nur verfügbar, wenn Sie als Systemadministrator angemeldet sind
Diese Änderung ermöglicht Mitarbeitern mit der Rolle Sachbearbeiter Abrechnung den Zugriff auf die Abrechnungsinformationen auf der Seite **Änderungszeitachse > Änderungen verwalten** für die Planstelle.

### <a name="job-fields-default-to-positions"></a>Stellenfelder standardmäßig auf Planstellen voreingestellt
Wenn Sie die Stelle an einer Stelle ändern, werden die Stellenfelder standardmäßig auf die Stelle gesetzt. Es erscheint eine Warnmeldung, die die Möglichkeit bietet, die Standardwerte zu übernehmen oder die vorhandenen Werte für diese Felder beizubehalten.

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a>Probezeit und Kalender werden für zukünftige eingestellte Mitarbeiter nicht angezeigt.
Mit dieser Änderung wurden die Felder **Probezeit** und **Kalender** auf der Seite **Änderungen verwalten** hinzugefügt, um die Dateneingabe für zukünftige und ehemalige Mitarbeiter zu ermöglichen.

### <a name="platform-update-23"></a>Plattformupdate 23
Kleinere Bugfixes wurden im Rahmen des Plattform-Updates 23 aufgenommen. Weitere Informationen finden Sie unter [Was ist neu oder geändert in Dynamics 365 for Finance and Operations Plattform-Update 23 (Januar 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23). 
