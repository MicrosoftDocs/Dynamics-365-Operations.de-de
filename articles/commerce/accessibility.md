---
title: Funktionen und Leistungsspektrum der Eingabehilfe
description: Dieses Thema enthält Informationen über die Eingabehilfefunktionen und -funktionalitäten in Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e667f89ffbc5496cc93f83fd3e7b29ba6ffa979
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946017"
---
# <a name="accessibility-features-and-capabilities"></a>Funktionen und Leistungsspektrum der Eingabehilfe

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema enthält Informationen über die Eingabehilfefunktionen und -funktionalitäten in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Übersicht

Eingabehilfen und Funktionen bieten allen Benutzern die Möglichkeit, auf Aktionen zuzugreifen und diese auszuführen, um ihre Ziele zu erreichen. Dieses breite Anwenderspektrum erfordert möglicherweise Hilfsmittel für das Hören, Sehen, die Mobilität oder die Neurodiversität.

Mit verschiedenen Funktionen in Dynamics 365 Commerce können Sie Ihre Site so erstellen, dass sie unterstützende Funktionen enthält. Beim Entwerfen Ihrer Website sollten Sie die im Abschnitt zu Eingabehilfen genannten Bereiche berücksichtigen [Microsoft Accessibility Center](https://www.microsoft.com/accessibility). 

In diesem Thema werden einige zusätzliche Bereiche der Eingabehilfen beschrieben, die Sie bei der Verwendung von Dynamics 365 Commerce berücksichtigen sollten.

## <a name="image-alt-text"></a>Bildalttext

Dynamics 365 Commerce verfügt über ein integriertes digitales System zur Anlagenverwaltung zum Verfolgen von Bild- und Video-Assets, die auf Ihrer Site verwendet werden. Bildunterschriften, Beschreibungen und Alternativtext können im Eigenschaftenfenster für ein Bild hinzugefügt werden, wenn es ausgewählt oder hochgeladen wird.

## <a name="video-accessibility"></a>Video-Eingabehilfen

Das Dynamics 365 Commerce-System zur digitalen Anlagenverwaltung unterstützt mehrere Eingabehilfen für Videoinhalte. Einige Beispiele sind in der folgenden Tabelle aufgeführt.

| Video-Funktion               | Beschreibung |
|-----------------------------|-------------|
| Untertitel (CC)      | Text, der für die Audio- und Audiodeskriptionselemente eines Videos angezeigt werden kann, um hörgeschädigten Benutzern zu helfen |
| Untertitel                   | Beschriftungsdateien, die den Text von Kontexthinweisen oder Dialogfeldern auf dem Bildschirm anzeigen |
| Audio-Transkripte           | Eine Texttranskription gesprochener Wörter, die aus dem Audio eines Video-Assets generiert wird |
| Audiodeskription           | Ein nicht primärer Audiokanal, der den auf dem Bildschirm angezeigten Inhalt oder Kontext beschreibt |
| Mindestalter-Abgrenzung            | Ein Attribut, in dem das Mindestalter für die Anzeige eines Videos gespeichert werden kann (nur Metadaten). |

### <a name="configure-video-accessibility-elements"></a>Konfigurieren von Videozugriffselementen

In Dynamics 365 Commerce können Sie im Bereich **Assets** Ihrer Site Video-Assets hochladen, die separate Dateien für Untertitel, reguläres Audio und beschreibendes Audio enthalten. Untertitel können auch automatisch generiert werden, wenn ein Video-Asset hochgeladen wird.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Generieren oder Hochladen von Untertiteldateien während des Uploads von Video-Assets

Befolgen Sie diese Schritte, um eine Untertiteldatei beim Hochladen eines Videos automatisch zu generieren.

- Wählen Sie im Dialogfeld **Asset-Upload** die Option **Untertitel automatisch generieren** aus. Wenn Sie eine Untertiteldatei generieren, ist die Dateiauswahl für Untertiteldateien im Dialogfeld nicht verfügbar.

Befolgen Sie diese Schritte, um eine Untertiteldatei beim Hochladen eines Videos automatisch hochzuladen.

- Deaktivieren Sie im Dialogfeld **Asset-Upload** die Option **Untertitel automatisch generieren**.

Um normale Audio- oder beschreibende Audiodateien für das Video hochzuladen, verwenden Sie die Dateiauswahl im Dialogfeld **Asset-Upload**.

> [!NOTE]
> Objekte mit Untertiteln, normalem Audio und beschreibendem Audio können auch hinzugefügt werden, nachdem ein Video-Objekt hochgeladen wurde. Navigieren Sie zu **Assets**, wählen Sie das Video-Asset aus, und checken Sie es aus. Laden Sie dann im Eigenschaftenbereich für das Video-Asset die zusätzlichen Assets hoch.

#### <a name="edit-cc-and-audio-transcript-files"></a>Bearbeiten Sie CC- und Audio-Transkriptdateien

CC- und Audio-Transkriptdateien können direkt im Authoring-Tool bearbeitet werden. Die Videowiedergabe ist während der Bearbeitung verfügbar.

Führen Sie die folgenden Schritte aus, um CC- und Audio-Transkriptdateien zu bearbeiten.

1. Navigieren Sie zu **Assets**, wählen Sie das Video-Asset und dann **CC/Transkript bearbeiten** aus. Der Editor für Untertitel und Transkriptionsinhalte wird angezeigt.
1. Wählen Sie **Auschecken** aus.
1. Bearbeiten Sie die Untertitel oder den Transkriptionstext.
1. Wenn Sie fertig sind, wählen Sie **Speichern** und dann **Einchecken** aus.
1. Wenn Sie zum Veröffentlichen bereit sind, wählen Sie **Veröffentlichen** aus.

#### <a name="set-the-minimum-age-attribute"></a>Legen Sie das Attribut Mindestalter fest

Ein **Mindestalter**-Metadatenattribut kann mit Video-Assets verknüpft werden.

Gehen Sie zum Einstellen des Attributs **Mindestalter** für ein Video-Asset folgendermaßen vor.

1. Navigieren Sie zu **Assets**, und wählen Sie das Video-Asset aus.
1. Wählen Sie **Auschecken** aus.
1. Legen Sie im Eigenschaftenbereich für das Video-Asset das Attribut **Mindestalter** fest.

> [!NOTE]
> Der Eigenschaftenbereich wird nur zum Festlegen und Speichern des Metadatenattributwerts verwendet. Es müssen angepasste Module erstellt werden, um dieses Attribut für das Playback-Gating zu verwenden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eingabehilfen in Formularen, Produkten und Steuerelementen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Microsoft Accessibility Center](https://www.microsoft.com/accessibility)

[Dynamics 365 Accessibility Center](https://docs.microsoft.com/dynamics365/get-started/accessibility/index)

[Konformitätsübersicht](compliance-overview.md)

[Cookie-Compliance](cookie-compliance.md)

[Hinzufügen einer Datenschutzrichtlinienseite](add-privacy-page.md)
