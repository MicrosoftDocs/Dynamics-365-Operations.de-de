---
title: Bewertungsprofile
description: Dieser Artikel beschreibt, wie Sie die Daten für Bewertungsprofile festlegen.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f7408574187ddb099181bd2566c46c52307f603
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850466"
---
# <a name="rating-profiles"></a>Bewertungsprofile

[!include [banner](../../includes/banner.md)]

Ein Tarifprofil ähnelt einem Logistikvertrag (aber nicht einem Rechtsvertrag). Es wird verwendet, um Transporttarife für Ladungen zu bestimmen. 

Jedes Tarifprofil ist einzigartig für einen Spediteur. Im Profil verknüpfen Sie den Spediteur mit einem Tarifmaster. Der Tarifmaster definiert die Tarifbasiszuordnung und die Tarifbasis. Die Tarifbasis bestimmt den Satz des Spediteurs.

Sie können ein Satzprofil über eine generische Seite festlegen, die eine Übersicht über alle vorhandenen Satzprofile anzeigt. Alternativ können Sie ein Tarifprofil auch direkt vom Spediteur festlegen. In beiden Fällen sind die Informationen, die Sie für das Bewertungsprofil festlegen, die gleichen.

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a>Erstellen oder bearbeiten Sie ein Bewertungsprofil auf der Seite Bewertungsprofile

Auf der Seite **Bewertungsprofile** können Sie alle verfügbaren Bewertungsprofile einsehen. Sie können auch vorhandene Profile bearbeiten und neue Profile erstellen.

1. Gehen Sie zu **Transportverwaltung \> Einrichten \> Bewertung \> Bewertungsprofil**.
1. Wählen Sie im Aktivitätsbereich **Neu**, um ein neues Bewertungsprofil zum Raster hinzuzufügen, oder wählen Sie **Bearbeiten**, um ein vorhandenes Profil zu bearbeiten.
1. Legen Sie in der Zeile für das neue oder bestehende Bewertungsprofil die folgenden Felder fest:

    - **Bewertungsprofil** - Geben Sie einen eindeutigen Bezeichner (ID) für das Bewertungsprofil ein.
    - **Name** - Geben Sie einen beschreibenden Namen für das Bewertungsprofil ein.
    - **Spediteur** - Wählen Sie einen Spediteur aus. Das Bewertungsprofil, das Sie festlegen, wird auch auf der Seite **Versandunternehmen** für den gewählten Spediteur angezeigt.
    - **Standort** und **Lagerort** - Wählen Sie einen Standort und einen Lagerort.
    - **Tarifrechner** - Wählen Sie den Tarifrechner für das Tarifprofil.
    - **Tarifmaster** - Wählen Sie den Tarifmaster für das Tarifprofil. Sie können den Tarifmaster verwenden, um einen Tarifbasistyp und eine Tarifbasis zu definieren. Für weitere Informationen siehe [Tarifmaster festlegen](set-up-rate-masters.md).
    - **Transitzeit-Engine** - Wählen Sie die Transitzeit-Engine für das Rating-Profil.
    - **Kraftstoffindex des Spediteurs** - Wählen Sie den Kraftstoffindex des Spediteurs für das Tarifprofil aus.
    - **Effektives Startdatum und -uhrzeit** und **Effektives Enddatum und -uhrzeit** - Definieren Sie den Zeitraum, in dem das Bewertungsprofil aktiv sein soll.

1. Wählen Sie im Aktionsbereich **Speichern** aus.

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a>Erstellen Sie ein Bewertungsprofil direkt auf der Seite Spediteure

1. Wechseln Sie zu **Transportverwaltung \> Einstellungen \> Spediteure \> Spediteure**.
1. Wählen Sie einen Spediteur in der Liste aus.
1. Wählen Sie auf dem Inforegister **Bewertungsprofile** die Option **Neu**, um ein Bewertungsprofil zu erstellen.
1. Legen Sie die Felder für das neue Bewertungsprofil fest. Diese Felder entsprechen den Feldern auf der Seite **Bewertungsprofile**, wie im vorherigen Abschnitt dieses Artikels beschrieben.

> [!NOTE]
> Profile, die auf der Seite **Spediteure** erstellt werden, werden auch auf der Seite **Bewertungsprofile** angezeigt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]