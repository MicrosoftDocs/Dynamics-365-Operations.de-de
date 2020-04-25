---
title: Beurlaubungs- und Abwesenheitsparameter konfigurieren
description: Definieren Sie Personalparameter für Urlaub und Abwesenheit in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb992cbfbed33f88e125d3a8b721f8815414599a
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197980"
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

6. Auf der **Urlaub und Abwesenheit** Registerkarte, überprüfen Sie die Einstellungen und ändern Sie sie nach Bedarf.

7. Wählen Sie **Speichern**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Urlaub- und Abwesenheitsparameter anzeigen und ändern

1. Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.

2. Unter **Installieren**, wählen Sie **Urlaubs- und Abwesenheitsparameter**.

3. Legen Sie auf der Registerkarte **Allgemein** die folgenden Parameter fest:
 
    - **Einheit für Urlaub und Abwesenheit** auf Stunden oder Tage festlegen. Wenn Tage, können Sie **Aktivieren Sie die Halbtagesdefinition** auswählen, damit die Mitarbeiter in ihren Freistellungsanträgen entweder die erste oder die zweite Tageshälfte auswählen können. 

    - Wählen Sie **Datum des Inkrafttretens der Dienstmonate**, um festzulegen, wann die Abgrenzungssätze für Urlaubspläne mit monatelanger Dienstzeit wirksam werden.

    - Wählen Sie **Bilanzberechnung**, um Salden anzuzeigen, die ab heute oder ab dem Abgrenzungszeitraum angezeigt werden. Wenn Sie **Saldo ab heute** in der Bilanz auswählen, wird die Summe aller Rückstellungen, Anpassungen und Anforderungen bis heute angezeigt. Wenn Sie **Saldo zum Abgrenzungszeitraum** auswählen, zeigt der Saldo die Summe aller Rückstellungen, Anpassungen und Anforderungen ab dem Abgrenzungszeitraum an, der durch die Häufigkeit im Urlaubsplan definiert ist. 

## <a name="configure-calendar-parameters"></a>Konfigurieren Sie die Kalenderparameter

1. Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.

2. Unter **Installieren**, wählen Sie **Urlaubs- und Abwesenheitsparameter**.

3. Auf der **Kalender** Registerkarte, überprüfen Sie die Einstellungen und ändern Sie sie nach Bedarf.

4. Wählen Sie **Speichern**.

## <a name="see-also"></a>Siehe auch

- [Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)
