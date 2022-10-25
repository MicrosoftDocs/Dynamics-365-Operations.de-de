---
title: Commerce Chat mit Power Virtual Agents Modul
description: Dieser Artikel beschreibt den Commerce Chat mit Power Virtual Agents Modul, das Microsoft Power Virtual Agents mit Dynamics 365 Commerce Webseiten integriert.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691086"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>Commerce Chat mit Power Virtual Agents Modul

[!include [banner](includes/banner.md)]

Dieser Artikel beschreibt den Commerce Chat mit Power Virtual Agents Modul, das Microsoft Power Virtual Agents mit Dynamics 365 Commerce Webseiten integriert.

Der Handels-Chat mit Power Virtual Agents Funktion ermöglicht E-Commerce-Kunden von Dynamics 365 die Nutzung von Power Virtual Agents Chatbot-Funktionen zur Bearbeitung ihrer Anfragen. Ab der Dynamics 365 Commerce Version 10.0.30 kann diese Funktion in E-Commerce-Websites integriert werden, indem der Commerce Chat mit Power Virtual Agents Modul verwendet wird, das Teil der Commerce-Modulbibliothek ist.

Die Commerce Chat mit Power Virtual Agents Funktion hilft Unternehmen, die folgenden Ziele zu erreichen:

- Steigerung der personalisierten Interaktion mit ihren Kunden und Verbesserung der Kundenbindung.
- Verbesserung des Kundendienstes durch die Integration von Self-Service-Chatbots.
- Die allgemeine Kundenzufriedenheit verbessern, und dadurch den Umsatz steigern.

> [!NOTE]
> Um mehr über die Unterschiede zwischen Dynamics 365 Omnichannel for Customer Service und Power Virtual Agents Anwendungen zu erfahren, siehe [Übersicht über die E-Commerce-Chat-Module](/commerce-chat-modules-overview.md).

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a>Voraussetzungen für die Verwendung von Power Virtual Agents

Um die Commerce Chat mit Power Virtual Agents Funktion zu nutzen, müssen Sie zuerst einen Power Virtual Agents Chatbot für Ihre E-Commerce-Website erstellen. Anweisungen finden Sie unter [Erstellen Sie einen Power-Virtual-Agent-Bot](/power-virtual-agents/authoring-first-bot).

Nachdem Sie den Chatbot konfiguriert haben, müssen Sie die Werte der Chatbotparameter **Bot-ID** und **Mandanten-ID** zum Konfigurieren des E-Commerce-Chat-Erlebnisses kopieren. Informationen zum Kopieren dieser Werte finden Sie unter [Rufen Sie Ihre Power Virtual Agents Bot-Parameter ab](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters).

## <a name="configure-your-e-commerce-site"></a>E-Commerce-Website konfigurieren 

Eine empfohlene Methode zum Implementieren des Chat-Erlebnisses für Ihre E-Commerce-Website besteht darin, das Modul Commerce Chat mit Power Virtual Agents zum freigegebenen Kopfzeilenfragment hinzuzufügen, das auf den Seiten Ihrer Website verwendet wird.

Gehen Sie folgendermaßen vor, um das Chatmodul dem Kopfzeilenfragment Ihrer Website im Commerce-Website-Generator hinzuzufügen.

1. Gehen Sie im Commerce Website-Generator für Ihre Webite zu **Fragmente**.
1. Wählen Sie **Neu** aus.
1. Wählen Sie im Dialogfeld **Ein Fragment auswählen** das Modul **Commerce Chat mit Power Virtual Agents** aus, geben Sie einen Namen für das Fragment ein und wählen Sie dann **OK** aus.
1. Wählen Sie in der Gliederungsansicht den Slot **Msdyn365 PVA Chat-Connector** aus.
1. Führen Sie im Bereich Eigenschaften rechts die folgenden Schritte aus:

    1. Belassen Sie im Feld **Bot-Parameter** im Feld **Bot Framework CDN-URL für den Webchat-Chat** den Standardwert (z. B. `https://cdn.botframework.com/botframework-webchat/latest/webchat.js`).
    1. Belassen Sie im Feld **Bot Framework Direct Line Authentifizierungs-URL** den Standardwert (z. B. `https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`).
    1. Geben Sie im Feld **Bot-ID** den Wert Power Virtual Agents **Bot-ID** ein, den Sie in den Abschnitt [Voraussetzungen für die Nutzung von Power Virtual Agents](#prereq) kopiert haben.
    1. Geben Sie im Feld **Mandanten-ID** den **Mandanten-ID** Wert ein, den Sie kopiert haben.

1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Gehen Sie zu **Fragmente** und öffnen Sie das Kopfzeilenfragment für Ihre Website.
1. Wählen Sie im Slot **Standardcontainer** die Auslassungspunkte (**...**) und dann **Fragment hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Module auswählen** das Chat-Fragment aus, das Sie zuvor erstellt haben, und wählen Sie dann **OK** aus.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

## <a name="proactive-chat-parameters"></a>Proaktive Chat-Parameter

Eine vollständige Liste der proaktiven Chat-Konfigurationsparameter finden Sie unter [Proaktive Chat-Parameter des Commerce-Chat-Moduls](chat-proactive-chat-parameters.md).

> [!NOTE]
> Derzeit unterstützt Power Virtual Agents keine Azure Active Directory B2C (Azure AD B2C) Authentifizierung. Es unterstützt nur anonyme Retail Cloud Scale Unit (RCSU)-Aufrufe, um die Produktverfügbarkeit abzurufen oder mit anderen anonymen APIs zu interagieren. Aufrufe an authentifizierte APIs über Power Virtual Agents Chatbots erfordern eine explizite Kundenanmeldung.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die E-Commerce-Chat-Funktionen](commerce-chat-overview.md)

[Modul „Commerce Chat mit Omnichannel for Customer Service“](commerce-chat-module.md)

[Proaktive Chat-Parameter des Commerce Chat-Moduls](chat-proactive-chat-parameters.md)
