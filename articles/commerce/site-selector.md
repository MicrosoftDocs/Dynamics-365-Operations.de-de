---
title: Websiteauswahlmodul
description: Dieses Thema befasst sich mit dem Websiteauswahlmodul und es wird beschrieben, wie Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 02/11/2022
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
ms.openlocfilehash: 381163fdd6180a76def2e1bfb733f597b611c517
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109705"
---
# <a name="site-picker-module"></a>Websiteauswahlmodul

[!include [banner](includes/banner.md)]

Dieses Thema befasst sich mit dem Websiteauswahlmodul und es wird beschrieben, wie Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Wenn ein Unternehmen unterschiedliche Websites in verschiedenen Märkten, Regionen und Gebiete hat, benötigen Websitebenutzer eine einfache Möglichkeit, zwischen Websites zu wechseln und ihre bevorzugte Einkaufsseite auszuwählen. Um diesem Szenario gerecht zu werden, können Benutzer mit dem Websiteauswahlmodul mehrere Sites durchsuchen.

Das Websiteaswahlmodul muss mit der Liste der Sites (Märkte, Regionen oder Gebietsschemas) konfiguriert sein, die Site-Benutzer durchsuchen können.

> [!NOTE]
> Das Websiteauswahlmodul ist in Dynamics 365 Commerce Release 10.0.14 verfügbar.

Die folgende Abbildung zeigt ein Beispiel für ein Websiteauswahlmodul, das in der Kopfzeile einer Seite enthalten ist.

![Beispiel eines Websiteauswahlmoduls in der Kopfzeile einer Seite.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Eigenschaften des Websiteauswahlmoduls

| Eigenschaftenname | Wert                 | Description |
|---------------|-----------------------|-------------|
| Überschrift       | Text                  | Die Überschrift für das Modul. |
| Websiteoptionen  | Name, Bild, URL      | Diese Eigenschaft gibt einen Namen, einen Link zur Homepage der Site und ein optionales Bild für jede Site an, die im Modul enthalten ist. Das Bild kann eine Flagge oder eine Darstellung eines Marktes, einer Region oder eines Gebietsschemas sein. |

## <a name="add-a-site-picker-module-to-a-page"></a>Hinzufügen eines Websiteauswahlmoduls zu einer Seite

Das Websiteauswahlmodul kann dem **Websiteauswahl**-Slot des [Kopfzielenmoduls](author-header-module.md) hinzugefügt werden. Nach dem Hinzufügen eines Websiteauswahlmoduls können Sie die Modulüberschrift und die Site-Optionen definieren. Im Allgemeinen ist ein Kopfzeilenmodul in einem Kopfzeilenfragment enthalten, das über E-Commerce-Seiten für eine Website gemeinsam genutzt werden kann. Im folgenden Beispiel wurde das Websiteauswahlmodul zum **Websiteauswahl**-Slot eines Kopfzeilenmoduls hinzugefügt, das in einem Kopfzeilenfragment namens **HeaderContainer** enthalten ist.

![Beispiel eines Websiteauswahlmoduls in einem Kopfzeilenfragment.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Kopfzeilenmodul](author-header-module.md)

[Breadcrumb-Modul](add-breadcrumb.md)

[Navigationsmenümodul](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
