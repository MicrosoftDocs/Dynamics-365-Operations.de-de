---
title: "Buchungskonten für die Anlagenveräußerung"
description: "Dieser Artikel beschreibt, wie Buchungskonten im Hauptbuch für den Abgang von Anlagen eingerichtet werden."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0540ba30cb26abe274075deea80ca1e9cfc686f9
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="fixed-asset-disposal-posting-accounts"></a>Buchungskonten für die Anlagenveräußerung

[!include[banner](../includes/banner.md)]


Dieser Artikel beschreibt, wie Buchungskonten im Hauptbuch für den Abgang von Anlagen eingerichtet werden.

Wählen Sie auf der Seite "Anlagenbuchungsprofile" im Inforegister "Sachkonten" die Optionen "Abgang – Verkauf" und "Abgang – Ausschuss" aus, um Buchungen im Sachkonto einzurichten.

Für beide Buchungsarten wird der Abgangswert der Anlage dem Sachkonto gutgeschrieben. Das Soll wird in einem Gegenkonto gebucht, das beispielsweise ein Bankkonto sein kann. Bei Veräußerung einer Anlage an einen Debitor wird anstelle des Gegenkontos das Debitorenkonto verwendet.

Klicken Sie auf "Abgang" und anschließend auf "Verkauf" oder "Ausschuss", und richten Sie dann detaillierte Konten ein, um eine Rückbuchung des Nettobuchwerts der Anlage auszuführen. Sie können auch Informationen in die Felder "Buchungswert" und "Verkaufswert" auf der Seite "Abgangsparameter" eingeben. 

Durch die Abgangsbuchung für eine Anlage in einem Low-Value-Pool verringert sich der Nettobuchwert des Low-Value-Pools lediglich um den Abgangsbetrag. Übersteigt allerdings der Verkaufswert einer Anlage den Nettobuchwert des Low-Value-Pools, verringert sich der Nettobuchwert auf Null.






