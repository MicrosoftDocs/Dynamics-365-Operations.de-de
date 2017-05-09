---
title: "Überblick über Kreditorenrechnungen"
description: "Dieser Artikel enthält allgemeine Informationen zu Kreditorenrechnungen. Kreditorenrechnungen sind Zahlungsaufforderungen für Produkte und Dienste, die empfangen wurden. Kreditorenrechnungen können eine Rechnung für laufende Dienstleistungen darstellen oder auf Bestellungen für bestimmte Artikel und Dienstleistungen basieren."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: ecd32549b6067ed4c1211996e846e210f77f5013
ms.openlocfilehash: bc6fb66e9038612cc133dc89e60eb3cb75cc7943
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-invoices-overview"></a>Überblick über Kreditorenrechnungen

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält allgemeine Informationen zu Kreditorenrechnungen. Kreditorenrechnungen sind Zahlungsaufforderungen für Produkte und Dienste, die empfangen wurden. Kreditorenrechnungen können eine Rechnung für laufende Dienstleistungen darstellen oder auf Bestellungen für bestimmte Artikel und Dienstleistungen basieren. 

<a name="vendor-invoices"></a>Kreditorenrechnungen
---------------

Eine Kreditorenrechnung für eine Bestellung ist eine Rechnung, die produziert wird, wenn Produkte oder Dienstleistungen gemäß einer vom Kreditor getätigten Bestellung zugestellt wurden. Die Kreditorenrechnung enthält eine Kopfzeile und eine oder mehrere Positionen für Artikel oder Dienstleistungen. Mit der Kreditorenrechnung wird der Zyklus aus Bestellung, Produktempfang und Kreditorenrechnung abgeschlossen. 

Obwohl einige Kreditorenrechnungen mit einer Bestellung verbunden sind, können Kreditorenrechnungen auch Positionen enthalten, die nicht den Bestellpositionen entsprechen. Sie können auch Kreditorenrechnungen erstellen, die keinen Bestellungen zugeordnet sind. Diese Kreditorenrechnungen stellen möglicherweise laufende Dienstleistungen dar, wie eine Nutzungsrechnung. Wenn Sie diese hinzufügen, muß sie nicht auf eine Bestellung verweisen. 

Es gibt mehrere Möglichkeiten, eine Kreditorenrechnung einzugeben:

-   Über das Kreditorenrechnungsbuch können Sie schnell Rechnungen eingeben, die auf keine Bestellung verweisen, und so die Ausgaben antizipieren. Mit der Rechnungsgenehmigungserfassung für Kreditoren können Sie diese Rechnungen auswählen und als Kreditorensaldo buchen, um die Abgrenzungsbeträge zurückzusetzen.
-   In der Kreditorenrechnungserfassung können Sie Rechnungen, die nicht auf eine Bestellung verweisen, schnell in einem Einzelschritt eingeben.
-   Zusammen mit dem Kreditorenrechnungspool, ermöglicht Ihnen das Kreditorenrechnungsregister, Rechnungen zum Antizipieren der Ausgaben schnell zu eingeben, . Sie können die zugeordneten Bestellungen später öffnen, um die Rechnung für das Ausgabenkonto zu buchen.
-   Auf den Seiten **Offene Kreditorenrechnungen** und **Ausstehende Kreditorenrechnungen** können Sie Kreditorenrechnung auf Basis bestätigter Bestellungen erstellen.

In der nachstehenden Erläuterung finden Sie weitere Informationen dazu, wie Sie **Offene Kreditorenrechnungen** oder **Ausstehende Kreditorenrechnungen** verwenden, um eine Kreditorenrechnung aus einer Bestellung zu erstellen.

## <a name="understanding-invoice-line-quantities"></a>Rechnungspositionsmengen verstehen
Wenn Sie eine Kreditorenrechnung für eine entsprechenden Bestellung öffnen, werden die Rechnungspositionen aus der Bestellung erstellt. Standardmäßig werden die Mengen aus der Produktzugangsmenge übernommen. Allerdings können Sie jedes der folgenden Standardverhalten verwenden:

-   **Menge der aktuellen Lieferung** - Verwenden Sie diese Option für Teillieferungen. Der Standardwert im Feld **Menge** stammt aus dem Mengenfeld **Aktuelle Lieferung** der Bestellung.
-   **Bestellte Menge** - Verwenden Sie diese Option für vollständige Lieferungen. Die Standardmenge im Feld **Menge** stammt aus dem Mengenfeld **Bestellt** der Bestellung.
-   **Erfasste Menge** - Verwenden Sie diese Option, wenn der Artikel erfasst werden muss, wie auf der Seite **Lagersteuerungsgruppen** angegeben. Bei dem Standardwert im Feld **Menge** handelt es sich um die registrierte physische Aktualisierungsmenge.
-   **Produktzugangsmenge** – Verwenden Sie diese Option, wenn für den Auftrag bereits ein Produktzugang eingegangen ist. Beim Standardwert im Feld **Menge** handelt es sich um die Gesamtmenge der verfügbaren Produktzugänge.
-   **Erfasste Menge und Services** – Verwenden Sie diese Option, wenn Mengen für gelagerte oder nicht gelagerte Artikel in der Wareneingangserfassungen registriert wurden. Diese Option schließt auch registrierte und nicht registrierte Dienstleistungen ein.

