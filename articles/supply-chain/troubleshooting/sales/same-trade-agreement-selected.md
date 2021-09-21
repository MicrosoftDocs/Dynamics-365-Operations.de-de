---
title: Dieselbe Handelsvereinbarung wurde beim Erstellen von Auftragspositionen ausgewählt
description: Wenn es für ein bestimmtes Datum mehr als eine Handelsvereinbarung gibt, wird immer die Handelsvereinbarung mit dem niedrigsten Preis ausgewählt, wenn eine Auftragszeile erstellt wird.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a586a399fb349965b972191bec1271651bec5fcb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476449"
---
# <a name="if-two-trade-agreements-exist-for-overlapping-dates-the-same-one-is-always-selected"></a>Existieren zwei Handelsvereinbarungen mit sich überschneidenden Terminen, wird immer dieselbe ausgewählt

## <a name="symptoms"></a>Symptome

Wenn zwei Handelsvereinbarungen für denselben Zeitraum oder überlappende Zeiträume definiert sind, scheint jedes Mal, wenn Sie Auftragspositionen erstellen, die diese Artikel enthalten, dieselbe Handelsvereinbarung ausgewählt zu werden.

## <a name="resolution"></a>Lösung

Wenn es für ein bestimmtes Datum mehr als eine Handelsvereinbarung gibt, wird immer die Handelsvereinbarung mit dem niedrigsten Preis ausgewählt. Laden Sie für weitere Informationen das folgende Whitepaper herunter: [Handelsvereinbarungen in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).
