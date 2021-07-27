---
title: Siteauswahlmodul
description: Dieses Thema enthält das Siteauswahlmodul und es wird beschrieben, wie Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b69156ee79dbbe8cbb8f5eb5988a751f0488d8e5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357737"
---
# <a name="site-selector-module"></a>Siteauswahlmodul

[!include [banner](includes/banner.md)]

Dieses Thema enthält das Siteauswahlmodul und es wird beschrieben, wie Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Wenn ein Unternehmen unterschiedliche Websites in verschiedenen Märkten, Regionen und Gebiete hat, benötigen Websitebenutzer eine einfache Möglichkeit, zwischen Websites zu wechseln und ihre bevorzugte Einkaufsseite auszuwählen. Um diesem Szenario gerecht zu werden, können Benutzer mit dem Site-Auswahlmodul mehrere Sites durchsuchen.

Das Site-Auswahlmodul muss mit der Liste der Sites (Märkte, Regionen oder Gebietsschemas) konfiguriert sein, die Site-Benutzer durchsuchen können.

> [!NOTE]
> Das Siteauswahl-Modul ist in Dynamics 365 Commerce 10.0.14 Release verfügbar.

Die folgende Abbildung zeigt ein Beispiel für ein Site-Auswahlmodul, das in der Kopfzeile einer Site-Seite enthalten ist.

![Beispiel eines Site-Auswahlmoduls in der Kopfzeile einer Site-Seite.](./media/ecommerce-sitepicker.PNG)

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