---
title: Identifizieren und Beheben von Konflikten bei der Aufgabentrennung
description: In diesem Thema wird erläutert, wie Sie Konflikte bei der Aufgabentrennung ermitteln und lösen.
author: maertenm
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c89d27eb8b587e8936258aae3ec1fee4574ccfb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180920"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Identifizieren und Beheben von Konflikten bei der Aufgabentrennung

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Thema wird erläutert, wie Sie Konflikte bei der Aufgabentrennung ermitteln und lösen. Sie können Regeln einrichten, Aufgaben abzugrenzen, die von unterschiedlichen Benutzern ausgeführt werden müssen. Dieses Konzept wird Aufgabentrennung benannt. Wenn die Definierung einer Sicherheitsrolle oder die Rollenzuweisungen eines Benutzers die Regeln verletzt, wird der Konflikt protokolliert. Alle Konflikte müssen vom Administrator aufgelöst werden. Führen Sie die folgende Prozedur aus, um Konflikte zu erkennen und beheben. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Überprüfen, ob Benutzerrollenzuweisungen mit den neuen Aufgabentrennungsregel übereinstimmen
1. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Aufgabentrennung > Konformität mit Benutzerrollenzuweisungen überprüfen**.
2. Wählen Sie **OK**. In einer Benachrichtigung werden die Ergebnisse der Überprüfung angezeigt. Falls ein Konflikt vorliegt, können Sie die **Benutzerseite** öffnen und die Rollenzuweisungen des Benutzers ändern. Konflikte werden auch auf der Konflikt-Seite **Aufgabentrennung** angezeigt. Um den Prüfprozess als Stapelverarbeitungsauftrag auszuführen, wählen Sie **Stapelverarbeitung** aus, und legen Sie dann die anderen Stapelverarbeitungsparameter fest. Nachdem der Stapelverarbeitungsauftrag ausgeführt wurde, können Sie die Konflikte auf der Seite **Konflikte bei der Aufgabentrennung** prüfen.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Zuweisung Ansichts- und des Beschlusses Konflikt verursachende Benutzerrolle
1. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Aufgabentrennung > Konflikte bei der Aufgabentrennung**. Wählen Sie einen Konflikt aus, und klicken Sie anschließend auf eine der folgenden Schaltflächen: **Zuweisung verweigern – verweigern Sie die Zuweisung des Benutzers zur zusätzlichen Sicherheitsrolle**. Wenn Sie eine automatische Rollenzuweisung verweigern, wird der Benutzer als von der Rolle ausgeschlossen markiert. Dem ausgeschlossenen Benutzer wird kein der Rolle zugeordneter Zugriff gewährt, und er kann der Rolle erst zugewiesen werden, wenn der Administrator den Ausschluss aufhebt (bzw. entfernt). Zuweisung erlauben – **Überschreiben** Sie den Konflikt, und lassen Sie zu, dass der Benutzer beiden Sicherheitsrollen zugewiesen wird. Wenn Sie einen Konflikt außer Kraft setzen, müssen Sie im Feld **Grund für die Außerkraftsetzung** einen Grund angeben.  
2. Schließen Sie die Seite.
3. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Aufgabentrennung > Aufgabentrennung - nicht behobene Konflikte**. Wählen Sie einen Konflikt aus, und klicken Sie anschließend auf eine der folgenden Schaltflächen: **Zuweisung verweigern – verweigern Sie die Zuweisung des Benutzers zur zusätzlichen Sicherheitsrolle**. Wenn Sie eine automatische Rollenzuweisung verweigern, wird der Benutzer als von der Rolle ausgeschlossen markiert. Dem ausgeschlossenen Benutzer wird kein der Rolle zugeordneter Zugriff gewährt, und er kann der Rolle erst zugewiesen werden, wenn der Administrator den Ausschluss aufhebt (bzw. entfernt). Zuweisung erlauben – **Überschreiben** Sie den Konflikt, und lassen Sie zu, dass der Benutzer beiden Sicherheitsrollen zugewiesen wird. Wenn Sie einen Konflikt außer Kraft setzen, müssen Sie im Feld **Grund für die Außerkraftsetzung** einen Grund angeben.    
4. Schließen Sie die Seite.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Überprüfen, ob existierende Rollen mit neuen Aufgabentrennungsregeln übereinstimmen
1. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Aufgabentrennung > Aufgabentrennungsregeln**. Wählen Sie eine Rolle aus.  
2. Wählen Sie **Aufgaben und Rollen überprüfen** aus. Werden irgendwelche verstoßen vorhandene Rollen die ausgewählte Regel, wird eine Meldung angezeigt, die den Namen der Rolle und die Namen der Konflikte verursachenden Aufgaben enthält. Der Administrator muss entweder den Ausgleich für das Sicherheitsrisiko angeben oder Rolle ändern, sodass sie nicht die Regeln für Aufgabentrennung verstößt. Wenn keine Rollen die ausgewählte Regel verstoßen, wird eine Meldung mit, dass alle Rollen in der Kompatibilität sind.  

