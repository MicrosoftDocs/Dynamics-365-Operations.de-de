---
title: Filialauftragserfüllung
description: Dieses Thema enthält eine Übersicht über die Filialauftragserfüllung.
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: rubendel
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 68132a78921e0a38c61c85bcc2b89dca3c25b04e
ms.sourcegitcommit: 4c6d31f3ebd88212d3d1497a4bba9c64c5300444
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2020
ms.locfileid: "4412714"
---
# <a name="store-order-fulfillment"></a>Filialauftragserfüllung

[!include [banner](includes/banner.md)]

Viele Einzelhändler möchten die Auftragserfüllung optimieren, indem Sie es Filialen ermöglichen, Aufträge zu erfüllen. Durch Auftragserfüllung auf Filialebene können zu große Lagerbestände für eine bestimmte Filiale vermieden werden. Sie kann auch aus logistischer Sicht in bestimmten Fällen erforderlich sein, wenn eine Filiale zusätzliche Kapazitäten besitzt oder sich in einer geringeren Versandentfernung zum Debitoren befindet. Um dieser Anforderung zu entsprechen, ist ein vereinheitlichter Auftragserfüllungsarbeitsgang in der Verkaufsstelle verfügbar.

Bei Aufträgen für die Erfüllung in einer bestimmten Filiale ist der Lagerort der Filiale in der Kopfzeile oder den Positionen des Auftrags festgelegt.

Der Auftragserfüllungsarbeitsgang in der Verkaufsstelle enthält einen einzelnen Arbeitsbereich in der Verkaufsstelle, der verwendet werden kann, um Aufträge zu verarbeiten. Dies umfasst alles von der Annahme des Auftrags bis zur Markierung als versendet oder zum Initiieren der Filialabholung.

## <a name="access-unified-order-fulfillment-in-the-point-of-sale"></a>Auf vereinheitlichte Auftragserfüllung in der Verkaufsstelle zugreifen

Auftragserfüllung, [Arbeitsgangskennungs-ID 928](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations), kann dazu verwendet werden, um auf den Arbeitsbereich für die Filialauftragserfüllung in der Verkaufsstelle zuzugreifen.

Der Auftragserfüllungsarbeitsgang verfügt nicht über einen eigenen Berechtigungsstandard, aber in der Zukunft werden Benutzer in der Lage sein, die Berechtigung **Abrufen des Auftrags zulassen** zu verwenden, um den Arbeitsgang von der Verkaufsstelle aus aufzurufen.

Auf Filialebene ist eine Konfigurationseinstellung verfügbar, um zu bestimmen, ob eine Auftragsposition manuell von innerhalb der Verkaufsstelle aus angenommen werden muss. Wenn diese Konfigurationsoption nicht festgelegt wird, werden Auftragspositionen standardmäßig angenommen. Wenn diese Konfigurationsoption aktiviert ist, müssen Benutzer in der Verkaufsstelle die Berechtigung **Annahme von Auftrag zulassen** aktivieren, um Aufträge von innerhalb der Verkaufsstelle aus anzunehmen.

Auftragspositionen können von der Verkaufsstelle aus auch abgelehnt werden. Die Ablehnung einer Auftragsposition bedeutet, dass sie nicht in dieser Filiale erfüllt wird und die Auftragsposition wird zurückgesendet, um einer anderen Filiale oder Lagerort zugewiesen zu werden. Auftragspositions-Ablehnungsberechtigung wird durch die Berechtigung **Auftragsablehnung zulassen** gewährt.

## <a name="order-fulfillment-operation-parameters"></a>Auftragserfüllungsarbeitsgang-Parameter

Auftragserfüllung enthält Standardparameter, die dem Arbeitsgang zugeordnet werden können, der in der Verkaufsstelle aufgerufen wird. Wenn der Parameter **Alle Aufträge** konfiguriert ist, werden alle Aufträge angezeigt, wenn der Arbeitsgang verwendet wird. Vom Parameter **Aufträge zum Versand** werden nur Aufträge angezeigt, die von der Filiale versendet werden müssen und **Aufträge zur Abholung** zeigt Aufträge an, die in der Filiale abgeholt werden.

## <a name="orders-for-fulfillment"></a>Aufträge zur Erfüllung

