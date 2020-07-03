---
title: Sätze konfigurieren
description: Sätze in Microsoft Dynamics 365 Human Resources definieren, wie viel Arbeitgeber und Mitarbeiter für einen Vorteil beitragen.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: c90a45b79f2a383f0ace0cb07e791f6613d7a3c3
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429910"
---
# <a name="configure-rates"></a>Sätze konfigurieren

Sätze in Microsoft Dynamics 365 Human Resources definieren, wie viel Arbeitgeber und Mitarbeiter für einen Vorteil beitragen. Der Wert kann abhängig von Ihrer Konfiguration ein Betrag oder ein Flexguthaben sein.

Bestimmen Sie mithilfe der Sätze, wie viel Arbeitnehmer und Mitarbeiter basierend auf mehreren Faktoren für jeden Vorteil zahlen. Deckungssätze haben ein Gültigkeitsdatum, deshalb können Sie einen historischen Datensatz für die Sätze führen. 

## <a name="set-up-rates"></a>Sätze einrichten

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellungen** die Option **Sätze** aus.

2. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Satz** | Ein eindeutiger Name, der den Vergütungssatz identifiziert. |
   | **Beschreibung** | Eine Beschreibung des Vergütungssatzes. |
   | **Gültig** | Das Datum, an dem der Satz gültig ist. Das aktuelle Systemdatum ist der Standardwert. 
   | **Ablaufdatum** | Das Enddatum des Satzes. Der Standardwert lautet 12/31/2154 (stellvertretend für nie). |
   | **Ebenen verwenden** | Die Stufe, die zur Berechnung des Vergütungssatzes verwendet werden soll. Für den Vergütungssatz kann entweder eine einfache oder eine zweifache Stufe verwendet werden. Ein Beispiel für eine zweifache Stufe ist eine Stufe, die auf Geschlecht und Alter basiert. |
   | **Zahlungshäufigkeit** | Die Zahlungshäufigkeit bestimmt, wie oft der Vergütungsprämiensatz an den Vorteilsanbieter ausgezahlt wird. Wenn die Auszahlung beispielsweise monatlich erfolgt, entspricht der Vergütungssatz dem monatlichen Zahlungsbetrag. |
   | **Rundung des Zahlungshäufigkeitssatzes** | Die Methode zum Runden des Satzes: Standard oder Gekürzt. |
   | **Mitarbeiterbetrag für Nichtraucher** | Der Betrag, den der Vorteilsanbieter für einen nicht rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Arbeitgeberbetrag für Nichtraucher** | Der Betrag, den der Vorteilsanbieter für einen nicht rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Mitarbeiterbetrag für Raucher** | Der Betrag, den der Vorteilsanbieter für einen rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Arbeitgeberbetrag für Raucher** | Der Betrag, den der Vorteilsanbieter für einen rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Verwaltungsbetrag** | Der von einem Drittanbieteradministrator in Rechnung gestellte Verwaltungsbetrag. Dies ist der Betrag, den der Arbeitgeber an den Drittanbieteradministrator zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Flexibler Gutschriftensatz** | Die Höhe des Flexguthabens, den der Vorteil kostet. Dies gilt nur für Sätze, die für Vergütungspläne gelten, die mit Flexguthabenprogrammen verbunden sind. Wenn Sie Stufensätze verwenden, wird der Flexguthabensatz unter Aktionen > Stufensätze definiert. |
   | **Gültigkeitsdatum ändern** | Das Datum, an dem der Vergütungssatz wirksam wird. Das System ändert automatisch den Vergütungssatz und aktualisiert alle Vergütungspläne, die mit diesem Satz verbunden sind, solange Sie die Verarbeitung von aktualisierten Satzänderungen ausführen. Sie sollten dieses Datum nicht festlegen, es sei denn, Sie möchten, dass das System die Personalvergütungspläne basierend auf diesem Satz automatisch aktualisiert. Das ist normalerweise der automatischen Verarbeitung zukünftiger Änderungen des Vergütungssatzes vorbehalten. Das Datum des Inkrafttretens der Änderung muss innerhalb des Datums des Inkrafttretens und des Ablaufs des Vergütungssatzes liegen. |
   | **Satzänderung abgeschlossen** | Das Kontrollkästchen **Satzänderung abgeschlossen** wird automatisch aktiviert, nachdem die Änderungen des Satzes durch die Verarbeitung von aktualisierten Satzänderungen abgeschlossen wurden. |

