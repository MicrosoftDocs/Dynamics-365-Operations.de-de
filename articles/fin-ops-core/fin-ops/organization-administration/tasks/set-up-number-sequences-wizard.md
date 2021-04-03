---
title: Einrichten von Nummernkreisen mit einem Assistenten
description: In diesem Abschnitt wird erläutert, wie Sie mit Hilfe eines Assistenten alle erforderlichen Zahlenreihen gleichzeitig einrichten können.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b79924e2c8d94b5e5e160a123e9b0cde0971fd96
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560482"
---
# <a name="set-up-number-sequences-using-a-wizard"></a>Einrichten von Nummernkreisen mit einem Assistenten

[!include [banner](../../includes/banner.md)]

Nummernkreise dienen zum Generieren von lesbaren, eindeutigen Kennungen für Masterdaten- und Buchungsdatensätze, die diese benötigen. Ein Masterdaten- oder Buchungsdatensatz, der eine Kennung erfordert, wird als Referenz bezeichnet. Bevor neue Datensätze für eine Referenz erstellt werden können, muss ein Nummernkreis eingerichtet und der Referenz zugeordnet werden. In diesem Abschnitt wird erläutert, wie Sie mit Hilfe eines Assistenten alle erforderlichen Zahlenreihen gleichzeitig einrichten können. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.

1. Gehen Sie zu **Navigation > Module > Organisationsverwaltung > Zahlenreihen > Zahlenreihen**.
2. Wählen Sie **Generieren**.
3. Wählen Sie **Weiter**.

   - Auf dieser Seite können der Kennungscode, der niedrigste Wert und der höchste Wert geändert werden. Zudem kann auf dieser Seite angegeben werden, ob der aktuelle Nummernkreis fortlaufend sein muss.   
   - Wählen Sie die Option **Kontinuierlich** nicht, wenn Sie Zahlen für die Zahlenfolge vorbelegen müssen. Um ein Umfangssegment zum Format einer Zahlenfolge hinzuzufügen, wählen Sie das Format in der Liste aus und wählen Sie dann **Umfang in Format** aufnehmen. Um ein Umfangssegment aus dem Format einer Zahlenfolge zu entfernen, wählen Sie das Format in der Liste aus und wählen Sie dann **Scope aus dem Format** entfernen. Um eine Zahlenfolge von der automatischen Generierung auszuschließen, markieren Sie die Zahlenfolge in der Liste und wählen Sie dann **Löschen**.  

4. Wählen Sie **Weiter**.
5. Wählen Sie **Fertig stellen** aus.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]