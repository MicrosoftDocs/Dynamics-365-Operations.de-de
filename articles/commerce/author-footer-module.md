---
title: Fußzeilenmodul
description: In diesem Thema werden Fußzeilenmodule behandelt nd wie sie in Dynamics 365 Commerce erstellt werden.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 542796ffce08694954d03878cd7782b01c2c6b27
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780258"
---
# <a name="footer-module"></a>Fußzeilenmodul  

[!include [banner](includes/banner.md)]

In diesem Thema werden Fußzeilenmodule behandelt und deren Erstellung in Microsoft Dynamics 365 Commerce beschrieben.

Das Fußzeilenmodul ist ein spezielle Container, der verwendet wird, um die Module zu hosten, die in der Fußzeile erscheinen. Zum Beispiel kann es Verknüpfungen an verschiedene Seiten auf der Site umfassen wie **Kontaktieren Sie uns** und **Speichern Sie Richtlinien**.

Das folgende Bild zeigt ein Beispiel eines Fußzeilenmoduls, das auf einer Homepage verwendet wird.

![Beispiel eines Fußzeilenmoduls.](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Fußzeilenmoduleigenschaften 

Wie die meisten Container unterstützt ein Fußzeilenmodul die Eigenschaften für die Überschrift und die Breite. Es unterstützt außerdem das Hinzufügen mehrerer Fußzeilenkategoriemodulen. Jedes Fußzeilenkategoriemodul, das hinzugefügt wird, wird als Spalte im Fußzeilenmodul dargestellt.

## <a name="modules-available-in-a-footer-module"></a>Module, di in einem Fußzeilenmodul verfügbar sind

**Fußzeilenelement** - Ein Fußzeilenelement-Modul kann entweder eine Überschrift oder einen Link enthalten. Die Überschrift wird allgemein als Fußzeilentitel verwendet.  Jeder Link in der Fußzeile kann so konfiguriert werden, damit nur Text (z.B. „kontaktieren Sie uns“ und „Datenschutz“ Links) enthalten ist oder Text und ein Bild hat (beispielsweise, Social Media Links). Wenn sowohl eine Überschrift als auch ein Link angegeben sind, hat die Eigenschaft Überschrift Vorrang vor dem Link. 

**Zurück zum Anfang** – Ein Modul zurück nach oben stellt einen Link für die rasche Navigation zum Seitenanfang bereit. Ein Ziel ist erforderlich. Der Standardzielwert ist \#, den Benutzer an den Seitenanfang bringt.

## <a name="create-a-footer-module"></a>Erstellen eines Fußzeilenmoduls

1. Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus, um ein neues Fragment zu erstellen.
1. Wählen Sie im Dialogfeld **Ein Fragment auswählen** das Modul **Container** aus, geben Sie einen Namen für das Fragment ein und wählen Sie dann **OK** aus.
1. Wählen Sie im Slot **Standard-Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Im Dialogfeld **Module auswählen** wählen Sie das **Fußzeilenkategoriemodul** und wählen Sie dann **OK**.
1. Wählen Sie im Slot **Fußzeilenkategorie** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Fußzeilenelement** und dann **OK** aus.
1. Wählen Sie den Slot **Fußzeilenelement** und wählen Sei dann im Eigenschaftenbereich auf der rechten Seite konfigurieren Sie die Überschrift und verknüpfen Sie Text und Bild nach Bedarf.
1. Um weitere Fußzeilenelemente hinzuzufügen, wiederholen Sie die Schritte 5 bis 7.
1. Um einen Link „Zurück zum Anfang“ der Fußzeile hinzuzufügen, wählen Sie die Ellipsen-Schaltfläche (**...**) für die **Fußzeilenkategorie** und anschließend **Modul hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Zurück zum Anfang** und dann **OK** aus.
1. Wählen Sie den Slot **Zurück an den Anfang** und wählen Sie dann im Eigenschaftenbereich auf der rechten Seite Konfigurieren Sie den Text und andere Moduleigenschaften nach Bedarf.
1. Wählen **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

Um Sicherzustellen, dass eine Kopfzeile auf jeder Seite angezeigt wird, führen Sie die folgenden Schritte für jede Seitenvorlage aus, die für die Site erstellt wird.

1. Im Slot **Fußzeile** wählen Sie das Modul **Standardseite** und fügen das Fußzeilenfragment hinzu, das Sie erstellt haben.
1. Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

Wenn Sie das Fragment der Seitenvorlagen hinzufügen, helfen Sie sicherzustellen, dass die Fußzeile auf jeder Seite angezeigt wird.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kauffeldmodul](add-buy-box.md)

[Einkaufswagenmodul](add-cart-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
