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
ms.reviewer: kfend
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1272cdb16396d24b5495f023e7b9fe3dee341507
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871332"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>Buchungskonten für Anlagenveräußerung

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Buchungskonten im Hauptbuch eingerichtet werden, wenn Sie einen Abgang von Anlagen duchführen.

Um Hauptbuch-Buchungskonten einzurichten, die bei der Veräußerung eines Vermögenswerts verwendet werden sollen, wählen Sie **Abgang – Verkauf** und **Abgang – Ausschuss** in dem **Sachkonten**-Inforregister auf der **Buchungsprofile für Anlagen**-Seite.

Für beide Buchungsarten (Abgang einer Anlage durch Verkauf oder Ausschuss) wird der Abgangswert der Anlage dem Sachkonto gutgeschrieben. Das Soll wird in einem Gegenkonto gebucht, das (beispielsweise) ein Bankkonto sein kann. Bei Veräußerung einer Anlage an einen Debitor wird anstelle des Gegenkontos das Debitorenkonto verwendet. Weitere Informationen finden Sie unter [Abgang einer Anlage als Ausschuss](dispose-of-a-fixed-asset-as-scrap.md).

Klicken Sie auf **Abgang** und anschließend auf **Verkauf** oder **Ausschuss**, und richten Sie dann detaillierte Konten ein, um eine Rückbuchung des Nettobuchwerts der Anlage auszuführen. Sie können auch Informationen in die Felder **Buchungswert** und **Verkaufswert** auf der Seite **Abgangsparameter** eingeben. 

Durch die Abgangsbuchung für eine Anlage in einem Low-Value-Pool verringert sich der Nettobuchwert des Low-Value-Pools lediglich um den Abgangsbetrag. Übersteigt allerdings der Verkaufswert einer Anlage den Nettobuchwert des Low-Value-Pools, verringert sich der Nettobuchwert auf Null.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
