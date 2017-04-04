---
title: "Zielorte für elektronische Berichterstellung"
description: "Sie können ein Ziel für jede Formatvariante zur &quot;Elektronischen Berichterstellung&quot; (ER) und die Ausgabenkomponente (einen Ordner oder eine Datei) konfigurieren. Benutzer, die entsprechende Zugriffsrechte haben, können auch Zieleinstellungen zur Laufzeit ändern. Dieser Artikel beschreibt die ER Zielverwaltung, die unterstützten Zieltypen und die Sicherheitsaspekte."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: d38d05fe445bf0326d408038dff84ccf8c0ff64c
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-destinations"></a>Zielorte für elektronische Berichterstellung

Sie können ein Ziel für jede Formatvariante zur "Elektronischen Berichterstellung" (ER) und die Ausgabenkomponente (einen Ordner oder eine Datei) konfigurieren. Benutzer, die entsprechende Zugriffsrechte haben, können auch Zieleinstellungen zur Laufzeit ändern. Dieser Artikel beschreibt die ER Zielverwaltung, die unterstützten Zieltypen und die Sicherheitsaspekte.

Die Formatkonfiguration für die elektronische Berichterstellung (ER) umfasst in der Regel mindestens eine Ausgabekomponente: eine Datei. Konfigurationen enthalten in der Regel mehrere Ausgabedatei-Komponenten verschiedener Typen (XML, TXT oder XLSX), die entweder in einen einzelnen Ordner oder mehrere Ordner gruppiert sind. Die ER-Zielverwaltung ermöglicht die Vorkonfiguration der Ausführung jeder Komponente. Bei einer Konfiguration ausgeführt ist, erscheint das Dialogfeld den Benutzer, das die Datei speichern oder öffnen können. Dasselbe Verhalten wird auch beim Importieren einer ER-Konfiguration ohne spezifischen Ziele für diese verwendet. Nachdem ein Ziel für eine Hauptausgabekomponente erstellt wurde, überschreibt das Ziel das Standardverhalten und der Ordner oder die Datei wird entsprechend dem Ziel gesendet.

## <a name="availability-and-general-prerequisites"></a>Verfügbarkeit und allgemeine Voraussetzungen
Die er-Zielfunktionen werden nicht in Microsoft Dynamics 365 zur Freigabe der Arbeitsgänge 7,0 (Februar 2016 )verfügbar. Daher müssen Sie Microsoft Dynamics 365 für Arbeitsgänge (November 2016 Freigabe) einrichten um alle Funktionen verwenden, die in diesem Thema beschrieben sind. Alternativ können Sie eine der folgenden Voraussetzungen einrichten. Beachten Sie jedoch, dass dieses begrenztere eine Alternative ER-Zielerfahrung enthalten.

