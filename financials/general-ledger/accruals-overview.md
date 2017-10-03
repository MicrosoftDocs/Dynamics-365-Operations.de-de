---
title: "Abgrenzungsüberblick"
description: Dieser Artikel beschreibt Abgrenzungen und gibt Informationen, wie sie aufgesetzt werden und wie Transaktionen erstellt werden.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 87d9f7fbdbc06a3399a6ec5c2492de0f053b1513
ms.contentlocale: de-de
ms.lasthandoff: 08/01/2017

---

# <a name="accruals-overview"></a>Abgrenzungsüberblick

[!include[banner](../includes/banner.md)]


Dieser Artikel beschreibt Abgrenzungen und gibt Informationen, wie sie aufgesetzt werden und wie Transaktionen erstellt werden.

Abgrenzungen werden in der periodengerechten Abgrenzung verwendet, um den Umsatzerlös zu verfolgen, der in der Periode realisiert wird, in der er erzielt wurde und nicht bezahlt, und um Aufwendungen (Kosten) zu verfolgen, die realisiert werden, wenn Sie entstehen, nicht wenn Sie bezahlt werden.

## <a name="accrual-schemes"></a>Abgrenzungsschemata
Abgrenzungsschemata werden verwendet, um den Umsatzerlös und die Kosten einzurichten. Das gleiche Abgrenzungsschema kann für Umsatzerlöse und Kosten verwendet werden. Mit Sachkontoabgrenzungen werden die Kosten oder der Umsatzerlös einer Erfassungsposition neu verteilt, damit die Kosten und Umsatzerlöse in den entsprechenden Perioden berücksichtigt werden. Geben Sie auf der **Abgrenzungsschema**-Seite das die Soll- und Habenkonten an, die verwendet werden, wenn das Abgrenzungsschema angewendet wird.

-   **Soll** - Das Hauptkonto, das Sie definieren, ersetzt das Sollhauptkonto auf der Erfassungsbelegposition. Dieses Konto wird auf Grundlage der Sachkontoabgrenzungsbuchungen auch für die Rückbuchung der Stundung verwendet.
-   **Gutschrift** - Das Hauptkonto, das Sie definieren, ersetzt das Gutschriftenhauptkonto auf der Erfassungsbelegposition. Dieses Konto wird auf Grundlage der Sachkontoabgrenzungsbuchungen auch für die Rückbuchung der Stundung verwendet.

Nachdem Sie bestimmt haben, welche Konten Sie verwenden, können Sie angeben, wie die Belegnummer erstellt wird, wenn Abgrenzungsbuchungen erstellt werden. Sie können auch angeben, wie häufig die Buchungen auftreten, die Häufigkeit, mit der die Buchungen erstellt werden, und wann die Buchungen gebucht werden. Nachdem das Abgrenzungsschema erstellt wurde, können Sie es in einigen der Erfassungen verwenden, indem Sie die Sachkontoabgrenzungsfunktion verwenden.

## <a name="ledger-accruals"></a>Sachkontoabgrenzungen
Wenn Sie eine Erfassung eingeben, können Sie im Menü **Funktionen** auf **Sachkontenabgrenzungen** klicken. Wenn Sie anschließend das Abgrenzungsschema auswählen, wird der Grundbetrag aus der Erfassung angezeigt, die so über die Periode verteilt wird, wie es das Abgrenzungsschema bestimmt. Wenn Sie beispielsweise die Versicherung eines Mitarbeiters für das gesamte Jahr im Januar begleichen und der Betrag ist 12.000, müssen Sie diese Ausgaben jeden Monat realisieren. Sie können das Startdatum auswählen. Wählen Sie das Startdatum der Vereinbarung aus. Sie können auch angeben, ob der antizipierte Betrag auf dem Konto oder dem Gegenkonto basiert ist. Nachdem Sie Ihre Auswahl treffen, klicken Sie auf **Buchungen**, um alle Buchungen anzuzeigen, die basierend auf das Abgrenzungsschema erstellt wurden. Wenn Sie 12.000 in den Versicherungskosten auf ein Jahr verteilen, sehen Sie die Zahl 1.000 für jeden Monat. Nachdem Sie die Erfassung buchen, können Sie die Buchungen anzeigen, indem Sie die Abfragenseite **Belegbuchunge** verwenden. Wenn ein Abgrenzungsschema nicht angewendet werden kann (beispielsweise, wenn eine Auftrags- oder eine Einkaufsrechnung vorhanden ist), können Sie den bereits bezahlten Betrag gutschreiben und den Kostenbetrag belasten. Sie können dann **Gegenkonto** auswählen, wenn Sie das Abgrenzungsschema anwenden.


Weitere Informationen finden Sie unter [Erstellen von Abgrenzungsschemata](tasks/create-accrual-schemes.md) [Erstellen von Sachkonto-Abgrenzungsbuchungen](tasks/create-ledger-accrual-transactions.md).

