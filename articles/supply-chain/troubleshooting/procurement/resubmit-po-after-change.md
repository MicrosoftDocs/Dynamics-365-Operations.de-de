---
title: Ein Fehler ist beim erneuten Senden einer Bestellung an einen Workflow nach einer Änderung aufgetreten
description: Ein Fehler ist beim erneuten Senden einer Bestellung an einen Workflow nach einer Änderung aufgetreten
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476491"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>Ein Fehler ist beim erneuten Senden einer Bestellung an einen Workflow nach einer Änderung aufgetreten


## <a name="symptoms"></a>Symptome

Der folgende Fehler tritt im Workflow auf, wenn eine Bestellung nach einer Änderung erneut übermittelt wird:

> Gestoppt (Fehler): X++ Ausnahme: Änderungen an der Bestellung PO0000569 sind nur im Status Entwurf zulässig, wenn die Änderungsverwaltung aktiviert ist unter<br>
SysWorkflowParticipantProvider-Auflösung<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

Dieses Problem tritt nur auf, wenn sich die Bestellung in einem *Bestätigt*-Zustand befand, bevor Sie Änderungen angefordert haben. Wenn Sie Änderungen anfordern, während sich die Bestellung in einem *Genehmigt*-Zustand befindet, kann der Workflow erfolgreich verarbeitet werden.

## <a name="resolution"></a>Lösung

Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.

So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf*-Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**. Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Das Problem wird behoben durch [diesen Artikel in der Microsodft Wissensdatenbank (KB)](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).
