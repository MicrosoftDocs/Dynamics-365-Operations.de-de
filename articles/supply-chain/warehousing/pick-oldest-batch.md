---
title: "Älteste Charge auf einem mobilen Gerät entnehmen"
description: "In diesem Thema wird beschrieben, wie Sie die Optionen für die älteste Charge auf einem mobilen Gerät einrichten und anwenden."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 929c55559f1eac9681e632572ffee71bf83158de
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a>Älteste Charge auf einem mobilen Gerät entnehmen

[!include [banner](../includes/banner.md)]

Sie können auf die Konfiguration **Älteste Charge entnehmen** über ein Menü auf dem mobilen Gerät zugreifen. Zudem können Sie Arbeitskräfte zwingen oder warnen, die älteste Charge an deren aktuellen Lagerplatz zu entnehmen.  

## <a name="where-it-applies"></a>Wofür es angewendet wird
Die Entnahme der ältesten Charge wird über Menüoptionen auf dem mobilen Gerät konfiguriert und wirkt sich auf die Entnahme von Artikeln der ältesten Charge aus.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>So richten Sie die Konfiguration für die Entnahme der ältesten Charge ein 
Für Artikel, die für vorhandene Arbeit genutzt werden sollen, können Sie über das Menü des mobilen Geräts die Option für **Älteste Charge entnehmen** auf Werte wie **Keine**, **Warnen** oder **Erzwingen** setzen.

**Keine**: Arbeitskräfte enthalten keine Nachrichten. Sie sind befugt, jede Charge von ihrem Lagerplatz zu entnehmen.

**Warnen** und **Erzwingen**: Eine Liste der Chargen mit dem ältesten Ablaufdatum wird über der Chargenkontrolle anzeigt, wenn die Arbeitskraft eine Charge auswählt. Wenn der Speicherort durch Ladungsträger kontrolliert wird, wird eine Liste mit Ladungsträgern, bei denen die älteste Charge über der Ladungsträgerkontrolle erscheint, angezeigt. 
-   **Warnen**: Wenn die Arbeitskraft einen Ladungsträger oder eine Charge auswählt, die nicht auf der Liste angezeigt wird, ist das Steuerelement leer und es wird eine Warnung angezeigt, dass eine ältere Charge ausgewählt werden kann. Damit die Arbeitskraft mit der Arbeit fortfahren kann, kann Sie denselben Ladungsträger oder dieselbe Charge erneut auswählen.  
-   **Erzwingen**: Arbeitskräfte erhalten weiterhin Meldung dahingehend, dass eine ältere Charge zur Verfügung steht.

