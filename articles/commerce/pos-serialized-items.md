---
title: Arbeiten mit serialisierten Artikeln in der POS
description: In diesem Thema wird erläutert, wie Sie serialisierte Artikel in der Verkaufsstellen-(POS)-Anwendung verwalten.
author: boycezhu
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 39135111a8e7bf16d1e56ca42726ae8a8e130c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798680"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Arbeiten mit serialisierten Artikeln in der POS

[!include [banner](includes/banner.md)]

Viele Einzelhändler verkaufen Produkte, die eine serielle Kontrolle erfordern. Diese Produkte werden als *serialisierte Artikel* bezeichnet. Einige Einzelhändler möchten möglicherweise Seriennummern im Shop- oder Lagerortbestand für Nachverfolgungszwecke beibehalten. Andere Einzelhändler möchten möglicherweise während des Verkaufsprozesses Seriennummern für Service- und Garantiezwecke erfassen. In diesem Thema wird erläutert, wie Sie serialisierte Artikel in der Microsoft Dynamics 365 Commerce-Verkaufsstellen-(POS)-Anwendung verwalten können.

## <a name="serial-number-configurations"></a>Seriennummernkonfigurationen

Ein Artikel wird als serialisierter Artikel betrachtet, wenn ihm eine Rückverfolgungsangaben-Gruppe zugewiesen ist, der eingerichtet ist, um Seriennummern zu ermöglichen. Wählen Sie in der Commerce-Zentralverwaltung auf der **Verfolgen von Dimensionsgruppen**-Seite die **Aktiv**-Option, um Seriennummern für den Inventarisierungsprozess zu aktivieren, oder wählen Sie die **Aktiv im Verkaufsprozess**-Option zum Aktivieren von Seriennummern für den Verkaufsprozess.

Schalten Sie im Inforegister **Rückverfolgungsangaben** die Parameter **Leerer Zugang zulässig** ein, um zuzulassen, dass die Seriennummer eine optionale Eingabe während des Bestandszugangsprozesses ist. Durch das Deaktivieren dieses Parameters wird die Seriennummer als erforderliche Eingabe erzwungen. Ebenso steuert der **Leerer Abgang zulässig** -Parameter, ob während des Bestandsversandvorgangs eine Seriennummer erforderlich ist.

> [!NOTE]
> Um die POS-Vorgänge **Eingehender Bestand** oder **Ausgehender Bestand** zu verwenden, um Seriennummern gegenüber einem serialisierten Artikel zu registrieren oder zu validieren, müssen Sie diesen Artikel so konfigurieren, dass er einer Rückverfolgungsangaben-Gruppe zugewiesen wird, die so eingerichtet ist, dass Seriennummern für die Option **Aktiv**, nicht für die Option **Aktiv im Verkaufsprozess** zulässig sind.

## <a name="serial-number-management-page"></a>Seite zur Verwaltung der Seriennummer

Wenn es sich bei dem ausgewählten, empfangenen oder versendeten Artikel in den **Eingangsbestand**- und **Ausgangsbestand**-POS-Vorgängen um einen serialisierten Artikel handelt, enthält der **Einzelheiten**-Bereich eine **Seriennummer verwalten**-Option, die auf die **Seriennummernverwaltung**-Seite verweist, auf der Sie Seriennummern für den Artikel registrieren oder validieren können. Alternativ können Sie die Seite **Seriennummernverwaltung** öffnen, entweder durch die Auswahl der **Seriennummer**-Aktion in der App-Leiste der Auftragsdetailansicht oder durch Auswahl von **Seriennummer verwalten** im Dialogfeld, das Sie während des Empfangs- oder Lieferprozesses auffordert. 

Die Seite **Seriennummernverwaltung** listet alle offenen Seriennummernpositionen auf, deren Registrierung oder Überprüfung aussteht. Auf dieser Seite befinden sich möglicherweise zwei Registerkarten: eine für den aktuellen Artikel und eine andere für alle serialisierten Artikel im Auftrag.

Das Feld **Status** auf der Seite **Seriennummernverwaltung** bietet Informationen über die aktuelle Phase, in der sich jede Seriennummer befindet:

