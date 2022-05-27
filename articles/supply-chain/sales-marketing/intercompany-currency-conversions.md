---
title: Intercompany-Währungsumrechnungen
description: In diesem Thema werden Währungsumrechnungen für Intercompany-Transaktionen erläutert.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f0af05c324bb67744ba6650e3d7a4ba8b958040e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671897"
---
# <a name="intercompany-currency-conversions"></a>Intercompany-Währungsumrechnungen

[!include [banner](../../includes/banner.md)]

Unterscheidet sich der Währungscode zwischen Originalauftrag und Intercompany-Bestellung, wird die Währung für die folgenden Felder bei aktivierter Synchronisierung konvertiert.

- **Preis je Einheit**
- **Verkaufsbelastungen** oder **Belastungen für Einkäufe**
- **Skonto**
- **Sammelrabatt**

Diese Felder werden dann mit der Intercompany-Auftragsposition synchronisiert.

Da jedoch die Währung im Intercompany-Auftrag und in der Intercompany-Bestellung immer synchronisiert wird, werden die folgenden Felder ohne Währungskonvertierung synchronisiert:

- **Preis je Einheit**
- **Verkaufsbelastungen** oder **Belastungen für Einkäufe**
- **Skonto**
- **Rabatt in Prozent**
- **Sammelrabatt**
- **Sammelrabatt (Prozentsatz)**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
