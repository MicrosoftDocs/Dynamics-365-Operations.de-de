---
title: Seriennummern im Vertriebsprozess registrieren
description: Dieses Thema erläutert, wie Sie Seriennummern auf Lieferscheinen oder Rechnungen während des Verkaufsprozesses erfassen können. Diese Funktion ist sinnvoll, wenn ein Unternehmen nur Seriennummern zu Dienstleistungs- und Garantiezwecken aufzeichnen möchte, aber keine Seriennummern von Zugang bis Abgang im Bestand verwalten muss.
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e86c2f8d1d5920198db74dc3b64f2393c5e13ff7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "350411"
---
# <a name="register-serial-numbers-in-the-sales-process"></a>Seriennummern im Vertriebsprozess registrieren

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Dieses Thema erläutert, wie Sie Seriennummern auf Lieferscheinen oder Rechnungen während des Verkaufsprozesses erfassen können. Diese Funktion ist sinnvoll, wenn ein Unternehmen nur Seriennummern zu Dienstleistungs- und Garantiezwecken aufzeichnen möchte, aber keine Seriennummern von Zugang bis Abgang im Bestand verwalten muss.

Viele Unternehmen möchten nur Seriennummern zu Dienstleistungs- und Garantiezwecken aufzeichnen und müssen keine Seriennummern von Zugang bis Abgang im Bestand verwalten. In diesen Szenarien ermöglicht Microsoft Dynamics 365 for Finance and Operations es Ihnen, die Seriennummern auf den Lieferscheinen oder Rechnungen zu erfassen, wenn Produkte verkauft werden. Wenn Produkte später zurückgesendet werden, können Sie jedes Produkt zu einer Rechnung nachverfolgen, um zu bestimmen, ob Sie das Produkt verkauft haben und ob die Service- oder Garantieverpflichtungen gültig sind.

Sie müssen Seriennummern für den Verkaufsprozess aktivieren, indem Sie die Option **Aktiv im Verkaufsprozess** auf der Seite **Rückverfolgungsangabengruppen** auswählen. Folgende Ereignisse treten in Microsoft Dynamics 365 for Finance and Operations auf:
-   Wählen Sie im Inforegister **Seriennummern** die Option **Seriennummernkontrolle** aus. Wenn diese Option ausgewählt ist, müssen Sie eine Seriennummer für jeden Artikel auf dem Lieferschein oder der Rechnung erfassen.
-   Alle Auswahlen auf der Rückverfolgungsangabengruppe für Seriennummern werden deaktiviert, außer der Option **Leerer Abgang zulässig**. Sie können die Option **Leerer Abgang zulässig** auswählen, um die Seriennummernkontrolle zu überschreiben und zuzulasen, dass Produkte ohne Registrierung von Seriennummern verpackt und fakturiert werden.

## <a name="when-do-i-register-serial-numbers-during-the-sales-process"></a>Wann erfasse ich Seriennummern während des Verkaufsprozesses?
Sie können Seriennummern entweder auf dem Lieferschein für einen Auftrag oder auf der Rechnung erfassen. Wenn Sie eine Rechnung für einen serialisierten Artikel vorbereiten, der zusammen mit einem Lieferschein geliefert wurde, können Sie wählen, welche der Seriennummern auf dem Lieferschein fakturiert werden. Die Anzahl der erfassten Seriennummern darf nicht die Menge der versendeten Artikel überschreiten. Wenn Sie eine Teilrechnung erstellen, können Sie weniger serialisierte Artikel auswählen, als auf dem Lieferschein erfasst wurden. Wenn Sie einen Lieferschein oder eine Rechnung drucken, sind die Seriennummern, die erfasst wurden, enthalten.

## <a name="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them"></a>Kann ich Seriennummern eingeben, indem ich sie scanne, oder muss ich sie eingeben?
Sie können entweder Seriennummern scannen oder eingeben. Wenn Sie einen Scanner verwenden, bestimmt der Scanmodus, ob die Seriennummern der Liste der Seriennummern auf der Rechnung oder dem Lieferschein hinzugefügt bzw. von ihr entfernt werden. Wenn Sie Seriennummern scannen möchten, indem Sie beispielsweise einen Handbarcodescanner verwenden, konfigurieren Sie den Scanner, um einen Befehl Eingeben oder einen TAB-Befehl nach der Seriennummer zu senden. Dieser Befehl zeigt das Ende des Datenstreams an. Andernfalls müssen Sie Eingeben oder TAB auf der Tastatur drücken, nachdem Sie jede Seriennummer gescannt haben.

## <a name="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items"></a>Wenn ich Seriennummern für den Verkaufsprozess aktiviere, muss ich alle Seriennummern für alle Artikel erfassen?
Die Einstellungen der Rückverfolgungsangabengruppe, die dem Produkt zugewiesen sind, bestimmen, ob Seriennummern für alle Artikel auf einem Lieferschein oder einer Rechnung erfasst werden müssen. Wenn Sie Seriennummern für den Verkaufsprozess aktivieren, wird die Option **Seriennummernkontrolle** automatisch ausgewählt. Sie müssen dann eine Seriennummer erfassen oder eine leere Erfassung für eine nicht lesbare Zahl, für jeden Artikel auf dem Lieferschein oder der Rechnung erfassen. Wenn Sie keine Seriennummer für jeden Artikel anfordern möchten, wählen Sie die Option **Leerer Abgang zulässig** auf der Rückverfolgungsangabengruppe aus, die dem Artikel zugeordnet ist. Sie können dann weniger Seriennummern als die Menge der Artikel, die versendet werden, erfassen. Wenn Sie mehr Seriennummern als die Menge der Artikel erfassen, die versendet werden, können Sie den Lieferschein oder die Rechnung nicht buchen oder fakturieren.