- **Nicht registriert** – Die Seriennummer wurde nicht angegeben oder die vorregistrierte Seriennummer wurde noch nicht überprüft (im Empfangsprozess).
- **Wird registriert** – Die Seriennummer wurde registriert und lokal in der Kanaldatenbank der Filiale gespeichert, oder die vorregistrierte Seriennummer wurde überprüft. Nur Seriennummern mit dem Status **Wird registriert** werden zur Commerce-Zentrale übermittelt, wenn Sie Ihrem Empfang oder Ihre Erfüllung abschließen.

## <a name="receive-serialized-items"></a>Serialisierte Artikel empfangen

Der POS-Vorgang **Eingehender Bestand** ermöglicht es Benutzern, die folgenden Aufgaben für serialisierte Elemente auszuführen:

- Registrieren Sie Seriennummern für serialisierte Artikel, wenn diese Artikel über eine Bestellung in der Filiale eingehen.
- Überprüfen Sie vorregistriere Seriennummern für serialisierte Artikel, wenn diese Artikel über eine Bestellung oder ein Umlagerungsauftrag in der Filiale eingehen.

### <a name="register-serial-numbers-against-serialized-items"></a>Registrieren Sie Seriennummern für serialisierte Artikel

Für eine Bestellung werden Sie von einem Dialogfeld mit der Option **Seriennummer verwalten** während des Empfangsprozesses eines serialisierten Artikels aufgefordert. Sie können diese Option auswählen, um die Seite **Seriennummernverwaltung** zu öffnen und mit der Registrierung von Seriennummern zu beginnen. Sie können diesen Schritt auch während des Empfangsprozesses überspringen und die Eingabe später bereitstellen, bevor der Beleg gebucht wird.

Standardmäßig wird die Registerkarte für den aktuellen Artikel angezeigt. Alle Seriennummernpositionen haben einen leeren Seriennummernwert und den Status **Nicht registriert**. Sie können Seriennummern-Strichcodes scannen oder **Seriennummer** in der App-Leiste auswählen, um fortlaufend Seriennummern einzugeben. Die von Ihnen eingegebenen Seriennummern werden in der Liste angezeigt, und ihr Status wird in **Wird registriert** geändert. Die maximale Anzahl von Seriennummern, die Sie in der Liste registrieren können, entspricht der Empfangsmenge. Wenn Sie einen Fehler machen, können Sie **Bearbeiten** oder **Löschen** im Bereich **Details** auswählen, um Änderungen an den von Ihnen eingegebenen Seriennummern vorzunehmen.

Sie können auch Seriennummern auf der Registerkarte **Alle serialisierten Artikel** der Seite **Seriennummernverwaltung** registrieren. Wählen Sie in der Liste den Artikel aus, für den Sie Seriennummern registrieren möchten.

### <a name="validate-serial-numbers-on-serialized-items"></a>Seriennummern für serialisierte Artikel überprüfen

Bei einem Umlagerungsauftrag muss die ausgehende Seite während des Versandvorgangs Seriennummern für die serialisierten Artikeln vorregistrieren. Bei einer Bestellung kann der Lieferant Informationen zur Seriennummer über einen Versand-Avis (ASN) bereitstellen, und Sie können die Nummern der zu versendenden Artikel vorregistrieren. In beiden Fällen sind die Seriennummern vor dem Empfang bekannt. Auf der eingehenden Seite müssen Sie daher nur überprüfen, ob Sie das erhalten haben, was Sie erhalten sollten.

Um Seriennummern zu überprüfen, können Sie die Seite **Seriennummernverwaltung** öffnen, entweder während des Empfangsprozesses oder zu einem beliebigen Zeitpunkt, bevor der Empfang verbucht wird. Für jeden serialisierten Artikel mit vorregistrierten Seriennummern werden alle Seriennummern automatisch auf den Anfangsstatus **Nicht registriert** auf dieser Seite festgelegt. Um Seriennummern zu validieren, können Sie diese scannen oder eingeben. Bei der Eingabe der Seriennummer überprüft die Anwendung, ob sie mit vorregistrierten Seriennummern übereinstimmen. Wenn sie übereinstimmen, wird ihr Status in **Wird registriert** geändert. Anderenfalls wird eine Fehlermeldung angezeigt. Alternativ können Sie direkt eine Seriennummer und dann die **Seriennummer überprüfen**-Option im **Einzelheiten**-Bereich auswählen, um diese Seriennummer schnell als validiert zu markieren. Die maximale Anzahl von Seriennummern, die Sie in der Liste überprüfen können, entspricht der Empfangsmenge.

