---
title: Manuelle Veröffentlichung von Bewertungen und Prüfungen durch einen Moderator aktivieren
description: In diesem Thema wird beschrieben, wie Sie die manuelle Veröffentlichung von Bewertungen und Rezensionen durch einen Moderator in Microsoft Dynamics 365 Commerce aktivieren, und wie Sie Bewertungen und Rezensionen manuell veröffentlichen.
author: gvrmohanreddy
manager: annbe
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 25ae7074fcf39bf4408ea1fa0acfc334281bb254
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675048"
---
# <a name="enable-manual-publishing-of-ratings-and-reviews-by-a-moderator"></a>Manuelle Veröffentlichung von Bewertungen und Prüfungen durch einen Moderator aktivieren

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie die manuelle Veröffentlichung von Bewertungen und Rezensionen durch einen Moderator in Microsoft Dynamics 365 Commerce aktivieren, und wie Sie Bewertungen und Rezensionen manuell veröffentlichen.

Bei der Bewertungs- und Rezensionslösung von Dynamics 365 Commerce werden Azure Cognitive Services verwendet, um Obszönitäten in Rezensionstiteln und -inhalten automatisch zu redigieren und Bewertungen und Rezensionen zu veröffentlichen. Daher ist kein manueller Eingriff erforderlich, um Bewertungen und Rezensionen auf Ihrer E-Commerce-Website zu überprüfen und zu veröffentlichen.

Einige Unternehmen bevorzugen es jedoch möglicherweise, dass Moderatoren Bewertungen manuell überprüfen und genehmigen, bevor sie veröffentlicht werden. Um die manuelle Veröffentlichung von Bewertungen und Rezensionen durch einen Moderator zu aktivieren, müssen Sie die **Moderator für Bewertungen und Rezensionen erforderlich**-Funktion im Commerce Site Builder aktivieren.

## <a name="enable-the-require-moderator-for-ratings-and-reviews-feature-in-commerce-site-builder"></a>Aktivieren Sie die Funktion „Moderator für Bewertungen und Rezensionen erforderlich“ im Commerce-Site-Builder

Um die Funktion **Moderator für Bewertungen und Rezensionen erforderlich** im Commerce-Site-Builder zu aktivieren, führen Sie diese Schritte aus.

1. Navigieren Sie zu **Start \> Bewertungen \> Einstellungen**.
1. Stellen Sie die **Moderator für Bewertungen und Rezensionen erforderlich**-Option auf **Ein**.

> [!NOTE]
> Durch das Aktivieren der **Moderator für Bewertungen und Rezensionen erforderlich**-Funktion stoppen Sie die automatische Veröffentlichung von Bewertungen und Rezensionen, sodass nun eine manuelle Veröffentlichung erforderlich ist. Azure Cognitive Services wird jedoch weiterhin Obszönitäten in Rezensionstiteln und -inhalten entfernen.

<!--![Require moderator for ratings and reviews setting in Commerce site builder.](media/Ratings-reviews-settings-human-moderation.png)-->

## <a name="publish-ratings-and-reviews"></a>Bewertungen und Rezensionen veröffentlichen

Wenn Sie die Funktion **Moderator für Bewertungen und Rezensionen erforderlich** aktivieren, muss ein Moderator Bewertungen und Rezensionen manuell überprüfen, damit sie auf Ihrer E-Commerce-Seite erscheinen.

Führen Sie die folgenden Schritte aus, um Bewertungs- und Rezensionen im Commerce Site Builder zu überprüfen und zu veröffentlichen.

1. Navigieren Sie zu **Bewertungen \> Moderation**.
1. Wenn das **Status**-Feld im Raster für eine Zeile auf **Unveröffentlicht** festgelegt ist, wurde die Bewertung und Rezension in dieser Zeile noch nicht veröffentlicht. Um nur unveröffentlichte Bewertungen und Rezensionen anzuzeigen, wählen Sie **Status: Überprüfung erforderlich** im Statusfilter über dem Raster aus.
1. Wählen Sie eine oder mehrere Bewertungen und Rezensionen mit dem Status **Unveröffentlicht** aus, und wählen Sie dann **Veröffentlichen** in der Befehlsleiste. Die ausgewählten Bewertungen und Rezensionen werden der Veröffentlichungswarteschlange hinzugefügt und erscheinen nach der Veröffentlichung auf der E-Commerce-Site.

> [!NOTE]
> - Nachdem eine Bewertung und eine Rezension veröffentlicht wurden, ändert sich der Statuswert von **Unveröffentlicht** auf einen Nullwert (leeres Feld).
> - Wenn Sie mehrere Bewertungen und Rezensionen mit unterschiedlichem Status auswählen, und dann **Veröffentlichen** wählen, werden Bewertungen und Rezensionen, die noch nicht veröffentlicht wurden, veröffentlicht. Bereits veröffentlichte Bewertungen und Rezensionen werden jedoch nicht erneut veröffentlicht.

Die folgende Abbildung zeigt ein Beispiel, in dem drei unveröffentlichte Bewertungen und Rezensionen auf der Seite **Moderation** im Commerce Site Builder ausgewählt wurden.

![Drei unveröffentlichte Bewertungen und Rezensionen, die auf der Moderationsseite im Commerce-Site-Builder ausgewählt wurden.](media/Ratings-reviews-publishing-reviews.png)

<!--![Dynamics 365 Commerce - Ratings and Review configuration 2](media/Ratings-reviews-published-reviews.png)-->
<!--![Status filter](media/Ratings-reviews-published-reviews-status-filter.png)-->

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Bewertungen und Prüfungen](ratings-reviews-overview.md)
