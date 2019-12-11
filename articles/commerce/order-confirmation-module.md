---
title: Auftragsbestätigungsmodul
description: In diesem Thema werden Auftragsbestätigungsmodule behandelt und deren Erstellung in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698325"
---
# <a name="order-confirmation-module"></a>Auftragsbestätigungsmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema werden Auftragsbestätigungsmodule behandelt und deren Erstellung in Microsoft Dynamics 365 Commerce beschrieben.

## <a name="overview"></a>Übersicht

Ein Auftragsbestätigungsmodul wird verwendet, um eine Bestätigungsnachricht auf einer Auftragsbestätigungsseite anzuzeigen, nachdem ein Auftrag aufgegeben wurde. Das Auftragsbestätigungsmodul zeigt die Auftragsbestätigungsnummer und die Debitoren-E-Mail-Adresse an, die beim Bezahlen angegeben wurden.

Wenn ein Auftrag während des Bestellvorgangs aufgegeben wird, werden die Auftragsbestätigungsnummer und die Debitoren-E-Mail-Adresse als Abfragezeichenfolge in der URL der Seite an die Auftragsbestätigungsseite übergeben. Das Auftragsbestätigungsmodul erhält diese Informationen und zeigt den Auftragsstatus auf der Auftragsbestätigungsseite an. Das Auftragsbestätigungsmodul benötigt diesen Seitenkontext, um den Status des Auftrags anzuzeigen.

## <a name="order-confirmation-module-properties"></a>Eigenschaften des Auftragsbestätigungsmoduls

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Überschrift       | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Das Auftragsbestätigungsmodul kann eine Überschrift haben. Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet. Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen. |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a>Module, die in einem Modul einer Auftragsbestätigungsseite verwendet werden können 

- **Empfehlungen** – Das Empfehlungsmodul kann auf der Auftragsbestätigungsseite platziert werden, um dem Kunden andere Produkte vorzuschlagen.
- **Marketing** – Das Marketingmodul kann der Auftragsbestätigungsseite Marketinginhalte hinzufügen.

## <a name="create-an-order-confirmation-page-module"></a>Erstellen eines Moduls für eine Auftragsbestätigungsseite

1. Erstellen Sie eine Seitenvorlage, die mit **Auftragsbestätigung** bezeichnet ist.
1. Im **Haupt-** Slot der Standardseite fügen Sie ein Auftragsbestätigungsmodul hinzu.
1. Fügen Sie im Auftragsbestätigungsmodul ein Empfehlungsmodul hinzu.
1. Vorlage speichern und Vorschau anzeigen. Das Auftragsbestätigungsmodul soll nicht gerendert werden, da es den Kontext der Auftragsbestätigungsnummer benötigt.
1. Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.
1. Verwenden Sie die Auftragsbestätigungsvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Auftragsbestätigung** hat.
1. Fügen Sie die Standardseite zum Seitenumriss hinzu.
1. Fügen Sie im **Kopfzeilen**-Slot ein Kopffragment hinzu.
1. Fügen Sie im **Fußzeilen**-Slot ein Fußzeilenfragment hinzu.
1. Fügen Sie im **Haupt**-Slot ein Auftragsbestätigungsmodul hinzu.
1. Fügen Sie im Eigenschaftenbereich des Auftragsbestätigungsmoduls die Überschrift **Auftragsbestätigung** hinzu.
1. Fügen Sie unter dem Auftragsbestätigungsmodul ein Empfehlungsmodul hinzu und konfigurieren Sie es so, dass es die Einstellungen **Neu** und **Bestseller** verwendet.
1. Speichern Sie die Seite, laden Sie es hoch und zeigen Sie eine Vorschau an.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kauffeldmodul](add-buy-box.md)

[Einkaufswagenmodul](add-cart-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)
