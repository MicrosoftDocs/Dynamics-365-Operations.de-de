---
title: Videos hochladen
description: In diesem Thema wird beschrieben, wie Sie Videos in Microsoft Dynamics 365 Commerce Site Builder hochladen können.
author: psimolin
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f481e5d3f323b0c86d637b67c119d13b956d5714dc0d990004834e2be05b370e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735629"
---
# <a name="upload-videos"></a>Videos hochladen

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Videos in Microsoft Dynamics 365 Commerce Site Builder hochladen können.

Die Medienbibliothek des Commerce-Site-Builders ermöglicht Ihnen das Hochladen von Videos. Sie sollten immer die Version eines Videos mit der höchsten Bitrate und Auflösung hochladen, da das Video automatisch so konvertiert wird, dass es für verschiedene Ansichtsfenster und deren Haltepunkte geeignet ist.

### <a name="video-information-specified-during-upload"></a>Beim Hochladen angegebene Videoinformationen

Beim Hochladen eines Videos können die folgenden Informationen angegeben werden.

- **Titel, Beschreibung, Schlüsselwörter**: Metadaten des Videos.
- **Automatische Generierung von Untertiteln**: Gibt an, ob Untertitel für das Video automatisch generiert werden sollen (nur die englische Sprache wird unterstützt). 
- **Untertitel**: Gibt die zu verwendenden Untertitel an.
- **Regular Audio**: Gibt die zu verwendende reguläre Tonspur an.
- **Miniaturansicht**: Gibt die Miniaturansicht für das Video an. Wenn nicht angegeben, wird es automatisch generiert.
- **Beschreibendes Audio**: Gibt die zu verwendende beschreibende Tonspur an.

## <a name="upload-a-video"></a>Ein Video hochladen

Führen Sie die folgenden Schritte aus, um ein Video in Site Builder hochzuladen.

1. Wählen Sie im linken Navigationsbereich **Medienbibliothek**.
1. Wählen Sie in der Befehlsleiste **Hochladen \> Medienelemente hochladen**.
1. Navigieren Sie im Fenster Datei-Explorer zu einer oder mehreren hochzuladenden Videodateien und wählen Sie **Öffnen**.
1. Geben Sie im Dialogfenster **Medienelement hochladen** den gewünschten Titel und den Alt-Text ein.
1. Geben Sie eine optionale Beschreibung und Schlüsselwörter ein und wählen Sie eine Kategorie aus, falls gewünscht. 
1. Wenn Sie das Bild bzw. die Bilder nach dem sofortigen Hochladen veröffentlichen möchten, wählen Sie das Kontrollkästchen **Medienelemente nach dem Hochladen veröffentlichen**.
1. Wählen Sie **OK**.

Wenn Sie mehrere Arten von Assets gleichzeitig hochladen (z. B. Bilder und Videos), können Sie im Dialogfeld **Medienelement hochladen** nur Schlüsselwörter angeben, ob die Dateien unmittelbar nach dem Hochladen veröffentlicht werden sollen und ob für Videodateien automatisch Untertitel generiert werden sollen. Alle Assets werden die gleichen Schlüsselwörter verwenden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Verwaltung der digitalen Assets](dam-overview.md)

[Bilder hochladen](dam-upload-images.md)

[Dateien hochladen](dam-upload-files.md)

[Bilder zuschneiden](dam-crop-images.md)

[Bildfokuspunkte anpassen](dam-custom-focal-point.md)

[Statische Dateien hochladen und bedienen](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
