---
title: Intercompany-Währungsumrechnungen
description: In diesem Artikel werden Währungsumrechnungen für Intercompany-Transaktionen erläutert.
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
ms.openlocfilehash: 41bfafc0dcb3bd356931b67dc63b717c0d098116
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851477"
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
