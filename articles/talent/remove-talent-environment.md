---
title: Talent-Umgebungen entfernen
description: Dieses Thema führt Sie durch den Prozess des Entfernens eine Testversions- oder Produktionsumgebung für Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: bbc65a77b7c3df6545dfd7aa2109aba5c4e1b57b
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773033"
---
# <a name="remove-talent-environments"></a>Talent-Umgebungen entfernen

[!include [banner](includes/banner.md)]

Dieses Thema führt Sie durch den Prozess des Entfernens eine Testversions- oder Produktionsumgebung für Microsoft Dynamics 365 Talent.

## <a name="removing-a-test-drive-environment"></a>Entfernen einer Testversionsumgebung

Talent-Testversionen werden mit einer 60-Tage-Ablaufrichtlinie bereitgestellt. Aber Eigentümer von Testumgebungen haben die Option, ihren Versuch früh zu beenden, indem Sie die folgenden Schritte ausführen. 

1. Zum [Power Apps Admin Center](https://admin.businessplatform.microsoft.com/) navigieren.
2. Wählen Sie **Umgebungen** aus.
3. Wählen Sie die Testversionsumgebung aus, die ein Benennungsmuster hat, das mit diesem vergleichbar ist: TestDrive - alias@domain
4. Wählen Sie **Löschen** aus, und bestätigen Sie die Entscheidung. 

Die vorhandene Testversionsumgebung wird entfernt. Wenn sie entfernt wird, können Sie sich für eine neue Testversionsumgebung anmelden. 

## <a name="removing-a-production-environment"></a>Entfernen einer Produktionsumgebung

Für dieses Thema wird vorausgesetzt, dass Sie Talent über einen Cloud-Lösungsanbieter (CSP) oder eine Unternehmensarchitekturvereinbarung erworben haben. 

Da eine einzelne Talent-Umgebung innerhalb einer einzelnen Power Apps-Umgebung „enthalten“ ist, sind zwei Optionen zu bedenken. Die erste Option bezieht entfernt die gesamte Power Apps-Umgebung, die zweite Option entfernt nur Talent. Die erste Option wird bevorzugt, wenn Sie eine Power Apps-Umgebung speziell für den Zweck der Bereitstellung von Talent erstellt haben und wenn Sie gerade erst mit der Implementierung begonnen haben oder wenn Sie keine eingerichteten Integrationen haben. Die zweite Option ist sinnvoll, wenn Sie eine etablierte Power Apps-Umgebung mit umfangreichen Daten haben, die in Power Apps und Power Automate genutzt wird.

> [!Important]
> Bevor Sie die Power Apps-Umgebung entfernen, stellen Sie sicher, dass sie nicht für Ihr Datenintegrationen außerhalb der Bereich des Talents verwendet wird. Standardmäßig kann die Power Apps-Umgebung nicht entfernt werden. 

Entfernen der gesamten Power Apps-Umgebung, einschließlich Talent und der zugehörigen Anwendungen und Flows:

1. Zum [Power Apps Admin Center](https://admin.businessplatform.microsoft.com/) navigieren.
2. Wählen Sie **Umgebungen** aus.
3. Wählen Sie die zu entfernende Umgebung aus.
4. Wählen Sie **Löschen** aus, und bestätigen Sie die Entscheidung. 
5. Warten Sie, bis der Löschvorgang abgeschlossen ist.
6. Melden Sie sich an bei [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS), indem Sie das Konto verwenden, das Sie verwendet haben, um Talent zu abonnieren. 
7. Wählen Sie das Talent-Projekt aus, das die Umgebung enthält. 
8. In Ihrem LCS-Projekt wählen Sie die Kachel **Talent App-Verwaltung** aus. 
9. Wählen Sie die zu entfernende Instanz aus. 
10. Wählen Sie **Instanz entfernen** aus, und bestätigen Sie Ihre Entscheidung.  

Um eine Talent-Umgebung aus einer vorhandenen Power Apps-Umgebung zu entfernen, führen Sie die folgenden Schritte aus. Beachten Sie, dass die Anforderung, Support einzubeziehen und das Talent DevOps-Team zu kontaktieren temporär ist, nachdem diese Funktion direkt in Kreditbriefen aktiviert ist.

1. Kontaktaufnahme von Support, um eine Entfernung einer Anforderung zu initiieren.
2. Das Supportteam initiiert eine Entfernungsanforderung mit dem Talent DevOps-Team. 
3. Fahren Sie fort, nachdem Sie wissen, dass die Umgebung entfernt wurde.
4.  Melden Sie sich bei LCS an, indem Sie das Konto verwenden, das Sie verwendet haben, um Talent zu abonnieren. 
5. Wählen Sie das Talent-Projekt aus, das die Umgebung enthält. 
6. In Ihrem LCS-Projekt wählen Sie die Kachel **Talent App-Verwaltung** aus. 
7. Wählen Sie die Instanz aus, die Sie entfernen möchten, die mit dem Bereitstellungsstatus **Fehler** markiert werden muss.
8. Wählen Sie **Instanz entfernen** aus, und bestätigen Sie Ihre Entscheidung. 

