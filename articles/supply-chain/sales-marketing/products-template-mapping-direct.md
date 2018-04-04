---
title: Produkte direkt von Finance and Operations mit Produkten in Sales synchronisieren
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Sales zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3ae50372edcd473f2288f8172b71eac33e24b636
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a>Produkte direkt von Finance and Operations mit Produkten in Sales synchronisieren

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration) vertraut sein.

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Produkte direkt aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Sales zu synchronisieren.

## <a name="data-flow-in-prospect-to-cash"></a>Datenfluss in Interessent nach Bargeld

Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Finance and Operations und Sales hinweg zu synchronisieren. Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Finance and Operations und Sales. Die folgende Abbildung zeigt, wie Daten zwischen Finance and Operations und Sales synchronisiert werden.

[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [PowerApps-Administrator-Center](https://preview.admin.powerapps.com/dataintegration). Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.

Die folgenden Vorlagen und grundlegenden Aufgaben werden für die Synchronisierung von Konten aus Sales für Kunden in Finance and Operations verwendet:

- **Name der Vorlage in der Datenintegration:** Produkte (Finance and Operations zu Sales) - direkt
- **Name der Aufgaben im Datenintegrationsprojekt**: Podukte

Keine Synchronisierungsaufgaben sind erforderlich, damit Produktsynchronisierung auftreten kann.

## <a name="entity-set"></a>Entitätssatz

| Finance and Operations     | Vertrieb    |
|----------------------------|----------|
| Freigegebene Produkte für Verkauf | Produkte |

## <a name="entity-flow"></a>Entitätsfluss

Produkte werden in Finance and Operations verwaltet und mit Sales synchronisiert. Die **Verkäufliche freigegebene Produkte**-Datenentität im Bereich Finance and Operations exportiert nur Produkte, die *verkäuflich* sind. Verkäufliche Produkte sind Produkte, die die Informationen enthalten, die diese benötigen, damit sie in Aufträgen verwendet werden können. Die gleichen Regeln gelten, wenn ein Produkt mit der Funktion **Überprüfen** auf der Seite **Freigegebenes Produkt** überprüft wird.

Die Produktnummer wird als Schlüssel verwendet. Wenn Produktvarianten mit Sales synchronisiert werden, hat jede eine Produktvariante individuelle Produkt-Kennung

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales

In Sales wurde ein neues Feld **Wird extern verwaltet** bei Produkten hinzugefügt, um anzugeben, dass ein bestimmtes Produkt extern verwaltet wird. Der Wert wird beim Import nach Sales standardmäßig auf **Ja** festgelegt. Folgende Werte sind verfügbar:

- **Ja** – Das Produkt, stammt aus Finance and Operations und wird nicht in Sales bearbeitet.
- **Nein** – Das Produkt wurde direkt in Sales eingegeben.
- **(Kein Wert)** – Das Produkt war in Sales vorhanden, bevor der Interessent für Bargeldlösung aktiviert wurde.

Das Feld **Wird extern verwaltet** hilft, sicherzustellen, dass nur Angebote und Aufträge mit Extern verwalteten Produkten mit Finance and Operations synchronisiert werden.

Extern verwaltete Produkte werden automatisch der ersten gültigen Preisliste mit derselben Währung hinzugefügt. Preislisten sind alphabetisch sortiert nach Name. Der Produktverkaufspreis von Finance and Operations wird als Preis in der Preisliste verwendet. Vergewissern Sie sich daher, dass Preislisten in Sales für jede Produktverkaufswährung in Finance and Operations vorhanden sind. Die Währung für die freigegebenen verkäuflichen Produkte ist auf die Buchhaltungswährung in der juristischen Person festgelegt, von der das Produkt exportiert wird.

> [!NOTE]
> Produktsynchronisierung erfolgt nicht, es sei denn, es gibt eine Liste mit Preisen, die eine entsprechende Währung haben.

## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung

- Bevor Sie die allererste Synchronisierung ausführen, müssen Sie die Tabelle eindeutig identifizierbarer Produkte für vorhandene Produkte in Finance and Operations auffüllen. Vorhandene Produkte werden nicht synchronisiert, bis der Einzelvorgang abgeschlossen ist.

    1. In Finance and Operations verwenden Sie Suche, um nach **Tabelle eindeutig identifizierbarer Produkte auffüllen** zu suchen.
    2. Klicken Sie auf **Tabelle eindeutig identifizierbarer Produkte auffüllen**, um den Einzelvorgang auszuführen. Dieser Vorgang muss nur einmal aktiviert werden.

- Vergewissern Sie sich, dass die erforderliche Wertzuordnung für die Verkaufsmaßeinheit (ME) zwischen Finance and Operations und Sales in der Zuordnung von **SalesUnitSymbol** zu **DefaultUnit (Name)** vorhanden ist.
- Aktualisieren Sie Wertzuordnung für **Einheitengruppe** (**defaultuomscheduleid.name**), um den **Einheitengruppen** in Sales zu entsprechen.

    Der Vorlagenwert ist standardmäßig auf **Standardeinheit** festgelegt.

- Stellen Sie sicher, dass alle Maßseinheiten für Produktverkäufe von Finance and Operations in Sales vorhanden sind.
- Vergewissern Sie sich, dass Preislisten in Sales für jede Produktverkaufswährung in Finance and Operations vorhanden sind.
- Wenn Produkte in Sales erstellt werden, können sie den Status **Entwurf** oder **Aktiv** besitzen. Das Verhalten wird mit **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Verkäufe** in Sales gesteuert.

    Produkte, die den Status **Entwurf** besitzen, wenn sie erstellt werden, müssen aktiviert werden, bevor sie in Anführungszeichen gesetzt oder ausgewählten Aufträgen hinzugefügt werden können.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator. 

> [!NOTE]
> Die Zuordnung zeigt, welche Feldinformationen von Sales zu Finance and Operations synchronisiert werden.

![Vorlagenzuordnung im Datenintegrator](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Verwandte Themen

[Interessent zu Bargeld](prospect-to-cash.md)

[Konten von Sales direkt mit Debitoren in Finance and Operations synchronisieren](accounts-template-mapping-direct.md)

[Kontakte direkt von Sales mit Kontakten oder Debitoren in Finance and Operations synchronisieren](contacts-template-mapping-direct.md)

[Auftragskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren](sales-order-template-mapping-direct-two-ways.md)

[Verkaufsrechnungskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren](sales-invoice-template-mapping-direct.md)