Der Auftragserfüllungsarbeitsgang zeigt nur Aufträge an, die entweder abgeholt oder von der aktuellen Filiale versendet werden. Aufträge für andere Filialen, die zu erfüllen sind, werden nicht aufgelistet, wenn Sie den Auftragserfüllungsarbeitsgang verwenden.

## <a name="line-selection"></a>Positionsauswahl

Positionen können mithilfe der Funktion **Auswählen** im Aktivitätsbereich ausgewählt werden. Wenn **Auswählen** aktiviert ist, können mehrere Positionen zur Bearbeitung ausgewählt werden. Sie können ausgewählte Positionen deaktivieren, indem Sie wieder auf die gleiche Position klicken.

## <a name="line-details"></a>Positionsdetails

Positionsdetails können mittels des Positionsdetail-Flyoutmenüs angezeigt werden. Wenn dieses Menü verwendet wird, werden drei Registerkarten bereitgestellt, um zusätzliche Informationen für die ausgewählte Position anzuzeigen. Die erste Registerkarte **Positionsdetails** zeigt Details für die Position selbst an, wie bestellte und verbleibende Menge. Zusätzliche Details werden bereitgestellt, einschließlich entnommene, verpackete und fakturierte Menge sowie Lieferart und die Lieferadresse. Die Registerkarte **Auftragsdetails** enthält Angaben im Auftragskopf, einschließlich Debitor, Debitorkennung, Auftragsnummer, Auftragsgesamtsumme und Saldo. Die Registerkarte **Lager** enthält Informationen für die ausgewählte Position hinsichtlich physischen Lagerbestand, reservierten Lagerbestand und bestellte Lagerbestand angezeigt.

Wenn mehrere Positionen ausgewählt sind, wird vom Auftragspositionsdetail-Flyoutmenü nur angegeben, dass mehrere Positionen ausgewählt sind. Um Details für eine einzelne Position anzuzeigen, deaktivieren Sie die Positionen, bis nur eine Position verbleibt.

## <a name="pending-order-lines"></a>Ausstehende Auftragspositionen

Einheitliche Auftragserfüllung umfasst die Möglichkeit, Aufträge manuell anzunehmen. Standardmäßig werden Aufträge für Erfüllung in der Filiale bereits angenommen. Wenn Geschäftsprozesse jedoch vorschreiben, dass eine Arbeitskraft auf Filialebene Aufträge annehmen muss, kann die manuelle Annahme auf Einzelhandelsfilial-Ebene aktiviert werden. Um die Auftragsannahme zu aktivieren, wechseln Sie zu **Retail und Commerce** \> **Channel** \> **Shop** \> **Alle Shops**. Öffnen Sie die gewünschte Filiale auf der Registerkarte **Allgemein**, suchen Sie die Unterüberschrift **Auftragserfüllung**. Diese Unterüberschrift hat eine Option **Manuelle Annahme**, die standardmäßig auf **Nein** festgelegt ist. Indem Sie diese Option auf **Ja** festlegen und die Änderungen an der Kanaldatenbank synchronisieren, können Auftragspositionen den Annahmeprozess durchlaufen.

Arbeitskräfte mit der Berechtigung **Auftragsannahme zulassen** können die Auftragserfüllung öffnen und Positionen zur Annahme auswählen. Sobald Positionen angenommen wurden, ändert sich ihr Status von **Ausstehend** zu **Angenommen**, und der Rest des Auftragserfüllungsprozesses kann fortgesetzt werden. Wenn **Manuelle Annahme** aktiviert ist, werden Aufträge erst verarbeitet, wenn sie angenommen wurden.

Aufträge für Abholung in der Filiale haben nie den Status **Ausstehend**. So wird ein Szenario vermieden, bei dem ein Debitor in der Filiale eintrifft und die Auftragsposition nicht verarbeitet werden kann, weil die Arbeitskraft mit den richtigen Rechten nicht verfügbar ist.

## <a name="accepted-order-lines"></a>Angenommene Auftragspositionen

Aufträge mit dem Positionsstatus **Angenommen** können den übrigen Auftragserfüllungsprozess in der Verkaufsstelle durchlaufen. Nachdem ein Auftrag angenommen wurde, können alle verbleibenden Aktivitäten gegenüber der Auftragsposition durchgeführt werden.

So kann beispielsweise eine angenommene Auftragsposition ausgewählt und dann direkt abgeholt werden, ohne die Entnahme und Verpackung zu durchlaufen.

## <a name="line-actions"></a>Positionsaktivitäten

