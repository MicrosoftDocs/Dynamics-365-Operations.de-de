---
title: Willkommens-E-Mail wird nicht gesendet, wenn neue Kunden erstellt werden
description: Dieses Thema enthält Hinweise zur Problembehandlung, die Ihnen helfen können, wenn beim Erstellen eines neuen Kunden in Microsoft Dynamics 365 Commerce keine Begrüßungs-E-Mail gesendet wird.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349963"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Willkommens-E-Mail wird nicht gesendet, wenn neue Kunden erstellt werden

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Hinweise zur Problembehandlung, die Ihnen helfen können, wenn beim Erstellen eines neuen Kunden in Microsoft Dynamics 365 Commerce keine Begrüßungs-E-Mail gesendet wird.

## <a name="description"></a>Description

Wenn ein neuer Kunde in der Commerce-Zentrale erstellt wird, wird keine Willkommens-E-Mail an den Kunden gesendet, obwohl eine E-Mail-Benachrichtigung für den E-Mail-Benachrichtigungstyp **Kunde erstellt** konfiguriert ist.

## <a name="resolution"></a>Lösung

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>Legen Sie den korrekten Wert der E-Mail-ID für den vom Kunden erstellten E-Mail-Benachrichtigungstyp fest

Um den korrekten **E-Mail-ID**-Wert für den E-Mail-Benachrichtigungstyp **Kunde erstellt** in der Zentrale festzulegen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Einzelhandel und Commerce \> Einrichtung des Hauptsitzes \> Commerce E-Mail-Benachrichtigungsprofil**.
1. Wählen Sie im linken Navigationsbereich das E-Mail-Benachrichtigungsprofil.
1. Legen Sie unter **Einstellungen für Einzelhandelsereignisbenachrichtigungen** für den E-Mail-Benachrichtigungstyp **Kunde erstellt** das Feld **E-Mail-ID** auf **NewCust** fest.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[E-Mail-Benachrichtigungsprofil einrichten](../email-notification-profiles.md)
