---
title: Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren
description: Der Leiter für Vergütungen/Bezüge kann Mitarbeiter zu Plänen für feste Vergütung zuweisen, um ihren Grundlohn zu verwalten.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b7c2423faa4a0c50d9d319a9e6f489e2946c36a7
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071495"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Der Leiter für Vergütungen/Bezüge kann Mitarbeiter zu Plänen für feste Vergütung zuweisen, um ihren Grundlohn zu verwalten. Für dieses Verfahren wird vorausgesetzt, dass ein fester Plan erstellt wurde und aktiv ist und dass Berechtigungsregeln für den Plan festgelegt wurden. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Um das Verfahren zu starten, gehen Sie zu **Human Resources** > **Arbeitskräfte** > **Mitarbeiter** > **Vergütung** > **Fester Plan**.

1. Klicken Sie auf **Neu**.
2. Wählen Sie im Feld **Aktion** eine Aktivität bezüglich fester Vergütung vom Typ **Einstellen/Neu einstellen** aus, um die Änderung in der Mitarbeitervergütung zu beschreiben.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie im Feld **Position** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Die Ebene, die angezeigt wird, stammt aus dem Feld **Vergütung** Inforegister > **Ebene** von dem **Job**, der der **Position** zugeordnet ist. Die Ebene muss für den Einzelvorgang festgelegt werden, bevor dem Mitarbeiter eine Vergütung zugewiesen werden kann.  
6. Wählen Sie im Feld **Plan** den Plan für feste Vergütung für den Mitarbeiter aus. Das **Nachschlagefeld** ist so gefiltert, dass nur die Pläne angezeigt werden, für die der Mitarbeiter auf der Grundlage der **Zulassungsregeln** berechtigt ist.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Die Werte für **Gültigkeitsdatum** und **Ablaufdatum** für die Vergütung werden standardmäßig auf das Start- und Enddatum für die Positionszuweisung der Arbeitskraft festgelegt. Sie können diese Daten bei Bedarf ändern.  
    * Wenn der Plan mit fester Vergütung ein Schrittplan ist, wählen Sie den Schritt aus, der den korrekten Lohnsatz für den Mitarbeiter enthält. Wenn der Plan mit fester Vergütung ein gradueller oder flexibler Plan ist, geben Sie den Lohnsatz für den Mitarbeiter ein. Der Lohnsatz wird gegen die Toleranzeinstellungen für den Plan und die minimalen und maximalen Referenzpunkte für die Vergütungsstufe des Einzelvorgangs geprüft.  
8. Klicken Sie auf **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
