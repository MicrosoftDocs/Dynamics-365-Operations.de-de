---
title: Versandrabatt
description: Dieser Artikel beschreibt die Versandrabattfunktionen in Microsoft Dynamics 365 Commerce und wie Sie sie einrichten, um sie verwenden zu können.
author: ShalabhjainMSFT
ms.date: 08/23/2020
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2019-01-31
ms.openlocfilehash: f19566ce64becea4a53a8479cb5a08579567cda1
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346401"
---
# <a name="shipping-discount"></a>Versandrabatt

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dieser Artikel beschreibt die Versandrabattfunktionen in Microsoft Dynamics 365 Commerce und wie Sie sie einrichten, um sie verwenden zu können.

Der kostenlose oder ermäßigte Versand ist ein Faktor, der die Online-Kaufentscheidungen der Kunden beeinflusst. Um ihren Umsatz pro Transaktion zu steigern, nutzen viele Einzelhändler einen kostenlosen Versandvorteil, um Kunden zu motivieren, mehr Artikel in ihren Warenkorb zu legen.

Commerce unterstützt eine Versandrabattfunktion, mit der Einzelhändler einen Rabattprozentsatz auf die Versandkosten für eine bestimmte Versandmethode konfigurieren können, wenn der Gesamtverkaufsbetrag für qualifizierte Artikel in der Transaktion bestimmte Kriterien erfüllt. Ein Beispiel für ein Szenario, das die Versandrabattfunktion verwendet, ist „Geben Sie 50 $ oder mehr aus, um Ihre Lieferung kostenlos am nächsten Tag zu erhalten.“

## <a name="prerequisites"></a>Voraussetzungen

Die Versandrabattfunktion wird von den Funktionen [Erweiterte automatische Omni-Channel-Belastungen](/dynamics365/unified-operations/retail/omni-auto-charges) von Commerce unterstützt. Damit die Versandrabattfunktion funktioniert, müssen Sie die Konfiguration **Erweiterte Auto-Belastungen verwenden** auf der Registerkarte **Debitorenauftrag** auf der Seite **Commerce-Prameter** von Commerce headquarters aktivieren. Einzelhändler können die erweiterte automatische Gebührenfunktion verwenden, um verschiedene Arten von Gebühren einzurichten, wie z. B. Handhabung, Installation und Entsorgung.

Dieser Versandrabatt gilt nur für die Versandkosten. Daher muss ein Einzelhändler angeben, bei welchen Gebühren es sich um Versandkosten handelt. Um die Versandkosten anzugeben, gehen Sie in Commerce headquarters zu **Kanaleinstellung \> Gebühren \> Gebührencode** und stellen Sie die Option **Versandkosten** für die gewünschten Gebühren auf **Ja**.

![Eine Gebühr als Versandkosten festlegen.](./media/Specify_shipping_charge.png)

## <a name="configuration"></a>Variante

Die Versandrabattfunktion ist stufenbasiert und unterstützt nur die Berechnungsart **Prozentsatz**. Um einen Versandrabatt einzurichten, gehen Sie in Commerce headquarters auf **Preise und Rabatte \> Versandschwellenwertrabatt**. Sie können dann die Lieferart angeben, für die der Rabatt gilt, einen oder mehrere Schwellenwertbeträge und den Rabattprozentsatz für jeden Schwellenwert festlegen. Sie können auch eine Liste mit Kategorien oder Produkten als qualifizierte Artikel konfigurieren. Auf diese Weise wird nur der Verkaufsbetrag für diese Artikel in einer Transaktion gezählt, wenn das Preisgestaltungsmodul auswertet, ob die Transaktionssumme den Schwellenwert erreicht.

> [!NOTE]
> Im Gegensatz zu anderen Rabattarten erstellt der Versandrabatt keine Rabattpositionen. Stattdessen bearbeitet er direkt die Versandkosten und fügt den Namen des Rabatts an die Kostenbeschreibung an.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
