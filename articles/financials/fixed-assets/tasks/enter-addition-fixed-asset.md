---
title: Eingeben einer Anlagenerweiterung für eine Anlage
description: Diese Prozedur zeigt an, wie einer vorhandenen Anlage einer Erweiterung hinzugefügt wird.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c9733f07f995dd37669f3c33fd0f082daa34dd2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566937"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a>Eingeben einer Anlagenerweiterung für eine Anlage

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt an, wie einer vorhandenen Anlage einer Erweiterung hinzugefügt wird. Der Zweck der Anlagenerweiterungen besteht darin, Artikelerweiterungen, Verwaltung oder Verbesserungen für eine Anlage nachzuverfolgen und dient nur zur Information. Sämtliche Änderungen am Anlagenwert oder der Nutzungsdauer müssen separat vorgenommen werden.   



Die Prozedur verwendet die "Buchhalterrolle" und die Demodaten für die juristische Person USMF.

1. Wechseln Sie zu Anlagen > Anlagen > Anlagen.
2. Suchen Sie in der Liste die Anlage für die Erweiterung und wählen Sie diese aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie im Aktivitätsbereich auf "Anlage".
5. Klicken Sie auf "Anlagenerweiterungen".
6. Klicken Sie auf Neu.
7. Geben Sie im Feld "Name" einen Wert ein.
8. Legen Sie das Datum des Erweiterungseinkaufs oder des Erweiterungsdienstes fest.
9. Geben Sie die Kosten für den Artikel, die Wartung oder für andere Verbesserungen für die Anlage ein.
10. Geben Sie im Feld "Menge" eine Zahl ein.
    * Die Gesamtkosten haben keine Auswirkungen auf den Wert der Anlage und dienen nur Nachverfolgungs- und Informationszwecken. Wenn die Kosten aktiviert werden, muss eine Höherbewertungstransaktion separat gebucht werden.  
11. Klicken Sie auf die Registerkarte "Allgemein".
    * Legen Sie "Verlängert die Nutzungsdauer" fest, falls die Erweiterung die Nutzungsdauer der Anlage erhöht.  
    * Dieses Feld dient nur zur Information. Um die Nutzungsdauer zu erhöhen, ändern Sie die "Nutzungsdauer" in den "Wertmodellen" und/oder den "Abschreibungsbüchern" für die Anlage.  

