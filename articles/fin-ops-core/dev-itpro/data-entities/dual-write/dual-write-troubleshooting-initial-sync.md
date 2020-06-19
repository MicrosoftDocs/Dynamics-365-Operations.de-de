---
title: Probleme bei der anfänglichen Synchronisierung behandeln
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Synchronisierung zusammenhängen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410080"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Probleme bei der anfänglichen Synchronisierung behandeln

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Common Data Service. Dieses Thema enthält insbesondere Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Synchronisierung zusammenhängen.

> [!IMPORTANT]
> Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Überprüfen Sie eine Finance and Operations App auf anfängliche Synchronisationsfehler

Nachdem Sie die Zuordnungsvorlagen aktiviert haben, sollte der Status der Zuordnungen lauten **Laufen**. Wenn der Status ist **Nicht ausgeführt** angezeigt wird, sind bei der ersten Synchronisierung Fehler aufgetreten. Um die Fehler anzuzeigen, wählen Sie die **Anfängliche Synchronisierungsdetail** Registerkarte auf der **Duales Schreiben** Seite.

![Registerkarte Details zur Erstsynchronisierung](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Sie können die anfängliche Synchronisierung nicht abschließen: 400 Bad Request

**Erforderliche Rolle zum Beheben der Fehler:** System Administrator

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, das Mapping und die anfängliche Synchronisierung auszuführen:

*Der Remote-Server hat einen Fehler zurückgegeben: (400) Bad Request.), beim AX Export ist ein Fehler aufgetreten*

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

