---
title: Regeln für Aufgabentrennung einrichten
description: Sie können Regeln einrichten, Aufgaben abzugrenzen, die von unterschiedlichen Benutzern ausgeführt werden müssen.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40b40b77877680e28671b7a15ea8c8b58ce94417
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180874"
---
# <a name="set-up-segregation-of-duties"></a>Regeln für Aufgabentrennung einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Sie können Regeln einrichten, Aufgaben abzugrenzen, die von unterschiedlichen Benutzern ausgeführt werden müssen. Dieses Konzept wird Aufgabentrennung benannt. Beispielsweise kann die gleiche Person des Eingangs von Waren bestätigen und Zahlung an den Kreditor nicht verarbeiten. Aufgabentrennungshilfen reduzieren Sie das Risiko des Betrugs und es auch Hilfsprogrammen, die Sie Fehler oder Unregelmäßigkeiten erkennen. Sie können Aufgabentrennung auch verwenden, um Richtlinien der internen Kontrolle zu erzwingen. Gehen Sie zum Erstellen einer Regel folgendermaßen vor. Sie müssen ein -Systemadministrator sein, um dieses Verfahren auszuführen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DAT. 

1. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Aufgabentrennung > Aufgabentrennungsregeln**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Name** einen Wert für die Regel ein.
4. Klicken Sie im Feld **Erste Aufgabe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wählen Sie die erste Aufgabe, die mit der Regel gesteuert wird.
6. Klicken Sie im Feld **Zweite Aufgabe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen. 
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wählen Sie die zweite Aufgabe, die mit der Regel gesteuert wird.
10. Wählen Sie im Feld **Schweregrad** eine Option aus. Wählen Sie hier den Schweregrad des Risikos aus, das auftritt, wenn der gleiche Benutzer oder die gleiche Rolle beide Aufgaben ausführt.  
11. Geben Sie im Feld **Sicherheitsrisiko** einen Wert ein. Beschreibung des Sicherheitsrisikos eingeben.  
12. Geben Sie im Feld **Sicherheitsbehandlung** einen Wert ein. Geben Sie eine Beschreibung der Aktivitäten ein, die Sie nehmen, um das Sicherheitsrisiko zu minimieren. So können Sie das Risiko minimieren, indem Sie detailliertere Überprüfung des Prozesses durchführen, indem Sie einen Monatsverwaltungsreview tätigen oder indem Sie Ressourcen mit anderen Abteilungen freigeben.     
13. Klicken Sie auf **Speichern**.

