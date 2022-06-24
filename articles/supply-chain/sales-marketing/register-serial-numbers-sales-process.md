---
title: Mit serialisierten Artikeln arbeiten
description: Dieser Artikel erläutert, wie Sie Seriennummern auf Lieferscheinen oder Rechnungen während des Verkaufsprozesses erfassen können. Diese Funktion ist sinnvoll, wenn ein Unternehmen nur Seriennummern zu Dienstleistungs- und Garantiezwecken aufzeichnen möchte, aber keine Seriennummern von Zugang bis Abgang im Bestand verwalten muss.
author: Henrikan
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable, InventSerial
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b89e9ab547d13e68ead88d76f9922d14fde4beb3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901849"
---
# <a name="working-with-serialized-items"></a>Mit serialisierten Artikeln arbeiten

[!include [banner](../includes/banner.md)]

Dieser Artikel erläutert, wie Sie Seriennummern auf Lieferscheinen oder Rechnungen während des Verkaufsprozesses erfassen können. Diese Funktion ist sinnvoll, wenn ein Unternehmen nur Seriennummern zu Dienstleistungs- und Garantiezwecken aufzeichnen möchte, aber keine Seriennummern von Zugang bis Abgang im Bestand verwalten muss.

Viele Unternehmen möchten nur Seriennummern zu Dienstleistungs- und Garantiezwecken aufzeichnen und müssen keine Seriennummern von Zugang bis Abgang im Bestand verwalten. In diesen Szenarien können Sie die Seriennummern auf den Lieferscheinen oder Rechnungen erfassen, wenn Produkte verkauft werden. Wenn Produkte später zurückgesendet werden, können Sie jedes Produkt zu einer Rechnung nachverfolgen, um zu bestimmen, ob Sie das Produkt verkauft haben und ob die Service- oder Garantieverpflichtungen gültig sind.

Sie müssen Seriennummern für den Verkaufsprozess aktivieren, indem Sie die Option **Aktiv im Verkaufsprozess** auf der Seite **Rückverfolgungsangabengruppen** auswählen. Folgende Ereignisse treten anschließend in Supply Chain Management auf:
-   Wählen Sie im Inforegister **Seriennummern** die Option **Seriennummernkontrolle** aus. Wenn diese Option ausgewählt ist, müssen Sie eine Seriennummer für jeden Artikel auf dem Lieferschein oder der Rechnung erfassen.
-   Alle Auswahlen auf der Rückverfolgungsangabengruppe für Seriennummern werden deaktiviert, außer der Option **Leerer Abgang zulässig**. Sie können die Option **Leerer Abgang zulässig** auswählen, um die Seriennummernkontrolle zu überschreiben und zuzulasen, dass Produkte ohne Registrierung von Seriennummern verpackt und fakturiert werden.

## <a name="when-do-i-register-serial-numbers-during-the-sales-process"></a>Wann erfasse ich Seriennummern während des Verkaufsprozesses?
Sie können Seriennummern entweder auf dem Lieferschein für einen Auftrag oder auf der Rechnung erfassen. Wenn Sie eine Rechnung für einen serialisierten Artikel vorbereiten, der zusammen mit einem Lieferschein geliefert wurde, können Sie wählen, welche der Seriennummern auf dem Lieferschein fakturiert werden. Die Anzahl der erfassten Seriennummern darf nicht die Menge der versendeten Artikel überschreiten. Wenn Sie eine Teilrechnung erstellen, können Sie weniger serialisierte Artikel auswählen, als auf dem Lieferschein erfasst wurden. Wenn Sie einen Lieferschein oder eine Rechnung drucken, sind die Seriennummern, die erfasst wurden, enthalten.

## <a name="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them"></a>Kann ich Seriennummern eingeben, indem ich sie scanne, oder muss ich sie eingeben?
Sie können entweder Seriennummern scannen oder eingeben. Wenn Sie einen Scanner verwenden, bestimmt der Scanmodus, ob die Seriennummern der Liste der Seriennummern auf der Rechnung oder dem Lieferschein hinzugefügt bzw. von ihr entfernt werden. Wenn Sie Seriennummern scannen möchten, indem Sie beispielsweise einen manuellen Strichcodescanner verwenden, konfigurieren Sie den Scanner so, dass er nach der Seriennummer einen Eingabe- oder TAB-Befehl sendet. Dieser Befehl zeigt das Ende des Datenstreams an. Andernfalls müssen Sie Eingeben oder TAB auf der Tastatur drücken, nachdem Sie jede Seriennummer gescannt haben.

## <a name="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items"></a>Wenn ich Seriennummern für den Verkaufsprozess aktiviere, muss ich alle Seriennummern für alle Artikel erfassen?
Die Einrichtung der Rückverfolgungsangabengruppe, die dem Produkt zugewiesen ist, bestimmt, ob für alle Artikel auf einem Lieferschein oder einer Rechnung die Seriennummern erfasst werden müssen. Wenn Sie Seriennummern für den Verkaufsprozess aktivieren, wird die Option **Seriennummernkontrolle** automatisch ausgewählt. Sie müssen dann eine Seriennummer erfassen oder eine leere Erfassung für eine nicht lesbare Zahl, für jeden Artikel auf dem Lieferschein oder der Rechnung erfassen. Wenn Sie keine Seriennummer für jeden Artikel anfordern möchten, wählen Sie die Option **Leerer Abgang zulässig** auf der Rückverfolgungsangabengruppe aus, die dem Artikel zugeordnet ist. Sie können dann weniger Seriennummern als die Menge der Artikel, die versendet werden, erfassen. Wenn Sie mehr Seriennummern als die Menge der Artikel erfassen, die versendet werden, können Sie den Lieferschein oder die Rechnung nicht buchen oder fakturieren.

