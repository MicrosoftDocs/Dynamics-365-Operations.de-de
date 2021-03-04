---
title: Neuerungen oder Änderungen in Dynamics 365 Talent – Core HR (11. Januar 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent – Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d49a4aca368e3de10ae37b56c6d286d78f7f369a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461300"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-11-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent – Core HR (11. Januar 2019)

**Build 8.1.2100**

In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.

## <a name="changes"></a>Änderungen

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>Validierung von Urlaubsanträgen durch Prognose des verfügbaren Saldos
Die in diesem Release vorgenommenen Änderungen ermöglichen es den Mitarbeitern, zukünftige Urlaubszeiten zu beantragen, ohne von ihrem aktuellen Saldo abzuziehen. Für zukünftige Anfragen werden Standard-Workflows verwendet. Weitere Informationen finden Sie unter [Zeit basierend auf Freizeit auf Grundlage der gearbeiteten Stunden abgrenzen](leave-accrue-hours-worked.md).

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>Ansicht der prognostizierten Urlaubsbilanz in ESS und People
Diese Funktion ermöglicht die Anzeige von Salden für zukünftige Urlaubszeiträume durch HR, Manager und Mitarbeiter. Mitarbeiter können zukünftige Salden im **Mitarbeiter-Self-Service**-Arbeitsbereich einsehen und die Personalabteilung hat über den **Mitarbeiterarbeitsbereich** Zugriff auf die gleichen Informationen.

### <a name="notifications-for-changing-leave-balances"></a>Benachrichtigungen zur Änderung von Urlaubssalden
Die Urlaubssalden zeigen den aktuellen Saldo des Mitarbeiters an. Zukünftige Salden sind auf den **Mitarbeiter-Self-Service**-**Arbeitsbereichen** verfügbar, indem Sie ein "Ab-Datum" eingeben, um den prognostizierten Saldo zu berechnen.

Die Navigation zur Anzeige der prognostizierten Salden in den folgenden Bereichen wurde hinzugefügt:
  - **Urlaub**-Karte im **Mitarbeiter-Self-Service**-Arbeitsbereich.
  - **Urlaubs- und Abwesenheitskarte** im **Manager-Self-Service**-Arbeitsbereich.
  - **Urlaubs- und Abwesenheitsseite** im **Mitarbeiter-Self-Service**-Arbeitsbereich.

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>Dezimalstellen für variable Vergütungspläne (Cash-Pläne) zulassen
Variable Barzuteilungen und -pläne haben nun die zusätzliche Flexibilität für Beträge und Überschreibungen für Werte mit Dezimalbeträgen.

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>Es ist nicht möglich, die Daten der Anmeldungen für variable Komponenten nach dem Speichern des Plans zu ändern.
Diese Änderung ermöglicht es, das Planenddatum nach dem Speichern des Plans zu aktualisieren (zu verlängern oder zu verfallen). Sie können Pläne unabhängig vom Start- und Enddatum weiterhin aktivieren oder deaktivieren.

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>Abrechnungsinformationen, die bei Zuweisung der Sicherheitsrolle Personalsachbearbeiter verfügbar sind
Die Rolle Sachbearbeiter Abrechnung wurde aktualisiert, um während des Antragsprozesses Zugriff auf die Abrechnungsinformationen zu haben.

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Mitarbeiter-Self-Service | Details der Positionshierarchie aus der Kachel führt nicht zum übergeordneten Knoten
Es wurden Änderungen vorgenommen, um einen Fehler zu beheben, der beim Hinzufügen der Positionshierarchie zu neuen Arbeitsbereichen und beim Navigieren innerhalb der Organisationsstruktur aufgetreten ist.

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>Neue Validierungsmeldung bei Verwendung der Personalnummernreihenfolge
Es wurde eine Änderung vorgenommen, um zu klären, worum es geht, wenn Sie einen Mitarbeiter einstellen und die nächste Personalnummer verwendet wird.

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>Mitarbeiter-Self-Service-Arbeitsbereich, der als Einstiegsseite ausgewählt wurde
Wenn der **Mitarbeiter-Self-Service**-Arbeitsbereich als Einstiegsseite für einen Benutzer ausgewählt ist und diesem Benutzer nicht die Mitarbeiterrolle zugewiesen ist, leitet das System zum Standard-Dashboard um.

### <a name="termination-reason-code-updates-position-assignment-record"></a>Abbruchgrund Code aktualisiert Positionszuordnungssatz
Der Kündigungsgrund aktualisiert nun die Planstellenzuordnung, wenn ein Mitarbeiter gekündigt und die Planstelle beendet wird. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]