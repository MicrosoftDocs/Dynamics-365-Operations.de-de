---
title: Artikel ohne Bestand können ausgecheckt werden
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn Kunden nicht vorrätige Artikel in ihren Warenkorb legen und mit der Kaufabwicklung fortfahren können.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1458328056a3ace8e5600a4c2d188e05b66c8110acbe44c869294a6b6e251e84
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753693"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Artikel ohne Bestand können ausgecheckt werden

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn Kunden nicht vorrätige Artikel in ihren Warenkorb legen und mit der Kaufabwicklung fortfahren können.

## <a name="description"></a>Beschreibung

Benutzer können einen Artikel in ihren Warenkorb legen, obwohl sich im Shop kein Bestand befindet, und dann zur Kasse gehen.

## <a name="resolution"></a>Lösung

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>Die Eigenschaft „Nicht vorrätig-Fehlermeldungen anzeigen“ im Commerce-Website-Generator aktivieren

Befolgen Sie diese Schritte, im die Eigenschaft **Nicht vorrätig-Fehlermeldungen anzeigen** im Commerce-Website-Generator zu aktivieren.

1. Wählen Sie die Website aus, an der Sie arbeiten.
1. Wählen Sie im linken Navigationsbereich **Seiten** aus.
1. Wählen Sie zum Öffnen **CartPage** aus.
1. Wählen Sie den Slot **Einkaufswagen 1** und **Bearbeiten** aus. Wählen Sie dann im Eigenschaftenbereich das Kontrollkästchen **Nicht vorrätig-Fehlermeldungen anzeigen** aus.
1. Speichern und veröffentlichen Sie die Seite.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Bestandseinstellungen anwenden](../inventory-settings.md)

[Lagerverfügbarkeit für Retail Channels berechnen](../calculated-inventory-retail-channels.md)

[Bestandpuffer und Bestandsebenen konfigurieren](../inventory-buffers-levels.md)
