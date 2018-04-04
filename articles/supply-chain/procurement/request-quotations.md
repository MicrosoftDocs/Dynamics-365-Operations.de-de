---
title: Angebotsanforderungen
description: "Dieses Thema bietet eine Übersicht über Angebotsanforderungen. Organisationen stellen eine Angebotsanforderung aus, um von mehreren Kreditoren Angebote für die Artikel oder Dienstleistungen, die sie kaufen müssen, zwecks Vergleich anzufordern."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b86363004b8702d1a654f2a1da49bba82fc8ff2a
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="requests-for-quotation-rfqs"></a>Angebotsanforderungen

[!include[banner](../includes/banner.md)]

Dieses Thema bietet eine Übersicht über Angebotsanforderungen. Organisationen stellen eine Angebotsanforderung aus, um von mehreren Kreditoren Angebote für die Artikel oder Dienstleistungen, die sie kaufen müssen, zwecks Vergleich anzufordern. Mit einer Angebotsanforderung werden Kreditoren gebeten, Preise und Lieferzeiten für die angegebenen Produktmengen bereitzustellen. Sie können Kreditoren auch bitten, anzugeben, ob zusätzliche Gebühren, etwa Lieferkosten, anfallen, oder ob der Kreditor Rabatte für große Bestellungen oder bei frühzeitiger Bezahlung der Rechnung anbietet.

Der Angebotsanforderungsprozess besteht aus den folgenden Aufgaben:

1. Erstellen und senden Sie eine Angebotsanforderung an einen oder mehrere Kreditoren.
2. Erhalten und erfassen Sie Antworten auf eine Angebotsanforderung (Angebote).
3. Übertragen Sie Angebote, die Sie akzeptieren, auf eine Bestellung, einen Kaufvertrag oder eine Bestellanforderung.

Die folgende Abbildung zeigt eine Übersicht über den Angebotsanforderungsprozess.

