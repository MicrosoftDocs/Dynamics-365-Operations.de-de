---
title: MwSt.-Erklärung (Dänemark)
description: In diesem Thema wird erläutert, wie Sie eine Umsatzsteuervoranmeldung für Dänemark einrichten und erstellen.
author: anasyash
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 4d4a1185fa3c3b059744018b6e4e195de07126c9
ms.sourcegitcommit: 9c19898e1f41495f804c7f07e2636b53a098c4c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2022
ms.locfileid: "8402983"
---
# <a name="vat-declaration-denmark"></a>MwSt.-Erklärung (Dänemark)

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die MwSt.- bzw. Mehrwertsteuererklärung für Dänemark einrichten und eine Vorschau in Microsoft Excel anzeigen.

Um den Bericht automatisch zu erstellen, erstellen Sie zunächst genügend Mehrwertsteuercodes, um für jedes Feld in der Mehrwertsteuervoranmeldung eine separate Mehrwertsteuerabrechnung zu führen. Verknüpfen Sie außerdem in den anwendungsspezifischen Parametern des Formats für die elektronische Berichterstellung (ER) für die Umsatzsteuervoranmeldung Mehrwertsteuercodes mit dem Ergebnis der Suche nach den Feldern in der Umsatzsteuererklärung.

Für Dänemark müssen Sie **Nachschlagen von Berichtfeldern** konfigurieren. Weitere Informationen zum Einrichten anwendungsspezifischer Parameter finden Sie im Abschnitt [Anwendungsspezifische Parameter für Umsatzsteuererklärungsfelder einrichten](#set-up-application-specific-parameters) weiter unten in diesem Thema.

In der folgenden Tabelle zeigt die Spalte „Suchergebnis“ das Suchergebnis, das für eine bestimmte Mehrwertsteuererklärungszeile im Mehrwertsteuererklärungsformat vorkonfiguriert ist. Verwenden Sie diese Informationen, um die Mehrwertsteuercodes dem Suchergebnis und dann der Zeile der Mehrwertsteuererklärung korrekt zuzuordnen.

### <a name="vat-declaration-overview"></a>Übersicht über die Umsatzsteuererklärung

Die Mehrwertsteuererklärung in Dänemark enthält folgende Informationen.

**VAT-Zahlung**

| Description                                                  | Steuerbemessungsgrundlage/Steuerbetrag | Suchergebnis/Summe                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ausgangssteuer                                                   | Umsatzsteuer          | **OutputVAT**</br> **DomesticVATUseTax** (wird auch im Feld „Vorsteuer“ ausgewiesen)                                                                                                                                                                                                                                                                       |
| MwSt. auf im Ausland bezogene Waren usw.                           | Umsatzsteuer          | **PurchaseGoodsAbroad**</br>**PurchaseGoodsAbroadUseTax** (wird auch im Feld „Vorsteuer“ ausgewiesen)</br>**PurchaseGoodsEU** (Die Steuerbemessungsgrundlage wird in „Feld A – Erwerb von Waren“ ausgewiesen.)</br>**PurchaseGoodsEUUseTax** (Der Steuerbetrag wird auch im Feld „Vorsteuer“ ausgewiesen. Die Steuerbemessungsgrundlage wird in „Feld A – Erwerb von Waren“ ausgewiesen.)                   |
| MwSt. auf im Ausland erworbene Dienstleistungen, die einer Verlagerung der Steuerschuld unterliegen | Umsatzsteuer          | **PurchaseServicesAbroad**</br> **PurchaseServicesAbroadUseTax** (wird auch im Feld „Vorsteuer“ ausgewiesen)</br>**PurchaseServicesEU** (Die Steuerbemessungsgrundlage wird in „Feld A – Erwerb von Dienstleistungen“ ausgewiesen.)</br>**PurchaseServicesEUUseTax** (Der Steuerbetrag wird auch im Feld „Vorsteuer“ ausgewiesen. Die Steuerbemessungsgrundlage wird in „Feld A – Erwerb von Dienstleistungen“ ausgewiesen.) |
| Fällige Gesamtsumme                                                | Umsatzsteuer          | Summe der vorherigen drei Felder                                                                                                                                                                                                                                                                                                            |

**Abzüge**

| Description                                                                               | Steuerbemessungsgrundlage/Steuerbetrag | Suchergebnis/Summe                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorsteuer                                                                                 | Umsatzsteuer          | **InputVAT**</br> **DomesticVATUseTax** (wird auch im Feld „Ausgangssteuer“ ausgewiesen)</br>**PurchaseGoodsAbroadUseTax** (auch ausgewiesen im Feld „MwSt. auf im Ausland bezogene Waren usw.“)</br>**PurchaseServicesAbroadUseTax** (auch ausgewiesen im Feld „MwSt. auf im Ausland bezogene Dienstleistungen mit Verlagerung der Steuerschuld“)</br>**PurchaseGoodsEUUseTax** (auch ausgewiesen im Feld „MwSt. auf im Ausland bezogenen Waren usw.“)</br> **PurchaseServicesEUUseTax** (auch ausgewiesen im Feld „MwSt. auf im Ausland bezogene Dienstleistungen mit Verlagerung der Steuerschuld“) |
| Öl- und Flaschengasabgabe                                                                  | Umsatzsteuer          | **OilGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Erdgas- und Stadtgasabgabe                                                             | Umsatzsteuer          | **NaturalTownGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Kohlenstoffabgabe                                                                               | Umsatzsteuer          | **CarbonDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| CO2Duty                                                                                   | Umsatzsteuer          | **CO2Duty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Wasserabgabe                                                                              | Umsatzsteuer          | **WaterCharge**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Gesamte Abzüge                                                                          | Umsatzsteuer          | Summe der vorherigen sechs Felder                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Gesamtbetrag der Abgaben (positiver Betrag = Zahlung, negativer Betrag = Rückerstattung) | Umsatzsteuer          | „Zu zahlender Gesamtbetrag“ – „Gesamtbetrag der Abzüge“                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

**Zusätzliche Informationen**

| Description                                                                                                                                                                                                                                | Steuerbemessungsgrundlage/Steuerbetrag | Suchergebnis/Summe                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-------------------------------------------------|
| Feld A – Erwerb von Waren. Der Wert ohne MwSt. des innergemeinschaftlichen Erwerbs von Waren.                                                                                                                                                   | Bemessungsgrundlage            | **PurchaseGoodsEU PurchaseGoodsEUUseTax**       |
| Feld A – Erwerb von Dienstleistungen. Der Wert ohne MwSt. des innergemeinschaftlichen Erwerbs von Dienstleistungen.                                                                                                                                             | Bemessungsgrundlage            | **PurchaseServicesEU PurchaseServicesEUUseTax** |
| Feld B – Warenlieferung – zu melden an „EU-Verkäufe ohne MwSt.“/DK VIES. Der Wert ohne MwSt. der innergemeinschaftlichen Lieferung von Waren                                                                                                           | Bemessungsgrundlage            | **SalesGoodsEU**                                |
| Feld B – Lieferungen – nicht zu melden an „EU-Verkäufe ohne MwSt.“/DK VIES. Der Wert ohne MwSt. bestimmter innergemeinschaftlicher Lieferungen, z. B. Installation, Montage, Fernabsatz und neue Transportmittel an Nichtsteuerpflichtige. | Bemessungsgrundlage            | **SalesInstallationAssemblyEtcEU**              |
| Feld B – Erbringung von Dienstleistungen. Der umsatzsteuerfreie Wert der innergemeinschaftlichen Dienstleistungserbringung, für die der Erwerber die MwSt. als Verlagerung der Steuerschuld zahlen muss – muss ebenfalls an „EU-Verkäufe ohne MwSt.“/DK VIES gemeldet werden.                          | Bemessungsgrundlage            | **SalesServicesEU**                             |
| Feld C – andere Lieferungen. Wert der Lieferung anderer Waren und Dienstleistungen, die ohne Mehrwertsteuer im Hoheitsgebiet Dänemarks, in andere EU-Mitgliedstaaten und in Drittländer oder Drittgebiete geliefert werden.                                     | Bemessungsgrundlage            | **OtherSuppliesWithoutVAT**                     |

#### <a name="purchase-reverse-charge-vat"></a>Einkaufssteuerschuldumkehr

Wenn Sie Mehrwertsteuercodes so konfigurieren, dass eingehende Verlagerung der Steuerschuld unter Verwendung der Verbrauchsteuer gebucht wird, verknüpfen Sie Ihre Mehrwertsteuercodes mit dem Suchergebnis der **Nachschlagen von Berichtfeldern**, die „UseTax“ im Namen enthält.

Alternativ können Sie zwei separate Mehrwertsteuercodes konfigurieren: einen für die fällige Mehrwertsteuer und einen für den Mehrwertsteuerabzug. Verknüpfen Sie dann jeden Code mit den entsprechenden Lookup-Ergebnissen von **Nachschlagen von Berichtfeldern**.

Für steuerpflichtige innergemeinschaftliche Erwerbe konfigurieren Sie beispielsweise den Mehrwertsteuercode **UT_S_EU** mit der Verbrauchssteuer und verbinden ihn mit dem **PurchaseGoodsEUUseTax**-Suchergebnis von **Nachschlagen von Berichtfeldern**. In diesem Fall werden Steuerbeträge, die den **UT_S_EU**-Mehrwertsteuercode verwenden, in den Feldern „MwSt. auf im Ausland bezogene Waren usw.“ und „Vorsteuer“ wiedergegeben. Steuerbemessungsgrundlagen werden in „Feld A – Erwerb von Waren“ berücksichtigt.

Alternativ konfigurieren Sie zwei Umsatzsteuerkennzeichen:

- **VAT_S_EU**, das einen Steuersatz von -25 Prozent hat
- **InVAT_S_EU**, das einen Steuersatz von 25 Prozent hat

Verknüpfen Sie dann die Codes mit den Such-Ergebnissen von **Nachschlagen von Berichtfeldern** auf die folgende Weise:

- Ordnen Sie **VAT_S_EU** dem **PurchaseGoodsEU**-Nachschlageergebnis zu.
- Ordnen Sie **InVAT_S_EU** dem **InputVAT**-Nachschlageergebnis zu.

In diesem Fall werden Steuerbeträge, die den **VAT_S_EU**-Mehrwertsteuercode verwenden, in den Feldern „MwSt. auf im Ausland bezogene Waren usw.“ und „Feld A – Erwerb von Waren“ berücksichtigt. Beträge, die den **InVAT_S_EU**-Mehrwertsteuercode verwenden, werden im Feld „Vorsteuer“ wiedergegeben.

Weitere Informationen über die Konfiguration von Verlagerung der Steuerschuld finden Sie unter [Verlagerung der Steuerschuld](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Konfigurieren von Systemparametern

Um eine Mehrwertsteuererklärung zu erstellen, müssen Sie die Mehrwertsteuernummer konfigurieren.

1. Gehen Sie zu **Organisationsverwaltung** > **Organisationen** > **Juristische Personen**.
2. Wählen Sie die juristische Person und dann **Registrierungskennungen** aus.
3. Wählen oder erstellen Sie die Adresse in Dänemark und wählen Sie dann auf dem Inforegister **Registrierungskennungen** **Hinzufügen**.
4. Im Feld **Registrierungstyp** wählen Sie die Registrierungsart aus, die für Dänemark bestimmt ist und die die **MwSt.-ID**-Registrierungskategorie verwendet.
5. Geben Sie in das Feld **Registrierungsnummer** die Steuernummer ein.
6. Auf der **Allgemein**-Registerkarte geben Sie im Feld **In Kraft** das Datum ein, an dem die Nummer gültig wird.

Weitere Informationen zum Einrichten von Registrierungskategorien und Registrierungstypen finden Sie unter [Registrierungskennung](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-preview-for-denmark"></a>Vorschauversion der MwSt.-Erklärung für Dänemark einrichten

### <a name="import-er-configurations"></a>ER Konfigurationen importieren

Öffnen Sie den **Elektronische Berichterstattung**-Arbeitsbereich und importieren Sie das ER-Format **MwSt.-Erklärung Excel (DK)**.

Weitere Informationen finden Sie unter [Herunterladen von ER-Konfigurationen aus dem Global Repository des Konfigurationsdienstes](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters"></a>Anwendungsspezifische Parameter für Umsatzsteuererklärungsfelder einrichten

> [!NOTE]
> Es wird empfohlen, dass Sie die Funktion **Anwendungsspezifische Parameter aus früheren Versionen von ER-Formaten verwenden** im **Funktionsverwaltung**-Arbeitsbereich aktivieren. Wenn diese Funktion aktiviert ist, gelten Parameter, die für die frühere Version eines ER-Formats konfiguriert wurden, automatisch für die spätere Version desselben Formats. Wenn diese Funktion nicht aktiviert ist, müssen Sie anwendungsspezifische Parameter explizit für jede Formatversion konfigurieren. Die **Anwendungsspezifische Parameter aus früheren Versionen von ER-Formaten verwenden**-Funktion ist ab der Finance-Version 10.0.23 im **Funktionsverwaltung**-Arbeitsbereich verfügbar. Weitere Informationen zum Einrichten der Parameter eines ER-Formats für jede juristische Person finden Sie unter [Parameter eines ER-Formats pro juristischer Person einrichten](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Um automatisch eine MwSt.-Erklärung zu generieren, ordnen Sie der Anwendung Mehrwertsteuercodes zu und suchen Sie die Ergebnisse in der ER-Konfiguration.

Führen Sie diese Schritte aus, um zu definieren, welche Mehrwertsteuercodes welche Felder in der Mehrwertsteuererklärung generieren.

1. Gehen Sie zu **Arbeitsbereiche** > **Elektronisches Berichtswesen**, und wählen Sie dann **Berichtskonfigurationen**.
2. Wählen Sie die **MwSt.-Erklärung Excel (DK)**-Konfiguration, und wählen Sie dann **Konfigurationen \> Anwendungsspezifische Parametereinstellung**.
3. Wählen Sie auf der **Anwendungsspezifische Parameter**-Seite auf dem Inforegister **Nachschlagen** **Nachschlagen von Berichtfeldern**.
4. Legen Sie auf dem Inforegister **Bedingungen** die folgenden Felder fest, um die Mehrwertsteuercodes und Berichtsfelder zuzuordnen.

    | Feld                  | Description                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Suchergebnis          | Wählen Sie den Wert des Berichtsfelds aus. Weitere Informationen zu den Werten und deren Zuordnung zu den Umsatzsteuererklärungszeilen finden Sie im [Übersicht über die Umsatzsteuererklärung](#vat-declaration-overview)-Abschnitt weiter oben in diesem Thema.                                                                                               |
    | MwSt.-Code               | Wählen Sie den Mehrwertsteuercode aus, der mit dem Berichtsfeld verknüpft werden soll. Gebuchte Steuertransaktionen, die den ausgewählten Mehrwertsteuercode verwenden, werden im entsprechenden Deklarationsfeld erfasst. Wir empfehlen Ihnen, die Umsatzsteuerkennzeichen so zu trennen, dass ein Umsatzsteuerkennzeichen Beträge in nur einem Deklarationsfeld generiert. |
    | Transaktionsklassifizierer | Wenn Sie genügend Mehrwertsteuercodes erstellt haben, um ein Deklarationsfeld zu bestimmen, wählen Sie **\*Nicht leer\*** aus. Wenn Sie nicht genügend Mehrwertsteuercodes erstellt haben, damit ein Mehrwertsteuercode Beträge in nur einem Deklarationsfeld generiert, können Sie einen Transaktionsklassifizierer einrichten. Folgende Transaktionsklassifizierer sind verfügbar:</br>-   **Kaufen**</br>-   **PurchaseExempt** (Steuerbefreiter Einkauf)</br>-   **PurchaseReverseCharge** (Vorsteuer aus Verlagerung der Steuerschuld)</br>-   **Vertrieb**</br>-   **SalesExempt** (Steuerbefreiter Verkauf)</br>-   **SalesReverseCharge** (Vorsteuer aus Verlagerung der Steuerschuld Einkauf oder Verkauf)</br>-   **Steuer verwenden**. </br>Für jeden Transaktionsklassifizierer steht auch ein Klassifikator für die Gutschrift zur Verfügung. Einer dieser Klassifikatoren ist beispielsweise **PurchaseCreditNote** (Gutschrift kaufen).</br>Stellen Sie sicher, dass Sie für jeden Mehrwertsteuercode zwei Zeilen erstellen: eine mit dem Transaktionsklassifikatorwert und eine mit dem Transaktionsklassifikator für den Gutschriftswert. |


    > [!NOTE]
    > Verknüpfen Sie alle Mehrwertsteuercodes mit den Nachschlageergebnissen. Wenn Mehrwertsteuercodes keine Werte in der Mehrwertsteuererklärung generieren sollen, ordnen Sie sie dem **Sonstiges**-Nachschlageergebnis zu.

    ![Seite für anwendungsspezifische Parameter.](media/7db74920fad66a0db7fad60758698cc0.png)


5. Ändern Sie im Feld **Status** den Wert in **Abgeschlossen**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Richten Sie das Mehrwertsteuer-Berichtsformat für Vorschaubeträge in Excel ein

1. Suchen und wählen Sie im Arbeitsbereich **Funktionsverwaltung** die Funktion **MwSt.-Abrechnungs-Formatberichte** in der Liste und wählen Sie dann **Jetzt aktivieren** aus.
2. Wechseln Sie zu **Hauptbuch** > **Einrichtung** > **Hauptbuchparameter**.
3. Auf der **Mehrwertsteuer**-Registerkarte im Inforegister **Steueroptionen** im Feld **MwSt.-Abrechnungs-Formatzuordnung** wählen Sie das ER-Format **MwSt.-Erklärung Excel (DK)** aus.

   Dieses Format wird gedruckt, wenn Sie den **Mehrwertsteuer für Abrechnungszeitraum melden**-Bericht ausführen. Es wird auch gedruckt, wenn Sie **Drucken** auf der **Umsatzsteuerzahlungen**-Seite auswählen.

4. Auf der Seite **Steuerbehörden** wählen Sie die Steuerbehörde aus, und wählen Sie dann im **Berichtslayout**-Feld **Standard**.

Wenn Sie die Mehrwertsteuererklärung in einer juristischen Person konfigurieren, die über [mehrere MwSt.-Registrierungen](emea-reporting-for-multiple-vat-registrations.md) verfügt, folgen Sie diesen Schritten.

1. Gehen Sie zu **Hauptbuch** \> **Einrichtung** \> **Hauptbuchparameter**.
2. Auf der **Mehrwertsteuer**-Registerkarte, auf dem Inforegister **Elektronische Berichte für Länder/Regionen** in der Zeile für **DNK** wählen Sie das **MwSt.-Erklärung Excel (DK)**-ER-Format.

## <a name="set-up-electronic-messages"></a>Elektronische Nachrichten einrichten

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Laden und importieren Sie das Datenpaket mit Beispieleinstellungen für elektronische Nachrichten

Das Datenpaket enthält elektronische Nachrichteneinstellungen, die verwendet werden, um eine Vorschauversion der MwSt.-Erklärung in Excel anzuzeigen. Sie können diese Einstellungen erweitern oder eigene erstellen. Weitere Informationen zum Arbeiten mit elektronischen Nachrichten und zum Erstellen eigener Einstellungen finden Sie unter [Elektronische Nachrichtenübermittlung](../general-ledger/electronic-messaging.md).

1. In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) wählen Sie in der Bibliothek für freigegebene Anlagen **Datenpaket** als Anlagentyp und laden dann das **DK MwSt.-Erklärungspaket** herunter. Die heruntergeladene Datei heißt **DK VAT declaration package.zip**.
2. In Finance wählen Sie im **Datenverwaltung**-Arbeitsbereich **Importieren** aus.
3. Geben Sie auf dem Inforegister **Importieren** im Feld **Gruppenname** einen Namen für den Auftrag ein.
4. Wählen Sie im Inforegister **Ausgewählte Entitäten** **Datei hinzufügen** aus.
5. Im **Datei hinzufügen**-Dialogfeld überprüfen Sie, ob das **Quelldatenformat**-Feld auf **Paket** gesetzt ist, wählen **Hochladen und hinzufügen** aus und wählen dann die zuvor heruntergeladene ZIP-Datei aus.
6. Wählen Sie **Schließen** aus.
7. Nachdem die Datenentitäten hochgeladen wurden, wählen Sie im Aktivitätsbereich **Importieren**.
8. Gehen Sie zu **Steuer** > **Anfragen und Berichte** > **Elektronische Nachrichten** > **Elektronische Nachrichten**, und validieren Sie die importierte elektronische Nachrichtenverarbeitung (**DK MwSt.-Erklärung**).

### <a name="configure-electronic-messages"></a>Elektronische Nachrichten konfigurieren

1. Gehen Sie zu **Steuer** > **Einrichten** > **Elektronische Nachrichten** > **Datensatzauffüllungsaktivitäten**.
2. Wählen Sie die Zeile für **DK Umsatzsteuererklärungsdatensätze ausfüllen**, und wählen Sie dann **Abfrage bearbeiten**.
3. Verwenden Sie den Filter, um die Abrechnungszeiträume anzugeben, die in den Bericht aufgenommen werden sollen.
4. Wenn Sie Steuertransaktionen aus anderen Abrechnungszeiträumen in einer anderen Meldung melden müssen, erstellen Sie eine neue **Datensätze ausfüllen**-Aktion, und wählen Sie die entsprechenden Abrechnungszeiträume aus.

## <a name="preview-the-vat-declaration-in-excel"></a>Vorschau der Mehrwertsteuererklärung in Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a><a name="preview-vat-excel"></a>Vorschau der Mehrwertsteuererklärung in Excel aus der periodischen Aufgabe Umsatzsteuer für Abrechnungszeitraum melden

1. Wechseln Sie zu **Steuer** > **Periodische Aufgaben** > **Erklärungen** > **Mehrwertsteuer** > **Mehrwertsteuer für Abrechnungszeitraum melden**.
2. Wählen Sie im Feld **Abrechnungszeitraum** einen Wert aus.
3. Wählen Sie im Feld **Mehrwertsteuer, Zahlungsversion** einen der folgenden Werte aus:

    - **Original**: Generieren Sie einen Bericht für die Mehrwertsteuertransaktionen der ursprünglichen Mehrwertsteuerzahlung oder bevor die Mehrwertsteuerzahlung generiert wird.
    - **Korrekturen**: Einen Mehrwertsteuerbericht generieren für alle nachfolgenden Mehrwertsteuerzahlungen für das Periodenintervall.
    - **Gesamtliste**: Einen Mehrwertsteuerbericht generieren für alle Mehrwertsteuerbuchungen für das Periodenintervall, einschließlich der Originake und aller Korrekturen.

4. Wählen Sie im Feld **Von Datum** das Startdatum des Steuererklärungszeitraums aus.
5. **OK** wählen und den Excel-Bericht überprüfen.

### <a name="settle-and-post-sales-tax"></a>Mehrwertsteuer abrechnen und buchen

1. Wechseln Sie zu **Steuer** > **Periodische Aufgaben** > **Meldungen** > **Mehrwertsteuer** > **Mehrwertsteuer abrechnen und buchen**.
2. Wählen Sie im Feld **Abrechnungszeitraum** einen Wert aus.
3. Wählen Sie im Feld **Mehrwertsteuer, Zahlungsversion** einen der folgenden Werte aus:

    - **Original**: Generieren Sie die ursprüngliche Mehrwertsteuerzahlung für den Abrechnungszeitraum.
    - **Letzte Korrekturen**: Generieren Sie eine Korrekturumsatzsteuerzahlung, nachdem die ursprüngliche Umsatzsteuerzahlung für den Abrechnungszeitraum erstellt wurde.

4. Wählen Sie im Feld **Von Datum** das Startdatum des Steuererklärungszeitraums aus.
5. Wählen Sie **OK** aus.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Vorschau der Mehrwertsteuererklärung in Excel aus einer Mehrwertsteuerzahlung

1. Gehen Sie zu **Steuer** > **Anfragen und Berichte** > **Umsatzsteueranfragen** > **Umsatzsteuerzahlungen**, und wählen Sie eine Mehrwertsteuer-Zahlungszeile aus.
2. Wählen Sie **Bericht drucken** aus, und wählen Sie dann **OK** aus.
3. Überprüfen Sie die Excel-Datei, die für die ausgewählte Mehrwertsteuerzahlungszeile generiert wird.

> [!NOTE]
> Der Bericht wird nur für die ausgewählte Mehrwertsteuerzahlungszeile generiert. Wenn Sie z. B. eine Korrekturmeldung mit allen Korrekturen für die Periode oder eine Ersatzmeldung mit den Originaldaten und allen Korrekturen erstellen müssen, verwenden Sie die periodische Aufgabe **Mehrwertsteuer für Abrechnungszeitraum melden**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Erstellen Sie eine Mehrwertsteuererklärung aus elektronischen Nachrichten

Wenn Sie elektronische Nachrichten zum Generieren des Berichts verwenden, können Sie Steuerdaten von mehreren juristischen Personen erfassen. Weitere Informationen finden Sie im [Mehrwertsteuererklärung für mehrere juristische Personen ausführen](#run-vat-declaration)-Abschnitt weiter unten in diesem Thema.

Das folgende Verfahren gilt für das Beispiel für die Verarbeitung elektronischer Nachrichten, das Sie vorher aus der LCS-Bibliothek freigegebener Anlagen importiert haben.

1. Wechseln Sie zu **Steuer \> Abfragen und Berichte \> Elektronische Nachrichten \> Elektronische Nachrichten**.
2. Wählen Sie im linken Bereich **DK MwSt.-Erklärung**.
3. Auf dem Inforegister **Mitteilungen** wählen Sie **Neu** aus und dann im **Verarbeitung ausführen**-Dialogfeld **OK**.
4. Wählen Sie die erstellte Meldungszeile aus, geben Sie eine Beschreibung ein und geben Sie dann das Start- und Enddatum für die Meldung an.

   > [!NOTE]
   > Die Schritte 5 bis 7 sind optional.

5. Optional: Auf dem Inforegister **Mitteilungen** wählen Sie **Daten sammeln** aus, und wählen Sie dann **OK**. Die zuvor generierten Umsatzsteuerzahlungen werden der Nachricht hinzugefügt. Weitere Informationen finden Sie im Abschnitt [Mehrwertsteuer abrechnen und buchen](#settle-and-post-sales-tax) am Anfang dieses Themas. Wenn Sie diesen Schritt überspringen, können Sie trotzdem eine Umsatzsteuererklärung erstellen, indem Sie das **Version der Steuererklärung**-Feld im **Erklärung**-Dialogfeld verwenden.
6. Optional: Auf dem Inforegister **Nachrichtenelemente** überprüfen Sie die Mehrwertsteuerzahlungen, die zur Verarbeitung übertragen werden. Standardmäßig werden alle Mehrwertsteuerzahlungen des ausgewählten Zeitraums berücksichtigt, die in keiner anderen Nachricht derselben Verarbeitung enthalten waren.
7. Optional: Wählen Sie **Originaldokument**, um die Mehrwertsteuerzahlungen zu überprüfen, oder wählen Sie **Löschen**, um Mehrwertsteuerzahlungen von der Verarbeitung auszuschließen. Wenn Sie diesen Schritt überspringen, können Sie trotzdem eine Umsatzsteuererklärung erstellen, indem Sie das **Version der Steuererklärung**-Feld im **Erklärung**-Dialogfeld verwenden.
8. Wählen Sie im Inforegister **Nachrichten** **Status aktualisieren** aus. Im **Status aktualisieren**-Dialogfeld wählen Sie **Bereit zum Generieren**, und wählen Sie dann **OK**. Stellen Sie sicher, dass der Nachrichtenstatus geändert wurde in **Bereit zum Generieren**.
9. Wählen Sie **Bericht generieren** aus. Um die Beträge der Mehrwertsteuererklärung in der Vorschau anzuzeigen, wählen Sie im **Verarbeitung ausführen**-Dialogfeld **Vorschaubericht**, und wählen Sie dann **OK**.
10. Legen Sie im Dialogfeld **Elektronische Berichtsparameter** die Felder wie im Abschnitt [Vorschau der Mehrwertsteuererklärung in Excel aus der periodischen Aufgabe „Mehrwertsteuer für Abrechnungszeitraum melden“](#preview-vat-excel) weiter oben in diesem Thema beschrieben fest, und wählen Sie dann **OK** aus.
11. Wählen Sie die Schaltfläche **Anhänge** (Büroklammersymbol) in der oberen rechten Ecke der Seite und dann **Öffnen** aus, um die Datei zu öffnen. Prüfen Sie die Beträge im Excel-Dokument.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-vat-declaration"></a>Mehrwertsteuererklärung für mehrere juristische Personen ausführen

Um die Formate zum Melden der Umsatzsteuererklärung für eine Gruppe von juristischen Personen zu verwenden, müssen Sie zunächst die anwendungsspezifischen Parameter der ER-Formate für Umsatzsteuerkennzeichen aller erforderlichen juristischen Personen einrichten.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Richten Sie elektronische Nachrichten ein, um Steuerdaten von mehreren juristischen Personen zu sammeln

Befolgen Sie diese Schritte, um elektronische Nachrichten einzurichten, um Daten von mehreren juristischen Personen zu sammeln.

1. Wechseln Sie zu **Arbeitsbereiche** > **Funktionsverwaltung**.
2. Suchen und wählen Sie die **Unternehmensübergreifende Abfragen für Aktivitäten zum Auffüllen von Datensätzen**-Funktion in der Liste und wählen Sie dann **Jetzt aktivieren**.
3. Gehen Sie zu **Steuer** > **Einrichten** > **Elektronische Nachrichten** > **Datensatzauffüllungsaktivitäten**.
4. Auf der **Aktion zum Auffüllen von Datensätzen**-Seite wählen Sie die Zeile für **DK Umsatzsteuererklärungsdatensätze ausfüllen**.

   Im **Einrichtung von Datenquellen**-Raster ist ein neues **Unternehmen**-Feld vorhanden. Bei vorhandenen Datensätzen zeigt dieses Feld die Kennung der aktuellen juristischen Person an.

5. Im Raster **Einrichtung von Datenquellen** fügen Sie für jede weitere juristische Person, die in die Berichterstellung einbezogen werden muss, eine Zeile hinzu. Legen Sie für jede neue Zeile die folgenden Felder fest:

    | Feld                  | Description                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Name                   | Geben Sie einen Wert ein, der Ihnen hilft zu verstehen, woher dieser Datensatz stammt. Geben Sie beispielsweise **Umsatzsteuerzahlung der Tochtergesellschaft 1** ein. |
    | Nachrichtenelementtyp      | Wählen Sie **Umsatzsteuererklärung**. Dieser Wert ist der einzige Wert, der für alle Datensätze verfügbar ist.                                    |
    | Kontenart           | **Alle** auswählen.                                                                                                               |
    | Mastertabellenname      | Legen Sie **TaxReportVoucher** für alle Aufzeichnungen fest.                                                                             |
    | Feld „Dokumentnummer”  | Legen Sie **Beleg** für alle Aufzeichnungen fest.                                                                                      |
    | Feld „Dokumentdatum”    | Legen Sie **TransDate** für alle Aufzeichnungen fest.                                                                                    |
    | Feld „Dokumentenkonto” | Legen Sie **TaxPeriod** für alle Aufzeichnungen fest.                                                                                    |
    | Unternehmen                | Wählen Sie die ID der juristischen Person aus.                                                                                            |
    | Benutzerabfrage             | Dieses Kontrollkästchen wird automatisch aktiviert, wenn Sie Kriterien definieren, indem Sie **Abfrage bearbeiten** auswählen.                                 |

6. Wählen Sie für jede neue Zeile **Abfrage bearbeiten** aus und geben Sie eine Ausgleichsperiode an, das für die im Feld **Unternehmen** der Zeile angegebene juristische Person spezifisch ist.

Wenn die Einrichtung abgeschlossen ist, sammelt die **Daten sammeln**-Funktion auf der **Elektronische Nachrichten**-Seite Mehrwertsteuerzahlungen von allen juristischen Personen, die Sie definiert haben.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
