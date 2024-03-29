---
title: Einzelhandelsaufstellungen
description: In diesem Artikel wird beschrieben, wie Auszüge erstellt und gebucht werden.
author: ashishmsft
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 0717c1198171f411e3c52233200ecfcc213dc13f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878456"
---
# <a name="retail-statements"></a>Einzelhandelsaufstellungen

[!include [banner](includes/banner.md)]

In Dynamics 365 Commerce wird der Auszugsbuchungsprozess verwendet, um die Buchungen zu berücksichtigen, die in Cloud Point of Sale (POS) oder Modern POS (MPOS) erfolgen. Der Auszugsbuchungsprozess verwendet den Verteilungszeitplan, um einen Satz POS-Buchungen in den Headquarters (HQ)-Client einzubeziehen. Die Parameter, die auf den Seiten **Commerce-Parameter** und **Filialen** definiert werden, werden dazu verwendet, um die Transaktionen auszuwählen, die in einzelne Auszüge einbezogen werden.

Das folgende Abbildung zeigt den Auszugsbuchungsprozess. In diesem Vorgang werden Transaktionen, die im POS erfasst werden, mit dem Commerce-Steuerprogramm an den Client gesendet. Nachdem der Client die Buchungen erhält, können Sie den Buchungsauszug für die Filialen erstellen, berechnen und buchen.

[![Auszugsbuchungsprozess.](./media/retail-statements.png)](./media/retail-statements.png)

## <a name="creating-and-posting-statements"></a>Auszüge erstellen und buchen

Sie können eine Aufstellung manuell oder durch Stapelverarbeitungsvorgänge verwenden, die Sie so einrichten, dass sie in regelmäßigen Abständen während des ganzen Tages ausgeführt werden. In beiden Fällen werden die folgenden Schritte verwendet, um Auszüge zu erstellen und zu buchen.

### <a name="create-the-statement"></a>Den Auszug erstellen

In diesem Schritt wird der Shop angegeben, für den die Aufstellung manuell erstellt wird. Wenn Sie eine Stapelverarbeitung konfigurieren, können Sie automatisch für alle Shops Aufzüge auf Basis eines Zeitplans erstellen, den Sie definieren.

### <a name="calculate-the-statement"></a>Den Auszug berechnen

In diesem Schritt werden die Transaktionspositionen auf Basis der Kriterien ausgewählt, die für jede Filiale auf den Seiten **Commerce-Parameter** und **Filialen** definiert sind. Auf diesen Seiten definieren Sie die Kriterien und geben an, wie die Buchungen berechnet werden. Sie können die Seite **Buchungen** verwenden, um eine Liste der Buchungen anzuzeigen, die in den Auszug einbezogen werden, bevor die Aufstellung berechnet wird.

Die Auszugsberechnung verwendet Kassenstürze aus den Registern als gezählten Betrag. Ersatzweise können Sie die gezählte Summe manuell eingeben. Der Auszug zeigt die Differenz zwischen dem Umsatzbetrag für die Buchungen und dem tatsächlich gezählten Betrag in allen Zahlungtypen an. Der Auszug wird nur gebucht, wenn diese Differenz nicht die maximale Buchungsdifferenz überschreitet, die für den Shop definiert ist.

> [!NOTE]
> Der Auszugsberechnungsprozess verwendet den globalen Nummernkreis.

Wenn Sie einen Auszug berechnen, umfasst die Berechnung die folgenden Aufgaben:

- Markieren Sie für den ausgewählten Datumsbereich Buchungen, die nicht in einer früheren Auszugsberechnung enthalten waren.
- Berechnen Sie die Gesamtbeträge, die in den ausgewählten Buchungen gezahlt wurden. Die Ergebnisse werden auf den Auszugspositionen angezeigt, abhängig von der Auszugsmethode:

    - Falls die Auszugsmethode **Gesamt** ist, wird eine Position für jede einzelne Zahlungsmethode in den ausgewählten Buchungen erstellt.
    - Falls die Auszugsmethode **Mitarbeiter** ist, wird eine Position für jede einzelne Zahlungsmethode in Buchungen erstellt, die von dem ausgewählten Mitarbeiter durchgeführt wurden.
    - Falls die Auszugsmethode **POS-Terminal** ist, wird eine Position für jede einzelne Zahlungsmethode in Buchungen erstellt, die im ausgewählten Register durchgeführt wurden.
    - Falls die Auszugsmethode **Schicht** ist, wird eine Position für jede einzelne Zahlungsmethode in Buchungen erstellt, die während einer Schicht durchgeführt wurden.