[![RFQ-Prozess](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Sie können eine Angebotsanforderung aus geplanten Aufträgen, einer Bestellanforderung oder durch einen manuellen Eintrag erstellen. Die Angebotsanforderung, die Sie erstellen, wird Angebotsanforderungsanfrage bezeichnet. Die Angebotsanforderungsanfrage ist das Basisdokument, dass Sie verwenden, um eine Angebotsanforderung für jeden Kreditor auszugeben.

Nachdem Sie die Angebotsanforderungsanfrage vorbereiten und Kreditoren hinzufügen, wählen Sie **Senden** auf der Angebotsanforderungsanfrage aus. Eine Angebotsanforderungserfassung wird für jeden Kreditor generiert, an den Sie eine Angebotsanforderung senden. Die Druckverwaltungseinstellungen können Sie die für die Sendeaktivität so konfigurieren, dass entweder ein Bericht für jeden Kreditor in ein Archiv ausgedruckt wird oder ein Bericht an die E-Mail-Adresse jedes Kreditors gesendet wird. Außerdem können Sie die Angebotsanforderungserfassung für jeden Kreditor verwenden, um einen Bericht zu generieren, den Sie später an den Kreditor senden oder erneut senden können. Sie können die Aktivität „Senden” auch so konfigurieren, dass ein Antwortbogen generiert wird, den der Kreditor ausfüllen kann.

Dieses Thema behandelt den Prozess der Handhabung von Angebotsanforderungen, wenn die Kreditorenzusammenarbeit nicht verwendet wird. Wenn Ihr System für Kreditorenzusammenarbeit eingerichtet ist, können Kreditoren Angebote direkt in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, eingeben. Weitere Informationen finden Sie unter [Kreditorenzusammenarbeit mit Debitoren](vendor-collaboration-work-customers-dynamics-365-operations.md).
 
Wenn Sie eine Angebotsanforderung ergänzen müssen, nachdem sie übermittelt wurde, können Sie die Angebotsanforderung an Kreditoren erneut senden, wenn Sie mit der Verwendung der beiden Zusatzaktivitäten fertig sind: Erstellen und Abschließen.

Wenn Sie Angebote per E-Mail erhalten, müssen Sie sie auf der Seite **Antworten auf Angebotsanforderung** eingeben. Wenn Sie die Option **Daten in Antwort kopieren** auswählen, werden Daten, wie die Menge und Daten aus der Angebotsanforderungsanfrage in die Antwort kopiert. Sie können diese Daten ändern, um das Angebot des Kreditors widerzuspiegeln.

Wenn eine zweite Iteration einer Antwort für einen bestimmten Kreditor erforderlich ist, klicken Sie auf **Zurück** auf der Seite **Antwort auf Angebotsanforderung**. Die Aktion „Zurück” generiert eine neue Erfassung und einen Bericht, die gemäß den Druckverwaltungseinstellungen gedruckt, archiviert und gesendet werden.

Wenn Sie Bewertungskriterien zu Ihrer Angebotsanforderungsanfrage hinzugefügt haben, hat die Antwort auf Angebotsanforderung einen Bewertungsbereich, in dem Sie die Punktzahlen eingeben können. Die Gesamtbewertungen werden angezeigt, wenn Sie die Antworten auf der Seite **Antworten vergleichen** vergleichen. Auf dieser Seite können Sie auch andere Antwortdaten vergleichen, wie beispielsweise den Positionspreis, das Lieferdatum und den Gesamtpreis.

Nachdem Sie ein Angebot oder Teilangebote wählen, können Sie diese annehmen und die restlichen ablehnen. Annahmeerfassungen, Ablehnungserfassungen und entsprechende Berichte werden generiert und werden gemäß den Druckverwaltungseinstellungen gedruckt, archiviert und gesendet werden. Wenn Sie ein Angebot oder bestimmte Positionen in einem Angebot annehmen, wird entweder ein Kaufvertrag oder eine Bestellung generiert, oder eine Bestellanforderung wird aktualisiert, je nach Bestelltyp der Angebotsanforderung. Sie können eine Handelsvereinbarung erstellen, die Sie später für jede der Antworten verwenden können, unabhängig davon, ob Sie diese akzeptiert oder zurückgewiesen haben.

Der Status einer Angebotsanforderung wird im Angebotsanforderungskopf angezeigt und hängt vom Status der Angebotsanforderungspositionen ab. Der Status gibt an, wie viel Sie in der Angebotsanforderung verarbeitet haben. Jede Angebotsanforderung besitzt zwei Werte für den Status: einen niedrigsten Status und einen höchsten Status. Der niedrigste Status steht für die am wenigsten fortgeschrittene Phase und der höchste Status für die am weitesten fortgeschrittene Phase einer Position in der Angebotsanforderung. Wenn beispielsweise die am wenigsten fortgeschrittene Phase in einer Angebotsanforderung für eine Position besteht, die erstellt wurde, ist der niedrigste Status für die Angebotsanforderung **Erstellt**. Wenn die am weitesten fortgeschrittene Phase in der Angebotsanforderung für eine Position besteht, die an Kreditoren gesendet wurde, ist der höchste Status für die Angebotsanforderung **Versendet**. Die Statusangaben werden bei der Verarbeitung einer Angebotsanforderung automatisch aktualisiert.

Sie können den niedrigsten und höchsten Status eines Angebotsanforderungskopfs auf der Seite **Alle Angebotsanforderungen** anzeigen. Sie können den niedrigsten und höchsten Status einer Angebotsanforderungsposition auf der Registerkarte **Positionen** auf der Seite **Angebotsanforderungen** anzeigen.

Hier ist die Reihenfolge der Statusangaben bei der Verarbeitung einer Angebotsanforderung:

1. **Erstellt**
2. **Gesendet**
3. **Eingegangen**
4. **Angenommen**, **Storniert** oder **Abgelehnt**

Diese Statusangaben werden detaillierter später in diesem Thema beschrieben.

## <a name="setting-up-rfq-functionality"></a>Einrichten von Angebotsanforderungsfunktionen

Bevor Sie eine Angebotsanforderungsanfrage erstellen können, müssen Sie Angebotsanforderungsinformationen auf der Seite **Beschaffungsparameter** einrichten. Wenn Sie eine Angebotsanforderungsanfrage erstellen, können Sie die Standardwerte angeben, die in die Angebotsanforderung kopiert werden. Sie können die folgenden Standardwerte angeben:

- Der Bestelltyp neuer Angebotsanforderungen: **Bestellung** oder **Kaufvertrag**
- Das Ablaufdatum und -uhrzeit
- Lieferinformationen und Zahlungsbedingungen
- Felder, die in der Antwort auf Angebotsanforderung einbezogen werden sollen

Sie können diese Werte für eine bestimmte Angebotsanforderungsanfrage überschreiben.

Sie sollten auch den Ergänzungsprozess konfigurieren. Als Teil dieser Konfiguration können Sie Feldsperre aktivieren. Wenn die Feldsperre aktiviert ist, muss ein Prokurist, der eine Angebotsanforderung ergänzen möchte, erst auf **Erstellen** im Abschnitt **Zusatz** auf der Registerkarte **Angebot** klicken. Nachdem dann die Angebotsanforderung durch den Zusatz ergänzt wurde, muss der Prokurist den Vorgang abschließen, indem er auf **Abschließen** klickt. Durch die Aktivität „Abschließen” wird eine E-Mail-Nachricht generiert, die Kreditoren über die ergänzte Angebotsanforderung benachrichtigt.

Auf der Seite **Beschaffungsparameter** wählen Sie die Vorlage für die E-Mail-Benachrichtigung aus, die an Kreditoren gesendet wird. Wenn eine Vorlage erstellt wird, kann sie die folgenden Ersatztoken enthalten:

- %Angebotsanforderungsanfrage%
- %Grund für Rücksendung des Angebots%
- %Grund für den Zusatz%
- %Zusatz erstellt von%
- %Unternehmen%
- %Name der Angebotsanforderungsanfrage%
- %ExpiryDateTime%
- %Datum%

Die Tokens %Grund für Angebotrücksendung% und %Grund für Ergänzung% werden durch Text ersetzt, die der Beschaffungsspezialist eingeben kann, wenn er oder sie die Ergänzung im Assistenten **Ergänzung** abschließt. Die Werte für die Tokens %Ergänzung vorbereitet von% und %Unternehmen% werden automatisch aus der Angebotsanforderung übernommen. Das Token %Datum% wird durch das aktuelle Datum ersetzt.

Eine E-Mail-Vorlage ist auch erforderlich, wenn eine Angebotsanforderung stornieren, nachdem sie versendet wurde. Diese E-Mail-Vorlage wird verwendet, um die Stornierungsbenachrichtigung an Kontaktpersonen des Kreditors zu senden. Die Vorlage muss auf der Seite **Beschaffungsparameter** ausgewählt werden. Wenn die Vorlage erstellt ist, kann sie die folgenden Ersatztoken enthalten:

- %Stornierungsgrund%
- %Angebotsanforderungsanfrage% 
- %Angebotsanforderung storniert von%
- %Unternehmen%
- %Name der Angebotsanforderungsanfrage%
- %Datum%

Das Token %Grund für Stornierung% wird von Text ersetzt, den der Prokurist im **Stornierungs**-Assistenten eingeben kann. Das Token %Datum% wird durch das aktuelle Datum ersetzt.

Wenn Sie Ursachencodes für eine Angebotsanforderungsantwort verwenden möchten, um anzugeben, um anzugeben, warum ein Angebot angenommen oder abgelehnt wurde, müssen Sie Ursachencodes auf der Seite **Ursachen für Kreditorenbuchungen** einrichten.

Auf der Seite **Formulareinstellungen** in „Beschaffung” können Sie die Darstellung Ihrer gedruckten oder gespeicherten Angebotsanforderungsdokumente konfigurieren.

> [!NOTE]
> Für eine Konfiguration für den öffentlichen Sektor müssen Sie den Ergänzungsprozess verwenden, um eine Angebotsanforderung zu ändern, die bereits gesendet wurde. Wenn eine Angebotsanforderung gesendet wird, sind Felder gesperrt. Um an der Angebotsanforderung Änderungen vornehmen zu können, müssen Sie daher **Erstellen** auswählen, um den Ergänzungsprozess zu beginnen, der zuvor beschrieben wurde. Das Sperrungsverhalten wird von der Option **Angebotsanforderung sperren, wenn diese gesendet wird** auf der Seite **Beschaffungsparameter** gesteuert. Standardmäßig ist dieser Parameter auf **Ja** festgelegt, und für eine Konfiguration für den öffentlichen Sektor kann die Standardeinstellung nicht geändert werden. Daher, obwohl der Ergänzungsprozess in einer Konfiguration, die nicht für den öffentlichen Sektor bestimmt ist, manuell gehandhabt werden kann, muss er in einer Konfiguration für den öffentlichen Sektor verwendet werden.

Wenn Sie eine Angebotsanforderung für eine Bestellung erstellen und einen Lagerartikel zur Angebotsanforderung hinzufügen, wird eine Lagerbuchung mit dem Zugangsstatus **Angebotszugang** erstellt. Es werden nur Angebotsanforderungspositionen mit diesem Status berücksichtigt, wenn Sie einen Produktprogrammplan verwenden, um den Bestand zu berechnen. Wenn Sie möchten, dass der Produktprogrammplan Angebotsanforderungspositionen als erwarteten Zugang umfasst, müssen Sie dieses Verhalten in den Einstellungen des Produktprogrammplans konfigurieren.

Ein Einkaufsleiter oder Agent kann Anfragentypen erstellen und verwalten, die zu den Beschaffungsanforderungen der Organisation passen. Jeder Anfragentyp kann einer Bewertungsmethode zugeordnet werden. Bewertungsmethoden bestehen aus einem Satz von Kriterien, die verwendet werden können, wenn Sie Angebote bewerten. Sie müssen Anfragentypen, Bewertungsmethoden und Bewertungskriterien auf den Seiten **Anfragentyp** und **Bewertungsmethode** einrichten.

## <a name="creating-and-sending-an-rfq"></a>Eine Angebotsanforderung erstellen und senden

Sie erstellen eine Angebotsanforderung, wählen die Kreditoren aus, die auf die Angebotsanforderung antworten sollen, und senden die Angebotsanforderung dann an die Kreditoren. Sie können die Druckverwaltung verwenden, um den Angebotsanforderungsbericht und Antwortbogenberichte an Ihr bevorzugtes Ziel weiterzuleiten.

Sie können eine Angebotsanforderung entweder für den Bestelltyp **Bestellung** oder den Bestelltyp **Kaufvertrag** erstellen.

Wenn die Angebotsanforderung vom Typ **Bestellung** ist, tritt das folgende Verhalten auf:

- Wenn Angebotsanforderungspositionen erstellt werden, werden Lagerbuchungen generiert, die den Zugangsstatus von **Angebotszugang** besitzen.
- Wenn Sie ein Angebot akzeptieren, wird eine Bestellung generiert.

Wenn die Angebotsanforderung vom Typ **Kaufvertrag** ist, tritt das folgende Verhalten auf:

- Die Angebotsanforderung wird für eine Vereinbarung zum Einkauf einer bestimmten Produktmenge oder eines bestimmten Produktwerts über einen gewissen Zeitraum verwendet. Sie müssen den Datumsbereich auswählen, der für den Kaufvertrag und den Namen des Mitarbeiters gilt, der mit der Verwaltung der Rahmenbestellung betraut ist.
- Wenn Sie ein Angebot annehmen, wird ein Kaufvertrag generiert.

Wenn die Angebotsanfordernung aus einer Bestellanforderung generiert wird, wird der Typ **Bestellanforderung** automatisch zugewiesen. Sie können eine Angebotsanforderung vom Typ **Bestellanforderung** nicht manuell erstellen.

Sie können nur eine Angebotsanforderung aus einer Bestellanforderung erstellen, wenn der Status der Bestellanforderung **Wird überprüft** ist und Ihnen die Erledigung der nächsten Workflowaufgabe zugewiesen ist. Die Positionen der Bestellanforderung werden automatisch aktualisiert, wenn Sie Positionen aus den Antworten auf Angebotsanforderung (Angebote) annehmen, die Sie von Kreditoren erhalten haben. Solange sich eine Angebotsanforderung in Bearbeitung befindet, können Sie eine Bestellanforderung also weder abschließen, ablehnen, genehmigen, noch irgendwelche anderen Aktionen an ihr ausführen.

Wenn Sie eine Angebotsanforderung erstellen, können Sie einen Anfragentyp auswählen. Der Anfragentyp bestimmt die Gruppe von Bewertungskriterien, die verwendet wird, um Antworten auf die Angebotsanforderung zu bewerten.

Sie können einer Angebotsanforderungsanfrage einen Fragebogen hinzufügen. Dieser Fragebogen wird dann auf allen Antworten angezeigt, nachdem Sie die Angebotsanforderung senden.

Es gibt drei Möglichkeiten, um die Kreditoren auswählen, die einer Angebotsanforderungsanfrage hinzugefügt werden sollen:

- Fügen Sie die Kreditoren nacheinander hinzu.
- Suchen Sie nach allen Kreditoren, die bestimmten Kriterien entsprechen.
- Fügen Sie automatisch alle Kreditoren hinzu, die für die Beschaffungskategorien, die bei den Angebotsanforderungspositionen verwendet werden, genehmigt sind.

Wenn die Angebotsanforderungsanfrage bereit ist, wählen Sie **Senden** aus. Die Aktion „Senden” generiert Erfassungen und Berichte, die gemäß Ihren Druckverwaltungseinstellungen gedruckt, archiviert und gesendet werden.

Wenn Sie die Kontrollkästchen **Kreditor zur Neuberechnung von Preisen verwenden** und **Kreditorenspezifische Artikelinformationen verwenden** auf der Seite **Angebotsanforderung wird gesendet** auf **Ja** festgelegt haben, wenn Sie die Angebotsanforderung an Kreditoren schickten, werden einige kreditorenspezifische Informationen automatisch eingegeben. Sie können diese Informationen auf der Seite **Antwort auf Angebotsanforderung** ändern.

In der folgenden Tabelle wird angezeigt, wie sich der Angebotsanforderungsstatus ändert, wenn Sie eine Angebotsanforderung erstellen und sie an Kreditoren senden.

| Aktion                             | Niedrigster Status der Angebotsanforderungskopfzeile | Höchster Status der Angebotsanforderungskopfzeile                        | Niedrigster Status einer Angebotsanforderungszeile | Höchster Status einer Angebotsanforderungszeile |
|------------------------------------|--------------------------|--------------------------------------------------|------------------------|-------------------------|
| Erstellen Sie den Angebotsanforderungskopf und die -position.    | Erstellt                  | Erstellt                                          | Erstellt                | Erstellt |
| Senden Sie die Angebotsanforderung an einen bestimmten Kreditor. | Versendet                     | Versendet                                             | Versendet                   | Versendet |
| Einen weiteren Kreditor hinzufügen                | Erstellt                  | Versendet (Die Angebotsanforderung ist nur einem Kreditor zugesendet worden). | Erstellt                | Versendet |
| Senden Sie die Angebotsanforderung an den zweiten Kreditor. | Versendet                     | Versendet                                             | Versendet                   | Versendet |

> [!NOTE]
> Sie können einer Angebotsanforderung jederzeit weitere Kreditoren hinzufügen. Der höchste und der niedrigste Status werden aktualisiert, um die neuen Kreditoren widerzuspiegeln. Wenn Sie z. B. ein Angebot von allen Kreditoren erhalten und mindestens eine Position in dem Angebot akzeptiert haben, lautet der niedrigste Status im Kopf der Angebotsanforderung **Abgelehnt** und der höchste Status ist **Angenommen**. Wenn Sie einen neuen Kreditor hinzufügen, ist der niedrigste Status in jeder beliebigen Position jetzt **Erstellt**. Daher wird der niedrigste Status im Angebotsanforderungskopf zu **Erstellt** aktualisiert, aber der höchste Status bleibt bei **Angenommen**.

## <a name="amending-an-rfq"></a>Ergänzen einer Angebotsanforderung

Gelegentlich müssen Sie eine Angebotsanforderung ändern, nachdem Sie sie gesendet haben. Möglicherweise müssen Sie die Angebotsanforderung ändern, wenn sich beispielsweise die Lieferdaten geändert haben oder Sie zusätzliche Produkte oder andere Mengen von Produkte möchten. Sie können den Ergänzungsprozess so konfigurieren, dass er entweder einschränkender oder weniger einschränkend ist.

Wenn Sie den Ergänzungsprozess konfigurieren, sodass er einschränkender ist, bevor Sie die Felder in einer Angebotsanforderungsanfrage ändern können, die bereits übermittelt wurde, müssen Sie **Erstellen** in der Angebotsanforderungsanfrage auswählen, um eine Ergänzung zu starten. Nachdem Sie Ihre Änderungen abgeschlossen haben, müssen Sie **Abschließen** auswählen. Sie werden dann durch den Prozess zum Hinzufügen von Informationen für die E-Mail-Nachricht geführt, die gesendet wird, um Kreditoren zur Ergänzung zu informieren. Der aktualisierte Angebotsanforderungsbericht, der einen Ergänzungshinweis umfasst, wird automatisch der E-Mail zugeordnet.

Wenn Sie den Ergänzungsprozess so konfigurieren, dass er weniger einschränkend ist, müssen Sie nicht **Erstellen** auswählen, bevor Sie die Felder auf einer Angebotsanforderungsanfrage ändern können, die bereits übermittelt wurde. Sie müssen allerdings einen Ergänzungshinweis zur Angebotsanforderung manuell hinzufügen und die Anfrage erneut senden. Beachten Sie, dass dieser Ansatz nur verwendet werden kann, wenn keine der Antworten (Angebote) verarbeitet wurden. Wenn Sie eine Antwort eingegeben haben und sie sich im Status **Eingegangen** befindet, ist die Schaltfläche **Senden** nicht verfügbar. In diesem Fall müssen Sie **Erstellen** und anschließend **Abschließen** auswählen, wie Sie es in einem einschränkenderen Prozess erfolgen muss. Die Antwort wird dann zurückgesetzt, um die Änderungen an der Angebotsanforderungsanfrage widerzuspiegeln. 

Wenn Kreditoren die Kreditorenzusammenarbeitschnittstelle verwenden, um Angebote einzugeben, müssen Sie immer den Ergänzungsprozess verwenden, um Kreditoren zu Änderungen an der Angebotsanforderungsanfrage zu informieren. Mithilfe dieser Anforderung wird die Situation verhindert, in der Kreditoren Angebote auf eine veraltete Angebotsanforderungsanfrage abgeben, während sich ihr Angebot in Bearbeitung befindet. Weitere Informationen über die Kreditorenzusammenarbeit finden Sie unter [Kreditorenzusammenarbeit mit externen Kreditoren](vendor-collaboration-work-external-vendors.md) 

Wenn Sie weitere Kreditoren dazu einladen möchten, Angebote zu unterbreiten, und keine Änderungen an der Angebotsanforderungsanfrage vorgenommen wurden, können Sie die Schaltfläche **Senden** verwenden. Die Kreditoren, die Sie hinzugefügt haben, werden auf der Seite **Senden** angezeigt und erhalten die E-Mail-Einladung.

## <a name="receiving-and-registering-rfq-replies"></a>Erhalten und Erfassen von Antworten auf Angebotsanforderungen

Wenn Sie eine Angebotsanforderung senden, wird automatisch ein Antwortblatt generiert. Wenn Sie Antworten (Angebote) auf eine Angebotsanforderung erhalten, müssen Sie die Antwortinformationen der einzelnen Kreditoren in einen kreditorenspezifischen Antwortbogen auf Angebotsanforderung eingeben. Wenn Sie Bewertungskriterien hinzugefügt haben, können Sie die Antworten bewerten. Sie vergleichen dann die Kreditorenangebote, indem Sie sie anhand Ihrer Bewertungskriterien, wie bester Gesamtpreis oder beste Gesamtlieferzeit, sortieren.

Wenn ein Fragebogen der Angebotsanforderungsanfrage zugeordnet ist, müssen Sie die Antworten auf die Fragen im Antwortbogen manuell eingeben.

Sie können auch alternative Positionen eingeben, wenn die Angebotsanforderungsanfrage alternative Positionen zulässt. Wählen Sie im Inforegister **Bestellanforderungspositionen** die Option **Position hinzufügen** aus. Geben Sie dann die Produktinformationen ein, beispielsweise Artikelnummer oder Beschaffungskategorie, Menge, Preis und Rabatt.

Wenn Sie eine Antwort eingegeben, aber ein neues Angebot vom Kreditor anfordern haben, können Sie die Angebotsanforderung erneut senden. Eine neue Erfassung und ein neuer Bericht werden generiert, und Sie können sie verwenden, um Änderungen vom Kreditor anzufordern.

Sie können eine Übersicht über alle Angebotsanforderungen und deren Antwortstatus auf der Seite **Weiterverfolgung der Angebotsanforderung** anzeigen.

In der folgenden Tabelle wird angezeigt, wie der Angebotsanforderungsstatus sich ändert, während Sie Angebote empfangen und die Informationen im Antwortbogen für Angebotsanforderung erfassen.

| Vorgang                                         | Niedrigster Angebotsstatus | Höchster Angebotsstatus | Niedrigster Status der Angebotsanforderungskopfzeile | Höchster Status der Angebotsanforderungskopfzeile | Niedrigster Status einer Angebotsanforderungszeile | Höchster Status einer Angebotsanforderungszeile |
|------------------------------------------------|-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Erfassen Sie ein Angebot eines Kreditors, und speichern Sie es.        | Gesendet              | Eingegangen           | Gesendet                     | Eingegangen                  | Gesendet                   | Eingegangen |
| Erfassen Sie das Angebot des zweiten Kreditors, und speichern Sie es. | Eingegangen          | Eingegangen           | Eingegangen                 | Eingegangen                  | Eingegangen               | Empfangen |

> [!NOTE]
> Wenn Sie ein Angebot zur weiteren Verhandlung an den Kreditor zurücksenden, bleiben der niedrigste und höchste Status **Erhalten**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Angebote annehmen und ablehnen sowie angenommene Angebote an Downstreamdokumente übertragen

Nach Ermittlung des besten Angebots – beispielsweise des Angebots mit dem besten Gesamtpreis – akzeptieren Sie es. Sie können manche Positionen in einem Angebot annehmen und andere ablehnen. Sie können auch Positionen von verschiedenen Kreditoren akzeptieren. Beachten Sie, dass wenn Sie manche Positionen annehmen, Sie dazu aufgefordert werden, alle anderen Positionen abzulehnen. Wenn Sie andere Positionen annehmen möchten, müssen Sie daher **Abbrechen** auswählen, wenn Sie die dazu aufgefordert werden. Der Status der Angebotsanforderungsantwort für jeden Kreditor, von dem Sie Angebote oder Positionen annehmen, wird auf **Angenommen** aktualisiert. 

Wenn Sie ein Angebot oder bestimmte Positionen in einem Angebot annehmen, wird automatisch eine Bestellung oder ein Kaufvertrag generiert. Sie können dann die Angebote von allen anderen Kreditoren ablehnen.

In der Antwort können Sie einen Ursachencode hinzufügen, um zu erläutern, warum Sie ein Angebot angenommen oder abgelehnt haben.

Wenn Sie eine Angebotsanforderungsantwort vom Typ **Bestellanforderung** annehmen, aktualisieren die Angebotsanforderungspositionen die Bestellanforderungspositionen mit den folgenden Informationen:

- Preis je Einheit
- Rabattprozentsatz
- Rabattbetrag
- Einkaufszuschläge
- Positionsgebühren
- Lieferant
- Externe Nummer
- Externe Beschreibung

In der folgenden Tabelle wird angezeigt, wie sich der Angebotsanforderungs-Status ändert, während Sie Angebote von Kreditoren annehmen und ablehnen.

| Vorgang                      | Niedrigster Angebotsstatus | Höchster Angebotsstatus | Niedrigster Status des Angebotsanforderungskopfes | Höchster Status der Angebotsanforderungskopfzeile | Niedrigster Status einer Angebotsanforderungszeile | Höchster Status einer Angebotsanforderungszeile |
|-------------------------    |-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Nehmen Sie eines derAngebote an.     | Eingegangen          | Angenommen           | Eingegangen                 | Angenommen                  | Eingegangen               | Angenommen |
| Lehnen Sie alle anderen Angebote ab.  | Verweigert          | Angenommen           | Verweigert                 | Angenommen                  | Verweigert               | Akzeptiert |

