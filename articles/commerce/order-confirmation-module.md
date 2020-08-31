---
title: Auftragsdetailmodul
description: In diesem Thema werden Auftragsdetailmodule behandelt und deren Verwendung in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar
manager: annbe
ms.date: 06/18/2020
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
ms.openlocfilehash: 5876b953a3b3d960c106acf37731fde13b93f8e7
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661171"
---
# <a name="order-details-module"></a>Auftragsdetailmodul

[!include [banner](includes/banner.md)]

In diesem Thema werden Auftragsdetailmodule behandelt und deren Verwendung in Microsoft Dynamics 365 Commerce beschrieben.

## <a name="overview"></a>Übersicht

Nachdem eine Bestellung aufgegeben wurde, kann das Bestelldetailmodul verwendet werden, um die Bestätigungsdetails anzuzeigen. Hier werden die Bestellbestätigungs-ID, die Bestellkontaktinformationen und andere Bestelldetails angezeigt, z. B. die gekauften Artikel, die Zahlungsinformationen und die Versandmethode.

## <a name="order-details-module-properties"></a>Details der Eigenschaften des Auftragsbestätigungsmoduls

| Eigenschaftenname  | Werte | Beschreibung |
|----------------|--------|-------------|
| Überschrift        | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Das Auftragsdetailmodul kann eine Überschrift haben. Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet. Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen. |
| Kontaktnummer | Text | Für auftragsbezogene Fragen kann eine Telefonnummer angegeben werden. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Module, die in einem Modul einer Auftragsdetailseite verwendet werden können

Wenn Sie eine Bestelldetailseite erstellen, können Sie zusätzlich zum Bestelldetail-Modul weitere relevante Module hinzufügen. Im Folgenden finden Sie einige Beispiele hierfür:

- **Empfehlungsmodule** – Das Empfehlungsmodul kann auf der Auftragsbestätigungsseite platziert werden, um dem Kunden andere Produkte vorzuschlagen.
- **Marketing-Module** – Zur Seite mit den Bestelldetails kann ein beliebiges Marketingmodul hinzugefügt werden, um Marketinginhalte anzuzeigen.

## <a name="add-an-order-details-module-to-a-page"></a>Ein Auftragsdetailmodul einer Seite hinzufügen

Um ein Auftragsdetailmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
1. Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie einen Namen für die **Auftragsdetailvorlage** ein und wählen **OK**.
1. Wählen Sie im Slot **Körper** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Standardseite** und dann **OK** aus.
1. Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Auftragsdetails** an und wählen dann **OK** aus.
1. Wählen Sie **Speichern** und dann **Vorschau** aus, um eine Vorlage in der Vorschau anzuzeigen. Das Auftragsdetailmodul soll nicht gerendert werden, da es den Kontext der Auftragsbestätigungsnummer benötigt.
1. Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.
1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. In dem Dialogfeld **Wählen Sie eine Vorlage** wählen Sie die Vorlage **Auftragsdetails-Vorlage** aus. Unter **Seitenname** geben Sie **Auftragsdetailseite** ein und wählen dann **OK**.
1. Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Auftragsdetails** an und wählen dann **OK** aus.
1. Wählen Sie im Eigenschaftenbereich der Auftragsdetails die Option **Überschrift** neben dem Stiftsymbol.
1. In dem **Überschriftstext** Feld des Dialogfelds **Überschrift** geben Sie den Überschriftentext ein und wählen dann **Bestelldetails** aus und dann **OK**.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einkaufswagenmodul](add-cart-module.md)

[Modul für Einkaufswagensymbol](cart-icon-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Zahlungsmodul](payment-module.md)

[Versandadressmodul](ship-address-module.md)

[Lieferoptionsmodul](delivery-options-module.md)

[Geschenkkartenmodul](add-giftcard.md)
