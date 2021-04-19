---
title: Elektronische Rechnungsstellung in Regulatory Configuration Services (RCS) konfigurieren
description: In diesem Thema wird erläutert, wie Sie die elektronische Rechnungsstellung in Dynamics 365 Regulatory Configuration Services (RCS) konfigurieren.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 9958091db4a3d7ce0b625e5adc8e2a6b37878618
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840243"
---
# <a name="configure-electronic-invoicing-in-regulatory-configuration-services-rcs"></a>Elektronische Rechnungsstellung in Regulatory Configuration Services (RCS) konfigurieren

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zu den Konfigurationsfunktionen der elektronischen Rechnungsstellung in RCS (Dynamics 365 Regulatory Configuration Services).

Dank der Konfigurationsfunktionen können Sie mit der elektronischen Rechnungsstellung die geschäftlichen und behördlichen Anforderungen elektronischer Rechnungen erfüllen, ohne eine Codierung vornehmen zu müssen. In Szenarien, in denen elektronische Rechnungen von einem Webdienst elektronisch genehmigt werden müssen, können Sie mithilfe der Konfigurationsfunktionen auch die Anforderungen für den Austausch von Nachrichten mit einem Webdienst erfüllen, ohne Code ausführen zu müssen.

## <a name="electronic-reporting"></a>Elektronische Berichterstellung

Die elektronische Berichterstellung (Electronic Reporting, ER) unterstützt die elektronische Rechnungsstellung.

Die Datenmodellzuordnung und -formate sind konfigurierbare Komponenten, die über ER erstellt und verwaltet sowie in der elektronischen Rechnungsstellung verwendet werden. Der ER-Formatdesigner ist das Tool zum Erstellen und Verwalten von Dateiformaten. Es wird verwendet, um die Funktionen für die elektronische Rechnungsstellung zu konfigurieren.

