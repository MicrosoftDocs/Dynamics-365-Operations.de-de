---
title: Amortisierung konstanter Kosten für einen produzierten Artikel
description: Die konstanten Kosten eines produzierten Artikels beinhalten die Arbeitsgangrüstzeiten sowie die Komponenten mit einer konstanten Menge oder einem konstanten Schrottwert.
author: JennySong-SH
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: d466395859e19874183691e697c8aca3a774d359
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675402"
---
# <a name="amortize-constant-costs-for-a-manufactured-item"></a>Amortisierung konstanter Kosten für einen produzierten Artikel

[!include [banner](../includes/banner.md)]

Die konstanten Kosten eines produzierten Artikels beinhalten die Arbeitsgangrüstzeiten sowie die Komponenten mit einer konstanten Menge oder einem konstanten Schrottwert. 

Das Konzept der Nachkalkulationslosgröße dient zum Amortisieren dieser konstanten Kosten in den berechneten Kosten eines produzierten Artikels. Dieses Konzept besitzt mehrere Synonyme, von denen eines "Abrechnungslosgröße" lautet. Selbiges gilt auch für das Konzept der Amortisierung konstanter Kosten, das beispielsweise auch als proportionale konstante Kosten bezeichnet wird.

Die Menge einer Nachkalkulationslosgröße für einen produzierten Artikel fließt in die Herstellkostenkalkulation ein. Die Menge ist von der Initiierung und Ausführung der Herstellkostenkalkulation abhängig. Dies wird im Folgenden veranschaulicht:

-   Standardberechnungsmenge in der Herstellkostenkalkulation eines Artikels − Die Standardauftragsmenge des Artikels (für das Lager) fungiert als Standardwert für dessen Nachkalkulationslosgröße, bei dem Standardwert handelt es sich jedoch möglicherweise um eine größere Menge, die ein Vielfaches der Auftragsmenge für den Artikel darstellt. Die Standard-Auftragsmenge sowie das Vielfache werden in den Standardauftragseinstellungen oder in den standortspezifischen Auftragseinstellungen definiert.
-   Angegebene Berechnungsmenge in der Herstellkostenkalkulation eines Artikels − Die angegebene Berechnungsmenge fungiert als Nachkalkulationslosgröße für den Artikel. Als Berechnungsmenge wird zunächst die Standardauftragsmenge des Artikels verwendet, doch dieser Standardwert kann manuell außer Kraft gesetzt werden. Die angegebene Berechnungsmenge stellt die Nachkalkulationslosgröße für den angegebenen Artikel und für hergestellte Komponenten mit dem Stücklistenpositionstyp "Produktion" dar. Dies beruht auf der Annahme, dass die Komponente in der exakten Menge produziert wird. Die Nachkalkulationslosgröße für andere produzierte Komponenten mit dem Stücklistenpositionstyp "Artikel" gibt deren jeweilige Standardauftragsmenge wieder.
-   Angegebene Berechnungsmenge vom Typ "Auf Auftrag fertigen" in der Herstellkostenkalkulation eines Artikels − Die angegebene Berechnungsmenge fungiert als Nachkalkulationslosgröße für den Artikel und dessen produzierte Komponenten, wenn in einer Herstellkostenkalkulation der Stücklistenauflösungsmodus "Auf Auftrag fertigen" verwendet wird. Es wird angenommen, dass die produzierten Komponenten – ebenso wie beim Stücklistenpositionstyp "Produktion" – in der exakten Menge produziert werden.
-   Angegebene Berechnungsmenge in einer auftragsspezifischen Herstellkostenkalkulation − Eine auftragsspezifische Herstellkostenkalkulation kann für den Positionsartikel eines Auftrags, eines Verkaufsangebots oder eines Serviceauftrags ausgeführt werden. Für die angegebene Berechnungsmenge wird standardmäßig auf die Menge des ursprünglichen Positionsartikels verwendet, diese Standardmenge kann jedoch außer Kraft gesetzt werden. Sie können wählen, ob für die auftragsspezifische Herstellkostenkalkulation der Stücklistenauflösungsmodus "Auf Auftrag fertigen" oder der Stücklistenauflösungsmodus "Mehrere Ebenen" verwendet werden soll.

Der berechnete Betrag der amortisierten konstanten Kosten eines produzierten Artikels wird als Belastungen bezeichnet.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]