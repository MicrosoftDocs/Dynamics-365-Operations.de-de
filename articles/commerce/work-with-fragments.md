---
title: Arbeiten mit Fragmenten
description: In diesem Thema wird beschrieben, warum, wann und wie Fragmente in Microsoft Dynamics 365 Commerce verwendet werden.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d92b9077f8584bfa0710bbaacbc7caa3220baa4a
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698095"
---
# <a name="work-with-fragments"></a>Arbeiten mit Fragmenten 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, warum, wann und wie Fragmente in Microsoft Dynamics 365 Commerce verwendet werden.

## <a name="overview"></a>Übersicht

Fragmente ermöglichen ein zentrales Authoring für Modulkonfigurationen, die auf Ihrer Website wiederverwendet werden müssen. Beispielsweise werden Kopf- und Fußzeilen sowie Banner häufig als Fragmente konfiguriert, da sie auf mehreren Seiten gemeinsam genutzt werden. Sie können sich Fragmente als Miniaturwebseiten vorstellen, die in andere Seiten Ihrer Site eingefügt werden können. Fragmente haben ihren eigenen Lebenszyklus. Mit anderen Worten, sie werden als unabhängige Entitäten in den Authoring-Tools erstellt, referenziert, aktualisiert und gelöscht.

Nachdem Fragmente konfiguriert wurden, können sie überall dort verwendet werden, wo Module in Ihrer Site-Struktur verwendet werden können. Fragmente können auf Seiten, in Layouts, in Vorlagen und in anderen Fragmenten referenziert werden.

> [!NOTE]
> Fragmente können bis zu sieben Ebenen tief in anderen Fragmenten verschachtelt werden.

Wenn Sie beispielsweise eine saisonale Veranstaltung über mehrere Seiten auf unserer Website bewerben möchten, können Sie ein Fragment verwenden. Der erste Schritt beim Erstellen eines neuen Fragments ist die Auswahl des Modultyps, von dem aus Sie beginnen möchten. In diesem Beispiel können Sie das Fragment aus einem Hero-Modul erstellen.

> [!NOTE]
> Fragmente können aus jedem Modultyp erstellt werden.

Sie können dann das Hero-Fragment mit Ihrem spezifischen Werbeinhalt konfigurieren. Sie können es auch nach Bedarf lokalisieren. Das neue eigenständige Hero-Fragment kann dann als vorkonfiguriertes Modul auf Ihrer Website verwendet werden. Sie können es einfach Vorlagen, bestimmten Seiten oder anderen Fragmenten hinzufügen, die Hero-Module enthalten können.

Alle Stellen, an denen das Fragment hinzugefügt wird, verweisen auf das von Ihnen erstellte zentrale Hero-Fragment. Wenn Sie Änderungen am Fragment veröffentlichen, wirken sich diese Änderungen sofort auf alle Stellen aus, auf die das Fragment auf der Site verweist. Daher bieten Fragmente eine leistungsstarke und effiziente Möglichkeit, Modulkonfigurationen auf einer Site wiederzuverwenden und zentral zu verwalten. Indem Sie sie effektiv einsetzen, können Sie die Flexibilität erheblich steigern und die Kosten für die Verwaltung des Websiteinhalts senken.

Die folgende Abbildung zeigt, wie Fragmente verwendet werden können, um das Authoring gemeinsam genutzter Modulkonfigurationen auf einer E-Commerce-Site zu zentralisieren.

