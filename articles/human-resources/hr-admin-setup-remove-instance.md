---
title: Eine Instanz entfernen
description: Dieser Artikel beschreibt den Prozess der Entfernung einer Test- oder Produktionsumgebung für Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ce676c93e133cc04ad9c49417ed2ca0d6791e93
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178471"
---
# <a name="remove-an-instance"></a>Eine Instanz entfernen

_**Gilt für:** Human Resources in der eigenständigen Infrastruktur_ 

> [!NOTE]
> Ab Juli 2022 können neue Human Resources Umgebungen nicht mehr in der eigenständigen Human Resources Infrastruktur bereitgestellt werden und neue Microsoft Dynamics Lifecycle Services (LCS) Projekte können dort nicht mehr erstellt werden. Debitor kann Human Resources Umgebungen in der Finanzen und Betrieb Infrastruktur bereitstellen. Weitere Informationen finden Sie unter [Personal Resources in der Finanzen und Betrieb Infrastruktur bereitstellen](/hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Die Finanz- und Betriebs-App-Infrastruktur unterstützt die Löschung einer Umgebung. Weitere Informationen darüber, wie Sie eine Umgebung löschen, finden Sie unter [Löschen einer Umgebung](../fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure.md#delete-an-environment).

In diesem Artikel wird erklärt, wie Sie eine Testversions- oder Produktionsumgebung für Microsoft Dynamics 365 Human Resources entfernen können.

## <a name="remove-a-test-drive-environment"></a>Testversionsumgebung entfernen

Human Resources-Testversionen werden mit einer 60-Tage-Ablaufrichtlinie bereitgestellt. Aber Eigentümer von Testumgebungen haben die Option, ihren Versuch früh zu beenden, indem Sie die folgenden Schritte ausführen. 

1. Zum [Power Apps Admin Center](https://admin.businessplatform.microsoft.com/) navigieren.
2. Wählen Sie **Umgebungen** aus.
3. Wählen Sie die Testversionsumgebung aus, die ein Benennungsmuster hat, das mit diesem vergleichbar ist: TestDrive - alias@domain
4. Wählen Sie **Löschen** aus, und bestätigen Sie die Entscheidung. 

Die vorhandene Testversionsumgebung wird entfernt. Wenn sie entfernt wird, können Sie sich für eine neue Testversionsumgebung anmelden. 

## <a name="remove-a-production-environment"></a>Produktionsumgebung entfernen

Für diesen Artikel wird vorausgesetzt, dass Sie Human Resources über einen Cloud-Lösungsanbieter (CSP) oder eine Unternehmensarchitekturvereinbarung erworben haben. 

Da eine einzelne Human Resources Umgebung in einer einzigen Power Apps-Umgebung enthalten ist, gibt es zwei Optionen, die Sie beim Entfernen einer Umgebung berücksichtigen müssen: 
- **Entfernen Sie die gesamte Power Apps Umgebung.** Diese Option wird bevorzugt, wenn die Power Apps-Umgebung zum Zweck der Bereitstellung von Human Resources erstellt wurde, die Implementierung gerade erst begonnen hat oder Sie über keine etablierten Integrationen verfügen.  
- **Nur Human Resources entfernen.** Diese Option ist geeignet, wenn es eine etablierte Power Apps-Umgebung gibt, die mit Daten gefüllt ist, die in Microsoft Power Apps und Power Automate verwendet werden.


> [!Important]
> Bevor Sie die Power Apps-Umgebung entfernen, stellen Sie sicher, dass sie nicht für Datenintegrationen außerhalb des Bereichs Human Resources verwendet wird. Standardmäßig kann die Power Apps-Umgebung nicht entfernt werden. 

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

Wenn Sie die Power Apps-Umgebung löschen, mit der Ihre Human Resources Umgebung verbunden ist, lautet der Status der Human Resources Umgebung in LCS **Soft gelöscht**. In diesem Fall können Benutzer keine Verbindung zu Human Ressources herstellen.

So stellen Sie die Umgebung wieder her:

1. Folgen Sie den Anweisungen unter [Die Power Apps Umgebung wiederherstellen](/power-platform/admin/recover-environment).

2. Wenden Sie sich an den Support, um die Human-Resources-Umgebung wiederherzustellen. Weitere Informationen erhalten Sie über den [Support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

> [!Warning]
> Power Apps Umgebungen werden nach dem Löschen nur sieben Tage lang gespeichert. Sie müssen die Umgebung innerhalb der Sieben-Tage-Frist wiederherstellen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
