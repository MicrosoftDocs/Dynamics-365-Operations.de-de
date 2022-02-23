---
title: Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Mexiko
description: Dieses Thema enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung für Mexiko in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management erleichtern.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6d15a79a359b3c708b2b33893d700377a57c3eb7
ms.sourcegitcommit: cfd84321fba38e02e270d361df369a536a48efa3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2020
ms.locfileid: "4512233"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-mexico"></a>Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Mexiko

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Das Add-On für die elektronische Rechnungsstellung für Mexiko unterstützt derzeit eventuell nicht alle Funktionen, die im Dokument Comprobante Fiscal Digital por Internet (CFDI) und in der zugehörigen Integration in Microsoft Dynamics 365 Finance oder Dynamics 365 Supply Chain Management verfügbar sind.

Dieses Thema enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung für Mexiko erleichtern. Es führt Sie durch die Konfigurationsschritte, die in Regulatory Configuration Services (RCS) sowie in Finance länderabhängig sind. Außerdem werden Sie durch die Schritte geführt, die Sie in Finance ausführen müssen, um CFDI-Rechnungen über den Service zu übermitteln, und es wird erläutert, wie Sie die Verarbeitungsergebnisse und den Status von CFDI-Rechnungen überprüfen.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Schritte in diesem Thema ausführen, müssen Sie die Schritte in [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung](e-invoicing-get-started.md) ausführen.

## <a name="rcs-setup"></a>RCS-Einstellungen

Während der RCS-Einrichtung führen Sie folgende Aufgaben aus:

1. Importieren Sie die Funktion für die elektronische Rechnungsstellung zur Verarbeitung von CFDI-Rechnungen.
2. Überprüfen Sie die Formatkonfigurationen, die zum Generieren, Übermitteln und Empfangen von Antworten zu CFDI-Rechnungen sowie zum Übermitteln und Empfangen von Antworten zu Stornierungen erforderlich sind.
3. Konfigurieren Sie die Ereignisse, die die Szenarien für die Übermittlung von CFDI-Rechnungen unterstützen.
4. Veröffentlichen Sie die Funktion für die elektronische Rechnungsstellung für CFDI-Rechnungen.

> [!NOTE]
> „Die Funktion für die elektronische Rechnungsstellung“ ist der generische Name für die Ressource, die so konfiguriert und veröffentlicht ist, dass sie den Add-On-Server für die elektronische Rechnungsstellung verwendet. In diesem Fall sind CFDI-Rechnungen (MX) die Funktion für die elektronische Rechnungsstellung, die Sie einrichten werden.

## <a name="import-the-e-invoicing-feature"></a>Importieren der Funktion für die elektronische Rechnungsstellung

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktionen** im Abschnitt **Funktionen** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** die Option **Importieren** aus, um die Funktion **CFDI-Rechnungen (MX)** aus dem globalen Repository zu importieren.

    > [!NOTE]
    > Wenn Sie die Funktion in der Liste nicht sehen können, wählen Sie **Synchronisieren** aus und wiederholen Sie Schritt 3.

