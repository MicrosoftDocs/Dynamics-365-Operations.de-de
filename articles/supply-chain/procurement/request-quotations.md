---
title: Angebotsanforderungen
description: "Dieses Thema bietet einen Überblick über Angebotsanforderungen (RFQs/requests for quotation), die Organisationen ausstellen, um vor einem Einkauf von mehreren Kreditoren Angebote für Artikel oder Dienstleistungen zwecks Vergleich anzufordern."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8b817ffd905f1d3e99befc149416006e1a51f5e2
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="request-for-quotations-rfqs"></a>Angebotsanforderungen

[!include[banner](../includes/banner.md)]


Dieses Thema bietet einen Überblick über Angebotsanforderungen (RFQs/requests for quotation), die Organisationen ausstellen, um vor einem Einkauf von mehreren Kreditoren Angebote für Artikel oder Dienstleistungen zwecks Vergleich anzufordern. Mit einer Angebotsanforderung werden Kreditoren gebeten, Preise und Lieferzeiten für die angegebenen Produktmengen bereitzustellen. Sie können Kreditoren auch bitten, anzugeben, ob zusätzliche Gebühren, etwa Lieferkosten, anfallen, oder ob der Kreditor Rabatte für große Bestellungen oder bei frühzeitiger Bezahlung der Rechnung anbietet.

Der Angebotsanforderungsprozess umfasst die folgenden Aufgaben:

-   Erstellen und Senden einer Angebotsanforderung an einen oder mehrere Kreditoren
-   Erhalten und Erfassen von Antworten auf Angebotsanforderungen.
-   Übertragen der akzeptierten Angebote auf eine Bestellung, einen Kaufvertrag oder eine Bestellanforderung.

Die folgende Abbildung bietet eine Übersicht über den Angebotsanforderungsprozess.  