![Liste der Azure AD Bewerbungen](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Selbstreferenzfehler oder Zirkelreferenzfehler während der ersten Synchronisation

Möglicherweise wird eine Fehlernachricht angezeigt, die dem folgenden Beispiel ähnelt, wenn eine Ihrer Zuordnungen Selbstreferenzen oder Zirkelreferenzen enthält: Die Fehler fallen in folgende Kategorien:

- [Kreditoren V2 zu msdyn_vendors Entitätzuordnung](#error-vendor-map)
- [Zuordnung der Entitäten von Kunden V3 zu Konten](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Beheben Sie einen Fehler in der Entitätszuordnung von Vendors V2 zu msdyn_vendors

Möglicherweise treten auf dem Computer die folgenden anfänglichen Synchronisierungsfehler auf **Anbieter V2** zu **msdyn_vendors** Zuordnung, wenn die Entitäten vorhandene Datensätze mit Werten in der **PrimaryContactPersonId** und **InvoiceVendorAccountNumber** Felder haben. Das ist so, weil **InvoiceVendorAccountNumber** ein selbstreferenzierendes Feld ist und **PrimaryContactPersonId** eine Zirkelreferenz in der Lieferantenzuordnung ist.

*Die Anleitung für das Feld konnte nicht aufgelöst werden: <field>. Die Suche wurde nicht gefunden: <value>. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>? $ select =<field>& $ filter=<field> Gl <value>*

Hier einige Beispiele:

- *Die GUID für das Feld konnte nicht aufgelöst werden: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Die Suche wurde nicht gefunden: 000056. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$ select = msdyn_contactpersonid.contactid & $ filter = msdyn_contactpersonid eq '000056'*
- *Die GUID für das Feld konnte nicht aufgelöst werden: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Die Suche wurde nicht gefunden: 1. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*

Wenn Sie Datensätze mit Werten in diesen Feldern in der Lieferantenentität haben, führen Sie die Schritte im folgenden Abschnitt aus, um die erste Synchronisierung erfolgreich abzuschließen.

1. In dem Finance and Operations App löschen Sie die **PrimaryContactPersonId** und **InvoiceVendorAccountNumber** Felder aus der Zuordnung und speichern Sie die Änderungen.

    1. Navigieren Sie zur Zuordnungsseite duales Schreiben für **Anbieter V2 (msdyn_vendors)** und wählen Sie die Registerkarte **Entitätszuordnungen**. Wählen Sie im linken Filter **Finance and Operations Apps.Vendors V2**. Wählen Sie im rechten Filter **Sales.Vendor**.

    2. Suchen Sie nach **Hauptkontaktperson**, um das Quellfeld zu finden **PrimaryContactPersonId**.
    
    3. Klicken Sie auf die Schaltfläche **Aktionen** und wählen Sie **Löschen**.
    
        ![Selbst- oder Zirkelverweis 3](media/vend_selfref3.png)
    
    4. Wiederholen Sie diesen Vorgang, um das Feld **InvoiceVendorAccountNumber** zu löschen.
    
        ![Selbst- oder Zirkelverweis 4](media/vend-selfref4.png)
    
    5. Speichern Sie die Zuordnungsänderungen.

2. Deaktivieren Sie die Änderungsverfolgung für **Anbieter V2** Entität.

    1. Navigieren Sie zu **Datenmanagement \> Dateneinheiten**.
    
    2. Wählen Sie die Entität **Anbieter V2** aus.
    
    3. Klicken Sie auf **Optionen** in der Menüleiste und dann **Nachverfolgung ändern**.
    
        ![Selbst- oder Zirkelverweis 5](media/selfref_options.png)
    
    4. Klicken Sie auf **Änderungsverfolgung deaktivieren**.
    
        ![Selbst- oder Zirkelverweis 6](media/selfref_tracking.png)

3. Führen Sie die erste Synchronisierung von **Anbieter V2 (msdyn_vendors)** Zuordnung aus. Die anfängliche Synchronisierung sollte ohne Fehler erfolgreich ausgeführt werden.

4. Führen Sie die erste Synchronisierung für die **CDS-Kontakte V2 (Kontakte)** Zuordnung aus. Sie müssen diese Zuordnung synchronisieren, wenn Sie das primäre Kontaktfeld auf der Entität des Anbieters synchronisieren möchten, da die Kontaktdatensätze auch zunächst synchronisiert werden müssen.

5. Fügen Sie die Felder **PrimaryContactPersonId** und **InvoiceVendorAccountNumber** wieder der **Anbieter V2 (msdyn_vendors)** Zuordnung hinzu und speichern Sie die Zuordnung.

6. Führen Sie die erste Synchronisierung erneut für die **Anbieter V2 (msdyn_vendors)** Zuordnung aus. Alle Datensätze werden synchronisiert, da die Änderungsverfolgung deaktiviert ist.

7. Aktivieren Sie die Änderungsverfolgung für **Anbieter V2** Entität.

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>Beheben Sie einen Fehler in der Entitätszuordnung von Kunden V3 zu Konten

Möglicherweise treten auf dem Computer die folgenden anfänglichen Synchronisierungsfehler auf **Anbieter V3** zu **msdyn_vendors** Zuordnung, wenn die Entitäten vorhandene Datensätze mit Werten in den Feldern **ContactPersonId** und **InvoiceAccount** haben. Das ist so, weil **InvoiceAccount** ein selbstreferenzierendes Feld ist und **ContactPersonId** eine Zirkelreferenz in der Lieferantenzuordnung ist.

*Die Anleitung für das Feld konnte nicht aufgelöst werden: <field>. Die Suche wurde nicht gefunden: <value>. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>? $ select =<field>& $ filter=<field> Gl <value>*

- *Die GUID für das Feld konnte nicht aufgelöst werden: primarycontactperson.msdyn_contactpersonid. Die Suche wurde nicht gefunden: 000056. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$ select = msdyn_contactpersonid.contactid & $ filter = msdyn_contactpersonid eq '000056'*
- *Die GUID für das Feld konnte nicht aufgelöst werden: msdyn_billingacount.accountnumber. Die Suche wurde nicht gefunden: 1206-1. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq 1206-1*

Wenn Sie Datensätze mit Werten in diesen Feldern in der Kundenenentität haben, führen Sie die Schritte im folgenden Abschnitt aus, um die erste Synchronisierung erfolgreich abzuschließen. Sie können diesen Ansatz für alle sofort einsatzbereiten Entitäten wie Konten und Kontakte verwenden.

1. In der Finance and Operations App löschen Sie Felder **ContactPersonID** und **InvoiceAccount** aus der Zuordnung **Kunden V3 (Konten)** und speichern Sie die Zuordnung.

    1. Navigieren Sie zur Zuordnungsseite duales Schreiben für **Kunden V3 (msdyn_vendors)** und wählen Sie die Registerkarte **Entitätszuordnungen**. Wählen Sie im linken Filter **Finance and Operations Apps.Customers V3**. Wählen Sie im rechten Filter **Common Data Service Konto**.

    2. Suchen Sie nach **contactperson**, um das Quellfeld **ContactPersonID** zu finden.
    
    3. Klicken Sie auf die Schaltfläche **Aktionen** und wählen Sie **Löschen**.
    
        ![Selbst- oder Zirkelverweis 3](media/cust_selfref3.png)
    
    4. Wiederholen Sie diesen Vorgang, um das Feld **InvoiceAccount** zu löschen.
    
        ![Selbst- oder Zirkelverweis](media/cust_selfref4.png)
    
    5. Speichern Sie die Zuordnungsänderungen.

2. Deaktivieren Sie die Änderungsverfolgung für **Customers V3** Entität.

    1. Navigieren Sie zu **Datenmanagement \> Dateneinheiten**.
    
    2. Wählen Sie die Entität **Customers V3** aus.
    
    3. Klicken Sie auf **Optionen** in der Menüleiste und dann **Nachverfolgung ändern**.
    
        ![Selbst- oder Zirkelverweis 5](media/selfref_options.png)
    
    4. Klicken Sie auf **Änderungsverfolgung deaktivieren**.
    
        ![Selbst- oder Zirkelverweis 6](media/selfref_tracking.png)

3. Führen Sie die erste Synchronisierung für die **Customers V3 (Konten)** Zuordnung aus. Die anfängliche Synchronisierung sollte ohne Fehler erfolgreich ausgeführt werden.

4. Führen Sie die erste Synchronisierung für die **CDS-Kontakte V2 (Kontakte)** Zuordnung aus. Es gibt 2 Karten mit dem gleichen Namen. Wählen Sie jene mit der Beschreibung **Vorlage Duales Schreiben für die Synchronisierung zwischen FO.CDS-Kontakten V2 und CDS.Contacts. Benötigt neues Paket \[Dynamics365SupplyChainExtended\].** Auf der Registerkarte **Einzelheiten** auf der Karte.

5. In der  App fügen Sie die Felder **InvoiceAccount** und **ContactPersonID** wieder der **Kunden V3 (Konten)** Zuordnung hinzu und speichern Sie die Zuordnung. Nun sind das Feld **Rechnungskonto** und das Feld **ContactPersonID** wieder Teil des Live-Synchronisationsmodus. Im nächsten Schritt schließen Sie die anfängliche Synchronisierung für diese Felder ab.

6. Führen Sie die erste Synchronisierung nochmals für die **Customers V3 (Konten)** Zuordnung aus. Da die Änderungsverfolgung deaktiviert ist, werden beim Ausführen der Synchronisierung die Daten für **InvoiceAccount** und **ContactPersonId** von der Finance and Operations App zu Common Data Service synchronisiert.

7. Um die Daten für **Rechnungskonto** und **ContactPersonId** von Common Data Service zu Finance and Operations zu synchronisieren, verwenden Sie ein Datenintegrationsprojekt.

    1. Im Power Apps erstellen Sie ein Datenintegrationsprojekt zwischen dem **Verkaufskonto** und **Finance and Operations Apps.Customers V3** Entitäten. Die Datenrichtung muss von Common Data Service zu Finance and Operations App sein.  Weil **Rechnungskonto** ein neues Attribut in dualem Schreiben ist, wollen Sie möglicherweise die anfängliche Synchronisierung für dieses Attribut überspringen. Weitere Informationen finden Sie unter [Datenintegration in Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Das folgende Bild zeigt ein Projekt, das **Kundenkonto** und **ContactPersonId** aktualisiert.

        ![Selbst- oder Zirkelverweis](media/cust_selfref6.png)

    2. Fügen Sie die Firmenkriterien im Filter auf der Seite Common Data Service ein, da nur die Datensätze, die den Filterkriterien entsprechen, in der Finance and Operations App aktualisiert werden. Klicken Sie zum Hinzufügen eines Filters auf das Filtersymbol. In dem Dialog **Abfrage bearbeiten** können Sie eine Filterabfrage hinzufügen wie **_msdyn_company_value eq\<guid\>**. Wenn das Filtersymbol nicht vorhanden ist, erstellen Sie ein Support-Ticket, um das Datenintegrationsteam zu bitten, die Filterfunktion für Ihren Mandanten zu aktivieren. Wenn Sie keine Filterabfrage für eingeben **_msdyn_company_value**, dann werden alle Datensätze synchronisiert.

        ![Selbst- oder Zirkelverweis](media/cust_selfref7.png)

        Damit ist die anfängliche Synchronisierung der Datensätze abgeschlossen.

8. Aktivieren Sie die Änderungsverfolgung für **Customers V3** Entität in der Finance and Operations App.

