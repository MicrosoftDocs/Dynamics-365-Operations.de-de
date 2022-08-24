---
title: E-Mail-Benachrichtigungsprofil einrichten
description: In diesem Artikel wird beschrieben, wie Sie ein E-Mail-Benachrichtigungsprofil in Microsoft Dynamics 365 Commerce erstellen.
author: bicyclingfool
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: db6c46d471e3b54982132df3e4819236833cf4a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292134"
---
# <a name="set-up-an-email-notification-profile"></a>E-Mail-Benachrichtigungsprofil einrichten

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie ein E-Mail-Benachrichtigungsprofil in Microsoft Dynamics 365 Commerce erstellen.

Wenn Sie Kanäle erstellen, können Sie ein E-Mail-Benachrichtigungsprofil einrichten. Das E-Mail-Benachrichtigungsprofil definiert die Ereignisse einer Transaktion (wie z.B. Auftrag erstellt, Auftrag verpackt und Auftrag fakturiert), für die Sie Benachrichtigungen an Ihre Debitor senden werden. 

Weitere Informationen über die Konfiguration von E-Mails finden Sie unter [E-Mail konfigurieren und senden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).



## <a name="create-an-email-template"></a>E-Mail-Vorlage erstellen

Bevor ein E-Mail-Benachrichtigungstyp aktiviert werden kann, müssen Sie in der Commerce-Zentrale für jeden Benachrichtigungstyp, den Sie unterstützen möchten, eine Organisations-E-Mail-Vorlage erstellen. Diese Vorlage definiert den E-Mail-Betreff, den Absender, die Standardsprache und den E-Mail-Text für jede unterstützte Sprache.

Führen Sie folgende Schritte aus, um eine E-Mail-Vorlage zu erstellen:

1. Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Parameter \> Organisations-E-Mail-Vorlagen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **E-Mail-Kennung** eine Kennung ein, um diese Vorlage zu identifizieren.
1. Geben Sie im Feld **Absendername** den Namen des Absenders ein.
1. Geben Sie im Feld **E-Mail-Beschreibung** eine aussagekräftige Beschreibung ein.
1. Geben Sie im Feld **E-Mail des Absenders** die E-Mail-Adresse des Absenders ein.
1. Wählen Sie im Abschnitt **Allgemein** eine Standardsprache für die E-Mail-Vorlage aus. Die Standardsprache wird verwendet, wenn für die angegebene Sprache keine lokalisierte Vorlage vorhanden ist.
1. Erweitern Sie die Abschnitt **Inhalt der E-Mail-Nachricht** und wählen Sie **Neu**, um den Vorlageninhalt zu erstellen. Wählen Sie für jedes Inhaltselement die Sprache aus und geben Sie den Betreff der E-Mail an. Wenn die E-Mail einen Textkörper haben soll, stellen Sie sicher, dass das Kästchen **Hat Text** markiert ist.
1. Wählen Sie im Aktionsbereich **E-Mail-Nachricht**, um eine E-Mail-Textvorlage bereitzustellen.

Das folgende Bild zeigt einige Beispieleinstellungen für E-Mail-Vorlagen.

![E-Mail-Vorlageneinstellungen.](media/email-template.png)

Weitere Informationen zum Erstellen von E-Mail-Vorlagen finden Sie unter [Erstellen von E-Mail-Vorlagen für transaktionale Ereignisse](email-templates-transactions.md). 

## <a name="create-an-email-notification-profile"></a>Ein E-Mail-Benachrichtigungsprofil erstellen

Gehen Sie folgendermaßen vor, um ein E-Mail-Benachrichtigungsprofil in Headquarters zu erstellen.

1. Gehen Sie im Navigationsbereich zu **Module \> Retail and Commerce \> Headquarters-Einrichtung \> Commerce-E-Mail-Benachrichtigungsprofil**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **E-Mail-Benachrichtigungsprofil** einen Namen ein, um das Profil zu identifizieren.
1. Geben Sie im Feld **Beschreibung** eine entsprechende Beschreibung ein.
1. Stellen Sie den Hebel **Aktiv** auf **Ja**.

## <a name="add-a-notification-type"></a>Einen Benachrichtigungstyp hinzufügen

Führen Sie folgende Schritte aus, um eine E-Mail-Ereignis zu erstellen:

1. Gehen Sie im Navigationsbereich zu **Module \> Retail and Commerce \> Headquarters-Einrichtung \> Commerce-E-Mail-Benachrichtigungsprofil**.
1. Wählen Sie unter **Einstellungen für Einzelhandels-E-Mail-Benachrichtigung** **Neu** aus.
1. Wählen Sie aus der Dropdownliste den entsprechenden **E-Mail-Kennungstyp**.
1. Wählen Sie die oben erstellte E-Mail-Vorlage aus der Dropdownliste **E-Mail-ID** aus.
1. Wählen Sie das Kontrollkästchen **Aktiv** aus.
1. Wählen Sie im Aktivitätsbereich **Speichern** aus.

Das folgende Bild zeigt einige Beispiele für die Einstellungen der Ereignisbenachrichtigung.

![Einstellungen für die Ereignisbenachrichtigung.](media/email-notification-profile.png)


## <a name="schedule-a-recurring-email-notification-process-job"></a>Einen Verarbeitungsauftrag für eine Serien-E-Mail-Benachrichtigung planen

Zum Versenden von E-Mail-Benachrichtigungen muss der Auftrag **E-Mail-Benachrichtigung für Einzelhandelsauftrag verarbeiten** ausgeführt werden.

Gehen Sie wie folgt vor, um in Headquarters einen Stapelverarbeitungsauftrag zum Senden von Transaktions-E-Mails einzurichten.

1. Gehen Sie zu **Einzelhandel und Handel \> Einzelhandel und Handel IT \> E-Mail und Benachrichtigungen \> E-Mail-Benachrichtigungen senden**.
1. Wählen Sie im Dialogfeld **E-Mail-Benachrichtigung für Einzelhandelsauftrag verarbeiten** **Serie** aus.
1. Wählen Sie im Dialogfeld **Wiederholung definieren** **Kein Enddatum** aus.
1. Wählen Sie unter **Wiederholungsmuster** **Minuten** aus und legen Sie dann das Feld **Anzahl** auf **1** fest. Diese Einstellungen stellen sicher, dass E-Mail-Benachrichtigungen so schnell wie möglich verarbeitet werden.
1. Wählen Sie im Dialogfeld **E-Mail-Benachrichtigung für Einzelhandelsauftrag verarbeiten** **OK** aus.
1. Wählen Sie **OK**, um das Einrichten des Auftrags abzuschließen.

## <a name="next-steps"></a>Nächste Schritte

Bevor E-Mails gesendet werden können, müssen Sie Ihren Postausgangsdienst konfigurieren. Weitere Informationen finden Sie unter [E-Mail konfigurieren und senden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[E-Mails konfigurieren und senden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Kanäle – Übersicht](channels-overview.md)

[Kanaleinstellungen – Voraussetzungen](channels-prerequisites.md)

[Organisationen und Organisationshierarchien – Übersicht](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
