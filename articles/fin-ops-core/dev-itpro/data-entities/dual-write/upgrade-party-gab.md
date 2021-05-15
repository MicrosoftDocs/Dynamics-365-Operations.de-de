---
title: Auf das Partei- und globale Adressbuchmodell aktualisieren
description: In diesem Thema wird beschrieben, wie Sie Daten aus dualem Schreiben auf das Partei- und das globale Adressbuchmodell aktualisieren.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 32128d48bfac195530d70b60e67cfd4921fc001e
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941082"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Auf das Partei- und globale Adressbuchmodell aktualisieren

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Die [Azure Data Factory-Vorlage](https://aka.ms/dual-write-gab-adf) hilft Ihnen beim Aktualisieren vorhandener **Konto**-, **Kontakt**- und **Kreditor**-Tabellendaten in dualem Schreiben in das Partei- und das globale Adressbuchmodell. Die Vorlage stimmt die Daten sowohl von Finance and Operations-Apps als auch von Anwendungen zur Kundenbindung ab. Am Ende des Prozesses werden die Felder **Partei** und **Kontakt** für **Partei**-Datensätze erstellt und mit **Konto**-, **Kontakt**- und **Kreditor**-Datensätzen in Anwendungen zur Kundenbindung verknüpft. Eine .csv-Datei (`FONewParty.csv`) wird generiert, um einen neuen **Partei**-Datensatz in der Finance and Operations-App zu erstellen. Dieses Thema enthält Anweisungen zur Verwendung der Data Factory-Vorlage und zum Aktualisieren Ihrer Daten.

Wenn Sie keine Anpassungen vorgenommen haben, können Sie die Vorlage unverändert verwenden. Wenn Sie Anpassungen für **Konto**, **Kontakt** und **Kreditor** vorgenommen haben, müssen Sie die Vorlage anhand der folgenden Anweisungen ändern.

> [!Note]
> Die Vorlage hilft nur, die **Partei**-Daten zu aktualisieren. Ein zukünftiger Release wird postalische und elektronische Adressen enthalten.

## <a name="prerequisites"></a>Voraussetzungen

Es gelten die folgenden Voraussetzungen:

+ [Azure-Abonnement](https://portal.azure.com/)
+ [Zugriff auf die Vorlage](https://aka.ms/dual-write-gab-adf)
+ Sie sind ein bestehender Kunde für duales Schreiben.

## <a name="prepare-for-the-upgrade"></a>Vorbereitung auf die Aktualisierung

+ **Vollständig synchronisiert**: Beide Umgebungen sind vollständig im Hinblick auf **Konto (Kunde)**, **Kontakt** und **Kreditor** synchronisiert.
+ **Integrationsschlüssel**: Die Tabellen **Konto (Kunde)**, **Kontakt** und **Kreditor** in Apps zur Kundenbindung verwenden die sofort einsatzbereiten Integrationsschlüssel. Wenn Sie die Integrationsschlüssel angepasst haben, müssen Sie die Vorlage anpassen.
+ **Parteinummer**: Alle **Konto (Kunde)**-, **Kontakt**- und **Kreditor**-Datensätze, die aktualisiert werden, haben eine **Partei**-Nummer. Aufzeichnungen ohne **Partei**-Nummer werden ignoriert. Wenn Sie diese Datensätze aktualisieren möchten, fügen Sie eine **Partei**-Nummer hinzu, bevor Sie den Aktualisierungsprozess starten.
+ **Systemausfall**: Während des Aktualisierungsprozesses müssen Sie sowohl die Finance and Operations- als auch die Kundenbindungsumgebung offline nehmen.
+ **Momentaufnahme**: Machen Sie sowohl von der Finance and Operations als auch der App zur Kundenbindung eine Momentaufnahme. Verwenden Sie die Momentaufnahmen, um bei Bedarf den vorherigen Status wiederherzustellen.

## <a name="deployment"></a>Bereitstellung

1. Laden Sie die Vorlage von [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf) herunter.

2. Melden Sie sich auf [Microsoft Azure](https://portal.azure.com/) an.

3. Erstellen Sie eine [Ressourcengruppe](/azure/azure-resource-manager/management/manage-resource-groups-portal).

4. Erstellen Sie ein [Speicherkonto](/azure/storage/common/storage-account-create?tabs=azure-portal) in der von Ihnen erstellten Ressourcengruppe.

5. Erstellen Sie eine [Data Factory](/azure/data-factory/quickstart-create-data-factory-portal) über der von Ihnen erstellten Ressourcengruppe.

6. Öffnen Sie die Data Factory und wählen Sie die Kachel **Erstellen und überwachen** aus.

7. Wählen Sie in der Registerkarte **Verwalten** die **ARM-Vorlage** aus.

8. Wählen Sie **ARM-Vorlage importieren** aus, um die **Partei**-Vorlage zu importieren.

9. Importieren Sie die Vorlage in die Data Factory. Geben Sie die folgenden Werte für **Projektdetails** und **Instanzdetails** ein.

    Feld | Wert
    ---|---
    Abonnement | Azure-Abonnement
    Ressourcengruppe | Geben Sie dieselbe Ressource an, unter der das Speicherkonto erstellt wird.
    Region | Geben Sie die Region an.
    Name der Factory | Geben Sie den Namen der Factory an.
    FO Linked Service_service Principal Key | Geben Sie den Schlüssel der Anwendung an.
    Azure Blob Storage_connection String | Azure Blob Storage-Verbindungszeichenfolge.
    Dynamics Crm Linked Service_password | Das Kennwort für das Benutzerkonto, das Sie als Benutzernamen angegeben haben.
    FO Linked Service_properties_type Properties_url  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    FO Linked Service_properties_type Properties_tenant | Geben Sie die Mandanteninformationen (Domänenname oder Mandanten-ID) an, unter denen sich Ihre Anwendung befindet.
    FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com`
    FO Linked Service_properties_type Properties_service Principal Id | Geben Sie den Schlüssel der Client-ID an.
    Dynamics Crm Linked Service_properties_type Properties_username | Der Benutzername für die Verbindung zu Dynamics.

    Weitere Informationen finden Sie unter [Manuelles Höherstufen einer Resource Manager-Vorlage für jede Umgebung](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Eigenschaften des verknüpften Diensts](/azure/data-factory/connector-dynamics-ax#linked-service-properties) und [Daten mit Azure Data Factory kopieren](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Überprüfen Sie nach der Bereitstellung die Datensätze, den Datenfluss und den verknüpften Dienst der Data Factory.

   ![Datensätze, Datenfluss und verknüpfter Dienst](media/data-factory-validate.png)

11. Gehen Sie zu **Verwalten**. Wählen Sie unter **Verbindungen** **Verknüpfter Dienst** aus. Wählen Sie **DynamicsCrmLinkedService** aus. Geben Sie im Formular **Verknüpften Dienst bearbeiten (Dynamics CRM)** die folgenden Werte ein:

    Feld | Wert
    ---|---
    Name | DynamicsCrmLinkedService
    Beschreibung | Verknüpfte Dienste zur Verbindung mit der CRM-Instanz zum Abrufen von Entitätsdaten
    Verbindung über Integration Runtime herstellen | AutoResolvelntegrationRuntime
    Bereitstellungstyp | Online
    Dienst-URI | `https://<organization-name>.crm[x].dynamics.com`
    Authentifizierungstyp | Office365
    Benutzername |
    Kennwort oder Azure Key Vault | Kennwort
    Kennwort |

## <a name="run-the-template"></a>Die Vorlage ausführen

1. Halten Sie das folgende duale Schreiben für **Konto**, **Kontakt** und **Kreditor** mit der Finance and Operations-App an.

    + Debitoren V3 (Konten)
    + Debitoren V3 (Kontakte)
    + CDS-Kontakte V2 (Kontakte)
    + CDS-Kontakte V2 (Kontakte)
    + Kreditor V2 (msdyn_vendor)

2. Stellen Sie sicher, dass die Karten aus der Tabelle `msdy_dualwriteruntimeconfig` in Dataverse entfernt werden.

3. Installieren Sie [Partei- und globale Adressbuchlösungen mit dualem Schreiben](https://aka.ms/dual-write-gab) aus AppSource.

4. Führen Sie in der Finance and Operations-App **Erstsynchronisierung** für die folgenden Tabellen durch, die Daten enthalten.

    + Anreden
    + Arten von Persönlichkeitsmerkmalen
    + Schlussformel
    + Titel von Kontaktpersonen
    + Entscheidungsfunktionen
    + Treueebenen

5. Deaktivieren Sie in der App zur Kundenbindung die folgenden Plugin-Schritte.

    + Konto aktualisieren
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualisieren des Kontos
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualisieren des Kontos
    + Kontakt aktualisieren
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualisieren des Kontakts
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualisieren des Kontakts
    + msdyn_party-Aktualisierung
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualisieren von msdyn_party
    + msdyn_vendor-Aktualisierung
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualisieren von msdyn_vendor

6. Deaktivieren Sie in der App zur Kundenbindung die folgenden Workflows:

    + Lieferanten in der Kontotabelle erstellen
    + Lieferanten in der Kontotabelle erstellen
    + Kreditoren vom Typ „Person“ in der Kontakttabelle erstellen
    + Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen
    + Lieferanten in der Kontotabelle aktualisieren
    + Lieferanten in der Lieferantentabelle aktualisieren
    + Lieferanten vom Typ „Person“ in der Kontakttabelle aktualisieren
    + Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren

7. Führen Sie in der Data Factory die Vorlage aus, indem Sie **Jetzt auslösen** wie im folgenden Bild gezeigt auswählen. Dieser Prozess kann je nach Datenvolumen einige Stunden dauern.

    ![Ausführung auslösen](media/data-factory-trigger.png)

    > [!NOTE]
    > Wenn Sie Anpassungen für **Konto**, **Kontakt** und **Kreditor** vorgenommen haben, müssen Sie die Vorlage ändern.

8. Importieren Sie den neuen **Partei**-Datensatz in der Finance and Operations-App.

    + Laden Sie die Datei `FONewParty.csv` aus dem Azure Blob Storage herunter. Der Pfad lautet `partybootstrapping/output/FONewParty.csv`.
    + Konvertieren Sie die Datei `FONewParty.csv` in eine Excel-Datei und importieren Sie die Excel-Datei in die Finance and Operations-App.  Wenn der CSV-Import bei Ihnen funktioniert, können Sie die CSV-Datei direkt importieren. Das Importieren kann je nach Datenvolumen einige Stunden dauern. Weitere Informationen finden Sie unter [Übersicht über Datenimport- und -exportaufträge](../data-import-export-job.md).

    ![Die Datavers-Partei-Datensätze importieren](media/data-factory-import-party.png)

9. Aktivieren Sie in den Apps zur Kundenbindung die folgenden Plugin-Schritte:

    + Konto aktualisieren
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualisieren des Kontos
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualisieren des Kontos
    + Kontakt aktualisieren
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualisieren des Kontakts
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualisieren des Kontakts
    + msdyn_party-Aktualisierung
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualisieren von msdyn_party
    + msdyn_vendor-Aktualisierung
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualisieren von msdyn_vendor

10. Aktivieren Sie in den Kundenbindungs-Apps die folgenden Workflows, wenn Sie sie in den vorherigen Schritten deaktiviert haben:

    + Lieferanten in der Kontotabelle erstellen
    + Lieferanten in der Kontotabelle erstellen
    + Kreditoren vom Typ „Person“ in der Kontakttabelle erstellen
    + Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen
    + Lieferanten in der Kontotabelle aktualisieren
    + Lieferanten in der Lieferantentabelle aktualisieren
    + Lieferanten vom Typ „Person“ in der Kontakttabelle aktualisieren
    + Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren

11. Führen Sie die mit der **Partei** zusammenhängenden Karten wie in [Partei- und globales Adressbuch](party-gab.md) angewiesen aus.

## <a name="troubleshooting"></a>Problembehandlung

1. Wenn der Prozess fehlschlägt, führen Sie die Data Factory beginnend mit der fehlgeschlagenen Aktivität erneut aus.
2. Einige Dateien werden von der Data Factory generiert, die Sie zur Datenüberprüfung verwenden können.
3. Die Data Factory wird basierend auf durch Kommas getrennten CSV-Dateien ausgeführt. Wenn ein Feldwert ein Komma hat, kann dies die Ergebnisse beeinträchtigen. Sie müssen die Kommas entfernen.
4. Die Registerkate **Überwachung** enthält Informationen zu allen Schritten und verarbeiteten Daten. Wählen Sie einen bestimmten Schritt zum Debuggen aus.

    ![Registerkarte „Überwachung“](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Mehr über die Vorlage

In der [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)-Datei finden Sie Anmerkungen zur Vorlage.