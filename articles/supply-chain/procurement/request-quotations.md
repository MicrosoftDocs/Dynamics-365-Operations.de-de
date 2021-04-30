---
title: Übersicht über Angebotsanfragen (RFQs)
description: Dieses Thema bietet eine Übersicht über Angebotsanforderungen. Organisationen stellen eine Angebotsanforderung aus, um von mehreren Kreditoren Angebote für die Artikel oder Dienstleistungen, die sie kaufen müssen, zwecks Vergleich anzufordern.
author: kamaybac
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage, BOMExpandPurchRFQ, PurchRFQReplyFollowupItem, PurchRFQCaseVend, PurchRFQReplyFollowup, PurchRFQCaseAmendmentInfo, PurchRFQReplyFollowupCase, PurchRFQReplyStatus, PurchRFQCaseReplyFields, PurchRFQAddQuestionnaire, PurchRFQAmendmentWizard, PurchRFQReplyTableStatus, PurchRFQReplyTableListPage, PurchRFQCancelWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48830c975f1bdfd953f57e7c0b6601a78e3a521b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910038"
---
# <a name="requests-for-quotation-rfqs-overview"></a>Übersicht über Angebotsanfragen (RFQs)

[!include [banner](../includes/banner.md)]

Dieses Thema bietet eine Übersicht über Angebotsanforderungen. Organisationen stellen eine Angebotsanforderung aus, um von mehreren Kreditoren Angebote für die Artikel oder Dienstleistungen, die sie kaufen müssen, zwecks Vergleich anzufordern. Mit einer Angebotsanforderung werden Kreditoren gebeten, Preise und Lieferzeiten für die angegebenen Produktmengen bereitzustellen.
Sie können Kreditoren auch bitten, anzugeben, ob zusätzliche Gebühren, etwa Lieferkosten, anfallen, oder ob der Kreditor Rabatte für große Bestellungen oder bei frühzeitiger Bezahlung der Rechnung anbietet.

Der Angebotsanforderungsprozess besteht aus den folgenden Aufgaben:

1. Erstellen und senden Sie eine Angebotsanforderung an einen oder mehrere Kreditoren.
1. Erhalten und erfassen Sie Antworten auf Angebote (Angebotsanforderung).
1. Übertragen Sie Angebote, die Sie akzeptieren, auf eine Bestellung, einen Kaufvertrag oder eine Bestellanforderung.

Die folgende Abbildung zeigt eine Übersicht über den Angebotsanforderungsprozess.