Wenn Ihre juristische Person den Rechnungsabgleich verwendet, können Sie die Ergebnisse der Menge anzeigen, die mit der Spalte **Produktzugang-Mengenabgleich** übereinstimmt. Sie können auch den Menübefehl **Detailabgleich** auf der Registerkarte **Prüfen** verwenden, um die Ergebnisse des Mengenabgleichens anzuzeigen.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Eine Position hinzufügen, die nicht in der Bestellung war
Sie können der Kreditorenrechnung eine neue Position hinzuzufügen, die nicht in der Bestellung enthalten war. Sie müssen eine Artikelnummer oder eine Beschaffungskategorie auswählen. Sie können nun Mengen, Preise und Beträge der Position hinzufügen. Die Position wird nur in die Abgleichsrichtlinien für Rechnungssummen einbezogen.

## <a name="submitting-a-vendor-invoice-for-review"></a>Senden einer Kreditorenrechnung zur Prüfung
Möglicherweise werden in der Organisation Workflows zur Verwaltung des Prüfprozesses für Kreditorenrechnungen verwendet. Der Prüfungsworkflow kann für den Rechnungskopf und/oder die Rechnungsposition erforderlich sein. Die Steuerelemente des Workflows werden je nachdem, worauf der Fokus vor dem Klicken auf das Steuerelement lag, auf die Kopfzeile oder die Position angewendet. Statt der Schaltfläche **Buchen** finden Sie eine **Übermitteln** Schaltfläche, die Sie verwenden können, um die Kreditorenrechnung durch den Prüfprozess zu senden.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Abgleichen von Kreditorenrechnungen mit Produktzugängen
Sie können Informationen zu Kreditorenrechnungen eingeben und speichern, und Sie können Rechnungspositionen mit Produktzugangspositionen abgleichen. Für eine Position können auch Teilmengen abgeglichen werden. 

Sie können eine Kreditorenrechnung basierend auf den bisher empfangenen Artikeln der Produktzugangspositionen erstellen, auch wenn noch nicht alle Artikel einer bestimmten Bestellung eingegangen sind. Das kann der Fall sein, wenn ein Kreditor monatlich eine Rechnung zu allen Lieferungen sendet, die er während des Monats geleistet hat. Jeder Produktzugang stellt eine teilweise oder vollständig abgeschlossene Artikellieferung für die Bestellung dar. 

Durch Buchen der Rechnung wird die Menge des **Rechnungsrestbetrags** jedes Artikels mit der Summe der eingegangenen Mengen aus den ausgewählten Produktzugängen aktualisiert. Wenn sowohl die Menge für den **Rechnungsrestbetrag** als auch die Menge **Rest liefern** für alle Artikel des Auftrags gleich 0 (Null) ist, wird der Status der Bestellung zu **In Rechnung gestellt** geändert. Ist die Menge des **Rechnungsrestbetrags** nicht 0 (Null), bleibt der Status der Bestellung unverändert, und es können weitere Rechnungen für den Auftrag erstellt werden.

Für die folgende Option wird vorausgesetzt, dass für die Bestellung mindestens ein Produktzugang gebucht wurde. Die Kreditorenrechnung basiert auf diesen Produktzugängen und enthält die auf den Lieferscheinen angegebenen Mengen. Die Finanzinformationen für die Rechnung basieren auf den beim Buchen der Rechnung eingegebenen Informationen.

## <a name="working-with-multiple-invoices"></a>Arbeiten mit mehreren Rechnungen

Mehrere Rechnungen können zur gleichen Zeit bearbeitet und gleichzeitig gebucht werden. Wenn Sie mehrere Rechnungen erstellen müssen, verwenden Sie die Seite **Ausstehende Kreditorenrechnungen**. Wenn sie mehrere Kreditorenrechnungen buchen und drucken müssen, verwenden Sie die Seite "Rechnungsgenehmigungserfassung". Wenn Sie die Rechnungsgenehmigungserfassung verwenden, muss mindestens ein Produktzugang der Bestellung und eine Rechnung für die Bestellung in einem Rechnungsbuch gebucht sein. Die Finanzdaten für die Rechnung stammen aus der im Register gebuchten Rechnung.





