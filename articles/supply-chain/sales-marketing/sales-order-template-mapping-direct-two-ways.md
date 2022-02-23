---
title: Synchronisieren von Aufträgen direkt zwischen Sales und Supply Chain Management
description: Das Thema erklärt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Synchronisierung von Auträgen direkt aus Dynamics 365 Sales mit Dynamics 365 Supply Chain Management auszuführen.
author: ChristianRytt
manager: tfehr
ms.date: 05/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 3eaa25f0befcff448250ba2cce8e568fa4a4c707
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428897"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a>Synchronisieren von Aufträgen direkt zwischen Sales und Supply Chain Management

[!include [banner](../includes/banner.md)]

Das Thema erklärt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Synchronisierung von Auträgen direkt aus Dynamics 365 Sales mit Dynamics 365 Supply Chain Management auszuführen.

## <a name="data-flow-in-prospect-to-cash"></a>Datenfluss in Interessent nach Bargeld

Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Supply Chain Management und Sales hinweg zu synchronisieren. Die „Interessent zu Bargeld“-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Supply Chain Management und Sales. Die folgende Abbildung zeigt, wie Daten zwischen Supply Chain Management und Sales synchronisiert werden.

[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [Power Apps-Administrator-Center](https://preview.admin.powerapps.com/dataintegration). Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Auftragskopfzeilen und -positionen direkt zwischen Finance and Operations und Supply Chain Management zu synchronisieren:

- **Name der Vorlagen in der Datenintegration:** 

    - Aufträge (Sales zu Supply Chain Management) – Direkt
    - Aufträge (Supply Chain Management zu Sales) – Direkt

- **Namen der Aufgaben im Datenintegrationsprojekt:**

    - OrderHeader
    - OrderLine

Die folgenden Synchronisierungsaufgaben sind erforderlich, bevor die Synchronisierung von Rechnungskopfzeilen und -positionen erfolgen kann:

- Produkte (Supply Chain Management zu Sales) – Direkt
- Konten (Sales zu Supply Chain Management) – Direkt (falls verwendet)
- Kontakte zu Kunden (Sales zu Supply Chain Management) – Direkt (falls verwendet)

## <a name="entity-set"></a>Entitätssatz

| Lieferkettenverwaltung  | Verk.             |
|-------------------------|-------------------|
| Auftragskopfzeilen CDS | SalesOrders       |
| CDS-Auftragspositionen   | SalesOrderDetails |

## <a name="entity-flow"></a>Entitätsfluss

Aufträge werden in Sales erstellt und mit Supply Chain Management synchronisiert, wenn die **Projekt ausführen** für ein Projekt auf Basis der Vorlage **Aufträge (Sales zu Supply Chain Management) - Direkt** ausgelöst wird. Sie können Aufträge aus Sales aktivieren und synchronisieren, wenn alle **Auftrag (Produkte)** aus Produkten bestehen, die außerhalb verwaltet werden. Daher kann es keine nicht-beschreibbare Produkte geben. Nachdem der Auftrag aktiviert ist, wird der Auftrag in der Benutzeroberfläche (UI) schreibgeschützt. Zu diesem Zeitpunkt werden Aktualisierungen von Supply Chain Management vorgenommen. Nachdem ein Auftrag den Status **Bestätigt** besitzt, wird die **Aufträge (Supply Chain Management zu Sales) - Direkt** Vorlage verwendet, um alle Aktualisierungen oder den Erfüllungsstatus von Supply Chain Management mit Sales zu synchronisieren.

Sie müssen keine Aufträge in Sales erstellen. Sie können neue Aufträge im Bereich Supply Chain Management stattdessen erstellen. Nachdem ein Auftrag den Status **Bestätigt** besitzt, wird er mit Sales synchronisiert, wie im vorherigen Absatz beschrieben.

In Supply Chain Management helfen Filter in der Vorlage, sicherzustellen, dass nur relevante Aufträge in die Synchronisierung einfließen:

- Sowohl der Bestellungskunde als auch der Rechnungsdebitor auf dem Auftrag, der aus Sales stammt, werden in die Synchronisierung einbezogen. In Supply Chain Management werden die Felder **OrderingCustomerIsExternallyMaintained** und **InvoiceCustomerIsExternallyMaintained** verwendet, um Aufträge aus den Datenentitäten zu filtern.
- Der Auftrag in Supply Chain Management muss bestätigt werden. Nur bestätigte Aufträge oder Aufträge mit fortgeschrittenem Verarbeitungsstatus (beispielsweise **Versendet** oder **Fakturiert**) werden mit Sales synchronisiert.
- Nach dem Erstellen oder Ändern eines Auftrags, muss der Stapelverarbeitungsauftrag **Verkaufssummen berechnen** aus Supply Chain Management ausgeführt werden. Nur Aufträge, bei denen Auftragssummen berechnet wurden, werden mit Sales synchronisiert.

## <a name="freight-tax"></a>Frachtsteuer

Sales unterstützt keine Steuer auf Kopfzeilenebene, da Steuer auf Positionsebene gespeichert wird. Um Steuer auf Kopfebene von der Supply Chain Management zu erhalten, wie Steuer auf Fracht zu unterstützen, synchronisiert das System Steuer mit Sales als eine Einfügungsprodukt namens **Frachtsteuer** und dies hat den Steuerbetrag aus Supply Chain Management. Auf diese Weise kann die Standardkostenkalkulation in Sales verwendet werden, um Summen zu berechnen, wenn es Steuer auf Kopfebene von Supply Chain Management gibt.

## <a name="discount-calculation-and-rounding"></a>Anwendung und Rundung von Rabatten.

Das Rabattberechnungsmodell in Sales unterscheidet sich insofern vom Modell im Bereich Supply Chain Management. In Supply Chain Management kann der endgültige Rabattbetrag in einer Sales-Position die Ergebnisse einer Kombination von Rabattbeträgen und von Rabattprozentsätzen sein. Bei der abschließenden Rabattbetrag durch die Menge für die Position geteilt wird, kann möglicherweise das Runden auftreten. Allerdings wird diese Rundung nicht berücksichtigt, wenn ein Pro Einheit-Rabattbetrag, der gerundet werden soll, mit Sales synchronisiert wird. Um den gesamten Rabattbetrag in einer Verkaufsposition in Supply Chain Management ordnungsgemäß zu synchronisieren, muss der Gesamtbetrag mit Sales synchronisiert werden, ohne nach Positionsmenge aufgeteilt werden. Daher müssen Sie **Rabattberechnungsmethode** als **Positionsartikel** in Sales festlegen.

Wenn eine Auftragsposition von Sales zu Supply Chain Management synchronisiert wird, wird der vollständige Betrag für den Positionsrabatt verwendet. Da Supply Chain Management kein Feld hat, das den Rabattbetrag für vollständigen eine Position speichern kann, wird der Betrag durch die Menge dividiert und gespeichert im Feld **Positionsrabatt**. Jede Rundung, die für diese Periode vorkommt, wird im Feld **Sales - Belastungen** auf der Verkaufsposition gespeichert.

### <a name="example"></a>Beispiel

**Synchronisierung von Sales zu Supply Chain Management**

- **Sales:** = Menge = 3, Pro-Positionsrabatt = $10.00
- **Supply Chain Management:** Menge = 3, Positionsrabattbetrag = $3,33, Verkaufszuschlag = -$0,01 

**Synchronisierung von Supply Chain Management zu Sales**

- **Supply Chain Management:** Menge = 3, Positionsrabattbetrag = $3,33, Verkaufszuschlag = -$0,01
- **Sales:** = Menge = 3, Pro-Positionsrabatt = (3 × $3.33) + $0.01 = $10.00

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales

Neue Felder wurden der Entität **Auftrag** hinzugefügt und auf der Seite angezeigt:

- **Wird extern verwaltet** – Auf **Ja** setzen, wenn der Auftrag aus Supply Chain Management stammt.
- **Verarbeitungsstatus** – Wird verwendet, um den Verarbeitungsstatus des Auftrags in Supply Chain Management anzuzeigen. Folgende Werte sind verfügbar:

    - **Entwurf** – Der anfängliche Status, wenn der erstmals Auftrag in Sales erstellt wird. In Sales können nur Aufträge mit diesem Bearbeitungsstatus bearbeitet werden.
    - **Aktiv** – Der Status wird nach dem Auftrag in Sales mithilfe der Schaltfläche **Aktivieren** in Sales aktiviert.
    - **Bestätigt**
    - **Lieferschein**
    - **Fakturiert**
    - **Entnommen**
    - **Teilweise kommissioniert**
    - **Teilweise verpackt**
    - **Versendet**
    - **Teilweise geliefert**
    - **Teilweise fakturiert**
    - **Storniert**

Das Feld **Verfügt nur über extern verwaltete Produkte** ist der Entität „Angebot” hinzugefügt worden, um stets nachzuverfolgen, ob das Verkaufsangebot vollständig aus extern verwalteten Produkten besteht. Wenn ein Verkaufsauftrag nur aus extern verwalteten Produkten besteht, werden die Produkte in Supply Chain Management verwaltet. Mit diesem Verhalten wird sichergestellt, dass Sie nicht aktivieren und versuchen, Verkaufsangebotspositionen mit Produkten zu synchronisieren, die in Supply Chain Management unbekannt sind.

Bei extern verwalteten Aufträgen, werden die Schaltflächen **Rechnung erstellen**, **Auftrag stornieren**, **Neu berechnen** und die für **Produkte abrufen** und **Adresse suchen** auf der Seite **Auftrag** ausgeblendet, da Rechnungen in Supply Chain Management erstellt und mit Sales synchronisiert werden. Die Seite „Auftrag“ kann nicht geändert werden, da Auftragsinformationen über Supply Chain Management synchronisiert werden.

Der Auftragsstatus bleibt **Aktiv**, um sicherstellen, dass Änderungen aus Supply Chain Management in Sales in den Auftrag einfließen. Dies wird gesteuert, indem Sie den standardmäßigen **Statecode \[Status\]** Wert auf **Aktiv** setzen.

## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung

Vor dem Synchronisieren von Aufträgen müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:

### <a name="setup-in-sales"></a>Einrichtung in Sales

- Stellen Sie sicher, dass Berechtigungen für das Team, zu dem der Benutzer (aus Ihren Verbindungseinstellungen in Sales) zugewiesen ist, vorhanden sind. Werden Demodaten verwendet, hat in der Regel der Benutzer einen Administratorzugriff aber nicht das Team. Wenn dieses Team nicht Administratorzugriff hat, wenn Sie das Projekt vom Datenintegrator ausführen, erhalten Sie eine Fehlermeldung, die angibt, dass das Hauptteam fehlt.

    Wählen Sie unter **Einstellungen** &gt; **Sicherheit** &gt; **Teams** das relevante Team aus, klicken Sie auf die Option für **Rollen verwalten**, und wählen Sie eine Rolle mit den benötigten Berechtigungen aus, beispielsweise **Systemadministrator**.

- Um die korrekte Berechnung von Rabatten in Sales und Supply Chain Management sicherzustellen, muss **Rabattberechnungsmethode** auf **Positionsartikel** festgelegt werden.
- Gehen Sie zu &gt; Sie **Einstellungen** **Verwaltung** &gt; **Systemeinstellungen** &gt; **Sales** zu öffnen, und überprüfen Sie, ob die folgenden Einstellungen verwendet werden:

    - Die Option **Systempreisberechnungssystem verwenden** wird auf **Ja** festgelegt.
    - Das Feld **Rabattberechnungsmethode** wird auf **Positionsartikel** festgelegt.

### <a name="setup-in-supply-chain-management"></a>Einrichtung in Supply Chain Management

- Gehen Sie zu &gt; **Vertrieb und Marketing** **Periodische Aufgaben** &gt; **Berechnen Sie wünschenswert**, und richten Sie sie, dass sie als Stapelverarbeitungslauf ausgeführt wird. Legen sie Option **Berechnen Sie Summen für Aufträge** auf **Ja** fest. Diese Einstellung ist wichtig, da nur Aufträge, bei denen Auftragssummen berechnet wurden, werden mit Sales synchronisiert. Die Häufigkeit des Stapelverarbeitungsauftrags sollte sich an der Häufigkeit der Auftragssynchronisierung orientieren.

Wenn Sie auch Arbeitsauftragsintegration verwenden, müssen Sie die Auftragsgrundlage einrichten. Die Auftragsgrundlage wird verwendet, um zwischen Aufträgen in Supply Chain Management zu unterscheiden, die aus Arbeitsaufträgen in Field Service erstellt wurden. Wenn ein Auftrag eine Auftragsgrundlage des Typs **Arbeitsauftragsintegration** hat, wird das Feld **Externer Arbeitsauftragsstatus** im Auftragskopf angezeigt. Darüber hinaus wird durch die Auftragsgrundlage sichergestellt, dass Aufträge, die aus Arbeitsaufträgen in Field Service erstellt wurden, während der Auftragssynchronisierung von Supply Chain Management mit Field Service herausgefiltert werden.

1. Wechseln Sie zu **Vertrieb und Marketing** \> **Setup** \> **Aufträge** \> **Auftragsgrundlage**.
2. Wählen Sie **Neu** aus, um einen neuen Auftragsgrundlage zu erstellen.
3. Geben Sie im Feld **Auftragsgrundlage** einen Namen für den Auftragsgrundlage ein, wie beispielsweise **SalesOrder**.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein, wie beispielsweise **Auftrag aus Verkauf**.
5. Aktivieren Sie das Kontrollkästchen **Ursprungstypzuweisung**.
6. Legen Sie das Feld **Auftragsgrundlagentyp** auf **Auftragsintegration** fest.
7. Wählen Sie **Speichern**.

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a>Einstellungen in Aufträgen (Sales zu Supply Chain Management) - direktes Datenenintegrationsprojekt

- Vergewissern Sie sich, dass die erforderliche Zuordnung für **Shipto\_Land** zu **DeliveryAddressCountryRegionISOCode** vorhanden ist. Sie können Leer als Standardwert in der Wertzuordnung festlegen, um für Zahlungen nationaler Aufträge kein Land eingeben zu müssen. Lassen Sie einfach die linke Seite leer, und legen die rechte Seite auf das gewünschte Land oder die Region fest.

    Der Vorlagenwert ist eine Wertzuordnung, in der verschiedene Länder/Regionen zugeordnet sind, und wo ein leerer Wert dem Wert USA entspricht.

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a>Einstellungen in Aufträgen (Supply Chain Management zu Sales) - direktes Datenenintegrationsprojekt

#### <a name="salesheader-task"></a>SalesHeader-Aufgabe

- Preisliste ist erforderlich, um Aufträge in Sales zu erstellen. Aktualisieren Sie die Wertzuordnung für **pricelevelid.name \[Price List Name\]** auf die Preisliste, die in Sales pro Währung verwendet wird. Sie können die Standardpreisliste für eine einzelne Währung verwenden. Alternativ können Sie, wenn Sie Preislisten in mehreren Währungen haben, eine Zuordnung verwenden.

    Der Standardvorlagewert für **pricelevelid.name \[Price List Name\]** ist **CRM Service USA (Beispiel)**.

#### <a name="salesline-task"></a>SalesLine-Aufgabe

- Stellen Sie sicher, dass die erforderliche Wertzuordnung für **SalesUnitSymbol** in Supply Chain Management vorhanden ist.
- Überprüfen Sie, dass die obligatorischen Einheiten in Sales definiert sind.

    Ein Vorlagenwert, eine der Wertzuordnung ist, wird für **SalesUnitSymbol** definiert **oumid.name**

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

> [!NOTE]
> Die Felder **Zahlungsbedingungen**, **Frachtkonditionen**, **Lieferbedingungen**, **Liefermethode** und **Liefermodus** sind nicht Teil der Standardzuordnungen. Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung in Datenintegration.

> [!NOTE]
> Die Zuordnung zeigt, welche Feldinformationen von Sales zu Supply Chain Management synchronisiert werden oder von Supply Chain Management zu Sales.

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a>Aufträge (Supply Chain Management zu Sales) – Direkt: OrderHeader

[![Vorlagenzuordnung in Datenintegration](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a>Aufträge (Supply Chain Management zu Sales) – Direkt: OrderLine

[![Vorlagenzuordnung in Datenintegration](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a>Aufträge (Sales zu Supply Chain Management) – Direkt: OrderHeader

[![Vorlagenzuordnung in Datenintegration](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a>Aufträge (Sales zu Supply Chain Management) – Direkt: OrderLine

[![Vorlagenzuordnung in Datenintegration](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Verwandte Themen

[Interessent zu Bargeld](prospect-to-cash.md)
