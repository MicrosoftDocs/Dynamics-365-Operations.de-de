---
title: Willkommens-E-Mail wird nicht gesendet, wenn neue Kunden erstellt werden
description: Dieser Artikel enthält Hinweise zur Problembehandlung, die Ihnen helfen können, wenn beim Erstellen eines neuen Kunden in Microsoft Dynamics 365 Commerce keine Begrüßungs-E-Mail gesendet wird.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 8e95b33d4b8a9af13c613ab89dd33de6b4934694
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853682"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Willkommens-E-Mail wird nicht gesendet, wenn neue Kunden erstellt werden

[!include [banner](../../includes/banner.md)]

Dieser Artikel enthält Hinweise zur Problembehandlung, die Ihnen helfen können, wenn beim Erstellen eines neuen Kunden in Microsoft Dynamics 365 Commerce keine Begrüßungs-E-Mail gesendet wird.

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
