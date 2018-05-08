---
title: Unterlieferungs-Wiederbeschaffungsauftrag erstellen
description: "Dieses Verfahren zeigt, wie ein Unterlieferungs-Wiederbeschaffungsauftrag erstellt wird, in dem Sie die erwartete Lieferung von einem Kreditor in den Lieferungsbestand verfolgen können."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f7f8005ec9e723c94d53e6ab81f04ee388c83faa
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-consignment-replenishment-order"></a>Unterlieferungs-Wiederbeschaffungsauftrag erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie ein Unterlieferungs-Wiederbeschaffungsauftrag erstellt wird, in dem Sie die erwartete Lieferung von einem Kreditor in den Lieferungsbestand verfolgen können. Es zeigt auch, wie einen Produktempfang erfassen, damit der Lieferungsbestand als verfügbarer Lagerbestand im Besitz des Kreditors erfasst wird. Diese Prozedur würde normalerweise durch einen Beschaffungsspezialist durchgeführt. Sie können diese Anleitung im Demodatenunternehmen USMF ausführen. Diese Prozedur ist für eine Funktion gedacht, die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.




## <a name="create-a-consignment-replenishment-order"></a>Unterlieferungs-Wiederbeschaffungsauftrag erstellen
1. Wechseln Sie zu "Beschaffung" > "Lieferung" > "Unterlieferungs-Wiederbeschaffungsaufträge".
2. Klicken Sie auf "Neu".
3. Wählen Sie im Feld "Kreditorenkonto" "US-104" aus.
    * Sie müssen einen Kreditor auswählen, der als Besitzer in der Bestandseigentümerseite erfasst wird.  
4. Klicken Sie auf "OK".
5. Klicken Sie auf "Position hinzufügen".
6. Geben Sie im Feld "Artikelnummer" die Zeichenfolge "M9211CI." ein.
    * Sie müssen ein Artikel ausgewählt, der für Lieferungsbestand eingerichtet wird.  
7. Geben Sie im Feld "Menge" eine Zahl ein.
8. Geben Sie im Feld "Angefordertes Lieferdatum:" ein Datum ein.
    * Die Angefordert und Bestätigt-Daten werden im MRP-Modul für den Wareneingang der erwarteten Waren verwendet.  
9. Geben Sie im Feld "Bestätigtes Lieferdatum" ein Datum ein.
10. Erweitern Sie den Abschnitt "Positionsdetails".
11. Klicken Sie auf die Registerkarte "Lagerungsdimension".
12. Um den Eigentümer im Feld Lagerungsdimensionseigentümer anzuzeigen, aktualisieren der Seite.
    * Kreditor US-104 wird jetzt als Besitzer aufgeführt.  

## <a name="check-the-inventory-transaction-status"></a>Prüfen des Lagerbuchungstatus
1. Klicken Sie auf Lager.
2. Klicken Sie auf "Transaktionen".
3. Markieren Sie in der Liste die ausgewählte Zeile.
    * Beachten Sie, dass das Zugangsfeld auf "Bestellt" festgelegt wird.  
4. Schließen Sie die Seite.

## <a name="receive-items"></a>Artikel empfangen
1. Klicken Sie auf "Produktzugang".
2. Geben Sie im Feld "Externer Produktzugang" einen Wert ein.
3. Geben Sie im Feld "Menge" Sie eine Zahl ein, die geringer ist als die Zahl, die dort angezeigt wird.
4. Klicken Sie auf "OK".

## <a name="check-the-on-hand-inventory"></a>Prüfen des verfügbaren Lagerbestands
1. Klicken Sie auf Lager.
2. Klicken Sie auf "Verfügbar".
3. Klicken Sie auf "Überblick".
    * Die Artikel, die als verfügbarer Lieferungsbestand eingegangen sind, der dem Kreditor gehört, sind der verfügbare Bestand. Die Restmenge wird im auf dem Unterlieferungs-Wiederbeschaffungsauftrag wird im Feld "Insgesamt bestellt" angezeigt.  
4. Schließen Sie die Seite.
5. Klicken Sie auf "Schließen".

