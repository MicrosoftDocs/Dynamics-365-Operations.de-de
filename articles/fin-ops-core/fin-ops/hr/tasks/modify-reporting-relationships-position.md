---
title: Berichtsbeziehungen für eine Position ändern
description: Diese Prozedur zeigt, wie Berichtsbeziehungen für einen Mitarbeiter geändert werden.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a1afd2c1cdc2ebaa303030d01b3bbe5fd2af44f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178006"
---
# <a name="modify-reporting-relationships-for-a-position"></a>Berichtsbeziehungen für eine Position ändern

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie Berichtsbeziehungen für einen Mitarbeiter geändert werden. Die Berichtbeziehungen können für das Weiterleiten von Dokumenten durch Workflow verwendet werden. Die Prozedur zeigt auch, wie Sie den Mitarbeiter weiteren Hierarchien zuweisen. Beispielsweise kann ein Mitarbeiter Teil eines Projektteams mit informellen Berichtsbeziehungen zu einem Projekt-Supervisor sein. Zusätzliche Berichtsbeziehungen können für die Position definiert werden, um verschiedene Projekt- oder Matrixszenarien zu berücksichtigen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.

1. Wechseln Sie zu "Personalverwaltung" > "Positionen" > "Positionen".
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Position" mit dem Wert "000091".
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Erweitern Sie die Berichte um den Abschnitt "Position".
5. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
6. Geben Sie im Feld "Vorgesetzter" einen Wert ein, oder wählen Sie einen Wert aus.
7. Klicken Sie auf "Erstellen".
8. Erweitern Sie den Abschnitt 'Beziehungen'.
9. Klicken Sie auf Hinzufügen.
10. Aktivieren Sie das Kontrollkästchen in der Kopfzeile von ''.
11. Geben Sie im Feld "Hierarchiename" einen Wert ein, oder wählen Sie einen Wert aus.
    * Beispiel: Projekt  
12. Geben Sie im Feld "Position" einen Wert ein, oder wählen Sie einen Wert aus.  Beispiel: 000437
13. Klicken Sie auf "Speichern".
