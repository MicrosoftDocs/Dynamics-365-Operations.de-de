---
title: Ausführen von Rechnungsaktualisierungen für Rücklieferungen
description: Diese Funktion unterstützt die Geschäftsprozesse von Organisationen, in denen Rücklieferungen und Aufträge gleichzeitig und von der gleichen Person fakturiert werden sollen.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41d3b884d1ed11d2f79e968a5a099860486ef600
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810653"
---
# <a name="perform-invoice-updates-for-returns"></a>Ausführen von Rechnungsaktualisierungen für Rücklieferungen 

[!include [banner](../includes/banner.md)]


Eine Rücklieferung ist ein Typ eines Auftrags, der als zurückgegebener Auftrag markiert ist. **Daher wird die Listenseite** zum Erzeugen von Rechnungen für Rücklieferungen anstelle des Formulars **Rücklieferungen** verwendet. Diese Funktion unterstützt die Geschäftsprozesse von Organisationen, in denen Rücklieferungen und Aufträge gleichzeitig und von der gleichen Person fakturiert werden sollen.

Da die Rechnung für einen zurückgelieferten Artikel einen negativen Betrag ausweist, wird sie als Gutschrift bezeichnet.

Beim Einrichten der Rechnungsaktualisierung für die Stapelverarbeitung muss für den Auftrag vom Typ **Rücklieferung** der Status der Rückgabeposition **Eingegangen** lauten, womit angezeigt wird, dass der Lieferschein des Auftrags aktualisiert wurde.

## <a name="post-an-invoice-for-a-return-order"></a>Buchen einer Rechnung für eine Rücklieferung

1.  Klicken auf **Debitorenkonten** \> **Allgemein** \> **Aufträge** \> **Alle Aufträge**.

2.  Wählen Sie einen Auftrag aus, für den **rückstendungen** im Feld **Auftragstyp** angezeigt wird.

3.  Klicken Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** auf **Rechnung**.

4.  Wählen Sie auf der Registerkarte **Parameter** das Kontrollkästchen **Buchung** aus.

5.  Prüfen Sie die Informationen im Formular, und nehmen Sie ggf. erforderliche Änderungen vor.

6.  Klicken Sie auf **OK**. Die Gutschrift wird gebucht.

## <a name="see-also"></a>Siehe auch

[Lieferscheinaktualisierungen für Rücklieferungen](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]