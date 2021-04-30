---
title: Einen Urlaubsanforderungsworkflow erstellen
description: Erstellen Sie einen Workflow für Urlaubsanträge und Abwesenheitsanträge, um Urlaubsanträge in Dynamics 365 Human Resources konsistent zu verwalten.
author: andreabichsel
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb726f37d25e782a90938b7794be6dea2c30a7d5
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890722"
---
# <a name="create-a-leave-request-workflow"></a>Einen Urlaubsanforderungsworkflow erstellen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sie können einen Workflow für Urlaubsanträge und Abwesenheitsanträge erstellen, um Urlaubsanträge in Dynamics 365 Human Resources konsistent zu verwalten. Mit einem Workflow **Urlaub und Abwesenheit** können Sie:

- Aufgaben definieren
- Bestimmen, wer die Aufgaben ausführen muss
- Geben Sie an, wer Anforderungen genehmigen oder ablehnen kann

## <a name="create-a-leave-and-absence-request-workflow"></a>Eine Urlaubs- und Abwesenheitsworkflowanfrage erstellen

1. Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.

2. Unter **Einrichtung** wählen Sie **Personalverwaltungsparameter Workflows**.

3. Wählen Sie **Neu** und dann wählen Sie **Urlaubs- und Abwesenheitsantrag**. 

4. Wenn die Nachricht **Diese Datei öffnen?** erscheint, wählen Sie **Öffnen** und melden sich mit Ihren Unternehmensdaten an.

5. Verwenden Sie den Workflow-Editor, um einen Workflow für Ihre Urlaubsanträge zu erstellen. Weitere Informationen zum Arbeiten mit Workflows finden Sie unter [Erstellen Sie eine Workflow-Übersicht](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Datenelemente des Urlaubs- und Abwesenheitsanforderungs-Workflows

Mit den folgenden Datenelementen können Sie in Workflows bedingte oder automatische Genehmigungen für Urlaubs- und Abwesenheitsanträge erstellen:

- **Betrag**
- **Kommentar**
- **Firma**
- **Erstellt von**
- **Erstellungsdatum und -uhrzeit**
- **Enddatum**
- **Sonderurlaubstyp**
- **Geändert von**
- **Änderungsdatum und -uhrzeit**
- **Ursachencode**
- **Anforderungskennung**
- **Startdatum**
- **Status** 
- **Übermittlungsdatum**
- **Übermittelt von**
- **Übermittelt von der Personalverwaltung**
- **Übermittelt vom Manager**
- **Übermittelt im Auftrag von**
- **Worker**
- **Arbeitskrafttyp**

Diese Beispiele zeigen, wie Sie mithilfe dieser Datenelemente verschiedene Typen von Workflowbedingungen erstellen können:

- Verwenden Sie den **Ursachencode** in einer bedingten Anweisung zur Weiterleitung von Krankmeldungn mit dem Ursachencode **Medizinische Behandlung** an die Personalverwaltung zur Genehmigung, während alle anderen Ursachencodes an den Manager weitergeleitet werden. Weitere Informationen zu bedingten Anweisungen finden Sie unter [Konfigurieren bedingter Entscheidungen in einem Workflow](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md). 

- Verwenden Sie **Übermittelt von der Personalverwaltung** und **Übermittelt vom Manager** in einer automatischen Aktivität zum automatischen Genehmigen von Abwesenheitsanträgen, die diese Rollen im Auftrag von Mitarbeitern übermitteln. Weitere Informationen über automatische Aktivitäten finden Sie unter [Genehmigungsprozesse in einem Workflow konfigurieren](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Verwenden Sie **Urlaubstyp** in einer bedingten Anweisung oder einer automatischen Aktivität, um zu steuern, wie der Workflow Anforderungen mit bestimmten Abwesenheitstypen weiterleitet.

## <a name="see-also"></a>Siehe auch

- [Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]