### <a name="pick"></a>Entnehmen

Die Aktivitätenkategorie  **Entnahme** wird bereitgestellt, um den Prozess der Entnahme von Auftragspositionen aus Regalen zu erleichtern. Die Entnahmeaktivität kann nur bei Auftragspositionen ausgeführt werden, die zuvor angenommen wurden.

**Aktivität: Entnahme**

- **Resultierender POS-Status:** Entnahme
- **Resultierender Backofficestatus:** Keine Änderung

Nachdem ein Auftrag angenommen wurde, können Positionen als **Entnahme** ausgewählt und markiert werden. Eine Position als **Entnahme** zu markieren ist eine Möglichkeit, um anzugeben, dass die Entnahmearbeit bereits bei einer Position ausgeführt wird. Dies verhindert, dass zwei Arbeitskräfte versuchen, gleichzeitig dieselben Auftragspositionen zu entnehmen.

**Aktivität: Kommissionierliste drucken**

- **Resultierender Status:** Entnahme
- **Resultierender Backofficestatus:** Keine Änderung

Kommissionierlisten können in der Verkaufsstelle gedruckt werden, um die Arbeitskräfte dabei zu unterstützen, den Entnahmeprozess auszuführen. Eine gedruckte Kommissionierliste kann die Arbeitskraft bei sich tragen, die die Entnahme ausführt, und während die Produkte entnommen werden, markiert die Arbeitskraft sie manuell auf der Kommissionierliste als entnommen.

Das Kommissionierlistenformat wird in Commerce konfiguriert und dem Bonprofil hinzugefügt. Weitere Informationen zum Einrichten von Bonprofilen finden Sie unter [Bonvorlagen und Drucken](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).

Wenn Positionen ausgewählt sind und eine Kommissionierliste für diese Positionen gedruckt wird, werden diese automatisch mit dem Status **Entnahme** aktualisiert.

**Aktivität: Als entnommen markieren**

- **Resultierender Status:** Entnommen oder teilweise entnommen
- **Resultierender Backoffice-Status:** Entnommen oder teilweise entnommen

Nachdem der physische Entnahmeprozess ausgeführt wurde, können Positionen als **Entnommen** markiert werden. Indem eine Position ausgewählt und sie als **Entnommen** markiert wird, wird ein Echtzeitaufruf zur Aktualisierung der Auftragsposition ausgeführt. Nachdem die Position als **Entnommen** in der Verkaufsstelle markiert wurde, wird der Status im Backoffice auch auf **Entnommen** aktualisiert, und die Lagerbuchungen spiegeln wieder, dass die angegebene Menge abgezogen wurde.

Wenn Aufträge im Zeitverlauf verarbeitet werden, können Teilmengen für eine bestimmte Position verarbeitet werden. Wenn eine Position ausgewählt wurde und die Aktivität **Als entnommen markieren** ausgeführt wird und die Menge größer als eins ist, wird der Benutzer bezüglich der Menge aufgefordert. Die zu entnehmende Restmenge wird automatisch ausgefüllt. Wenn weniger als die Restmenge angegeben wird, wird der Positionsstatus **Teilweise entnommen**. Wenn die Auftragsposition im Backoffice aktualisiert wird, spiegelt sie auch den Status „Teilweise Entnommen” wieder, und die vom Debitor eingegebene Menge wir für die Bestandsaktualisierung verwendet.

Wenn eine Auftragsposition fälschlicherweise entnommen wird, muss die Stornierung der Entnahme der Auftragsposition im Backoffice ausgeführt werden. Aktuell wird keine Aktivität zur Entnahmestornierung in der Verkaufsstelle unterstützt.

Auftragspositionen aus verschiedenen Aufträgen können ausgewählt und als **Entnahme** markiert werden und auf derselben Kommissionierliste gedruckt werden, oder als **Entnommen** markiert werden.

### <a name="pack"></a>Verpackung

Auftragspositionen können jederzeit verpackt werden, nachdem die Auftragsposition angenommen wurde.

**Aktivität: Lieferschein drucken**

- **Resultierender Status:** Verpackt oder teilweise verpackt
- **Resultierender Backoffice-Status:** Geliefert oder teilweise geliefert

