---
title: Inhaltsblockmodul
description: Dieses Thema behandelt Inhaltsblockmodule und erläutert, wie sie Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f91de93ce5ed4813f9f2adbe7678229189b5af2f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025757"
---
# <a name="content-block-module"></a>Inhaltsblockmodul


[!include [banner](includes/banner.md)]

Dieses Thema behandelt Inhaltsblockmodule und erläutert, wie sie Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Ein Inhaltsblockmodul wird zur Vermarktung von Produkten oder Werbeaktionen durch eine Kombination aus Bildern und Texten verwendet. So kann ein Einzelhändler beispielsweise ein Inhaltsblockmodul der Homepage einer E-Commerce-Seite hinzufügen, um ein neues Produkt zu bewerben und Kunden darauf aufmerksam zu machen.

Ein Inhaltsblockmodul wird durch Daten aus dem Content-Management-System (CMS) gesteuert. Es ist ein Stand-Alone-Module, das die nicht von Seiteninhalt oder anderen Modulen auf der Seite abhängt. Ein Inhaltsblockmodul kann auf jeder Seite der Website platziert werden, auf der ein Einzelhändler etwas vermarkten oder bewerben möchte (z. B. Produkte, Verkäufe oder Funktionen).

## <a name="examples-of-content-block-module-in-e-commerce"></a>Beispiele von Inhaltsblockmodulen in E-Commerce

- Ein Inhaltsblockmodul kann auf der Homepage einer E-Commerce-Seite verwendet werden, um Werbeaktionen und neue Produkte hervorzuheben.
- Ein Inhaltsblockmodul kann auf einer Detailseite für Produkte verwendet werden, um Produktinformationen darzustellen.
- Mehrere Inhaltsblockmodule können innerhalb eines Karusselmoduls platziert werden, um mehrere Produkte oder Werbeaktionen hervorzuheben.

## <a name="content-block-modules-and-themes"></a>Inhaltsblockmodule und Designs

Inhaltsblockmodule können vielfältige Layouts und Stile basierend auf einem Thema unterstützen. So unterstützt zum Beispiel das Fabrikam-Design drei Layoutvariationen eines Inhaltsblockmoduls: Held, Funktion und Kachel. Das Helden-Layout zeigt im Hintergrund ein Bild mit Textüberlagerung. Das Funktions-Layout zeigt ein Bild und einen Text nebeneinander. Das Kachel-Layout erlaubt mehrere Inhaltsblöcke im Kachelformat.

Zusätzlich kann das Design für jedes Layout unterschiedliche Eigenschaften aufweisen. Ein Design-Entwickler kann mithilfe des Inhaltsblockmoduls mehr Layouts mit mehr Stilen erstellen.

Die folgende Abbildung zeigt das Beispiel eines Inhaltsblockmoduls mit einem Helden-Layout.

![Beispiel eines Hero-Moduls](./media/Hero.PNG)

Die folgende Abbildung zeigt das Beispiel eines Inhaltsblockmoduls mit einem Funktions-Layout.

![Beispiele für Funktionsmodule](./media/Feature.PNG)

## <a name="content-block-module-properties"></a>Eigenschaften eines Inhaltsblockmoduls

