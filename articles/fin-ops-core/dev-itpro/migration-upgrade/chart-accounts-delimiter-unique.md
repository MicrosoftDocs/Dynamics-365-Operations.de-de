---
title: Eindeutiges Trennzeichen für den Kontenplan erstellen
description: In diesem Artikel wird erläutert, wie Sie nicht die gleichen Trennzeichen für den Kontenplan und die Dimensionswerte verwenden können. Sie müssen die Trennzeichenwerte nach dem Upgrade ändern.
author: panolte
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 2fd29d747c7141b051e6c7c68db94abfd849f947
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123495"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Erstellen eines eindeutigen Trennzeichens für den Kontenplan

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics AX 2012 können Sie die gleichen Trennzeichen für den Kontenplan und Dimensionswerte verwenden. In den aktuellen Versionen von Finanzen und Betrieb können Sie für den Kontenplan und die Namen bzw. Werte der Dimensionen nicht dasselbe Begrenzungszeichen verwenden. Wenn ein Trennzeichen doppelt vorkommt, können Sie es nach dem Upgrade ändern. 

## <a name="update-delimiter"></a>Trennzeichen aktualisieren
Bei einem Konflikt mit dem Kontenplan kann das Kontenplan-Trennzeichen und das Projekt-/Unterprojekt-ID-Format geändert werden. Keine anderen Dimensionstrennzeichen können geändert werden. 
- Sie können das Kontenplan-Trennzeichen nach dem Upgrade in **Hauptbuchparameter** > **Kontenplan und Dimensionen** > **Trennzeichen ändern** ändern. 
- Wenn es nur einen Konflikt mit dem Projekt-/Unterprojekt-ID-Format gibt, können Sie diesen Wert in **Projektverwaltung und Buchhaltungsparameter** > **Allgemein** > **Unterprojektformat ändern** ändern. 

### <a name="other-considerations"></a>Weitere Überlegungen
Ähnlich wie bei der Projekt-/Teilprojekt-ID sollten auch alle anderen als finanzielle Dimensionen verwendeten Datensätze, wie z.B. Lieferanten oder Kunden, keine Konto-ID-Werte haben, die dasselbe Zeichen wie das Begrenzungszeichen des Kontenplans verwenden. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>So wird festgestellt, ob Ihre Umgebung aktualisierte Trennzeichen benötigt 
Wenn Trennzeichen in Ihrer aktualisierten Umgebung Konflikte verursachen, kommt es möglicherweise zu einer Instabilität, wenn Werte in einem segmentierten Eingabesteuerelement oder einem Dimensionseingabe-Steuerelement eingegeben werden. Das bedeutet, dass Sie immer Suchen oder ein Flyoutmenü verwenden müssen, wenn Sie Konten- und Dimensionskombinationen eingeben.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

