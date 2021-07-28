---
title: Druckbare Freitextrechnungsformulare generieren
description: In diesem Thema wird erläutert, wie das Framework für die elektronische Berichterstellung (EB) dazu verwendet werden kann, um druckbare Freitextrechnungs-(FTR)-Formulare als Microsoft Office-Dokumente zu generieren.
author: NickSelin
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: f5556195a1a787420061fbcaef5d97ac47823221
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359004"
---
# <a name="generate-printable-fti-forms"></a>Generieren von druckbaren FTI-Formularen

[!include[banner](../includes/banner.md)]

Das Framework für die elektronische Berichterstellung (EB) ermöglicht Ihnen das Generieren druckbarer Freitextrechnungs-(FTR)-Formulare als Microsoft Office-Dokumente. Dieses Thema enthält Informationen darüber, wie Sie Ihre eigenen Konfigurationen sowie Details verfügbarer Konfigurationsvorlagen erstellen können.

## <a name="overview"></a>Übersicht

Neben der vorhandenen Funktion zum Generieren druckbarer FTR-Formulare mithilfe von Microsoft SQL Server Reporting Services (SSRS) können Sie jetzt das EB-Framework verwenden. Sie können druckbare FTR-Formulare in Microsoft Office Excel und Word verwalten. Sie können auch das Layout, den Datenfluss und die Formatierungen ändern, um bestimmte Anforderungen zu erfüllen, ohne Codeänderungen vorzunehmen.

> [!NOTE]
> Wenn Sie mit einer Übersicht über die vorhandenen EB-Konfigurationen für dieses Beispiel der druckbaren FTR-Formularlösung beginnen möchten, können Sie direkt zum Abschnitt **EB-Beispielkonfigurationen herunterladen, um FTR-Formulare zu generieren** weiter unten in diesem Thema gehen.

## <a name="create-customized-configurations-for-fti-printable-forms"></a>Angepasste Konfigurationen für druckbare FTR-Formulare erstellen
Als Teil der benutzerdefinierten Lösung für druckbare FTR-Formulare müssen Sie eine Reihe von EB-Konfigurationen erstellen.

### <a name="configure-the-er-data-model"></a>Das EB-Datenmodell konfigurieren
Ihre Anwendung muss die EB-Datenmodellkonfiguration umfassen, die ein Datenmodell enthält, das die Geschäftsdomäne für die Debitorenfakturierung beschreibt. Als Anforderung muss der Name des Datenmodells **CustomersInvoicing** sein. Informationen zum Design von ER-Datenmodellen finden Sie unter [ER Design domänenspezifisches Datenmodell](tasks/er-design-domain-specific-data-model-2016-11.md).

### <a name="configure-the-er-model-mapping"></a>Die EB-Modellzuordnung konfigurieren
Ihre Anwendung muss die EB-Modellzuordnung für das Datenmodell „CustomersInvoicing” enthalten. Die Modellzuordnung kann entweder die EB-Datenmodellkonfiguration oder die EB-Modellzuordnungskonfiguration sein. Allerdings muss der Name des Stammdeskriptors der Modellzuordnung **FreeTextInvoice** lauten.

Die Zuordnung muss die folgenden Datenquellen enthalten:

- Datenquellentyp: **Tabellendatensätze**

    - Diese Datenquelle muss **CustInvoiceJour** genannt werden.
    - Sie muss auf die CustInvoiceJour-Anwendungstabelle verweisen.
    - Sie muss zur Laufzeit verwendet werden, um von der Anwendung zum EB-Modell übergeben zu werden, das die Liste der Rechnungen zuordnet, die zum Druck ausgewählt wurden.

- Datenquelltyp: **Objekt**

    - Diese Datenquelle muss **PrintMgmtPrintSettingDetail** genannt werden.
    - Sie muss auf die Anwendungsklasse **PrintMgmtPrintSettingDetail** verweisen.
    - Sie wird zur Laufzeit verwendet, um von der Anwendung zum EB-Modell übergeben zu werden, das die Details der Druckverwaltungseinstellungen für das EB-Format zuordnet, das ausgeführt wird.

Die Details der Anwendungsintegration mit dem EB-Framework können in der Klasse **ERPrintMgmtReportFormatSubscriber** (EB-Anwendungssuite-Integrationsmodell) im Quellcode der Anwendung gefunden werden.

