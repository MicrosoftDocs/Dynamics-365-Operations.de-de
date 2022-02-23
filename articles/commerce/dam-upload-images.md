---
title: Bilder hochladen
description: In diesem Thema wird beschrieben, wie Sie Bilder in Microsoft Dynamics 365 Commerce Site Builder hochladen können.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 69b812c58739357dfdb3f9e65e34e5d54d890284
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963009"
---
# <a name="upload-images"></a>Bilder hochladen

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Bilder in Microsoft Dynamics 365 Commerce Site Builder hochladen können.

## <a name="overview"></a>Übersicht

Die Medienbibliothek des Commerce-Site-Builders ermöglicht Ihnen das Hochladen von Bildern, entweder einzeln oder in großen Mengen mit Hilfe von Ordnern. Sie sollten immer die Version des Bildes mit der höchsten Auflösung und Qualität hochladen, da die Image Resizer-Komponente das Bild automatisch für verschiedene Ansichtsfenster und deren Haltepunkte optimiert.

### <a name="image-information-specified-during-upload"></a>Während des Uploads angegebene Bildinformationen

Beim Hochladen eines Bildes können die folgenden Informationen angegeben werden.

- **Titel, Alt-Text, Beschreibung, Schlüsselwörter**: Metadaten des Bildes oder der Bilder. Titel und Alt-Text sind Pflichtwerte.
- **Kategorie auswählen**:
    - **Keine**: Wird für ein E-Commerce-Storytelling-Bild oder -Bilder verwendet.
    - **Produkt, Kategorie, Kunde, Mitarbeiter, Katalog**: Wird für Dynamics 365 Commerce Omni-Channel-Bild oder -Bilder verwendet.
- **Assets nach dem Hochladen veröffentlichen**: Wenn dieses Kontrollkästchen aktiviert ist, werden das Bild oder die Bilder sofort nach dem Hochladen veröffentlicht.

> [!NOTE]
> Bild-Assets mit einer zugewiesenen Kategorie werden auch automatisch mit der Kategorie als Schlüsselwort versehen, um die Suche nach Assets einer bestimmten Kategorie zu erleichtern.

### <a name="naming-conventions-for-omni-channel-images"></a>Namenskonventionen für Omni-Channel-Bilder 

Wenn Sie die Medienbibliothek als Omni-Channel-Bild-Backend konfiguriert haben, können Sie über Bildkategorien angeben, zu welcher Kategorie das hochgeladene Bild gehört. Es gibt auch eine Namenskonvention, die befolgt werden sollte, um sicherzustellen, dass die Bilder von anderen Kanälen, wie z.B. dem Point-of-Sale (POS), korrekt abgerufen werden.

Die Standardnamenskonvention variiert je nach Kategorie:
- Katalogbilder sollten „**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**“ benannt werden
- Kategoriebilder sollten „**/Categories/\{CategoryName\}.png**“ genannt werden
- Kundenbilder sollten „**/Customers/\{CustomerNumber\}.jpg**“ genannt werden
- Bilder von Mitarbeitern sollten „**/Workers/\{WorkerNumber\}.jpg**“ genannt werden
- Produktbilder sollten „**/Products/\{ProductNumber\}_000_001.png**“ genannt werden
    - 001 ist die Bildfolge und kann 001, 002, 003, 004 oder 005 sein
- Produktvariantenbilder sollten „**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**“ genannt werden

## <a name="upload-an-image"></a>Ein Bild hochladen

Um ein Bild in Site Builder hochzuladen, folgen Sie diesen Schritten.

1. Wählen Sie im linken Navigationsbereich **Medienbibliothek**.
1. Wählen Sie in der Befehlsleiste **Hochladen \> Medienelemente hochladen**.
1. Navigieren Sie im Fenster Datei-Explorer zu einer oder mehreren Bilddateien, die Sie hochladen möchten, und wählen Sie dann **Öffnen**.
1. Geben Sie im Dialogfenster **Medienelement hochladen** den gewünschten Titel und den Alt-Text ein.
1. Geben Sie eine optionale Beschreibung und Schlüsselwörter ein und wählen Sie eine Kategorie aus, falls gewünscht. 
1. Wenn Sie das/die Bild(er) unmittelbar nach dem Upload veröffentlichen möchten, markieren Sie das Kontrollkästchen **Medienobjekte nach dem Upload veröffentlichen**.
1. Wählen Sie **OK**.

## <a name="upload-a-folder-of-images"></a>Einen Ordner mit Bildern hochladen

Gehen Sie folgendermaßen vor, um einen Ordner mit Bildern in Site Builder hochzuladen.

1. Wählen Sie im linken Navigationsbereich **Medienbibliothek**.
1. Wählen Sie in der Befehlsleiste **Upload \> Upload-Ordner**.
1. Navigieren Sie im Datei-Explorer-Fenster zu einem Ordner, den Sie hochladen möchten, und wählen Sie dann **Öffnen**.
1. Geben Sie im Dialogfenster **Medienelemente hochladen** optionale Schlüsselwörter ein und wählen Sie, falls gewünscht, eine Kategorie aus. 
1. Wenn Sie die Bilder in dem Ordner unmittelbar nach dem Hochladen veröffentlichen möchten, markieren Sie das Kontrollkästchen **Medienobjekte nach dem Hochladen veröffentlichen**.
1. Wählen Sie **OK**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Verwaltung der digitalen Assets](dam-overview.md)

[Video hochladen](dam-upload-video.md)

[Dateien hochladen](dam-upload-files.md)

[Bilder zuschneiden](dam-crop-images.md)

[Bildfokuspunkte anpassen](dam-custom-focal-point.md)

[Statische Dateien hochladen und bedienen](upload-serve-static-files.md)
