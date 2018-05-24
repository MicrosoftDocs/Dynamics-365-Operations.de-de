---
title: "Zielorte für elektronische Berichterstellung"
description: "Sie können ein Ziel für jede Formatvariante zur \"Elektronischen Berichterstellung\" (ER) und die Ausgabenkomponente (einen Ordner oder eine Datei) konfigurieren. Benutzer, die entsprechende Zugriffsrechte haben, können auch Zieleinstellungen zur Laufzeit ändern. Dieser Artikel beschreibt die ER Zielverwaltung, die unterstützten Zieltypen und die Sicherheitsaspekte."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fb7d0dc8b3ff9e8f1e4ade5cacfeed8f1a6871ab
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="electronic-reporting-destinations"></a>Zielorte für elektronische Berichterstellung

[!include [banner](../includes/banner.md)]

Sie können ein Ziel für jede Formatvariante zur "Elektronischen Berichterstellung" (ER) und die Ausgabenkomponente (einen Ordner oder eine Datei) konfigurieren. Benutzer, die entsprechende Zugriffsrechte haben, können auch Zieleinstellungen zur Laufzeit ändern. Dieser Artikel beschreibt die ER Zielverwaltung, die unterstützten Zieltypen und die Sicherheitsaspekte.

Die Formatkonfiguration für die elektronische Berichterstellung (ER) umfasst in der Regel mindestens eine Ausgabekomponente: eine Datei. Konfigurationen enthalten in der Regel mehrere Ausgabedatei-Komponenten verschiedener Typen (XML, TXT oder XLSX), die entweder in einen einzelnen Ordner oder mehrere Ordner gruppiert sind. Die ER-Zielverwaltung ermöglicht die Vorkonfiguration der Ausführung jeder Komponente. Standardmäßig wird dem Benutzer bei der Ausführung einer Konfiguration ein Dialogfeld angezeigt, das zum Speichern oder Öffnen der Datei verwendet wird. Dasselbe Verhalten wird auch beim Importieren einer ER-Konfiguration ohne spezifischen Ziele für diese verwendet. Nachdem ein Ziel für eine Hauptausgabekomponente erstellt wurde, überschreibt das Ziel das Standardverhalten und der Ordner oder die Datei wird entsprechend dem Ziel gesendet.

## <a name="availability-and-general-prerequisites"></a>Verfügbarkeit und allgemeine Voraussetzungen
Die Funktionalität für die ER-Ziele ist nicht in Microsoft Dynamics AX 7.0 (Februar 2016) verfügbar. Daher müssen Sie Microsoft Dynamics 365 for Operations, Version 1611 (November 2016) einrichten, um alle Funktionen zu verwenden, die in diesem Thema beschrieben sind. Alternativ können Sie eine der folgenden Komponenten installieren. Beachten Sie jedoch, dass diese Alternative eine eher begrenzte ER-Zielerfahrung bietet.

