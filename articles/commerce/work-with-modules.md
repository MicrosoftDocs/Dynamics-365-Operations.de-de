---
title: Arbeiten mit Modulen
description: In diesem Thema wird beschrieben, wie und wann Module in Microsoft Dynamics 365 Commerce verwendet werden.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 769d6754fa944830b989d657e0dad9cc42212932
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025878"
---
# <a name="work-with-modules"></a>Arbeiten mit Modulen

In diesem Thema wird beschrieben, wie und wann Module in Microsoft Dynamics 365 Commerce verwendet werden.


[!include [banner](includes/banner.md)]

## <a name="overview"></a>Übersicht

Module sind logische Bausteine, aus denen sich Ihre Seitenstruktur zusammensetzt. Sie dienen verschiedenen Zwecken und Bereichen. Einige Module sind übergeordnete Container, und ihr einziger Zweck besteht darin, andere Module (untergeordnete Module) zu speichern und zu organisieren. Andere Module, z. B. ein einfaches Bildplatzierungsmodul, haben einen ganz bestimmten Zweck. Weitere Module, z. B. ein Karussellmodul, lassen sich irgendwo zwischen diesen beiden Kategorien einordnen.

Standardmäßig enthält Ihre Dynamics 365 Commerce-Site eine Starter-Kit-Modulbibliothek, mit der Sie die grundlegendsten E-Commerce-Szenarien erstellen können. Sie sollten in der Lage sein, eine End-to-End-E-Commerce-Site zu erstellen, indem Sie diese Module verwenden. Sie können diese Module jedoch auch anpassen oder neue, benutzerdefinierte Module für bestimmte Anforderungen erstellen. Wenn Sie benutzerdefinierte Module erstellen möchten, steht ein SDK (Module Design Software Development Kit) zur Verfügung, mit dem Sie eine benutzerdefinierte Modulbibliothek erstellen können.

## <a name="container-modules-and-slots"></a>Containermodule und -Slots

Wie bereits erwähnt, enthalten einige Module untergeordnete Module. Diese Module sind als *Container* bekannt und sie ermöglichen Hierarchien geschachtelter Module. Containermodule enthalten *Slots*. Slots werden verwendet, um das Layout und den Zweck von untergeordneten Modulen im Container zu verwalten. Ein Beispiel ist ein grundlegendes Seitencontainermodul (ein übergeordnetes Modul für jede Seite), das mehrere wichtige Slots definiert:

- Ein Kopfzeilen-Slot
- Ein Text-Slot
- Ein Fußzeilen-Slot

Der Modulentwickler definiert diese Slots und legt fest, welche untergeordneten Module und wie viele untergeordnete Module direkt darin platziert werden können. Beispielsweise unterstützt der Kopfzeilen-Slot möglicherweise nur einen Typ des **Kopfzeilen-Moduls**, wohingegen der Text-Slot eine unbegrenzte Anzahl an Modulen jedes Typs unterstützt (mit Ausnahme andere Seitencontainermodule).

In den Erstellungstools müssen Seitenautoren nicht im Voraus wissen, welche Module in die einzelnen Slots eingefügt werden können und welche nicht. Wenn Seitenautoren einen Slot auswählen und dann versuchen, ein Modul zum Hinzufügen auszuwählen, wird eine gefilterte Ansicht der Modultypen angezeigt, die für diesen Slot unterstützt werden.

## <a name="content-modules"></a>Inhaltsmodule

Inhaltsmodule enthalten Inhalts- und Medienelemente wie Text (z. B. Überschriften, Absätze und Links) oder Ressourcenverweise (z. B. Bilder, Videos und PDFs). Zu den Beispielen typischer Inhaltsmodultypen zählen **Hero**, **Funktion** und **Banner**. Module dieser drei Typen können Text oder Medien enthalten und erfordern keine untergeordneten Module, um etwas auf einer Seite sichtbar zu machen.

Die Mehrzahl der typischen täglichen Seiten- und Inhaltserstellungsaktivitäten umfasst Inhaltsmodule, hauptsächlich weil diese Module den tatsächlichen Inhalt definieren, der in ihren übergeordneten Containermodulen gerendert wird. Es sind viele Inhaltsmodule verfügbar, und diese Module sind normalerweise die letzten Elemente, die Sie der Hierarchie der verschachtelten Module einer Seite hinzufügen.

Die folgende Abbildung zeigt, wie Module in übergeordneten Containermodul-Slots verschachtelt sind.