Bei dieser Aktivität werden Positionen als verpackt oder teilweise verpackt markiert, und ein Lieferschein wird ausgedruckt. Ein Lieferschein kann gedruckt werden, um die Produkte zu überprüfen, die zusammen verpackt wurden. Das Lieferschein wird in Commerce konfiguriert und dem Bonprofil hinzugefügt. Weitere Informationen zum Einrichten von Bonprofilen finden Sie unter [Bonvorlagen und Drucken](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).

**Aktivität: Als verpackt markieren**

- **Resultierender Status:** Verpackt oder teilweise verpackt
- **Resultierender Backoffice-Status:** Geliefert oder teilweise geliefert

Die Aktivität **Als verpackt markieren** kann verwendet werden, um anzugeben, dass Positionen verpackt wurden, ohne einen Lieferschein zu drucken. Sowohl **Lieferschein drucken** als auch **Als gepackt markieren** ergeben Lagerbuchungen im Backoffice. Verpackungspositionen in der Verkaufsstelle führen dazu, dass Lieferscheinerfassungen im Backoffice generiert werden.

Wenn eine Auftragsposition fälschlicherweise verpackt wird, muss die Lieferscheinerfassung im Backoffice korrigiert werden.

Nur Positionen auf dem gleichen Auftrag und mit derselben Lieferart können gleichzeitig verpackt werden.

Aktuell ist die Option, Filialabholungspositionen als **Verpackt** zu markieren, deaktiviert. Diese Funktion wird in einer späteren Version hinzugefügt. Der Lieferscheinerstellungsprozess wird erweitert, damit die Einfügung von Versandinformationen Dritter in den Lieferscheinprozess unterstützt wird.

### <a name="pick-up"></a>Abholen

Aufträge für die Filialabholung können unmittelbar abgeholt werden, sobald sie in der Verkaufsstelle abgerufen worden sind. Aufträge für die Filialabholung unterliegen nicht der Annahme.

**Aktivität: Abholen**

- **Resultierender Status:** Fakturiert oder teilweise fakturiert
- **Resultierender Backoffice-Status:** Fakturiert oder teilweise fakturiert

Wenn eine Position für die Abholung aus der einheitlichen Auftragserfüllung ausgewählt ist, wird der gesamte Auftrag in die Verkaufsstelle geladen, und die Gesamtmenge für die ausgewählte Position wird markiert. Andere Positionen im Auftrag werden auch in die Buchungsansicht der Verkaufsstelle geladen, aber mit der Menge als null markiert.

Nachdem Positionen für die Abholung in die Buchungsansicht geladen wurden, kann die Buchung wie gewöhnlich angeboten werden.

Positionen, die vollständig durch die Abholung fakturiert wurden, werden nicht mehr in der einheitlichen Auftragsverarbeitung angezeigt. Positionen, die teilweise abgeholt wurden, werden weiterhin in der einheitlichen Auftragserfüllung angezeigt, bis sie vollständig abgeholt worden sind.

Wenn eine Position fälschlicherweise abgeholt wird, muss eine Rückgabe, bzw. Rücklieferung ausgeführt werden, um den Fehler zu beheben.

Nur Positionen auf dem gleichen Auftrag und mit derselben Lieferart können gleichzeitig abgeholt werden.

### <a name="shipping"></a>Versand

Die von der Filiale aus zu versendenden Auftragspositionen können durch die einheitliche Auftragserfüllung mithilfe der Aktivität **Versenden** verarbeitet werden. Wenn eine manuelle Auftragspositionsannahme auf der Kanalebene konfiguriert wird, müssen Aufträge vor dem Versand angenommen werden. Nachdem eine Auftragsposition angenommen wurde und den Status **Ausstehend** oder einen anderen Status aufweist, können Positionen versendet werden.

**Aktivität: Versenden**

- **Resultierender Status:** Fakturiert oder teilweise fakturiert
- **Resultierender Backoffice-Status:** Fakturiert oder teilweise fakturiert

Positionen, die aus der einheitlichen Auftragserfüllung versendet werden, werden vom Backoffice fakturiert. Das ist ähnlich, wie wenn der Auftrag direkt vom Backoffice fakturiert wird. Die Positionen, die aus der einheitlichen Auftragserfüllung versendet werden, werden nicht in die Buchungsansicht geladen, und zum Zeitpunkt, zu dem die Positionen versendet werden, wird kein Anbieten ausgeführt.

