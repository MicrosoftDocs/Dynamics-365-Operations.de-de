---
title: Fußzeilenmodul
description: In diesem Thema werden Fußzeilenmodule behandelt nd wie sie in Dynamics 365 Commerce erstellt werden.
author: anupamar
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 51f8d26d6223dcd1f6961058cd9d772a67c69670
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269635"
---
# <a name="footer-module"></a>Fußzeilenmodul  


[!include [banner](includes/banner.md)]

In diesem Thema werden Fußzeilenmodule behandelt und deren Erstellung in Microsoft Dynamics 365 Commerce beschrieben.

## <a name="overview"></a>Übersicht

Das Fußzeilenmodul ist ein spezielle Container, der verwendet wird, um die Module zu hosten, die in der Fußzeile erscheinen. Zum Beispiel kann es Verknüpfungen an verschiedene Seiten auf der Site umfassen wie **Kontaktieren Sie uns** und **Speichern Sie Richtlinien**.

## <a name="footer-module-properties"></a>Fußzeilenmoduleigenschaften 

Wie die meisten Container unterstützt ein Fußzeilenmodul die Eigenschaften für die Überschrift und die Breite. Es unterstützt außerdem das Hinzufügen mehrerer Fußzeilenkategoriemodulen. Jedes Fußzeilenkategoriemodul, das hinzugefügt wird, wird als Spalte im Fußzeilenmodul dargestellt.

## <a name="modules-available-in-a-footer-module"></a>Module, di in einem Fußzeilenmodul verfügbar sind

**Fußzeilenartikel** – Ein Fußzeilenartikelmodul kann eine Überschrift, ein Bild und einen Link enthalten. Die Überschrift kann entweder alleine oder mit einem Bild und einem Link zusammen verwendet werden. Jeder Link in der Fußzeile kann so konfiguriert werden, damit nur Text (z.B. „kontaktieren Sie uns“ und „Datenschutz“ Links) enthalten ist oder Text und ein Bild hat (beispielsweise, Social Media Links).

**Zurück zum Anfang** – Ein Modul zurück nach oben stellt einen Link für die rasche Navigation zum Seitenanfang bereit. Ein Ziel ist erforderlich. Der Standardzielwert ist der #, den Benutzer an den Seitenanfang bring.

## <a name="author-a-footer-module"></a>Erstellen eines Fußzeilenmoduls

1. Im Navigationsbereich wählen Sie **Fragmente** und **Neues Seiten-Fragment** aus.
1. Im Dialogfeld **Neues Seiten-Fragment** wählen Sie das Fußzeilenmodul aus, geben Sie einen Namen für das Seitenfragment ein, und wählen Sie dann **OK**.
1. Wählen Sie im Seitenlayout auf der linken Seite die Ellipsen-Schaltfläche (**...**) für das Fußzeilenmodul und anschließend **Modul hinzufügen** aus.
1. Im Dialogfeld **Modul hinzufügen** wählen Sie das Fußzeilenkategoriemodul und wählen Sie dann **OK**.
1. Wählen Sie im Seitenlayout auf der linken Seite die Ellipsen-Schaltfläche für das Fußzeilenmodul und anschließend **Modul hinzufügen** aus.
1. Im Dialogfeld **Modul hinzufügen** wählen Sie das Fußzeilenelementmodul und wählen Sie dann **OK**.
1. In der Gliederungsstruktur wählen Sie das Fußzeilenelementmodul aus. Im Eigenschaftenbereich auf der rechten Seite konfigurieren Sie die Überschrift und verknüpfen Sie Text und Bild nach Bedarf.
1. Um weitere Fußzeilenelemente hinzuzufügen, wiederholen Sie die Schritte 5 bis 7.
1. Um einen Link „Zurück zum Anfang“ der Fußzeile hinzuzufügen, wählen Sie die Ellipsen-Schaltfläche für das Fußzeilenmodul und anschließend **Modul hinzufügen** aus.
1. Im Dialogfeld **Modul hinzufügen** wählen Sie das Modul zurück zum Anfang und wählen dann **OK**.
1. In der Gliederungsstruktur wählen Sie das Modul zurück zum Anfang aus. Im Eigenschaftenbereich auf der rechten Seite konfigurieren Sie das Modul zurück zum Anfang, wie Sie es benötigen.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Seitenfragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

Auf jeder Seitenvorlage, die für den Standort erstellt wurde, folgen Sie diesen Schritten.

1. Im **Haupt-** Slot der Standardseite im Fußzeilenmodul fügen Sie das Fußzeilenfragment hinzu, das Sie erstellt haben.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

Wenn Sie das Seitenfragment der Seitenvorlagen hinzufügen, helfen Sie sicherzustellen, dass die Fußzeile auf jeder Seite angezeigt wird.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kauffeldmodul](add-buy-box.md)

[Einkaufswagenmodul](add-cart-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)
