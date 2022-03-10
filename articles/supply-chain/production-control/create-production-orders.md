---
title: Produktionsauftragslebenszyklus – Übersicht
description: Durch Erstellen eines Produktionsauftrags wird für einen Artikel eine Fertigungsanforderung erstellt. Im Produktionsauftrag ist angegeben, was und wie viel produziert werden und wann die Produktion abgeschlossen sein soll. Sie enthält auch Informationen darüber, welche Materialien genommen werden müssen und welchem Prozess gefolgt werden muss, um den Artikel zu produzieren,
author: johanhoffmann
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19741"
- intro-internal
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4c3632d644070f064ec70d3dd7c0d480927eafe
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982876"
---
# <a name="production-order-lifecycle-overview"></a>Produktionsauftragslebenszyklus – Übersicht

[!include [banner](../includes/banner.md)]

Durch Erstellen eines Produktionsauftrags wird für einen Artikel eine Fertigungsanforderung erstellt. Im Produktionsauftrag ist angegeben, was und wie viel produziert werden und wann die Produktion abgeschlossen sein soll. Sie enthält auch Informationen darüber, welche Materialien genommen werden müssen und welchem Prozess gefolgt werden muss, um den Artikel zu produzieren,

Ein Produktionsauftrag durchläuft Phasen des Produktionslebenszyklus. Beim Erstellen eines Auftrags erhält dieser den Status **Erstellt**. Bei Fertigstellung eines Auftrags erhält dieser den Status **Beendet**. Eine Parametereinstellung in jeder Phase ermöglicht dem Benutzer, jeden Schritt zu konfigurieren. Die Einstellung kann für einen einzelnen Benutzer oder für alle Benutzer eingerichtet werden.

Eine Produktionsstückliste und der Produktionsarbeitsplan sind die wichtigsten Entitäten des Produktionsauftrags. Sie werden basierend auf dem ausgewählten Artikel und der Menge, die produziert wird, in den Produktionsauftrag kopiert. Vor Beginn des Produktionsauftrags können die Produktionsstückliste und die Route bearbeitet werden.

Ein Produktionsauftrag kann in den folgenden Szenarien erstellt werden:

-   Erstellt durch Produktprogrammplanungslauf basierend auf Materialnachfrage.
-   Erstellt direkt aus einer Auftragsposition, oder wenn eine höhere Ebene des Produktionsauftrags erstellt und geschätzt wird (Lieferung mit Bedarfsverursachung).
-   Manuell erstellt.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]