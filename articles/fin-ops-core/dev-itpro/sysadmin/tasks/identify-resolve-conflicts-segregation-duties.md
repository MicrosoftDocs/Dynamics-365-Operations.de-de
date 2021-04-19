---
title: Identifizieren und Beheben von Konflikten bei der Aufgabentrennung
description: In diesem Thema wird erläutert, wie Sie Konflikte bei der Aufgabentrennung ermitteln und lösen.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ebd59c7018a50e01253697d792698664a981566
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745812"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Identifizieren und Beheben von Konflikten bei der Aufgabentrennung

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Konflikte bei der Aufgabentrennung ermitteln und lösen. Sie können Regeln einrichten, um Aufgaben abzugrenzen, die von unterschiedlichen Benutzern ausgeführt werden müssen. Dieses Konzept wird Aufgabentrennung benannt. Wenn die Definierung einer Sicherheitsrolle oder die Rollenzuweisungen eines Benutzers die Regeln verletzt, wird der Konflikt protokolliert. Alle Konflikte müssen vom Administrator aufgelöst werden. Führen Sie die folgende Prozedur aus, um Konflikte zu erkennen und beheben.

Überprüfen Sie nach dem Hinzufügen einer Regel, ob alle vorhandenen Rollen kompatibel sind. 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a>Überprüfen, ob existierende Rollen und Aufgaben mit neuen Aufgabentrennungsregeln übereinstimmen
1. Wechseln Sie zu **Systemverwaltung** > **Sicherheit** > **Aufgabentrennung** > **Aufgabentrennungsregeln**.
3. Wählen Sie **Aufgaben und Rollen überprüfen** aus. Werden irgendwelche vorhandene Rollen gegen die Regeln verstoßen, wird eine Meldung angezeigt, die den Namen der Regel, die Rolle und die Namen der Konflikte verursachenden Aufgaben enthält. Widersprüchliche Rollen müssen mit der **Sicherheitskonfiguration** geändert werden und dürfen keine widersprüchliche Aufgaben enthalten. Wenn keine Rollen gegen die ausgewählte Regel verstoßen, wird eine Meldung angezeigt, dass alle Rollen in der Kompatibilität sind.   

> [!NOTE]
> Die Validierung wird nur für die ausgewählte Regel durchgeführt. Es ist wichtig, die Konformität für jede Regel zu überprüfen.   

Wenn Sie eine Rolle erstellen oder ändern, werden die Regeln für die Aufgabentrennung automatisch durchgesetzt. Sie können einer Rolle keine widersprüchlichen Aufgaben zuweisen.

Stellen Sie als Nächstes sicher, dass alle vorhandenen Rollenzuweisungen kompatibel sind.

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Überprüfen, ob Benutzerrollenzuweisungen mit den neuen Aufgabentrennungsregeln übereinstimmen
1. Wechseln Sie zu **Systemverwaltung > Sicherheit > Aufgabentrennung > Übereinstimmung mit Benutzerrollenzuweisungen überprüfen**.
2. Wählen Sie **OK**. In einer Benachrichtigung werden die Ergebnisse der Überprüfung angezeigt. Konflikte werden auf der Seite **Aufgabentrennung - nicht behobene Konflikte** angezeigt.   

Wenn Sie Benutzern Rollen zuweisen, werden die Regeln für die Aufgabentrennung automatisch durchgesetzt. Wenn Sie versuchen, einen Benutzer Rollen zuzuweisen, die widersprüchliche Aufgaben enthalten, wird eine Fehlermeldung angezeigt. Sie müssen den Konflikt dann lösen, indem Sie die zusätzliche Rollenzuweisung verweigern oder zulassen. Die zusätzliche Rolle wird zugewiesen, nachdem die Zuweisung zugelassen wird. 

> [!NOTE]
> Konflikte werden derzeit nicht für Benutzer überprüft, denen Rollen basierend auf den Active Directory-Domänengruppen zugewiesen wurden.

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Zuweisung Ansichts- und des Beschlusses Konflikt verursachende Benutzerrolle
1. Wechseln Sie zu **Systemverwaltung** > **Sicherheit** > **Aufgabentrennung** > **Aufgabentrennung - nicht behobene Konflikte**. 
2. Wählen Sie einen Konflikt aus, und wählen Sie dann eine der folgenden Aktionen aus: 

  - **Zuweisung verweigern**: Dadurch wird die Zuordnung des Benutzers zur zusätzlichen Sicherheitsrolle verweigert. Wenn Sie eine automatische Rollenzuweisung verweigern, wird der Benutzer als von der Rolle ausgeschlossen markiert. Dem ausgeschlossenen Benutzer wird kein der Rolle zugeordneter Zugriff gewährt, und er kann der Rolle erst zugewiesen werden, wenn der Administrator den Ausschluss aufhebt (bzw. entfernt). 
-  **Zuweisung erlauben**: Dies überschreibt den Konflikt und ermöglicht, dass dem Benutzer die zusätzliche Sicherheitsrolle zugewiesen wird. Wenn Sie einen Konflikt außer Kraft setzen, müssen Sie im Feld **Grund für die Außerkraftsetzung** einen Grund angeben. Alle überschriebenen Rollenzuweisungen können auf der Seite **Konflikte bei der Aufgabentrennung** angezeigt werden.  

> [!NOTE]
> Wenn mehrere Konflikte für denselben Benutzer aufgelistet sind, wählen Sie den Benutzerdatensatz aus, und bewerten Sie die zugewiesenen Rollen auf der Seite **Benutzer**. Um diesen Konflikt zu vermeiden, überprüfen Sie jede Regel, nachdem sie hinzugefügt oder geändert wurde.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]