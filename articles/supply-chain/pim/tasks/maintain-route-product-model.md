--- 
title: "Arbeitsplan für ein Produktmodell verwalten"
description: "Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2f3df2bd6018d07d65950398e38821cad475752e
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="maintain-a-route-for-a-product-model"></a>Arbeitsplan für ein Produktmodell verwalten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell. Bei diesem Verfahren wird das Spitzenlautsprechermodell im Vorführungsunternehmen USMF verwendet.


## <a name="add-a-route-operation"></a>Hinzufügen eines Arbeitsplanarbeitsgangs
1. Klicken Sie auf "Produktvariantenmodell-Definition".
2. Klicken Sie auf "Produktkonfigurationsmodelle".
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie den Spitzenlautsprecher für diese Aufgabe aus.  
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Erweitern Sie den Abschnitt "Arbeitsgänge".
6. Klicken Sie auf Hinzufügen.
7. Geben Sie im Feld "Name" einen Wert ein.
8. Geben Sie im Feld "Beschreibung" einen Wert ein.
9. Klicken Sie auf "Speichern".

## <a name="enter-route-operation-details"></a>Eingeben von Arbeitsplanarbeitsgangdetails
1. Klicken Sie auf "Details zum Arbeitsplanarbeitsgang"
2. Geben Sie im Feld 'Arbeitsgang' einen Wert ein, oder wählen Sie einen Wert aus.
3. Geben Sie im Feld Arbeitsgang- Nr. eine Zahl ein.
    * Vorgangsnummer legen die Arbeitsplansequenz fest.  
    * Jede Eigenschaft eines Arbeitsplanvorgang kann einen statischen Wert enthalten oder einem Attribut zugeordnet werden. Die Zuordnung zu einem Attribut arbeitet mit dem Wert, die als Teil der Konfiguration festgelegt ist.  
4. Geben Sie im Feld "Arbeitsplangruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Die Arbeitsgangsteuerungsgruppe bestimmt das grundlegende Verhalten der Nachkalkulation, des Verbrauch und der Einstellungen.  
5. Klicken Sie auf die Registerkarte "Einstellungen".
6. Klicken Sie auf die Registerkarte 'Zeiten'.
7. Geben Sie im Feld Prozessmenge eine Zahl ein.
    * Bestimmen Sie, wie viele während eines Arbeitsgangs verarbeitet werden.  
8. Geben Sie im Feld "Stunden/Zeit" eine Zahl ein.
    * Geben Sie einen Zeitanteil ein.  
9. Wählen Sie das Kontrollkästchen "Festlegen" aus.
10. Geben Sie im Feld "Laufzeit" eine Zahl ein.
    * Bestimmen Sie die Bearbeitungszeit zur Menge, die Sie angegeben haben.  
11. Klicken Sie auf die Ressourcenanforderungsregisterkarte.
12. Klicken Sie auf Hinzufügen.
13. Markieren Sie in der Liste die ausgewählte Zeile.
14. Wählen Sie im Feld "Anforderungstyp" eine Option aus.
    * Entscheiden Sie, ob spezifische Ressourcen oder Funktionen vorhanden sein müssen.  
15. Geben Sie im Feld 'Anforderung' einen Wert ein, oder wählen Sie einen Wert aus.
16. Klicken Sie auf "OK".


