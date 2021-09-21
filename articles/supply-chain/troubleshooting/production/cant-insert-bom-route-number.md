---
title: Aktive Versionen der Stücklisten- und Arbeitsplannummern können nicht eingegeben werden
description: Wenn für ein ausgewähltes Produkt Standardstandort und -lagerort bereits definiert sind, werden Sie nicht aufgefordert, die aktiven Versionen der Stücklisten- und Arbeitsplannummern einzugeben.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 241618d70f01c85df946a48493f5d84e0964218e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476397"
---
# <a name="cant-insert-bill-of-material-and-route-when-creating-a-new-production-order"></a>Stückliste und Arbeitsplan können beim Erstellen eines neuen Produktionsauftrags nicht eingefügt werden.

## <a name="symptoms"></a>Symptome

Wenn Sie einen neuen Produktionsauftrag erstellen, werden nach Eingabe der Elementnummer die Felder **Standort** und **Lagerort** automatisch auf den Standard-Standort und den Standard-Lagerort festgelegt, die auf der Seite **Standard-Auftragseinstellungen** für den Artikel der fertigen Ware definiert sind. Darüber hinaus werden die aktive Stücklistennummer und die aktive Arbeitsplannummer automatisch eingegeben, sodass nicht die folgende Meldung angezeigt wird, die Sie zur Eingabe dieser Werte auffordert:

> Aktive Version für Stückliste und Arbeitsplan einfügen?

## <a name="resolution"></a>Lösung

Sie werden nicht aufgefordert, die Stücklisten- und Arbeitsplannummern einzugeben, wenn Sie ein Produkt auswählen, für das auf der Seite **Standardauftragseinstellungen** bereits ein Standort und ein Lagerort festgelegt sind. Sie werden nur aufgefordert, wenn diese Werte nicht für das ausgewählte Produkt definiert sind.
