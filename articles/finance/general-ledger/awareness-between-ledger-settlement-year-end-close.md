---
title: Unterschied zwischen Sachkontoausgleich und Jahresendabschluss
description: In diesem Thema finden Sie Informationen zu Verbesserungen, die sich auf Hauptbuchabrechnungen und den Jahresabschluss des Hauptbuchs auswirken.
author: kweekley
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: acfbcf1467363262769884063efbc1a6d6e21eb1
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075572"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Unterschied zwischen Sachkontoausgleich und Jahresendabschluss

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In Microsoft Dynamics 365 Finance Version 10.0.25 ist die Funktion **Zwischen Ledgerabrechnung und Jahresabschluss unterscheiden** im Arbeitsbereich **Funktionsverwaltung** verfügbar. Mit dieser Funktion werden zwei wesentliche Verbesserungen vorgenommen, die sich auf die Abrechnung des Sachkontos und den Jahresabschluss des Hauptbuchs auswirken.

Während des Hauptbuch-Jahresabschlusses werden abgerechnete Transaktionen des Hauptbuchs nicht mehr in der Eröffnungsbilanz des nächsten Geschäftsjahres berücksichtigt. Diese Erweiterung stellt sicher, dass nur nicht abgerechnete Transaktionen des Sachkontos in die Eröffnungsbilanz aufgenommen werden. Es ist wichtig, wenn die Neubewertung von Fremdwährungen im Hauptbuch ausgeführt wird. Die Neubewertung von Fremdwährungen wird nur für Transaktionen im Sachkonto ausgeführt, die den Status **Nicht erledigt** haben. Bevor jedoch die Funktion **Zwischen Sachkontoabrechnung und Jahresabschluss** freigegeben wurde, wurden in der Eröffnungsbilanz sowohl Transaktionen mit dem Status **abgerechnet** als auch solche mit dem Status **nicht abgerechnet** zusammengefasst, und der Status des zusammengefassten Betrags wurde auf **nicht abgerechnet** festgelegt.

Mit der zweiten Erweiterung können Sie während des Hauptbuch-Jahresabschlusses detaillierte Transaktionen der Eröffnungsbilanz buchen. Wenn die Option **Details beim Jahresabschluss beibehalten** auf **Ja** festgelegt ist, wird für jede nicht abgerechnete Transaktion des Sachkontos eine separate Eröffnungsbilanz erstellt. Diese Einstellung wird für jedes Hauptkonto in der Einrichtung der Sachkontenabrechnung festgelegt. Indem Sie detaillierte Transaktionen für die Eröffnungsbilanz aufbewahren, verbessern Sie die Möglichkeit, die noch nicht abgerechneten Transaktionen des Sachkontos im nächsten Geschäftsjahr abzurechnen, erheblich.

Um die neuen Erweiterungen zu unterstützen, wurden Änderungen an der Sachkontoabrechnung und dem Jahresabschluss vorgenommen.

### <a name="changes-to-ledger-settlement"></a>Änderungen an der Sachkontoabrechnung

- Die Abrechnung des Sachkontos muss innerhalb eines Geschäftsjahres erfolgen.
- Für Transaktionen auf einem einzigen Sachkonto muss die Sachkonto-Abrechnung durchgeführt werden. Das Hauptkonto ist jetzt ein erforderlicher Filter auf der Seite **Sachkonto-Abrechnung**.
- Die Sachkonto-Abrechnung und die Stornierung der Sachkonto-Abrechnung können nicht für Transaktionen durchgeführt werden, die innerhalb eines abgeschlossenen Geschäftsjahres gebucht werden (mit anderen Worten, der Jahresabschluss wurde ausgeführt).

### <a name="changes-to-year-end-close"></a>Änderungen am Jahresabschluß

- Ein Jahresabschluss kann nicht rückgängig gemacht werden, wenn Transaktionen in der Eröffnungsbilanz im nächsten Geschäftsjahr beglichen wurden. Diese Änderung gilt, wenn ein Jahresabschluss rückgängig gemacht wird oder wenn ein Jahresabschluss erneut durchgeführt wird und die Option **Bestehende Jahresendbuchungen bei erneutem Jahresabschluss löschen** in den Parametern des Hauptbuchs auf **Ja** festgelegt ist.
- Wenn die Option **Details beim Jahresabschluss beibehalten** für ein beliebiges Bilanzkonto in der Sachkontoabrechnung auf **Ja** festgelegt ist, werden für dieses Hauptkonto detailliertere Eröffnungsbilanztransaktionen erstellt.

