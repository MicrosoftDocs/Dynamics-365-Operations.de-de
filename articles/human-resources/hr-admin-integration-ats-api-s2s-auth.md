---
title: Server-zu-Server-Authentifizierung für das API zur ATS-Integration
description: In diesem Artikel wird beschrieben, wie Sie die Server-zu-Server-Authentifizierung für Integrationen mit der API zur Integration des Dynamics 365 Human Resources Applicant Tracking System (ATS) einrichten.
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: de3dc29c5366996276c02576eba27f7e831e4ccf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879365"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>Server-zu-Server-Authentifizierung für das API zur ATS-Integration


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird beschrieben, wie Sie die Server-zu-Server-Authentifizierung für Anwendungsintegrationen mit der API zur Integration des Dynamics 365 Human Resources Applicant Tracking System (ATS) einrichten. Es gibt einige Sicherheitsebenen, die verwaltet werden müssen, damit der Dienstprinzipal Zugriff auf die virtuelle Microsoft Dataverse- Tabelle und die zugehörigen Daten hat. Dem Benutzer muss Zugriff auf die virtuelle Dataverse-Tabelle in Microsoft Power Platform auf die Daten in Dynamics 365 Human Resources erteilt werden.

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>Zugriff auf virtuelle Dataverse-Tabellen in Power Platform aktivieren

