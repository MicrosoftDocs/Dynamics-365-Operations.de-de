---
title: Modul „Commerce Chat mit Omnichannel for Customer Service“
description: Dieser Artikel beschreibt das Modul „Commerce Chat mit Omnichannel for Customer Service“ in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: 99e8b9d66a04390ab70fd1deff9f95fe28bdfae3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690315"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>Modul „Commerce Chat mit Omnichannel for Customer Service“

[!include [banner](includes/banner.md)]

Dieser Artikel beschreibt das Modul *Commerce Chat mit Omnichannel for Customer Service* in Microsoft Dynamics 365 Commerce.

In der Commerce-Version 10.0.29 wurde der Commerce-Modulbibliothek ein neues Modul zum Commerce-Chat mit Omnichannel for Customer Service hinzugefügt. Die Commerce-Chat-Funktion stellt E-Commerce-Kunden die Chat-Funktionen von Dynamics 365 Omnichannel for Customer Service zur Verfügung, wozu die Unterstützung von Live-Agenten zur Beantwortung von Kundenanfragen, zur Bereitstellung des Kundendienstes und zur Erleichterung der Verkäufe für Commerce-Kunden gehört.

Die Commerce-Chat-Funktion ermöglicht es Einzelhändlern, diese Ziele zu erreichen:

- Steigerung der personalisierten Interaktion mit Kunden, um die Kundenbindung zu verbessern.
- Verbesserung des Kundendienstes durch die Integration von menschlichen Agenten und Self-Service-Chatbots.
- Helfen Sie Agenten dabei, Erfahrungen durch Kundenprofil-, Bestell- und Kaufdaten in Echtzeit zu sammeln, die Betriebsverbesserungen und Kundenbindung fördern.
- Die allgemeine Kundenzufriedenheit verbessern, um den Umsatz zu steigern.

Die folgenden Fähigkeiten sind mit der Commerce-Chat-Funktion verfügbar:

- Commerce Chat mit Omnichannel for Customer Service
- Hinzufügen des **Commerce Callcenter** als Anwendungsregisterkarte in das Agentenerlebnis in Dynamics 365 Omnichannel for Customer Service

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>Voraussetzungen für Omnichannel for Customer Service

Als Voraussetzung müssen Sie den Chat im Verwaltungs-Widget von Omnichannel for Customer Service konfigurieren und einige der Parameter abrufen, um das Commerce-Chat-Erlebnis zu konfigurieren. Weitere Informationen unter [Einen Chat-Kanal konfigurieren](/dynamics365/customer-service/set-up-chat-widget).

Nachdem Sie den Chat im Verwaltungs-Widget von Omnichannel for Customer Service konfiguriert haben, erhalten Sie ein Skript, das dem folgenden Beispiel ähnelt.

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

Kopieren Sie dieses Skript, da Sie die darin enthaltenen Werte benötigen, um das Chat-Modul zu konfigurieren.

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>Pflichtfelder in Commerce Chat mit Omnichannel for Customer Service

Die folgende Tabelle zeigt die Skriptwerte aus dem Verwaltungs-Widget von Omnichannel for Customer Service, die erforderlich sind, um das Modul des Commerce Chat mit Omnichannel for Customer Service zu konfigurieren.

| Widget-Eigenschaft | Description |
| ------------- |--------------|
| Skriptquelle | Der Wert von **src** im Chat-Widget-Skript. |
| Datenanwendungskennung | Der Wert von **data-app-id** im Chat-Widget-Skript. |
| Datenorganisationskennung | Der Wert von **data-org-id** im Chat-Widget-Skript. |
| Datenorganisations-URL | Der Wert von **data-org-url** im Chat-Widget-Skript. |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>Das Commerce-Chat-Erlebnis für Ihre E-Commerce-Site konfigurieren

Eine empfohlene Methode zum Implementieren des Chat-Erlebnisses für Ihre E-Commerce-Website besteht darin, das Modul „Commerce Chat mit Omnichannel for Customer Service“ zum freigegebenen Kopfzeilenfragment hinzuzufügen, das auf den Seiten Ihrer E-Commerce-Website verwendet wird.

