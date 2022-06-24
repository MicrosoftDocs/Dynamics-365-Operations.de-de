---
title: Einschränkungen für eine Nachkalkulationsversion für Standardkosten
description: In diesem Artikel werden die Einschränkungen beschrieben, die für eine Nachkalkulationsversion für Standardkosten gelten.
author: JennySong-SH
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
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5c00ae8952e2c80d97d039271a6f5c63e9a72f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867984"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Einschränkungen für eine Nachkalkulationsversion für Standardkosten

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Einschränkungen beschrieben, die für eine Nachkalkulationsversion für Standardkosten gelten. 

Durch die folgenden Einschränkungen wird besser gewährleistet, dass die Standardprinzipien der Nachkalkulation eingehalten werden:

-  Belastungen müssen in die Kosten eines Artikels einbezogen werden. Die Belastungen für einen produzierten Artikel stellen die amortisierten konstanten Kosten aus den Stücklisten- und Arbeitsplaninformationen dar. Die Gebühren müssen daher in den Einheitenkosten enthalten sein. Die Belastungen für einen eingekauften Artikel werden ebenfalls in die Einheitenkosten des Artikels einbezogen.

-  Die Berechnung von Standardkosten für produzierte Artikel muss auf den Kostendatensätzen in einer Nachkalkulationsversion für Standardkosten basieren. Alternative Quellen für Kostendaten können ausschließlich mit einer Nachkalkulationsversion für geplante Kosten – beispielsweise mit Einkaufspreis-Handelsvereinbarungen für eingekaufte Artikel – verwendet werden. Alternative Quellen für Kostendaten werden durch die Stücklistenberechnungsgruppe definiert.

-  Herstellkostenkalkulationen müssen unter Verwendung eines Stücklistenauflösungsmodus mit nur einer Ebene ausgeführt werden.

Die Artikelkostendaten für Standardkosten können in eine andere Nachkalkulationsversion mit Standardkosten oder geplanten Kosten kopiert werden. Die Artikelkostendaten für geplante Kosten können dagegen nicht in eine Kostenversion mit Standardkosten kopiert werden, da die weiter oben in diesem Artikel aufgeführten Einschränkungen nicht für geplante Kosten gelten.

## <a name="related-articles"></a>Zugehörige Artikel

[Nachkalkulationsversionen – Übersicht](costing-versions.md)

[Aktualisieren der Standardkosten in einer Umgebung ohne Produktion](update-standard-costs-non-manufacturing-environment.md)

[Vorbereiten der Verwaltung von Standardkosten für produzierte Artikel](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]