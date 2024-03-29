---
title: Einen Produktionsauftrag mit Vorgängen und Feinterminierung planen
description: In diesem Artikel geht es um die Terminierung eines Fertigungsauftrags mit Arbeitsvorbereitung und Arbeitsvorbereitung.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d82d5439e57c02ddc9db4222a946bd15f4ed67e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903926"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Einen Produktionsauftrag mit Vorgängen und Feinterminierung planen

[!include [banner](../../includes/banner.md)]

In diesem Artikel geht es um die Terminierung eines Fertigungsauftrags mit Arbeitsvorbereitung und Arbeitsvorbereitung. Es werden keine Einzelvorgänge mit Grobterminierung erstellt. Es werden jedoch Einzelvorgänge mit Feinterminierung erstellt. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF. Dieses Verfahren ist für Produktionsleiter, Produktionsplaner oder Werkstattleiter gedacht, die in einer Einzelfertigungsumgebung arbeiten.


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