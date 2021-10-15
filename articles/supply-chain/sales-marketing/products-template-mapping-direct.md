---
title: Produkte direkt von Supply Chain Management mit Produkten in Sales synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgaben, die verwendet werden, um die Produkte aus Dynamics 365 Supply Chain Management mit Dynamics 365 Sales zu synchronisieren.
author: Henrikan
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d7aa4eddf8d6a18b8203785ddd3dca6ff8537067
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573440"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>Produkte direkt von Supply Chain Management mit Produkten in Sales synchronisieren

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Integration von Daten in Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator) vertraut sein.

Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgaben, die verwendet werden, um die Produkte direkt aus Dynamics 365 Supply Chain Management mit Dynamics 365 Sales zu synchronisieren.

## <a name="data-flow-in-prospect-to-cash"></a>Datenfluss in Interessent nach Bargeld

Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Supply Chain Management und Sales hinweg zu synchronisieren. Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Supply Chain Management und Sales. Die folgende Abbildung zeigt, wie Daten zwischen Supply Chain Management und Sales synchronisiert werden.

[![Datenfluss in Interessent nach Bargeld.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [Power Apps-Administrator-Center](https://admin.powerapps.com/dataintegration). Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.

Die folgenden Vorlagen und grundlegenden Aufgaben werden für die Synchronisierung von Konten aus Sales für Kunden in Supply Chain Management verwendet:

- **Name der Vorlage in der Datenintegration:** Produkte (Supply Chain Management zu Sales) - direkt
- **Name der Aufgaben im Datenintegrationsprojekt**: Podukte

Keine Synchronisierungsaufgaben sind erforderlich, damit Produktsynchronisierung auftreten kann.

## <a name="entity-set"></a>Entitätssatz

| Lieferkettenverwaltung    | Verk.    |
|----------------------------|----------|
| Freigegebene Produkte für Verkauf | Produkte |

## <a name="entity-flow"></a>Entitätsfluss

Produkte werden in Supply Chain Management verwaltet und mit Sales synchronisiert. Die **Verkäufliche freigegebene Produkte**-Datenentität im Bereich Supply Chain Management exportiert nur Produkte, die *verkäuflich* sind. Verkäufliche Produkte sind Produkte, die die Informationen enthalten, die diese benötigen, damit sie in Aufträgen verwendet werden können. Die gleichen Regeln gelten, wenn ein Produkt mit der Funktion **Überprüfen** auf der Seite **Freigegebenes Produkt** überprüft wird.

Die Produktnummer wird als Schlüssel verwendet. Wenn Produktvarianten mit Sales synchronisiert werden, hat jede eine Produktvariante individuelle Produkt-Kennung

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales

In Sales wurde ein neues Feld **Wird extern verwaltet** bei Produkten hinzugefügt, um anzugeben, dass ein bestimmtes Produkt extern verwaltet wird. Der Wert wird beim Import nach Sales standardmäßig auf **Ja** festgelegt. Folgende Werte sind verfügbar:

- **Ja** – Das Produkt, stammt aus Supply Chain Management und wird nicht in Sales bearbeitet.
- **Nein** – Das Produkt wurde direkt in Sales eingegeben.
- **(Kein Wert)** – Das Produkt war in Sales vorhanden, bevor der Interessent für Bargeldlösung aktiviert wurde.

Das Feld **Wird extern verwaltet** hilft, sicherzustellen, dass nur Angebote und Aufträge mit Extern verwalteten Produkten mit Supply Chain Management synchronisiert werden.

Extern verwaltete Produkte werden automatisch der ersten gültigen Preisliste mit derselben Währung hinzugefügt. Preislisten sind alphabetisch sortiert nach Name. Der Produktverkaufspreis von Supply Chain Management wird als Preis in der Preisliste verwendet. Vergewissern Sie sich daher, dass Preislisten in Sales für jede Produktverkaufswährung in Supply Chain Management vorhanden sind. Die Währung für die freigegebenen verkäuflichen Produkte ist auf die Buchhaltungswährung in der juristischen Person festgelegt, von der das Produkt exportiert wird.

> [!NOTE]
> - Produktsynchronisierung ist nicht erfolgreich, es sei denn, es gibt eine Liste mit Preisen, die eine entsprechende Währung haben.
> - Sie können auch die verwendete Preisliste mit der Integration steuern, indem Sie den pricelevelid.name [Standard-Preisliste (Name)] im Daten-Integrationsprojekt zuordnen. Die Eingabe muss in Kleinbuchstaben sein. Beispielsweise kann der Standardwert für eine Liste mit Preisen auf Verkäufen mit dem Namen "Standard" wie folgt sein: Empfangsfeld: pricelevelid.name [Standard-Preisliste (Name)] und Zuordnungstyp: [ { "transformType" "Standard", "defaultValue": "Standard" } ].

## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung

- Bevor Sie die allererste Synchronisierung ausführen, müssen Sie die Tabelle eindeutig identifizierbarer Produkte für vorhandene Produkte in Supply Chain Management auffüllen. Vorhandene Produkte werden nicht synchronisiert, bis der Einzelvorgang abgeschlossen ist.

    1. In Supply Chain Management verwenden Sie Suche, um nach **Tabelle eindeutig identifizierbarer Produkte auffüllen** zu suchen.
    2. Klicken Sie auf **Tabelle eindeutig identifizierbarer Produkte auffüllen**, um den Einzelvorgang auszuführen. Dieser Vorgang muss nur einmal aktiviert werden.

- Vergewissern Sie sich, dass die erforderliche Wertzuordnung für die Verkaufsmaßeinheit (ME) zwischen Supply Chain Management und Sales in der Zuordnung von **SalesUnitSymbol** zu **DefaultUnit (Name)** vorhanden ist.
- Aktualisieren Sie Wertzuordnung für **Einheitengruppe** (**defaultuomscheduleid.name**), um den **Einheitengruppen** in Sales zu entsprechen.

    Der Vorlagenwert ist standardmäßig auf **Standardeinheit** festgelegt.

- Stellen Sie sicher, dass alle Maßseinheiten für Produktverkäufe von Supply Chain Management in Sales vorhanden sind.
- Vergewissern Sie sich, dass Preislisten in Sales für jede Produktverkaufswährung in Supply Chain Management vorhanden sind.
- Wenn Produkte in Sales erstellt werden, können sie den Status **Entwurf** oder **Aktiv** besitzen. Das Verhalten wird mit **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Verkäufe** in Sales gesteuert.

    Produkte, die den Status **Entwurf** besitzen, wenn sie erstellt werden, müssen aktiviert werden, bevor sie in Anführungszeichen gesetzt oder ausgewählten Aufträgen hinzugefügt werden können.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator. 

> [!NOTE]
> Die Zuordnung zeigt, welche Feldinformationen von Sales zu Supply Chain Management synchronisiert werden.

![Vorlagenzuordnung im Datenintegrator.](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Verwandte Themen

[Prospect-to-Cash](prospect-to-cash.md)

[Konten direkt von Sales mit Konten in Supply Chain Management synchronisieren](accounts-template-mapping-direct.md)

[Kontakte direkt von Sales mit Kontakten oder Debitoren in Supply Chain Management synchronisieren](contacts-template-mapping-direct.md)

[Synchronisieren von Aufträgen direkt zwischen Sales und Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Rechnungskopfzeilen und ‑positionen direkt von Supply Chain Management zu Sales synchronisieren](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]