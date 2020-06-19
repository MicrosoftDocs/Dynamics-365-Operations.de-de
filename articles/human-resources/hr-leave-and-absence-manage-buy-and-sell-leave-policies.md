---
title: Verwalten Sie Kauf- und Verkaufsurlaubsrichtlinien
description: Sie können Mitarbeitern ermöglichen, Urlaub zu kaufen und zu verkaufen in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429012"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Verwalten Sie Kauf- und Verkaufsurlaubsrichtlinien

[!include [banner](includes/preview-feature.md)]

Sie können Mitarbeitern den Kauf von Urlaub ermöglichen, indem Sie eine Richtlinie für den Kauf von Urlaub erstellen.  

## <a name="enable-employees-to-buy-and-sell-leave"></a>Sie können Mitarbeitern ermöglichen, Urlaub zu kaufen und zu verkaufen in

1. Auf der **Urlaubs- und Abwesenheitsparameter** Seite wählen Sie **Ja**, um **Mitarbeitern zu erlauben, Urlaub zu kaufen**. 

## <a name="create-a-buy-leave-policy"></a>Erstellen einer Richtlinie für den Kuaf von Urlaub

1. Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**. 

2. Wählen Sie **Richtlinie für den Kauf- und Verkauf von Urlaub**.

3. Wählen Sie **Neu** aus.

4. Geben Sie einen **Namen** und eine **Beschreibung** für die Richtlinie ein unter **Richtlinie für den Kauf- und Verkauf von Urlaub**. 

5. Einen **Dokumenttyp** auswählen. 

   Die verfügbaren Richtlinientypen sind **Menge** und **Stunden pro Woche**. Wählen Sie **Menge** aus, um einen **Festen Betrag** für die maximalen Beträge, die Mitarbeiter kaufen und verkaufen können, einzugeben. Wenn Sie **Stunden pro Woche** auswählen, wrid die im zugewiesenen Arbeitszeitkalender des Mitarbeiters definierte Arbeitszeit verwendet, um den Höchstbetrag der Richtlinieolice zu bestimmen. 

6. Wählen Sie ein **Startdatum** und ein **Enddatum** für die Richtlinie aus. Anträge auf Kauf oder Verkauf von Urlaub können nur in diesem Zeitraum eingereicht werden. 

7. Unter **Kaufrichtlinie**, wählen **Vollzeitäquivalenz** (FTE) aus, um den Höchstbetrag basierend auf dem auf der Position des Mitarbeiters definierten FTE aufzuteilen. Wenn der Richtlinientyp **Menge** ist, geben Sie einen **Maximalen festen Betrag** ein. 

8. Wählen Sie **Hinzufügen**, um die Urlaubsarten für Mitarbeiter hinzuzufügen, um Urlaub zu kaufen. Sie können der Richtlinie mehrere Urlaubstypen hinzufügen. 

9. Geben Sie die **Dienstmonate** für die Urlaubsart ein, damit verschiedene Dienstmonate den Höchstbetrag bestimmen können, den ein Mitarbeiter kaufen kann. 

10. Dient zum Eingeben des **Maximalen Betrags** für den Urlaubstyp. 

11. Geben Sie die **Rate** ein, zu der der Arbeitnehmer den Urlaub kauft. 

12. Optional geben Sie den **Verdienstcode** ein, der für den Kauf von Urlaub verwendet werden soll. 

13. Legen Sie optional fest, ob FTE verwendet werden soll, um den Höchstbetrag für die Urlaubsart zu bestimmen. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Fügen Sie die Kauf- und Verkaufsurlaubsrichtlinie einem Urlaubs- und Abwesenheitsplan hinzu

1. Auf der **Urlaub und Abwesenheit** Seite, wählen Sie einen Urlaubs- und Abwesenheitsplan.

2. Wählen Sie **Regeln** für die **Richtlinie für den Kauf- und Verkauf**.

## <a name="see-also"></a>Siehe auch

[Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)</br>
[Urlaubs- und Abwesenheitstypen konfigurieren](hr-leave-and-absence-types.md)</br>
[Urlaubs- und Abwesenheitspläne antizipieren](hr-leave-and-absence-accrue.md)</br>
[Urlaub kaufen und verkaufen](hr-employee-self-service-buy-sell-leave.md)

