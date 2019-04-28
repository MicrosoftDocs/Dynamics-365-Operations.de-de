---
title: Delegieren von Arbeitsaufgaben in einem Workflow
description: Wenn Sie für einige Zeit abwesend oder anderweitig für Arbeitsaufgaben nicht verfügbar sind, können Sie Ihre Arbeitsaufgaben an andere Benutzer delegieren oder diesen neu zuweisen.
author: jasongre
manager: AnnBe
ms.date: 04/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: feace647d7acef6abf86b13fcb8019c622c55ff6
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/12/2019
ms.locfileid: "976780"
---
# <a name="delegate-work-items-in-a-workflow"></a>Delegieren von Arbeitsaufgaben in einem Workflow

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a>Manuelles Delegieren einer Arbeitsaufgabe

Um eine einzelne Arbeitsaufgabe zu delegieren, wählen Sie die Option **Delegieren** im Menü **Workflow** aus, und geben Sie dann den Benutzer an, an den delegiert werden soll, zusammen mit einem Kommentar. Dadurch wird die Arbeitsaufgabe an diesen Benutzer neu zugewiesen, sodass sie ausgeführt werden kann.

## <a name="automatically-delegate-work-items"></a>Arbeitsaufgaben automatisch delegieren

Wenn Sie planen, für einen Zeitraum nicht im Büro anwesend oder anderweitig nicht verfügbar zu sein, um sich um Arbeitsaufgaben zu kümmern, können Sie neue Arbeitsaufgaben automatisch an andere Benutzer mithilfe der Seite **Benutzeroptionen** delegieren.

### <a name="set-up-automatic-delegation"></a>Einrichten der automatischen Delegierung
1. Gehen Sie zu > Allgemein > Benutzeroptionen.
2. Klicken Sie auf die Registerkarte „Workflow”.
    * Stellen Sie sicher, dass der Bereich „Delegation” erweitert ist.    Um das System so zu konfigurieren, dass Ihre Arbeitsaufgaben automatisch an andere Benutzer delegiert werden, müssen Sie Delegierungsregeln erstellen. Diese geben an, wann bestimmte Typen von Arbeitsaufgaben delegiert werden. Gehen Sie folgendermaßen vor, um eine Delegierungsregel zu erstellen.  
3. Klicken Sie auf Hinzufügen.
4. Wählen Sie im Feld „Bereich” eine Option aus.
    * Alle – Delegiert alle Arbeitsaufgaben, die Ihnen zugewiesen sind.    Modul – Delegiert nur die Arbeitsaufgaben, die mit einem bestimmten Workflowtyp zusammenhängen. Wenn Sie diese Option aktivieren, müssen Sie den Workflowtyp im Feld „Name” auswählen.    Workflow – Delegiert nur die Arbeitsaufgaben, die mit einem bestimmten Workflow zusammenhängen. Wenn Sie diese Option aktivieren, müssen Sie den Workflow im Feld „Name” auswählen.  
5. Wählen Sie im Feld „Delegat” den Benutzer aus, an den die Arbeitsaufgaben delegiert werden sollen.
    * Geben Sie in den Feldern Startdatum/-zeit und Enddatum/-zeit an, wann die Arbeitsaufgaben automatisch delegiert werden sollten.  
6. Geben Sie im Feld „Startdaum/-uhrzeit” ein Datum und eine Uhrzeit ein.
7. Geben Sie im Feld „Enddatum/-uhrzeit” ein Datum und eine Uhrzeit ein.
8. Aktivieren Sie die Delegierungsregel durch Aktivieren des Kontrollkästchens „Aktiviert”.
    * Wenn Sie „Modul” als den „Bereich” ausgewählt haben, müssen Sie das Modul im Feld „Name” auswählen.    Wenn Sie „Workflow” als den „Bereich” ausgewählt haben, müssen Sie den spezfischen zu delegierenden Workflow im Feld „Name” auswählen.  
9. Geben Sie im Feld „Kommentar” einen Kommentar ein, der den Grund für die Delegierung der Arbeitsaufgaben erläutert.

