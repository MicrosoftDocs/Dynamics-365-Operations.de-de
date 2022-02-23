---
title: Auftragsbestätigungsmodul
description: In diesem Thema werden Auftragsbestätigungsmodule behandelt und deren Verwendung in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bf33ebf9c0c5136f40fcd7e1012988d186c4169b
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2020
ms.locfileid: "4412728"
---
# <a name="order-confirmation-module"></a>Auftragsbestätigungsmodul

[!include [banner](includes/banner.md)]

In diesem Thema werden Auftragsbestätigungsmodule behandelt und deren Verwendung in Microsoft Dynamics 365 Commerce beschrieben.

## <a name="overview"></a>Übersicht

Nachdem ein Auftrag erteilt wurde, werden mit dem Auftragsbestätigungsmodul Auftragsbestätigungsdetails angezeigt. Es werden Auftragsbestätigungs-ID, Auftragskontaktinformationen und andere Auftragsdetails angezeigt, wie z. B. erworbene Artikel, Zahlungsinformationen, Abholoptionen und Liefermethode.

## <a name="order-confirmation-module-properties"></a>Eigenschaften des Auftragsbestätigungsmoduls

| Eigenschaftenname  | Werte | Beschreibung |
|----------------|--------|-------------|
| Überschrift        | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Das Auftragsbestätigungsmodul kann eine Überschrift haben. Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet. Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen. |
| Kontaktnummer | Text | Für auftragsbezogene Fragen kann eine Telefonnummer angegeben werden. |
| Informationen zum Abholzeitfenster anzeigen | True oder False | Diese Eigenschaft ist verfügbar in Dynamics 365 Commerce 10.0.15 und höher. Wenn true, werden die Informationen zum Abholzeitfenster angezeigt, sofern diese für einen Abholartikel bereitgestellt wurden|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a>Module, die auf einer Auftragsbestätigungsseite verwendet werden können

Wenn Sie eine Auftragsbestätigungsseite erstellen, können Sie zusätzlich zum Auftragsbestätigungsmodul weitere relevante Module hinzufügen. Im Folgenden finden Sie einige Beispiele hierfür:

- **Empfehlungsmodul** – Das Empfehlungsmodul kann zur Auftragsbestätigungsseite hinzugefügt werden, um dem Kunden andere Produkte vorzuschlagen.
- **Marketing-Module** – Zur Auftragsbestätigungsseite kann ein beliebiges Marketingmodul hinzugefügt werden, um Marketinginhalte anzuzeigen.

## <a name="add-an-order-confirmation-module-to-a-page"></a>Ein Auftragsbestätigungsmodul zu einer Seite hinzufügen

Um ein Auftragsbestätigungsmodul zu einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
1. Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie den Namen **Auftragsbestätigungsvorlage** ein und wählen Sie **OK**.
1. Wählen Sie im Slot **Körper** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Standardseite** und dann **OK** aus.
1. Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** aus, wählen Sie die **Auftragsbestätigung** aus, und wählen dann **OK** aus.
1. Wählen Sie **Speichern** und dann **Vorschau** aus, um eine Vorlage in der Vorschau anzuzeigen. Das Auftragsbestätigungsmodul wird nicht gerendert werden, da es den Kontext der Auftragsbestätigungsnummer benötigt.
1. Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.
1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. In dem Dialogfeld **Vorlage auswählen** wählen Sie **Auftragsbestätigungsvorlage** aus. Unter **Seitenname** geben Sie **Auftragsbestätigungsseite** ein und wählen Sie dann **OK**.
1. Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** aus, wählen Sie die **Auftragsbestätigung** aus, und wählen dann **OK** aus.
1. Wählen Sie im Eigenschaftenbereich für das Auftragsbestätigungsmodul die Option **Überschrift** neben dem Stiftsymbol aus.
1. Im Feld **Überschriftstext** des Dialogfelds **Überschrift** geben Sie den Überschriftentext **Auftragsbestätigung** ein, und wählen Sie dann **OK** aus.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einkaufswagenmodul](add-cart-module.md)

[Modul für Einkaufswagensymbol](cart-icon-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Zahlungsmodul](payment-module.md)

[Versandadressenmodul](ship-address-module.md)

[Lieferoptionenmodul](delivery-options-module.md)

[Abholinformationsmodul](pickup-info-module.md)

[Geschenkkartenmodul](add-giftcard.md)