[![RFQ-Prozess](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Sie können eine Angebotsanforderung aus geplanten Aufträgen, einer Bestellanforderung oder durch einen manuellen Eintrag erstellen. Die Angebotsanforderung ist das Basisdokument, dass Sie verwenden, um eine Angebotsanforderung für jeden Lieferanten auszugeben.

Nachdem Sie die Angebotsanforderungsanfrage vorbereitet und Kreditoren hinzugefügt haben, wählen Sie **Senden** (**Senden und Veröffentlichen** für den öffentlichen Sektor) in der  Angebotsanforderungsanfrage. Eine Angebotsanforderungserfassung wird für jeden Kreditor generiert, an den Sie eine Angebotsanforderung senden. Sie können die Druckverwaltungseinstellung für die Sendeaktivität so konfigurieren, dass entweder ein Bericht für jeden Kreditor in ein Archiv ausgedruckt wird oder ein Bericht an die E-Mail-Adresse jedes Kreditors gesendet wird. Außerdem können Sie die Angebotsanforderungserfassung für jeden Kreditor verwenden, um einen Bericht zu generieren, den Sie später an den Kreditor senden oder erneut senden können. Sie können die Aktivität „Senden” auch so konfigurieren, dass ein Antwortbogen generiert wird, den der Kreditor ausfüllen kann.

Dieses Thema behandelt den Prozess der Handhabung von Angebotsanforderungen, wenn die Kreditorenzusammenarbeit nicht verwendet wird. Wenn Ihr System für Kreditorenzusammenarbeit eingerichtet ist, können Kreditoren Angebote direkt in Supply Chain Management eingeben. Weitere Informationen über die Kreditorenzusammenarbeit finden Sie unter [Kreditorenzusammenarbeit mit externen Kreditoren](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations) und [Kreditorenzusammenarbeit mit Kunden](vendor-collaboration-work-external-vendors.md).

Wenn Sie eine Angebotsanforderung ergänzen müssen, nachdem sie übermittelt wurde, können Sie die Angebotsanforderung an Lieferanten erneut senden, wenn Sie fertig sind. Dazu verwenden Sie die beiden Zusatzaktivitäten: Erstellen und Abschließen.

Wenn Sie Angebote per E-Mail erhalten, müssen Sie diese Angebote auf der Seite **Antworten auf Angebotsanforderung** eingeben.

Wenn eine zweite Iteration von einer Antwort für einen bestimmten Kreditor erforderlich ist, klicken Sie auf **Zurück** auf der Seite **Antwort auf Angebotsanforderung**. Die Aktion „Zurück” generiert eine neue Erfassung und einen Bericht, der gemäß den Druckverwaltungseinstellungen gedruckt, archiviert und gesendet werden.

Wenn Sie Bewertungskriterien zu Ihrer Angebotsanforderungsanfrage hinzugefügt haben, hat die Antwort auf die Angebotsanforderung einen Bewertungsbereich, in dem Sie die Punktzahlen eingeben können. Die Gesamtbewertungen werden in der Angebotsanforderung angezeigt, wenn Sie die Antworten auf der Seite **Antworten vergleichen** vergleichen. Auf dieser Seite können Sie auch **Antwortdaten vergleichen**, wie beispielsweise den Positionspreis, das Lieferdatum und den Gesamtpreis.

Nachdem Sie ein Angebot oder mehrere Positionen in einem Angebot ausgewählt haben, können Sie einige oder alle Positionen übernehmen und die restliche ablehnen. Annahmeerfassungen, Ablehnungserfassungen und entsprechende Berichte werden generiert und  gemäß den Druckverwaltungseinstellungen gedruckt, archiviert und gesendet werden. Wenn Sie ein Angebot oder bestimmte Positionen in einem Angebot annehmen, wird entweder ein Kaufvertrag oder eine Bestellung generiert, oder eine Bestellanforderung wird aktualisiert, je nach Bestelltyp der Angebotsanforderung. Sie können eine Handelsvereinbarung erstellen, die Sie später für jede der Antworten verwenden können, unabhängig davon, ob Sie diese akzeptiert oder zurückgewiesen haben.

Eine Angebotsanforderung hat zwei Stati: den niedrigsten und den höchsten Status, Sie sehen den Status auf der Listenseite für **Alle Angebotsanforderungen** anzeigen. Der niedrigste Status steht für die am wenigsten fortgeschrittene Phase  in der Angebotsanforderung und der höchste Status für die am weitesten fortgeschrittene Phase einer Position in der Angebotsanforderung. Beispielsweise wird eine Angebotsanforderung mit drei Positionen an zwei Kreditoren gesendet und so gibt es zwei Angebotsanforderungen mit je drei Positionen. Alle Positionen sind **Versendet**. Nun wird ein Angebot von einem der Kreditoren erfasst und die Angebotsanforderungspositionen erhält den Status **Eingegangen**. Das bedeutet, dass von den drei Positionen auf der Angebotsanforderungsanfrage, alle für eine Angebotsanforderung **Versendet** und für eine andere Angebotsanforderungen **Eingegangen** sind. Der niedrigste Status ist dann **Versendet** und der höchste Status ist **Empfangen.**

Diese Statusangaben werden detaillierter später in diesem Thema beschrieben.

## <a name="setting-up-rfq-functionality"></a>Einrichten von Angebotsanforderungsfunktionen

Bevor Sie eine Angebotsanforderungsanfrage erstellen können, müssen Sie Angebotsanforderungsinformationen auf der Seite **Beschaffungsparameter** einrichten. Wenn Sie eine Angebotsanforderungsanfrage erstellen, können Sie die Standardwerte angeben, die in die Angebotsanforderung kopiert werden. Sie können die folgenden Standardwerte angeben:

- Der Bestelltyp neuer Angebotsanforderungen: **Bestellung** oder **Kaufvertrag**
- Das Ablaufdatum und das Zeitgegenkonto ab dem Zeitpunkt der Angebotsanforderung wird erstellt.
- Anfragetyp, der der Angebotsanforderung eine bestimmte Bewertungsmethode vorgeben kann.
- Lieferinformationen und Zahlungsbedingungen.

Sie können diese Werte für eine bestimmte Angebotsanforderungsanfrage überschreiben.

Sie sollten auch den Ergänzungsprozess konfigurieren. Als Teil dieser Konfiguration können Sie Feldsperre aktivieren. Wenn die Feldsperre aktiviert ist, muss ein Beschaffungsspezialist, der eine Angebotsanforderung ergänzen möchte, zuerst auf **Erstellen** im Abschnitt  **Ergänzung** auf der Registerkarte **Angebot** klicken. Nachdem die Angebotsanforderung mit der Ergänzung aktualisiert wurde, muss der Beschaffungsspezialist den Prozess abschließen, indem er noch auf **Abschließen** klickt. Durch die Aktivität „Abschließen” wird eine E-Mail-Nachricht generiert, die Kreditoren über die ergänzte Angebotsanforderung benachrichtigt.

Auf der Seite **Beschaffungsparameter** wählen Sie die Vorlage für die E-Mail-Benachrichtigung aus, die an Kreditoren gesendet wird. Wenn eine Vorlage in den **E-Mail-Vorlagen** erstellt wird, kann sie die folgenden Ersatztoken enthalten:

- %Angebotsanforderungsanfrage%
- %Grund für Rücksendung des Angebots%
- %Grund für den Zusatz%
- %Zusatz erstellt von%
- %Company%
- %Name der Angebotsanforderungsanfrage%
- %Gültig bis%
- %Date%

Die Tokens %Grund für Angebotrücksendung% und %Grund für Ergänzung% werden durch Text ersetzt, die der Beschaffungsspezialist eingeben kann, wenn er oder sie die Ergänzung im Assistenten **Ergänzung** abschließt. Die Werte für die Token %Amendment prepared by% und %Company% werden automatisch aus der RFQ übernommen. Das %Date%-Zeichen wird durch das aktuelle Datum ersetzt.

Wenn Sie eine Angebotsanforderung löschen möchten, nachdem sie versendet wurde, können Sie das über den Angebotsanforderungsfall tun. Für die Stornierung ist eine E-Mail-Vorlage erforderlich, um die Stornierungsbenachrichtigung an Kontaktpersonen des Kreditors zu senden. Die Vorlage muss auf der Seite **Beschaffungsparameter** ausgewählt werden. Wenn die Vorlage erstellt ist, kann sie die folgenden Ersatztoken enthalten:

- %Stornierungsgrund%
- %Angebotsanforderungsanfrage%
- %Angebotsanforderung storniert von%
- %Company%
- %Name der Angebotsanforderungsanfrage%
- %Date%

Das Token %Grund für Stornierung% wird von Text ersetzt, den der Prokurist im **Stornierungs**-Assistenten eingeben kann. Das %Date%-Zeichen wird durch das aktuelle Datum ersetzt.

Wenn Sie Ursachencodes für eine Angebotsanforderungsantwort verwenden möchten, um anzugeben, warum ein Angebot angenommen oder abgelehnt wurde, müssen Sie Ursachencodes auf der Seite **Ursachen für Kreditorenbuchungen** einrichten.

Auf der Seite **Formulareinstellungen** in „Beschaffung” können Sie die Darstellung Ihrer gedruckten oder gespeicherten Angebotsanforderungsdokumente konfigurieren.

> [!NOTE]
> Für eine Konfiguration für den öffentlichen Sektor müssen Sie den Ergänzungsprozess verwenden, um eine Angebotsanforderung zu ändern, die bereits gesendet wurde. Wenn eine Angebotsanforderung gesendet wird, sind Felder gesperrt.
Um an der Angebotsanforderung Änderungen vornehmen zu können, müssen Sie daher **Erstellen** auswählen, um den Ergänzungsprozess zu beginnen, der zuvor beschrieben wurde. Das Sperrungsverhalten wird von der Option **Angebotsanforderung sperren, wenn diese gesendet wird** auf der Seite **Beschaffungsparameter** gesteuert. Standardmäßig ist dieser Parameter auf **Ja** festgelegt, und für eine Konfiguration für den öffentlichen Sektor kann die Standardeinstellung nicht geändert werden. Daher, obwohl der Ergänzungsprozess in einer Konfiguration, die nicht für den öffentlichen Sektor bestimmt ist, manuell gehandhabt werden kann, muss er in einer Konfiguration für den öffentlichen Sektor verwendet werden.

Wenn Sie eine Angebotsanforderung für eine Bestellung erstellen und einen Lagerartikel zur Angebotsanforderung hinzufügen, wird eine Lagerbuchung mit dem Zugangsstatus **Angebotszugang** erstellt. Es werden nur Angebotsanforderungspositionen mit diesem Status berücksichtigt, wenn Sie einen Produktprogrammplan verwenden, um den Bestand zu berechnen. Wenn Sie möchten, dass der Produktprogrammplan Angebotsanforderungspositionen als erwarteten Zugang umfasst, müssen Sie dieses Verhalten in den Einstellungen des Produktprogrammplans konfigurieren.

Ein Einkaufsleiter oder Agent kann Anfragentypen erstellen und verwalten, die zu den Beschaffungsanforderungen der Organisation passen. Jeder Anfragentyp kann einer Bewertungsmethode zugeordnet werden. Bewertungsmethoden bestehen aus einem Satz von Kriterien, die verwendet werden können, wenn Sie Angebote bewerten. Sie müssen Anfragentypen, Bewertungsmethoden und Bewertungskriterien auf den Seiten **Anfragentyp** und **Bewertungsmethode** einrichten.

## <a name="choose-default-fields-to-include-in-vendor-rfq-reply-forms"></a><a name="default-reply-fields"></a>Wählen Sie Standardfelder aus, die in die Antwortformulare für Lieferantenanfragen aufgenommen werden sollen

Sie können bestimmte Arten von Informationen angeben, die Sie von Kreditoren als Antwort auf eine Angebotsanforderung erhalten möchten. Felder, die Sie als Standard markieren, sind in dem Online-Formular enthalten, das für die Zusammenarbeit mit Lieferanten bereitgestellt wird. Um diese Einstellungen vorzunehmen:

1. Wenn Sie dies noch nicht getan haben, verwenden Sie die Seite [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um die Funktion *Auswählen der Angebotsanforderungsfelder, die in die Antwortformulare für Lieferantenanfragen aufgenommen werden sollen* zu aktivieren.
1. Gehen Sie zu **Beschaffung > Setup > Beschaffungsparameter**.
1. Öffnen Sie die Registerkarte **Angebotsanforderung**.
1. Wählen Sie den Antwortfelderlink **Standardwerte für Angebot** unter der Überschrift **Standardwerte für Angebotsanforderungen einrichten**.
1. Das Dialogfeld **Standardanforderung für Angebotsantwortfelder** wird geöffnet.
1. Der Abschnitt **Angebotsanforderungsfelder in Antwortformularen für Lieferantenanforderungen** enthält einen Schieberegler für jedes Feld, das für die Verwendung in Antwortformularen für Lieferantenanfragen zur Verfügung steht. Felder, die in diesem Abschnitt auf *Ja* gesetzt sind, werden (zusammen mit ihren Werten) in Angebotsanforderung-Antwortformulare aufgenommen. Stellen Sie den Schieberegler auf *Nein* für jedes Feld, in dem Sie verhindern möchten, dass Lieferanten bei der Überprüfung von Geboten Daten sehen. Auf diese Weise können Sie geschätzte oder erwartete Werte während der Angebotsanforderungseingabe für interne Zwecke eingeben, ohne dass der Lieferant sieht, was eingegeben wurde.

Sie können diese Einstellungen für einzelne Angebotsanforderungsfälle nach Bedarf überschreiben.

## <a name="creating-and-sending-an-rfq"></a>Eine Angebotsanforderung erstellen und senden

Sie erstellen eine Angebotsanforderung, wählen die Kreditoren aus, die auf die Angebotsanforderung antworten sollen, und senden die Angebotsanforderung dann an die Kreditoren. Sie können die Druckeinstellungen verwenden, um den Angebotsanforderungsbericht und Antwortbogenberichte an Ihr bevorzugtes Ziel weiterzuleiten.

Sie können manuell eine Angebotsanforderung entweder für den Bestelltyp **Bestellung** oder den Bestelltyp **Kaufvertrag** erstellen.

Wenn die Angebotsanforderungsanfrage vom Typ **Bestellung** ist, erfolgt das folgende Verhalten auf, das aus anderen Typen Angebotsanforderungsfälle abweicht:

- Wenn Angebotsanforderungspositionen erstellt werden, werden Lagerbuchungen generiert, die den Zugangsstatus von **Angebotszugang** besitzen.
- Wenn Sie ein Angebot akzeptieren, wird eine Bestellung generiert.

Wenn die Angebotsanforderungsanfrage vom Typ **Kaufvertrag** ist, erfolgt das folgende Verhalten auf, das aus anderen Typen Angebotsanforderungsfälle abweicht:

- Die Angebotsanforderung wird für eine Vereinbarung zum Einkauf einer bestimmten Produktmenge oder eines bestimmten Produktwerts über einen gewissen Zeitraum verwendet. Sie müssen den Datumsbereich auswählen, der für den Kaufvertrag und den Namen des Mitarbeiters gilt, der mit der Verwaltung der Rahmenbestellung betraut ist.
- Wenn Sie ein Angebot annehmen, wird ein Kaufvertrag generiert.

Wenn die Angebotsanfordernung aus einer Bestellanforderung generiert wird, wird der Typ **Bestellanforderung** automatisch zugewiesen. Sie können eine Angebotsanforderung vom Typ **Bestellanforderung** nicht manuell erstellen.

Sie können nur eine Angebotsanforderung aus einer Bestellanforderung erstellen, wenn der Status der Bestellanforderung **Wird überprüft** ist und Ihnen die Erledigung der nächsten Workflowaufgabe zugewiesen ist. Die Positionen der Bestellanforderung werden automatisch aktualisiert, wenn Sie Positionen aus den Antworten auf Angebotsanforderung (Angebote) annehmen, die Sie von Kreditoren erhalten haben. Sie können nicht abschließen, genehmigen, ablehnen, oder, alle sonstigen Aktivitäten für die Bestellanforderung ausgeführt, nachdem die Bestellanforderungsposition mit einer oder dem angenommenen Angebotsanforderungsposition Angebotsanforderungsanfrage aktualisiert wurde, wird storniert.

Wenn Sie eine Angebotsanforderung erstellen, können Sie einen Anfragentyp auswählen. Der Anfragentyp bestimmt die Gruppe von Bewertungskriterien, die verwendet wird, um Antworten auf die Angebotsanforderung zu bewerten.

Sie können einer Angebotsanforderungsanfrage einen Fragebogen hinzufügen. Dieser Fragebogen wird dann auf allen Antworten angezeigt, nachdem Sie die Angebotsanforderung senden. Der Abschluss des Fragebogens ist eine erforderliche Aufgabe, bevor das Angebot gesendet werden kann.

Obwohl Standardeinstellungen angegeben sind, können Sie die Einstellungen **Angebotsanforderungsfelder in Angebotsanforderung-Antwortformularen des Lieferanten** für jeden einzelnen Angebotsanforderungsfall nach Bedarf ändern. Erstellen oder öffnen Sie dazu einen Angebotsanforderungsfall. Öffnen Sie dann im Aktionsbereich die Registerkarte **Angebot** und wählen Sie dann aus dem Abschnitt **Antworten** **Einstellen der Standardantworten für Angebotsanforderungen** aus. Das Dialogfeld **Standardanforderung für Angebotsantwortfelder** wird geöffnet; es funktioniert genauso wie beim Festlegen der Standardeinstellungen für Lieferanten-Angebotsanforderung-Antwortformulare, außer dass Ihre Änderungen hier nur den aktuellen Angebotsanforderungsfall betreffen. Ausführliche Informationen zum Aktivieren und Funktionieren dieser Funktionalität finden Sie unter [Wählen Sie Standardfelder aus, die in die Antwortformulare für Lieferantenanfragen aufgenommen werden sollen](#default-reply-fields).

Es gibt drei Möglichkeiten, um die Kreditoren auswählen, die einer Angebotsanforderungsanfrage hinzugefügt werden sollen:

- Fügen Sie die Kreditoren nacheinander hinzu.
- Suchen Sie nach allen Kreditoren, die bestimmten Kriterien entsprechen.
- Fügen Sie automatisch alle Kreditoren hinzu, die für die Beschaffungskategorien, die bei den Angebotsanforderungspositionen verwendet werden, genehmigt sind.

Wenn die Angebotsanforderungsanfrage bereit ist, wählen Sie **Senden** aus. Die Aktion „Senden” generiert Erfassungen und Berichte, die gemäß Ihren Druckverwaltungseinstellungen gedruckt, archiviert und gesendet werden.

Wenn Sie die Kontrollkästchen **Kreditor zur Neuberechnung von Preisen verwenden** und **Kreditorenspezifische Artikelinformationen verwenden** auf der Seite **Angebotsanforderung wird gesendet** auf **Ja** festgelegt haben, wenn Sie die Angebotsanforderung an Kreditoren schickten, werden einige kreditorenspezifische Informationen für diese Angebotsanforderung für diesen Lieferant automatisch eingegeben.

## <a name="amending-an-rfq-case"></a>Anpassen einer Angebotsanforderung

Gelegentlich müssen Sie eine Angebotsanforderung anpassen, nachdem Sie sie gesendet haben. Möglicherweise müssen Sie die Angebotsanforderung anpassen, wenn sich beispielsweise die Lieferdaten geändert haben oder Sie zusätzliche Produkte oder andere Mengen von Produkte möchten. Sie können den Ergänzungsprozess so konfigurieren, dass er entweder einschränkender oder weniger einschränkend ist.

Wenn Sie den Ergänzungsprozess konfigurieren, sodass er einschränkender ist, bevor Sie die Felder in einer Angebotsanforderungsanfrage ändern können, die bereits übermittelt wurde, müssen Sie **Erstellen** in der Angebotsanforderungsanfrage auswählen, um eine Ergänzung zu starten. Nachdem Sie Ihre Änderungen abgeschlossen haben, müssen Sie **Abschließen** auswählen. Sie werden dann durch den Prozess zum Hinzufügen von Informationen für die E-Mail-Nachricht geführt, die gesendet wird, um Kreditoren zur Ergänzung zu informieren. Der aktualisierte Angebotsanforderungsbericht, der einen Ergänzungshinweis umfasst, wird automatisch der E-Mail zugeordnet.

Wenn Sie den Ergänzungsprozess so konfigurieren, dass er weniger einschränkend ist, müssen Sie nicht **Erstellen** auswählen, bevor Sie die Felder auf einer Angebotsanforderungsanfrage ändern können, die bereits übermittelt wurde. Sie müssen allerdings einen Ergänzungshinweis zur Angebotsanforderung manuell hinzufügen und die Anfrage erneut senden. Beachten Sie, dass dieser Ansatz nur verwendet werden kann, wenn keine der Antworten (Angebote) verarbeitet wurden. Wenn Sie eine Antwort eingegeben haben und sie sich im Status **Eingegangen** befindet, ist die Schaltfläche **Senden** nicht verfügbar. In diesem Fall müssen Sie **Erstellen** und anschließend **Abschließen** auswählen, wie Sie es in einem einschränkenderen Prozess erfolgen muss. Die Antwort wird dann zurückgesetzt, um die Änderungen an der Angebotsanforderungsanfrage widerzuspiegeln.

Wenn Kreditoren die Kreditorenzusammenarbeitschnittstelle verwenden, um Angebote einzugeben, müssen Sie immer den Ergänzungsprozess verwenden, um Kreditoren zu Änderungen an der Angebotsanforderungsanfrage zu informieren. Mithilfe diesem Prozess wird die Situation verhindert, in der Kreditoren Angebote auf eine veraltete Angebotsanforderungsanfrage abgeben, während sich ihr Angebot in Bearbeitung befindet. Weitere Informationen über die Kreditorenzusammenarbeit finden Sie unter [Kreditorenzusammenarbeit mit externen Kreditoren](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-external-vendors)

Wenn Sie weitere Kreditoren dazu einladen möchten, Angebote zu unterbreiten, und keine Änderungen an der Angebotsanforderungsanfrage vorgenommen wurden, können Sie die Schaltfläche **Senden** verwenden. Die Kreditoren, die Sie hinzugefügt haben, werden auf der Seite **Senden** angezeigt und erhalten die E-Mail-Einladung.

## <a name="receiving-and-registering-rfq-replies"></a>Erhalten und Erfassen von Antworten auf Angebotsanforderungen

Wenn Sie eine Angebotsanforderung senden, wird automatisch ein Antwortblatt generiert. Da Sie Angebote auf eine Angebotsanforderung erhalten, müssen Sie diese über die Seite **Angebotsanforderung** eingegeben, indem Sie auf **Antwort auf Angebotsanforderung bearbeiten** klicken. Dies ermöglicht es Ihnen, eine Anngebotsinformationen in ein dediziertes Angebotsformular einzugeben. Zuerst ist der **Antwortfortschritt** auf **Nicht gestartet** festgelegt. Wenn Sie **Bearbeiten Antwort auf Angebotsanforderung,** klicken, wird der Status **Einkäufer aktualisiert** das Angebot gesendet wird. Klicken Sie auf **Übermitteln**, wenn Sie die Angebotsinformationen eingegeben haben. Der Antwortfortschrittsstatus wechselt zu **Versendet von Käufer.** Und auch wenn die Zusammenarbeit aktiviert ist, aktualisiert sich der  **Antwortfortschritt**, während der Kreditor mit dem Angebot interagiert. Der Status ändert sich dann von **Kreditor aktualisiert** zu **Versendet durch Kreditor**. Wenn das Angebot gesendet wird, wird eine Erfassung als **Eingegangen** erstellt. Die Antwort "(Angebot) muss übermittelt werden, damit sie als eingegangen erfasst werden, und nur dann kann sie weiter als angenommen oder abgelehnt erfasst werden.

Wenn Sie das Angebot aktualisieren müssen, können Sie den gleichen Prozess durchlaufen wie oben und  erneut übermitteln.

Beachten Sie, dass das Bearbeiten des Formulars **Angebotsanforderung** nur zu Informationszwecken erlaubt ist, die sich auf das Verarbeiten des Angebots bezieht, und nicht für die Eingabe des Angebots zulässig ist. Um die Antwort einzugeben oder zu ändern klicken Sie auf **Angebotsanforderung bearbeiten.**

Wenn Sie die Angebotsinformationen eingeben, und wenn die Angebotsanforderungsanfrage alternative Positionen zulässt, können Sie alternative Positionen für Positionen hinzufügen, die nur eine Beschaffungskategorie keinen Katalogartikel ha en, die angegeben werden. Klicken Sie auf **Fügen Sie Alternative hinzu**, um alternative Positionen hinzuzufügen.

Wenn Sie eine Antwort eingegeben, aber ein neues Angebot vom Kreditor angefordert haben, können Sie die Angebotsanforderung erneut senden. Eine neue Erfassung und ein Bericht werden erstellt, die an den Kreditor übermittelt werden können.

Sie können eine Übersicht über alle Angebotsanforderungen und deren Antwortstatus auf der Seite **Weiterverfolgung der Angebotsanforderung** anzeigen. Dort finden Sie die Stati **Senden, empfangen, akzeptiert, zurückgewiesen. storniert, abgelehnt**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Angebote annehmen und ablehnen sowie angenommene Angebote an Downstreamdokumente übertragen

Nach Ermittlung des besten Angebots – beispielsweise des Angebots mit dem besten Gesamtpreis – akzeptieren Sie es. Sie können manche Positionen in einem Angebot annehmen und andere ablehnen.
Sie können auch Positionen von verschiedenen Kreditoren akzeptieren. Beachten Sie, dass wenn Sie manche Positionen annehmen, Sie dazu aufgefordert werden, alle anderen Positionen abzulehnen. Wenn Sie andere Positionen annehmen möchten, müssen Sie daher **Abbrechen** auswählen, wenn Sie die dazu aufgefordert werden. Der Status der Angebotsanforderungsantwort für jeden Kreditor, von dem Sie Angebote oder Positionen annehmen, wird auf **Angenommen** aktualisiert.

Wenn Sie, während Sie die Bestellung oder die Rahmenbestellung vorbereiten, Anforderung, einer anderen Position der Angebotsanforderung, hinzuzufügen können Sie dies tun, indem Sie **Position hinzufügen** im Feld **Angebotsanforderung** Seitenpositionsraster klicken. Sie können diese Position nur auf der Seite **Angebotsanforderung** anzeigen und bearbeiten. Sie wird auf der Angebotsseite angezeigt, wenn diese akzeptiert wird.

Wenn Sie ein Angebot oder eine oder mehrere Positionen in einem Angebot annehmen, wird automatisch eine Bestellung oder ein Kaufvertrag generiert. Sie können dann die Angebote von allen anderen Kreditoren ablehnen.

In der Antwort können Sie einen Ursachencode hinzufügen, um zu erläutern, warum Sie ein Angebot angenommen oder abgelehnt haben.

Wenn Sie ein Angebot vom Typ **Bestellanforderung** akzeptiert, werden die Bestellanforderungspositionen mit den folgenden Informationen aktualisiert, die die Informationen des angenommenen Angebots angezeigt:

- Preis je Einheit
- Rabattprozentsatz
- Skontobetrag
- Belastungen für Einkauf
- Positionsgebühren
- Lieferant
- Externe Nummer
- Externe Beschreibung

In der folgenden Tabelle wird angezeigt, wie sich der Angebotsanforderungs-Status ändert, während Sie Angebote von Kreditoren annehmen und ablehnen.

## <a name="statuses--highest-and-lowest"></a>Status - höchster und niedrigster

Auf der Kreditorenregisterkarte des Angebotsanforderungsfalls können Sie die Positionen mit dem höchsten und niedrigsten Status für einen bestimmten Kreditor finden. Wenn der Lieferant hinzugefügt wird und noch keine Positionen gesendet wurden, ist sowohl der niedrigste als auch der höchste Status <strong>Erstellt.</strong> Wenn die Angebotsanforderung mit allen Positionen an den Lieferanten gesendet wird, lautet der Status der beiden Zeilen <strong>Gesendet</strong>. Wenn einige Positionen in einem Angebot von einem Kreditor akzeptiert werden und andere abgelehnt werden, erhalten die abgelehnten Positionen den niedrigsten Status in <strong>Abgelehnt</strong> und die akzeptierte Positionen erhalten den höchsten Status <strong>Angenommen</strong>.

Wählen Sie dien Angebotsanforderungsfallpositionen können Sie den höchsten und niedrigsten Status pro Position für alle Kreditoren anzeigen. Wenn Sie eine Position für alle Kreditoren im Angebotsanforderungsanfrage gesendet haben und niemand geantwortet hat, wird dennoch der niedrigste und höchste Status **Versendet.** Wenn mindestens ein Kreditor antwortet, ändert der höchste Status **Eingegangen**. Wenn Sie einen neuen Kreditor dem Fall hinzufügen, ändern sich der niedrigste Status **Erstellt**

Der niedrigste und höchste Status in der Angebotsanforderungsanfrage ist eine Aggregation des Status auf der \<Kreditorenregisterkarte und der Registerkarte Position.

Die Statusangaben werden folgendermaßen sind in aufsteigender Reihenfolge sortiert geordnet: Erstellt, gesendet, empfangen, abgelehnt, angenommen, abgelehnt, storniert.

In der folgenden Tabelle wird angezeigt, wie sich der Angebotsanforderungsstatus ändert, wenn Sie eine Angebotsanforderung erstellen und diese an die Kreditoren senden.

| **Aktivität**                                | **Niedrigster Status von einer Angebotsanforderungsposition** | **Höchster Status einer Angebotsanforderungsposition** | **Niedrigster Status von einer Angebotsanforderungsposition** | **Höchster Status von einer Angebotsanforderungsposition** |
|-------------------------------------------|----------------------------|-----------------------------|---------------------------------|----------------------------------|
| Erstellen Sie den Angebotsanforderungskopf und die Anforerungsposition.      | Erstellt am                    | Erstellt am                     | Erstellt am                         | Erstellt am                          |
| Senden von Angebotsanforderungen für alle Kreditoren im Angebotsanforderungsanfrage. | Gesendet                       | Gesendet                        | Gesendet                            | Gesendet                             |
| Einen weiteren Kreditor hinzufügen                       | Erstellt am                    | Gesendet                        | Erstellt am                         | Gesendet                             |
| Senden Sie die Angebotsanforderung an den zweiten Kreditor.        | Gesendet                       | Gesendet                        | Gesendet                            | Gesendet                             |

Alle Positionen in der Angebotsanforderung, die der Angebotsanforderungsanfrage zugeordnet sind, sind in Zustand **Versendet**.

In der folgenden Tabelle wird angezeigt, wie der Angebotsanforderungsstatus sich ändert, während Sie Angebote empfangen und die Informationen im Antwortbogen für Angebotsanforderung erfassen.

| **Aktivität**                                               | **Niedrigster Status aller Positionen in der Angebotsanfrage** | **Höchster Status aller Positionen in der Angebotsanfrage** | **Niedrigster Status des Angebotsanforderungskopfes** | **Höchster Fall des Angebotsanforderungskopfes** | **Niedrigster Status von einer Angebotsanforderungsposition** | **Höchster Status von einer Angebotsanforderungsposition** |
|----------------------------------------------------------|------------------------------------------------|-------------------------------------------------|-----------------------------------|------------------------------------|---------------------------------|----------------------------------|
| Erfassen Sie ein Angebot für eine Angebotsanforderung und speichern Sie es.        | Gesendet                                           | Eingegangen                                        | Gesendet                              | Eingegangen                           | Gesendet                            | Eingegangen                         |
| Erfassen Sie das Angebot des zweiten Angebots des Kreditors in einer Angebotsanforderung und speichern Sie es. | Eingegangen                                       | Eingegangen                                        | Eingegangen                          | Eingegangen                           | Eingegangen                        | Eingegangen                         |


Im Beispiel unten sehen Sie den niedrigsten und höchsten Status in der Angebotsanforderung, für die ein Angebot empfangen wurde und das andere Angebot akzeptiert wurde. Wenn ein empfangenes Angebot abgelehnt wird, ändert der niedrigste Status von erhalten auf  abgelehnt im Feld Angebotsanforderungsfallkopf und -Position.


|            <strong>Aktivität</strong>             | <strong>Niedrigster Status aller Positionen in der Angebotsanfrage</strong> | <strong>Höchster Status aller Positionen in der Angebotsanfrage</strong> | <strong>Niedrigster Status des Angebotsanforderungskopfes </strong> | <strong>Höchster Fall des Angebotsanforderungskopfes </strong> | <strong>Niedrigster Status einer Angebotsanforderungsposition</strong> | <strong>Höchster Status einer Angebotsanforderungsposition</strong> |
|------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------|-------------------------------------------------|----------------------------------------------|-----------------------------------------------|
| Nehmen Sie eines derAngebote an. (oder mindestens eine Position ist erforderlich) |                          Eingegangen                           |                           Angenommen                           |                    Eingegangen                    |                    Angenommen                     |                   Eingegangen                   |                   Angenommen                    |
|           Lehnen Sie alle anderen Angebote ab.           |                          Verweigert                           |                           Angenommen                           |                    Verweigert                    |                    Angenommen                     |                   Verweigert                   |                   Akzeptiert                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]