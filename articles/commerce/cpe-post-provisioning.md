---
title: Eine Dynamics 365 Commerce-Sandbox-Umgebung konfigurieren
description: In diesem Artikel wird erläutert, wie eine Microsoft Dynamics 365 Commerce-Sandbox-Umgebung nach ihrer Bereitstellung konfiguriert wird.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ae6a8c63721ac32f525e1846a10c0b2caeb08f9f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270371"
---
# <a name="configure-a-dynamics-365-commerce-sandbox-environment"></a>Eine Dynamics 365 Commerce-Sandbox-Umgebung konfigurieren

[!include [banner](includes/banner.md)]

In diesem Artikel wird erläutert, wie eine Microsoft Dynamics 365 Commerce-Sandbox-Umgebung nach ihrer Bereitstellung konfiguriert wird.

Führen Sie die in diesem Artikel beschriebenen Prozeduren erst aus, nachdem Ihre Commerce-Sandbox-Umgebung bereitgestellt wurde. Informationen zum Bereitstellen Ihrer Commerce-Sandbox-Umgebung nach deren Bereitstellung finden Sie unter [Stellen Sie eine Commerce-Sandbox-Umgebung bereit](provisioning-guide.md).

Nachdem Ihre Commerce-Sandbox-Umgebung vollständig bereitgestellt wurde, müssen zusätzliche Konfigurationsschritte nach der Bereitstellung ausgeführt werden, bevor Sie mit der Verwendung der Umgebung beginnen können. Um diese Schritte abzuschließen, müssen Sie Microsoft Dynamics Lifecycle Services (LCS) und Dynamics 365 Commerce verwenden.

## <a name="before-you-start"></a>Bevor Sie beginnen

