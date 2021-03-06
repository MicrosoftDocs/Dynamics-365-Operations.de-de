---
title: Einen Produktionsauftrag mit Vorgängen und Feinterminierung planen
description: In diesem Thema geht es um die Terminierung eines Fertigungsauftrags mit Arbeitsvorbereitung und Arbeitsvorbereitung.
author: ChristianRytt
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 883a68af78a9d91df089d30d8f1b3d7ba498d577
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841382"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Einen Produktionsauftrag mit Vorgängen und Feinterminierung planen

[!include [banner](../../includes/banner.md)]

In diesem Thema geht es um die Terminierung eines Fertigungsauftrags mit Arbeitsvorbereitung und Arbeitsvorbereitung. Es werden keine Einzelvorgänge mit Grobterminierung erstellt. Es werden jedoch Einzelvorgänge mit Feinterminierung erstellt. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF. Dieses Verfahren ist für Produktionsleiter, Produktionsplaner oder Werkstattleiter gedacht, die in einer Einzelfertigungsumgebung arbeiten.


## <a name="create-a-production-order"></a>Produktionsauftrag erstellen
1. Gehen Sie im Navigationsbereich zu **Module > Fertigungssteuerung > Fertigungsaufträge > Alle Fertigungsaufträge**.
2. Wählen Sie **Neuer Fertigungsauftrag**.
3. Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus. Wählen Sie die Artikelnummer **D0001**.  
4. Wählen Sie **Erstellen** aus.

## <a name="schedule-operations-for-the-production-order"></a>Planen von Vorgängen für den Produktionsauftrag
1. Markieren Sie die neu angelegte Zeile.      
2. Wählen Sie im Aktionsbereich **Terminplan**.
3. Wählen Sie **Vorgänge terminieren**.
4. Wählen Sie im Feld **Terminierungsrichtung** **Vorwärts vom Terminierungsdatum**.
5. Geben Sie im Feld **Terminierungsdatum** ein Datum ein. Wählen Sie ein zukünftiges Datum (beispielsweise heute plus eine Woche). Mit der ausgewählten Planungsrichtung wird der Produktionsauftrag vorwärts ab diesem Datum geplant.  
6. Wählen Sie **OK**.
7. Markieren Sie in der Liste die ausgewählte Zeile. Beachten Sie, dass der Status auf **Planung** geändert wird. 
8. Wählen Sie **Alle Aufträge**. Beachten Sie, dass keine Aufträge mit geplanten Vorgängen erstellt werden.  
9. Schließen Sie die Seite.

## <a name="schedule-jobs-for-the-production-order"></a>Planen von Einzelvorgängen für den Produktionsauftrag
1. Wählen Sie im Aktionsbereich **Terminplan**.
2. Wählen Sie **Jobs einplanen**.
3. Wählen Sie im Feld **Terminierungsrichtung** **Vorwärts vom Terminierungsdatum**.
4. Geben Sie im Feld **Terminierungsdatum** ein Datum ein. Wählen Sie ein zukünftiges Datum (beispielsweise heute plus eine Woche). Mit der ausgewählten Planungsrichtung wird der Produktionsauftrag vorwärts ab diesem Datum geplant.  
5. Wählen Sie **OK**.
6. Wählen Sie im Aktionsbereich **Produktionsauftrag**.
7. Wählen Sie **Alle Aufträge**. Beachten Sie, dass (basieren auf der aktiven Route) 5 neue Einzelaufträge mit Feinterminierung erstellt werden.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]