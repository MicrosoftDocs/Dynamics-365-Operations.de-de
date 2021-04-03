---
title: Eine Instanz entfernen
description: Diese Artikel führt Sie durch den Prozess des Entfernens eine Testversions- oder Produktionsumgebung für Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1e6d1eff32b6f925541760f0c0408238f3c4d947
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466855"
---
# <a name="remove-an-instance"></a>Eine Instanz entfernen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Diese Artikel führt Sie durch den Prozess des Entfernens eine Testversions- oder Produktionsumgebung für Microsoft Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>Testversionsumgebung entfernen

Human Resources-Testversionen werden mit einer 60-Tage-Ablaufrichtlinie bereitgestellt. Aber Eigentümer von Testumgebungen haben die Option, ihren Versuch früh zu beenden, indem Sie die folgenden Schritte ausführen. 

1. Zum [Power Apps Admin Center](https://admin.businessplatform.microsoft.com/) navigieren.
2. Wählen Sie **Umgebungen** aus.
3. Wählen Sie die Testversionsumgebung aus, die ein Benennungsmuster hat, das mit diesem vergleichbar ist: TestDrive - alias@domain
4. Wählen Sie **Löschen** aus, und bestätigen Sie die Entscheidung. 

Die vorhandene Testversionsumgebung wird entfernt. Wenn sie entfernt wird, können Sie sich für eine neue Testversionsumgebung anmelden. 

## <a name="remove-a-production-environment"></a>Produktionsumgebung entfernen

Für diesen Artikel wird vorausgesetzt, dass Sie Human Resources über einen Cloud-Lösungsanbieter (CSP) oder eine Unternehmensarchitekturvereinbarung erworben haben. 

Da eine einzelne Human Resources-Umgebung innerhalb einer einzelnen Power Apps-Umgebung „enthalten“ ist, sind zwei Optionen zu bedenken. Die erste Option entfernt die gesamte Power Apps-Umgebung, die zweite Option entfernt nur Human Resources. Die erste Option wird bevorzugt, wenn Sie eine Power Apps-Umgebung speziell für den Zweck der Bereitstellung von Human Resources erstellt haben und wenn Sie gerade erst mit der Implementierung begonnen haben oder wenn Sie keine eingerichteten Integrationen haben. Die zweite Option ist sinnvoll, wenn Sie eine etablierte Power Apps-Umgebung mit umfangreichen Daten haben, die in Power Apps und Power Automate genutzt wird.

> [!Important]
> Bevor Sie die Power Apps-Umgebung entfernen, stellen Sie sicher, dass sie nicht für Ihr Datenintegrationen außerhalb der Bereich von Human Resources verwendet wird. Standardmäßig kann die Power Apps-Umgebung nicht entfernt werden. 

So entfernen Sie die gesamte Power Apps-Umgebung, einschließlich Human Resources und zugehörige Anwendungen und Flows:

1. Zum [Power Apps Admin Center](https://admin.businessplatform.microsoft.com/) navigieren.
2. Wählen Sie **Umgebungen** aus.
3. Wählen Sie die zu entfernende Umgebung aus.
4. Wählen Sie **Löschen** aus, und bestätigen Sie die Entscheidung. 
5. Warten Sie, bis der Löschvorgang abgeschlossen ist.
6. Melden Sie sich an bei [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS), indem Sie das Konto verwenden, das Sie verwendet haben, um Human Resources zu abonnieren. 
7. Wählen Sie das Human Resources-Projekt aus, das die Umgebung enthält. 
8. In Ihrem LCS-Projekt wählen Sie die Kachel **Human Resources App-Verwaltung** aus. 
9. Wählen Sie die zu entfernende Instanz aus. 
10. Wählen Sie **Instanz entfernen** aus, und bestätigen Sie Ihre Entscheidung.  

Um eine Human Resources-Umgebung aus einer vorhandenen Power Apps-Umgebung zu entfernen, führen Sie die folgenden Schritte aus. Beachten Sie, dass die Anforderung, Support einzubeziehen und das Human Resources DevOps-Team zu kontaktieren temporär ist, nachdem diese Funktion direkt in LCS aktiviert ist.

1. Kontaktaufnahme von Support, um eine Entfernung einer Anforderung zu initiieren.
2. Das Supportteam initiiert eine Entfernungsanforderung mit dem Human Resources DevOps-Team. 
3. Fahren Sie fort, nachdem Sie wissen, dass die Umgebung entfernt wurde.
4. Melden Sie sich an bei LCS indem Sie das Konto verwenden, das Sie verwenden, um Human Resources zu abonnieren. 
5. Wählen Sie das Human Resources-Projekt aus, das die Umgebung enthält. 
6. In Ihrem LCS-Projekt wählen Sie die Kachel **Human Resources App-Verwaltung** aus. 
7. Wählen Sie die Instanz aus, die Sie entfernen möchten, die mit dem Bereitstellungsstatus **Gelöscht** markiert werden muss.
8. Wählen Sie **Instanz entfernen** aus, und bestätigen Sie Ihre Entscheidung. 

## <a name="recover-a-soft-deleted-environment"></a>Eine nicht vollständig gelöschte Umgebung wiederherstellen

Wenn Sie die Power Apps Umgebung, mit der Ihre Human-Ressources-Umgebung verbunden ist, löschen, lautet der Status der Human-Ressources-Umgebung in Lifecycle Services **weich gelöscht**. In diesem Fall können Benutzer keine Verbindung zu Human Ressources herstellen.

So stellen Sie die Umgebung wieder her:

1. Folgen Sie den Anweisungen unter [Die Power Apps Umgebung wiederherstellen](/power-platform/admin/recover-environment.md).

2. Wenden Sie sich an den Support, um die Human-Resources-Umgebung wiederherzustellen. Weitere Informationen erhalten Sie über den [Support](hr-admin-troubleshooting-support.md).

> [!Warning]
> Power Apps Umgebungen werden nach dem Löschen nur sieben Tage lang gespeichert. Sie müssen die Umgebung innerhalb dieser sieben Tage wiederherstellen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]