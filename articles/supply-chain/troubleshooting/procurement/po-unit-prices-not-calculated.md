---
title: Stückpreise auf Bestellungen werden nicht basierend auf der Stückumrechnung berechnet
description: Stückpreise auf Bestellungen werden nicht basierend auf der Stückumrechnung berechnet
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476439"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Stückpreise auf Bestellungen werden nicht basierend auf der Stückumrechnung berechnet

## <a name="symptoms"></a>Symptome

Wenn eine Einheit in einer Bestellung geändert wird, werden die Handelsvertragspreise nicht gemäß den Definitionen der Einheitenumrechnung neu berechnet.

## <a name="cause"></a>Ursache

Die Preise werden immer aus Handelsabkommen (oder anderen Preiseinstellungen im System, wie z. B. Verkaufsvereinbarungen oder Artikelpreisen) ermittelt und für eine Einheit festgelegt.

Wenn die Einheit in einer Bestellposition geändert wird, sucht das System nach einem Preis für die neue Einheit und wendet diesen Preis an. Wenn für das Gerät kein Preis gefunden wird, wendet das System keinen Preis an. Die Einheitenumrechnung kann nicht verwendet werden, um den Preis in eine andere Einheit umzurechnen. Theoretisch entspricht der Preis für eine Schachtel mit zehn Stück möglicherweise nicht dem Zehnfachen des Preises einer Schachtel.

## <a name="workaround"></a>Problemumgehung

Eine Möglichkeit, dieses Problem zu umgehen, besteht darin, sicherzustellen, dass Handelsabkommen für die Einheiten bestehen, von denen Sie erwarten, dass sie in den Bestellpositionen für den Artikel verwendet werden.
