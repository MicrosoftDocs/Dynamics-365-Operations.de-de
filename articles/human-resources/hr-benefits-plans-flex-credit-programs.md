---
title: Flexguthabenprogramme einrichten
description: Sie können Flexguthabenprogramme in Microsoft Dynamics 365 Human Resources verwenden, um Mitarbeiter für Vorteile gemäß einer festgelegten Höhe von Flexguthaben zu registrieren.
author: twheeloc
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitCreditPrograms, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1808d703983fd11e29f83c13f6181fb3068bc49
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533767"
---
# <a name="set-up-flex-credit-programs"></a>Flexguthabenprogramme einrichten


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sie können Flexguthabenprogramme in Microsoft Dynamics 365 Human Resources verwenden, um Mitarbeiter für Vorteile gemäß einer festgelegten Höhe von Flexguthaben zu registrieren. Mitarbeiter können wählen, wie sie ihr Flexguthaben zuordnen möchten. Wenn ein Mitarbeiter beispielsweise in der Krankenversicherung seines Ehepartners mitversichert ist, möchte er möglicherweise das Guthaben, das er sonst für die Krankenversicherung verwendet hätte, für andere Vorteile verwenden. 

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Pläne** die Option **Flexguthabenprogramme**.

2. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Vergütungsgutschriftenkennung** | Der eindeutige Bezeichner des Flexguthabenprogramms. |
   | **Beschreibung** | Eine Beschreibung des Flexguthabenprogramms. | 
   | **Anfangsdatum** | Das Datum, an dem das Flexguthabenprogramm aktiv wird. |
   | **Enddatum** | Das Enddatum des Flexguthabenprogramms. Sie können den Standardwert (31.12.2154) beibehalten, um anzugeben, dass für das Flexguthabenprogramm kein geplanter Ablauf festgelegt ist. |
   | **Guthabenwert gesamt** | Die Höhe des Guthabens, das jeder Mitarbeiter für seine Vorteile verwenden muss. |
   | **Regel zur anteiligen Verrechnung** | Die Regel zur anteiligen Verrechnung von Flexguthaben, wenn ein Mitarbeiter in der Mitte der Flexguthabenperiode eingestellt wird. </br></br><ul><li>**Kein** – Der Mitarbeiter erhält kein Flexguthaben, wenn er nach dem Start des Flexguthabenprogramms eingestellt wird.</li><li>**Volles Guthaben** – Der Mitarbeiter erhält die volle Höhe des Flexguthabens, unabhängig davon, wann er eingestellt wird.</li><li>**Anteilige Verrechnung** – Der Mitarbeiter erhält einen Anteil des Flexguthabens, das auf seinem Startdatum basiert.</li></ul> |
   | **Formel für anteilige Berechnung des Flexguthabens** | Die Regel zur anteiligen Verrechnung von Flexguthaben, wenn Mitarbeiter in der Mitte der Flexguthabenperiode eingestellt werden. Die anteilige Verrechnung basiert auf dem Einstellungsbeginn. Dieses Feld wird nur verwendet, wenn im Feld **Regel zur anteiligen Verrechnung** die Option **Anteilige Verrechnung** ausgewählt wird. </br></br><ul><li>**Täglich** – Teilt die Höhe des Flexguthabens, die ein Mitarbeiter erhält, auf dem Tageslevel. Die Gesamthöhe des Flexguthabens wird durch die Anzahl der Tage in der Periode geteilt. Wenn Ihre Vorteilsperiode beispielsweise 400 Tage beträgt, dividiert das System die Gesamthöhe des Flexguthabens durch 400, um die Höhe des Flexguthabens zu berechnen, das ein Mitarbeiter pro Tag erhält.</li><li>**Aktueller Monat** – Teilt die Höhe des Flexguthabens, die ein Mitarbeiter erhält, auf dem Monatslevel, auf den aktuellen Monat gerundet. Die Gesamthöhe des Flexguthabens wird durch die Anzahl der Monate in der Periode geteilt. Wenn Ihre Vorteilsperiode beispielsweise 15 Monate beträgt, dividiert das System die Gesamthöhe des Flexguthabens durch 15, um die Höhe des Flexguthabens zu berechnen, das ein Mitarbeiter pro Monat erhält.</li><li>**Folgender Monat** – Teilt die Höhe des Flexguthabens, die ein Mitarbeiter erhält, auf dem Monatslevel, auf den nächsten Monat gerundet. Die Gesamthöhe des Flexguthabens wird durch die Anzahl der Monate in der Periode geteilt. Wenn Ihre Vorteilsperiode beispielsweise 15 Monate beträgt, dividiert das System die Gesamthöhe des Flexguthabens durch 15, um die Höhe des Flexguthabens zu berechnen, das ein Mitarbeiter pro Monat erhält.</li></ul> |
   


[!INCLUDE[footer-include](../includes/footer-banner.md)]