Auftragspositionen, die vollständig versendet wurden, werden nicht mehr in der einheitlichen Auftragserfüllung angezeigt. Positionen, die teilweise versendet wurden, werden weiterhin in der einheitlichen Auftragserfüllung angezeigt, bis sie vollständig versendet worden sind.

Nur Positionen aus demselben Auftrag können gleichzeitig versendet werden. Wenn die Positionen aus dem gleichen Auftrag verschiedene Lieferarten haben, können sie immer noch für den gleichzeitigen Versand ausgewählt werden.

### <a name="reject"></a>Ablehnen

Positionen oder Teilpositionen können abgelehnt werden. Dadurch können sie vom Backoffice einer anderen Filiale oder einem anderen Lagerort zugewiesen werden. Positionen können nur abgelehnt werden, wenn sie noch nicht entnommen oder verpackt wurden. Um eine Position abzulehnen die bereits entnommen oder verpackt wurde, muss vom Backoffice die Entnahme storniert und die Position wieder ausgepackt werden.

**Aktivität: Ablehnen**

- **Resultierender Status:** Abgelehnt
- **Resultierender Backofficestatus:** Keine Änderung

Die abgelehnten Auftragspositionen können vom Arbeitsbereich **Auftragsverarbeitung und Abfrage** aus angezeigt werden. Deakivieren Sie den Personenfilter im Arbeitsbereich, um alle abgelehnten Auftragspositionen in allen Filialen anzuzeigen. Über die Registerkarte **Abgelehnte Auftragspositionen** unter dem Abschnitt **Aufträge und Favoriten** werden Auftragspositionsdetails angezeigt. Darüber hinaus können die Benutzer auf die Schaltfläche **Abgelehnte Auftragspositionen** unter dem Abschnitt **Zusammenfassung** klicken, um zur Auftragsansicht zu navigieren. Dadurch werden alle Aufträge angezeigt, die eine oder mehrere abgelehnte Auftragspositionen haben. Wenn die verteilte Auftragsverwaltung (DOM) aktiviert ist, dann werden diese abgelehnten Aufträge automatisch den entsprechenden Filialen zur Erfüllung neu zugewiesen. Diese Auftragspositionen können jedoch auch manuell neu zugewiesen werden. Wählen Sie dazu die Position aus, bei der der **Erfüllungsstatus** als **Abgelehnt** angezeigt wird, und ändern Sie den Standort/Lagerort nach Bedarf. Klicken Sie auf das Dropdownmenü **Position aktualisieren**, und klicken Sie auf **Erfüllungsstatus zurücksetzen**, um den Erfüllungsstatus von **Abgelehnt** zu **Angenommen** oder **Ausstehend** zu ändern, entsprechend der Auftragserfüllungseinstellungen. Nachdem der Erfüllungsstatus zurückgesetzt wurde, können die Filialmitarbeiter die Auftragspositionen in POS anzeigen.

## <a name="line-quantity-tracking"></a>Positionsmengennachverfolgung

Eine einzelne Auftragsposition mit einer Menge größer als eins kann über einen längeren Zeitraum verarbeitet werden. Dies resultiert in mehreren Unterstatus für Auftragspositionen. Wenn beispielsweise ein Bauherr ein Projekt hat, für das 500 Bretter benötigt werden, der Bauherr aber im Lauf des Projekts nur jeweils einige wenige Bretter auf einmal abholt oder liefern lässt, könnte es Mengen geben, die gleichzeitig entnommen, verpackt und versendet werden.

Jedes Mal, wenn eine Position ausgewählt wird, wird die verbleibende Menge der Position automatisch ausgefüllt, um anzunehmen, dass die verbleibende Menge verarbeitet wird. Verwenden wir das obige Beispiel: Wenn 200 Bretter bereits entnommen wurden und die Position für Bretter zur Entnahme ausgewählt wurde, wird die verbleibende Menge von 300 automatisch in der Menge ausgefüllt werden. Gleiches gilt, wenn 200 Bretter bereits fakturiert wurden. In diesem Fall wird nur die Restmenge automatisch ausgefüllt.

Wenn man mit dem obigen Beispiel fortfährt: Wenn 200 Bretter als verpackt markiert sind und der Versand ausgewählt ist, wird die Gesamtmenge von 500 automatisch ausgefüllt. Wenn nur 200 Bretter versendet werden, nimmt das System an, dass die zuvor verpackten Bretter versendet werden und die verpackte Menge wird abgezogen. Wenn 201 Bretter versendet werden, werden die verpackten Bretter zuerst abgezogen, wobei das verbleibende einzelne Brett von der verbleibenden Menge abgezogen wird.