Weitere Informationen zum Design von ER-Modell-Mappings finden Sie unter [Definieren von ER-Modellzuordnungen und Auswählen von Datenquellen](tasks/er-define-model-mapping-select-data-sources-2016-11.md).

### <a name="configure-the-er-format"></a>Das EB-Format konfigurieren
In Ihrer Anwendungsinstanz müssen Sie die EB-Formatkonfiguration haben, die verwendet wird, um FTR-Formulare zu generieren. 

> [!NOTE]
> Diese Formatkonfiguration muss für das CustomersInvoicing-Datenmodell erstellt werden, und sie muss die Modellzuordnung verwenden, die den Stammdeskriptor **FreeTextInvoice** hat.

Informationen zur Konfiguration von ER-Formaten finden Sie unter [ER Erstellen einer Formatkonfiguration (November 2016)](tasks/er-format-configuration-2016-11.md). Informationen zum Entwerfen von ER-Formaten zur Generierung von Berichten im OpenXML-Format finden Sie unter [ER Entwerfen einer Konfiguration zur Generierung von Berichten im OPENXML-Format (November 2016)](tasks/er-design-reports-openxml-2016-11.md).

## <a name="configure-print-management"></a>Druckverwaltung konfigurieren
Um FTR-Formulare mithilfe eines EB-Frameworks zu generieren, können Sie EB-Formate in derselben Art zuweisen, wie Sie SSRS-Berichte zuweisen. Um das EB-Format allen Debitoren-FTRs zuzuordnen, wechseln Sie zu **Debitoren** \> **Einstellungen** \> **Formulare** \> **Formulareinstellungen** \> **Allgemein** \> **Druckverwaltung** \> **Freitextrechnung** \> **Original**. Um das EB-Format einem bestimmten Debitor oder einer bestimmten Rechnung zuzuordnen, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Debitoren** \> **Rechnungen** \> **Alle Freitextrechnungen**.
2. Wählen Sie die FTR aus, der das EB-Format zugeordnet werden soll, und öffnen Sie die Seite **Druckverwaltungseinstellungen**.
3. Wählen Sie die Dokumentebene aus, um den Bereich von Rechnungen für das Verarbeiten anzugeben.
4. Wählen Sie das EB-Format für die angegebene Dokumentebene aus.

