---
title: Masterdatensuche für die Steuerberechnungskonfiguration aktivieren
description: In diesem Artikel wird erläutert, wie Sie Masterdaten-Suchfunktion für die Steuerberechnung einrichten und aktivieren.
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f9d882340171173e5e503f8b5e3aa856e8544b0
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306202"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Masterdatensuche für die Steuerberechnungskonfiguration aktivieren 

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie Masterdaten-Suchfunktion für die Steuerberechnung einrichten und aktivieren. Es steht eine Dropdown-Liste zur Auswahl von Werten in der Steuerberechnungskonfiguration für Felder wie **Juristische Person**, **Kreditorenkonto**, **Artikelcode** und **Lieferbedingungen** zur Verfügung. Diese Werte stammen aus der angeschlossenen Microsoft Dynamics 365 Finance Umgebung unter Verwendung der Microsoft Dataverse Datenquelle.

> [!NOTE] 
> Die Masterdaten-Suchfunktion für die Steuerberechnung ist eine optionale Funktion. Sie können die folgenden Schritte überspringen, wenn Sie im Regulatory Configuration Service (RCS) die Funktion **Unterstützung von Datenquellen für den Steuerdienst Dataverse** deaktivieren. In diesem Fall ist die Dropdown-Liste jedoch in der Steuerberechnungskonfiguration nicht verfügbar.

Um die Dropdown-Liste in der Konfiguration der Funktion Version der Steuerberechnung zu aktivieren, führen Sie die folgenden Schritte aus.

