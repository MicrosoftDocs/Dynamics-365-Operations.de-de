---
title: "Hier können Sie Produkte, die produziert werden oder verschafft werden können"
description: "Produkte können auf verschiedene Weise Ursprungs sein - sie können produziert werden () oder produziert wurde verschafft werden (erworben wurden). In diesem Artikel werden einige typische Punkte beschrieben, die Sie berücksichtigen müssen, wenn Sie Produkte zur Inanspruchnahme mehrerer Quellen konfigurieren."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 5360c7b1475763b8e33205bff560393e9ee51882
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-products-that-can-be-produced-or-procured"></a>Hier können Sie Produkte, die produziert werden oder verschafft werden können

Produkte können auf verschiedene Weise Ursprungs sein - sie können produziert werden () oder produziert wurde verschafft werden (erworben wurden). In diesem Artikel werden einige typische Punkte beschrieben, die Sie berücksichtigen müssen, wenn Sie Produkte zur Inanspruchnahme mehrerer Quellen konfigurieren. 

Die Inanspruchnahme mehrerer Quellen wird in der Regel für einen gekauften Artikel verwendet, die gelegentlich produziert werden, oder wenn ein Artikel, der in erster Linie ein produzierter Artikel war, geändert wird, sodass dieser nun in erster Linie ein eingekaufter Artikel ist. Der Artikel wird zunächst als produzierter Artikel festgelegt, um die Stückliste und die Arbeitsplaninformationen zu definieren und die Produktionsaufträge für den Artikel zu unterstützen. Der Produktionstyp soll auf **Stückliste** festgelegt werden (oder, für die Fertigungsverarbeitung**Formel** oder **Kuppelprodukt**).

Wenn Sie Standardkosten verwenden, kann der Artikelkostendatensatz für den produzierten Artikel verwendet werden. Der Artikelkostendatensatz entspricht möglicherweise nicht den Standardkosten, die für Kaufzwecke vorgesehen sind. Die gewünschten Standardkosten müssen in diesem Fall manuell eingegeben und für den Artikelkostendatensatz aktiviert werden. Für die Kostenberechnung, sollten Sie eine spezielle Stückliste und einen Arbeitsplan verwenden, die die Zubehörmischung des Produkts im Laufe eines Finanzzeitraums darstellen, um die Abweichungen im Zeitverlauf zu minimieren. Außerdem kann ein produzierter Artikel, der sich an einem bestimmten Standort befindet, an einen anderen Standort umgelagert werden. Daher müssen die Kosten des Artikels für den Standort, an den der Artikel umgelagert wird, manuell eingegeben und aktiviert werden. Bei Verwendung des produzierten Artikels als Komponente in höher eingestuften Produkten sollten die Kosten der Komponente als gekaufte Artikel behandelt werden. Diese Richtlinie ist gültig – egal, ob die Kosten der Komponente berechnet oder manuell eingegeben wurden. Dies bedeutet, dass bei einer Stücklistenkalkulation die Kosten des Artikels als gekaufte Komponente behandelt werden sollten, anstatt die Stückliste und die Arbeitsplaninformationen des Artikel zur Kostenberechnung zu verwenden. Diese Berechnung kann durch Auswählen der Kennzeichnung **Stücklistenauflösung beenden** verhindert werden, die in die dem Artikel zugeordneten Herstellkostenkalkulationsgruppe eingebettet ist. Um die Auflösung für die Berechnungen der Produktprogrammplanung zu verhindern, legen Sie mittels den Stücklistenauflösungszeitraum in der Artikeldeckung oder der Abdeckungsgruppe auf 0 Tage fest. Der Artikel wird in der Berechnung der Produktprogrammplanung als gekaufter Artikel behandelt (wie beispielsweise die Empfehlung von Bestellvorschlägen). Weitere Berechnungen für die Stücklisten- und Arbeitsplaninformationen werden nicht durchgeführt.




