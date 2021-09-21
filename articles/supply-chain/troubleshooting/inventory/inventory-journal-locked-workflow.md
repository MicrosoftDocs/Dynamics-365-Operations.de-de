---
title: Ihre Bestandserfassung ist gesperrt und der Workflow-Batchauftrag funktioniert nicht.
description: Eine Ihrer Bestandserassungen ist durch einen Vorgang gesperrt und wird nicht freigegeben
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476417"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>Ihre Bestandserfassung ist gesperrt und der Workflow-Batchauftrag funktioniert nicht.

## <a name="symptoms"></a>Symptome

Eine Ihrer Bestandserassungen ist durch einen Vorgang gesperrt und wird nicht freigegeben. Wenn beispielsweise während der Buchung (einem Vorgang, bei dem das System gesperrt wird) ein unbekannter Fehler auftritt, bleibt die Erfassung möglicherweise im Status „System gesperrt“. In diesem Fall gibt der Handler für das Workflowarbeitselement einen Fehler aus, während er die Prüfung sperrt.

## <a name="resolution"></a>Lösung

Melden Sie sich bei der SQL Server-Instanz für Supply Chain Management an und prüfen Sie, ob **InventJournalTable.SystemBlocked** auf *1* festgelegt ist. Wenn dies der Fall ist, stellen Sie sicher, dass die Erfassung nicht gesperrt ist, und setzen Sie **InventJournalTable.SystemBlocked** dann auf *0* zurück.
