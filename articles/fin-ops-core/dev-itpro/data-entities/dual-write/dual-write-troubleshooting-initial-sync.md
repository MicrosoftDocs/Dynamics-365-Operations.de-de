---
title: Probleme bei der anfänglichen Synchronisierung behandeln
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Synchronisierung zusammenhängen.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 241277ada768cc6497035cc377d0e158646a42d6
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781113"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Probleme bei der anfänglichen Synchronisierung behandeln

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse. Dieses Thema enthält insbesondere Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Synchronisierung zusammenhängen.

> [!IMPORTANT]
> Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Überprüfen Sie eine Finance and Operations App auf anfängliche Synchronisationsfehler

Nachdem Sie die Zuordnungsvorlagen aktiviert haben, sollte der Status der Zuordnungen lauten **Laufen**. Wenn der Status ist **Nicht ausgeführt** angezeigt wird, sind bei der ersten Synchronisierung Fehler aufgetreten. Um die Fehler anzuzeigen, wählen Sie die **Anfängliche Synchronisierungsdetail** Registerkarte auf der **Duales Schreiben** Seite.

![Fehler auf der Registerkarte Details zur Erstsynchronisierung.](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Sie können die anfängliche Synchronisierung nicht abschließen: 400 Bad Request

**Erforderliche Rolle zum Beheben der Fehler:** System Administrator

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, das Mapping und die anfängliche Synchronisierung auszuführen:

*(\[Bad Request \], Der Remote-Server hat einen Fehler zurückgegeben: (400) Bad Request.), AX Export ist auf einen Fehler gestoßen.*

Hier ist ein Beispiel für die vollständige Fehlernachricht.

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

Wenn dieser Fehler konsistent auftritt und Sie die anfängliche Synchronisierung nicht abschließen können, führen Sie die folgenden Schritte aus, um das Problem zu beheben.

1. Melden Sie sich bei der virtuellen Maschine (VM) für die Finance and Operations App an.
2. Öffnen Sie die Microsoft Management Console.
3. In dem Bereich **Dienstleistungen** stellen Sie sicher, dass der Microsoft Dynamics 365 Data Import Export Framework-Dienst wird ausgeführt. Starten Sie ihn neu, wenn er gestoppt wurde, da die anfängliche Synchronisierung dies erfordert.

## <a name="initial-synchronization-error-403-forbidden"></a>Anfänglicher Synchronisationsfehler: 403 Forbidden

Während der ersten Synchronisierung wird möglicherweise die folgende Fehlermeldung angezeigt:

*(\[Forbidden\], der Remote-Server hat einen Fehler zurückgegeben: (403) Forbidden.), AX beim Export ist ein Fehler aufgetreten*

Führen Sie folgende Schritte aus, um das Problem zu beheben.

1. Bei der Finance and Operations App anmelden.
2. Auf der **Azure Active Directory Anwendungen** Seite löschen Sie den **DtAppID** Client, und fügen Sie ihn dann erneut hinzu.

![DtAppID-Client in der Liste von Azure AD Anwendungen.](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Selbstreferenzfehler oder Zirkelreferenzfehler während der ersten Synchronisation

Möglicherweise wird eine Fehlernachricht angezeigt, die dem folgenden Beispiel ähnelt, wenn eine Ihrer Zuordnungen Selbstreferenzen oder Zirkelreferenzen enthält: Die Fehler fallen in folgende Kategorien:

- [Fehler in der Tabellenzuordnung Lieferanten V2 zu msdyn_vendors](#error-vendor-map)
- [Fehler in der Tabellenzuordnung Kunden V3 zu Konten](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>Fehler in der Tabellenzuordnung von Lieferanten V2 zu msdyn_vendors beheben

Möglicherweise treten auf dem Computer die folgenden anfänglichen Synchronisierungsfehler für die Zuordnung **Kreditoren V2** zu **msdyn\_vendors** auf, wenn die Tabellen vorhandene Zeilen mit Werten in den Spalten **PrimaryContactPersonId** und **InvoiceVendorAccountNumber** haben. Diese Fehler passieren, weil **InvoiceVendorAccountNumber** eine selbstreferenzierende Spalte ist und **PrimaryContactPersonId** eine Zirkelreferenz in der Kreditorenzuordnung ist.

Die Fehlermeldungen, die Sie erhalten, haben das folgende Formular.

*Die Anleitung für das Feld konnte nicht aufgelöst werden: \<field\>. Die Suche wurde nicht gefunden: \<value\>. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Im Folgenden finden Sie einige Beispiele hierfür:

- *Die Anleitung für das Feld konnte nicht aufgelöst werden: msdy\_vendorprimarycontactperson.msdyn\_contactpersonid. Die Suche wurde nicht gefunden: 000056. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Die Anleitung für das Feld konnte nicht aufgelöst werden: msdyn\_.invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Die Suche wurde nicht gefunden: V24-1. Testen Sie diese URL(s), um zu prüfen, ob die Referenzdaten vorhanden sind: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Wenn Sie Zeilen mit Werten in der Kreditorentabelle in den Spalten **PrimaryContactPersonID** und **InvoiceVendorAccountNumber** haben, führen Sie die Schritte im folgenden Abschnitt aus, um die erste Synchronisierung erfolgreich abzuschließen.

1. In der Finance and Operations-App löschen Sie die Spalten **PrimaryContactPersonId** und **InvoiceVendorAccountNumber** aus der Zuordnung, und speichern Sie die Änderungen.

    1. Wählen Sie auf der Zuordnungsseite für duales Schreiben für **Lieferant V2 (msdyn\_vendors)** auf der Registerkarte **Tabellenzuordnungen** im linken Filter **Finance and Operations apps.Vendors V2** aus. Wählen Sie im rechten Filter **Sales.Vendor**.
    2. Suchen Sie nach **primarycontactperson**, um das Quellfeld **PrimaryContactPersonId** zu finden.
    3. Wählen Sie **Aktionen** und dann **Löschen**.

        ![Löschen der Spalte „PrimaryContactPersonId“.](media/vend_selfref3.png)

    4. Wiederholen Sie diese Schritte, um die Spalte **InvoiceVendorAccountNumber** zu löschen.

        ![Löschen des Feldes „InvoiceVendorAccountNumber“.](media/vend-selfref4.png)

    5. Speichern Sie Ihre Änderungen am Mapping.

2. Deaktivieren Sie die Änderungsverfolgung für die Tabelle **Kreditoren V2**.

    1. Im Arbeitsbereich **Datenmanagement** wählen Sie die Kachel **Datentabellen** aus.
    2. Wählen Sie die Tabelle **Kreditoren V2** aus.
    3. Wählen Sie im Aktionsbereich **Optionen** und wählen Sie dann **Änderungsnachverfolgung**.

        ![Auswahl der Option Änderungsnachverfolgung ändern.](media/selfref_options.png)

    4. Wählen Sie **Änderungsverfolgung deaktivieren**.

        ![Wählen Sie Änderungsnachverfolgung deaktivieren.](media/selfref_tracking.png)

3. Führen Sie die erste Synchronisierung erneut für die **Anbieter V2** (msdyn\_vendors) Zuordnung aus. Die erstmalige Synchronisierung sollte ohne Fehler erfolgreich ausgeführt werden.
4. Führen Sie die erste Synchronisierung für **CDS-Kontakte V2 (Kontakte)** Zuordnung aus. Sie müssen diese Zuordnung synchronisieren, wenn Sie die Spalte des primären Kontakts in der Tabelle der Kreditoren synchronisieren möchten, da die Kontaktzeilen zunächst synchronisiert werden müssen.
5. Fügen Sie die Spalten **PrimaryContactPersonId** und **InvoiceVendorAccountNumber** wieder der **Kreditor V2 (msdyn\_vendors)** Zuordnung hinzu, und speichern Sie die Zuordnung.
6. Führen Sie die erste Synchronisierung noch einmal für die **Anbieter V2** (msdyn\_vendors) Zuordnung aus. Weil die Änderungsnachverfolgung deaktiviert ist, werden alle Zeilen synchronisiert.
7. Aktivieren Sie die Änderungsnachverfolgung für die Tabelle **Kreditor V2**.

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>Beheben von Fehlern in der Tabellenzuordnung von Kunden V3 zu Konten

Möglicherweise treten auf dem Computer die folgenden anfänglichen Synchronisierungsfehler von **Debitoren V3** zu **Konten** auf, wenn die Tabellen vorhandene Zeilen mit Werten in den Spalten **ContactPersonID** und **InvoiceAccount** haben. Diese Fehler passieren, weil **InvoiceAccount** eine selbstreferenzierende Spalte ist und **ContactPersonId** eine Zirkelreferenz in der Kreditorenzuordnung ist.

Die Fehlermeldungen, die Sie erhalten, haben das folgende Formular.

*Die Anleitung für das Feld konnte nicht aufgelöst werden: \<field\>. Die Suche wurde nicht gefunden: \<value\>. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Im Folgenden finden Sie einige Beispiele hierfür:

- *Die Anleitung für das Feld konnte nicht aufgelöst werden: primarycontactid.msdyn\_contactpersonid. Die Suche wurde nicht gefunden: 000056. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Die Anleitung für das Feld konnte nicht aufgelöst werden: msdyn\_billingaccount.accountnumber. Die Suche wurde nicht gefunden: 1206-1. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Wenn Sie Zeilen mit Werten in der Debitorentabelle in den Spalten **ContactPersonID** und **InvoiceAccount** haben, führen Sie die Schritte im folgenden Abschnitt aus, um die erste Synchronisierung erfolgreich abzuschließen. Sie können diesen Ansatz für alle sofort einsatzbereiten Tabellen wie **Konten** und **Kontakte** verwenden.

1. In der Finance and Operations-App löschen Sie Spalten **ContactPersonID** und **InvoiceAccount** aus der Zuordnung **Debitoren V3 (Konten)**, und speichern Sie dann die Zuordnung.

    1. Wählen Sie auf der Zuordnungsseite für duales Schreiben für **Kunden V3 (Konten)** auf der Registerkarte **Tabellenzuordnungen** im linken Filter **Finance and Operations app.Customers V3** aus. Wählen Sie im rechten Filter **Dataverse Konto**.
    2. Suchen Sie nach **contactperson**, um die Quellspalte **ContactPersonID** zu finden.
    3. Wählen Sie **Aktionen** und dann **Löschen**.

        ![Löschen der Spalte „ContactPersonID“.](media/cust_selfref3.png)

    4. Wiederholen Sie diese Schritte, um die Spalte **InvoiceAccount** zu löschen.

        ![Löschen der Spalte „InvoiceAccount“.](media/cust_selfref4.png)

    5. Speichern Sie Ihre Änderungen am Mapping.

2. Deaktivieren Sie die Änderungsverfolgung für die Tabelle **Debitoren V3**.

    1. Im Arbeitsbereich **Datenmanagement** wählen Sie die Kachel **Datentabellen** aus.
    2. Wählen Sie die Tabelle **Debitoren V3** aus.
    3. Wählen Sie im Aktionsbereich **Optionen** und wählen Sie dann **Änderungsnachverfolgung**.

        ![Auswahl der Option Änderungsnachverfolgung ändern.](media/selfref_options.png)

    4. Wählen Sie **Änderungsverfolgung deaktivieren**.

        ![Wählen Sie Änderungsnachverfolgung deaktivieren.](media/selfref_tracking.png)

3. Führen Sie die erste Synchronisierung nochmals für die **Debitoren V3 (Konten)** Zuordnung aus. Die erstmalige Synchronisierung sollte ohne Fehler erfolgreich ausgeführt werden.
4. Führen Sie die erste Synchronisierung für **CDS-Kontakte V2 (Kontakte)** Zuordnung aus.

    > [!NOTE]
    > Es gibt zwei Karten mit demselben Namen. Stellen Sie sicher, dass Sie jene Zuordnung mit der folgenden Beschreibung auf der Registerkarte **Details** auswählen: **Duales Schreiben für die Synchronisierung zwischen FO.CDS-Kontakten V2 und CDS.Contacts. Benötigt neues Paket \[Dynamics365SupplyChainExtended\]**.

5. Fügen Sie die Spalten **InvoiceAccount** und **ContactPersonID** wieder der Zuordnung **Debitoren V3 (Konten)** hinzu, und speichern Sie dann die Zuordnung. Jetzt sind die Spalte **InvoiceAccount** und die Spalte **ContactPersonID** wieder Teil des Live-Synchronisationsmodus. Im nächsten Schritt machen Sie die anfängliche Synchronisierung für diese Spalten.
6. Führen Sie die erste Synchronisierung noch einmal für die **Debitoren V3 (Konten)** Zuordnung aus. Da die Änderungsverfolgung deaktiviert ist, werden die Daten für **InvoiceAccount** und **ContactPersonId** von der Finance and Operations App zu Dataverse synchronisiert.
7. Um die Daten für **Rechnungskonto** und **ContactPersonId** von Dataverse zu Finance and Operations zu synchronisieren, müssen Sie ein Datenintegrationsprojekt verwenden.

    1. Erstellen Sie in Power Apps ein Datenintegrationsprojekt zwischen den Tabellen **Sales.Account** und **Finance and Operations apps.Customers V3**. Die Datenrichtung muss von Dataverse zu Finance and Operations App sein. Weil **Rechnungskonto** ein neues Attribut in dualem Schreiben ist, wollen Sie möglicherweise die anfängliche Synchronisierung dazu überspringen. Weitere Informationen finden Sie unter [Datenintegration in Dataverse](/power-platform/admin/data-integrator).

        Das folgende Illustration zeigt ein Projekt, das **Kundenkonto** und **ContactPersonId** aktualisiert.

        ![Datenintegrationsprojekt zum Aktualisieren von CustomerAccount und ContactPersonId.](media/cust_selfref6.png)

    2. Fügen Sie die Firmenkriterien im Filter auf der Seite von Dataverse ein, da nur die Zeilen, die den Filterkriterien entsprechen, in der Finance and Operations-App aktualisiert werden. Wählen Sie zum Hinzufügen die Schaltfläche Filter. In dem Dialog **Abfrage bearbeiten** können Sie eine Filterabfrage hinzufügen wie **\_msdyn\__company\_value eq\<guid\>**.

        > [HINWEIS] Wenn die Schaltfläche Filter nicht vorhanden ist, erstellen Sie ein Support-Ticket, um das Datenintegrationsteam zu bitten, die Filterfunktion für Ihren Mandanten zu aktivieren.

        Wenn Sie keine Filterabfrage für **\_msdyn\_company\_value** eingeben, werden alle Zeilen synchronisiert.

        ![Hinzufügen einer Filterabfrage.](media/cust_selfref7.png)

    Die anfängliche Synchronisierung der Zeilen ist nun abgeschlossen.

8. Aktivieren Sie die Änderungsnachverfolgung in Finance and Operations für die Tabelle **Debitoren V3**.

## <a name="initial-sync-failures-on-maps-with-more-than-10-lookup-fields"></a>Anfängliche Sync-Fehler bei Zuordnungen mit mehr als 10 Nachschlagefeldern

Sie erhalten möglicherweise die folgende Fehlermeldung, wenn Sie versuchen, eine anfängliche Synchronisierung für **Kunden V3 - Konten**, **Verkaufsaufträge**-Zuordnungen oder eine beliebige Zuordnung mit mehr als 10 Nachschlagefeldern auszuführen:

*CRMExport: Paketausführung abgeschlossen. Fehlerbeschreibung 5 Versuche, Daten von https://xxxxx//datasets/yyyyy/tables/accounts/items?$select=accountnumber, address2_city, address2_country, ... (msdyn_company/cdm_companyid eq 'id')&$orderby=accountnumber asc schlug fehl.*

Aufgrund der Nachschlagefeld-Beschränkung der Abfrage schlägt die anfängliche Synchronisierung fehl, wenn die Zuordnung der Entitäten mehr als 10 Nachschlagefelder enthält. Weitere Informationen finden Sie unter [Abrufen von Datensätzen der Bezugstabelle mit einer Abfrage](/powerapps/developer/common-data-service/webapi/retrieve-related-entities-query).

Um dieses Problem zu beheben, führen Sie die folgenden Schritte aus:

1. Entfernen Sie optionale Nachschlagefelder aus der Dual-Write-Entitätszuordnung, so dass die Anzahl der Nachschlagefelder 10 oder weniger beträgt.
2. Speichern Sie die Zuordnung und führen Sie die erste Synchronisierung durch.
3. Wenn die initiale Synchronisierung für den ersten Schritt erfolgreich ist, fügen Sie die restlichen Nachschlagefelder hinzu und entfernen die Nachschlagefelder, die Sie im ersten Schritt synchronisiert haben. Stellen Sie sicher, dass die Anzahl der Nachschlagefelder 10 oder weniger beträgt. Speichern Sie die Zuordnung und führen Sie die erste Synchronisierung aus.
4. Wiederholen Sie diese Schritte, bis alle Nachschlagefelder synchronisiert sind.
5. Fügen Sie alle Nachschlagefelder wieder zur Zuordnung hinzu, speichern Sie die Zuordnung und führen Sie die Zuordnung mit **Anfangssynchronisation überspringen** aus.

Durch diesen Vorgang wird die Zuordnung für den Live-Sync-Modus aktiviert.

## <a name="known-issue-during-initial-sync-of-party-postal-addresses-and-party-electronic-addresses"></a>Bekanntes Problem bei der Erstsynchronisation von postalischen Adressen der Partei und elektronischen Adressen der Partei

Wenn Sie versuchen, die initiale Synchronisation von Postadressen der Partei und elektronischen Adressen der Partei auszuführen, erhalten Sie möglicherweise die folgende Fehlermeldung:

*Partei-Nummer konnte nicht in Dataverse gefunden werden.*

Es gibt einen auf **DirPartyCDSEntity** festgelegten Bereich in Finance and Operations Apps, der Parteien vom Typ **Person** und **Organisation** filtert. Infolgedessen wird eine anfängliche Synchronisierung der Zuordnung **CDS-Parteien - msdyn_parties** keine Parteien anderer Typen zuordnen, einschließlich **Juristische Entität** und **Betriebseinheit**. Wenn die anfängliche Synchronisierung für **CDS Partei Postadressen (msdyn_partypostaladdresses)** oder **Partei Kontakte V3 (msdyn_partyelectronicaddresses)** ausgeführt wird, erhalten Sie möglicherweise den Fehler.

Wir arbeiten an einer Korrektur, um den Parteitypenbereich auf der Entität Finance and Operations zu entfernen, so dass Parteien aller Typen erfolgreich auf Dataverse synchronisiert werden können.

## <a name="are-there-any-performance-issues-while-running-initial-sync-for-customers-or-contacts-data"></a>Gibt es Leistungsprobleme beim Ausführen der anfänglichen Synchronisierung für Kunden oder Kontakte?

Wenn Sie die Erstsynchronisation für **Kunden**-Daten ausgeführt haben und die **Kunden**-Zuordnungen laufen haben und dann die Erstsynchronisation für **Kontakte**-Daten ausführen, kann es zu Leistungsproblemen beim Einfügen und Aktualisieren der **LogistikPostalAdresse**- und **LogistikElektronischeAdresse**-Tabellen für **Kontakte**-Adressen kommen. Die gleichen globalen Postadress- und elektronischen Adresstabellen werden für **CustomerV3Entity** und **VendVendorV2Entity** verfolgt und Dual-Write versucht, weitere Abfragen zu erstellen, um Daten auf die andere Seite zu schreiben. Wenn Sie die initiale Synchronisierung für **Debitor** bereits ausgeführt haben, dann stoppen Sie die entsprechende Zuordnung, während Sie die initiale Synchronisierung für **Kontakte**-Daten ausführen. Machen Sie das Gleiche für die **Kreditor**-Daten. Wenn die initiale Synchronisierung beendet ist, können Sie alle Zuordnungen ausführen, indem Sie die initiale Synchronisierung überspringen.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
