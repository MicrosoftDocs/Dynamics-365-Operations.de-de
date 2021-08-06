---
title: Für Zahlung bereit
description: Dieses Thema zeigt, wie Sie einen Mitarbeiter als zahlungsbereit markieren in Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f9aa9e60b51b1801c07981ad120cb77f65fee286
ms.sourcegitcommit: baad2723291774f610324a8054fc14abf3287fe1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/14/2021
ms.locfileid: "6560107"
---
# <a name="ready-to-pay"></a>Für Zahlung bereit

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

> [!NOTE]
> Wenn Sie einen Mitarbeiter als zahlungsbereit kennzeichnen möchten, müssen Sie zunächst die **(Vorschau-) Integration der Gehaltsabrechnung** Funktionalität in der Funktionsverwaltung aktivieren. Weitere Informationen zur Aktivierung der Vorschaufunktionen finden Sie unter [Funktonen verwalten](hr-admin-manage-features.md).

Diese Funktion ermöglicht es Personalfachleuten zu verstehen, welche Mitarbeiter für die Gehaltsabrechnung bereit sind und welche Maßnahmen erforderlich sind, bevor sie von einem externen Gehaltsabrechnungsanbieter verwendet werden.

## <a name="mark-employee-as-ready-to-pay"></a>Mitarbeiter als zahlungsbereit kennzeichnen

Das Sammeln und Validieren von Mitarbeiterinformationen kann zeitaufwändig und fehleranfällig sein. Durch die Bereitstellung einer Möglichkeit für Personalverantwortliche, Mitarbeiterinformationen zu überprüfen und einfach zu aktualisieren hilft Dynamics 365 Human Resources, den Zeitaufwand für die Vorbereitung der Gehaltsabrechnung zu reduzieren.

Um einen Mitarbeiter als zahlungsbereit zu kennzeichnen:

1. Öffnen Sie **Vergütungsverwaltung**. Es gibt zwei Kacheln im Arbeitsbereich 
    - **Für Zahlung bereite Mitarbeiter**
    - **Mitarbeiter nicht zahlungsbereit**
    ![Arbeitsbereich Vergütungsmanagement.](./media/hr-ready-to-pay-1-workspace.png)

2. Wählen Sie die Kachel **Mitarbeiter nicht zahlungsbereit** aus.

3. Wählen Sie die zu überprüfenden Mitarbeiter aus. Auf der **Registerkarte Gehaltsabrechnung** wählen Sie die Gruppe **Zahlungsbereit** und **Bestätigen**.
    ![Mitarbeiter überprüfen.](./media/hr-ready-to-pay-2-validate.png)

4. Um die Ergebnisse zu überprüfen, wählen Sie auf der **Registerkarte Gehaltsabrechnung** die Gruppe **Zahlungsbereit** und **Ergebnisse**.

## <a name="validation"></a>Prüfung

Bevor ein Mitarbeiter als zahlungsbereit markiert wird, führt das System eine grundlegende Überprüfung der Profilvollständigkeit durch.

![Das Ergebnis überprüfen.](./media/hr-ready-to-pay-3-results.png)

Die folgende Tabelle enthält weitere Informationen über jede zusätzliche Prüfung, die ausgeführt wird. 

| Prüfung | Informationen |
| --- | --- |
| Parameter für Zweck der Adresse | Prüft, ob der Parameter **Zweck der Gehaltsabrechnung verwenden** aktiviert ist. |
| Lohnadresse | Überprüft, ob das Arbeitskraftprofil mindestens eine Adresse mit dem Zweck Wohnort der Gehaltsabrechnung oder Arbeitsort der Gehaltsabrechnung hat und nur eine Adresse pro Zweck vorhanden ist. |
| Beschäftigung | Überprüfen Sie, ob der Arbeitnehmer mindestens eine Beschäftigung hat (aktuell, früher oder zukünftig). |
| Kennungsnummer | Überprüft, ob der Parameter Identifikationstypen in der Personalabrechnung verwenden auf Ja gesetzt ist und ob der im Parameter angegebene Identifikationstyp im Arbeiterprofil ausgefüllt ist. |
| Vor- und Nachname | Überprüft, ob das Arbeitskraft-Profil gültig ist, und prüft, ob die Felder **Name** und **Familienname, Nachname** ausgefüllt sind.|
| Positionsnummer | Überprüfen Sie, ob der Arbeitskraft eine Position zugewiesen ist. |
| Geburtstag | Überprüft, ob das Arbeitskraft-Profil gültig ist, und prüft, ob das Feld **Geburtstag** ausgefüllt ist. |
| Vergütung | Überprüfen Sie, ob die Arbeitskraft in einen festen Vergütungsplan eingeschrieben ist. |

Schlägt eine dieser Validierungen fehl, können Sie den Mitarbeiter nicht als zahlungsbereit markieren.

Wenn das Feld **Zahlungsbereit** **Nein** ist, ist dies ein Hinweis darauf, dass Sie eine Aktion ausführen müssen, um sicherzustellen, dass das Arbeitskraft-Profil vollständig ist. Dies verhindert nicht, dass die Daten in einer Datenentität verfügbar gemacht werden. 

## <a name="known-issues"></a>Bekannte Probleme

- Sie müssen die Funktion **Optimierter Mitarbeitereinstieg** in der Funktionsveraltung deaktivieren. Die Kacheln im Arbeitsbereich Vergütungsverwaltung funktionieren nicht richtig, wenn Sie diese Funktion verwenden.
- Im Formular Arbeitskraft ist die Gruppe **Registerkarte Gehaltsabrechnung**, **Zahlungsbereit** ist für jede Benutzerrolle verfügbar. 

## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
