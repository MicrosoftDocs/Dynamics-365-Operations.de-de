---
title: E-Mail-ER-Zieltyp
description: In diesem Artikel wird erläutert, wie für jede FOLDER- oder FILE-Komponente eines EB-Formats (elektronische Berichterstellung) ein E-Mail-Ziel konfiguriert wird.
author: kfend
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 97423
ms.assetid: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 5e58618618d9125db4c81f49f62f48c2ce2f5e62
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285424"
---
# <a name="email-er-destination-type"></a>E-Mail-ER-Zieltyp

[!include [banner](../includes/banner.md)]

Wenn ein EB-Format ausgeführt wird, können ein oder mehrere ausgehende Dokumente generiert werden. Die Formatkomponenten **Ordner** oder **Datei** werden in EB-Formaten verwendet, um die Struktur ausgehender Dokumente festzulegen. Sie können ein E-Mail-Ziel für diese Arten von Komponenten konfigurieren, um ausgehende Dokumente als E-Mail-Anhänge zu senden.

Sie können für jede **Ordner**- oder **Datei**-Komponente eines EB-Formats ein E-Mail-Ziel konfigurieren. In diesem Fall **wird jedes ausgehende Dokument einzeln per E-Mail gesendet**. Basierend auf dieser Zieleinstellung wird ein generiertes Dokument als Anhang einer E-Mail zugestellt. 

> [!NOTE]
> Wenn kein Dokument generiert wird, weil der Ausdruck **Aktiviert** für die relevante Komponente **Datei** so konfiguriert wurde, dass ein boolescher Wert **Falsch** zurückgegeben wird, wird selbst dann keine E-Mail gesendet, wenn für die Komponente ein E-Mail-Ziel konfiguriert und aktiviert ist.

