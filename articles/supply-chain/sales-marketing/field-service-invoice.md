---
title: Vereinbarungsrechnungen in Field Service mit Freitextrechnungen in Supply Chain Management synchronisieren
description: Dieser Artikel erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Vereinbarungsrechnungen in Dynamics 365 Field Service mit Freitextrechnungen in Dynamics 365 Supply Chain Management zu synchronisieren.
author: Henrikan
ms.date: 04/10/2018
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
ms.openlocfilehash: c4ef70af71ae223baaa2abb2b64428beab946e3d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900882"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a>Vereinbarungsrechnungen in Field Service mit Freitextrechnungen in Supply Chain Management synchronisieren

[!include[banner](../includes/banner.md)]



Dieser Artikel erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Vereinbarungsrechnungen in Dynamics 365 Field Service mit Freitextrechnungen in Dynamics 365 Supply Chain Management zu synchronisieren.

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um die Synchronisierung von Vereinbarungsrechnungen aus Field Service mit Freitextrechnungen in Supply Chain Management auszuführen.

**Name der Vorlage in der Datenintegration**

- Vereinbarungsrechnungen (Field Service an Supply Chain Management)

**Namen der Aufgaben im Datenintegrationsprojekt**

- Rechnungsköpfe
- Rechnungspositionen

Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von Vereinbarungsrechnungen erfolgen kann:

- Konten (Sales zu Supply Chain Management) – Direkt

## <a name="entity-set"></a>Entitätssatz

| Field Service  | Lieferkettenverwaltung                 |
|----------------|----------------------------------------|
| Rechnungen       | Debitoren-Freitextrechnungskopfzeilen in Dataverse |
| Rechnungsdetails | Debitoren-Freitextrechnungspositionen in Dataverse   |

## <a name="entity-flow"></a>Entitätsfluss

Rechnungen, die aus einer Vereinbarung in Field Service erstellt werden, können mit Supply Chain Management über ein Microsoft Dataverse-Datenintegrationsprojekt synchronisiert werden. Aktualisierungen dieser Rechnungen werden mit den Freitextrechnungen in Supply Chain Management synchronisiert, wenn der Buchhaltungsstatus der Freitextrechnungen **In Bearbeitung** ist. Nachdem die Freitextrechnungen in Supply Chain Management gebucht werden und der Buchhaltungsstatus auf **Abgeschlossen** aktualisiert wird, können Sie keine Aktualisierungen aus Field Service mehr synchronisieren.

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung

Die Spalte **Hat Positionen mit Vereinbarungsursprung** ist der Tabelle **Rechnung** hinzugefügt worden. Mithilfe dieser Spalte wird sichergestellt, dass nur Rechnungen synchronisiert werden, die aus einer Vereinbarung erstellt werden. Der Wert entspricht **true**, wenn die Rechnung mindestens eine Rechnungsposition enthält, die ihren Ursprung in einer Vereinbarung hat.

Die Spalte **Hat Positionen mit Vereinbarungsursprung** ist der Tabelle **Rechnungsposition** hinzugefügt worden. Mithilfe dieser Spalte wird sichergestellt, dass nur Rechnungspositionen synchronisiert werden, die aus einer Vereinbarung erstellt werden. Der Wert ist **true**, wenn die Rechnungsposition ihren Ursprung in einer Vereinbarung hat.

**Rechnungsdatum** ist ein Pflichtfeld in Supply Chain Management. Daher muss die Spalte einen Wert in Field Service haben, bevor eine Synchronisierung erfolgt. Um diese Anforderung zu erfüllen, wird die folgende Logik hinzugefügt:

- Wenn die Spalte **Rechnungsdatum** in der Tabelle **Rechnung** leer ist (das heißt, wenn sie keinen Wert hat), wird sie auf das aktuelle Datum festgelegt, wenn eine Rechnungsposition hinzugefügt wird, die ihren Ursprung in einer Vereinbarung hat.
- Der Benutzer kann die Spalte **Rechnungsdatum** ändern. Wenn allerdings der Benutzer versucht, eine Rechnung zu speichern, die ihren Ursprung in einer Vereinbarung hat, erhält er oder sie einen Geschäftsprozessfehler, wenn die Spalte **Rechnungsdatum** auf der Rechnung leer ist.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

### <a name="in-supply-chain-management"></a>In Supply Chain Management

Ein Rechnungsursprung muss für die Integration eingerichtet werden, um die Freitextrechnungen in Supply Chain Management zu unterscheiden, die aus Vereinbarungsrechnungen in Field Service erstellt werden. Wenn eine Rechnung einen Rechnungsursprung des Typs **Vereinbarungsrechnungsintegration** hat, wird das Feld **Externe Rechnungsnummer** in der Kopfzeile der **Verkaufsrechnung** angezeigt.

Außer dass sie im Rechnungskopf angezeigt wird, kann die Information **Externe Rechnungsnummer** verwendet werden, um zu gewährleisten, dass Rechnungen, die aus Field Service-Vereinbarungsrechnungen erstellt werden, während der Rechnungssynchronisierung von Supply Chain Management mit Field Service herausgefiltert werden.

1. Wechseln Sie zu **Debitoren** \> **Einstellungen** \> **Rechnungsursprungscodes**.
2. Wählen Sie **Neu** aus, um einen neuen Rechnungsursprung zu erstellen.
3. Geben Sie im Feld **Rechnungsursprung** einen Namen für den Rechnungsursprung ein, wie beispielsweise **FS**.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein, wie beispielsweise **Field Service-Vereinbarungsrechnung**.
5. Aktivieren Sie das Kontrollkästchen **Ursprungstypzuweisung**.
6. Legen Sie das Feld **Rechnungsursprungstyp** auf **Vereinbarungsrechnungsintegration** fest.
7. Wählen Sie **Speichern**.

### <a name="in-the-data-integration-project"></a>Im Datenenintegrationsprojekt

Aufgabe: **Rechnungspositionen**  

Stellen Sie sicher, dass der Standardwert für das Supply Chain Management-Feld **Hauptkonto-Anzeigewert** aktualisiert wird, um dem gewünschten Wert zu entsprechen.

Der Standardvorlagenwert ist **401100**.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a>Vereinbarungsrechnungen (Field Service an Supply Chain Management): Rechnungskopfzeilen

[![Vorlagenzuordnung in der Datenintegration für Rechnungskopfzeilen.](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a>Vereinbarungsrechnungen (Field Service an Supply Chain Management): Rechnungspositionen

[![Vorlagenzuordnung in der Datenintegration für Rechnungszeilen.](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]