Sie können auch Seriennummern auf der Registerkarte **Alle serialisierten Artikel** der Seite **Seriennummernverwaltung** registrieren. Wählen Sie in der Liste den Artikel aus, für den Sie Seriennummern überprüfen möchten.

## <a name="ship-serialized-items"></a>Versenden serialisierter Artikel

Sie können den **Ausgangsbestand**-POS-Vorgang zum Registrieren von Seriennummern für serialisierte Artikel verwenden, wenn diese über einen Transportauftrag aus dem aktuellen Shop versendet werden.

### <a name="register-serial-numbers-against-serialized-items"></a>Registrieren Sie Seriennummern für serialisierte Artikel

Für einen Transfer werden Sie von einem Dialogfeld mit der Option **Seriennummer verwalten** während des Versandprozesses eines serialisierten Artikels aufgefordert. Sie können die Option auswählen, um die Seite **Seriennummernverwaltung** zu öffnen und mit der Registrierung von Seriennummern zu beginnen. Sie können diesen Schritt auch während des Versandprozesses überspringen und den Versand später bereitstellen, bevor der Beleg gebucht wird.

Standardmäßig wird die Registerkarte für den aktuellen Artikel angezeigt. Alle Seriennummernpositionen haben einen leeren Seriennummernwert und den Status **Nicht registriert**. Sie können Seriennummern-Strichcodes scannen oder **Seriennummer** in der App-Leiste auswählen, um fortlaufend Seriennummern einzugeben. Die von Ihnen eingegebenen Seriennummern werden in der Liste angezeigt, und ihr Status wird in **Wird registriert** geändert. Die maximale Anzahl von Seriennummern, die Sie in der Liste registrieren können, entspricht der Versandmenge. Wenn Sie einen Fehler machen, können Sie **Bearbeiten** oder **Löschen** im Bereich **Details** auswählen, um Änderungen an den von Ihnen eingegebenen Seriennummern vorzunehmen.

Sie können auch Seriennummern auf der Registerkarte **Alle serialisierten Artikel** der Seite **Seriennummernverwaltung** registrieren. Wählen Sie in der Liste den Artikel aus, für den Sie Seriennummern registrieren möchten.

Optional können Sie die Überprüfung der Verfügbarkeit von Seriennummern während der Registrierung der Seriennummer für einen ausgehenden Überweisungsauftrag aktivieren. Wenn Sie bei dieser Validierung versuchen, eine Seriennummer zu versenden, die nicht im Bestand des Versandgeschäfts verfügbar ist, erhalten Sie eine Fehlermeldung und müssen eine andere Nummer angeben.

Um eine solche Validierung als Voraussetzung zu aktivieren, müssen Sie die folgenden Einzelvorgänge so planen, dass sie regelmäßig ausgeführt werden:

- **Einzelhandel und Handel** > **Einzelhandel und Handel IT** > **Produkte und Bestand** > **Produktverfügbarkeit mit Rückverfolgungsangaben**
- **Einzelhandel und Handel** > **Verteilungspläne** > **1130** (**Produktverfügbarkeit**)

## <a name="sell-serialized-items-in-pos"></a>Serialisierte Artikel am POS verkaufen

Während die POS-Anwendung den Verkauf von serialisierten Artikeln immer unterstützt hat, können Unternehmen in Commerce Version 10.0.17 und höher Funktionen aktivieren, die die Geschäftslogik verbessern, die beim Verkauf von Produkten ausgelöst wird, die für die Nachverfolgung von Seriennummern konfiguriert sind.

