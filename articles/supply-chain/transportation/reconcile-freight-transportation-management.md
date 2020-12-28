---
title: Fracht in der Transportverwaltung abstimmen
description: Dieser Artikel beschreibt den Frachtabstimmungsprozess.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable,TMSFBDetailReconcile,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13fecd5256c7bfc3a27d15482e0fa6200cfd72df
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2020
ms.locfileid: "4429171"
---
# <a name="reconcile-freight-in-transportation-management"></a>Fracht in der Transportverwaltung abstimmen

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt den Frachtabstimmungsprozess.

Die Frachtabstimmung kann manuell oder automatischen durchgeführt werden. Um die automatische Frachtabstimmung zu verwenden, müssen Sie einen Überwachungsmaster einrichten. In ihm können Sie die Kriterien definieren, die festlegen, welche Fracht automatisch abgestimmt wird.

## <a name="the-freight-reconciliation-process"></a>Der Frachtabstimmungsprozess
Frachtkosten werden vom den Tarifmodul berechnet, das dem relevanten Spediteur zugeordnet ist. Wenn ein Ladung bestätigt ist, wird ein Frachtbrief erstellt und die Frachtkosten werden an diesen übertragen. Die Frachtkosten werden je nach Konfiguration für den regulären Abrechnungsprozess als sonstige Zuschläge auf das entsprechende Quelldokument umgelegt (Bestellung, Auftrag und/oder Umlagerungsauftrag). Der Frachtabstimmungsprozesse (auch Abgleichsprozess genannt) kann starten sobald die Frachtrechnung vom Spediteur eingeht. Die Rechnung elektronisch oder auf Papier erhalten werden. Wenn die Rechnung auf Papier erhalten wird, können Sie mit dem Frachtbrief als Vorlage eine elektronische Rechnung generieren. 

[![Frachtabstimmungsprozess](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Manuelle Abstimmung
Wenn Sie die Fracht manuell abstimmen, müssen Sie jede Rechnungsposition mit der Frachtbriefposition oder den-positionen für die zu fakturierende Ladung abgleichen. Diesen Abgleich führen Sie auf der Seite **Frachtbrief- und Rechnungsabgleich** durch. Wenn der Betrag der Rechnungsposition nicht mit dem Frachtbriefbetrag übereinstimmt, müssen Sie einen Abstimmungsgrund für die Abweichung auswählen. Sind mehrere Gründe für die Abstimmung zutreffen, können Sie die nicht abgeglichenen Mengen auf diese Gründe verteilen. Der Abstimmungsgrund bestimmt, wie die Differenzbeträge im Hauptbuch gebucht werden. Bei die Abstimmung des gesamten Rechnungsbetrags gebucht wird, wird dieser zur Genehmigung gesendet. Dann wird die Erfassung gebucht. Die folgende Abbildung zeigt, wie eine Frachtrechnung generiert und eine Frachtabstimmung ausgeführt wird. 
[![Frachtabstimmungsaufgaben](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>Automatische Abstimmung
Um die automatische Abstimmung zu verwenden, müssen Sie den Zeitplan für die Abstimmung und die zu verwendenden Rechnungen und Spediteure angeben. Der Abgleich der Rechnungspositionen und Frachtbriefe wird entsprechend der Einrichtung des Überwachungsmasters und der Frachtbriefart ausgeführt. Nach dem Ausführen der automatischen Abstimmung müssen Sie alle Rechnungen bearbeiten, die das System nicht zuordnen kann. Sie müssen diese Rechnungen dann manuell verarbeiten, bevor Sie alle Rechnung für die Zahlung buchen können.



