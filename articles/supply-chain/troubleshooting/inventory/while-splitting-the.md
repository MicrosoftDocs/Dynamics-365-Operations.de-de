---
title: Wenn eine Artikelgewichtsmenge aufgeteilt wird, wird anstelle der nominellen Menge die Mindestmenge verwendet
description: Wenn eine Artikelgewichtsmenge in Batches aufgeteilt wird, verwendet das Feld „Entnahmemenge“ die Mindestmenge, die für den Artikel festgelegt wurde, nicht die nominelle Menge.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026550"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>Wenn eine Artikelgewichtsmenge aufgeteilt wird, wird anstelle der nominellen Menge die Mindestmenge verwendet

KB-Nummer: 4612073

## <a name="symptoms"></a>Symptome

Wenn eine Artikelgewichtsmenge in Batches aufgeteilt wird, verwendet das Feld **Entnahmemenge** die Mindestmenge, die für den Artikel festgelegt wurde, nicht die nominelle Menge.

## <a name="resolution"></a>Lösung

Das System verhält sich wie vorgesehen. Das System verwendet für die Kommissionierung die Mindestmengeneinstellung jedes Artikels.
