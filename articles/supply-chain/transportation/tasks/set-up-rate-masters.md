--- 
title: Satzmaster einrichten
description: Dieses Verfahren zeigt Ihnen an, wie ein Satzmaster eingerichtet wird.
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
ms.openlocfilehash: b7c02e5a6f5eeee270ca4b6f91e90f7799c2ca11
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-rate-masters"></a>Satzmaster einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt Ihnen an, wie ein Satzmaster eingerichtet wird. Der Logistik-Manager legt normalerweise Satzmaster fest, abhängig von Verträgen mit den Spediteuren. In diesem Szenario richten Sie einen Satzmaster für eine Luftfahrtgesellschaft ein. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="set-up-rate-master"></a>Satzmaster einrichten
1. Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Bewertung" > "Satzmaster".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Satzmaster" einen Wert ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Klicken Sie im Feld "Metadatenkennung bewerten" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Bewertungsmetadaten-Kennung bestimmt die Daten, die für den Satzmaster erforderlich sind, indem sie die Metadaten definiert, die über das TMS-Modul mithilfe dieses Satzmasters erwartet werden.  
6. Für dieses Beispiel die P2P-Option auswählen
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie auf "Speichern".

## <a name="set-up-rate-base"></a>Satzbasis einrichten
1. Klicken Sie auf "Satzbasis".
    * Die Satzbasis bestimmt den Satz des Spediteurs und kann verwendet werden, um eine Tarifstruktur einzurichten, da sie die Sätze in den Breakpoints strukturiert, die im Pausenmaster definiert werden.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Satzbasis" einen Wert ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Klicken Sie im Feld "Umbruchmaster" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Pausenmaster werden verwendet, um die Preisgestaltungsstruktur und die Breakpoints zu definieren. Die Preisgestaltungsstruktur verwendet abgestufte Preisgestaltung auf Grundlage der physischen Dimensionen.  
6. Für dieses Beispiel verwenden Sie Gewicht
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Schalten Sie die Erweiterung des Abschnitts "Details" ein/aus.
9. Klicken Sie auf Neu.
10. Geben Sie im Feld "Postleitzahl der Lieferung ab" "30301 "ein.
11. Geben Sie im Feld "Postleitzahl der Lieferung bis" "30318 "ein.
12. Geben Sie im Feld "Land/Region für Einlieferung" "USA" ein.
13. Geben Sie im Feld "<1,00 kg" "100" ein.
    * Fügen Sie den Preis pro Kilogramm ein, wenn das Gesamtgewicht der Auslastung kleiner als 1 Pfund ist.  
14. Geben Sie im Feld <"5.00 kg" "300" ein.
    * Fügen Sie den Preis pro Kilogramm ein, wenn das Gesamtgewicht der Auslastung kleiner als 5 Pfund ist.  
15. Geben Sie im Feld <"20.00 kg" "500" ein.
    * Fügen Sie den Preis pro Kilogramm ein, wenn das Gesamtgewicht der Auslastung kleiner als 20 Pfund ist.  
16. Geben Sie im Feld <"100.00 kg" "1000" ein.
    * Fügen Sie den Preis pro Kilogramm ein, wenn das Gesamtgewicht der Auslastung kleiner als 100 Pfund ist.  
17. Geben Sie im Feld <"1,000.00 kg" "3000" ein.
    * Fügen Sie den Preis pro Kilogramm ein, wenn das Gesamtgewicht der Auslastung kleiner als 1000 Pfund ist.  
18. Klicken Sie auf "Speichern".
19. Schließen Sie die Seite.

## <a name="assign-rate-base"></a>Satzbasis zuweisen
1. Schalten Sie die Erweiterung des Satzbasiszuweisungs-Abschnitts ein/aus.
2. Klicken Sie auf "Neu".
    * Sie können mehrere Satzbasiszuweisungen für jeden Satzmaster haben. Auf diese Weise ist es möglich, mehrere verschiedene Preispunkte für jeden Spediteur abhängig von Zielen, Dienstleistungen oder unterschiedlichen Satzbasen zu erstellen. In diesem Verfahren erstellen Sie nur eine Satzbasiszuweisung.  
3. Geben Sie im Feld "Name" einen Wert ein.
4. Klicken Sie im Feld "Satzbasis" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Klicken Sie im Feld "Dienstleistung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Geben Sie im Feld "Postleitzahl für Abholung" "98052" ein.
    * Geben Sie an, für welche Postleitzahl diese Satzbasiszuweisung gültig sein soll aus.    
10. Geben Sie im Feld "Land/Region für Abholung" "USA" ein.
11. Klicken Sie auf "Speichern".


