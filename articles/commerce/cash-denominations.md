---
title: Bargeldnennwerte für die Verkaufsstelle (POS) konfigurieren
description: Bargeldnennwerte für Banknoten und Münzen können Backoffice definiert werde, um von den Kassierern, von den Vertriebsmitarbeitern und von Managern in Ihrem Unternehmen in POS verwendet zu werden.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.industry: Retail
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
ms.openlocfilehash: c61cde76bf2bfe3ff48b306a8a161fa27f50ac41
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273692"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a>Bargeldnennwerte für die Verkaufsstelle (POS) konfigurieren

[!include [banner](includes/banner.md)]

Bargeldnennwerte für Banknoten und Münzen können Backoffice definiert werde, um von den Kassierern, von den Vertriebsmitarbeitern und von Managern in Ihrem Unternehmen in POS verwendet zu werden. Diese Nennwerte können verwendet werden, um bei der Bargeld-Inventur für die Berechnung des Tagesumsatzes oder für ein schelles Produktangebot verwendet werden.

## <a name="define-denominations"></a>Nennwerte definieren

Die Nennwerte werden pro Laden unter der Option **Einstellungen** \> **Bargelddeklaration** von der Laden-Eigenschaftenseite eingerichtet.

![Bargelddeklarationsoption.](./media/image1-denomination.png)

Nennwerte definieren:

1. Klicken Sie auf **Neu**.
1. Geben Sie den Typ an (Banknote oder Münzen).
1. Geben Sie den Betrag ein (Wert).

![Seite für Bargelddeklarationsnennungen.](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>Funktionsprofil konfigurieren

Wenn in bar am POS bezahlt wird, kann der Benutzer die Währungen rasch verwenden, um den vom Kunden bezahlten Betrag einzugeben. Im Funktionsprofil können Sie die beiden Optionen für die Anzeige für den Nennwert in POS sperren konfigurieren.

- **Größer oder gleich fälligen Betrag**: Standardmäßig zeigt POS nur die Hinweisnennwerte an, die größer als der fällige Betrag sind, der das Einnotenanbieten zulässt. Wenn beispielsweise der fällige Betrag $7,50 POS ist, würden die folgenden Nennwerte angezeigt: EUR 10, 20, 50 und 100. Wenn Sie einen dieser Beträge berühren, wird automatisch das Zahlungsmittel des Verkaufs für diesen Betrag ausgefüllt. Die $1 und $5 Noten werden nicht angezeigt, da diese Beträge kleiner sind als der fällige Betrag.
- **Alle Nennwerte**: – Wählen Sie diese Option aus, um alle Hinweisnennwerte in POS, unabhängig vom fälligen Betrag immer anzuzeigen. Das bedeutet, dass der Benutzer eine Kombination von Hinweisen verwenden kann, um den fälligen Betrag zu erreichen. Wenn beispielsweise der fällige Betrag $25.00 ist, kann der Benutzer $20 und $5 wählen, um den Verkauf abzuschließen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
