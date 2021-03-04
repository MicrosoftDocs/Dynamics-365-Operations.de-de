---
title: Siteauswahlmodul
description: Dieses Thema enthält das Siteauswahlmodul und es wird beschrieben, wie Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b4e5f715efcac7f883df99508d282db904be0d80
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665222"
---
# <a name="site-selector-module"></a>Siteauswahlmodul

[!include [banner](includes/banner.md)]

Dieses Thema enthält das Siteauswahlmodul und es wird beschrieben, wie Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Wenn ein Unternehmen unterschiedliche Websites in verschiedenen Märkten, Regionen und Gebiete hat, benötigen Websitebenutzer eine einfache Möglichkeit, zwischen Websites zu wechseln und ihre bevorzugte Einkaufsseite auszuwählen. Um diesem Szenario gerecht zu werden, können Benutzer mit dem Site-Auswahlmodul mehrere Sites durchsuchen.

Das Site-Auswahlmodul muss mit der Liste der Sites (Märkte, Regionen oder Gebietsschemas) konfiguriert sein, die Site-Benutzer durchsuchen können.

> [!NOTE]
> Das Siteauswahl-Modul ist in Dynamics 365 Commerce 10.0.14 Release verfügbar.

Die folgende Abbildung zeigt ein Beispiel für ein Site-Auswahlmodul, das in der Kopfzeile einer Site-Seite enthalten ist.

![Beispiel eines Site-Auswahlmoduls in der Kopfzeile einer Site-Seite](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>Eigenschaften des Siteauswahlmoduls

| Eigenschaftenname | Wert                 | Beschreibung |
|---------------|-----------------------|-------------|
| Überschrift       | Text                  | Die Überschrift für das Modul. |
| Websiteoptionen  | Name, Bild, URL      | Diese Eigenschaft gibt einen Namen, einen Link zur Homepage der Site und ein optionales Bild für jede Site an, die im Modul enthalten ist. Das Bild kann eine Flagge oder eine Darstellung eines Marktes, einer Region oder eines Gebietsschemas sein. |

## <a name="add-a-site-selector-module-to-a-page"></a>Hinzufügen eines Siteauswahlmoduls zu einer Seite

Das Site-Auswahlmodul kann dem [Header-Modul](author-header-module.md) unter dem Site-Auswahl-Slot hinzugefügt werden. Nach dem Hinzufügen können Sie die Modulüberschrift und die Site-Optionen definieren.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Kopfzeilenmodul](author-header-module.md)

[Breadcrumb-Modul](add-breadcrumb.md)

[Navigationsmenümodul](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]