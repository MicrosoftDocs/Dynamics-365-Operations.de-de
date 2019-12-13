---
title: Karussellmodul
description: Dieses Thema enthält Karusellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785236"
---
# <a name="carousel-module"></a>Karussellmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema enthält Karusellmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Ein Karussellmodul wird verwendet, um mehrere Werbeartikel in ein Karussell einzusetzen, das Debitoren durchsuchen können. Es handelt sich um einen spezielles Containermodul, das andere Module hostet. So kann beispielsweise ein Einzelhänder ein Karussellmodul auf eine Startseite verwenden, um mehrere neue Produkte oder Promotionen zu veröffentlichen.

Sie können Hero- und Funktionsmodule innerhalb eines Karussellmoduls hinzufügen. Die Eigenschaften des Karussellmoduls definieren dann, wie diese Module angezeigt werden.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Beispiele für Containermodulen in E-Commerce

- Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Startseite verwendet werden.
- Ein Karussell, das mehrere Promotionsmodule hat, kann auf einer Produktetailseite verwendet werden.
- Ein Karussell kann auf einer beliebigen Marketings-Seite verwendet werden, um mehrere Aktionen oder Produkte zu bewerben.

## <a name="carousel-module-properties"></a>Karussellmoduleigenschaften

| Eigenschaftenname             | Wert                                | Beschreibung |
|---------------------------|--------------------------------------|-------------|
| Automatische Wiedergabe                  | **True** oder **False**                | Wenn der Wert auf **Wahr** gesetzt wird, erfolgt der Übergangs zwischen Artikeln innerhalb des Karussells automatisch. Wenn der Wert auf **Falsch** gesetzt wird, erfolgt kein Übergang, es sei denn, der Debitor nutzt die Tastatur oder den Mauszeiger, um von einem Artikel zum nächsten Schritt zu gehen. |
| Folienübergangsintervall | Ein Wert in Sekunden                   | Das Intervall für Übergänge zwischen Artikeln. |
| Übergangsanimation      | **Anzeigen** oder **Ausblenden**                | Der Übergangseffekt |
| Breite                     | **Eingepasster Container** oder **Bildschirm ausfüllen** | Wenn der Wert auf **Eingepasster Container** festgelegt ist, werden die Module im Karussell auf die Breite des Karussells beschränkt. Wenn der Wert auf **Bildschirm ausfüllen** gesetzt wird, wird das Karussell nicht auf die Karussellbreite eingeschränkt und können den Bildschirm ausfüllen. Sie können den Wert ändern, um das gewünschte Layout zu erreichen. |

## <a name="add-a-carousel-module-to-a-page"></a>Ein Karussellmodul einer neuen Seite hinzufügen

Um ein Karussellmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie eine Seitenvorlage, die mit **Karussellvorlage** bezeichnet ist.
1. Im **Haupt-** Slot der Standardseite fügen Sie ein Karussellmodul hinzu.
1. Hinzufügen eines Heromoduls dem Karussellmodul.
1. Hinzufügen eines Funktionsmoduls dem Karussellmodul.
1. Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie. 
1. Verwenden Sie die Karoussellvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Karussellseite** hat.
1. Im **Haupt-** Slot der neuen Seite fügen Sie ein Karussellmodul hinzu.
1. Hier können Sie die Eigenschaft **Breite** des Karussellmoduls auf **Bildschirm ausfüllen** festlegen. 
1. Hier können Sie die Eigenschaft **Übergangsanimation** auf **Folie** festlegen.
1. Hinzufügen eines Heromoduls dem Karussellmodul.
1. Im Heromodul fügen Sie ein Bild und eine Kurzbeschreibung hinzu und wählen Sie dann **Speichern**.
1. Hinzufügen eines Funktionsmoduls dem Karussellmodul.
1. Im Funktionsmodul fügen Sie ein Bild, eine Überschrift und einen Absatz des Texts hinzu.
1. Seite speichern und Vorschau anzeigen. Die Seite sollte ein Karussell anzeigen, das zwei Module darin hat (ein Heromodul und ein Funktionsmodul). Sie können zusätzliche Eigenschaften für das Karussell, den Hero und Funktionsmodule ändern, um den gewünschten Effekt zu erreichen.
1. Laden Sie die Seite hoch und veröffentlichen Sie sie.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Warnmmodul](add-alert.md)

[Umfangreiches Inhaltsblockmodul](add-content-rich-block.md)

[Inhaltsplatzierungsmodul](add-content-placement-modules.md)

[Funktionsmodul](add-feature-module.md)

[Hero-Modul](add-hero-module.md)

[Video-Player-Modul](add-video-player.md)