Auch die [Gruppierung](#grouping) mehrerer **Ordner**- oder **Datei**-Komponenten ist möglich, wobei Sie anschließend ein E-Mail-Ziel für alle Komponenten in der Gruppe konfigurieren können. In diesem Fall werden alle ausgehenden Dokumente, die von Komponenten generiert werden, die zu der Gruppe gehören, **als mehrere Anhänge einer einzelnen E-Mail gesendet**. Basierend auf dieser Zieleinstellung wird jedes generierte Dokument als Anhang einer einzelnen E-Mail zugestellt.

> [!NOTE]
> Wenn mindestens ein Dokument von einer **Datei**-Komponente in einer Gruppe von Komponenten generiert wird, wird eine E-Mail gesendet. Wenn kein Dokument von gruppierten Komponenten generiert wird, weil der Ausdruck **Aktiviert** für jede Komponente **Datei** so konfiguriert wurde, dass ein boolescher Wert **Falsch** zurückgegeben wird, wird selbst dann keine E-Mail gesendet, wenn für diese Gruppe von Komponenten ein E-Mail-Ziel konfiguriert und aktiviert ist.
>
> **E-Mail** ist das einzige Ziel, das für eine Gruppe von Komponenten konfiguriert werden kann. Fügen Sie einen weiteren Zieldatensatz hinzu, wählen Sie die gewünschte Komponente aus und konfigurieren Sie ein anderes Ziel für diesen Datensatz, um ein Dokument zu versenden, das basierend auf der E-Mail-Zieleinstellung für eine Gruppe per E-Mail gesendet werden soll.

Für eine einzelne EB-Formatkonfiguration können mehrere Gruppen von Komponenten konfiguriert werden. Auf diese Weise können Sie für jede Gruppe von Komponenten sowie für jede Komponente ein E-Mail-Ziel konfigurieren.

## <a name="enable-an-email-destination"></a>Ein E-Mail-Ziel aktivieren

Gehen Sie folgendermaßen vor, um eine oder mehrere Ausgabedateien per E-Mail zu senden.

1. Auf der Seite **Ziel der elektronischen Berichterstellung** wählen Sie im Inforegister **Dateiziel** im Raster eine Komponente oder Gruppe von Komponenten aus.
2. Wählen Sie **Einstellungen** und setzen Sie dann im Dialogfeld **Zieleinstellungen** auf der Registerkarte **E-Mail** die Option **Aktiviert** auf **Ja** fest.

[![Festlegen der Option „Aktiviert“ für ein E-Mail-Ziel auf „Ja“.](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="configure-an-email-destination"></a>Ein E-Mail-Ziel konfigurieren

### <a name="email-content"></a>Inhalt der E-Mail

Sie können den Betreff und den Textkörper der E-Mail-Nachricht bearbeiten.

Geben Sie in das Feld **Betreff** den Text des E-Mail-Betreffs ein, der im Betreff-Feld einer elektronischen Nachricht erscheinen soll, die zur Laufzeit erzeugt wird. Geben Sie in das Feld **Body** den Text des E-Mail-Bodys ein, der im Body-Feld einer elektronischen Nachricht erscheinen soll. Sie können einen konstanten Text für den E-Mail-Betreff und den Textkörper festlegen, oder Sie können ER [Formeln](er-formula-language.md) verwenden, um den E-Mail-Text dynamisch zur Laufzeit zu erstellen. Die konfigurierte Formel muss einen Wert vom Typ [String](er-formula-supported-data-types-primitive.md#string) zurückgeben.

Der Textkörper Ihrer E-Mail wird im TEXT- oder HTML-Format verfasst, je nach E-Mail Client. Sie können jedes für HTML- und Inline-Cascading Style Sheets verwenden (CSS) zulässige Layout, Stilelement und Branding.

> [!NOTE]
> E-Mail-Clients legen Layout- und Stilbeschränkungen fest, die möglicherweise Anpassungen an HTML und CSS erfordern, die Sie für den Nachrichtentext verwenden. Wir empfehlen Ihnen, sich mit den bewährten Verfahren zum Erstellen von HTML vertraut zu machen, die von den gängigsten E-Mail-Clients unterstützt werden.
>
> Verwenden Sie die richtige Kodierung, um einen Wagenrücklauf zu implementieren, abhängig von der Formatierung des Textkörpers. Weitere Informationen finden Sie in der Definition des Datentyps [String](er-formula-supported-data-types-primitive.md#string).

### <a name="email-addresses"></a>E-Mail-Adressen

Sie können den E-Mail-Absender und die E-Mail-Empfänger angeben. Standardmäßig wird die E-Mail im Namen des aktuellen Benutzers gesendet. Um einen anderen E-Mail-Sender anzugeben, müssen Sie das Feld **Von** konfigurieren.

> [!NOTE]
> Wenn ein E-Mail-Ziel konfiguriert ist, ist das Feld **Von** nur für Benutzer sichtbar, die über das `ERFormatDestinationSenderEmailConfigure`-Sicherheitsprivileg **Die Sender-E-Mail-Adresse für EB-Formatziele konfigurieren** verfügen.
>
> Wenn ein E-Mail-Ziel zur Änderung bei der [Runtime](electronic-reporting-destinations.md#security-considerations) angeboten wird, ist das Feld **Von** nur für Benutzer sichtbar, die über das `ERFormatDestinationSenderEmailMaintain`-Sicherheitsprivileg **Die Sender-E-Mail-Adresse für EB-Formatziel beibehalten** verfügen.
>
> Wenn das Feld **Von** so konfiguriert ist, dass eine andere E-Mail-Adresse als die des aktuellen Benutzers verwendet wird, muss entweder die **Senden als**- oder **Senden im Auftrag von**-Berechtigung im Voraus richtig [eingestellt](/microsoft-365/solutions/allow-members-to-send-as-or-send-on-behalf-of-group) sein. Andernfalls wird zur Runtime die folgende Ausnahme geworfen: „E-Mail konnte nicht als \<from email account\> von dem \<current user account\>-Konto gesendet werden. Bitte überprüfen Sie die ‚Senden als‘-Berechtigungen auf dem \<from email account\>.“

Sie können das Feld **Von** konfigurieren, um mehr als eine E-Mail-Adresse zurückzugeben. In diesem Fall wird die erste Adresse in der Liste als E-Mail-Senderadresse verwendet.

Um E-Mail-Empfänger anzugeben, müssen Sie die (optionalen) Felder **An** und **CC**.

Sie könnne E-Mail-Adressen für ER auf zwei Arten konfigurieren. Die Konfiguration kann auf dieselbe Weise abgeschlossen werden wie die Druckverwaltungsfunktion. Sie können auch eine E-Mail-Adresse auflösen, indem Sie einen direkten Verweis auf die EB-Konfiguration über eine Formel erstellen.

## <a name="email-address-types"></a>E-Mail-Adressen-Arten

Wenn Sie **Bearbeiten** neben dem Feld **Von**, **An** oder **CC** im Dialogfeld **Zieleinstellungen** auswählen, wird das entsprechende Dialogfeld **E-Mail von**, **E-Mail an** oder **E-Mail CC** angezeigt. Dort können Sie den E-Mail-Sender und E-Mail-Empfänger konfigurieren. Wählen Sie **Hinzufügen** aus und wählen Sie dann den Typ der zu verwendenden E-Mail-Adresse aus. Derzeit werden zwei Typen unterstützt: **Druckverwaltung** und **Konfiguration**.

[![Typ der E-Mail-Adresse auswählen.](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>Verwaltungs-E-Mail ausdrucken

Wenn Sie **Druckverwaltung-E-Mail** als Typ der E-Mail-Adresse auswählen, können Sie im Dialogfeld **E-Mail von**, **E-Mail an** oder **E-Mail CC** als feste E-Mail-Adressen eingeben, indem Sie folgende Felder festlegen:

- Wählen Sie im Feld **E-Mail-Quelle** die Option **Keine** aus.
- Geben Sie im Feld **Zusätzliche E-Mail-Adressen, getrennt durch ";"** die festen E-Mail-Adressen ein.

Alternativ können Sie E-Mail-Adressen aus den Kontaktdaten der Partei beziehen, für die Sie ein ausgehendes Dokument erstellen. Um keine festen E-Mail-Adressen zu verwenden, wählen Sie im Feld **E-Mail-Quelle** die [Rolle](../../fin-ops/organization-administration/overview-global-address-book.md#party-roles) der Partei für ein Dateiziel aus. Folgende Rollen werden unterstützt:

- Debitor
- Lieferant
- Interessent
- Kontakt
- Mitbewerber
- Worker
- Bewerber
- Künftiger Kreditor
- Unzulässiger Kreditor
- Juristische Person

Um beispielsweise ein E-Mail-Ziel für ein EB-Format zu konfigurieren, das zur Verarbeitung von Lieferantenzahlungen verwendet wird, wählen Sie die Rolle **Lieferant** aus.

Nachdem Sie die gewünschte Rolle ausgewählt haben, wählen Sie die Schaltfläche **Binden** (Kettensymbol) neben dem Feld **E-Mail-Quellkonto** aus, um die Seite [Formeldesigner](general-electronic-reporting-formula-designer.md) zu öffnen. Auf dieser Seite können Sie dann eine Formel konfigurieren, die zur Laufzeit die Kontonummer der Partei zurückgibt, die der konfigurierten Rolle über das verarbeitete Dokument zum E-Mail-Ziel zugewiesen wird.

> [!NOTE]
> Formeln sind für die ER-Konfiguration spezifisch sind.

Geben Sie auf der Seite **Formeldesigner** in das Feld **Formel** einen dokumentspezifischen Verweis auf eine unterstützte Rolle ein. Anstatt die Referenz einzugeben, suchen Sie im Bereich **Datenquelle** den Datenquellenknoten, der ein Konto der konfigurierten Rolle darstellt, und wählen ihn aus. Wählen Sie dann **Datenquelle hinzufügen** aus, um die Formel zu aktualisieren. Wenn Sie beispielsweise das E-Mail-Ziel für die Konfiguration **Kreditübertragung (ISO 20022)** konfigurieren, die zur Verarbeitung von Lieferantenzahlungen verwendet wird, ist es der Knoten `'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`, der ein Lieferantenkonto darstellt.

![Ein E-Mail-Quellkonto konfigurieren.](./media/er_destinations-emaildefineaddresssource.gif)

Wenn die Kontonummern der konfigurierten Rolle für die gesamte Instanz von Microsoft Dynamics 365 Finance eindeutig sind, kann das Feld **Unternehmen aus der E-Mail-Quelle** im Dialogfeld **E-Mail an** leer bleiben.

Alternativ kann es vorkommen, dass verschiedene Parteien im [globalen Adressbuch](../../fin-ops/organization-administration/overview-global-address-book.md) in verschiedenen Unternehmen auf eine Weise als ([juristische Personen](../../fin-ops/organization-administration/organizations-organizational-hierarchies.md#legal-entities)) registriert wurden, dass alle dieselbe Kontonummer verwenden, um die konfigurierte Rolle auszufüllen. In diesem Fall sind die Kontonummern für die konfigurierte Rolle nicht für die gesamte Instanz von Finance eindeutig. Um eine Partei explizit auszuwählen, können Sie daher nicht nur eine Kontonummer angeben. Sie müssen auch das Unternehmen angeben, in dessen Geltungsbereich die Partei registriert wurde, um die konfigurierte Rolle auszufüllen. Wählen Sie die Schaltfläche **Binden** (Kettensymbol) neben dem Feld **Unternehmen der E-Mail-Quelle** im Feld **E-Mail an** aus, um die Seite [Formeldesigner](general-electronic-reporting-formula-designer.md) zu öffnen. Auf dieser Seite können Sie dann eine Formel konfigurieren, die zur Laufzeit den Code des Unternehmens zurückgibt, in dessen Geltungsbereich die gewünschte Quelle gefunden werden muss.

> [!TIP]
> Wenn Sie den Buchungskreis verwenden müssen, um ein EB-Format auszuführen, das EB-Format jedoch keine Datenquelle bereitstellt, aus der der Buchungskreis abgerufen werden kann, konfigurieren Sie die Formel `GetCurrentCompany()` unter Verwendung der integrierten EB-Funktion [GETCURRENTCOMPANY](er-functions-other-getcurrentcompany.md).

> [!NOTE]
> Formeln sind für die ER-Konfiguration spezifisch sind.

Um den Typ der E-Mail-Adressen anzugeben, die zur Laufzeit verwendet werden müssen, wählen Sie im Dialogfeld **E-Mail an** die Option **Bearbeiten** neben dem Feld **An** aus, um das Dropdown-Dialogfeld **E-Mail-Adresse zuweisen** zu öffnen. Legen Sie anschließend die folgenden Felder fest:

- Wählen Sie im Feld **Zweck** die gewünschten Zwecke aus. Es werden nur E-Mail-Adressen für die ausgewählten Zwecke von Kontakten der erkannten Partei verwendet.
- Legen Sie die Option **Hauptansprechpartner** auf **Ja** fest, um eine E-Mail-Adresse zu verwenden, die für die erkannte Partei als primäre E-Mail-Adresse konfiguriert ist.

> [!NOTE]
> Wenn Zwecke im Feld **Zweck** ausgewählt sind und gleichzeitig die Option **Hauptansprechpartner** auf **Ja** festgelegt ist, wird jede E-Mail, die mindestens ein konfiguriertes Kriterium erfüllt, zur Laufzeit verwendet.

### <a name="configuration-email"></a>Konfigurations-E-Mail

Wählen Sie **Konfigurations-E-Mail** als E-Mail-Adresstyp aus, wenn die von Ihnen verwendete Konfiguration einen Knoten in den Datenquellen enthält, der entweder eine einzelne E-Mail-Adresse oder mehrere E-Mail-Adressen zurückgibt, die durch Semikolons (;) getrennt sind. Sie können Datenquellen und [Funktionen](er-formula-language.md#Functions) im Formeldesigner verwenden, um eine korrekt formatierte E-Mail-Adresse oder korrekt formatierte E-Mail-Adressen zu erhalten, die durch Semikolons getrennt sind. Wenn Sie beispielsweise die Konfiguration **Kreditübertragung (ISO 20022)** verwenden, ist es der Knoten `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`, der die primäre E-Mail-Adresse eines Lieferanten aus den Kontaktdaten des Lieferanten darstellt, an die das Anschreiben gesendet werden soll.

[![Eine Quelle für E-Mail-Adressen konfigurieren.](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="group-format-components"></a><a id="grouping"></a>Formatkomponenten gruppieren

Um Formatkomponenten zu gruppieren, wählen Sie auf der Seite **Ziel der elektronischen Berichterstellung** im Inforegister **Dateiziel** im Raster die Komponenten aus. Wählen Sie dann **Gruppe** aus.

**E-Mail** ist das einzige zuvor konfigurierte Ziel, das für die ausgewählten Komponenten noch verfügbar ist. Es sind keine anderen zuvor konfigurierten Ziele verfügbar, da sie für eine Gruppe von Komponenten als nicht unterstützt gelten. Sie werden über diese Änderungen gegebenenfalls informiert.

Der zuvor hinzugefügte Datensatz wird als Kopfzeile der erstellten Gruppe betrachtet. Dieser Kopfzeilen-Datensatz enthält die E-Mail-Zieleinstellungen für die Gruppe. Andere Datensätze sind Gruppenmitglieder, die die E-Mail-Zieleinstellungen des Kopfzeilen-Datensatzes der Gruppe verwenden.

Um die Gruppierung von Formatkomponenten aufzuheben, wählen Sie im Inforegister **Dateiziel** einen Datensatz aus, der zur Gruppe gehört, und wählen Sie dann **Gruppierung aufheben** aus.

- Wenn Sie einen Kopfzeilen-Datensatz auswählen, wird die Gruppierung für die gesamte Gruppe aufgehoben.
- Wenn Sie einen Mitgliedsdatensatz auswählen und dies der letzte Mitgliedsdatensatz in einer Gruppe ist, wird die Gruppierung für die gesamte Gruppe aufgehoben.
- Wenn Sie einen Mitgliedsdatensatz auswählen, der nicht der letzte Mitgliedsdatensatz in einer Gruppe ist, wird dieser Datensatz aus der aktuellen Gruppe ausgeschlossen.

Die folgende Abbildung zeigt die Struktur eines EB-Formats, das so konfiguriert wurde, dass eine komprimierte ausgehende Datei erstellt wird, die ein Mahnschreiben und entsprechende Kundenrechnungen im PDF-Format enthält.

[![Struktur eines EB-Formats, das ausgehende Dokumente generiert.](./media/ER_Destinations-Email-Grouping1.png)](./media/ER_Destinations-Email-Grouping1.png)

Die folgende Abbildung zeigt, wie einzelne Komponenten entsprechend der Beschreibung in diesem Artikel gruppiert werden und wie das **E-Mail**-Ziel für die neue Gruppe aktiviert wird, sodass ein Mahnschreiben zusammen mit den entsprechenden Kundenrechnungen als E-Mail-Anhang gesendet wird.

[![Einzelne Komponenten gruppieren und das E-Mail-Ziel aktivieren.](./media/ER_Destinations-Email-Grouping2.gif)](./media/ER_Destinations-Email-Grouping2.gif)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)
- [Zielorte für elektronische Berichterstellung (ER)](electronic-reporting-destinations.md)
- [Formeldesigner in der elektronischen Berichterstellung (EB)](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
