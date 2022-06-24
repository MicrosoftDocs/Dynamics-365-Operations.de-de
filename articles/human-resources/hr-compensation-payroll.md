---
title: Für Zahlung bereit
description: Dieser Artikel zeigt, wie Sie einen Mitarbeiter als zahlungsbereit markieren in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 81c73584e3567d620292227ce4a24c3c0945fa96
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862858"
---
# <a name="ready-to-pay"></a>Für Zahlung bereit


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!NOTE]
> Wenn Sie einen Mitarbeiter als zahlungsbereit kennzeichnen möchten, müssen Sie zunächst die **(Vorschau-) Integration der Gehaltsabrechnung** Funktionalität in der Funktionsverwaltung aktivieren. Weitere Informationen zur Aktivierung der Vorschaufunktionen finden Sie unter [Funktonen verwalten](hr-admin-manage-features.md).

Diese Funktion ermöglicht es Personalfachleuten zu verstehen, welche Mitarbeiter für die Gehaltsabrechnung bereit sind und welche Maßnahmen erforderlich sind, bevor sie von einem externen Gehaltsabrechnungsanbieter verwendet werden.

## <a name="mark-employee-as-ready-to-pay"></a>Mitarbeiter als zahlungsbereit kennzeichnen

Das Sammeln und Validieren von Mitarbeiterinformationen kann zeitaufwändig und fehleranfällig sein. Durch die Bereitstellung einer Möglichkeit für Personalverantwortliche, Mitarbeiterinformationen zu überprüfen und einfach zu aktualisieren hilft Dynamics 365 Human Resources, den Zeitaufwand für die Vorbereitung der Gehaltsabrechnung zu reduzieren.

Um einen Mitarbeiter als zahlungsbereit zu kennzeichnen:

1. Öffnen Sie **Vergütungsverwaltung**. Es gibt zwei Kacheln im Arbeitsbereich: 
    - **Für Zahlung bereite Mitarbeiter**
    - **Mitarbeiter nicht zahlungsbereit**
    ![Arbeitsbereich Vergütungsmanagement.](./media/hr-ready-to-pay-1-workspace.png)

2. Wählen Sie die Kachel **Mitarbeiter nicht zahlungsbereit** aus.

3. Wählen Sie die zu überprüfenden Mitarbeiter aus. Auf der **Registerkarte Gehaltsabrechnung** wählen Sie die Gruppe **Zahlungsbereit** und **Bestätigen**.
    ![Mitarbeiter überprüfen.](./media/hr-ready-to-pay-2-validate.png)

4. Um die Ergebnisse zu überprüfen, wählen Sie auf der **Registerkarte Gehaltsabrechnung** die Gruppe **Zahlungsbereit** und **Ergebnisse**.

## <a name="validation"></a>Prüfung

Bevor ein Mitarbeiter als zahlungsbereit markiert wird, wird das Profil des Mitarbeiters auf Vollständigkeit überprüft.

![Das Ergebnis überprüfen.](./media/hr-ready-to-pay-3-results.png)

| Prüfung | Informationen |
| --- | --- |
| **Parameter für Zweck der Adresse** | Bestätigt, dass der Parameter **Zweck der Gehaltsabrechnung verwenden** ausgewählt ist |
| **Lohnadresse** | Bestätigt, dass das Mitarbeiterprofil mindestens eine Adresse mit dem Zweck **Standort der Gehaltsabrechnung** oder **Arbeitsort der Gehaltsabrechnung** hat und nur eine Adresse pro Zweck vorhanden ist |
| **Beschäftigung** | Bestätigt, dass der Arbeitnehmer mindestens eine Beschäftigung hat (aktuell, früher oder zukünftig) |
| **Kennungsnummer** | Bestätigt, dass das Feld **Identifikationstypen in der Personalabrechnung verwenden** auf **Ja** auf der Seite **Personalverwaltungsparameter** gesetzt ist, und dass der im Parameter angegebene Identifikationstyp im Mitarbeiterprofil ausgefüllt ist |
| **Vor- und Nachname** | Bestätigt, dass die Felder **Name** und **Nachname** ausgefüllt sind|
| **Positionsnummer** | Bestätigt, dass der Arbeitskraft eine Position zugewiesen ist |
| **Geburtstag** | Bestätigt, dass das Feld **Geburtstag** ausgefüllt ist |
| **Vergütung** | Bestätigt, dass die Arbeitskraft in einen festen Vergütungsplan eingeschrieben ist |

Schlägt eine dieser Validierungen fehl, können Sie den Mitarbeiter nicht als zahlungsbereit markieren.

Wenn das Feld **Zahlungsbereit** **Nein** ist, ist dies ein Hinweis darauf, dass Sie eine Aktion ausführen müssen, um sicherzustellen, dass das Arbeitskraft-Profil vollständig ist. Dies verhindert nicht, dass die Daten in einer Datenentität verfügbar gemacht werden. 

## <a name="process-automation"></a>Prozessautomatisierung

Sie können die Validierung aller Mitarbeiter mit der [Prozessautomatisierung](/dynamics365/fin-ops-core/dev-itpro/sysadmin/process-automation) automatisieren. Wechseln Sie im Arbeitsbereich **Vergütungsverwaltung** zu **Links** \> **Parameter** \> **Prozessautomatisierungen**.

## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
