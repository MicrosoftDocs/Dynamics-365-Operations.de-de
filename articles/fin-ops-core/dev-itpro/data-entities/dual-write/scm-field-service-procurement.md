---
title: Integrieren der Beschaffung zwischen Supply Chain Management und Field Service
description: In diesem Thema wird beschrieben, wie die Dual-Write-Integration die Erstellung und Aktualisierung von Bestellungen sowohl über Supply Chain Management als auch Field Service unterstützt.
author: RamaKrishnamoorthy
ms.date: 11/11/2020
ms.topic: article
audience: Application User
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: c29efb885babea833e3c3fde0155e3722f8b77e9
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542390"
---
# <a name="integrate-procurement-between-supply-chain-management-and-field-service"></a>Integrieren der Beschaffung zwischen Supply Chain Management und Field Service

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management bietet robuste Beschaffungsfunktionen. Dynamics 365 Field Service bietet ähnliche Funktionen, die die mit dem Serviceprozess verknüpften Einkaufsprozesse unterstützen. Die Funktionen dieser beiden Apps werden über Dual-Write integriert und die daraus resultierenden funktionsübergreifenden Anwendungsfälle werden durch Tabellenzuordnungen, Lösungslogik, Ansichten und Formulare aktiviert.

Diese Integration unterstützt die Erstellung von Bestellungen und in den meisten Fällen auch Aktualisierungen über beide Apps. Preise, Adressen und Produkteingänge werden jedoch von Supply Chain Management gesteuert. Für Unternehmen, die sowohl Field Service als auch Supply Chain Management verwenden, sind mehrere leistungsstarke funktionsübergreifende Anwendungsfälle aktiviert. Diese Anwendungsfälle ermöglichen die Initiierung und Nachverfolgung von Beschaffungen auf beiden Systemen.

Die folgende Abbildung zeigt die Tabellen in beiden Systemen und wie sie aufeinander abgebildet werden. Bestellungen in Field Service verweisen auf eine *Kontozeile*, während Bestellungen in Supply Chain Management auf eine *Lieferantenzeile* verweisen. Um die Integration aufzulösen, verwendet Dual-Write einen Verweis, um *Lieferantenzeilen* mit *Kontozeilen* zu verknüpfen. Weitere Informationen finden Sie unter [Integrierte Masterdaten von Lieferanten](vendor-mapping.md).

![Zuordnungen für die Beschaffung.](media/scm-field-service-tables.png)

## <a name="prerequisites"></a>Voraussetzungen

Um Supply Chain Management in Field Service zu integrieren, müssen Sie die folgenden Komponenten installieren:

- Field Service Version 8.8.31.60 oder höher für eine umfassende Integration von Bestellungen
- Supply Chain Management Version 10.0.14 oder höher
- Dual-Write, um die OneFSSCM-Lösung auszuführen

## <a name="installation-guidelines"></a>Installationsrichtlinien

### <a name="prerequisites"></a>Voraussetzungen

