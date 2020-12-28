---
title: Fehlerbehebung bei Beschaffungsworkflows
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Beschaffungsworkflows auftreten können.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cdedc45b8f057310801f134104156a732fb58d86
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429129"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a>Fehlerbehebung bei Beschaffungsworkflows

In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Beschaffungsworkflows auftreten können.

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a>Fehler beim erneuten Übermitteln einer Bestellung an den Workflow nach einer Änderung: „Änderungen an Bestellung X sind nur in einem Entwurfsstatus zulässig, wenn das Änderungsmanagement aktiviert ist.“

Dieses Problem tritt nur auf, wenn sich die Bestellung in einem *Bestätigt*-Zustand befand, bevor Sie Änderungen angefordert haben. Wenn Sie Änderungen anfordern, während sich die Bestellung in einem *Genehmigt*-Zustand befindet, kann der Workflow erfolgreich verarbeitet werden.

### <a name="error-description"></a>Fehlerbeschreibung

Der folgende Fehler tritt im Workflow auf, wenn eine Bestellung nach einer Änderung erneut übermittelt wird:

> Gestoppt (Fehler): X++ Ausnahme: Änderungen an der Bestellung PO0000569 sind nur im Status Entwurf zulässig, wenn die Änderungsverwaltung aktiviert ist unter<br>
SysWorkflowParticipantProvider-Auflösung<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

### <a name="issue-resolution"></a>Problemlösung

Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.

So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf*-Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**. Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Das Problem wird behoben durch [diesen Artikel in der Microsodft Wissensdatenbank (KB)](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Eine oder mehrere Buchhaltungsverteilungen sind entweder über- oder unterverteilt.

Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.

So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf*-Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**. Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a>Wenn eine verbleibende Liefermenge für eine Bestellung storniert wird, für die das Änderungsmanagement aktiviert ist, wechselt die Bestellung in den Status Bestätigt.

### <a name="issue-description"></a>Problembeschreibung

Bei einer Bestellung, die dem Änderungsmanagement unterliegt, wird die Bestellung, wenn die einzige angeforderte Änderung die Stornierung einer verbleibenden Liefermenge bei einer oder mehreren Positionen ist, direkt an den Zustand *Bestätigt* weitergeleitet, wann sie genehmigt wurde, und es wird kein Journal erstellt.

### <a name="issue-resolution"></a>Problemlösung

Die Stornierung einer verbleibenden Liefermenge hat keine Auswirkungen auf den Inhalt des Bestätigungsjournals. Diese Funktionalität sollte verwendet werden, wenn die Position teilweise zugegangen ist, und die verbleibende Liefermenge sollte im Prozessschritt storniert werden, nachdem die Bestellung beim Lieferanten bestätigt wurde.

Sollte dies in der Bestellbestätigung berücksichtigt werden, sollte die Menge in der Bestellposition angepasst werden, sodass die Bestätigung erforderlich ist. Wenn alternativ nichts in der Position empfangen wurde, kann die Menge entfernt werden. In diesem Fall ist eine erneute Bestätigung erforderlich.

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a>Stornierte Bestellungen werden in der Entwurfsliste im Arbeitsbereich für die Bestellvorbereitung angezeigt.

### <a name="issue-description"></a>Problembeschreibung

Nachdem Sie Bestellungen storniert haben, die im *Bestätigt*-Zustand waren, erscheinen die stornierten Bestellungen im **Bestellvorbereitung**-Arbeitsbereich weiterhin in der Liste der Bestellentwürfe.

### <a name="issue-resolution"></a>Problemlösung

Dieses Problem tritt nur bei Bestellungen auf, die dem Änderungsmanagement unterliegen. Dies liegt daran, dass die Stornierung als eine Änderung angesehen wird, die genehmigt werden muss. Die Genehmigung kann automatisch vom System erfolgen. Daher besteht der Prozess darin, die stornierte Bestellung an den Genehmigungsworkflow zu senden, damit sie in einen *Genehmigt*-Zustand wechseln kann. Ab diesem Zeitpunkt erscheint die Bestellung nicht mehr im **Bestellvorbereitung**-Arbeitsbereich in der Liste der Bestellentwürfe.