Weitere Informationen finden Sie unter [Überblick über die elektronische Berichtserstellung (Electronic Reporting, ER)](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

## <a name="electronic-invoicing-features"></a>Funktionen für die elektronische Rechnungsstellung

Die Funktionen für die elektronische Rechnungsstellung sind für die Erstellung elektronischer Rechnungen über die elektronische Rechnungsstellung verantwortlich. Sie beinhalten die Konfigurationsregeln und verwenden sie zur Verarbeitung der von Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management an die elektronische Rechnungsstellung und an elektronische Rechnungen übermittelten Daten.

Die Funktionen unterstützen auch Szenarien, in denen die Einhaltung der Dateiformatspezifikationen erforderlich und die Ausgabe eine eigenständige elektronische Datei ist. In den meisten Fällen werden die Dateiformatspezifikationen von der Steuerbehörde veröffentlicht.

Schließlich unterstützen die Funktionen den Austausch von Nachrichten mit externen Webdiensten, die entweder von der Steuerbehörde oder einer akkreditierten Partei gehostet werden, sowie Anträge auf Genehmigung oder einen Genehmigungsstempel in der elektronischen Rechnung.

### <a name="availability-of-electronic-invoicing-features"></a>Verfügbarkeit von Funktionen für die elektronische Rechnungsstellung

Die Verfügbarkeit von Funktionen für die elektronische Rechnungsstellung hängt vom Land oder der Region ab. Obwohl einige Funktionen grundsätzlich verfügbar sind, befinden sich andere in der Vorschauversion.

#### <a name="preview-features"></a>Vorschaufunktionen

Die folgende Tabelle zeigt die Funktionen für die elektronische Rechnungsstellung an, die sich derzeit in der Vorschauversion befinden.

| Land/Region | Funktionsname                         | Geschäftsdokument |
|----------------|--------------------------------------|-------------------|
| Österreich        | Elektronische Rechnungen für Österreich (AT)    | Verkaufs- und Projektrechnungen |
| Belgien        | Elektronische Rechnungen für Belgien (BE)      | Verkaufs- und Projektrechnungen |
| Brasilien         | Brasilianisches NF-e (BR)                  | Steuerdokumentmodell 55, Korrekturschreiben, Stornierungen und Verwerfungen |
| Brasilien         | Brasilianisches NFS-e ABRASF Curitiba (BR) | Dienst Steuerdokumente |
| Dänemark        | Elektronische Rechnungen für Dänemark (DK)       | Verkaufs- und Projektrechnungen |
| Ägypten          | Elektronische Rechnungen für Ägypten (EG) | Verkaufs- und Projektrechnungen |
| Estland        | Elektronische Rechnungen für Estland (EE)     | Verkaufs- und Projektrechnungen |
| Finnland        | Elektronische Rechnungen für Finnland (FI)      | Verkaufs- und Projektrechnungen |
| Frankreich         | Elektronische Rechnungen für Frankreich (FR)       | Verkaufs- und Projektrechnungen |
| Deutschland        | Elektronische Rechnungen für Deutschland (DE)       | Verkaufs- und Projektrechnungen |
| Italien          | FatturaPA (IT)                       | Verkaufs- und Projektrechnungen |
| Mexiko         | Mexikanisches CFDI (MX)                    | Verkaufsrechnungen, Lieferscheine, Bestandsumlagerungen, Zahlungsergänzungen und Stornierungen |
| Niederlande    | Elektronische Rechnungen für die Niederlande (NL)        | Verkaufs- und Projektrechnungen |
| Norwegen         | Elektronische Rechnungen für Norwegen (NO)    | Verkaufs- und Projektrechnungen |
| Spanien          | Elektronische Rechnungen für Spanien (ES)      | Verkaufs- und Projektrechnungen |
| Europa         | Elektronische Rechnungen im PEPPOL-Format            | PEPPOL Verkaufs- und Projektrechnungen |

### <a name="configurable-components-of-electronic-invoicing-features"></a>Konfigurierbare Komponenten elektronischer Rechnungsstellungsfunktionen

Die Funktionen für die elektronische Rechnungsstellung bestehen aus den folgenden Gruppen konfigurierbarer Komponenten:

- **Formate** – Mithilfe von Formaten können Sie konfigurieren, was die elektronische Rechnungsstellung generieren muss, damit aus einem elektronischen Dokument eine elektronische Rechnung wird. Die Formate umfassen die Formatkonfiguration für die elektronische Rechnung sowie für Dateien und Nachrichten, die zum Übermitteln von Anfragen und zum Empfangen von Antworten verwendet werden, wenn die Kommunikation mit einem externen Webdienst erforderlich ist.
- **Aktionen** – Mithilfe von Aktionen können Sie konfigurieren, wie die elektronische Rechnungsstellung die Umwandlung eines elektronischen Dokuments, das von Finance und Supply Chain Management übermittelt wurde, in eine elektronische Rechnung generiert.
- **Anwendbarkeitsregeln** – Mithilfe von Anwendbarkeitsregeln können Sie den Kontext konfigurieren, den die elektronische Rechnungsstellung berücksichtigen muss, um eine Funktion für die elektronische Rechnungsstellung zu verarbeiten.
- **Variablen** – Mithilfe von Variablen können Sie die Unterstützung für den Aufbau der Konfigurationslogik konfigurieren. Variablen können zur Eingabe von Werten dienen, um eine bestimmte Aktion auszuführen. Alternativ können sie für den Austausch von Werten zwischen Finance und Supply Chain Management sowie der elektronischen Rechnungsstellung dienen.
- **Elektronische Dokumentmodellzuordnung** – Mithilfe der elektronischen Dokumentmodellzuordnung können Sie die ER-Modellzuordnung konfigurieren. Die Modellzuordnung definiert die Datenzuordnung der abstrakten Rechnung, die beim Übermitteln elektronischer Dokumente in der elektronischen Rechnungsstellung integriert ist.
- **Rechnungskontextmodell** – Mithilfe des Rechnungskontextmodells können Sie das ER-Rechnungskontextmodell konfigurieren und den Kontext einer elektronischen Rechnungsstellungsfunktion definieren.
- **Antworttypen** – Mithilfe von Antworttypen können Sie konfigurieren, was die elektronische Rechnungsstellung in Finance und Supply Chain Management als Ergebnis der elektronischen Rechnungsverarbeitung aktualisieren muss.

### <a name="formats"></a>Formate

Die folgenden Listen zeigen die ER-Formatkonfigurationen, die für die Funktionen zur elektronischen Rechnungsstellung verfügbar sind.

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a>Österreichische (AT) elektronische Rechnungen: Verkaufs- und Projektrechnungen für Österreich

- OIOUBL Verkaufsrechnung
- OIOUBL Projektrechnung
- OIOUBL Verkaufsgutschrift
- OIOUBL Projektgutschrift

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a>Belgische (BE) elektronische Rechnung: Verkaufs- und Projektrechnungen für Belgien

- UBL Verkaufsrechnung BE
- UBL Projektrechnung BE
- UBL Projektgutschrift BE
- UBL Verkaufsgutschrift BE

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a>Brasilianisches (BR) NF-e: NF-e Federal (Brasilien)

- Exportformat zur Übermittlung der NF-e (BR)
- Exportformat des NF-e-Korrekturschreibens (BR)
- Exportformat der NF-e-Stornierung (BR)
- Exportformat der NF-e-Verwerfung (BR)

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a>Brasilianisches NFS-e (BR): NFS-e ABRASF Curitiba (Stadt)

- NFS-e ABRASF Curitiba (BR)
- NFS-e ABRASF-Abfrage Curitiba (BR)

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a>Dänische (DK) elektronische Rechnung: Verkaufs- und Projektrechnungen für Dänemark

- OIOUBL Verkaufsrechnung
- OIOUBL Projektrechnung
- OIOUBL Verkaufsgutschrift
- OIOUBL Projektgutschrift

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a>Niederländische (NL) elektronische Rechnung: Verkaufs- und Projektrechnungen für die Niederlande

- UBL Verkaufsrechnung NL
- UBL Projektrechnung NL
- UBL Projektgutschrift NL
- UBL Verkaufsgutschrift NL

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a>Ägyptische (EG) elektronische Rechnung: Verkaufs- und Projektrechnungen für Ägypten

- Verkaufsrechnung (EG) (Fakturierung)
- Projektrechnung (EG) (Fakturierung)

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a>Estnische (EE) elektronische Rechnung: Verkaufs- und Projektrechnungen für Estland

- Vertriebsrechnung (EE)
- Projektrechnung (EE)

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a>Finnische (FI) elektronische Rechnung: Verkaufs- und Projektrechnungen für Finnland

- Vertriebsrechnung (FI)
- Projektrechnung (FI)

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a>Französische (FR) elektronische Rechnung: Verkaufs- und Projektrechnungen für Frankreich

- UBL Verkaufsrechnung FR
- UBL Projektrechnung FR
- UBL Projektgutschrift FR
- UBL Verkaufsgutschrift FR

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a>Deutsche (DE) elektronische Rechnung: Verkaufs- und Projektrechnungen für Deutschland

- Verkaufsrechnung (DE)
- Projektrechnung (DE)

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a>Italienische (IT) elektronische Rechnung: Verkaufs- und Projektrechnungen für Italien

- Verkaufsrechnung (IT)
- Projektrechnung (IT)

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a>Mexikanisches (MX) CFDI: CFDI für Mexiko

- CFDI-Rechnungsformat (MX)
- CFDI-Lieferschein (MX)
- CFDI-Lagerübertragung (MX)
- CFDI-Zahlungsformat (MX)
- CFDI-Rechnungsstornierungsformat (MX)

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a>Norwegische (NO) elektronische Rechnung: Verkaufs- und Projektrechnungen für Norwegen

- OIOUBL Verkaufsrechnung
- OIOUBL Projektrechnung
- OIOUBL Verkaufsgutschrift
- OIOUBL Projektgutschrift

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a>Elektronische PEPPOL-Rechnung: Verkaufs- und Projektrechnungen im PEPPOL-Format

- Verkaufsrechnung im PEPPOL-Format
- Projektrechnung im PEPPOL-Format
- Verkaufsgutschrift im PEPPOL-Format
- Projektgutschrift im PEPPOL-Format

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a>Spanische (ES) elektronische Rechnung: Verkaufs- und Projektrechnungen für Spanien

- Vertriebsrechnung (ES)
- Projektrechnung (ES)

### <a name="actions"></a>Aktionen

In der folgenden Tabelle sind die verfügbaren Aktionen aufgeführt, und ob sie derzeit allgemein verfügbar sind oder sich noch in der Vorschauversion befinden.

| Vorgang                                        | Beschreibung                                                                  | Verfügbarkeit         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| Umwandeln des Dokuments                            | Führen Sie das elektronische Berichterstellungsformat aus, um das Dokument umzuwandeln.                   | Allgemein verfügbar  |
| XML-Dokument unterzeichnen                             | Unterzeichnen Sie XML-Dokumente mit einer digitalen Signatur.                                   | Vorschau           |
| JSON-Dokument für die ägyptische Steuerbehörde unterzeichnen | Unterzeichnen Sie JSON-Dokumente für die ägyptische Steuerbehörde mit einer digitalen Signatur.       | Allgemein verfügbar  |
| In ägyptischen ETA-Dienst integrieren           | Kommunizieren Sie mit der ägyptischen Steuerbehörde.                                     | Allgemein verfügbar  |
| Brasilianischen SEFAZ-Dienst aufrufen                  | Integration in den brasilianischen SEFAZ-Dienst zur Übermittlung von Steuerdokumenten.       | Vorschau           |
| Mexikanischen PAC-Dienst aufrufen                      | Integration in den mexikanischen PAC-Dienst zur CFDI-Übermittlung.                      | Vorschau           |
| Verarbeiten der Antwort                              | Analysieren Sie die vom Webdienstaufruf erhaltene Antwort.                     | Allgemein verfügbar  |
| MS Power Automate verwenden                         | Integrieren Sie in den in Microsoft Power Automate eingebauten Flow.                       | Vorschau           |

## <a name="configuration-providers"></a>Konfigurationsanbieter

Konfigurationsanbieter stellen die Funktionen für die elektronische Rechnungsstellung und ihre ER-Komponenten bereit, z. B. die Modellzuordnung, die Formatkonfiguration und das Kontextmodell. Sie veröffentlichen die elektronischen Rechnungsstellungsfunktionen und ER-Komponenten im zugehörigen globalen Repository. Von dort können andere Organisationen sie herunterladen.

Bevor Sie die Funktionen für die elektronische Rechnungsstellung über RCS konfigurieren, müssen Sie Ihre eigene Organisation als Konfigurationsanbieter im Modul für die **Elektronische Berichterstellung** konfigurieren. Weitere Informationen zum Festlegen eines Konfigurationsanbieters auf **Aktiv** finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a>Anzeigen von Funktionen für die elektronische Rechnungsstellung im globalen Repository

Synchronisieren Sie die RCS-Instanz Ihrer Organisation, um die Funktionen für die elektronische Rechnungsstellung zu durchsuchen, die im globalen Repository für einen bestimmten Konfigurationsanbieter verfügbar sind. Nach Abschluss der Synchronisierung wird die Liste der verfügbaren Funktionen für die elektronische Rechnungsstellung aktualisiert.

## <a name="importing-electronic-invoicing-features"></a>Importieren elektronischer Rechnungsstellungsfunktionen

Bevor Sie die Funktionen für die elektronische Rechnungsstellung verwenden oder konfigurieren, müssen Sie sie in die RCS-Instanz Ihrer Organisation importieren. Der Importvorgang erstellt eine lokale Kopie der Funktionen und kopiert alle von den Funktionen verwendeten ER-Artefakte (z. B. Format- und Modellkonfigurationen) in die RCS-Instanz Ihrer Organisation.

Sie können die Funktionen für die elektronische Rechnungsstellung über jeden Konfigurationsanbieter importieren.

## <a name="creating-electronic-invoicing-features"></a>Erstellen elektronischer Rechnungsstellungsfunktionen

Sie können eine Funktion für die elektronische Rechnungsstellung von Grund auf neu erstellen oder aus einer anderen elektronischen Rechnungsstellungsfunktion ableiten.

Wenn Sie eine elektronische Rechnungsstellungsfunktion von Grund auf neu erstellen, müssen Sie die ER-Komponenten manuell hinzufügen (z. B. Konfigurationen der Funktionsversion und andere Konfigurationen, wie beispielsweise die Einrichtung der Funktionsversion und die Einrichtung der Anwendung). Wenn Sie eine Funktion durch Ableiten aus einer anderen erstellen, erbt die neue Funktion alle Konfigurationen des Originals. 

## <a name="electronic-invoicing-feature-version"></a>Version der elektronischen Rechnungsstellungsfunktion

Die Funktionen für die elektronische Rechnungsstellung sind versioniert. Wird eine neue Version erstellt, erhöht sich automatisch die Versionsnummer. Für die neue Version kann ein „Gültig ab“-Datum definiert werden.

Die Versionen der elektronischen Rechnungsfunktion folgen einem Lebenszyklus mit bis zu drei Status:

- **Entwurf** – Wenn sich eine Funktionsversion in diesem Status befindet, können Sie ihre Konfigurationsattribute und alle Artefakte (z. B. Dateiformatkonfigurationen) bearbeiten.
- **Abgeschlossen** – Befindet sich eine Funktionsversion in diesem Status, wurde sie im globalen Repository veröffentlicht, das Ihrer Organisation zugeordnet ist. Sie können die Funktionsversion oder eine der ER-Komponenten nicht mehr bearbeiten.
- **Veröffentlicht** – Befindet sich eine Funktionsversion in diesem Status, wurde sie in der elektronischen Rechnungsstellung veröffentlicht. Sie können die Funktionsversion oder eine der ER-Komponenten nicht mehr bearbeiten.

### <a name="feature-configurations"></a>Funktionskonfigurationen

Funktionskonfigurationen enthalten alle ER-Formatkonfigurationen, welche die elektronischen Rechnungsstellungsfunktionen nutzen. Alle elektronischen Dateien, die eine elektronische Rechnungserstellungsfunktion während der Verarbeitung verwendet, stammen aus den Formatkonfigurationen, die den Funktionskonfigurationen dieser Funktion hinzugefügt wurden.

Über die Funktionskonfigurationen können Sie auf den ER-Formatdesigner zugreifen, das ER-Tool, mit dem Formatkonfigurationen erstellt werden.

### <a name="feature-setup"></a>Einrichtung von Funktionen

Funktionseinrichtungen werden in Kombination mit Funktionskonfigurationen verwendet. Jede Funktionseinrichtung enthält eine Reihe von Aktionen, Anwendbarkeitsregeln und Variablen, die das erwartete Verhalten bereitstellen, sodass eine elektronische Rechnungsstellungsfunktion eine bestimmte Anforderung der elektronischen Rechnung erfüllen kann.

### <a name="application-setup"></a>Anwendungseinrichtung

Die Anwendungseinrichtung muss einer zuvor erstellten verbundenen Anwendung zugeordnet sein.

Über die Anwendungseinrichtung können Sie den Teil einer elektronischen Rechnungsstellungsfunktion konfigurieren, der in Finance und Supply Chain Management ausgeführt werden muss. Unabhängig von der elektronischen Rechnungsstellungsfunktion sind mindestens drei konfigurierbare Komponenten obligatorisch:

- **Tabellenname** – Die Entität in Finance und Supply Chain Management, das die gebuchten Rechnungen hält und auf dem die elektronische Rechnungsstellungsfunktion basiert.
- **Kontext** – Der Name des über ER konfigurierten Rechnungskontextmodells.
- **Geschäftsdokumentzuordnung** – Der Name des über ER konfigurierten Rechnungszuordnungsmodells.

> [!IMPORTANT]
> Die in der Anwendungseinrichtung eingegebene Konfiguration kann in Finance und Supply Chain Management angezeigt werden. Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**. Wählen Sie auf der Registerkarte **Elektronisches Dokument** **Bereitstellen** und anschließend die Option **Verbundene Anwendung** aus.

### <a name="deploying-feature-versions"></a>Bereitstellen von Funktionsversionen

Verwenden Sie in RCS den Befehl **Bereitstellen** zum gezielten Veröffentlichen einer Funktionsversion für die elektronische Rechnungsstellung. Wählen Sie **Bereitstellen** und anschließend eine der folgenden Optionen aus, um das Ziel der Bereitstellung zu definieren: 

- **Service-Umgebung** – Wenn das Ziel der Bereitstellung die Service-Umgebung ist, wird die Funktionsversion für die elektronische Rechnungsstellung in der Service-Umgebung veröffentlicht. Die elektronische Rechnungsstellung ist dann bereit, elektronische Dokumente zu empfangen und zu verarbeiten, die von Finance und Supply Chain Management gesendet werden.
- **Verbundene Anwendung** – Wenn das Ziel der Bereitstellung die verbundene Anwendung ist, wird die Konfiguration, die von der Anwendungseinrichtung bereitgestellt wird, in die zuvor zugeordnete Instanz für Finance und Supply Chain Management geschrieben.

Es können nur Funktionsversionen für die elektronische Rechnungsstellung mit dem Status **Abgeschlossen** bereitgestellt werden – entweder in einer Service-Umgebung oder in einer verbundenen Anwendung.

### <a name="removing-feature-versions"></a>Entfernen von Funktionsversionen

Verwenden Sie in RCS den Befehl **Bereitstellung zurücknehmen**, um eine bestimmte Funktionsversion für die elektronische Rechnungsstellung aus einer Service-Umgebung in der elektronischen Rechnungsstellung zu entfernen.

> [!IMPORTANT]
> Der Befehl **Bereitstellung zurücknehmen** funktioniert nur in Service-Umgebungen. Es werden keine Funktionsversionen für die elektronische Rechnungsstellung aus verbundenen Anwendungen entfernt.

### <a name="rebasing-electronic-invoicing-features"></a>Rebasieren elektronischer Rechnungsstellungsfunktionen

Wird eine elektronische Rechnungsstellungsfunktion von einer anderen abgeleitet, aktualisiert der Befehl **Rebasieren** die abgeleitete Funktion mit den Änderungen, die mit der ursprünglichen Funktion eingeführt wurden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Elektronische Rechnungen in Finance und Supply Chain Management ausstellen](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