-   Microsoft Dynamics AX 7.0.1 (Mai 2016)
-   [Anwendungs-Hotfix](https://fix.lcs.dynamics.com/issue/results/?q=3160213) für die ER Zielverwaltung

Sie können Ziele nur für ER-Konfigurationen einrichten, die importiert wurden und für die Formate auf der Seite **Konfigurationen für die elektronische Berichterstellung** verfügbar sind.

## <a name="overview"></a>Überblick
Die ER-Zielverwaltungsfunktionalität steht unter **Organisationsverwaltung** &gt; **Elektronische Berichterstattung** bereit. Hier können Sie das Standardverhalten für eine Konfiguration überschreiben. Importierte Konfigurationen werden hier nicht angezeigt, bis Sie auf **Neu** klicken und dann im Feld **Verweis** eine Konfiguration für die Zieleinstellungen wählen.

[![Wählen Sie im Feld eine Konfigurationstechnologie aus](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Nachdem Sie einen Verweis erstellt haben, können Sie ein Ziel für jeden Ordner oder eine Datei erstellen. 

[![Erstellen Sie die Zieldatei.](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

> [!NOTE] 
> Sie können ein Dateiziel für jede Ausgabekomponente des gleichen Formats im Feld **Dateiname** erstellen (z. B. einen Ordner oder eine Datei). Sie können die Ziele für die Dateiziele im **Zieleinstellungen**-Dialogfeld separat aktivieren und deaktivieren. Die **Einstellungen**-Schaltfläche wird verwendet, um alle Ziele für eine ausgewählte Dateiziel steuern. Im **Zieleinstellungen**-Dialogfeld Sie können jedes Ziel separat steuern, indem Sie die **Aktiviert**-Option nutzen.

[![Dialogfeld Zieleinstellungen](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Zieltypen
Es werden verschiedene Zieltypen unterstützt. Sie können alle gleichzeitig aktivieren oder deaktivieren. Auf diese Weise können Sie entweder nichts machen, oder die Komponente an alle konfigurierten Ziele senden. In den folgenden Abschnitten werden die unterstützten Ziele beschrieben.

### <a name="email-destination"></a>E-Mail-Ziel

Legen Sie **Aktiviert** auf **Ja** fest, um eine Ausgabedatei per E-Mail zu senden. Wenn diese Option aktiviert ist, können Sie den E-Mail-Betreff bearbeiten und die E-Mail-Empfänger angeben. Sie können für den E-Mail-Betreff konstante Texte und den Text einrichten, oder Sie können ER-Formeln verwenden, um E-Mail-Texte dynamisch zu erstellen. Sie könnne E-Mail-Adressen für ER auf zwei Arten konfigurieren. Die Konfiguration kann auf die gleiche Wiese abgeschlossen werden, wie die Druckverwaltungsfunktion in Finance and Operations. Alternativ können Sie eine E-Mail-Adresse auflösen, indem Sie einen direkten Verweis auf die ER-Konfiguration mit einer Formel verwenden.

### <a name="email-address-types"></a>E-Mail-Adressen-Arten

Wenn Sie für das Feld **Zu** oder **CC** auf **Bearbeiten** klicken, erscheint das Dialogfeld **E-Mail an**. Sie können dann den Typ der E-Mail-Adresse auswählen, den Sie verwenden möchten.

[![E-Mail an Dialogfeld](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Druckverwaltung

Wenn Sie den Typ **Management E-Mail drucken** auswählen, können Sie die feste E-Mail-Adressen im Feld **An** eingeben. Um keine festen E-Mail-Adressen zu verwenden, müssen Sie die E-Mail-Herkunftsart für ein Ziel auswählen. Folgende Werte werden unterstützt: **Kunde**, **Lieferant**, **Interessent**, **Kontakt**, **Konkurrent**, **Arbeitskraft**, **Bewerber**, **Künftiger Kreditor** und **Unzulässiger Lieferant**. Nachdem Sie einen E-Mail-Quelltyp ausgewählt haben, verwenden Sie die Schaltfläche neben dem Feld **E-Mail-Quellkonto**, um das Formular **Formel-Designer** zu öffnen. Sie können dieses Formular verwenden, um eine Formel zuzuordnen, die das ausgewählte Parteienkonto mit dem E-Mail-Ziel darstellt.

[![Durckverwaltungs-E-Mail-Typ konfigurieren](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Beachten Sie, dass Formeln für die ER-Konfiguration spezifisch sind. Im Feld **Formel** geben Sie einen dokumentspezifischen Verweis auf einen Debitoren- oder Händlerparteityp ein. Anstelle es einzugeben, können Sie einen Datenquellknoten finden, der das Debitoren- oder Händlerkonto darstellt, und klicken Sie auf die Schaltfläche **Datenquelle hinzufügen**, um die Formel zu aktualisieren. Beispiel: Wenn Sie die Konfiguration "Kreditübertragung (ISO 20022)" verwenden, lautet der Knoten, der ein Händlerkonto darstellt, **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Andernfalls geben Sie einen beliebigen Zeichenfolgenwert ein, wie **DE-001**, um eine Formel zu speichern.

[![Formeldesigner](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

Im Dialogfeld **E-Mail an** klicken Sie auf den Papierkorb neben dem Feld **E-Mail-Quellkonto**, um die Formel zum E-Mail-Quellkonto dauerhaft zu löschen. Alternativ öffnen Sie den Formeldesigner, um eine Formel zu ändern, die zuvor gespeichert wurde. Wenn Sie E-Mail-Adressen zuweisen, klicken Sie auf **Bearbeiten**, um das Dialogfeld **E-Mail-Adresse zuweisen** zu öffnen.

[![E-Mail-Adressen einem E-Mail-Ziel zuweisen](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Konfigurations-E-Mail

Verwenden Sie diesen E-Mail-Typ, wenn die Konfiguration, die Sie verwenden, einen Knoten der Datenquellen hat, der eine E-Mail-Adresse ist. Sie können Datenquellen und Funktionen im Formeldesigner verwenden, um eine ordnungsgemäße formatierte E-Mail-Adresse abzurufen.

[![E-Mail-Adressen einem E-Mail-Ziel zuweisen](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Hinweis:** Ein SMTP-Server (Simple Mail Transfer Protocol) muss konfiguriert und verfügbar sein. Sie können Ihren SMTP-Server in Finance and Operations unter **Systemadministration** &gt; **Einrichten** &gt; **E-Mail** &gt; **E-Mail Parameter** angeben.

### <a name="archive-destination"></a>Archivziel

Mit dieser Option können Ausgaben als Microsoft SharePoint-Ordner oder Microsoft Azure Storage senden. Legen Sie **Aktiviert** auf **Ja** fest, um die Ausgabe an ein Ziel zu senden, das über den ausgewählten Dokumenttyp definiert ist. Nur Dokumenttypen mit der Gruppe **Datei** stehen zur Auswahl. Sie legen die Dokumenttypen unter **Organisationsadministration** &gt; **Dokumentenmanagement** &gt; **Dokumenttypen** fest. Die Konfiguration für ER-Ziele ist identisch mit der Konfiguration für das Dokumentverwaltungssystem.

[![Seite „Dokumenttypen”](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Der Speicherort bestimmt, wo die Datei gespeichert wird. Nachdem das Ziel **Archiv** aktiviert ist, können Sie die Ergebnisse der Konfigurationsausführung im Einzelvorgangsarchiv gespeichert werden. Sie können die Ergebnisse **Organisationsverwaltung** &gt; **Elektronische Berichterstattung** &gt; **Elektronische Berichterstellung archivierte Einzelvorgänge** anzeigen. **Hinweis** Sie können einen Dokumenttyp für das Einzelvorgangsarchiv in Finance and Operations **Organisationsverwaltung** &gt; **Arbeitsbereiche** &gt; **Elektronische Berichterstattung** &gt; **Elektronische Berichterstattungsparameter** auswählen.

#### <a name="sharepoint"></a>SharePoint

Sie können eine Datei in einem bestimmten SharePoint-Ordner speichern. Sie definieren den Standardwert SharePoint-Server unter: **Organisationsverwaltung** &gt; **Dokumentverwaltung** &gt; **Parameter der Dokumentverwaltung** auf der Registerkarte **SharePoint** . Nachdem der SharePoint-Ordner konfiguriert ist, können Sie diesen als den Ordner auswählen, in dem die ER-Ausgabe für den Dokumenttyp gespeichert wird. 

[![Einen SharePoint-Ordner auswählen](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure Storage

Wenn der Dokumenttypspeicherort auf **Archivverzeichnis** festgelegt ist, können Sie eine Datei in den Azure Storage speichern.

### <a name="file-destination"></a>Dateizielort

Legen Sie **Aktiviert** auf **Ja** fest, um das Öffnen- oder Speichern-Dialogfeld nach der Ausführung der Konfiguration anzuzeigen.

### <a name="screen-destination"></a>Bildschirmziel

Wenn Sie **Aktiviert** auf **Ja** setzen, wird eine Vorschau der Ausgabe erstellt werden. Sie können gewisse Dateitypen wie XML, TXT oder PDF direkt in einer Browserfenster anzeigen. Für andere Dateitypen wie Microsoft Excel oder Word wird der Microsoft Office Online-Service verwendet.

### <a name="power-bi-destination"></a>Power BI-Ziel

Setzen Sie **Aktiviert** auf **Ja**, um Ihre ER-Konfiguration zu verwenden, um die Übertragung von Daten aus Ihrer Instanz von Finance and Operations zu den Microsoft Power BI-Diensten zu veranlassen. Die übertragenen Dateien werden auf einem Microsoft SharePoint Server gespeichert, der für diesen Zweck konfiguriert wurde. Weitere Informationen finden Sie unter [Eine elektronische Berichtskonfiguration verwenden, um Power BI mit Daten aus Finance and Operations bereitzustellen](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Tipp:** Zum Überschreiben des Standardverhaltens (das Dialogfeld für eine Konfiguration) können Sie einen Zielverweis und ein Dateiziel für die Hauptausgabekomponente erstellen und alle Ziele deaktivieren.

## <a name="security-considerations"></a>Sicherheitsaspekte
Für ER Ziele werden zwei Arten von Rechte und Pflichten verwendet. Ein Typ steuert die Fähigkeit zur Pflege aller Ziele, die für eine juristische Person konfiguriert sind (steuert den Zugriff auf die **Elektronische Berichterstellung**-Seite). Der andere Typ steuert die Möglichkeit eines Benutzers der Anwendung, zur Laufzeit die Zieleinstellung zu überschreiben, die von einem ER-Entwickler oder vom funktionaler Berater konfiguriert wurden.

| Rolle (Name der AOT/Entwicklungsumgebung)                     | Rollenname                                  | Berechtigungen (Name der AOT/Entwicklungsumgebung)                     | Name der Berechtigungen                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Entwickler für elektronische Berichterstellung             | ERFormatDestinationConfigure        | Zielort für elektronisches Berichtsformat konfigurieren                |
| ERFunctionalConsultant              | Funktionaler Berater für elektronische Berichterstellung | ERFormatDestinationConfigure        | Zielort für elektronisches Berichtsformat konfigurieren                |
| PaymAccountsPayablePaymentsClerk    | Sachbearbeiter Kreditorenkontozahlungen            | ERFormatDestinationRuntimeConfigure | Zielort für elektronisches Berichtsformat zur Laufzeit konfigurieren |
| PaymAccountsReceivablePaymentsClerk | Sachbearbeiter Debitorenkontenzahlungen         | ERFormatDestinationRuntimeConfigure | Zielort für elektronisches Berichtsformat zur Laufzeit konfigurieren |

> [!NOTE]
> In der vorherigen Aufgaben werden zwei Rechte verwendet. Diese Berechtigungen haben dieselben Namen wie die entsprechenden Aufgaben: **ERFormatDestinationConfigure** und **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Ich habe elektronische Konfigurationen importiert und sehe sie auf der Seite "Elektronische Berichterstellung". Aber warum sehe ich sie nicht auf der Seite "Ziele für die elektronische Berichterstellung"?

Stellen Sie sicher, dass Sie auf **Neu** klicken und dann eine Konfiguration im Feld **Referenz** wählen. Auf der **Ziele für die elektronische Berichterstellung**-Seite sehen Sie nur die Konfigurationen, für die Ziele konfiguriert wurden.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Gibt es eine Möglichkeit zur Definition des verwendeten Azure Storage-Kontos und des Azure Blob-Speichers?

Nr. Nein. Der standardmäßige Azure Blob-Speicher, der definiert ist und für das Dokumentenmanagement-System verwendet wird, wird verwendet.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Wozu dient die Datei in den Zieleinstellungen? Was bewirkt diese Einstellung?

Das **Datei**-ziel dient zur Steuerung eines Dialogfelds. Wenn Sie dieses Ziel aktivieren oder wenn kein Ziel für eine Konfiguration definiert ist, sehen Sie ein Speichern- oder Öffnen-Dialogfeld nachdem eine Ausgabedatei erstellt.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Bitte geben Sie ein Beispiel für eine Formel, die auf ein Kreditorenkonto verweist, an das ich E-Mail senden kann.

Die Formel ist für die ER-Konfiguration spezifisch. Wenn Sie beispielsweise die ISO 20022-Kreditübertragunskonfiguration verwenden, dann können Sie **'$PaymentsForCoveringLetter'. Creditor.Identification.SourceID** oder **Modell. Payments.Creditor.Identification.SourceID** verwenden, um das zugeordnete Kreditorenkonto zu erhalten.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Eine meiner Formatkonfigurationen enthält mehrere Dateien, die in einem Ordner Gruppoert sind (z. B. Ordner1, der Datei1, Datei2 und Datei3 enthält). Wie richte ich Ziele ein, damit Ordner1.zip ist nicht erstellt wird, Datei1 per E-Mail gesendet wird, Datei2 an SharePoint gesendet wird und ich Datei3 direkt nach der Ausführung der Konfiguration öffnen kann?

Die Voraussetzung ist, dass das Format in ER-Konfigurationen verfügbar sein muss. Öffnen Sie das Format haben, öffnen Sie die Seite **Ziel für elektronische Berichterstellung**, und erstellen Sie eine neue Referenz zu dieser Konfiguration. Sie müssen dann über vier Dateiziele verfügen – eine für jede Komponente. Erstellen Sie das erste Ziel, geben sie ihm einen Namen (z. B. **Ordner**), und wählen Sie einen Dateinamen, die einen Ordner in Ihrer Konfiguration darstellt. Klicken Sie dann auf **Einstellungen**, und stellen Sie sicher, dass alle Ziele deaktiviert sind. Für dieses Dateiziel wird kein Ordner erstellt. Aufgrund der hierarchischen Abhängigkeiten zwischen Dateien und übergeordneten Ordner verhalten sich die Dateien genauso. Sie werden also auch nicht gesendet. Um dieses Standardverhalten zu überschreiben, müssen Sie drei weitere Datei Ziele für jede Datei erstellen. In jeder Zieleinstellungen müssen Sie das Ziel aktivieren, an das die Datei gesendet werden soll.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)




