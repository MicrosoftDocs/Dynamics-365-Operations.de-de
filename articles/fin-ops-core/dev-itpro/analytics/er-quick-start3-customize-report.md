---
title: Passen Sie die Konfigurationen für elektronische Berichte an, um ein elektronisches Dokument zu erstellen
description: In diesem Thema wird erläutert, wie Sie ein von Microsoft bereitgestelltes EB-Format (Elektronische Berichterstellung) anpassen, so dass ein benutzerdefiniertes elektronisches Dokument generiert wird.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c8cf4866b6a8c239359d726d8cd4f03a9eb4137
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2022
ms.locfileid: "8324086"
---
# <a name="customize-electronic-reporting-configurations-to-generate-an-electronic-document"></a>Passen Sie die Konfigurationen für elektronische Berichte an, um ein elektronisches Dokument zu erstellen

[!include[banner](../includes/banner.md)]

Der [Framework für die elektronische Berichterstattung (EB)](general-electronic-reporting.md) Mit dieser Option können Sie die EB [Konfigurationen](general-electronic-reporting.md#Configuration) hochladen, die in Ihrer Microsoft Dynamics 365 Finance Instanz bereitgestellt wird. Auf diese Weise können die von Microsoft bereitgestellten Konfigurationen als EB-Lösung dienen, mit der elektronische Kundenrechnungen (E-Rechnungen) erstellt werden. Mit dieser EB-Lösung können Sie Ihre benutzerdefinierte EB-Lösung für den Zugriff auf Ihre benutzerdefinierten Datenbankfelder konfigurieren und E-Rechnungen erstellen, die Ihren spezifischen Anforderungen entsprechen, ohne den Quellcode bearbeiten zu müssen.

## <a name="overview"></a>Übersicht

Für das Beispiel in diesem Thema müssen Sie einen Bundessteueridentifikationscode als neues benutzerdefiniertes Attribut für jeden Kunden angeben, den Sie elektronisch in Rechnung stellen. Daher müssen Sie die Struktur der aktuell verwendeten Rechnung anpassen, indem Sie in jeder generierten E-Rechnung einen neuen Artikel hinzufügen, der mit dem Steuerkennzeichen gefüllt werden muss.

Die Prozeduren in diesem Thema erläutern, wie ein Benutzer mit der Rolle Systemadministrator, Entwickler für die elektronische Berichterstattung oder funktionaler Berater für die elektronische Berichterstellung die folgenden Aufgaben ausführen kann:

- [Konfigurieren Sie den minimalen Satz von EB-Parametern, der erforderlich ist, um das EB-Framework zu verwenden](#ConfigureER).
- [Importieren Sie die ersten Versionen der Standard-EB-Konfigurationen, die zum Generieren von E-Rechnungen bereitgestellt werden](#ImportERConfigurations1).
- [Konfigurieren Sie die Debitorenparameter so, dass die Standard-ER-Konfigurationen verwendet werden](#ConfigureAR1).
- [Konfigurieren Sie die Parameter der juristischen Person, um Kunden Rechnung zu stellen](#ConfigureLE).
- [Bereiten Sie einen Kundendatensatz für die elektronische Rechnungsstellung vor](#ConfigureCustomer1).
- [Hinzufügen, Buchen und Senden einer Kundenrechnung mithilfe der Standard-EB-Konfigurationen](#ProcessInvoice1).
- [Fügen Sie ein benutzerdefiniertes Datenbankfeld hinzu, um einen Steueridentifikationscode für Kunden zu verwalten](#AddCustomField).
- [Aktualisieren Sie die EB-Metadaten, um Datenbankänderungen für den EB-Modellzuordnungsdesigner zu aktivieren](#RefreshERMetadata).
- [Entwerfen Sie die benutzerdefinierten EB-Konfigurationen, um E-Rechnungen zu generieren, die das neue Steuerkennzeichen enthalten](#DesignCustomERConfigurations).
- [Konfigurieren Sie die Debitorenparameter so, dass die benutzerdefinierten EB-Konfigurationen verwendet werden](#ConfigureAR2).
- [Aktualisieren Sie einen Kundendatensatz für die elektronische Rechnungsstellung](#ConfigureCustomer2).
- [Hinzufügen, Buchen und Senden einer Kundenrechnung mithilfe der benutzerdefinierten-EB-Konfigurationen](#ProcessInvoice2).
- [Importieren Sie die neuen Versionen der Standard-EB-Konfigurationen, die zum Generieren von E-Rechnungen bereitgestellt werden](#ImportERConfigurations2).
- [Übernehmen Sie die Änderungen an den neuen Versionen der Standard-EB-Konfigurationen in Ihre benutzerdefinierten EB-Konfigurationen](#RebaseCustomERConfigurations).
- [Hinzufügen, Buchen und Senden einer Kundenrechnung mithilfe der neuen Versionen der benutzerdefinierten-EB-Konfigurationen](#ProcessInvoice3).

Alle diese Prozeduren können im Unternehmen **DEMF** ausgeführt werden.

## <a name="configure-the-er-framework"></a><a name="ConfigureER"></a>Konfigurieren des EB-Frameworks

Als Benutzer in der Rolle des Electronic Reporting Functional Consultant oder des Electronic Reporting Developer müssen Sie den minimalen Satz von EB-Parametern konfigurieren. Anschließend können Sie das EB-Framework verwenden, um benutzerdefinierte Versionen der Standardkonfigurationen der EB-Lösung zu entwerfen, mit denen E-Rechnungen erstellt werden.

### <a name="configure-er-parameters"></a>Parameter der elektronischen Berichterstellung konfigurieren

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Parameter für elektronische Berichterstellung** aus.
3. Auf der Seite **Parameter für elektronische Berichterstellung** legen Sie auf der Registerkarte **Allgemein** die Option **Entwurfsmodus aktivieren** auf **Ja** fest.
4. Auf der **Anhänge** Registerkarte im Feld **Konfigurationen** wählen Sie **Datei** aus.
5. Wählen Sie in den Feldern **Einzelvorgangsarchiv**, **Temporär**, **Grundlage** und **Andere** den **Dateityp** aus.

Weitere Informationen zu EB-Parametern finden Sie unter [Konfigurieren des EB-Frameworks](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a>Aktivieren eines EB-Konfigurationsanbieters

Jede hinzugefügte EB-Konfiguration wird als Eigentum eines EB-Konfigurationsanbieters markiert. Der EB-Konfigurationsanbieter, der im Arbeitsbereich **Elektronische Berichterstellung** aktiviert ist, wird zu diesem Zweck verwendet. Daher müssen Sie im Arbeitsbereich **Elektronische Berichterstellung** einen EB-Konfigurationsanbieter aktivieren, bevor Sie mit dem Hinzufügen oder Bearbeiten von EB-Konfigurationen beginnen.

> [!NOTE]
> Nur der Besitzer einer EB-Konfiguration kann diese bearbeiten. Daher muss im Arbeitsbereich **Elektronische Berichterstellung** der entsprechende EB-Konfigurationsanbieter aktiviert werden, bevor eine EB-Konfigurationen bearbeitet werden kann.

#### <a name="review-the-list-of-er-configuration-providers"></a>Überprüfen der Liste der EB-Konfigurationsanbieter

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Konfigurationsanbieter** aus.
3. Auf der Seite **Konfigurationsanbietertabelle** hat jeder Anbieterdatensatz einen eindeutigen Namen und eine eindeutige URL. Überprüfen Sie den Inhalt dieser Seite. Wenn bereits ein Datensatz für **Litware, Inc.** (`https://www.litware.com`) vorhanden ist, überspringen Sie die nächste Prozedur [Hinzufügen eines neuen EB-Konfigurationsanbieters](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Hinzufügen eines neuen EB-Konfigurationsanbieters

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Konfigurationsanbieter** aus.
3. Wählen Sie auf der Seite **Konfigurationsanbieter** die Option **Neu** aus.
4. Geben Sie im Feld **Name** **Litware, Inc.** ein.
5. Geben Sie im Feld **Internetadresse** `https://www.litware.com` ein.
6. Wählen Sie **Speichern** aus.

#### <a name="activate-an-er-configuration-provider"></a>Aktivieren eines EB-Konfigurationsanbieters

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Konfigurationsanbieter** die Kachel **Litware, Inc.** aus. Wählen Sie dann **Als aktiv festlegen** aus.

Weitere Informationen zu EB-Konfigurationsanbietern finden Sie unter [Erstellen von Konfigurationsanbietern und Markieren als aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-initial-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations1"></a>Importieren der ursprünglichen Versionen der standardmäßigen EB-Konfigurationen

Um Ihrer aktuellen Instanz von Finance die standardmäßigen EB-Konfigurationen hinzuzufügen, müssen Sie sie aus dem EB [Repository](general-electronic-reporting.md#Repository) importieren, das für diese Instanz konfiguriert wurde.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Konfigurationsanbieter** die Kachel **Microsoft** aus. Wählen Sie dann **Repositorys** aus, um die Liste der Repositorys für den Microsoft-Anbieter anzuzeigen.
3. Wählen Sie auf der Seite **Konfigurationsrepositorys** das Repository des Typs **Global** aus. Wählen Sie dann **Öffnen** aus. Wenn Sie aufgefordert werden, das Herstellen einer Verbindung zum Regulatory Configuration Service zu autorisieren, folgen Sie den Autorisierungsanweisungen.
4. Wählen Sie auf der Seite **Konfigurationsrepositorys** in der Konfigurationsstruktur im linken Bereich die Formatkonfiguration **Peppol Verkaufsrechnung** aus.
5. Wählen Sie im Inforegister **Versionen** die Version **11.2.2** aus.
6. Wählen Sie **Importieren**, um die ausgewählte Version vom globalen Respository herunterzuladen.

![Konfigurationsrepository-Seite.](./media/er-quick-start3-import-solution1.png)

> [!TIP]
> Wenn Sie Probleme beim Zugriff auf das [globale Repository](er-download-configurations-global-repo.md) haben, können Sie für das [Herunterladen von Konfigurationen](download-electronic-reporting-configuration-lcs.md) stattdessen Microsoft Dynamics Lifecycle Services (LCS) verwenden.

### <a name="review-the-imported-er-configurations"></a>Überprüfen der importierten EB-Konfigurationen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
3. Auf der Seite **Konfigurationen** erweitern Sie die Registerkarte **Konfigurationskomponenten**.
4. Erweitern Sie im Konfigurationsbaum im linken Bereich **Rechnungsmodell** und erweitern **UBL Verkaufsrechnung**.

Beachten Sie, dass zusätzlich zum ausgewählten EB-Format **Peppols Verkaufsrecnung** weitere erforderliche EB-Konfigurationen importiert wurden. Da ständig neue Versionen von EB-Konfigurationen im Global Repository und LCS veröffentlicht werden, damit die entsprechenden Lösungen den neuen Anforderungen entsprechen, wurden die neuesten Versionen der erforderlichen Datenmodell Konfiguration und der Modellabbildung importiert.

![Seite „Konfigurationen“.](./media/er-quick-start3-imported-solution1a.png)

Um den Status zu simulieren, den EB-Konfigurationen in der aktuellen Finanzinstanz hätten, wenn Sie Version **11.2.2** des EB-Formats **Peppol Verkaufsrechnung** früher importiert hätten, (z. B. am 7. August 2019) folgen Sie diesen Schritten.

- Wählen Sie im Aktionsbereich die Option **Löschen**, um alle EB-Konfigurationen zu löschen, die nach dem 7. August 2019 veröffentlicht wurden. Einzig **Rechnungsmodell**, **Rechnungsmodellzuordnung** (ursprünglich **Rechnungsmodellzuordnung**), **UBL Verkaufsrechnung** und **Peppol Verkaufsrechnung** Konfigurationen müssen verbleiben.
- Für die verbleibenden EB-Konfigurationen auf der Registerkarte **Versionen** wählen Sie **Löschen**, um alle Versionen von EB-Konfigurationen zu löschen, die nach dem 7. August 2019 veröffentlicht wurden.

Prüfen Sie, dass die folgenden EB-Konfigurationen in der Konfigurationsstruktur verfügbar sind:

- **Rechnungsmodell** Konfiguration des EB-Datenmodells (ursprünglich **Kundenrechnungsmodell** benannt):

    - Version 11 enthält Version 10 der Datenmodell EB-Komponente, die die Datenstruktur der Fakturierungsgeschäftsdomäne darstellt. Diese EB-Konfiguration wurde als Vorgänger des **Peppol Verkaufsrechnung** EB-Format importiert das für den Import ausgewählt wurde.
    - Version 50 enthält Version 31 der EB-Datenmodellkomponente. Diese EB-Konfiguration wurde als Vorfahr der Version vom 7. August 2019 importiert, **Rechnungsmodellzuordnung** Konfiguration der EB-Modellzuordnung.

    ![Konfiguration des EB-Datenmodells für das Rechnungsmodell auf der Seite Konfigurationen.](./media/er-quick-start3-imported-solution1b1.png)

    > [!TIP]
    > Wenn Sie Version 50 dieses Datenmodells nicht sehen, öffnen Sie das globale Repository und importieren Sie Version 50.19 der EB-Konfiguration **Rechnungsmodellzuordnung**.

- **Rechnungsmodellzuordnung** Konfiguration des EB-Datenmodells (ursprünglich **KundenRechnungsmodellzuordnung** benannt):

    - Version 50.19 wurde als neueste Implementierung von Version 50 der **Rechnungsmodell** Konfiguration des EB-Datenmodells importiert. Es enthält zwei Modellzuordnung EB-Komponenten, die beschreiben, wie das Datenmodell zur Laufzeit mit Anwendungsdaten gefüllt wird.

    ![Konfiguration des EB-Datenmodells für das Rechnungsmodellzuordnung auf der Seite Konfigurationen.](./media/er-quick-start3-imported-solution1b2.png)

    > [!TIP]
    > Wenn Sie Version 50.19 dieser Modellzuordnung nicht sehen, öffnen Sie das globale Repository und importieren Sie Version 50.19 der EB-Konfiguration **Rechnungsmodellzuordnung**.

- **UBL-Vertriebsrechung** EB-Formatkonfiguration:

    - Version 11.2 enthält die EB-Komponenten Format und Formatzuordnung. Die Formatkomponente legt das Berichtslayout fest. Die Formatzuordnungskomponente enthält die Modelldatenquelle und legt fest, wie die Datenquelle verwendet wird, um das Berichtslayout zur Laufzeit auszufüllen. Dieses EB-Format wurde so konfiguriert, dass E-Rechnungen im Universal Business Language Format (UBL) erstellt werden. Sie wurde als übergeordnetes EB-Format der **Peppol Verkaufsrechnung** importiert, die für den Import ausgewählt wurde.

- **Peoppol Vertriebsrechung** EB-Formatkonfiguration:

    - Version 11.2.2 enthält die Format- und Formatzuordnungs-EB-Komponenten, die für die Erstellung von E-Rechnungen im PEPPOL-Format (Pan-European Public Procurement OnLine) konfiguriert wurden.

    ![Peppol Vertriebsrechnug EB-Formatkonfiguration auf der Seite Konfigurationen.](./media/er-quick-start3-imported-solution1b3.png)

## <a name="configure-the-accounts-receivable-parameters"></a><a name="ConfigureAR1"></a>Debitorenparameter konfigurieren

1. Gehen Sie zu **Debitoren** \> **Einrichtung** \> **Debitorenparameter**.
2. Auf der Registerkarte **Elektronische Dokumente** auf dem Inforegister **Elektronische Berichterstattung** im Feld **Verkaufs- und Freitextrechnung** wählen Sie **Peppol Verkaufsrechnung**.
3. Wählen Sie **Speichern** aus.

![Registerkarte Elektronische Dokumente auf der Seite Debitorenparameter.](./media/er-quick-start3-configure-ar1.png)

## <a name="configure-the-legal-entity-parameters"></a><a name="ConfigureLE"></a>Konfigurieren Sie die Parameter der juristischen Person

1. Gehen Sie zu **Organisationsverwaltung** \> **Organisationen** \> **Juristische Personen**.
2. Für die ausgewählte **DEMF** Firma, auf dem Inforegister **Bankkonto-Information** im Feld **Routing-Nummer** geben Sie **1234** ein.
3. Wählen Sie **Speichern** aus.
4. Schließen Sie die Seite **Juristische Personen**.

## <a name="prepare-a-customer-record"></a><a name="ConfigureCustomer1"></a>Einen Debitorendatensatz vorbereiten

1. Wechseln Sie zu **Debitoren** \> **Debitoren** \> **Alle Debitoren**.
2. Auf der Seite **Alle Kunden** Seite wählen Sie den **DE-014** Kundenkonto-Link aus.

### <a name="add-a-customer-contact"></a>Einen Kundenkontakt hinzufügen

1. Wechseln Sie zu **Debitoren** \> **Debitoren** \> **Alle Debitoren**.
2. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Kunde** in der Gruppe **Konto** auf **Kontakte**.
3. Wählen Sie **Kontakte hinzufügen**.
4. Auf der Seite **Kontakte** im Feld **Vorname** öffnen Sie die Suche, wählen Sie **Adam Carter** und dann wählen Sie **Wählen**, um die Suche zu schließen.
5. Wählen Sie **Speichern** aus.
6. Schließen Sie die Seite **Konakte**.

### <a name="define-a-primary-contact"></a>Definieren Sie einen primären Kontakt

1. Wechseln Sie zu **Debitoren** \> **Debitoren** \> **Alle Debitoren**.
2. Auf dem Inforegister **Verkaufsdemografie** im Feld **Hauptansprechpartner** wählen Sie **Adam Carter**.

### <a name="set-the-e-invoicing-option"></a>Stellen Sie die Option für die elektronische Rechnungsstellung ein

1. Wechseln Sie zu **Debitoren** \> **Debitoren** \> **Alle Debitoren**.
2. Auf dem Inforegister **Rechnung und Lieferung** stellen Sie die Option **E-Rechnung** auf **Ja**.
3. Wählen Sie **Speichern** aus.
4. Schließen Sie die Seite **Alle Kunden**.

## <a name="process-a-customer-invoice-by-using-the-standard-er-configurations"></a><a name="ProcessInvoice1"></a>Verarbeiten einer Kundenrechnung mithilfe der Standard-EB-Konfigurationen

Sie können jetzt die von Ihnen importierten Standard-EB-Konfigurationen verwenden, um eine Freitextrechnung elektronisch an einen Kunden zu senden.

### <a name="add-a-new-invoice"></a>Fügen Sie eine neue Rechnung hinzu

1. Wechseln Sie zu **Debitoren** \> **Rechnungen** \> **Alle Freitextrechnungen**.
2. Auf der Seite **Freitextrechnung** wählen Sie **Neu**.
3. Auf dem Inforegisterr **Freitext-Rechnungskopf** im Feld **Kundenkonto** wählen Sie **DE-014**.
4. Auf dem Inforegister **Rechnungszeilen** wird eine Rechnungsposition automatisch hinzugefügt. Legen Sie die folgenden Felder für diese Position fest:

    - Geben Sie im Feld **Beschreibung** **Notebook** ein.
    - Wählen Sie im Feld **Hauptkonto** die Option **401100** aus.
    - Geben Sie im Feld **Einzelpreis** die Zahl **1000** ein.

5. Wählen Sie **Speichern** aus.

![Freitextrechnungs-Seite.](./media/er-quick-start3-add-invoice.png)

Weitere Informationen finden Sie unter [Erstellen einer Freitextrechnung](../../../finance/accounts-receivable/create-free-text-invoice-new.md).

### <a name="post-a-new-invoice"></a>Eine neue Rechnung buchen

1. Wechseln Sie zu **Debitoren** \> **Rechnungen** \> **Alle Freitextrechnungen**.
2. Auf der Seite **Freitextrechnung** wählen Sie im Aktionsbereich die Option **Buchen**.
3. Im Dialogfeld **Freitextrechnung buchen** wählen Sie **OK** aus.

![Details der Seite Freitextrechnung.](./media/er-quick-start3-post-invoice.png)

### <a name="send-a-posted-invoice"></a>Senden Sie eine gebuchte Rechnung

1. Wechseln Sie zu **Debitoren** \> **Rechnungen** \> **Alle Freitextrechnungen**.
2. Auf der Seite **Freitextrechnung** im Aktionsbereich in der Gruppe **Dokument** wählen Sie **Senden** \> **Original**.

    ![Vorschau der Originalrechnung.](./media/er-quick-start3-send-invoice.png)

3. Schließen Sie die Seite **Freitextrechnung**.

### <a name="analyze-a-generated-e-invoice"></a>Analysieren Sie eine generierte E-Rechnung

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Einzelvorgänge für elektronische Berichterstellung**.
2. Auf der Seite **Rlektronische Berichterstattung** wählen Sie auf dieser Seite den ersten Datensatz mit der Aufgabenbeschreibung aus die **Senden Sie das E-Rechnungs-XML**.
3. Wählen Sie **Dateien anzeigen**, um auf die Liste der generierten Dateien zuzugreifen.

    ![Elektronische Berichterstellungsseite.](./media/er-quick-start3-jobs-list.png)

4. Wählen Sie **Öffnen**, um die generierte E-Rechnungs-XML-Datei herunterzuladen.
5. Analysieren Sie die XML-Datei für die elektronische Rechnung. Beachten Sie, dass das Kundensteuerschema derzeit durch die **SchemaID** und **SchemaAgencyID** XML-Attribute dargestellt wird. Beachten Sie auch, dass das **cbc: CustomizationID** XML-Element derzeit den folgenden Text enthält: `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0`.

    ![Vorschau der generierten XML-Datei für die elektronische Rechnung.](./media/er-quick-start3-e-invoice1.png)

## <a name="add-a-custom-database-field"></a><a name="AddCustomField"></a>Fügen Sie ein benutzerdefiniertes Datenbankfeld hinzu

Sie können die Funktion [Benutzerdefinierte Feld](../../fin-ops/get-started/user-defined-fields.md) nutzen zum Ausführen der folgenden Anpassung in der aktuellen Finanzinstanz:

- Passen Sie die Datenbankstruktur an, indem Sie ein neues benutzerdefiniertes Datenbankfeld hinzufügen, in dem für jeden Kunden ein Bundessteueridentifikationscode gespeichert ist.
- Passen Sie die Seite **Kunde** durch Hinzufügen eines neuen Dateneingabefelds an, mit dem ein Steuerkennzeichenwert in das neue benutzerdefinierte Datenbankfeld eingegeben werden kann.

Befolgen Sie diese Schritte, um die Anpassung vorzunehmen.

1. Wechseln Sie zu **Debitoren** \> **Kunden** \> **Alle Kunden**.
2. Auf der Seite **Alle Kunden** Seite wählen Sie den **DE-014** Kundenkonto-Link aus.
3. Auf dem Inforegister **Allgemeines** klicken Sie mit der rechten Maustaste in einen leeren Bereich im Feld **Sprache** und wählen Sie dann **Personalisieren: UpperGroup**.

    Der Inhalt im Inforegister **Allgemeines** wird hervorgehoben und ein Menü **Personalisieren** wird angezeigt.

4. Auf dem Menü **Personifizieren** wählen Sie **Fügen Sie ein Feld hinzu**.
5. In dem Dialogfeld **Spalten hinzufügen** wählen Sie **Neues Feld erstellen**.
6. In dem Dialogfeld **Neues Feld erstellen** im Feld **Tabellenname** wählen Sie **Kunden**.
7. Geben Sie im Feld **Namenpräfix** **FederalTaxID** ein.

    > [!NOTE]
    > Der gesamte Feldname wurde automatisch als **FederalTaxID\_Benutzerdefiniert** definiert.

8. Geben Sie im Feld **Beschriftung** die **Steuernummer** ein.
9. Wählen Sie im Feld **Typ** die Option **Text**.
10. In das Feld **Länge** geben Sie **20** ein.
11. Wählen Sie **Speichern** aus.
12. Wählen Sie im angezeigten Meldungsfeld die Option **Ja**, um zu bestätigen, dass Sie einen neuen Feldeintrag **FederalTaxID** für die Tabelle **Kunden** erstellen möchten.
13. Wählen Sie **Einfügen**, um <a name="insert_custom_field"></a>das Feld **FederalTaxID\_Benutzerdefiniert** der aktuellen Seite hinzuzufügen.

    ![Seite alle Debitoren.](./media/er-quick-start3-create-new-field.gif)

14. Schließen Sie die Seite **Alle Kunden**.

## <a name="refresh-the-er-metadata"></a><a name="RefreshERMetadata"></a>Aktualisieren Sie die EB-Metadaten

Sie müssen die EB-Metadaten aktualisieren, um das von Ihnen hinzugefügte benutzerdefinierte Feld [sichtbar](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) im EB Modellzuordnungsdesigner anzuzeigen.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Tabellenreferenz neu erstellen**.
2. In dem Dialogfeld **Datenmodell aktualisieren** wählen Sie **OK**.

## <a name="design-the-custom-er-configurations"></a><a name="DesignCustomERConfigurations"></a>Entwerfen Sie die benutzerdefinierten EB-Konfigurationen

Sie können die von Microsoft bereitgestellten EB-Konfigurationen verwenden, um Ihre benutzerdefinierten EB-Konfigurationen so zu gestalten, dass sie E-Rechnungen generieren, die das neue Steuerkennzeichen enthalten.

### <a name="customize-the-data-model-configuration"></a>Datenmodellkonfiguration anpassen

Als Benutzer in der Rolle des Electronic Reporting Functional Consultant können Sie Ihr benutzerdefiniertes EB-Datenmodell entwerfen.

#### <a name="add-a-custom-data-model-configuration"></a>Benutzerdefinierte Daten-Modellkonfiguration hinzufügen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Wählen Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich **Benutzerdefiniertes Rechnungsmodell** aus.
3. Wählen Sie im Aktivitätsbereich **Konfiguration erstellen** aus.
4. Im Dropdown-Dialogfeld im Feld **Neu** wählen Sie **Ableiten vom Namen: Kundenrechnungsmodell, Microsoft**, um anzuzeigen, dass Ihre neue benutzerdefinierte EB-Datenmodellkonfiguration auf der EB-Datenmodellkonfiguration basieren sollte.
5. Geben Sie im Feld **Name** die Bezeichnung **Rechnungsmodell (Litware)** ein.
6. Wählen Sie **Konfiguration erstellen** aus, um die neue EBKonfiguration zu erstellen.

Sie können jetzt den EB-Datenmodell-Designer verwenden, um Version 50.1 der EB-Konfiguration **Rechnungsmodells (Litware)** in **Entwurf** [Status](general-electronic-reporting.md#component-versioning) zu ändern.

![Version 50.1 der EB-Konfiguration auf der Seite Konfigurationen.](./media/er-quick-start3-added-custom-model.png)

#### <a name="configure-a-custom-data-model"></a>Konfigurieren ein benutzerdefiniertes Datenmodell

Sie müssen Ihr benutzerdefiniertes Datenmodell ändern, indem Sie ein neues Feld hinzufügen, um den Wert eines Steueridentifikationscodes des Bundes anzugeben. Dieser Code ist Teil der Kundendaten für jedes EB-Format, das dieses Datenmodell als Datenquelle verwendet.

1. Wählen Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich **Rechnungsmodell (Litware)** aus.
2. Wählen Sie auf dem Inforegister **Versionen** die Version **50.1** der ausgewählten EB-Datenmodellkonfiguration aus und wählen Sie den Status **Entwurf**.
3. Wählen Sie im Aktionsbereich die Option **Designer** für die ausgewählte Konfigurationsversion.
4. Auf der Seite **Datenmodelldesigner** wählen Sie im Datenmodellbaum die Seite **Kundeninformation (Kunde)** aus.
5. Wählen Sie **Neu** aus.
6. Im Dropdown-Dialogfeld im Feld **Neuer Knoten als** akzeptieren Sie den Standardwert **Untergeordnetes Element eines aktiven Knotens**.
7. Geben Sie im Feld **Name** **FederalTaxId\_Litware** ein.
8. In dem Feld **Artikeltyp** akzeptieren Sie den Standardwert **Zeichenfolge**.
9. Wählen Sie **Hinzufügen** und dann **Speichern** aus.

    ![Datenmodell-Designerseite.](./media/er-quick-start3-add-data-model-field.png)

    > [!NOTE]
    > Die Felder **Beschriftung** und **Beschreibung** beschreiben den Zweck des neuen Feldes. Sie können diese Felder in mehreren Sprachen ausfüllen. Weitere Informationen finden Sie unter [Mehrsprachige Berichte in der elektronischen Berichterstattung erstellen](er-design-multilingual-reports.md).

10. Schließen Sie die Seite **Datenmodelldesigner**.

#### <a name="complete-a-custom-data-model-configuration"></a>Benutzerdefinierte Daten-Modellkonfiguration ergänzen

Sie müssen Ihre Arbeit mit Version 50.1 Ihrer benutzerdefinierten EB-Datenmodellkonfiguration [abschließen](general-electronic-reporting.md#component-versioning), um sie verfügbar zu machen, damit andere benutzerdefinierte EB-Konfigurationen hinzugefügt werden können.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Rechnungsmodell** und wählen Sie dann **Rechnungsmodell (Litware)** aus.
3. Wechseln Sie auf dem Inforegister **Versionen** zu **Status ändern** \> **Abgeschlossen** und wählen Sie dann **OK** aus.

Der Status von Version 50.1 wird von **Entwurf** zu **Abgeschlossen** geändert und die Version ist jetzt schreibgeschützt. Eine neue bearbeitbare Version 50.2 mit dem Status **Entwurf** wird hinzugefügt. Mit dieser Version können Sie weitere Änderungen an Ihrer benutzerdefinierten EB-Datenmodellkonfiguration vornehmen.

![Version 50.1 wurde auf der Seite Konfigurationen abgeschlossen.](./media/er-quick-start3-completed-custom-model1.png)

### <a name="customize-the-model-mapping-configuration"></a>Datenmodellkonfigurationazuordnung anpassen

Als Benutzer in der Rolle Entwickler für elektronische Berichterstellung können Sie Ihr benutzerdefiniertes EB-Datenmodell entwerfen.

#### <a name="add-a-custom-model-mapping-configuration"></a>Eine benutzerdefinierte Modellkonfigurationszuordnung hinzufügen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Benutzerdefiniertes Rechnungsmodell** und wählen Sie dann **Benutzerdefiniertes Rechnungsmodellzuordnung** aus.
3. Wählen Sie im Aktivitätsbereich **Konfiguration erstellen** aus.
4. Im Dropdown-Dialogfeld im Feld **Neu** wählen Sie **Ableiten vom Namen: Kundenrechnungsmodellzuordnung, Microsoft**, um anzuzeigen, dass Ihre neue benutzerdefinierte EB-Modellzuordnungskonfiguration auf der EB-Datenzuordnungskonfiguration basieren sollte.
5. Geben Sie im Feld **Name** die Bezeichnung **Rechnungsmodellzuordnung (Litware)** ein.
6. In dem Feld **Zielmodell** wählen Sie **Rechnungsmodell (Litware)**.

    > [!IMPORTANT]
    > Dieser Schritt ist sehr wichtig. Wenn Sie es weglassen, können Sie Ihr benutzerdefiniertes Datenmodell nicht in der konfigurierten Modellzuordnung verwenden.

7. Wählen Sie **Konfiguration erstellen** aus, um die neue EBKonfiguration zu erstellen.

![Eine benutzerdefinierte Modellzuordnungskonfiguration auf der Konfigurationsseite hinzufügen.](./media/er-quick-start3-adding-custom-mapping.png)

#### <a name="configure-a-custom-model-mapping"></a>Konfigurieren einer benutzerdefinierten Modellzuordnung

Sie müssen Ihre benutzerdefinierte Modellzuordnung ändern und angeben, wie das benutzerdefinierte Feld **FederalTaxID\_Litware** des benutzerdefinierten Datenmodells zur Laufzeit mit Anwendungsdaten ausgefüllt werden sollte.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Benutzerdefiniertes Rechnungsmodell** \> **Benutzerdefiniertes Rechnungsmodellzuordnung** und wählen Sie **Rechnugsmodellzuordnung (Litware)** aus.
3. Wählen Sie im Aktivitätsbereich **Designer** aus.
4. Wählen Sie auf der Seite **Modell für Datenquellenzuordnung** die Zuordnung **Kundenrechnung** aus.

    ![Modell für die Seite Datenquellenzuordnung.](./media/er-quick-start3-select-customer-mapping.png)

5. Wählen Sie **Designer** aus.
6. Auf der Seite **Modellzuordnungsdesigner** im Bereich **Datenquellen** erweitern Sie die **CustInvoiceJour** Datenquelle, die die Anwendungstabelle **CustInvoiceJour** darstellen.
7. Unter **CustInvoiceJour**, erweitern Sie **Beziehungen**, um die Liste der Beziehungen vom Typ Viele-zu-Eins (N: 1) für die **CustInvoiceJour** Tabelle zu überprüfen.
8. Unter **CustInvoiceJour** \> **Beziehungen**, erweitern Sie **Kunden (CustTable)** um Zugang zu den Feldern und Beziehungen der **Kunden (CustTable)** Tabelle zu erhalten.
9. Wählen Sie das Datenquellenfeld **FederalTaxID\_Benutzerdefiniert** aus, das Sie [zuvor](#insert_custom_field) implementiert haben.
10. In dem Bereich **Datenmodell** erweitern Sie **Benutzerdefinierte Information (Kunde)** und wählen Sie das Datenmodellfeld **FederalTaxIDv\_Litware** aus.
11. Wählen Sie **Bindung** aus.

    ![Modellzuordnungsdesigner-Seite.](./media/er-quick-start3-customize-model-mapping.gif)

12. Wählen Sie **Speichern** aus.
13. Schließen Sie die Seite **Modellzuordnungsdesigner**.
14. Schließen Sie die Seite **Zuordnung Modell zu Datenquelle**.

#### <a name="complete-a-custom-model-mapping-configuration"></a>Benutzerdefinierte Modellzuordnungskonfiguration ergänzen

Sie müssen Ihre Arbeit mit Version 50.19.1 Ihrer benutzerdefinierten EB-Modellzuordnungskonfiguration [ergänzen](general-electronic-reporting.md#component-versioning) , um sie zur Verwendung verfügbar zu machen.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Benutzerdefiniertes Rechnungsmodell** \> **Benutzerdefiniertes Rechnungsmodellzuordnung** und wählen Sie **Rechnugsmodellzuordnung (Litware)** aus.
3. Wechseln Sie auf dem Inforegister **Versionen** zu **Status ändern** \> **Abgeschlossen** und wählen Sie dann **OK** aus.

Der Status von Version 50.19.1 wird von **Entwurf** zu **Abgeschlossen** geändert und die Version ist jetzt schreibgeschützt. Eine neue bearbeitbare Version 50.19.2 mit dem Status **Entwurf** wird hinzugefügt. Mit dieser Version können Sie weitere Änderungen an Ihrer benutzerdefinierten EB-Modellzuordnungskonfiguration vornehmen.

![Version 50.19.1 wurde auf der Seite Konfigurationen abgeschlossen.](./media/er-quick-start3-completed-custom-mapping1.png)

> [!NOTE]
> Die unterstützte Konfiguration [Lebenszyklus](general-electronic-reporting-manage-configuration-lifecycle.md) deckt nicht den Lebenszyklus von Datenbankänderungen ab. Wenn Sie die Version 50.19.1 der exportierten **Rechnungsmodellzuordnung (Litware)** Konfiguration von der aktuellen Finanzinstanz exportieren und versuchen, sie in eine andere Instanz zu importieren, die das benutzerdefinierte Feld **FederalTaxID\_Benutzerdefiniert** in der Tabelle **CustTable** nicht enthält, wird eine Ausnahme auftreten. Die Ausnahme besagt, dass die importierte EB-Konfiguration nicht mit den Metadaten der Zielfinanzinstanz kompatibel ist.

### <a name="customize-the-format-configuration"></a>Anpassen der Formatkonfiguration

Als Benutzer in der Rolle des Electronic Reporting Functional Consultant können Sie Ihr benutzerdefiniertes EB Format entwerfen.

#### <a name="add-a-custom-format-configuration"></a>Neue benutzerdefinierte Formatkonfiguration hinzufügen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Benutzerdefiniertes Rechnungsmodell** \> **UBL Vertriebsrechung** und wählen Sie dann **Peppol Verkaufsrechnung** aus.
3. Wählen Sie im Aktivitätsbereich **Konfiguration erstellen** aus.
4. Im Dropdown-Dialogfeld im Feld **Neu** wählen Sie **Ableiten vom Namen: Peppol Verkaufsrechnung, Microsoft**, um anzuzeigen, dass Ihre neue benutzerdefinierte EB-Formatkonfiguration auf der EB-Formatkonfiguration basieren sollte.
5. Geben Sie im Feld **Name** die Bezeichnung **Peppol Verkaufsrechnung** ein.
6. In dem Feld **Datenmodell** wählen Sie **Rechnungsmodell (Litware)**, um Ihr benutzerdefiniertes Datenmodell und Ihre Modellzuordnungkomponenten zu verwenden.

    > [!NOTE]
    > Dieser Schritt ist sehr wichtig. Wenn Sie es weglassen, können Sie Ihr benutzerdefiniertes Datenmodell nicht im konfigurierten Format nutzen.

7. Wählen Sie im Feld **Datenmodell** die Staffdefinition **InvoiceCustomer** aus.
8. Wählen Sie **Konfiguration erstellen** aus, um die neue EBKonfiguration zu erstellen.

![Eine benutzerdefinierte Formatkonfiguration auf der Konfigurationsseite hinzufügen.](./media/er-quick-start3-adding-custom-format.png)

Sie können jetzt den EB-Vorgangs-Designer verwenden, um Version 11.2.2.1 der EB-Konfiguration **Peppol Verkaufsrechnung (Litware)** im **Entwurf** [Status](general-electronic-reporting.md#component-versioning) zu bearbeiten.

![Version 11.2.2.1 der EB-Konfiguration auf der Seite Konfigurationen.](./media/er-quick-start3-added-custom-format.png)

#### <a name="configure-a-custom-format"></a>Konfigurieren eines benutzerdefinierten Formats

Sie müssen Ihr benutzerdefiniertes Format ändern, indem Sie ein neues Formatelement hinzufügen, um den Wert des Steueridentifikationscodes eines in Rechnung gestellten Kunden einzugeben.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Benutzerdefiniertes Rechnungsmodell** \> **UBL Vertriebsrechung** \> **Peppol Verkaufsrechnung** und wählen Sie dann **Peppol Verkaufsrechnung (Litware)** aus.
3. Wählen Sie im Aktivitätsbereich **Designer** aus.
4. Erweitern Sie im Formatbaum **XMLHeader** \> **Rechnung** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme**, und wählen **cbc:ID**.
5. Wählen Sie **Hinzufügen** und dann **XML** \> **Attribut** aus.
6. Geben Sie im Dialogfeld **Komponenteneigenschaft** im Feld **Name** **FederalTaxId** ein.
7. Wählen Sie **OK**, um ein neues Formatelement hinzuzufügen, um ein neues **FederalTaxID** XML-Attribut in einer generierten XML-Datei zu erstellen.
8. Erweitern Sie im Formatbaum unter **XMLHeader** \> **Rechnung** \> **cac:AccountingCustomerParty** \> **cac.Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID** und wählen **cac.AccountingCustomerParty**.
9. Wählen Sie **Nach oben**.

![Neues Formatelement auf der Seite Format-Designer.](./media/er-quick-start3-customized-format.png)

#### <a name="configure-a-custom-format-mapping"></a>Konfigurieren einer benutzerdefinierten Formatzuordnung

1. Erweitern Sie auf der Seite **Format Designer**, auf der Registerkarte **Zuordnung** die Datenquelle **Rechnung** vom Typ **Modell**.
2. Unter **Rechnung**, erweitern Sie **Kundeninformation (Kunde)** und wählen **FederalTaxID\_Litware**.
3. Wählen Sie **Bindung** aus.

    ![Formatdesignerseite.](./media/er-quick-start3-customized-format-mapping.png)

4. Wählen Sie aus der Datenquelle **Rechnung** den Typ **Modell** aus und wählen Sie **Bearbeiten**.
5. In dem Feld **Version** Version **1** von Ihrem benutzerdefinierten Datenmodell auswählen und dann **OK** wählen.
6. Wählen Sie **Speichern** aus.
7. Seite **Format-Designer** schließen.

#### <a name="complete-a-custom-format-configuration"></a>Eine benutzerdefinierte Formatkonfiguration ergänzen

Sie müssen Ihre Arbeit mit Version 11.2.2.1 Ihrer benutzerdefinierten EB-Formatkonfiguration [ergänzen](general-electronic-reporting.md#component-versioning) , um sie zur Verwendung verfügbar zu machen.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Benutzerdefiniertes Rechnungsmodell** \> **UBL Vertriebsrechung** \> **Peppol Verkaufsrechnung** und wählen Sie dann **Peppol Verkaufsrechnung (Litware)** aus.
3. Wechseln Sie auf dem Inforegister **Versionen** zu **Status ändern** \> **Abgeschlossen** und wählen Sie dann **OK** aus.

Der Status von Version 11.2.2.1 wird von **Entwurf** zu **Abgeschlossen** geändert und die Version ist jetzt schreibgeschützt. Eine neue bearbeitbare Version 11.2.2.2 mit dem Status **Entwurf** wird hinzugefügt. Mit dieser Version können Sie weitere Änderungen an Ihrer benutzerdefinierten EB-Formatkonfiguration vornehmen.

![Version 11.2.2.1 wurde auf der Seite Konfigurationen abgeschlossen.](./media/er-quick-start3-completed-custom-format1.png)

## <a name="configure-the-accounts-receivable-parameters-to-start-to-use-custom-er-configurations"></a><a name="ConfigureAR2"></a>Konfigurieren Sie die Debitorenparameter so, dass die benutzerdefinierten EB-Konfigurationen verwendet werden

1. Gehen Sie zu **Debitoren** \> **Einrichtung** \> **Debitorenparameter**.
2. Auf der Registerkarte **Elektronische Dokumente** auf dem Inforegister **Elektronische Berichterstattung** im Feld **Verkaufs- und Freitextrechnung** wählen Sie **Peppol Verkaufsrechnung (Litware)**.
3. Wählen Sie **Speichern** aus.

![Seite Debitorenparameter, Registerkarte Elektronische Dokumenten, Inforegister Elektronische Berichterstattung.](./media/er-quick-start3-configure-ar2.png)

## <a name="update-a-customer-record-by-adding-a-federal-tax-identification-code"></a><a name="ConfigureCustomer2"></a>Aktualisieren Sie einen Kundendatensatz, indem Sie einen Bundessteueridentifikationscode hinzufügen

1. Wechseln Sie zu **Debitoren** \> **Debitoren** \> **Alle Debitoren**.
2. Auf der Seite **Alle Kunden** Seite wählen Sie den **DE-014** Kundenkonto-Link aus.
3. Auf dem Inforegister **Allgemeines** im Feld **Federal Tax ID** geben Sie **LITWARE-6789** ein.
4. Wählen Sie **Speichern** aus.

    ![DE-014 Kundendetails-Seite.](./media/er-quick-start3-added-tax-id-value.png)

5. Schließen Sie die Seite **Alle Kunden**.

## <a name="process-a-customer-invoice-by-using-custom-er-configurations"></a><a name="ProcessInvoice2"></a>Verarbeiten einer Kundenrechnung mithilfe der benutzerdefinierten EB-Konfigurationen

### <a name="select-and-send-a-posted-invoice"></a>Wählen Sie eine gebuchte Rechnung aus und senden Sie diese

1. Wechseln Sie zu **Debitoren** \> **Rechnungen** \> **Alle Freitextrechnungen**.
2. Auf der Seite **Freitextrechnung** wählen Sie die Rechnung aus, die Sie zuvor hinzugefügt und gebucht haben.
3. Im Aktionsbereich in der Gruppe **Dokument** wählen Sie **Senden** \> **Original**.
4. Schließen Sie die Seite **Freitextrechnung**.

### <a name="analyze-a-generated-e-invoice"></a>Analysieren Sie eine generierte E-Rechnung

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Einzelvorgänge für elektronische Berichterstellung**.
2. Auf der Seite **Elektronische Berichterstattung** wählen Sie den letzten Datensatz mit der Aufgabenbeschreibung **Senden Sie das E-Rechnungs-XML** aus.
3. Wählen Sie **Dateien anzeigen**, um auf die Liste der generierten Dateien zuzugreifen.
4. Wählen Sie **Öffnen**, um die generierte E-Rechnungs-XML-Datei herunterzuladen.
5. Analysieren Sie die XML-Datei für die elektronische Rechnung. Beachten Sie, dass das Kundensteuerschema gemäß Ihrer Anpassung das benutzerdefinierte Steuerschema **FederalTaxID** XML-Attribut zusätzlich zu den **SchemaID** und **SchemaAgencyID** XML-Attributen enthält. Der Wert dieses neuen XML-Attributs wird durch die **LITWARE-6789** Bundessteuer-ID definiert, die für einen in Rechnung gestellten Kunden eingegeben wurde.

    ![Vorschau der generierten XML-Datei für die elektronische Rechnung mit Ihren Anpassungen.](./media/er-quick-start3-e-invoice2.png)

## <a name="import-the-latest-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations2"></a>Importieren der letzten Versionen der standardmäßigen EB-Konfigurationen

Um die Standard-EB-Konfigurationen in Ihrer Finanzinstanz [auf dem Laufenden](general-electronic-reporting-manage-configuration-lifecycle.md) zu halten, müssen Sie neue Versionen davon importieren, sobald sie im EB [Repository](general-electronic-reporting.md#Repository), das für diese Instanz eingerichtet wurde, verfügbar sind.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Konfigurationsanbieter** die Kachel **Microsoft** aus. Wählen Sie dann **Repositorys** aus, um die Liste der Repositorys für den Microsoft-Anbieter anzuzeigen.
3. Wählen Sie auf der Seite **Konfigurationsrepositorys** das Repository des Typs **Global** aus. Wählen Sie dann **Öffnen** aus. Wenn Sie aufgefordert werden, das Herstellen einer Verbindung zum Regulatory Configuration Service zu autorisieren, folgen Sie den Autorisierungsanweisungen.
4. Wählen Sie auf der Seite **Konfigurationsrepositorys** in der Konfigurationsstruktur im linken Bereich die Formatkonfiguration **Peppol Verkaufsrechnung** aus.
5. Auf dem Inforegister **Versionen** wählen Sie **32.6.7** der ausgewählten EB-Formatkonfiguration, die zur Unterstützung elektronischer Kundenrechnungen im PEPPOL BIS 3-Format freigegeben wurde. Weitere Informationen finden Sie unter [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic).
6. Wählen Sie **Importieren** aus, um die ausgewählte Version aus dem globalen Repository auf die aktuelle Finance-Instanz herunterzuladen.

![Version 32.6.7 auf der Seite Konfigurations-Repository ausgewählt.](./media/er-quick-start3-import-solution2.png)

Informationen dazu, wie dieser Prozess automatisiert werden kann, finden Sie unter [Importieren Sie aktualisierte Versionen von EB-Konfigurationen](er-download-updated-versions-global-repo.md).

### <a name="review-the-imported-er-configurations"></a>Überprüfen der importierten EB-Konfigurationen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
3. Erweitern Sie das Inforegister **Konfigurationskomponenten**.
4. Wählen Sie in der Konfigurationsstruktur im linken Bereich **Rechnungsmodell** aus. Beachten Sie, dass der Name vom **Benutzerdefinierten Rechnungsmodell** in **Rechnungsmodell** in einer der importierten EB-Datenmodellkonfigurationen geändert wurde.
5. Wählen Sie in der Konfigurationsstruktur im linken Bereich **Rechnungsmodellzuordnung** aus. Beachten Sie, dass der Name vom **Benutzerdefinierten Rechnungsmodellmapping** in **Rechnungsmodellmapping** in einer der importierten EB-Modelkonfigurationen geändert wurde.
6. Erweitern Sie **UBL Verkaufsrechnung** \> **Peppol Verkaufsrechnung**.

Beachten Sie, dass zusätzlich zum ausgewählten EB-Format **Peppols Verkaufsrechnung** die neuesten Versionen der weiteren erforderlichen EB-Konfigurationen importiert wurden. Da ständig neue Versionen von EB-Konfigurationen im Global Repository und LCS veröffentlicht werden, damit die entsprechenden EB-Lösungen den neuen Anforderungen entsprechen, wurden die neuesten Versionen der erforderlichen Datenmodell-Konfiguration und der Modellabbildung importiert.

Stellen Sie sicher, dass die folgenden EB-Konfigurationen auch in der Konfigurationsstruktur verfügbar sind:

- **Rechnungsmodell** EB Datenmodellkonfiguration:

    - Version 206 (oder höher) enthält Version 24 (oder höher) der Datenmodell EB-Komponente, die die Datenstruktur der Fakturierungsgeschäftsdomäne darstellt. Diese EB-Konfiguration wurde als Vorfahr der neuesten verfügbaren EB-Modellzuordnungskonfiguration **Rechnungsmodellzuordnung** importiert.

    ![Version 206 auf der Seite Konfiguration.](./media/er-quick-start3-imported-solution2b1.png)

- **Rechnungsmodellzuordnung** EB Modellzuordnungskonfiguration:

    - Version 206.132 (oder höher) wurde als neueste Implementierung von Version 206 der **Rechnungsmodell** Konfiguration des EB-Datenmodells importiert. Es enthält mehrere Komponenten der Modellzuordnung, die beschreiben, wie das Datenmodell zur Laufzeit mit Anwendungsdaten gefüllt wird.

    ![Version 206.132 auf der Seite Konfiguration.](./media/er-quick-start3-imported-solution2b2.png)

- **UBL-Vertriebsrechung** EB-Formatkonfiguration:

    - Version 32.6 enthält die EB-Komponenten Format und Formatzuordnung. Die Formatkomponente legt das Berichtslayout fest. Die Formatzuordnungskomponente enthält die Modelldatenquelle und legt fest, wie die Datenquelle verwendet wird, um das Berichtslayout zur Laufzeit auszufüllen. Dieses EB-Format wurde so konfiguriert, dass E-Rechnungen im UBL-Forma erstellt werden. Sie wurde als übergeordnetes EB-Format der **Peppol Verkaufsrechnung** importiert, die für den Import ausgewählt wurde.

- **Peoppol Vertriebsrechung** EB-Formatkonfiguration:

    - Version 32.6.7 enthält die EB-Komponenten Format- und Formatzuordnung, die für die Erstellung von E-Rechnungen im PEPPOL-Format eingerichtet wurden.

    ![Version 32.6.7 auf der Seite Konfiguration.](./media/er-quick-start3-imported-solution2b3.png)

## <a name="adopt-the-changes-to-the-new-standard-er-configurations-in-your-custom-er-configurations"></a><a name="RebaseCustomERConfigurations"></a>Übernehmen Sie die Änderungen an den neuen Versionen der Standard-EB-Konfigurationen in Ihre benutzerdefinierten EB-Konfigurationen

### <a name="adopt-your-custom-er-data-model"></a>Übernehmen Sie Ihr benutzerdefiniertes EB-Datenmodell

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Rechnungsmodell** und wählen Sie dann **Rechnungsmodell (Litware)** aus.
3. Wählen Sie auf dem Inforegister **Versionen** die Entwurfversion **50.2** der ausgewählten EB-Datenmodellkonfiguration aus und wählen Sie **Zurücksetzen** aus.
4. In dem Feld **Zielversion** bestätigen Sie die Auswahl der Version **206** der Basis-EB-Datenmodellkonfiguration und wählen Sie dann **OK**.

    Die Entwurfsversion Ihrer benutzerdefinierten EB-Datenmodellkonfiguration wird neu nummeriert von **50.2** zu **206.2**, um anzuzeigen, dass es jetzt Ihre Anpassung enthält, die mit den Änderungen in der neuesten Version (206) der Basis-EB-Datenmodellkonfiguration zusammengeführt wurde.

    > [!NOTE]
    > Das Zurücksetzen kann nicht rückgängig gemacht werden. Um das Zurücksetzen abzubrechen, wählen Sie Version **50.1** des Modells **Rechnungsmodell (Litware)** auf dem Inforegister **Versionen** aus und wählen Sie dann **Diese Version abrufen** aus. Version 206.2 wird dann in **50.2** umnummeriert und der Inhalt der Entwurfsversion 50.2 stimmt mit dem Inhalt von Version 50.1 überein.

5. Wechseln Sie auf dem Inforegister **Versionen** zu **Status ändern** \> **Abgeschlossen** und wählen Sie dann **OK** aus.

Der Status von Version 206.2 wird von **Entwurf** zu **Abgeschlossen** geändert und die Version ist jetzt schreibgeschützt. Eine neue bearbeitbare Version 206.3 mit dem Status **Entwurf** wird hinzugefügt. Mit dieser Version können Sie weitere Änderungen an Ihrer benutzerdefinierten EB-Datenmodellkonfiguration vornehmen.

![Version 206.2 wurde auf der Seite Konfigurationen abgeschlossen.](./media/er-quick-start3-completed-custom-model2.png)

### <a name="adopt-your-custom-er-model-mapping"></a>Übernehmen Sie Ihr benutzerdefiniertes EB-Modellzuordnung

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Rechnungsmodell** \> **Benutzerdefiniertes Rechnungsmodellzuordnung** und wählen Sie **Rechnugsmodellzuordnung (Litware)** aus.
3. Wählen Sie auf dem Inforegister **Versionen** die Entwurfsversion **50.19.2** des ausgewählten EB-Datenzuordnungskonfiguration aus und wählen Sie **Zurücksetzen** aus.
4. In dem Feld **Zielversion** bestätigen Sie die Auswahl der Version **206.132** der Basis-EB-Modellzuordnungskonfiguration und wählen Sie dann **OK**.

    Die Entwurfsversion Ihrer benutzerdefinierten EB-Modellzuordnungskonfiguration wird neu nummeriert von **50.19.2** zu **206.132.2**, um anzuzeigen, dass es jetzt Ihre Anpassung enthält, die mit den Änderungen in der neuesten Version (206.132) der Basis-EB-Modellzuordnungskonfiguration zusammengeführt wurde.

    Beachten Sie, dass einige Konflikte beim Zurücksetzen entdeckt wurden. Sie müssen diese Konflikte jetzt manuell lösen.

    ![Konfliktnachrichten auf der Seite Konfigurationen neu starten.](./media/er-quick-start3-rebase-conflicts-model-mapping1.png)

5. Wählen Sie im Aktionsbereich die Option **Designer** aus und wählen Sie dann in der Zuordnungsliste **Kundenrechnung** aus.
6. Wählen Sie für jeden Zurücksetzungs-Konflikt **Eigenen Wert behalten** aus, weil Sie die Versionsnummer Ihres benutzerdefinierten Datenmodells für jede erwähnte Komponente behalten müssen.

    ![Zurücksetzungskonflikte auf der Modellzuordnungsdesigner-Seite.](./media/er-quick-start3-rebase-conflicts-model-mapping2.png)

7. Wählen Sie **Speichern** und dann schließen Sie die Seite **Modellzuordnungsdesigner**.
8. Wählen Sie in der Liste der Zuordnungen **Projektrechnung** aus.
9. Wählen Sie für jeden Zurücksetzungs-Konflikt **Eigenen Wert behalten** aus, weil Sie die Versionsnummer Ihres benutzerdefinierten Datenmodells für jede erwähnte Komponente behalten müssen.
10. Wählen Sie **Speichern** aus und dann schließen Sie die Seite **Modellzuordnung**.

    > [!NOTE]
    > Das Zurücksetzen kann nicht rückgängig gemacht werden. Um das Zurücksetzen abzubrechen, wählen Sie Version **50.19.1** der Modellzuordnung **Rechnungsmodellzuordnung (Litware)** auf dem Inforegister **Versionen** aus und wählen Sie dann **Diese Version abrufen** aus. Version 206.132.2 wird dann in **50.19.2** umnummeriert und der Inhalt der Entwurfsversion 50.19.2 stimmt mit dem Inhalt von Version 50.19.1 überein.

11. Wechseln Sie auf dem Inforegister **Versionen** zu **Status ändern** \> **Abgeschlossen** und wählen Sie dann **OK** aus.

Der Status von Version 206.132.2 wird von **Entwurf** zu **Abgeschlossen** geändert und die Version ist jetzt schreibgeschützt. Eine neue bearbeitbare Version 206.132.3 mit dem Status **Entwurf** wird hinzugefügt. Mit dieser Version können Sie weitere Änderungen an Ihrer benutzerdefinierten EB-Modellzuordnungskonfiguration vornehmen.

![Version 206.132.2 wurde auf der Seite Konfigurationen abgeschlossen.](./media/er-quick-start3-completed-custom-mapping2.png)

### <a name="adopt-your-custom-er-format"></a>Übernehmen Sie Ihr benutzerdefiniertes EB-Format

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Rechnungsmodell** \> **Peppol Verkaufsrechung** \> **Peppol Verkaufsrechnung** und wählen Sie dann **Peppol Verkaufsrechnung (Litware)** aus.
3. Wählen Sie auf dem Inforegister **Versionen** die Entwurfsversion **11.2.2.2** der ausgewählten EB-Formatkonfiguration aus und wählen Sie **Zurücksetzen** aus.
4. In dem Feld **Zielversion** bestätigen Sie die Auswahl der Version **32.6.7** der Basis-EB-Formatkonfiguration und wählen Sie dann **OK**.

    Die Entwurfsversion Ihrer benutzerdefinierten EB-Formatkonfiguration wird neu nummeriert von **11.2.2.2** zu **32.6.7.2**, um anzuzeigen, dass es jetzt Ihre Anpassung enthält, die mit den Änderungen in der neuesten Version (32.6.7) der Basis-EB-Formatkonfiguration zusammengeführt wurde.

    Beachten Sie, dass einige Konflikte beim Zurücksetzen entdeckt wurden. Sie müssen diese Konflikte jetzt manuell lösen.

5. Wählen Sie im Aktivitätsbereich **Designer** aus.
6. Wählen Sie für jeden Zurücksetzungs-Konflikt **Eigenen Wert behalten** aus, weil Sie die Versionsnummer Ihres benutzerdefinierten Datenmodells für jede erwähnte Komponente behalten müssen.
7. Wählen Sie **Speichern** aus.
8. Wählen Sie auf der Registerkarte **Zuordnung** den Typ **Modell** aus der Datenquelle **Rechnung** aus und wählen Sie dann **Bearbeiten**.
9. In dem Feld **Version** Version **2** von Ihrem benutzerdefinierten Datenmodell auswählen und dann **OK** wählen.
10. Wählen Sie **Speichern** aus.

    > [!NOTE]
    > Das Zurücksetzen kann nicht rückgängig gemacht werden. Um das Zurücksetzen abzubrechen, wählen Sie Version **11.2.2.1** des Formats **Peppol Verkaufsrechnung (Litware)** auf dem Inforegister **Versionen** aus und wählen Sie dann **Diese Version abrufen** aus. Version 32.6.7.2 wird dann in **11.2.2.2** umnummeriert und der Inhalt der Entwurfsversion 11.2.2.2 stimmt mit dem Inhalt von Version 11.2.2.1 überein.

11. Seite **Format-Designer** schließen.
12. Wechseln Sie auf dem Inforegister **Versionen** zu **Status ändern** \> **Abgeschlossen** und wählen Sie dann **OK** aus.

Der Status von Version 32.6.7.2 wird von **Entwurf** zu **Abgeschlossen** geändert und die Version ist jetzt schreibgeschützt. Eine neue bearbeitbare Version 32.6.7.3 mit dem Status **Entwurf** wird hinzugefügt. Mit dieser Version können Sie weitere Änderungen an Ihrer benutzerdefinierten EB-Formatkonfiguration vornehmen.

![Version 32.6.7.2 wurde auf der Seite Konfigurationen abgeschlossen.](./media/er-quick-start3-completed-custom-format2.png)

## <a name="process-a-customer-invoice-by-using-new-versions-of-the-custom-er-configurations"></a><a name="ProcessInvoice3"></a>Verarbeiten einer Kundenrechnung mithilfe der neuen Versionen der benutzerdefinierten EB-Konfigurationen

### <a name="select-and-send-a-posted-invoice"></a>Wählen Sie eine gebuchte Rechnung aus und senden Sie diese

1. Wechseln Sie zu **Debitoren** \> **Rechnungen** \> **Alle Freitextrechnungen**.
2. Auf der Seite **Freitextrechnung** wählen Sie die Rechnung aus, die Sie zuvor hinzugefügt und gebucht haben.
3. Im Aktionsbereich in der Gruppe **Dokument** wählen Sie **Senden** \> **Original**.

    > [!NOTE] 
    > Weil Sie jetzt zwei Versionen der **Peppol Verkaufsrechnung (Litware)** EB-Formatkonfiguration haben und keine Version ein [Datum des Inkrafttretens](general-electronic-reporting.md#component-date-effectivity) hat, wird die neueste Version verwendet, um eine E-Rechnung zu erstellen.

4. Schließen Sie die Seite **Freitextrechnung**.

### <a name="analyze-a-generated-e-invoice"></a>Analysieren Sie eine generierte E-Rechnung

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Einzelvorgänge für elektronische Berichterstellung**.
2. Auf der Seite **Elektronische Berichterstattung** wählen Sie den neuesten Datensatz mit der Aufgabenbeschreibung **Senden Sie das E-Rechnungs-XML** aus.
3. Wählen Sie **Dateien anzeigen**, um auf die Liste der generierten Dateien zuzugreifen.
4. Wählen Sie **Öffnen**, um die generierte E-Rechnungs-XML-Datei herunterzuladen.
5. Analysieren Sie die XML-Datei für die elektronische Rechnung. Beachten Sie, dass das Kundensteuerschema gemäß Ihrer Anpassung immer noch das benutzerdefinierte Steuerschema **FederalTaxID** XML-Attribut zusätzlich zu den **SchemaID** und **SchemaAgencyID** XML-Attributen enthält. Weil die Änderungen in der neuen Version des Basis-Formats **UBL Verkaufsrechnung** mit Ihrer Anpassung zusammengeführt wurde, wurde der Text im **cbc: CustomizationID** XML-Element von `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` zu `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0` geändert.

    ![Vorschau der generierten XML-Datei für die elektronische Rechnung mit Ihren Anpassungen.](./media/er-quick-start3-e-invoice3.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)
- [Herunterladen elektronischer Berichterstellungskonfigurationen von Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [Herunterladen von EB-Konfigurationen aus dem globalen Repository des Konfigurationsdienstes](er-download-configurations-global-repo.md)
- [Freitextrechnung erstellen](../../../finance/accounts-receivable/create-free-text-invoice-new.md)
- [Benutzerdefinierte Felder erstellen und damit arbeiten](../../fin-ops/get-started/user-defined-fields.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