Wenn die Funktion **Verbesserte Validierung der Seriennummer bei der POS-Auftragserfassung und Auftragserfüllung** aktiviert ist, werden die folgenden Produktkonfigurationen beim Verkauf von serialisierten Produkten am POS ausgewertet:

- **Serientyp**-Setup für das Produkt (**aktiv** oder **im Verkauf aktiv**).
- **Leere Abgang zulässig**-Einstellungen für das Produkt.
- **Physischer negativer Bestand**-Einstellungen für das Produkt und/oder das Verkaufslager.

### <a name="active-serial-configurations"></a>Aktive Serienkonfigurationen

Wenn Artikel am POS verkauft werden, die mit einer **Aktiven** Rückverfolgungsangaben für Seriennummern konfiguriert sind, initiiert POS eine Validierungslogik, die verhindert, dass Benutzer den Verkauf eines serialisierten Artikels mit einer Seriennummer abschließen, die nicht im aktuellen Inventar des Verkaufslagers enthalten ist. Es gibt zwei Ausnahmen von dieser Validierungsregel:

- Wenn das Element auch mit aktiviertem **Leere Abgabe zulässig** konfiguriert ist, können Benutzer die Eingabe der Seriennummer überspringen und den Artikel ohne Seriennummernbezeichnung verkaufen.
- Wenn der Artikel und/oder das Verkaufslager mit aktiver Option **Physische negativer Bestand** konfiguriert ist, akzeptiert und verkauft die Anwendung eine Seriennummer, die in dem Lager, von dem verkauft wird, nicht als Bestand bestätigt werden kann. Diese Konfiguration ermöglicht, dass die Bestandstransaktion für diese bestimmte Artikel-/Seriennummer negativ wird, und daher ermöglicht das System den Verkauf unbekannter Seriennummern.

> [!IMPORTANT]
> Um sicherzustellen, dass die POS-Anwendung ordnungsgemäß überprüfen kann, ob die Seriennummern, die für **Aktive** Serientypartikel verkauft werden, sich im Bestand des Verkaufslagers befinden, ist es erforderlich, dass Unternehmen den Auftrag **Produktverfügbarkeit mit Rückverfolgungsangaben** häufig in der Commerce-Zentralverwaltung ausführen, ebenso wie den zugehörigen **1130**-Auftrag zur Verteilung der Produktverfügbarkeit über die Commerce-Zentralverwaltung. Da neuer serialisierter Bestand in den Verkaufslagern eingeht, muss der Bestandsmaster die Kanaldatenbank regelmäßig mit den aktuellen Bestandsverfügbarkeitsdaten aktualisieren, damit der POS die Bestandsverfügbarkeit der verkauften Seriennummern überprüfen kann. Der **Produktverfügbarkeit mit Rückverfolgungsangaben**-Auftrag erstellt eine aktuelle Momentaufnahme des Hauptinventars, einschließlich der Seriennummern, für alle Firmenlager. Der **1130**-Verteilungsauftrag erstellt diese Bestandsmomentaufnahme und teilt sie mit allen konfigurierten Kanaldatenbanken.

### <a name="active-in-sales-process-serial-configurations"></a>Aktive Seriennummern des Vertriebsprozesses

Artikel, die mit der Seriendimension als **Im Verkaufsprozess aktiv** konfiguriert sind, durchlaufen keine Bestandsvalidierungslogik, da diese Konfiguration impliziert, dass die Bestandsseriennummern nicht vorab in den Bestand registriert sind und die Seriennummern nur zum Zeitpunkt des Verkaufs erfasst werden.  

Wenn **Leere Abgabe zulässig** auch für als **Im Verkaufsprozess aktiv** konfigurierte Artikel konfiguriert ist, kann die Eingabe der Seriennummer übersprungen werden. Wenn **Leere Abgabe zulässig** nicht konfiguriert ist, fordert die Anwendung vom Benutzer, die Eingabe einer Seriennummer, die jedoch nicht anhand des verfügbaren Bestands überprüft wird.

### <a name="apply-serial-numbers-during-creation-of-pos-transactions"></a>Beim Erstellen von POS-Transaktionen Seriennummern anwenden

