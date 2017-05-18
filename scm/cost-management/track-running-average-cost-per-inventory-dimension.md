---
title: Nachverfolgen der laufenden Durchschnittskosten pro Lagerungsdimension
description: "Jedem Lagerartikel ist eine Lagerdimensionsgruppe zugewiesen. Der laufende Durchschnittseinstandspreis für einen Artikel wird deshalb auf Basis der Auswahl von Lagerungsdimensionen berechnet, die wertmäßig verfolgt werden."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d9d92f436ce2e0757ce69f0dd5e11234e30c2df8
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a>Nachverfolgen der laufenden Durchschnittskosten pro Lagerungsdimension

[!include[banner](../includes/banner.md)]


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