-   Microsoft Dynamics 365 für Arbeitsgangsbewerbungsversion 7.0.1 ()Mai 2016
-   [Anwendungs-Hotfix](https://fix.lcs.dynamics.com/issue/results/?q=3160213) für die ER Zielverwaltung

Sie können Ziele nur für ER-Konfigurationen einrichten, die importiert wurden und für die Formate auf der Seite **Konfigurationen für die elektronische Berichterstellung** verfügbar sind.

## <a name="overview"></a>Überblick
Die er-Zielverwaltungsfunktionen sind ** Organisationsverwaltung ** ** bei der elektronischen &gt; Berichterstellung ** verfügbar. Hier können Sie das Standardverhalten für eine Konfiguration überschreiben. Importierte Konfigurationen werden hier nicht angezeigt, bis Sie auf **Neu** klicken und dann im Feld **Verweis** eine Konfiguration für die Zieleinstellungen wählen.

[![einer Konfiguration im Feld Referenz auswählen]" . /media/ger-destinations-2-1611-1024x574.jpg)]". /media/ger-destinations-2-1611.jpg) 

Nachdem Sie eine Referenz erstellt haben, können Sie ein Dateiziel für jeden Ordner oder für eine Datei erstellt. 

[![ein Dateiziel]" erstellt . /media/ger-destinations-1611-1024x586.jpg)]". /media/ger-destinations-1611.jpg)

**Hinweis:** Sie können ein Dateiziel für jede Ausgabekomponente des gleichen Formats im Feld **Dateiname** erstellen (z. B. einen Ordner oder eine Datei). Sie können einzelne Ziele für das im Dateiziel ** Zieleinstellungen ** Dialogfeld dann aktivieren und deaktivieren. Die **Einstellungen**-Schaltfläche wird verwendet, um alle Ziele für eine ausgewählte Dateiziel steuern. Im **Zieleinstellungen**-Dialogfeld Sie können jedes Ziel separat steuern, indem Sie die **Aktiviert**-Option nutzen.

![Zieleinstellungsdialogfeld ([]. /media/ger-destinations-settings-1611-1024x589.jpg)]". /media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Zieltypen
Es werden verschiedene Zieltypen unterstützt. Sie können alle gleichzeitig aktivieren oder deaktivieren. Auf diese Weise können Sie entweder nichts machen, oder die Komponente an alle konfigurierten Ziele senden. In den folgenden Abschnitten werden die unterstützten Ziele beschrieben.

### <a name="email-destination"></a>E-Mail-Ziel

Legen Sie **Aktiviert ** auf **Ja** fest, um eine Ausgabedatei per E-Mail zu senden. Nachdem diese Option aktiviert ist, können Sie den E-Mail-Empfängern angeben bearbeiten und den Betreff sowie den Text der E-Mail-Nachricht. Sie können für den E-Mail-Betreff konstante Texte und den Text einrichten, oder Sie können ER-Formeln verwenden, um E-Mail-Texte dynamisch zu erstellen. Sie kann E-Mail-Adressen für ER auf zwei Arten konfigurieren. Die Konfiguration kann können abgeschlossen werden, in der die Druckverwaltungsfunktion Dynamics 365 für Arbeitsgänge es ab. Alternativ können Sie eine E-Mail-Adresse auflösen, indem Sie eine direkte Verweis auf die ER-Konfiguration mit einer Formel verwenden.

### <a name="email-address-types"></a>E-Mail-Adressen-Typen

Wenn Sie ** Bearbeiten ** für ** ** oder ** ** eine Kopie auf klicken, wird das Feld E-Mail ** ** Dialogfeld. Sie können den gesuchten der E-Mail-Adresse zu verwendende dann auswählen.

[![Dialogfeld] (E-Mail an. /media/ger-destinations-email-1-1611-1024x588.jpg)]". /media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Druckverwaltung

Wenn Sie auswählen Druckverwaltungse-mail ** ** geben Sie, Sie kann E-Mail-Adressen auf dem festen ** zu ** ein Feld eingeben. Wenn Sie E-Mail-Adressen zu verwenden die nicht behoben werden, muss der E-Mail-Quelltyp für ein Dateiziel auswählen. Folgende Werte werden unterstützt: ** ** ** Debitor, Kreditor, Interessent ** ** **, ** Kontakt ** **, Mitbewerber **, ** Arbeitskraft ** **, Bewerber **, ** ** ** und künftiger Kreditor unzulässig **. Nachdem Sie einen E-Mail-Quelltyp auswählen, verwenden Sie die Schaltfläche neben dem Feld, E-Mail-Quellkonto ** ** ** Formeldesigner ** um das Formular zu öffnen. Sie können dieses Formular verwenden, um eine Formel zugeordnet werden, die das ausgewählte Parteienkonto dem E-Mail-Ziel darstellt.

[]( Druckverwaltungse-mail-Typ ![konfigurieren . /media/ger-destinations-email-2-1611-1024x588.jpg)]". /media/ger-destinations-email-2-1611.jpg) 

Beachten Sie, dass Formeln für die ER-Konfiguration spezifisch sind. Im Feld **Formel** geben Sie einen dokumentspezifischen Verweis auf einen Debitoren- oder Händlerparteityp ein. Anstelle es einzugeben, können Sie einen Datenquellknoten finden, der das Debitoren- oder Händlerkonto darstellt, und klicken Sie auf die Schaltfläche **Datenquelle hinzufügen**, um die Formel zu aktualisieren. Beispiel: Wenn Sie die Konfiguration "Kreditübertragung (ISO 20022)" verwenden, lautet der Knoten, der ein Händlerkonto darstellt, **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Andernfalls geben Sie einen beliebigen Zeichenfolgenwert ein, wie **DE-001**, um eine Formel zu speichern.

[![Formula designer](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

** ** E-Mail im Dialogfeld auf den Papierkorb neben dem Feld E-Mail-Quellkonto ** **, um die Formel zum E-Mail-Quellkonto dauerhaft zu löschen. Alternativ Öffnet den Formeldesigner, um eine Formel zu ändern, die zuvor gespeichert wurde. Wenn Sie E-Mail-Adressen zuweisen, auf ** Bearbeiten ** um das ** weisen Sie E-Mail-Adressen ** Dialogfeld zu öffnen.

[![für ein E-Mail-Ziel E-Mail-Adressen zuweist] ". /media/ger-destinations-email-3-1611-1024x587.jpg)]". /media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Konfigurations-E-Mail

Mithilfe den E-Mail-Typ, wenn die Konfiguration, die Sie verwenden, einen Knoten der Datenquellen hat, der eine E-Mail-Adresse ein. Sie können Funktionen im Formeldesigner Datenquellen und verwenden, um eine ordnungsgemäße formatierte E-Mail-Adresse abzurufen.

[![eine E-Mail-Adressen-Datenquelle für ein E-Mail-Ziel zuweist] ". /media/ger-destinations-email-4-1611-1024x587.jpg)]". /media/ger-destinations-email-4-1611.jpg) 

**Hinweis:** Ein SMTP-Server (Simple Mail Transfer Protocol) muss konfiguriert und verfügbar sein. Sie können Ihrem SMTP-Server in Dynamics 365 für Arbeitsgänge, ** Systemverwaltung ** ** &gt; an den Einstellungen angeben ** &gt; ** E-Mail ** &gt; ** E-Mail-Parameter **.

### <a name="archive-destination"></a>Archivziel

Mit dieser Option können Ausgaben als Microsoft SharePoint-Ordner oder Microsoft Azure Storage senden. Legen Sie **Aktiviert** auf **Ja **fest, um die Ausgabe an ein Ziel zu senden, das über den ausgewählten Dokumenttyp definiert ist. Nur Dokumenttypen mit der Gruppe **Datei** stehen zur Auswahl. Sie legen Dokumenttypen ** Organisationsverwaltung ** ** &gt; an der Dokumentverwaltung ** ** &gt; Dokumenttypen **. Die Konfiguration für ER-Ziele ist identisch mit der Konfiguration für das Dokumentverwaltungssystem.

![Dokumenttypseite( [] . /media/ger_documenttypefile-1024x542.jpg)]". /media/ger_documenttypefile.jpg) 

Der Speicherort bestimmt, wo die Datei gespeichert wird. Nachdem das Archiv ** ** Ziel aktiviert ist, können Sie die Ergebnisse der Konfigurations ausführung im Einzelvorgangsarchiv gespeichert werden. Sie können die Ergebnisse ** Organisationsverwaltung ** ** bei &gt; der elektronischen Steuererklärung anzeigen ** ** &gt; elektronische Berichterstellung archivierten ** Einzelvorgänge. ** Hinweis: ** Sie können einen Dokumenttyp für das Einzelvorgangsarchiv in Dynamics 365 für Arbeitsgänge, ** Organisationsverwaltung ** ** für &gt; den ausgewählten Geschäftsbereich ** ** elektronische &gt; Berichterstellung ** ** elektronische &gt; Berichterstellungsparameter **.

#### <a name="sharepoint"></a>SharePoint

Sie können eine Datei in einem bestimmten SharePoint-Ordner speichern. Sie definieren den Standardwert SharePoint-Server ** Organisationsverwaltung ** ** &gt; an der Dokumentverwaltung ** ** &gt; Dokumentverwaltungsparameter **, SharePoint ** ** auf der Registerkarte. Nachdem der SharePoint-Ordner konfiguriert ist, können Sie diesen als auswählen der Ordner, in dem die ER-Ausgabe für den Dokumenttyp gespeichert wird. 

[![einen SharePoint-Ordner auswählt] ". /media/ger_sharepointfolderselection-1024x543.jpg)]". /media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure Storage

Wenn der Dokumenttypspeicherort auf **Archivverzeichnis** festgelegt ist, können Sie eine Datei in den Azure Storage speichern.

### <a name="file-destination"></a>Dateizielort

Ist aktiviert ** ** ** ** auf Ja, oder Abwehrdialogfeld ein offenes werden, wenn die Konfiguration die Ausführung abgeschlossen ist.

### <a name="screen-destination"></a>Bildschirmziel

Ist aktiviert ** ** ** ** auf Ja, eine Vorschau der Ausgabe erstellt werden. Sie können eine, Dateitypen XML, z TXT PDF, oder direkt in einer Browserfenster angezeigt. Für andere Dateitypen solches wird Microsoft Excel oder Word, der Microsoft Office Online-Service verwendet.

### <a name="power-bi-destination"></a>Leistung BIziel

Satz ** aktiviert ** ** Ja ** um die ER-Konfiguration verwendet werden soll, um die Übertragung von Daten aus der Instanz von Microsoft Dynamics 365 für Arbeitsgänge zu den Microsoft-Energie BI-Dienstleistungen anzuordnen. Die übertragenen Dateien werden in einer Microsoft SharePoint Server-Instanz gespeichert, die zu diesem Zweck muss konfiguriert werden. Weitere Informationen finden Sie [Verwenden der elektronischen Berichterstellungskonfiguration, um BI Leistung mit Daten von Microsoft Dynamics 365]" Arbeitsgänge für general-electronic-reporting-report-configuration-get-data-powerbi.md) zu ermöglichen. **Tipp:** Zum Überschreiben des Standardverhaltens (das Dialogfeld für eine Konfiguration) können Sie einen Zielverweis und ein Dateiziel für die Hauptausgabekomponente erstellen und alle Ziele deaktivieren.

## <a name="security-considerations"></a>Sicherheitsaspekte
Für ER Ziele werden zwei Arten von Rechte und Pflichten verwendet. Ein Typ steuert die Möglichkeit, die Gesamtziele verwalten, die für eine juristische Person konfiguriert werden (das heißt, steuert sie Zugriff auf die elektronische Berichterstellungsziele ** ** Seite ). Der andere Typ steuert die Möglichkeit eines Benutzers der Anwendung, zur Laufzeit die Zieleinstellung zu überschreiben, die von einem ER-Entwickler oder vom funktionaler Berater konfiguriert wurden.

| Rolle (Name der AOT/Entwicklungsumgebung)                     | Rollenname                                  | Berechtigungen (Name der AOT/Entwicklungsumgebung)                     | Name der Berechtigungen                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Entwickler für elektronische Berichterstellung             | ERFormatDestinationConfigure        | Zielort für elektronisches Berichtsformat konfigurieren                |
| ERFunctionalConsultant              | Funktionaler Berater für elektronische Berichterstellung | ERFormatDestinationConfigure        | Zielort für elektronisches Berichtsformat konfigurieren                |
| PaymAccountsPayablePaymentsClerk    | Sachbearbeiter Kreditorenkontozahlungen            | ERFormatDestinationRuntimeConfigure | Zielort für elektronisches Berichtsformat zur Laufzeit konfigurieren |
| PaymAccountsReceivablePaymentsClerk | Sachbearbeiter Debitorenkontenzahlungen         | ERFormatDestinationRuntimeConfigure | Zielort für elektronisches Berichtsformat zur Laufzeit konfigurieren |

**Hinweis:** In der vorherigen Aufgaben werden zwei Rechte verwendet. Diese Berechtigungen haben dieselben Namen wie die entsprechenden Aufgaben: **ERFormatDestinationConfigure** und **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Ich habe elektronische Konfigurationen importiert und sehe sie auf der Seite "Elektronische Berichterstellung". Will warum nicht sehe ich sie auf der elektronischen Berichterstellungszielseite?

Überprüfen Sie, ob Sie klicken ** neu ** und anschließend auf eine Variante im Feld Referenz ** ** Feld auswählen. Auf der **Ziele für die elektronische Berichterstellung**-Seite sehen Sie nur die Konfigurationen, für die Ziele konfiguriert wurden.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Gibt es eine Weise definieren, die Azure, Speicherkontoen- und Azure-BLOB-Speicher verwendet werden?

Nr. Der Standardwert Azure BLOB-Speicher, der für die Dokumentverwaltung verwendet wird und definiert, wird verwendet.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Welches ist im Dateiziels in den Zieleinstellungen? Was bewirkt diese Einstellung?

Das **Datei**-ziel dient zur Steuerung eines Dialogfelds. Wenn Sie dieses Feld aktivieren oder wenn kein Ziel für eine Konfiguration festgelegt wird, finden Sie ein offenes oder Abwehrdialogfeld, nach einer Ausgabedatei erstellt wurde.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Bitte geben Sie ein Beispiel für eine Formel, die auf ein Kreditorenkonto verweist, an das ich E-Mail senden kann.

Die Formel ist für die ER-Konfiguration spezifisch. Wenn Sie beispielsweise die ISO 20022-Kreditübertragunskonfiguration verwenden, dann können Sie **'$PaymentsForCoveringLetter'. Creditor.Identification.SourceID** oder **Modell. Payments.Creditor.Identification.SourceID** verwenden, um das zugeordnete Kreditorenkonto zu erhalten.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Eine meiner Formatkonfigurationen enthält mehrere Dateien, die in einem Ordner Gruppoert sind (z. B. Ordner1, der Datei1, Datei2 und Datei3 enthält). Wie richte ich Ziele ein, damit Ordner1.zip ist nicht erstellt wird, Datei1 per E-Mail gesendet wird, Datei2 an SharePoint gesendet wird und ich Datei3 direkt nach der Ausführung der Konfiguration öffnen kann?

Die Voraussetzung ist, dass im Format in den ER-Konfigurationen verfügbar sein muss. Öffnen Sie das Format haben, öffnen Sie die Seite **Ziel für elektronische Berichterstellung**, und erstellen Sie eine neue Referenz zu dieser Konfiguration. Sie müssen dann über vier Dateiziele verfügen – eine für jede Komponente. Erstellen Sie das erste Ziel, geben sie ihm einen Namen (z. B. **Ordner**), und wählen Sie einen Dateinamen, die einen Ordner in Ihrer Konfiguration darstellt. Klicken Sie dann auf **Einstellungen**, und stellen Sie sicher, dass alle Ziele deaktiviert sind. Für dieses Dateiziel wird kein Ordner erstellt. Aufgrund der hierarchischen Abhängigkeiten zwischen Dateien und übergeordneten Ordner verhalten sich die Dateien genauso. Sie werden also auch nicht gesendet. Um dieses Standardverhalten zu überschreiben, müssen Sie drei weitere Datei Ziele für jede Datei erstellen. In jeder Zieleinstellungen müssen Sie das Ziel aktivieren, an das die Datei gesendet werden soll.

# <a name="see-also"></a>Siehe auch

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)


