---
title: Rückvergütungen verarbeiten, überprüfen und buchen
description: In diesem Thema wird beschrieben, wie Sie Ihre Rückvergütungsverwaltungsdeals verarbeiten, deren Rabatte berechnen, die generierten Transaktionen überprüfen, Transaktionen buchen und die Buchungen überprüfen.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 524aec8025378391057275f77e31191f88e4a98b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690273"
---
# <a name="process-review-and-post-rebates"></a>Rückvergütungen verarbeiten, überprüfen und buchen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Ihre Rückvergütungsverwaltungsdeals verarbeiten, deren Rabatte berechnen, die generierten Transaktionen überprüfen, Transaktionen buchen und die Buchungen überprüfen.

## <a name="change-the-status-of-a-deal"></a>Ändern des Status eines Deals

Sie können jedem Deal einen Status zuweisen, um ihn besser nachverfolgen zu können. Dieser Status dient nur zu Informationszwecken.

1. Wählen Sie einen Deal aus (z. B. von der [Seite **Alle Rückvergütungsverwaltungsdeals**](rebate-management-deals.md)).
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rückvergütungsverwaltungsdeals** in der Gruppe **Verwalten** die Option **Status ändern**.
1. Legen Sie im Dialogfeld **Status ändern** einen neuen Status für das Feld **Rückvergütungsstatus** fest.
1. Wählen Sie **OK**.

## <a name="calculate-fifo-purchase-prices"></a>FIFO-Einkaufspreise berechnen

Die periodische Aufgabe **FIFO-Einkaufspreis berechnen** muss ausgeführt werden, um die Rückvergütung für [Deals](rebate-management-deals.md) zu berechnen, bei denen das Feld **Preisbasis** auf *FIFO* gesetzt ist. Das System berechnet anhand einer FIFO-Regel (First in, first out) den Wert des verkauften Bestands. Dieser Wert wird dann zur Berechnung der Kreditorenrückvergütungen verwendet.

Gehen Sie zu **Rückvergütungsverwaltung \> Periodische Aufgaben \> FIFO-Einkaufspreise berechnen**. Wählen Sie im angezeigten Dialogfeld **OK** aus, um die Berechnung auszuführen.

## <a name="create-source-transactions"></a>Quellentransaktionen erstellen

Sie können die Aufträge oder Bestellungen mit Quellentransaktionen entweder vor oder nach dem Erstellen eines entsprechenden Rückvergütungsverwaltungsdeals erstellen.

