---
title: Eine E-Commerce-Bewertungsumgebung konfigurieren
description: Dieses Handbuch enthält schrittweise Anweisungen zum Bereitstellen und Konfigurieren Ihrer Microsoft Dynamics 365 Commerce-Vorschauumgebung.
author: v-chgri
manager: annbe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0dce2796e69cd8dee87cba176a521c26c81eb1a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771679"
---
# <a name="configure-an-e-commerce-evaluation-environment"></a>Eine E-Commerce-Bewertungsumgebung konfigurieren

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Handbuch enthält schrittweise Anweisungen zum Bereitstellen und Konfigurieren Ihrer Microsoft Dynamics 365 Commerce-Vorschauumgebung. Bevor Sie beginnen, sollten Sie zumindest die Dokumentation durchgehen, um eine Vorstellung davon zu bekommen, was der Prozess beinhaltet und was das Handbuch enthält.

*Hinweis: Wenn Sie noch keinen Zugriff auf die Microsoft Dynamics 365 Commerce-Vorschau erhalten haben, können Sie einen Zugriff auf die Vorschau über die [Commerce-Website](https://aka.ms/Dynamics365CommerceWebsite) anfordern.*

## <a name="summary"></a>Summe
Um die Umgebung erfolgreich bereitzustellen, muss das Projekt mit einem bestimmten Produktnamen und -typ erstellt werden. Bei der Umgebung und Retail Cloud Scale Unit gibt es auch einige spezifische Parameter, die Sie verwenden müssen, um später die E-Commerce-Bereitstellung zu starten. Die Anweisungen in diesem Handbuch enthalten alle erforderlichen Schritte und Parameter.

Nach der erfolgreichen Bereitstellung müssen Sie einige Schritte nach der Bereitstellung ausführen, um Ihre Vorschauumgebung vorzubereiten. Einige Schritte sind optional, je nachdem, welche Aspekte des Systems Sie bewerten möchten. Sollten Sie später Ihre Meinung ändern, können Sie die optionalen Schritte jederzeit später ausführen.

Wenn Sie Fragen zu den Bereitstellungsschritten haben oder auf Probleme stoßen, teilen Sie uns dies bitte unter [Microsoft Dynamics 365 Commerce Vorschau Yammer-Gruppe](https://aka.ms/Dynamics365CommercePreviewYammer) mit. 

## <a name="prerequisites"></a>Voraussetzungen
Die folgenden Voraussetzungen sind für die Bereitstellung Ihrer Dynamics 365-Vorschauumgebung erforderlich:
* Sie haben Zugriff auf das **Lifecycle Services-Portal (LCS)**
* Sie wurden **beim Dynamics 365 Commerce-Vorschauprogramm angenommen**
* Sie besitzen die erforderlichen Berechtigungen, um ein Projekt für **Künftige Presales** oder **Migrieren, Erstellen von Lösungen und Kennenlernen von** zu erstellen.
* Sie sind Mitglied der Rolle **Umgebungsmanager** oder **Projektverantwortlicher** in dem Projekt, in dem Sie die Umgebung bereitstellen
* Sie haben Administratorzugriff auf Ihr Azure-Abonnement oder wenden sich an einen Abonnementadministrator, der in Ihrem Namen die beiden Schritte ausführen kann, für die Administratorberechtigungen erforderlich sind
* Ihnen liegt Ihre **AAD-Mandanten-ID** vor
* Sie haben eine **AAD-Sicherheitsgruppe** erstellt, die als **E-Commerce-Systemadministrator-Gruppe** verwendet wird, und Ihnen liegt deren ID vor
* Sie haben eine **AAD-Sicherheitsgruppe** erstellt, die als **Bewertungs- und Prüfungs-Moderatorgruppe** verwendet wird, und Ihnen liegt deren ID vor (kann dieselbe Sicherheitsgruppe wie die Systemadministratorgruppe oben sein)
## <a name="provisioning-preview-environment"></a>Bereitstellen der Vorschauumgebung
Diese Anweisungen beziehen sich auf die Bereitstellung einer Microsoft Dynamics 365 Commerce-Vorschauumgebung. Nachdem Sie diese Schritte erfolgreich ausgeführt haben, steht Ihnen eine Vorschau-Umgebung zur Verfügung, die konfiguriert werden kann. Alle hier beschriebenen Aktivitäten finden im LCS-Portal statt.

*Beachten Sie, dass der Vorschauzugriff an das LCS-Konto und die Organisation gebunden ist, die Sie in Ihrer Vorschau-Anwendung angegeben haben. Sie müssen dasselbe Konto für die Bereitstellung verwenden. Wenn Sie ein anderes LCS-Konto oder einen anderen Mandanten für die Vorschauumgebung verwenden müssen, müssen Sie uns diese Details mitteilen. Kontaktinformationen finden Sie unten unter „Zusätzliche Ressourcen“.*
### <a name="before-starting"></a>Vor dem Start
##### <a name="grant-access-to-e-commerce-applications"></a>Zugriff auf die E-Commerce-Anwendungen gewähren

*Hinweis: **Die Person, die sich anmeldet, muss ein AAD-Mandantenadministrator sein**. Ohne den erfolgreichen Abschluss dieses Schritts schlagen die restlichen Bereitstellungsschritte fehl.*

1. Für diesen Schritt benötigen Sie Ihre **AAD-Mandanten-ID**. Sie müssen E-Commerce-Anwendungen autorisieren, um auf Ihr Azure-Abonnement zugreifen zu können. Der einfachste Weg, dies zu erreichen, besteht darin, eine URL wie die folgende zusammenzustellen:

https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345

2. **Klicken Sie nicht direkt auf die URL**, kopieren Sie sie stattdessen und fügen Sie sie in Ihren Browser oder Texteditor ein und ersetzen Sie **\{AAD_TENANT_ID\}** durch Ihre **AAD-Mandanten-ID**, bevor Sie zur URL navigieren.
3. Daraufhin wird das Microsoft AAD-Anmeldedialogfeld angezeigt, in dem Sie bestätigen, dass Sie der „Dynamics 365 Commerce (Vorschau)“ die Berechtigung erteilen möchten.
4. Sie werden auf eine Seite weitergeleitet, auf der bestätigt wird, ob der Vorgang erfolgreich war.

##### <a name="log-in-to-the-lcs"></a>Beim LCS anmelden
1. Anmeldung beim LCS-Portal: https://lcs.dynamics.com
1. Stellen Sie sicher, dass Sie mit demselben LCS-Konto angemeldet sind, mit dem Sie den Zugriff auf die Vorschau angefordert haben.
##### <a name="confirm-that-preview-features-are-available-and-enabled"></a>Bestätigen, dass die Vorschaufunktionen verfügbar und aktiviert sind
1. Scrollen Sie auf der LCS-Startseite ganz nach rechts und klicken Sie auf die Kachel **Verwaltung von Vorschaufunktionen**.
1. Scrollen Sie nach unten zu „PRIVATE VORSCHAUFUNKTIONEN“ und stellen Sie sicher, dass die folgenden Funktionen verfügbar und aktiviert sind:
    1. **E-Commerce-Bewertung**
    1. **Commerce-Vorschau-Programmumgebungen**
1. Wenn Sie diese Funktionen nicht in der Liste sehen können, teilen Sie uns bitte Ihre geschäftliche E-Mail-Adresse, Ihr LCS-Konto und Ihre Mandantendetails mit. Weitere Informationen dazu, wie Sie mit uns Kontakt aufnehmen können, erhalten Sie unter **Zusätzliche Ressourcen**.

![Vorschau von Verwaltungskacheln](./media/preview1.png)

![Vorschaufunktionen](./media/preview2.png)
### <a name="create-project"></a>Projekt erstellen
##### <a name="creating-new-project"></a>Erstellen eines neuen Projekts
1. Klicken Sie auf **+**, um ein neues Projekt zu erstellen.
1. Wenn Sie ein Partner sind, wählen Sie **Migrieren, Erstellen von Lösungen und Kennenlernen von**.
1. Wenn Sie ein Kunde sind, wählen Sie **Künftige Presales** aus.
1. Geben Sie nach Belieben einen Namen, eine Beschreibung und eine Branche ein.
1. Wählen Sie für **Produktname** **Dynamics 365 Retail** aus.
1. Wählen Sie für **Produktversion** **Dynamics 365 Retail** aus.
1. Wählen Sie für **Methode** **Dynamics Retail-Implementierungsmethode** aus.
1. Sie können Rollen und Benutzer aus einem vorhandenen Projekt importieren, wenn dies gewünscht wird.
1. Klicken Sie auf **Erstellen**.
1. Sie werden zur Projektansicht weitergeleitet.
##### <a name="add-azure-connector"></a>Azure-Connector hinzufügen
1. Wenn Sie ein Partner sind, klicken Sie über die Tools-Kachel ganz rechts auf **Projekteinstellungen**.
1. Wenn Sie ein Kunde sind, wählen Sie **Projekteinstellungen** aus dem oberen Menü aus.
1. Wählen Sie **Azure-Connector**.
1. Klicken Sie auf **+ Hinzufügen**, um Azure Connector hinzuzufügen.
1. Geben Sie einen Namen ein.
1. Geben Sie Ihre **Azure-Abonnement-ID** ein.
1. Aktivieren Sie **Verwendung von Azure Resource Manager (ARM) konfigurieren**.
1. Überprüfen Sie, dass die **AAD-Mandantendomäne (oder ID) des Azure-Abonnements** korrekt ist. Wenden Sie sich bei Bedarf an Ihren Azure-Abonnementadministrator.
1. Klicken Sie auf **Weiter**.
1. Befolgen Sie die Anweisungen auf dem Bildschirm, um den entsprechenden Anwendungen Zugriff auf Ihr Abonnement zu gewähren. Wenden Sie sich bei Bedarf an Ihren Azure-Abonnementadministrator:
    1. Anmeldung beim Azure-Portal: https://portal.azure.com/
    1. Stellen Sie sicher, dass Sie das richtige Verzeichnis ausgewählt haben.
    1. Klicken Sie im linken Menü auf **Abonnements**.
    1. Suchen Sie das richtige Abonnement in der Liste und wählen Sie es aus. Verwenden Sie bei Bedarf die Suche.
    1. Wählen Sie **Zugriffssteuerung (IAM)** im Menü aus.
    1. Klicken Sie unter **Hinzufügen** auf **Rollenzuweisung hinzufügen** auf der rechten Seite. Der Bereich **Rollenzuweisung hinzufügen** wird geöffnet.
    1. Wählen Sie für **Rolle** **Mitwirkender** aus.
    1. Übernehmen Sie für **Zugriff gewähren auf** die Option **Azure AD-Benutzer, -Gruppe oder -Serviceprinzipal**.
    1. Geben Sie unter **Auswählen** **b96b7e94-b82e-4e71-99a0-cf7fb188acea** ein.
    1. Wählen Sie **Dynamics-Bereitstellungsdienste [wsfed-enabled]** aus der Liste aus.
    1. Klicken Sie auf **Speichern**.
1. Klicken Sie auf **Weiter**.
1. Befolgen Sie die Anweisungen auf dem Bildschirm, um den entsprechenden Anwendungen Zugriff auf Ihr Abonnement zu gewähren. Wenden Sie sich bei Bedarf an Ihren Azure-Abonnementadministrator.
1. Klicken Sie auf **Weiter**.
1. Wählen Sie für **Azure-Region** **USA, Osten**, **USA, Osten 2**, **USA, Westen** oder **USA, Westen 2** aus.
1. Klicken Sie auf **Verbinden**.
1. Ihr Azure Connector sollte in der Liste angezeigt werden.
### <a name="import-extension"></a>Import-Erweiterung
1. Navigieren Sie zurück zur Startseite Ihres Projekts, indem Sie oben auf den Projektnamen klicken.
1. Wenn Sie ein Partner sind, klicken Sie über die Tools-Kachel ganz rechts auf **Objektbibliothek**.
1. Wenn Sie ein Kunde sind, wählen Sie **Objektbibliothek** aus dem oberen Menü aus.
1. Wählen Sie **Bereitstellbares Softwarepaket** aus der Liste links aus.
1. Klicken Sie über den Aktionsbereich auf **IMPORTIEREN**.
1. Wählen Sie **Commerce-Vorschaudemobasiserweiterung** aus der Liste der Medienobjekte unter **GEMEINSAME OBJEKTBIBLIOTHEK** aus.
1. Klicken Sie auf **Abholen**.
1. Sie kehren zur Objektbibliothek zurück und sollten die Erweiterung in der Liste sehen.

![Projekterstellung – Versionen](./media/import.png)
### <a name="deploy-environment"></a>Bereitstellen der Umgebung

*Hinweis: Es ist möglich, dass die Schritte 6, 7 bzw. 8 nicht angezeigt werden, da die Bildschirme mit einer Option übersprungen werden. Wenn Sie sich in der Ansicht **Umgebungsparameter** befinden, bestätigen Sie, dass der Text „Dynamics 365 Commerce (Vorschau) - Demo (10.0.6 mit Plattformupdate 30)“ direkt über dem Feld **Umgebungsname** angezeigt wird. Siehe Screenshot unten.*

1. Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.
1. Klicken Sie auf **+ Hinzufügen**, um eine Umgebung hinzuzufügen.
1. Wählen Sie für **Anwendungsversion** **10.0.6** aus.
1. Wählen Sie für **Plattformversion** **Plattformupdate 30** aus.
1. Klicken Sie auf **Weiter**.
1. Wählen Sie für die Umgebungstopologie **DEMO** aus.
1. Wählen Sie für die Umgebungstechnologie **Dynamics 365 Commerce (Vorschau) - Demo** aus.
1. Wenn Sie zuvor einen einzelnen Azure Connector konfiguriert haben, wird dieser für diese Umgebung verwendet. Wenn Sie mehrere Azure Connectors konfiguriert haben, können Sie auswählen, welchen Connector Sie verwenden möchten: **USA, Osten**, **USA, Osten 2**, **USA, Westen** oder **USA, Westen 2** (empfohlen für die beste End-to-End-Leistung)
1. Geben Sie einen **Umgebungsnamen** ein.
1. Passen Sie die VM-Größe nach Bedarf an. (Wir empfehlen VM SKU **D13 v2**.)
1. Lassen Sie **Erweiterte Einstellungen** unverändert.
1. Aktivieren Sie das Kontrollkästchen, nachdem Sie die Preis- und Lizenzbedingungen auf dem Bildschirm überprüft haben, um die Zustimmung anzuzeigen.
1. Klicken Sie auf **Weiter**.
1. Klicken Sie auf dem Bestätigungsbildschirm für die Bereitstellung auf **Bereitstellen**, nachdem Sie die Richtigkeit der Angaben überprüft haben.
1. Sie werden zur Ansicht **In der Cloud gehostete Umgebungen** weitergeleitet und Ihre Umgebung sollte in der Liste angezeigt werden.
1. Ihre angeforderte Umgebung wird so angezeigt, dass sie in die Warteschlange gestellt und anschließend bereitgestellt wurde. Es wird einige Zeit dauern, bis alle Arbeitsabläufe in der Umgebung abgeschlossen sind. Bitte versuchen Sie es nach einigen Stunden (ca. 6 bis 9 Stunden) erneut.
1. Stellen Sie vor dem Fortfahren sicher, dass Ihr Umgebungsstatus **Bereitgestellt** lautet.

![Projekterstellung – Versionen](./media/project1.png)

![Projekterstellung - Topologie 1](./media/project2.png)

![Projekterstellung - Topologie 2](./media/project3.png)

![Projekterstellung – Umgebungsparameter](./media/project4.png)
### <a name="initialize-rcsu"></a>RCSU initialisieren
1. Wählen Sie in der Ansicht **In der Cloud gehostete Umgebungen** Ihre Umgebung aus der Liste aus.
1. Klicken Sie über die Umgebungsansicht rechts im Bildschirm auf **Vollständige Details**. Die Umgebungsdetails werden angezeigt.
1. Klicken Sie unter **UMGEBUNGSFUNKTIONEN** auf **Verwalten**.
1. Klicken Sie über die Registerkarte **Retail** auf **Initialisieren**. Die Ansicht RCSU-Initialisierungsparameter wird angezeigt.
1. Wählen Sie für **REGION** **USA, Osten**, **USA, Osten 2**, **USA, Westen** oder **USA, Westen 2** aus.
1. Wählen Sie für **VERSION** zunächst **Version angeben** aus der Dropdown-Liste aus. Geben Sie dann **9.16.19262.5** im Textfeld an, das unten angezeigt wird. *Hinweis: Stellen Sie sicher, dass Sie **genau die Version angeben**, die hier aufgeführt ist, um zu vermeiden, dass Sie zur Korrektur der Version die RCSU später aktualisieren müssen. *
1. Aktivieren Sie **Erweiterung anwenden**.
1. Wählen Sie aus der Erweiterungsliste unten **Commerce-Vorschaudemobasiserweiterung** aus.
1. Klicken Sie auf **Initialisieren**.
1. Klicken Sie auf dem Bestätigungsbildschirm für die Bereitstellung auf **Ja**, nachdem Sie die Richtigkeit der Angaben überprüft haben.
1. Sie werden zur Ansicht **Retail-Verwaltung** mit aktivierter Registerkarte **Retail** weitergeleitet. Ihre RCSU wurde für die Bereitstellung in die Warteschlange gestellt.
1. Warten Sie, bis Ihr RCSU-Status **SUCCESS** lautet, bevor Sie fortfahren (dies dauert ungefähr 2 bis 5 Stunden).
### <a name="initialize-e-commerce"></a>E-Commerce initialisieren
1. Wechseln Sie zur Registerkarte **E-Commerce (Vorschau)**.
1. Klicken Sie nach der Überprüfung der Vorschau-Zustimmung auf **Einstellungen**.
1. Geben Sie einen Namen für **E-Commerce-Mandantenname** ein. Beachten Sie jedoch, dass dies in einigen URLs sichtbar ist, die auf Ihre E-Commerce-Instanz verweisen.
1. Wählen Sie für **Retail Cloud Sale Unit-Name** Ihre RCSU aus der Liste aus (Liste sollte nur eine Option haben).
1. **E-Commerce-Geografie** wird automatisch ausgefüllt und kann nicht geändert werden.
1. Klicken Sie auf **Weiter**, um fortzufahren.
1. Geben Sie für **Unterstützte Hostnamen** eine gültige Domäne (z. B. www.fabrikam.com) ein.
1. Geben Sie für **AAD-Sicherheitsgruppe für Systemadministrator** die AAD SG-ID ein, die Sie als E-Commerce-Systemadministratorgruppe verwenden möchten.
1. Geben Sie für **AAD-Sicherheitsgruppe für Bewertungs- und Prüfungsmoderator** die AAD-SG-ID ein, die Sie für die Bewertungs- und Prüfungsmoderatorgruppe verwenden möchten.
1. Lassen Sie die Werte **B2C** leer (7 Felder, die mit B2C beginnen).
1. Lassen Sie **Bewertungs- und Prüfungsdienst aktivieren** aktiviert.
1. Klicken Sie auf **Initialisieren**.
1. Sie werden zur Ansicht **Retail-Verwaltung** mit aktivierter Registerkarte **E-Commerce (Vorschau)** weitergeleitet. Ihre E-Commerce-Initialisierung wurde gestartet.
1. Warten Sie, bevor Sie fortfahren, bis Ihr E-Commerce-Initialisierungsstatus **INITIALISIERUNG ERFOLGREICH** lautet.
1. Unter **LINKS** rechts unten.
    * Notieren Sie sich den Link **E-Commerce-Site**. Dies ist der Link zum Stammverzeichnis Ihre C2-Site.
    * Notieren Sie sich den Link **E-Commerce-Site-Verwaltungstool**. Dies ist der Link zum Site-Verwaltungstool (C1-Erstellungstool).
## <a name="post-provisioning-steps"></a>Schritte nach der Bereitstellung
Zu diesem Zeitpunkt wurde die Umgebung als End-to-End-Umgebung bereitgestellt, es müssen jedoch noch einige Konfigurationsschritte ausgeführt werden, bevor Sie mit der Evaluierung der Umgebung beginnen können.
### <a name="before-starting"></a>Vor dem Start
1. Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.
1. Wählen Sie Ihre Umgebung aus der Liste aus.
1. Klicken Sie über die Umgebungsinformationen rechts auf **Vollständige Details**.
1. Klicken Sie auf **Anmelden**, um ein Menü zu öffnen, und wählen Sie **An Umgebung anmelden** aus.

Stellen Sie sicher, dass die juristische Person **USRT** (oben rechts) ausgewählt ist.

### <a name="configure-pos"></a>POS konfigurieren
##### <a name="associate-worker-with-your-identity"></a>Mitarbeiter Ihrer Identität zuordnen
1. Navigieren Sie über das Menü links zu **Module > Retail > Mitarbeiter > Arbeitskräfte**.
1. Suchen Sie in der Liste den Datensatz **000713 - Andrew Collette**, und wählen Sie ihn aus.
1. Klicken Sie im Aktivitätsbereich auf **Retail**.
1. Klicken Sie auf **Vorhandene Identität zuordnen**.
1. Geben Sie im Feld **E-Mail** (rechts neben **Suchen mithilfe von E-Mails**) Ihre E-Mail-Adresse ein.
1. Klicken Sie auf **Suchen**.
1. Wählen Sie den Datensatz mit Ihrem Namen aus.
1. Klicken Sie auf **OK**.
1. Klicken Sie auf **Speichern**.
##### <a name="activate-cloud-pos"></a>Aktivieren von Cloud POS
1. Melden Sie sich beim LCS-Portal an.
1. Navigieren Sie zu Ihrem Projekt.
1. Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.
1. Wählen Sie Ihre Umgebung aus der Liste aus.
1. Klicken Sie über die Umgebungsinformationen rechts auf **Vollständige Details**.
1. Klicken Sie auf **Anmelden**, um ein Menü zu öffnen, wählen Sie **Bei Cloud Point of Sale anmelden**. Der POS sollte geladen werden.
1. Klicken Sie auf **Weiter**.
1. Melden Sie sich mit Ihrem AAD-Konto an.
1. Wählen Sie unter **Shopname** **San Francisco** aus.
1. Klicken Sie auf **Weiter**.
1. Wählen Sie unter **Register und Gerät** **SANFRAN-1** aus.
1. Klicken Sie auf **Aktivieren**.
1. Sie sollten abgemeldet sein und zum POS-Anmeldebildschirm gelangen.
1. Sie können sich nun bei der Cloud POS-Erfahrung mit der Operator-ID **000713** und dem Kennwort **123** anmelden.
### <a name="site-setup"></a>Site-Einstellungen
1. Melden Sie sich bei dem **Site-Verwaltungstool** mit der URL an, die Sie zuvor notiert haben.
1. Klicken Sie auf die Site **Fabrikam**, um das Einstellungsdialogfeld der Site zu öffnen.
1. Wählen Sie für Domäne die Domäne aus, die Sie zuvor beim Initialisieren von E-Commerce eingegeben haben.
1. Wählen Sie als Standardkanal **Erweiterter Fabrikam Online-Store** aus. *Hinweis: Stellen Sie sicher, dass Sie **erweiterter** Online-Store* auswählen.
1. Wählen Sie als Standardsprache **de-de** aus.
1. Lassen Sie den **Pfad** unverändert.
1. Klicken Sie auf **OK**.
1. Sie werden zur Liste der Seiten auf der Site weitergeleitet.
### <a name="enable-jobs"></a>Aufträge aktivieren
1. Melden Sie sich bei der Umgebung (HQ) an.
1. Navigieren Sie über das Menü links zu **Retail > Abfragen und Berichte > Batchaufträge**.
1. Führen Sie für jeden Auftrag in der folgenden Liste die folgenden Schritte aus:
    * **Einzelhandelsauftrag für E-Mail-Benachrichtigung verarbeiten**.
    * **Produktverfügbarkeit**.
    * **P-0001**.
    * **Einzelvorgang für Aufträge synchronisieren**.
1. Verwenden Sie den Schnellfilter, um nach dem Auftrag anhand seines Namens zu suchen (siehe oben).
1. Wenn der Status des Auftrags **Zurückhalten** lautet, führen Sie die folgenden Schritte aus:
    1. Wählen Sie den Datensatz aus.
    1. Öffnen Sie über den Aktivitätsbereich das Menüband **Batchauftrag** aus und klicken Sie auf **Status ändern**.
    1. Wählen Sie **Im Wartezustand** aus, und klicken Sie dann auf **OK**.
### <a name="run-full-data-sync"></a>Vollständige Datensynchronisierung ausführen
1. Navigieren Sie über das Menü links zu **Module > Retail > Zentralverwaltungseinrichtung > Retail Steuerprogramm > Kanaldatenbank**.
1. Der **Standard**-Kanal wird aus der Liste links ausgewählt. *Wählen Sie den anderen verfügbaren Kanal (mit der Bezeichnung **scXXXXXXXXX**)* aus.
1. Klicken Sie über den Aktivitätsbereich auf **Vollständige Datensynchronisierung**.
1. Geben Sie **9999** als Vertriebsplan ein.
1. Klicken Sie auf **OK**.
1. Klicken Sie auf **OK**.
### <a name="after-these-steps-you-are-ready-to-start-evaluating-your-preview-environment"></a>Nach diesen Schritten können Sie mit der Evaluierung Ihrer Vorschauumgebung beginnen!
Verwenden Sie die URL **E-Commerce-Site-Verwaltungstool**, um zur C1-Erstellungserfahrung zu navigieren, und die URL **E-Commerce-Site**, um zur C2-Site-Erfahrung zu navigieren.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
### <a name="how-to-find-your-aad-tenant-id"></a>So finden Sie Ihre AAD-Mandanten-ID
Die AAD-Mandanten-ID ist eine GUID und sieht wie dieses Beispiel aus: **72f988bf-86f1-41af-91ab-2d7cd011db47**
##### <a name="from-azure-portal"></a>Über das Azure-Portal
1. Anmeldung beim Azure-Portal: https://portal.azure.com/
1. Stellen Sie sicher, dass Sie das richtige Verzeichnis ausgewählt haben.
1. Klicken Sie über das Menü links auf **Azure Active Directory**.
1. Wählen Sie **Eigenschaften** unter **Verwalten** aus.
1. Die AAD-Mandanten-ID wird unter **Verzeichnis-ID** angezeigt.
##### <a name="from-openid-connect-metadata"></a>Über OpenID Connect-Metadaten
Erstellen Sie eine **OpenID-URL**, indem Sie **\{YOUR_DOMAIN\}** durch Ihre Domäne ersetzen, microsoft.com: https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration wird beispielsweise zu https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration

1. Navigieren Sie zu **OpenID-URL**, die Ihre Domäne enthält.
1. Die AAD-Mandanten-ID kann in mehreren Eigenschaftswerten angezeigt werden.
1. Suchen Sie **authorization_endpoint** und extrahieren Sie die GUID direkt nach **login.microsoftonline.com/**.
### <a name="how-to-find-the-id-of-your-aad-security-group"></a>So finden Sie die ID Ihrer AAD-Sicherheitsgruppe
Die AAD-Sicherheitsgruppen-ID ist eine GUID und sieht wie dieses Beispiel aus: **436ea7f5-ee6c-40c1-9f08-825c5811066a**

In diesem Schritt wird davon ausgegangen, dass der Benutzer Mitglied der Gruppe ist, für die er die ID ermitteln möchte.
1. Navigieren Sie zum Diagramm-Explorer: https://developer.microsoft.com/en-us/graph/graph-explorer#
1. Klicken Sie auf **Bei Microsoft anmelden** und melden Sie sich mit Ihren Anmeldeinformationen an.
1. Klicken Sie nach dem Anmelden links auf **Weitere Beispiele anzeigen**.
1. Aktivieren Sie **Gruppen** über den rechten Bereich.
1. Schließen Sie den rechten Bereich.
1. Klicken Sie auf **Alle Gruppen, denen ich angehöre**.
1. Suchen Sie Ihre Gruppe über das Textfeld **Antwortvorschau**.
1. Die Sicherheitsgruppen-ID ist unter der Eigenschafts-**ID** notiert.
### <a name="test-credit-card-information-to-perform-test-purchases"></a>Testen der Kreditkartendaten, um Testkäufe durchzuführen
Um Testtransaktionen auf der Site durchzuführen, können Sie diese Testkreditkartendaten verwenden:

Kartennummer: 4111-1111-1111-1111, Ablauf: 10/20, CVV: 737

*Hinweis: Sie sollten unter keinen Umständen versuchen, die tatsächlichen Kreditkarteninformationen auf der Testseite zu verwenden!*
### <a name="useful-links"></a>Nützliche Links
* [LCS (Lifecycle Services)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)
* [RCSU (Retail Cloud Scale Unit)](https://docs.microsoft.com/en-us/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)
* [Microsoft Azure-Portal](https://azure.microsoft.com/en-us/features/azure-portal)
* [Dynamics 365 Commerce-Website](https://aka.ms/Dynamics365CommerceWebsite)
* [Hilferessourcen für Dynamics 365 Retail](../retail/index.md)
### <a name="microsoft-dynamics-365-commerce-preview-support"></a>Microsoft Dynamics 365 Commerce-Vorschauunterstützung
Wenn beim Ausführen der Bereitstellungsschritte Probleme auftreten, schauen Sie sich die [Microsoft Dynamics 365 Commerce Vorschau Yammer-Gruppe](https://aka.ms/Dynamics365CommercePreviewYammer) an, um weitere Hilfe zu erhalten. 

Wenn Sie Probleme beim Zugriff auf die Yammer-Gruppe haben, erreichen Sie uns auch per E-Mail unter **Dynamics365Commerce@microsoft.com**. Diese E-Mail-Adresse wird nicht aktiv überwacht. Erwarten Sie daher eine Verzögerung bei der Antwort.
***
## <a name="prerequisites-for-optional-features"></a>Voraussetzungen für optionale Funktionen
Wenn Sie die Transaktions-E-Mail-Funktionen bewerten möchten, müssen die folgenden Voraussetzungen erfüllt sein:
* Ihnen steht ein E-Mail-Server (SMTP-Server) zur Verfügung, der über das Azure-Abonnement verwendet werden kann, auf dem Sie die Vorschauumgebung bereitstellen.
* Sie verfügen über den vollqualifizierten Domänennamen/die vollqualifizierte IP-Adresse, die SMTP-Portnummer und die Authentifizierungsdetails des Servers.

Wenn Sie Verwaltungsfunktionen für digitale Medienobjekte evaluieren, insbesondere neue Mehrkanal-Bilder aufnehmen möchten, müssen die folgenden Voraussetzungen erfüllt sein:
* Ihr **CMS-Mandantenname** muss verfügbar sein. Anweisungen zum Auffinden dieses Namens finden Sie unten.
### <a name="configure-image-backend-optional"></a>Konfigurieren des Image-Backend (optional)
##### <a name="finding-your-media-base-url"></a>Auffinden Ihrer medienbasierten URL
*Hinweis: Bevor Sie diesen Schritt ausführen können, müssen Sie **Site-Einstellung** abschließen.*
1. Melden Sie sich bei dem Site-Verwaltungstool mit der URL an, die Sie zuvor notiert haben.
1. Öffnen Sie die Site **Fabrikam**.
1. Wählen Sie **Medienobjekte** aus dem Menü links aus.
1. Wählen Sie ein einzelnes Image-Medienobjekt aus.
1. Suchen Sie **Öffentliche URL** aus dem Eigenschafteninspektor rechts aus. Er besitzt eine URL.
    * Beispiel-URL: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC
1. Ersetzen Sie den letzten Bezeichner in der URL (MA1nQC in der obigen Beispiel-URL) durch die folgende Zeichenfolge: **search?fileName=**
    * Beispiel-URL nach dem Austausch: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=
    * Dies ist die **Medienbasierte URL** - notieren Sie sich diese.
##### <a name="updating-the-media-base-url"></a>Aktualisieren der medienbasierten URL
1. Melden Sie sich bei der Umgebung (HQ) an.
1. Navigieren Sie über das Menü links zu **Module > Retail > Kanaleinstellungen > Kanalprofile**.
1. Klicken Sie auf **Bearbeiten**.
1. Ersetzen Sie über **Profileigenschaften** den Eigenschaftswert für **Media Server-Basis-URL** durch **Medienbasierte URL**, die Sie zuvor erstellt haben.
1. Wählen Sie den anderen Kanal aus der Liste links unter dem Kanal **Standard** aus.
1. Klicken Sie unter **Profileigenschaften** auf **+ Hinzufügen**.
1. Wählen Sie für die hinzugefügte Eigenschaft **Media Server-Basis-URL** als Eigenschaftsschlüssel aus, und geben Sie für den Eigenschaftswert die **Medienbasierte URL** ein, die Sie vorher erstellt haben.
1. Klicken Sie auf **Speichern**.

### <a name="configure-email-server-optional"></a>Konfigurieren des E-Mail-Servers (optional)
Beachten Sie, dass der SMTP-Server oder E-Mail-Dienst, den Sie hier eingeben, über das Azure-Abonnement zugänglich sein muss, das Sie für die Umgebung verwenden.
1. Melden Sie sich bei der Umgebung (HQ) an.
1. Navigieren Sie über das Menü links zu **Module > Retail > Zentralverwaltungseinrichtung > Parameter > E-Mail-Parameter**.
1. Klicken Sie auf die Registerkarte **SMTP-Einstellungen**.
1. Geben Sie im Feld **Name des SMTP-Servers** den vollständig qualifizierten Domänennamen oder die IP-Adresse Ihres SMTP-Servers oder Ihres E-Mail-Dienstes ein.
1. Geben Sie im Feld **SMTP-Anschlussnummer** die Portnummer ein (Standard ist 25, wenn nicht SSL verwendet wird).
1. Geben Sie im Feld **Benutzername** einen Wert ein (falls Authentifizierung erforderlich ist).
1. Geben Sie im Feld **Kennwort** einen Wert ein (falls Authentifizierung erforderlich ist).
1. Klicken Sie auf **Speichern**.
1. Klicken Sie auf **Aktualisieren**.
1. Klicken Sie auf die Registerkarte **Test-E-Mail**.
1. Wählen Sie im Feld für den E-Mail-Anbieter **SMTP** aus.
1. Geben Sie im Feld **Senden an** die E-Mail-Adresse ein, an die die Test-E-Mail gesendet werden soll.
1. Klicken Sie auf **Test-E-Mail senden**.
### <a name="configure-email-templates-optional"></a>Konfigurieren der E-Mail-Vorlagen (optional)
Die E-Mail-Vorlage für jedes Transaktionsereignis, für das Sie E-Mails senden möchten, muss mit einer gültigen Absender-E-Mail-Adresse aktualisiert werden.
1. Navigieren Sie über das Menü links zu **Module > Organisationsverwaltung > Einstellungen > Organisations-E-Mail-Vorlagen**.
1. Klicken Sie auf **Liste anzeigen**.
1. Gehen Sie bei jeder Vorlage in der Liste folgendermaßen vor:
    1. Geben Sie im Feld **E-Mail des Absenders** die E-Mail-Adresse des Absenders für diese E-Mail-Vorlage ein.
    1. (Optional) Geben Sie im Feld **Absendername** einen Namen ein, der als Absender für diese E-Mail-Vorlage verwendet wird.
1. Klicken Sie auf **Speichern**.
### <a name="customizing-email-templates-optional"></a>Anpassen der E-Mail-Vorlagen (optional)
Sie können die E-Mail-Vorlagen anpassen, um andere Bilder zu verwenden, oder die Links in der Vorlage aktualisieren, um wieder auf Ihre Vorschauumgebung zuzugreifen. In den folgenden Schritten wird erläutert, wie Sie die Standardvorlagen herunterladen, anpassen und die Vorlagen im System aktualisieren.
1. Laden Sie über einen Browser [die Datei Microsoft Dynamics 365 Commerce-Vorschau-Standard-E-Mail-Vorlagen .zip](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip), die die folgenden HTML-Dokumente enthält, auf Ihren lokalen Computer herunter.
    1. Auftragsbestätigungsvorlage
    1. Geschenkkartenvorlage ausstellen
    1. Neue Auftragsvorlage
    1. Verpackungsvorlage
    1. Entnahmevorlage
1. Passen Sie die Vorlagen mit einem Text- oder HTML-Editor an. Eine Liste der unterstützten Token finden Sie weiter unten.
1. Melden Sie sich bei der Umgebung (HQ) an.
1. Navigieren Sie über das Menü links zu **Module > Retail > Zentralverwaltungseinrichtung > Parameter > Organisations-E-Mail-Vorlagen**.
1. Erweitern Sie die Liste auf der linken Seite, um alle Vorlagen anzuzeigen.
1. Führen Sie für jede der Vorlagen, die Sie anpassen möchten, die folgenden Schritte aus:
    1. Wählen Sie die Vorlage aus der Liste aus.
    1. Wählen Sie unter **Inhalt der E-Mail-Nachricht** die entsprechende Sprachversion aus der Liste aus (Standard **de-de**).
    1. Klicken Sie unter **Inhalt der E-Mail-Nachricht** auf **Bearbeiten**. Der Bereich **E-Mail-Vorlage hochladen** sollte geöffnet werden.
    1. Klicken Sie auf **Durchsuchen** und suchen Sie die HTML-Datei mit dem angepassten Inhalt.
    1. Klicken Sie auf **Hochladen** Ihre Vorlage wird in das System hochgeladen und eine Vorschau wird angezeigt.
    1. Klicken Sie auf **OK**.
    1. (Optional) Passen Sie die Eigenschaft **Betreff** der Vorlage an.
    1. Klicken Sie auf **Speichern**.

#### <a name="supported-tokens-in-the-email-template"></a>Unterstützte Token in der E-Mail-Vorlage
Diese Token werden beim Rendern per E-Mail durch die tatsächlichen Werte ersetzt, die für den Kunden und dessen Bestellung gelten.

**Auftrag** - Die folgenden Token gelten für den gesamten Auftrag.

|Name des Token|Token |
|---|---|
|Auftragsnummer|%salesid%|
|Debitorenname|%customername%|
|Lieferadresse|%deliveryaddress%|
|Rechnungsadresse|%customeraddress%|
|Spätestens|%shipdate%|
|Liefermodus|%modeofdelivery%|
|Skonto|%discount%|
|Mehrwertsteuer|%tax%|
|Bestellung gesamt|%total%|

**Verkaufsposition** - Die folgenden Token werden für jedes Produkt im Auftrag aufgefüllt.

*Hinweis: Platzieren Sie die Token **Produktliste - Start** und **Produktliste - Ende** am Anfang und am Ende jedes HTML-Blocks, der sich für jedes Produkt wiederholt.*

|Name des Token|Token |
|---|---|
|Produktliste - Start|\<!--%tablebegin.salesline% -->|
|Produktliste - Ende|\<!--%tableend.salesline%-->|
|Produktname|%lineproductname%|
|Beschreibung|%lineproductdescription%|
|Leistung|%linequantity%|
|Preiseinheit der Position|%lineprice% (prüfen)|
|Positionsartikel gesamt|%linenetamount%|
|Positionsrabatt|%linediscount%|
|Versanddatum|%lineshipdate%|
|Beschaffungsmethode|%linedeliverymode%|
|Lieferadresse|%linedeliveryaddress%|
|Verkaufseinheit der Position|%lineunit%|

