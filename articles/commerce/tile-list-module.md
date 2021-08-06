---
title: Kachellistenmodul
description: Dieses Thema behandelt Kachellistenmodule und es wird beschrieben, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.openlocfilehash: 10bf7139ba89f5089d288e78fab9e3d63249aac9
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638903"
---
# <a name="tile-list-module"></a>Kachellistenmodul

[!include [banner](includes/banner.md)]

Dieses Thema behandelt Kachellistenmodule und es wird beschrieben, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Ein Kachellistenmodul ist eine Sammlung von Kacheln in einem Karussell. Es wird verwendet, um Produktkategorien oder Produktmarken durch Bilder und Text zu vermarkten. Ein Einzelhändler kann beispielsweise der Homepage einer E-Commerce-Site ein Kachellistenmodul hinzufügen, um alle umsatzstärksten Kategorien zu bewerben.

Ein Kachellistenmodul wird durch Daten des Content Management-Systems (CMS) gesteuert. Es hängt nicht von anderen Modulen oder Daten aus der Commerce-Zentralverwaltung ab. Das Kachellistenmodul kann auf jeder Seite der Website hinzugefügt werden, auf der ein Einzelhändler etwas vermarkten oder bewerben möchte (z. B. Produkte, Kategorien oder Marken).

Die folgende Abbildung zeigt ein Beispiel für ein Kachellistenmodul und Kachelmodule auf der Adventure Works-Homepage.

![Beispiel für ein Kachellistenmodul und Kachelmodule auf der Adventure Works-Homepage](./media/Tile_list.PNG)

> [!IMPORTANT]
> Das Kachellistenmodul ist ab der Dynamics 365 Commerce-Version 10.0.20 verfügbar.
> Das Kachellistenmodul wird im Adventure Works-Design vorgestellt.

## <a name="tile-list-modules-and-themes"></a>Kachellistenmodule und -designs

Das Kachellistenmodul kann vielfältige Layouts und Stile basierend auf einem Design unterstützen. Im Adventure Works-Design zeigen Kacheln beispielsweise einen Animationseffekt, wenn Site-Benutzer den Mauszeiger darüber bewegen. Jedes Design kann zusätzliche Eigenschaften für die Kachellisten- und Kachelmodule enthalten. Designentwickler können auch weitere Layouts in die Kachellisten- und Kachelmodule einbauen.

## <a name="tile-list-module-properties"></a>Kachellistenmodul-Eigenschaften

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Überschrift       | Überschriftentext und Überschriftsmarkierung | Eine Textüberschrift für das Kachellistenmodul. |

## <a name="tile-module-properties"></a>Kachelmoduleigenschaften

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Bild         | Bilddatei | Ein Bild kann verwendet werden, um ein Produkt oder eine Kategorie vorzustellen. Das Bild kann in die Medienbibliothek im Commerce-Site-Builder hochgeladen oder es kann ein vorhandenes Bild verwendet werden. |
| Überschrift       | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Standardmäßig wird für die Überschrift die **H2**-Überschriftsmarkierung verwendet, aber die Markierung kann nach Bedarf geändert werden, um die Zugangsanforderungen zu erfüllen. |
| Absatz     | Absatztext | Das Modul unterstützt Absatztext im Rich-Text-Format. Einige grundlegende Rich-Text-Funktionen werden unterstützt, wie Hyperlinks, fett und kursiv formatierte sowie unterstrichene Texte. Einige dieser Funktionen können vom Seitenthema überschrieben werden, das im Modul verwendet wird. |
| Verknüpfung          | Verknüpfen Sie Text, Link-URL, umfangreiche Internet-Anwendungs (ARIA)- Beschriftung und **Öffnen Sie die Verknüpfung in einer neuen Registerkarte** | Module unterstützen mindestens einen oder mehrere „Handlungsaufruf“-Links. Wenn ein Link hinzugefügt wird, sind der Linktext, eine URL und eine ARIA-Beschriftung erforderlich. ARIA-Beschriftungen sollen beschreibend sein, um Barrierefreiheitsbedingungen zu erfüllen. Links können konfiguriert werden, sodass sie auf einer neuen Registerkarte geöffnet werden. |
| Kachellink     | Link-Text, Link-URL, ARIA-Beschriftung und Auswahl **Link in neuer Registerkarte öffnen** | Diese Eigenschaft wird verwendet, um einen „Handlungsaufrufs“-Link festzulegen. Wenn ein Link hinzugefügt wird, sind der Linktext, eine URL und eine ARIA-Beschriftung erforderlich. ARIA-Beschriftungen sollen beschreibend sein, um Barrierefreiheitsbedingungen zu erfüllen. Links können konfiguriert werden, sodass sie auf einer neuen Registerkarte geöffnet werden.|
| Symbol          | Bild | Neben einem Produkt- oder Kategoriebild kann ein Symbol hinzugefügt werden. Das Symbolbild wird über dem Produkt- oder Kategoriebild angezeigt. |

## <a name="add-a-tile-list-module-to-a-new-page"></a>Ein Kachellistenmodul einer neuen Seite hinzufügen

Um ein Kachellistenmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Gehen Sie auf **Vorlagen** und öffnen Sie die Marketingvorlage für die Homepage Ihrer Site (oder erstellen Sie eine neue Marketingvorlage).
1. Auf der Standardseite wählen Sie **Haupt**-Slot und dann die Ellipsen (**...**) und **Modul hinzufügen**.
1. Im Dialogfeld **Modul hinzufügen** wählen Sie das **Kachellisten**-Modul und dann **OK** aus.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Gehen Sie zu **Seiten** und öffnen Sie die Homepage der Site (oder erstellen Sie eine neue Homepage mithilfe der Marketingvorlage).
1. Auf dem Seitenüberblick wählen Sie den **Haupt**-Slot und wählen die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Im Dialogfeld **Modul hinzufügen** wählen Sie das **Kachellisten**-Modul und dann **OK** aus.
1. Fügen Sie im Eigenschaftenbereich für das Kachellistenmodul eine Überschrift hinzu.
1. Wählen Sie im Slot **Kachelliste** das Ellipsen-Symbol (**...**) und dann **Modul hinzufügen** aus.
1. Im Dialogfeld **Modul hinzufügen** wählen Sie das **Kachelmodul** und dann **OK** aus.
1. Fügen Sie im Eigenschaftenbereich des Kachelmoduls ein Bild, eine Überschrift und ein Symbolbild hinzu.
1. Fügen Sie nach Bedarf zusätzliche Kachelmodule hinzu und konfigurieren Sie sie.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Adventure Works-Design](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
