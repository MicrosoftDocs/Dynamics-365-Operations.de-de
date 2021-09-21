---
title: Die Bedingungen der Handelsvereinbarung werden nicht auf importierte Auftragspositionen angewendet
description: Die Preise und Rabatte für Handelsabkommen gelten nicht für Verkaufs- oder Bestellpositionen, die über die Datenverwaltung importiert werden
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
ms.openlocfilehash: fef38819efaff2f2a927cf09fc7f469490149574
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476472"
---
# <a name="trade-agreement-conditions-arent-applied-to-imported-order-lines"></a>Die Bedingungen der Handelsvereinbarung werden nicht auf importierte Auftragspositionen angewendet

## <a name="symptoms"></a>Symptome

Handelsabkommen, die für Verkaufs- oder Bestellpositionen gelten, werden nicht auf Positionen angewendet, die über die Datenverwaltung importiert werden. Dieselben Handelsabkommen gelten jedoch für manuell erstellte Verkaufs- oder Bestellpositionen.

## <a name="cause"></a>Ursache

Wenn Bestellpositionen, die über die Datenverwaltung importiert werden, bereits Preisinformationen enthalten, wird das Handelsabkommen für diese Positionen nicht neu bewertet. Wenn zum Beispiel **Positionsrabatt in Prozent** oder einer der Preis- und Rabattwerte für eine Position festgelegt ist, werden Handelsabkommen für diese Position nicht nachgeschlagen.

## <a name="workaround"></a>Problemumgehung

Dieses Verhalten wird erwartet und ist sowohl für Aufträge als auch für Bestellungen ähnlich.

Importieren Sie zur Umgehung dieses Problems die Bestellpositionen, ohne Preisinformationen festzulegen. Die Handelsabkommen werden dann angewendet und die Bestellpositionen werden basierend auf den definierten Handelsabkommen aktualisiert.
