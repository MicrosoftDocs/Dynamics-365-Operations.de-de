---
title: Doppelte Währung
description: Dieses Thema enthält Informationen zu doppelter Währung. Dabei wird die Berichtswährung als eine zweite Buchhaltungswährung für Microsoft Dynamics 365 for Finance and Operations verwendet.
author: kweekley
manager: AnnBe
ms.date: 08/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, Ledger, AssetTransReportingCurrencyAmountsWizard,BankAccountTransReportingCurrencyAmountsWizard, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 6d5128ea9daaf22ee962ca5fc70a05cba05c7edb
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867510"
---
# <a name="dual-currency"></a>Doppelte Währung

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Funktion, die in Microsoft Dynamics 365 for Finance and Operations Version 8.1 (Oktober 2018) eingeführt wurden, ermöglichen es, die Berichtswährung als zweite Buchhaltungswährung zu verwenden. Diese Funktion wird auch als *Doppelte Währung* bezeichnet. Die Änderungen für doppelte Währung können nicht durch einen Konfigurationsschlüssel oder einen Parameter deaktiviert werden. Da die Berichtswährung als zweite Buchhaltungswährung verwendet wird, änderte sich die Art, in der die Berichtswährung in der Buchungslogik berechnet wird.

Darüber hinaus wurden zahlreiche Module verbessert, um die Berichtswährung in verschiedenen Prozessen zu überwachen, zu melden und zu verwenden. Die Module, die betroffen sind, umfassen Folgendes:

- Hauptbuch 
- Finanzberichterstellung 
- Kreditorenkonten
- Debitorenkonten 
- Bargeld- und Bankverwaltung 
- Anlagen 
- Konsolidierungen

Nachdem einer Aktualisierung, müssen Sie bestimmte Schritte für Bargeld- und Bankverwaltung und Anlagen abschließen. Stellen Sie daher sicher, dass Sie die entsprechenden Abschnitte dieses Themas lesen und verstehen.

## <a name="posting-process"></a>Buchungsprozess

Die Buchungslogik wurde für alle Buchungen geändert, die einen Buchhaltungseintrag im Hauptbuch generieren. So wurde die Berichtswährung zuvor berechnet:

Transaktionswährungsbetrag \> Buchungswährungsbetrag \> Berichtswährungsbetrag

Beispielsweise wird eine Transaktion in der Währung "Kanadischer Dollar (CAD)" eingegeben. Der CAD-Betrag wird in die Buchhaltungswährung US-Dollar (USD) umgerechnet. Der USD-Betrag wird dann in die Berichtswährung Euro (EUR) umgerechnet. Daher müssen die Wechselkurse zwischen CAD und USD und zwischen USD und EUR vorhanden sind.

Hier ist die neue Berechnung:

Buchungswährungsbetrag \> Buchhaltungswährungsbetrag

Transaktionswährungsbetrag \> Berichtswährungsbetrag

Aufgrund dieser Änderung müssen die Wechselkurse jetzt zwischen CAD und USD und zwischen CAD und EUR vorhanden sein.

## <a name="reports-and-inquiries"></a>Berichte und Abfragen

Verschiedene Berichte und Abfragen zeigen nun Berichtswährungsbeträge und Buchhaltungswährungsbeträge. Nicht jeder Bericht und jede Abfrage wurde aktualisiert. Beispielsweise wurden Berichte, die Beträge nur in der Buchungswährung anzeigen nicht geändert.

Die Änderungen folgen einem von zwei Mustern:

- Wenn im Bericht oder der Abfrage ausreichend Platz vorhanden sind, um Beträge in der Buchhaltungswährung und in der Berichtswährung anzuzeigen, wurden die Berichtswährungsbeträge hinzugefügt.
- Wenn im Bericht oder der Abfrage kein ausreichender Platz vorhanden ist, um Beträgen in beiden Währungen anzuzeigen, wurde eine Option hinzugefügt, damit Benutzer auswählen können, welche Währung angezeigt wird.

