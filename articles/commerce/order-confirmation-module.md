---
title: Auftragsdetailmodul
description: In diesem Thema werden Auftragsdetailmodule behandelt und deren Verwendung in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026016"
---
# <a name="order-details-module"></a>Auftragsdetailmodul


[!include [banner](includes/banner.md)]

In diesem Thema werden Auftragsdetailmodule behandelt und deren Verwendung in Microsoft Dynamics 365 Commerce beschrieben.

## <a name="overview"></a>Übersicht

Nachdem eine Bestellung aufgegeben wurde, kann das Bestelldetailmodul verwendet werden, um die Bestätigungsdetails anzuzeigen. Hier werden die Bestellbestätigungs-ID, die Bestellkontaktinformationen und andere Bestelldetails angezeigt, z. B. die gekauften Artikel, die Zahlungsinformationen und die Versandmethode.

## <a name="order-confirmation-module-properties"></a>Eigenschaften des Auftragsbestätigungsmoduls

| Eigenschaftenname  | Werte | Beschreibung |
|----------------|--------|-------------|
| Überschrift        | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Das Auftragsbestätigungsmodul kann eine Überschrift haben. Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet. Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen. |
| Kontaktnummer | Text | Für auftragsbezogene Fragen kann eine Telefonnummer angegeben werden. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Module, die in einem Modul einer Auftragsdetailseite verwendet werden können

Wenn Sie eine Bestelldetailseite erstellen, können Sie zusätzlich zum Bestelldetail-Modul weitere relevante Module hinzufügen. Im Folgenden finden Sie einige Beispiele hierfür:

- **Empfehlungsmodule** – Das Empfehlungsmodul kann auf der Auftragsbestätigungsseite platziert werden, um dem Kunden andere Produkte vorzuschlagen.
- **Marketing-Module** – Zur Seite mit den Bestelldetails kann ein beliebiges Marketingmodul hinzugefügt werden, um Marketinginhalte anzuzeigen.

## <a name="create-an-order-details-page-module"></a>Erstellen eines Moduls für eine Bestelldetailseite

1. Erstellen Sie eine Seitenvorlage, die mit **Auftragdetailvorlage** bezeichnet ist.
1. Im **Haupt-** Slot der Standardseite fügen Sie ein Auftragsdetailmodul hinzu.
1. Fügen Sie im Auftragsdetailmodul ein Empfehlungsmodul hinzu.
1. Vorlage speichern und Vorschau anzeigen. Das Auftragsdetailmodul soll nicht gerendert werden, da es den Kontext der Auftragsbestätigungsnummer benötigt.
1. Beenden Sie die Bearbeitung der Vorlage und veröffentlichen Sie sie.
1. Verwenden Sie die Auftragsdetailvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Auftragsdetail** hat.
1. Fügen Sie die Standardseite zum Seitenumriss hinzu.
1. Fügen Sie im **Kopfzeilen**-Slot ein Kopffragment hinzu.
1. Fügen Sie im **Fußzeilen**-Slot ein Fußzeilenfragment hinzu.
1. Fügen Sie im **Haupt**-Slot ein Auftragsdetailmodul hinzu.
1. Fügen Sie im Eigenschaftenbereich für Auftragsdetailmodule die Überschrift **Auftragsdetail** hinzu.
1. Fügen Sie unter dem Auftragsdetailmodul ein Empfehlungsmodul hinzu und konfigurieren Sie es so, dass es die Einstellungen **Neu** und **Bestseller** verwendet.
1. Seite speichern und Vorschau anzeigen.
1. Beenden Sie die Bearbeitung der Seite und veröffentlichen Sie sie.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Übersicht](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kauffeldmodul](add-buy-box.md)

[Einkaufswagenmodul](add-cart-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)