![Verschachteln von Modulen](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Module hinzufügen oder entfernen

Die folgenden Prozeduren beschreiben das Hinzufügen und Entfernen von Modulen.

### <a name="add-a-module"></a>Ein Modul hinzufügen

Gehen Sie folgendermaßen vor, um ein Modul aus einem Slot oder Container auf einer Seite hinzuzufügen.

1. Wählen Sie links im Gliederungsfenster einen Container oder Slot aus, dem ein untergeordnetes Modul hinzugefügt werden kann.

    > [!NOTE]
    > Der Moduldesigner definiert die Liste der Modultypen, die einem bestimmten Modul-Slot hinzugefügt werden können. Vorlagenautoren können dann die zulässigen Moduloptionen verfeinern, um eine konsistente Suchmaschinenoptimierung (SEO) und Autoreneffizienz für alle Seiten sicherzustellen, die aus einer bestimmten Vorlage erstellt wurden.

1. Wählen Sie die Ellipsen-Schaltfläche (**...**) für das Modul aus und dann **Modul hinzufügen**. Das Dialogfeld **Modul hinzufügen** wird angezeigt. Dieses Dialogfeld wird automatisch gefiltert, sodass nur Module angezeigt werden, die im ausgewählten Container oder Slot unterstützt werden. Die Liste der Module wird durch die Seitenvorlage oder die Containermoduldefinition bestimmt.

    > [!NOTE]
    > Wenn der Container oder Slot keine neuen untergeordneten Module unterstützt, ist die Option **Modul hinzufügen** nicht verfügbar.

1. Suchen Sie im Dialogfeld nach einem Modul und wählen Sie es aus, um es Ihrer Seite hinzuzufügen.

    > [!TIP]
    > **Funktion** und **Hero** sind hilfreiche Modultypen, mit denen Anfänger arbeiten können.

1. Wählen Sie **OK** aus, um das ausgewählte Modul dem ausgewählten Container oder Slot auf Ihrer Seite hinzuzufügen.

### <a name="remove-a-module"></a>Ein Modul entfernen

Gehen Sie folgendermaßen vor, um ein Moduls aus einem Slot oder Container auf einer Seite zu entfernen.

1. Wählen Sie links im Gliederungsbereich die Schaltfläche mit den Auslassungspunkten neben dem Namen des zu entfernenden Moduls und anschließend die Schaltfläche mit dem Papierkorb.
1. Wenn Sie aufgefordert werden, das Entfernen des Moduls zu bestätigen, wählen Sie **OK** aus.

## <a name="configure-modules"></a>Module konfigurieren

In den folgenden Prozeduren wird beschrieben, wie Sie Inhalts- und Containermodule konfigurieren.

### <a name="configure-a-content-module"></a>Ein Inhaltsmodul konfigurieren

Um ein Inhaltsmodul auf einer Seite zu konfigurieren, befolgen Sie diese Schritte.

1. Erweitern Sie die Baumstruktur im Gliederungsbereich links und wählen Sie einen beliebigen Inhaltsmodultyp (z. B. **Funktion**, **Hero** oder **Banner**) aus.
1. Suchen Sie im Eigenschaftenbereich rechts die Steuerelemente für Inhalt und Einstellungen des Moduls.
1. Geben Sie Eigenschaften für die gewünschten Modulsteuerelemente ein.
1. Wählen Sie in der Befehlsleiste **Sichern** aus. Dadurch wird auch der Vorschau-Canvas aktualisiert.

### <a name="configure-a-container-module"></a>Ein Containermodul konfigurieren

Um ein Containermodul auf einer Seite zu konfigurieren, befolgen Sie diese Schritte.

1. Wählen Sie ein Containermodul auf Ihrer Seite aus (z. B. ein Karussell oder ein flüssiges Containermodul).
1. Erweitern Sie im Eigenschaftenbereich rechts die verschachtelten Steuerelemente, indem Sie die Überschriften auswählen, und legen Sie die erforderlichen Steuerelementwerte fest.
1. Wählen Sie links im Gliederungsbereich die Schaltfläche mit den Auslassungspunkten neben dem Namen des Containers oder von Slots im Container und dann **Modul hinzufügen** aus. Fügen Sie dann dem ausgewählten Container untergeordnete Module hinzu. Weitere Informationen erhalten Sie im Abschnitt [Mit Modulen arbeiten](#add-a-module) am Anfang dieses Themas.
1. Wenn mehrere untergeordnete Module als gleichgeordnete Elemente in einem übergeordneten Container vorhanden sind, können Sie deren Anzeigereihenfolge im übergeordneten Container ändern. Wählen Sie die Auslassungsschaltfläche für ein Modul aus und verwenden Sie dann die Aufwärts- und Abwärtspfeiltasten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über Vorlagen und Layouts](templates-layouts-overview.md)

[Arbeiten mit Vorlagen](work-with-templates.md)

[Arbeiten mit Voreinstellungslayouts](work-with-layouts.md)

[Arbeiten mit Fragmenten](work-with-fragments.md)

[Ein Containermodul einer neuen Seite hinzufügen](add-container-module.md)

[Arbeiten mit Veröffentlichungsgruppen](publish-groups.md)