4. Um Änderungen an der Vorteilssatzeinstellung zu verfolgen und beizubehalten, wählen Sie **Aktionen** und dann **Versionen verwalten** aus.

5. Wählen Sie **Speichern**. 

## <a name="set-up-tier-rates"></a>Stufensätze einrichten

Sie können Stufensätze in Ihrer Vergütungssatzeinstellung verwenden, wenn der Satz abhängig von verschiedenen Faktoren variiert. Sie können die Stufensätze beispielsweise so konfigurieren, dass der Nichtraucherbetrag bis zu einem Alter von 34,99 Jahren 2 beträgt. Bis zu einem Alter von 39,99 Jahren beträgt der Nichtraucherbetrag 3.

Sie können auch doppelte Stufen verwenden. Wenn Sie **Zweifache Stufe** für den Wert **Stufen verwenden** im Formular **Vergütungssatzeinstellung** auswählen, können Sie Sätze definieren, die auf zwei Dimensionen basieren. Sie können ein zweistufiges System beispielsweise so konfigurieren, dass der Nichtraucherbetrag für Männer bis zu einem Alter von 34,99 Jahren 2 beträgt. Wenn Sie ein Mann sind, gilt bis zu einem Alter von 39,99 Jahren ein Nichtraucherbetrag von 3. Wenn Sie eine Frau sind, gilt bis zu einem Alter von 34,99 Jahren ein Nichtraucherbetrag von 1,8. Wenn Sie eine Frau sind, gilt bis zu einem Alter von 39,99 Jahren ein Nichtraucherbetrag von 2,8.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellungen** die Option **Sätze** aus.

2. Wählen Sie zuerst einen oder mehrere Sätze aus der Liste aus. Anschließend wählen Sie **Aktionen** und dann **Stufensätze** aus.

3. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- | 
   | **Beschreibung** | Der Wert im Beschreibungsfeld wird aus der Beschreibung im Datensatz der Vergütungssatzeinstellung übernommen. Auf diese Weise können Sie ermitteln, mit welcher Vergütungssatzeinstellung die Stufensätze verknüpft sind. |
   | **Stufencode** | Wählen Sie einen Stufencode aus. Stufencodes werden im Formular „Stufencodes“ definiert. Das System zeigt automatisch die Beschreibung des Stufencodes im Raster auf der linken Seite an. |
   | **Stufentyp** | Gibt an, welches Feld als Auswahlkriterium für die Berechnung des Stufensatzes verwendet werden soll. Beispiel:</br></br><ul><li>Wenn das Alter verwendet wird, verwendet das System bei der Berechnung des Vergütungssatzes das Geburtsdatum des Mitarbeiters.</li><li>Wenn das Gehalt verwendet wird, verwendet das System bei der Berechnung des Vergütungssatzes das jährliche Vorteilsgehalt des Mitarbeiters.</li><li>Wenn der Stellentyp verwendet wird, ermittelt das System anhand des aktuellen aktiven Positionsdatensatzes des Mitarbeiters den Stellentyp anhand des mit der Position verknüpften Stellendatensatzes.</li></ul></br></br>Die Stufentypen sind „Alter“, „Gehalt“, „Physisch“, „Geschlecht“, „Vollzeitäquivalent“, „Stellentyp“, „Kompensationsregion“ und „Ebene“. | 
   | **Stufe** | Der Wert, der zusammen mit dem Stufentyp bei der Berechnung des Vergütungssatzes verwendet werden soll. Beispiel:</br></br><ul><li>Für den Stufentyp „Alter“ wäre das der Alterswert.</li><li>Für den Stufentyp „Gehalt“ wäre das der Gehaltswert.</li><li> Für den Stufentyp „Stellentyp“ wäre das der Stellentyp.</li></ul></br></br>Bei einem Stufentyp „Alter“ oder „Gehalt“ verwendet das System bei der Stufensatzauswahl einen aufsteigenden Ansatz, d. h., dass der Wert im Feld „Ebene“ die Untergrenze der Stufe angibt. Bei einem Stufentyp „Stellentyp“ verwendet das System bei der Stufensatzauswahl einen Ansatz mit genauer Übereinstimmung. |
   | **Berechnungstyp** | Gibt an, wie der Betrag im Feld mit dem Berechnungsbetrag verwendet wird und welche mathematischen Berechnungen bei Bedarf durchgeführt werden sollen. Handelt es sich beim Berechnungstyp um einen Pauschalbetrag, verwendet das System die Betragsfelder ohne Änderung. Ist der Berechnungstyp ein prozentualer Betrag des Gehalts oder der Deckung, verwendet das System in der mathematischen Berechnung den Berechnungsbetrag und die Berechnungsrichtung.</br></br>Ist der Berechnungstyp ein prozentualer Betrag des Gehalts, verwendet das System die folgende mathematische Gleichung:</br></br>Jährliches Vorteilsgehalt geteilt durch den Berechnungsbetrag (auf- oder abgerundet) multipliziert mit den Beträgen für Raucher oder Nichtraucher für Mitarbeiter oder Arbeitgeber.</br></br>Ist der Berechnungstyp ein prozentualer Betrag der Deckung, verwendet das System die folgende mathematische Gleichung:</br></br>Deckungsbetrag geteilt durch den Berechnungsbetrag (auf- oder abgerundet) multipliziert mit den Beträgen für Raucher oder Nichtraucher für Mitarbeiter oder Arbeitgeber.</br></br>In beiden Berechnungen wird anhand der Berechnungsrichtung bestimmt, ob das jährliche Vorteilsgehalt oder der Deckungsbetrag durch den Berechnungsbetrag auf- oder abgerundet werden sollen. |
   | **Berechneter Betrag** | Der Betrag, der bei der Berechnung des Vergütungssatzes verwendet werden soll. Dieser Betrag wird der Teiler bei der mathematischen Berechnung des Stufensatzes sein. |
   | **Berechnungsrichtung** | Die Richtung (Erhöhen oder Verringern), in die der berechnete Ergebnisbetrag gerundet werden soll. Das System unterstützt drei Berechnungsrichtungen: „Leer“ (genaue Methode), „Erhöhen“ und „Verringern“.</br></br><ul><li>Für „Leer“ verwendet das System die exakte Berechnung des Gehalts-/Deckungsbetrags geteilt durch den Berechnungsbetrag. Weist dieser Wert einen Bruch auf, verwendet das System diesen in der Berechnung.</li><li>Für „Erhöhen“ erhöht das System die mathematische Berechnung des Gehalts-/Deckungsbetrags geteilt durch den Berechnungsbetrag auf die nächste Ganzzahl. Das bedeutet, dass 12,25 auf 13 aufgerundet wird.</li><li>Für „Verringern“ verringert das System die mathematische Berechnung des Gehalts-/Deckungsbetrags geteilt durch den Berechnungsbetrag auf die aktuelle Ganzzahl. Das bedeutet, dass 12,25 auf 12 abgerundet wird.</li></ul> |
   | **Mitarbeiterbetrag für Nichtraucher** | Der Betrag, den ein Vorteilsanbieter für einen nicht rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Arbeitgeberbetrag für Nichtraucher** | Der Betrag, den ein Vorteilsanbieter für einen nicht rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Mitarbeiterbetrag für Raucher** | Der Betrag, den ein Vorteilsanbieter für einen nicht rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Arbeitgeberbetrag für Raucher** | Der Betrag, den ein Vorteilsanbieter für einen nicht rauchenden Mitarbeiter berechnet. Dies ist der Betrag, den der Arbeitgeber an den Vorteilsanbieter zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Verwaltungsbetrag** | Der von einem Drittanbieteradministrator in Rechnung gestellte Verwaltungsbetrag. Dies ist der Betrag, den der Arbeitgeber an den Drittanbieteradministrator zahlt und der auf der Zahlungshäufigkeit für die Vergütungssatzeinstellung basieren sollte. |
   | **Nichtrauchersatz für Flexguthaben** | Die Höhe des Flexguthabens, den der Vorteil kostet, basierend auf der Berechnung, die für die Stufenebene für Nichtraucher definiert wurde. Wenn der Berechnungstyp beispielsweise **Pro-Dollar-Betrag der Deckung** lautet, der Berechnungsbetrag 10.000 beträgt und der Nichtrauchersatz für Flexguthaben 6, bedeutet dies, dass es 6 Punkte des Flexguthabens kostet, wenn ein nicht rauchender Mitarbeiter eine Deckungssumme von 10.000 US-Dollar auswählt. Für eine Deckung in Höhe von 20.000 US-Dollar entstehend dann Kosten in Höhe von 12 Punkten des Flexguthabens usw. |
   | **Rauchersatz für Flexguthaben** | Die Höhe des Flexguthabens, den der Vorteil kostet, basierend auf der Berechnung, die für die Stufenebene für Raucher definiert wurde. |

5. Wählen Sie **Speichern**. 
