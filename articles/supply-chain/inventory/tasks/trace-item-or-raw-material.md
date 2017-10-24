---
title: Artikel oder Rohmaterial nachverfolgen
description: Dieses Verfahren zeigt, wie die Artikelverfolgung angewendet wird, um zu erkennen, wo Artikel oder Rohmaterial verwendet wurden oder verwendet werden.
author: pjacobse
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d7eb282ddf9597385d6660a3fc0ef73f403ab898
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="trace-an-item-or-raw-material"></a>Artikel oder Rohmaterial nachverfolgen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie die Artikelverfolgung angewendet wird, um zu erkennen, wo Artikel oder Rohmaterial verwendet wurden oder verwendet werden. Mit dieser Prozedur können Sie einen Artikel identifizieren, ihn zur Quelle zurückverfolgen und dann die Abläufe vorwärts verfolgen über die Produktion und den Vertrieb des fertigen Produkts. Der Prozess kann verwendet werden, um die Debitoren, die beeinflusst werden, die betroffenen Aufträge usw. zu überprüfen. Für diese Prozedur wird das Demodatunternehmen USP2 verwendet.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Einen Artikel rückwärts mithilfe einer bekannten Chargennummer verfolgen
1. Wechseln Sie zu Lagerverwaltung >Abfragen und Berichte > Rückverfolgungsangaben > Artikelverfolgung.
2. Wählen Sie im Feld "Artikelnummer" die Zeichenfolge "P9100" aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Wählen Sie im Feld "Vorwärts oder rückwärts" "Rückwärts" aus.
5. Wählen Sie im Feld "Chargennummer" "as-12-344-01" aus.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Klicken Sie auf "OK".

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Einen Artikel festlegen, vorwärts verfolgen und analysieren
    * Der oberste Knoten der Struktur stellt die verfügbare Menge des ausgewählten Artikels und der Charge dar. Sie müssen die Knoten der Struktur erweitern, um den Artikel zu finden, bei dem die Vorwärtsablaufverfolgung ausgeführt werden soll.   
1. Erweitern Sie in der Struktur "die unten beschriebenen Knoten und wählen Sie dann den letzten Knoten aus".
    * Erweitern Sie: "P9100 / 1 / 10 / as-12-344-01 ● 117 Liter ● 26,4 Liter  \P9100 ● Entnommen ● Auftrag 000072 ● 22.12.2015 ● -58,6 Liter ● -15 Liter ● Standort=1, Lagerort=10, Chargennummer=als-12-344-01   \P9100 ● Produktion B-000050 ● 9.12.2015● 410,72 Liter ● 102,21 Liter ● Standort=1, Lagerort=10, Chargennummer=als-12-344-01 ● Co-Produkte: P9101" und wählen Sie dann diesen Knoten aus.     
2. Erweitern Sie in der Struktur "den unten beschriebenen Knoten und wählen Sie dann diesen Knoten aus".
    * Beginnend am Knoten, den Sie soeben ausgewählt haben, erweitern Sie "M9103 ● Produktionsposition B-000050 ● 09.12.2015 ● -72,57 kg ● Größe=70, Farbe=OK, Standort=1, Lagerort=10, Charennummer=App01" und wählen Sie dann diesen Knoten aus.  
3. Klicken Sie auf "Ausgangsknoten für Verfolgung".
4. Klicken Sie auf "Vorwärts".
5. Klicken Sie im Aktivitätsbereich auf "Verfolgung".
    * Es gibt mehrere Ablaufverfolgungsoptionen, die Informationen zu Debitoren bereitstellen, die vom Artikel betroffen sind, den Sie nachverfolgen, sowie von den Aufträgen, die sich auf den Artikel beziehen, der versendet wurde oder nicht versendet wurde.   
6. Klicken Sie auf "Debitoren".
7. Schließen Sie die Seite.
8. Klicken Sie im Aktivitätsbereich auf "Verfolgung".
9. Klicken Sie auf "Gelieferte Aufträge".
10. Schließen Sie die Seite.

