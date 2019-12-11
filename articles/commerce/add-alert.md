---
title: Warnungsmodul
description: Dieses Thema enthält allgemeine Module und es wird beschrieben, wie diese Standortsseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785351"
---
# <a name="alert-module"></a>Warnmmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema enthält allgemeine Module und es wird beschrieben, wie diese Standortsseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Ein Warnungsmodul wird verwendet, um Informationsmeldungen auf einer Seite anzeigen. Warnungsmodule unterstützen Textnachricht und einen Link. Sie können verwendet werden, um Standort-weite Aktionen anzuzeigen, die auf allen Seiten einer E-Commerce-Webseite verwendet werden. 

WModule Wachsame werden nach Daten des Content Management-System (CMS) gesteuert und können für jede beliebige Seite eingelagert werden.

## <a name="examples-of-alert-modules-in-e-commerce"></a>Beispiele der Warnungsmodule in E-Commerce

Warnungsmodule können im Sitekopf verwendet werden, um Standort-weite Aktionen oder Nachrichten anzugeben. Nachfolgend finden Sie einige Beispiele:

„Jahresendverkauf endet in 10 Tagen“

„Mit den Aktionen zum Schulbeginn viel sparen. Jetzt shoppen.“

## <a name="alert-module-properties"></a>Warnungsmoduleigenschaften

| Eigenschaftenname  | Wert                              | Beschreibung |
|----------------|------------------------------------|-------------|
| Text           | Text                               | Die Textnachricht erscheint im Warnungsmodul. |
| Textausrichtung | **Rechts** **Links** **Zentriert** | Ein Wert, der definiert, wie Text im Warnungsmodul dargestellt wird. |
| Warnung verwerfen  | **True** oder **False**              | Wenn der Wert auf **True** gesetzt wird, kann der Debitor die Warnung ablehnen. |
| Verknüpfung           | URL                                | Die URL für einen optionalen Link. |

## <a name="add-an-alert-module-to-a-page"></a>Ein Warnungsmodul einer Seite hinzufügen 

Um ein Warnungsmodul einer Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie eine Seitenvorlage, die mit **Warnungsvorlage** bezeichnet ist.
1. Im **Haupt-** Slot der Standardseite fügen Sie ein Warnungsmodul hinzu.
1. Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie. 
1. Verwenden Sie die Warnungsvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Warnungsseite** hat. 
1. Im **Haupt-** Slot der neuen Seite fügen Sie ein Warnungsmodul hinzu.
1. In den Einstellungen für das Warnungsmodul geben Sie den Warnungstext ein. Sie können die anderen Eigenschaften bearbeiten, wenn Sie das Modul weiter anpassen möchten.
1. Seite speichern und Vorschau anzeigen. Am oberen Rand der Seite können sollten Sie eine Warnung sehen, die den von Ihnen hinzugefügten Text hat.
1. Laden Sie die Seite hoch und veröffentlichen Sie sie. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Karussellmodul](add-carousel.md)

[Umfangreiches Inhaltsblockmodul](add-content-rich-block.md)

[Inhaltsplatzierungsmodul](add-content-placement-modules.md)

[Funktionsmodul](add-feature-module.md)

[Hero-Modul](add-hero-module.md)

[Video-Player-Modul](add-video-player.md)
