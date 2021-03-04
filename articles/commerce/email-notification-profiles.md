---
title: Ein E-Mail-Benachrichtigungsprofil einrichten
description: In diesem Thema wird beschrieben, wie Sie ein E-Mail-Benachrichtigungsprofil in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
manager: annbe
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c0ab56c15a37313d0a88b1174d5bcf51d391dcec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412478"
---
# <a name="set-up-an-email-notification-profile"></a>Ein E-Mail-Benachrichtigungsprofil einrichten


[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie ein E-Mail-Benachrichtigungsprofil in Microsoft Dynamics 365 Commerce erstellen.

## <a name="overview"></a>Übersicht

Bevor Sie Kanäle erstellen, sollten Sie ein Profil einrichten, um sicherzustellen, dass E-Mail-Benachrichtigungen für verschiedene Ereignisse gesendet werden können, z. B. Auftragserstellung, Auftragsversandstatus und Zahlungsfehler.

Weitere Informationen über die Konfiguration von E-Mails finden Sie unter [E-Mail konfigurieren und senden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>Ein E-Mail-Benachrichtigungsprofil erstellen

Gehen Sie folgendermaßen vor, um ein E-Mail-Benachrichtigungsprofil zu erstellen.

1. Gehen Sie im Navigationsbereich zu **Module \> Retail and Commerce \> Headquarters-Einrichtung \> Commerce-E-Mail-Benachrichtigungsprofil**.
1. Klicken Sie im Aktivitätsbereich auf **Neu**.
1. Geben Sie im Feld **E-Mail-Benachrichtigungsprofil** einen Namen ein, um das Profil zu identifizieren.
1. Geben Sie im Feld **Beschreibung** eine entsprechende Beschreibung ein.
1. Stellen Sie den Hebel **Aktiv** auf **Ja**.

### <a name="create-an-email-template"></a>E-Mail-Vorlage erstellen

Bevor eine E-Mail-Benachrichtigung erstellt werden kann, müssen Sie eine Organisations-E-Mail-Vorlage erstellen, die die E-Mail-Informationen des Absenders und die E-Mail-Vorlage enthält.

Führen Sie folgende Schritte aus, um eine E-Mail-Vorlage zu erstellen:

1. Gehen Sie im Navigationsbereich zu **Module \> Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Organisations-E-Mail-Vorlagen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **E-Mail-Kennung** eine Kennung ein, um diese Vorlage zu identifizieren.
1. Geben Sie im Feld **Absendername** den Namen des Absenders ein.
1. Geben Sie im Feld **E-Mail-Beschreibung** eine aussagekräftige Beschreibung ein.
1. Geben Sie im Feld **E-Mail des Absenders** die E-Mail-Adresse des Absenders ein.
1. Füllen Sie im Abschnitt **Allgemeines** die optionalen Informationen aus, die Sie benötigen (z. B. die E-Mail-Priorität).
1. Erweitern Sie die Abschnitt **Inhalt der E-Mail-Nachricht** und wählen Sie **Neu**, um den Vorlageninhalt zu erstellen. Wählen Sie für jedes Inhaltselement die Sprache aus und geben Sie den Betreff der E-Mail an. Wenn die E-Mail einen Textkörper haben soll, stellen Sie sicher, dass das Kästchen **Hat Text** markiert ist.
1. Wählen Sie im Aktionsbereich **E-Mail-Nachricht**, um eine E-Mail-Textvorlage bereitzustellen.

Das folgende Bild zeigt einige Beispieleinstellungen für E-Mail-Vorlagen.

![E-Mail-Vorlageneinstellungen](media/email-template.png)

### <a name="create-an-email-event"></a>E-Mail-Ereignis erstellen

Führen Sie folgende Schritte aus, um eine E-Mail-Ereignis zu erstellen:

1. Gehen Sie im Navigationsbereich zu **Module \> Retail and Commerce \> Headquarters-Einrichtung \> Commerce-E-Mail-Benachrichtigungsprofil**.
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. 
1. Wählen Sie die E-Mail-Vorlage aus der Dropdownliste **E-Mail-Kennung**.
1. Wählen Sie aus der Dropdownliste den entsprechenden **E-Mail-Kennungstyp**.
1. Aktivieren Sie das Kontrollkästchen **Aktiv**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Das folgende Bild zeigt einige Beispiele für die Einstellungen der Ereignisbenachrichtigung.

![Einstellungen für die Ereignisbenachrichtigung](media/email-notification-profile.png)

### <a name="next-steps"></a>Nächste Schritte

Bevor Sie E-Mails senden können, müssen Sie Ihren Postausgangsdienst konfigurieren und einen Batchauftrag einrichten. Weitere Informationen finden Sie unter [E-Mail konfigurieren und senden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).


## <a name="additional-resources"></a>Zusätzliche Ressourcen

[E-Mails konfigurieren und senden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Kanäle – Übersicht](channels-overview.md)

[Kanaleinstellungen – Voraussetzungen](channels-prerequisites.md)

[Organisationen und Organisationshierarchien – Übersicht](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]