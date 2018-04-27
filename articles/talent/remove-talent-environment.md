---
title: Eine Talent-Umgebung entfernen
description: "Dieses Thema führt Sie durch den Prozess des Entfernens einer Testversion oder einer Produktionsumgebung für Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d1870c84d4d5e7402bae44d192ce7587c2f67fe7
ms.openlocfilehash: 0e7748b079b1cd5c069917d46e05cd281ea6aa01
ms.contentlocale: de-de
ms.lasthandoff: 04/05/2018

---
# <a name="remove-a-talent-environment"></a>Eine Talent-Umgebung entfernen

Dieses Thema führt Sie durch den Prozess des Entfernens einer Testversion oder einer Produktionsumgebung für Microsoft Dynamics 365 for Talent.

## <a name="removing-a-test-drive-environment"></a>Entfernen einer Testversionsumgebung

Talent-Testversionen werden mit einer 60-Tage-Ablaufrichtlinie bereitgestellt. Aber Eigentümer von Testumgebungen haben die Option, ihren Versuch früh zu beenden, indem Sie die folgenden Schritte ausführen. 

1. [PowerApps-Administratorcenter](https://admin.businessplatform.microsoft.com/) öffnen.
2. Wählen Sie **Umgebungen** aus.
3. Wählen Sie die Testversionsumgebung aus, die ein Benennungsmuster hat, das mit diesem vergleichbar ist: TestDrive - alias@domain
4. Wählen Sie **Löschen** aus, und bestätigen Sie die Entscheidung. 

Die vorhandene Testversionsumgebung wird entfernt. Wenn sie entfernt wird, können Sie sich für eine neue Testversionsumgebung anmelden. 

## <a name="removing-a-production-environment"></a>Entfernen einer Produktionsumgebung

Für dieses Thema wird vorausgesetzt, dass Sie Talent über einen Cloud-Lösungsanbieter (CSP) oder eine Unternehmensarchitekturvereinbarung erworben haben. 

Da eine einzelne Talent-Umgebung innerhalb einer einzelnen PowerApps-Umgebung „enthalten” ist, sind zwei Optionen zu bedenken. Die erste Option bezieht entfernt die gesamte PowerApps-Umgebung, die zweite Option entfernt nur Talent. Die erste Option wird bevorzugt, wenn Sie eine PowerApps-Umgebung speziell für den Zweck der Bereitstellung von Talent erstellt haben und wenn Sie gerade erst mit der Implementierung begonnen haben oder wenn Sie keine eingerichteten Integrationen haben. Die zweite Option ist passend, wenn Sie eine eingerichtete PowerApps-Umgebung haben, die mit aussagekräftigen Daten haben, die in PowerApps und Flows eingesetzt werden.

> [!Important]
> Bevor Sie die PowerApps-Umgebung entfernen, stellen Sie sicher, dass sie nicht für Ihr Datenintegrationen außerhalb der Bereich des Talents verwendet wird. Standardmäßig kann die PowerApps-Umgebung nicht entfernt werden. 

So entfernen Sie die gesamte PowerApps-Umgebung, einschließlich Talent und den zugeordneten Apps und Flows:

1. [PowerApps-Administratorcenter](https://admin.businessplatform.microsoft.com/) öffnen.
2. Wählen Sie **Umgebungen** aus.
3. Wählen Sie die zu entfernende Umgebung aus.
4. Wählen Sie **Löschen** aus, und bestätigen Sie die Entscheidung. 
5. Warten Sie, bis der Löschvorgang abgeschlossen ist.
6. Melden Sie sich an bei [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS), indem Sie das Konto verwenden, das Sie verwendet haben, um Talent zu abonnieren. 
7. Wählen Sie das Talent-Projekt aus, das die Umgebung enthält. 
8. In Ihrem LCS-Projekt wählen Sie die Kachel **Talent App-Verwaltung** aus. 
9. Wählen Sie die zu entfernende Instanz aus. 
10. Wählen Sie **Instanz entfernen** aus, und bestätigen Sie Ihre Entscheidung.  

Um eine Talent-Umgebung aus einer vorhandenen PowerApps-Umgebung zu entfernen, führen Sie die folgenden Schritte aus. Beachten Sie, dass die Anforderung, Support einzubeziehen und das Talent DevOps-Team zu kontaktieren temporär ist, nachdem diese Funktion direkt in Kreditbriefen aktiviert ist.

1. Kontaktaufnahme von Support, um eine Entfernung einer Anforderung zu initiieren.
2. Das Supportteam initiiert eine Entfernungsanforderung mit dem Talent DevOps-Team. 
3. Fahren Sie fort, nachdem Sie wissen, dass die Umgebung entfernt wurde.
4.  Melden Sie sich bei LCS an, indem Sie das Konto verwenden, das Sie verwendet haben, um Talent zu abonnieren. 
5. Wählen Sie das Talent-Projekt aus, das die Umgebung enthält. 
6. In Ihrem LCS-Projekt wählen Sie die Kachel **Talent App-Verwaltung** aus. 
7. Wählen Sie die Instanz aus, die Sie entfernen möchten, die mit dem Bereitstellungsstatus **Fehler** markiert werden muss.
8. Wählen Sie **Instanz entfernen** aus, und bestätigen Sie Ihre Entscheidung. 


