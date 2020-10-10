---
title: Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Italien
description: Dieses Thema enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung für Italien in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management erleichtern.
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
ms.openlocfilehash: ea0408f4ef72bf77a0659799075338e4e6b2aa30
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835959"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a>Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Italien

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Das Add-On für die elektronische Rechnungsstellung für Italien unterstützt derzeit möglicherweise nicht alle Funktionen, die für elektronische Rechnungen in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management verfügbar sind. 

Dieses Thema enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung für Italien erleichtern. Es führt Sie durch die Konfigurationsschritte, die in Regulatory Configuration Services (RCS) sowie in Finance länderabhängig sind. Es führt Sie auch durch den Übermittlungsprozess für elektronische Rechnungen, die über den Service im für Italien spezifischen Format **FatturaPA** erstellt werden, und es wird erläutert, wie die Ergebnisse der Verarbeitung überprüft werden.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Schritte in diesem Thema ausführen, müssen Sie die Schritte in [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung](e-invoicing-get-started.md) ausführen.

## <a name="rcs-setup"></a>RCS-Einstellungen

Während der RCS-Einrichtung führen Sie folgende Aufgaben aus:

1. Importieren Sie die Funktion für die elektronische Rechnungsstellung für den Export elektronischer Kundenrechnungen im Format **FatturaPA**.
2. Überprüfen Sie die Formatkonfigurationen, die zum Generieren, Übermitteln und Empfangen von Antworten zu elektronischen Rechnungen erforderlich sind.
3. Konfigurieren Sie die Ereignisse, die die Szenarien für die elektronische Rechnungsübermittlung unterstützen.
4. Veröffentlichen Sie die Funktion für die elektronische Rechnungsstellung.

> [!NOTE]
> „Die Funktion für die elektronische Rechnungsstellung“ ist der generische Name für die Ressource, die so konfiguriert und veröffentlicht ist, dass sie den Add-On-Server für die elektronische Rechnungsstellung verwendet. In diesem Fall ist der Export elektronischer Kundenrechnungen die Funktion für die elektronische Rechnungsstellung, die Sie einrichten werden.

## <a name="import-the-e-invoicing-feature"></a>Importieren der Funktion für die elektronische Rechnungsstellung

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktionen** im Abschnitt **Funktionen** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** die Option **Importieren** aus, um die Funktion für die elektronische Rechnungsstellung aus dem globalen Repository zu importieren.

    > [!NOTE]
    > Wenn die Liste der verfügbaren Funktionen nicht angezeigt wird, wählen Sie **Synchronisieren** aus. 

4. Wählen Sie die Funktion **Elektronische Rechnungen exportieren (IT)** aus und wählen Sie dann **Importieren** aus.

