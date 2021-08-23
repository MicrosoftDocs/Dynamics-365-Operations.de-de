---
title: Wenden Sie Anzeigeeinstellungen für Produktabmessungen an
description: In diesem Thema werden die Anzeigeeinstellungen für Produktabmessungen behandelt und deren Anwendung in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar-ms
ms.date: 05/28/2021
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 80a0861c51ea14ddb6bce02d757667adac34e740cd04311e26211d9bdbae4ed8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716221"
---
# <a name="apply-display-settings-for-product-dimensions"></a>Wenden Sie Anzeigeeinstellungen für Produktabmessungen an

[!include [banner](includes/banner.md)]


In diesem Thema werden die Anzeigeeinstellungen für Produktabmessungen behandelt und deren Anwendung in Microsoft Dynamics 365 Commerce beschrieben.

Dynamics 365 Commerce unterstützt die Verwendung von Größe, Stil und Farbabmessungen um Produktvarianten zu unterscheiden. Bemaßungen werden normalerweise als Textwerte angezeigt, z. B. Klein, Mittel und Groß für Größen und Schwarz und Braun für Farben. Wenn ein Produkt jedoch viele Variationen unterstützt, kann es schwierig sein, in Produktvarianten zu suchen, weil mehrere Auswahlen erforderlich sind, um das Bild für jede Produktvariante anzuzeigen. Um das Durchsuchen von Produktvarianten zu vereinfachen, kann die Version 10.0.20 von Commerce Bilder und hexadezimalen (hexadezimale) Codes verwenden, um Abmessungen als Farbfelder anzuzeigen.

Im Commerce Website-Generator werden Abmessungsinstellungen unter **Seiteneinstellungen \> Erweiterungen \> Abmessungsverwaltung** definiert. Die folgende Abbildung zeigt ein Beispiel für die Abmessungseinstellungen im Website-Generator.

![Beispiel für Website-Einstellungen im Commerce Website-Generator.](./dev-itpro/media/swatch_site_settings.PNG)

Es stehen zwei Abmessungseinstellungen zur Verfügung:

- **Abmessungen, die als Bild angezeigt werden sollen** – Geben Sie an, welche Ambessungen auf E-Commerce-Websiteseiten als Farbfelder angezeigt werden sollen, z. B. auf Produktdetailseiten (PDPs) und Seiten mit Suchergebnislisten. Jede Kombination aus Farbe, Größe und Stilabmessungen kann als Farbfeld angezeigt werden. Wenn eine Abmessung für die Anzeige als Farbfeld ausgewählt ist, sucht das Commerce Modul Rendering nach einer verfügbaren Konfiguration eines Hexadezimalcode-Farbfelds. Wenn kein Hexadezimalcode konfiguriert ist, sucht die Systemlogik nach einer Konfiguration eines Bild-URL-Farbfelds. Wenn weder ein Hexadezimalcode noch eine Bild-URL konfiguriert sind, wird Text angezeigt.

    Die folgende Abbildung zeigt ein Beispiel, in dem ein PDP als E-Commerce Site einschließlich Farb- und Größenfelder angezeigt wird. In diesem Beispiel wird ein Hexadezimalcode für die Farbdimension konfiguriert. Daher werden Farbfelder als Farben angezeigt. Für die Größenabmessung ist jedoch weder ein Hexadezimalcode noch eine Bild-URL konfiguriert. Daher wird Text angezeigt.

    ![Beispiel für die Farbabmessung, die auf einer E-Commerce-Produktdetailseite als Farbfelder angezeigt wird.](./dev-itpro/media/swatch_pdp.png)

- **Abmessungen, die auf der Produktkarte angezeigt werden sollen** – Geben Sie an, welche Abmessungen auf Produktkarten angezeigt werden sollen, die in Listen und auf Listenseiten angezeigt werden. Bevor eine Abmessung auf einer Produktkarte angezeigt werden kann, muss diese Einstellung für diese Abmessung aktiviert werden. Die Einstellung **Abmessungen, die als Bild angezeigt werden sollen** sollte auch aktiviert sein. Das Farbfeldauswahlverhalten auf Produktkarten ist für die Farbabmessung optimiert. Für andere Dimensionen ist möglicherweise eine Ansichtserweiterung erforderlich, um das Farbfeldauswahlverhalten anzupassen.

    Die folgende Abbildung zeigt ein Beispiel, in dem eine Listenseite auf einer E-Commerce-Website Produktkarten mit Farbfeldern enthält.

    ![Beispiel für die Farbabmessung, die auf einer E-Commerce-Produktlistenseite als Farbfelder angezeigt wird.](./dev-itpro/media/swatch_searchresults.PNG)

Informationen zum Konfigurieren der Produktabmessungen, sodass sie auf den Websiteseiten als Farbfelder angezeigt werden, finden Sie unter [Konfigurieren Sie Produktdimensionswerte so, dass sie als Farbfelder angezeigt werden](./dev-itpro/dimensions-swatch.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Suchergebnismodul](search-result-module.md)

[Kauffeldmodul](add-buy-box.md)

[Konfigurieren Sie Produktdimensionswerte so, dass sie als Farbfelder angezeigt werden](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
