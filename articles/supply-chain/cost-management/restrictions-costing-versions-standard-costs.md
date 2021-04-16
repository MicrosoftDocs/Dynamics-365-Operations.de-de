---
title: Einschränkungen für eine Nachkalkulationsversion für Standardkosten
description: In diesem Thema werden die Einschränkungen beschrieben, die für eine Nachkalkulationsversion für Standardkosten gelten.
author: AndersGirke
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fdbe74f2f71d0fbd3c237cceb6b184747636e9a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821488"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Einschränkungen für eine Nachkalkulationsversion für Standardkosten

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Einschränkungen beschrieben, die für eine Nachkalkulationsversion für Standardkosten gelten. 

Durch die folgenden Einschränkungen wird besser gewährleistet, dass die Standardprinzipien der Nachkalkulation eingehalten werden:

-  Belastungen müssen in die Kosten eines Artikels einbezogen werden. Die Belastungen für einen produzierten Artikel stellen die amortisierten konstanten Kosten aus den Stücklisten- und Arbeitsplaninformationen dar. Die Gebühren müssen daher in den Einheitenkosten enthalten sein. Die Belastungen für einen eingekauften Artikel werden ebenfalls in die Einheitenkosten des Artikels einbezogen.

-  Die Berechnung von Standardkosten für produzierte Artikel muss auf den Kostendatensätzen in einer Nachkalkulationsversion für Standardkosten basieren. Alternative Quellen für Kostendaten können ausschließlich mit einer Nachkalkulationsversion für geplante Kosten – beispielsweise mit Einkaufspreis-Handelsvereinbarungen für eingekaufte Artikel – verwendet werden. Alternative Quellen für Kostendaten werden durch die Stücklistenberechnungsgruppe definiert.

-  Herstellkostenkalkulationen müssen unter Verwendung eines Stücklistenauflösungsmodus mit nur einer Ebene ausgeführt werden.

Die Artikelkostendaten für Standardkosten können in eine andere Nachkalkulationsversion mit Standardkosten oder geplanten Kosten kopiert werden. Die Artikelkostendaten für geplante Kosten können dagegen nicht in eine Kostenversion mit Standardkosten kopiert werden, da die weiter oben in diesem Thema aufgeführten Einschränkungen nicht für geplante Kosten gelten.

<a name="related-topics"></a>Verwandte Themen
--------

[Nachkalkulationsversionen – Übersicht](costing-versions.md)

[Aktualisieren der Standardkosten in einer Umgebung ohne Produktion](update-standard-costs-non-manufacturing-environment.md)

[Vorbereiten der Verwaltung von Standardkosten für produzierte Artikel](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]