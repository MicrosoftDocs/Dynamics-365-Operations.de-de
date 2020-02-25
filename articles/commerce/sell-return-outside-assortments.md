---
title: Verkaufen und zurückgeben von Produkten, die Teil des Sortiments eines Shops sind
description: Mit Dynamics 365 Commerce können Sie Produkte außerhalb eines Sortiments verkaufen und zurückgeben.
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 86c6ecf9ef67ca3ac4ed3c44d930acaa965112b6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022674"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a>Verkaufen und zurückgeben von Produkten, die Teil des Sortiments eines Shops sind

[!include [banner](includes/banner.md)]

Ein allgemeines Szenario für einen beliebigen Einzelhändler ist es, Produkte an seine Kunden zu verkaufen oder Rücklieferungen von den Debitoren zu akzeptieren, wenn sie keine spezifische Produkte in ihrer Filiale führen (das heißt, die Produkte werden nicht nach Shop sortiert).

Nachfolgend sind einige typische Szenarios:

+ Ein Einzelhändler führt nicht alle zugehörigen Produkte in einem bestimmten Shop. Die verbleibenden Produkte werden am Lagerort gelagert. Die Der Mitarbeiter der Filiale kann dem Kunden beim Suchen nach Produkten am Lagerort helfen, sie dem Einkaufskorb hinzufügen, das Auschecken und die Wahl der Versandart vornehmen, wie der Versand an eine Adresse vom Lagerort aus oder dafür sorgen, dass der Kunde das Produkt in der aktuellen Filiale oder einer anderen Filiale abholen kann.
+ Ein Einzelhändler führt nicht bestimmte Produkte im Shop oder hat diese nicht an Lager, aber das Produkt ist in einer anderen Filiale verfügbar. Der Mitarbeiter der Filiale kann dem Kunden helfen, das Produkt in einer anderen Filiale zu suchen, diese dem Einkaufskorb hinzuzufügen, sie Auszuchecken und die Versandmethode auszuwählen.
+ Ein Einzelhändler verfügt über eine Vielzahl von Shops in einem bestimmten Ort oder einem Postleitzahlkreis und möchte die Debitoren nicht dazu zwingen, die Produkte demselben Shop zurückzusenden, in dem sie bestellt wurden. Stattdessen können Debitoren Produkten an einem beliebigen Shop zurücksenden.

Diese allgemeine Szenarien sind in Commerce für Einzelhändler verfügbar. Mit Commerce können Sie:

+ Produkte in anderen Filialen suchen.
+ Alle vorhandenen Produkte suchen.
+ Cash- und Carry-Transaktionen oder Kundenaufträge erstellen.
+ Lieferoptionen für Kundenaufträge auswählen.
+ Produkte im aktuellen Shops oder in einer anderen Filiale abholen.
+ Eine Bestellung in der aktuellen Filiale oder in einer anderen Filiale stornieren.
+ Einen Auftrag mit oder ohne Beleg in der aktuellen Filiale oder in einer anderen Filiale zurückgeben.
