---
title: Artikel oder Rohmaterial nachverfolgen
description: Dieses Verfahren zeigt, wie die Artikelverfolgung angewendet wird, um zu erkennen, wo Artikel oder Rohmaterial verwendet wurden oder verwendet werden.
author: pjacobse
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe0fd9a7c27efb71f15cca9d3a0341b550bf9698
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916670"
---
# <a name="trace-an-item-or-raw-material"></a>Artikel oder Rohmaterial nachverfolgen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie die Artikelverfolgung angewendet wird, um zu erkennen, wo Artikel oder Rohmaterial verwendet wurden oder verwendet werden. Mit dieser Prozedur können Sie einen Artikel identifizieren, ihn zur Quelle zurückverfolgen und dann die Abläufe vorwärts verfolgen über die Produktion und den Vertrieb des fertigen Produkts. Der Prozess kann verwendet werden, um die Debitoren, die beeinflusst werden, die betroffenen Aufträge usw. zu überprüfen. Für diese Prozedur wird das Demodatunternehmen USP2 verwendet.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Einen Artikel rückwärts mithilfe einer bekannten Chargennummer verfolgen
1. Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Module > Bestandsmanagement > Anfragen und Berichte > Verfolgungsdimensionen > Artikelverfolgung**.
2. Wählen Sie im Feld **Artikelnummer**'P9100'.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Wählen Sie im Feld **Vorwärts oder Rückwärts** die Option'Rückwärts'.
5. Wählen Sie im Feld **Chargennummer** die Option'as-12-344-01'.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Klicken Sie auf **OK**.

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Einen Artikel festlegen, vorwärts verfolgen und analysieren

Der oberste Knoten der Struktur stellt die verfügbare Menge des ausgewählten Artikels und der Charge dar. Sie müssen die Knoten der Struktur erweitern, um den Artikel zu finden, bei dem die Vorwärtsablaufverfolgung ausgeführt werden soll.   
1. Erweitern Sie in der Struktur "die unten beschriebenen Knoten und wählen Sie dann den letzten Knoten aus".
    
    Erweitern Sie: "P9100 / 1 / 10 / as-12-344-01 ● 117 Liter ● 26,4 Liter  \P9100 ● Entnommen ● Auftrag 000072 ● 22.12.2015 ● -58,6 Liter ● -15 Liter ● Standort=1, Lagerort=10, Chargennummer=als-12-344-01   \P9100 ● Produktion B-000050 ● 9.12.2015● 410,72 Liter ● 102,21 Liter ● Standort=1, Lagerort=10, Chargennummer=als-12-344-01 ● Co-Produkte: P9101" und wählen Sie dann diesen Knoten aus.     
2. Erweitern Sie in der Struktur "den unten beschriebenen Knoten und wählen Sie dann diesen Knoten aus".
    
    Beginnend am Knoten, den Sie soeben ausgewählt haben, erweitern Sie "M9103 ● Produktionsposition B-000050 ● 09.12.2015 ● -72,57 kg ● Größe=70, Farbe=OK, Standort=1, Lagerort=10, Charennummer=App01" und wählen Sie dann diesen Knoten aus.  
3. Klicken Sie auf **Trace vom Knoten**.
4. Klicken Sie auf **Vorwärts**.
5. Klicken Sie im **Aktionsbereich** auf **Verfolgung**.
    
    Es gibt mehrere Ablaufverfolgungsoptionen, die Informationen zu Debitoren bereitstellen, die vom Artikel betroffen sind, den Sie nachverfolgen, sowie von den Aufträgen, die sich auf den Artikel beziehen, der versendet wurde oder nicht versendet wurde.   
6. Klicken Sie auf **Kunden**.
7. Schließen Sie die Seite.
8. Klicken Sie im **Aktionsbereich** auf **Verfolgung**.
9. Klicken Sie auf **Versendete Kundenaufträge**.
10. Schließen Sie die Seite.

