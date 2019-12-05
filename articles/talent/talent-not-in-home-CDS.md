---
title: Talent wird nicht in den Microsoft Dynamics 365-Anwendungen angezeigt (Common Data Service 1.0)
description: In diesem Thema wird erklärt, was zu tun ist, wenn der Kunde die Microsoft Dynamics 365 Talent-App nicht unter den Microsoft Dynamics 365-Apps sieht.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7f0cc1c7ec1234b7eedaade0ffadb66965ed2121
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772987"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Talent wird nicht in den Microsoft Dynamics 365-Anwendungen angezeigt (Common Data Service 1.0)

[!include [banner](includes/banner.md)]

**Abgang**

Der Debitor wird nicht der Zeit-App Microsoft unter Dynamics 365 Talent Apps Microsoft Dynamics 365.

**Auflösung**

Der Benutzer muss der Umgebungsersteller-Rolle für die Umgebung in Microsoft Power Apps hinzugefügt werden.

1. Der Administratorbenutzer, der eine Power Apps Plan 2-Lizenz hat, muss das [Power Apps-Administratorportal](https://preview.admin.powerapps.com/) öffnen.
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
