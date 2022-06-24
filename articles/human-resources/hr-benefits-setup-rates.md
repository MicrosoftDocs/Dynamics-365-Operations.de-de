---
title: Sätze konfigurieren
description: Sätze in Microsoft Dynamics 365 Human Resources definieren, wie viel Arbeitgeber und Mitarbeiter für einen Vorteil beitragen.
author: twheeloc
ms.date: 08/25/2021
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
ms.openlocfilehash: 039b4aa3f044cda29944bcd4f5c42fc35818c58b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868158"
---
# <a name="configure-rates"></a>Sätze konfigurieren


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sätze definieren, wie viel Arbeitgeber und Mitarbeiter für einen Vorteil beitragen. Der Wert kann abhängig von Ihrer Konfiguration ein Betrag oder eine Zahl sein.

Bestimmen Sie mithilfe der Sätze, wie viel Arbeitnehmer und Mitarbeiter basierend auf mehreren Faktoren für jeden Vorteil zahlen. Deckungssätze haben ein Gültigkeitsdatum, deshalb können Sie einen historischen Datensatz für die Sätze führen. 

## <a name="set-up-rates"></a>Sätze einrichten

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellungen** die Option **Sätze** aus.

2. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Satz** | Ein eindeutiger Name, der den Vergütungssatz identifiziert. |
   | **Beschreibung** | Eine Beschreibung des Vergütungssatzes. |
   | **In Kraft** | Das Datum, an dem dieser Satz wirksam wird. Das aktuelle Systemdatum ist der Standardwert. Dieses Datum sollte auf oder vor Ihrem Leistungszeitraum liegen. Es empfiehlt sich, dieses Datum auf das Datum des Leistungsplans zu setzen. |
   | **Ablaufdatum** | Das Enddatum des Satzes. Der Standardwert lautet 12/31/2154 (stellvertretend für nie). |
   | **Ebenen verwenden** |  Verwenden Sie dieses Feld, wenn Sie über eine Logik verfügen, die verwendet werden muss, um einen Tarif zu bestimmen. Wenn ein Satz beispielsweise aufgrund des Alters steigen muss, wählen Sie hier einen Wert aus. Für den Vergütungssatz kann entweder eine **einfache** oder eine **zweifache Stufe** verwendet werden. Ein Beispiel für eine zweifache Stufe ist eine Stufe, die auf Geschlecht und Alter basiert. Nachdem Sie einen Wert ausgewählt haben, wählen Sie **Aktionen**, und wählen Sie dann **Stufensatz**. Wenn Sie eine Pauschale haben, die sich nicht ändert, lassen Sie dieses Feld leer. |
   | **Zahlungshäufigkeit** | Geben Sie an, wie oft der Leistungsprämiensatz an den Leistungserbringer gezahlt werden soll. Die Preise, die Sie auf der Seite eingeben, die weiter unten in diesem Artikel beschrieben wird, basieren auf der hier angegebenen Zahlungshäufigkeit. Wenn Sie beispielsweise in dieses Feld **Monatlich** eingeben und Sie geben einen Mitarbeitersatz von **$100** eib, wird davon ausgegangen, dass die Leistung den Mitarbeiter $100 pro Monat kostet. Ein Mitarbeiter kann jedoch zweimal pro Monat bezahlt werden, basierend auf der Häufigkeit der Leistungszahlung, die im Mitarbeiterdatensatz festgelegt ist. Wenn sich der Mitarbeiter in diesem Fall beim **Mitarbeiter-Selbstservice** anmeldet, beträgt der Betrag, den er zahlt, $50, da der Tarif, den der **Mitarbeiter-Selbstservice** anzeigt, auf der Zahlungshäufigkeit des Mitarbeiters basiert. |
   | **Rundung des Zahlungshäufigkeitssatzes** | Die Methoden zur Rundung des Satzes sind: Standard, Abgeschnitten, Normal, Abwärts und Aufrunden. </br></br><ul><li>**Standard** – Rundet immer auf. Zum Beispiel wird 10,611 auf 10,62 gerundet. -10,231 rundet auf -10,23. </li><li>**Abgeschnitten** – Rundet immer ab. Beispiel: 10,619 rundet auf 10,61. -10,231 rundet auf -10,24. </li><li>**Normal** – Dezimalwerte, die auf oder größer als 5 enden, werden von Null abgerundet. Dezimalwerte, die auf oder kleiner als 4 enden, werden gegen Null gerundet. Beispiel: 10,615 wird auf 10,62 gerundet. -10,235 rundet auf -10,24. 10,614 rundet auf 10,61. -10,234 rundet auf -10,23. </li><li>**Abwärts** – Rundet gegen Null. Beispiel: 10,619 rundet auf 10,61. -10,231 rundet auf -10,23. </li><li>**Aufrunden** – Rundet weg von Null. Zum Beispiel wird 10,619 auf 10,62 gerundet. -10,231 rundet auf -10,24. |
   | **Mitarbeiterbetrag für Nichtraucher** | Der Betrag, den der Vorteilsanbieter für einen nicht rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Arbeitgeberbetrag für Nichtraucher** | Der Betrag, den der Vorteilsanbieter für einen nicht rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Mitarbeiterbetrag für Raucher** | Der Betrag, den der Vorteilsanbieter für einen rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Arbeitgeberbetrag für Raucher** | Der Betrag, den der Vorteilsanbieter für einen rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Verwaltungsbetrag** | Der von einem Drittanbieteradministrator in Rechnung gestellte Verwaltungsbetrag. Dies ist der Betrag, den der Arbeitgeber an den Drittanbieteradministrator zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Flexibler Gutschriftensatz** | Die Höhe des Flexguthabens, den der Vorteil kostet. Dies gilt nur für Sätze, die für Vergütungspläne gelten, die mit Flexguthabenprogrammen verbunden sind. Wenn Sie Stufensätze verwenden, wird der Flexguthabensatz unter Aktionen > Stufensätze definiert. |
   | **Gültigkeitsdatum ändern** | Das Datum, an dem der Vergütungssatz wirksam wird. Das System ändert automatisch den Vergütungssatz und aktualisiert alle Vergütungspläne, die mit diesem Satz verbunden sind, sofern Sie die Verarbeitung von aktualisierten Satzänderungen ausführen. Sie sollten dieses Datum nicht festlegen, es sei denn, Sie möchten, dass das System die Personalvergütungspläne basierend auf diesem Satz automatisch aktualisiert. Das ist normalerweise der automatischen Verarbeitung zukünftiger Änderungen des Vergütungssatzes vorbehalten. Das **Datum des Inkrafttretens der Änderung** muss innerhalb des Datums des Inkrafttretens und des Ablaufs des Vergütungssatzes liegen. |
   | **Satzänderung abgeschlossen** | Das Kontrollkästchen **Satzänderung abgeschlossen** wird automatisch aktiviert, nachdem die Änderungen des Satzes durch die Verarbeitung von aktualisierten Satzänderungen abgeschlossen wurden. |

