---
title: Infocodes
description: "Dieser Artikel enthält einen Überblick über Infocodes, Infocodegruppen und wie sie verwendet werden."
author: mugunthanm
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5790f54a531336b30ee140ebf8b9c782d8b347f7
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="info-codes"></a>Infocodes

[!include[banner](includes/banner.md)]


Dieser Artikel enthält einen Überblick über Infocodes, Infocodegruppen und wie sie verwendet werden.

Infocodes bieten eine Methode, um Daten an einem Point-of-Sale (POS) Register zu erfassen. Mithilfe von Infocodes können Sie das Kassenpersonal auffordern, Informationen zu den verschiedenen Aktionen am POS, wie Artikelverkauf, Artikelrücklieferungen oder Auswählen von Debitoren einzugeben. Kassierer können Eingabe aus einer Liste auswählen oder als Code, Nummer, Datum oder Text eingeben. Infocodes können vordefinierten Shopaktionen, Einzelhandelsartikeln, Zahlungsmethoden, Debitoren oder bestimmten Point-of-Sale-Aktivitäten zugewiesen werden. Folgende Aufgaben können mit Infocodes ausgeführt werden:
-   Erfassen zusätzlicher Informationen während der Buchung, z. B. eine Flugnummer oder den Grund für eine Retoure
-   Anzeigen einer Bedienerführung, durch die der Kassierer am Register aufgefordert wird, Preise für bestimmte Produkte in einer Liste auszuwählen
-   Verknüpfen eines Untercodes mit einem Infocode, durch den der Kassierer beim Ausführen einer bestimmten Aktivität zur Eingabe von Informationen aufgefordert wird Wenn beispielsweise ein Debitor ein Produkt zurücksendet, können Sie den Kassierer auffordern, warum das Produkt zurückgegeben wird. Anschließend können Sie Untercodes verwenden, um eine Ursachenliste anzuzeigen, aus der der Kassierer auswählen kann.
-   Ein Produkt als regulärer Verkauf, Verkauf mit Preisnachlass oder kostenloses Produkt verkaufen.
-   Den Kassierer auffordern, einen Wert einzugeben oder aus einer Liste von Untercodes auszuwählen, wenn er die Registerkassenlade öffnet, ohne einen Verkaufsarbeitsgang auszuführen.

## <a name="info-codes-group-in-retail-and-commerce"></a>Infocodegruppe im Einzelhandel und im Handel
In Dynamics 365 for Operations - Retail Infocodes können Sie Gruppen erstellen. Infocodegruppen fügen Flexibilität hinzu, indem Sie Ihnen ermöglichen, weniger Infocodes zu definieren und sie dann auf vielseitigere Arten zu verwenden. Infocodes können wie im Folgenden beschrieben verwendet werden:
-   Definieren Sie weniger Infocodes und verwenden Sie diese leicht erneut. Infocodes, die in den Infocodegruppen enthalten sind, besitzen keine vordefinierten Abhängigkeiten von anderen Infocodes. Sie können den gleichen Infocode in mehreren Infocodegruppen einfügen und dann Priorisierung verwenden, um die gleichen Infocodes in der Reihenfolge darzustellen, der in einem bestimmten Fall sinnvoll ist.
-   Verknüpfen Sie Infocodes so mit anderen Infocodes oder Infocodegruppen, um Informationen über ein Produkt oder eine Transaktion zu sammeln, ohne einen separaten Infocode oder verknüpften Infocode für jedes Szenario zu definieren.

## <a name="info-code-examples"></a>Infocodebeispiele
**Beispiel 1: Wiederverwendung von Infocodes** Sie können Linkinformationenscodes so verknüpfen, dass, wenn ein Infocode ausgelöst wurde, ein anderer Infocode direkt nach ihm ausgelöst wird. Wenn Sie also beispielsweise bestimmte Produkte verkaufen, möchten Sie den Kassierer auffordern, den Debitor zu fragen, ob er Batterien und eine Produktgarantie kaufen möchte. Für andere Produkte, möchten Sie den Kassierer auffordern, den Debitor zu fragen, ob er Batterien kaufen möchten, und auch dessen Postleitzahl erfragen. Wenn Sie verknüpfte Infocodes für diese Szenarien erstellen, müssen Sie jede Variation des Infocodes einrichten, damit der Kassierer aufgefordert wird, die richtigen Informationen anzufordern. Wenn Sie jedoch Infocodegruppen verwenden, können allgemeine Infocodes, wie Fragen nach Batterien, einmal eingerichtet werden und in mehreren Infocodegruppen dann wieder verwendet werden. Sie können Priorisierung in den Infocodegruppen auch verwenden, um den Auftrag zu identifizieren, in dem die Aufforderungen angezeigt werden.


**Beispiel 2: Verknüpfen von Infocodes zu Infocodegruppen** Wenn Sie bestimmte Produkte verkaufen, beispielsweise mobile Geräte, möchten Sie immer einen Satz spezifische Informationen, beispielsweise Telefonnummer, Mobilgerätekennung (MEID) und Seriennummer, erfassen. Jedoch möchten Sie auch unterschiedliche Informationen für ein Tablet gegenüber einem Mobiltelefon erfassen. Sie können eine Infocodegruppe einrichten, die Aufforderungen für die Telefonnummer, MEID und die Seriennummer umfasst und dann die Infocodegruppe mit einem einzelnen Infocode verknüpfen. Wenn der produktspezifische Infocode ausgelöst wurde, kann als Nächstes die Infocodegruppe aktiviert werden, um es Ihnen zu ermöglichen, die allgemeinen Daten zu sammeln, ohne mehrere Sätze von verknüpften Infocodes für jedes Gerät zu definieren.

 



