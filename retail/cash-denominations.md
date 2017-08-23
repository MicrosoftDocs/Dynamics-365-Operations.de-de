---
title: "Konfigurieren Sie Bargeldnennwerte für POS"
description: "Bargeldnennwerte für Banknoten und Münzen können Backoffice definiert werde, um von den Kassierern, von den Vertriebsmitarbeitern und von Managern in Ihrem Unternehmen in POS verwendet zu werden."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d280a11670b5887ae5ae582cedf30c093b4b5d7c
ms.openlocfilehash: 9abcbb706d7120c6bcd91fc759b33cb518802a5b
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="configure-cash-denominations-for-pos"></a>Konfigurieren Sie Bargeldnennwerte für POS

[!include[banner](includes/banner.md)]

Bargeldnennwerte für Banknoten und Münzen können Backoffice definiert werde, um von den Kassierern, von den Vertriebsmitarbeitern und von Managern in Ihrem Unternehmen in POS verwendet zu werden. Diese Nennwerte können verwendet werden, um bei der Bargeld-Inventur für die Berechnung des Tagesumsatzes oder für ein schelles Produktangebot verwendet werden.

## <a name="define-denominations"></a>Nennwerte definieren
Die Nennwerte werden pro Shop auf der Seite **Einstellungen** > **Bargelddeklarationsoption von der Shopeigenschaft** eingerichtet. 

![Bargeld-Denominationen](./media/image1-denomination.png)

Nennwerte definieren:
1. Klicken Sie auf **Neu**.
1. Geben Sie den Typ an (Banknote oder Münzen).
1. Geben Sie den Betrag ein (Wert).

![Bargeld-Denominationen](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>Funktionsprofil konfigurieren
Wenn in bar am POS bezahlt wird, kann der Benutzer die Währungen rasch verwenden, um den vom Kunden bezahlten Betrag einzugeben. Im Funktionsprofil können Sie die beiden Optionen für die Anzeige für den Nennwert in POS sperren konfigurieren.

**Größer oder gleich fälligen Betrag**: Standardmäßig zeigt POS nur die Hinweisnennwerte an, die größer als der fällige Betrag sind, der das Einnotenanbieten zulässt. Wenn beispielsweise der fällige Betrag $7,50 POS ist, würden die folgenden Nennwerte angezeigt: EUR 10, 20, 50 und 100. Wenn Sie einen dieser Beträge berühren, wird automatisch das Zahlungsmittel des Verkaufs für diesen Betrag ausgefüllt. Die $1 und $5 Noten werden nicht angezeigt, da diese Beträge kleiner sind als der fällige Betrag.

**Alle Nennwerte**: Wählen Sie diese Option aus, um alle Hinweisnennwerte in POS, unabhängig vom fälligen Betrag immer anzuzeigen. Das bedeutet, dass der Benutzer eine Kombination von Hinweisen verwenden kann, um den fälligen Betrag zu erreichen. Wenn beispielsweise der fällige Betrag $25.00 ist, kann der Benutzer $20 und $5 wählen, um den Verkauf abzuschließen.