1. [Aktivieren Sie Microsoft Power Platform Integration und öffnen Sie die Dataverse Umgebung.](#enable)
2. [Installieren Sie virtuelle Entitäten für Finanzen und Betrieb.](#install)
3. [Registrieren Sie eine Azure Active Directory (Azure AD) Anwendung.](#register)
4. [Erteilung von Berechtigungen für Apps in Finanz- und Betriebs-Apps.](#grant)
5. [Konfigurieren Sie die Datenquelle für virtuelle Entitäten.](#configure)
6. [Aktivieren Sie Dataverse virtuelle Entitäten.](#virtual)
7. [Die verbundene Anwendung für die Steuerberechnung festlegen.](#set-up)
8. [Importieren und Festlegen der Dataverse-Modellzuordnung.](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a>Aktivieren Sie die Microsoft Power Platform Integration und öffnen Sie die Dataverse Umgebung

Die Integration von Finanz- und Betriebs-Apps mit Microsoft Power Platform kann aktiviert werden, wenn Sie eine neue Umgebung für Finanz- und Betriebs-Apps in Microsoft Dynamics Lifecycle Services (LCS) erstellen. Weitere Informationen finden Sie unter [Integration von Microsoft Power Platform – Übersicht über Add-Ins](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Wenn Sie fertig sind, erscheint der Name einer Microsoft Power Platform-Umgebung im Abschnitt **Power Platform Integration**.

1. Suchen Sie in LCS in Ihrer Finanz- und Betriebs-Umgebung im Bereich **Power Platform Integration** den Wert **Umgebungsname** für die verknüpfte Umgebung und notieren Sie sich diesen.

    [![Wert des Umgebungsnamens.](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. Wählen Sie im [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments) auf der Registerkarte **Umgebungen** die Umgebung aus, die dem Wert **Umgebungsname** entspricht, den Sie sich notiert haben.
3. Suchen Sie auf der Seite **Details** den **Umgebungs-URL**-Wert der Umgebung Dataverse. Notieren Sie sich diesen Wert, denn Sie werden ihn in [Schritt 7 benötigen. Legen Sie die verbundene Anwendung für die Steuerberechnung fest](#set-up).
4. Vergewissern Sie sich, dass Sie die Umgebung Dataverse in Ihrem Browser öffnen können, indem Sie den Wert **Umgebungs-URL** auswählen.

    [![Dataverse Umgebung Seite.](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > Halten Sie die Umgebung Dataverse in Ihrem Browser geöffnet. Sie werden es in [Schritt 5 benötigen. Konfigurieren Sie die Datenquelle für virtuelle Entitäten](#configure).

Weitere Informationen finden Sie unter [Aktivieren Sie die Microsoft Power Platform-Integration](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a>Installieren Sie virtuelle Entitäten für Finanzen und Betrieb

Die Dataverse-Lösung für die virtuellen Entitäten von Finanzen und Betrieb muss von der Microsoft AppSource-Lösung für virtuelle Entitäten installiert werden.

1. Suchen Sie in AppSource die virtuelle Entität [Finanzen und Betrieb](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity).
2. Wählen Sie **Jetzt holen**.
3. Geben Sie in das Feld **Wählen Sie eine Umgebung** den Wert **Umgebungsname** ein, den Sie sich zuvor notiert haben.
4. Aktivieren Sie die Kontrollkästchen und wählen Sie dann **Installieren**.

Wenn die Installation abgeschlossen ist, finden Sie die App **Finanzen und Betrieb virtuelle Entität** im [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/), unter **Ressourcen** \> **Dynamics 365 Apps**.

Weitere Informationen finden Sie unter [Die Lösung für virtuelle Entitäten herunterladen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution).

## <a name="register-an-azure-ad-application"></a><a name='register'></a>Registrieren Sie eine Azure AD Anwendung

Sie müssen eine Azure AD-Anwendung auf demselben Mandant wie die Finanz- und Betriebs-Apps registrieren, damit diese von Dataverse aufgerufen werden können.

1. Gehen Sie im [Azure-Portal](https://portal.azure.com) zu **Azure Active Directory \> App-Registrierungen**.
2. Wählen Sie **Neue Registrierung**, und geben Sie die folgenden Informationen ein:

    - **Name** – Geben Sie einen eindeutigen Namen ein.
    - **Kontotyp** – Geben Sie **ein beliebiges Azure AD-Verzeichnis** ein (Einzelmandant oder Mehrmandant).
    - **Redirect URI** – Lassen Sie dieses Feld leer.

3. Wählen Sie **Registrieren** aus.
4. Notieren Sie sich den Wert der **Anwendungs(Client)-ID**, da Sie ihn zu einem späteren Zeitpunkt benötigen.

    [![Azure AD Anwendung (Client) ID-Wert.](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. Erzeugen Sie einen symmetrischen Schlüssel für die Anwendung.
6. Wählen Sie in der neuen Anwendung **Zertifikate & Geheimnisse**.
7. Wählen Sie **Neuer Clientschlüssel**.
8. Geben Sie eine Beschreibung ein, wählen Sie ein Ablaufdatum und wählen Sie dann **Speichern**. Es wird ein Schlüssel erstellt und angezeigt. Kopieren Sie den Wert zur späteren Verwendung.

Weitere Informationen finden Sie unter [Registrierung der Anwendung Azure AD](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal).

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a>Erteilen Sie App Berechtigungen in Finanz- und Betriebs-Apps

Dataverse verwendet die von Ihnen erstellte Azure AD-Anwendung, um Finanz- und Betriebs-Apps aufzurufen. Daher muss die Anwendung von den Finanz- und Betriebs-Apps als vertrauenswürdig eingestuft und mit einem Benutzerkonto verknüpft werden, das über die entsprechenden Rechte verfügt. In den Finanz- und Betriebs-Apps müssen Sie einen speziellen Service-Benutzer erstellen, der **nur** Rechte für die Funktionalität der virtuellen Entitäten hat. Dieser Service-Benutzer darf keine anderen Rechte haben. Nachdem Sie diesen Schritt abgeschlossen haben, kann jede App, die über das Geheimnis der von Ihnen erstellten Anwendung Azure AD verfügt, die Umgebung von Finanz- und Betriebs-Apps aufrufen und auf die Funktionalität der virtuellen Entität zugreifen.

1. Gehen Sie in Ihrer Umgebung zu **Systemverwaltung** \> **Benutzer** \> **Benutzer**.
2. Wählen Sie **Neu**, um einen neuen Benutzer hinzuzufügen, und geben Sie die folgenden Informationen ein:

    - **Benutzer-ID** – Geben Sie **dataverse integration** oder einen anderen Wert ein.
    - **Benutzername** – Geben Sie **dataverse integration** oder einen anderen Wert ein.
    - **Provider** – Legen Sie dieses Feld auf **NonAAD** fest.
    - **Email** – Geben Sie **dataverse integration** oder einen anderen Wert ein. (Der Wert muss nicht unbedingt ein gültiges E-Mail-Konto sein.)

3. Weisen Sie dem Benutzer die Sicherheitsrolle **Integrations-App für die virtuelle Dataverse-Entität** zu.
4. Entfernen Sie alle anderen Rollen, einschließlich **Systembenutzer**.
5. Gehen Sie zu **Systemverwaltung** \> **Einrichtung** \> **Azure Active Directory Anwendungen** um Dataverse zu registrieren. 
6. Fügen Sie eine Zeile hinzu und geben Sie dann in das Feld **Kunden-ID** den Wert **Anwendungs-(Kunden-)ID** ein, den Sie sich zuvor notiert haben.
7. Geben Sie im Feld **Name** einen Namen ein. Geben Sie zum Beispiel **Dataverse Integration** ein.
8. Geben Sie in das Feld **Benutzer-ID** die Benutzer-ID ein, die Sie zuvor erstellt haben.

Weitere Informationen finden Sie unter [Erteilen von Berechtigungen für Apps in Finanz- und Betriebs-Apps](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps).

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>Konfigurieren Sie die Datenquelle der virtuellen Entität

Sie müssen Dataverse die Instanz der Finanz- und Betriebs-App zur Verfügung stellen, mit der eine Verbindung hergestellt werden soll.

1. Ihre Dataverse-Umgebung sollte noch in Ihrem Browser aus [Schritt 1 geöffnet sein. Aktivieren Sie die Microsoft Power Platform Integration und öffnen Sie die Dataverse Umgebung](#enable). Wählen Sie die Schaltfläche Einstellungen (Zahnradsymbol) oben rechts und wählen Sie dann **Erweiterte Einstellungen**.

    [![Öffnen der erweiterten Einstellungen in der Dataverse Umgebung.](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. Wählen Sie im Dropdown-Menü **Einstellungen** die Option **Verwaltung**.

    [![Verwaltung.](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. Wählen Sie **Virtuelle Entitäten Datenquellen**.

    [![Datenquellen für virtuelle Entitäten.](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. Wählen Sie die Datenquelle mit dem Namen **Finanzen und Betrieb**.

    [![Finanzen und Betrieb Datenquelle.](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. Geben Sie die folgenden Informationen aus früheren Schritten ein:

    - **Ziel-URL** – Geben Sie die URL ein, unter der Sie auf Finanz- und Betriebs-Apps zugreifen können.
    - **OAuth URL** – Geben Sie `https://login.windows.net/` ein.
    - **Mandanten-ID** – Geben Sie Ihren Mandanten an. Dieser Wert kann der Domänenname der E-Mail Ihrer Firma sein (z.B. contoso.com).
    - **AAD Anwendungs-ID** – Geben Sie den **Anwendungs-(Client)-ID**-Wert ein, der zuvor erstellt wurde.
    - **AAD Anwendungsgeheimnis** – Geben Sie das zuvor erstellte Geheimnis ein.
    - **AAD Ressource** – Geben Sie **00000015-0000-0000-c000-000000000000** ein. Dieser Wert ist die Azure AD Anwendung, die für Finanz- und Betriebs-Apps steht. Es sollte immer derselbe Wert sein.

6. Speichern Sie die Änderungen.
7. Schließen Sie die Seite, um zur Seite **Verwaltung** zurückzukehren, wo Sie mit [Schritt 6 beginnen. Aktivieren Sie Dataverse virtuelle Entitäten](#virtual).

    [![Schließen der Entität zur Bearbeitung.](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

Weitere Informationen finden Sie unter [Konfigurieren Sie die Datenquelle für virtuelle Entitäten](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source).

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a>Aktivieren Sie Dataverse virtuelle Entitäten

Die Sichtbarkeit der virtuellen Entitäten aus Finanz- und Betriebs-Apps muss auf **Ja** festgelegt werden, bevor sie von der Konfiguration der Steuerberechnung verwendet werden können.

> [!NOTE]
> Sie können diesen Schritt überspringen, indem Sie die mit Tax Calculation verbundenen virtuellen Entitäten mit nur einem Klick in [Schritt 8 aktivieren. Legen Sie die verbundene Anwendung für Tax Calculation fest](#import). Wir empfehlen Ihnen jedoch, mindestens eine virtuelle Entität manuell zu aktivieren, um anzuzeigen, dass die Verbindung zwischen Finanz- und Betriebs-Apps und Dataverse gut hergestellt ist.

1. Wählen Sie in Ihrer Dataverse-Umgebung auf der Seite **Verwaltung** die Schaltfläche Filter (Trichtersymbol) in der oberen rechten Ecke.

    [![Schaltfläche „Filtern“.](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. Wählen Sie im Fenster **Erweiterte Suche** im Feld **Suchen nach** die Option **Verfügbare Entitäten für Finanzen und Betrieb**.
3. Fügen Sie die folgende Regel hinzu: **Name** – **Enthält** – **CompanyInfoEntity**. Wählen Sie dann **Ergebnisse**.

    [![Erweitertes Suchfenster.](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. Wählen Sie **CompanyInfoEntity** in den Suchergebnissen, aktivieren Sie das Kontrollkästchen **Sichtbar** und wählen Sie dann **Speichern**.

    [![Sichtbarkeit der Entitäten festlegen.](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. Wiederholen Sie die vorangegangenen Schritte für die folgenden Entitäten, auf die in der Konfiguration der Steuerberechnung verwiesen wird:

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity
    - InventOperationalSiteV2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > Nur die ersten 5.000 Datensätze einer Entität können mit Dataverse abgerufen und in der Dropdown-Liste der Steuerberechnungskonfiguration verfügbar gemacht werden.

Weitere Informationen finden Sie unter [virtuelle Microsoft Dataverse-Entitäten aktivieren](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a>Die verbundene Anwendung für die Steuerberechnung festlegen

1. Gehen Sie zu **Elektronische Berichterstattung** und wählen Sie dann im Bereich **Verwandte Links** die Option **Verbundene Anwendungen**.

    [![Verbundene Anwendungen.](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

2. Wählen Sie **Neu**, um einen Datensatz hinzuzufügen, und geben Sie die folgenden Informationen ein.

    - **Name**: Geben Sie einen Namen ein.
    - **Typ** – Wählen Sie **Dataverse**.
    - **Anwendung** – Geben Sie den **Umgebungs-URL**-Wert Ihrer Dataverse-Umgebung ein, den Sie sich in [Schritt 1 notiert haben. Aktivieren Sie die Microsoft Power Platform Integration und öffnen Sie Ihre Dataverse Umgebung](#enable).
    - **Mandant** – Geben Sie Ihren Mandanten ein.
    - **Benutzerdefinierte URL** – Geben Sie Ihre Dataverse URL ein und fügen Sie **/api/data/v9.1** hinzu.

3. Wählen Sie **Verbindung prüfen** und wählen Sie dann in dem Dialogfeld **Hier klicken, um eine Verbindung zur ausgewählten Remote-Anwendung herzustellen**.

    [![Überprüfen der Verbindung.](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
4. Stellen Sie sicher, dass Sie ein „Success!“ erhalten. Nachricht, die anzeigt, dass die Verbindung erfolgreich hergestellt wurde.

    [![Erfolgsmeldung.](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)
    
5. Öffnen Sie in RCS den Arbeitsbereich **Funktionsverwaltung**, und aktivieren Sie die folgenden Funktionen:

    - Globalisierungsfunktionen
    - Unterstützung von Dataverse-Datenquellen der elektronischen Berichterstellung
    - Unterstützung für Dataverse-Datenquellen des Steuerdienstes

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a>Importieren und Festlegen der Dataverse Model Mapping Konfiguration

Microsoft bietet Standardkonfigurationen für die Zuordnung von Entitäten aus Finanz- und Betriebs-Apps zu Tax Calculation.

1. Gehen Sie in RCS zu **Elektronische Berichterstattung**.
2. Wählen Sie im Abschnitt **Konfigurationsanbieter** auf der Kachel für den **Microsoft**-Anbieter **Repositories**.

    [![Repositories.](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. Markieren Sie den Datensatz **Globales Konfigurations-Repository** und wählen Sie dann **Öffnen**.
4. Wählen Sie unter **Steuerdatenmodell** \> **Steuerberechnungsdatenmodell** die Konfiguration **Dataverse Modellzuordnung**.
5. Wählen Sie auf der Registerkarte **Versionen** Inforegister eine Version aus, die der Version Ihrer Finanz- und Betriebs-Apps entspricht, und wählen Sie dann **Importieren**.

    [![Importieren der Dataverse Modell Zuordnung Konfiguration.](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > Die Konfiguration **Dataverse Model Mapping** ist nur in der höchsten importierten Version wirksam. Daher sollten Sie keine Version der **Dataverse Model Mapping** Konfiguration importieren, die höher ist als die Version der Steuerberechnungskonfiguration, die Sie zu implementieren planen. Wenn Sie zum Beispiel die Version 40.50.225 der Konfiguration Steuerberechnung implementieren möchten, sollten Sie nur die Version 40.50.13 der Konfiguration **Dataverse Modellzuordnung** importieren. Sie sollten die Version 40.54.14 nicht importieren. Andernfalls kommt es zu einer Fehlanpassung des Datenmodells in der Konfiguration.

6. Gehen Sie zurück zu **Elektronisches Berichtswesen**, und wählen Sie die Kachel **Steuerkonfigurationen**.
7. Wählen Sie die importierte **Dataverse Model Mapping** Konfiguration und wählen Sie dann **Bearbeiten**.
8. Hier können Sie die Option **Standard für Modellzuordnung** auf **Ja** festlegen.
9. Wählen Sie im Feld **Verbundene Anwendung** die verbundene Anwendung, die Sie in [Schritt 7 festgelegt haben. Legen Sie die verbundene Anwendung für die Steuerberechnung fest](#set-up).
10. Legen Sie die Option **Sichtbarkeit der virtuellen Tabelle festlegen** auf **Ja** fest, um alle mit der Steuerberechnung verbundenen virtuellen Entitäten sichtbar zu machen.

Sie haben nun die Einrichtung für das Nachschlagefeld für Stammdaten abgeschlossen. Eine Dropdown-Liste für Felder wie **Juristische Entitäten**, **Kreditorenkonto**, **Artikelcode** und **Lieferbedingung** aus Dynamics 365 Finance wird jetzt in der Einrichtung der Funktion **Steuerberechnung Version** aktiviert.

[![Dropdown-Liste juristische Entitäten.](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
