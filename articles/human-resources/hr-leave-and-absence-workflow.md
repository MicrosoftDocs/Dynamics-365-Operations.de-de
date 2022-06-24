---
title: Einen Urlaubsanforderungsworkflow erstellen
description: Erstellen Sie einen Workflow für Urlaubsanträge und Abwesenheitsanträge, um Urlaubsanträge in Dynamics 365 Human Resources konsistent zu verwalten.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a4ce8d0a121e2fa24e3c221a30eb13debd6e44ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855085"
---
# <a name="create-a-leave-request-workflow"></a>Einen Urlaubsanforderungsworkflow erstellen

> [!Important]
> Die in diesem Artikel beschriebene Funktionalität ist derzeit für Kunden der eigenständigen Version von Dynamics 365 Human Resources verfügbar. Einige oder die gesamten Funktionen werden in einem zukünftigen Release der Finance-Infrastruktur nach Finance-Version 10.0.26 verfügbar sein.

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
