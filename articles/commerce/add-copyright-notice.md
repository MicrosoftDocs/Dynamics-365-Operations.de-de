---
title: Hinzufügen eines Urheberrechtshinweises
description: In diesem Thema wird beschrieben, wie eine Urheberrechts-Meldung der E-Comerce Website hinzugefügt wird.
author: psimolin
manager: AnnBe
ms.date: 01/23/2020
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
ms.openlocfilehash: 54b48ee74bc9d9f2b77f0584a0bf1739a8dfdbdb
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025481"
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

1. Wechseln Sie zu **Fragmente**, und wählen Sie dann **Neues Seiten-Fragment** aus.
1. Wählen Sie im Dialogfeld **Fußzeile** das Modul und geben Sie dem Fragment einen Namen. Geben Sie zum Beispiel **Fußzeile-Urheberrecht** ein.
1. Wählen Sie **OK**.
1. Im Navigationsbereich wählen Sie die Ellipsis-Schaltfläche (**...**) neben der **Fußzeile** aus, und wählen Sie dann **Fügen Sie Modul hinzu** aus.
1. Wählen Sie im Dialogfeld **Fußzeilenkategorie** und **OK** aus.
1. Im Navigationsbereich wählen Sie die Ellipsis-Schaltfläche (...) neben der **Fußzeilenkategorie** aus, und wählen Sie dann **Fügen Sie Modul hinzu** aus.
1. Wählen Sie im Dialogfeld **Textblock** und dann **OK** aus.
1. Wählen Sie im Navigationsbereich **Textblock** aus.
1. Im Eigenschaftenbereich auf der rechten Seite im Feld **Absatz**, fügen Sie die Urheberrechtsnachricht hinzu. Geben Sie beispielsweise **(C) Fabrikam 2019** ein.
1. Wählen Sie **Speichern** aus, wählen Sie **Einchecken** und **Veröffentlichen** aus.
1. Wechseln Sie zu **Vorlagen**, wählen Sie die Vorlage, und wählen Sie dann **Auschecken** aus.
1. Erweitern Sie unter **Seiten-Gliederung**, **Text** und erweitern Sie dann **Standardseite**.
1. Aktivieren Sie die Schaltfläche neben **Fußzeilen-Slot**, und wählen Sie dann **Fügen Sie Fragment hinzu** aus.
1. Wählen Sie das Fragment, das Sie eben erstellt haben, und wählen Sie dann **Auswählen** aus.
1. Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.

Die Fußzeile, die den Urheberrechtshinweis automatisch enthält, wird im unteren Bereich alle Seiten hinzugefügt, die auf der ausgewählten Vorlage basieren.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hinzufügen eines Logos](add-logo.md)

[Auswählen eines Sitedesigns](select-site-theme.md)

[Arbeiten mit CSS-Überschreibungsdateien](css-override-files.md)

[Hinzufügen eines Favicons](add-favicon.md)

[Hinzufügen einer Begrüßungsnachricht](add-welcome-message.md)

[Hinzufügen von Sprachen zu Ihrer Website](add-languages-to-site.md)

[Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie](add-telemetry.md)