[![Angebotsanforderungsprozess](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)  

Sie können eine Angebotsanforderung aus geplanten Aufträgen, einer Bestellanforderung oder aus einem manuellen Eintrag erstellen. Die Angebotsanforderung, die Sie erstellen, wird als Angebotsanforderungsanfrage bezeichnet und dies ist das Basisdokument, das Sie verwenden, um eine Angebotsanforderung an jedem Kreditor auszustellen. Nachdem die Angebotsanforderungsanfrage vorbereiten und Kreditoren hinzufügen, wird auf **Übermitteln** im Angebotsanforderungsanfrage und für jeden Kreditor eine Angebotsanforderungserfassung erstellt, für den die Angebotsanforderung zu schickten. Druckverwaltungseinstellungen können Sie die für die Sendenaktivität entweder von Scheckbegleitschreiben ein Bericht für jeden Kreditor in einem Archiv konfigurieren oder einen Bericht an die E-Mail-Adresse jedes Kreditors gesendet. Außerdem kann die Angebotsanforderungserfassung für jeden Kreditor verwendet werden, um einen Bericht zu generieren, den Sie später an einen Kreditor senden oder erneut senden können. Sie können die Aktion "Senden" auch so konfigurieren, dass ein Antwortbogen generiert wird, den der Kreditor ausfüllen kann.  

Wenn Sie eine Angebotsanforderung ergänzen müssen, nachdem Sie diese senden, können Sie die Angebotsanforderung erneut an Kreditoren senden, wenn Sie fertig sind.  

Wenn Sie Angebote erhalten, müssen Sie sie auf der Seite **Antworten auf Angebotsanforderung** eingeben. Wenn Sie die Option **Daten in Antwort kopieren** auswählen, werden Daten, wie die Menge und Daten aus der Angebotsanforderungsanfrage in die Antwort kopiert. Sie können diese Daten ändern, um das Angebot des Kreditors widerzuspiegeln.  

Wenn eine zweite Iteration einer Antwort für einen bestimmten Kreditor erforderlich ist, klicken Sie auf **Zurück** auf der Seite **Antwort auf Angebotsanforderung**. Die Aktion "Zurück" generiert eine neue Erfassung und einen Bericht, die gemäß den Druckverwaltungseinstellungen gedruckt, archiviert und gesendet werden.  

Wenn Sie Bewertungskriterien zu Ihrer Angebotsanforderungsanfrage hinzugefügt haben, hat die Antwort auf Angebotsanforderung einen Bewertungsbereich, in dem Sie die Punktzahlen eingeben können. Die Gesamtpunktzahlen werden angezeigt, wenn Sie die Antworten auf der Seite **Antworten vergleichen** vergleichen, wo Sie auch andere Antwortdaten vergleichen können, wie beispielsweise den Positionspreis, das Lieferdatum und den Gesamtpreis.  

Nachdem Sie sich zu einem Angebot oder Teilangeboten entscheiden, können Sie diese annehmen und die restlichen ablehnen. Annahmenerfassungen, Ablehnungserfassungen und entsprechende Berichte werden generiert. Diese werden gemäß Ihren Druckverwaltungseinstellungen gedruckt, archiviert und übermittelt. Wenn Sie ein Angebot oder bestimmte Positionen in einem Angebot akzeptieren, wird entweder ein Kaufvertrag oder eine Bestellung generiert, oder eine Bestellanforderung wird aktualisiert, je nach Bestelltyp der Angebotsanforderung. Sie können eine Handelsvereinbarung erstellen, die Sie später für jede der Antworten verwenden können, unabhängig davon, ob Sie diese akzeptiert oder zurückgewiesen haben.  

Der Status einer Angebotsanforderung wird im Angebotsanforderungskopf angezeigt und hängt vom Status der Angebotsanforderungspositionen ab. Der Status gibt an, wie weit die Verarbeitung der Angebotsanforderung fortgeschritten ist. Jede Angebotsanforderung besitzt zwei Werte für den Status: den niedrigsten und denhöchsten. Der niedrigste Status steht für die am wenigsten fortgeschrittene Phase und der höchste Status für die am weitesten fortgeschrittene Phase einer Position in der Angebotsanforderung. Wenn beispielsweise die am wenigsten fortgeschrittene Phase in einer Angebotsanforderung für eine Position besteht, die erstellt wurde, ist der niedrigste Status für die Angebotsanforderung **Erstellt**. Wenn die am weitesten fortgeschrittene Phase in der Angebotsanforderung für eine Position besteht, die an Kreditoren gesendet wurde, ist der höchste Status für die Angebotsanforderung **Versendet**. Die Statusangaben werden bei der Verarbeitung einer Angebotsanforderung automatisch aktualisiert.  

Sie können den niedrigsten und höchsten Status eines Angebotsanforderungskopfs auf der Seite **Alle Angebotsanforderungen** anzeigen. Sie können den niedrigsten und höchsten Status einer Angebotsanforderungsposition auf der Registerkarte **Positionen** auf der Seite **Angebotsanforderungen** anzeigen.  

Hier ist die Reihenfolge der Statusangaben bei der Verarbeitung einer Angebotsanforderung:

1.  **Erstellt**
2.  **Versendet**
3.  **Eingegangen**
4.  **Angenommen**/**Storniert**/**Abgelehnt**

Die Statusangaben werden detaillierter in späteren Abschnitten dieses Themas beschrieben.

## <a name="setting-up-rfq-functionality"></a>Einrichten von Angebotsanforderungsfunktionen
Bevor Sie eine Angebotsanforderungsanfrage erstellen können, müssen Sie Angebotsanforderungsinformationen auf der Seite **Beschaffungsparameter** einrichten. Wenn Sie eine Angebotsanforderungsanfrage erstellen, können Sie die Standardwerte angeben, die in die Angebotsanforderung kopiert werden. Sie können die folgenden Standardwerte angeben:

-   Der Bestelltyp neuer Angebotsanforderungen: **Bestellung** oder **Kaufvertrag**.
-   Einstellungen für Ablaufdatum und -uhrzeit.
-   Lieferinformationen und Zahlungsbedingungen.
-   Felder, die in der Antwort auf Angebotsanforderung einbezogen werden sollen.

Sie können diese Werte für eine bestimmte Angebotsanforderungsanfrage überschreiben. Sie sollten auch den Ergänzungsprozess konfigurieren. Als Teil dieser Konfiguration können Sie Feldsperre aktivieren. Wenn die Feldsperre aktiviert ist, muss ein Beschaffungsspezialist, der eine Angebotsanforderung ergänzen möchte, erst auf **Erstellen** im Abschnitt **Zusatz** auf der Registerkarte **Angebot** klicken. Nachdem die Angebotsanforderung durch den Zusatz ergänzt wurde, muss der Beschaffungsspezialist den Vorgang abschließen, indem er auf **Abschließen** klickt. Durch die Aktivität **Abschließen** wird eine E-Mail-Nachricht generiert, die Kreditoren über die ergänzte Angebotsanforderung benachrichtigt. Sie wählen die Vorlage für die E-Mail-Benachrichtigung aus, die an Kreditoren auf der Seite **Beschaffungsparameter** gesendet wird. Wenn eine Vorlage erstellt wird, kann sie die folgenden Ersatztoken enthalten:

-   %Grund für Rücksendung des Angebots%
-   %Grund für den Zusatz%
-   %Zusatz erstellt von%
-   %Unternehmen%

Die Tokens %Grund für Angebotrücksendung% und %Grund für Ergänzung% werden durch Text ersetzt, die der Beschaffungsspezialist eingeben kann, wenn er oder sie die Ergänzung im Assistenten **Ergänzung** abschließt. Die Werte für die Tokens %Ergänzung vorbereitet von% und %Unternehmen% werden automatisch aus der Angebotsanforderung übernommen.  

Wenn Sie Ursachencodes für eine Angebotsanforderungsantwort verwenden möchten, um anzugeben, um anzugeben, warum ein Angebot angenommen oder abgelehnt wurde, müssen Sie Ursachencodes auf der Seite **Ursachen für Kreditorenbuchungen** einrichten.  

Sie können die Darstellung Ihrer gedruckten oder gespeicherten Angebotsanforderungsdokumente auf der Seite **Formulareinstellungen** in "Beschaffung" konfigurieren. 

**Hinweis:** Für eine Konfiguration für den öffentlichen Sektor erfordern sämtliche Änderungen an einer Angebotsanforderung, die bereits gesendet wurde, die Verwendung eines Ergänzungsprozesses. Wenn die Angebotsanforderung gesendet wird, werden Felder gesperrt. Das Klicken auf **Erstellen**, um den Ergänzungsprozess wie oben beschrieben zu verwenden, ist somit ein obligatorischer Schritt, um Änderungen an der Angebotsanforderung vorzunehmen.
Dies wird durch den Feldsperrungsparameter **Angebotsanforderung sperren, wenn diese gesendet werden** in **Beschaffungsparameter** gesteuert. Dieser Parameter ist auf **Ja** festgelegt, und für eine Konfiguration für den öffentlichen Sektor ist dies ein Standard, der nicht geändert werden kann. Das bedeutet, dass, während der Ergänzungsprozess in einer Konfiguration, die nicht für den öffentlichen Sektor ist, manuell gehandhabt werden kann, der Prozess der Handhabung von Ergänzungen durch das Sperren von Feldern nach dem Senden der Angebotsanforderung im öffentlichen Sektor obligatorisch ist.

Wenn Sie eine Angebotsanforderung für eine Bestellung erstellen und einen Lagerartikel zur Angebotsanforderung hinzufügen, wird eine Lagerbuchung mit dem Zugangsstatus **Angebotszugang** erstellt. Es werden nur Angebotsanforderungspositionen mit diesem Status berücksichtigt, wenn Sie einen Produktprogrammplan verwenden, um den Bestand zu berechnen. Wenn Sie möchten, dass der Produktprogrammplan Angebotsanforderungspositionen als erwarteten Zugang umfasst, müssen Sie dieses Verhalten in den Einstellungen des Produktprogrammplans konfigurieren.  

Als Einkaufsleiter oder Agent können Sie Anfragentypen erstellen und verwalten, die zu den Beschaffungsanforderungen Ihrer Organisation passen. Jeder Anfragentyp kann Bewertungsmethoden treiben. Bewertungsmethoden bestehen aus einem Satz von Kriterien, die verwendet werden können, wenn Sie Angebote bewerten. Sie müssen Anfragentypen, Bewertungsmethoden und Bewertungskriterien auf den Seiten **Anfragentyp** und **Bewertungsmethode** einrichten.

## <a name="creating-and-sending-an-rfq"></a>Eine Angebotsanforderung erstellen und senden
Sie erstellen eine Angebotsanforderung, wählen die Kreditoren aus, die auf die Angebotsanforderung antworten sollen, und senden die Angebotsanforderung dann an die Kreditoren. Sie können die Druckverwaltung verwenden, um den Angebotsanforderungsbericht und Antwortbogenberichte an Ihr bevorzugtes Ziel weiterzuleiten.  

Sie können eine Angebotsanforderung für die **Bestellung** oder den **Kaufvertrag** erstellen.  

Wenn die Angebotsanfordernung aus einer Bestellanforderung generiert wird, wird der Typ **Bestellanforderung** automatisch zugewiesen. Sie können eine Angebotsanforderung vom Typ **Bestellanforderung** nicht manuell erstellen. Wenn die Angebotsanforderung vom Typ **Bestellung** ist:

-   Wenn Angebotsanforderungspositionen erstellt werden, werden Lagerbuchungen generiert, die den Zugangsstatus von **Angebotszugang** besitzen.
-   Wenn Sie ein Angebot akzeptieren, wird eine Bestellung generiert.

Wenn die Angebotsanforderung vom Typ **Kaufvertrag** ist:

-   Die Angebotsanforderung wird für eine Vereinbarung zum Einkauf einer bestimmten Produktmenge oder eines bestimmten Produktwerts über einen gewissen Zeitraum verwendet. Sie müssen den Datumsbereich auswählen, der für den Kaufvertrag und den Namen des Mitarbeiters gilt, der mit der Verwaltung der Rahmenbestellung betraut ist.
-   Wenn Sie ein Angebot annehmen, wird ein Kaufvertrag generiert.

Sie können nur eine Angebotsanforderung aus einer Bestellanforderung erstellen, wenn der Status der Bestellanforderung **Wird überprüft** ist und Ihnen die Erledigung der nächsten Workflowaufgabe zugewiesen ist. Die Positionen der Bestellanforderung werden automatisch aktualisiert, wenn Sie Positionen aus den Antworten auf Angebotsanforderung (Angebote) annehmen die Sie von Kreditoren erhalten haben. Solange sich eine Angebotsanforderung in Bearbeitung befindet, können Sie eine Bestellanforderung also weder abschließen, ablehnen, genehmigen, noch irgendwelche anderen Aktionen an ihr ausführen.  

Wenn Sie eine Angebotsanforderung erstellen, können Sie einen bestimmten Anfragentyp auswählen. Der Anfragentyp bestimmt die Gruppe von Bewertungskriterien, die verwendet wird, um Antworten auf die Angebotsanforderung zu bewerten.  

Sie können einer Angebotsanforderungsanfrage einen Fragebogen hinzufügen. Dieser Fragebogen wird dann auf allen Antworten angezeigt, nachdem Sie die Angebotsanforderung senden.  

Es gibt drei Möglichkeiten, um die Kreditoren auswählen, die einer Angebotsanforderungsanfrage hinzugefügt werden sollen:

-   Fügen Sie die Kreditoren nacheinander hinzu.
-   Suchen Sie nach allen Kreditoren, die bestimmten Kriterien entsprechen.
-   Fügen Sie automatisch alle Kreditoren hinzu, die für die Beschaffungskategorien, die bei den Angebotsanforderungspositionen verwendet werden, genehmigt sind.

Wenn die Angebotsanforderungsanfrage bereit ist, klicken Sie auf **Senden**. Die Aktion "Senden" generiert Erfassungen und Berichte, die gemäß den Druckverwaltungseinstellungen gedruckt, archiviert und gesendet werden.  

Wenn Sie die Kontrollkästchen **Kreditor zur Neuberechnung von Preisen verwenden** und **Kreditorenspezifische Artikelinformationen verwenden** auf der Seite **Angebotsanforderung wird gesendet.** aktiviert haben, wenn Sie die Anforderung an Kreditoren schickten, werden einige kreditorenspezifische Informationen automatisch eingegeben. Sie können diese Informationen auf der Seite **Antwort auf Angebotsanforderung** ändern.  

In der folgenden Tabelle wird angezeigt, wie sich der Angebotsanforderungsstatus ändert, wenn Sie eine Angebotsanforderung erstellen und sie an Kreditoren senden.

|                                    |                              |                                                 |                            |                             |
|------------------------------------|------------------------------|-------------------------------------------------|----------------------------|-----------------------------|
| **Aktion**                         | **Niedrigster Status des Angebotsanforderungskopfes** | **Höchster Status des Angebotsanforderungskopfes**                   | **Niedrigster Status einer Angebotsanforderungsposition** | **Höchster Status einer Angebotsanforderungsposition** |
| Erstellen Sie den Angebotsanforderungskopf und die -position.    | Erstellt                      | Erstellt                                         | Erstellt                    | Erstellt                     |
| Senden Sie die Angebotsanforderung an einen bestimmten Kreditor. | Versendet                         | Versendet                                            | Versendet                       | Versendet                        |
| Einen weiteren Kreditor hinzufügen                | Erstellt                      | Versendet (Die Angebotsanforderung ist nur einem Kreditor zugesendet worden). | Erstellt                    | Versendet                        |
| Senden Sie die Angebotsanforderung an den zweiten Kreditor. | Versendet                         | Versendet                                            | Versendet                       | Versendet                        |

**Hinweis:** Sie können einer Angebotsanforderung jederzeit weitere Kreditoren hinzufügen. Der höchste und der niedrigste Status ändern sich, um die neuen Kreditoren widerzuspiegeln. Wenn Sie z. B. ein Angebot von allen Kreditoren erhalten und mindestens eine Position in dem Angebot akzeptiert haben, lautet der niedrigste Status im Kopf der Angebotsanforderung **Abgelehnt** und der höchste Status ist **Angenommen**. Wenn Sie einen neuen Kreditor hinzufügen, ist der niedrigste Status in jeder beliebigen Position jetzt **Erstellt**. Daher ändert sich der niedrigste Status im Angebotsanforderungskopf zu **Erstellt** und der höchste Status ändert sich zu **Angenommen**.

## <a name="amending-an-rfq"></a>Ergänzen einer Angebotsanforderung
Gelegentlich müssen Sie eine Angebotsanforderung ändern, nachdem Sie sie gesendet haben. Dieser Fall kann beispielsweise eintreten, wenn sich die Lieferdaten geändert haben oder Sie zusätzliche Produkte oder andere Mengen von Produkte möchten. Sie können den Ergänzungsprozess so konfigurieren, dass er entweder einschränkender oder weniger einschränkend ist.  

Wenn Sie den einschränkenderen Ergänzungsprozess verwenden, müssen Sie auf **Erstellen** auf der Angebotsanforderungsanfrage klicken, um eine Ergänzung zu starten, bevor Sie die Felder in der Angebotsanforderungsanfrage ändern können. Nachdem Sie Ihre Änderungen vorgenommen haben, müssen Sie auf **Abschließen** klicken. Sie werden dann durch den Prozess zum Hinzufügen von Informationen für die E-Mail-Nachricht geführt, die gesendet wird, um Kreditoren zur Ergänzung zu informieren. Der aktualisierte Angebotsanforderungsbericht, der einen Ergänzungshinweis umfasst, wird automatisch der Nachricht zugeordnet.  

Wenn Sie den weniger einschränkenden Ergänzungsprozess verwenden, müssen Sie keine Ergänzung erstellen, bevor Sie die Felder auf einer Angebotsanforderungsanfrage ändern können, die bereits übermittelt wurde. Sie müssen allerdings einen Ergänzungshinweis zur Angebotsanforderung manuell hinzufügen.

## <a name="receiving-and-registering-rfq-replies"></a>Erhalten und Erfassen von Antworten auf Angebotsanforderungen
Wenn Sie eine Angebotsanforderung senden, wird automatisch ein Antwortblatt generiert. Wenn Sie Antworten (Angebote) auf eine Angebotsanforderung erhalten, müssen Sie die Antwortinformationen der einzelnen Kreditoren in einen kreditorenspezifischen Antwortbogen auf Angebotsanforderung eingeben. Wenn Sie Bewertungskriterien hinzugefügt haben, können Sie die Antworten bewerten. Sie vergleichen dann die Kreditorenangebote, indem Sie sie anhand Ihrer Bewertungskriterien, wie bester Gesamtpreis oder beste Gesamtlieferzeit, sortieren.  

Wenn ein Fragebogen der Angebotsanforderungsanfrage zugeordnet ist, müssen Sie die Antworten auf die Fragen im Antwortbogen manuell eingeben.  

Wenn Sie alternative Positionen eingeben müssen und die Angebotsanforderungsanfrage dies zulässt, klicken Sie im Inforegister **Bestellanforderungspositionen** auf **Position hinzufügen**. Geben Sie dann die Produktinformationen ein, beispielsweise Artikelnummer oder Beschaffungskategorie, Menge, Preis und Rabatt.  

Wenn Sie eine Antwort eingegeben, aber ein neues Angebot vom Kreditor anfordern haben, können Sie die Angebotsanforderung erneut senden. Dadurch wird eine neue Erfassung erstellen und Berichte, die Sie verwenden können, um Änderungen vom Kreditor anzufordern.  

Sie können eine Übersicht über alle Angebotsanforderungen und deren Antwortstatus auf der Seite **Weiterverfolgung der Angebotsanforderung** anzeigen.  

In der folgenden Tabelle wird angezeigt, wie der Angebotsanforderungsstatus sich ändert, während Sie Angebote empfangen und die Informationen im Antwortbogen für Angebotsanforderung erfassen.

|                                                |                       |                        |                              |                               |                            |                             |
|------------------------------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Aktion**                                     | **Niedrigster Angebotsstatus** | **Höchster Angebotsstatus** | **Niedrigster Status des Angebotsanforderungskopfes** | **Höchster Status des Angebotsanforderungskopfes** | **Niedrigster Status einer Angebotsanforderungsposition** | **Höchster Status einer Angebotsanforderungsposition** |
| Erfassen Sie das ein Angebot eines Kreditors, und speichern Sie es.        | Versendet                  | Empfangen               | Versendet                         | Empfangen                      | Versendet                       | Empfangen                    |
| Erfassen Sie das ein Angebot des zweiten Kreditors, und speichern Sie es. | Empfangen              | Empfangen               | Empfangen                     | Empfangen                      | Empfangen                   | Empfangen                    |

**Hinweis:** Wenn Sie ein Angebot zur weiteren Verhandlung an den Kreditor zurücksenden, bleiben der niedrigste und höchste Status **Erhalten**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Angebote annehmen und ablehnen sowie angenommene Angebote an Downstreamdokumente übertragen

Nach Ermittlung des besten Angebots – beispielsweise des Angebots mit dem besten Gesamtpreis – akzeptieren Sie es. Der Status der Antwort auf die Angebotsanforderung für diesen Kreditor wird in **Angenommen** aktualisiert. Wenn Sie ein Angebot oder bestimmte Positionen in einem Angebot annehmen, wird automatisch eine Bestellung oder ein Kaufvertrag generiert, und sie können die Angebote von den anderen Kreditoren ablehnen.  

Wenn Sie eine Angebotsanforderungsantwort vom Typ **Bestellanforderung** annehmen, aktualisieren die Angebotsanforderungspositionen die Bestellanforderungspositionen mit den folgenden Informationen:

-   Preis je Einheit
-   Rabattprozentsatz
-   Rabattbetrag
-   Einkaufszuschläge
-   Positionsgebühren
-   Händler
-   Externe Nummer
-   Externe Beschreibung

In der Antwort können Sie einen Ursachencode hinzufügen, um zu erläutern, warum Sie ein Angebot angenommen oder abgelehnt haben.  

Sie können manche Positionen in einem Angebot annehmen und andere ablehnen. Sie können auch Positionen von verschiedenen Kreditoren akzeptieren. Beachten Sie, dass wenn Sie manche Positionen annehmen, Sie dazu aufgefordert werden, alle anderen Positionen abzulehnen. Wenn Sie andere Positionen annehmen möchten, müssen Sie daher auf **Abbrechen** klicken, wenn Sie die Eingabeaufforderung erhalten.  

In der folgenden Tabelle wird angezeigt, wie sich der Angebotsanforderungs-Status ändert, während Sie Angebote von Kreditoren annehmen und ablehnen.

|                         |                       |                        |                              |                               |                            |                             |
|-------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Aktivität**              | **Niedrigster Angebotsstatus** | **Höchster Angebotsstatus** | **Niedrigster Status des Angebotsanforderungskopfes** | **Höchster Status des Angebotsanforderungskopfes** | **Niedrigster Status einer Angebotsanforderungsposition** | **Höchster Status einer Angebotsanforderungsposition** |
| Nehmen Sie eines derAngebote an. | Empfangen              | Akzeptiert               | Empfangen                     | Akzeptiert                      | Empfangen                   | Akzeptiert                    |
| Lehnen Sie die anderen Angebote ab.  | Abgelehnt              | Akzeptiert               | Abgelehnt                     | Akzeptiert                      | Abgelehnt                   | Akzeptiert                    |






