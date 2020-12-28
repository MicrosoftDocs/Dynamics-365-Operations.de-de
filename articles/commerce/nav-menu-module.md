---
title: Navigationsmenümodul
description: Dieses Thema enthält Navigationsmenümodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: eee3523be26369aecdb36c0143a6ee3dab4b7966
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4412701"
---
# <a name="navigation-menu-module"></a>Navigationsmenümodul

[!include [banner](includes/banner.md)]

Dieses Thema enthält Navigationsmenümodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Der Hauptzweck von Navigationsmenümodulen besteht darin, Website-Benutzern das Durchsuchen von Produkten und Website-Seiten gemäß der in Dynamics 365 Commerce-Zentralverwaltung definierten Kanalnavigationshierarchie zu ermöglichen . In einem Navigationsmenümodul konfigurierte Elemente werden als Website-Header-Navigation angezeigt. Navigationsmenümodule unterstützen auch statische Menüelemente, die auf andere Seiten einer E-Commerce-Wensite verweisen.

Das Navigationsmenümodul kann dem Header-Modul einer Seite hinzugefügt werden. Im Fabrikam-Design werden im Navigationsmenü standardmäßig zwei Ebenen angezeigt. Im Starter-Design werden im Navigationsmenü standardmäßig drei Ebenen angezeigt. Um die Anzahl der Ebenen zu ändern, ist eine Ansichtserweiterung für das Design erforderlich.

Die folgende Abbildung zeigt ein Beispiel für ein Navigationsmenü für die Fabrikam-Website mit zwei Ebenen der Kategoriehierarchie und einigen statischen Menüelementen.
![Beispiel eines Navigationsmenümoduls](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Eigenschaften des Navigationsmenümoduls

| Eigenschaftenname             | Wert                 | Beschreibung |
|---------------------------|-----------------------|-------------|
| Grundlage                  | **Retail**, **Manuelle Dokumenterstellung**, **Retail und manuelle Dokumenterstellung** | Der **Retail**-Wert ermöglicht der Kanalnavigationshierarchie der Commerce-Zentralverwaltung im Navigationsmenü angezeigt zu werden. Der Wert **Manuelle Dokumenterstellung** ermöglicht das Kuratieren statische Menüelemente. Der Wert **Retail und manuelle Dokumenterstellung** ermöglicht eine Mischung aus beiden. |
| Kategoriebilder anzeigen | **True** oder **False**    | Wenn diese Eigenschaft aktiviert ist, werden Kategoriebilder so im Navigationsmenü angezeigt, wie Sie in der Commerce-Zentralverwaltung für jede Kategorie definiert sind. Hinzugefügt in Commerce-Version 10.0.14. |
| Aktivieren Sie das mehrstufige Navigationsmenü | **True** oder **False** | Wenn diese Eigenschaft aktiviert ist, kann das Navigationsmenü mehrere Ebenen der Navigationshierarchie anzeigen. Diese Funktion ist nur in Dynamics 365 Commerce, Release 10.0.15 verfügbar. |
| Anzahl der Ebenen | Integer | Diese Eigenschaft definiert die Anzahl der Ebenen, die angezeigt werden sollen, wenn die Eigenschaft **Aktivieren Sie das mehrstufige Navigationsmenü** auf **Wahr** festgelegt ist. |
| Statisches Menüelement| Wertearray| Statische Menüelemente, die einen Menüelementnamen mit einem Link zu einer statischen Website-Seite verknüpfen. Sie können Menüelemente unter anderen Menüelementen erstellen. Standardmäßig werden statische Menüs auf der Stammebene angezeigt und an die Kanalnavigationshierarchie angehängt, falls diese vorhanden ist. |
| Stamm-Menü anzeigen | **True** oder **False** | Wenn diese Eigenschaft aktiviert ist, kann das Navigationsmenü unter einem benutzerdefinierten Stamm definiert werden (z. B. **Jetzt einkaufen**). Diese Funktion ist nur in Dynamics 365 Commerce, Release 10.0.15 verfügbar. |
| Stamm-Menü | Zeichenfolge | Diese Eigenschaft kann verwendet werden, um Text für einen benutzerdefinierten Stamm zu definieren, wenn die **Stamm-Menü anzeigen** Eigenschaft ist auf **Wahr** festgelegt ist. |

Die folgende Abbildung zeigt ein Beispiel für ein Kategoriebild, das im Navigationsmenü für die Fabrikam-Website angezeigt wird.
![Beispiel eines Navigationsmoduls mit Kategoriebildern](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Hinzufügen eines Header-Moduls zu einem Navigationsmenümodul

Ausführliche Informationen zum Hinzufügen eines Navigationsmenümoduls zu einem Header-Modul finden Sie unter [Header-Modul](author-header-module.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Breadcrumb-Modul](add-breadcrumb.md)

[Siteauswahlmodul](site-selector.md)

[Kauffeldmodul](add-buy-box.md)

[Cookie-Compliance](cookie-compliance.md)

[Kopfzeilenmodul](author-header-module.md)
