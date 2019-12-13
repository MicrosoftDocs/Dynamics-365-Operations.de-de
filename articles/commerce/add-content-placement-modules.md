---
title: Inhaltsplatzierungsmodul
description: Dieses Thema deckt Inhaltsblockmodule und Inhaltsplatzierungselementmodule ab und beschreibt, wie sie den Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785299"
---
# <a name="content-placement-module"></a>Inhaltsplatzierungsmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema deckt Inhaltsblockmodule und Inhaltsplatzierungselementmodule ab und beschreibt, wie sie den Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Ein Inhaltsplatzierungsmodul ist ein spezieller Container, in den andere Module innerhalb einem spezifische Layout platziert werden können. Inhaltplatzierungsmodule unterstützen die folgenden Modultypen als untergeordnete Module: Inhaltplatzierungselement, Kontobegrüßungselement, Kontoauftragselement, Konto-Wunschlistenelement und Kontoprofilelement.

Inhaltplatzierungsmodule berechnen Daten aus untergeordneten Modulen, die sie unterstützen. Daher können Platzierungsmodule auf verschiedene Weise nutzen, abhängig von den Modulen, die hinzugefügt werden.

Inhaltsplatzierungsartikelmodule nutzen Bilder und Text, um Aktionen, Richtlinien und Produktfunktionen zu zeigen. So kann ein Inhalts-Platzierungsartikelmodul auf einer Startseite verwendet werden, um Shoprichtlinien oder -Versandinformationen anzuzeigen. Inhaltselementmodule werden von Daten des Content Management-System (CMS) gesteuert und können für jede beliebige Seite verwendet werden. Diese können jedoch nur innerhalb eines Inhaltplatzierungsmoduls verwendet werden.

## <a name="examples-of-content-placement-modules-in-e-commerce"></a>Beispiele für Inhaltplatzierungsmodule in E-Commerce

* Inhaltplatzierungsmodule, die Platzierungselementmodule enthalten, können auf einer Startseite oder Marketingseite verwendet werden, um Produktfunktionen, verkaufsfördernde Maßnahmen, Shop-Richtlinien, Versandinformationen und andere Informationen über Bilder und Text anzuzeigen.
* Inhaltplatzierungsmodule, die Platzierungselementmodule enthalten, können auf Produktdetailseiten verwendet werden, um Produktfunktionen bekannt zu machen.
* Inhaltsplatzierungsmodule, die Kontobegrüßungselement oder Kontoauftragselementmodule enthalten, können auf einer Krediterweiterungsverwaltungsseite verwendet werden.

## <a name="content-placement-module-properties"></a>Inhaltsplatzierungsmoduleigenschaften

| Eigenschaftenname | Wert | Beschreibung |
|---------------|-------|-------------|
| Breite         | **Eingepasster Container** oder **Bildschirm ausfüllen** | Wenn der Wert auf **Eingepasster Container** festgelegt ist, wird das Inhaltsplatzierungsmodul auf die breite des Inhaltsplatzierungsmoduls festgelegt. Wenn der Wert auf **Bildschirm ausfüllen** gesetzt wird, werden die Elemente nicht auf die Inhaltsplatzierungsmodulbreite beschränkt und aber können den Bildschirm ausfüllen. |

## <a name="content-placement-item-module-properties"></a>Inhaltsplatzierungsmodulelementeigenschaften

| Eigenschaftenname | Wert | Beschreibung |
|---------------|-------|-------------|
| Überschrift       | Überschriftentext und Überschriftentags (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Jedes Inhaltsplatzierungsmodul kann eine Überschrift haben. Die Eigenschaft **Überschrift** unterstützt Überschriftentags. Standardmäßig wird das **H2** Überschriftsmarkierung verwendet, aber die Überschriftsmarkierung kann nach Bedarf geändert werden, um die Zugangsanforderungen zu erfüllen. |
| Absatz     | Absatztext | Inhaltsplatzierungsmodul unterstützt Absatztext im Rich-Text-Format. Einige grundlegende umfangreiche Inhaltsblockmodule werden unterstützt wie Fettformatierung und Kursivformattierung und Hyperlinks. Einige dieser Funktionen können vom Seitenthema überschrieben werden, das im Modul verwendet wird. |
| Bild         | Bilddatei | Ein Bild kann dem Text zugeordnet werden. |
| Verknüpfung          | Link URL und Hyperlinktext | Ein Link kann dem Text hinzugefügt werden und auf die bestimmte Seite des Benutzers umgeleitet werden. |
| Kachelgröße     | Eine Nummer aus **1** bis **12** | Für jedes Inhaltsplatzierungsmodul definiert diese Eigenschaft die Anzahl der Slots, die ein Element im Inhaltsplatzierungsmodul ausfüllen sollte. Die maximale Größe des Inhaltsplatzierungsmodul beträgt 12 Slots. Wenn die gesamte Kachelgröße für das erste Element *n* im Inhaltsplatzierungsmodul 12 Slots übersteigt, wird das Element in die nächste Zeile eingebunden. |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a>Hinzufügen eines Inhaltsplatzierungsmoduls, das ein Inhaltsplatzierungselementmodul enthält für eine Seite enthält.

Um ein Inhaltsplatzierungsmodul hinzuzufügen, das ein Inhaltsplatzierungselementmodul für eine neue Seite enthält und die erforderliche Eigenschaft festgelegt werden muss, folgenden Sie diesen Schritten.

1. Erstellen Sie eine Vorlage, die mit **Inhaltserstellungsvorlage** bezeichnet wird.
1. Im **Haupt-** Slot der Standardseite fügen Sie ein Inhaltsplatzierungsmodul hinzu.
1. Im Inhaltsplatzierungsmodul fügen Sie ein Inhaltsplatzierungselementmodul hinzu.
1. Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.
1. Verwenden Sie die Inhaltsplatzierungsmodulvorlage, die Sie soeben erstellt haben, um eine Seite zu erstellen, die als **Inhaltsplatzierungsseite** bezeichnet wird.
1. Im **Haupt-** Slot der neuen Seite fügen Sie ein Inhaltsplatzierungsmodul hinzu.
1. Im Inhaltsplatzierungsmodul fügen Sie ein Inhaltsplatzierungselementmodul hinzu.
1. Im Eigenschaftsbereich für das Platzierungelementmodul wählen Sie ein Bild aus, fügen Sie eine Überschrift hinzu, fügen Sie einen Absatz hinzu, fügen Sie eine Verknüpfung hinzu, legen Sie den Link URL fest und legen Sie die Kachelgröße auf **6** fest.
1. Wiederholen Sie die Schritte 7 und 8, um ein anderes Inhaltsplatzierungselementmodul hinzuzufügen, dass die gleiche Kachelgröße hat.
1. Seite speichern und Vorschau anzeigen. Sie sollten zwei Inhaltsplatzierungselemente sehen, die nebeneinander angezeigt werden. Sie können die Eigenschaft der **Kachelgröße** jedes Platzierungselementmoduls anpassen oder mehr Module hinzufügen, um das gewünschte Layout zu erreichen.
1. Laden Sie die Seite hoch und veröffentlichen Sie sie.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Warnmmodul](add-alert.md)

[Karussellmodul](add-carousel.md)

[Umfangreiches Inhaltsblockmodul](add-content-rich-block.md)

[Funktionsmodul](add-feature-module.md)

[Hero-Modul](add-hero-module.md)

[Video-Player-Modul](add-video-player.md)
