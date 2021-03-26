---
title: Artikel über mehrere Debitorenaufträge und Rechnungen zurückgeben
description: In diesem Thema werden die Funktionen erläutert, um Rücklieferungen über mehrere Debitorenaufträgen und Rechnungen in Dynamics 365 Commerce zu ermöglichen.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4d1be6606793d498d01be91de6205e3a45c6dfdf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251258"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Artikel über mehrere Debitorenaufträge und Rechnungen zurückgeben

[!include [banner](includes/banner.md)]


Dieser Artikel beschreibt zwei Funktionen, mit denen die Rückgabe von Debitorenaufträgen über mehrere Rechnungen optimiert wird. 

## <a name="enable-refunds-over-multiple-captures"></a>Rückerstattungen über mehrere Erfassungen aktivieren

Diese Funktion ermöglicht mehrere verknüpfte Rückerstattungen für denselben Debitorenauftrag. 

1. Wechseln Sie zum Arbeitsbereich **Funktionsverwaltung** und suchen Sie nach **Rückerstattungen über mehrere Erfassungen aktivieren**.
2. Wählen Sie **Rückerstattungen über mehrere Erfassungen aktivieren** und klicken Sie dann auf **Aktivieren**. 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Richtige Steuerberechnung für Retouren mit Teilmengen aktivieren

Diese Funktion stellt sicher, dass bei der Retoure eines Auftrags über mehrere Rechnungen die Steuern letztendlich dem ursprünglich berechneten Steuerbetrag entsprechen. 

1. Wechseln Sie zum Arbeitsbereich **Funktionsverwaltung** und suchen Sie nach **Richtige Steuerberechnung für Retouren mit Teilmengen aktivieren**.
2. Wählen Sie **Richtige Steuerberechnung für Retouren mit Teilmengen aktivieren** aus und klicken Sie dann auf **Aktivieren**. 


## <a name="process-returns"></a>Rücklieferungen verarbeiten

Nachdem diese Funktionen aktiviert und die Änderungen mit den Shops synchronisiert wurden, kann der Kassierer im Shop mehrere Aufträge für einen Debitor zur Rücklieferung auswählen.

Wenn die Aufträge ausgewählt werden, wird eine Liste aller retournierbaren Produkte für alle Rechnungen des Auftrags angezeigt. Der Kassierer kann dann die Produkte auswählen, die retourniert werden sollen. Es wird ein einzelner Rücklieferungsauftrag für alle ausgewählten Produkte erstellt.

Wenn der Auftrag vollständig zurückgesandt wird, entspricht der an den Kunden zurückgegebene Steuerbetrag dem ursprünglich berechneten Steuerbetrag.



[!INCLUDE[footer-include](../includes/footer-banner.md)]