## <a name="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments"></a>Kann ich Seriennummern für Teilrechnungen und Teillieferungen erfassen?
Sie können Teilrechnungen und Lieferscheine für Aufträge erstellen und nur die Seriennummern für Artikel erfassen, die diese Rechnungen und Lieferscheine beinhalten. Wenn Sie eine Teilrechnung erstellen möchten und Sie mehr als einen Lieferschein für den Auftrag haben, können Sie Seriennummern von mehr als einem Lieferschein einschließen. Es kann jedoch nur einen Lieferschein geben, der nicht alle Seriennummern umfasst. Wenn also beispielsweise drei Lieferscheine vorliegen und jeder Lieferschein zwei serialisierte Artikel umfasst, können Sie keine Teilrechnung für einen Artikel von jedem Lieferschein erstellen.

## <a name="what-do-i-do-when-a-serial-number-isnt-readable"></a>Was tue ich, wenn eine Seriennummer nicht lesbar ist?
Wenn eine Seriennummer nicht gelesen oder gescannt werden kann, können Sie eine Leerzeile für den Artikel erstellen, indem Sie auf **Nicht lesbar** auf der Seite **Seriennummern** klicken. Wenn die Seriennummer später verfügbar wird, können Sie die Rechnung oder der Lieferschein aktualisieren. Weitere Informationen finden Sie im nächsten Abschnitt, "Kann ich die Seriennummern korrigieren oder ändern, die ich für einen Auftrag erfasst habe?"

## <a name="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order"></a>Kann ich die Seriennummern korrigieren oder ändern, die ich für einen Auftrag erfasst habe?
Ja, Sie können Seriennummern ändern, wenn die folgenden Bedingungen erfüllt sind:
-   **Rechnungen**  – Sie können die Seriennummern für Artikel ändern, die Sie noch nicht fakturiert haben. Der Lieferschein wird dann ebenfalls aktualisiert. Wenn eine Auftragsposition durch das Erfassen einer negativen Menge jedoch korrigiert wurde, können Sie Seriennummern für die Auftragsposition nicht ändern.
-   **Lieferscheine**  – Sie können eine Lieferscheinposition nicht teilweise korrigieren, die serialisierte Artikel enthält. Deshalb müssen Sie die vollständige Menge für die Position stornieren. Wenn ein Lieferschein storniert oder korrigiert wurde, müssen Sie die stornierten Seriennummern nicht erneut erfassen, wenn Sie einen neuen Lieferschein für dieselben serialisierten Artikel erstellen. Die Nummern, die erfasst wurden, werden verwendet.

## <a name="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice"></a>Kann ich die Seriennummern anzeigen, die zusammen mit einem bestimmten Lieferschein geliefert wurden; oder die auf einer Rechnung einbezogen waren?
Ja, können Sie eine Abfrage auf der Lieferscheinerfassungsposition oder der Rechnungserfassungsposition ausführen, um eine Liste aller Seriennummern anzeigen, die im Dokument enthalten waren.

## <a name="can-i-view-the-serialized-items-that-i-have-on-hand"></a>Kann ich die serialisierten Artikel anzeigen, die ich am Lager habe?
Nein, Sie können die serialisierten Artikel nicht anzeigen, die für Sie verfügbar sind, da Seriennummern für Artikel nicht erfasst werden, bis die Artikel verkauft werden.

## <a name="can-i-register-serial-numbers-for-catchweight-items"></a>Kann ich Seriennummern für Artikelgewicht-Artikel erfassen?
Nein, Sie können Seriennummern für Artikelgewichtsartikel während des Verkaufsprozesses nicht erfassen. Wenn darüber hinaus ein Produkt als Artikelgewichtsartikel eingerichtet ist, können Sie das Produkt keiner Rückverfolgungsangabengruppe zuweisen, die eingerichtet ist, um Seriennummern nur während des Verkaufsprozesses zu verwenden.

## <a name="can-i-register-serial-numbers-at-the-retail-pos"></a>Kann ich Seriennummern beim Einzelhandels-POS erfassen?

Ja, die Einzelhandelsverkaufsstelle (POS) fordert den Benutzer dazu auf, eine Seriennummer einzugeben, wenn der Benutzer einen Artikel verkauft, dem eine Rückverfolgungsangabengruppe zugewiesen ist, die eingerichtet wird, um Seriennummern nur während des Verkaufsprozesses zu verwenden.

## <a name="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process"></a>Welche Sicherheitsrollen sind erforderlich, um Seriennummern während des Verkaufsprozesses zu erfassen?
Diese Funktionalität ist für alle Rollen verfügbar, die Verkaufslieferscheine und Verkaufsrechnungen verwalten können. Die folgenden Aufgaben ermöglichen Arbeitskräften, Seriennummern zu korrigieren und leere Einträge für Seriennummern zu erfassen, die nicht gelesen oder gescannt werden können:
-   Korrekturen von Seriennummern verwalten
-   Registrierung nicht lesbarer Seriennummern verwalten