Sie können jede Dealposition so einrichten, dass automatisch eine Rückvergütungsbereitstellung erstellt wird, indem die Lieferung oder Rechnung für einen Auftrag oder eine Bestellung gebucht wird. Legen Sie das Feld **Transaktionstyp** für die Dealposition auf *Lieferung* oder *Rechnung* fest und stellen Sie die Option **Bei Buchung verarbeiten** auf *Ja*. Wenn das Feld **Transaktionstyp** auf *Auftrag* festgelegt ist, ist die Verarbeitung bei der Buchung deaktiviert. Bei Quellentransaktionen, die nach der Aktivierung eines Deals angelegt wurden, können Sie die Bereitstellung weiterhin wie im Abschnitt [Rückvergütungsverwaltungsdeals verarbeiten](#process-deals) weiter unten in diesem Thema beschrieben verarbeiten.

### <a name="enable-price-details"></a>Preisdetails aktivieren

Bevor Sie Quellen transaktionen erstellen können, müssen Sie die Option **Preisdetails aktivieren** Option für Debitoren aktivieren.

1. Gehen Sie zu **Debitoren \> Einrichtung \> Debitorenparameter**.
1. Legen Sie auf der Registerkarte **Preise** im Inforegister **Preisdetails** die Option **Preisdetails aktivieren** auf *Ja* fest.

### <a name="create-a-source-transaction"></a>Eine Quellentransaktionen erstellen

Gehen Sie folgendermaßen vor, um einen Quellentransaktion zu erstellen.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus.

    Um die Methode zu imitieren, mit der Rückvergütungsansprüche generiert werden, müssen Sie Auftrag erstellen, in dem das Produkt und die Menge den Debitor für eine Rückvergütung qualifizieren.

1. Geben Sie im Feld **Debitorenkonto** einen Debitor ein oder wählen Sie einen aus, der sich für einen Rückvergütungsdeal qualifiziert.
1. Wählen Sie **OK** aus, um den Auftrag zu erstellen.
1. Fügen Sie im Inforegister **Auftragspositionen** eine Position ein und legen Sie die folgenden Felder dafür fest:

    - **Artikelnummer**: Geben Sie einen Artikel an, der sich für eine Rückvergütung qualifiziert.
    - **Menge**: Geben Sie eine Menge an, die sich für einen Rückvergütungsdeal qualifiziert, der eine Position enthält, in der das Feld **Basis** auf *Menge* gesetzt ist.
    - **Preis je Einheit**: Geben Sie einen Preis an, der sich für einen Rückvergütungsdeal qualifiziert, der eine Position enthält, in der das Feld **Basis** auf *Wert* gesetzt ist.
    - **Standort**: Wählen Sie einen Standort aus, an dem das Produkt verfügbar ist und der sich für einen Rückvergütungsdeal qualifiziert.
    - **Lagerort**: Wählen Sie einen Lagerort aus, an dem das Produkt verfügbar ist und der sich für einen Rückvergütungsdeal qualifiziert.

1. Wählen Sie auf der Symbolleiste im Inforegister **Auftragspositionen** **Auftragsposition \> Preisdetails** aus. Dieser Befehl ist nur verfügbar, wenn Sie Preisdetails wie im vorherigen Abschnitt beschrieben aktiviert haben.
1. Wählen Sie auf der Seite **Preisdetails** das Inforegister **Rückvergütungsverwaltung** aus. Dieses Inforegister listet alle Rückvergütungsverwaltungsdeal auf, die für die aktuelle Auftragsposition gültig sind und zeigt den geschätzten Rückvergütungsbetrag in der Währung des Auftrags an. Beachten Sie, dass es sich bei den Beträgen nur um Schätzungen der zukünftigen Rückvergütungsansprüche handelt. Die tatsächlichen Rückvergütungsansprüche können abweichen. Hier sind einige der Faktoren, die die tatsächlichen Beträge beeinflussen können:

    - Das Gesamtumsatzvolumen, das der Kunde im Rahmen einer periodischen Rückvergütungsvereinbarung erzielt hat.
    - Ob der Kunde alle Mengen oder Teilmengen zurückgeschickt hat.
    - Ob der entsprechende Auftrag den Transaktionstyp (*Auftrag, Lieferung* oder *Rechnung*) erreicht hat, der für den Rückvergütungsverwaltungsdeal definiert ist.
    - Der **Ausgabe** wert des Deals. Ein leerer Rückvergütungsbetrag wird für Deals angezeigt, bei denen das Feld **Ausgabe** auf *Artikel* gesetzt ist.

1. Bitte beachten Sie, dass auf dem Inforegister **Detail** der Abschnitt **Margenvorkalkulation** die folgenden Felder enthält. Diese Felder werden von der Rückvergütungsverwaltung hinzugefügt. Alle zeigen Werte pro Einheit (während die Felder auf dem Inforegister **Rückvergütungsverwaltung** Gesamtwerte für die Position anzeigt).

    - **Rückvergütungsbetrag Rückvergütungsverwaltung** (nur Aufträge)
    - **Lizenzbetrag Rückvergütungsverwaltung** (nur Aufträge)
    - **Betrag Kreditorenrückvergütung Rückvergütungsverwaltung** (Aufträge und Bestellungen)

1. Schließen Sie die Seite **Preisdetails**.
1. Wenn der Auftrag nicht für die gerade angezeigten Rückvergütungen in Frage kommt, führen Sie diese Schritte aus, um Rückvergütungen auszuschließen. (Allerdings würden Sie normalerweise Rückvergütungen nicht ausschließen.)

    1. Wählen Sie im Inforegister **Auftragspositionen** die entsprechende Position aus.
    1. Setzen Sie im Inforegister **Positionsdetails** in der Registerkarte **Preis und Rabatt** die Option **Von der Rückvergütungsverwaltung ausschließen** auf *Ja*. Diese Option gilt nicht für Bestellungen. Außerdem sind nur Debitorenrückvergütungen ausgeschlossen, wenn diese Option auf *Ja* gesetzt ist. Debitorenlizenzrückvergütungen und Kreditorenrückvergütungen gelten weiterhin.

1. Im Aktivitätsbereich wählen Sie auf der Registerkarte **Entnehmen und verpacken** in der Gruppe **Generieren** **Lieferschein buchen** aus.
1. Wählen Sie im Inforegister **Parameter** im Feld **Menge** *Alle* aus.
1. Wählen Sie **OK** aus.
1. Klicken Sie auf **Ja**, wenn Sie zum Bestätigen des Vorgangs aufgefordert werden.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** **Rechnung** aus.
1. Wählen Sie im Inforegister **Parameter** im Feld **Menge** *Alle* oder *Lieferschein* aus.
1. Wählen Sie **OK** aus.
1. Klicken Sie auf **Ja**, wenn Sie zum Bestätigen des Vorgangs aufgefordert werden.

## <a name="process-rebate-management-deals"></a><a name="process-deals"></a>Rückvergütungsverwaltungsdeals verarbeiten

Wenn Sie einen Deal verarbeiten, berechnet das System alle relevanten Rückvergütungen und Lizenzgebühren, die eingerichtet wurden. Nur ausgewählte Deals mit Berechnungsperioden, die zur Berechnung bereit sind und den Status *Aktiv* haben, werden verarbeitet. Nach Abschluss der Verarbeitung generiert das System eine Reihe von Transaktionen, die Sie überprüfen und anschließend buchen können.

> [!NOTE]
> In allen Fällen werden Rückvergütungen auf der Ebene verarbeitet, die in den einzelnen Deals unter der Einstellung **Abstimmen nach** festgelegt ist (*Deal* oder *Position*). Sie können Berechnungen mit nur einer Position nur für Deals durchführen, bei denen das Feld **Abstimmen nach** auf *Position* gesetzt ist.

### <a name="process-all-lines-for-one-or-more-deals"></a>Alle Positionen für einen oder mehrere Deals verarbeiten

1. Öffnen Sie die entsprechende [Listenseite mit den Rückvergütungsdeals](rebate-management-deals.md) für den Dealtyp, mit dem Sie arbeiten möchten.
1. Wählen Sie die Zeile für jeden Deal aus, den Sie verarbeiten möchten (oder öffnen Sie den Deal, den Sie verarbeiten möchten).
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rückvergütungsverwaltungsdeals** in der Gruppe **Generieren** einen der folgenden Befehle:

    - **Verarbeiten \> Rückstellung** – Stellen Sie für jeden relevanten Rückvergütungsdeal eine Reihe von Abgrenzungen bereit, ohne diese zu buchen. Dieser Menüpunkt ist nicht verfügbar für Abschlüsse, bei denen das Feld **Ausgangstermin** auf *Element* festgelegt ist.
    - **Verarbeiten \> Rückvergütungsverwaltung** – Verarbeiten Sie eine Reihe von Transaktionen, die den Wert der Rückvergütung für die einzelnen Deals angeben.
    - **Bearbeiten \> Abschreibung** – Verarbeiten Sie für jede Quelltransaktion für das Bonusgeschäft und die angegebene Periode die Abweichung zwischen den Beträgen, die für eine Rückstellung und für die Bonusverwaltung gebucht wurden. Dieser Menüpunkt ist nicht verfügbar für Abschlüsse, bei denen das Feld **Ausgangstermin** auf *Element* festgelegt ist.

1. Legen Sie im angezeigten Dialogfeld die Felder **Startdatum** und **Enddatum** den Datumsbereich für die Berechnung fest.
1. Wählen Sie zum Ausführen der Berechnung **OK** aus.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Eine oder mehrere spezifische Deal-Positionen für einen ausgewählten Deal verarbeiten

1. Öffnen Sie die entsprechende [Listenseite mit den Rückvergütungsdeals](rebate-management-deals.md) für den Dealtyp, mit dem Sie arbeiten möchten.
1. Öffnen Sie den Deal, dessen Position Sie verarbeiten möchten.
1. Wählen Sie die Registerkarte **Positionen** in der oberen rechten Ecke aus.
1. Wählen Sie im Inforegister **Rückvergütungsverwaltung** die Zeile jeder Deal-Position aus, die Sie verarbeiten möchten.
1. Wählen Sie auf der Symbolleiste des Inforegisters **Rückvergütungsverwaltung** einen der folgenden Befehle aus. (Diese Befehle sind nur für Deals verfügbar, bei denen das Feld **Abstimmen nach** auf *Position* gesetzt ist.)

    - **Verarbeiten \> Rückstellung** – Stellen Sie für jede relevanten Deal-Position eine Reihe von Abgrenzungen bereit, ohne diese zu buchen. Dieser Menüpunkt ist nicht verfügbar für Abschlüsse, bei denen das Feld **Ausgangstermin** auf *Element* festgelegt ist.
    - **Verarbeiten \> Rückvergütungsverwaltung** – Verarbeiten Sie eine Reihe von Transaktionen, die den Wert der Rückvergütung für die einzelnen Positionen angeben.
    - **Bearbeiten \> Abschreibung** – Verarbeiten Sie für jede Quelltransaktion für das Bonusgeschäft und die angegebene Periode die Abweichung zwischen den Beträgen, die für eine Rückstellung und für die Bonusverwaltung gebucht wurden. Dieser Menüpunkt ist nicht verfügbar für Abschlüsse, bei denen das Feld **Ausgangstermin** auf *Element* festgelegt ist. 

1. Legen Sie im angezeigten Dialogfeld die Felder **Startdatum** und **Enddatum** den Datumsbereich für die Berechnung fest.
1. Wählen Sie zum Ausführen der Berechnung **OK** aus.

### <a name="process-deals-using-a-batch-job"></a>Stapelverarbeitung von Deals

Anstatt bestimmte Deals oder Deal-Positionen zu verarbeiten, können Sie eine Stapelverarbeitung ausführen, um mehrere Deals gleichzeitig zu verarbeiten. Sie können optional Datensatzfilter anwenden und/oder einen wiederkehrenden Zeitplan einrichten. Führen Sie für eine Stapelverarbeitung von Deals die folgenden Schritte aus.

1. Führen Sie einen dieser Schritte aus:

    - Gehen Sie zu **Rückvergütungsverwaltung \> Periodische Aufgaben \> Verarbeiten \> Rückstellung**, eine Reihe von Abgrenzungen für jeden relevanten Deal bereitzustellen, ohne ihn jedoch zu buchen.
    - Gehen Sie zu **Rückvergütungsverwaltung \> Periodische Aufgaben \> Verarbeiten \> Rückvergütungsverwaltung**, um eine Reihe von Transaktionen zu verarbeiten, die den Wert der Rückvergütung für die einzelnen Deals bereitstellen.
    - Gehen Sie auf **Rückvergütungsverwaltung \> Periodische Aufgaben \> Verarbeiten \> Abschreiben**, um zuvor gebuchte Transaktionen zu stornieren, um sie abzuschreiben, damit neue Transaktionen mit Rückvergütungsdeals berechnet werden können.

1. Legen Sie im daraufhin angezeigten Dialogfeld im Inforegister **Parameter** im Abschnitt **Periode** das **Startdatum** und **Enddatum** fest, um den Datumsbereich für die Berechnung von Transaktionen festzulegen.
1. Legen Sie im Abschnitt **Garantieperiode** über die Felder **Startdatum** und **Enddatum** den Datumsbereich für die Berechnung von Garantien fest.
1. Im Inforegister **Einzuschließende Datensätze** können Sie Filter einrichten, um die Anzahl der Deals für die Stapelverarbeitung zu begrenzen. Diese Einstellungen funktionieren genauso wie für andere Arten von Stapelverarbeitungen.
1. Bei Bedarf können Sie im Inforegister **Im Hintergrund ausführen** Optionen für die Stapelverarbeitung und die Terminplanung einrichten. Diese Einstellungen funktionieren genauso wie für andere Arten von Stapelverarbeitungen.
1. Wählen Sie **OK**, um die Berechnung auszuführen und/oder zu planen.

### <a name="process-deals-by-using-the-rebate-workbench"></a>Deals mit der Rückvergütungsworkbench verarbeiten

Anstatt bestimmte Deals oder Deal-Positionen zu verarbeiten, können Sie mit der *Rückvergütungsworkbench* mehrere Deals gleichzeitig verarbeiten. Sie können optional Datensatzfilter anwenden und/oder einen wiederkehrenden Zeitplan einrichten. Sie müssen keine Zeilen auswählen. Das System verarbeitet alle Positionen, die die von Ihnen eingerichteten Datums- und Filteranforderungen erfüllen.

Gehen Sie wie folgt vor, um Deals mit der Rückvergütungsworkbench zu verarbeiten.

1. Gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsdeals \> Rückvergütungsworkbench**.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rückvergütungsverwaltungsworkbench** in der Gruppe **Verarbeitung** einen der folgenden Befehle:

    - **Verarbeiten \> Bereitstellung**: Stellen Sie für jede relevanten Deal-Position eine Reihe von Abgrenzungen bereit, buchen Sie sie aber nicht.
    - **Verarbeiten \> Rückvergütungsverwaltung** – Verarbeiten Sie eine Reihe von Transaktionen, die den Wert der Rückvergütung für die einzelnen Positionen angeben.
    - **Verarbeiten \> Abschreibung**: Verarbeiten Sie die Abweichung zwischen der Bereitstellung und der Rückvergütungsverwaltung, die für jede Quellentransaktion gebucht wurde nach dem Rückvergütungsdeal und dem jeweiligen Zeitraum.

1. Legen Sie im Dialogfeld **Rückvergütungsverwaltung** im Abschnitt **Zeitraum** das **Startdatum** und **Enddatum** fest, um den Datumsbereich für die Berechnung von Transaktionen festzulegen.
1. Legen Sie im Abschnitt **Garantiezeitraum** über die Felder **Startdatum** und **Enddatum** den Datumsbereich für die Berechnung von Garantien fest.
1. Im Inforegister **Einzuschließende Datensätze** können Sie Filter einrichten, um die Anzahl der Deals für die Stapelverarbeitung zu begrenzen. Diese Einstellungen funktionieren genauso wie für andere Arten von Stapelverarbeitungen.
1. Bei Bedarf können Sie im Inforegister **Im Hintergrund ausführen** Optionen für die Stapelverarbeitung und die Terminplanung einrichten. Diese Einstellungen funktionieren genauso wie für andere Arten von Stapelverarbeitungen.
1. Wählen Sie **OK**, um die Berechnung auszuführen und/oder zu planen.

## <a name="view-and-edit-rebate-management-transactions"></a>Rückvergütungsverwaltungstransaktionen überprüfen und bearbeiten

Wenn Sie einen oder mehrere Deals bearbeiten, erstellt das System Transaktionen, die Sie anzeigen und möglicherweise bearbeiten können, bevor Sie sie buchen.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-deals-list-page"></a>Rückvergütungsverwaltungstransaktionen mit der Listenseite mit den Rückvergütungsdeals anzeigen und bearbeiten

Um Rückvergütungsverwaltungstransaktionen mit der Listenseite mit den Rückvergütungsdeals anzuzeigen und zu bearbeiten, gehen Sie wie folgt vor.

1. Führen Sie einen dieser Schritte aus:

    - Wählen Sie den Deal aus, für den Transaktionen angezeigt werden sollen (z. B. auf der [Seite **Alle Rückvergütungsverwaltungsdeals**](rebate-management-deals.md)). Im Aktivitätsbereich der Registerkarte **Rückvergütungsverwaltungsdeals** wählen Sie in der Gruppe **Transaktionen** entweder **Transaktionen** oder **Garantietransaktionen** aus, abhängig von der Art der Transaktion, die Sie anzeigen möchten.
    - Öffnen Sie den Deal (z. B. auf der [Seite **Alle Rückvergütungsverwaltungsdeals**](rebate-management-deals.md)), um Details anzuzeigen. Wählen Sie im Inforegister **Rückvergütungsverwaltung** die Deal-Position aus, für die Sie Transaktionen anzeigen möchten. Wählen Sie dann in der Symbolleiste **Transaktionen** oder **Garantietransaktionen** aus, abhängig vom Typ der Transaktion, die Sie anzeigen möchten. (Diese Schaltflächen sind nur für Deals verfügbar, bei denen das Feld **Abstimmen nach** auf *Position* gesetzt ist.)

1. Die Seite **Rückvergütungsverwaltungs-Datumstransaktionen** oder **Rückvergütungsverwaltungs-Garantietransaktionen** erscheint. Sie enthält ein Raster, in dem jede Position für eine Reihe von Transaktionen aus einer einzelnen Rückvergütungs- oder Garantieperiode steht. Wählen Sie eine Zeile im Raster und dann im Aktivitätsbereich **Quellentransaktionen**, um die Transaktionen anzuzeigen, die zu dieser Zeile gehören.
1. Die angezeigte Seite zeigt eine Liste der Transaktionen des ausgewählten Typs, die zur ausgewählten Zeile gehören. Jede Transaktion enthält je nach Transaktionstyp relevante Details. Bei Garantietransaktionen können Sie die Liste nur anzeigen. Für andere Transaktionstypen können Sie auf dieser Seite die folgenden Aktionen ausführen:

    - Um den Gesamtwert aller beanspruchten Transaktionen auf der Seite zu überprüfen, gehen Sie zum Feld **Beanspruchter Betrag**.
    - Um weitere Informationen zu einer Transaktion anzuzeigen, wählen Sie diese aus und wählen Sie dann die Registerkarte **Allgemein**, **Finanzdimension** oder **Dimension** aus.
    - Um die zutreffenden Reduzierungen anzuzeigen, wählen Sie im Aktivitätsbereich **Reduzierungstransaktionen** aus. Weitere Informationen finden Sie unter [Prinzipien zur Rückvergütungsreduzierung](rebate-reduction-principle.md).
    - Um Transaktionen als beansprucht oder nicht beansprucht zu markieren, wenn Sie einen Anspruchsprozess verwenden, wählen Sie die entsprechenden Zeilen und dann im Aktivitätsbereich einen der folgenden Befehle aus. (Sie können Anspruchsprozesse auf der [Seite **Rückvergütungsverwaltungsparameter**](rebate-management-parameters.md) aktivieren.)

        - **Als beansprucht markieren \> Alle**: Markieren Sie alle Transaktionen als beansprucht.
        - **Als beansprucht markieren \> Ausgewählt**: Markieren Sie die ausgewählten Transaktionen als beansprucht.
        - **Als nicht beansprucht markieren \> Alle**: Markieren Sie alle Transaktionen als nicht beansprucht.
        - **Als nicht beansprucht markieren \> Ausgewählt**: Markieren Sie die ausgewählten Transaktionen als nicht beansprucht.

    - Wählen Sie **Abschreiben** im Aktionsbereich, um den Anspruch für alle relevanten Zeilen zu buchen. Wenn Sie einen Anspruchsprozess verwenden (wenn die Option **Anspruchsprozess verwenden** auf der Seite **Parameter für die Rückvergütungsverwaltung** aktiviert ist), werden nur die Zeilen gebucht, die als **Gefordert** markiert sind. Andernfalls werden alle Quelltransaktionen für die ausgewählte Bonus-Transaktion gebucht. Die Schaltfläche **Buchen** ist nur für Rabatt-Transaktionen verfügbar. Für Rückstellungs- und Ausbuchungstransaktionen ist sie nicht verfügbar. Im Dialogfeld **Buchen** werden die Felder **Von-Datum** und **Bis-Datum** automatisch festgelegt. Klicken Sie auf das Feld **Buchungsdatum** und dann **OK** aus.
    - Um den Betrag anzupassen, der für eine offene oder nicht gebuchte Transaktion angezeigt wird, wählen Sie die Transaktion aus und führen Sie einen der folgenden Schritte aus:

        - Bearbeiten Sie den Wert im Feld **Korrigierter Betrag**.
        - Wählen Sie im Aktivitätsbereich **Korrektur festlegen** aus. Geben Sie dann im Feld **Korrigierter Betrag** im angezeigten Dropdown-Dialogfeld einen Wert ein.

> [!NOTE]
> Wenn Sie einen Anspruchsprozess verwenden, enthält die Transaktionsliste bei der Verarbeitung der nächsten Periode alle nicht beanspruchten Transaktionen der vorherigen Buchung sowie alle neuen Transaktionen für die ausgewählte Periode.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-workbench"></a>Rückvergütungsverwaltungstransaktionen mit der Rückvergütungsworkbench anzeigen und bearbeiten

Um Rückvergütungsverwaltungstransaktionen mit der Rückvergütungsworkbench anzuzeigen und zu bearbeiten, gehen Sie wie folgt vor.

1. Gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsdeals \> Rückvergütungsworkbench**.
1. Legen Sie das Feld **Anzeigen** auf *Nicht gebucht* fest.
1. Die Seite **Rückvergütungsworkbench** zeigt eine Liste der Transaktionen an. Jede Transaktion enthält relevante Details. Diese Details variieren je nach Transaktionstyp. Sie können auf dieser Seite folgende Aktivitäten durchführen:

    - Um weitere Informationen zu einer Transaktion anzuzeigen, wählen Sie diese aus und wählen Sie dann die Registerkarte **Allgemein**, **Finanzdimension** oder **Dimension** aus.
    - Wenn Sie einen Anspruchsprozess verwenden, können Sie Transaktionen als beansprucht oder nicht beansprucht markieren. Wählen Sie die entsprechenden Zeilen und dann im Aktivitätsbereich auf der Registerkarte **Rückvergütungsverwaltungsworkbench** einen der folgenden Befehle aus. (Sie können Anspruchsprozesse auf der Seite [Rückvergütungsverwaltungsparameter **Rückvergütungsverwaltungsparameter**](rebate-management-parameters.md) aktivieren.)

        - **Als beansprucht markieren**: Markieren Sie die ausgewählten Transaktionen als beansprucht.
        - **Als nicht beansprucht markieren**: Markieren Sie die ausgewählten Transaktionen als nicht beansprucht.

    - Um den Anspruch für eine oder mehrere Positionen zu buchen, markieren Sie die entsprechenden Zeilen. Wählen Sie dann im Aktivitätsbereich auf die Registerkarte **Rückvergütungsworkbench** **Buchen** aus. Die Schaltfläche **Buchen** steht für Bereitstellungs-, Rückvergütungs- und Abschreibungstransaktionen zur Verfügung. Im Dialogfeld **Buchen** werden die Felder **Von-Datum** und **Bis-Datum** automatisch festgelegt. Klicken Sie auf das Feld **Buchungsdatum** und dann **OK** aus.
    - Um den Betrag anzupassen, der für eine offene oder nicht gebuchte Transaktion angezeigt wird, wählen Sie die Transaktion aus und führen Sie einen der folgenden Schritte aus:

        - Bearbeiten Sie den Wert im Feld **Korrigierter Betrag**.
        - Wählen Sie im Aktivitätsbereich auf die Registerkarte **Rückvergütungsworkbench** **Korrektur festlegen** aus. Geben Sie dann im Feld **Korrigierter Betrag** im angezeigten Dropdown-Dialogfeld einen Wert ein.

> [!NOTE]
> Wenn Sie einen Anspruchsprozess verwenden, enthält die Transaktionsliste bei der Verarbeitung der nächsten Periode alle nicht beanspruchten Transaktionen der vorherigen Buchung sowie alle neuen Transaktionen für die ausgewählte Periode.

## <a name="post-rebates-transactions"></a>Rückvergütungstransaktionen buchen

Um den Wert einer verarbeiteten Rückstellung, eines Rabattverwaltungsbetrags und einer Ausbuchung zu buchen, müssen Sie den Buchungsprozess ausführen. Der Buchungsprozess markiert die Rückstellungs-, Bonusverwaltungs- oder Abschreibungstransaktionen als gebucht und erstellt die Zieltransaktion. Wenn Sie die Zieltransaktion nicht überprüfen müssen, können Sie diese Transaktionen so festlegen, dass sie automatisch gebucht werden.

### <a name="set-up-the-system-to-post-all-target-transactions-automatically"></a>Festlegen, dass das System alle Zieltransaktionen automatisch bucht

Um Ihr System so einzurichten, dass alle Zieltransaktionen gebucht werden, sobald sie durch eine Buchungsvorschrift, einen Rabattverwaltungsbetrag und eine Abschreibung erzeugt werden, aktivieren Sie die Option **Erfassungen automatisch buchen** und/oder **Freitextrechnungen automatisch buchen** auf der Seite **Parameter der Rabattverwaltung**. Weitere Informationen finden Sie unter [Rückvergütungsverwaltungsparameter](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Alle Transaktionen für alle Positionen eines oder mehrerer Deals verarbeiten

Nachdem Sie die relevanten Geschäfte verarbeitet haben, folgen Sie diesen Schritten, um die generierten Transaktionen für alle Zeilen für ein oder mehrere Geschäfte zu überprüfen und zu buchen.

1. Öffnen Sie die entsprechende [Listenseite mit den Rückvergütungsdeals](rebate-management-deals.md) für den Dealtyp, mit dem Sie arbeiten möchten.
1. Wählen Sie die Zeile für jeden Deal aus, den Sie buchen möchten (oder öffnen Sie den Deal, den Sie buchen möchten).
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rückvergütungsverwaltungsdeals** in der Gruppe **Generieren** einen der folgenden Befehle:

    - **Buchen \> Rückstellung**: Buchen Sie verfügbare Abgrenzungstransaktionen, die Sie erstellt haben.
    - **Buchen \> Rückvergütungsverwaltung**: Buchen Sie verfügbare Rückvergütungstransaktionen, die Sie erstellt haben.
    - **Buchen \> Abschreibung**: Buchen Sie verfügbare Abschreibungstransaktionen, die Sie erstellt haben.

1. Legen Sie im angezeigten Dialogfeld das Feld **Buchungsdatum** fest. Legen Sie dann in den Feldern **Startdatum** und **Enddatum** den Datumsbereich für die zu buchende Transaktion fest.
1. Klicken Sie auf **OK**, um die Transaktionen zu buchen.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Transaktionen für eine oder mehrere spezifische Deal-Positionen für einen ausgewählten Deal buchen

Nachdem Sie die relevanten Geschäfte verarbeitet haben, führen Sie diese Schritte aus, um die generierten Transaktionen für eine oder mehrere bestimmte Zeilen für ein ausgewähltes Geschäft zu überprüfen und zu buchen. Dieses Verfahren ist nur für Geschäfte anwendbar, bei denen das Feld **Abstimmen nach** auf *Zeile* festgelegt ist.

1. Öffnen Sie die entsprechende [Listenseite mit den Rückvergütungsdeals](rebate-management-deals.md) für den Dealtyp, mit dem Sie arbeiten möchten.
1. Öffnen Sie den Deal mit einer Position, für die Sie Transaktionen buchen möchten.
1. Wählen Sie die Registerkarte **Positionen** in der oberen rechten Ecke aus.
1. Wählen Sie im Inforegister **Rückvergütungsverwaltung** die Zeile jeder Deal-Position aus, die Sie buchen möchten.
1. Wählen Sie auf der Symbolleiste des Inforegisters **Rückvergütungsverwaltung** einen der folgenden Befehle aus. (Diese Befehle sind nur für Deals verfügbar, bei denen **Abstimmen nach** auf *Position* gesetzt ist.)

    - **Buchen \> Rückstellung**: Buchen Sie verfügbare Abgrenzungstransaktionen, die Sie erstellt haben.
    - **Buchen \> Rückvergütungsverwaltung**: Buchen Sie verfügbare Rückvergütungstransaktionen, die Sie erstellt haben.
    - **Buchen \> Abschreibung**: Buchen Sie verfügbare Abschreibungstransaktionen, die Sie erstellt haben.

1. Legen Sie im angezeigten Dialogfeld das Feld **Buchungsdatum** fest. Legen Sie dann in den Feldern **Startdatum** und **Enddatum** den Datumsbereich für die zu buchende Transaktion fest.
1. Klicken Sie auf **OK**, um die Transaktionen zu buchen.

### <a name="post-transactions-using-a-batch-job"></a>Transaktionen als Stapelverarbeitung buchen

Anstatt bestimmte Transaktionen für spezifische Deals oder Deal-Positionen zu buchen, können Sie eine Stapelverarbeitung ausführen, um Transaktionen für mehrere Deals gleichzeitig zu buchen. Sie können optional Datensatzfilter anwenden und/oder einen wiederkehrenden Zeitplan einrichten. Führen Sie für eine Stapelverarbeitung von Transaktionsbuchungen die folgenden Schritte aus.

1. Führen Sie einen dieser Schritte aus:

    - Gehen Sie zu **Rückvergütungsverwaltung \> Periodische Aufgaben \> Buchen \> Rückstellung**, um verfügbare Abgrenzungstransaktionen zu buchen, die Sie erstellt haben.
    - Gehen Sie zu **Rückvergütungsverwaltung \> Periodische Aufgaben \> Buchen \> Rückvergütungsverwaltung**, um verfügbare Rückvergütungstransaktionen zu buchen, die Sie erstellt haben.
    - Gehen Sie zu **Rückvergütungsverwaltung \> Periodische Aufgaben \> Buchen \> Abschreibung**, um verfügbare Abschreibungstransaktionen zu buchen, die Sie erstellt haben.

1. Im daraufhin im Inforegister **Parameter** angezeigten Dialogfeld im Abschnitt **Periode** legen Sie das Feld **Buchungsdatum** fest. Legen Sie dann in den Feldern **Startdatum** und **Enddatum** den Datumsbereich für die zu buchende Transaktion fest.
1. Legen Sie im Abschnitt **Garantieperiode** über die Felder **Startdatum** und **Enddatum** den Datumsbereich für die zu buchenden Garantien fest.
1. Im Inforegister **Einzuschließende Datensätze** können Sie Filter einrichten, um die Anzahl der Deals für die Stapelverarbeitung zu begrenzen. Diese Einstellungen funktionieren genauso wie für andere Arten von Stapelverarbeitungen.
1. Bei Bedarf können Sie im Inforegister **Im Hintergrund ausführen** Optionen für die Stapelverarbeitung und die Terminplanung einrichten. Diese Einstellungen funktionieren genauso wie für andere Arten von Stapelverarbeitungen.
1. Wählen Sie **OK**, um die Berechnung auszuführen und/oder zu planen.

### <a name="post-transactions-by-using-the-rebate-workbench"></a>Transaktionen mit der Rückvergütungsworkbench buchen

Nachdem Sie Bereitstellungs-, Rückvergütungs- oder Abschreibungstransaktionen verarbeitet haben, führen Sie diese Schritte aus, um die Rückvergütungsworkbench zum Überprüfen und Buchen der generierten Transaktionen für eine oder mehrere spezifische Transaktionspositionen für alle Deals zu verwenden.

1. Gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsdeals \> Rückvergütungsworkbench**.
1. Aktivieren Sie im Raster das Kontrollkästchen für jede Zeile, die Sie buchen möchten. Sie können ungebuchte Bereitstellungs-, Rückvergütungs- und/oder Abschreibungstransaktionen auswählen. Dabei gelten folgende Regeln:

    - Das System bucht alle Positionen, die den gleichen Wert für die **Rückvergütungstransaktionsnummer** haben, wie die von Ihnen ausgewählten Positionen.
    - Das System bucht keine Position als Transaktionstyp *Rückvergütung*, die nicht als beansprucht gekennzeichnet sind.
    - Wenn Sie bereits gebuchte Positionen markieren, überspringt das System die gebuchten Positionen.
    - Die Schaltfläche **Buchen** ist nur verfügbar, wenn Sie mindestens eine nicht gebuchte Position auswählen.

1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Rückvergütungsworkbench** in der Gruppe **Verarbeiten** auf **Buchen**.
1. Legen Sie im Dialogfeld **Buchen** das Feld **Buchungsdatum** fest. Das Feld **Startdatum** und **Enddatum** werden automatisch festgesetzt, basierend auf dem frühesten **Startdatum** dem spätesten **Enddatum** für die ausgewählten Positionen.
1. Klicken Sie auf **OK**, um die Transaktionen zu buchen.

## <a name="review-rebate-management-journals"></a><a name="review-journals"></a>Erfassungen der Rückvergütungsverwaltung überprüfen

Nachdem Ihre Transaktionen gebucht wurden, können Sie die resultierenden Erfassungen, Dokumente oder Artikel überprüfen. Zieltransaktionen für Rückvergütungen und Lizenzgebühren basieren auf der Zahlungsart, die im Buchungsprofil festgelegt ist, und der Ausgabeart der Rückvergütung. Wenn z. B. der Rabattausgang auf *Element* festgelegt ist, wird ein Verkaufsauftrag für einen Debitor-Rabatt und eine Bestellung für einen Kreditor-Rabatt erstellt. Diese Aufträge können über die Zieltransaktionen eingesehen werden. Wenn für die Zahlung dagegen Kreditorenkonten verwendet werden sollen, wird für Debitorenrückvergütungen alternativ eine Kreditorenrechnung für den Kreditor erstellt, der für den Debitor eingestellt wurde.

### <a name="review-journals-by-using-the-rebate-deals-list-page"></a>Erfassungen Listenseite mit den Rückvergütungsdeals überprüfen

Führen Sie die folgenden Schritte aus, um die Journaleinträge zu überprüfen, die mit einem Deal zur Rückvergütungsverwaltung verknüpft sind.

1. Öffnen Sie die entsprechende [Listenseite mit den Rückvergütungsdeals](rebate-management-deals.md) für den Dealtyp, mit dem Sie arbeiten möchten.
1. Wählen Sie den Deal aus, für den Journaleinträge überprüft werden sollen.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Rabattverwaltungsgeschäfte** in der Gruppe **Transaktionen** entweder **Transaktionen** oder **Garantietransaktionen**, je nachdem, welche Art von Transaktionen Sie sich ansehen möchten.
1. Legen Sie das Feld **Anzeigen** auf *Alle* oder *Gebucht* fest.
1. Suchen Sie die Transaktionssammlung, die Sie untersuchen möchten, und wählen Sie sie aus. Wählen Sie dann im Aktivitätsbereich eine der folgenden Schaltflächen aus. (Diese Schaltflächen sind nur verfügbar, wenn relevante Buchungen für die ausgewählte Transaktionssammlung vorhanden sind.)

    - **Zieltransaktionen**: Überprüfen Sie relevante Erfassungen und andere Dokumententypen, die durch den ausgewählten Deal generiert wurden.
    - **Elemente** – Überprüfen Sie relevante Verkaufsaufträge oder Bestellungen, die durch das ausgewählte Geschäft erzeugt wurden.

1. Eine Liste relevanter Erfassungen, Dokumente oder Artikel wird angezeigt. Um weitere Informationen zu einer Erfassung, einem Dokument oder Artikel anzuzeigen, wählen Sie dessen Zeile und dann im Aktivitätsbereich die Option **Details anzeigen**.

### <a name="review-journals-by-using-the-rebate-workbench"></a>Erfassungen mit der Rückvergütungsworkbench überprüfen

Gehen Sie wie folgt vor, um Erfassungen mit der Rückvergütungsworkbench zu überprüfen.

1. Gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsdeals \> Rückvergütungsworkbench**.
1. Legen Sie das Feld **Anzeigen** auf _Alle_ oder _Gebucht_ fest.
1. Suchen Sie die Position, die Sie überprüfen möchten, und wählen Sie sie aus. Klicken Sie dann im Aktivitätsbereich auf der Registerkarte **Rückvergütungsworkbench** in der Gruppe **Anzeigen** auf **Zieltransaktionen**. Diese Schaltfläche ist nur verfügbar, wenn für die ausgewählte Position relevante Buchungen vorhanden sind.
1. Eine Liste relevanter Erfassungen, Dokumente oder Artikel wird angezeigt. Um weitere Informationen zu einer Erfassung, einem Dokument oder Artikel anzuzeigen, wählen Sie dessen Zeile und dann im Aktivitätsbereich die Option **Details anzeigen**.

## <a name="rebate-management-transactions-on-the-deduction-workbench"></a>Rückvergütungsverwaltungstransaktionen auf der Abzugsworkbench

Wenn Sie eine Rückvergütungsverwaltungstransaktion buchen, die eine der folgenden **Zahlungstypen** hat, erstellt das System eine Debitorenabzugserfassung oder eine Freitextrechnung für das entsprechende Debitorenkonto:

- Debitorenabzüge
- Steuerrechnungs-Debitorabzüge
- Handelsausgaben
- Bericht

Nachdem eine Zieltransaktion erstellt und gebucht wurde, steht sie als offene Transaktion auf der Seite **Abzugsworkbench** zur Verfügung (**Vertrieb und Marketing \> Handelsvergütungen \> Abzüge \> Abzugsworkbench**). Bei offenen Transaktionen lautet der Wert **Anspruchstyp** *Rückvergütungsverwaltung* und der Wert **Rückvergütungstransaktionsnummer** ist verfügbar, um die Rückverfolgbarkeit zu ermöglichen. Das Datum wird auf das Buchungsdatum der Rückvergütungsverwaltungs-Zieltransaktion gesetzt. Um die Abzugsworkbench zu verwenden, um offene Transaktionen mit bestehenden Abzügen für dasselbe Debitorenkonto auszugleichen, wählen Sie im Aktivitätsbereich **Verwalten \> Abgleichen**.

Weitere Informationen finden Sie unter [Verwalten von Abzügen mit der Abzugsworkbench](deduction-workbench.md).

## <a name="purge-unposted-transactions"></a>Nicht gebuchte Transaktionen löschen

Nachdem Sie Bereitstellungs-, Rückvergütungs- oder Abschreibungstransaktionen verarbeitet haben, führen Sie diese Schritte aus, um ausgewählte nicht gebuchte Transaktionen zu löschen.

1. Gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsdeals \> Rückvergütungsworkbench**.
2. Legen Sie das Feld **Anzeigen** auf *Nicht gebucht* fest.
3. Suchen und wählen Sie die zu löschenden Transaktionen aus. Klicken Sie dann im Aktivitätsbereich auf der Registerkarte **Rückvergütungsworkbench** in der Gruppe **Verarbeiten** auf **Löschen**.
4. Wählen Sie **OK**, um die nicht gebuchten Transaktionen zu löschen.

## <a name="cancel-a-posted-provision"></a>Eine gebuchte Bereitstellung abbrechen

Nachdem Sie eine Bereitstellung verarbeitet und gebucht haben, führen Sie diese Schritte aus, um die gebuchten Bereitstellungstransaktionen abzubrechen.

1. Gehen Sie zu **Rückvergütungsverwaltung \> Rückvergütungsverwaltungsdeals \> Rückvergütungsworkbench**.
2. Legen Sie das Feld **Anzeigen** auf *Gebucht* fest.
3. Suchen und wählen Sie die abzubrechenden Bereitstellungstransaktionen aus. Klicken Sie dann im Aktivitätsbereich auf der Registerkarte **Rückvergütungsworkbench** in der Gruppe **Verarbeiten** auf **Bereitstellung abbrechen**.
4. Klicken Sie auf **OK**, um die Transaktionen zurückzubuchen.

Diese Bereitstellungsrückbuchungen werden auch in den entsprechenden [Rückvergütungsverwaltungserfassungen](#review-journals) sichtbar.
