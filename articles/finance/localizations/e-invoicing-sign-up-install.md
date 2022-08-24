---
title: Melden Sie sich für den Dienst für die elektronische Rechnungsstellung an und installieren Sie ihn.
description: Hier erfahren Sie, wie Sie sich für den Dienst für die elektronische Rechnungsstellung anmelden und ihn installieren.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 99f484e5ab8821c78fde776a9d3195dade2a09d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283956"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Melden Sie sich für den Dienst für die elektronische Rechnungsstellung an und installieren Sie ihn.

[!include [banner](../includes/banner.md)]

Hier erfahren Sie, wie Sie sich für den Dienst für die elektronische Rechnungsstellung anmelden und ihn installieren. Dieser Prozess besteht aus vier Schritten. Die Schritte 1 bis 3 sind erforderlich, Schritt 4 ist optional.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>Schritt 1: Melden Sie sich für den Regulatory Configuration Service an.

Der Regulatory Configuration Service (RCS) stellt die Konfigurations- und Designfunktionen für die Elektronische Rechnungsstellung zur Verfügung. Ressourcen wie Umgebungen und Funktionen für die Elektronische Rechnungsstellung werden in RCS erstellt, gepflegt und verwaltet. Wenn die Ressourcen fertig sind, werden sie im Dienst für die elektronische Rechnungsstellung veröffentlicht.

Weitere Informationen über RCS finden Sie unter [Regulatory Configuration Services (RCS) - Globalisierungsfunktionen](rcs-globalization-feature.md).

Um sich für RCS anzumelden, gehen Sie auf die Seite [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>Schritt 2: Installieren Sie das Add-In für Microservices in Microsoft Dynamics Lifecycle Services

Bei dem Dienst für die elektronische Rechnungsstellung handelt es sich um eine Reihe von Microservices, die in Microsoft-Rechenzentren gehostet werden. Standardmäßig haben Kunden von Dynamics 365 Finance und Dynamics 365 Supply Chain Management keinen Zugriff auf den Dienst für die elektronische Rechnungsstellung. Sie müssen es als Add-In in den Microsoft Dynamics Lifecycle Services (LCS) installieren. Wenn Sie das Add-In installieren, wird Ihre Finance- oder Supply Chain Management-Umgebung in das Register der Anwendungen aufgenommen, die eine Verbindung zum Dienst für die elektronische Rechnungsstellung zulassen.

Um diesen Schritt abzuschließen, siehe [Installieren Sie das Add-In für Microservices in Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>Schritt 3: RCS festlegen

Sie müssen die Integration zwischen RCS und dem Dienst für die elektronische Rechnungsstellung festlegen. Sie müssen auch die Hauptkomponenten festlegen.

Um diesen Schritt abzuschließen, lesen Sie bitte [Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md) einrichten.

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>Schritt 4: Microsoft Power Platform Plug-in Admin-Referenz

Einige Szenarien erfordern die Integration mit Dataverse im Rahmen von Microsoft Power Platform.

Diese Einrichtung ist derzeit obligatorisch, wenn Sie Lösungen zur Elektronischen Rechnungsstellung für indonesische Szenarien der elektronischen Rechnungsstellung verwenden. Für saudi-arabische Szenarien der Elektronischen Rechnungsstellung ist es jedoch optional. Weitere Informationen finden Sie unter [Verfügbarkeit der Funktionen für die Elektronische Rechnungsstellung nach Land oder Region](e-invoicing-country-specific-availability.md).

Um diesen Schritt auszuführen, siehe [Microsoft Power Platform Plug-in Admin-Referenz](e-invoicing-power-platform-plug-in.md).
