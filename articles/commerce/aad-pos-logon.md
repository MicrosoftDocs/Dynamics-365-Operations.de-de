---
title: Aktivieren Sie die Azure Active Directory-Authentifizierung für die POS-Anmeldung
description: In diesem Thema wird erläutert, wie die Anmeldung für die Microsoft Dynamics 365 Commerce POS (Point of Sale) so konfiguriert wird, dass sie die Azure Active Directory Authentifizierung verwendet.
author: boycezhu
manager: annbe
ms.date: 03/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: dfc49585434383385b6b993893d93b95ef888384
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248939"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>Aktivieren Sie die Azure Active Directory-Authentifizierung für die POS-Anmeldung
[!include [banner](includes/banner.md)]


Viele Kunden, die Microsoft Dynamics 365 Commerce verwenden, nutzen auch andere Cloud-Dienste von Microsoft, und sie könnten Azure Active Directory (Azure AD) verwenden, um die Benutzeranmeldeinformationen für diese Dienste zu verwalten. In diesen Fällen möchten die Kunden möglicherweise anwendungsübergreifend dasselbe Azure AD-Konto verwenden. In diesem Thema wird erläutert, wie die Anmeldemöglichkeit am POS (Point of Sale) für die Verwendung der Azure AD-Authentifizierung konfiguriert wird.

## <a name="configure-azure-ad-authentication"></a>Konfigurieren der Azure AD-Authentifizierung

Um Azure AD als Authentifizierungsmethode für die POS-Anmeldung für eine Filiale verfügbar zu machen, müssen Sie die Einstellungen des Funktionsprofils der Filiale konfigurieren und diese Einstellungen dann auf POS-Clients anwenden.

Führen Sie die folgenden Schritte aus, um ein Funktionsprofil zu konfigurieren.

1. Gehen Sie zu **Retail und Commerce** \> **Kanaleinrichtung** \> **POS-Einrichtung** \> **POS-Profile** \> **Funktionsprofile**.
1. Wählen Sie das zu ändernde Funktionalitätsprofil aus.
1. Ändern Sie auf der Registerkarte **Funktionen** im Abschnitt **POS-Personalanmeldung** den Wert des Feldes **Anmeldeauthentifizierungsmethode** von **Personal-ID und Passwort** auf **Azure Active Directory**.

Standardmäßig verwenden alle Funktionsprofile **Personen-ID und Passwort** als POS-Authentifizierungsmethode. Daher müssen Sie den Wert des Feldes **Anmelde-Authentifizierungsmethode** ändern, wenn Sie Azure AD verwenden möchten. Jedes Einzelhandelsgeschäft, das mit dem ausgewählten Funktionsprofil verknüpft ist, ist von dieser Änderung betroffen.

Um die Einstellungen auf POS-Clients anzuwenden, führen Sie folgende Schritte aus.

1. Gehen Sie zu **Retail and Commerce** \> **Retail and Commerce IT** \> **Vertriebsplan**.
1. Führen Sie den Verteilungsplan **1070** (**Kanalkonfiguration**) aus.

> [!NOTE]
> Die Azure AD-Authentifizierung erfordert eine Internetverbindung. Sie funktioniert nicht, wenn sich POS im Offline-Modus befindet.

## <a name="associate-an-azure-ad-account-with-a-worker"></a>Verknüpfen eines Azure AD-Kontos mit einem Mitarbeiter

Bevor sich ein Mitarbeiter einer Filiale mit einem Azure AD-Konto bei der POS-Anwendung anmelden kann, muss das Azure AD-Konto mit diesem Mitarbeiter verknüpft sein.

Um ein Azure AD-Konto mit einem Mitarbeiter zu verknüpfen, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Retail and Commerce** \> **Mitarbeiter** \> **Arbeitskräfte**.
1. Öffnen Sie die Detailseite für einen Mitarbeiter.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Commerce** in der Gruppe **Externe Identität** die Option **Existierende Identität zuordnen**.
1. Wählen Sie im Dialogfeld **Existierende externe Identität verwenden** **Mit E-Mail** suchen, geben Sie eine E-Mail-Adresse Azure AD ein und wählen Sie dann **Suchen**.
1. Wählen Sie das Konto Azure AD, das zurückgegeben wird, und wählen Sie dann **OK**.

Die Felder **Alias**, **UPN** und **Externer Sub-Identifikator** auf der Registerkarte **Commerce** auf der Seite mit den Details des Mitarbeiters werden ausgefüllt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Erweiterte Anmeldungsfunktionen für MPOS und Cloud POS einrichten](extended-logon.md)

[Ein Einzelhandelsfunktionsprofil erstellen](retail-functionality-profile.md)

[ Eine Arbeitskraft konfigurieren](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
