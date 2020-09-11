---
title: Hinzufügen eines Logos
description: In diesem Thema wird beschrieben, wie Sie ein Logo zu Ihrer Site in Microsoft Dynamics 365 Commerce hinzufügen.
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62b8237fa0c30fa9d901d670de38416cf8615c8d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686645"
---
# <a name="add-a-logo"></a>Hinzufügen eines Logos

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie ein Logo zu Ihrer Site in Microsoft Dynamics 365 Commerce hinzufügen.

## <a name="overview"></a>Übersicht

Wenn Sie Ihre Site erstellen, ist eines der ersten Dinge, die Sie wahrscheinlich tun werden, das Hinzufügen Ihres Firmen- oder Markenlogos zum Header der Site. Das Dynamics 365 Commerce-Online-Starter-Kit enthält ein Modul, das diese Aufgabe vereinfacht.

Sie können ein Logo direkt zu einer Vorlage, einem Layout oder einer Seite hinzufügen. Auf diese Weise können Sie ganz einfach das Logo ändern, das auf bestimmten Seiten oder Seitengruppen angezeigt wird. In diesem Thema wird jedoch das häufigste Szenario behandelt, in dem Sie ein Headerfragment mit Ihrem Logo versehen, das auf allen Seiten Ihrer Website wiederverwendet werden kann.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie allen Seiten Ihrer Site ein Logo hinzufügen können, müssen Sie diese Aufgaben ausführen.

1. Laden Sie Ihr Logo in die Medienbibliothek hoch.
1. Erstellen Sie ein Header-Fragment. Weitere Informationen zum Erstellen und Verwenden von Fragmenten finden Sie unter [Arbeiten mit Fragmenten](work-with-fragments.md).
1. Fügen Sie das Headerfragment in die Vorlage ein, die die Seiten Ihrer Site für ihre Layout- und Moduloptionen verwenden. Weitere Informationen zu Vorlagen erhalten Sie unter [Arbeiten mit Vorlagen](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Einem Headerfragment ein Logo hinzufügen

Gehen Sie folgendermaßen vor, um dem Headerfragment für Ihre Site ein Logo hinzuzufügen.

1. Wählen Sie im linken Navigationsbereich **Fragmente** aus.
1. Wählen Sie das Headerfragment, das Sie eben erstellt haben, aus und dann **Bearbeiten**.
1. Erweitern Sie das Kopfmodul.
1. Geben Sie im Eigenschaftenbereich für das Kopfzeilenmodul ein Bild und einen Link für das Logo ein. 
1. Speichern Sie das Headerfragment, beenden Sie die Bearbeitung und veröffentlichen Sie sie.

Nachdem Sie das aktualisierte Headerfragment veröffentlicht haben, wird auf allen Websiteseiten, die die Vorlage mit dem Headerfragment verwenden, Ihr Logo angezeigt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Auswählen eines Sitedesigns](select-site-theme.md)

[Arbeiten mit CSS-Überschreibungsdateien](css-override-files.md)

[Hinzufügen eines Favicons](add-favicon.md)

[Hinzufügen einer Begrüßungsnachricht](add-welcome-message.md)

[Hinzufügen eines Urheberrechtshinweises](add-copyright-notice.md)

[Hinzufügen von Sprachen zu Ihrer Website](add-languages-to-site.md)

[Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie](add-telemetry.md)

