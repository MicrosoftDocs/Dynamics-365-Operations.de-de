---
title: Anpassen der Sitenavigation
description: In diesem Thema wird beschrieben, wie Sie eine benutzerdefinierte Online-Navigationshierarchie erstellen, um die Produkte für das Durchsuchen auf Ihrer Microsoft Dynamics 365 Commerce Site zu organisieren.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2b6a7a3b35873e80be391c627d0397fd6398a99
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412550"
---
# <a name="customize-site-navigation"></a>Anpassen der Sitenavigation


[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie eine benutzerdefinierte Online-Navigationshierarchie erstellen, um die Produkte für das Durchsuchen auf Ihrer Microsoft Dynamics 365 Commerce Site zu organisieren.

## <a name="overview"></a>Übersicht

Online-Schaufenster ermöglichen es Debitoren, Produkte zu entdecken und zu suchen, indem sie durch Produktkategorien navigieren. Diese Funktion wird normalerweise von den Registerkarten am oberen Seitenrand oder auf einer Navigationsleiste links bereitgestellt. In Dynamics 365 Commerce können Sie die hierarchische Struktur der Kategorienavigation und der Produkte erstellen und verwalten, die in den unterschiedlichen Kategorien enthalten sind.

## <a name="create-a-channel-navigation-hierarchy"></a>Eine Kanalnavigationshierarchie erstellen

Um eine Kanalnavigationshierarchie zu erstellen, führen Sie die folgenden Schritte aus.

1. Navigieren Sie zu **Retail and Commerce \> Produkte und Kategorien \> Kategorie- und Produktverwaltung**.
1. Wählen Sie **Kategoriehierarchien** und **Neu** aus.
1. Der Name der Hierarchie.

    > [!NOTE]
    > Die oberste Kategorie, die Sie erstellen, ist der Stammkategorieknoten. Sie wird nicht auf dem Standort angezeigt. Um eine Kategoriehierarchie zu erstellen, in der ein einzelner oberste Knoten auf dem Standort angezeigt wird, erstellen und benennen Sie die Kategorie als untergeordnetes Element der Stammkategorie.

1. Wählen Sie **Neuer Kategorieknoten** und benennen Sie die Kategorie.
1. Fahren Sie fort, um gleichgeordnete und untergeordnete Kategorien nach Bedarf zu erstellen.

Sie können Produkte nun jeder Kategorie zuweisen, die Sie unter der obersten Ebene erstellt haben.

## <a name="customize-the-order-of-categories"></a>Passen Sie die Reihenfolge der Kategorien an

Standardmäßig werden die Kategorien, die Sie festlegen, in alphabetischer Reihenfolge auf der Site angezeigt. Allerdings können Sie die Anzeigereihenfolge der Kategorien auch anpassen.

## <a name="assign-a-category-hierarchy-type"></a>Zuweisen eines Kategoriehierarchietyps

1. Navigieren Sie zu **Retail and Commerce \> Produkte und Kategorien \> Kategorie- und Produktverwaltung**.
1. Wählen Sie **Kategoriehierarchien**.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte auf **Kategoriehierarchie** in der Gruppe **Einrichten** und wählen Sie **Hierarchietyp zuordnen**.
1. Wählen Sie **Neu** aus.
1. Wählen Sie im Feld **Kategoriehierarchietyp** die **Kanalnavigationshierarchie** aus.
1. Wählen Sie im Feld **Kategoriehierarchie** die Kanalnavigationshierarchie aus, die Sie eben erstellt haben.

## <a name="publish-new-or-updated-navigation-hierarchies"></a>Veröffentlichen Sie die neuen oder aktualisierten Navigationshierarchien

Um Ihre Navigationshierarchie im Online Schaufenster verfügbar zu machen, folgen Sie diesen Schritten.

1. Wählen Sie **Retail and Commerce \> Kanaleinstellung \> Kanalkategorien und Produktattribute**.
1. In der Struktur auf der linken Seite wählen Sie den Onlineshop aus.
1. Wählen Sie **Kanalupdates veröffentlichen**.
1. Gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**.
1. Wählen Sie **Job 1040** suchen und auswählen.
1. Wählen Sie **Jetzt ausführen** aus.
1. Wiederholen Sie die Schritte 5 und 6 für Job 1070 und 1150.

## <a name="show-categories-on-your-site"></a>Anzeigen der Kategorien auf der Site

Um Ihre Kategoriehierarchie in Ihrem Online-Schaufenster anzuzeigen, müssen Sie das Navigationsmenümodul am geeigneten Speicherort in einer Vorlage oder Fragment hinzufügen. Das Navigationsmenümodul wird dann in der Navigationshierarchie angezeigt, vorausgesetzt, die Navigationshierarchie wurde im Kanal veröffentlicht, mit dem Ihre Site verbunden ist.

> [!NOTE]
> Mit dem Navigationsmenümodul, das in der Modulbibliothek enthalten ist, können Benutzer nur zu Kategorien navigieren, die keine Unterkategorien umfassen. Wenn Ihre Debitoren nicht in der Lage sind, zu der Kategorien zu navigieren, die Unterkategorien umfassen, müssen Sie das Navigationsmenümodul anpassen.

## <a name="add-custom-navigation-options"></a>Fügen Sie benutzerdefinierte Navigationsoptionen hinzu

Auf dem Navigationsmenü können Sie Navigationsoptionen hinzufügen, die nicht Teil der Hierarchie Ihrer Produktkategorie sind. Zum Beispiel am Ende der Liste der Produktkategorien können Sie ein Element **Kontaktieren Sie uns** hinzufügen, das auf die Kontaktseite verweist, die Sie für Ihren Standort erstellt haben.

Um benutzerdefinierte Navigationsoptionen Ihrem Navigationsmenü hinzuzufügen, führen Sie die folgenden Schritte aus.

1. In der Vorlage oder im Fragment, das Sie anpassen möchten, wählen Sie das Navigationsmenümodul aus.
1. Im Eigenschaftenbereich auf der Registerkarte **Daten**, wählen Sie **Artikel hinzufügen**, um einen neuen Navigationsartikel des Content Management-Systems (CMS) zu erstellen.
1. Geben Sie Hyperlinktext und eine URL ein.
1. Wiederholen Sie die Schritte 2 und 3, um kundenspezifischere Navigationsoptionen hinzuzufügen.
1. Wenn Sie fertig sind, wählen Sie **Speichern**, um die Vorlage oder das Fragment zu speichern, und wählen Sie dann **Bearbeitung beenden**, um diese einzuchecken.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über Vorlagen und Layouts](templates-layouts-overview.md)

[Arbeiten mit Vorlagen](work-with-templates.md)

[Arbeiten mit Voreinstellungslayouts](work-with-layouts.md)

[Arbeiten mit Fragmenten](work-with-fragments.md)

[Arbeiten mit Modulen](work-with-modules.md)

[Erstellen einer Seiten-URL](create-page-url.md)

[Arbeiten mit Veröffentlichungsgruppen](publish-groups.md)
