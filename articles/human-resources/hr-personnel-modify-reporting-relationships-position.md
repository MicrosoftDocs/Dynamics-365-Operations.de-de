---
title: Berichtsbeziehungen für eine Position ändern
description: Diese Prozedur zeigt, wie Berichtsbeziehungen für einen Mitarbeiter geändert werden.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ad7220661677ce72168d20903486230411ec00f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688523"
---
# <a name="modify-reporting-relationships-for-a-position"></a>Berichtsbeziehungen für eine Position ändern


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Diese Prozedur zeigt, wie Berichtsbeziehungen für einen Mitarbeiter geändert werden. Die Berichtbeziehungen können für das Weiterleiten von Dokumenten durch Workflow verwendet werden. Die Prozedur zeigt auch, wie Sie den Mitarbeiter weiteren Hierarchien zuweisen. Beispielsweise kann ein Mitarbeiter Teil eines Projektteams mit informellen Berichtsbeziehungen zu einem Projekt-Supervisor sein. Zusätzliche Berichtsbeziehungen können für die Position definiert werden, um verschiedene Projekt- oder Matrixszenarien zu berücksichtigen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.

1. Wechseln Sie zu **Personalverwaltung** \> **Positionen** \> **Positionen**.
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise auf einen Wert von **000091** für das Feld **Position**.
3. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
4. Erweitern Sie den Abschnitt **Berichte an Position**.
5. Wählen Sie **Neu** aus, um das Dropdown-Dialogfeld zu öffnen.
6. Geben Sie im Feld **Vorgesetzter** einen Wert ein, oder wählen Sie einen Wert aus.
7. Wählen Sie **Erstellen** aus.
8. Erweitern Sie den Abschnitt **Beziehungen**.
9. Wählen Sie **Hinzufügen** aus.
10. Aktivieren Sie das Kontrollkästchen auf der linken Seite.
11. Geben Sie im Feld **Hierarchiename** einen Wert ein, oder wählen Sie einen Wert aus (zum Beispiel **Projekt**).
12. Geben Sie im Feld **Berichte an Position** einen Wert ein, oder wählen Sie einen Wert aus (zum Beispiel **000437**).
13. Wählen Sie **Speichern** aus.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
