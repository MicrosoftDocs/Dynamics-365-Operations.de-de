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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a2f0e0cbf0f8710dc020a48506775fa28df9c2d2
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744636"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Probleme bei der anfänglichen Synchronisierung behandeln

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse. Dieses Thema enthält insbesondere Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Synchronisierung zusammenhängen.

> [!IMPORTANT]
> Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Überprüfen Sie eine Finance and Operations App auf anfängliche Synchronisationsfehler

Nachdem Sie die Zuordnungsvorlagen aktiviert haben, sollte der Status der Zuordnungen lauten **Laufen**. Wenn der Status ist **Nicht ausgeführt** angezeigt wird, sind bei der ersten Synchronisierung Fehler aufgetreten. Um die Fehler anzuzeigen, wählen Sie die **Anfängliche Synchronisierungsdetail** Registerkarte auf der **Duales Schreiben** Seite.

![Fehler auf der Registerkarte Details zur Erstsynchronisierung](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Sie können die anfängliche Synchronisierung nicht abschließen: 400 Bad Request

**Erforderliche Rolle zum Beheben der Fehler:** System Administrator

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, das Mapping und die anfängliche Synchronisierung auszuführen:

*(\[Unzulässige Anforderung\], der Remote-Server hat einen Fehler zurückgegeben: (400) Unzulässige Anforderung), AX beim Export ist ein Fehler aufgetreten*

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

![DtAppID-Client in der Liste von Azure AD Anwendungen](media/aad_applications.png)

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

        ![Löschen der Spalte „PrimaryContactPersonId“](media/vend_selfref3.png)

    4. Wiederholen Sie diese Schritte, um die Spalte **InvoiceVendorAccountNumber** zu löschen.

        ![Löschen des Feldes „InvoiceVendorAccountNumber“](media/vend-selfref4.png)

    5. Speichern Sie Ihre Änderungen am Mapping.

2. Deaktivieren Sie die Änderungsverfolgung für die Tabelle **Kreditoren V2**.

    1. Im Arbeitsbereich **Datenmanagement** wählen Sie die Kachel **Datentabellen** aus.
    2. Wählen Sie die Tabelle **Kreditoren V2** aus.
    3. Wählen Sie im Aktionsbereich **Optionen** und wählen Sie dann **Änderungsnachverfolgung**.

        ![Auswahl der Option Änderungsnachverfolgung ändern](media/selfref_options.png)

    4. Wählen Sie **Änderungsverfolgung deaktivieren**.

        ![Wählen Sie Änderungsverfolgung deaktivieren](media/selfref_tracking.png)

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

        ![Löschen der Spalte „ContactPersonID“](media/cust_selfref3.png)

    4. Wiederholen Sie diese Schritte, um die Spalte **InvoiceAccount** zu löschen.

        ![Löschen der Spalte „InvoiceAccount“](media/cust_selfref4.png)

    5. Speichern Sie Ihre Änderungen am Mapping.

2. Deaktivieren Sie die Änderungsverfolgung für die Tabelle **Debitoren V3**.

    1. Im Arbeitsbereich **Datenmanagement** wählen Sie die Kachel **Datentabellen** aus.
    2. Wählen Sie die Tabelle **Debitoren V3** aus.
    3. Wählen Sie im Aktionsbereich **Optionen** und wählen Sie dann **Änderungsnachverfolgung**.

        ![Auswahl der Option Änderungsnachverfolgung ändern](media/selfref_options.png)

    4. Wählen Sie **Änderungsverfolgung deaktivieren**.

        ![Wählen Sie Änderungsverfolgung deaktivieren](media/selfref_tracking.png)

3. Führen Sie die erste Synchronisierung nochmals für die **Debitoren V3 (Konten)** Zuordnung aus. Die erstmalige Synchronisierung sollte ohne Fehler erfolgreich ausgeführt werden.
4. Führen Sie die erste Synchronisierung für **CDS-Kontakte V2 (Kontakte)** Zuordnung aus.

    > [!NOTE]
    > Es gibt zwei Karten mit demselben Namen. Stellen Sie sicher, dass Sie jene Zuordnung mit der folgenden Beschreibung auf der Registerkarte **Details** auswählen: Duales Schreiben für die Synchronisierung zwischen FO.CDS-Kontakten V2 und CDS.Contacts.  Benötigt neues Paket \[**Dynamics365SupplyChainExtended\].**

5. Fügen Sie die Spalten **InvoiceAccount** und **ContactPersonID** wieder der Zuordnung **Debitoren V3 (Konten)** hinzu, und speichern Sie dann die Zuordnung. Jetzt sind die Spalte **InvoiceAccount** und die Spalte **ContactPersonID** wieder Teil des Live-Synchronisationsmodus. Im nächsten Schritt machen Sie die anfängliche Synchronisierung für diese Spalten.
6. Führen Sie die erste Synchronisierung noch einmal für die **Debitoren V3 (Konten)** Zuordnung aus. Da die Änderungsverfolgung deaktiviert ist, werden die Daten für **InvoiceAccount** und **ContactPersonId** von der Finance and Operations App zu Dataverse synchronisiert.
7. Um die Daten für **Rechnungskonto** und **ContactPersonId** von Dataverse zu Finance and Operations zu synchronisieren, müssen Sie ein Datenintegrationsprojekt verwenden.

    1. Erstellen Sie in Power Apps ein Datenintegrationsprojekt zwischen den Tabellen **Sales.Account** und **Finance and Operations apps.Customers V3**. Die Datenrichtung muss von Dataverse zu Finance and Operations App sein. Weil **Rechnungskonto** ein neues Attribut in dualem Schreiben ist, wollen Sie möglicherweise die anfängliche Synchronisierung dazu überspringen. Weitere Informationen finden Sie unter [Datenintegration in Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Das folgende Illustration zeigt ein Projekt, das **Kundenkonto** und **ContactPersonId** aktualisiert.

        ![Datenintegrationsprojekt zum Aktualisieren von CustomerAccount und ContactPersonId](media/cust_selfref6.png)

    2. Fügen Sie die Firmenkriterien im Filter auf der Seite von Dataverse ein, da nur die Zeilen, die den Filterkriterien entsprechen, in der Finance and Operations-App aktualisiert werden. Wählen Sie zum Hinzufügen die Schaltfläche Filter. In dem Dialog **Abfrage bearbeiten** können Sie eine Filterabfrage hinzufügen wie **\_msdyn\__company\_value eq\<guid\>**. 

        > [HINWEIS] Wenn die Schaltfläche Filter nicht vorhanden ist, erstellen Sie ein Support-Ticket, um das Datenintegrationsteam zu bitten, die Filterfunktion für Ihren Mandanten zu aktivieren.

        Wenn Sie keine Filterabfrage für **\_msdyn\_company\_value** eingeben, werden alle Zeilen synchronisiert.

        ![Hinzufügen einer Filterabfrage](media/cust_selfref7.png)

    Die anfängliche Synchronisierung der Zeilen ist nun abgeschlossen.

8. Aktivieren Sie die Änderungsnachverfolgung in Finance and Operations für die Tabelle **Debitoren V3**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]