4. Um Änderungen an der Vorteilssatzeinstellung zu verfolgen und beizubehalten, wählen Sie **Aktionen** und dann **Versionen verwalten** aus.

5. Wählen Sie **Speichern**. 

## <a name="set-up-tier-rates"></a>Stufensätze einrichten

Sie können Stufensätze in Ihrer Vergütungssatzeinstellung verwenden, wenn der Satz abhängig von verschiedenen Faktoren variiert. Sie können die Stufensätze beispielsweise so konfigurieren, dass der Nichtraucherbetrag bis zu einem Alter von 34,99 Jahren 2 beträgt. Bis zu einem Alter von 39,99 Jahren beträgt der Nichtraucherbetrag 3.

Sie können auch doppelte Stufen verwenden. Wenn Sie **Zweifache Stufe** für den Wert **Stufen verwenden** im Formular **Vergütungssatzeinstellung** auswählen, können Sie Sätze definieren, die auf zwei Dimensionen basieren. Sie können ein zweistufiges System beispielsweise so konfigurieren, dass der Nichtraucherbetrag für Männer bis zu einem Alter von 34,99 Jahren 2 beträgt. Wenn Sie ein Mann sind, gilt bis zu einem Alter von 39,99 Jahren ein Nichtraucherbetrag von 3. Wenn Sie eine Frau sind, gilt bis zu einem Alter von 34,99 Jahren ein Nichtraucherbetrag von 1,8. Wenn Sie eine Frau sind, gilt bis zu einem Alter von 39,99 Jahren ein Nichtraucherbetrag von 2,8.

