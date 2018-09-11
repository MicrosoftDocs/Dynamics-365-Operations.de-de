--- 
title: Identifizieren und beheben Sie Konflikte bei der Aufgabentrennung
description: "Sie können Regeln einrichten, Aufgaben abzugrenzen, die von unterschiedlichen Benutzern ausgeführt werden müssen."
author: maertenm
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c3a366ea4b558ba4e4af7336992dbb091b0b1414
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Identifizieren und beheben Sie Konflikte bei der Aufgabentrennung

[!include [task guide banner](../../includes/task-guide-banner.md)]

Sie können Regeln einrichten, Aufgaben abzugrenzen, die von unterschiedlichen Benutzern ausgeführt werden müssen. Dieses Konzept wird Aufgabentrennung benannt. Wenn die Definierung einer Sicherheitsrolle oder die Rollenzuweisungen eines Benutzers die Regeln verletzt, wird der Konflikt protokolliert. Alle Konflikte müssen vom Administrator aufgelöst werden. Führen Sie die folgende Prozedur aus, um Konflikte zu erkennen und beheben. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Überprüfen, ob Benutzerrollenzuweisungen mit den neuen Aufgabentrennungsregel übereinstimmen
1. Wechseln Sie zu Systemverwaltung > Sicherheit > Aufgabentrennung > Übereinstimmung mit Benutzerrollenzuweisungen überprüfen.
2. Klicken Sie auf "OK".
    * In einer Benachrichtigung werden die Ergebnisse der Überprüfung angezeigt.     Falls ein Konflikt vorliegt, können Sie die Benutzerseite öffnen und die Rollenzuweisungen des Benutzers ändern. Konflikte werden auch auf der Konflikt-Seite "Aufgabentrennung" angezeigt.     Wenn Sie den Prüfprozess als Stapelverarbeitungsauftrag, ausgewählte Stapelverarbeitung ausführen und die andere dann Stapelverarbeitungsparameter festgelegt. Nachdem der Stapelverarbeitungsauftrag ausgeführt wird, können Sie die Konflikte in der Aufgabentrennungskonfliktseite prüfen.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Zuweisung Ansichts- und des Beschlusses Konflikt verursachende Benutzerrolle
1. Wechseln Sie zu Systemverwaltung > Sicherheit > Aufgabentrennung > Konflikte bei der Aufgabentrennung.
    * Wählen Sie einen Konflikt aus, und klicken Sie anschließend auf eine der folgenden Schaltflächen:   Verweigern Sie Zuweisung - verweigern Sie die Zuweisung des Benutzers zur zusätzlichen Sicherheitsrolle. Wenn Sie eine automatische Rollenzuweisung verweigern, wird der Benutzer als von der Rolle ausgeschlossen markiert. Dem ausgeschlossenen Benutzer wird kein der Rolle zugeordneter Zugriff gewährt, und er kann der Rolle erst zugewiesen werden, wenn der Administrator den Ausschluss aufhebt (bzw. entfernt).     Zulassen von Zuweisung - überschreiben Sie Konflikt und ermöglichen Sie den sowohl Sicherheitsrollen Benutzer die Zuweisung. Wenn Sie einen Konflikt außer Kraft setzen, müssen Sie im Feld Grund für die Außerkraftsetzung einen Grund angeben.  
2. Schließen Sie die Seite.
3. Wechseln Sie zu Systemverwaltung > Sicherheit  Aufgabentrennung > Aufgabentrennung - nicht behobene Konflikte.
    * Wählen Sie einen Konflikt aus, und klicken Sie anschließend auf eine der folgenden Schaltflächen:   Verweigern Sie Zuweisung - verweigern Sie die Zuweisung des Benutzers zur zusätzlichen Sicherheitsrolle. Wenn Sie eine automatische Rollenzuweisung verweigern, wird der Benutzer als von der Rolle ausgeschlossen markiert. Dem ausgeschlossenen Benutzer wird kein der Rolle zugeordneter Zugriff gewährt, und er kann der Rolle erst zugewiesen werden, wenn der Administrator den Ausschluss aufhebt (bzw. entfernt).     Zulassen von Zuweisung - überschreiben Sie Konflikt und ermöglichen Sie den sowohl Sicherheitsrollen Benutzer die Zuweisung. Wenn Sie einen Konflikt außer Kraft setzen, müssen Sie im Feld Grund für die Außerkraftsetzung einen Grund angeben.    
4. Schließen Sie die Seite.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Überprüfen, ob existierende Rollen mit neuen Aufgabentrennungsregeln übereinstimmen
1. Wechseln Sie zu Systemverwaltung > Sicherheit > Aufgabentrennung > Aufgabentrennungsregeln.
    * Wählen Sie eine Rolle aus.  
2. Klicken Sie auf Aufgaben und Rollen überprüfen.
    * Werden irgendwelche verstoßen vorhandene Rollen die ausgewählte Regel, wird eine Meldung angezeigt, die den Namen der Rolle und die Namen der Konflikte verursachenden Aufgaben enthält. Der Administrator muss entweder den Ausgleich für das Sicherheitsrisiko angeben oder Rolle ändern, sodass sie nicht die Regeln für Aufgabentrennung verstößt.     Wenn keine Rollen die ausgewählte Regel verstoßen, wird eine Meldung mit, dass alle Rollen in der Kompatibilität sind.  


