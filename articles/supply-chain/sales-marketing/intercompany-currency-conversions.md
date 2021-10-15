---
title: Intercompany-Währungsumrechnungen
description: In diesem Thema werden Währungsumrechnungen für Intercompany-Transaktionen erläutert.
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 540849003d532ef2f0905c18332d9cb82a04cf7c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548295"
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
