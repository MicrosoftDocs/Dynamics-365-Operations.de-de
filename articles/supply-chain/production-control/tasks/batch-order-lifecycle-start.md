---
title: Chargenauftragslebenszyklus von der Erstellung bis zum Start
description: Diese Prozedur führt Sie durch den ersten Teils des Lebenszyklus eines Chargenauftrags.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5fd04587c95ba8a48750f96302a11aeaf82308d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981405"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Chargenauftragslebenszyklus von der Erstellung bis zum Start

[!include [banner](../../includes/banner.md)]

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