Der erste Schritt zur Aktivierung des Zugriffs auf die virtuelle Dataverse-Tabellen Power Platform ist die Einrichtung Ihrer Anwendung in Power Platform zur Authentifizierung für Endpunkte virtueller Dataverse-Tabellen. Die Schritte dazu finden Sie im [Microsoft Dataverse-Entwicklerhandbuch](/powerapps/developer/data-platform).

  - Für App-Registrierungen mit einem Mandanten: [Verwenden Sie die Server-zu-Server-Authentifizierung für einen Mandanten](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - Für App-Registrierungen mit mehreren Mandanten: [Verwenden Sie die Server-zu-Server-Authentifizierung für mehrere Mandanten](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>Eine Sicherheitsrolle für ATS-Integrationen erstellen

Einer der Schritte nach dem Erstellen des Anwendungsbenutzers besteht darin, dem Benutzer eine Sicherheitsrolle zuzuweisen, die den Zugriff der Anwendung auf die Endpunkte definiert. Dies ist Schritt 7 in [Anwendungsbenutzererstellung](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation) für App-Registrierungen mit einem Mandanten und [Eine Sicherheitsrolle für den Anwendungsbenutzer erstellen](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user) für Registrierungen mit mehreren Mandanten. 

Die Rolle, der Sie den Anwendungsbenutzer zuweisen, sollte Zugriff auf die Datenentitäten haben, die für Ihre ATS-Integration verwendet werden. Dies ist nicht standardmäßig vorhanden, daher muss eine neue Sicherheitsrolle erstellt werden. Die neue Rolle kann mit den Schritten in [Eine Sicherheitsrolle erstellen](/power-platform/admin/create-edit-security-role#create-a-security-role) erstellt werden.

Für die neue Rolle muss mindestens folgenden Entitäten auf der Registerkarte **Benutzerdefinierte Entitäten** Registerkarte der neuen Rolle angemessener Zugriff zugewiesen werden. Beachten Sie, dass Sie möglicherweise zusätzliche Entitäten hinzufügen müssen, wenn die Integration umfangreichere Anwendungsdaten verwendet. Nachdem die neue Rolle erstellt wurde, kann sie dem Anwendungsbenutzer zugewiesen werden.

  - Basisarbeitskraft (mshr)
  - Einzustellender Kandidat (mshr)
  - Kompetenz – Bescheinigung (mshr)
  - Art der Bescheinigung (mshr)
  - Firma
  - Vergütung (Stellenfunktion) (mshr)
  - Art der Vergütung (mshr)
  - Land/Regionen (mshr)
  - Abteilung (mshr)
  - Kompetenz – Ausbildung (mshr)
  - Abschluss – Ausbildung (mshr)
  - Ausbildungsfächer (mshr)
  - Ausbildungsanforderungen (mshr)
  - Ausweis (mshr)
  - Ausweistyp (mshr)
  - Institution (mshr)
  - Ausstellende Behörde (mshr)
  - Stellenvergütung (mshr)
  - Stellen (mshr)
  - Bildungsgrad (mshr)
  - Parteikontakte (mshr)
  - Personal (mshr)
  - Adresse für Person (mshr)
  - Prüfung der Person (mshr)
  - Positionstyp (mshr)
  - Positionen V2 (mshr)
  - Kompetenz – Berufserfahrung (mshr)
  - Bewertungsebene (mshr)
  - Bewertungsmodelle (mshr)
  - Ursachencodes (mshr)
  - Personalbeschaffungsantrag (mshr)
  - Personalbeschaffungsantrag –Standort (mshr)
  - Personalbeschaffungsantrag –Position (mshr)
  - Personalbeschaffungsantrag – Qualifikationen (mshr)
  - Prüfungstyp (mshr)
  - Kompetenz – Qualifikation (mshr)
  - Qualifikationen (mshr)
  - Titel (mshr)
  - Veteranenstatus (mshr)
  - Arbeitskraft (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>Anwendungsberechtigungen für Human Resources-Daten erteilen

Der zweite Schritt besteht darin, sicherzustellen, dass der Anwendung die entsprechenden Berechtigungen für die Daten in Human Resources erteilt werden, indem sie mit einem Benutzer in der Human Resources-Anwendung verknüpft wird. Für einen Anwendungsbenutzer erfolgen die Server-zu-Server-Aufrufe durch virtuelle Dataverse-Tabellen im Kontext der Identität des Benutzers (App) in Dataverse, das die Aktivität auslöst. Der Adapterservice für virtuelle Tabellen sucht dann den zugeordneten Benutzer in Human Resources und führt die Abfrage im Kontext dieses Benutzers aus. Dies bedeutet, dass in Human Resources ein Benutzer mit den richtigen Rollen angelegt werden muss, um Zugriff auf die Daten zu bereitzustellen, die die integrierende Anwendung benötigen wird.

Dem Benutzer von Human Resources müssen außerdem die richtigen Berechtigungen für die Daten in Human Resources zugewiesen werden. Die **Personalbeschaffungsanwendung** (HcmRecruitingIntegrator) steht mit Berechtigungen für die primären Entitäten zur Verfügung, die für die Integration mit Rekrutierungsdaten erforderlich sind. Diese Rolle kann dem Anwendungsbenutzer auf der Seite **Benutzer** zugewiesen werden, um einen entsprechenden Zugriff auf die Daten zu gewähren. Weitere Informationen zu Sicherheitsrollen in Human Resources finden Sie unter [Rollenbasierte Sicherheit](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>Den neuen Benutzer mit den entsprechenden Berechtigungen einrichten

Um den neuen Benutzer mit den entsprechenden Berechtigungen einzurichten, gehen Sie wie folgt vor:

  1. Öffnen Sie in Human Resources die Seite **Benutzer** und wählen Sie **Neu** aus.
  2. Geben Sie eine **Benutzer-ID** und einen **Benutzernamen** für den neuen Anwendungsbenutzer ein. Sie können beispielsweise „RecruitingIntegration“ eingeben.

      > [!NOTE]
      > Wenn die App kein Microsoft Azure Active Directory-Benutzerkonto (Azure AD) oder keine E-Mail-Adresse hat, können Sie in die Felder „E-Mail-Adresse“ und „Anbieter“ für den Benutzer etwas wie „RecruitingApp“ eingeben.

  3. Wählen Sie auf der Registerkarte **Rollen des Benutzers** die Aktivität **Rollen zuweisen** aus.
  4. Wählen Sie im Bereich **Dem Benutzer Rollen zuweisen** **Personalbeschaffungsanwendung** und dann **OK** aus.
  5. Speichern Sie den neuen Benutzerdatensatz.

### <a name="link-the-new-human-resources-user-to-the-application"></a>Den neuen Human Resources-Benutzer mit der Anwendung verknüpfen

Nach dem Anlegen des Benutzers muss ein Datensatz für die Anwendung im Formular **Azure Active Directory-Anwendungen** erstellt werden, um die App mit dem Human Resources-Benutzer zu verknüpfen.

  1. Öffnen Sie das Formular **Azure Active Directory-Anwendungen** und wählen Sie dann **Neu** aus.
  2. Geben Sie im Feld **Client-ID** die Client-ID des Anwendungsbenutzers ein, der für die Anwendung erstellt wurde.
  3. Geben Sie im Feld **Name** den Namen der zu integrierenden Anwendung ein.
  4. Wählen Sie im Feld **Benutzer-ID** den neuen Human Resources-Benutzer aus, der für die Personalbeschaffungsintegration angelegt wurde.
  5. Speichern Sie den neuen Datensatz.

Die Bewerbung hat dann Zugriff auf Human Resources-Daten, beschränkt auf die Daten, die für die Integration der Personalbeschaffungsanwendung erforderlich sind.

## <a name="see-also"></a>Siehe auch

[Kandidaten für Stelle anwerben](hr-personnel-recruit.md)<br>
[Was ist Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Verwenden der Microsoft Dataverse-Web-API](/powerapps/developer/data-platform/webapi/overview)<br>
[Erstellen und Aktualisieren von Optionssätzen mithilfe der Web-API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
