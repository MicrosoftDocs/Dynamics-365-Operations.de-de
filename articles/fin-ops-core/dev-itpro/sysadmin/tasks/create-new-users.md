---
title: Erstellen neuer Benutzer
description: Benutzer sind interne Mitarbeiter der Organisation oder externe Debitoren und Kreditoren, die Zugriff auf Microsoft Dynamics AX anfordern, ihre Einzelvorgänge auszuführen.
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 480d181e8abb3af5a7406efd13c8bd9961a7490a
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595385"
---
# <a name="create-new-users"></a>Neue Benutzer erstellen

[!include [banner](../../includes/banner.md)]

Bevor Sie auf Finance and Operations-Apps zugreifen können, müssen Sie der Seite **Benutzer** (**Systemverwaltung \> Benutzer \> Benutzer**) hinzugefügt werden. Zu den Benutzern gehören interne Mitarbeiter Ihres Unternehmens oder externe Kunden und Lieferanten. Benutzer können manuell importiert oder hinzugefügt werden. Alle Benutzer müssen für die konforme Verwendung ordnungsgemäß lizenziert sein.

Informationen zum Kauf und zur Lizenzierung für Finance and Operations-Apps siehe [Microsoft Dynamics 365-Lizenzierungshandbuch](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).

## <a name="assign-a-license-to-a-user"></a>Zuweisen einer Lizenz zu einem Benutzer
Systemadministratoren können [Benutzern Lizenzen zuordnen](/office365/admin/subscriptions-and-billing/assign-licenses-to-users) – im [Microsoft 365 Admin Center](/office365/admin/admin-overview/about-the-admin-center).

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>Einen externen Benutzer in Azure AD hinzufügen und eine Lizenz zuweisen 
Externe Benutzer müssen in Ihrem Mandantenverzeichnis vertreten sein (Azure Active Directory (Azure AD)) damit ihnen Lizenzen zugewiesen werden können. Diese externen Benutzer sollten dem Mandanten in Azure AD als Gastbenutzer hinzugefügt werden und dann sollten ihnen die entsprechenden Lizenzen zugewiesen werden. Eine Voraussetzung für Finance and Operations-Apps ist, dass die Firma des Gastbenutzers Azure AD verwenden muss. Weitere Informationen finden Sie unter [Azure Active Directory Benutzer der B2B-Zusammenarbeit im Azure-Portal hinzufügen](/azure/active-directory/b2b/add-users-administrator).

## <a name="import-new-users-from-azure-ad"></a>Neue Benutzer aus Azure AD importieren 
1. Wechseln Sie zu **Systemverwaltung** \> **Benutzer** \> **Benutzer**.
2. Wählen Sie im Aktivitätsbereich **Benutzer importieren** aus.
3. Wählen Sie die Benutzer aus, die importiert werden sollen. Die Liste enthält Azure AD-Benutzer, die derzeit keine Benutzer in dieser Umgebung sind.
4. Wählen Sie **Benutzer importieren** aus.
5. Wählen Sie **Schließen** aus.

> [!NOTE]
> Der Wert für das Feld **Unternehmen** wird basierend auf dem aktuellen Sitzungsunternehmen für den Administrator festgelegt. Nach dem Import müssen Sie gegebenenfalls Rollen und Organisationen zuweisen. Ausführlichere Informationen finden Sie unter [Zuweisen von Benutzern zu Sicherheitsrollen](assign-users-security-roles.md). Bedingt kann es auch erforderlich sein, den Benutzer mit einer **Person** zu verknüpfen und Benutzeroptionen wie Sprache zu aktualisieren.

## <a name="manually-add-a-new-user"></a>Manuelles Hinzufügen eines neuen Benutzers
1. Wechseln Sie zu **Systemverwaltung** \> **Benutzer** \> **Benutzer**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Geben Sie im Feld **Benutzerkennung** eine eindeutige Kennung für den Benutzer ein.   
4. Geben Sie im Feld **Benutzername** den Namen des Benutzers ein.  
5. Im Feld **Anbieter**:
 - Verwenden Sie für interne Benutzer den Standardwert. Zum Beispiel Ihren Azure AD-Mandanten mit dem Präfix https://sts.windows.net/.  
 - Für Nicht-Azure AD-Benutzer, z. B. Service-2-Service-Konten, geben Sie einen grundlegenden Textwert ein. Beispielsweise NA. Dieser Wert hilft, falsche Authentifizierungsaufrufe zu vermeiden, die zu Fehlern führen können, wenn ein gültiger Identitätsanbieterwert verwendet wird.  
 - Fügen Sie für externe Benutzer oder Gastbenutzer deren Azure AD-Mandantennamen nach https://sts.windows.net/ hinzu.
6. Geben Sie im Feld **E-Mail** die vollständige E-Mail-Adresse/den Benutzerprinzipalnamen des Benutzers ein.  
7. Wählen Sie im Feld **Unternehmen** das Standardstartunternehmen für den Benutzer aus. 
8. Wählen Sie **Speichern** aus.

Die Werte für Identitätsanbieter und Telemetrie-ID werden basierend auf einem [Microsoft Graph](/graph/overview)-Aufruf aktualisiert, wenn der Benutzerdatensatz gespeichert wird. Die Telemetrie-ID basiert auf der Objekt-ID/Sicherheitskennung (SID) des Benutzers in Azure AD.

> [!NOTE]
> Nachdem Sie einen Benutzer hinzugefügt haben, müssen Sie gegebenenfalls Rollen und Organisationen zuweisen. Ausführlichere Informationen finden Sie unter [Zuweisen von Benutzern zu Sicherheitsrollen](assign-users-security-roles.md). Bedingt kann es auch erforderlich sein, den Benutzer mit einer **Person** zu verknüpfen und **Benutzeroptionen** wie Sprache zu aktualisieren.

## <a name="change-a-user-id"></a>Ändern einer Benutzer-ID
Um eine Benutzer-ID zu ändern, müssen Sie den Schlüssel in der Datenbank umbenennen. Wenn Sie eine Benutzer-ID mithilfe dieses Verfahrens ändern, werden alle zugehörigen Benutzereinstellungen geändert, um die neue Benutzer-ID zu verwenden. Die Nutzungsinformationen in der Tabelle **SysLastValue** werden z. B. aktualisiert, um auf die neue Benutzer-ID zu verweisen.

> [!NOTE]
> Die Benutzer-ID ist der Primärschlüssel der Benutzerinformationstabelle. Das Umbenennen des Primärschlüssels kann für vorhandene Benutzer einige Zeit in Anspruch nehmen, da alle Verweise auf den Schlüssel auch in der Datenbank aktualisiert werden. 

1. Wechseln Sie zu **Systemverwaltung \> Benutzer \> Benutzer**.
2. Wählen Sie einen Benutzer in der Liste aus, und wählen Sie **Optionen \> Datensatzinfo**.
3. Wählen Sie **Umbenennen** aus.
4. Geben Sie einen neuen und eindeutigen Wert für die Benutzer-ID ein, und wählen Sie **OK** aus. 
5. Wählen Sie **Ja** aus, um bestätigen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Weitere Optionen zum Implementieren von B2B-Benutzern finden Sie unter [B2B-Benutzer in Azure AD exportieren](../implement-b2b.md).

Informationen zu vorkonfigurierten Systemkonten finden Sie unter [Vorkonfigurierte Systemkonten](../pre-configured-system-accounts.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]