## <a name="before-you-enable-the-feature"></a>Bevor Sie die Funktion aktivieren

Aufgrund der Änderungen in der Funktionalität und im Datenmodell ist es wichtig, dass Sie die folgenden Punkte berücksichtigen, bevor Sie die Funktion aktivieren:

- Alle Transaktionen, die für die Abrechnung markiert sind, aber noch nicht abgerechnet wurden, werden automatisch entmarkiert, wenn die Funktion aktiviert ist. Um Arbeitsverluste zu vermeiden, rechnen Sie alle markierten Transaktionen ab, bevor Sie die Funktion aktivieren.
- Einige Organisationen führen den Jahresabschluss mehrfach für dasselbe Geschäftsjahr aus. Aktivieren Sie die Funktion nicht, wenn der Jahresabschluss bereits einmal ausgeführt wurde und für dasselbe Geschäftsjahr erneut ausgeführt werden soll. Die Funktion muss aktiviert werden, bevor Sie den ersten Jahresabschluss verarbeiten oder nachdem Sie den letzten Jahresabschluss für das Geschäftsjahr verarbeitet haben.

  Wenn Sie die Funktion aktivieren möchten, aber der Jahresabschluss bereits einmal ausgeführt wurde, müssen Sie den Jahresabschluss rückgängig machen, bevor Sie die Funktion aktivieren können.

- Da die Abrechnung über mehrere Geschäftsjahre hinweg nicht mehr zulässig ist, empfehlen wir Ihnen, die Funktion zu aktivieren, bevor Sie mit dem Jahresabschluss beginnen. Um sicherzustellen, dass die Eröffnungssalden des nächsten Geschäftsjahres nicht durch frühere geschäftsjahresübergreifende Abrechnungen beeinflusst werden, sollte die Transaktion für den Eröffnungssaldo für das abzuschließende Geschäftsjahr abgerechnet werden.
- Da die Abrechnung über Hauptkonten hinweg nicht mehr zulässig ist, passen Sie Ihren Kontenplan oder Ihre Prozesse nach Bedarf an, um sicherzustellen, dass die Sachkontoabrechnung über dasselbe Hauptkonto erfolgen kann.
- Die Funktion kann nicht aktiviert werden, wenn der Jahresabschluss für den öffentlichen Sektor verwendet wird.

## <a name="set-up-ledger-settlement"></a>Sachkontoabrechnung festlegen

Nachdem Sie die Funktion aktiviert haben und bevor Sie den nächsten Jahresabschluss ausführen, muss jedes Unternehmen festlegen, ob es die Details der Transaktionen während des Jahresabschlusses beibehalten will. Die Auswahl hat keine Auswirkung auf Eröffnungsbilanzbuchungen aus früheren Jahresabschlussprozessen.

Die Option **Details während des Jahresabschlusses beibehalten** wird für jedes Hauptkonto auf der Seite **Sachkontoabrechnung einrichten** festgelegt.

1.  Gehen Sie zu **Hauptbuch** > **Hauptbuch-Einrichtung** > **Hauptbuch-Parameter**.
2.  Auf der Registerkarte **Sachkontoabrechnungen** wählen Sie **Sachkontoabrechnungen**.

– oder –

1.  Gehen Sie zu **Hauptbuch** > **Periodische Aufgaben** > **Sachkonto Abrechnungen**.
2.  Wählen Sie **Sachkonten abrechnen**.

Auf der Seite **Sachkontoabrechnungen** wurden zwei Spalten hinzugefügt:
    
- **Hauptkontotyp** - Diese Spalte dient nur zu Informationszwecken. Sie zeigt den Typ an, der dem Hauptkonto zugewiesen ist.
- **Details während des Jahresabschlusses beibehalten** - Standardmäßig ist die Option auf **Nein** festgelegt. Es kann nur auf **Ja** festgelegt werden, wenn der Wert in der Spalte **Hauptkontotyp** **Bilanz**, **Vermögen** oder **Haftung** lautet. Wenn die Option auf **Nein** festgelegt ist, werden die Eröffnungssalden in einer Zusammenfassung gebucht, wie es beim Jahresabschluss üblich ist. Wenn es auf **Ja** festgelegt ist, werden Eröffnungssalden im Detail für jede Transaktion des Sachkontos erstellt, die nicht für das Hauptkonto abgerechnet wird.

