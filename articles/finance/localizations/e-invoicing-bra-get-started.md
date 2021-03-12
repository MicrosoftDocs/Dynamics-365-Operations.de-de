---
title: Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Brasilien
description: Dieses Thema enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung für Brasilien in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management erleichtern.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 0320bd1d9e93cc30ed75f28e387ac2ec8dbfc226
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962833"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Brasilien 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Das Add-On für die elektronische Rechnungsstellung für Brasilien unterstützt derzeit nicht alle Funktionen, die in der Integration von Steuerdokumenten, die in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management integriert ist, verfügbar sind.

Dieses Thema enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung für Brasilien erleichtern. Es führt Sie durch die Konfigurationsschritte, die in Regulatory Configuration Services (RCS) sowie in Finance und Supply Chain Management länderabhängig sind. Außerdem werden Sie durch den Prozess der Übermittlung eines NF-e-Steuerdokuments (elektronisches Steuerdokumentmodell 55) über den Dienst geführt und es wird erläutert, wie die Verarbeitungsergebnisse und der Status der Steuerdokumente überprüft werden.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Schritte in diesem Thema ausführen, müssen Sie die Schritte in [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung](e-invoicing-get-started.md) ausführen.

## <a name="rcs-setup"></a>RCS-Einstellungen

Während der RCS-Einrichtung führen Sie folgende Aufgaben aus:

1. Importieren Sie die Funktion für die elektronische Rechnungsstellung für NF-e-Steuerdokumente.
2. Überprüfen Sie die Dateiformate, die erforderlich sind, um NF-e-Steuerdokumente zur Autorisierung zu übermitteln.
3. Überprüfen Sie die Dateiformate, die erforderlich sind, um die Stornierung eines genehmigten NF-e zu beantragen.
4. Konfigurieren Sie das Ereignis, das erforderlich ist, um NF-e-Steuerdokumente zur Autorisierung zu übermitteln.
5. Konfigurieren Sie das Ereignis, das erforderlich ist, um die Stornierung eines genehmigten NF-e zu beantragen.
6. Weisen Sie die Funktion für die elektronische Rechnungsstellung einer Add-On-Umgebung für die elektronische Rechnungsstellung zu.
7. Veröffentlichen Sie die Funktion für die elektronische Rechnungsstellung.

> [!NOTE]
> „Die Funktion für die elektronische Rechnungsstellung“ ist der generische Name für die Ressource, die so konfiguriert und veröffentlicht ist, dass sie den Add-On-Server für die elektronische Rechnungsstellung verwendet. Das Einrichten der Funktion für die elektronische Rechnungsstellung umfasst unter anderem die Verwendung von Konfigurationsformaten der elektronischen Berichterstellung (EB) zum Erstellen konfigurierbarer Export- und Importdateien sowie die Verwendung von Aktionen und Aktionsabläufen, um die Erstellung konfigurierbarer Regeln zum Senden von Anforderungen, zum Importieren von Antworten und zum Analysieren des Inhalts der Antworten zu ermöglichen.