![Importieren der Funktion „CFDI-Rechnungen (MX)“](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

Wenn Sie die Funktion **CFDI-Rechnungen (MX)** aus dem globalen Repository importieren, werden alle Funktionseinstellungen, einschließlich der Konfigurationen und Aktionen, ebenfalls importiert.

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a>Erstellen einer neuen Version der Funktion „CFDI-Rechnungen (MX)“

Sie können eine neue Version erstellen, wenn beispielsweise URLs aktualisiert werden müssen. Weitere Informationen finden Sie unter [E-Rechnungsstellung CFDI](tasks/mx-00010-e-invoicing-cfdi.md).

- Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Versionen** die Option **Neu** aus.

![Hinzufügen einer neuen Version der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a>Aktualisieren der Konfigurationsversion

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Konfigurationen** entweder **Hinzufügen** oder **Löschen** aus, um die Konfigurationsversionen (EB-Dateiformatkonfigurationen) zu verwalten.

    ![Verwalten der Konfigurationen der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    Wenn Sie eine neue Version erstellen, werden alle Konfigurationen von der zuletzt veröffentlichten Version geerbt. Zur Verarbeitung von CFDI-Rechnungen sind folgende Konfigurationen erforderlich:

    - CFDI-Rechnung (BusinessDocumentService)
    - Import der CFDI-Antwortnachricht
    - Import des CFDI-Fehlerprotokolls
    - CFDI-Stornierungsanfrage (MX) (BusinessDocumentService)
    - CFDI-Rechnung (BusinessDocumentService)

2. Wählen Sie in der Liste eine Konfigurationsversion aus und wählen Sie dann **Bearbeiten** oder **Anzeigen** aus, um die Seite **Formatdesigner** zu öffnen, auf der Sie die Konfiguration bearbeiten oder anzeigen können.

    ![Öffnen der Seite „Formatdesigner“](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. Verwenden Sie die Seite **Formatdesigner**, um die EB-Formatkonfigurationen für Dateien zu bearbeiten und anzuzeigen. Weitere Informationen finden Sie unter [Erstellen elektronischer Berichterstellungskonfigurationen](../../dev-itpro/analytics/electronic-reporting-configuration.md).

    ![Formatdesignerseite](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>Verwalten der Einrichtungen der Funktion für die elektronische Rechnungsstellung

- Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Einrichtungen** entweder **Hinzufügen**, **Löschen** oder **Bearbeiten** aus, um die Einrichtungen der Funktion für die elektronische Rechnungsstellung zu verwalten.

![Verwalten der Einrichtungen der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

Um CFDI-Rechnungen zur Autorisierung zu übermitteln (generieren und übermitteln Sie die XML-Datei und verarbeiten Sie die Antwort), ist die Funktionseinrichtung **Verkaufsrechnung** erforderlich.

Um eine CFDI-Rechnungsstornierung zu übermitteln, sind die Funktionseinrichtungen **Stornierung** und **Abbrechen** erforderlich.

### <a name="configure-the-sales-invoice-feature-setup"></a>Konfigurieren der Funktionseinrichtung „Verkaufsrechnung“

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Einrichtungen** in der Spalte **Funktionseinrichtung** die Option **Verkaufsrechnung** aus.
2. Wählen Sie **Bearbeiten** aus, um Aktionen, Anwendbarkeitsregeln und Variablen zu konfigurieren.

    ![Bearbeiten der Einrichtung der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. Wählen Sie auf der Seite **Einrichtung der Funktionsversion** die Registerkarte **Aktionen** aus, um die Liste der Aktionen zu verwalten. Aktionen definieren eine Liste von Vorgängen, die nacheinander ausgeführt werden müssen, um die vollständige Ausführung des Ereignisses zu erreichen.

    ![Registerkarte „Aktionen“](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | Aktivitätskennung | Vorgang                   | Aktivitätsname                                  | Aktivitätsbeschreibung                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | 1         | Umwandeln des Dokuments       | Generieren einer CFDI-E-Rechnung ohne digitale Signatur | Generieren Sie die CFDI-E-Rechnung.                                |
    | 2         | Dokument signieren            | Digitale Signatur                                 | Unterzeichnen Sie die elektronische Rechnung zur Übermittlung digital.                |
    | 3         | Aufrufen des mexikanischen PAC-Service | Übermitteln der CFDI-E-Rechnung                        | Der WCF-Client (Windows Communication Foundation) übermittelt die CFDI-E-Rechnung. |
    | 4         | Verarbeiten der Antwort         | Analysieren der Antwort des Webdienstes                 | Analysieren Sie die Antwort des Webdienstes und geben Sie das Fehlerprotokoll zurück. |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a>Einrichten der URL mexikanische PAC-Webdienste 

1. Wählen Sie auf der Seite **Einrichtung der Funktionsversion** auf der Registerkarte **Aktionen** auf dem Inforegister **Aktionen** die Option **Aufrufen des mexikanischen PAC-Dienstes** aus.
2. Geben Sie auf dem Inforegister **Parameter** in das Feld **URL-Adresse** die URL des Webdienstes für die Übermittlung von CFDI-Rechnungen ein.

> [!NOTE]
> Gehen Sie ebenso vor, um die URL für die Aktion **Aufrufen des mexikanischen PAC-Dienstes** für die Funktionseinrichtungen **Abbrechen** und **Stornierungsanfrage** zu aktualisieren.

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a>Zuweisen der Entwurfsversion zu einer Umgebung für die elektronische Rechnungsstellung

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Umgebungen** die Option **Aktivieren** aus.
2. Wählen Sie im Feld **Umgebung** die Umgebung aus.
3. Wählen Sie im Feld **Gültig ab** das Datum aus, an dem die Umgebung wirksam werden soll.
3. Wählen Sie **Aktivieren** aus.

![Aktivieren einer Umgebung für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a>Ändern des Versionsstatus in „Abgeschlossen“

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Versionen** die Version der Funktion für die elektronische Rechnungsstellung mit dem Status **Entwurf** aus.
2. Wählen Sie **Status ändern \>Abschließen** aus.

## <a name="change-the-version-status-to-published"></a>Ändern des Versionsstatus in „Veröffentlicht“

- Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Versionen** die Option **Status ändern \> Veröffentlichen** aus.

## <a name="publish-the-e-invoicing-feature"></a>Veröffentlichen der Funktion für die elektronische Rechnungsstellung

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** die Registerkarte **Versionen** aus, um den Status der Funktion **CFDI-Rechnungen (MX)** zu verwalten.
2. Wählen Sie **Status ändern** aus, um den Status der Funktion zu ändern.

![Ändern des Status der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance"></a>Einrichten der Integration des Add-Ons für die elektronische Rechnungsstellung in Finance

Um das Add-On für die elektronische Rechnungsstellung in Finance einzurichten, führen Sie die folgenden Aufgaben aus:

1. Importieren Sie das EB-Datenmodell, die EB-Datenmodellzuordnung und die Formate, die für CFDI-Rechnungen erforderlich sind.
2. Konfigurieren Sie Antworttypen für die Aktualisierung der CFDI-Rechnungen. Diese Antworttypen werden für die Antwort vom Server der autorisierten Zertifizierungsstelle (PAC) verwendet.

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a>Importieren des EB-Datenmodells, der EB-Datenmodellzuordnung und der Kontextkonfigurationen für CFDI-Rechnungen

1. Melden Sie sich bei Finance an.
2. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Konfigurationsanbieter** die Kachel **Microsoft** aus. Stellen Sie sicher, dass dieser Konfigurationsanbieter auf **Aktiv** festgelegt ist. Weitere Informationen zum Festlegen eines Anbieters auf **Aktiv** finden Sie unter [Erstellen von Konfigurationsanbietern und Markieren als aktiv](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Wählen Sie **Repositorys** aus.
4. Wählen Sie **Globale Ressource \> Öffnen** aus.
5. Importieren Sie **Rechnungsmodell**, **Rechnungsmodellzuordnung**, **CFDI-Rechnungsformat (MX)**, **Format CFDI-Rechnungsstornierungsanforderung (MX)** und **Format CFDI-Rechnungsabbruch (MX)**.

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a>Aktivieren der Funktion zur Verarbeitung von CDFI-Rechnungen

1. Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.
2. Aktivieren Sie auf der Registerkarte **Funktionen** das Kontrollkästchen **Aktivieren** in den Zeilen für die Funktionsreferenzen **MX-00010** und **MX-00016**.

![Aktivieren der Funktionen zur Verarbeitung von CDFI-Rechnungen](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a>Importieren der EB-Konfigurationen und Einrichten der Antworttypen zur Aktualisierung von CFDI-Rechnungen

#### <a name="import-er-configurations"></a>ER Konfigurationen importieren

1. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Konfigurationsanbieter** die Kachel **Microsoft** aus.
3. Wählen Sie **Repositorys** aus.
4. Wählen Sie **Globale Ressource \> Öffnen** aus.
5. Importieren von **Antwortnachrichtenmodell**, **Import des CFDI-Fehlerprotokolls (MX)** und **Import der CFDI-Antwortnachricht (MX)**.

#### <a name="set-up-the-response-types"></a>Einrichten der Antworttypen

1. Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.
2. Wählen Sie auf der Registerkarte **Elektronisches Dokument** die Option **Hinzufügen** aus.
3. Geben Sie die Debitorenrechnungserfassung ein und wählen Sie dann im Feld **Tabellenname** die Projektrechnung aus.
4. Definieren Sie für jede Tabelle einen zugehörigen Dokumentkontext:

    - Wählen Sie für **Debitorenrechnungserfassung** die Option **Kontext Debitorenrechnung** aus.
    - Wählen Sie für **Projektrechnung** die Option **Kontext Projektrechnung** aus.

4. Wählen Sie **Antworttypen** aus, um die Antworttypen zu konfigurieren, die vom Add-On für die elektronische Rechnungsstellung zurückgegeben und in einer Debitorenrechnungserfassung oder einer Projektrechnung enthalten sein können.
5. Wählen Sie **Neu** aus und wählen Sie anschließend im Feld **Antworttyp** die Option **Antwort** aus.
6. Wählen Sie im Feld **Übermittlungsstatus** die Option **Ausstehend** aus.
7. Wählen Sie im Feld **Modellzuordnung** die Option **Importformat für Antwortnachrichten – Modellzuordnung aus Antwortnachricht** aus.
8. Wählen Sie **Speichern** aus.
9. Wählen Sie **Neu** aus und wählen Sie anschließend im Feld **Antworttyp** die Option **Antwortdaten** aus.
10. Wählen Sie im Feld **Übermittlungsstatus** die Option **Ausstehend** aus.
11. Wählen Sie im Feld **Modellzuordnung** die Option **Importformat für CFDI-Antwortdaten (Details) – Import von Antwortdaten** aus.
12. Wählen Sie **Speichern** aus.

## <a name="process-electronic-invoices-in-finance"></a>Verarbeiten elektronischer Rechnungen in Finance 

Während der Verarbeitung von CFDI-Rechnungen in Finance über das Add-On für die elektronische Rechnungsstellung können Sie folgende Aufgaben ausführen:

- Übermitteln Sie CFDI-Rechnungen.
- Zeigen Sie die Ausführungsprotokolle für die Übermittlung an.
- Übermitteln Sie die Stornierung einer CFDI-Rechnung.

### <a name="submit-cfdi-invoices"></a>Übermitteln von CFDI-Rechnungen

Nachdem Sie die Funktion **Integration des konfigurierbaren Add-Ons für die elektronische Rechnungsstellung** aktiviert haben, kann der Prozess **Elektronischen Rechnungsprozess exportieren/importieren** (**Debitoren \> Rechnungen \> Elektronische Rechnungen**) zur Übermittlung von CFDI-Rechnungen nicht mehr verwendet werden. Er wird durch einen neuen Prozess mit dem Namen **Elektronische Dokumente übermitteln** ersetzt.

> [!NOTE]
> Bevor Sie den neuen Prozess **Elektronische Dokumente übermitteln** verwenden, vergewissern Sie sich, dass die für elektronische Rechnungen in Mexiko erforderliche Einrichtung abgeschlossen ist. Weitere Hinweise zur Umrechnung finden Sie unter [Layoutversion 3.3 für CFDI](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).

1. Navigieren Sie zu **Organisationsverwaltung \> Periodisch \> Elektronische Dokumente \> Elektronische Dokumente übermitteln**.
2. Legen Sie für die erste Übermittlung irgendeines Dokuments immer die Option **Dokumente erneut übermitteln** auf **Nein** fest. Wenn Sie ein Dokument erneut über den Service übermitteln müssen, legen Sie diese Option auf **Ja** fest.
3. Wählen Sie auf dem Inforegister **Einzuschließende Datensätze** die Option **Filtern** aus, um das Dialogfeld **Anfrage** zu öffnen, in dem Sie eine Abfrage erstellen können, um Dokumente für die Übermittlung auszuwählen.

![Übermitteln eines CFDI-Dokuments](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> Bei Ihrem ersten Versuch, ein Dokument über den Service zu übermitteln, werden Sie aufgefordert, die Verbindung mit dem Add-On für die elektronische Rechnungsstellung zu bestätigen. Wählen Sie **Hier klicken, um eine Verbindung mit dem Electronic Document Submission Service herzustellen** aus.

### <a name="view-submission-logs"></a>Anzeigen von Übermittlungsprotokollen

Sie können die Übermittlungsprotokolle für alle übermittelten Dokumente oder nur für ein übermitteltes Dokument anzeigen.

#### <a name="view-all-submission-logs"></a>Anzeigen aller Übermittlungsprotokolle

Nach dem Aktivieren der Funktion **Integration des konfigurierbaren Add-Ons für die elektronische Rechnungsstellung** ist eine neue Seite verfügbar, über die Sie den Übermittlungsprozess für das Dokument nachverfolgen können. Sie können diese Seite verwenden, um die Übermittlungsprotokolle für alle übermittelten Dokumente anzuzeigen.

1. Navigieren Sie zu **Organisationsverwaltung \> Periodisch \> Elektronische Dokumente \> Übermittlungsprotokoll für elektronische Dokumente**.
2. Wählen Sie im Feld **Dokumenttyp** die Option **Debitorenrechnungserfassung** aus, um nach den erforderlichen elektronischen Dokumenten zu filtern.

    ![Auswählen eines Dokumenttyps, um die Übermittlungsprotokolle anzuzeigen](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. Wählen Sie im Aktivitätsbereich die Option **Anfragen \> Übermittlungsdetails** aus, um die Details der Ausführungsprotokolle für die Übermittlung anzuzeigen.

    ![Anzeigen der Details des Übermittlungsprotokolls](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

Die Informationen in den Übermittlungsprotokollen sind auf drei Inforegister aufgeteilt:

- **Verarbeitungsaktivitäten** – Dieses Inforegister zeigt das Ausführungsprotokoll für die Aktionen an, die in der in RCS eingerichteten Funktionsversion konfiguriert sind. Die Spalte **Status** zeigt an, ob die Aktion erfolgreich ausgeführt wurde.
- **Aktionsdateien** – Dieses Inforegister zeigt die Zwischendateien an, die während der Ausführung der Aktionen generiert wurden. Sie können **Anzeigen** auswählen, um die Datei herunterzuladen und anzuzeigen.
- **Aktivitätsprotokoll verarbeiten** – Dieses Inforegister zeigt die Ergebnisse der Kommunikation zwischen dem Add-On für die elektronische Rechnungsstellung und dem Ziel-Webdienst an. Außerdem zeigt es an, was von der Verarbeitung durch den Webdienst zurückgegeben wurde. Die Spalte **Fehlercode** zeigt den Rückgabecode an, der vom Autorisierungs-Webdienst zurückgegeben wurde.

Wenn die übermittelte CFDI-Rechnung autorisiert ist, wird ihr Status auf **Genehmigt** aktualisiert.

#### <a name="view-submission-logs-from-cfdi-invoices"></a>Anzeigen von Übermittlungsprotokollen über CFDI-Rechnungen

Nach dem Aktivieren der Funktion **Integration des konfigurierbaren Add-Ons für die elektronische Rechnungsstellung** können Sie die Übermittlungsprotokolle auch über die CFDI-Rechnungen anzeigen.

1. Wechseln Sie zu **Debitoren \> Abfragen und Berichte \> CFDI (elektronische Rechnungen)**.
2. Wählen Sie eine CFDI-Rechnung aus, die nach dem Aktivieren der Funktion **Integration des konfigurierbaren Add-Ons für die elektronische Rechnungsstellung** übermittelt wurde.
3. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Verlauf** die Option **Elektronisches Dokumentenprotokoll** aus.

![Anzeigen von Übermittlungsprotokollen über CFDI-Rechnungen](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> Für CFDI-Rechnungen, die vor dem Aktivieren der Funktion **Integration des konfigurierbaren Add-Ons für die elektronische Rechnungsstellung** übermittelt wurden, ist die Schaltfläche **Verlauf** verfügbar. Die Schaltfläche **Verlauf** ist für CFDI-Rechnungen, die nach dem Aktivieren der Funktion **Integration des konfigurierbaren Add-Ons für die elektronische Rechnungsstellung** übermittelt wurden, nicht verfügbar.

### <a name="submit-cancellation-of-cfdi-invoices"></a>Übermitteln der Stornierung von CFDI-Rechnungen

Nachdem Sie die Funktion **Integration des konfigurierbaren Add-Ons für die elektronische Rechnungsstellung** aktiviert haben, kann der alte Prozess zum Stornieren von CFDI-Rechnungen nicht mehr verwendet werden. Er wird durch einen neuen Stornierungsprozess ersetzt, der in die Seite **Übermittlungsprotokoll für elektronische Dokumente** eingebettet ist.

1. Wechseln Sie zu **Debitoren \> Abfragen und Berichte \> CFDI (elektronische Rechnungen)**.
2. Wenn die CFDI-Rechnung den Status **Genehmigt** hat, wählen Sie **Funktionen \> CFDI stornieren** aus.
3. Navigieren Sie zu **Organisationsverwaltung \> Periodisch \> Elektronische Dokumente \> Übermittlungsprotokoll für elektronische Dokumente**.
4. Wählen Sie die CFDI-Rechnung aus und wählen Sie dann **Funktionen \> Zugehörige Übermittlungen senden** aus.
5. Geben Sie eine Beschreibung für die zugehörige Übermittlung ein und wählen Sie dann **OK** aus.

#### <a name="view-cancellation-submission-logs"></a>Anzeigen von Übermittlungsprotokollen zu Stornierungen

1. Navigieren Sie zu **Organisationsverwaltung \> Periodisch \> Elektronische Dokumente \> Übermittlungsprotokoll für elektronische Dokumente**.
2. Wählen Sie im Feld **Dokumenttyp** die Option **Debitorenrechnungserfassung** aus, um ausschließlich nach Debitorenrechnungserfassungen zu filtern.
3. Wählen Sie die CFDI-Rechnung aus und wählen Sie dann im Aktivitätsbereich **Anfragen \> Zugehörige Übermittlungen** aus.

    Die Seite **Zugehörige Übermittlungen** zeigt alle zugehörigen Übermittlungen und ihren Übermittlungsstatus für eine bestimmte CFDI-Rechnung an. In der folgenden Abbildung stellt die erste Zeile die Übermittlung dar, die die Genehmigung der CFDI-Rechnung beantragt hat. Die zweite Zeile stellt die Übermittlung dar, mit der diese CFDI-Rechnung storniert wurde.

    ![Anzeigen der Übermittlungsprotokolle zu Stornierungen](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. Wählen Sie im Aktivitätsbereich die Option **Anfragen \> Übermittlungsdetails** aus, um die Details der Ausführungsprotokolle für die Übermittlung anzuzeigen.

    ![Anzeigen der Details des Übermittlungsprotokolls zu Stornierungen](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a>Datenschutzhinweis
Für die Aktivierung der Funktionen MX-00010 und MX-00016 (CFDI-Rechnung und CFDI-Stornierung) müssen möglicherweise nur begrenzte Daten gesendet werden, einschließlich der Steuerregistrierungskennung für die Organisation. Diese Daten werden an von der Steuerbehörde autorisierte Drittagenturen weitergeleitet, um elektronische Rechnungen in dem für die Integration in den Webdienst der Behörde erforderlichen Format an diese Steuerbehörde zu senden. Ein Administrator kann die Funktionen MX-00010 und MX-00016 (CFDI-Rechnung und CFDI-Stornierung) aktivieren und deaktivieren, indem er zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente** navigiert. Wählen Sie auf der Registerkarte **Funktionen** die Zeilen mit den Funktionen MX-00010 und MX-00016 aus und treffen Sie die entsprechende Auswahl. Daten, die aus diesen externen Systemen in diesen Dynamics 365-Onlinedienst importiert werden, unterliegen unseren [Datenschutzbestimmungen](https://go.microsoft.com/fwlink/?LinkId=512132). Weitere Informationen finden Sie in den Abschnitten zum Datenschutz in der landesspezifischen Funktionsdokumentation.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Übersicht über das Add-On für die elektronische Rechnungsstellung](e-invoicing-service-overview.md)
- [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung](e-invoicing-get-started.md)
- [Einrichten des Add-Ons für die elektronische Rechnungsstellung](e-invoicing-setup.md)