## <a name="year-end-close"></a>Jahresabschluss

Wenn Sie den Jahresabschluss ausführen, indem Sie auf **Hauptbuch** > **Periodenabschluss** > **Jahresabschluss** gehen, erstellt der Prozess die Eröffnungssalden für die Hauptkonten, die für die Sachkontoverrechnung definiert sind. Die Eröffnungssalden werden je nach Einrichtung der Sachkontenabrechnung entweder als Zusammenfassung oder als Detail erstellt. Der Prozess schließt abgerechnete Sachkonto-Transaktionen aus, unabhängig davon, ob Sie den Eröffnungssaldo für jedes Hauptkonto in einer Zusammenfassung oder im Detail buchen.

Zum Beispiel werden im Geschäftsjahr 2021 mehrere Transaktionen auf das Hauptkonto 130100 gebucht.

| Lfd. Nr. | Beleg  | Datum       | Typ      | Sachkonto | Kontoname        | Description       | Währung | Betrag in Buchungswährung | Betrag  | Betrag in Berichtswährung |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 3.12.2021  | Benutzung | 130100-001-    | Debitorenkonten | Servicegebühr       | USD      | 100                            | 100     | 100                          |
| 20855          | FTV-3004 | 05.12.2021  | Benutzung | 130100-002-    | Debitorenkonten | Dienstprogramme         | USD      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 16.12.2021 | Benutzung | 130100-001-    | Debitorenkonten | Rückerstattung            | USD      | -100                           | -100    | -100                         |
| 20851          | ARP-8000 | 20.12.2021 | Benutzung | 130100-002-    | Debitorenkonten |                   | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20.12.2021 | Benutzung | 130100-002-    | Debitorenkonten |                   | EUR      | -127,11                        | -174,12 | -174,12                      |
| 20856          | CMV-4010 | 21.12.2021 | Benutzung | 130100-002-    | Debitorenkonten | Guthaben auf Rechnung | USD      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 28.12.2021 | Benutzung | 130100-001-    | Debitorenkonten | Dienstprogramme         | USD      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 29.12.2021 | Benutzung | 130100-002-    | Debitorenkonten | Service           | USD      | 300                            | 300     | 300                          |

Von diesen Transaktionen werden drei bei der Abrechnung des Sachkontos abgerechnet.

Es gibt eine Rechnung über 175 US Dollar (USD 175). Diese Rechnung wurde durch eine Zahlung in Euro (EUR) beglichen, und es wurde ein Skonto abgezogen.

| Lfd. Nr. | Beleg  | Datum       | Typ      | Sachkonto | Kontoname        | Description | Währung | Betrag in Buchungswährung | Betrag  | Betrag in Berichtswährung |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 5.12.2021  | Benutzung | 130100-002-    | Debitorenkonten | Dienstprogramme   | USD      | 175                            | 175     | 175                          |
| 20851          | ARP-8000 | 20.12.2021 | Benutzung | 130100-002-    | Debitorenkonten |             | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20.12.2021 | Benutzung | 130100-002-    | Debitorenkonten |             | EUR      | -127,11                        | -174,12 | -174,12                      |

Die Ergebnisse für das Hauptkonto 130100 hängen davon ab, ob die Funktion aktiviert ist, bevor der Jahresabschluss ausgeführt wird. Wenn die Funktion aktiviert ist, hängt das Ergebnis auch von der Einstellung der Option Details während des Jahresabschlusses behalten ab.

### <a name="the-feature-isnt-enabled"></a>Die Funktion ist nicht aktiviert
Der Jahresabschluss erstellt drei Transaktionen des Eröffnungssaldos für das Hauptkonto 130100 im Jahr 2022. Die Summe der Transaktionen in der Buchhaltungswährung beträgt USD 525.

