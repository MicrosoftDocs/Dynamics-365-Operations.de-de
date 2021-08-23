---
title: Eingeben einer Anlagenerweiterung für eine Anlage
description: Diese Prozedur zeigt an, wie einer vorhandenen Anlage einer Erweiterung hinzugefügt wird.
author: saraschi2
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 966fd191ad876aae86ff2511d6981b0437679becbe4984b087c1975dece351b6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742952"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a>Eingeben einer Anlagenerweiterung für eine Anlage

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt an, wie einer vorhandenen Anlage einer Erweiterung hinzugefügt wird. Der Zweck der Anlagenerweiterungen besteht darin, Artikelerweiterungen, Verwaltung oder Verbesserungen für eine Anlage nachzuverfolgen und dient nur zur Information. Sämtliche Änderungen am Anlagenwert oder der Nutzungsdauer müssen separat vorgenommen werden.   

Die Prozedur verwendet die "Buchhalterrolle" und die Demodaten für die juristische Person USMF.

1. Wechseln Sie im Navigationsbereich zu **Module > Anlagen > Anlagen > Anlagen**.
2. Suchen Sie in der Liste die Anlage für die Erweiterung und wählen Sie diese aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie im Aktivitätsbereich auf **Anlage**.
5. Klicken Sie auf **Anlagenerweiterungen**.
6. Klicken Sie auf **Neu**.
7. Geben Sie im Feld **Name** einen Wert ein.
8. Legen Sie im Feld **Anschaffungsdatum** das Datum des Erweiterungseinkaufs oder des Erweiterungsdienstes fest.
9. Geben Sie im Feld **Einheitenkosten** die Kosten für den Artikel, die Wartung oder für andere Verbesserungen an der Anlage ein.
10. Geben Sie im Feld **Menge** eine Zahl ein. Die Gesamtkosten haben keine Auswirkungen auf den Wert der Anlage und dienen nur Nachverfolgungs- und Informationszwecken. Wenn die Kosten aktiviert werden, muss eine Höherbewertungstransaktion separat gebucht werden.  
11. Klicken Sie auf die Registerkarte **Allgemein**.

    * Legen Sie **Verlängert die Nutzungsdauer** auf **Ja** fest, falls die Erweiterung die Nutzungsdauer der Anlage erhöht.  
    * Dieses Feld dient nur zur Information. Um die Nutzungsdauer zu erhöhen, ändern Sie die "Nutzungsdauer" in den "Wertmodellen" und/oder den "Abschreibungsbüchern" für die Anlage.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]