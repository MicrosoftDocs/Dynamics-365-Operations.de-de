--- 
title: "Hub-Zusatzgebühren und Zusatzleistungsmaster einrichten"
description: "Im folgenden Verfahren wird dargestellt, wie ein Zusatzleistungsmaster für einen Hub erstellt und dieser Master verwendet wird, um eine Hub-Zusatzgebühr zu erstellen."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6381416640ffacf0a9d96d7da96bc33612ca7137
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a>Hub-Zusatzgebühren und Zusatzleistungsmaster einrichten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Im folgenden Verfahren wird dargestellt, wie ein Zusatzleistungsmaster für einen Hub erstellt und dieser Master verwendet wird, um eine Hub-Zusatzgebühr zu erstellen. Das Verfahren verwendet das USMF-Dataset. Diese Einstellung wird normalerweise von einem Transportkoordinator vorgenommen.


## <a name="set-up-a-hub-master"></a>Einen Hubmaster einrichten
1. Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Bewertung" > "Zusatzleistungsmaster".
2. Klicken Sie auf "Neu".
3. Geben Sie einen Wert in das Feld "Zusatzleistungsmaster" ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Wählen Sie im Feld "Zusatzleistungstyp" "Hub" aus.
6. Klicken Sie auf "Speichern".
7. Schließen Sie die Seite.

## <a name="set-up-a-hub-accessorial-charge"></a>Hubzusatzgebühr einrichten
1. Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Bewertung" > "Hubzusatzgebühren".
2. Klicken Sie auf "Neu".
3. Geben Sie einen Wert in das Feld "Kennung für Hubzusatzgebühren" ein.
4. Klicken Sie im Feld "Hub" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
6. Wählen Sie im Feld "Hubposition" eine Option aus.
    * Sie können den Zuschlag entweder als Abholung oder Lieferung erstellen. Je nach getroffener Auswahl wird der Zuschlag dem entsprechenden Transportsegment auf den Arbeitsplan angewendet.  
7. Klicken Sie im Feld "Zusatzleistungsmaster" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie den Master aus, den Sie soeben erstellt haben.  
9. Klicken Sie auf "Speichern".
10. Schließen Sie die Seite.


