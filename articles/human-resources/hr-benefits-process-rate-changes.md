---
title: Vergütungssatzänderungen verarbeiten
description: Vergütungssatzänderungen verarbeiten in Microsoft Dynamics 365 Human Resources, wenn ein neuer oder bestehender Vorteilsplan eine Änderung an den Einstellungen der Berechtigungsregel aufweist.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb9206df990fa8980c4c641b565203828715ada9f1d2f2107a7bb707f545e225
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718130"
---
# <a name="process-rate-changes"></a>Vergütungssatzänderungen verarbeiten

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Vergütungssatzänderungen verarbeiten in Microsoft Dynamics 365 Human Resources, wenn ein neuer oder bestehender Vorteilsplan eine Änderung an den Einstellungen der Berechtigungsregel aufweist. Wenn eine neue Berechtigungsregel erstellt und dem Plan zugewiesen wird, fordert dies das System auf, die Berechtigung der Mitarbeiter erneut auszuführen, um zu prüfen, ob die Mitarbeiter nun aufgrund der neuen Berechtigungsoptionen für den Plan berechtigt sind. 

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