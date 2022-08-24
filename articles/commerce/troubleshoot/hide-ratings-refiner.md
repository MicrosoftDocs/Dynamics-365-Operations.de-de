---
title: Wenn die Lösung für Bewertungen und Prüfungen nicht aktiviert ist, wird die Bewertungsverfeinerung auf Suchergebnis- und Kategorieseiten angezeigt.
description: Dieser Artikel beschreibt die Problembehandlung zum Ausblenden der Bewertungsverfeinerung auf Suchergebnis- und Kategorieseiten, wenn die Lösung für Bewertungen und Prüfungen von Microsoft Dynamics 365 Commerce nicht aktiviert ist.
author: gvrmohanreddy
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
manager: annbe
ms.openlocfilehash: 28a3cefd6aab81f5e7907bda457763f2306e5a1d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267376"
---
# <a name="ratings-refiner-appears-on-search-results-and-category-pages-when-the-ratings-and-reviews-solution-isnt-enabled"></a>Wenn die Lösung für Bewertungen und Prüfungen nicht aktiviert ist, wird die Bewertungsverfeinerung auf Suchergebnis- und Kategorieseiten angezeigt.

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Problembehandlung zum Ausblenden der Bewertungsverfeinerung auf Suchergebnis- und Kategorieseiten, wenn die Lösung für Bewertungen und Prüfungen von Microsoft Dynamics 365 Commerce nicht aktiviert ist.

## <a name="description"></a>Beschreibung

Die Bewertungsverfeinerung wird auf Suchergebnis- und Kategorieseiten in einem E-Commerce-Kanal angezeiigt, der nicht die Lösung für Bewertungen und Prüfungen verwendet.

## <a name="resolution"></a>Lösung

### <a name="enable-the-hide-rating-setting-in-commerce-site-builder"></a>Einstellung „Bewertung ausblenden“ in Commerce-Website-Generator aktivieren

Gehen Sie folgendermaßen vor, um die Einstellung **Bewertung ausblenden** im Commerce-Website-Generator zu aktivieren, damit die Bewertungsverfeinerung auf Suchergebnis- und Kategorieseiten ausgeblendet wird.

1. Gehen Sie zu **Seiteneinstellungen \> Erweiterungen**.
1. Aktivieren Sie unter **Bewertungen und Überprüfungen** das Kontrollkästchen **Bewertung ausblenden**.
1. Wählen Sie **Speichern und veröffentlichen** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Bewertungen und Prüfungen](../ratings-reviews-overview.md)

[Nutzung von Bewertungen und Prüfungen aktivieren](../opt-in-ratings-reviews.md)
