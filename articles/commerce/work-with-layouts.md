---
title: Arbeiten mit Voreinstellungslayouts
description: In diesem Thema wird beschrieben, wie Sie mit vordefinierten Layouts in Microsoft Dynamics 365 Commerce arbeiten.
author: phinneyridge
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
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1f2c0638caa7e4f6f831e592e3f7e3f5ab7d1d81
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697818"
---
# <a name="work-with-preset-layouts"></a>Arbeiten mit Voreinstellungslayouts

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie mit vordefinierten Layouts in Microsoft Dynamics 365 Commerce arbeiten.

## <a name="overview"></a>Übersicht

Bevor Sie die Prozeduren in diesem Thema abschließen, lesen Sie unbedingt [Vordefinierte und benutzerdefinierte Layouts](templates-layouts-overview.md#preset-and-custom-layouts). Einen allgemeinen Überblick erhalten Sie in [Übersicht über Vorlagen und Layouts](templates-layouts-overview.md).

## <a name="create-a-new-preset-layout"></a>Ein neues vordefiniertes Layout erstellen

Es gibt zwei Methoden zum Erstellen eines vordefinierten Layouts. Sie können ein vorhandenes benutzerdefiniertes Layout als neues vordefiniertes Layout speichern oder ein vordefiniertes Layout von Grund auf neu erstellen.

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a>Erstellen eines vordefinierten Layouts aus einem vorhandenen benutzerdefinierten Layout

Gehen Sie folgendermaßen vor, um ein vordefiniertes Layout aus einem vorhandenen benutzerdefinierten Layout zu erstellen.

1. Öffnen Sie eine vorhandene Seite, die derzeit kein vordefiniertes Layout verwendet und deren Modulstruktur Sie für andere Seiten Ihrer Site wiederverwenden möchten.
1. Wählen Sie **Auschecken** aus.
1. Wählen Sie **Als neues Layout speichern** aus. Das Dialogfeld **Als neues Layout speichern** wird angezeigt.
1. Geben Sie einen Namen und eine Beschreibung für Ihr vordefiniertes Layout ein. Die von Ihnen eingegebenen Werte werden anderen Autoren angezeigt, wenn sie neue Seiten aus Ihrem Layout erstellen oder zu diesem wechseln. Geben Sie daher Werte ein, die für Seitenautoren hilfreich sind.
1. Wählen Sie **OK**.

Das vordefinierte Layout ist jetzt verfügbar, wenn Sie neue Seiten erstellen oder ein anderes Layout für eine Seite in derselben Vorlagenhierarchie auswählen.

> [!TIP]
> Um schnell festzustellen, ob eine bestimmte Seite derzeit an ein vordefiniertes Layout gebunden ist, wählen Sie die Seite in der Seitenlistenansicht aus und überprüfen Sie die Layout-Metadaten im Eigenschaftsfenster auf der rechten Seite.

### <a name="create-a-new-preset-layout"></a>Ein neues vordefiniertes Layout erstellen

Gehen Sie folgendermaßen vor, um ein vordefiniertes Layout von Grund auf neu zu erstellen.

1. Wählen Sie im linken Navigationsbereich **Layouts** aus.
1. Wählen Sie **Neues Layout** aus. Das Dialogfeld **Neues Layout** wird angezeigt.
1. Wählen Sie die Vorlage aus, die für Ihr vordefiniertes Layout verwendet werden soll.
1. Geben Sie einen Namen und eine Beschreibung für Ihr vordefiniertes Layout ein. Die von Ihnen eingegebenen Werte werden anderen Autoren angezeigt, wenn sie neue Seiten aus Ihrem Layout erstellen oder zu diesem wechseln. Geben Sie daher Werte ein, die für Seitenautoren hilfreich sind.
1. Wählen Sie **OK** aus, um das neue vordefinierte Layout zu erstellen und den Layout-Editor zu öffnen.
1. Fügen Sie im Layout-Editor Module hinzu und konfigurieren Sie sie mithilfe der Gliederungsstruktur links und des Eigenschaftsfensters rechts. (Der Vorgang ähnelt dem Vorgang zum Hinzufügen und Konfigurieren von Modulen für eine Vorlage im Vorlageneditor.) Die Anordnung der Module und die gesperrten Standardeinstellungen werden zur zentralen Modulkonfiguration für alle Seiten, die dieses vordefinierte Layout verwenden.

## <a name="modify-a-preset-layout"></a>Ändern eines vordefinierten Layouts

Führen Sie folgende Schritte aus, um ein vordefiniertes Layout zu ändern.

1. Wählen Sie im linken Navigationsbereich **Layouts** aus.
1. Wählen Sie im Layout-Editor links in der Gliederungsstruktur das zu ändernde Modul aus. Befolgen Sie dann einen dieser Schritte:

    - Um ein Modul innerhalb seines übergeordneten Moduls nach oben oder unten zu verschieben, wählen Sie die Ellipsen-Schaltfläche (**...**) für das Modul und dann **Nach oben verschieben** oder **Nach unten verschieben** aus.
    - Um die Standardeinstellungen eines Moduls zu ändern, geben Sie im Eigenschaftenbereich Standardwerte ein und sperren Sie diese optional für alle nachgeordneten Seiten.
    - Um neue Module oder Fragmente zu Containermodulen hinzuzufügen, klicken Sie auf die Ellipsen-Schaltfläche und dann auf **Modul hinzufügen** oder **Fragment hinzufügen**.
    - Um ein Modul aus dem Layout zu entfernen, wählen Sie die Ellipsen-Schaltfläche und anschließend **Löschen** aus.

## <a name="change-a-preset-layout-theme"></a>Ändern eines vordefinierten Layoutdesigns

In der Regel wird für alle Seiten, die ein vordefiniertes Layout verwenden, ein Standarddesign festgelegt.

Gehen Sie folgendermaßen vor, um das Design für alle untergeordneten Seiten festzulegen oder zu ändern, die Ihr vordefiniertes Layout verwenden.

1. Wählen Sie im Layout-Editor in der linken Gliederungsstruktur das Seitencontainer-Modul aus. (In der Regel ist dieses Modul der zweite Knoten und heißt **Standardseite**.)
1. Wählen Sie im Eigenschaftenbereich rechts im Feld **Design** ein Design aus.

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a>Speichern, Einchecken, Anzeigen einer Vorschau und Veröffentlichen eines vordefinierten Layouts

Gehen Sie folgendermaßen vor, um Ihr vordefiniertes Layout zu speichern und einzuchecken.

1. Wählen Sie **Speichern** oben im Layouteditor aus. Gespeicherte Änderungen wirken sich erst beim Einchecken auf nachfolgende Seiten aus.
1. Wählen Sie **Einchecken** aus. Ihre Änderungen sind jetzt für nachfolgende Workflows erkennbar.

Um eine Vorschau Ihrer Änderungen anzuzeigen, öffnen Sie entweder eine vorhandene Seite, die das vordefinierte Layout verwendet, oder erstellen Sie eine neue Seite aus dem Layout.

Führen Sie einen der folgenden Schritte aus, um das Layout auf Ihrer Live-Site zu veröffentlichen, nachdem Sie eine Vorschau der Änderungen an Ihrem vordefinierten Layout angezeigt haben:

* Navigieren Sie zu **Layouts**, wählen Sie das Layout und dann **Veröffentlichen** aus.
* Wählen Sie im Layout-Editor **Veröffentlichen** aus.
* Veröffentlichen Sie eine Seite, die auf das unveröffentlichte Layout verweist. Das Layout wird automatisch veröffentlicht.

> [!WARNING]
> Vordefinierte Layouts können von mehreren Seiten referenziert werden. Beachten Sie beim Veröffentlichen eines vordefinierten Layouts, dass sich dies möglicherweise auf das Layout mehrerer Seiten auswirkt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über Vorlagen und Layouts](templates-layouts-overview.md)

[Arbeiten mit Vorlagen](work-with-templates.md)
