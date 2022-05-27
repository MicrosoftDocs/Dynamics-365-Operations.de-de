---
title: Einen Intercompany-Auftrag zur internen Verwendung erstellen
description: In diesem Thema wird erläutert, wie Sie einen Intercompany-Auftrag zur internen Verwendung erstellen.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 9b4d2dc450fb5996e0e08c92836c1d1942a05b73
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673689"
---
# <a name="create-an-intercompany-sales-order-for-internal-use"></a>Einen Intercompany-Auftrag zur internen Verwendung erstellen

[!include [banner](../../includes/banner.md)]

In der Regel wird ein Intercompany-Auftrag automatisch anhand einer Intercompany-Bestellung angelegt. Sie können einen Intercompany-Auftrag auch manuell erstellen, der dann eine Intercompany-Bestellung in der juristischen Person des Intercompany-Debitors generiert.

![Interner Intercompany-Verkaufsprozess](media/intercompanyinternalsalesprocess.png)

## <a name="create-an-intercompany-sales-order-manually"></a>Intercompany-Auftrag manuell erstellen

Führen Sie diese Schritte unter „Juristische Person B“ aus, wie in der Abbildung dargestellt.

1. Wechseln Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Aktionsbereich die Option **Auftrag** aus, um einen Auftrag zu erstellen.
1. Wählen Sie auf der Seite **Auftrag erstellen** ein Debitorenkonto aus. Stellen Sie sicher, dass das Kontrollkästchen **Intercompany** im Inforegister **Allgemein** aktiviert ist. Damit wird angegeben, dass der ausgewählte Debitor ein Intercompany-Debitor ist.
1. Geben Sie Daten ein, oder ändern Sie vorhandene Angaben, und wählen Sie **OK** aus. Füllen Sie die Auftragspositionen dann wie gewohnt aus.

    Der Wert des Felds **Lieferadresse** wird aus dem Kopf des Intercompany-Auftrags in den Kopf der Intercompany-Bestellung kopiert. Der Wert des Felds **Artikelnummer**, einschließlich Produktdimensionen, und die Werte der Felder **Lieferdatum** und **Währungscode** werden aus den Intercompany-Auftragspositionen in die Intercompany-Bestellpositionen kopiert.

1. Wählen Sie im Auftragskopf **Intercompany** aus, um die zugehörige Intercompany-Bestellung anzuzeigen.
1. Wählen Sie in den Auftragspositionen **Intercompany** aus, um Informationen zum Intercompany-Handel anzuzeigen.

> [!TIP]
> Sie können Intercompany-Verkaufsaufträge auf der Seite **Intercompany-Aufträge** anzeigen.

> [!NOTE]
> Wenn Sie mit „Intercompany“ arbeiten, wird empfohlen, dass Sie das Kontrollkästchen **Auftrag nach Rechnungsstellung löschen** auf der Seite **Debitorenparameter** deaktivieren. Andernfalls wird die zugehörige Bestellung gelöscht. Außerdem wird empfohlen, dass Sie das Kontrollkästchen **Bestellung nach Rechnungsstellung löschen** auf der Seite **Kreditorenparameter** deaktivieren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
