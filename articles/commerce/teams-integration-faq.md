---
title: Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ
description: Dieses Thema enthält Antworten auf häufig gestellte Fragen zur Integration von Microsoft Dynamics 365 Commerce und Microsoft Teams.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3fc7cff0a3f8d0fbfb196ec5951b138088afece7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019469"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ

[!include [banner](includes/banner.md)]

Dieses Thema enthält Antworten auf häufig gestellte Fragen zur Integration von Microsoft Dynamics 365 Commerce und Microsoft Teams.

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>Wer im Shop wird Besitzer eines Teams, wenn Teams aus Commerce bereitgestellt werden? 

Alle Filialleiter werden automatisch als Besitzer zur entsprechenden Teamgruppe hinzugefügt, damit sie Vorgänge wie das Hinzufügen eines privaten Kanals und das Hinzufügen oder Löschen von Mitgliedern ausführen können. 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>Wie ordne ich einem Mitarbeiter in der Commerce-Zentralverwaltung die Rolle „Kommunikationsmanager“ zu? 

Kommunikationsmanager können in Microsoft Teams Aufgabenlisten erstellen und veröffentlichen. Organisationsmitarbeiter, die Kommunikationsmanager werden müssen, muss die Rolle des „Retail Task Managers“ in der Commerce-Zentralverwaltung zugewiesen werden.

Führen Sie die folgenden Schritte aus, um einem Mitarbeiter in der Commerce-Zentralverwaltung die Rolle des Retails Task Managers zuzuweisen.

1. Gehen Sie zu **Retail and Commerce \> Mitarbeiter \> Benutzer**.
1. Wählen Sie einen Mitarbeiter aus.
1. Wählen Sie auf der Registerkarte **Rollen des Benutzers** **Rollen zuweisen**.
1. Wählen Sie im Dialogfenster **Rollen zu Benutzer** die Rolle **Retail Task Manager** und dann **OK**.

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>Wie stelle ich eine bestimmte Organisationshierarchie zum Hochladen in Microsoft Teams zur Verfügung?

In der Commerce-Zentralverwaltung ist die Hierarchie jeder Organisation einem oder mehreren Zwecken zugeordnet. Stellen Sie sicher, dass der Hierarchie, die Sie in Microsoft Teams bereitstellen möchten, der Zweck **Einzelhandelsberichterstellung** wie im folgenden Beispielbild gezeigt zugeordnet ist. 

![Beispiel für einen Organisationshierarchiezweck in der Commerce-Zentralverwaltung](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>Wie kann ich Mitarbeitern von Einzelhandelsgeschäften ermöglichen, sich bei Commerce Point of Sale (POS) mit Azure Active Directory (Azure AD) anzumelden?

Informationen zum Konfigurieren der zu verwendenden Commerce POS-Anmeldeumgebung zur Verwendung der Azure AD-Authentifizierung finden Sie unter [Azure Active Directory-Authentifizierung bei POS-Anmeldung aktivieren](aad-pos-logon.md).

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>Wie ordne ich Shops und entsprechende Teams in der Commerce-Zentralverwaltung zu, wenn meine Organisation bereits Teams in Microsoft Teams erstellt hat?

Informationen zum Zuordnen von Shops und Teams, wenn bereits Teams vorhanden sind, finden Sie unter [Shops und entsprechende Teams zuordnen, wenn in Ihrer Organisation bereits Teams Microsoft Teams vorhanden sind](map-stores-existing-teams.md).

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>Wie lösche ich das im Sitzungsspeicher gespeicherte Microsoft Graph API-Token?

Ein Benutzer, der sich am Point of Sale (POS) mit einem Azure Active Directory (Azure AD) Konto angemeldet hat, sollte sich vom POS abmelden oder die Anwendung schließen, um den Sitzungsspeicher zu löschen. 

> [!TIP]
> Es hat sich bewährt, dass die Mitarbeiter des Shops das POS-Terminal immer sperren oder sich von einer Sitzung abmelden, wenn sie das Terminal nicht verwenden. 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>Was passiert, wenn ein Shop keinen Filialleiter hat?

Wenn ein Shop keinen Leiter hat, wird keine Teamgruppe für das Shop oder in Teams erstellt. 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>Was passiert, wenn ein Filialleiter das Unternehmen verlässt?

Jeder mit der Besitzerrolle kann einen neuen Filialleiter in der Commerce-Zentralverwaltung hinzufügen und Teams erneut bereitstellen, damit der neue Leiter über die erforderlichen Berechtigungen in Teams für die Gruppe verfügt. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick Integration Dynamics 365 Commerce und Microsoft Teams](commerce-teams-integration.md)

[Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren](enable-teams-integration.md)

[Microsoft Teams aus Dynamics 365 Commerce bereitstellen](provision-teams-from-commerce.md)

[Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren](synchronize-tasks-teams-pos.md)

[Benutzerrollen in Microsoft Teams verwalten](manage-user-roles-teams.md)

[Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind](map-stores-existing-teams.md)
