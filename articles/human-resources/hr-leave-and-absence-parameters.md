---
title: Beurlaubungs- und Abwesenheitsparameter konfigurieren
description: Definieren Sie Personalparameter für Urlaub und Abwesenheit in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 196c3901b5bc19f73b882bac7d3361e5bcc37e07
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712375"
---
# <a name="configure-leave-and-absence-parameters"></a>Beurlaubungs- und Abwesenheitsparameter konfigurieren

Bevor Sie Urlaubs- und Abwesenheitspläne einrichten in Dynamics 365 Human Resourcesi st es eine gute Idee, die Einstellungen für alle zugehörigen Personalparameter zu überprüfen, einschließlich:

- Nummernfolge für Urlaubsanträge
- Family and Medical Leave Act (FMLA) Einstellungen
- Self-Service-Einstellungen für Mitarbeiter für Urlaubs- und Abwesenheitsanträge
- Urlaubs- und Abwesenheitsparameter

## <a name="view-and-change-human-resources-parameters"></a>Personalverwaltungsparameter anzeigen und ändern

1. Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.

2. Unter **Einrichtung** wählen Sie **Personalverwaltungsparameter einrichten**.

3. Auf der **Zahlenfolgen** Registerkarte, überprüfen Sie die **Zahlenfolgecode** für **Urlaubsanfragen-ID** und ändern Sie nach Bedarf. Diese Einstellung legt die Reihenfolge fest, in der IDs zum automatischen Zuweisen von IDs für Urlaubsanforderungen.

4. Auf der **FMLA** Registerkarte, überprüfen Sie die FMLA-Einstellungen und ändern Sie sie nach Bedarf.

5. Auf der Registerkarte **Mitarbeiter-Selbstservice** geben Sie an, ob Manager Urlaubs- und Abwesenheitsanträge für ihre Mitarbeiter eingeben können.

7. Wählen Sie **Speichern** aus.

## <a name="view-and-change-leave-and-absence-parameters"></a>Urlaub- und Abwesenheitsparameter anzeigen und ändern

1. Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.

2. Unter **Installieren**, wählen Sie **Urlaubs- und Abwesenheitsparameter**.

3. Legen Sie auf der Registerkarte **Allgemein** die folgenden Parameter fest:
 
    - **Einheit für Urlaub und Abwesenheit** auf Stunden oder Tage festlegen. Wenn Tage, können Sie **Aktivieren Sie die Halbtagesdefinition** auswählen, damit die Mitarbeiter in ihren Freistellungsanträgen entweder die erste oder die zweite Tageshälfte auswählen können. 

    - Wählen Sie **Datum des Inkrafttretens der Dienstmonate**, um festzulegen, wann die Abgrenzungssätze für Urlaubspläne mit monatelanger Dienstzeit wirksam werden.

    - Wählen Sie **Bilanzberechnung** aus, um Salden anzuzeigen, die ab heute oder ab dem Abgrenzungszeitraum angezeigt werden. Wenn Sie **Saldo ab heute** in der Bilanz auswählen, wird die Summe aller Rückstellungen, Anpassungen und Anforderungen bis heute angezeigt. Wenn Sie **Saldo zum Abgrenzungszeitraum** auswählen, zeigt der Saldo die Summe aller Rückstellungen, Anpassungen und Anforderungen ab dem Abgrenzungszeitraum an, der durch die Häufigkeit im Urlaubsplan definiert ist. 

    - Legen Sie die Startzeit für den Vortragsablaufuhrzeit-Batchauftrag fest.  
    
    - Wählen Sie **Ja** für **Mitarbeitern erlauben, Urlaub zu kaufen** und **Mitarbeitern erlauben, Urlaub zu verkaufen** aus. Wenn Sie für diese Optionen **Ja** auswählen, können Sie Richtlinien zum Kauf und Verkauf von Urlaub erstellen und es Mitarbeitern ermöglichen, Anforderungen zum Kaufen und Verkaufen von Urlaubsanforderungen einzureichen.

## <a name="configure-calendar-parameters"></a>Konfigurieren Sie die Kalenderparameter

1. Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.

2. Unter **Installieren**, wählen Sie **Urlaubs- und Abwesenheitsparameter**.

3. Auf der **Kalender** Registerkarte, überprüfen Sie die Einstellungen und ändern Sie sie nach Bedarf.

4. Wählen Sie **Speichern**.

## <a name="see-also"></a>Siehe auch

- [Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)
