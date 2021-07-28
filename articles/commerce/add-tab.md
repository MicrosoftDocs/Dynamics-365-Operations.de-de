---
title: Registerkartenmodul
description: Dieses Thema behandelt Registerkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e7d2cd7b7ce9446d77eff66433739c8ea6b1f309
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348295"
---
# <a name="tab-module"></a>Registerkartenmodul

[!include [banner](includes/banner.md)]

Dieses Thema behandelt Registerkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Registerkartenmodule sind containerähnliche Module, mit denen die Informationen auf einer Site-Seite auf Registerkarten organisiert werden. Sie können auf jeder Seite verwendet werden, auf der Informationen auf Registerkarten angezeigt werden müssen.

In jedem Registerkartenmodul kann ein oder mehrere Registerkartenelemente hinzugefügt werden. Jedes Registerkartenelementmodul repräsentiert eine einzelne Registerkarte. In jedem Registerkartenelementmodul können ein oder mehrere Module hinzugefügt werden. Es gibt keine Einschränkungen hinsichtlich der Modultypen, die einem Registerkartenelementmodul hinzugefügt werden können.

Das folgende Bild zeigt ein Beispiel eines Registerkartenmoduls, das auf einer Homepage verwendet wird. In diesem Beispiel ist die **Versand** Registerkarte ausgewählt.

![Beispiel eines Registerkarten-Moduls.](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a>Registerkartenmoduleigenschaften

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Überschrift | Text | Diese Eigenschaft gibt eine optionale Textüberschrift für das Registerkartenmodul an. |
| Aktiver Registerkartenindex | Nummer | Diese Eigenschaft gibt die Registerkarte an, die beim Laden einer Seite standardmäßig aktiv sein soll. Wenn kein Wert angegeben wird, ist das erste Registerkartenelement standardmäßig aktiv. |

## <a name="tab-item-module-properties"></a>Registerkartenelementmoduleigenschaften

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Titel | Text | Diese Eigenschaft gibt die Textüberschrift für das Registerkartenelementmodul an. |

## <a name="add-a-tab-module-to-a-page"></a>Ein Registerkartenmodul einer Seite hinzufügen

Um ein Registerkartenmodul einer Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Verwenden Sie die Fabrikam-Marketingvorlage (oder eine Vorlage ohne Einschränkungen), um eine neue Seite mit dem Namen **Richtlinienseite speichern** zu erstellen.
1. Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.
1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Registerkarte** und dann **OK** aus.
1. Wählen Sie im Eigenschaftenbereich des Registerkartenmoduls die Option **Überschrift** neben dem Stiftsymbol.
1. In dem **Überschrift** Dialogfeld unter **Überschriftstext** geben Sie den Überschriftentext ein (z. B. **Richtlinien**). Wählen Sie dann **OK** aus.
1. Wählen Sie im Slot **Registerkarte** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Im Dialogfeld **Modul hinzufügen** wählen Sie das **Registerkartenelement**-Modul und wählen Sie dann **OK**.
1. Im Eigenschaftenbereich des Registerkartenelementmoduls unter **Titel** geben Sie den Titeltext ein (z. B. **Lieferung**).
1. Wählen Sie im Slot **Registerkartenelement** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Textblock** und dann **OK** aus.
1. Fügen Sie im Eigenschaftenbereich des Textblockmoduls unter **Rich Text** einen Textabschnitt hinzu.
1. Im Slot **Registerkarte** fügen Sie einige weitere Registerkartenelementmodule mit Titeln hinzu. Fügen Sie in jedem Registerkartenelementmodul ein Textblockmodul mit Inhalt hinzu.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen. Auf der Seite wird ein Registerkartenmodul angezeigt, das Registerkartenelementmodule enthält, deren Inhalt Sie hinzugefügt haben.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Akkordeonmodul](add-accordion.md)

[Textblockmodul](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]