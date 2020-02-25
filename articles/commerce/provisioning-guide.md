---
title: Bereitstellen einer Dynamics 365 Commerce-Vorschauumgebung
description: In diesem Thema wird erläutert, wie eine Vorschauumgebung in Microsoft Dynamics 365 Commerce bereitgestellt wird.
author: psimolin
manager: annbe
ms.date: 01/31/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cbd4c118de2e91c8849461b20a01403049a07e66
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024635"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a>Bereitstellen einer Dynamics 365 Commerce-Vorschauumgebung


[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie eine Vorschauumgebung in Dynamics 365 Commerce bereitgestellt wird.

Bevor Sie beginnen, empfehlen wir, dass Sie einen kurzen Blick in dieses Thema werfen, um eine Vorstellung davon zu bekommen, was der Prozess erfordert.

> [!NOTE]
> Wenn Sie noch keinen Zugriff auf die Dynamics 365 Commerce-Vorschau erhalten haben, können Sie einen Zugriff auf die Vorschau über die [Dynamics 365 Commerce-Website](https://aka.ms/Dynamics365CommerceWebsite) anfordern.

## <a name="overview"></a>Übersicht

Um Ihre Commerce-Vorschauumgebung erfolgreich bereitzustellen, müssen Sie ein Projekt mit einem bestimmten Produktnamen und -Typ erstellen. Bei der Umgebung und der Commerce-Skalierungseinheit (CSU) gibt es auch einige spezifische Parameter, die Sie verwenden müssen, um später E-Commerce bereitstellen zu können. In den Anweisungen in diesem Thema werden alle Schritte, die zum Ausführen der Bereitstellung erforderlich sind, sowie die Parameter, die Sie verwenden müssen, beschrieben.

Nach der erfolgreichen Bereitstellung Ihrer Commerce-Vorschauumgebung müssen Sie einige Schritte nach der Bereitstellung ausführen, um Ihre Vorschauumgebung vorzubereiten. Einige Schritte sind optional, je nachdem, welche Aspekte des Systems Sie bewerten möchten. Sie können die optionalen Schritte später jederzeit ausführen.

Informationen zum Konfigurieren Ihrer Commerce-Vorschauumgebung nach deren Bereitstellung finden Sie unter [Konfigurieren Sie eine Commerce-Vorschauumgebung](cpe-post-provisioning.md). Informationen zum Konfigurieren optionaler Funktionen für Ihre Commerce-Vorschauumgebung erhalten Sie unter [Optionale Funktionen für eine Commerce-Vorschauumgebung konfigurieren](cpe-optional-features.md).

Wenn Sie Fragen zu den Bereitstellungsschritten haben oder auf Probleme stoßen, teilen Sie Microsoft dies bitte in der [Microsoft Dynamics 365 Commerce Vorschau Yammer-Gruppe](https://aka.ms/Dynamics365CommercePreviewYammer) mit.

## <a name="prerequisites"></a>Voraussetzungen

Die folgenden Voraussetzungen müssen erfüllt sein, damit Sie Ihre Commerce-Vorschauumgebung bereitstellen können:

- Sie haben Zugriff auf das Microsoft Dynamics Lifecycle Services-Portal (LCS).
- Sie sind ein bestehender Partner oder Kunde von Microsoft Dynamics 365 und können ein Dynamics 365 Commerce-Projekt erstellen.
- Sie wurden beim Dynamics 365 Commerce-Vorschauprogramm angenommen.
- Sie besitzen die erforderlichen Berechtigungen, um ein Projekt für **Migrieren, Erstellen von Lösungen und Kennenlernen von** zu erstellen.
- Sie sind Mitglied der Rolle **Umgebungsmanager** oder **Projektverantwortlicher** in dem Projekt, in dem Sie die Umgebung bereitstellen.
- Sie haben Administratorzugriff auf Ihr Microsoft Azure-Abonnement oder wenden sich an einen Abonnementadministrator, der in Ihrem Namen die beiden Schritte abschließen kann, für die Administratorberechtigungen erforderlich sind.
- Ihnen liegt Ihre Azure Active Directory-Mandanten-ID (Azure AD) vor.
- Sie haben eine Azure AD-Sicherheitsgruppe erstellt, die als E-Commerce-Systemadministrator-Gruppe verwendet wird, und Ihnen liegt deren ID vor.
- Sie haben eine Azure AD-Sicherheitsgruppe erstellt, die als Bewertungs- und Prüfungsmoderatorgruppe verwendet wird, und Ihnen liegt deren ID vor. (Diese Sicherheitsgruppe kann mit der Administratorgruppe des E-Commerce-Systems identisch sein.)

## <a name="provision-your-commerce-preview-environment"></a>Bereitstellen Ihrer Commerce-Vorschauumgebung

In diesen Verfahren wird erläutert, wie eine Commerce-Vorschauumgebung bereitgestellt wird. Nachdem Sie sie erfolgreich abgeschlossen haben, kann die Commerce-Vorschauumgebung konfiguriert werden. Alle hier beschriebenen Aktivitäten finden im LCS-Portal statt.

> [!IMPORTANT]
> Der Vorschauzugriff ist an das LCS-Konto und die Organisation gebunden, die Sie in Ihrer Commerce-Vorschauanwendung angegeben haben. Sie müssen dasselbe Konto verwenden, um die Commerce-Vorschauumgebung bereitzustellen. Wenn Sie ein anderes LCS-Konto oder einen anderen Mandanten für die Commerce-Vorschauumgebung verwenden müssen, müssen Sie diese Details Microsoft bereitstellen. Kontaktinformationen finden Sie im Abschnitt [Unterstützung der Commerce-Vorschauumgebung](#commerce-preview-environment-support) weiter unten in diesem Thema.

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a>Bestätigen, dass die Vorschaufunktionen verfügbar und im LCS aktiviert sind

Um zu bestätigen, dass die Vorschaufunktionen verfügbar und im LCS aktiviert sind, gehen Sie folgendermaßen vor.

1. Melden Sie sich beim [LCS-Portal](https://lcs.dynamics.com) über dasselbe LCS-Konto an, mit dem Sie den Zugriff auf die Vorschau angefordert haben.
1. Scrollen Sie auf der LCS-Startseite ganz nach rechts, und wählen Sie auf die Kachel **Verwaltung von Vorschaufunktionen** aus.

    ![Vorschau von Verwaltungskacheln](./media/preview1.png)

1. Scrollen Sie nach unten zu **Private Vorschaufunktionen**, und bestätigen Sie, dass die folgenden Funktionen verfügbar und aktiviert sind:

    - E-Commerce-Bewertung
    - Commerce-Vorschau-Programmumgebungen

    ![Private Vorschaufunktionen](./media/preview2.png)

1. Wenn diese Funktionen nicht in der Liste aufgeführt sind, wenden Sie sich an Microsoft und geben Sie Ihre geschäftliche E-Mail-Adresse, Ihr LCS-Konto und Ihre Mandantendetails an. Kontaktinformationen finden Sie im Abschnitt [Unterstützung der Commerce-Vorschauumgebung](#commerce-preview-environment-support).

### <a name="create-a-new-project"></a>Neues Projekt erstellen

Gehen Sie folgendermaßen vor, um ein neues Projekt in LCS zu erstellen.

1. Wählen Sie auf der LCS-Startseite das Pluszeichen (**+**) aus, um ein Projekt zu erstellen.
1. Führen Sie im rechten Bereich einen der folgenden Schritte aus:

    - Wenn Sie ein Partner sind, wählen Sie **Migrieren, Erstellen von Lösungen und Kennenlernen von** aus.
    - Wenn Sie ein Debitor sind, wählen Sie **Künftige Presales** aus.

1. Geben Sie einen Namen, eine Beschreibung und die Branche ein.
1. Wählen Sie im Feld **Produktname** die Option **Dynamics 365 Retail** aus.
1. Wählen Sie im Feld **Produktversion** die Option **Dynamics 365 Retail** aus.
1. Wählen Sie im Feld **Methode** **Dynamics Retail-Implementierungsmethode** aus.
1. Optional: Sie können Rollen und Benutzer aus einem vorhandenen Projekt importieren.
1. Wählen Sie **Erstellen** aus. Die Projektansicht wird angezeigt.

### <a name="add-the-azure-connector"></a>Azure-Connector hinzufügen

Gehen Sie folgendermaßen vor, um den Azure Connector zu Ihrem LCS-Projekt hinzuzufügen.

1. Führen Sie einen dieser Schritte aus:

    - Wenn Sie ein Partner sind, wählen Sie die Kachel **Projekteinstellungen** ganz rechts aus.
    - Wenn Sie ein Debitor sind, wählen Sie **Projekteinstellungen** aus dem oberen Menü aus.

1. Wählen Sie **Azure-Connector**.
1. Wählen Sie **Hinzufügen** aus, um Azure Connector hinzuzufügen.
1. Geben Sie einen Namen ein.
1. Geben Sie Ihre Azure-Abonnement-ID ein.
1. Aktivieren Sie die Option **Verwendung von Azure Resource Manager konfigurieren**.
1. Überprüfen Sie, dass die **AAD-Mandantendomäne (oder ID) des Azure-Abonnements** gültig ist. Wenden Sie sich bei Bedarf an Ihren Azure-Abonnementadministrator.
1. Wählen Sie **Weiter**.
1. Befolgen Sie die Anweisungen auf der Seite, um den entsprechenden Anwendungen Zugriff auf Ihr Abonnement zu gewähren. Wenden Sie sich bei Bedarf an Ihren Azure-Abonnementadministrator.

    1. Melden Sie sich beim [Azure-Portal](https://portal.azure.com/) an.
    1. Stellen Sie sicher, dass das richtige Verzeichnis ausgewählt ist, und wählen Sie dann im Menü auf der linken Seite **Abonnements** aus.
    1. Suchen Sie das richtige Abonnement in der Liste, und wählen Sie es aus. Verwenden Sie nach Bedarf die Suchfunktion.
    1. Wählen Sie im Menü **Zugangskontrolle (IAM)** aus.
    1. Wählen Sie rechts unter **Rollenzuweisung hinzufügen** die Option **Hinzufügen** aus. Der Bereich **Rollenzuweisung hinzufügen** wird angezeigt.
    1. Wählen Sie im Feld **Rolle** **Mitwirkender** aus.
    1. Lassen Sie im Feld **Zugriff gewähren auf** den Standardwert **Azure AD-Benutzer, -Gruppe oder -Serviceprinzipal** leer.
    1. Geben Sie unter **Auswählen** **b96b7e94-b82e-4e71-99a0-cf7fb188acea** ein.
    1. Wählen Sie **Dynamics-Bereitstellungsdienste \[wsfed-enabled\]** in der Liste aus.
    1. Wählen Sie **Speichern**.

1. Wählen Sie **Weiter**.
1. Befolgen Sie die Anweisungen auf der Seite, um den entsprechenden Anwendungen Zugriff auf Ihr Abonnement zu gewähren. Wenden Sie sich bei Bedarf an Ihren Azure-Abonnementadministrator.
1. Wählen Sie **Weiter**.
1. Wählen Sie im Feld **Azure-Region** **USA, Osten**, **USA, Osten 2**, **USA, Westen** oder **USA, Westen 2** aus.
1. Wählen Sie **Verbinden** aus. Ihr Azure Connector sollte in der Liste angezeigt werden.

### <a name="import-the-commerce-preview-demo-base-extension"></a>Importieren Sie die Commerce Preview Demo Base Extension

Gehen Sie folgendermaßen vor, um die Commerce Preview Demo Base Extension in Ihrem Projekt zu importieren.

1. Öffnen Sie die Homepage für Ihr Projekt, indem Sie oben den Projektnamen auswählen.
1. Führen Sie einen dieser Schritte aus:

    - Wenn Sie ein Partner sind, wählen Sie die Kachel **Asset-Bibliothek** ganz rechts aus.
    - Wenn Sie ein Debitor sind, wählen Sie **Asset-Bibliothek** aus dem oberen Menü aus.

1. Wählen Sie **Bereitstellbares Softwarepaket** aus der Liste links aus.
1. **Import** auswählen
1. Wählen Sie **Commerce-Vorschaudemobasiserweiterung** in der Liste der Medienobjekte unter **Gemeinsame Objektbibliothek** aus.
1. Wählen Sie **Entnehmen** aus. Sie kehren zur Objektbibliothek zurück und sollten die Erweiterung in der Liste sehen.

Die folgende Abbildung zeigt die Aktionen, die auf der LCS-Seite **Objektbibliothek** ausgeführt werden müssen.

![Importieren Sie die Commerce Preview Demo Base Extension](./media/import.png)

### <a name="deploy-the-environment"></a>Bereitstellen der Umgebung

Gehen Sie folgendermaßen vor, um die Umgebung bereitzustellen.

> [!NOTE]
> Möglicherweise müssen Sie die Schritte 6, 7 und/oder 8 nicht ausführen, da Seiten mit einer einzelnen Option übersprungen werden. Wenn Sie sich in der Ansicht **Umgebungsparameter** befinden, bestätigen Sie, dass der Text **Dynamics 365 Commerce – Demo (10.0.* x* mit Plattform-Update *xx*)** direkt über dem Feld **Umgebungsname** angezeigt wird. Weitere Details finden Sie in der Abbildung, die nach Schritt 8 angezeigt wird.

1. Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.
1. Wählen Sie **Hinzufügen** aus, um eine Umgebung hinzuzufügen.
1. Wählen Sie im Feld **Anwendungsversion** die aktuellste Version aus. Wenn Sie aus einem bestimmten Grund eine andere Anwendungsversion als die aktuellste auswählen müssen, wählen Sie keine Version vor **10.0.8** aus.
1. Verwenden Sie im Feld **Plattformversion** die Plattformversion, die automatisch für die von Ihnen ausgewählte Anwendungsversion ausgewählt wird. 

    ![Auswählen von Anwendungs- und Plattformversionen](./media/project1.png)

1. Wählen Sie **Weiter**.
1. Wählen Sie **Demo** als Umgebungstopologie aus.

    ![Auswählen der Umgebungstopologie 1](./media/project2.png)

1. Wählen Sie **Dynamics 365 Commerce – Demo** als Umgebungstopologie aus. Wenn Sie zuvor einen einzelnen Azure Connector konfiguriert haben, wird dieser für diese Umgebung verwendet. Wenn Sie mehrere Azure Connectors konfiguriert haben, können Sie auswählen, welcher Connector verwendet werden soll: **USA, Osten**, **USA 2, Osten**, **USA, Westen** oder **USA2, Westen**. (Für die beste End-to-End-Leistung empfehlen wir, dass Sie **USA 2, Westen**) auswählen.

    ![Auswählen der Umgebungstopologie 2](./media/project3.png)

1. Geben Sie auf der Seite **Umgebung bereitstellen** einen Umgebungsnamen ein. Lassen Sie die erweiterten Einstellungen unverändert.

    ![Bereitstellen der Umgebungsseite](./media/project4.png)

1. Passen Sie die VM-Größe nach Bedarf an. (Wir empfehlen die VM-Lagermengeneinheit \[SKU\] **D13 v2**.)
1. Überprüfen Sie die Preis- und Lizenzbedingungen und aktivieren Sie das Kontrollkästchen, um anzuzeigen, dass Sie diesen zustimmen.
1. Wählen Sie **Weiter**.
1. Prüfen Sie auf der Bestätigungsseite für die Bereitstellung, ob die Details korrekt sind, und wählen Sie dann **Bereitstellen** aus. Sie werden zur Ansicht **In der Cloud gehostete Umgebungen** weitergeleitet, und Ihre Umgebung sollte in der Liste angezeigt werden.

    Ihre angeforderte Umgebung wird so angezeigt, dass sie in die Warteschlange gestellt und anschließend bereitgestellt wurde. Es wird einige Zeit dauern, bis die Arbeitsabläufe in der Umgebung abgeschlossen sind. Versuchen Sie es daher nach ungefähr sechs bis neun Stunden erneut.

1. Stellen Sie vor dem Fortfahren sicher, dass der Status Ihrer Umgebung **Bereitgestellt** lautet.

### <a name="initialize-the-commerce-scale-unit-csu"></a>Initialisieren der Commerce-Skalierungseinheit (CSU)

Führen Sie folgende Schritte aus, um eine CSU zu initialisieren.

1. Wählen Sie in der Ansicht **In der Cloud gehostete Umgebungen** Ihre Umgebung in der Liste aus.
1. Wählen Sie in der Umgebungsansicht rechts die Option **Vollständige Details** aus. Die Ansicht zu Umgebungsdetails wird angezeigt.
1. Wählen Sie unter **Umgebungsfunktionen** die Option **Verwalten** aus.
1. Wählen Sie auf der Registerkarte **Commerce** die Option **Initialisieren** aus. Die Ansicht zu CSU-Initialisierungsparametern wird angezeigt.
1. Wählen Sie im Feld **Region** **USA, Osten**, **USA, Osten 2**, **USA, Westen** oder **USA, Westen 2** aus.
1. Wählen Sie im Feld **Version** die Option **Version angeben** in der Liste aus und, geben Sie dann **9.18.20014.4** im angezeigten Feld an. Stellen Sie sicher, dass Sie die genaue Version angeben, die hier angegeben ist. Andernfalls müssen Sie RCSU später auf die richtige Version aktualisieren.
1. Aktivieren Sie die Option **Erweiterung anwenden**.
1. Wählen Sie aus der Erweiterungsliste **Commerce-Vorschaudemobasiserweiterung** aus.
1. Wählen Sie **Initialisieren** aus.
1. Prüfen Sie auf der Bestätigungsseite für die Bereitstellung, ob die Details korrekt sind, und wählen Sie dann **Ja** aus. In der Ansicht **Commerce-Verwaltung** wird erneut angezeigt, wo die Registerkarte **Commerce** ausgewählt ist. Ihre CSU wurde für die Bereitstellung in die Warteschlange gestellt.
1. Stellen Sie vor dem Fortfahren sicher, dass Ihr CSU-Status **Erfolgreich** lautet. Die Initialisierung dauert ungefähr zwei bis fünf Stunden.

### <a name="initialize-e-commerce"></a>E-Commerce initialisieren

Führen Sie folgende Schritte aus, um e-Commerce zu initialisieren.

1. Prüfen Sie auf der Registerkarte **E-Commerce** die Vorschaueinwilligung und wählen Sie dann **Einrichten** aus.
1. Geben Sie im Feld **E-Commerce-Mandantenname** einen Namen ein. Beachten Sie jedoch, dass dieser Name in einigen URLs sichtbar ist, die auf Ihre E-Commerce-Instanz verweisen.
1. Wählen Sie im Feld **Commerce-Skalierungseinheit-Name** Ihre CSU in der Liste aus. (Die Liste sollte nur eine Option haben.)

    Das Feld **E-Commerce-Geografie** wird automatisch festgelegt und der Wert kann nicht geändert werden.

1. Wählen Sie **Weiter** aus, um fortzufahren.
1. Geben Sie im Feld **Unterstützte Hostnamen** eine gültige Domäne, wie `www.fabrikam.com`, ein.
1.  Geben Sie im Feld **AAD-Sicherheitsgruppe für Systemadministratoren** die ersten Buchstaben des Namens der Sicherheitsgruppe ein, die Sie verwenden möchten. Wählen Sie das Symbol für die Vergrößerungsklasse aus, um die Suchergebnisse anzuzeigen. Wählen Sie die richtige Sicherheitsgruppe aus der Liste aus.
2.  Geben Sie im Feld **AAD-Sicherheitsgruppe für Bewertungs- und Prüfungsmoderator** die ersten Buchstaben des Namens der Sicherheitsgruppe ein, die Sie verwenden möchten. Wählen Sie das Symbol für die Vergrößerungsklasse aus, um die Suchergebnisse anzuzeigen. Wählen Sie die richtige Sicherheitsgruppe aus der Liste aus.
1. Lassen Sie die Optoin **Bewertungs- und Prüfungsdienst aktivieren** aktiviert.
1. Wählen Sie **Initialisieren** aus. In der Ansicht **Commerce-Verwaltung** wird erneut angezeigt, wo die Registerkarte **E-Commerce** ausgewählt ist. Die E-Commerce-Initialisierung wurde gestartet.
1. Warten Sie, bevor Sie fortfahren, bis Ihr E-Commerce-Initialisierungsstatus **Initialisierung erfolgreich** lautet.
1. Notieren Sie sich unten rechts im Bereich **Links** die URLs für die folgenden Links:

    * **E-Commerce-Website** – Der Link zum Stammverzeichnis Ihrer E-Commerce-Website.
    * **E-Commerce-Site-Management-Tool** – Der Link zum Site-Management-Tool.

## <a name="commerce-preview-environment-support"></a>Unterstützung für die Commerce-Vorschauumgebung

Wenn beim Abschließen der Bereitstellungsschritte Probleme auftreten, schauen Sie sich die [Microsoft Dynamics 365 Commerce Vorschau Yammer-Gruppe](https://aka.ms/Dynamics365CommercePreviewYammer) an, um weitere Hilfe zu erhalten.

Wenn Sie Probleme haben, wenn Sie versuchen, auf die Yammer-Gruppe zuzugreifen, können Sie sich per E-Mail unter <Dynamics365Commerce@microsoft.com> an Microsoft wenden. Diese E-Mail-Adresse wird nicht aktiv überwacht. Erwarten Sie daher eine Verzögerung in der Antwort.

## <a name="next-steps"></a>Nächste Schritte

Um den Prozess zum Bereitstellen und Konfigurieren Ihrer Commerce-Vorschauumgebung fortzusetzen, schauen Sie sich [Konfigurieren Sie eine Commerce-Vorschauumgebung](cpe-post-provisioning.md) an.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Dynamics 365 Commerce-Vorschauumgebung – Übersicht](cpe-overview.md)

[Konfigurieren einer Dynamics 365 Commerce-Vorschauumgebung](cpe-post-provisioning.md)

[Konfigurieren optionaler Funktionen für eine Dynamics 365 Commerce-Vorschauumgebung](cpe-optional-features.md)

[Dynamics 365 Commerce-Vorschauumgebung – FAQ](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-Portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-Website](https://aka.ms/Dynamics365CommerceWebsite)

