---
title: Human Resources wird nicht in Microsoft Dynamics 365-Apps angezeigt
description: In diesem Artikel wird erklärt, was zu tun ist, wenn der Kunde die Microsoft Dynamics 365 Human Resources-App nicht unter den Microsoft Dynamics 365-Apps sieht.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 658c6a4f17c022c3d0e3e49d16eb89624c4be27c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803968"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources wird nicht in Microsoft Dynamics 365-Apps angezeigt

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Abgang**

Der Kunde sieht Dynamics 365 Human Resources nicht bei den Microsoft Dynamics 365-Apps.

**Lösung**

Der Benutzer muss der Umgebungsersteller-Rolle für die Umgebung in Microsoft Power Apps hinzugefügt werden.

1. Der Administratorbenutzer, der eine Power Apps Plan 2-Lizenz hat, muss das [Power Apps-Administratorportal](https://preview.admin.powerapps.com/) öffnen.

2. Wählen Sie **Umgebungen** aus, und wählen Sie die richtige Umgebung für Human Resources aus.

3. Wählen Sie auf der Registerkarte **Sicherheit** auf der Registerkarte **Umgebungsrollen** die Option **Umgebungsersteller** aus.

    ![Registerkarte „Umgebungsrollen”](media/environment-roles.png)

4. Fügen Sie auf der Registerkarte **Benutzer** den Benutzer oder Ihre Organisation hinzu.

    ![Registerkarte „Benutzer”](media/environment-maker.png)

5. Wählen Sie **Speichern**.

6. Der Benutzer muss sich jetzt bei [Microsoft Dynamics 365](https://home.dynamics.com/) anmelden.

7. Wählen Sie **Synchronisieren** aus, m die Benutzer-Apps zu aktualisieren.

    ![Schaltfläche „Synchronisieren”](media/get-more.png)

    Nachdem die Synchronisierung abgeschlossen ist, wird Human Resources auf der Startseite angezeigt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]