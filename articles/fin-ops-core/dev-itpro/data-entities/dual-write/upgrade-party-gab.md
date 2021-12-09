---
title: Auf das Partei- und globale Adressbuchmodell aktualisieren
description: In diesem Thema wird beschrieben, wie Sie Daten aus dualem Schreiben auf das Partei- und das globale Adressbuchmodell aktualisieren.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 7434c2ed486fe0546a746afdd2c4c4aacdcc3d5c
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817287"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Auf das Partei- und globale Adressbuchmodell aktualisieren

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Die [Microsoft Azure Data Factory-Vorlagen](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) helfen Ihnen beim Aktualisieren folgender vorhandener Daten in dualem Schreiben in das Partei- und das globale Adressbuchmodell: Daten in **Konto-**, **Kontakt**- und **Kreditor**-Tabellen sowie postalische und elektronische Adressen.

Die folgenden drei Data Factory-Vorlagen werden bereitgestellt. Die Vorlage stimmt die Daten sowohl von Finance and Operations-Apps als auch von Anwendungen zur Kundenbindung ab.

- **[Partei-Vorlage](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (Aktualisieren Sie die Daten auf das Party-GAB schema/arm_template.json mit dualem Schreiben)** – Diese Vorlage hilft beim Upgrade von **Partei**- und **Kontakt**-Daten, die mit **Konto**, **Kontakt** und **Kreditoren**-Daten verbunden sind.
- **[Vorlage für die Postadresse der Partei](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (Upgrade von Daten auf Party-GAB-Schema/Upgrade auf Partei-Postadresse - GAB/arm_template.json mit dualem Schreiben)** – Diese Vorlage hilft bei der Aktualisierung der Postadressen, die mit **Konto**, **Kontakt** und **Kreditoren**-Daten verknüpft sind.
- **[Vorlage für die elektronische Adresse der Partei](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (Upgrade von Daten auf Party-GAB-Schema/Upgrade auf elektronische Partei-Adresse - GAB/arm_template.json mit dualem Schreiben)** – Diese Vorlage hilft bei der Aktualisierung der elektronsichen Adressen, die mit **Konto**, **Kontakt** und **Kreditoren**-Daten verknüpft sind.

Am Ende des Prozesses werden die folgenden Dateien mit durch Kommas getrennten Werten (.csv) generiert.

| Dateiname | Kostenträger |
|---|---|
| FONewParty.csv | Durch diese Datei werden neue **Partei**-Datensatz in der Finance and Operations-App erstellt. |
| ImportFONewPostalAddressLocation.csv | Diese Datei hilft beim Erstellen neuer **Postadressorte**-Datensätze in der Finance and Operations-App. |
| ImportFONewPartyPostalAddress.csv | Diese Datei hilft beim Erstellen neuer **Postadressorte der Partei**-Datensätze in der Finance and Operations-App. |
| ImportFONewPostalAddress.csv | Diese Datei hilft beim Erstellen neuer **Postadress**-Datensätze in der Finance and Operations-App. |
| ImportFONewElectronicAddress.csv | Diese Datei hilft beim Erstellen neuer **Elektronische Adresse**-Datensätze in der Finance and Operations-App. |

Dieses Thema erläutert die Verwendung der Data Factory-Vorlagen und Upgrades Ihrer Daten. Wenn Sie keine Anpassungen vorgenommen haben, können Sie die Vorlagen unverändert verwenden. Wenn Sie jedoch Anpassungen für Daten von **Konto**, **Kontakt** und **Kreditor** vorgenommen haben, müssen Sie die Vorlagen anhand der Anweisungen in diesem Thema ändern.

> [!IMPORTANT]
> Es gibt spezielle Anweisungen, wenn Sie die Vorlagen für die Postanschrift der Partei und die elektronische Adresse der Partei verwenden. Sie müssen zuerst die Partei-Vorlage ausführen, dann die Partei-Postadressenvorlage und dann die elektronische Partei-Adressvorlage.

## <a name="prerequisites"></a>Voraussetzungen

Die folgenden Voraussetzungen gegeben sein, um ein Upgrade auf das Partei- und das globale Adressbuchmodell durchzuführen:

+ Sie benötigen ein [Azure-Abonnement](https://portal.azure.com/).
+ Sie müssen Zugriff [auf die Vorlagen](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) haben.
+ Sie müssen ein bestehender Kunde für duales Schreiben sein.

## <a name="prepare-for-the-upgrade"></a>Vorbereitung auf die Aktualisierung

Ein Upgrade erfordert folgende Vorbereitungen:

+ **Vollständige Synchronisierung:** Sowohl die Finanz- und Betriebsumgebung als auch die Kundenbindungsumgebung befinden sich in einem vollständig synchronisierten Zustand für die Tabellen **Konto (Kunde)**, **Kontakt** und **Kreditoren**.
+ **Integrationsschlüssel**: Die Tabellen **Konto (Kunde)**, **Kontakt** und **Kreditor** in Apps zur Kundenbindung verwenden die sofort einsatzbereiten Integrationsschlüssel. Wenn Sie die Integrationsschlüssel angepasst haben, müssen Sie die Vorlage anpassen.
+ **Parteinummer**: **Alle Konto (Kunde)**-, **Kontakt**- und **Kreditor**-Datensätze, die aktualisiert werden, haben eine Partei-Nummer. Datensätze ohne Parteinummer werden ignoriert. Wenn Sie diese Datensätze aktualisieren möchten, fügen Sie eine Partei-Nummer hinzu, bevor Sie den Aktualisierungsprozess starten.
+ **Systemausfall**: Während des Aktualisierungsprozesses müssen Sie sowohl die Finance and Operations- als auch die Kundenbindungsumgebung offline nehmen.
+ **Momentaufnahme**: Machen Sie sowohl von der Finance and Operations-App als auch der App zur Kundenbindung eine Momentaufnahme. Sie können die Momentaufnahmen verwenden, um bei Bedarf den vorherigen Status wiederherzustellen.

## <a name="deployment"></a>Bereitstellung

1. Laden Sie die Vorlagen von [Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) herunter.
2. Melden Sie sich beim [Azure-Portal](https://portal.azure.com/) an.
3. Erstellen Sie eine [Ressourcengruppe](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. Erstellen Sie ein [Speicherkonto](/azure/storage/common/storage-account-create?tabs=azure-portal) in der von Ihnen erstellten Ressourcengruppe.
5. Erstellen Sie eine [Data Factory](/azure/data-factory/quickstart-create-data-factory-portal) über der von Ihnen erstellten Ressourcengruppe.
6. Öffnen Sie die Data Factory und wählen Sie die Kachel **Erstellen und überwachen** aus.
7. Wählen Sie in der Registerkarte **Verwalten** die **ARM-Vorlage** aus.
8. Wählen Sie **ARM-Vorlage importieren** aus, um die **Partei**-Vorlage zu importieren.
9. Importieren Sie die Vorlage in die Data Factory. Geben Sie die folgenden Werte für **Projektdetails** und **Instanzdetails** ein.

    | Feld | Wert |
    |---|---|
    | Abonnement | Das Azure-Abonnement |
    | Ressourcengruppe | Geben Sie dieselbe Ressource an, unter der das Speicherkonto erstellt wird. |
    | Region | Die Region |
    | Name der Factory | Name der Factory |
    | FO Linked Service_service Principal Key | Der Schlüssel der Anwendung |
    | Azure Blob Storage_connection String | Azure Blob Storage-Verbindungszeichenfolge |
    | Dynamics Crm Linked Service_password | Das Kennwort für das Benutzerkonto, das Sie als Benutzernamen angegeben haben. |
    | FO Linked Service_properties_type Properties_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO Linked Service_properties_type Properties_tenant | Informationen (Domänenname oder Mandanten-ID) über den Mandanten, unter denen sich Ihre Anwendung befindet |
    | FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO Linked Service_properties_type Properties_service Principal Id | Die Client-ID der Anwendung |
    | Dynamics Crm Linked Service_properties_type Properties_username | Der Benutzername für die Verbindung zu Dynamics 365 |

    Weitere Informationen finden Sie in folgenden Themen:

    - [Manuelles Heraufstufen einer Resource Manager-Vorlage für jede Umgebung](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Verknüpfte Serviceeigenschaften](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Kopieren Sie Daten mit Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Überprüfen Sie nach der Bereitstellung die Datensätze, den Datenfluss und den verknüpften Dienst der Data Factory.

    ![Datensätze, Datenfluss und verknüpfter Dienst.](media/data-factory-validate.png)

11. Gehen Sie zu **Verwalten**. Wählen Sie unter **Verbindungen** **Verknüpfter Dienst** aus. Wählen Sie **DynamicsCrmLinkedService** aus. Geben Sie im Dialofgfeld **Verknüpften Dienst bearbeiten (Dynamics CRM)** die folgenden Werte ein.

    | Feld | Wert |
    |---|---|
    | Name | DynamicsCrmLinkedService |
    | Beschreibung | Verknüpfte Dienste zur Verbindung mit der CRM-Instanz zum Abrufen von Entitätsdaten |
    | Verbindung über Integration Runtime herstellen | AutoResolvelntegrationRuntime |
    | Bereitstellungstyp | Online |
    | Dienst-URI | `https://<organization-name>.crm[x].dynamics.com` |
    | Authentifizierungstyp | Office365 |
    | Benutzername | |
    | Kennwort oder Azure Key Vault | Kennwort |
    | Kennwort | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Bereiten Sie die Ausführung der Data Factory-Vorlagen vor

In diesem Abschnitt wird die Einrichtung beschrieben, die erforderlich ist, bevor Sie die Data Factory-Vorlagen für die Postadresse der Partei und die elektronische Adresse der Partei ausführen.

### <a name="setup-to-run-the-party-postal-address-template"></a>Einrichtung zum Ausführen der Partei-Postadressenvorlage

1. Melden Sie sich bei den Apps zur Kundenbindung an und gehen Sie zu **Einstellungen** \> **Personalisierungseinstellungen**. Dann auf der **Allgemein**-Registerkarte konfigurieren Sie die Zeitzoneneinstellung für das Systemadministratorkonto. Die Zeitzone muss in koordinierter Weltzeit (UTC) angegeben sein, um die Datumsangaben „Gültig ab“ und „Gültig bis“ der Postadressen von Finance and Operations-Apps zu aktualisieren.

    ![Zeitzoneneinstellung für das Systemadministratorkonto.](media/ADF-1.png)

2. Erstellen Sie in Data Factory auf der **Verwalten**-Registerkarte unter **Globale Parameter** den folgenden globalen Parameter.

    | Anzahl | Name | Typ | Wert |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | Zeichenfolge | Dieser Parameter hängt eine Seriennummer als Präfix an neu erstellte Postadressen an. Stellen Sie sicher, dass Sie eine Zeichenfolge angeben, die nicht mit Postadressen in Finance and Operations-Apps und Kundenbindungs-Apps kollidiert. Verwenden Sie für dieses Beispiel **ADF-PAD-**. |

    ![PostalAddressIdPrefix (Globaler Parameter), der auf der Registerkarte „Verwalten“ erstellt wurde.](media/ADF-2.png)

3. Wählen Sie abschließend **Alle veröffentlichen** aus.

    ![Schaltfläche „Alle veröffentlichen“.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Einrichtung zum Ausführen der elektronischen Partei-Adressenvorlage

1. Erstellen Sie in Data Factory auf der **Verwalten**-Registerkarte unter **Globale Parameter** die folgenden globalen Parameter.

    | Anzahl | Name | Typ | Wert |
    |---|---|---|---|
    | 1 | IsFOSource | bool | Dieser Parameter legt fest, welche primären Systemadressen bei Konflikten ersetzt werden. Wenn der Wert **wahr** ist, ersetzen die primären Adressen in Finance and Operations-Apps die primären Adressen in Apps zur Kundenbindung. Wenn der Wert **false** ist, ersetzen die primären Adressen in Apps zur Kundenbindung die primären Adressen in Finance and Operations-Apps. |
    | 2 | ElectronicAddressIdPrefix | Zeichenfolge | Dieser Parameter hängt eine Seriennummer als Präfix an neu erstellte elektronische Adressen an. Stellen Sie sicher, dass Sie eine Zeichenfolge angeben, die nicht mit elektronischen Adressen in Finance and Operations-Apps und Kundenbindungs-Apps kollidiert. Verwenden Sie für dieses Beispiel **ADF-EAD-**. |

    ![IsFOSource und ElectronicAddressIdPrefix (Globale Parameter), die auf der Registerkarte „Verwalten“ erstellt wurden.](media/ADF-4.png)

2. Wählen Sie abschließend **Alle veröffentlichen** aus.

## <a name="run-the-templates"></a>Die Vorlagen ausführen

1. Halten Sie das folgende duale Schreiben für **Konto**, **Kontakt** und **Kreditor** mit der Finance and Operations-App an:

    + Debitoren V3 (Konten)
    + Debitoren V3 (Kontakte)
    + CDS-Kontakte V2 (Kontakte)
    + CDS-Kontakte V2 (Kontakte)
    + Kreditor V2 (msdyn_vendor)

2. Stellen Sie sicher, dass die Karten aus der Tabelle **msdy_dualwriteruntimeconfig** in Dataverse entfernt werden.
3. Installieren Sie [Partei- und globale Adressbuchlösungen mit dualem Schreiben](https://aka.ms/dual-write-gab) aus AppSource.
4. Führen Sie in der Finance and Operations-App **Erstsynchronisierung** für die folgenden Tabellen durch, wenn sie Daten enthalten:

    + Anreden
    + Arten von Persönlichkeitsmerkmalen
    + Schlussformel
    + Titel von Kontaktpersonen
    + Entscheidungsfunktionen
    + Treueebenen

5. Deaktivieren Sie in der App zur Kundenbindung die folgenden Plugin-Schritte:

    + Kontoupdate

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualisieren des Kontos
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualisieren des Kontos

    + Kontakt aktualisieren

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualisieren des Kontakts
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualisieren des Kontakts

    + msdyn_party-Aktualisierung

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualisieren von msdyn_party

    + msdyn_vendor-Aktualisierung

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualisieren von msdyn_vendor

    + Customeraddress

        + Erstellen

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: Erstellen der Kundenadresse

        + Aktualisieren

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: Aktualisieren der Kundenadresse

        + Löschen

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress: Löschen der Kundenadresse

    + msdyn_partypostaladdress

        + Erstellen

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Erstellen von msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Erstellen von msdyn_partypostaladdress

        + Aktualisieren

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Aktualisieren von msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Aktualisieren von msdyn_partypostaladdress

    + msdyn_postaladdress

        + Erstellen

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: Erstellen von msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: Erstellen von msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Erstellen von msdyn_postaladdress

        + Aktualisieren

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: Aktualisieren von msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Aktualisieren von msdyn_postaladdress

    + msdyn_partyelectronicaddress

        + Erstellen

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Erstellen von msdyn_partyelectronicaddress

        + Aktualisieren

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Aktualisieren von msdyn_partyelectronicaddress

        + Löschen

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: Löschen von msdyn_partyelectronicaddress

6. Deaktivieren Sie in der App zur Kundenbindung die folgenden Workflows:

    + Lieferanten in der Kontotabelle erstellen
    + Lieferanten in der Kontotabelle erstellen
    + Kreditoren vom Typ „Person“ in der Kontakttabelle erstellen
    + Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen
    + Lieferanten in der Kontotabelle aktualisieren
    + Lieferanten in der Lieferantentabelle aktualisieren
    + Lieferanten vom Typ „Person“ in der Kontakttabelle aktualisieren
    + Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren

7. Führen Sie in der Data Factory die Vorlage aus, indem Sie **Jetzt auslösen** wie in der folgenden Abbildung gezeigt auswählen. Dieser Prozess kann je nach Datenvolumen einige Stunden dauern.

    ![Ausführen der Vorlage.](media/data-factory-trigger.png)

    > [!NOTE]
    > Wenn Sie Anpassungen für **Konto**, **Kontakt** und **Kreditor** vorgenommen haben, müssen Sie die Vorlage ändern.

8. Importieren Sie den neuen **Partei**-Datensatz in der Finance and Operations-App.

    1. Laden Sie die Datei **FONewParty.csv** aus dem Azure Blob Storage herunter. Der Pfad lautet **partybootstrapping/output/FONewParty.csv**.
    2. Konvertieren Sie die Datei **FONewParty.csv** in eine Excel-Datei und importieren Sie die Excel-Datei in die Finance and Operations-App. Wenn der CSV-Import bei Ihnen funktioniert, können Sie alternativ die CSV-Datei direkt importieren. Dieser Schritt kann je nach Datenvolumen einige Stunden dauern. Weitere Informationen finden Sie unter [Übersicht über Datenimport- und -exportaufträge](../data-import-export-job.md).

    ![Importieren der Dataverse-Parteidatensätze.](media/data-factory-import-party.png)

9. Führen Sie in der Data Factory nacheinander die Vorlagen für die Postadresse der Partei und die elektronische Adresse der Partei aus.

    + Die Partei-Postadressenvorlage fügt alle Postadressendatensätze in der Kundenbindungs-App ein und verknüpft sie mit entsprechenden **Konto**, **Kontakt** und **Kreditoren**-Datensätzen. Außerdem werden drei CSV-Dateien generiert: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv und ImportFONewPostalAddress.csv.
    + Die elektronische Partei-Adressenvorlage fügt alle elektronischen Adressendatensätze in der Kundenbindungs-App ein und verknüpft sie mit entsprechenden **Konto**, **Kontakt** und **Kreditoren**-Datensätzen. Außerdem wird eine CSV-Datei generiert: ImportFONewElectronicAddress.csv.

    ![Ausführen der Vorlagen für die Postanschrift der Partei und die elektronischen Adressvorlagen der Partei.](media/ADF-7.png)

10. Um die Finance and Operations-App mit diesen Daten zu aktualisieren, müssen Sie die CSV-Dateien in eine Excel-Arbeitsmappe konvertieren und [in die Finance and Operations-App importieren](/data-entities/data-import-export-job). Wenn der CSV-Import bei Ihnen funktioniert, können Sie alternativ die CSV-Dateien direkt importieren. Dieser Schritt kann je nach Volumen einige Stunden dauern.

    ![Erfolgreicher Import.](media/ADF-8.png)

11. Aktivieren Sie in der App zur Kundenbindung die folgenden Plugin-Schritte:

    + Kontoupdate

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualisieren des Kontos
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualisieren des Kontos

    + Kontakt aktualisieren

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualisieren des Kontakts
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualisieren des Kontakts

    + msdyn_party-Aktualisierung

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualisieren von msdyn_party

    + msdyn_vendor-Aktualisierung

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualisieren von msdyn_vendor

    + msdyn_partypostaladdress

        + Erstellen

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Erstellen von msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Erstellen von msdyn_partypostaladdress

        + Aktualisieren

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Aktualisieren von msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Aktualisieren von msdyn_partypostaladdress

    + msdyn_postaladdress

        + Erstellen

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: Erstellen von msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: Erstellen von msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Erstellen von msdyn_postaladdress

        + Aktualisieren

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: Aktualisieren von msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Aktualisieren von msdyn_postaladdress
 
    + msdyn_partyelectronicaddress

        + Erstellen

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Erstellen von msdyn_partyelectronicaddress

        + Aktualisieren

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Aktualisieren von msdyn_partyelectronicaddress

        + Löschen

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: Löschen von msdyn_partyelectronicaddress

12. Aktivieren Sie in der Kundenbindungs-App die folgenden Workflows, wenn Sie sie in den vorherigen Schritten deaktiviert haben:

    + Lieferanten in der Kontotabelle erstellen
    + Lieferanten in der Kontotabelle erstellen
    + Kreditoren vom Typ „Person“ in der Kontakttabelle erstellen
    + Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen
    + Lieferanten in der Kontotabelle aktualisieren
    + Lieferanten in der Lieferantentabelle aktualisieren
    + Lieferanten vom Typ „Person“ in der Kontakttabelle aktualisieren
    + Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren

13. Führen Sie die mit den **Partei**-Datensätzen zusammenhängenden Karten wie in [Partei- und globales Adressbuch](party-gab.md) beschrieben aus.

## <a name="explanation-of-the-data-factory-templates"></a>Erläuterung der Data Factory-Vorlagen

Dieser Abschnitt führt Sie durch die Schritte in jeder Data Factory-Vorlage.

### <a name="steps-in-the-party-template"></a>Schritte in der Partei-Vorlage

1. In den Schritten 1 bis 6 werden die Unternehmen identifiziert, die für duales Schreiben aktiviert sind, und eine Filterklausel für sie erstellt.
2. Schritte 7-1 bis 7-9 rufen Daten von der Finance and Operations-App und der Kundenbindungs-App ab und stellen diese Daten für ein Upgrade bereit.
3. Schritte 8 bis 9 vergleichen die Parteinummer für die Datensätze **Konto**, **Kontakt** und **Kreditor** zwischen der Finance and Operations-App und die Kundenbindungs-App. Alle Datensätze ohne Parteinummer werden übergangen.
4. Schritt 10 generiert zwei CSV-Dateien für die Parteiendatensätze, die in der Kundenbindungs-App und der Finance and Operations-App erstellt werden müssen.

    - **FOCDSParty.csv** – Diese Datei enthält alle Teilnehmerdatensätze beider Systeme, unabhängig davon, ob das Unternehmen für duales Schreiben aktiviert ist.
    - **FONewParty.csv** – Diese Datei enthält eine Teilmenge der Parteiaufzeichnungen, die Dataverse bekannt sind (zum Beispiel Konten vom **Interessent**-Typ).

5. Schritt 11 erstellt die Parteien in der Kundenbindungs-App.
6. Schritt 12 ruft die Global Unique Identifiers (GUIDs) der Parteien aus der Kundenbindungs-App ab und stellt sie so bereit, dass sie **Konto**, **Kontakt** und **Kreditoren**-Datensätzen in den nachfolgenden Schritten zugeordnet werden können.
7. Schritt 13 verknüpft die **Konto**, **Kontakt** und **Kreditoren**-Datensätze mit Partei-GUIDs.
8. Schritte 14-1 bis 14-3 aktualisieren die **Konto**, **Kontakt** und **Kreditoren**-Datensätze in der Kundenbindungs-App mit Partei-GUIDs.
9. Schritte 15-1 bis 15-3 bereiten die **Kontakt für Partei**-Datensätze für **Konto**, **Kontakt** und **Kreditoren**-Datensätze vor.
10. Schritte 16-1 bis 16-7 rufen Referenzdaten wie Anreden und persönliche Zeichentypen ab und verknüpfen sie mit **Kontakt für Partei**-Datensätzen.
11. Schritte 17 verbindet die **Kontakt für Partei**-Datensätze für **Konto**, **Kontakt** und **Kreditoren**-Datensätze.
12. Schritt 18 importiert die **Kontakt für Partei**-Datensätze in die Kundenbindungs-App.

### <a name="steps-in-the-party-postal-address-template"></a>Schritte in der Partei-Postadressenvorlage

1. Schritte 1-1 bis 1-10 rufen Daten von der Finance and Operations-App und der Kundenbindungs-App ab und stellen diese Daten für ein Upgrade bereit.
2. Schritt 2 denormalisiert die Postadressdaten in der Finance and Operations-App, indem die Postadresse und die Postadresse der Partei zusammengefügt wird.
3. Schritt 3 dedupliziert und führt Konto-, Kontakt- und Kreditorenadressdaten aus der Kundenbindungs-App zusammen.
4. Schritt 4 erstellt CSV-Dateien für die Finance and Operations-App, um neue Adressdaten zu erstellen, die auf Konto-, Kontakt- und Kreditorenadressen basieren.
5. Schritt 5-1 erstellt CSV-Dateien für die Kundenbindungs-App, um alle Adressdaten basierend auf der Finance and Operations-App und der Kundenbindungs-App zu erstellen.
6. Schritt 5-2 konvertiert die CSV-Dateien ins Finance and Operations-Importformat für den manuellen Import.

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. Schritt 6 importiert die Daten zur Erfassung der Postanschrift in die Kundenbindungs-App.
8. Schritt 7 ruft die Daten zur Erfassung der Postanschrift aus der Kundenbindungs-App ab.
9. Schritt 8 erstellt Kundenadressdaten und ordnet eine Postadresssammlungs-ID zu.
10. Die Schritte 9-1 bis 9-2 verknüpfen Partei- und Postadressensammlungs-IDs mit Postadressen und Postadressen der Partei.
11. Schritte 10-1 bis 10-3 importieren Kundenadressen, Postadressen und Postadressen von Parteien in die Kundenbindungs-App.

### <a name="steps-in-the-party-electronic-address-template"></a>Schritte in der elektronischen Partei-Adressenvorlage

1. Schritte 1-1 bis 1-5 rufen Daten von der Finance and Operations-App und der Kundenbindungs-App ab und stellen diese Daten für ein Upgrade bereit.
2. Schritt 2 konsolidiert elektronische Adressen in der Kundenbindungs-App von Konto-, Kontakt- und Kreditoren-Entitäten.
3. Schritt 3 führt die primären elektronischen Adressdaten aus der Kundenbindungs-App und der Finance and Operations-App zusammen.
4. Schritt 4 erstellt CSV-Dateien.

    - Erstellen Sie neue elektronische Adressdaten für die Finance and Operations-App basierend auf Konto-, Kontakt- und Kreditorenadressen.
    - Erstellen Sie neue elektronische Adressdaten für die Kundenbindungs-App, basierend auf elektronischen Adress-, Konto-, Kontakt- und Kreditorenadressen in der Finance and Operations-App.

5. Schritt 5-1 importiert elektronische Adressen in die Kundenbindungs-App.
6. Schritt 5-2 erstellt CSV-Dateien, um die primären Adressen für Konten und Kontakte in der Kundenbindungs-App zu aktualisieren.
7. Schritte 6-1 bis 6-2 importieren Konten und Kontakthauptadressen in die Kundenbindungs-App.

## <a name="troubleshooting"></a>Problembehandlung

1. Wenn der Vorgang fehlschlägt, führen Sie die Data Factory erneut aus. Beginnen Sie mit der fehlgeschlagenen Aktivität.
2. Einige von der Data Factory generierte Dateien, können Sie zur Datenüberprüfung verwenden.
3. Die Data Factory wird basierend auf CSV-Dateien ausgeführt. Wenn ein Feldwert demnach ein Komma enthält, kann dies die Ergebnisse beeinträchtigen. Sie müssen alle Kommas aus den Feldwerten entfernen.
4. Die Registerkate **Überwachung** enthält Informationen zu allen Schritten und verarbeiteten Daten. Wählen Sie einen bestimmten Schritt zum Debuggen aus.

    ![Registerkarte „Überwachung“.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Mehr über die Vorlage

Weitere Informationen zur Vorlage finden Sie unter [Kommentare zur Readme-Datei für Azure Data Factory-Vorlagen](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