| Eigenschaftenname  | Werte | Beschreibung |
|----------------|--------|-------------|
| Bild          | Bilddatei | Ein Bild kann verwendet werden, um ein Produkt oder eine verkaufsfördernde Aktion zu machen. Ein Bild kann zu der Bildergalerie hochgeladen werden, oder ein vorhandenes Bild kann verwendet werden. |
| Überschrift        | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Jedes Heromodul kann eine Überschrift haben. Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet. Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen. |
| Absatz      | Absatztext | Heromodul unterstützt Absatztext im Rich-Text-Format. Einige grundlegende umfangreiche Inhaltsblockmodule werden unterstützt wie Fettformatierung und Kursivformattierung und Hyperlinks. Einige dieser Funktionen können vom Seitenthema überschrieben werden, das im Modul verwendet wird. |
| Verknüpfung           | Verknüpfen Sie Text, Link-URL, umfangreiche Internet-Anwendungs (ARIA)- Beschriftung und **Öffnen Sie die Verknüpfung in einer neuen Registerkarte** | Heromodul unterstützt mindestens einen oder mehrere Links „Aufruf zum Handelns“. Wenn ein Link hinzugefügt wird, sind der Linktext, eine URL und eine ARIA-Beschriftung erforderlich. ARIA-Beschriftungen sollen beschreibend sein, um Barrierefreiheitsbedingungen zu erfüllen. Links können konfiguriert werden, sodass sie auf einer neuen Registerkarte geöffnet werden. |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a>Im Fabrikam-Design dargestellte Eigenschaften von Inhaltsblockmodulen 

| Eigenschaftenname  | Werte | Beschreibung |
|----------------|--------|-------------|
| Textplatzierung | **Links**, **Rechts**, **Mitte** | Diese Eigenschaft definiert die Position des Textes auf dem Bild. Sie gilt nur für das Helden-Layout. |
| Textdesign     | **Hell** oder **Dunkel** | Ein Farbschema kann für den Text definiert werden, der auf Grundlage des Hintergrundbilds basiert. Wenn beispielsweise das Bild einen dunklen Hintergrund hat, kann ein Lichtthema angewendet werden, damit der Text sichtbarer wird und die Farbenkontrast-Verhältnisse verbessert. Sie gilt nur für das Helden-Layout.|
| Bildplatzierung       | **Links**, **Rechts** | Diese Eigenschaft gibt an, ob das Bild links oder rechts des Textes platziert sein soll. Sie gilt nur für das Funktions-Layout.  |

## <a name="add-a-content-block-module-to-a-new-page"></a>Einer neuen Seite ein Inhaltsblockmodul hinzufügen

Um ein Heromodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Rufen Sie **Vorlagen** auf, und erstellen Sie eine Seitenvorlage namens **Inhaltsblockvorlage**.
1. Im **Haupt-** Slot der Standardseite fügen Sie ein Heromodul hinzu.
1. Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.
1. Verwenden Sie das soeben erstellte Helden-Layout zur Erstellung einer Seite namens **Inhaltsblockseite**.
1. Auf dem Seitenüberblick wählen Sie den Slot (**Haupt**) und wählen die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Im Dialogfeld **Modul hinzufügen** unter **Modul wählen** wählen Sie das Heromodul, und wählen Sie dann **OK**.
1. Wählen Sie im Gliederungsbaum links das Inhaltsblockmodul aus.
1. Wählen Sie im Eigenschaftenbereich rechts und wählen Sie **Eine Bild hinzufügen** aus. Wählen Sie dann ein vorhandenes Bild aus oder laden Sie ein neues Bild hoch.
1. Wählen Sie **Kopfzeile** aus.
1. Im Dialogfeld **Überschrift** fügen Sie den Überschriftentext hinzu, wählen Sie die Überschriftsebene, und wählen Sie dann **OK** aus.
1. Fügen Sie unter **Rich-Text** Text hinzufügen, wie Sie diesen benötigen.
1. Wählen Sie **Link hinzufügen** aus.
1. Fügen Sie im Dialogfeld **Link** den Linktext, eine Link-URL sowie die ARIA-Kennzeichnung des Links ein, und wählen Sie anschließend **OK** aus.
1. Wählen Sie die Seite **Helden-** Layout aus.
1. Seite speichern und Ihre Änderungen in der Vorschau anzeigen.
1. Laden Sie die Seite hoch und veröffentlichen Sie sie.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Übersicht](starter-kit-overview.md)

[Werbebannermodul](add-alert.md)

[Karussellmodul](add-carousel.md)

[Textblockmodul](add-content-rich-block.md)

[Video-Player-Modul](add-video-player.md)
