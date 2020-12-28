---
title: Hinzufügen eines Urheberrechtshinweises
description: In diesem Thema wird beschrieben, wie eine Urheberrechts-Meldung der E-Comerce Website hinzugefügt wird.
author: psimolin
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 838047cac694c65047332e146a7c43ee2ae0f401
ms.sourcegitcommit: 1a12b42cc17f004a981c716aed3da6cf538475a5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4412692"
---
# <a name="add-a-copyright-notice"></a>Hinzufügen eines Urheberrechtshinweises

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie eine Urheberrechts-Meldung der E-Comerce Website hinzugefügt wird.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie einen Urheberrechtshinweis Ihrer Site hinzufügen können, müssen Sie die folgenden Artikel haben:

- Eine Vorlage, die freigegebenesFußzeilenfragment enthält.
- Eine Seite, die diese Vorlage verwendet.

## <a name="add-a-copyright-notice"></a>Hinzufügen eines Urheberrechtshinweises

Um einen Urheberrechtshinweis am Fuß jeder Seite hinzuzufügen die eine bestimmte Vorlage verwendet, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus.
1. Wählen Sie im Dialogfeld **Neues Seitenfragment** das Modul **Fußzeile** und den Namen des Fragments aus. Geben Sie zum Beispiel **Fußzeile-Urheberrecht** ein.
1. Wählen Sie **OK**.
1. Im Navigationsbereich wählen Sie die Ellipsis-Schaltfläche (**...**) neben der **Fußzeile** aus, und wählen Sie dann **Fügen Sie Modul hinzu** aus.
1. Wählen Sie im Dialogfeld **Fußzeilenkategorie** und **OK** aus.
1. Im Navigationsbereich wählen Sie die Ellipsis-Schaltfläche (...) neben der **Fußzeilenkategorie** aus, und wählen Sie dann **Fügen Sie Modul hinzu** aus.
1. Wählen Sie im Dialogfeld **Textblock** und dann **OK** aus.
1. Wählen Sie im Navigationsbereich **Textblock** aus.
1. Im Eigenschaftenbereich auf der rechten Seite im Feld **Absatz**, fügen Sie die Urheberrechtsnachricht hinzu. Geben Sie beispielsweise **(C) Fabrikam 2019** ein.
1. Wählen Sie **Speichern** aus, wählen Sie **Beenden Sie die Bearbeitung** und **Veröffentlichen** aus.
1. Navigieren Sie zu **Vorlagen**, wählen Sie die Vorlage und dann **Bearbeiten** aus.
1. Erweitern Sie unter **Seiten-Gliederung**, **Text** und erweitern Sie dann **Standardseite**.
1. Aktivieren Sie die Schaltfläche neben **Fußzeilen-Slot**, und wählen Sie dann **Fügen Sie Fragment hinzu** aus.
1. Wählen Sie das Fragment, das Sie eben erstellt haben, und wählen Sie dann **Auswählen** aus.
1. Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

Die Fußzeile, die den Urheberrechtshinweis automatisch enthält, wird im unteren Bereich alle Seiten hinzugefügt, die auf der ausgewählten Vorlage basieren.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hinzufügen eines Logos](add-logo.md)

[Auswählen eines Sitedesigns](select-site-theme.md)

[Arbeiten mit CSS-Überschreibungsdateien](css-override-files.md)

[Hinzufügen eines Favicons](add-favicon.md)

[Hinzufügen einer Begrüßungsnachricht](add-welcome-message.md)

[Hinzufügen von Sprachen zu Ihrer Website](add-languages-to-site.md)

[Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie](add-telemetry.md)

