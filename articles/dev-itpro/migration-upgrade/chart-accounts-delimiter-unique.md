---
title: Kontenplan-Trennzeichen muss eindeutig sein
description: "In Dynamics 365 for Finance and Operations können Sie nicht dasselbe Trennzeichen für den Kontenplan und die Dimensionswerte haben. Sie müssen die Trennzeichenwerte nach dem Upgrade ändern."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c9728714944b54f3bff1e2a8b43c7adcf5200f08
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="chart-of-accounts-delimiter-must-be-unique"></a>Kontenplan-Trennzeichen muss eindeutig sein

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics AX 2012 können Sie die gleichen Trennzeichen für den Kontenplan und Dimensionswerte verwenden. In Dynamics 365 for Finance and Operations können Sie nicht dasselbe Trennzeichen für den Kontenplan und die Dimensionswerte haben. Wenn ein Trennzeichen doppelt vorkommt, können Sie es nach dem Upgrade ändern. 

Diese Funktion ist verfügbar in:
- Dynamics 365 for Finance and Operations – Version 8.0
- Dynamics 365 for Finance and Operations, Version 7.1, KB 4094701 – Die Finanzdimensionen können nicht eingegeben werden, wenn die Dimensionswerte das Trennzeichen für den Kontenplan enthalten
- Dynamics 365 for Finance and Operations, Version 7.2, KB 4092967 – Unterprojekt kann nicht als Dimension ausgewählt werden, wenn das Unterprojektformat das Dimensionstrennzeichen enthält

## <a name="update-delimiter"></a>Trennzeichen aktualisieren
Bei einem Konflikt mit dem Kontenplan kann das Kontenplan-Trennzeichen und das Projekt-/Unterprojekt-ID-Format geändert werden. Keine anderen Dimensionstrennzeichen können geändert werden. 
- Sie können das Kontenplan-Trennzeichen nach dem Upgrade zu Finance and Operations in **Hauptbuchparameter** > **Kontenplan und Dimensionen** > **Trennzeichen ändern** ändern. 
- Wenn es nur einen Konflikt mit dem Projekt-/Unterprojekt-ID-Format gibt, können Sie diesen Wert in **Projektverwaltung und Buchhaltungsparameter** > **Allgemein** > **Unterprojektformat ändern** ändern. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>So wird festgestellt, ob Ihre Umgebung aktualisierte Trennzeichen benötigt 
Wenn Trennzeichen in Ihrer aktualisierten Umgebung Konflikte verursachen, kommt es möglicherweise zu einer Instabilität, wenn Werte in einem segmentierten Eingabesteuerelement oder einem Dimensionseingabe-Steuerelement eingegeben werden. Das bedeutet, dass Sie immer Suchen oder ein Flyoutmenü verwenden müssen, wenn Sie Konten- und Dimensionskombinationen eingeben.

