--- 
title: Chargenauftragslebenszyklus von der Erstellung bis zum Start
description: "Diese Prozedur führt Sie durch den ersten Teils des Lebenszyklus eines Chargenauftrags."
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
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: dcb0814ae51f5914654736a957638f7d8be81e3f
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Chargenauftragslebenszyklus von der Erstellung bis zum Start

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur führt Sie durch den ersten Teils des Lebenszyklus eines Chargenauftrags.

Von der Erstellung, über die Vorkalkulation und vom Produktionseinzelvorgang zum tatsächlichen Beginn eines Chargenauftrages.



Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. 



Die Voraussetzungen für die Ausführung der Prozedur mit einem anderen Dataset sind ein freigegebenes Produkt mit einer aktiven Formel und Arbeitsplanversion.


## <a name="create-a-batch-order"></a>Erstellen eines Chargenauftrags
1. Welchsen Sie zu "Alle Produktionsaufträge".
2. Klicken Sie auf "Neuer Chargenauftrag".
3. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
4. Klicken Sie auf Erstellen.
5. Verwenden Sie den Schnellfilter, um im Feld "Produktion" nach dem Wert "b" zu filtern.

## <a name="view-production-formula-and-expected-co-products"></a>Anzeigen von Produktionsformel und erwarteten Kuppelprodukten
1. Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".
2. Klicken Sie auf Formel.
3. Schließen Sie die Seite.
4. Klicken Sie auf Kuppelprodukte.
5. Schließen Sie die Seite.

## <a name="estimate-the-batch-order"></a>Vorkalkulation des Chargenauftrags
1. Klicken Sie auf "Vorkalkulation".
2. Klicken Sie auf "OK".
3. Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".
4. Klicken Sie auf Berechnungsdetails anzeigen
5. Schließen Sie die Seite.

## <a name="release-the-batch-order"></a>Freigeben des Chargenauftrags
1. Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".
2. Klicken Sie auf "Freigabe".
3. Klicken Sie auf "OK".

## <a name="schedule-production-jobs"></a>Planen von Produktionseinzelvorgängen
1. Klicken Sie im Aktivitätsbereich auf "Zeitplan".
2. Klicken Sie auf Einzelvorgänge planen.
3. Wählen Sie "Nein" im Feld "Begrenzte Kapazität" aus.
4. Wählen Sie "Nein" im Feld "Begrenztes Material" aus.
5. Klicken Sie auf "OK".
6. Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".
7. Klicken Sie auf "Alle Einzelvorgänge".
8. Schließen Sie die Seite.

## <a name="start-the-batch-order"></a>Starten des Chargenauftrags
1. Klicken Sie auf "Start".
2. Klicken Sie auf die Registerkarte "Allgemein".
3. Wählen Sie im Feld "Kommissionierliste jetzt buchen" die Antwort "Nein" aus.
4. Klicken Sie auf "OK".
5. Klicken Sie im Aktivitätsbereich auf "Anzeigen".
6. Klicken Sie auf "Kommissionierliste".
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Schließen Sie die Seite.
9. Schließen Sie die Seite.
10. Klicken Sie auf Arbeitsplanliste.
11. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
12. Schließen Sie die Seite.
13. Schließen Sie die Seite.


