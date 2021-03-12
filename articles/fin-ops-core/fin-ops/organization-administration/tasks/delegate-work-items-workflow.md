---
title: Delegieren von Arbeitsaufgaben in einem Workflow
description: Wenn Sie für einige Zeit abwesend oder anderweitig für Arbeitsaufgaben nicht verfügbar sind, können Sie Ihre Arbeitsaufgaben an andere Benutzer delegieren oder diesen neu zuweisen.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48d8fd06217d318fa8208e11ffa5624f6be25be1
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796705"
---
# <a name="delegate-work-items-in-a-workflow"></a>Delegieren von Arbeitsaufgaben in einem Workflow

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>Manuelles Delegieren einer Arbeitsaufgabe

Um eine einzelne Arbeitsaufgabe zu delegieren, wählen Sie die Option **Delegieren** im Menü **Workflow** aus, und geben Sie dann den Benutzer an, an den delegiert werden soll, zusammen mit einem Kommentar. Dadurch wird die Arbeitsaufgabe an diesen Benutzer neu zugewiesen, sodass sie ausgeführt werden kann.

## <a name="manually-delegate-multiple-work-items"></a>Manuelles Delegieren mehrerer Arbeitsaufgaben

Mehrere Arbeitsaufgaben können zusammen über die Seite **Mir zugewiesene Arbeitsaufgaben** delegiert werden. Die folgenden Workflowtypen können für die Massendelegierung verwendet werden: Workflow zur Genehmigung von Kaufverträgen, Workflow für Bestellungen, Workflow zur Überprüfung von Bestellanforderungen und Workflow für Kreditorenrechnungen. Die Funktion **Mehrere Arbeitsaufgaben delegieren** ist standardmäßig deaktiviert und kann unter **Arbeitsbereiche > Funktionsverwaltung** aktiviert werden. Bitten Sie Ihren Systemadministrator um Hilfe, um diese Funktion zu aktivieren.
1.  Wechseln Sie zu **Allgemeines > Allgemeines > Arbeitsaufgaben > Mir zugewiesene Arbeitsaufgaben**.
2.  Wählen Sie die Arbeitsaufgaben aus, die delegiert werden sollen.
3.  Klicken Sie auf das Menü **Arbeitsaufgaben delegieren**.
4.  Wählen Sie im Feld **Benutzer** den Benutzer aus, an den die Arbeitsaufgaben delegiert werden sollen.
5.  Geben Sie in das Feld **Kommentar** einen Kommentar ein, der den Grund für die Delegierung der Arbeitsaufgaben erläutert.
6.  Klicken Sie auf die Schaltfläche **Arbeitsaufgaben delegieren**, um die Delegierung der Arbeitsaufgaben abzuschließen.

## <a name="automatically-delegate-work-items"></a>Arbeitsaufgaben automatisch delegieren

Wenn Sie planen, für einen Zeitraum nicht im Büro anwesend oder anderweitig nicht verfügbar zu sein, um sich um Arbeitsaufgaben zu kümmern, können Sie neue Arbeitsaufgaben automatisch an andere Benutzer mithilfe der Seite **Benutzeroptionen** delegieren.

### <a name="set-up-automatic-delegation"></a>Einrichten der automatischen Delegierung
1. Gehen Sie zu **Allgemein > Einstellungen > Benutzeroptionen**.
2. Klicken Sie auf die Registerkarte **Workflow** und überprüfen Sie, ob der Abschnitt „Delegierungׅ“ erweitert ist. Um das System so zu konfigurieren, dass Ihre Arbeitsaufgaben automatisch an andere Benutzer delegiert werden, müssen Sie Delegierungsregeln erstellen. Diese geben an, wann bestimmte Typen von Arbeitsaufgaben delegiert werden. Gehen Sie folgendermaßen vor, um eine Delegierungsregel zu erstellen.  
3. Klicken Sie auf **Hinzufügen**.
4. Wählen Sie im Feld **Bereich** eine Option aus:
    - Alle – Delegiert alle Arbeitsaufgaben, die Ihnen zugewiesen sind.
    - Modul – Delegiert nur die Arbeitsaufgaben, die mit einem bestimmten Workflowtyp zusammenhängen. Wenn Sie diese Option auswählen, müssen Sie den Workflowtyp im Feld **Name** auswählen.
    - Workflow – Delegiert nur die Arbeitsaufgaben, die mit einem bestimmten Workflow zusammenhängen. Wenn Sie diese Option aktivieren, müssen Sie den Workflow im Feld **Name** auswählen.  
5. Im Feld **Name**:
    - Für den Bereich **Modul** wählen Sie das Zielmodul aus.
    - Für den Bereich **Workflow** wählen Sie den Zielworkflow aus.
6. Wählen Sie im Feld **Delegat** den Benutzer aus, an den die Arbeitsaufgaben delegiert werden sollen. Verwenden Sie die Felder **Startdatum/-uhrzeit** und **Enddatum/-uhrzeit**, um anzugeben, wann die Arbeitsaufgaben automatisch delegiert werden sollten.  
7. Geben Sie im Feld **Startdatum/-uhrzeit** ein Datum und eine Uhrzeit ein.
8. Geben Sie im Feld **Enddatum/-uhrzeit** ein Datum und eine Uhrzeit ein.
9. Aktivieren Sie die Delegierungsregel durch Aktivieren des Kontrollkästchens **Aktiviert**. 
10. Geben Sie in das Feld **Kommentar** einen Kommentar ein, der den Grund für die Delegierung der Arbeitsaufgaben erläutert.
