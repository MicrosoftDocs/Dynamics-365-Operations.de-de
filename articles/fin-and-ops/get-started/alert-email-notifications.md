---
title: Clientwarnbenachrichtigungen per E-Mail
description: Dieses Thema enthält Informationen zur Einrichtung von Regeln, die bei vordefinierten Ereignisse E-Mail-Benachrichtigungen senden.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 9545731af20a96c322b4e92c17f3a46b7077295b
ms.sourcegitcommit: a13f44549ab402cfd04b600f6097ba179915f233
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "775063"
---
# <a name="client-alert-notifications-by-email"></a>Clientwarnbenachrichtigungen per E-Mail

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In Microsoft Dynamics 365 for Finance and Operations können Sie benutzerdefinierte Warnregeln definieren, die gefilterte Datenansichten überwachen und automatisch E-Mail-Benachrichtigungen senden, wenn vordefinierte Ereignisse auftreten. Die Option zum Senden von Benachrichtigungen steht für alle unterstützten Warntypen zur Verfügung und kann auch für vorhandene Warnregeln aktiviert werden.

Sie können integrierte Kontrollen verwenden, um Warnregeln zu erstellen, die die gefilterten Ansichten von Systembatchaufträgen überwachen. Durch die Überwachung des Werts des Felds **Status** können Sie auch Warnregeln konfigurieren, die E-Mails senden, wenn ein Batchauftrag fehlschlägt. Nachdem diese Warnregeln erstellt wurden, müssen Sie die Berichte nicht mehr auf Änderungen an Geschäftsdaten überprüfen. Stattdessen kann der intelligente Änderungserkennungsdienst von Finance and Operations die Überwachung für Sie übernehmen.

Clientwarnungen hängen vom E-Mail-Subsystem ab, das durch die Integration in Microsoft Office bereitgestellt wird. Es wird empfohlen, den Simple Mail Transfer Protocol (SMTP)-Anbieter zu verwenden, sodass die E-Mail-Verteilung nicht von einem lokalen Mailclient abhängt.

Um Benachrichtigungen per E-Mail zu senden, müssen Kunden integrierte E-Mail-Services konfigurieren. E-Mail-Benachrichtigungen werden an Empfänger im Auftrag der Warnungseigentümer gesendet.

Weitere Informationen über die Konfiguration von E-Mails in Finance and Operations finden Sie unter [E-Mail konfigurieren und senden](../organization-administration/configure-email.md).

Das folgende Bild zeigt das Dialogfeld **Warnregel erstellen**, das jetzt die Option **E-Mail senden** enthält.

[![Erstellen Sie ein Warnregeldialogfeld, bei dem die Option "E-Mail senden" auf "Ja" festgelegt ist](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Wenn die Option **E-Mail senden** auf **Ja** festgelegt wurde, werden weiter Warnbenachrichtigungen vom Aktivitätszentrum übermittelt.

## <a name="alert-notification-email-templates"></a>E-Mail-Vorlagen für Warnbenachrichtigungen

Der Dienst sendet E-Mail-Benachrichtigungen, indem er vordefinierte E-Mail-Vorlagen verwendet, die die grundlegenden Details der Warnbenachrichtigung enthalten.

Das folgende Bild zeigt die Warnbenachrichtigungen, wenn sie per E-Mail eingehen.

[![Auf Vorlagen basierende Warnbenachrichtigungen für Datensatzerstellungen, Feldänderungen und Vorlagenlöschvorgänge](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)