Für verschiedene Berichte und Abfragen wurde auch Logik hinzugefügt, um die Berichtswährungsbeträge zu unterdrücken, wenn Berichtswährung und Buchhaltungswährung gleich sind oder die Berichtswährung auf dem Sachkonto der juristischen Person nicht definiert wurde.

## <a name="financial-journals"></a>Finanzerfassungen

Für Finanzerfassungen, wie allgemeine Erfassung und die Kreditorenrechnungserfassung, wurden aktualisiert, sodass diese zusätzliche Informationen zu der Berichtswährung enthalten. Summen für den Beleg und die Erfassung werden jetzt in der Berichtswährung angezeigt. Darüber hinaus werden Informationen zum Wechselkurs der Berichtswährung nun auf der Registerkarte **Allgemeines** der Erfassungspositionen angezeigt. Daher können Sie den Wechselkurs der Berichtswährung überschreiben, wenn Sie Buchungen eingeben.

## <a name="vendor-invoices-sales-orders-and-sales-agreements"></a>Lieferantenrechnungen, Aufträge und Kaufverträge
Kreditorenrechnungen, Aufträge und Kaufverträgen wurden aktualisiert, um festen Wechselkurs für die Berichtswährung einzubeziehen. Ein fester Wechselkurs kann für die Buchhaltungswährung und Berichtswährung definiert werden, wenn die Buchungswährung anders ist. Wenn die Buchhaltungswährung und die Berichtswährung übereinstimmen, wird der feste Wechselkurs synchron gehalten, indem der feste Wechselkurs der Buchhaltungswährung als Berichtswährung verwendet wird. Der feste Wechselkurs für die Berichtswährung kann nicht für diese Konfiguration geändert werden. Wenn die Buchhaltungswährung und die Berichtswährung unterschiedlich sind, kann ein fester Wechselkurs während demm Transaktionseintrag für die Buchhaltungswährung und die Berichtswährung definiert werden. Wenn die Berichtswährung für das Sachkonto nicht festgelegt wurde, ist das Feld **Fester Wechselkurs für Berichtswährung** nicht aktiviert und es wird keine Berichtswährungsbetrag berechnet.

## <a name="module-changes"></a>Moduländerungen

Folgende Module verwenden die Berichtswährung als zweite Buchhaltungswährung:

