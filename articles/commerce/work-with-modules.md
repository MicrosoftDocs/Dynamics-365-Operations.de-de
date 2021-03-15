---
title: Arbeiten mit Modulen
description: In diesem Thema wird beschrieben, wie und wann Module in Microsoft Dynamics 365 Commerce verwendet werden.
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 89d95814e892e3afcb6514ab0d0219f7b08b9c63
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000458"
---
# <a name="work-with-modules"></a>Arbeiten mit Modulen

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie und wann Module in Microsoft Dynamics 365 Commerce verwendet werden.

## <a name="overview"></a>Übersicht

Module sind logische Bausteine, aus denen sich Ihre Seitenstruktur zusammensetzt. Sie dienen verschiedenen Zwecken und Bereichen. Einige Module sind übergeordnete Container, und ihr einziger Zweck besteht darin, andere Module (untergeordnete Module) zu speichern und zu organisieren. Andere Module, z. B. ein einfaches Bildplatzierungsmodul, haben einen ganz bestimmten Zweck. Weitere Module, z. B. ein Karussellmodul, lassen sich irgendwo zwischen diesen beiden Kategorien einordnen.

Standardmäßig enthält Ihre Dynamics 365 Commerce-Site eine Modulbibliothek, mit der Sie die grundlegendsten E-Commerce-Szenarien erstellen können. Sie sollten in der Lage sein, eine End-to-End-E-Commerce-Site zu erstellen, indem Sie diese Module verwenden. Sie können diese Module jedoch auch anpassen oder neue, benutzerdefinierte Module für bestimmte Anforderungen erstellen. Wenn Sie benutzerdefinierte Module erstellen möchten, steht ein SDK (Module Design Software Development Kit) zur Verfügung, mit dem Sie eine benutzerdefinierte Modulbibliothek erstellen können.

## <a name="container-modules-and-slots"></a>Containermodule und -Slots

Wie bereits erwähnt, enthalten einige Module untergeordnete Module. Diese Module sind als *Container* bekannt und sie ermöglichen Hierarchien geschachtelter Module. Containermodule enthalten *Slots*. Slots werden verwendet, um das Layout und den Zweck von untergeordneten Modulen im Container zu verwalten. Ein Beispiel ist ein grundlegendes Seitencontainermodul (ein übergeordnetes Modul für jede Seite), das mehrere wichtige Slots definiert:

- Ein Kopfzeilen-Slot
- Ein Unterkopfzeilen-Slot
- Ein Haupt-Slot
- Ein Fußzeilen-Slot
- Ein Unterfußzeilen-Slot

Der Modulentwickler definiert diese Slots und legt fest, welche untergeordneten Module und wie viele untergeordnete Module direkt darin platziert werden können. Beispielsweise unterstützt der Kopfzeilen-Slot möglicherweise nur einen Typ des **Kopfzeilen-Moduls**, wohingegen der Text-Slot eine unbegrenzte Anzahl an Modulen jedes Typs unterstützt (mit Ausnahme andere Seitencontainermodule).

In den Erstellungstools müssen Seitenautoren nicht im Voraus wissen, welche Module in die einzelnen Slots eingefügt werden können und welche nicht. Wenn Seitenautoren einen Slot auswählen und dann versuchen, ein Modul zum Hinzufügen auszuwählen, wird eine gefilterte Ansicht der Modultypen angezeigt, die für diesen Slot unterstützt werden.

## <a name="content-modules"></a>Inhaltsmodule

Inhaltsmodule enthalten Inhalts- und Medienelemente wie Text (z. B. Überschriften, Absätze und Links) oder Ressourcenverweise (z. B. Bilder, Videos und PDFs). Typische Inhaltsmodultypen umfassen Inhaltsblock-, Textblock- und Promobannermodule. Module dieser drei Typen können Text oder Medien enthalten und erfordern keine untergeordneten Module, um etwas auf einer Seite sichtbar zu machen.

