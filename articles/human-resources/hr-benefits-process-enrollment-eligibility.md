---
title: Registrierungsberechtigung verarbeiten
description: In diesem Artikel wird erläutert, wie der Prozess der Registrierungsberechtigung ausgeführt wird.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bd05585f691a4c6aa55a7aec7ceaaf0273f0abcb
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323480"
---
# <a name="process-enrollment-eligibility"></a>Registrierungsberechtigung verarbeiten

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird erläutert, wie der Prozess der Registrierungsberechtigung ausgeführt wird.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Bearbeitung** die Option **Verarbeitung von Registrierungsberechtigung**.

2. Geben Sie im Dialogfeld **Verarbeitung von Vorteilsregistrierungsberechtigung ausführen** Werte für die folgenden Felder ein:

   | Feld | Beschreibung |
   | --- | --- |
   | **Registrierungsperiode** | Die Registrierungsperiode, für die die Registrierungsberechtigung verarbeitet wird. |
   | **Juristische Person** | Die juristische Person, für die die Registrierungsberechtigung verarbeitet wird. |
   | **Arbeitskraft** | Die Arbeitskraft, für die die Registrierungsberechtigung verarbeitet wird. Wenn Sie dieses Feld leer lassen, wird die Registrierungsberechtigung für alle Arbeitskräfte verarbeitet. |
   | **Vergütungsplan** | Der Vorteilsplan, für den die Registrierungsberechtigung verarbeitet wird.

3. Wenn Sie den Prozess im Hintergrund ausführen möchten, wählen Sie **Im Hintergrund ausführen** und führen Sie die folgenden Aufgaben aus:

   1. Geben Sie Informationen für den Prozess ein.

   2. Um eine wiederkehrende Stelle einzurichten, wählen Sie **Wiederholung**, geben Sie die Wiederholungsinformationen ein und wählen Sie **OK**.

   3. Um eine Stellenbenachrichtigung einzurichten, wählen Sie **Benachrichtigungen**, wählen Sie die zu empfangenden Benachrichtigungen und wählen Sie dann **OK**.

   4. Wählen Sie **OK**. Der Prozess wird mit den von Ihnen festgelegten Parametern ausgeführt.

4. Wählen Sie **OK**.

## <a name="view-process-results"></a>Anzeigen von Prozessergebnissen

In diesem Artikel wird erläutert, wie die Berechtigung der Prozessergebnisse angezeigt wird.

1.  Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Prozess** die Option **Prozessergebnisse**.

2.  Auf der Seite **Prozessergebnisse** werden die folgenden Felder angegeben:

   | Feld | Beschreibung |
   | --- | --- |
   | **Prozesskennung** | Die eindeutige ID für die Kombination aus Arbeitskraft, juristischer Person und Prozesslauf. |
   | **Prozesstyp** | Dies identifiziert den Prozess, der ausgeführt wurde. Zum Beispiel: Anmeldung. |
   | **Zeitstempel** | Die Zeit, zu der der Berechtigungsprozess ausgeführt wurde. |
   | **Juristische Person** | Die während des Registrierungsprozesses angegebene juristische Person. |
   | **Worker** | Die Arbeitskraft, die verarbeitet wurde. |
   | **Plan | Der Leistungsplan, für den eine Registrierung versucht wurde. |
   | **Berechtigungsregel** | Die Berechtigungsregel, die verarbeitet wurde. Wenn vor dem Ausführen der Berechtigung ein Fehler aufgetreten ist, ist dieser leer. Beispiel: Wenn für einen Mitarbeiter keine Vergütung definiert wurde, wird der Berechtigungsprozess nicht ausgeführt, und dieses Feld bleibt leer. |
   | **Ergebnisstatus** | Dies ist berechtigt oder nicht berechtigt. Der Ergebnisstatus ist nicht berechtigt, wenn der Arbeitnehmer die Kriterien für die Berechtigungsregel nicht erfüllt, wenn dem Arbeitnehmer die erforderlichen Informationen wie eine Gehaltshäufigkeit oder eine feste Vergütung fehlen oder wenn im Leistungsplan Informationen fehlen, die die Einschreibung von Arbeitnehmern verhindern. |
   | **Ergebnismeldung** | Gibt an, warum ein Arbeitnehmer keinen Anspruch auf einen Leistungsplan hat oder ob die Anspruchsregel erfüllt wurde. |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
