---
title: "Abgrenzungsüberblick"
description: Dieser Artikel beschreibt Abgrenzungen und gibt Informationen, wie sie aufgesetzt werden und wie Transaktionen erstellt werden.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 328a4a7bef32ee8634e4a9f4854ebe78fcc99f6d
ms.lasthandoff: 03/31/2017


---

# <a name="accruals-overview"></a>Abgrenzungsüberblick

Dieser Artikel beschreibt Abgrenzungen und gibt Informationen, wie sie aufgesetzt werden und wie Transaktionen erstellt werden.

Abgrenzungen werden in der periodengerechten Abgrenzung verwendet, um den Umsatzerlös zu verfolgen, der in der Periode realisiert wird, in der er erzielt wurde und nicht bezahlt, und um Aufwendungen (Kosten) zu verfolgen, die realisiert werden, wenn Sie entstehen, nicht wenn Sie bezahlt werden.

## <a name="accrual-schemes"></a>Abgrenzungsschemata
Abgrenzungsschemata werden verwendet, um den Umsatzerlös und die Kosten einzurichten. Das gleiche Abgrenzungsschema kann für Umsatzerlöse und Kosten verwendet werden. Mit Sachkontoabgrenzungen werden die Kosten oder der Umsatzerlös einer Erfassungsposition neu verteilt, damit die Kosten und Umsatzerlöse in den entsprechenden Perioden berücksichtigt werden. Geben Sie auf der **Abgrenzungsschema**-Seite das die Soll- und Habenkonten an, die verwendet werden, wenn das Abgrenzungsschema angewendet wird.

-   **Soll** - Das Hauptkonto, das Sie definieren, ersetzt das Sollhauptkonto auf der Erfassungsbelegposition. Dieses Konto wird auf Grundlage der Sachkontoabgrenzungsbuchungen auch für die Rückbuchung der Stundung verwendet.
-   **Gutschrift** - Das Hauptkonto, das Sie definieren, ersetzt das Gutschriftenhauptkonto auf der Erfassungsbelegposition. Dieses Konto wird auf Grundlage der Sachkontoabgrenzungsbuchungen auch für die Rückbuchung der Stundung verwendet.

Nachdem Sie bestimmt haben, welche Konten Sie verwenden, können Sie angeben, wie die Belegnummer erstellt wird, wenn Abgrenzungsbuchungen erstellt werden. Sie können auch angeben, wie häufig die Buchungen auftreten, die Häufigkeit, mit der die Buchungen erstellt werden, und wann die Buchungen gebucht werden. Nachdem das Abgrenzungsschema erstellt wurde, können Sie es in einigen der Erfassungen verwenden, indem Sie die Sachkontoabgrenzungsfunktion verwenden.

## <a name="ledger-accruals"></a>Sachkontoabgrenzungen
Wenn Sie eine Erfassung eingeben, können Sie im Menü **Funktionen** auf **Sachkontenabgrenzungen** klicken. Wenn Sie anschließend das Abgrenzungsschema auswählen, wird der Grundbetrag aus der Erfassung angezeigt, die so über die Periode verteilt wird, wie es das Abgrenzungsschema bestimmt. Wenn Sie z die Versicherung eines Mitarbeiters für das gesamte Jahr im Januar bezahlen, und der Betrag ist 12.000, Sie müssen diese Ausgaben jeden Monat realisieren. Sie können das Startdatum auswählen. Sie können auch angeben, ob der antizipierte Betrag auf dem Konto oder dem Gegenkonto basiert ist. Nachdem Sie Ihre Auswahl treffen, klicken Sie auf Buchungen ** ** um alle Buchungen anzuzeigen, die basierend das Abgrenzungsschema erstellt wurden. Wenn Sie z die 12.000 in den Versicherungskosten in dem Jahr ausgebreitet werden finden Sie, 1.000 für jeden Monat. Nachdem Sie die Erfassung buchen, können Sie die Buchungen anzeigen, indem Sie die Abfragenseite ** Belegbuchungen ** verwenden. Wenn Sie ein Abgrenzungsschema nicht angewendet werden kann (beispielsweise, wenn eine Auftrags- oder eine Einkaufsrechnung vorhanden ist), können Sie den frankierten Betrag gutgeschrieben und den Kostenbetrag belasten. Sie können dann **Gegenkonto** auswählen, wenn Sie das Abgrenzungsschema anwenden.