Wenn das Kontrollkästchen **Nach Auszugsmethode aufteilen** auf der Seite **Filialen** aktiviert ist, wird ein separater Auszug basierend auf dem Wert erstellt, der im Feld **Auszugsmethode** ausgewählt ist.

Wenn Ihre Geschäftssstunden über Mitternacht hinausgehen, können Sie die Auszugsbuchung so konfigurieren, dass sie auf dem Ende des Arbeitstags basiert anstelle des Endes des Kalendertags.

Geben Sie auf der Seite **Filialen** im Inforegister **Auszug/Abschluss** im Feld **Ende des Arbeitstags** die Zeit ein, zu der die letzte Buchung aufgezeichnet werden muss, die im Auszug des Arbeitstags enthalten sein muss. Aktivieren Sie das Kontrollkästchen **Als Arbeitstag buchen**, um die Buchungen innerhalb des gleichen Arbeitstags zu buchen. Wenn der Auszug gebucht wird, können Buchungen, die innerhalb des gleichen Arbeitstages erfasst sind, im gleichen Auftrag einbezogen werden, auch wenn einige Buchungen vor Mitternacht und andere Buchungen nach Mitternacht auftreten.

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a>Beispiel: Buchen eines Auszugs für einen Werktag, der sich über zwei Kalendertage erstreckt

Eine Filiale ist von 8:00 Uhr vormittags bis 3:00 Uhr morgens geöffnet, und das Kontrollkästchen **Als Arbeitstag buchen** ist in der Konfiguration der Filiale aktiviert. Am 31. Mai erfasst die Filiale Buchungen zwischen 8:00 Uhr vormittags und Mitternacht. Die Filiale erfasst auch Buchungen am 1. Juni zwischen 24:00 Uhr und 3:00 Uhr.

Wenn die Filiale den Auszug für den Abschluss des Arbeitstages bucht, umfasst der Auftrag, der generiert wird, alle Buchungen, die zwischen den Geschäftsstunden von 8:00 Uhr vormittags und von 3:00 Uhr morgens erfasst wurden, obwohl die Buchungen an zwei Tagen erfolgten, nämlich am 31. Mai und 1. Juni.

Wenn das Kontrollkästchen **Als Arbeitstag buchen** für dieselbe Filiale deaktiviert ist, werden separate Aufträge generiert, wenn die Filiale den Auszug für den Abschluss des Werktages bucht. Ein Auftrag umfasst die Buchungen, die zwischen den Geschäftsstunden 8:00 Uhr und Mitternacht am 31. Mai erfasst wurden, und der zweite Auftrag umfasst die Buchungen, die zwischen Geschäftsstunden von 24:01 Uhr und 3:00 Uhr am 1. Juni erfasst wurden.

> [!NOTE]
> Bevor Sie Aufstellungen erstellen können, sollten Sie die Schichten im Aufstellungszeitraum schließen.

### <a name="post-the-statement"></a>Buchen des Auszugs

Wenn Sie einen Auszug buchen, werden Aufträge und Rechnungen für die Verkäufe in der Aufstellung erstellt.

- Cash-and-carry-Aufträge werden in einem Auftrag zusammengefasst und für den Standarddebitor fakturiert, der der Filiale zugewiesen ist.
- Verkäufe, für die ein Debitor zu der Transaktion in POS hinzugefügt wurde, generieren für jeden einzelnen Debitor separate Aufträge und Rechnungen.

Zahlungserfassungen werden automatisch für die Zahlungen in der Aufstellung erstellt, und der Lagerbestand wird für den POS-Speicher aktualisiert.


[!INCLUDE[footer-include](../includes/footer-banner.md)]