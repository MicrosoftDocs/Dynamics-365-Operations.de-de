---
title: Nachverfolgen der laufenden Durchschnittskosten pro Lagerungsdimension
description: Jedem Lagerartikel ist eine Lagerdimensionsgruppe zugewiesen. Der laufende Durchschnittseinstandspreis für einen Artikel wird deshalb auf Basis der Auswahl von Lagerungsdimensionen berechnet, die wertmäßig verfolgt werden.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8ade2981056e9e4f49726a8c01c45f77b8e151b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563088"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a>Nachverfolgen der laufenden Durchschnittskosten pro Lagerungsdimension

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Jedem Lagerartikel ist eine Lagerdimensionsgruppe zugewiesen. Der laufende Durchschnittseinstandspreis für einen Artikel wird deshalb auf Basis der Auswahl von Lagerungsdimensionen berechnet, die wertmäßig verfolgt werden.

Drei Arten von Lagerungsdimensionen sind verfügbar: Produkt, Lagerung und Nachverfolgung. Zu den Produktdimensionen zählen "Variante", "Größe" und "Farbe". Produktdimensionen werden immer wertmäßig verfolgt. Zu den Lager- und Überwachungsdimensionen zählen "Standort", "Lagerort", ""Lagerplatz", "Bestandsstatus", "Ladungsträger", "Chargennummer" und "Seriennummer". Bei Lager- und Überwachungsdimensionen können Sie entscheiden, welche Dimensionen wertmäßig verfolgt werden sollen. 

**Beispiel 1** 

Wenn die Lagerdimensionsgruppe, die dem zugeordnete ist, wertmäßig nach Lagerort verfolgt wird, werden die laufenden Durchschnittseinstandspreis für jeden Lagerort berechnet. Folgende Bestellungen wurden fakturiert:

-   Eine Bestellung der Menge "2" zu einem Einstandspreis von EUR 10,00, fakturiert für den Lagerort "GW".
-   Eine Bestellung der Menge "3" zu einem Einstandspreis von EUR 12,00, fakturiert für den Lagerort "GW".
-   Eine Bestellung der Menge "5" zu einem Einstandspreis von EUR 15,00, fakturiert für den Lagerort "MW".

Der laufende Durchschnittseinstandspreis für den Lagerort "GW" beträgt EUR 11,20, und der laufende Durchschnittseinstandspreis für den Lagerort "MW" beträgt EUR 15,00. Für den Lagerort "GW" wird eine Auftragsrechnung gebucht. Der Wert für das Lager und für den Wareneinsatz (vor dem Ausführen des Lagerabschlusses und ohne Markierung) beträgt EUR 11,20. Für den Lagerort "MW" wird ein weiterer Auftrag gebucht. Der Wert für das Lager und für den Wareneinsatz (vor dem Ausführen des Lagerabschlusses und ohne Markierung) beträgt EUR 15,00. 

**Beispiel 2** Wenn die Lagerdimensionsgruppe, die dem Artikel zugeordnet ist, wertmäßig nach Lagerort und die Rückverfolgungsangabengruppe wertmäßig nach Chargennummer verfolgt wird, wird der laufende Durchschnittseinstandspreis für jede Charge berechnet. 

**Hinweis:** Es empfiehlt sich, den Einstandspreis immer zusammen mit allen wertmäßig nachverfolgten Dimensionen zu betrachten. Folgende Bestellungen wurden fakturiert:

-   Eine Bestellung der Menge "2" zu einem Einstandspreis von EUR 10,00 wurde für den Lagerort "GW" und die Charge "AAA" fakturiert.
-   Eine Bestellung der Menge "3" zu einem Einstandspreis von EUR 12,00 wurde für den Lagerort "GW" und die Charge "AAA" fakturiert.
-   Eine Bestellung der Menge "2" zu einem Einstandspreis von EUR 15,00 wurde für den Lagerort "GW" und die Charge "BBB" fakturiert.

Der laufende Durchschnittseinstandspreis für den Lagerort "GW" und Charge "AAA" beträgt EUR 11,20, und der laufende Durchschnittseinstandspreis für den Lagerort "GW" und Charge "BBB" beträgt EUR 15,00.



