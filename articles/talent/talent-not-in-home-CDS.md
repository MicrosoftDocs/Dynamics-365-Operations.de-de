---
title: Talent wird nicht unter den Microsoft Dynamics 365-Apps (CDS1.0) angezeigt
description: "In diesem Thema wird erklärt, was zu tun ist, wenn der Kunde die Microsoft Dynamics 365 for Talent-App nicht unter den Microsoft Dynamics 365-Apps sieht."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: de-de
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a>Talent wird nicht unter den Microsoft Dynamics 365-Apps (CDS1.0) angezeigt

[!include [banner](includes/banner.md)]

**Abgang**

Der Kunde sieht nicht die Microsoft Dynamics 365 for Talent-App unter den Microsoft Dynamics 365-Apps.

**Auflösung**

Der Benutzer muss der Umgebungsersteller-Rolle für die Umgebung in Microsoft PowerApps hinzugefügt werden.

1. Der Administratorbenutzer, der eine PowerApps Plan 2-Lizenz hat, muss das [PowerApps-Administratorportal](https://preview.admin.powerapps.com/) öffnen.
2. Wählen Sie **Umgebungen** aus, und wählen Sie die richtige Umgebung für Talent aus.
3. Wählen Sie auf der Registerkarte **Sicherheit** auf der Registerkarte **Umgebungsrollen** die Option **Umgebungsersteller** aus.

    ![Registerkarte „Umgebungsrollen”](media/environment-roles.png)

4. Fügen Sie auf der Registerkarte **Benutzer** den Benutzer oder Ihre Organisation hinzu.

    ![Registerkarte „Benutzer”](media/environment-maker.png)

5. Wählen Sie **Speichern**.
6. Der Benutzer muss sich jetzt bei [Microsoft Dynamics 365](https://home.dynamics.com/) anmelden.
7. Wählen Sie **Synchronisieren** aus, m die Benutzer-Apps zu aktualisieren.

    ![Schaltfläche „Synchronisieren”](media/get-more.png)

    Nachdem die Synchronisierung abgeschlossen ist, wird Talent auf der Startseite angezeigt.

