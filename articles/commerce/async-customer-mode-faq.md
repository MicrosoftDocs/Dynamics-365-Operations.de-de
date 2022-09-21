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
ms.openlocfilehash: bd5741aeb3278f1d40d63bb02ca57571a907dc21
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474068"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>Häufig gestellte Fragen zum asynchronen Debitorenerstellungsmodus

[!include [banner](includes/banner.md)]

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