- **Dual-Write** – Weitere Informationen finden Sie auf der [Dual-Write-Homepage](dual-write-home-page.md#dual-write-setup).
- **Dynamics 365 Field Service** – Weitere Informationen finden Sie unter [Installieren von Dynamics 365 Field Service](/dynamics365/field-service/install-field-service#step-1-install-dynamics-365-field-service).

Wenn sie in Microsoft Dataverse aktiviert sind, führen Dual-Write und Field Service mehrere Lösungsebenen ein, die die Umgebung mit neuen Metadaten, Formularen, Ansichten und Logik erweitern. Diese Lösungen können in beliebiger Reihenfolge aktiviert werden, obwohl Sie sie normalerweise in der hier angegebenen Reihenfolge installieren:

1. **Field Service Common** – Field Service Common wird installiert, wenn Field Service in der Umgebung installiert ist.
2. **Field Service (Anchor)** – Field Service (Anchor) wird installiert, wenn Field Service in der Umgebung installiert ist. 
3. **Supply Chain Management Extended** – Supply Chain Management Extended wird automatisch installiert, wenn Dual-Write in einer Umgebung aktiviert ist. 
4. **OneFSSCM-Lösung** – OneFSSCM wird automatisch von der zuletzt installierten Lösung (Field Service oder Supply Chain Management) installiert.

    - Wenn Field Service bereits in der Umgebung installiert ist und Sie Dual-Write aktivieren, wodurch Supply Chain Management Extended installiert wird, wird OneFSSCM installiert.
    - Wenn Supply Chain Management Extended bereits in der Umgebung installiert ist und Sie Field Service installieren, wird OneFSSCM installiert.

## <a name="initial-synchronization"></a>Erstsynchronisierung

Um neue Bestellungen zu erstellen und mit vorhandenen Bestellungen zu arbeiten, müssen Sie die Referenzdaten zwischen Supply Chain Management und Dataverse synchronisieren. Sie verwenden die anfängliche Schreibfunktion, um die Tabellenbeziehungen zu erkennen und die Tabellen zu finden, die Sie für eine bestimmte Zuordnung aktivieren müssen.

Sie müssen die folgenden Tabellen synchronisieren:

- Produktvorlagen

    Wenn Sie den ersten Schreibvorgang ausführen, erhalten Sie eine vollständige Liste der erforderlichen Tabellen. Beispiele für diese Vorlagen:

    - Alle Produkte
    - Freigegebene Produkte V2
    - Von Dataverse freigegebene eindeutig identifizierbare Produkte

- Standorte
- Lagerorte
- Vorlagen für Beschaffungskategorien

    Beispiele für diese Vorlagen:

    - Beschaffungskategorien
    - Pro
    - Produktkategoriehierarchie
    - Produktkategoriezuweisungen

- Lieferantenvorlagen, z. B. Lieferant V2
- Vorlagen für Kontaktpersonen, z. B. Dataverse-Kontakte V2
- Arbeitskraftvorlagen, z. B. Arbeitskraft

Durch die Synchronisierung der Tabellen wird sichergestellt, dass alle Dokumente (Bestellungen und Produktzugänge) in Supply Chain Management in Dataverse verfügbar sind.

### <a name="account-and-vendor-tables"></a>Konto- und Lieferantentabellen

Bestellungen in Field Service basieren auf der Kontotabelle, um Lieferanten zu verfolgen. Deshalb verwenden die Dataverse-Tabellen für Bestellungen Konten, um Kredtitoren zu verfolgen. Um diesen entscheidenden Unterschied auszugleichen, müssen die folgenden vier Workflows aktiviert werden, um die Konten und Lieferanten synchron zu halten: 

- Lieferanten in der Kontotabelle erstellen
- Lieferanten in der Lieferantentabelle erstellen
- Lieferanten in der Kontotabelle aktualisieren
- Lieferanten in der Lieferantentabelle aktualisieren

Wenn OneFSSCM installiert ist, da sowohl Field Service als auch Supply Chain Management Extended installiert sind, werden diese Workflows automatisch aktiviert. Wenn Field Service nicht installiert ist, Sie aber die Bestellungstabellen in Dataverse integrieren möchten, müssen Sie diese Workflows aktivieren. In beiden Fällen müssen Sie möglicherweise sicherstellen, dass vor der Erstellung von Bestellungen alle Lieferanten als Konten in Dataverse erstellt werden, sofern Sie nicht bei Null beginnen. Andernfalls können Fehler auftreten.

### <a name="initial-synchronization"></a>Erstsynchronisierung

Nachdem alle Voraussetzungen erfüllt sind, müssen Sie eine erste Synchronisierung der folgenden Vorlagen durchführen, wenn bestehende Bestellungen und Produktzugänge in beiden Systemen verfügbar sein sollen:

- Bestellkopf V2
- CDS-Bestellungsposition
- CDS-Bestellungsposition weich löschen
- Bestellungszugang
- Produktzugang für Bestellung

## <a name="mappings-with-logic"></a>Zuordnungen mit Logik

Die Beschaffungsintegration erweitert die Produktzuordnung um die folgende Logik, um sicherzustellen, dass die Spalte **Produkttyp Field Service** in der Produkttabelle in Dataverse korrekt festgelegt wird:

- Wenn **Produkttyp** auf *Produkt* festgelegt ist und **Artikelmodellgruppe, Gelagertes Produkt** auf *True*, wird **Produkttyp Field Service** auf *Bestandsware* festgelegt.
- Wenn **Produkttyp** auf *Produkt* festgelegt ist und **Artikelmodellgruppe, Gelagertes Produkt** auf *False*, wird **Produkttyp Field Service** auf *Nicht-Bestandsware* festgelegt.
- Wenn **Produkttyp** auf *Dienstleistung* festgelegt ist, wird **Produkttyp Field Service** auf *Dienstleistung* festgelegt.

Des Weiteren beinhaltet Dataverse eine Logik, die Lieferanten ihren zugehörigen Konten zuordnet. Diese Logik legt das Standardkonto des Rechnungslieferanten fest. Beim Erstellen legt die serverseitige Plug-In-Logik das Standardkonto des Rechnungslieferanten fest, der zu dem Konto gehört. Der Lieferant hat einen Verweis auf das Rechnungskonto, mit dem dieser Wert festgelegt wird.

## <a name="supported-scenarios"></a>Unterstützte Szenarien

- Bestellungen können von Dataverse-Benutzern erstellt und aktualisiert werden. Der Prozess und die Daten werden jedoch von Supply Chain Management gesteuert. Die Einschränkungen für Aktualisierungen von Bestellungsspalten in Supply Chain Management gelten, wenn Aktualisierungen aus Field Service stammen. Beispielsweise können Sie eine Bestellung nicht aktualisieren, wenn sie abgeschlossen wurde. 
- Wenn die Bestellung vom Änderungsmanagement in Supply Chain Management gesteuert wird, kann ein Field Service-Benutzer die Bestellung nur aktualisieren, wenn der Genehmigungsstatus für Supply Chain Management *Entwurf* lautet.
- Einige Spalten werden nur von Supply Chain Management verwaltet und können in Field Service nicht aktualisiert werden. Überprüfen Sie die Zuordnungstabellen im Produkt, um zu sehen, welche Spalten nicht aktualisiert werden können. Der Einfachheit halber sind die meisten dieser Spalten auf Dataverse-Seiten schreibgeschützt. 

    Beispielsweise werden die Spalten für Preisinformationen von Supply Chain Management verwaltet. Supply Chain Management verfügt über Handelsabkommen, von denen Field Service profitieren kann. Spalten wie **Preis je Einheit**, **Rabatt** und **Nettobetrag** stemmen ausschließlich aus Supply Chain Management. Um sicherzustellen, dass der Preis mit Field Service synchronisiert wird, sollten Sie die Funktion **Synchronisieren** auf den Seiten **Bestellung** und **Bestellprodukt** in Dataverse verwenden, wenn Bestellungsdaten eingegeben wurden. Weitere Informationen finden Sie unter [Synchronisieren mit den Beschaffungsdaten in Dynamics 365 Supply Chain Management bei Bedarf](#sync-procurement).

- Die Spalte **Summen** ist nur in Field Service verfügbar, da in Supply Chain Management keine aktuellen Summen der Bestellung vorhanden sind. Die Summen in Supply Chain Management werden basierend auf mehreren Parametern berechnet, die in Field Service nicht verfügbar sind.
- Bestellpositionen, in denen nur eine Beschaffungskategorie angegeben ist oder in denen das angegebene Produkt ein Artikel des Produkttyps *Dienstleistung* oder des Field Service-Produkttyps ist, können nur in Supply Chain Management initiiert werden. Die Positionen werden dann mit Dataverse synchronisiert und sind in Field Service sichtbar.
- Wenn nur Field Service installiert ist und Supply Chain Management nicht, ist die Spalte **Lagerort** auf der Bestellung obligatorisch. Wenn Supply Chain Management jedoch installiert ist, wird diese Anforderung gelockert, da Supply Chain Management Bestellpositionen ermöglicht, für die in bestimmten Situationen kein Lagerort angegeben ist.
- Produktzugänge (Bestellungszugänge in Dataverse) werden von Supply Chain Management verwaltet und können nicht mit Dataverse erstellt werden, wenn Supply Chain Management installiert ist. Die Produktzugänge von Supply Chain Management werden von Supply Chain Management zu Dataverse synchronisiert.
- In Supply Chain Management ist eine Unterlieferung zulässig. Die OneFSSCM-Lösung fügt Logik hinzu, sodass beim Erstellen oder Aktualisieren der Produktzugangsposition (oder des Bestellzugangsprodukts in Dataverse) eine Bestandserfassungszeile in Dataverse erstellt, um die verbleibende Menge anzupassen, die für Unterlieferungsszenarien bestellt wurde.

## <a name="unsupported-scenarios"></a>Nicht unterstützte Szenarien

- Field Service verhindert, dass einer stornierten Bestellung in Supply Chain Management Positionen hinzugefügt werden. Um dieses Problem zu umgehen, können Sie den Systemstatus der Bestellung in Field Service ändern und dann die neue Position entweder in Field Service oder in Supply Chain Management hinzufügen.
- Obwohl Beschaffungszeilen die Bestandsebenen in beiden Systemen beeinflussen, gewährleistet diese Integration keine Bestandsausrichtung zwischen Supply Chain Management und Field Service. Sowohl Field Service als auch Supply Chain Management verfügen über andere Prozesse, mit denen die Bestandsebenen aktualisiert werden. Diese Prozesse fallen nicht in den Bereich der Beschaffung.

## <a name="status-management"></a>Statusverwaltung

Der Status von Bestellungen in Field Service unterscheidet sich vom Status in Supply Chain Management.

### <a name="field-service-purchase-order-and-purchase-order-product-statuses"></a>Status der Bestellung und des Bestellprodukts in Field Service

| Kopfzeile – Systemstatus | Kopfzeile – Genehmigungsstatus | Artikelstatus |
|---|---|---|
| <ul><li>Übersicht</li><li>Übermittelt</li><li>Storniert</li><li>Produkt erhalten</li><li>Fakturiert</li></ul> | <ul><li>NULL</li><li>Genehmigt</li><li>Verweigert</li></ul> | <ul><li>Ausstehend</li><li>Eingegangen</li><li>Storniert</li></ul> |

### <a name="supply-chain-management-purchase-order-and-purchase-order-line-statuses"></a>Status der Bestellung und der Bestellposition in Supply Chain Management

Genehmigungsstatus für Positionen sind nur aktiv, wenn ein Positionsworkflow vorhanden ist.

| Kopfzeile – Dokumentstatus | Kopfzeile – Genehmigungsstatus | Positionsstatus | Genehmigungsstatus der Position |
|---|---|---|---|
| <ul><li>Offene Bestellung (Nachbestellung)</li><li>Eingegangen</li><li>Fakturiert</li><li>Storniert</li></ul> | <ul><li>Übersicht</li><li>In Überprüfung</li><li>Genehmigt</li><li>Verweigert</li><li>In externer Überprüfung</li><li>Bestätigt</li><li>Zum Abschluss gebracht</li></ul> | <ul><li>Offene Bestellung (Nachbestellung)</li><li>Eingegangen</li><li>Fakturiert</li><li>Storniert</li></ul> | <ul><li>Nicht übermittelt</li><li>In Überprüfung</li><li>Genehmigt</li><li>Verweigert</li></ul> |

Die folgenden Regeln werden auf die Statusspalten angewendet:

- Der Status in Supply Chain Management kann nicht über Field Service aktualisiert werden. In einigen Fällen wird der Status in Field Service jedoch aktualisiert, wenn der Status der Bestellung in Supply Chain Management geändert wird.
- Wenn sich eine Bestellung in Supply Chain Management im Änderungsmanagement befindet und eine Änderung verarbeitet wird, lautet der Genehmigungsstatus *Entwurf* oder *Wird überprüft*. In diesem Fall wird der Genehmigungsstatus in Field Service auf *Null* gesetzt.
- Wenn der Genehmigungsstatus der Bestellung in Supply Chain Management auf *Genehmigt*, *In externer Überprüfung*, *Bestätigt* oder *Abgeschlossen* festgelegt ist, wird der Genehmigungsstatus der Bestellung in Field Service auf *Genehmigt* festgelegt.
- Wenn der Genehmigungsstatus der Bestellung in Supply Chain Management auf *Abgelehnt* festgelegt ist, wird der Genehmigungsstatus der Bestellung in Field Service auf *Abgelehnt* festgelegt.
- Wenn der Status des Dokumentkopfes in Supply Chain Management in *Offene Bestellung (Nachbestellung)* geändert wird und der Status der Bestellung in Field Service *Entwurf* oder *Storniert* lautet, wird der Status der Bestellung in Field Service in *Übermittelt* geändert.
- Wenn der Status des Dokumentkopfes in Supply Chain Management in *Storniert* geändert wird und der Bestellung in Field Service kein Produktzugang zugeordnet ist (über Bestellprodukte), wird der Systemstatus in Field Service auf *Storniert* festgelegt.
- Wenn der Status der Bestellposition in Supply Chain Management *Storniert* lautet, wird der Status des Bestellprodukts in Field Service auf *Storniert* festgelegt. Darüber hinaus wird, wenn der Status der Bestellposition in Supply Chain Management von *Storniert* in *Nachbestellung* geändert wird, der Status des Einkaufsartikels in der Bestellung in Field Service auf *Ausstehend* festgelegt.

## <a name="sync-with-the-supply-chain-management-procurement-data-on-demand"></a><a id="sync-procurement"></a>Synchronisieren mit den Beschaffungsdaten von Supply Chain Management bei Bedarf

Supply Chain Management umfasst Beschaffungsdaten, die Handelsabkommen, Rabatte und andere Szenarien behandeln, die auf sekundären Prozessen in Supply Chain Management beruhen. Das Beschaffungsmodul verwendet komplexe Regeln, um den besten Preis für eine bestimmte Bestellung zu ermitteln. Wenn Sie Dual-Write verwenden, werden Daten in beiden Umgebungen nicht immer synchron gehalten, insbesondere in Szenarien, in denen die Zeile über Dataverse erstellt oder aktualisiert wurde, und es können Folgeprozesse in Supply Chain Management ausgelöst werden.

## <a name="sync-the-procurement-data-from-supply-chain-management"></a>Synchronisieren der Beschaffungsdaten von Supply Chain Management

1. Wechseln Sie in Dataverse zu **Bestand \> Bestellung**.
2. Wählen Sie **Neu** aus, um eine neue Bestellung zu erstellen, oder wählen Sie die Zeile für eine bestehende Bestellung aus.
3. Aus der Bestellung oder der Bestellposition.
4. Wählen Sie im Aktionsbereich **Synchronisieren** aus.

Alle Spalten aus Dataverse und Field Service, die von Supply Chain Management gemeinsam genutzt werden, werden synchronisiert.

Hier sind die Situationen, in denen Sie die Funktion **Synchronisieren** verwenden könnten:

- Wenn Sie mehrere aufeinanderfolgende Änderungen an derselben Zeile aus Dataverse vornehmen, führen Sie die Funktion **Synchronisieren** aus.
- Wenn Sie nicht sicher sind, ob eine Änderung die zweite Änderung in Folge aus Dataverse sein könnte, ist es eventuell sinnvoll, die Funktion **Synchronisieren** auszuführen.
- Wenn Sie eine Fehlermeldung zur Aktualisierung eines Werts aus Supply Chain Management erhalten, führen Sie die Funktion **Synchronisieren** aus und wiederholen Sie anschließend die Aktualisierung in Dataverse.

## <a name="cancelling-the-posting-process"></a>Stornieren des Buchungsvorgangs

Wenn der Buchungsvorgang für den Produktzugang während der Verarbeitung abgebrochen wird, wird von Dual-Write möglicherweise eine Produktzugangszeile in Dataverse erstellt, nicht jedoch in Supply Chain Management. Diese Situation tritt auf, weil Dual-Write verteilte Transaktionen nicht unterstützt.

## <a name="templates"></a>Vorlagen

Die folgenden Vorlagen stehen für die Integration von beschaffungsbezogenen Dokumenten zur Verfügung.

| Lieferkettenverwaltung | Field Service | Beschreibung |
|---|---|---|
| [Bestellkopf V2](mapping-reference.md#183) | msdyn\_Purchaseorders | Diese Tabelle enthält die Spalten, die den Bestellkopf darstellen. |
| [Bestellpositionsentität](mapping-reference.md#181) | msdyn\_PurchaseOrderProducts | Diese Tabelle enthält die Zeilen, die den Positionen in einer Bestellung entsprechen. Die Produktnummer wird zur Synchronisierung verwendet. Dies identifiziert das Produkt als Lagermengeneinheit (SKU), inklusive der Produktabmessungen. Weitere Informationen zur Produktintegration mit Dataverse finden Sie unter [Einheitliche Produktumgebung](product-mapping.md). |
| [Produktzugangskopfzeile](mapping-reference.md#185) | msdyn\_purchaseorderreceipts | Diese Tabelle enthält die Produktzugangsköpfe, die erstellt werden, wenn ein Produktzugang in Supply Chain Management gebucht wird. |
| [Produktzugangsposition](mapping-reference.md#184) | msdyn\_purchaseorderreceiptproducts | Diese Tabelle enthält die Produktzugangspositionen, die erstellt werden, wenn ein Produktzugang in Supply Chain Management gebucht wird. |
| [Entität einer Auftragsposition weich gelöscht](mapping-reference.md#182) | msdyn\_purchaseorderproducts | Diese Tabelle enthält Informationen zu Bestellpositionen, die weich gelöscht werden. Eine Bestellposition in Supply Chain Management kann nur dann weich gelöscht werden, wenn die Bestellung bei aktiviertem Änderungsmanagement bestätigt oder genehmigt wurde. Die Zeile ist in der Datenbank von Supply Chain Management vorhanden und als **Wird gelöscht** gekennzeichnet. Da es in Dataverse das Konzept des weichen Löschens nicht gibt, müssen diese Informationen unbedingt nach Dataverse synchronisiert werden. Auf diese Weise können Positionen, die in Supply Chain Management weich gelöscht werden, automatisch aus Dataverse gelöscht werden. In diesem Fall befindet sich die Logik zum Löschen einer Position in Dataverse in Supply Chain Management Extended. |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
