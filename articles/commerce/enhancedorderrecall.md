---
title: Auftragsrückrufe in POS
description: In diesem Artikel werden die Funktionen erläutert, die für verbesserte Auftragsrückrufseiten in POS verfügbar sind.
author: hhainesms
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0624c251646110644a8a72658a6dd6f8d319c57f
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734293"
---
# <a name="recall-order-operation-in-pos"></a>Auftragsrückrufe in POS

[!include [banner](includes/banner.md)]

Der Vorgang **Auftrag zurückrufen** in der Commerce-Verkaufsstelle (POS) bietet aktualisierte Funktionen zum Suchen und Filtern von Aufträgen sowie auftragsspezifische Informationen. Diese Funktion ist in Commerce Version 10.0.15 und höher verfügbar.

Um diese Funktionalität zu aktivieren, schalten Sie die Funktion **Verbesserter Auftragsrückruf in POS** im **Funktionsverwaltung**-Arbeitsbereich in der Commerce-Zentrale ein. Nachdem Sie die Funktion aktiviert haben, sollten Sie Ihre [Bildschirmlayouts](pos-screen-layouts.md) in POS aktualisieren, um einige der geänderten Funktionen zu nutzen.

Mit der Konfiguration der Schaltfläche **Auftrag zurückrufen** können Organisationen den Vorgang mit einer vordefinierten Anzeige bereitstellen.

![Konfiguration des Schaltflächenrasters.](media/recallorderbuttongrid.png)

Die Anzeigeoptionen sind wie folgt:
- **Keine** – Diese Option stellt den Vorgang ohne spezifische Anzeige bereit. Wenn ein Benutzer den Vorgang mit dieser Konfiguration öffnet, wird er aufgefordert, Aufträge zu suchen und zu finden oder aus einem vordefinierten Auftragsfilter auszuwählen.
- **Zu erfüllende Aufträge** – Wenn ein Benutzer den Vorgang startet, wird automatisch eine Abfrage ausgeführt, um eine Liste der Aufträge zu durchsuchen und anzuzeigen, die vom aktuellen Shop des Benutzers ausgeführt werden sollen. Diese Aufträge sind für die Abholung im Store oder den Versand konfiguriert, und die Zeilen dieser Aufträge wurden noch nicht kommissioniert oder verpackt.
- **Aufträge zur Abholung** – Wenn ein Benutzer den Vorgang startet, wird automatisch eine Abfrage ausgeführt, um eine Liste der Aufträge zu durchsuchen und anzuzeigen, die für die Abholung im aktuellen Store des Benutzers konfiguriert sind.
- **Aufträge zum Versand** – Wenn ein Benutzer den Vorgang startet, wird automatisch eine Abfrage ausgeführt, um eine Liste der Aufträge zu durchsuchen und anzuzeigen, die für den Versand vom aktuellen Store des Benutzers konfiguriert sind.

Beim Starten des Vorgangs **Auftrag zurückrufen** in POS, wenn das Display als **Keine** konfiguriert ist, kann ein Benutzer Aufträge auf eine der folgenden Arten suchen und abrufen.
- Auftrags-Barcodes scannen. Dadurch werden die Felder für Auftragsnummer, Kanalreferenz und Beleg-ID nach Übereinstimmungen durchsucht.
- Wählen Sie das Symbol **Aufträge durchsuchen** oder **Suchen und Filtern** in der AppBar aus, um mithilfe des Filtermechanismus Aufträge zu finden, die die Filterkriterien erfüllen.
- Wählen Sie aus einem vordefinierten Filter aus dem Dropdown-Menü **Aufträge anzeigen** (zu erfüllende Aufträge, Aufträge zur Abholung oder Aufträge zum Versand).

![RecallOrderMainMenu.](media/recallordermain.png)

Nachdem die Suchkriterien angewendet wurden, zeigt die Anwendung eine Liste der übereinstimmenden Kundenaufträge an. Es ist wichtig zu beachten, dass bei Verwendung der Such-/Filteroptionen die abgerufenen Aufträge keine Aufträge sein müssen, die mit dem aktuellen Shop des Benutzers verknüpft sind. Bei diesem Suchvorgang wird jeder Debitorauftrag abgerufen und angezeigt, der den Suchkriterien entspricht, auch wenn der Auftrag so erstellt oder festgelegt wurde, dass er von einem anderen Shop/Kanal oder Lagerort erfüllt wird.

![RecallOrderDetail.](media/orderrecalldetail.png)

Ein Benutzer kann einen Auftrag in der Liste auswählen, um zusätzliche Details anzuzeigen. Das Informationsfeld auf der rechten Seite des Bildschirms zeigt Einzelheiten zum ausgewählten Auftrag an, einschließlich Details zur Auftragsposition, Lieferdetails und Erfüllungsdetails.

In der AppBar kann ein Benutzer einen Vorgang auswählen. Abhängig vom Auftragsstatus sind bestimmte Vorgänge möglicherweise nicht aktiviert.

- **Rückgabe** – Leitet den Prozess zum Erstellen einer Rückgabe für eines der in Rechnung gestellten Produkte auf dem ausgewählten Debitorenauftrag ein.

- **Stornieren** – Stellt eine vollständige Stornierung des ausgewählten Kundenauftrags aus. Diese Option ist nicht für Aufträge verfügbar, die über einen Callcenterkanal initiiert wurden, und kann nicht zum teilweisen Stornieren eines Auftrags verwendet werden.

- **Erfüllen** – Überträgt den Benutzer auf die Seite zur Auftragserfüllung, die für die ausgewählte Bestellung vorgefiltert wird. Es werden nur Auftragspositionen angezeigt, die vom Store des Benutzers für den ausgewählten Auftrag zur Erfüllung geöffnet sind.

- **Bearbeiten** – Ermöglicht Benutzern das Vornehmen von Änderungen am ausgewählten Kundenauftrag. Aufträge können nur in [bestimmten Szenarien](customer-orders-overview.md#edit-an-existing-customer-order) bearbeitet werden.

- **Abholen** – Diese Option ist verfügbar, wenn auf dem Auftrag eine oder mehrere Positionen zur Abholung im aktuellen Geschäft des Benutzers vorgesehen sind. Dieser Vorgang startet den Abholungs-Flow, mit dem der Benutzer die abzuholenden Produkte auswählen kann, und erstellt die Warenabholungstransaktion.

## <a name="add-notifications-to-the-recall-order-operation"></a>Dem Auftragsrückrufvorgang Benachrichtigungen hinzufügen

In Version 10.0.18 und höher können Sie POS-Benachrichtigungen und Live-Kachel-Warnungen für den Vorgang **Auftragsrückruf** konfigurieren, falls gewünscht. Weitere Informationen finden Sie unter [Auftragsbenachrichtigungen in Point of Sale (POS) anzeigen](notifications-pos.md).  

> [!NOTE]
> Um die Funktion zur Auftragssuche zu aktivieren, stellen Sie sicher, dass der Schlüssel **Angebote** unter **Lizenzkonfiguration** > **Konfigurationsschlüssel** aktiviert ist.
>
> ![Die Konfiguration des Angebotslizenzschlüssels muss aktiviert sein](./media/Quotations_License_Key_Configuration.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