| Lfd. Nr. | Beleg  | Datum     | Typ    | Sachkonto | Kontoname        | Description | Währung | Betrag in Buchungswährung | Betrag  | Betrag in Berichtswährung |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 01.01.2022 | Vortrag | 130100-002-    | Debitorenkonten |             | USD      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 01.01.2022 | Vortrag | 130100-001-    | Debitorenkonten |             | USD      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 01.01.2022 | Vortrag | 130100-002-    | Debitorenkonten |             | EUR      | -127,11                        | -174,12 | -174,12                      |

Obwohl die Transaktion der Zahlung für EUR -127,11 buchhalterisch abgewickelt wurde, wird die Transaktion weiterhin als Anfangssaldo ausgewiesen.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>Funktion ist aktiviert und Details während des Jahresabschlusses behalten = Nein

Der Jahresabschluss erstellt zwei Eröffnungssaldo-Transaktionen für das Hauptkonto 130100 im Jahr 2022. Die Summe der Transaktionen in der Buchhaltungswährung beträgt immer noch 525 USD, aber die Transaktionen, die über das Sachkonto abgewickelt werden, sind von der Eröffnungsbilanz ausgeschlossen. Der Gesamtbetrag für das Konto 130100-002- beträgt USD 125 statt USD 299,12, und die Transaktion für EUR 127,11/USD 174,12 ist völlig ausgeschlossen.

| Lfd. Nr. | Beleg  | Datum     | Typ    | Sachkonto | Kontoname        | Description | Währung | Betrag in Buchungswährung | Betrag | Betrag in Berichtswährung |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 01.01.2022 | Vortrag | 130100-002-    | Debitorenkonten |             | USD      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 01.01.2022 | Vortrag | 130100-001-    | Debitorenkonten |             | USD      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>Funktion ist aktiviert und Details während des Jahresabschlusses aufbewahren = Ja

Der Jahresendabschluss erstellt fünf Transaktionen für den Eröffnungssaldo des Hauptkontos 130100 im Jahr 2022. Für jede der fünf Transaktionen, die nicht abgerechnet wurden, wird eine eigene Eröffnungsbilanztransaktion erstellt. Die Summe der Transaktionen in der Buchhaltungswährung beträgt immer noch 525 USD.

| Lfd. Nr. | Beleg  | Datum     | Typ    | Sachkonto | Kontoname        | Description       | Währung | Betrag in Buchungswährung | Betrag | Betrag in Berichtswährung |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 01.01.2022 | Vortrag | 130100-001-    | Debitorenkonten | Servicegebühr       | USD      | 100                            | 100    | 100                          |
| 20910          | YEC_2021 | 01.01.2022 | Vortrag | 130100-001-    | Debitorenkonten | Rückerstattung            | USD      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 01.01.2022 | Vortrag | 130100-002-    | Debitorenkonten | Guthaben auf Rechnung | USD      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 01.01.2022 | Vortrag | 130100-001-    | Debitorenkonten | Dienstprogramme         | USD      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 01.01.2022 | Vortrag | 130100-002-    | Debitorenkonten | Service           | USD      | 300                            | 300    | 300                          |

Wenn die Transaktionsdetails beibehalten werden, sind die ursprünglichen detaillierten Transaktionen davon nicht betroffen. Sie bleiben in dem Geschäftsjahr, das abgeschlossen wird, gebucht und nicht abgerechnet. Es wird eine Kopie dieser Transaktionen für die Eröffnungsbilanz erstellt. Die folgenden Werte aus den ursprünglichen Transaktionen werden in die Eröffnungsbilanztransaktionen kopiert.

- Sachkonto (das Hauptkonto und alle finanziellen Dimensionen)
- Beträge in den Währungen der Transaktion, der Buchhaltung und des Berichtswesens
- Description
- Buchungsebene
- Buchungstyp

   > [!NOTE]
   > Anderen Eröffnungssaldo-Transaktionen wird keine Buchungsart mehr zugewiesen. Daher kann die Buchungsart verwendet werden, um vorgezogene Eröffnungstransaktionen im Detail zu unterscheiden.

Einige Felder aus den ursprünglichen Transaktionen müssen sich in den detaillierten Transaktionen der Eröffnungsbilanz ändern. Das Datum der Transaktionen der Eröffnungsbilanz ist immer der erste Tag des nächsten Geschäftsjahres. Die Journalnummer muss sich ändern, und die Belegnummer ändert sich auf den Wert, der im Dialogfeld für den Jahresendabschluss eingegeben wurde.