Gehen Sie folgendermaßen vor, um das Chatmodul dem Kopfzeilenfragment Ihrer Website im Commerce-Website-Generator hinzuzufügen.

1. Gehen Sie im Website-Generator für Ihre Webite zu **Fragmente**.
1. Wählen Sie **Neu** aus.
1. Wählen Sie im Dialogfeld **Ein Fragment auswählen** das Modul **Commerce Chat mit Omnichannel for Customer Service** aus, geben Sie einen Namen für das Fragment ein und wählen Sie dann **OK** aus.
1. Wählen Sie in der Gliederungsansicht den Slot **Msdyn365 CS Chat-Connector** aus.
1. Führen Sie im Bereich **Chateigenschaften** rechts die folgenden Schritte aus:

    1. Geben Sie ins das Feld **Skriptquelle** den **src**-Wert ein, den Sie aus dem Omnichannel for Customer Service-Skript erhalten haben.
    1. Geben Sie ins das Feld **Datenanwendungskennung** den **data-app-id**-Wert ein, den Sie aus dem Omnichannel for Customer Service-Skript erhalten haben.
    1. Geben Sie ins das Feld **Datenorganisationskennung** den **data-org-id**-Wert ein, den Sie aus dem Omnichannel for Customer Service-Skript erhalten haben.
    1. Geben Sie ins das Feld **Datenorganisation-URL** den **data-org-url**-Wert ein, den Sie aus dem Omnichannel for Customer Service-Skript erhalten haben.

    ![Erstellen eines Commerce-Chat-Modulfragments im Commerce-Webitegenerator.](media/Commerce-chat-creating-new-fragment.png)

1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Gehen Sie zu **Fragmente** und öffnen Sie das Kopfzeilenfragment für Ihre Website.
1. Wählen Sie im Slot **Standardcontainer** die Auslassungspunkte (**...**) und dann **Fragment hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Module auswählen** das Chat-Fragment aus, das Sie zuvor erstellt haben, und wählen Sie dann **OK** aus.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

> [!NOTE]
> Eine vollständige Liste der Konfigurationsparameter finden Sie unter [Proaktive Chat-Parameter des Commerce-Chat-Moduls](chat-proactive-chat-parameters.md).

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>Commerce headquarters als Anwendungsregisterkarte für Omnichannel for Customer Service hinzufügen

Sie können zu eine Anwendungsregisterkarte für Commerce headquarters in Omnichannel for Customer Service hinzufügen. Live-Agenten können dann die Benutzeroberfläche für das Omnichannel for Customer Service-Agentenerlebnis verwenden, um einfach auf das Dynamics 365 Commerce Customer Service-Modul zuzugreifen, das kontextbezogene Informationen für den Kunden zusammen mit seinen Auftragsinformationen enthält. Darüber hinaus können Kundendienstagenten neue Aufträge aufgeben, Rücksendungen einleiten und Informationen zum Auftragsstatus überprüfen.

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>Eine neue Anwendungsregisterkarte erstellen, die Commerce headquarters in ein iFrame Modul lädt 

Gehen Sie wie folgt vor, um eine neue Anwendungsregisterkarte zu erstellen, die Commerce headquarters in ein iFrame Modul lädt.

