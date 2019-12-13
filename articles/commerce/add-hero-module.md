---
title: Hero-Modul
description: Dieses Thema enthält Heromodule und es wird beschrieben, wie diese den Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785389"
---
# <a name="hero-module"></a>Hero-Modul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema enthält Heromodule und es wird beschrieben, wie diese den Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Ein Heldmodul wird verwendet, um Produkte oder verkaufsfördernden Maßnahmen über eine Kombination von Bildern und Text zu promoten. So kann beispielsweise ein Einzelhändler ein Heldmodul der Startseite einer E-Commerce-Webseite hinzufügen, um ein neues Produkt zu bewerben und die Aufmerksamkeit von Debitoren zu erregen.

Ein Heromodul wird durch Daten des Content Management-System (CMS) gesteuert. Es ist ein Stand-Alone-Module, das die nicht von Seiteninhalt oder anderen Modulen auf der Seite abhängt. Ein Heromodul kann für jede beliebige Siteseite verwendet werden, in der ein Einzelhändler etwas promoten will (beispielsweise Produkte, Verkäufe oder Funktionen).

## <a name="examples-of-hero-module-in-e-commerce"></a>Beispiele für Heromodule im E-Commerce

- Ein Heromodul kann auf der Startseite einer E-Commerce-Webseite verwendet werden, um Aktionen und neue Produkte hervorzuheben.
- Ein Heromodul kann auf einer Produktdetailseite verwendet werden, um Produktinformationen zu zeigen.
- Mehrere Heromodule können innerhalb eines Karussellmoduls eingelagert werden, um mehrere Produkte oder Promotionen hervorzuheben.

## <a name="hero-module-properties"></a>Heromoduleigenschaften

| Eigenschaftenname  | Werte | Beschreibung |
|----------------|--------|-------------|
| Bild          | Bilddatei | Ein Bild kann verwendet werden, um ein Produkt oder eine verkaufsfördernde Aktion zu machen. Ein Bild kann zu der Bildergalerie hochgeladen werden, oder ein vorhandenes Bild kann verwendet werden. |
| Überschrift        | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Jedes Heromodul kann eine Überschrift haben. Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet. Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen. |
| Absatz      | Absatztext | Heromodul unterstützt Absatztext im Rich-Text-Format. Einige grundlegende umfangreiche Inhaltsblockmodule werden unterstützt wie Fettformatierung und Kursivformattierung und Hyperlinks. Einige dieser Funktionen können vom Seitenthema überschrieben werden, das im Modul verwendet wird. |
| Verknüpfung           | Verknüpfen Sie Text, Link-URL, umfangreiche Internet-Anwendungs (ARIA)- Beschriftung und **Öffnen Sie die Verknüpfung in einer neuen Registerkarte** | Heromodul unterstützt mindestens einen oder mehrere Links „Aufruf zum Handelns“. Wenn ein Link hinzugefügt wird, sind der Linktext, eine URL und eine ARIA-Beschriftung erforderlich. ARIA-Beschriftungen sollen beschreibend sein, um Barrierefreiheitsbedingungen zu erfüllen. Links können konfiguriert werden, sodass sie auf einer neuen Registerkarte geöffnet werden. |
| Textplatzierung | **Oben links**, **Oben rechts**, **Oben zentriert**, **Unten links**, **Unten rechts**, **Unten zentriert**, **Mitte links**, **Mitte rechts** oder **Mitte zentriert** | Diese Eigenschaft definiert die Bildlage relativ zum im Text. Wenn beispielsweise **Rechts** aktiviert ist, erscheint das Bild auf der rechten Seite des Texts. |
| Textdesign     | **Hell** oder **Dunkel** | Ein Farbschema kann für den Text definiert werden, der auf Grundlage des Hintergrundbilds basiert. Wenn beispielsweise das Bild einen dunklen Hintergrund hat, kann ein Lichtthema angewendet werden, damit der Text sichtbarer wird und die Farbenkontrast-Verhältnisse verbessert. |
| Farbverlauf       | **True** oder **False** | Ein Farbverlauf kann für das Bild angewendet werden, um Farbenkontrast-Verhältnisse zu verbessern. |

## <a name="add-a-hero-module-to-a-new-page"></a>Ein Heromodul einer neuen Seite hinzufügen

Um ein Heromodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Vorlagen** und erstellen Sie eine Seitenvorlage mit der Bezeichnung **Herovorlage**.
1. Im **Haupt-** Slot der Standardseite fügen Sie ein Heromodul hinzu.
1. Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.
1. Verwenden Sie die Herovorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Heroseite** hat.
1. Auf dem Seitenüberblick wählen Sie den Slot (**Haupt**) und wählen die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Im Dialogfeld **Modul hinzufügen** unter **Modul wählen** wählen Sie das Heromodul, und wählen Sie dann **OK**.
1. In der Gliederungsstruktur im Feld links wählen Sie das Heromodul aus.
1. Wählen Sie im Eigenschaftenbereich rechts und wählen Sie **Eine Bild hinzufügen** aus. Wählen Sie dann ein vorhandenes Bild aus oder laden Sie ein neues Bild hoch.
1. Wählen Sie **Kopfzeile** aus.
1. Im Dialogfeld **Überschrift** fügen Sie den Überschriftentext hinzu, wählen Sie die Überschriftsebene, und wählen Sie dann **OK** aus.
1. Fügen Sie unter **Rich-Text** Text hinzufügen, wie Sie diesen benötigen.
1. Wählen Sie **Fügen Sie Aktivitäts-Link hinzu** aus.
1. Im Dialogfeld **Aktivitäts-Link** fügen Sie Text des Links, eine URL und eine ARIA-Beschriftung hinzu und wählen Sie dann **OK**.
1. Seite speichern und Ihre Änderungen in der Vorschau anzeigen.
1. Laden Sie die Seite hoch und veröffentlichen Sie sie.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Warnmmodul](add-alert.md)

[Karussellmodul](add-carousel.md)

[Umfangreiches Inhaltsblockmodul](add-content-rich-block.md)

[Inhaltsplatzierungsmodul](add-content-placement-modules.md)

[Funktionsmodul](add-feature-module.md)

[Video-Player-Modul](add-video-player.md)
