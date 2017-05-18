---
title: Fracht in der Transportverwaltung abstimmen
description: Dieser Artikel beschreibt den Frachtabstimmungsprozess.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 59c5dd4574aed1bc97fc945c999016be1c399f71
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="reconcile-freight-in-transportation-management"></a>Fracht in der Transportverwaltung abstimmen

[!include[banner](../includes/banner.md)]


Dieser Artikel beschreibt den Frachtabstimmungsprozess.

Die Frachtabstimmung kann manuell oder automatischen durchgeführt werden. Um die automatische Frachtabstimmung zu verwenden, müssen Sie einen Überwachungsmaster einrichten. In ihm können Sie die Kriterien definieren, die festlegen, welche Fracht automatisch abgestimmt wird.

## <a name="the-freight-reconciliation-process"></a>Der Frachtabstimmungsprozess
Frachtkosten werden vom den Tarifmodul berechnet, das dem relevanten Spediteur zugeordnet ist. Wenn ein Ladung bestätigt ist, wird ein Frachtbrief erstellt und die Frachtkosten werden an diesen übertragen. Die Frachtkosten werden je nach Konfiguration für den regulären Abrechnungsprozess als sonstige Zuschläge auf das entsprechende Quelldokument umgelegt (Bestellung, Auftrag und/oder Umlagerungsauftrag). Der Frachtabstimmungsprozesse (auch Abgleichsprozess genannt) kann starten sobald die Frachtrechnung vom Spediteur eingeht. Die Rechnung elektronisch oder auf Papier erhalten werden. Wenn die Rechnung auf Papier erhalten wird, können Sie mit dem Frachtbrief als Vorlage eine elektronische Rechnung generieren. 

[![Frachtabstimmungsprozess](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Manuelle Abstimmung
Wenn Sie die Fracht manuell abstimmen, müssen Sie jede Rechnungsposition mit der Frachtbriefposition oder den-positionen für die zu fakturierende Ladung abgleichen. Diesen Abgleich führen Sie auf der Seite **Frachtbrief- und Rechnungsabgleich** durch. Wenn der Betrag der Rechnungsposition nicht mit dem Frachtbriefbetrag übereinstimmt, müssen Sie einen Abstimmungsgrund für die Abweichung auswählen. Sind mehrere Gründe für die Abstimmung zutreffen, können Sie die nicht abgeglichenen Mengen auf diese Gründe verteilen. Der Abstimmungsgrund bestimmt, wie die Differenzbeträge im Hauptbuch gebucht werden. Bei die Abstimmung des gesamten Rechnungsbetrags gebucht wird, wird dieser zur Genehmigung gesendet. Dann wird die Erfassung gebucht. Die folgende Abbildung zeigt, wie eine Frachtrechnung generiert und eine Frachtabstimmung in Microsoft Dynamics 365 for Operations ausgeführt wird. 
[![Frachtabstimmungsaufgaben in Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>Automatische Abstimmung
Um die automatische Abstimmung zu verwenden, müssen Sie den Zeitplan für die Abstimmung und die zu verwendenden Rechnungen und Spediteure angeben. Der Abgleich der Rechnungspositionen und Frachtbriefe wird entsprechend der Einrichtung des Überwachungsmasters und der Frachtbriefart ausgeführt. Nach dem Ausführen der automatischen Abstimmung müssen Sie alle Rechnungen bearbeiten, die das System nicht zuordnen kann. Sie müssen diese Rechnungen dann manuell verarbeiten, bevor Sie alle Rechnung für die Zahlung buchen können.




