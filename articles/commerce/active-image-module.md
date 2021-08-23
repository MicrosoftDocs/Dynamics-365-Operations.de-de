---
title: Aktives Bildmodul
description: Dieses Thema enthält aktive Bildmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.openlocfilehash: 36b7d6dea87c7f309c07608794d443a0ae19be211847d2cddcad95f2d933a8db
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716907"
---
# <a name="active-image-module"></a>Aktives Bildmodul

[!include [banner](includes/banner.md)]

Dieses Thema enthält aktive Bildmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Ein aktives Bildmodul kann verwendet werden, um Produkt-Tags in ein Bild einzubetten. Benutzer der E-Commerce-Site können dann mit der Maus über die Tags fahren, um eine Vorschau der im Bild angezeigten Produkte anzuzeigen. Die Vorschauen werden in Popupfenstern angezeigt. Durch Auswahl eines Vorschau-Popupfensters können Benutzer direkt zur Produktdetailseite (PDP) für das entsprechende Produkt gelangen.

Die Tags werden mithilfe von X- und Y-Koordinaten im Bild definiert. Jeder markierte Punkt sollte mit der Produkt-ID des im Bild gezeigten Produkts konfiguriert werden.

Die folgende Abbildung zeigt ein Beispiel für ein Vorschau-Popupfenster für ein Hero-Bild auf der Adventure Works-Homepage.

![Beispiel für ein Vorschau-Popupfenster in einem aktiven Bildmodul](./media/Active_image.PNG)

> [!IMPORTANT]
> - Das aktive Bildmodul ist ab der Version 10.0.20 von Dynamics 365 Commerce verfügbar.
> - Das aktive Bildmodul wird im Adventure Works-Design vorgestellt.

## <a name="active-image-module-properties"></a>Eigenschaften des aktiven Bildmoduls

| Eigenschaftenname      | Werte | Beschreibung |
|--------------------|--------|-------------|
| Bild              | Bilddatei | Ein Bild kann verwendet werden, um ein oder mehrere Produkte vorzustellen. Das Bild kann in die Medienbibliothek im Commerce-Site-Builder hochgeladen oder es kann ein vorhandenes Bild verwendet werden. |
| Breite              | Anzahl der Pixel | Diese Eigenschaft definiert die Breite des Bildes. Die aktiven Koordinaten werden basierend auf der Breite des Bildes berechnet.|
| Aktive Koordinaten | X- und Y-Koordinaten und eine Produkt-ID-Nummer | Jedes aktive Bildarray besteht aus X- und Y-Koordinaten und einer Produkt-ID-Nummer.|
| Überschrift            | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Standardmäßig wird für die Überschrift die **H2**-Überschriftsmarkierung verwendet, aber die Markierung kann nach Bedarf geändert werden, um die Zugangsanforderungen zu erfüllen. |
| Absatz          | Absatztext | Das Modul unterstützt Absatztext im Rich-Text-Format. Einige grundlegende Rich-Text-Funktionen werden unterstützt, wie Hyperlinks, fett und kursiv formatierte sowie unterstrichene Texte. Einige dieser Funktionen können vom Seitenthema überschrieben werden, das im Modul verwendet wird. |
| Verknüpfung               | Link-Text, Link-URL, Accessible Rich Internet Applications-Beschriftung (ARIA) und Auswahl **Link in neuer Registerkarte öffnen** | Das Modul unterstützt mindestens einen oder mehrere „Handlungsaufruf“-Links. Wenn ein Link hinzugefügt wird, sind der Linktext, eine URL und eine ARIA-Beschriftung erforderlich. ARIA-Beschriftungen sollen beschreibend sein, um Barrierefreiheitsbedingungen zu erfüllen. Links können konfiguriert werden, sodass sie auf einer neuen Registerkarte geöffnet werden. |
| Untertext           | Überschrift, Text und Links | Es kann zusätzlicher Kontext für das Bild hinzugefügt werden, z. B. ein Autoren- oder Designername oder Links zu persönlichen Blogs.|
| Textdesign         | **Hell** oder **Dunkel** | Mit dieser Eigenschaft kann ein Benutzer den Text basierend auf dem Hintergrundbild hell oder dunkel einstellen. Es ist als Designerweiterung im Adventure Works-Design verfügbar. |

## <a name="add-an-active-image-module-to-a-new-page"></a>Ein aktives Bildmodul einer neuen Seite hinzufügen

Um ein aktives Bildmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Gehen Sie auf **Vorlagen** und öffnen Sie die Marketingvorlage für die Homepage Ihrer Site (oder erstellen Sie eine neue Marketingvorlage).
1. Auf der Standardseite wählen Sie **Haupt**-Slot und dann die Ellipsen (**...**) und **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Aktives Bild** und dann **OK** aus.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Gehen Sie zu **Seiten** und öffnen Sie die Homepage der Site (oder erstellen Sie eine neue Homepage mithilfe der Marketingvorlage).
1. Auf dem Seitenüberblick wählen Sie den **Haupt**-Slot und wählen die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Aktives Bild** und dann **OK** aus.
1. Fügen Sie im Eigenschaftenbereich des aktiven Bildmoduls ein Bild hinzu und legen Sie die Canvasseite auf die Größe des Bildes fest.
1. Legen Sie die X- und Y-Koordinaten fest und fügen Sie die entsprechende Produkt-ID-Nummer hinzu.
1. Fügen Sie nach Bedarf zusätzliche aktive Bildmodul hinzu und konfigurieren Sie sie.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Adventure Works-Design](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
