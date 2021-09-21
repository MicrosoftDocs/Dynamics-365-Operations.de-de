---
title: Sie können ein freigegebenes Produkt nicht löschen.
description: Sie können ein freigegebenes Produkt und alle seine Varianten nur löschen, wenn das freigegebene Produkt keine zugehörigen Transaktionen hat.
author: SmithaNataraj
ms.date: 06/11/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f03d45a36401314a4b02ff354fabb474568c48b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476476"
---
# <a name="you-cant-delete-a-released-product"></a>Sie können ein freigegebenes Produkt nicht löschen.

## <a name="symptoms"></a>Symptome

Sie können ein freigegebenes Produkt und alle seine Varianten nur löschen, wenn das freigegebene Produkt keine zugehörigen Transaktionen hat.

## <a name="resolution"></a>Lösung

Gehen Sie folgendermaßen vor, um ein freigegebenes Produkt oder einen Produktstamm zu löschen.

1. Schließen Sie alle offenen Transaktionen für die Elemente.
1. Reduzieren Sie den Bestand auf 0 (Null).
1. Führen Sie den Bestandsabschluss durch.
1. Löschen Sie alle Produktvarianten für den Produktstamm, den Sie löschen möchten.