- [Hauptbuch](#general-ledger)
- [Finanzberichterstellung](#financial-reporting)
- [Kreditorenkonten](#accounts-payable-and-accounts-receivable)
- [Debitorenkonten](#accounts-payable-and-accounts-receivable)
- [Bargeld- und Bankverwaltung](#cash-and-bank-management)
- [Anlagen](#fixed-assets)
- [Konsolidierungen](#consolidations)

### <a name="general-ledger"></a>Hauptbuch

Wenn eine Berichtswährung auf dem Sachkonto festgelegt wurde, verfolgte das Hauptbuch Berichtswährungsbeträge bereits bei jedem Buchhaltungseintrag. Allerdings werden diese Beträge jetzt aus den Buchungswährungsbeträgen umgerechnet.

Die folgenden weiteren Änderungen im Modul **Hauptbuch** wurden vorgenommen:

- Ein separater Wechselkurstyp für die Berichtswährung kann auf dem Sachkonto festgelegt werden. Wenn eine Organisation keinen anderen Wechselkurstyp verwenden möchte, können Sie das Feld für den Wechselkurstyp für das Berichtswährung leer lassen. Alternativ können Sie den gleichen Wechselkurstyp auswählen, der für die Buchhaltungswährung verwendet wird. Wenn Sie das Feld leer lassen, verwendet das System den Wechselkurstyp für die Buchhaltungswährung.
- Eine neue Erfassung, die Regulierungserfassung der Berichtswährung ermöglicht die Buchung von Regulierungen auf Sachkonten nur in der Berichtswährung. Diese Erfassung ermöglicht nur die Buchung auf Sachkonten. Sie unterstützt kein Intercompany und die Währung muss die Berichtswährung der juristischen Person sein, wo die Erfassung gebucht wird. Wenn die Erfassung gebucht wird, sind die Buchungswährungs- und Buchhaltungswährungsbeträge 0 (Null), und der Berichtswährungsbetrag wird mit dem Betrag gebucht, die für die Buchung eingegeben wurde. Da die Methode, mit der die Berichtswährung in den Modulen **Kreditoren**, **Debitoren** und **Anlagevermögen** verwendet wird, geändert wurde, kann diese Erfassung bei einer Aktualisierung für Regulierungen verwendet werden. Beispiele, die zeigen, wie diese Erfassung verwendet werden kann, finden Sie in den Abschnitten zu diesen Modulen.
- Der Prozess für Periodenzuweisung wurde aktualisiert, sodass er Beträge in den Buchungs-, Buchhaltungs- und Berichtswährungen zuweist. Zuvor wurden Beträge in den Transaktions- und Buchhaltungswährungen zugewiesen, und dann wurde der Buchhaltungswährungsbetrag in die Berichtswährung umgerechnet. Durch dieses Verhalten kann ein Saldo auf dem Sachkonto in der Berichtswährung verbleiben. Wenn jetzt Beträge im Buchhaltungseintrag berechnet und verwendet werden, erfolgt keine Umrechnung.
- Der Prozess für eine Neubewertung der Fremdwährung hat bereits Beträge in der Berichtswährung neu bewertet. Allerdings wird der Berichtswährungsbetrag jetzt durch den Betrag in der Buchungswährung berechnet, wie im Abschnitt [Buchungsprozess](#posting-process) oben in diesem Thema beschrieben.
- Viele Berichte und Abfragen im Hauptbuch verwendeten bereits die Berichtswährung, einige jedoch nicht. Ein Beispiel ist die Listenseite **Zwischenbilanz**. Diese Listenseite enthält jetzt Spalten für die Buchhaltungswährung und die Berichtswährung. Beachten Sie, dass die Spalten für die Berichtswährung ausgeblendet werden, wenn die Buchhaltungswährung und die Berichtswährung identisch sind oder keine Berichtswährung auf das Sachkonto festgelegt wurde.

### <a name="financial-reporting"></a>Finanzberichterstellung

Dank der Verbesserung am Modul **Finanzberichterstellung** können Sie Berichtswährungsbeträge auf zwei Arten in einer Finanzaufstellung eingeben. In der Spaltendefinition können Sie direkt in den Berichtswährungsbeträgen melden, die auf dem Sachkonto gebucht werden (neue Funktionen). Alternativ können Sie Beträge weiterhin aus der Buchhaltungswährung der Berichtswährung übertragen (vorhandene Funktion).

Diese Änderung wird durch die Einstellung **Währungsanzeige** in der Spaltendefinition verfügbar. Wenn Sie **Berichtswährung aus dem Hauptbuch** auswählen, werden die Beträge in der Spalte nicht umgerechnet. Stattdessen werden Sie direkt im Hauptbuch gemeldet. Wenn Sie in der Spalte umgerechnete Beträge anzeigen möchten, wählen Sie die Option **In XXXX umrechnen** aus, wobei *XXXX* die Berichtswährung ist, die in der Spalte angezeigt werden soll. In diesem Fall werden Buchhaltungswährungsbeträge in die ausgewählte Währung umgerechnet, indem die vorhandene Übersetzungsfunktion verwendet wird.

### <a name="accounts-payable-and-accounts-receivable"></a>Kreditorenkonten und Debitoren

Die Module **Kreditorenkonten** und **Debitoren** haben bereits Berichtswährungsbeträge verfolgt. Allerdings wurden die Beträge in verschiedenen Prozesse nicht angezeigt oder verwendet. Die folgenden Änderungen wurden vorgenommen:

- Berichtswährungsbeträge werden jetzt bei Transaktionen für Debitoren und Kreditoren angezeigt. Berichtswährungsbeträge werden auch für den offenen Saldo jeder Buchung angezeigt.
- Der Fälligkeitsprozesses wurde aktualisiert, sodass eine Organisation die Zeitperioden in der Buchhaltungswährung oder der Berichtswährung anzeigen kann.
- Verschiedene Abfragen und Berichte wurden aktualisiert, sodass sie Berichtswährungsbeträge anzeigen. Hierzu gehören beispielsweise die Berichte **Debitor-/Sachkontenabstimmung** und **Kreditor-/Sachkontenabstimmung**.
- Der Prozess für eine Neubewertung der Fremdwährung hat bereits Beträge in der Berichtswährung neu bewertet. Allerdings wird der Berichtswährungsbetrag jetzt durch den Betrag in der Buchungswährung berechnet, wie im Abschnitt [Buchungsprozess](#posting-process) beschrieben.
- **Aktualisierungsüberlegung:** Vor einer Aktualisierung werden die Berichtswährungsbeträge für Dokumente (Rechnungen, Zahlungen usw.) über die Buchhaltungswährung berechnet. Beispielsweise wird eine Rechnung die gebucht wird, bevor ein Organisation eine Aktualisierung durchführt, nicht bezahlt. Während der Aktualisierung wird der Buchhaltungseintrag der Rechnung nicht geändert. Nach dem Upgrade gelten jedoch die Änderungen für doppelte Währung. Wenn also eine Zahlung für die Rechnung erfolgt, wird der Berichtswährungsbetrag der Zahlung nun über den Betrag in der Buchungswährung berechnet. Wenn die Zahlung und die Rechnung beglichen werden, wird beim realisierten Gewinn/Verlust möglicherweise eine geringfügige Betragsdifferenz berechnet, da die Berichtswährungsbeträge nun anders berechnet werden. Wenn die Differenz, die berechnet wird, als bedeutend gilt, kann die neue Regulierungserfassung für die Berichtswährung verwendet werden, um nur den Saldo des realisierten Gewinns/Verlusts und der Kreditoren-/Debitorsachkonten in der Berichtswährung zu regulieren.

### <a name="cash-and-bank-management"></a>Bargeld- und Bankverwaltung

Zuvor verfolgte das Modul **Bargeld- und Bankverwaltung** keine Berichtswährungsbeträge für Transaktionen, die für jedes Bankkonto gebucht wurden. Nach der Aktualisierung werden Berichtswährungsbeträge für alle neuen gebuchten Transaktionen automatisch nachverfolgt. Allerdings müssen Berichtswährungsbeträge für zuvor gebuchte Transaktionen im untergeordneten Sachkonto hinzugefügt werden.

- **Aktualisierungsüberlegung:** Da Bankkontotransaktionen zuvor keine Berichtswährungsbeträge im untergeordneten Sachkonto verfolgten, wurde ein Assistent hinzugefügt, damit Sie den Bankkontotransaktionen Berichtswährungsbeträge hinzufügen können. Dieser Assistent bucht **nicht** erneut im Hauptbuch. Stattdessen entnimmt er die Berichtswährungsbeträge aus dem Hauptbuch und aktualisiert sie in den Tabellen für untergeordnete Sachkonten.

    - Wenn Sie den Assistenten verwenden möchten, wählen Sie **Bargeld- und Bankverwaltung** \> **Einstellungen** \> **Berichtswährungsbeträge zu Bankkontobuchungen hinzufügen** aus.
    - Im Assistenten werden Transaktionen für alle Bankkonten mit einem Berichtswährungsbetrag von 0 (null) im aktuellen Unternehmen angezeigt. Nur Transaktionen, die vor die Aktualisierung gebucht wurden, werden einbezogen.
    - der Assistent sucht die entsprechenden Buchhaltungseinträge für jede Bankkontotransaktion im Hauptbuch und gibt einen Standardberichtswährungsbetrag ein. Zwar können die Beträge bearbeitet werden, es wird jedoch empfohlen, dass dies **nicht** zu tun. Andernfalls sind Sie möglicherweise nicht in der Lage, die Bankkontosalden im Hauptbuch abzustimmen. Sie sollten einen Betrag nur bearbeiten, wenn der Berichtswährungsbetrag nicht im Hauptbuch gefunden werden kann. In diesem Fall zeigt der Assistent einen Betrag von 0 (null) für die Berichtswährung an.
    - Wenn Sie im Assistenten **Abbrechen** auswählen, werden die Bankkontobuchungen und alle Änderungen an den Berichtswährungsbeträgen bis zur nächsten Ausführung des Assistenten gespeichert. Die Berichtswährungsbeträge werden für Bankkontobuchungen allerdings nicht aktualisiert. Die Aktualisierung erfolgt nur, wenn Sie **Fertig stellen** im Assistenten auswählen. Sie können den Assistenten mehrmals ausführen. Daher können Sie alle fehlerhaften Berichtswährungsbeträge korrigieren, wenn Sie einen Fehler machen.

- In der Bargeld- und Bankverwaltung wurden keine Prozesse geändert. Jedoch wurden verschiedene Berichte und Abfragen aktualisiert, sodass sie Berichtswährungsbeträge anzeigen. Die Bargeld-Planungsberichte sind eine Ausnahme. Bei ihnen wurden die Berichtswährungsbeträge nicht hinzugefügt.

### <a name="fixed-assets"></a>Anlagevermögen

Zuvor verfolgte das Modul **Anlagen** keine Berichtswährungsbeträge für Transaktionen, die für jedes Anlagebuch gebucht wurden. Nach der Aktualisierung werden Berichtswährungsbeträge für alle neuen gebuchten Transaktionen automatisch nachverfolgt. Allerdings müssen Berichtswährungsbeträge für zuvor gebuchte Transaktionen im untergeordneten Sachkonto hinzugefügt werden.

Darüber hinaus wurden am Abschreibungsprozess größere Änderungen vorgenommen. Bei diesen Änderungen ist nach einer Aktualisierung Benutzeraktivität erforderlich. Es ist wichtig, dass Sie die folgenden Änderungen lesen und verstehen, auch wenn Sie noch keine Anlagen verwenden.

- Die Methode, über die der Abschreibungsprozess den Berichtswährungsbetrag bestimmt, wurde geändert. Das folgende Szenario vergleicht, der Berichtswährungsbetrag für Abschreibungen zuvor bestimmt wurde und wie der Berichtswährungsbetrag nun bestimmt wird.



    **Abschreibungsszenario**

    Eine Anlage wird in den folgenden Beträge erworben und gebucht. Beachten Sie, dass der Berichtswährungsbetrag im Hauptbuch gebucht wird, aber nicht in den Tabellen des untergeordneten Anlagen-Sachkontos gespeichert wird.

    | Buchungsart | Buchungsbetrag | Kurs | Betrag in Buchhaltungswährung | Kurs | Berichtswährungsbetrag |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Anschaffung      | 1.000.000 DKK      | 2.0           | 500.000 USD                | 2,5           | 200.000 EUR               |

    **Bisherige Abschreibung der Berichtswährung**

    Am Jahresende wird der Abschreibungsvorschlag ausgeführt und die folgenden Beträge werden berechnet.

    | Buchungsart | Buchungsbetrag | Kurs | Betrag in Buchhaltungswährung | Kurs | Berichtswährungsbetrag |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Abschreibung     | 50.000 USD         | 1.0           | 50.000 USD                 | 2.6           | 19.230.77 EUR             |

    Wenn der Abschreibungsvorschlag ausgeführt wird, berechnet er den Buchhaltungswährungsbetrag, mithilfe die Abschreibungsmethode. Dann rechnet der diesen Betrag in die Berichtswährung um, indem er den aktuellen Wechselkurs zwischen USD und EUR verwendet. Diese Umrechnung verursacht Probleme, da die Anlage in der Berichtswährung nicht vollständig abgeschrieben werden kann, wenn der Kasskurs verwendet wird.

    **Neue Abschreibung der Berichtswährung**

    Der Abschreibungsprozess wurde geändert, sodass der Berichtswährungsbetrag auch mithilfe der Abschreibungsmethode berechnet wird. Hier finden Sie die Ergebnisse, wenn die Abschreibung für die Anlage ausgeführt wird.

    | Buchungsart | Buchungsbetrag | Kurs | Betrag in Buchhaltungswährung | Kurs                                                       | Berichtswährungsbetrag |
    |------------------|--------------------|---------------|----------------------------|---------------------------------------------------------------------|---------------------------|
    | Abschreibung     | 50.000 USD         | 1.0           | 50.000 USD                 | 2,5<blockquote>[!NOTE] Obwohl dieser Kurs angezeigt wird, wurde er nicht verwendet, um in die Berichtswährung umzurechnen.</blockquote> | 20.000 EUR                |

    Wenn der Abschreibungsvorschlag ausgeführt wird, berechnet er den Buchhaltungswährungsbetrag und den Berichtswährungsbetrag mittels der Abschreibungsmethode. Die Beträge werden dann im Buchhaltungseintrag im Hauptbuch verwendet. Es erfolgt keine Umrechnung zur Bestimmung des Berichtswährungsbetrags.

- **Aktualisierungsüberlegung:** Da Anlagenbuchtransaktionen zuvor keine Berichtswährung verfolgten, wurde ein Assistent hinzugefügt, damit Sie den Anlagenbuchtransaktionen Berichtswährungsbeträge hinzufügen können. Dieser Assistent bucht **nicht** erneut im Hauptbuch. Da die Methode, mit der der Abschreibungsvorschlag die Berichtswährungsbeträge berechnet, geändert wurde, **muss** der Assistent ausgeführt und für jedes Unternehmen beendet werden, bevor eine Organisation Abschreibungsbuchungen eingeben kann.

    - Wenn Sie den Assistenten verwenden möchten, wählen Sie **Anlagevermögen** \> **Einstellungen** \> **Berichtswährungsbeträge zu Anlagenbüchern hinzufügen** aus.
    - Im Assistenten werden Transaktionen für alle Anlagenbücher mit einem Berichtswährungsbetrag von 0 (null) im aktuellen Unternehmen angezeigt. Nur Transaktionen, die vor die Aktualisierung gebucht wurden, werden einbezogen.
    - Der Assistent ruft **keine** Berichtswährungsbeträge aus dem Hauptbuch ab. Wie im vorherigen Szenario beschrieben, haben die Berichtswährungsbeträge, die ursprünglich in das Hauptbuch gebucht wurden, den Kasskurs falsch verwendet. Diese Beträge sollten im untergeordneten Anlagen-Sachkonto nicht angezeigt werden, da die folgende Abschreibungsberechnung falsche Beträge verwendet. Stattdessen sucht der Assistent den Wechselkurs zum Datum der ersten Anschaffung. Anschließend verwendet er den Wechselkurs, um den Berichtswährungsbetrag zu empfehlen, der im untergeordneten Sachkonto gebucht werden sollte. Hier finden Sie ein Beispiel dessen, was der Assistent im vorherigen Szenario möglicherweise angezeigt hat.

        | Anlagen | Buchen      | Buchungsart | Transaktionsdatum | Währung | Betrag in Buchungswährung | Dauer  | Wechselkurs | Berichtswährungsbetrag |
        |-------------|-----------|------------------|------------------|----------|--------------------------------|---------|-----------|---------------------------|
        | BUIL-00001  | 200\_SLLT | Anschaffung      | 6/3/2016         | DKK      | 1.000.000                      | 500.000 | 2,5       | 250.000                   |
        | BUIL-00001  | 200\_SLLT | Abschreibung     | 6/3/2016         | DKK      | 50.000                         | 50.000  | 2,5       | 250.000                   |
        | BUIL-00001  | 200\_SLLT | Abschreibung     | 6/3/2016         | DKK      | 50.000                         | 50.000  | 2,5       | 250.000                   |
        | BUIL-00001  | 200\_SLLT | Abschreibung     | 6/3/2016         | DKK      | 50.000                         | 50.000  | 2,5       | 250.000                   |

    - Zahlreiche Debitoren haben ihre Anlagentransaktionsdetails in Arbeitsmappen v erfolgt. Diese Details umfassen die Wechselkurse und Beträge. Wenn Sie diese Daten in einer Arbeitsmappe aufbewahren, können Sie mit einen benutzerdefinierten Wechselkurstyp erstellen und diesen mit den Wechselkursen aus der Arbeitsmappe aktualisieren. Dieser Wechselkurstyp wird dann verwendet, um einem Standardwechselkurs zum Anschaffungsdatum einzugeben und den Berichtswährungsbetrag zu berechnen. Wenn kein Wechselkurstyp ausgewählt ist, verwendet der Assistent den Wechselkurstyp, der für das Sachkonto festgelegt wurde.
    - Der Wechselkurs für die Buchhaltungswährungsbeträge können geändert werden. Wenn der Wechselkurs geändert wird, wird der Berichtswährungsbetrag mit dem neuen Kurs neu berechnet.
    - Wenn Sie im Assistenten **Abbrechen** auswählen, werden die Analgenbuchtransaktionen und alle Änderungen am Wechselkurs oder den Berichtswährungsbeträgen bis zur nächsten Ausführung des Assistenten gespeichert. Die Berichtswährungsbeträge werden für Anlagenbuchtransaktionen allerdings nicht aktualisiert. Die Aktualisierung erfolgt nur, wenn Sie **Fertig stellen** im Assistenten auswählen. Sie können den Assistenten mehrmals ausführen. Daher können Sie alle fehlerhaften Berichtswährungsbeträge korrigieren, wenn Sie einen Fehler machen.
    - Wenn die Berichtswährungsbeträge vollständig im untergeordneten Sachkonto aktualisiert sind, **müssen** Sie die Option **Haben Sie alle Berichtswährungsbeträge in den Anlagenbuchtransaktionen aktualisiert?** auf **Ja** festlegen und dann **Fertigstellen** auswählen. Abschreibungsberechnungen können nicht abgeschlossen werden, bis Sie die Option **Haben Sie alle Berichtswährungsbeträge in den Anlagenbuchtransaktionen aktualisiert?** auf **Ja** festlegen. Nachdem diese Option auf **Ja** festgelegt wurde, ist der Assistent nicht mehr verfügbar.
    - Nachdem die Anlagetransaktionen im untergeordneten Sachkonto mit Berichtswährungsbeträgen aktualisiert wurden, stimmen diese Beträge nicht mehr mit den Beträgen überein, die ursprünglich im Hauptbuch gebucht wurden. Allerdings kann die Regulierungserfassung der Berichtswährung verwendet werden, um die Salden der Abschreibungssachkonten im Hauptbuch zu aktualisieren, sodass sie den Beträgen entsprechen, die ursprünglich gebucht wurden.
    - Ein neuer **Berichtswährungsbeträge zu Anlagenbuchungen**-Eintrag, der im Arbeitsbereich **Datenverwaltung** hinzugefügt wurde, erlaubt Ihnen, die Daten aus dem Assistenten zu exportieren. Sie können die Daten dann verwenden, um den Saldo im untergeordneten Anlagen-Sachkonto für die Abschreibungstransaktionen zu bestimmen. Dieser Saldo kann dann verwendet werden, um den Betrag der Berichtswährungswechselkursregulierung im Hauptbuch festzulegen.

- **Aktualisierungsüberlegung:** Den Anlagen Neue wurden Setupfelder hinzugefügt und werden in der Abschreibungsberechnung verwendet. Möglicherweise müssen Sie diese Felder vor der nächsten Abschreibungsberechnung aktualisieren.

    - Im Anlagenbuch (**Anlage** \> **Bücher**) hat das Inforegister **Allgemeines** ein neues **Anschaffungspreis in Berichtswährung**-Feld.
    - Im Anlagenbuch (**Anlage** \> **Bücher**) hat das Inforegister **Abschreibung** ein neues **Voraussichtlicher Schrottwert in Berichtswährung**-Feld.
    - In den Anlagenparametern (**Anlage** \> **Einstellungen** \> **Anlageparameter**), hat das Inforegister **Allgemeines** ein neues **Mindestabschreibungsbetrag in Berichtswährung**-Feld.
    - In den Büchern (**Anlage** \> **Einstellungen** \> **Bücher**) hat das Inforegister zwei neue Felder: **Allgemeines** das Inforegister zwei neue Felder: **Abschreibung in Berichtswährung runden** und **Nettobuchwert in der Berichtswährung belassen**.

- Da der Abschreibungsvorschlag nun Beträge in der Buchhaltungswährung in der Berichtswährung berechnet, wurde die Anlagenerfassung aktualisiert, sodass Abschreibungsbeträge in der Berichtswährung angezeigt werden. Für Abschreibungstransaktionen, ist die Transaktionswährung immer die Buchhaltungswährung. Daher werden diese Beträge weiterhin in den Spalten **Soll** und **Haben** angezeigt. Zwei neue Spalten, **Sollwert in Berichtswährung** und **Habenwert in Berichtswährung** wurden dem Raster hinzugefügt.

    - Die neuen Felder sind nur verfügbar, wenn der Transaktionstyp einer der vier Abschreibungstypen ist: **Abschreibung**, **Abschreibungsregulierung**, **Außerordentliche Abschreibung** oder **Sonderabschreibung**.
    - Wenn ein Abschreibungstransaktionstyp in die Anlagenerfassung eingegeben wird, werden die Berichtswährungsbeträge in den neue Spalten angezeigt. Diese Beträge können geändert werden.
    - Wenn die Buchhaltungswährung und Berichtswährungen im Sachkonto überein, werden die Beträge synchron gehalten. Wenn Sie den **Haben**-Betrag   ändern, wird der **Habenwert in Berichtswährung**-Betrag automatisch geändert, sodass er übereinstimmt.
    - Werden ein anderer Transaktionstyp in die Anlagenerfassung eingegeben wird, werden die Beträge **Sollwert in Berichtswährung** und **Habenwert in Berichtswährung** niemals angezeigt, weder vor noch nach der Buchung. Die Buchhaltungswährungs- und Berichtswährungsbeträge sind auf dem Beleg, der im Hauptbuch gebucht wird, weiterhin verfügbar.
    
### <a name="consolidations"></a>Konsolidierungen
    
Funktionen, die in Microsoft Dynamics 365 for Finance and Operations 10.0.5 Version (Oktober 2019) eingeführt wurden, aktivieren Funktionen durch die Funktionsverwaltung für erweiterte Flexibilität für die Konsolidierung und doppelte Währung. Um diese Funktionen zu aktivieren, gehen Sie zum **Funktionsverwaltung**-Arbeitsbereich und wählen Sie **Funktionen für doppelte Währung in der Hauptbuchkonsolidierung aktivieren** aus.

In der Hauptbuchkonsolidierung wurde eine neue Option hinzugefügt, um entweder die Buchhaltungs- oder die Berichtswährungsbeträge von den Quellunternehmen zu konsolidieren. Wenn die Buchhaltungs- oder Berichtswährung mit der Buchhaltungs- oder Berichtswährung im Konsolidierungsunternehmen identisch ist, werden die Beträge direkt kopiert anstatt übersetzt.

-  Sie können nun auswählen, ob die Buchhaltungswährung oder die Berichtswährung vom Quellunternehmen als die Buchungswährung im Konsolidierungsunternehmen verwendet wird.

- Die Buchhaltungs- oder Berichtswährungsbeträge vom Quellunternehmen werden direkt in die Buchhaltungs- oder Berichtswährungsbeträge im Konsolidierungsunternehmen kopiert, wenn eine der Währungen übereinstimmt. Die Buchführungs- und Berichtswährungsbeträge im Konsolidierungsunternehmen werden mithilfe des Wechselkurses berechnet, wenn keine der Währungen übereinstimmt.