## <a name="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments"></a>Kann ich Seriennummern für Teilrechnungen und Teillieferungen erfassen?
Sie können Teilrechnungen und Lieferscheine für Aufträge erstellen und nur die Seriennummern für Artikel erfassen, die diese Rechnungen und Lieferscheine beinhalten. Wenn Sie eine Teilrechnung erstellen möchten und Sie mehr als einen Lieferschein für den Auftrag haben, können Sie Seriennummern von mehr als einem Lieferschein einschließen. Es kann jedoch nur einen Lieferschein geben, der nicht alle Seriennummern umfasst. Wenn also beispielsweise drei Lieferscheine vorliegen und jeder Lieferschein zwei serialisierte Artikel umfasst, können Sie keine Teilrechnung für einen Artikel von jedem Lieferschein erstellen.

## <a name="what-do-i-do-when-a-serial-number-isnt-readable"></a>Was tue ich, wenn eine Seriennummer nicht lesbar ist?
Wenn eine Seriennummer nicht gelesen oder gescannt werden kann, können Sie eine Leerzeile für den Artikel erstellen, indem Sie auf **Nicht lesbar** auf der Seite **Seriennummern** klicken. Wenn die Seriennummer später verfügbar wird, können Sie die Rechnung oder der Lieferschein aktualisieren. Weitere Informationen finden Sie im nächsten Abschnitt mit dem Titel „Kann ich die Seriennummern korrigieren oder ändern, die ich für einen Auftrag erfasst habe?“.

## <a name="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order"></a>Kann ich die Seriennummern korrigieren oder ändern, die ich für einen Auftrag erfasst habe?
Ja, Sie können Seriennummern ändern, wenn die folgenden Bedingungen erfüllt sind:
-   **Rechnungen** – Sie können die Seriennummern für Artikel ändern, die Sie noch nicht fakturiert haben. Der Lieferschein wird dann ebenfalls aktualisiert. Wenn eine Auftragsposition durch das Erfassen einer negativen Menge jedoch korrigiert wurde, können Sie Seriennummern für die Auftragsposition nicht ändern.
-   **Lieferscheine** – Sie können eine Lieferscheinposition, die serialisierte Artikel enthält, nicht teilweise korrigieren. Deshalb müssen Sie die vollständige Menge für die Position stornieren. Wenn ein Lieferschein storniert oder korrigiert wurde, müssen Sie die stornierten Seriennummern nicht erneut erfassen, wenn Sie einen neuen Lieferschein für dieselben serialisierten Artikel erstellen. Die Nummern, die erfasst wurden, werden verwendet.

## <a name="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice"></a>Kann ich die Seriennummern anzeigen, die zusammen mit einem bestimmten Lieferschein geliefert wurden; oder die auf einer Rechnung einbezogen waren?
Ja, können Sie eine Abfrage auf der Lieferscheinerfassungsposition oder der Rechnungserfassungsposition ausführen, um eine Liste aller Seriennummern anzeigen, die im Dokument enthalten waren.

## <a name="can-i-view-the-serialized-items-that-i-have-on-hand"></a>Kann ich die serialisierten Artikel anzeigen, die ich am Lager habe?
Nein, Sie können die serialisierten Artikel nicht anzeigen, die für Sie verfügbar sind, da Seriennummern für Artikel nicht erfasst werden, bis die Artikel verkauft werden.

## <a name="can-i-register-serial-numbers-for-catchweight-items"></a>Kann ich Seriennummern für Artikelgewicht-Artikel erfassen?
Nein, Sie können Seriennummern für Artikelgewichtsartikel während des Verkaufsprozesses nicht erfassen. Wenn darüber hinaus ein Produkt als Artikelgewichtsartikel eingerichtet ist, können Sie das Produkt keiner Rückverfolgungsangabengruppe zuweisen, die so eingerichtet ist, dass sie Seriennummern nur während dem Vertriebsprozess verwendet.

## <a name="can-i-register-serial-numbers-at-the-retail-pos"></a>Kann ich Seriennummern beim Einzelhandels-POS erfassen?

Ja, die Einzelhandelsverkaufsstelle (POS) fordert den Benutzer dazu auf, eine Seriennummer einzugeben, wenn der Benutzer einen Artikel verkauft, dem eine Rückverfolgungsangabengruppe zugewiesen ist, die so eingerichtet ist, dass sie Seriennummern nur während des Vertriebsprozesses verwendet.

## <a name="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process"></a>Welche Sicherheitsrollen sind erforderlich, um Seriennummern während des Verkaufsprozesses zu erfassen?
Diese Funktionalität ist für alle Rollen verfügbar, die Verkaufslieferscheine und Verkaufsrechnungen verwalten können. Die folgenden Aufgaben ermöglichen Arbeitskräften, Seriennummern zu korrigieren und leere Einträge für Seriennummern zu erfassen, die nicht gelesen oder gescannt werden können:
-   Korrekturen von Seriennummern verwalten
-   Registrierung nicht lesbarer Seriennummern verwalten







[!INCLUDE[footer-include](../../includes/footer-banner.md)]