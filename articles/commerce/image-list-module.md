---
title: Bildlistenmodul
description: Dieser Artikel behandelt Bildlistenmodule und es wird beschrieben, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8e47c9806c21de24f0e519d0132374d2e1ff2bbf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892799"
---
# <a name="image-list-module"></a>Bildlistenmodul

[!include [banner](includes/banner.md)]

Dieser Artikel behandelt Bildlistenmodule und es wird beschrieben, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Das Bildlistenmodul kann verwendet werden, um auf einfache Weise eine Sammlung (ein Array) von Bildern zu Websiteseiten hinzuzufügen. Jedes Bild im Array kann mit Absatztext und Link-URLs konfiguriert werden. Das Bildlistenmodul ist am besten geeignet, um Markenlogos oder eine Liste mit Logos anzuzeigen.

> [!IMPORTANT]
> - Das Bildlistenmodul ist in der Commerce-Modulbibliothek ab der Dynamics 365 Commerce-Version 10.0.20 verfügbar.
> - Das Bildlistenmodul wird im Adventure Works-Design vorgestellt.

Die folgende Abbildung zeigt ein Beispiel, in dem ein Bildlistenmodul eine Textliste mit Logos auf einer Business-to-Consumer-Seite (B2C) mit Adventure Works anzeigt.

![Beispiel für ein Bildlistenmodul, das eine Textliste mit Logos anzeigt](./media/Image_list.PNG)

Die folgende Abbildung zeigt ein Beispiel, in dem ein Bildlistenmodul Markenlogos auf einer Business-to-Business-Seite (B2B) mit Adventure Works anzeigt.

![Beispiel für ein Bildlistenmodul, das Markenlogos anzeigt](./media/Image_list_B2B.PNG)

## <a name="image-list-module-properties"></a>Bildlistenmodul-Eigenschaften

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Überschrift       | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Eine Textüberschrift für das Bildlistenmodul. |
| Bildliste    | Bilder, Texte und URLs | Jedes Element im Array ist ein Bild, das von Absatztext und einer URL begleitet wird. |

## <a name="add-an-image-list-module-to-a-new-page"></a>Ein Bildlistenmodul einer neuen Seite hinzufügen

Um ein Bildlistenmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften im Commerce-Website-Generator festzulegen, führen Sie die folgenden Schritte aus.

1. Gehen Sie auf **Vorlagen** und öffnen Sie die Marketingvorlage für die Homepage Ihrer Site (oder erstellen Sie eine neue Marketingvorlage).
1. Auf der Standardseite wählen Sie **Haupt**-Slot und dann die Ellipsen (**...**) und **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Bildliste** und dann **OK** aus.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Gehen Sie zu **Seiten** und öffnen Sie die Homepage der Site (oder erstellen Sie eine neue Homepage mithilfe der Marketingvorlage).
1. Auf dem Seitenüberblick wählen Sie den Slot **Haupt** und wählen die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Bildliste** und dann **OK** aus.
1. Fügen Sie im Eigenschaftenbereich für das Bildlistenmodul eine Überschrift hinzu (z. B. **Unsere Marken**).
1. Fügen Sie ein Bildlistenelement hinzu und geben Sie ein Bild, einen Absatztext und eine Umleitungs-URL an.
1. Fügen Sie nach Bedarf zusätzliche Bildlistenmodule hinzu und konfigurieren Sie sie.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Adventure Works-Design](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
