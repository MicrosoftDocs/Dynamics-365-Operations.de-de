---
title: Buchungskonten für Anlagenveräußerung
description: Dieser Artikel beschreibt, wie Buchungskonten im Hauptbuch für den Abgang von Anlagen eingerichtet werden.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c82cb8b82f2cc8424675f76c68613a2b5aa76745
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675517"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>Buchungskonten für Anlagenveräußerung

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Buchungskonten im Hauptbuch eingerichtet werden, wenn Sie einen Abgang vbon Anlagen duchführen.

Um Hauptbuch-Buchungskonten einzurichten, die bei der Veräußerung eines Vermögenswerts verwendet werden sollen, wählen Sie **Abgang – Verkauf** und **Abgang – Ausschuss** in dem **Sachkonten**-Inforregister auf der **Buchungsprofile für Anlagen**-Seite.

Für beide Buchungsarten (Abgang einer Anlage durch Verkauf oder Ausschuss) wird der Abgangswert der Anlage dem Sachkonto gutgeschrieben. Das Soll wird in einem Gegenkonto gebucht, das (beispielsweise) ein Bankkonto sein kann. Bei Veräußerung einer Anlage an einen Debitor wird anstelle des Gegenkontos das Debitorenkonto verwendet. Weitere Informationen finden Sie unter [Abgang einer Anlage als Ausschuss](dispose-of-a-fixed-asset-as-scrap.md).

Klicken Sie auf **Abgang** und anschließend auf **Verkauf** oder **Ausschuss**, und richten Sie dann detaillierte Konten ein, um eine Rückbuchung des Nettobuchwerts der Anlage auszuführen. Sie können auch Informationen in die Felder **Buchungswert** und **Verkaufswert** auf der Seite **Abgangsparameter** eingeben. 

Durch die Abgangsbuchung für eine Anlage in einem Low-Value-Pool verringert sich der Nettobuchwert des Low-Value-Pools lediglich um den Abgangsbetrag. Übersteigt allerdings der Verkaufswert einer Anlage den Nettobuchwert des Low-Value-Pools, verringert sich der Nettobuchwert auf Null.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
