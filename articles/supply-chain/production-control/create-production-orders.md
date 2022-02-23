---
title: Produktionsauftragslebenszyklus – Übersicht
description: Durch Erstellen eines Produktionsauftrags wird für einen Artikel eine Fertigungsanforderung erstellt. Im Produktionsauftrag ist angegeben, was und wie viel produziert werden und wann die Produktion abgeschlossen sein soll. Sie enthält auch Informationen darüber, welche Materialien genommen werden müssen und welchem Prozess gefolgt werden muss, um den Artikel zu produzieren,
author: johanhoffmann
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80031737ab0d0c4ab1e4dbd5646ad91f1a010cd5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428848"
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




