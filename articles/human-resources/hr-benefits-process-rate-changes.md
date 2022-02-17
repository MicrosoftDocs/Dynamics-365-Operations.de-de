---
title: Satzänderungen verarbeiten
description: Dieses Thema erklärt, wie Sie Änderungen von Leistungssätzen in Microsoft Dynamics 365 Human Resources verarbeiten können.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5e0dfbdde8ee950a0341fffb1e268fff05434953
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070374"
---
# <a name="process-rate-changes"></a>Satzänderungen verarbeiten


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird erklärt, wie Sie Änderungen von Leistungssätzen in Microsoft Dynamics 365 Human Resources verarbeiten, wenn ein neuer oder bestehender Leistungsplan eine Änderung der Einstellungen für die Berechtigungsregeln aufweist. Wenn eine neue Berechtigungsregel erstellt und dem Plan zugewiesen wird, fordert dies das System auf, die Berechtigung der Mitarbeiter erneut auszuführen, um zu prüfen, ob die Mitarbeiter nun aufgrund der neuen Berechtigungsoptionen für den Plan berechtigt sind. 

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Bearbeitung** die Option **Verarbeitung von aktualisierten Satzänderungen**.

2. Geben Sie im Dialogfeld **Verarbeitung von Vorteilssatzaktualisierungen ausführen** Werte für die folgenden Felder ein:

   | Feld | Beschreibung |
   | --- | --- |
   | **Registrierungsperiode** | Die Registrierungsperiode, für die die Vergütungssatzänderung verarbeitet wird. |

3. Wenn Sie den Prozess im Hintergrund ausführen möchten, wählen Sie **Im Hintergrund ausführen** und führen Sie die folgenden Aufgaben aus:

   1. Geben Sie Informationen für den Prozess ein.

   2. Um eine wiederkehrende Stelle einzurichten, wählen Sie **Wiederholung**, geben Sie die Wiederholungsinformationen ein und wählen Sie **OK**.

   3. Um eine Stellenbenachrichtigung einzurichten, wählen Sie **Benachrichtigungen**, wählen Sie die zu empfangenden Benachrichtigungen und wählen Sie dann **OK**.

   4. Wählen Sie **OK**. Der Prozess wird mit den von Ihnen festgelegten Parametern ausgeführt.

4. Wählen Sie **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
