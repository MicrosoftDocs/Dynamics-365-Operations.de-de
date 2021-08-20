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
ms.openlocfilehash: 424ad46281612f6a3e8cb4c90478a39f757d5416c3ce1d77ed6ff6dba7b20dcb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723454"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>Wenn eine Artikelgewichtsmenge aufgeteilt wird, wird anstelle der nominellen Menge die Mindestmenge verwendet

KB-Nummer: 4612073

## <a name="symptoms"></a>Symptome

Wenn eine Artikelgewichtsmenge in Batches aufgeteilt wird, verwendet das Feld **Entnahmemenge** die Mindestmenge, die für den Artikel festgelegt wurde, nicht die nominelle Menge.

## <a name="resolution"></a>Lösung

Das System verhält sich wie vorgesehen. Das System verwendet für die Kommissionierung die Mindestmengeneinstellung jedes Artikels.