![Importieren der Funktion „Elektronische Rechnungen exportieren (IT)“](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

Wenn Sie die Funtion **Elektronische Rechnungen exportieren (IT)** aus dem globalen Repository importieren, werden auch alle Einstellungen importiert, die in den nächsten Abschnitten beschrieben werden.

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a>Erstellen einer neuen Version der Funktion „Elektronische Rechnungen exportieren (IT)“

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Versionen** die Option **Neu** aus. 

    ![Hinzufügen einer neuen Version der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    Als Nächstes konfigurieren Sie die EB-Formate (Elektronische Berichterstellung), die der Funktion für die elektronische Rechnungsstellung zugeordnet sind.

2. Wählen Sie auf der Registerkarte **Konfigurationen** die Option **Hinzufügen** aus, um die Konfigurationsversionen zu verwalten.

    ![Verwalten der Konfigurationsversionen der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    In diesem Schritt fügen Sie die EB-Formate verschiedener Dateien hinzu, die zum Exportieren elektronischer Rechnungen in Italien verwendet werden, und konfigurieren sie. Verwenden Sie in Italien für elektronische Rechnungen im FatturaPA-Format entweder die folgenden Standardkonfigurationen oder die tatsächlich angepassten Konfigurationen, die Sie für die elektronische Rechnungsstellung verwenden:

    - Verkaufsrechnung (IT)
    - Projektrechnung (IT)

    Wenn Sie eine Funktion für die elektronische Rechnungsstellung erstellen, die von einer anderen Funktion für die elektronische Rechnungsstellung abgeleitet ist, werden alle EB-Formate von der ursprünglichen Funktion geerbt.

3. Wählen Sie eine bestimmte Dateikonfiguration im ER-Format aus.
4. Wählen Sie **Bearbeiten** oder **Anzeigen** aus, um die Seite **Formatdesigner** zu öffnen.

    ![Öffnen der Seite „Formatdesigner“](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. Verwenden Sie die Seite **Formatdesigner**, um die EB-Formatkonfigurationen für Dateien zu bearbeiten und anzuzeigen.

    ![Formatdesignerseite](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>Verwalten der Einrichtungen der Funktion für die elektronische Rechnungsstellung

- Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Einrichtungen** entweder **Hinzufügen**, **Löschen** oder **Bearbeiten** aus, um die Einrichtungen der Funktion für die elektronische Rechnungsstellung zu verwalten.

![Verwalten der Einrichtungen der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

In diesem Schritt konfigurieren Sie die Ereignisse, die für elektronische Rechnungen gelten, einschließlich der Generierung der XML-Ausgabedateien im Format **FatturaPA** und digitaler Signaturen (falls erforderlich).

### <a name="configure-the-sales-invoice-feature-setup"></a>Konfigurieren der Funktionseinrichtung „Verkaufsrechnung“

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Einrichtungen** in der Spalte **Funktionseinrichtung** die Option **Verkaufsrechnung** aus.
2. Wählen Sie **Bearbeiten** aus.
3. Wählen Sie auf der Seite **Einrichtung der Funktionsversion** die Registerkarte **Aktionen** aus, um die Liste der Aktionen zu verwalten. Aktionen definieren eine Liste von Vorgängen, die nacheinander ausgeführt werden müssen, um die vollständige Ausführung des Ereignisses zu erreichen.

    ![Registerkarte „Aktionen“](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | Aktivitätskennung | Aktivitätsname        | Aktivitätsbeschreibung                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | 1         | Umwandeln des Dokuments | Erstellen Sie die XML-Datei der elektronischen Rechnung im Format **FatturaPA**. |
    | 2         | Dokument signieren      | Wenden Sie die digitale Signatur auf die XML-Datei an.             |

4. Wählen Sie die Registerkarte **Anwendbarkeitsregeln** aus, um die Anwendbarkeitsregeln anzuzeigen und zu verwalten. Anwendbarkeitsregeln definieren den Kontext, in dem die Aktion ausgeführt wird.

    ![Registerkarte „Anwendbarkeitsregeln“](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. Wählen Sie die Registerkarte **Variablen** aus, um die Variablen anzuzeigen und zu verwalten.

    ![Registerkarte „Variablen“](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. Definieren Sie die öffentlichen Variablen, die zum Ausführen der Aktionen erforderlich sind.

### <a name="configure-the-project-invoice-feature-setup"></a>Konfigurieren der Funktionseinrichtung „Projektrechnung“ 

Die Schritte und Einstellungen, die zum Konfigurieren der Funktionseinrichtung **Projektrechnung** erforderlich sind, sind den Schritten und Einstellungen für die Funktionseinrichtung **Verkaufsrechnung** sehr ähnlich. Wenn Sie mit Projektrechnungen arbeiten, lesen Sie die Prozeduren für Verkaufsrechnungen.

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a>Zuweisen der Funktion für die elektronische Rechnungsstellung zur Umgebung

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Umgebungen** die Option **Aktivieren** aus.
2. Wählen Sie im Feld **Umgebung** die Umgebung aus.
3. Wählen Sie im Feld **Gültig ab** das Datum aus, an dem die Umgebung wirksam werden soll.
4. Wählen Sie **Aktivieren** aus. 

![Aktivieren der Umgebung für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a>Veröffentlichen der Funktion für die elektronische Rechnungsstellung

Sie können die Funktion für die elektronische Rechnungsstellung veröffentlichen, indem Sie den Versionsstatus in **Abgeschlossen** oder **Veröffentlicht** ändern.

### <a name="change-the-version-status-to-completed"></a>Ändern des Versionsstatus in „Abgeschlossen“

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Versionen** die Version der Funktion für die elektronische Rechnungsstellung mit dem Status **Entwurf** aus.
2. Wählen Sie **Status ändern \>Abschließen** aus. 

### <a name="change-the-version-status-to-published"></a>Ändern des Versionsstatus in „Veröffentlicht“ 

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Versionen** die Version der Funktion für die elektronische Rechnungsstellung mit dem Status **Abgeschlossen** aus.
2. Wählen Sie **Status ändern \> Veröffentlichen** aus.

![Ändern des Status der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a>Einrichten der Integration des Add-Ons für die elektronische Rechnungsstellung in Finance

Während der Einrichtung von Finance führen Sie folgende Aufgaben aus:

1. Importieren Sie das EB-Datenmodell, die EB-Datenmodellzuordnung und die Kontextkonfigurationen für elektronische Rechnungen im FatturaPA-Format.
2. Konfigurieren Sie das Zertifikat, das zum digitalen Signieren elektronischer Rechnungen in Italien erforderlich ist.

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a>Importieren des EB-Datenmodells, der Datenmodellzuordnung und der Formate

1. Überprüfen Sie im Arbeitsbereich **Elektronische Berichterstellung**, ob der Konfigurationsanbieter **Geschäftsdokumentservice** auf **Aktiv** festgelegt ist.
2. Wählen Sie **Repositorys** aus.
3. Wählen Sie **Globale Ressource \> Öffnen** aus.
4. Importieren Sie **Rechnungsmodell**, **Rechnungsmodellzuordnung** und **Kontextmodell Debitorenrechnung**.

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a>Aktivieren der Funktion zum Exportieren von elektronischen Kundenrechnungen für Italien

1. Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.
2. Aktivieren Sie auf der Registerkarte **Funktionen** das Kontrollkästchen **Aktivieren** in der Zeile für Funktionsreferenz **IT00036**.

![Aktivieren der FatturaPA-Funktion](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a>Konfigurieren elektronischer Dokumente

1. Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.
2. Wählen Sie auf der Registerkarte **Elektronisches Dokument** die Option **Hinzufügen** aus und geben Sie die Tabellen ein, die zum Generieren elektronischer Rechnungen in Italien erforderlich sind:

    - **Tabellenname:** Debitorenrechnungserfassung
    - **Tabellenname:** Projektrechnung

3. Definieren Sie für jede Tabelle einen zugehörigen Dokumentkontext:

    - Wählen Sie für **Debitorenrechnungserfassung** die Option **Kontext Debitorenrechnung** aus.
    - Wählen Sie für **Projektrechnung** die Option **Kontext Projektrechnung** aus.

![Einrichten von Antworttypen](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a>Verarbeitung der elektronischen Rechnung

Während der Verarbeitung in Finance führen Sie folgende Aufgaben aus:

1. Generieren elektronischer Rechnungen in Italien über das Add-On für die elektronische Rechnungsstellung
2. Anzeigen der Ausführungsprotokolle und Überprüfen der Ergebnisse der Verarbeitung

### <a name="generate-electronic-invoices"></a>Generieren elektronischer Rechnungen

Nachdem Sie die Funktion **Integration des konfigurierbaren Add-Ons für die elektronische Rechnungsstellung** und die Funktion **IT00036** aktiviert haben, kann der alte Prozess von Finance zum Generieren elektronischer Rechnungen in Italien nicht mehr verwendet werden. Er wird durch einen neuen Prozess mit dem Namen **Elektronische Dokumente übermitteln** ersetzt.

Sie können die Dokumente manuell übermitteln, basierend auf Ihrer Nachfrage nach elektronischen Rechnungsdokumenten.

> [!NOTE]
> Bevor Sie fortfahren, stellen Sie sicher, dass die für elektronische Rechnungen in Italien erforderliche Einrichtung abgeschlossen wurde. Weitere Informationen finden Sie unter [Elektronische Rechnungen für Kunden](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices). Beachten Sie, dass einige der in diesem Thema beschriebenen Einrichtungsschritte aufgrund der Aktivierung des Add-Ons für die elektronische Rechnungsstellung möglicherweise nicht verfügbar sind.

1. Navigieren Sie zu **Organisationsverwaltung \> Periodisch \> Elektronische Dokumente \> Elektronische Dokumente übermitteln**.
2. Legen Sie für die erste Übermittlung irgendeines Dokuments die Option **Dokumente erneut übermitteln** auf **Nein** fest. Wenn Sie ein Dokument erneut über den Service übermitteln müssen, legen Sie diese Option auf **Ja** fest.
3. Wählen Sie auf dem Inforegister **Einzuschließende Datensätze** die Option **Filtern** aus, um das Dialogfeld **Anfrage** zu öffnen, in dem Sie eine Abfrage erstellen können, um Dokumente für die Übermittlung auszuwählen.

![Dialogfeld „Elektronische Dokumente übermitteln“](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a>Filterabfrage

1. Konfigurieren Sie im Dialogfeld **Anfrage** die Filterbedingungen für Verkaufs- und Projektrechnungen oder lassen Sie die Bedingungen leer, um alle nicht übermittelten Rechnungen einzuschließen.

    ![Einrichten von Filterkriterien für Übermittlungen](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. Wählen Sie **OK** aus, um das Dialogfeld **Anfrage** zu schließen.
3. Wählen Sie **OK** aus, um die ausgewählten Dokumente zu übermitteln.

> ! [HINWEIS] Bei Ihrem ersten Versuch, ein Dokument über den Service zu übermitteln, werden Sie aufgefordert, die Verbindung mit dem Add-On für die elektronische Rechnungsstellung zu bestätigen. Wählen Sie **Hier klicken, um eine Verbindung mit dem Electronic Document Submission Service herzustellen** aus.

#### <a name="view-submission-logs"></a>Anzeigen von Übermittlungsprotokollen

Sie können die Übermittlungsprotokolle für alle übermittelten Dokumente anzeigen.

1. Navigieren Sie zu **Organisationsverwaltung \> Periodisch \> Elektronische Dokumente \> Übermittlungsprotokoll für elektronische Dokumente**.
2. Wählen Sie im Feld **Dokumenttyp** entweder **Debitorenrechnungserfassung** oder **Projektrechnung** aus, um nach den erforderlichen elektronischen Dokumenten zu filtern.

    ![Auswählen eines Dokumenttyps, um die Übermittlungsprotokolle anzuzeigen](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    Der Wert, der in der Spalte **Übermittlungsstatus** angezeigt wird, gibt den Status des Übermittlungsprozesses an. Er zeigt an, ob der Prozess wie konfiguriert ausgeführt wurde und ob zusätzliche Aktionen erforderlich sind.

3. Wählen Sie im Aktivitätsbereich die Option **Anfragen \> Übermittlungsdetails** aus, um die Details der Ausführungsprotokolle für die Übermittlung anzuzeigen.

    ![Anzeigen der Details des Übermittlungsprotokolls](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. Auf dem Inforegister **Verarbeitungsaktivitäten** können Sie das Ausführungsprotokoll für die Aktionen anzeigen, die in der in RCS eingerichteten Funktionsversion konfiguriert sind. Die Spalte **Status** zeigt an, ob die Aktion erfolgreich ausgeführt wurde.
5. Auf dem Inforegister **Aktionsdateien** können Sie die Zwischendateien anzeigen, die während der Ausführung der Aktionen generiert wurden. Sie können **Anzeigen** auswählen, um die ausgegebene-XML-Datei im Format **FatturaPA** herunterzuladen und ihren Inhalt anzuzeigen.

## <a name="related-topics"></a>Verwandte Themen

- [Übersicht über das Add-On für die elektronische Rechnungsstellung](e-invoicing-service-overview.md)
- [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung](e-invoicing-get-started.md)
- [Einrichten des Add-Ons für die elektronische Rechnungsstellung](e-invoicing-setup.md)
