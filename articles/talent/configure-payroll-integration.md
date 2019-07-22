---
title: Die Lohnintegration zwischen Talent und Dayforce konfigurieren
description: In diesem Thema wird erläutert, wie Sie die Integration zwischen Microsoft Dynamics 365 for Talent und Ceridian Dayforce konfigurieren, damit Sie den Zahlungslauf verarbeiten können.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 59234ef44ad22383ae5daf71d4b663c6183e6c05
ms.sourcegitcommit: d599bc1fc60a010c2753ca547219ae21456b1df9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2019
ms.locfileid: "1702817"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a>Lohnintegration zwischen Talent und Dayforce konfigurieren

[!include [banner](includes/banner.md)]

Die Integration zwischen Microsoft Dynamics 365 for Talent und Ceridian Dayforce beruht auf mehreren Konfigurationsschritten, die in diesem Thema beschrieben sind. Sie müssen die Integration sowohl in Talent als auch in Dayforce konfigurieren, bevor Sie einen Zahllauf verarbeiten können.

Wenn Sie einen Dienst wie Dayforce verwenden, um Zahlläufe abzuschließen, müssen Sie die Integration in Talent ermöglichen. Die Integration erfordert bestimmte Daten aus Talent. Daher müssen Sie überprüfen, dass die Daten, die Dayforce zugeordnet sind, in Talent in einer Weise konfiguriert werden, die die Integration unterstützt. Bei der Integration werden die folgenden allgemeinen Kategorien von Daten verwendet:

- Personalverwaltungsdaten
- Vergütungsdaten
- Lohndaten, wie Lohnzyklen, Lohnperioden und Einkommenscodes
- Arbeitskraftdaten

In diesem Thema werden die Schritte beschrieben, die Sie befolgen müssen, um die Integration zu ermöglichen. Es werden auch die Datentypen und die Konfigurationsdetails erklärt, die für die Integration erforderlich sind.

## <a name="enable-the-integration"></a>Die Integration aktivieren

In Talent müssen Sie die Integration aktivieren und die Konfigurationsinformationen eingeben, um eine Verbindung mit Dayforce herzustellen. Wenn Sie möchten, dass die erstellte Hauptbuchtransaktion in Microsoft Dynamics 365 for Finance and Operations importiert wird, müssen Sie auch ein Microsoft Azure-Speicherkonto einrichten und die Azure Storage-Verbindungszeichenfolge in Finance and Operations eingeben.

Um die Integration in Talent zu aktivieren, gehen Sie folgendermaßen vor.

1. Wählen Sie auf der Seite **Systemverwaltung** die Option **Integrationskonfiguration** aus.
2. Geben Sie den sicheren Datenübertragungsprotokoll-(FTP)-Endpunkt und den sicheren FTP-Ordnerpfad ein.
3. Geben Sie den Benutzernamen und das Kennwort des Benutzers ein, der auf den sicheren FTP-Endpunkt und Ordnerpfad zugreift.
4. Testen Sie die Verbindung nach Bedarf, und legen Sie die Option **Lohnintegration aktivieren** auf **Ja** fest.

Wenn die Integration aktiviert ist, werden Datenexportpaket und Dateien erstellt und die Häufigkeit wird festgelegt. Sie können diese Häufigkeit nach Bedarf ändern.

Weitere Informationen zu Azure-Speicherkonten und Azure Storage-Verbindungszeichenfolgen finden Sie in den folgenden Azure-Themen:

- [Über Azure-Speicherkonten](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [Azure Storage-Verbindungszeichenfolgen konfigurieren](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a>Technische Details, wenn Lohnintegration aktiviert ist

Die Aktivierung von Lohnintegration hat zwei primäre Auswirkungen:

- Ein Datenexportprojekt namens „Lohnintegrationsexport“ wird erstellt. Dieses Projekt enthält die Entitäten und Felder, die für die Lohnintegration erforderlich sind. Um das Projekt zu überprüfen, wechseln Sie zu **Systemverwaltung**, wählen Sie die Kachel **Datenverwaltung** aus, und öffnen Sie anschließend das Datenprojekt aus der Projektliste.
- Dieser Stapelverarbeitungsauftrag führt das Datenexportprojekt aus, verschlüsselt das Datenpaket und überträgt die Datenenpaketdatei auf den SFTP-Endpunkt, der auf dem Bildschirm **Integrationskonfiguration** konfiguriert wird.

> [!NOTE]
> Das Datenpaket, das zum SFTP-Endpunkt übertragen wird, wird mit einem Schlüssel verschlüsselt, für das Paket eindeutig ist. Der Schlüssel befindet sich in einer Azure Key Vault, auf den nur durch Ceridian zugegriffen werden kann. Es ist nicht möglich, die Datenpaketinhalte zu entschlüsseln und zu überprüfen. Wenn Sie den Inhalt des Datenpakets überprüfen möchten, müssen Sie das Datenprojekt „Lohnintegrationsexport“ manuell exportieren, herunterladen und dann öffnen. Beim manuellen Export wird keine Verschlüsselung angewendet oder das Paket übertragen.

## <a name="configure-your-data"></a>Ihre Daten konfigurieren 

Um die Lohnbuchung zu verarbeiten, müssen Sie Personalverwaltungsdaten in Talent konfigurieren. Sie müssen Organisationsdaten, wie Stellen und Positionen, zusammen mit Vorteilen Vergütungsinformationen einrichten. Diese Informationen stellen Beschäftigung, Lohn und die Abzugsinformationen bereit, die zur Generierung der Mitarbeiterentlohnung erforderlich sind.

### <a name="human-resource-data"></a>Personalverwaltungsdaten

#### <a name="benefits"></a>Vergütungen 

Die Personalverwaltung stellt eine Reihe von Tools für die Einrichtung und Verwaltung der Vorteile, Abzüge und Vergütungspläne der Arbeitskräfte bereit, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet.

Wenn Sie Vorteile erstellen, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.

##### <a name="benefit-plans"></a>Vorteilspläne

- Plan (erforderlich)
- Typ (erforderlich)
- Lohnauswirkung (erforderlich)
- Rückstände wiederherstellen
- Abzugsverfahren
- Abzugspriorität
- Periode eingrenzen
- Limitbetrag

##### <a name="benefits"></a>Vergütungen

- Plan (erforderlich)
- Typ (erforderlich)
- Option (erforderlich)
- Vorteilskennung (erforderlich)
- Häufigkeit
- Basis
- Betrag oder Satz
- Einkommenscode

##### <a name="supported-frequencies"></a>Unterstützte Häufigkeiten 

- Wöchentlich
- 14-tägig
- Halbmonatlich
- Monatlich

##### <a name="supported-bases"></a>Unterstützte Basen 

- Fester Betrag
- Prozent des Einkommens
- Produktive Stunden

Dayforce erstellt die folgenden Abzüge, basierend auf den Lohnauswirkungen, die im Vorteilsplan definiert sind.

| Auswahl in Talent        | Ergebnis in Dayforce                            |
|----------------------------|-----------------------------------------------|
| None                       | Es wird kein Abzug erstellt.                      |
| Nur Abzug             | Ein Mitarbeiterabzug wird erstellt.             |
| Nur Beitrag          | Ein Arbeitgeberabzug wird erstellt.             |
| Abzug und Beitrag | Mitarbeiter- und Arbeitgeberabzüge werden erstellt. |

Weitere Informationen darüber, wie Sie ein Vorteilsprogramm definieren und verwalten finden Sie in den folgenden Themen:

- [Mitarbeitervergütungsprogramm bereitstellen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [Neuen Vorteil erstellen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [Vorteilsberechtigungsregeln und Richtlinien definieren](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [Vorteile von Arbeitskräften registrieren und entfernen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a>Vergütung 

Die Vergütungsverwaltung dient zum Steuern der Abwicklung des Grundlohns und der Prämien. Sie steuern den festen Grundlohn eines Mitarbeiters und dessen Lohnsteigerungen nach Plänen für feste Vergütung. Die Zahlung leistungsbezogener Prämien, wie Boni, Leistungsprämien, Aktienoptionen und -überlassungen sowie Einmalprämien werden durch Pläne für variable Vergütung gesteuert.

Dayforce verwendet Vergütungsinformationen, um einen Stunden- oder Jahressatz für einen Mitarbeiter zu berechnen. Feste Vergütungspläne und Lohnsatzumrechnungen sind erforderlich. Mitarbeiter müssen einem festen Vergütungsplan zugeordnet werden.

Weitere Informationen zu Vergütungsplänen finden Sie in den folgenden Themen:

- [Feste Vergütungspläne erstellen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [Variable Vergütungspläne erstellen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [Gehalts-/Vergütungsstruktur und -pläne entwickeln](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [Vergütung verarbeiten](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [Vergütungsprozess definieren und Ergebnisse berechnen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [Einen Mitarbeiter in einem Plan für variable Vergütung registrieren](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a>Stellentyp 

Eine Stelle ist eine Sammlung der Aufgaben und Zuständigkeiten, die für eine Person, die eine Tätigkeit ausführt, obligatorisch sind. Weitere Informationen finden Sie in folgenden Themen:

- [Komponenten einer Stelle einrichten](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [Neue Einzelvorgänge definieren](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a>Positionen

Eine Position ist eine einzelne Instanz eines Einzelvorgangs. Beispielsweise ist die Position „Verkaufsleiter (Ost)” eine der Positionen, die der Stelle „Verkaufsleiter” zugeordnet werden. Eine Position ist in einer Abteilung vorhanden. Nur jeweils eine Arbeitskraft kann jeder Position zugeordnet werden.

Bedenken Sie die folgenden Daten und Konfigurationen, wenn Sie Positionen einrichten:

- Position (erforderlich)
- Beschreibung (erforderlich)
- Stelle (erforderlich)
- Abteilung (erforderlich)
- Positionstyp (erforderlich)
- Vollzeitäquivalent
- Normale Stunden pro Jahr (erforderlich)
- Gezahlt von der juristischen Person (erforderlich)
- Lohnzyklus (erforderlich)
- Standardfinanzdimension – Kostenstelle (erforderlich)
- Arbeitskraftzuweisung – Arbeitskraft, Zuweisungsanfang, Zuweisungsende, Ursachencode

Wenn mehrere Positionen in derselben Abteilung derselben Stelle zugeordnet sind, werden sie in einer einzelnen Position in Dayforce konsolidiert.

Weitere Informationen finden Sie in folgenden Themen:

- [Organisieren der Belegschaft anhand von Abteilungen, Stellen und Positionen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [Positionen einrichten](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a>Abteilungen

Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt. Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig. Sie können Abteilungen verwenden, um zu Funktionsbereiche zu melden. Abteilungen können Gewinn- und Verlustzuständigkeit haben.

Weitere Informationen finden Sie in folgenden Themen:

- [Eine Abteilung erstellen und der Abteilungshierarchie zuordnen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [Neue Abteilungen definieren](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a>Lohnzyklen und Lohnperioden

Ein Lohnzyklus bestimmt, wie oft Lohn ausgezahlt wird, sowie die spezifischen Tage, an denen Arbeitskräfte bezahlt werden. Ein Lohnzyklus kann beispielsweise monatlich sein, und Mitarbeiter werden am letzten Tag des Monats bezahlt. Alternativ könnte ein Lohnzyklus wöchentlich sein, und Mitarbeiter werden am Dienstag nach Ende der Lohnperiode bezahlt. Lohnzyklen werden Positionen zugewiesen, um zu steuern, wann Mitarbeiter in diesen Positionen bezahlt werden.

Nachdem Sie Lohnzyklen erstellen, können Sie Lohnperioden für jeden Zyklus generieren. Jede Lohnperiode enthält ein Standardzahlungsdatum, das auf den von Ihnen bereitgestellten Informationen basiert. Allerdings können Sie das Standardzahlungsdatum in einer Lohnperiode ändern, um Ausnahmen zuzulassen, wie beispielsweise wenn das Zahlungsdatum auf einen Feiertag fällt.

Die folgenden Informationen werden in Dayforce verwendet:

- Lohnzyklus (erforderlich)
- Lohnzyklushäufigkeit (erforderlich)
- Periodenstartdatum (erstes erforderliche Lohnperiode)
- Standardzahlungsdatum (erste erforderliche Lohnperiode)

Diese Informationen werden mit Dayforce als Lohngruppen integriert und sind nach Land oder Region für jeden Lohnzyklus getrennt. Es muss mindestens eine Lohnperiode vor der Integration generiert werden. Dayforce generiert Lohngruppenkalender und Zahlungsdaten basierend auf dem Anfangsdatum der ersten Lohnperiode und dem Standardzahlungsdatums, das in Talent eingerichtet ist.

#### <a name="earning-codes"></a>Einkommenscodes

Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten Die Codes haben verschiedene Parameter, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.

Die folgenden Informationen werden in Dayforce verwendet:

- Einkommenscode (erforderlich)
- Beschreibung
- Maßeinheit
- Produktiv

### <a name="worker-data"></a>Arbeitskraftdaten

Datensätze für die verschiedenen Arten von Arbeitskräften, die Sie haben, sind für Ihre Personalverwaltung- sowie für Ihre Lohnsysteme von Bedeutung. Anhand der eingegebenen Informationen lassen sich Arbeitskräfte sowie personenbezogene Informationen nachverfolgen.

Sie können die folgenden Informationen für Arbeitskräfte verwalten:

- **Basis** – Verwalten grundlegender Informationen über eine Arbeitskraft, beispielsweise Kontaktinformationen, demografische Informationen, Kennungsinformationen, Familieninformationen, Militärdienststatus, Ausländerinformationen sowie personenbezogene und Notfallkontakte.
- **Beschäftigung** – Verwalten von Informationen zum Beschäftigungsverhältnis einer Arbeitskraft, wie Unternehmens- oder Organisationszugehörigkeit, Positionszuweisung, Start- und Enddatum, Arbeitsberechtigung, Beschäftigungsbedingungen, Rente, Urlaub und Versetzungen.
- **Urlaub und Abwesenheit** – Verwalten von Informationen zur Abwesenheit einer Arbeitskraft, beispielsweise Arbeitszeitkalender, Abwesenheitsbuchungen und Abwesenheitseinrichtung.
- **Vergütung und Lohn** – Verwalten von Informationen zu den Vergütungsplänen und Lohndaten einer Arbeitskraft, wie der Planregistrierung, Boni, Leistung, Provision, Steuerdaten, Pensionierung und Gehaltsabzüge.

Wenn Sie Arbeitskraftinformationen eingeben, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.

#### <a name="general-information"></a>Allgemeine Angaben

- Personalnummer (erforderlich)
- Vorname (erforderlich)
- Nachname (erforderlich)
- Zweiter Vorname
- Dienstalterdatum
- Bekannt als

#### <a name="personal-information"></a>Personenbezogene Informationen

- Familienstand (erforderlich)
- Geburtsdatum (erforderlich)
- Geschlecht (erforderlich)
- Person mit Behinderung
- Nationalitätsland/-region (nur für Mexiko)

#### <a name="address-information"></a>Adressdaten

- Primär (erforderlich)
- Land/Region (erforderlich)
- Postleitzahl (erforderlich)
- Hausnummer (erforderlich) (nur für Mexiko)
- Gebäudeergänzung (nur für Mexiko)
- Ort (erforderlich)
- Bundesland/Kanton (erforderlich)
- Landkreis (erforderlich)

#### <a name="contact-information"></a>Kontaktdaten 

- Primär (erforderlich)
- Kontaktnummer (erforderlich)
- Durchwahl

#### <a name="payroll-information-and-earning-codes"></a>Lohndaten und Einkommenscodes

Mitarbeitern müssen bestimmte Einkommen mit einer bestimmten Zahlungshäufigkeit zugewiesen werden und sie müssen eine bevorzugte Zahlungsmethode haben. Die folgenden Felder werden in Dayforce verwendet, um zu gewährleisten, dass diese Voreinstellungen und Einstellungen verwendet werden.

##### <a name="earning-codes"></a>Einkommenscodes

- Position (erforderlich)
- Einkommenscode (erforderlich)
- Häufigkeit (erforderlich)
- Betrag (erforderlich)

##### <a name="payroll-information"></a>Lohndaten

- Zahlungsmethode
- Wirtschaftliche Region (erforderlich)
- Mitarbeitervergütungs-ID
- Personalausweisnummer (erforderlich)
- Militärdienstnummer
- Schichtkennung (erforderlich)
- Steuernummer (erforderlich)
- Gewerkschaftskennung (erforderlich)
- Arbeitstagkennung (erforderlich)
- Arbeitserlaubnisnummer (erforderlich)

> [!NOTE]
> Für die Zahlungsmethode unterstützt Mexiko **Bargeld**, **Scheck** (der physische Scheck des Unternehmens) und **Elektronische Zahlung**. Wenn keine Zahlungsmethode angegeben wird, wird **Scheck** standardmäßig verwendet.

#### <a name="employment-details"></a>Anstellungsdetails

Beschäftigungsdetailhistorie wird als Schlüsselinformation verwendet, um die Status für Einstellung, Kündigung und erneute Einstellung in Dayforce abzuleiten. Dayforce unterstützt nur einen aktiven Beschäftigungsdatensatz gleichzeitig.

- Datum des Beschäftigungsbeginns (erforderlich)
- Datum des Beschäftigungsendes
- Eintrittstermin
- Angepasster Tätigkeitsbeginn
- Kündigungsdatum (erforderlich)
- Kündigungsgrund (erforderlich bei Kündigung)

Die Schlüsseldaten eines Mitarbeiters werden abgeleitet, indem die folgenden Informationen verwendet werden.

| Talent                | Dayforce                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| Aktuellstes Einstellungsdatum | Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung                                 |
| Kündigungsdatum      | Kündigungsdatum des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung                                 |
| Eintrittstermin            | Angepasstes Startdatum, Startdatum oder Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht aktiven Beschäftigung |
| Ursprüngliches Einstellungsdatum    | Beschäftigungsbeginn des frühesten Beschäftigungsverlaufsdatensatzes                                               |

#### <a name="compensation"></a>Vergütung

Ein fester Vergütungsplan muss der primären Position jedes Mitarbeiters während einer Beschäftigungsperiode zugeordnet werden. Diese Periode beginnt mit dem Datum, an dem der Mitarbeiter eingestellt wurde (oder dem Datum des Beschäftigungsbeginns), und setzt sich bis zur Kündigung fort.

- Gültigkeitsdatum (erforderlich)
- Ablaufdatum
- Lohnsatz (erforderlich)
- Lohnsatzkonvertierungen (erforderlich)
- Jährliches Äquivalent (erforderlich)
- Stündliches Äquivalent (erforderlich)

Wenn ein Mitarbeiter auf Stundenbasis mehrere Positionen hat, wird die feste Vergütung der primären Position in Dayforce als Basissatz/-gehalt auf Mitarbeiterebene importiert. Für nicht-primäre Positionen wird der Stundensatz in der entsprechenden Position in Dayforce gespeichert.

Wenn ein Gehalt beziehender Mitarbeiter mehrere Positionen hat, wird der kumulative Stundensatz und das Jahresgehalt über alle aktiven Positionen hinweg abgeleitet und als Basissatz/-gehalt auf Arbeitnehmerebene verwendet.

#### <a name="identification-numbers"></a>Kennnummern

##### <a name="social-security-identifier"></a>Sozialversicherungsbezeichner 

Jeder Mitarbeiter muss einen primären Bezeichner haben. Dieser Bezeichner muss vom Kennungstyp **P.Reg.Nr.** sein. In Dayforce wird er automatisch als Sozialversicherungsbezeichner des Mitarbeiters abgeleitet, der für die Einstellung erforderlich ist.

- Primär (erforderlich)
- Kennungstyp = „P.Reg.Nr.”
- Ausstellungsdatum
- Ablaufdatum

Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **P.Reg.Nr.** melden. Jedoch wird nur der Datensatz, der als **Primär** markiert ist, in Dayforce integriert, unabhängig davon, ob die Nummer aktiv oder abgelaufen ist.

#### <a name="bank-accounts-and-disbursements"></a>Bankkonten und Auszahlungen

Gültige Bankkontoinformationen müssen für jeden Mitarbeiter eingegeben werden, der per Bankkontoüberweisungen bezahlt werden möchte.

| Talent                         | Dayforce                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| Bankkontonummer (erforderlich) |                                                                                                             |
| SWIFT-Code (erforderlich)          | Feld **Bankkennung** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.                                                             |
| Filialnummer (erforderlich)       |                                                                                                             |
| Bankkontotyp (erforderlich)   | Feld **Kontotyp** wird verwendet, wenn Lohn in Mexiko verarbeitet wird. Unterstützte Werte umfassen **Wird geprüft** und **Lohn**. |

> [!NOTE]
> Mitarbeiter, die per Bankkontoüberweisungen bezahlt werden möchten, müssen eine Verknüpfung zu einem Restbetrags-Bankkonto angeben, das sich unter einer juristischen Person befindet, deren primäre Adresse in Mexiko ist und das einem gültigen Bankkonto von einer mexikanischen Bank zugeordnet ist. Alle anderen Nicht-Restbetrags-Bankkonten werden ignoriert.

#### <a name="address-information"></a>Adressdaten

Jeder Mitarbeiter muss einen primären Standort haben. In Dayforce wird dieser Standort verwendet, um den primären Wohnsitz des Mitarbeiters für Steuerzwecke zu bestimmen.

- Primär (erforderlich)
- Land/Region (erforderlich)
- Postleitzahl (erforderlich)
- Straße (erforderlich)
- Hausnummer (erforderlich)
- Gebäudeergänzung
- Ort (erforderlich)
- Bundesland/Kanton (erforderlich)
- Landkreis (erforderlich)

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a>Konfigurieren Ihrer Daten, um Vergütung in den USA und Kanada zu generieren

Wenn Sie Vergütung für Mitarbeiter in den USA und Kanada generieren, müssen die folgenden Elemente konfiguriert werden:

- Abteilungen sind für Positionen erforderlich.
- Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.

> [!NOTE] 
> Sie können Talent so konfigurieren, dass es anfordert, dass Positionen eine Abteilung angegeben. Dazu wechseln Sie zu **Freigegebene Positionen der Personalverwaltung > Positionen > Abteilungen zu Positionen anfordern**. Es wird empfohlen, dass diese Einstellungen für die Integration erzwungen wird.

### <a name="job-types"></a>Stellentypen

Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren. Stellentypen sind erforderlich, damit Lohn in den USA und Kanada zu bearbeitet wird. Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn. Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.

Folgende Stellentypen und Beschreibungen sind erforderlich.

| Stellentyp   | Beschreibung |
|------------|-------------|
| Stündlich     | Stündlich      |
| Fest angestellt   | Fest angestellt    |

### <a name="position-types"></a>Positionstypen 

Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist. Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.

Folgende Positionstypen und Beschreibungen sind erforderlich.

| Positionstyp   | Beschreibung        |
|-----------------|--------------------|
| Vollzeit       | Vollzeitmitarbeiter |
| Teilzeit       | Teilzeitmitarbeiter |

### <a name="reason-codes"></a>Ursachencodes

Ursachencodes enthalten Informationen zum Status eines Mitarbeiters. Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.

Folgende Ursachencodes und Beschreibungen sind erforderlich.

| Ursachencode    | Beschreibung      | Zutreffende Szenarios |
|----------------|------------------|----------------------|
| RESIGNATION    | Kündigung durch Mitarbeiter      | Arbeitskraft kündigen     |
| TERMINATION    | Beendigung      | Arbeitskraft kündigen     |
| RETIREMENT     | Ruhestand       | Arbeitskraft kündigen     |
| OTHER          | Andere Gründe    | Arbeitskraft kündigen     |
| DEATH          | Tod            | Arbeitskraft kündigen     |
| LEAVEOFABSENCE | Beurlaubung | Arbeitskraft kündigen     |
| CONTRACTEND    | Vertragsende  | Arbeitskraft kündigen     |
| SALARYCHANGE   | Gehaltsänderung | Vergütung         |

### <a name="marital-status"></a>Familienstand

Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.

Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.

| Talent                 | Dayforce             |
|------------------------|----------------------|
| Verheiratet                | Verheiratet              |
| Ledig                 | Ledig               |
| Verwitwet                | Verwitwet              |
| Geschieden               | Geschieden             |
| Eingetragene Partnerschaft | Inländische Partnerschaft |
| None                   | None                 |
| Freie Partnerschaft             | Freie Partnerschaft           |

### <a name="gender"></a>Geschlecht

Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.

Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.

| Talent       | Dayforce        |
|--------------|-----------------|
| Männlich         | Männlich            |
| Weiblich       | Weiblich          |
| Nicht spezifisch | *Nicht unterstützt* |

### <a name="earning-codes"></a>Einkommenscodes

Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit. Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.

#### <a name="supported-frequencies"></a>Unterstützte Häufigkeiten

- Alle
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH – 1N2N3N4OFMTH
- 2N3N4N5OFMth – 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Adressen

Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können. Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.

| Talent          | Dayforce              |
|-----------------|-----------------------|
| Land/Region  | Ländercode          |
| Postleitzahl | PLZ           |
| Zustand           | Bundeslandcode            |
| Stadt            | Stadt                  |
| Verwaltungsbezirk          | Landkreis (Gemeinde) |
| Straße          | Adresszeile 1        |

### <a name="tax-regions"></a>Steuerregionen

Steuerregionen werden verwendet, um die entsprechende Steuer festzulegen, die bei der Lohngenerierung angewendet wird. Steuerregionen werden Dayforce als Standortadressen zugeordnet. Die Standardsteuerregion muss der aktiven Position der Arbeitskraft zugeordnet werden. 

- Steuerregion (erforderlich)
- Land/Region (erforderlich)
- Bundesland/Kanton (erforderlich)
- Verwaltungsbezirk 
- Ort (erforderlich)

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a>Konfigurieren Ihrer Daten, um Lohn in Mexiko zu generieren

Wenn Sie Vergütung für Mitarbeiter in Mexiko generieren, müssen die folgenden Elemente konfiguriert werden:

- Abteilungen sind für Positionen erforderlich.
- Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.

### <a name="job-types"></a>Stellentypen

Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren. Stellentypen sind erforderlich, um Lohn in Mexiko zu bearbeiten. Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn. Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.

Folgende Stellentypen und Beschreibungen sind erforderlich.

| Stellentyp   | Beschreibung |
|------------|-------------|
| Stündlich     | MX – Stundenbasis   |
| Fest angestellt   | MX – Fest angestellt |

### <a name="position-types"></a>Positionstypen 

Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist. Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.

Folgende Positionstypen und Beschreibungen sind erforderlich.

| Positionstyp   | Beschreibung        |
|-----------------|--------------------|
| Vollzeit       | Vollzeitmitarbeiter |
| Teilzeit       | Teilzeitmitarbeiter |

### <a name="reason-codes"></a>Ursachencodes

Ursachencodes enthalten Informationen zum Status eines Mitarbeiters. Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.

Folgende Ursachencodes und Beschreibungen sind erforderlich.

| Ursachencode            | Beschreibung                    | Zutreffende Szenarios |
|------------------------|--------------------------------|----------------------|
| DEPARTUREBEFOREPAYMENT | Abgang vor erster Lohnzahlung | Arbeitskraft kündigen     |
| RESIGNATION            | Kündigung durch Mitarbeiter                    | Arbeitskraft kündigen     |
| PENSION                | Rente                        | Arbeitskraft kündigen     |
| TERMINATION            | Beendigung                    | Arbeitskraft kündigen     |
| RETIREMENT             | Ruhestand                     | Arbeitskraft kündigen     |
| ABSENTEE               | Abwesende Person                       | Arbeitskraft kündigen     |
| OTHER                  | Andere Gründe                  | Arbeitskraft kündigen     |
| CLOSURE                | Betriebsferien               | Arbeitskraft kündigen     |
| DEATH                  | Tod                          | Arbeitskraft kündigen     |
| LEAVEOFABSENCE         | Beurlaubung               | Arbeitskraft kündigen     |
| CONTRACTEND            | Vertragsende                | Arbeitskraft kündigen     |
| SALARYCHANGE           | Gehaltsänderung               | Vergütung         |

### <a name="terms-of-employment"></a>Einstellungsbedingungen

Beschäftigungsbedingungen werden verwendet, um Kategorien von Beschäftigungsbedingungen zu erstellen. Die Bedingungen werden Dayforce als Beschäftigungsindikatorwerte zugeordnet.

Die folgenden Bedingungen für Beschäftigung und Beschreibungen sind erforderlich.

| Einstellungsbedingungen   | Beschreibung |
|-----------------------|-------------|
| Regelmäßig               | Regelmäßig     |
| Direkt                | Direkt      |
| Praktikum            | Praktikum  |
| Unbefristet             | Unbefristet   |

### <a name="marital-status"></a>Familienstand

Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.

Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.

| Talent                 | Dayforce                  |
|------------------------|---------------------------|
| Verheiratet                | Verheiratet                   |
| Ledig                 | Ledig                    |
| Verwitwet                | Verwitwet                   |
| Geschieden               | Geschieden                  |
| Eingetragene Partnerschaft | Inländische Partnerschaft      |
| None                   | *Wird von Mexiko nicht unterstützt* |
| Freie Partnerschaft             | *Wird von Mexiko nicht unterstützt* |

### <a name="gender"></a>Geschlecht

Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.

Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.

| Talent       | Dayforce                  |
|--------------|---------------------------|
| Männlich         | Männlich                      |
| Weiblich       | Weiblich                    |
| Nicht spezifisch | *Wird von Mexiko nicht unterstützt* |

### <a name="payment-method"></a>Zahlungsweise

Zahlungsmethoden geben dem Mitarbeiter und dem Unternehmen die Möglichkeit zu beschreiben, wie Mitarbeiter bezahlt werden. Zahlungsmethoden werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.

Die folgende Tabelle zeigt, wie Zahlungsmethoden Dayforce zugeordnet werden.

| Talent             | Dayforce                  |
|--------------------|---------------------------|
| Bargeld               | Bargeld                      |
| Elektronische Zahlung | Übertragen                  |
| Scheck              | Scheck                    |
| Bankwechsel         | *Wird von Mexiko nicht unterstützt* |
| Sonstige              | *Wird von Mexiko nicht unterstützt* |

### <a name="bank-account-type"></a>Bankkontotyp

Bankkontotypen werden für elektronische Zahlungen an Mitarbeiter verwendet. Bankkontotypen werden Dayforce als Übergweisungskontoinformationen zugeordnet. Die Bankkontotypen werden bei Bedarf zu den akzeptierten Werte nach der Integration übersetzt.

| Talent            | Dayforce                  |
|-------------------|---------------------------|
| Girokonto  | Girokonto           |
| Lohnkonto   | PayrollAccount            |
| Sparkonto   | *Wird von Mexiko nicht unterstützt* |
| BankGirot-Konto | *Wird von Mexiko nicht unterstützt* |
| PlusGirot-Konto | *Wird von Mexiko nicht unterstützt* |

### <a name="earning-codes"></a>Einkommenscodes

Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit. Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.

#### <a name="supported-frequencies"></a>Unterstützte Häufigkeiten

- Alle
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH – 1N2N3N4OFMTH
- 2N3N4N5OFMth – 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Adressen

Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können. Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.

| Talent              | Dayforce              |
|---------------------|-----------------------|
| Land/Region      | Ländercode          |
| Postleitzahl     | PLZ           |
| Zustand               | Bundeslandcode            |
| Stadt                | Stadt                  |
| Verwaltungsbezirk              | Landkreis (Gemeinde) |
| Straße              | Adresszeile 1        |
| Hausnummer       | Adresszeile 2        |
| Gebäudeergänzung | Adresszeile 5        |

### <a name="passport-number"></a>Ausweisnummer

Mitarbeiter können Ausweisinformationen melden. Diese Informationen haben den Kennungstyp **Ausweis** und sind in Dayforce als Teil der für Mexiko spezifischen Informationen eines Mitarbeiters integriert.

- Kennungstyp = „Ausweis”
- Ausstellungsdatum
- Ablaufdatum

Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **Ausweis** melden. Jedoch wird nur der aktuell aktive Ausweiseintrag in Dayforce integriert. Wenn alle Ausweiseinträge abgelaufen sind, ist der Ausweis, der zuletzt ausgestellt wurde, in Dayforce integriert.
