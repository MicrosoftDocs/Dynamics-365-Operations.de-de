---
title: Attract-Benutzer können sich nicht mit dem Karriereportal auf Stellen bewerben
description: In diesem Thema wird erläutert, wie Sie ein Problem behandeln können, wenn sich Attract-Benutzer nicht über das Karriereportal auf Stellen bewerben können.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461247"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>Attract-Benutzer können sich nicht mit dem Karriereportal auf Stellen bewerben

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Abgang

Attract-Benutzer können sich nicht mit dem Karriereportal auf Stellen bewerben. Wenn sie versuchen, sich auf eine Stelle zu bewerben, die in Dynamics 365 Talent: Attract erstellt wurde, lädt der Browser die Seite kontinuierlich und schließt die Aktivität nicht ab.

## <a name="cause"></a>Ursache

Dieses Problem tritt auf, wenn das Talent Relationship Team nicht über die Talent-Benutzerrolle verfügt.

## <a name="resolution"></a>Lösung

Weisen Sie dem Talent Relationship Team die Talent-Benutzerrolle zu.

1. Melden Sie sich im [Power Platform Admin Center](https://admin.powerplatform.microsoft.com) mit einem der folgenden Administratoranmeldeinformationen an:

   - Dynamics 365-Administrator
   - Globaler Administrator
   - Power Platform-Administrator

2. Wählen Sie im Navigationsbereich **Umgebungen** und dann die Umgebung aus, in der die Talent-Benutzerrolle dem Talent Relationship Team zugewiesen werden soll.

   ![Umgebung auswählen](./media/attract-troubleshoot-career-portal-select-environment.png)

3. Wählen Sie im Bereich **Umgebungen** die **Umgebungs-URL** aus und melden Sie sich beim Admininistratorportal der Umgebung an (z. B. https:<orgname>.crm.dynamics.com).

4. Wählen Sie **Einstellungen**, **System** und dann **Sicherheit**.

   ![Zu Sicherheit navigieren](./media/attract-troubleshoot-career-portal-security.png)

5. Wählen Sie **Teams** aus.

   ![Teams auswählen](./media/attract-troubleshoot-career-portal-security-teams.png)

6. Suchen Sie im Suchfeld nach dem **Talent Relationship Team** und wählen Sie dann aus den Suchergebnissen das Team aus.

7. Wählen Sie im Menüband **ROLLEN VERWALTEN** aus.

8. Wählen Sie im Dialogfeld **Teamrollen verwalten** und dann **Talent-Benutzer** aus der Liste der verfügbaren Rollen aus. Übernehmen Sie die Rolle dann mit **OK**.

   ![Rolle übernehmen](./media/attract-troubleshoot-career-portal-apply-role.png)

9. Testen Sie Ihre Änderungen:

   1. Melden Sie sich über ein neues Browserfenster im Karriereportal an.
   2. Bewerben Sie sich über das Karriereportal auf die Stelle. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]