---
title: Vorteils-E-Mail-Benachrichtigung
description: Dieser Artikel enthält einen Überblick über die E-Mail-Benachrichtigungsfunktion der Vorteilsverwaltung in Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d550cbb2f639535dbb43765c9fb0632a514fbe8c
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229910"
---
# <a name="benefits-email-notification"></a>Vorteils-E-Mail-Benachrichtigung

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [banner](../includes/preview-banner.md)]

Die E-Mail-Benachrichtigungsfunktion ermöglicht das Versenden von E-Mail-Benachrichtigungen und Erinnerungen an Mitarbeiter in den folgenden Szenarien:

- Registrierung neu eingestellter Mitarbeiter
- Offene Registrierung
- Qualifizierende Lebensereignisse

Sie können mehrere E-Mail-Vorlagen erstellen und festlegen und die Benachrichtigungen mithilfe des Arbeitsbereich **Vorteilsverwaltung** und der Seite **Arbeitskräftevergütungen** senden. Sie können auch den Benachrichtigungs-/Erinnerungsverlauf nachverfolgen.

## <a name="set-up-human-resources-shared-parameters"></a>Freigegebene Personalverwaltungsparameter einrichten

Sie können auf der Seite **Freigegebene Personalverwaltungsparameter** die Vorteils-E-Mail-Vorlagen für verschiedene Kommunikationsarten erstellen, die an Mitarbeiter oder Mitarbeitergruppen gesendet werden.

## <a name="create-a-new-email-id-template"></a>Eine neue E-Mail-ID-Vorlage erstellen

Führen Sie folgende Schritte aus, um eine neue E-Mail-ID-Vorlage zu erstellen.

1. Gehen Sie zu **System-E-Mail-Vorlagen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **E-Mail-ID** einen Namen ein.
4. Legen Sie andere Felder nach Bedarf fest.
5. Wählen Sie **E-Mail-Nachrichten** aus, um die Vorlage hochzuladen.
6. Wählen Sie auf der Seite **Freigegebene Personalverwaltungsparameter** die neue Vorlage unter **Systemvorlagen** aus und verschieben Sie sie zu **Vorlagen für Vorteile**.

## <a name="send-email-to-employees"></a>E-Mail an Mitarbeiter senden

Gehen Sie folgendermaßen vor, um eine E-Mail an einen neuen Mitarbeiter zu senden, der noch nicht angefangen hat.

1. Öffnen Sie den Arbeitsbereich **Vorteilsverwaltung**.
2. Wählen Sie die Kachel für die Gruppe von Mitarbeitern aus, an die Sie die E-Mail senden möchten.
3. Wählen Sie **E-Mail senden** aus.
4. Wählen Sie die Mitarbeiter aus, denen Sie die E-Mail senden möchten.
5. Wählen Sie **E-Mail senden** aus.
6. Wählen Sie die Vorlage aus, die Sie verwenden möchten.
7. Wählen Sie **OK** aus, um die E-Mail zu senden.

    Sie können die E-Mail-Nachricht und den Status auf der Seite **Arbeitskräftevergütungen** des Mitarbeiters überprüfen oder indem Sie **Vorteiles-E-Mail-Verlauf** im Abschnitt **Verknüpfungen** des Arbeitsbereich **Vorteilsverwaltung** auswählen. Sie können die E-Mail auch von der Seite **Vergütungsplan für Arbeitskraft** aus senden.

8. Um den E-Mail-Verlauf für Vorteile anzuzeigen, wählen Sie im Arbeitsbereich **Vorteilsverwaltung** im Abschnitt **Verknüpfungen** **Vorteils-E-Mail-Verlauf** aus.
9. Zeigen Sie den vollständigen E-Mail-Verlauf für gesendete Vorteils-E-Mails an. Um den Inhalt der E-Mail zu überprüfen, wählen Sie **Nachricht anzeigen** aus.
10. Wählen Sie **Arbeitskraft** aus.
11. Auf der Seite **Vergütungsplan für Arbeitskraft** können Sie E-Mails senden und den Vorteils-E-Mail-Verlauf anzeigen.

Der Arbeitsbereich **Vorteilsverwaltung** enthält verschiedene Kacheln. Sie können E-Mails senden, indem Sie die entsprechende Vorlage auswählen. Wenn die Registrierungs-E-Mails für neue Mitarbeiter gesendet wurden, wählen Sie die Kachel **Neuer Mitarbeiter, nicht angefangen** und dann die Verknüpfung **Erinnerung senden**. Sie können eine Erinnerungsvorlage auswählen und den Titel der Benachrichtigung als erste, zweite oder dritte Erinnerung festlegen.