1. Melden Sie sich beim [LCS-Portal](https://lcs.dynamics.com) an.
1. Gehen Sie zu Ihrem Projekt.
1. Wählen Sie Ihre Umgebung in der Liste aus.
1. Wählen Sie in den Umgebungsinformationen rechts die Option **Bei Umgebung anmelden** aus. Sie werden zur Zentralverwaltung von Commerce übermittelt.
1. Stellen Sie sicher, dass die juristische Person **USRT** oben rechts ausgewählt ist. Diese juristische Person wurde in den Demodaten vorkonfiguriert.
1. Wechseln Sie zu **Handelsparameter \> Konfigurationsparameter** und vergewissern Sie sich, dass ein Eintrag für **ProductSearch.UseAzureSearch** vorhanden ist und der Wert auf **true** festgelegt ist. Wenn dieser Eintrag fehlt, fügen Sie ihn hinzu, und setzen Sie den Wert auf **Wahr**.
1. Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Handelsplanung \> Commerce-Steuerprogramm initialisieren**. Legen Sie im Flyoutmenü **Commerce-Steuerprogramm initialisieren** die Option **Vorhandene Konfiguration löschen** auf **Ja** fest, und wählen Sie dann **OK** aus.
1. Damit die Store- und E-Commerce-Kanäle ordnungsgemäß funktionieren, müssen sie der Commerce Scale Unit hinzugefügt werden. Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Handelsplanung \> Kanaldatenbank**, und führen Sie dann im linken Bereich die Commerce Scale Unit aus. Fügen Sie auf dem Inforegister **Retail Channel** die Kanäle **AW-Onlineshop**, **AW Business-Onlineshop** und **Erweiterter Onlineshop von Fabrikam** hinzu, wenn Sie planen, die se E-Commerce-Kanäle zu verwenden. Optional können Sie auch Einzelhandelsgeschäfte hinzufügen, wenn Sie Verkaufsstellen (POS) verwenden (z. B. **Seattle**, **San Francisco** und/oder **San Jose**).
1. Um sicherzustellen, dass alle Änderungen mit der Kanaldatenbank synchronisiert werden, wählen Sie **Kanaldatenbank \> Vollständige Datensynchronisierung** für die Commerce Scale Unit.

Stellen Sie bei Aktivitäten nach der Bereitstellung in der Commerce-Zentralverwaltung sicher, dass die juristische Person **USRT** immer ausgewählt ist.

## <a name="configure-the-point-of-sale"></a>Die Verkaufsstelle konfigurieren

### <a name="associate-a-worker-with-your-identity"></a>Mitarbeiter Ihrer Identität zuordnen

Gehen Sie in der Commerce-Zentralverwaltung folgendermaßen vor, um einen Mitarbeiter Ihrer Identität zuzuordnen.

1. Verwenden Sie das Menü auf der linken Seite, um zu **Module \> Einzelhandel und Handel \> Mitarbeiter \> Arbeitskräfte** zu gehen.
1. Suchen Sie in der Liste den folgenden Datensatz, und wählen Sie ihn aus: **000713 - Andrew Collette**. Dieser Beispielbenutzer ist mit dem Geschäft in San Francisco verknüpft, das im nächsten Abschnitt verwendet wird.
1. Wählen Sie im Aktionsbereich **Commerce** aus.
1. Wählen Sie **Vorhandene Identität zuordnen** aus.
1. Geben Sie im Feld **E-Mail** rechts neben **Suchen mithilfe von E-Mails** Ihre E-Mail-Adresse ein.
1. Wählen Sie **Suchen** aus.
1. Wählen Sie den Datensatz mit Ihrem Namen aus.
1. Wählen Sie **OK**.
1. Wählen Sie **Speichern** aus.

### <a name="activate-cloud-pos"></a>Aktivieren von Cloud POS

Führen Sie diese Schritte in LCS aus, um Cloud POS zu aktivieren.

1. Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.
1. Wählen Sie Ihre Umgebung in der Liste aus.
1. Wählen Sie in den Umgebungsinformationen rechts die Option **Bei Cloud-Verkaufsstelle anmelden** aus.
1. Wählen Sie **Weiter** aus, um das Dialogfeld **Bevor Sie anfangen** zu öffnen.
1. Lassen Sie das Feld **Server-URL** wie es ist. Wählen Sie **Weiter**.
1. Melden Sie sich mit Ihrem Microsoft Azure Active Directory-Konto (Azure AD) an.
1. Unter **Ladenname** wählen Sie **San Francisco** und dann **Weiter** aus.
1. Wählen Sie unter **Register und Gerät** **SANFRAN-1** aus.
1. Wählen Sie **Aktivieren** aus. Sie werden abgemeldet und zur POS-Anmeldeseite weitergeleitet.
1. Sie können sich nun bei der Cloud POS-Erfahrung mit der Operator-ID **000713** und dem Kennwort **123** anmelden.

## <a name="set-up-your-e-commerce-sites"></a>Ihre Sites in E-Commerce einrichten

Es gibt drei verfügbare E-Commerce-Demoseiten: Fabrikam, Adventure Works und Adventure Works Business. Befolgen Sie die nachstehenden Schritte, um jede Demo-Site zu konfigurieren.

1. Melden Sie sich beim Website-Generator mit der URL an, die Sie bei der Initialisierung von E-Commerce während der Bereitstellung notiert haben (siehe [E-Commerce initialisieren](provisioning-guide.md#initialize-e-commerce)).
1. Wählen Sie die Site (**Fabrikam**, **Adventure Works** oder **Adventure Works Business**) aus, um das Dialogfeld „Site-Setup“ zu öffnen.
1. Wählen Sie die Domäne aus, die Sie bei der Initialisierung von Commerce eingegeben haben.
1. Wählen Sie in der Zentrale den vorkonfigurierten Onlineshop-Kanal (**Erweiterter Online-Shop von Fabrikam**, **AW-Online-Shop** oder **AW Business Online-Shop**) aus, der dem Standardkanal entspricht.
1. Wählen Sie als Standardsprache **de-de** aus.
1. Konfigurieren Sie die Pfadfelder. Dies kann für eine einzelne Sites leer gelassen werden, muss aber konfiguriert werden, wenn derselbe Domänenname für mehrere Sites verwendet wird. Wenn der Domänenname beispielsweise `https://www.constoso.com` lautet, können Sie einen leeren Pfad für Fabrikam (`https://contoso.com`) verwenden, und verwenden dann „aw“ für Adventure Works (`https://contoso.com/aw`) und „awbusiness“ für die Adventure Works Business-Site (`https://contoso.com/awbusiness`).
1. Wählen Sie **OK** aus. Die Liste der Seiten auf der Site wird angezeigt.
1. Wiederholen Sie optional die Schritte 2–7, um die anderen Demo-Sites nach Bedarf zu konfigurieren.

## <a name="enable-jobs"></a>Aufträge aktivieren

Um Jobs in Commerce zu ermöglichen, folgen Sie diesen Schritten.

1. Melden Sie sich in der Umgebung der Zentralverwaltung an.
1. Verwenden Sie das Menü auf der linken Seite, um zu **Retail and Commerce \> Anfragen und Berichte \> Batch-Jobs** zu gehen.

    Die verbleibenden Schritte dieses Verfahrens müssen für jeden der folgenden Jobs ausgeführt werden:

    * Einzelhandelsauftrag für E-Mail-Benachrichtigung verarbeiten
    * Produktverfügbarkeit
    * P-0001
    * Einzelvorgang für Aufträge synchronisieren

1. Verwenden Sie den Schnellfilter, um nach dem Auftrag anhand seines Namens zu suchen.
1. Wenn der Status des Auftrags **Wird ausgeführt** lautet, führen Sie die folgenden Schritte aus:

    1. Wählen Sie den Datensatz aus.
    1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Batchauftrag** die Option **Status ändern** aus.
    1. Wählen Sie **Wird abgebrochen** aus, und wählen Sie dann **OK** aus.

1. Wenn der Status des Auftrags **Zurückgehalten** lautet, führen Sie die folgenden Schritte aus:

    1. Wählen Sie den Datensatz aus.
    1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Batchauftrag** die Option **Status ändern** aus.
    1. Wählen Sie **Im Wartezustand** und dann **OK** aus.

Optional können Sie auch das Serienintervall für die folgenden Einzelvorgänge auf eine (1) Minute festlegen:

* E-Mail-Benachrichtigungseinzelvorgang für Einzelhandelsauftrag verarbeiten
* P-0001-Einzelvorgang
* Einzelvorgang für Aufträge synchronisieren

### <a name="run-full-data-synchronization"></a>Vollständige Datensynchronisation ausführen

Um die vollständige Datensynchronisierung in Commerce auszuführen, führen Sie diese Schritte in der Commerce-Zentralverwaltung aus.

1. Verwenden Sie das Menü auf der linken Seite, um zu **Module \> Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Kanaldatenbank** zu wechseln.
1. Wählen Sie den Kanal mit der Bezeichnung **scXXXXXXXXX** aus.
1. Wählen Sie **Vollständige Datensynchronisierung** im Aktionsbereich aus.
1. Geben Sie **9999** als Vertriebsplan ein.
1. Wählen Sie **OK**.
1. Wählen Sie **OK**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Testen der Kreditkartendaten, um Testkäufe durchzuführen

Um Testtransaktionen auf der Site durchzuführen, können Sie diese Testkreditkartendaten verwenden:

- **Kartennummer:** 4111-1111-1111-1111
- **Ablaufdatum:** 10/30
- **Kartenprüfwert-Code (CVV):** 737

> [!IMPORTANT]
> Sie sollten unter keinen Umständen versuchen, die tatsächlichen Kreditkarteninformationen auf der Testseite zu verwenden.

## <a name="next-steps"></a>Nächste Schritte

Nachdem die Bereitstellungs- und Konfigurationsschritte abgeschlossen sind, können Sie mit der Verwendung Ihrer Sandbox-Umgebung beginnen. Verwenden Sie die URL des Commerce-Website-Generators, um zur Erstellungsumgebung zu gelangen. Verwenden Sie die URL der Commerce-Website, um zur Umgebung der Einzelhandelskundenwebsite zu wechseln.

Informationen zum Konfigurieren optionaler Funktionen für Ihre Commerce-Sandbox-Umgebung erhalten Sie unter [Optionale Funktionen für eine Commerce-Sandbox-Umgebung konfigurieren](cpe-optional-features.md).

Damit sich E-Commerce-Benutzer bei der E-Commerce-Site anmelden können, ist eine zusätzliche Konfiguration erforderlich, um die Site-Authentifizierung über Azure Active Directory Business-to-Consumer (B2C) zu aktivieren. Anweidungen finden Sie unter [Einrichten eines B2C-Mandanten in Commerce](set-up-b2c-tenant.md).

## <a name="troubleshooting"></a>Problembehandlung

### <a name="site-builder-channel-list-is-empty-when-configuring-site"></a>Die Site-Builder-Kanalliste ist beim Konfigurieren der Site leer

Wenn der Site Builder keine Onlineshop-Kanäle anzeigt, stellen Sie in der Zentralverwaltung sicher, dass die Kanäle der Commerce Scale Unit hinzugefügt wurden, wie im Abschnitt [Bevor Sie beginnen](#before-you-start) oben beschrieben. Führen Sie außerdem **Commerce-Steuerprogramm initialisieren** mit dem Wert **Vorhandene Konfiguration löschen** auf **Ja** festgelegt aus.  Sobald diese Schritte abgeschlossen sind, führen Sie auf der Seite **Kanaldatenbank** (**Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Handelsplanung \> Kanaldatenbank**) den Einzelvorgang **9999** in der Commerce Scale Unit aus.

### <a name="color-swatches-are-not-rendering-on-the-category-page-but-are-rendering-on-the-product-details-page-pdp-page"></a>Farbmuster werden nicht auf der Kategorieseite gerendert, sondern auf der Seite mit den Produktdetails (PDP)

Befolgen Sie diese Schritte, um sicherzustellen, dass die Farb- und Größenmuster so eingestellt sind, dass sie verfeinert werden können.

1. Gehen Sie in der Zentralverwaltung zu **Einzelhandel und Handel \> Kanaleinstellungen \> Kanalkategorien und Produktattribute**.
1. Wählen Sie im linken Bereich den Onlineshop-Kanal aus, und wählen Sie dann **Attributmetadaten festlegen** aus.
1. Legen Sie die Option **Attribut für Kanal anzeigen** auf **Ja** fest, setzen Sie die Option **Kann verfeinert werden** auf **Ja**, und wählen Sie dann **Speichern** aus. 
1. Kehren Sie zur Kanalseite des Onlineshops zurück und wählen Sie dann **Kanalupdates veröffentlichen** aus.
1. Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Handelsplanung \> Kanaldatenbank**, und führen Sie den Einzelvorgang **9999** in der Commerce Scale Unit aus.

### <a name="business-features-dont-appear-to-be-turned-on-for-the-adventureworks-business-site"></a>Funktionen für Unternehmen scheinen für die AdventureWorks Business-Site nicht aktiviert zu sein

Stellen Sie in der Zentralverwaltung sicher, dass der Onlineshop-Kanal so konfiguriert ist, dass **Kundentyp** auf **B2B** festgelegt ist. Wenn **Kundentyp** auf **B2C** festgelegt ist, muss ein neuer Kanal erstellt werden, da der vorhandene Kanal nicht bearbeitet werden kann. 

Demodaten, die in Commerce-Version 10.0.26 und früher ausgeliefert wurden, hatten einen Fehler, bei dem der **AW Business-Onlineshop**-Kanal falsch konfiguriert war. Die Problemumgehung besteht darin, einen neuen Kanal mit denselben Einstellungen und Konfigurationen zu erstellen, mit Ausnahme von **Kundentyp**, der auf **B2B** eingestellt werden sollte.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eine Dynamics 365 Commerce-Sandbox-Umgebung bereitstellen](provisioning-guide.md)

[Optionale Funktionen für eine Dynamics 365 Commerce-Sandbox-Umgebung konfigurieren](cpe-optional-features.md)

[BOPIS in einer Dynamics 365 Commerce-Sandbox-Umgebung konfigurieren](cpe-bopis.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-Portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-Website](https://aka.ms/Dynamics365CommerceWebsite)

[B2C-Mandanten in Commerce einrichten](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
