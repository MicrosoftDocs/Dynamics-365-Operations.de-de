---
title: Zahlungshäufigkeiten einrichten
description: Microsoft Dynamics 365 Human Resources verwendet Zahlungshäufigkeiten zur Berechnung des jährlichen Vorteilsgehalts, zur Bestimmung des Vorteilszulagenbetrags, den ein Mitarbeiter für jede Lohnperiode zahlt, und zur Festlegung der Häufigkeit, mit der Zahlungen an Anbieter erfolgen.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f5a2ad19d9f9f3a6afa2574d9fdb8841c70d6e6e
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112693"
---
# <a name="set-up-payment-frequencies"></a>Zahlungshäufigkeiten einrichten

Microsoft Dynamics 365 Human Resources verwendet Zahlungshäufigkeiten zur Berechnung des jährlichen Vorteilsgehalts, zur Bestimmung des Vorteilszulagenbetrags, den ein Mitarbeiter für jede Lohnperiode zahlt, und zur Festlegung der Häufigkeit, mit der Zahlungen an Anbieter erfolgen.

Die Vorteilszahlungshäufigkeiten verwenden Umrechnungsfaktoren, um Vorteilzahlungsperioden zwischen monatlichen, halbmonatlichen, zweiwöchentlichen, wöchentlichen und täglichen Zahlungshäufigkeiten umzurechnen. Auf diese Weise können Unternehmen die gegenseitige Abhängigkeit zwischen den Zahlungshäufigkeiten in einem Vorteilsplan definieren.

Die Felder für die Umrechnungsfaktoren identifizieren den Umrechnungsfaktor von der Zahlungshäufigkeit zu den Standardzahlungsperioden und ermöglichen dem System, Berechnungen zwischen Zahlungshäufigkeiten durchzuführen. Der Betrag des Umrechnungsfaktors bestimmt auch den Vorteilszulagenbetrag, den ein Mitarbeiter für jede Lohnzahlungshäufigkeit zahlen soll.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Zahlungshäufigkeiten**.

2. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Zahlungshäufigkeit** | Ein eindeutiger Name für die Zahlungshäufigkeit. |
   | **Beschreibung** | Eine Beschreibung der Zahlungshäufigkeit. |
   | **Periode** | Die angemessene Periode, die am besten zur Zahlungshäufigkeit des Vorteilsanbieters und des Mitarbeiters passt. Die Liste „Periode“ setzt sich aus den Standardzahlungsperioden zusammen. |
   | **Anzahl der Lohnzahlungsperioden** | Die Anzahl der Zahlungsperioden, die angibt, wie oft der Vorteilsanbieter oder die Mitarbeiter bezahlt werden. Dieser Betrag wird zur Berechnung des Vorteilsjahresgehalts des Mitarbeiters verwendet. |
   | **Jährlicher Umrechnungsfaktor** | Der jährliche Umrechnungsfaktor für die Zahlungshäufigkeit. Zum Beispiel lautet der jährliche Umrechnungsfaktor für die monatliche Lohnzahlungshäufigkeit: </br></br>(12 monatliche Zahlungen/1 Jahr) = 12 |
   | **Halbjährlicher Umrechnungsfaktor** | Der halbjährliche Umrechnungsfaktor für die Zahlungshäufigkeit. Zum Beispiel lautet der halbjährliche Umrechnungsfaktor für die monatliche Lohnzahlungshäufigkeit: </br></br>(12 monatliche Zahlungen/2mal im Jahr) = 6 |
   | **Vierteljährlicher Umrechnungsfaktor** | Der vierteljährliche Umrechnungsfaktor für die Zahlungshäufigkeit. Zum Beispiel lautet der vierteljährliche Umrechnungsfaktor für die monatliche Lohnzahlungshäufigkeit: </br></br>(12 monatliche Zahlungen/4 Quartale) = 3 |
   | **Monatlicher Umrechnungsfaktor** | Der monatliche Umrechnungsfaktor für die Zahlungshäufigkeit. Zum Beispiel lautet der monatliche Umrechnungsfaktor für die monatliche Lohnzahlungshäufigkeit: </br></br>(12 monatliche Zahlungen/12 Monate) = 1 |
   | **Halbmonatlicher Umrechnungsfaktor** | Der halbmonatliche Umrechnungsfaktor für die Zahlungshäufigkeit. Zum Beispiel lautet der halbmonatliche Umrechnungsfaktor für die monatliche Lohnzahlungshäufigkeit: </br></br>(12 monatliche Zahlungen /24 (2mal pro Monat)) = 0,5 | 
   | **Zweiwöchentlicher Umrechnungsfaktor** | Der jährliche Umrechnungsfaktor für die Zahlungshäufigkeit. Zum Beispiel lautet der jährliche Umrechnungsfaktor für die monatliche Lohnzahlungshäufigkeit: </br></br>(12 monatliche Zahlungen/26 Wochen) = 0,461538 |
   | **Wöchentlicher Umrechnungsfaktor** | Der jährliche Umrechnungsfaktor für die Zahlungshäufigkeit. Zum Beispiel lautet der jährliche Umrechnungsfaktor für die monatliche Lohnzahlungshäufigkeit: </br></br>(12 monatliche Zahlungen/52 Wochen) = 0,230769 |
   | **Täglicher Umrechnungsfaktor** | Der jährliche Umrechnungsfaktor für die Zahlungshäufigkeit. Zum Beispiel lautet der jährliche Umrechnungsfaktor für die monatliche Lohnzahlungshäufigkeit: </br></br>(12 monatliche Zahlungen/365 Tage) = 0,032877 |
   | **Stündlicher Umrechnungsfaktor** | Der jährliche Umrechnungsfaktor für die Zahlungshäufigkeit. Zum Beispiel lautet der jährliche Umrechnungsfaktor für die monatliche Lohnzahlungshäufigkeit: </br></br>(12 monatliche Zahlungen/2080 Stunden) = 0,005769

4. Wählen Sie **Speichern**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]