1. Öffnen Sie das [Power Apps Maker Portal](https://make.powerapps.com).
1. Wählen Sie im linken Navigationsbereich **Apps** aus.
1. Wählen Sie **Kundendienst Admin Center** aus.
1. Gehen Sie zu **Agentenerlebnis**.
1. Wählen Sie für **Vorlagen für Anwendungsregisterkarten** **Verwalten** aus.
1. Erstellen Sie eine neue Anwendungsregisterkarte des Typs **Drittanbieter-Website**. Weitere Anweisungen finden Sie unter [Vorlagen für Anwendungsregisterkarten verwalten](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter).
1. Geben Sie unter **Parameter** im Feld **Wert** des Parameters **URL** die folgende URL ein, wobei Sie `<YourOrganizationHeadquartersURL>` und `<LegalEntityname>` durch die entsprechenden Werte ersetzen. Omnichannel for Customer Service liest **{AccountNumber}** aus dem Chat-Kontext aus. Lassen Sie **{AccountNumber}** deshalb, wie es ist.

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. Lassen Sie das Feld **Wert** des Parameters **Daten** leer.

![Erstellen einer Anwendungsregisterkarte in Dynamics 365 Omnichannel Customer Service.](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>Eine neue Anwendungsregisterkarte für Kundenagenten in Dynamics 365 Omnichannel for Customer Service aktivieren

Gehen Sie wie folgt vor, um eine neue Anwendungsregisterkarte für Kundenagenten in Dynamics 365 Omnichannel for Customer Service zu aktivieren.
    
1. Öffnen Sie das [Power Apps Maker Portal](https://make.powerapps.com).
1. Wählen Sie im linken Navigationsbereich **Apps** aus.
1. Wählen Sie **Kundendienst Admin Center** aus.
1. Gehen Sie zu **Kundensupport \> Arbeitsstream**.
1. Öffnen Sie den Arbeitsstream, den Sie für Ihre Agenten erstellt haben, und wählen Sie dann unter **Erweiterte Einstellungen** **Sitzungsstandard** aus.
1. Wählen Sie unter **Anwendungsregisterkarten** **Vorhandene Anwendungsregisterkarte hinzufügen** aus und fügen Sie dann die neue Anwendungsregisterkarte hinzu, die Sie zuvor erstellt haben. Dieser Schritt stellt sicher, dass eine Anwendungsregisterkarte, die Commerce headquarters in ein iFrame Modul lädt, erscheint, wenn ein Agent einen eingehenden Chat-Anruf von Ihrer E-Commerce-Website erhält.

> [!NOTE]
> Sie können die standardmäßige Chat-Sitzungsvorlage im Workstream nicht ändern. Daher möchten Sie möglicherweise eine neue Vorlage erstellen oder die vorhandene Vorlage duplizieren, um sie zu aktualisieren. Weitere Informationen erhalten Sie unter [Vorlagen mit Arbeitsstream zuordnen](/dynamics365/app-profile-manager/associate-templates).

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>Kontextvariablen in Dynamics 365 Omnichannel for Customer Service hinzufügen

Gehen Sie wie folgt vor, um Kontextvariablen in Dynamics 365 Omnichannel for Customer Service hinzuzufügen.

1. Öffnen Sie das [Power Apps Maker Portal](https://make.powerapps.com).
1. Wählen Sie im linken Navigationsbereich **Apps** aus.
1. Wählen Sie **Kundendienst Admin Center** aus.
1. Gehen Sie zu **Kundensupport \> Arbeitsstream**.
1. Öffnen Sie den Arbeitsstream, den Sie für Ihre Agenten erstellt haben, und gehen Sie dann unter **Erweiterte Einstellungen** zum Abschnitt **Kontextvariable**.
1. Wählen Sie **Bearbeiten** aus und fügen Sie dann **AccountNumber** als Kontextvariable vom Typ **Text** hinzu. Diese Variable hilft Commerce headquarters, Kundeninformationen mit übereinstimmenden Kontonummern zu laden.

> [!NOTE]
> Wenn Sie die E-Mail-Adressen und Namen von angemeldeten Benutzern aus einem E-Commerce-Kanal auslesen möchten, können Sie **E-Mail** und **Name** als Kontextvariablen vom Typ **Text** zusätzlich zur Kontextvariablen **AccountNumber** hinzufügen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die E-Commerce-Chat-Funktionen](commerce-chat-overview.md)

[Commerce Chat mit Power Virtual Agents Modul](chat-module-pva.md)

[Proaktive Chat-Parameter des Commerce Chat-Moduls](chat-proactive-chat-parameters.md)
