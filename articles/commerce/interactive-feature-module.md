---
title: Interaktives Funktionsmodul
description: Dieses Thema enthält interaktive Funktionsmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
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
ms.openlocfilehash: 5b18a29ce43e69ec0578602535f21e52388fe3d04ac14673bbdefed9ec8ea161
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749849"
---
# <a name="interactive-feature-module"></a>Interaktives Funktionsmodul

[!include [banner](includes/banner.md)]

Dieses Thema enthält interaktive Funktionsmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Interaktive Funktionsmodule sind mosaikartige Module, die verwendet werden können, um mehrere Produktkategorien oder Produktmarken zu vermarkten, indem eine Kombination aus Bildern und Text verwendet wird. Ein Einzelhändler kann beispielsweise der Homepage einer E-Commerce-Site ein interaktives Funktionsmodul hinzufügen, um alle umsatzstärksten Kategorien zu bewerben. Das interaktive Funktionsmodul ähnelt dem Kachellistenmodul, hat jedoch ein anderes Layout und eine andere Interaktionsfunktionalität.

Jedes interaktive Funktionsmodul ist eine Sammlung interaktiver Funktionselementmodulen. Jedes Funktionselementmodul wird durch Daten des Content Management-System (CMS) gesteuert. Es hängt nicht von anderen Modulen oder Daten aus der Commerce-Zentralverwaltung ab. Das interaktive Kachellistenmodul kann auf jeder Seite der Website hinzugefügt werden, auf der ein Einzelhändler etwas vermarkten oder bewerben möchte (z. B. Produkte, Kategorien oder Marken).

> [!IMPORTANT]
> - Das interaktive Funktionsmodul ist ab der Version 10.0.20 von Dynamics 365 Commerce verfügbar.
> - Das interaktive Funktionsmodul wird im Adventure Works-Design vorgestellt.

Die folgende Abbildung zeigt ein Beispiel für ein interaktives Funktionsmodul auf der Adventure Works-Homepage.

![Beispiel für ein interaktives Funktionsmodul auf der Adventure Works-Homepage](./media/Feature.PNG)

## <a name="interactive-feature-module-and-themes"></a>Interaktives Funktionsmodul und Designs

Das interaktive Funktionsmodul kann vielfältige Layouts und Stile basierend auf einem Design unterstützen. Im Adventure Works-Design verfügt das interaktive Funktionsmodul beispielsweise über ein zweispaltiges Layout, das Animationseffekte anzeigt, wenn ein Websitebenutzer den Mauszeiger über die einzelnen Elemente bewegt. Das interaktive Funktionsmodul ist für eine gerade Anzahl von Bildern optimiert, die in einem zweispaltigen Layout angeordnet sind.

## <a name="interactive-feature-module-properties"></a>Eigenschaften des interaktiven Funktionsmoduls

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Überschrift       | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Eine Textüberschrift für das interaktive Funktionsmodul. |

## <a name="interactive-feature-item-module-properties"></a>Eigenschaften des interaktiven Funktionselementmoduls

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Bild         | Bilddatei | Ein Bild, das ein Produkt oder eine Kategorie darstellt. Das Bild kann in die Medienbibliothek im Commerce-Site-Builder hochgeladen oder es kann ein vorhandenes Bild verwendet werden. |
| Überschrift       | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Standardmäßig wird für die Überschrift die **H2**-Überschriftsmarkierung verwendet, aber die Markierung kann nach Bedarf geändert werden, um die Zugangsanforderungen zu erfüllen. |
| Absatz     | Absatztext | Das Modul unterstützt Absatztext im Rich-Text-Format. Einige grundlegende Rich-Text-Funktionen werden unterstützt, wie Hyperlinks, fett und kursiv formatierte sowie unterstrichene Texte. Einige dieser Funktionen können vom Seitenthema überschrieben werden, das im Modul verwendet wird. |
| Verknüpfung          | Link-Text, Link-URL, Accessible Rich Internet Applications-Beschriftung (ARIA) und Auswahl **Link in neuer Registerkarte öffnen** | Das Modul unterstützt mindestens einen oder mehrere „Handlungsaufruf“-Links. Wenn ein Link hinzugefügt wird, sind der Linktext, eine URL und eine ARIA-Beschriftung erforderlich. ARIA-Beschriftungen sollen beschreibend sein, um Barrierefreiheitsbedingungen zu erfüllen. Links können konfiguriert werden, sodass sie auf einer neuen Registerkarte geöffnet werden. |

## <a name="add-an-interactive-feature-module-to-a-new-page"></a>Ein interaktives Funktionsmodul einer neuen Seite hinzufügen

Um ein interaktives Funktionsmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften im Commerce-Website-Generator festzulegen, führen Sie die folgenden Schritte aus.

1. Gehen Sie auf **Vorlagen** und öffnen Sie die Marketingvorlage für die Homepage Ihrer Site (oder erstellen Sie eine neue Marketingvorlage).
1. Auf der Standardseite wählen Sie **Haupt**-Slot und dann die Ellipsen (**...**) und **Modul hinzufügen**.
1. Im Dialogfeld **Modul hinzufügen** wählen Sie das **interaktives Funktionsmodul** und wählen Sie dann **OK**.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Gehen Sie zu **Seiten** und öffnen Sie die Homepage der Site (oder erstellen Sie eine neue Homepage mithilfe der Marketingvorlage).
1. Auf dem Seitenüberblick wählen Sie den **Haupt**-Slot und wählen die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Im Dialogfeld **Modul hinzufügen** unter **Modul wählen** wählen Sie das Modul **Interaktive Funktion** dann **OK** aus.
1. Fügen Sie im Eigenschaftenbereich für das interaktive Funktionsmodul eine Überschrift hinzu.
1. Wählen Sie im Slot **Interaktives Funktionsmodul** das Ellipsen-Symbol (**...**) und dann **Modul hinzufügen** aus.
1. Im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Interaktives Funktionselement** und dann **OK** aus.
1. Fügen Sie im Eigenschaftenbereich des interaktiven Funktionselementmoduls ein Bild, Überschriftentext, Absatztext und eine URL hinzu.
1. Fügen Sie nach Bedarf zusätzliche interaktive Funktionselementmodule hinzu und konfigurieren Sie sie.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Adventure Works-Design](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
