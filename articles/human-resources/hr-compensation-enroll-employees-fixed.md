---
title: Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren
description: Der Leiter für Vergütungen/Bezüge kann Mitarbeiter zu Plänen für feste Vergütung zuweisen, um ihren Grundlohn zu verwalten.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3029e52a7cc1fb6dfda390f5d892c89f1eda8509
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429712"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren

Der Leiter für Vergütungen/Bezüge kann Mitarbeiter zu Plänen für feste Vergütung zuweisen, um ihren Grundlohn zu verwalten. Für dieses Verfahren wird vorausgesetzt, dass ein fester Plan erstellt wurde und aktiv ist und dass Berechtigungsregeln für den Plan festgelegt wurden. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Um das Verfahren zu starten, gehen Sie zu "Personalverwaltung" > "Arbeitskräfte" > "Mitarbeiter"  > "Vergütung" > "Fester Plan"

1. Klicken Sie auf "Neu".
2. Wählen Sie im Feld "Aktion" eine Aktivität bezüglich fester Vergütung vom Typ "Einstellen/Neu einstellen" aus, um die Änderung in der Mitarbeitervergütung zu beschreiben.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie im Feld "Position" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Die Ebene, die angezeigt wird, stammt aus der Vergütungsstufe des Einzelvorgangs in der Position. Die Ebene muss für den Einzelvorgang festgelegt werden, bevor dem Mitarbeiter eine Vergütung zugewiesen werden kann.  
6. Wählen Sie im Feld "Plan" den Plan für feste Vergütung für den Mitarbeiter aus. Die Plansuche wird gefiltert, um nur die Pläne anzuzeigen, für die der Mitarbeiter auf Grundlage der Berechtigungsregeln freigegeben wurde.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Die Gültigkeits- und die Ablaufdaten für die Vergütung werden standardmäßig auf das Start- und Enddatum für die Positionszuweisung der Arbeitskraft festgelegt. Sie können diese Daten bei Bedarf ändern.  
    * Wenn der Plan mit fester Vergütung ein Schrittplan ist, wählen Sie den Schritt aus, der den korrekten Lohnsatz für den Mitarbeiter enthält. Wenn der Plan mit fester Vergütung ein gradueller oder flexibler Plan ist, geben Sie den Lohnsatz für den Mitarbeiter ein. Der Lohnsatz wird gegen die Toleranzeinstellungen für den Plan und die minimalen und maximalen Referenzpunkte für die Vergütungsstufe des Einzelvorgangs geprüft.  
8. Klicken Sie auf "OK".

