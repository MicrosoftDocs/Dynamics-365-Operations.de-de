---
title: Strichcodes einrichten
description: Dieser Artikel beschreibt, wie Sie die Strichcodes in Dynamics 365 Commerce verwenden.
author: jblucher
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0785f499a3e106e36b803ae61a9acbdbb072ce17
ms.sourcegitcommit: 28a771d81322e72d88db63a20ff360de084a6087
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3835061"
---
# <a name="set-up-bar-codes"></a>Strichcodes einrichten

[!include [banner](includes/banner.md)]

Dieser Artikel beschreibt, wie Sie die Strichcodes in Dynamics 365 Commerce verwenden.

Sie können mithilfe von Strichcodes Produkte erwerben und verkaufen, Produktvarianten nachverfolgen und Debitoren und Mitarbeiter einrichten. Sie können außerdem Strichcodes verwenden, um Coupons, Geschenkkarten und Gutschriften auszustellen und zu indossieren. Sie können die Produkte so einrichten, dass sie mit Standard-Barcodes oder benutzerdefinierten, hauseigenen Barcodes versehen sind. Produkte können mehrere Strichcodes aufweisen. Beispielsweise könnte ein Produkt mehrere Strichcodes haben, wenn es von verschiedenen Herstellern stammt oder wenn es über Varianten verfügt, hinsichtlich Größe, Stil oder Farbe. Strichcodes können das Gewicht oder den Preis des Produkts enthalten. Strichcodemasken sind Vorlagen, die verwendet werden, um Strichcodes zu erstellen.

> [!NOTE]
> Wenn Sie einen eindeutigen Strichcodes für jede Variantenkombination zuweisen, können Sie den Strichcode am Register scannen und vom Programm feststellen lassen, welche Variante des Produkts verkauft wird. Sie können außerdem Statistiken zu Verkäufen nach Varianten sammeln und anzeigen. Jede Größen-, Farb- und Stilgruppe kann einer eindeutigen Nummer zugewiesen werden, durch die diese Gruppe im Strichcode gekennzeichnet ist. Der Handel verwendet die Barcode-Maske, um automatisch Barcodes für jede Variantenkombination zu erzeugen. Diese Funktion kann hilfreich sein, wenn es viele Größen, Farben und Stile gibt, da die Anzahl der Kombinationen mit jedem zusätzlichen Variantencode erheblich zunimmt. Wird diese Funktion nicht verwendet, müssen die Strichcodes manuell jeder Kombination zugewiesen werden, die eine Produktvariante darstellt.

Sie können Strichcodes manuell oder automatisch erstellen. Um Strichcodes zu erstellen, schließen Sie die folgenden Aufgaben im Auftrag ab, in dem sie aufgeführt sind.

1. [Einrichten von Strichcode-Maskenzeichen](set-up-bar-code-masks.md).
2. [Einrichten von Strichcodemasken](set-up-bar-code-masks.md).
3. Konfigurieren Sie Strichcodeeinstellungen.
4. [Erstellen Sie Strichcodes für Produkte](../supply-chain/pim/tasks/create-bar-code-product.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Strichcodemasken einrichten](set-up-bar-code-masks.md)
