---
title: Einen Workflow zum Kaufen und Verkaufen von Urlaubsanforderungen erstellen
description: Erstellen Sie einen Workflow zum Kaufen und Verkaufen von Urlaubsanforderungen, um Urlaubsanforderungen in Dynamics 365 Human Resources konsistent zu kaufen und zu verkaufen.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5bc31740218e3f171d89debace339dee0177d826
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053970"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>Einen Workflow zum Kaufen und Verkaufen von Urlaubsanforderungen erstellen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sie können in Dynamics 365 Human Resources einen Workflow erstellen, um Ihre Käufe und Verkäufe von Urlaubsanforderungen konsistent zu verwalten. Ein Workflow zum **Kaufen und Verkaufen von Urlaub** ermöglicht Ihnen:

- Aufgaben definieren
- Bestimmen, wer die Aufgaben ausführen muss
- Geben Sie an, wer Anforderungen genehmigen oder ablehnen kann

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>Einen Workflow zum Kaufen und Verkaufen von Urlaubsanforderungen erstellen

1. Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.

2. Unter **Einrichtung** wählen Sie **Personalverwaltungsparameter Workflows**.

3. Wählen Sie **Neu** aus, und dann wählen Sie **Urlaubsanforderung kaufen und verkaufen** aus. 

4. Wenn die Nachricht **Diese Datei öffnen?** erscheint, wählen Sie **Öffnen** und melden sich mit Ihren Unternehmensdaten an.

5. Verwenden Sie den Workflow-Editor, um einen Workflow für Ihre Urlaubsanträge zu erstellen. Weitere Informationen zum Arbeiten mit Workflows finden Sie unter [Erstellen Sie eine Workflow-Übersicht](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Datenelemente des Urlaubs- und Abwesenheitsanforderungs-Workflows

Mit den folgenden Datenelementen können Sie in Workflows bedingte oder automatische Genehmigungen zum Kauf und Verkauf von Urlaubsanforderungen erstellen:

- **Betrag**
- **Richtlinie zum Kauf und Verkauf von Urlaub**
- **Firma**
- **Erstellt von**
- **Datum und Uhrzeit der Erstellung**
- **Enddatum**
- **Urlaubstyp**
- **Geändert von**
- **Änderungsdatum und -uhrzeit**
- **Anforderungskennung**
- **Startdatum**
- **Status** 
- **Übermittlungsdatum**
- **Übermittelt von**
- **Übermittelt von der Personalverwaltung**
- **Übermittelt vom Manager**
- **Übermittelt im Auftrag von**
- **Worker**

## <a name="workflow-examples"></a>Workflowbeispiele

Diese Beispiele zeigen, wie Sie mithilfe dieser Datenelemente verschiedene Typen von Workflowbedingungen erstellen können:

- Verwenden Sie **Übermittelt von der Personalverwaltung** und **Übermittelt vom Manager** in einer automatischen Aktivität zum automatischen Genehmigen des Kaufs und Verkaufs von Urlaubsanforderungen, die diese Rollen im Auftrag von Mitarbeitern übermitteln. Weitere Informationen über automatische Aktivitäten finden Sie unter [Genehmigungsprozesse in einem Workflow konfigurieren](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Verwenden Sie **Urlaubstyp** in einer bedingten Anweisung oder einer automatischen Aktivität, um zu steuern, wie der Workflow Anforderungen mit bestimmten Abwesenheitstypen weiterleitet.

## <a name="see-also"></a>Siehe auch

[Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)<br>
[Kauf- und Verkaufsurlaubsrichtlinien verwalten](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]