Informationen zu den ursprünglichen Transaktionen finden Sie auf der Seite **Sachkontoabrechnung**. Jede detaillierte Eröffnungsbilanztransaktion zeigt die Spalte **Ursprungsdatum der Transaktion** im Raster an. Diese Spalte kann Ihnen helfen, Transaktionen im neuen Geschäftsjahr abzugleichen. Sie können **Originalgutschein anzeigen** wählen, um den vollständigen Originalgutschein aufzurufen.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Buchungen ausgleichen
Um Sachkontobuchungen auszugleichen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Hauptbuch** > **Periodische Aufgaben** > **Sachkonto Abrechnungen**.
2.  Legen Sie die Filter am oberen Rand der Seite fest.

    1. Wählen Sie einen Datumsbereich. Alternativ können Sie auch einen Code für ein Datumsintervall auswählen, um den Datumsbereich automatisch auszufüllen.

       - Der Datumsbereich kann keine Geschäftsjahre überschneiden. Wenn sich der Datumsbereich über mehrere Geschäftsjahre erstreckt, werden keine Transaktionen angezeigt, wenn Sie **Transaktionen anzeigen** wählen.
       - Wenn der Datumsbereich in einem offenen Geschäftsjahr liegt, können Transaktionen abgerechnet und die Abrechnung storniert werden. Liegt der Datumsbereich in einem abgeschlossenen Geschäftsjahr oder ist der Jahresabschluss abgeschlossen, werden zwar Transaktionen angezeigt, aber sie können nicht abgerechnet oder nicht abgerechnet werden. Sie können die Markierung von Transaktionen nur in einem abgeschlossenen Geschäftsjahr aufheben. Wenn sich der Datumsbereich in einem geschlossenen Geschäftsjahr befindet, sind die Schaltflächen **Markiert**, **Markierte Transaktionen abrechnen** und **Markierte Transaktionen stornieren** nicht verfügbar.

    2. Wählen Sie das Hauptkonto aus, für das Transaktionen angezeigt werden sollen. Dieses Feld ist erforderlich. Das Suchfeld zeigt nur die Hauptkonten an, die auf der Seite **Sachkontoabrechnung** für den Kontenplan der Firma ausgewählt wurden.
    3. Wählen Sie die Buchungsebene. Sie können keine Transaktionen abrechnen, die sich in verschiedenen Buchungsebenen befinden.
    4. Um das Hauptkonto und die Dimensionen in separaten Spalten anzuzeigen, wählen Sie ein Finanzdimensionen-Set.

3.  Wählen Sie **Transaktionen anzeigen**, um alle Transaktionen anzuzeigen, die den von Ihnen festgelegten Filtern entsprechen. Wenn Sie Filter- oder Dimensionseinstellungen ändern, müssen Sie **Buchungen anzeigen** wieder aktivieren.
4.  Wählen Sie Zeilen für die Abrechnung. Der Wert im Feld **Ausgewählter Betrag** oben auf der Seite erhöht oder verringert sich, um den Gesamtbetrag der ausgewählten Zeilen wiederzugeben.
5.  Wenn Sie die Auswahl der Transaktionen abgeschlossen haben, wählen Sie **Ausgewählte markieren**. Für jede ausgewählte Transaktion erscheint ein Häkchen in der Spalte **Markiert**. Außerdem erhöht oder verringert sich der Wert im Feld **Markierter Betrag** oberhalb des Rasters, um den Gesamtbetrag auf den markierten Zeilen wiederzugeben.
6.  Wenn der Wert im Feld **Markierte Menge** **0** (Null) ist, wählen Sie **Markierte Transaktionen ausgleichen**.

    - Eine Teilabrechnung ist nicht zulässig. Sie können z.B. eine Transaktion im Soll von 100 $ nicht mit einer Transaktion im Haben von 90 $ verrechnen. Die verbleibende $10-Gutschriftstransaktion muss ebenfalls für die Abrechnung markiert werden.
    - Geben Sie ein Abrechnungsdatum ein. Das Datum muss auf oder nach dem spätesten Datum der Transaktionen liegen, die zur Abrechnung markiert sind.

Der Status der markierten Transaktionen wird auf **Ausgeglichen** geändert.

