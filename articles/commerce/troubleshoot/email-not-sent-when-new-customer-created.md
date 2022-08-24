---
title: Willkommens-E-Mail wird nicht gesendet, wenn neue Kunden erstellt werden
description: Dieser Artikel enthält Hinweise zur Problembehandlung, die Ihnen helfen können, wenn beim Erstellen eines neuen Kunden in Microsoft Dynamics 365 Commerce keine Begrüßungs-E-Mail gesendet wird.
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219403"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>Willkommens-E-Mail wird nicht gesendet, wenn neue Kunden erstellt werden

[!include [banner](../../includes/banner.md)]

Dieser Artikel enthält Hinweise zur Problembehandlung, die Ihnen helfen können, wenn beim Erstellen eines neuen Kunden in Microsoft Dynamics 365 Commerce keine Begrüßungs-E-Mail gesendet wird.

## <a name="description"></a>Description

Wenn ein neuer Kunde in der Commerce-Zentrale erstellt wird, wird keine Willkommens-E-Mail an den Kunden gesendet, obwohl eine E-Mail-Benachrichtigung für den E-Mail-Benachrichtigungstyp **Kunde erstellt** konfiguriert ist.

## <a name="resolution"></a>Lösung

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>Ein E-Mail-Benachrichtigungsprofil unter Handelsparameter zuordnen

1. Gehen Sie zu in Headquarters zu **Einzelhandel und Handel \> Headquarter-Einstellungen \> Parameter \> Handelsparameter \> Allgemein**.
2. Wählen Sie in der Dropdownliste **E-Mail-Benachrichtigungsprofil** das E-Mail-Benachrichtigungsprofil aus, das eine Zuordnung zwischen dem vom Kunden erstellten Benachrichtigungstyp und einer vom Kunden erstellen E-Mail-Vorlage enthält.  

> [!NOTE] 
> Wenn Sie von Kunden erstellte Benachrichtigungen aktivieren, erhalten Kunden, die in allen Kanälen innerhalb der juristischen Person erstellt wurden, eine vom Kunden erstellte E-Mail. Derzeit können von Kunden erstellte Benachrichtigungen nicht auf einen einzelnen Kanal beschränkt werden.

Weitere Informationen finden Sie unter [E-Mail-Vorlagen für Transaktionsereignisse erstellen](../email-templates-transactions.md). 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[E-Mail-Benachrichtigungsprofil einrichten](../email-notification-profiles.md)
