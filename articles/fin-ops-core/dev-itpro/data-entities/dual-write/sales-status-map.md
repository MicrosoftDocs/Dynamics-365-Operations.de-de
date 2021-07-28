---
title: Zuordnung für die Kundenauftragsstatusspalten einrichten
description: In diesem Thema wird erläutert, wie Sie die Auftragsstatusspalten für duales Schreiben einrichten.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: a1f85c100f1d062517c14d31a19838cc4af18f10
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346569"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a>Zuordnung für die Kundenauftragsstatusspalten einrichten

[!include [banner](../../includes/banner.md)]

Die Spalten, die den Auftragsstatus angeben, haben in Microsoft Dynamics 365 Supply Chain Management und Dynamics 365 Sales unterschiedliche Aufzählungswerte. Zusätzliche Einstellungen sind erforderlich, um diese Spalten in Dual-Write abzubilden.

## <a name="columns-in-supply-chain-management"></a>Spalten in Supply Chain Management

In Supply Chain Management spiegeln zwei Spalten den Status des Auftrags wider. Die Spalten, die Sie zuordnen müssen, sind **Status** und **Dokumentstatus**.

Die **Status**-Aufzählung gibt den Gesamtstatus der Bestellung an. Dieser Status wird im Auftragskopf angezeigt.

Die **Status**-Aufzählung hat die folgenden Werte:

- Offene Bestellung
- Geliefert
- Fakturiert
- Storniert

Die **Dokumentstatus**-Aufzählung gibt das letzte Dokument an, das für die Bestellung generiert wurde. Wenn die Bestellung beispielsweise bestätigt wird, handelt es sich bei diesem Dokument um eine Auftragsbestätigung. Wenn ein Kundenauftrag teilweise in Rechnung gestellt wird und dann die verbleibende Position bestätigt wird, bleibt der Belegstatus **Rechnung** erhalten, weil die Rechnung später im Prozess generiert wird.

Die **Dokumentstatus**-Aufzählung hat die folgenden Werte:

- Bestätigung
- Kommissionierliste
- Lieferschein
- Rechnung

## <a name="columns-in-sales"></a>Spalten in Sales

In Sales geben zwei Felder den Status der Bestellung an. Die Spalten, die Sie zuordnen müssen, sind **Status** und **Verarbeitungsstatus**.

Die **Status**-Aufzählung gibt den Gesamtstatus der Bestellung an. Es weist die folgenden Werte auf:

- Aktiv
- Übermittelt
- Erfüllt
- Fakturiert
- Storniert

Die Aufzählung **Verarbeitungsstatus** wurde eingeführt, damit der Status genau auf Supply Chain Management zugeordnet werden kann.

Die folgende Tabelle zeigt die Zuordnung von **Verarbeitungsstatus** auf Supply Chain Management.

| Verarbeitungsstatus   | Status in Supply Chain Management | Dokumentstatus in Supply Chain Management |
|---------------------|-----------------------------------|--------------------------------------------|
| Aktiv              | Offene Bestellung                        | Keines                                       |
| Bestätigt           | Offene Bestellung                        | Bestätigung                               |
| Entnommen              | Offene Bestellung                        | Kommissionierliste                               |
| Teilweise geliefert | Offene Bestellung                        | Lieferschein                               |
| Geliefert           | Geliefert                         | Lieferschein                               |
| Teilweise fakturiert  | Geliefert                         | Rechnung                                    |
| Fakturiert            | Fakturiert                          | Rechnung                                    |
| Storniert           | Storniert                         | Nicht zutreffend                             |

Die folgende Tabelle zeigt die Zuordnung von **Verarbeitungsstatus** zwischen Sales und Supply Chain Management.

| Verarbeitungsstatus   | Status in Sales | Status in Supply Chain Management |
|---------------------|-----------------|-----------------------------------|
| Aktiv              | Aktiv          | Offene Bestellung                        |
| Bestätigt           | Übermittelt       | Offene Bestellung                        |
| Entnommen              | Übermittelt       | Offene Bestellung                        |
| Teilweise geliefert | Aktiv          | Offene Bestellung                        |
| Teilweise fakturiert  | Aktiv          | Offene Bestellung                        |
| Teilweise fakturiert  | Erfüllt       | Geliefert                         |
| Fakturiert            | Fakturiert        | Fakturiert                          |
| Storniert           | Storniert       | Storniert                         |

## <a name="setup"></a>Einstellung

Um die Zuordnung für die Auftragsstatusspalten einzurichten, müssen Sie die Attribute **IsSOPIntegrationEnabled** und **isIntegrationUser** aktivieren.

Um das **IsSOPIntegrationEnabled**-Attribut zu aktivieren, führen Sie die folgenden Schritte aus.

1. Gehen Sie in einem Webbrowser zu `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. Ersetzen Sie **\<test-name\>** durch den Link Ihres Unternehmens zu Sales.
2. Suchen Sie auf der geöffneten Seite **organisationid** und notieren Sie sich den Wert.

    ![Suchen von organizationid.](media/sales-map-orgid.png)

3. Öffnen Sie in Sales die Browserkonsole und führen Sie das folgende Skript aus. Verwenden Sie den **organisationid**-Wert aus Schritt 2.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-Code in der Browserkonsole.](media/sales-map-script.png)

4. Überprüfen Sie, ob **IsSOPIntegrationEnabled** auf **true** festgelegt ist. Verwenden Sie die URL aus Schritt 1, um den Wert zu überprüfen.

    ![Auf „wahr“ festgelegtes IsSOPIntegrationEnabled.](media/sales-map-integration-enabled.png)

Um das **isIntegrationUser**-Attribut zu aktivieren, führen Sie die folgenden Schritte aus.

1. Wechseln Sie in Sales zu **Einstellung \> Anpassung \> System anpassen**, wählen Sie **Benutzertabelle** aus und öffnen Sie dann **Formular \> Benutzer**.

    ![Öffnen des Benutzerformulars.](media/sales-map-user.png)

2. Suchen Sie im Feld-Explorer **Integrationsbenutzermodus** und klicken Sie zweimal darauf, um es dem Formular hinzuzufügen. Speichern Sie die Änderung.

    ![Hinzufügen der Spalte „Integrationsbenutzermodus“ zum Formular.](media/sales-map-field-explorer.png)

3. Gehen Sie in Sales zu **Einstellung \> Sicherheit \> Benutzer** und ändern Sie die Ansicht von **Aktivierte Benutzer** zu **Anwendungsbenutzer**.

    ![Ändern der Ansicht von „Aktivierte Benutzer“ zu „Anwendungsbenutzer“.](media/sales-map-enabled-users.png)

4. Wählen Sie die beiden Einträge für **DualWrite IntegrationUser** aus.

    ![Liste der Anwendungsbenutzer.](media/sales-map-user-mode.png)

5. Ändern Sie den Wert der Spalte **Integrationsbenutzermodus** in **Ja**.

    ![Ändern des Werts der Spalte „Integrationsbenutzermodus“.](media/sales-map-user-mode-yes.png)

Ihre Aufträge sind jetzt zugeordnet.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]