Die Mehrzahl der typischen täglichen Seiten- und Inhaltserstellungsaktivitäten umfasst Inhaltsmodule, hauptsächlich weil diese Module den tatsächlichen Inhalt definieren, der in ihren übergeordneten Containermodulen gerendert wird. Es sind viele Inhaltsmodule verfügbar, und diese Module sind normalerweise die letzten Elemente, die Sie der Hierarchie der verschachtelten Module einer Seite hinzufügen.

Die folgende Abbildung zeigt, wie Module in übergeordneten Containermodul-Slots verschachtelt sind.

![Verschachteln von Modulen](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Module hinzufügen oder entfernen

Die folgenden Prozeduren beschreiben das Hinzufügen und Entfernen von Modulen.

### <a name="add-a-module"></a>Ein Modul hinzufügen

Gehen Sie folgendermaßen vor, um ein Modul aus einem Slot oder Container auf einer Seite hinzuzufügen.

1. Wählen Sie im Gliederungsbereich links oder direkt auf der Haupt-Canvas einen Container oder Slot aus, zu dem ein untergeordnetes Modul hinzugefügt werden kann.

    > [!NOTE]
    > Der Moduldesigner definiert die Liste der Modultypen, die einem bestimmten Modul-Slot hinzugefügt werden können. Vorlagenautoren können dann die zulässigen Moduloptionen verfeinern, um eine konsistente Suchmaschinenoptimierung (SEO) und Autoreneffizienz für alle Seiten sicherzustellen, die aus einer bestimmten Vorlage erstellt wurden. Wenn Sie einem Slot ein Modul hinzufügen, wird das Dialogfeld **Modul hinzufügen** automatisch gefiltert, sodass nur Module angezeigt werden, die im ausgewählten Container oder Slot unterstützt werden. Die Liste der zulässigen Module wird durch die Seitenvorlage oder die Containermoduldefinition bestimmt.

1. Wenn Sie den Gliederungsbereich verwenden, wählen Sie die Auslassungspunkte (**...**) neben dem Modulnamen und dann **Modul hinzufügen** aus. Wenn Sie die Steuerelemente direkt auf der Canvas verwenden, wählen Sie das Pluszeichen (**+**) in einem leeren Slot oder neben dem aktuell ausgewählten Modul und dann **Modul hinzufügen** aus.

    > [!NOTE]
    > Wenn der Container oder Slot keine neuen untergeordneten Module unterstützt, ist die Option **Modul hinzufügen** nicht verfügbar.

1. Wählen Sie im Dialogfeld **Modul hinzufügen** ein Modul aus, um es Ihrer Seite hinzuzufügen.

    > [!TIP]
    > **Inhaltsblock** ist ein guter Modultyp für Anfänger.

1. Wählen Sie **OK** aus, um das ausgewählte Modul dem ausgewählten Container oder Slot auf Ihrer Seite hinzuzufügen.

### <a name="remove-a-module"></a>Ein Modul entfernen

Gehen Sie folgendermaßen vor, um ein Moduls aus einem Slot oder Container auf einer Seite zu entfernen.

1. Wählen Sie links im Gliederungsbereich die Auslassungspunkte (**...**) neben dem Namen des zu entfernenden Moduls und anschließend das Papierkorbsymbol aus. Alternativ können Sie auf der Haupt-Canvas das Papierkorbsymbol in der Symbolleiste eines ausgewählten Moduls auswählen.
1. Wenn Sie aufgefordert werden, das Entfernen des Moduls zu bestätigen, wählen Sie **OK** aus.

## <a name="move-a-module-to-a-new-position"></a>Ein Modul an eine neue Position verschieben

Verwenden Sie eine der folgenden Methoden, um ein Modul an eine neue Position auf Ihrer Seite zu verschieben.

### <a name="move-a-module-using-the-outline-pane"></a>Ein Modul mithilfe des Gliederungsbereichs verschieben

Führen Sie die folgenden Schritte aus, um ein Modul mithilfe des Gliederungsbereichs zu verschieben.

1. Wählen und halten Sie das Modul, das Sie verschieben möchten, im Gliederungsbereich, und ziehen Sie das Modul an eine neue Position in der Gliederung. Die blaue Linie in der Gliederung und auf der Canvas zeigt an, wo das Modul platziert werden kann.
1. Lassen Sie das Modul los, um es in der neuen Position abzulegen.

### <a name="move-a-module-directly-within-the-canvas"></a>Ein Modul direkt auf der Canvas verschieben

Führen Sie die folgenden Schritte aus, um ein Modul direkt auf der Canvas zu verschieben.

1. Wählen Sie das Modul aus, das Sie auf der Canvas verschieben möchten. 
1. Wählen Sie in der Symbolleiste des Moduls entweder ein nach oben oder nach unten zeigendes Pfeilsymbol aus, und ziehen Sie den Pfeil an eine neue Position auf der Seite. Die blaue Linie auf der Canvas und in der Gliederung zeigt an, wo das Modul platziert werden kann. Wenn ein Modul nicht nach oben oder unten verschoben werden kann, ist dieses Pfeilsymbol ausgegraut. 
1. Lassen Sie das Modul los, um es in der neuen Position abzulegen.

### <a name="move-a-module-using-the-ellipsis-menu"></a>Ein Modul mithilfe des Auslassungsmenüs verschieben

Führen Sie die folgenden Schritte aus, um ein Modul mithilfe des Auslassungsmenüs zu verschieben.

1. Wählen Sie ein Modul entweder in der Gliederung oder auf der Canvas aus.
1. Wählen Sie die Auslassungspunkte (**...**) neben dem Namen des Moduls im Gliederungsbereich oder in der Symbolleiste des ausgewählten Moduls auf der Canvas aus.
1. Wenn das Modul innerhalb des Containers oder Slots nach oben oder unten verschoben werden kann, werden Optionen für **Nach oben** oder **Nach unten** angezeigt. Wählen Sie die gewünschte Verschiebungsoption aus, um das Modul relativ zu seinen gleichgeordneten Elementen nach oben oder unten zu verschieben.

## <a name="configure-modules"></a>Module konfigurieren

In den folgenden Prozeduren wird beschrieben, wie Sie Inhalts- und Containermodule konfigurieren.

### <a name="configure-a-content-module"></a>Ein Inhaltsmodul konfigurieren

Um ein Inhaltsmodul auf einer Seite zu konfigurieren, befolgen Sie diese Schritte.

1. Erweitern Sie die Baumstruktur im Gliederungsbereich links, und wählen Sie einen beliebigen Inhaltsmodultyp (z. B. **Inhaltsblock**) aus. Alternativ können Sie das Modul auf der Haupt-Canvas auswählen.
1. Geben Sie im Moduleigenschaftsbereich auf der rechten Seite Eigenschaften für alle gewünschten Modulsteuerelemente ein.
1. Wählen Sie in der Befehlsleiste **Speichern** aus. Dadurch wird auch der Vorschau-Canvas aktualisiert.

### <a name="edit-module-text-properties"></a>Modultexteigenschaften bearbeiten

Modultexteigenschaften, die nicht schreibgeschützt sind, können direkt auf der Canvas bearbeitet werden.

Führen Sie die folgenden Schritte aus, um die Modultexteigenschaften zu bearbeiten.

1. Wählen Sie das Textsteuerelement auf der Canvas aus, und platzieren Sie den Cursor an der Stelle, an der Sie Text bearbeiten möchten.
1. Geben Sie Ihren Textinhalt ein.
1. Wählen Sie eine beliebige Stelle außerhalb des Textinhalts aus, um weitere Inhalte zu bearbeiten.

### <a name="inline-image-selection"></a>Inline-Bildauswahl

Modulbilder, die nicht schreibgeschützt sind, können direkt über die Canvas geändert werden.

Führen Sie die folgenden Schritte aus, um ein neues Bild für ein Inhaltsmodul auszuwählen.

1. Doppelklicken Sie auf der Canvas auf das Bild. Dadurch wird das Medienauswahlfenster geöffnet.
1. Suchen Sie ein neues Bild, das Sie verwenden möchten, und wählen Sie es aus. Wählen Sie dann **OK** aus. Das neue Bild wird jetzt auf der Canvas gerendert.

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]