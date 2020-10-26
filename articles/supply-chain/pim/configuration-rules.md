---
title: Variantenregeln
description: Dieser Artikel enthält allgemeine Informationen zu Variantenregeln. Variantenregeln definieren Beziehungen zwischen Artikeln in einer Stückliste (BOM) für Produkte, die die Technologie der dimensionsbasierten Konfiguration verwenden.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e70713fb25584e26f97bcb7c769da6954aa36b81
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984823"
---
# <a name="configuration-rules"></a>Variantenregeln

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält allgemeine Informationen zu Variantenregeln. Variantenregeln definieren Beziehungen zwischen Artikeln in einer Stückliste (BOM) für Produkte, die die Technologie der dimensionsbasierten Konfiguration verwenden.

Variantenregeln sind nur verfügbar, wenn Sie dimensionsbasierte Konfigurationsmodelle definieren. Variantenregeln werden dazu verwendet, bestimmte Artikelkombinationen in einer Stückliste (BOM) entweder zu erzwingen oder zu verhindern. Nachdem eine Stückliste erstellt wurde und die jeweiligen Artikel den entsprechenden Variantengruppen zugewiesen wurden, können Sie eine oder mehrere Variantenregeln definieren. Wenn zwei Artikel zusammen gehören, wird der Operator **Auswählen** verwendet, um Einbeziehung sicherzustellen. Wenn zwei Artikel sich gegenseitig ausschließen, wird der Operator **Auswahl aufheben** verwendet, um Ausschluss sicherzustellen.  

**Hinweis:** Diese Informationen gelten nur für Produktmaster, die dimensionsbasierte Konfigurationstechnologie verwenden.  

Vorhandene Varianten sind von nachfolgenden Änderungen der Variantenregeln nicht betroffen. Es ist jedoch wichtig, die Regeln vor der Definition einer neuen Variante festzulegen und diese zu prüfen, wenn Sie vermuten, dass die Regeln geändert wurden.  

**Hinweis:** Die Methode **Auswählen** bedeutet, dass die abgeleitete Variantengruppe, Artikelnummer und Variante automatisch ausgewählt wird. Die Methode **Auswahl aufheben** bedeutet, dass die abgeleitete Variantengruppe, Artikelnummer und Variante nicht ausgewählt werden kann.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Dimensionsbasierte Produktkonfigurationen – Übersicht](dimension-based-product-configuration.md)



