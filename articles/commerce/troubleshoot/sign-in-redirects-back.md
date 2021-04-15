---
title: Der Anmeldelink leitet zurück zu einer E-Commerce-Website
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn ein Anmeldelink zur E-Commerce-Website zurückleitet, anstatt zur Anmeldeseite zu wechseln.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ee2ac8636dad8d31719971b2cc17c8b923f07959
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801458"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>Der Anmeldelink leitet zurück zu einer E-Commerce-Website

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn ein Anmeldelink zur E-Commerce-Website zurückleitet, anstatt zur Anmeldeseite zu wechseln.

## <a name="description"></a>Beschreibung

Nach Konfiguration eines neuen Microsoft Azure Active Directory B2C (Azure AD B2C)-Mandanten im Commerce-Website-Generator, werden Benutzer, die den **Anmelde**-Link auswählen, zur Haupt-E-Commerce-Landingpage zurückgeleitet, ohne zur Anmeldeseite zu gelangen.

## <a name="resolution"></a>Lösung

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>Sicherstellen, dass die Antwort-URL in der Azure AD B2C-Anwendung korrekt konfiguriert ist

Befolgen Sie diese Schritte, um sicherzustellen, dass die Antwort-URL in der Azure AD B2C-Anwendung korrekt konfiguriert ist.

1. Gehen Sie zu [Azure-Portal](https://portal.azure.com/).
1. Wählen Sie die Azure AD B2C-Anwendung aus, die Sie für Ihren Website-Zugriff erstellt haben.
1. Wählen Sie die Anwendung aus, die Sie während der Einrichtung von Azure AD B2C erstellt haben.
1. Vergewissern Sie sich, dass die unter **Antwort-URL** befindliche Liste Einträge sowohl für die Website-Domänen-URL als auch für die von E-Commerce generierte URL enthält, wie im Beispiel in der folgenden Abbildung gezeigt.

    ![Azure AD B2C – Antwort-URL-Einträge](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> Sowohl die URL der Website-Domäne als auch die von E-Commerce generierte URL müssen in einem gültigen URL-Format vorliegen, das keine führenden oder nachfolgenden Schrägstriche enthält.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Registrieren einer Webanwendung in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[B2C-Mandanten in Commerce einrichten](../set-up-b2c-tenant.md)
