---
title: Leere Liste der steuerlichen Funktionen in den Steuerberechnungsparametern
description: In diesem Thema wird erklärt, wie Sie ein Problem beheben, bei dem die Liste der Funktionen auf der Seite Steuerberechnungsparameter leer ist.
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: ef8158c2ada18e7d132eebbedef559b3f80ab19f
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612288"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>Leere Liste der steuerlichen Funktionen in den Steuerberechnungsparametern

[!include [banner](../includes/banner.md)]


## <a name="symptom"></a>Symptom

Sie haben eine Funktion in Regulatory Configuration Service (RCS) veröffentlicht, sodass Sie sie in Microsoft Dynamics 365 Finance verwenden können. Wenn Sie jedoch Finance öffnen, zu **Steuern** \> **Einrichtung** \> **Steuerkonfiguration** \> **Steuerberechnungsparameter** gehen und versuchen, einen Wert im Feld **Name der Einrichtung** auszuwählen, ist die Liste der Werte leer.

## <a name="reason"></a>Ursache

Dieses Problem tritt in der Regel auf, weil Ihre Finance Umgebung und Ihre RCS Umgebung nicht unter demselben Mandant stehen.

### <a name="rcs-tenant"></a>RCS-Mandant

Führen Sie diese Schritte aus, um die ID Ihres RCS-Mandanten zu ermitteln.

1. Kopieren Sie die vollständige RCS-URL. Zum Beispiel könnte die URL `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace` lauten.
2. Öffnen Sie ein InPrivate-Browserfenster, fügen Sie die RCS-URL in die Adressleiste ein und wählen Sie **Eingabe**. Sie werden auf die Anmeldeseite weitergeleitet, auf der Sie die RCS-Mandanten-ID finden können. Wenn die URL der Anmeldeseite zum Beispiel `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d` lautet, ist die Mandant-ID die Information, die nach `https://login.microsoftonline.com/` erscheint, oder **d335a570-a05b-4bc5-8eb3-c42c65f9560d**.

### <a name="finance-environment-tenant-id"></a>Finance Umgebung Mandant ID

Um die Mandant-ID für Ihre Finance Umgebung zu finden, befolgen Sie die gleichen Schritte, die Sie für die Suche nach dem RCS-Mandanten durchgeführt haben. Kopieren Sie jedoch die vollständige URL Ihrer Finance Umgebung und fügen Sie diese anstelle der vollständigen RCS URL ein.

## <a name="resolution"></a>Lösung

Wenn sich die beiden Mandanten-IDs unterscheiden, tritt das in diesem Thema beschriebene Problem auf. Wenn sie übereinstimmen, liegt ein anderes Problem vor. In diesem Fall empfehlen wir Ihnen, sich an den Microsoft Support zu wenden.

### <a name="solution-1"></a>Lösung 1

Melden Sie Ihre RCS Umgebung bei demselben Mandanten an, bei dem auch Ihre Finance Umgebung angemeldet ist. Dann erstellen und veröffentlichen Sie die steuerliche Funktion.

### <a name="solution-2"></a>Lösung 2

Teilen Sie die Funktion Steuern mit dem Mandant Finance in RCS.

1. Gehen Sie in RCS zu **Globalisierungsfunktionen** \> **Steuerberechnung**.
2. Wählen Sie die Funktion, die Sie freigeben möchten, und wählen Sie dann auf der Registerkarte **Organisationen** die Option **Freigeben mit**.
3. Geben Sie in das Feld **Name der Domäne der Organisation** einen Namen ein. Geben Sie zum Beispiel **contoso.onmicrosoft.com** ein.
4. Wählen Sie **Teilen**.

![Dropdown-Dialogfeld Mit externer Organisation teilen.](media/ShareTaxFeature.png)
