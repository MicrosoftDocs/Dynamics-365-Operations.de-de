---
title: Lagerplatz für Produktions-Warenabgang
description: In diesem Thema wird die Hierarchie beschrieben, die verwendet wird, um den Lagerplatz für den Produktions-Warenabgang zu identifizieren.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 48b68c36718fa42b7f80e3ffe1f54b7efbbee8bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814631"
---
# <a name="production-output-location"></a>Lagerplatz für Produktions-Warenabgang

[!include [banner](../includes/banner.md)]

In diesem Thema wird die Hierarchie beschrieben, die verwendet wird, um den Lagerplatz für den Produktions-Warenabgang zu identifizieren.

Der Lagerplatz für den Produktions-Warenabgang ist der Lagerplatz, an dem die fertigen Waren zuerst gelagert werden, nachdem sie hergestellt wurden. Normalerweise ist dieser Lagerplatz nahe dem Produktionsprozess gelegen, durch den die fertigen Produkte hergestellt werden. Der Lagerplatz für den Produktions-Warenabgang wird als Zwischenlager für das Material verwendet, bevor es in den Lieferungsbereich verschoben wird, einen Lagerplatz, einen Lagerplatz für den Wareneingang für den nachfolgenden Produktionsprozess und so weiter. 

Ein standardmäßiger Lagerplatz für den Produktions-Warenabgang wird festgelegt, wenn die fertigen Waren in einem Produktionsauftrag oder einem Chargenauftrag gemeldet werden. Die folgende Hierarchie wird verwendet, um diesen Abgangslagerplatz zu identifizieren:

1. Verwenden Sie den Abgangslagerplatz, der im Produktionsauftrag oder dem Chargenauftragskopf definiert ist.
2. Wenn sich dort kein Lagerplatz befindet, verwenden Sie den Abgangslagerplatz, der in der Ressource definiert ist, die vom letzten Vorgang verwendet wird, der im Produktionsarbeitsplan definiert ist.
3. Wenn sich dort kein Lagerplatz befindet, verwenden Sie den Abgangslagerplatz, der in der Ressourcengruppe definiert ist, die von der Ressource für den letzten Vorgang verwendet wird, der im Produktionsarbeitsplan definiert ist.
4. Wenn sich dort kein Lagerplatz befindet, verwenden Sie den Abgangslagerplatz, der für den Lagerort definiert ist, der für den Produktionsauftrag definiert ist.

Ein standardmäßiger Lagerplatz für den Produktions-Warenabgang wird nur für Produkte festgelegt, die mithilfe erweiterter Lagerortprozesse eingerichtet werden. Wenn dieser Artikeltyp als fertig gemeldet wird, wird Lagerortarbeit des Typs **Eingelagerte Fertigerzeugnisse** oder **Einlagerung von Co-Produkt und Nebenprodukt** erstellt. Dieser Arbeitstyp verwendet den Lagerplatz für den Produktions-Warenabgang als Entnahmeort. Der Einlagerungslagerplatz wird durch Lagerplatzrichtlinien festgelegt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]