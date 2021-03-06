---
title: Regeln für Aufgabentrennung einrichten
description: Sie können Regeln einrichten, Aufgaben abzugrenzen, die von unterschiedlichen Benutzern ausgeführt werden müssen.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e25fee324ce95cd04b86ee0e4e6a56cfacb61a53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745740"
---
# <a name="set-up-segregation-of-duties"></a>Regeln für Aufgabentrennung einrichten

[!include [banner](../../includes/banner.md)]

Sie können Regeln einrichten, Aufgaben abzugrenzen, die von unterschiedlichen Benutzern ausgeführt werden müssen. Dieses Konzept wird Aufgabentrennung benannt. Beispielsweise kann es sein, dass Sie nicht möchten, dass dieselbe Person den Wareneingang bestätigt und sich um die Bezahlung des Lieferanten kümmert. Aufgabentrennungshilfen reduzieren Sie das Risiko des Betrugs und es auch Hilfsprogrammen, die Sie Fehler oder Unregelmäßigkeiten erkennen. Sie können Aufgabentrennung auch verwenden, um Richtlinien der internen Kontrolle zu erzwingen. Gehen Sie zum Erstellen einer Regel folgendermaßen vor. Sie müssen ein -Systemadministrator sein, um dieses Verfahren auszuführen.

1. Wechseln Sie zu **Systemverwaltung** > **Sicherheit** > **Aufgabentrennung** > **Aufgabentrennungsregeln**.
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

> [!IMPORTANT] 
> Die Einhaltung der Regeln für die Aufgabentrennung wird beim Erstellen einer Regel nicht überprüft. Sie können eine Regel erstellen, die einen Konflikt für vorhandene Rollen erstellt. Bestehende Benutzerrollenzuweisungen können ebenfalls im Widerspruch zur neuen Regel stehen. Sie müssen die Einhaltung überprüfen, nachdem Sie eine Regel erstellt oder geändert haben. Weitere Informationen finden Sie unter [Konflikte bei der Aufgabentrennung erkennen und beheben](identify-resolve-conflicts-segregation-duties.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]