![Eine Abbildung, die zeigt, wie Fragmente zum Zentralisieren des Erstellens gemeinsam genutzter Modulkonfigurationen auf einer E-Commerce-Site verwendet werden können](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Fragment erstellen

Sie können entweder ein neues Fragment erstellen oder eine vorhandene Modulkonfiguration als Fragment speichern.

### <a name="create-a-new-fragment"></a>Ein neues Fragment erstellen

Um ein neues Fragment zu erstellen, befolgen Sie diese Schritte.

1. Wählen Sie im linken Navigationsbereich **Fragmente** aus.
1. Wählen Sie **Neues Seitenfragment** aus. Ein Dialogfeld mit allen verfügbaren Modultypen wird angezeigt. Wie bereits erwähnt, können Fragmente aus jedem Modultyp erstellt werden.
1. Wählen Sie einen Modultyp für Ihr Fragment und dann **OK** aus.

    > [!TIP]
    > Durch Auswahl eines generischen Containermodultyps erhalten Sie die größte Flexibilität, wenn Sie Ihr Fragment später aktualisieren und konfigurieren müssen.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Speichern einer vorhandenen Modulkonfiguration als Fragment

Gehen Sie folgendermaßen vor, um ein zuvor konfiguriertes Modul in ein wiederverwendbares Fragment zu konvertieren.

1. Öffnen Sie eine Seite oder Vorlage, die das Modul enthält, das Sie in ein Fragment konvertieren möchten.
1. Wählen Sie im Gliederungsbereich links die Ellipsen-Schaltfläche (**...**) neben dem Namen des Moduls und dann **Als Fragment speichern** aus. Ein Dialogfeld wird angezeigt.
1. Geben Sie einen Namen und Metadaten für das Fragment ein.
1. Wählen Sie **OK** aus, um die Modulkonfiguration als Fragment zu speichern, das anderen Seiten hinzugefügt werden kann.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Hinzufügen, Entfernen oder Bearbeiten von Fragmenten auf einer Seite

Die folgenden Prozeduren beschreiben das Hinzufügen, Entfernen und Bearbeiten von Fragmenten.

### <a name="add-a-fragment"></a>Fragment hinzufügen

Gehen Sie folgendermaßen vor, um einer Seite ein Fragment hinzuzufügen.

1. Wählen Sie links im Gliederungsfenster einen Container oder Steckplatz aus, zu dem untergeordnete Module hinzugefügt werden können.
1. Wählen Sie die Ellipsen-Schaltfläche neben dem Namen des Containers oder Slots und dann **Fragment hinzufügen** aus. Ein Dialogfeld wird angezeigt.

    > [!NOTE]
    > Wenn der Container oder Slot keine neuen untergeordneten Module unterstützt, ist die Option **Fragment hinzufügen** nicht verfügbar.

1. Suchen Sie im Dialogfeld nach einem Fragment, das Sie hinzufügen möchten, und wählen Sie es aus. Wenn keine verfügbaren Fragmente aufgelistet sind, müssen Sie möglicherweise zuerst ein Fragment aus einem Modultyp erstellen, den der ausgewählte Container oder Slot unterstützt.
1. Wählen Sie **OK** aus, um das ausgewählte Fragment dem ausgewählten Container oder Slot auf Ihrer Seite hinzuzufügen.

> [!NOTE]
> Die Module, die in einem Container oder Slot zulässig sind, werden durch die Seitenvorlage oder die eigenen Definitionen der Module definiert.

### <a name="remove-a-fragment"></a>Ein Fragment entfernen

Gehen Sie folgendermaßen vor, um ein Fragment aus einem Slot oder Container auf einer Seite zu entfernen.

1. Wählen Sie links im Gliederungsbereich die Schaltfläche mit den Auslassungspunkten neben dem Namen des zu entfernenden Fragments und anschließend die Schaltfläche mit dem Papierkorb.
1. Wenn Sie aufgefordert werden, das Entfernen des Fragments zu bestätigen, wählen Sie **OK** aus.

> [!NOTE]
> Wenn Sie ein Fragment von einer Seite entfernen, entfernen Sie einfach den Verweis darauf von dieser Seite. Sie löschen das Fragment **nicht** von Ihrer Site. Um Fragmente von Ihrer Site zu löschen, müssen Sie die Benutzeroberfläche des Fragmentinspektors verwenden. Sie können Fragmente nur dann von einer Site löschen, wenn derzeit keine Seiten, Vorlagen oder anderen Fragmente auf sie verweisen.

### <a name="edit-a-fragment"></a>Fragment bearbeiten

Um Fragmente zu bearbeiten, müssen Sie die Benutzeroberfläche des Fragmenteditors verwenden. Diese Beschränkung ist beabsichtigt. Es hilft, sicherzustellen, dass Autoren den Prozess der Bearbeitung der Module für eine bestimmte Seite nicht mit dem Prozess der Bearbeitung von Fragmenten verwechseln, die möglicherweise auf mehreren Seiten geteilt werden.

Um ein neues Fragment zu bearbeiten, befolgen Sie diese Schritte.

1. Wählen Sie im linken Navigationsbereich **Fragmente** aus.
1. Wählen Sie unter **Fragmente** das zu bearbeitende Fragment aus.
1. Bearbeiten Sie die Moduleigenschaften und die Struktur des Fragments nach Bedarf. Der Vorgang ähnelt dem Vorgang zum Bearbeiten von Modulen, die in der Seiteneditoransicht bearbeitet werden.

Sie können ein Fragment auch bearbeiten, indem Sie es auf einer Seite, in einer Vorlage oder in einem übergeordneten Fragment auswählen und dann **Fragment bearbeiten** im Eigenschaftenbereich rechts.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über Vorlagen und Layouts](templates-layouts-overview.md)

[Arbeiten mit Vorlagen](work-with-templates.md)

[Arbeiten mit Voreinstellungslayouts](work-with-layouts.md)
