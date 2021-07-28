---
title: TDS-Zahlungen an TDS-Behördenkreditoren abrechnen und TDS-Challan generieren
description: In diesem Thema wird erläutert, wie Zahlungen der Quellenbesteuerung (TDS) an TDS-Behördenkreditoren abgerechnet werden.
author: kailiang
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: a9912151ef9fc68941858545e39bccc1e5d3e411
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358313"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a>TDS-Zahlungen an TDS-Behördenkreditoren abrechnen und TDS-Challan generieren

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Zahlungen der Quellenbesteuerung (TDS) an TDS-Behördenkreditoren abgerechnet werden.

1. Gehen Sie zu **Kreditorenkonten \> Zahlungen \> Kreditorenzahlungserfassung**.

    [![Seite „Kreditorenzahlungserfassung“.](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)

2. Wählen Sie auf der Seite **Kreditorenzahlungserfassung** **Neu** aus, um eine Erfassungsposition zu erstellen.
3. Wählen Sie im Feld **Konto** einen TDS-Behördenkreditor aus, gegenüber dem Sie die TDS-Zahlung abrechnen möchten.
4. Wählen Sie **Ausgleichsbuchung**, um die Seite **Ausgleichsbuchungen** zu öffnen, auf der Sie die abgewickelten TDS-Buchungen für den TDS-Behördenkreditor anzeigen können.

    Die abgewickelten TDS-Buchungen für einen Ausgleichsperiode werden folgendermaßen angezeigt:

    - TDS-Buchungen, bei denen die Steuerschuldnerkategorie **Unternehmen** lautet, werden als eine Buchungsposition angezeigt.
    - TDS-Buchungen, bei denen es sich Steuerschuldnerkategorie **HUF**, **Firma**, **Einzelperson**, **AOP**, **BOI**, **Gemeinde** oder **Andere** lautet, werden als eine Buchungsposition angezeigt.
    - Das Feld **Betrag** zeigt den gesamten TDS-Betrag an, der an den TDS-Behördenkreditor zu zahlen ist.

5. Wählen Sie **Quellensteuerbuchungen** aus, um die verschiedenen TDS-Buchungen anzuzeigen, die für den Abrechnungsdatensatz enthalten sind. Auf dieser Seite können Sie die Aufteilung jeder TDS-Buchungen anzeigen, die im Ausgleichsperiode in den Ausgleichsprozess einbezogen wurde.
6. Auf der Registerkarte **Übersicht** kreuzen Sie das Kontrollkästchen **Markieren** bei den TDS-Buchungen an, die gegenüber dem TDS-Behördenkreditor abgerechnet werden sollen.

    Die Registerkarte **Übersicht** zeigt die folgenden Informationen für jede offene TDS-Buchung an:

    - **Datum**: Das Datum der TDS-Buchung.
    - **Beleg**: Die Belegnummer.
    - **Quelle**: Das Modul, in dem die TDS-Buchung gebucht wird.
    - **Kreditor/Debitor**: Die Nummer des Kreditoren- bzw. Debitorenkontos, von der die TDS abgezogen wird.
    - **Name des Steuerpflichtigen/der Partei**: Der Name des Kreditors bzw. Debitors, von dem die TDS abgezogen wird.
    - **Art des Steuerschuldners**: Die Steuerschuldnerkategorie, zu der Steuerpflichtige gehört.
    - **Betrag**: Der Rechnungsbetrag, auf dessen Grundlage die TDS berechnet wurde.
    - **Steuerbetrag**: Der TDS-Betrag, der für die Buchung berechnet wurde.

    > [!NOTE]
    > Deaktivieren Sie das Kontrollkästchen **Markieren** für alle TDS-Buchungen, die nicht gegenüber dem TDS-Behördenkreditor abgerechnet werden sollen.

    Auf der Registerkarte **Allgemein** ist im Feld **PAN** Permanente Kontonummer (PAN) des Steuerpflichtigen angegeben. Im Feld **Datum** ist das Datum der TDS-Berechnung und im Feld **Wert** der Gesamtprozentsatz angegeben, der für die TDS-Berechnung verwendet wurde.

7. Wählen Sie **Belege**, um die Belegeinträge für die TDS-Buchung anzuzeigen.
8. Schließen Sie die Seite.
10. Wählen Sie **Quellensteuerkomponenten**, um die Seite **Quellensteuerkomponenten** zu öffnen, auf der die TDS angezeigt wird, die pro TDS-Steuerkomponente für einen bestimmten TDS-Steuercode berechnet wurde.

    In der Registerkarte **Übersicht** wird im Feld **Steuerkomponente** die TDS-Steuerkomponente angezeigt, die für die Buchung verwendet wurde. Das Feld **Betrag** zeigt den TDS-Betrag in der Basiswährung an, der für die TDS-Steuerkomponente berechnet wurde. Das Feld **Kumulierter Betrag** zeigt den TDS-Gesamtbetrag an, der für die TDS-Steuerkomponente für alle ausgeglichenen Buchungen berechnet wurde.

    Auf der Registerkarte **Betrag** wird im Abschnitt **Standardwährung** der TDS-Betrag in der Standardswährung angegeben, der für die TDS-Steuerkomponente berechnet wurde. Der Abschnitt **Alternative Währung** zeigt den Betrag in der alternativen Währung an.

11. Schließen Sie die Seite **Quellensteuerkomponenten**.
12. Beachten Sie, dass auf der Seite **Bearbeiten offener Posten** im Feld **Betrag** der Gesamtbetrag, der in der Ausgleichsperiode gegenüber dem TDS-Behördenkreditor ausgeglichen werden soll, aktualisiert ist.
13. Um die TDS-Buchungen verschiedener TDS-Ausgleichsperioden an den TDS-Behördenkreditor auszugleichen, aktivieren Sie das Kontrollkästchen **Markieren** der Buchungen.
14. Schließen Sie die Seite **Bearbeiten offener Posten**.

    > [!NOTE]
    > Wenn nur wenige Buchungen zum Ausgleich auf der Seite **Quellensteuerbuchungen** ausgewählt sind, wird der TDS-Gesamtbetrag der ausgewählten Buchungen im Feld **Korrektur** auf der Seite **Bearbeiten offener Posten** aktualisiert. Der Korrekturbetrag wird im Erfassungsposten auf der Seite **Alle Journale** aktualisiert. Die Seite **Bearbeiten offener Posten** wird geschlossen.

    Auf der Seite **Alle Journale** zeigt das Feld **Soll** den Gesamtbetrag an, der an den TDS-Behördenkreditor zu zahlen ist.

15. Geben Sie die Daten des Gegenkontos ein.

    > [!NOTE]
    > Wenn TDS-Buchungen unterschiedliche Steuerkontonummern (TAN) haben, werden Erfassungsposten pro TAN auf der Seite **Alle Journale** erstellt.

16. Auf der Registerkarte **Zahlungsgebühr** wählen Sie im Feld **Gebührenkennung** eine Gebührenkennung mit dem Gebührentyp **Zinsen** oder **Andere** aus, um die Zahlungsgebühr für verspätete Zahlungen an den TDS-Behördenkreditor zu berechnen.

    Auf der Registerkarte **Steuerliche Angaben** ist im Abschnitt **Unternehmensdaten** im Feld **Name** der Name des Unternehmens angegeben. Im Abschnitt **Quellensteuer** enthält das Feld **Steuerkontonummer (TAN)** die TAN an, die mit der Buchungsposition verknüpft ist.

17. Prüfen und buchen Sie die Erfassung.
18. Wählen Sie **Quellensteuer \> Challan-Informationen**, um die Challan-Details für die Buchung einzugeben.

    Das Feld **Beleg** zeigt die Belegnummer der Buchung an.
    
19. Aktivieren Sie das Kontrollkästchen **TDS durch Buchungsposten eingezahlt**, wenn der TDS-Betrag mithilfe des Buchungspostens eingezahlt wird.
20. Geben Sie im Feld **Challan-Nummer** die Challan-Nummer ein, mit der die Zahlung an den TDS-Behördenkreditor erfolgt.
21. Geben Sie im Feld **Datum** das Challan-Datum ein.
22. Geben Sie im Feld **Bankname** den Namen der Bank aus, bei der der an den TDS-Behördenkreditor zu zahlende TDS-Betrag eingezahlt werden soll. In diesem Feld werden alle Bankkonten aufgelistet, die für den TDS-Behördenkreditor unter **Kreditorenkonten \> Alle Kreditoren \> Einstellungen \> Bankkonten** eingerichtet wurden.
23. Geben Sie im Feld **BSR-Code** den BSR-Code (Basic Statistical Return) der Bank ein.
24. Schließen Sie die Seite.

### <a name="example"></a>Beispiel

Der Zeitraum 01.04.2009 wird für die TDS-Komponentengrupe **Miete** mithilfe des periodischen TDS-Ausgleichsprozesses ausgeglichen. Der TDS-Gesamtbetrag von 141.625,00 wird für die TDS-Ausgleichsperiode auf das Konto des TDS-Behördenkreditors gebucht. Sie können sich diesen Betrag im Feld **Betrag** auf der Seite **Bearbeiten offener Posten** für den TDS-Behördenkreditor anzeigen lassen.

Wenn Sie **Quellensteuerbuchungen** auswählen, um die verschiedenen TDS-Buchungen anzuzeigen, die für den Zeitraum ausgeglichen wurden, werden die folgenden Informationen angezeigt.

| TDS-Betrag |
|------------|
| 16,995.00  |
| 22,660.00  |
| 28,325.00  |
| 16,995.00  |
| 28,325.00  |
| 16,995.00  |
| 11,330.00  |

Wählen Sie für einen spezifischen TDS-Betrag **Quellensteuerkomponenten** aus, um sich die TDS anzeigen zu lassen, die pro TDS-Steuerkomponente für einen bestimmten TDS-Steuercode berechnet wurde. Wählen Sie in diesem Beispiel **Quellensteuerkomponenten** für den TDS-Betrag 16.995,00 aus. Der Steuerbetrag, der pro Komponente für die Buchung berechnet wurde, wird angezeigt.

| MwSt.-Komponente | Dauer    | Kumulierter Betrag |
|---------------|-----------|--------------------|
| TDS           | 1,5000.00 | 125,000.00         |
| Zuschlag     | 1,500.00  | 12,500.00          |
| PE-Sondersteuer       | 330.00    | 2,750.00           |
| SHE-Sondersteuer      | 165.00    | 1,375.00           |

Wenn Sie auf der Seite **Quellensteuerbuchungen** nur die TDS-Beträge 16.995,00, 22.660,00 und 28.325,00 ausgewählt haben, wird der Gesamtbetrag für den Ausgleich als **67.980,00** im Feld **Korrektur** auf der Seite **Bearbeiten offener Posten** angezeigt. Wenn diese Buchung zum Ausgleich markiert ist und die Seite **Bearbeiten offener Posten** geschlossen wird, wird der Betrag von **67.980,00** im Feld **Soll** auf der Seite **Alle Journale** angezeigt.

Sie können jetzt die Erfassung buchen und das TDS-Challan generieren.

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a>Anpassung von Anzahlungen an TDS-Behördenkreditoren

Um eine Anzahlung an den TDS-Behördenkreditor an eine tatsächliche Zahlung anzupassen, gehen Sie zu **Kreditorenkonten \> Kreditoren \> Alle Kreditoren \> Buchungen bearbeiten**. Wenn die tatsächlich geleistete Zahlung die Anzahlung übersteigt, werden zwei Challan-Nummern für die Buchung generiert. In der TDS-Anfrage wird jedoch nur die erste Challan-Nummer angezeigt.