## <a name="import-the-e-invoicing-feature"></a>Importieren der Funktion für die elektronische Rechnungsstellung

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktionen** im Abschnitt **Funktionen** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** die Option **Importieren** aus, um eine Funktion für die elektronische Rechnungsstellung für NF-e-Steuerdokumente aus dem globalen Repository zu importieren.

    ![Schaltfläche „Importieren“](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. Wählen Sie die Funktion für NF-e-Steuerdokumente aus und wählen Sie dann **Importieren** aus.

    ![Importieren der Funktion für NF-e](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a>Erstellen Sie eine neue Version der Funktion für NF-e-Steuerdokumente

- Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Versionen** die Option **Neu** aus.

![Hinzufügen einer neuen Version der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a>Aktualisieren der Konfigurationsversion

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Konfigurationen** entweder **Hinzufügen** oder **Löschen** aus, um die Konfigurationsversionen (EB-Dateiformatkonfigurationen) zu verwalten.

    ![Verwalten der Konfigurationen der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - Wenn Sie eine neue Version der Funktion für NF-e-Steuerdokumente erstellen, werden alle Konfigurationsversionen (EB-Dateiformate) von der neuesten Version geerbt.
    - Um das NF-e-Steuerdokument zur Autorisierung zu übermitteln, sind die folgenden Konfigurationsversionen erforderlich:

        - Exportformat zur Übermittlung von NFe
        - Import der NFe-Antwortnachricht
        - Import des NFe-Fehlerprotokolls

    - Um die NF-e-Stornierung zu übermitteln, ist die folgende Konfigurationsversion erforderlich:

        - Exportformat zur Stornierung von NFe

2. Wählen Sie in der Liste eine Konfigurationsversion aus und wählen Sie dann **Bearbeiten** oder **Anzeigen** aus, um die Seite **Formatdesigner** zu öffnen, auf der Sie die Konfiguration bearbeiten oder anzeigen können.

    ![Öffnen der Seite „Formatdesigner“](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. Verwenden Sie die Seite **Formatdesigner**, um die EB-Formatkonfigurationen für Dateien zu bearbeiten oder anzuzeigen. Weitere Informationen finden Sie unter [Erstellen elektronischer Berichterstellungskonfigurationen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Formatdesignerseite](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a>Verwalten der Einrichtungen der Funktion für die elektronische Rechnungsstellung

- Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Einrichtungen** entweder **Hinzufügen** oder **Löschen** aus, um die Einrichtungen (d. h. NF-e-Ereignisse) der Funktion für die elektronische Rechnungsstellung zu verwalten.

![Verwalten der Einrichtungen der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

Wenn Sie eine neue Version der Funktion für NF-e-Steuerdokumente erstellen, die von einer anderen Funktion für die elektronische Rechnungsstellung abgeleitet ist, werden alle Funktionseinrichtungen (NF-e-Ereignisse) von der neuesten Version geerbt.

Um NF-e-Steuerdokumente zur Autorisierung zu übermitteln, ist die Funktionseinrichtung **Übermitteln** erforderlich.

Um die NF-e-Stornierung zu übermitteln, ist die Funktionseinrichtung **Stornierung** erforderlich.

#### <a name="configure-the-submit-feature-setup"></a>Konfigurieren der Funktionseinrichtung „Übermitteln“

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Einrichtungen** in der Spalte **Funktionseinrichtung** die Option **Übermitteln** aus.
2. Wählen Sie **Bearbeiten** aus.

    ![Bearbeiten der Einrichtung für die Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. Wählen Sie auf der Seite **Einrichtung der Funktionsversion** die Registerkarte **Aktionen** aus, um die Liste der Aktionen zu verwalten.

    ![Registerkarte „Aktionen“](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. Überprüfen Sie die Aktionen, die erforderlich sind, um ein NF-e zur Autorisierung zu übermitteln.

    | Aktivitätskennung | Aktivitätsname                  | Aktivitätsbeschreibung                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | 1         | Umwandeln des Dokuments           | Erstellen Sie die NF-e-XML-Datei zur Übermittlung.                          |
    | 2         | Dokument signieren                | Wenden Sie das digitale Zertifikat auf die XML-Datei an.                    |
    | 3         | Aufrufen des brasilianischen SEFAZ-Dienstes | Übermitteln Sie die signierte XML-Datei zur Autorisierung an die Webdienste. |
    | 4         | Verarbeiten der Antwort             | Rufen Sie die Antwort des Webdienstes ab.                                     |
    | 5         | Umwandeln des Dokuments           | Analysieren Sie den Inhalt der Datei, die Sie als Antwort erhalten.     |
    | 6         | Umwandeln des Dokuments           | Erstellen Sie die XML-Datei, um den Status der Übermittlung abzufragen.    |
    | 7         | Aufrufen des brasilianischen SEFAZ-Dienstes | Übermitteln Sie die XML-Datei, die den Übermittlungsstatus anfordert.          |
    | 8         | Verarbeiten der Antwort             | Rufen Sie die Antwort des Webdienstes ab.                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Einrichten der URL für SEFAZ-Webdienste 

1. Wählen Sie auf der Seite **Einrichtung der Funktionsversion** auf der Registerkarte **Aktionen** auf dem Inforegister **Aktionen** die Option **Aufrufen des brasilianischen SEFAZ-Dienstes** (Aktions-ID **3**) aus.
2. Geben Sie auf dem Inforegister **Parameter** in das Feld **Parameter der URL-Adresse** die URL des SEFAZ-Webdienstes für die NF-e-Übermittlung ein.
3. Wählen Sie auf dem Inforegister **Aktionen** die Option **Aufrufen des brasilianischen SEFAZ-Dienstes** aus (Aktions-ID **7**).
4. Geben Sie auf dem Inforegister **Parameter** in das Feld **Parameter der URL-Adresse** die URL des SEFAZ-Webdienstes für die NF-e-Übermittlung ein.

#### <a name="configure-the-cancellation-feature-setup"></a>Konfigurieren der Funktionseinrichtung „Stornierung“

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Einrichtungen** in der Spalte **Funktionseinrichtung** die Option **Stornierung** aus.
2. Wählen Sie **Bearbeiten** aus.
3. Wählen Sie auf der Seite **Einrichtung der Funktionsversion** die Registerkarte **Aktionen** aus, um die Liste der Aktionen zu verwalten.
4. Überprüfen Sie die Aktionen, die erforderlich sind, um die Stornierung eines genehmigten NF-e zu beantragen.

    | Aktivitätskennung | Aktivitätsname                  | Aktivitätsbeschreibung                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | 1         | Umwandeln des Dokuments           | Erstellen Sie für die NF-e-Stornierung die XML-Datei zur Übermittlung.            |
    | 2         | Dokument signieren                | Wenden Sie das digitale Zertifikat auf die XML-Datei an.                   |
    | 3         | Aufrufen des brasilianischen SEFAZ-Dienstes | Übermitteln Sie die signierte XML-Datei zur Stornierung an die Webdienste. |
    | 4         | Verarbeiten der Antwort             | Rufen Sie die Antwort des Webdienstes ab.                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Einrichten der URL für SEFAZ-Webdienste

1. Wählen Sie auf der Seite **Einrichtung der Funktionsversion** auf der Registerkarte **Aktionen** auf dem Inforegister **Aktionen** die Option **Aufrufen des brasilianischen SEFAZ-Dienstes** (Aktions-ID **3**) aus.
2. Geben Sie auf dem Inforegister **Parameter** in das Feld **Parameter der URL-Adresse** die URL des SEFAZ-Webdienstes für die Stornierung einer genehmigten NF-e ein.

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a>Bereitstellen einer Umgebung für die elektronische Rechnungsstellung und Zuweisen einer Entwurfsversion

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Umgebungen** die Option **Aktivieren** aus.
2. Wählen Sie im Feld **Umgebung** die Umgebung aus.
3. Wählen Sie im Feld **Gültig ab** das Datum aus, an dem die Umgebung wirksam werden soll.
4. Wählen Sie **Aktivieren** aus.

![Aktivieren einer Umgebung für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a>Ändern Sie den Status in „Abgeschlossen“.

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Versionen** die Version der Funktion für die elektronische Rechnungsstellung mit dem Status **Entwurf** aus.
2. Wählen Sie **Status ändern \>Abschließen** aus.

### <a name="change-the-status-to-publish"></a>Ändern Sie den Status in „Veröffentlichen“.

1. Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Versionen** die Version der Funktion für die elektronische Rechnungsstellung mit dem Status **Abgeschlossen** aus.
2. Wählen Sie **Status ändern \> Veröffentlichen** aus.

![Veröffentlichen der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Einrichten der Add-On-Integration für die elektronische Rechnungsstellung in Finance oder Supply Chain Management

Während dem Einrichten führen Sie folgende Aufgaben aus:

1. Aktivieren Sie die NF-e-Funktion für Brasilien.
2. Importieren Sie das spezifische EB-Datenmodell, die Datenmodellzuordnung und die Formate, die für NF-e-Steuerdokumente erforderlich sind.
3. Importieren Sie die BR-Konfiguration und richten Sie die Antworttypen ein, die erforderlich sind, um den Status des Steuerdokuments zu aktualisieren, nachdem der Übermittlungsprozess zurückgegeben wurde.

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a>Aktivieren der NF-e-Funktion für Brasilien.

1. Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.
2. Aktivieren Sie auf der Registerkarte **Funktionen** das Kontrollkästchen **Aktivieren** in der Zeile für Funktionsreferenz **BR00053**.

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a>Importieren der für NF-e-Steuerdokumente erforderlichen EB-Datenmodellzuordnung

1. Melden Sie sich bei Finance an.
2. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Konfigurationsanbieter** die Kachel **Microsoft** aus. Stellen Sie sicher, dass dieser Konfigurationsanbieter auf **Aktiv** festgelegt ist. Weitere Informationen zum Festlegen eines Anbieters auf **Aktiv** finden Sie unter [Erstellen von Konfigurationsanbietern und Markieren als aktiv](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Wählen Sie **Repositorys** aus.
4. Wählen Sie **Globale Ressource \> Öffnen** aus.
5. Importieren Sie die Konfigurationen **Zuordnung von Steuerdokumenten**.

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a>Importieren der EB-Konfigurationen und Einrichten der Antworttypen für Steuerdokumente

1. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Konfigurationsanbieter** die Kachel **Microsoft** aus.
2. Wählen Sie **Repositorys** aus.
3. Wählen Sie **Globale Ressource \> Öffnen** aus.
4. Importieren Sie **Import des NFe-Fehlerprotokolls (BR)**, **Importformat für NF-e-Antwortdaten (BR)** und **Import von NF-e-Antwortnachrichten (BR)**.
5. Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.
6. Wählen Sie auf der Registerkarte **Elektronisches Dokument** die Option **Hinzufügen** aus.
6. Wählen Sie im Feld **Tabellenname** die Option **Steuerdokumentkopf** aus.
7. Wählen Sie im Feld **Dokumentkontext** die Option **Kontextmodell Debitorenrechnung – Steuerdokumentkontext**.
8. Wählen Sie **Antworttypen** aus.
9. Wählen Sie **Neu** aus und wählen Sie anschließend im Feld **Antworttyp** die Option **Antwort** aus.
10. Wählen Sie im Feld **Übermittlungsstatus** die Option **Ausstehend** aus.
11. Wählen Sie im Feld **Modellzuordnung** die Option **Importformat für Antwortnachrichten – Modellzuordnung aus Antwortnachricht** aus.
12. Wählen Sie **Speichern** aus.
13. Wählen Sie **Neu** und anschließend im Feld **Antworttyp** die Option **Antwortdaten** aus.
14. Wählen Sie im Feld **Übermittlungsstatus** die Option **Ausstehend** aus.
15. Wählen Sie im Feld **Modellzuordnung** die Option **Importformat für NFe-Antwortdaten – Import von Antwortdaten** aus.
16. Wählen Sie **Speichern** aus.

## <a name="electronic-invoice-processing"></a>Verarbeitung der elektronischen Rechnung

Während der Verarbeitung in Finance führen Sie folgende Aufgaben aus:

1. Übermitteln Sie ein Steuerdokument über das Add-On für die elektronische Rechnungsstellung.
2. Zeigen Sie die Ausführungsprotokolle für die Übermittlung an und überprüfen Sie die Ergebnisse der Verarbeitung.
3. Übermitteln Sie die Stornierung eines Steuerdokuments über das Add-On für die elektronische Rechnungsstellung.

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a>Übermitteln von NF-e-Steuerdokumenten zur Autorisierung durch die SEFAZ 

Nachdem Sie die Funktion **Integration des konfigurierbaren Add-Ons für die elektronische Rechnungsstellung** aktiviert haben, kann der alte Prozess zum Übermitteln von NF-e-Steuerdokumenten zur Autorisierung (**Exportieren/Importieren des NF-e-Prozesses**) nicht mehr verwendet werden. Er wird durch einen neuen Prozess mit dem Namen **Elektronische Dokumente übermitteln** ersetzt.

> [!NOTE]
> Stellen Sie vor dem Fortfahren sicher, dass Sie über ein oder mehrere Kundensteuerdokumente Modell 55 verfügen, die von der Steuerbehörde des Kunden ausgestellt wurden. Die Richtung für diese Steuerdokumente muss auf **Ausgehend** festgelegt werden und der Status muss **Erstellt** lauten. Weitere Informationen finden Sie unter [Steuerdokumente für Debitoren ausstellen (Brasilien)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).

1. Navigieren Sie zu **Organisationsverwaltung \> Periodisch \> Elektronische Dokumente \> Elektronische Dokumente übermitteln**.
2. Legen Sie für die erste Übermittlung irgendeines Dokuments immer die Option **Dokumente erneut übermitteln** auf **Nein** fest. Wenn Sie ein Dokument erneut über den Service übermitteln müssen, legen Sie diese Option auf **Ja** fest.
3. Wählen Sie auf dem Inforegister **Einzuschließende Datensätze** die Option **Filtern** aus, um das Dialogfeld **Anfrage** zu öffnen, in dem Sie eine Abfrage erstellen können, um Dokumente für die Übermittlung auszuwählen.
4. Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen** aus.
5. Wählen Sie im Feld **Tabelle** die Option **Steuerdokumentkopf** aus.
6. Wählen Sie im Feld **Abgeleitete Tabelle** die Option **Steuerdokumentkopf** aus.
6. Wählen Sie im Feld **Feld** die Option **Nummer** aus.
7. Geben Sie in das Feld **Kriterien** die Nummer des Steuerdokuments ein, das übermittelt werden soll.
8. Wählen Sie **OK** aus, um das Dialogfeld **Anfrage** zu schließen.
8. Wählen Sie **OK** aus, um die ausgewählten Dokumente zu übermitteln.

> [!NOTE]
> Bei Ihrem ersten Versuch, ein Dokument über den Service zu übermitteln, werden Sie aufgefordert, die Verbindung mit dem Add-On für die elektronische Rechnungsstellung zu bestätigen. Wählen Sie **Hier klicken, um eine Verbindung mit dem Electronic Document Submission Service herzustellen** aus.

### <a name="view-all-submission-logs"></a>Anzeigen aller Übermittlungsprotokolle

Nach dem Aktivieren der Funktion **Integration des konfigurierbaren Add-Ons für die elektronische Rechnungsstellung** ist eine neue Seite verfügbar, über die Sie den Übermittlungsprozess für das Dokument nachverfolgen können. Sie können diese Seite verwenden, um die Übermittlungsprotokolle für alle übermittelten Dokumente anzuzeigen.

1. Navigieren Sie zu **Organisationsverwaltung \> Periodisch \> Elektronische Dokumente \> Übermittlungsprotokoll für elektronische Dokumente**.
2. Wählen Sie im Fenster **Dokumenttyp** die Option **Steuerdokumentkopf** aus, um eine Filterung nur nach Steuerdokumenten durchzuführen.
3. Wählen Sie im Aktivitätsbereich die Option **Anfragen \> Übermittlungsdetails** aus, um die Details der Ausführungsprotokolle für die Übermittlung anzuzeigen.

![Anzeigen der Details des Übermittlungsprotokolls](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> Für NF-e-Steuerdokumente zeigt die Spalte **Fehlercode** den Rückgabecode an, der von den SEFAZ-Webdiensten zurückgegeben wurde.

### <a name="view-submission-logs-through-the-fiscal-document-page"></a>Anzeigen von Übermittlungsprotokollen über die Steuerdokumentseite

Nach dem Aktivieren der Funktion **Integration des konfigurierbaren Add-Ons für die elektronische Rechnungsstellung** können Sie die Übermittlungsprotokolle auch über die Steuerdokumentseite anzeigen.

1. Wechseln Sie zu **Hauptbuch \> Anfragen und Berichte \> Steuerdokumente \> Alle Steuerdokumente**.
2. Wählen Sie ein Steuerdokument aus, das zuvor über das Add-On für die elektronische Rechnungsstellung übermittelt wurde.
3. Wählen Sie im Aktivitätsbereich auf der Registerkarte **NF-e** die Option **Elektronisches Dokumentenprotokoll** aus.

![Anzeigen von Übermittlungsprotokollen über die Steuerdokumentseite](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a>Übermitteln von genehmigten NF-e-Steuerdokumenten zur Stornierung durch die SEFAZ

Nachdem Sie die Funktion **Integration des konfigurierbaren Add-Ons für die elektronische Rechnungsstellung** aktiviert haben, kann der alte Prozess zum Stornieren von NF-e-Steuerdokumenten nicht mehr verwendet werden. Er wird durch einen neuen Stornierungsprozess ersetzt, der in die Seite **Übermittlungsprotokoll für elektronische Dokumente** eingebettet ist.

> [!NOTE]
> Stellen Sie sicher, dass Sie die Stornierung des Steuerdokuments für Debitoren für ein genehmigtes NF-e-Steuerdokument ausgeführt haben. Weitere Informationen finden Sie unter [Steuerdokumente für Debitoren stornieren (Brasilien)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).

1. Navigieren Sie zu **Organisationsverwaltung \> Periodisch \> Elektronische Dokumente \> Übermittlungsprotokoll für elektronische Dokumente**.
2. Wählen Sie das Steuerdokument aus und wählen Sie dann **Funktionen \> Zugehörige Übermittlungen senden** aus.
3. Geben Sie eine Beschreibung für die zugehörige Übermittlung ein und wählen Sie dann **OK** aus.

### <a name="view-cancellation-submission-logs"></a>Anzeigen von Übermittlungsprotokollen zu Stornierungen

1. Navigieren Sie zu **Organisationsverwaltung \> Periodisch \> Elektronische Dokumente \> Übermittlungsprotokoll für elektronische Dokumente**.
2. Wählen Sie im Fenster **Dokumenttyp** die Option **Steuerdokumentkopf** aus, um eine Filterung nur nach Steuerdokumenten durchzuführen.
3. Wählen Sie das Steuerdokument aus und wählen Sie dann im Aktivitätsbereich **Anfragen \> Zugehörige Übermittlungen** aus.

    Zugehörige Übermittlungen sind Übermittlungen, die zu einer zuerst übermittelten Hauptübermittlung gehören. Beispielsweise ist die Übermittlung, die eine bestimmte NF-e autorisiert, die Hauptübermittlung. Die Übermittlung, die die Stornierung derselben NF-e bei der SEFAZ beantragt, ist eine zugehörige Übermittlung. Sie existiert nur, weil sie die Stornierung des Vorgangs anfordert, der durch eine andere Übermittlung ausgeführt wurde.

    Die Seite **Zugehörige Übermittlungen** zeigt alle zugehörigen Übermittlungen und ihren Übermittlungsstatus für ein bestimmtes Steuerdokument an. In der folgenden Abbildung stellt die erste Zeile die Übermittlung dar, die die Genehmigung des Steuerdokuments beantragt hat. Die zweite Zeile stellt die Übermittlung dar, mit der dieses Steuerdokument storniert wurde.

    ![Anzeigen der Übermittlungsprotokolle zu Stornierungen](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. Wählen Sie im Aktivitätsbereich die Option **Anfragen \> Übermittlungsdetails** aus, um die Details der Ausführungsprotokolle für die Übermittlung anzuzeigen.

    ![Anzeigen der Details des Übermittlungsprotokolls zu Stornierungen](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a>Datenschutzhinweis
Für die Aktivierung der Funktion „BR-00053 (NF-e)“ müssen möglicherweise nur begrenzte Daten gesendet werden, einschließlich der Steuerregistrierungskennung für die Organisation. Diese Daten werden an von der Steuerbehörde autorisierte Drittagenturen weitergeleitet, um elektronische Rechnungen in dem für die Integration in den Webdienst der Behörde erforderlichen Format an diese Steuerbehörde zu senden. Ein Administrator kann die Funktion „BR-00053 (NF-e)“ aktivieren und deaktivieren, indem er zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente** navigiert. Wählen Sie auf der Registerkarte **Funktionen** die Zeile mit der Funktion „BR-00053“ aus und treffen Sie die entsprechende Auswahl. Daten, die aus diesen externen Systemen in diesen Dynamics 365-Onlinedienst importiert werden, unterliegen unseren [Datenschutzbestimmungen](https://go.microsoft.com/fwlink/?LinkId=512132). Weitere Informationen finden Sie in den Abschnitten zum Datenschutz in der landesspezifischen Funktionsdokumentation.


## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Übersicht über das Add-On für die elektronische Rechnungsstellung](e-invoicing-service-overview.md)
- [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung](e-invoicing-get-started.md)
- [Einrichten des Add-Ons für die elektronische Rechnungsstellung](e-invoicing-setup.md)