> [!IMPORTANT]
> Alle Transaktionen, die Sie für die aktive juristische Entität und das ausgewählte Hauptkonto zur Abrechnung markiert haben, werden abgerechnet. Die Transaktionen müssen nicht auf der Seite erscheinen. Sie werden abgerechnet, auch wenn sie aufgrund eines Filters ausgeblendet sind.

Einige Prozesse, wie z.B. die Stornierung einer Transaktion, rechnen automatisch Sachkonto-Transaktionen ab. Zum Beispiel werden eine Zahlung und eine Rechnung in Debitoren abgerechnet, und die Abrechnung erzeugt einen realisierten Gewinn/Verlust. Die Abrechnung der Zahlungen und Rechnungen gleicht keine Transaktionen des Sachkontos aus, wie z.B. Transaktionen für das Sachkonto Debitoren. Wenn jedoch die Zahlung und die Rechnung in der Debitorenbuchhaltung nicht ausgeglichen sind, führt die Stornobuchung, die bei der Stornierung der Debitorenbuchhaltung gebucht wurde, dazu, dass die ursprünglichen und die stornierten Buchungen im Hauptbuch ausgeglichen werden. Wenn die Funktion **Abgleich zwischen Sachkonto und Jahresabschluss** aktiviert ist, erfolgt der Sachkontoausgleich einer Stornierung nicht automatisch, wenn das Stornodatum in einem anderen Geschäftsjahr liegt.

## <a name="use-excel-for-ledger-settlement"></a>Excel für die Abrechnung von Sachkonten verwenden

Transaktionen, die auf der Seite **Sachkontoabrechnung** angezeigt werden, können nach Excel exportiert werden. In Excel können Sie Transaktionen weiter filtern, um zu bestimmen, welche Transaktionen für die Abrechnung markiert werden sollen.
Beide Entitäten für die Abrechnung von Sachkonten exportieren Transaktionen nur für das Hauptkonto, das auf der Seite **Abrechnung von Sachkonten** ausgewählt wurde. Transaktionen für abgeschlossene Geschäftsjahre können zwar immer noch mit Excel markiert bzw. die Markierung aufgehoben werden, aber sie können nicht abgerechnet werden. Außerdem können abgerechnete Transaktionen für dieses Geschäftsjahr nicht mehr storniert werden.

## <a name="make-transactions-easier-to-find"></a>Suchen Sie Transkaktionen einfacher

Die Seite **Sachkontoabrechnungen** enthält Funktionalitäten, die es Ihnen erleichtern, die Transaktionen anzuzeigen, die Sie für die Abrechnung benötigen.

- Verwenden Sie den Filter **Markiert**, um Transaktionen danach zu filtern, ob das Kontrollkästchen **Markiert** für sie aktiviert ist.
- Verwenden Sie den Filter **Status**, um Transaktionen nach ihrem Status zu filtern.
- Wählen Sie **Sortieren nach absolutem Betrag**, um die Beträge nach absolutem Wert zu sortieren. Auf diese Weise können Sie Belastungen und Gutschriften, die denselben Betrag haben, gruppieren.

## <a name="reverse-a-settlement"></a>Ausgleich stornieren

Sie können einen Ausgleich stornieren, die versehentlich vorgenommen wurde.

1.  Führen Sie die Schritte 1 bis 3 im Abschnitt [Transaktionen abrechnen](#settle-transactions) aus, um die Transaktionen anzuzeigen, an denen Sie interessiert sind.
2.  Wählen Sie im Feld **Status** die Option **ausgeglichen** aus.
3.  Wählen Sie Zeilen für die Umkehrung aus.
4.  Wählen Sie **Markierte Transaktionen rückgängig machen**. Der Status aller Transaktionen, die dieselbe Abrechnungs-ID haben, wird auf **Nicht abgerechnet** aktualisiert.

> [!IMPORTANT]
> Alle Transaktionen, die die gleiche Abrechnungs-ID haben, werden storniert, auch wenn sie nicht markiert sind. Zum Beispiel wurden vier Zeilen markiert und abgerechnet. Alle vier Zeilen haben die gleiche Abwicklungs-ID. Wenn Sie eine dieser vier Zeilen markieren und dann **Markierte Transaktionen stornieren** wählen, werden alle vier Zeilen storniert.






