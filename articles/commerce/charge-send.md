---
title: Aufträge aus einer anderen Filiale mithilfe der Funktion „Belastung übermitteln“ versenden
description: In diesem Artikel wird beschrieben die Funktion Belastung senden.
author: ashishmsft
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: d73a21bfe9a284bd6e222e73bb0250648912b230
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863512"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Aufträge aus einer anderen Filiale mithilfe der Funktion „Belastung übermitteln“ versenden

[!include [banner](includes/banner.md)]

Bei der „Belastung übermitteln”-Funktion in Commerce können Debitorenaufträge in einem Shop platziert und aus einem anderen Shop versendet werden.

Debitorenaufträge im Verkaufsstellen (POS)-Client unterstützen mehrere Erfüllungsoptionen. Einige Beispiele von Erfüllungsoptionen enthalten:

- Entnahme vom gleichen Shop an einem anderen Datum.
- Entnahme von einem anderen Shop an demselben oder an einem anderen Datum.
- Versand vom Standardversandlagerort, der dem Shop zugeordnet ist und Lieferung an einem bestimmtes Datum.

Die Belastung senden Funktion verwendet die folgenden POS-Vorgänge: Versand aller Produkte und die Lieferung bestimmter Produkte. Dies ermöglicht dem Ladenangestellten, den "Versand von"-Speicherort auszuwählen, von dem der Auftrag oder die Auftragsposition erfüllt werden können. Standardmäßig ist der "Versand von"-Lagerplatz der Versandlagerort, der dem Shop zugeordnet ist. Allerdings kann der Ladenangestellte diesen Ort ggf. ändern und einen beliebigen Shop wählen, der in der Filialsuchegruppe definiert wird, die dem Shop zugewiesen ist.

Die Möglichkeit, Versand zu"-Adressen auszuwählen bleibt unverändert.

Die Versandmethoden, die verwendet werden können, um die Auftragsposition zu decken, basieren auf der Konfiguration mit gültigen Lieferarten für Produkte und Adressen. Da die Regeln, die von Lieferarten gültig sind, nur im Zentralverwaltung (HQ) hat, der POS-Kunde ermöglicht einem Echtzeitanruf die gültigen Lieferarten für eine Schiffsposition abrufen verwaltet werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]