## <a name="line-statuses"></a>Positionsstatus

Auftragspositionen in der Verkaufsstelle haben mehrere Status, um den Status der Auftragsposition widerzuspiegeln. Status in der Verkaufsstelle und im Backoffice stimmen nicht in allen Fällen überein. Auftragspositionsstatus kann durch die Verkaufsstelle mithilfe der Auftragserfüllungsarbeitsgänge angezeigt werden. Im Backoffice können Auftragspositionen von den Auftragsdetails angezeigt werden. Auf Auftragsdetails kann über **Retail und Commerce** \> **Debitoren** \> **Alle Debitorenaufträge** zugegriffen werden. Wählen Sie die **Auftragskennung** aus, um Auftragsdetails anzuzeigen. Wählen Sie von den Auftragsdetails aus die Registerkarte **Auftrag** aus, wählen Sie dann **Detaillierter Status** unter der Unterüberschrift **Ansicht** aus.

- **Ausstehend** – Auftragspositionen, die einer Filiale zugewiesen wurden, aber noch nicht angenommen wurden, haben den Status **Ausstehend**, wenn sie in der Verkaufsstelle angezeigt werden. Positionen, bei denen die Annahme in der Verkaufsstelle aussteht, haben den Status **Auftragsabwicklung** im Backoffice.
- **Angenommen** – Auftragspositionen, die manuell angenommen wurden oder automatisch angenommen wurden, besitzen den Status **Angenommen**, wenn sie in der Verkaufsstelle angezeigt werden. Positionen mit dem Status **Angenommen** werden im Backoffice als **Auftragsabwicklung** angezeigt.
- **Entnahme** – Positionen, die aktuell auf der Filialebene entnommen werden, haben den Status **Entnahme**. Diese gleichen Positionen, wenn sie im Backoffice angezeigt werden, werden als **Auftragsabwicklung** angezeigt.
- **Entnommen** und **Teilweise entnommen** – Positionen, die in der Verkaufsstelle entnommen oder teilweise entnommen wurden, besitzen den Status **Entnommen** oder **Teilweise entnommen**. Die gleichen Positionen im Backoffice werden auch als **Entnommen** oder **Teilweise entnommen** angezeigt.
- **Verpackt** und **Teilweise verpackt** – Positionen, die in der Verkaufsstelle verpackt oder teilweise verpackt wurden, besitzen den Status **Verpackt** oder **Teilweise verpackt**. Die gleichen Positionen im Backoffice werden auch als **Geliefert** oder **Teilweise geliefert** angezeigt.
- **Teilweise fakturiert** – Positionen, die teilweise entnommen oder teilweise versendet wurden, besitzen den Status **Teilweise fakturiert** in der Verkaufsstelle und im Backoffice.
- **Fakturiert** – Positionen, die in der Verkaufsstelle vollständig fakturiert wurden, werden nicht mehr für die Erfüllung angezeigt. Im Backoffice ist der Status für diese Positionen **Fakturiert**.

## <a name="order-fulfillment-filtering"></a>Auftragserfüllungsfilterung

Auftragserfüllung in der Verkaufsstelle umfasst Filterung, sodass der Benutzer das Gesuchte leichter finden kann. Filter können über den Aktivitätsbereich unten im Bildschirm **Verkaufsstelle** geändert werden. Standardmäßig wird ein Filter **Liefertyp** angewendet, basierend darauf, wie der Arbeitsgang eingerichtet ist. Wenn der Arbeitsgang mit dem Parameter **Alle Aufträge** eingerichtet wird, dann wird dieser Filter angewendet, wenn auf die Auftragserfüllung zugegriffen wird. Gleiches gilt für die Parameter **Filialabholung** und **Versand ab Filiale**. Andere Filter, die auf die Auftragserfüllungsansicht angewendet werden können, sind unter anderem:

- Kundennummer
- Kundenname
- Debitoren-E-Mail
- Auftragsnummer
- Lieferart
- Eingangsnummer
- Kanalreferenzkennung
- Ursprüngliche Shopnummer
- Positionsstatus
- Erstellungsdatum
- Lieferdatum
- Wareneingangsdatum


[!INCLUDE[footer-include](../includes/footer-banner.md)]