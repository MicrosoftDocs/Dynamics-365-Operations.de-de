---
title: "Chargen- und Kennzeichenbestätigung"
description: "In diesem Thema wird beschrieben, wie Sie Chargen- und Kennzeichenbestätigung über ein mobiles Gerät einrichten und anwenden."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 70a8c18560f0cfc7a44625520f2f035a6004618a
ms.contentlocale: de-de
ms.lasthandoff: 06/20/2017


---

# <a name="batch-and-license-plate-confirmation"></a>Chargen- und Kennzeichenbestätigung

[!include[banner](../includes/banner.md)]

Chargenbestätigung ermöglicht Ihnen, zu bestätigen, dass die richtige Charge vom mobilen Gerät gewählt wird. Nur bei der ersten Arbeitsentnahme für Artikel aus Chargen oberhalb, wobei *Charge oberhalb* angibt, dass die Charge in der Suchenhierarchie höher reicht, als der Lagerplatz, müssen Sie überprüfen, dass die entnommene Charge mit der Charge auf der Arbeitsposition übereinstimmt. 

Kennzeichenbestätigung ermöglicht Ihnen, zu bestätigen, dass die richtige Kennzeichen vom mobilen Gerät gewählt wird. Wenn Arbeit aus einem Phasenlagerplatz entnommen wird, müssen Sie überprüfen dass das entnommene Kennzeichen mit dem Kennzeichen übereinstimmt, das der Arbeit zugeordnet ist. Wenn die Arbeit gestartet wird, indem ein Kennzeichen gescannt wird, wird dieser Bestätigungsschritt übersprungen.

## <a name="where-it-applies"></a>Wofür es angewendet wird
Bestätigung gilt in den folgenden Szenarien:

- Chargenbestätigung gilt für die erste Entnahme der Arbeit für Artikel der Chargen oberhalb.
- Kennzeichenbestätigung gilt für Entnahmen aus den Phasenlagerplätzen.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Chargen- und Kennzeichenbestätigung einrichten
Sie können Chargen- und Kennzeichenbestätigung von den Menüeinträgen des mobilen Geräts aus konfigurieren.  
1.  Geben Sie im Menüeintrag des mobilen Geräts die Einrichtung der Arbeitsbestätigung ein.  
2.  Wählen Sie die Option für Kennzeichen- oder Chargen-Bestätigung aus. Beide Optionen sind für Arbeitstypentnahmen verfügbar, bei denen keine automatische Bestätigung aktiviert ist.  

