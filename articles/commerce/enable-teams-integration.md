---
title: Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren
description: In diesem Thema wird beschrieben, wie die Integration von Microsoft Dynamics 365 Commerce und Microsoft Teams aktiviert wird.
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dfada577ab97fdb9912c22d2399529f934b25d54
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695733"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie die Integration von Microsoft Dynamics 365 Commerce und Microsoft Teams aktiviert wird.

Um Teams mit Informationen aus Dynamics 365 Commerce zu versorgen und die Funktionen der Aufgabenverwaltung zwischen Teams und der Point-of-Sale-Anwendung (POS-Anwendung) zu synchronisieren, müssen Sie die Integrationsfunktionen in der Commerce-Zentralverwaltung aktivieren.

> [!NOTE]
> Wenn Sie die Teams-Integration aktivieren, stimmen Sie zu, Ihre Daten für Teams freizugeben. Daten, die mit Teams geteilt werden, befinden sich möglicherweise in einem anderen Land als Ihre Commerce-Daten und unterliegen möglicherweise anderen Compliance-Standards. Weitere Informationen dazu, finden Sie unter [Microsoft Trust Center](https://www.microsoft.com/trust-center). Informationen zu den Microsoft-Datenschutzrichtlinien finden Sie in den [Microsoft-Datenschutzbestimmungen](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Teams-Integration aktivieren

Bevor Sie die Microsoft Teams-Integration in Commerce aktivieren können, müssen Sie die Teams-Anwendung mit Ihrem Mandanten im Azure-Portal registrieren.

Führen Sie die folgenden Schritte aus, um die Teams-Anwendung mit Ihrem Mandanten im Azure-Portal zu registrieren.

1. Befolgen Sie die Schritte in [Schnellstart: Registrieren einer Anwendung bei Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app), um die Teams-Anwendung mit Ihrem Mandanten im Azure-Portal zu registrieren.
1. Wählen Sie auf der Registerkarte **App-Registrierung** die App aus, die Sie im vorherigen Schritt erstellt haben. Wählen Sie dann auf der Registerkarte **Authentifizierung** eine **Plattform hinzufügen** aus.
1. Klicken Sie im Dialogfeld auf **Web**. Geben Sie dann im Feld **Umleitungs-URLs** eine URL im Format **\<HQUrl\>/oauth** ein. Ersetzen Sie **\<HQUrl\>** mit der URL Ihrer Commerce-Zentralverwaltung (z. B. `https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`).
1. Kopieren Sie den Wert **Anwendungs-ID (Client-ID)** auf der Seite **Überblick** der registrierten App. Sie müssen diesen Wert verwenden, um die Teams-Integration in der Commerce-Zentralverwaltung im nächsten Abschnitt zu aktivieren.
1. Befolgen Sie die Anweisungen in [Geheimen Clientschlüssel hinzufügen](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret), um einen geheimen Clientschlüssel hinzuzufügen. Kopieren Sie dann den Wert **Geheimer Wert** für den Kunden. Sie müssen diesen Wert verwenden, um die Teams-Integration in der Commerce-Zentralverwaltung im nächsten Abschnitt zu aktivieren.
1. Wählen Sie **API-Berechtigungen** und dann **Eine Berechtigung hinzufügen** aus.
1. Wählen Sie im Dialogfeld **API-Berechtigungen anfordern** **Microsoft Graph** und dann **Delegierte Berechtigungen** aus, erweitern Sie **Gruppe** und wählen Sie **Group.ReadWrite.All** und dann **Berechtigungen hinzufügen** aus.
1. Wählen Sie im Dialogfeld **API-Berechtigungen** anfordern **Eine Berechtigung hinzufügen**, **Microsoft Graph** und dann **Anwendungsberechtigungen** aus, erweitern Sie **Gruppe** und wählen Sie **Group.ReadWrite.All** und dann **Berechtigungen hinzufügen** aus.
1. Wählen Sie im Dialogfeld **API-Berechtigungen anfordern** **Eine Berechtigung hinzufügen** aus. Suchen Sie auf der Registerkarte **Von meiner Organisation verwendete APIs** nach **Microsoft Teams Retail Service** und wählen Sie ihn aus.
1. Wählen Sie **Delegierte Berechtigungen** aus, erweitern Sie **TaskPublishing**, **TaskPublishing.ReadWrite.All** und dann **Berechtigungen hinzufügen** aus. Weitere Informationen finden Sie unter [Eine Clientanwendung für den Zugriff auf eine Web-API konfigurieren](/azure/active-directory/develop/quickstart-configure-app-access-web-apis).

Führen Sie die folgenden Schritte aus, um die Teams-Integration in der Commerce-Zentralverwaltung zu aktivieren.

1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellungen \> Microsoft Teams Integrationskonfiguration**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Legen Sie die Option **Microsoft Teams-Integration aktivieren** auf **Ja** fest.
1. Geben Sie im Feld **Anwendungs-ID** den Wert **Anwendungs-ID (Client)** ein, den Sie erhalten haben, als Sie die Teams-Anwendung im Azure-Portal registriert haben.
1. Geben Sie im Feld **Anwendungsschlüssel** den Wert **Geheimer Wert** ein, den Sie erhalten haben, als Sie den geheimen Clientschüssel im Azure-Portal hinzugefügt haben.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Die folgende Abbildung zeigt ein Beispiel für die Konfiguration der Teams-Integration in der Commerce-Zentralverwaltung.

![Konfiguration der Teams-Integration in der Commerce-Zentralverwaltung.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Teams-Integration deaktivieren

Führen Sie die folgenden Schritte aus, um die Microsoft Teams-Integration in der Commerce-Zentralverwaltung zu deaktivieren.

1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellungen \> Microsoft Teams Integrationskonfiguration**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
3. Legen Sie die Option **Microsoft Teams-Integration aktivieren** auf **Nein** fest.
4. Löschen Sie die Werte aus den Feldern **Anwendungs-ID** und **Anwendungsschlüssel**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

> [!NOTE]
> Nachdem Sie die Teams-Integration in Commerce deaktiviert haben, werden auf den POS-Terminals keine Aufgaben mehr angezeigt, die in der Teams-Anwendung veröffentlicht wurden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick Integration Dynamics 365 Commerce und Microsoft Teams](commerce-teams-integration.md)

[Microsoft Teams aus Dynamics 365 Commerce bereitstellen](provision-teams-from-commerce.md)

[Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren](synchronize-tasks-teams-pos.md)

[Benutzerrollen in Microsoft Teams verwalten](manage-user-roles-teams.md)

[Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind](map-stores-existing-teams.md)

[Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ](teams-integration-faq.md)
