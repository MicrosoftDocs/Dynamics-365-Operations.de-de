---
title: Häufig gestellte Fragen zum asynchronen Debitorenerstellungsmodus
description: Dieser Artikel enthält Antworten auf häufig gestellte Fragen zum asynchronen Debitorenerstellungsmodus in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 35c999695ed33c4fc9731a5b8dd4d679cf55fa44
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229872"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>Häufig gestellte Fragen zum asynchronen Debitorenerstellungsmodus

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dieser Artikel enthält Antworten auf häufig gestellte Fragen zum asynchronen Debitorenerstellungsmodus in Microsoft Dynamics 365 Commerce.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>Warum kann ich die Funktion „Bearbeitung von Debitoren im asynchronen Modus ermöglichen“ nicht aktivieren?

Bevor Sie die Funktion **Bearbeitung von Debitoren im asynchronen Modus ermöglichen** müssen Sie die folgenden Funktionen aktivieren:

- Leistungsverbesserungen bei Debitorenaufträgen und Debitorenbuchungen
- Erweiterte asynchrone Debitorenerstellung aktivieren
- Asynchrone Erstellung für Kundenadressen aktivieren

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>Warum sehe ich immer noch Serviceanrufe in Echtzeit an die Commerce headquarters, nachdem die Funktion „Bearbeitung von Debitoren im asynchronen Modus ermöglichen“ aktiviert wurde?

Dieses Problem tritt auf, wenn Commerce Data Exchange-Aufträge (CDX-Aufträge) nicht ausgeführt wurde, um sicherzustellen, dass der Funktionsstatus und andere Kanalmetadaten mit dem Kanal synchronisiert werden. Bevor Sie das Szenario wiederholen, stellen Sie sicher, dass die folgenden CDX-Aufträge in Commerce headquarters ausgeführt werden:

- 1110 (globale Konfiguration)
- 1010 (Debitoren)
- 1070 (Kanalkonfiguration)

Daten, die in der Commerce Scale Unit (CSU) zwischengespeichert werden, werden möglicherweise nicht sofort in Commerce headquarters widergespiegelt, nachdem die CDX-Aufträge ausgeführt wurden.

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Warum zeigt Commerce headquarters keine Debitorenerstellung oder Aktualisierungen vom Point of Sale (POS) oder E-Commerce-Kanal an?

Stellen Sie sicher, dass die folgenden Aktionen in der hier aufgeführten Reihenfolge durchgeführt wurden.

1. Führen Sie den CDX P-Auftrag in Commerce headquarters aus, um sicherzustellen, dass asynchrone Debitorendaten, die in den Tabellen **RETAILASYNCCUSTOMERV2**, **RETAILASYNCADDRESSV2**, **RETAILASYNCCUSTOMERCONTACT**, **RETAILASYNCCUSTOMERAFFILIATION** und **RETAILASYNCCUSTOMERATTRIBUTEV2** gespeichert sind, in Commerce headquarters verfügbar sind.
1. Führen Sie **Debitoren- und Kanalanforderungen synchronisieren** Stapelverarbeitungsaufträge in Commerce headquarters aus. Nach erfolgreicher Ausführung des Stapelverarbeitungsauftrags haben alle Datensätze, die aus den zuvor genannten Tabellen erfolgreich verarbeitet wurden, im Feld **OnlineOperationCompleted** den Wert **1**.
