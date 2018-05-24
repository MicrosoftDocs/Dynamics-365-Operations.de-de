---
title: "Arbeitsaufträge in Field Service mit Aufträgen in Finance and Operations synchronisieren"
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Arbeitsaufträge in Field Service mit Aufträgen in Finance and Operations zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: 933d9755085d507310dd46d96a492d2124647ec3
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-finance-and-operations"></a>Arbeitsaufträge in Field Service mit Aufträgen in Finance and Operations synchronisieren

[!include[banner](../includes/banner.md)]

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Arbeitsaufträge in Microsoft Dynamics 365 for Field Service mit Auftrag in Microsoft Dynamics 365 for Finance and Operations zu synchonisieren.

[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Arbeitsaufträge in Field Service mit Aufträgen in Finance and Operations zu synchronisieren.

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um die Synchronisierung von Arbeitsaufträge in Field Service mit Aufträgen in Finance and Operations zu synchronisieren.

### <a name="names-of-the-templates-in-data-integration"></a>Namen der Vorlagen in der Datenintegration

Die Vorlage **Arbeitsaufträge zu Aufträgen (Field Service nach Finance and Operations)** wird verwendet, um die Synchronisierung auszuführen.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Namen der Aufgaben im Datenintegrationsprojekt

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Die folgenden Synchronisierungsaufgaben sind erforderlich, bevor die Synchronisierung von Auftragskopfzeilen und -positionen erfolgen kann:

- Field Service-Produkte (Finance and Operations nach Field Service)
- Konten (Sales nach Finance and Operations) – Direkt

## <a name="entity-set"></a>Entitätssatz

| **Field Service** | **Finance and Operations** |
|-------------------------|-------------------------|
| msdyn_workorders        | Auftragskopfzeilen CDS |
| msdyn_workorderservices | CDS-Auftragspositionen   |
| msdyn_workorderproducts | CDS-Auftragspositionen   |

## <a name="entity-flow"></a>Entitätsfluss

Arbeitsaufträge werden in Field Service erstellt. Wenn die Arbeitsaufträge nur extern verwaltete Produkte enthalten und wenn der Wert **Arbeitsauftragsstatus** sich von **Offen-ungeplant** und **Geschlossen – storniert** unterscheidet, können die Arbeitsaufträge mit Finance and Operations über ein CDS-Datenintegrationsprojekt synchronisiert werden. Aktualisierungen in den Arbeitsaufträgen werden als Auträge in Finance and Operations synchronisiert. Diese Updates umfassen die Informationen zum Ursprungstyp und Status.

## <a name="estimated-versus-used"></a>„Vorkalkuliert” gegenüber „Verwendet”

In Field Service haben Produkte und Dienstleistungen in Arbeitsaufträgen sowohl **Vorkalkuliert**-Werte als auch **Verwendet**-Werte für Mengen und Beträge. In Finance and Operations haben jedoch Aufträge nicht dasselbe Konzept der Werte **Vorkalkuliert** und **Verwendet**. Um eine Produktzuteilung zu unterstützen, bei der die erwartete Menge im Auftrag in Finance and Operations verwendet wird, aber um die verwendete Menge beizubehalten, die verbraucht und fakturiert werden soll, werden die Produkte und Dienstleistungen im Auftrag durch zwei Aufgabengruppen synchronisiert. Eine Gruppe von Aufgaben ist für **Vorkalkuliert**-Werte, und eine andere Aufgabengruppe ist für **Verwendet**-Werte.

Dieses Verhalten ermöglicht Szenarien, bei denen vorkalkulierte Werte für die Zuteilung oder Reservierung in Finance and Operations verwendet werden, wohingegen verwendete Werte für den Verbrauch und die Fakturierung verwendet werden.

### <a name="estimated"></a>Vorkalkuliert

Für die Synchronisierung von Produktpositionen werden die Werte **Vorkalkuliert** verwendet, wenn der Wert **Positionsstatus** **Vorkalkuliert** ist, die Option **Zugeordnet** auf **Ja** festgelegt ist und der Wert **Systemstatus** nicht **Geschlossen – gebucht** ist.

Für die Synchronisierung von Servicepositionen werden die Werte **Vorkalkuliert** verwendet, wenn der Wert **Positionsstatus** **Vorkalkuliert** ist und der Wert **Systemstatus** nicht **Geschlossen – gebucht** ist.

### <a name="used"></a>Verwendet

Die Werte **Verwendet** werden für Verbrauch und Rechnungsstellung verwendet. In diesen Fällen werden die Werte **Verwendet** synchronisiert.

Die folgende Tabelle enthält einen Überblick über die verschiedenen Kombinationen für Produktpositionen.

| Systemstatus <br>(Field Service) | Positionsstatus <br>(Field Service) | Zugeordnet <br>(Field Service) |Synchronisierter Wert <br>(Finance and Operations) |
|--------------------|-------------|-----------|---------------------------------|
| Offen – geplant   | Vorkalkuliert   | Ja       | Vorkalkuliert                       |
| Offen – geplant   | Vorkalkuliert   | Nr.        | Verwendet                            |
| Offen – geplant   | Verwendet        | Ja       | Verwendet                            |
| Offen – geplant   | Verwendet        | Nr.        | Verwendet                            |
| Offen – in Bearbeitung | Vorkalkuliert   | Ja       | Vorkalkuliert                       |
| Offen – in Bearbeitung | Vorkalkuliert   | Nr.        | Verwendet                            |
| Offen – in Bearbeitung | Verwendet        | Ja       | Verwendet                            |
| Offen – in Bearbeitung | Verwendet        | Nr.        | Verwendet                            |
| Offen – abgeschlossen   | Vorkalkuliert   | Ja       | Vorkalkuliert                       |
| Offen – abgeschlossen   | Vorkalkuliert   | Nr.        | Verwendet                            |
| Offen – abgeschlossen   | Verwendet        | Ja       | Verwendet                            |
| Offen – abgeschlossen   | Verwendet        | Nr.        | Verwendet                            |
| Geschlossen – gebucht    | Vorkalkuliert   | Ja       | Verwendet                            |
| Geschlossen – gebucht    | Vorkalkuliert   | Nr.        | Verwendet                            |
| Geschlossen – gebucht    | Verwendet        | Ja       | Verwendet                            |
| Geschlossen – gebucht    | Verwendet        | Nr.        | Verwendet                            |

Die folgende Tabelle enthält einen Überblick über die verschiedenen Kombinationen für Servicepositionen.

| Systemstatus <br>(Field Service) | Positionsstatus <br>(Field Service) | Synchronisierter Wert <br>(Finance and Operations) |
|--------------------|-------------|-----------|
| Offen – geplant   | Vorkalkuliert   | Vorkalkuliert |
| Offen – geplant   | Verwendet        | Verwendet      |
| Offen – in Bearbeitung | Vorkalkuliert   | Vorkalkuliert |
| Offen – in Bearbeitung | Verwendet        | Verwendet      |
| Offen – abgeschlossen   | Vorkalkuliert   | Vorkalkuliert |
| Offen – abgeschlossen   | Verwendet        | Verwendet      |
| Geschlossen – gebucht    | Vorkalkuliert   | Verwendet      |
| Geschlossen – gebucht    | Verwendet        | Verwendet      |

Synchronisierung von **Vorkalkuliert**-Werten gegenüber **Verwendet**-Werten wird durch die zwei Gruppen von Aufgaben für Produktpositionen und Servicepositionen verwaltet. Vordefinierte Filter lösen die korrekte Aufgabe aus, und die zugrunde liegende Zuordnung hilft zu gewährleisten, dass die korrekten Werte für **Voraussichtlich** gegenüber **Verwendet** synchronisiert werden.

### <a name="example"></a>Beispiel

1. Ein Arbeitsauftrag wird in Field Service erstellt und geplant.

    Der Wert **Systemstatus** ist **Offen – geplant**.

    - **Produktposition:** = Vorkalkulierte Menge = 5 Einheiten, Verwendete Menge = 0 Einheiten, Positionsstatus = Vorkalkuliert, Zugeordnet = Nein
    - **Serviceposition:** Vorkalkulierte Menge = 2 h, Verwendete Mente = 0 h, Positionsstatus = Vorkalkuliert

    In diesem Beispiel werden der Wert **Verwendete Menge** des Produkts von **0** (Null) und der Wert **Vorkalkulierte Menge** der Dienstleistung von **2 h** mit Finance and Operations synchronisiert.

2. Produkte werden in Field Service zugeordnet.

    Der Wert **Systemstatus** ist **Offen – geplant**.

    - **Produktposition:** = Vorkalkulierte Menge = 5 Einheiten, Verwendete Menge = 0 Einheiten, Positionsstatus = Vorkalkuliert, Zugeordnet = Ja
    - **Serviceposition:** Vorkalkulierte Menge = 2 h, Verwendete Mente = 0 h, Positionsstatus = Vorkalkuliert

    In diesem Beispiel werden der Wert **Vorkalkulierte Menge** des Produkts von **5 Einheiten** und der Wert **Vorkalkulierte Menge** der Dienstleistung von **2 h** mit Finance and Operations synchronisiert.

3. Der Servicetechniker beginnt die Arbeit am Arbeitsauftrag und erfasst eine Materialverwendung von 6.

    Der Wert **Systemstatus** ist **Offen – In Bearbeitung**.

    - **Produktposition:** = Vorkalkulierte Menge = 5 Einheiten, Verwendete Menge = 6 Einheiten, Positionsstatus = Verwendet, Zugeordnet = Ja
    - **Serviceposition:** Vorkalkulierte Menge = 2 h, Verwendete Mente = 0 h, Positionsstatus = Vorkalkuliert

    In diesem Beispiel werden der Wert **Verwendete Menge** des Produkts von **6** und der Wert **Vorkalkulierte Menge** der Dienstleistung von **2 h** mit Finance and Operations synchronisiert.

4. Der Servicetechniker schließt den Arbeitsauftrag ab und erfasst die verwendete Zeit von 1,5 Stunden.

    Der Wert **Systemstatus** ist **Offen – abgeschlossen**.

    - **Produktposition:** = Vorkalkulierte Menge = 5 Einheiten, Verwendete Menge = 6 Einheiten, Positionsstatus = Verwendet, Zugeordnet = Ja
    - **Serviceposition:** Vorkalkulierte Menge = 2 h, Verwendete Mente = 1,5 h, Positionsstatus = Verwendet

    In diesem Beispiel werden der Wert **Verwendete Menge** des Produkts von **6** und der Wert **Vorkalkulierte Menge** der Dienstleistung von **1,5 h** mit Finance and Operations synchronisiert.

## <a name="sales-order-origin-and-status"></a>Auftragsursprung und Status

### <a name="sales-origin"></a>Auftragsgrundlage

Um Aufträge in Finance and Operations nachzuverfolgen, die ihren Ursprung in Arbeitsaufträgen haben, können Sie eine Auftragsgrundlage erstellen, bei dem die Option **Ursprungstypzuweisung** auf **Ja** und das Feld **Auftragsgrundlagentyp** auf **Arbeitsauftragsintegration** festgelegt sind.

Standardmäßig wird von der Zuordnung der Auftragsgrundlage für den Auftragsgrundlagentyp **Arbeitsauftragsintegration** für alle Aufträge ausgewählt, die aus Arbeitsaufträgen erstellt werden. Dieses Verhalten kann nützlich sein, wenn Sie dem Auftrag in Finance and Operations arbeiten. Sie müssen sicherstellen, dass Aufträge, die ihren Ursprung in Arbeitsaufträgen haben, nicht als Arbeitsaufträge nach Field Service zurück synchronisiert werden.

Einzelheiten dazu, wie die korrekten Auftragsgrundlageneinstellungen in Finance and Operations erstellt werden, finden Sie im Abschnitt „Voraussetzungen und Zuordnungseinrichtung” in diesem Thema.

### <a name="status"></a>Status

Wenn der Auftrag in einem Arbeitsauftrag seinen Ursprung hat, wird das Feld **Externer Arbeitsauftragsstatus** auf der Registerkarte **Einstellungen** im Auftragskopf angezeigt. Dieses Feld zeigt den Systemstatus aus dem Arbeitsauftrag in Field Service an, um den synchronisierten Arbeitsauftragsstatus von Aufträgen in Finance and Operations nachzuverfolgen. Mithilfe dieses Felds kann der Benutzer von Finance and Operations auch bestimmen, wann der Auftrag geliefert und fakturiert werden soll.

Das Feld **Externer Arbeitsauftragsstatus** kann die folgenden Werte haben:

- Offen – geplant
- Offen – in Bearbeitung
- Offen – abgeschlossen
- Geschlossen – gebucht

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung

Um die Integration zwischen Field Service und Finance and Operations zu unterstützen, sind zusätzliche Funktionen aus der Field Service CRM-Lösung erforderlich. Die Lösung enthält die folgenden Änderungen.

### <a name="work-order-entity"></a>Arbeitsauftragsentität

Das Feld **Verfügt nur über extern verwaltete Produkte** ist der Entität **Arbeitsauftrag** hinzugefügt worden und wird auf der Seite angezeigt. Es wird verwendet, um durchgängig nachzuverfolgen, ob ein Arbeitsauftrag vollständig aus extern verwalteten Produkten besteht. Ein Arbeitsauftrag besteht vollständig aus extern verwalteten Produkten, wenn alle zugehörigen Produkte in Finance and Operations verwaltet werden. Mit diesem Feld wird sichergestellt, dass Benutzer keine Arbeitsaufträge synchronisieren, die Produkte enthalten, die in Finance and Operations unbekannt sind.

### <a name="work-order-product-entity"></a>Arbeitsauftragsprodukt-Entität

- Das Feld **Auftrag verfügt nur über extern verwaltete Produkte** ist der Entität **Arbeitsauftragsprodukt** hinzugefügt worden und wird auf der Seite angezeigt. Es wird verwendet, um konsistent nachzuverfolgen, ob das Arbeitsauftragsprodukt in Finance and Operations verwaltet wird. Mit diesem Feld wird sichergestellt, dass Benutzer keine Arbeitsauftragsprodukte synchronisieren, die in Finance and Operations unbekannt sind.
- Das Feld **Kopfzeilensystemstatus** ist der Entität **Arbeitsauftragsprodukt** hinzugefügt worden und wird auf der Seite angezeigt. Es wird verwendet, um konsistent den Systemstatus des Arbeitsauftrags nachzuverfolgen und gewährleistet die korrekte Filterung, wenn Arbeitsauftragspodukte mit Finance and Operations synchonisiert werden. Wenn Filter für die Integrationsaufgaben festgelegt werden, werden auch **Kopfzeilensystemstatus**-Informationen verwendet, um zu bestimmen, ob die vorkalkulierten oder verwendeten Werte synchronisiert werden sollen.
- Im Feld **Fakturierter Betrag pro Einheit** wird der Betrag angezeigt, der pro tatsächlich verwendeter Einheit fakturiert wird. Der Wert wird als **Gesamtbetrag** berechnet, der durch den Wert **Istmenge** geteilt wird. Das Feld wird für die Integration mit Systemen verwendet, die nicht verschiedene Werte für die verwendete Menge und die berechnete Menge unterstützen. Dieses Feld wird nicht in der Benutzeroberfläche (UI) angezeigt. 
- Das Feld **Fakturierter Rabattbetrag** wird als **Rabattbetrag**-Wert zuzüglich der Rundung aus der Berechnung von **Fakturierter Betrag pro Einheit** berechnet. Dieses Feld wird für die Integration verwendet und wird nicht in der Benutzeroberfläche angezeigt.
- Das Feld **Dezimale Menge** speichert den Wert aus dem Feld **Menge** als Dezimalzahl. Dieses Feld wird für die Integration verwendet und wird nicht in der Benutzeroberfläche angezeigt. 
- Der Wert in Feldern **Verwendet** wird auf **0** (null) zurückgesetzt, wenn der Wert **Positionsstatus** des Arbeitsauftragsprodukts von **Verwendet** zu **Vorkalkuliert** geändert wird. Diese Änderung trägt dazu bei, Situationen zu verhindern, in denen eine verwendete Menge, die fälschlicherweise eingegeben wird, für die Synchronisierung verwendet wird, wenn der Wert **Positionsstatus** **Vorkalkuliert** ist und die Option **Zugeordnet** auf **Nein** festgelegt ist.

### <a name="work-order-service-entity"></a>Arbeitsauftragsservice-Entität

- Das Feld **Auftrag verfügt nur über extern verwaltete Produkte** ist der Entität **Arbeitsauftragsservice** hinzugefügt worden und wird auf der Seite angezeigt. Es wird verwendet, um konsistent nachzuverfolgen, ob der Arbeitsauftragsservice in Finance and Operations verwaltet wird. Mit diesem Feld wird sichergestellt, dass Benutzer keine Arbeitsauftragsservices synchronisieren, die in Finance and Operations unbekannt sind.
- Das Feld **Kopfzeilensystemstatus** ist der Entität **Arbeitsauftragsservice** hinzugefügt worden und wird auf der Seite angezeigt. Es wird verwendet, um konsistent den Systemstatus des Arbeitsauftrags nachzuverfolgen und gewährleistet die korrekte Filterung, wenn Arbeitsauftragsservices mit Finance and Operations synchonisiert werden. Wenn Filter für die Integrationsaufgaben festgelegt werden, werden auch **Kopfzeilensystemstatus**-Informationen verwendet, um zu bestimmen, ob die vorkalkulierten oder verwendeten Werte synchronisiert werden sollen.
- Das Feld **Dauer in Stunden** speichert den Wert aus dem Feld **Dauer**, nachdem dieser Wert von Minuten in Stunden konvertiert wurde. Dieses Feld wird für die Integration verwendet und wird nicht in der Benutzeroberfläche angezeigt.
- Das Feld **Vorkalkulierte Dauer in Stunden** speichert den Wert aus dem Feld **Vorkalkulierte Dauer**, nachdem dieser Wert von Minuten in Stunden konvertiert wurde. Dieses Feld wird für die Integration verwendet und wird nicht in der Benutzeroberfläche angezeigt.
- Im Feld **Fakturierter Betrag pro Einheit** wird der Betrag gespeichert, der pro tatsächlich verwendeter Einheit fakturiert wird. Der Wert wird als **Gesamtbetrag** berechnet, der durch den Wert **Istmenge** geteilt wird. Dieses Feld wird für die Integration mit Systemen verwendet, die nicht verschiedene Werte für die verwendete Menge und die berechnete Menge unterstützen. Das Feld wird nicht in der Benutzeroberfläche angezeigt.
- Das Feld **Fakturierter Rabattbetrag** wird als **Rabattbetrag**-Wert zuzüglich der Rundung aus der Berechnung von **Fakturierter Betrag pro Einheit** berechnet. Dieses Feld wird für die Integration verwendet und wird nicht in der Benutzeroberfläche angezeigt.
- Das Feld **Externer Positionsauftrag** ist eine berechnete negative Positionsauftragsnummer, die in externen Systemen werden kann, in denen Arbeitsauftragsproduktpositionen und -servicepositionen kombiniert werden. Dieses Feld ermöglicht es, dass Arbeitsauftragsprodukte, die eingefügt werden, positive Positionsnummern haben und Arbeitsauftragsservices negative Positionsnummern haben. Der Wert dieses Felds wird als **Positionsauftrag** berechnet, der mit -1 multipliziert wird. Dieses Feld wird nicht in der Benutzeroberfläche angezeigt.
- Der Wert in Feldern **Verwendet** wird auf **0** (null) zurückgesetzt, wenn der Wert **Positionsstatus** des Arbeitsauftragsservices aus irgendeinem Grund von **Verwendet** zu **Vorkalkuliert** geändert wird. Diese Änderung trägt dazu bei, Situationen zu verhindern, in denen eine verwendete Menge, die fälschlicherweise eingegeben wird, für die Synchronisierung verwendet wird, wenn der Wert **Positionsstatus** **Vorkalkuliert** ist und der Wert **Kopfzeilensystemstatus** **Geschlossen – gebucht** ist.

## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung

Vor dem Synchronisieren von Arbeitsaufträgen müssen die Systeme mit den folgenden Einstellungen aktualisiert werden:

### <a name="setup-in-field-service"></a>Einstellungen in Field Service

- Stellen Sie sicher, dass die Nummernserie, die für Arbeitsaufträge in Field Service verwendet wird, sich nicht mit dem Nummernkreis überschneidet, die für Aufträge in Finance and Operations verwendet wird. Andernfalls können vorhandene Aufträge in Field Service oder Finance and Operations falsch aktualisiert werden.
- Das Feld **Arbeitsauftrags-Rechnungserstellung** muss auf **Nie** festgelegt werden, da die Rechnungsstellung von Finance and Operations aus erfolgt. Wechseln Sie zu **Field Service** \> **Einstellungen** \> **Verwaltung** \> **Field Service-Einstellungen** und stellen Sie sicher, dass das Feld **Arbeitsauftrags-Rechnungserstellung** auf **Nie** festgelegt ist.

### <a name="setup-in-finance-and-operations"></a>Einrichtung in Finance and Operations

Arbeitsauftragsintegration erfordert, dass Sie die Auftragsgrundlage einrichten. Die Auftragsgrundlage wird verwendet, um zwischen Aufträgen in Finance and Operations zu unterscheiden, die aus Arbeitsaufträgen in Field Service erstellt wurden. Wenn ein Auftrag eine Auftragsgrundlage des Typs **Arbeitsauftragsintegration** hat, wird das Feld **Externer Arbeitsauftragsstatus** im Auftragskopf angezeigt. Darüber hinaus wird durch die Auftragsgrundlage gewährleistet, dass Aufträge, die aus Arbeitsaufträgen in Field Service erstellt wurden, während der Auftragssynchronisierung von Finance and Operations mit Field Service herausgefiltert werden.

1. Wechseln Sie zu **Vertrieb und Marketing** \> **Setup** \> **Aufträge** \> **Auftragsgrundlage**.
2. Wählen Sie **Neu** aus, um einen neuen Auftragsgrundlage zu erstellen.
3. Geben Sie im Feld **Auftragsgrundlage** einen Namen für den Auftragsgrundlage ein, wie beispielsweise **WorkOrder**.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein, wie beispielsweise **Field Service-Arbeitsauftrag**.
5. Aktivieren Sie das Kontrollkästchen **Ursprungstypzuweisung**.
6. Legen Sie das Feld **Auftragsgrundlagentyp** auf **Arbeitsauftragsintegration** fest.
7. Wählen Sie **Speichern**.


### <a name="setup-in-data-integration"></a>Einrichtung in der Datenintegration

Stellen Sie sicher, dass **Integrationsschlüssel** für **msdyn_workorders** vorhanden ist
1. Gehen Sie zu Datenintegration
2. Wählen Sie **Verbindungssatz** Registerkarte
3. Wählen Sie das für die Synchronisation der Arbeitsaufträge verwendete Verbindungsset aus.
4. Wählen Sie **Integrationsschlüssel** Registerkarte
5. Suchen Sie msdyn_workorders und überprüfen Sie, ob der Schlüssel **msdyn_name (Work Order Number)** hinzugefügt wurde. Wenn es nicht angezeigt wird, fügen Sie es durch Klicken auf **Schlüssel hinzufügen** und klicken Sie auf **Speichern** im oberen Bereich der Seite.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderheader"></a>Arbeitsaufträge an Aufträge (Field Service to Fin und Ops): WorkOrderHeader

Filter: (msdyn_systemstatus ne 690970005) and (msdyn_systemstatus ne 690970000) and (msdynce_hasexternallymaintainedproductsonly eq true)

[![Vorlagenzuordnung in Datenintegration](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderservicelineestimate"></a>Arbeitsaufträge an Aufträge (Field Service to Fin und Ops): WorkOrderServiceLineEstimate

Filter: (msdynce_headersystemstatus ne 690970005) and (msdynce_headersystemstatus ne 690970000) and (msdynce_orderhasexternalmaintainedproductsonly eq true) and (msdyn_linestatus eq 690970000) and (msdynce_headersystemstatus ne 690970004)

[![Vorlagenzuordnung in Datenintegration](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderservicelineused"></a>Arbeitsaufträge an Aufträge (Field Service to Fin und Ops): WorkOrderServiceLineUsed

Filter: (msdynce_headersystemstatus ne 690970005) and (msdynce_headersystemstatus ne 690970000) and (msdynce_orderhasexternalmaintainedproductsonly eq true) and ((msdyn_linestatus eq 690970001) or (msdynce_headersystemstatus eq 690970004))

[![Vorlagenzuordnung in Datenintegration](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderproductlineestimate"></a>Arbeitsaufträge an Aufträge (Field Service to Fin und Ops): WorkOrderProductLineEstimate

Filter: (msdynce_headersystemstatus ne 690970005) and (msdynce_headersystemstatus ne 690970000) and (msdynce_orderhasexternalmaintainedproductsonly eq true) and (msdyn_linestatus eq 690970000) and (msdynce_headersystemstatus ne 690970004) and (msdyn_allocated eq true)

[![Vorlagenzuordnung in Datenintegration](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderproductlineused"></a>Arbeitsaufträge an Aufträge (Field Service to Fin und Ops): WorkOrderProductLineUsed

Filter: (msdynce_headersystemstatus ne 690970005) and (msdynce_headersystemstatus ne 690970000) and (msdynce_orderhasexternalmaintainedproductsonly eq true) and ((msdyn_linestatus eq 690970001) or (msdynce_headersystemstatus eq 690970004) or (msdyn_allocated ne true))

[![Vorlagenzuordnung in Datenintegration](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)