![Druckverwaltungseinstellungen.](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> Nur EB-Formate, die den Stammdeskriptor **FreeTextInvoice** des Datenmodells **CustomersInvoicing** verwenden, werden im Feld **Berichtsformatsuche** für das ausgewählte Format angezeigt.

## <a name="generate-fti-forms"></a>FTR-Formulare generieren
FTR-Formulare werden im EB-Framework in gleicher Weise generiert wie SSRS-Berichte.

Um FTR-Formulare zu generieren, können Sie Rechnungen entweder nach Bereich oder nach Auswahl auswählen. 

![Rechnungsauswahl.](media/FTIbyGER-InvoiceSelection.png)

![Rechnungsvorschau.](media/FTIbyGER-InvoiceExcelPreview.png)

Wenn Sie EB-Formate verwenden, um auf diese Weise FTR-Formulare zu drucken, werden die standardmäßigen EB-Dateiziele verwenden. Das Ziel kann nicht geändert werden. Weitere Informationen zur Konfiguration der ER-Ziele für ER-Formate finden Sie unter [Elektronische Berichtsziele (ER)](electronic-reporting-destinations.md).

Sie können auch FTR-Formulare generieren, wenn Sie eine FTR buchen, indem Sie **Rechnung drucken** aktivieren und **Druckverwaltungsziele verwenden** deaktivieren.

> [!NOTE]
> Wenn Sie EB-Formate verwenden, um auf diese Weise FTR-Formulare zu drucken, werden die standardmäßigen EB-Dateiziele verwenden. Sie können das Standardziel zur Laufzeit ändern, wenn das Ziel bereits konfiguriert wurde. Um das Ziel zu ändern, müssen Sie folgende Sicherheitsrechte haben:
>
> - **Name:** ERFormatDestinationRuntimeMaintain
> - **Bezeichnung:** Zielort für elektronisches Berichterstellungsformat zur Laufzeit verwalten

![Zielort für elektronische Berichterstellung.](media/FTIbyGER-ERFileDestinationSetting.png)

![Ziele für elektronisches Berichterstellungsformat.](media/FTIbyGER-ERFileDestinationUsage.png)

Das EB-Framework unterstützt aktuell die folgenden Ziele für generierte Dokumente:

- **Heruntergeladene Datei** – Generierte Formulare werden als Downloads angeboten, die Sie speichern können mithilfe des Browser.
- **Bildschirm** – Microsoft 365 Excel wird verwendet, um generierte FTR-Formulare im Excel-Format in der Vorschau anzuzeigen.
- **SharePoint-Ordner** – Generierte Formulare werden basierend auf den Einstellungen des Dokumentverwaltungsframeworks gespeichert.
- **Anwendungsarchiv** – Generierte Formulare werden als Anhänge von Ausführungsprotokolldatensätzen in Microsoft Azure Storage gespeichert.
- **E-Mail** – Generierte Formulare werden als E-Mail-Anhänge übermittelt.

> [!NOTE]
> Sie können die FTR-Formulare nicht übermitteln, die direkt für den Drucker generiert werden, da direktes Drucken unter Verwendung des Dynamics-Druckerweiterleitungsagent derzeit nicht unterstützt wird.

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a>Beispiel-EB-Konfigurationen zum Generieren druckbarer FTR-Formulare herunterladen
Sie können Beispiel-EB-Konfigurationen herunterladen, um sie als Vorlage für Ihre FTR-Lösung zu verwenden. Die Konfigurationen werden in der Bibliothek für freigegebene Anlagen in Microsoft Dynamics Lifecycle Services (LCS) gespeichert. Die Konfigurationen umfassen:

- Die Konfiguration **Debitorenfakturierungsmodell** enthält das erforderliche Datenmodell und Modellzuordnung.
- Die Konfiguration **Debitoren-FTR-Bericht (GER)** enthält das Beispielformat.

> [!NOTE]
> Diese Konfigurationen wurden als Beispiele erstellt, mit deren Hilfe mögliche Szenarien abgeklärt werden können. Die Zukunft dieser Konfigurationen hängt von den Ergebnissen dieser Bewertung und sämtlichen empfangenen Rückmeldungen ab.

### <a name="features-that-are-implemented-in-the-sample-er-format"></a>Funktionen, die im Beispiel-ER-Format implementiert werden
In der Beispiel-EB-Formatkonfiguration wird eine Excel-Datei als Vorlage verwendet, um FTR-Formulare zu generieren.

![Formatdesigner.](media/FTIbyGER-ERFormat.png)

Momentan unterstützt dieses Beispiel-EB-Format die folgenden Funktionen, um FTR-Formulare zu generieren:

- FTR-Formulare werden sowohl für ursprüngliche Rechnungen, die gebucht wurden, als auch für ursprüngliche Rechnungen, die noch nicht gebucht wurden, generiert. Korrigierte Rechnungen und Gutschriften werden nicht unterstützt.
- FTR-Formulare werden in der Rechnungssprache generiert. Das Format von Werten und Datumswerten in den generierten Formularen basiert auf den Einstellungen des Clientgebietsschemas des Benutzers.
- Generierte Rechnungen zeigen Benachrichtigungen zur Nichtverfügbarkeit von Daten an, wenn sich keine Positionen in den Rechnungen befinden, die verarbeitet werden.
- Generierte Rechnungsköpfe basieren auf dem Papierformat, das für das FTR-Formular auf der Seite **Debitorenparameter** ausgewählt wurde. Unternehmensdetails werden nur im Kopf des generierten Rechnungsformulars angezeigt, wenn das Papierformat leer ist.
- Generierte Rechnungsformulare zeigen Unternehmens- und Debitoren-Umsatzsteuernummern an, wenn die entsprechende Option für das FTR-Formular auf der Seite **Debitorenparameter** ausgewählt wurde.
- Die generierten Rechnungspositions- und Rechnungssummenabschnitte zeigen die standardmäßigen Währungsdetails der Rechnung in der Rechnungserfassungswährung an.
- Der generierte Rechnungssummenabschnitt kann Währungsdetails in der Euro-Währung und in der Rechnungserfassungswährung anzeigen, wenn die Option **Betrag in der Währung drucken, die für den Euro steht** auf der Seite **Debitorenparameter** aktiviert ist.
- Generierte Rechnungsformulare zeigen sämtliche Rechnungsverarbeitungshinweise an, die verfügbar sind, auf der Grundlage der Einstellungen auf der Seite **Debitorenparameter**. Hinweise sind sowohl für die gesamte Rechnung als auch für jede Rechnungsposition enthalten.
- Generierte Rechnungsformulare umfassen Hinweise für Debitoren-FTR-Formulare und die Sprache für die Rechnungsverarbeitung, wenn sie in der Debitorenformular-Hinweisliste konfiguriert worden sind.
- Abhängig von den Druckverwaltungseinstellungen umfassen generierte Rechnungen benutzerdefinierten Fußzeilentext, wenn er für die Rechnungssprache, das EB-Format und den FTR-Dokumentbereich konfiguriert wurde.
- Der Summenabschnitt generierter Rechnungsformulare umfasst sämtliche Skontoinformationen, die verfügbar sind.
- Der Zahlungsplanabschnitt generierter Rechnungsformulare beinhaltet sämtliche mögliche Zahlungsplandetails, die verfügbar sind.
- Der Aufschlagsabschnitt generierter Rechnungsformulare umfasst sämtliche Zuschlagsbuchungen, die zur Verfügung stehen.
- Generierte Rechnungsformulare enthalten Mehrwertsteuerdetails, basierend auf den Einstellungen **Mehrwertsteuerspezifikation** auf der Seite **Debitorenparameter**. Dieser Abschnitt kann Steuerdetails entweder nur in der Rechnungserfassungswährung oder in der Rechnungserfassungswährung und in der Unternehmensbuchhaltungswährung gleichzeitig anzeigen.
- Generierte Rechnungsformulare zeigen Lastschriftbenachrichtigungsdetails an. So zeigen sie beispielsweise an, wann die Zahlungsmethode für die Rechnung ausgewählt wurde, die die obligatorische Lastschrift-Vollmachtskennung aufweist, wenn die in Verarbeitung befindliche Rechnung in der Eurowährung erfasst wurde, und wann die Lastschrift-Vollmachtskennung für die Rechnung definiert wurde.
- Generierte Rechnungen zeigen sämtliche Vorauszahlungsdetails an, die für gebuchte Rechnungen verfügbar sind.
- Generierte Rechnungsformulare können einem Rechnungsdebitor als E-Mail-Anhang gesendet werden. Das entsprechende EB-Dateiziel sollte für das EB-Format konfiguriert werden, das verwendet wird.

### <a name="countryregion-specific-features"></a>Landes-/regionsspezifische Funktionen 
Die folgenden länder-/regionsspezifischen Funktionen sind im Muster-EB-Format enthalten, um anzuzeigen, wie spezifische Anforderungen in EB-Konfigurationen gehandhabt werden können.

#### <a name="norway"></a>Norwegen
Die Enterprise-Registerbedingung wird in den Kopf des generierten Rechnungsformulars platziert, wenn die Rechnung für eine juristische Person verarbeitet wird, die in folgender Weise konfiguriert ist:

- Der Landes-/Regionskontext für Norwegen wird verwendet.
- Der Parameter **Print Foretaksregisteret** ist auf Verkaufsbelegen aktiv.

#### <a name="spain"></a>Spanien
Die Bedingung **Sondersystem für Kassenbuchführungsmethode** wird in den Kopf des generierten Rechnungsformulars platziert, wenn die Rechnung für eine juristische Person verarbeitet wird, die in folgender Weise konfiguriert ist:

- Der Landes-/Regionskontext für Spanien wird verwendet.
- Das Sondersystem für die Kassenbuchführungsmethode ist am Rechnungsverarbeitungsdatum aktiviert.

Wenn Skontodetails, wie der Skontobetrag und der Nettobetrag der Rechnungsposition verfügbar sind, werden sie im Rechnungssummenabschnitt des generierten Rechnungsformulars dargestellt, wenn es für eine juristische Person verarbeitet wurde, die wie folgt konfiguriert ist:

- Der Landes-/Regionskontext für Spanien wird verwendet.
- **Skonto wird auf die Rechnung angewendet** ist in der Rechnungsoption aktiviert (**Hauptbuchparameter** \> **Mehrwertsteuerabschnitt**).

#### <a name="italy"></a>Italien
Die Warenrabattmarke ist in den Rechnungspositionen der generierten Rechnung eingeschlossen, wenn sie für eine juristische Person verarbeitet wird, die mithilfe des Landes-/Regionskontexts für Italien konfiguriert ist.

#### <a name="finland"></a>Finnland
Außer dem generierten Rechnungsformular können Girogeldüberweisungsbeleg folgendermaßen generiert werden:

- Für die juristische Person, die den Landes-/Regionskontext für Finnland verwendet und mindestens ein Bankkonto hat, das als **Girokonto** und **Bankstrichcode** markiert ist. 
- Für eine Rechnung, die für den zugeordneten Zahlungsanhang **Finnisch** als erforderlich markiert ist.

![Girobeleg.](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> Das Beispiel-EB-Format ist so konfiguriert worden, dass es optional die Girogeldüberweisungsbelege in einem getrennten Arbeitsblatt generiert.

> [!NOTE]
> Sie müssen zuerst die Schriftart installieren, die verwendet wird, um den Strichcode im lokalen Rechner zu generieren, in dem das generierte Rechnungsformular im Excel-Format in der Vorschau angezeigt wird.

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a>Das Beispiel-EB-Format verwenden, um E-Mail-Ziele zu konfigurieren
Die folgenden Elemente des Beispiel-EB-Formats verwenden, um E-Mail-Ziele zu konfigurieren:

- Auf die E-Mail-Adresse eines Debitorenkontakts kann über den folgenden EB-Ausdruck zugegriffen werden: **model.InvoiceBase.Contact.ElectronicMail**.
- Auf den E-Mail-Betrefftext kann über den folgenden EB-Ausdruck zugegriffen werden: **Emailing.TxtToUse.Subject**.
- Auf den E-Mail-Textkörper kann über den folgenden EB-Ausdruck zugegriffen werden: **Emailing.TxtToUse.Body**.

![Zielorteinstellungen.](media/FTIbyGER-ERFileDestinationSettingEmail.png)

Der Standardtext des Betreffs und des Textkörpers der E-Mail wird im Beispiel-EB-Format definiert. Die Sprache hängt von den Bezeichnungen des Formats ab. Dieser Standardtext wird für E-Mails verwendet, wenn eine benutzerdefinierte Organisations-E-Mail-Vorlage, die die vordefinierte **ERFTITMP**-Kennung aufweist, nicht hinzugefügt wurde.

> [!NOTE]
> Die E-Mail-Vorlagenkennung **ERFTITMP** wurde im Beispiel-EB-Format definiert. Sie kann bei Bedarf in ein neues EB-Format geändert werden, das aus diesem Beispielformat erstellt wird.

Wenn die Organisations-E-Mail-Vorlage, die die vordefinierte **ERFTITMP**-Kennung aufweist, für die juristische Person hinzugefügt wurde, für die Sie die Rechnung verarbeiten, wird die Vorlage für den E-Mail-Betreff und -Textkörper verwendet, um die E-Mail zu generieren. 

![Organisations-E-Mail-Vorlagen.](media/FTIbyGER-EmailTemplate.png)

![E-Mail-Vorlage hochladen.](media/FTIbyGER-EmailTemplateBody.png)

Der EB-Ausdruck **Emailing.TxtToUse.Subject** des Beispiel-EB-Formats wird so konfiguriert, dass sämtliche Vorkommen des Platzhalters %1 durch die Kennung der verarbeitenden Rechnung ersetzt werden.

Der Ausdruck **Emailing.TxtToUse.Body** des Beispielformats wird für die folgenden Ersetzungen für Platzhalter konfiguriert:

- "%1" wird durch den Namen der Kontaktperson des Debitors ersetzt.
- "%2" wird durch den Unternehmensnamen ersetzt.
- "%3" wird durch den Debitorennamen ersetzt.
- "%4" wird durch den Namen der Kontaktperson des Unternehmens ersetzt.
- "%5" wird durch den Stellentitel der Kontaktperson des Unternehmens ersetzt.
- "%6" wird durch die E-Mail-Adresse der Kontaktperson des Unternehmens ersetzt.

![E-Mail.](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a>Zusätzliche Ressourcen
[Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]