> [!IMPORTANT]
> In der Arbeitskraftakte gibt es unter **Persönliche Angaben** eine Option, mit der angegeben wird, ob der Mitarbeiter Raucher ist. Wenn der Mitarbeiter als Raucher registriert ist, wird der Rauchertarif verwendet. (Der Raucherhinweis wird dem Mitarbeiter nie angezeigt.)
   
1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellungen** die Option **Sätze** aus.

2. Wählen Sie zuerst einen oder mehrere Sätze aus der Liste aus. Anschließend wählen Sie **Aktionen** und dann **Stufensätze** aus.

3. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- | 
   | **Beschreibung** | Der Wert im Feld **Beschreibung** wird aus der Beschreibung im Datensatz der Vergütungssatzeinstellung übernommen. Auf diese Weise können Sie ermitteln, mit welcher Vergütungssatzeinstellung die Stufensätze verknüpft sind. |
   | **Stufencode** | Wählen Sie einen Stufencode aus. Stufencodes werden im Formular **Stufencodes** definiert. Das System zeigt automatisch die Beschreibung des Stufencodes im Raster auf der linken Seite an. |
   | **Stufentyp** | Gibt an, welches Feld als Auswahlkriterium für die Berechnung des Stufensatzes verwendet werden soll. Beispiel:</br></br><ul><li>Wenn die Option **Alter** verwendet wird, verwendet das System bei der Berechnung des Vergütungssatzes das Geburtsdatum des Mitarbeiters.</li><li>Wenn die Option **Gehalt** verwendet wird, verwendet das System bei der Berechnung des Vergütungssatzes das jährliche Vorteilsgehalt des Mitarbeiters.</li><li>Wenn die Option **Stellentyp** verwendet wird, wird der aktuelle aktive Positionsdatensatz des Mitarbeiters verwendet, um den Stellentyp anhand des mit der Position verknüpften Stellendatensatzes zu ermitteln.</li></ul></br></br>Die Stufentypen sind **Alter**, **Gehalt**, **Physisch**, **Geschlecht**, **Vollzeitäquivalent**, **Stellentyp**, **Kompensationsregion** und **Ebene**. | 
   | **Stufe** | Der Wert, der zusammen mit dem Stufentyp bei der Berechnung des Vergütungssatzes verwendet werden soll. Beispiel:</br></br><ul><li>Für den Stufentyp **Alter** wäre das der Alterswert.</li><li>Für den Stufentyp **Gehalt** wäre das der Gehaltswert.</li><li> Für den Stufentyp **Stellentyp** wäre das der Stellentyp.</li></ul></br></br>Für den Stufentyp **Alter** oder **Gehalt** gibt der Wert im Feld **Ebene** die obere Grenze der Stufe an. Für den Stufentyp **Stellentyp** wird bei der Stufensatzauswahl ein Ansatz mit genauer Übereinstimmung verwendet. |
   | **Berechnungstyp** | Gibt an, wie der Betrag im Feld mit dem Berechnungsbetrag verwendet wird und welche mathematischen Berechnungen bei Bedarf durchgeführt werden sollen. Handelt es sich beim Berechnungstyp um einen Pauschalbetrag, werden die Betragsfelder ohne Änderung verwendet. Ist der Berechnungstyp ein prozentualer Betrag des Gehalts oder der Deckung, werden in der mathematischen Berechnung der Berechnungsbetrag und die Berechnungsrichtung verwendet.</br></br>Ist der Berechnungstyp ein prozentualer Betrag des Gehalts, wird die folgende mathematische Gleichung verwendet:</br></br>Jährliches Vorteilsgehalt geteilt durch den Berechnungsbetrag (auf- oder abgerundet) multipliziert mit den Beträgen für Raucher oder Nichtraucher für Mitarbeiter oder Arbeitgeber.</br></br>Ist der Berechnungstyp ein prozentualer Betrag der Abdeckungssumme, wird die folgende mathematische Gleichung verwendet:</br></br>Deckungsbetrag geteilt durch den Berechnungsbetrag (auf- oder abgerundet) multipliziert mit den Beträgen für Raucher oder Nichtraucher für Mitarbeiter oder Arbeitgeber.</br></br>In beiden Berechnungen wird anhand der Berechnungsrichtung bestimmt, ob das jährliche Vorteilsgehalt oder der Deckungsbetrag durch den Berechnungsbetrag auf- oder abgerundet werden sollen. |
   | **Berechneter Betrag** | Der Betrag, der bei der Berechnung des Vergütungssatzes verwendet werden soll. Dieser Betrag wird der Teiler bei der mathematischen Berechnung des Stufensatzes sein. |
   | **Berechnungsrichtung** | Die Richtung, in die der berechnete Ergebnisbetrag gerundet werden soll. Das System unterstützt drei Berechnungsrichtungen: „Leer“ (genaue Methode), **Erhöhen** und **Verringern**.</br></br><ul><li>Für „Leer“ verwendet das System die exakte Berechnung des Gehalts-/Deckungsbetrags geteilt durch den Berechnungsbetrag. Weist dieser Wert einen Bruch auf, wird dieser in der Berechnung verwendet.</li><li>Für **Erhöhen** erhöht die mathematische Berechnung den Gehalts-/Deckungsbetrag geteilt durch den Berechnungsbetrag auf die nächste Ganzzahl. Das bedeutet, dass 12,25 auf 13 aufgerundet wird.</li><li>Für **Verringern** verringert die mathematische Berechnung den Gehalts-/Deckungsbetrags geteilt durch den Berechnungsbetrag auf die aktuelle Ganzzahl. Das bedeutet, dass 12,25 auf 12 abgerundet wird.</li></ul> |
   | **Mitarbeiterbetrag für Nichtraucher** | Der Betrag, den ein Vorteilsanbieter für einen nicht rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Arbeitgeberbetrag für Nichtraucher** | Der Betrag, den ein Vorteilsanbieter für einen nicht rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Mitarbeiterbetrag für Raucher** | Der Betrag, den ein Vorteilsanbieter für einen nicht rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Arbeitgeberbetrag für Raucher** | Der Betrag, den ein Vorteilsanbieter für einen nicht rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Verwaltungsbetrag** | Der von einem Drittanbieteradministrator in Rechnung gestellte Verwaltungsbetrag. Dies ist der Betrag, den der Arbeitgeber an den Drittanbieteradministrator zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Nichtrauchersatz für Flexguthaben** | Die Höhe des Flexguthabens, den der Vorteil kostet, basierend auf der Berechnung, die für die Stufenebene für Nichtraucher definiert wurde. Wenn der Berechnungstyp beispielsweise **Pro-Dollar-Betrag der Deckung** lautet, der Berechnungsbetrag 10.000 beträgt und der Nichtrauchersatz für Flexguthaben 6, bedeutet dies, dass es 6 Punkte des Flexguthabens kostet, wenn ein nicht rauchender Mitarbeiter eine Deckungssumme von 10.000 US-Dollar auswählt. Für eine Deckung in Höhe von 20.000 US-Dollar entstehend dann Kosten in Höhe von 12 Punkten des Flexguthabens usw. |
   | **Rauchersatz für Flexguthaben** | Die Höhe des Flexguthabens, den der Vorteil kostet, basierend auf der Berechnung, die für die Stufenebene für Raucher definiert wurde. |

5. Wählen Sie **Speichern**. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