Die POS-Anwendung fordert Benutzer beim Verkauf eines serialisierten Artikels sofort zur Erfassung der Seriennummer auf. Mit der Anwendung können Benutzer jedoch die Eingabe von Seriennummern bis zu einem bestimmten Punkt im Verkaufsprozess überspringen. Wenn der Benutzer mit der Erfassung der Zahlung beginnt, erzwingt die Anwendung die Eingabe der Seriennummer für alle Artikel, die nicht für die Erfüllung durch zukünftige Sendungen oder Abholungen konfiguriert sind. Bei serialisierten Artikeln, die für Abholungs- oder Bargelderfüllung konfiguriert sind, muss der Benutzer die Seriennummer erfassen (oder sich damit einverstanden erklären, sie leer zu lassen, wenn die Artikelkonfiguration dies zulässt), bevor er den Verkauf abschließt.

Bei serialisierten Artikeln, die zur zukünftigen Abholung oder zum Versand verkauft werden, können POS-Benutzer die Eingabe der Seriennummer zunächst überspringen und dennoch die Erstellung der Kundenbestellung abschließen.   

> [!NOTE]
> Beim Verkauf oder der Erfüllung von serialisierten Produkten über die POS-Anwendung wird für die serialisierten Artikel in der Verkaufstransaktion eine Menge von „1“ erzwungen. Dies ist ein Ergebnis der Art und Weise der Verfolgung der Seriennummerninformationen in der Verkaufszeile. Beim Verkauf oder der Ausführung einer Transaktion für mehrere serialisierte Artikel über den POS muss jede Verkaufszeile nur mit einer Menge von „1“ konfiguriert werden. 

### <a name="apply-serial-numbers-during-customer-order-fulfillment-or-pickup"></a>Seriennummern während der Auftragserfüllung oder Abholung anwenden

Bei der Erfüllung von Kundenauftragspositionen für serialisierte Produkte mit dem Vorgang **Auftragserfüllung** am POS erzwingt der POS die Erfassung der Seriennummer vor der endgültigen Erfüllung. Wenn bei der Erstbestellungserfassung keine Seriennummer angegeben wurde, muss diese daher während des Kommissionierungs-, Verpackungs- oder Versandprozesses am POS erfasst werden. Bei jedem Schritt wird eine Validierung durchgeführt, und der Benutzer wird nur dann nach Seriennummern gefragt, wenn diese fehlen oder nicht mehr gültig sind. Wenn ein Benutzer beispielsweise die Schritte zum Kommissionieren oder Verpacken überspringt und sofort eine Sendung initiiert und keine Seriennummer für die Leitung registriert wurde, muss die Seriennummer vor Abschluss des letzten Rechnungsschritts am POS eingegeben werden. Wenn Sie die Erfassung der Seriennummer während der Auftragserfüllung am POS erzwingen, gelten weiterhin alle zuvor in diesem Thema genannten Regeln. Nur als **Aktiv** serialisierte konfiguriert Elemente durchlaufen eine Bestandsüberprüfung der Seriennummer. Als **Im Verkaufsprozess aktiv** konfigurierte Elemente werden nicht validiert. Wenn **Physischer negativer Bestand** für **Aktiv**-Produkte zulässig ist, wird jede Seriennummer akzeptiert, unabhängig von der Verfügbarkeit des Bestands. Für **Aktive** und **Um Verkaufsprozess aktive** Artikel kann ein Benutzer, wenn **Leere Abgabe zulässig** konfiguriert ist, bei die Seriennummern Bedarf während der Schritte zum Kommissionieren, Verpacken und Versenden leer lassen.

Validierungen für Seriennummern werden auch durchgeführt, wenn ein Benutzer die Abholvorgänge für Kundenbestellungen am POS ausführt. Die POS-Anwendung ermöglicht nicht, dass eine Abholung eines serialisierten Produkts abgeschlossen wird, es sei denn, sie besteht die oben genannten Validierungen. Die Validierungen basieren immer auf der Rückverfolgungsangaben des Produkts und den Verkaufslagerkonfigurationen. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eingehender Bestandsvorgang in POS](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Ausgehender Bestandsvorgang in POS](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)


[!INCLUDE[footer-include](../includes/footer-banner.md)]