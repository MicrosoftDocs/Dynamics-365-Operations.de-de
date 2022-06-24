---
title: Human Resources wird nicht in Microsoft Dynamics 365-Apps angezeigt
description: Dieser Artikel erklärt, was zu tun ist, wenn Microsoft Dynamics 365 Human Resources nicht unter den Microsoft Dynamics 365-Apps aufgeführt ist.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d520ac06bcc0990714929c0fdd622516eda5f30
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872238"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Die Human Resources App erscheint nicht unter den Microsoft Dynamics 365 Apps


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Problem**

Der Kunde sieht Dynamics 365 Human Resources nicht bei den Microsoft Dynamics 365-Apps.

**Lösung**

Der Benutzer muss der Umgebungsersteller-Rolle für die Umgebung in Microsoft Power Apps hinzugefügt werden.

1. Der Administratorbenutzer, der eine Power Apps Plan 2-Lizenz hat, muss das [Power Apps-Administratorportal](https://preview.admin.powerapps.com/) öffnen.

2. Wählen Sie **Umgebungen** aus, und wählen Sie die richtige Umgebung für Human Resources aus.

3. Wählen Sie auf der Registerkarte **Sicherheit** auf der Registerkarte **Umgebungsrollen** die Option **Umgebungsersteller** aus.

    ![Registerkarte „Umgebungsrollen“.](media/environment-roles.png)

4. Fügen Sie auf der Registerkarte **Benutzer** den Benutzer oder Ihre Organisation hinzu.

    ![Registerkarte „Benutzer“.](media/environment-maker.png)

5. Wählen Sie **Speichern** aus.

6. Der Benutzer muss sich jetzt bei [Microsoft Dynamics 365](https://home.dynamics.com/) anmelden.

7. Wählen Sie **Synchronisieren** aus, m die Benutzer-Apps zu aktualisieren.

    ![Schaltfläche „Synchronisieren“.](media/get-more.png)

    Nachdem die Synchronisierung abgeschlossen ist, wird Human Resources auf der Startseite angezeigt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
