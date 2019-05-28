---
title: Synchronisieren von Vereinbarungsrechnungen in Field Service mit Freitextrechnungen in Finance and Operations
description: Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Vereinbarungsrechnungen in Microsoft Dynamics 365 for Field Service mit Freitextrechnungen in Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560162"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a>Vereinbarungsrechnungen in Field Service mit Freitextrechnungen in Finance and Operations synchronisieren

[!include[banner](../includes/banner.md)]

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Vereinbarungsrechnungen in Microsoft Dynamics 365 for Field Service mit Freitextrechnungen in Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um die Synchronisierung von Vereinbarungsrechnungen aus Field Service mit Freitextrechnungen in Finance and Operations auszuführen.

**Name der Vorlage in der Datenintegration:**

- Vereinbarungsrechnungen (Field Service nach Finance and Operations)

**Namen der Aufgaben im Datenintegrationsprojekt:**

- Rechnungsköpfe
- Rechnungspositionen

Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von Vereinbarungsrechnungen erfolgen kann:

- Konten (Sales nach Finance and Operations) – Direkt

## <a name="entity-set"></a>Entitätssatz

| Field Service  | Finance and Operations                 |
|----------------|----------------------------------------|
| Rechnungen       | CDS-Debitoren-Freitextrechnungskopfzeilen |
| Rechnungsdetails | CDS-Debitoren-Freitextrechnungspositionen   |

## <a name="entity-flow"></a>Entitätsfluss

Rechnungen, die aus einer Vereinbarung in Field Service erstellt werden, können mit Finance and Operations über ein Common Data Service (CDS)-Datenintegrationsprojekt synchronisiert werden. Aktualisierungen dieser Rechnungen werden mit den Freitextrechnungen in Finance and Operations synchronisiert, wenn der Buchhaltungsstatus der Freitextrechnungen **In Bearbeitung** ist. Nachdem die Freitextrechnungen in Finance and Operations gebucht werden und der Buchhaltungsstatus auf **Abgeschlossen** aktualisiert wird, können Sie keine Aktualisierungen aus Field Service mehr synchronisieren.

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung

Das Feld **Hat Positionen mit Vereinbarungsursprung** ist der Entität **Rechnung** hinzugefügt worden. Mithilfe dieses Felds wird sichergestellt, dass nur Rechnungen synchronisiert werden, die aus einer Vereinbarung erstellt werden. Der Wert entspricht **true**, wenn die Rechnung mindestens eine Rechnungsposition enthält, die ihren Ursprung in einer Vereinbarung hat.

Das Feld **Hat Vereinbarungsursprung** ist der Entität **Rechnungsposition** hinzugefügt worden. Mithilfe dieses Felds wird sichergestellt, dass nur Rechnungspositionen synchronisiert werden, die aus einer Vereinbarung erstellt werden. Der Wert ist **true**, wenn die Rechnungsposition ihren Ursprung in einer Vereinbarung hat.

**Rechnungsdatum** ist ein Pflichtfeld in Finance and Operations. Daher muss das Feld einen Wert in Field Service haben, bevor eine Synchronisierung erfolgt. Um diese Anforderung zu erfüllen, wird die folgende Logik hinzugefügt:

- Wenn das Feld **Rechnungsdatum** in der Entität **Rechnung** leer ist (das heißt, wenn es keinen Wert hat), wird es auf das aktuelle Datum festgelegt, wenn eine Rechnungsposition hinzugefügt wird, die ihren Ursprung in einer Vereinbarung hat.
- Der Benutzer kann das Feld **Rechnungsdatum** ändern. Wenn allerdings der Benutzer versucht, eine Rechnung zu speichern, die ihren Ursprung in einer Vereinbarung hat, erhält er oder sie einen Geschäftsprozessfehler, wenn das Feld **Rechnungsdatum** auf der Rechnung leer ist.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

### <a name="in-finance-and-operations"></a>In Finance and Operations

Ein Rechnungsursprung muss für die Integration eingerichtet werden, um die Freitextrechnungen in Finance and Operations zu unterscheiden, die aus Vereinbarungsrechnungen in Field Service erstellt werden. Wenn eine Rechnung einen Rechnungsursprung des Typs **Vereinbarungsrechnungsintegration** hat, wird das Feld **Externe Rechnungsnummer** in der Kopfzeile der **Verkaufsrechnung** angezeigt.

Außer dass sie im Rechnungskopf angezeigt wird, kann die Information **Externe Rechnungsnummer** verwendet werden, um zu gewährleisten, dass Rechnungen, die aus Field Service-Vereinbarungsrechnungen erstellt werden, während der Rechnungssynchronisierung von Finance and Operations mit Field Service herausgefiltert werden.

1. Wechseln Sie zu **Debitoren** \> **Einstellungen** \> **Rechnungsursprungscodes**.
2. Wählen Sie **Neu** aus, um einen neuen Rechnungsursprung zu erstellen.
3. Geben Sie im Feld **Rechnungsursprung** einen Namen für den Rechnungsursprung ein, wie beispielsweise **FS**.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein, wie beispielsweise **Field Service-Vereinbarungsrechnung**.
5. Aktivieren Sie das Kontrollkästchen **Ursprungstypzuweisung**.
6. Legen Sie das Feld **Rechnungsursprungstyp** auf **Vereinbarungsrechnungsintegration** fest.
7. Wählen Sie **Speichern**.

### <a name="in-the-data-integration-project"></a>Im Datenenintegrationsprojekt

Aufgabe: **Rechnungspositionen**  

Stellen Sie sicher, dass der Standardwert für das Finance and Operations-Feld **Hauptkonto-Anzeigewert** aktualisiert wird, um dem gewünschten Wert zu entsprechen.

Der Standardvorlagenwert ist **401100**.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a>Vereinbarungsrechnungen (Field Service zu Fin und Ops): Rechnungsköpfe

[![Vorlagenzuordnung in Datenintegration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a>Vereinbarungsrechnungen (Field Service zu Fin und Ops): Rechnungspositionen

[![Vorlagenzuordnung in Datenintegration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)
