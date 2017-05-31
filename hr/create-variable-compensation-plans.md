---
title: "Erstellen von Plänen für variable Vergütung"
description: "Die variable Vergütung ist ein irregulärer Lohn eines Mitarbeiters, wie Prämien oder Bestandsprämien. In diesem Artikel werden die Komponenten beschrieben, die eingerichtet werden müssen, bevor Sie eine variable Vergütung erstellen und Mitarbeiter in einem variablen Vergütungsplan registrieren können."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 26ed9de01bffbcd468ac0cf1b9eb3f101707eb04
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="create-variable-compensation-plans"></a>Erstellen von Plänen für variable Vergütung

[!include[banner](includes/banner.md)]


Die variable Vergütung ist ein irregulärer Lohn eines Mitarbeiters, wie Prämien oder Bestandsprämien. In diesem Artikel werden die Komponenten beschrieben, die eingerichtet werden müssen, bevor Sie eine variable Vergütung erstellen und Mitarbeiter in einem variablen Vergütungsplan registrieren können.

Die Berechnung von Beträgen für variable Vergütung für Ihre Mitarbeiter kann auf verschiedenen Faktoren basieren, beispielsweise der Leistung des Mitarbeiters, der Vergütungsstufe des Mitarbeiters und der Leistung der Abteilung.

## <a name="variable-compensation-components"></a>Variable Vergütungskomponenten
### <a name="create-compensation-types"></a>Erstellen von Vergütungstypen

**Typen für variable Vergütung**sind eine erforderliche Komponente. Anhand der Typen für variable Vergütung können Sie die Arten der variablen Vergütung beschreiben, die Ihre Organisation gewährt. Sie können Sie auch angeben, ob die Vergütung in bar oder in nicht monetärer Form erfolgt (z. B. durch Bestand).

### <a name="describe-vesting-rules"></a>Beschreiben von Übertragungsregeln

Unternehmen können optionale **Übertragungsregeln** einrichten. Übertragungsregeln beschreiben, wie die variable Prämie im Zeitverlauf zugewiesen werden soll. Beispielsweise kann eine Übertragungsregel festhalten, dass der Mitarbeiter 25 Prozent der gesamt Prämie jedes Jahr für die folgenden vier Jahre erhält. Übertragungsregeln sind nur zur Information.

## <a name="variable-compensation-plans"></a>Pläne für variable Vergütung
Der **Plan für variable Vergütung** enthält die Regeln, Berechnungsmethoden und Standardwerte für die Berechnung der variablen Vergütung für registrierte Mitarbeiter. Wenn Sie einen variablen Vergütungsplan erstellen,  muss der Typ für variable Vergütung eingerichtet werden. Der Typ der variablen Vergütung bestimmt, ob das System einen Währungsbetrag oder mehrere Einheiten für die Berechnung der Prämie berechnet. Sie müssen auch die Berechnungsmethode festlegen:

-   **Zeitpunkt** – Die Berechnung für variable Prämien handelt auf Grundlage der festen Vergütung, die ein Mitarbeiter auf einem bestimmten Datum worden wäre. Dieses Datum wird im Feld Prozessereignis angegeben, wenn neue Kompensationsbeträge verarbeitet werden.
-   **Zusammengesetzt** – Für jeden eindeutigen Lohnsatz der festen Vergütung, der für den Mitarbeiter zwischen dem Anfangsdatum des Zyklus und dem Enddatum des Zyklus im Prozessereignis galt, wird ein Prämienbetrag berechnet. Die Zinssätze werden dann zusammen hinzugefügt, um die abschließende Prämie zu bestimmen. Zum Beispiel wen ein Mitarbeiter in eine andere Position mit einem anderen Lohnsatz wechselt, ändert der Zyklus In diesem Fall wird der variable Bonus für den Zeitraum angepasst, während dem der jeweilige Lohnsatz für den Mitarbeiter galt.

Der Betrag für variable Prämien kann entweder auf einem Prozentsatz des regulären Basiseinkommens des Mitarbeiters basieren oder auf einer festgelegten Anzahl von Einheiten.

-   Wählen Sie die Option **Prozentsatz des Basiswerts** aus, um einen Standardprozentsatz einzugeben, und geben Sie an, ob der feste Lohnsatz des Mitarbeiters oder der Kontrollpunkt für die Vergütungsstufe des Mitarbeiters als Grundlage dienen soll. Die Vergütungsstufe wird auf der Stufe des Mitarbeiters festgelegt. Einer der Referenzpunkte aus der Vergütungsstruktur kann als Kontrollpunkt im Plan für feste Vergütung eingerichtet werden. Das System verwendet die Vergütungsstufe der Stufe des Mitarbeiters und überprüft sie mit dem Kontrollpunkt, der im Plan für feste Vergütung des Mitarbeiters aufgeführt ist, um den Kontrollpunktbetrag der Vergütungsstufe des Mitarbeiters zu suchen. Der Kontrollpunktbetrag wird anschließend anstelle des festen Lohnsatzes des Mitarbeiters als Basis für die Prämie verwendet.
-   Wählen Sie die Option**Anzahl der Einheiten** aus, um eine Standardanzahl von Einheiten, den Wert der einzelnen Einheiten und die Währung für den Wert der Einheiten einzugeben, wenn der Vergütungsplan eine nicht monetäre Prämie vorsieht (beispielsweise 200 Einheiten des Bestands mit einem Wert von EUR 40 pro Einheit). Wenn es sich um einen Vergütungsplan für eine Bargeldprämie handelt, geben Sie hier einfach die Anzahl der Einheiten ein. Für eine Bargeldprämie erhält der Mitarbeiter die angegebene Anzahl von Einheiten der Währung, die für den Plan für feste Vergütung verwendet wird (z, 500 Einheiten von 1 EUR). Das 1:1-Beziehungs-Steuerelement kann verwendet werden, um anzugeben, ob es eine direkte eins-zu-eins Zuordnung zwischen der Anzahl der Einheiten und dem Einheitenwert gibt. Wenn Sie einen Plan für variable Vergütung für einen Bargeld-basierten Plan erstellen, indem Sie die Anzahl der Einheiten verwenden, ist diese Option automatisch gesperrt auf **Ja** und der Einheitswert ist **1.0000**.

Über die **Einstellungsregel**können Sie festlegen, ob alle Mitarbeiter unabhängig von ihrem Einstellungsdatum die gleiche Erhöhung erhalten sollen (**Einstellungsregel** = **Keine**), oder ob Mitarbeiter basierend auf der Länge ihrer Beschäftigungsdauer in diesem Zyklus einen Prozentsatz der Prämie erhalten sollen (**Einstellungsregel** = **Prozent**). 

Mi der **Hebelwirkung** können die Prämie eines Mitarbeiters, basierend auf der Leistung der Abteilung des Mitarbeiters erfolgen. Leistungskennzahlen können für jede Abteilung auf der Seite **Abteilung** unter **Zugehörige Formulare**  &gt; **Vergütung** &gt; **Leistung** festgelegt werden.. Die Prämie, die Mitarbeiter in dieser Abteilung erhalten, hängt vom Wert im Feld **Prozent der erzielten Zielvorgabe** ab, die Leistung der Abteilung angibt:

-   Wenn die Leistung der Abteilung 100 Prozent beträgt, wird die Prämie für die Mitarbeiter in dieser Abteilung über den Prozentsatz berechnet, der im Feld**Auszahlung bei 100 %** festgelegt wurde.
-   Wenn die Leistung der Abteilung 100 Prozent übersteigt, addiert das System den Prozentsatz, der im Feld **Pro 1 % über Zielvorgabe** festgelegt wurde, zu dem Prozentsatz hinzu, der im Feld **Auszahlung bei 100 %** angegeben ist, bis der Wert im Feld **Höchste zulässige Auszahlung** erreicht ist.
-   Wenn die Leistung der Abteilung unter 100 Prozent liegt, subtrahiert das System den Prozentsatz, der im Feld **Pro 1 % unter Ziel** festgelegt wurde, von dem Prozentsatz, der im Feld **Auszahlung bei 100 %** angegeben ist, bis der Wert im Feld **Geringste zulässige Auszahlung** erreicht ist.

Sie können**Toleranzstufen** für die Schwellenwertprozentsätze festlegen, damit eine Warnmeldung angezeigt wird, wenn die Hebelwirkung bewirkt, dass der Prozentsatz außerhalb des Schwellenwertprozentsatzes liegt. 

Standardmäßig sucht das System nach der Abteilung, die für die Position des Mitarbeiters festgelegt wird. Hängt jedoch möglicherweise die Zuerkennung für einige Mitarbeiter von der Leistung von mehreren Abteilungen ab.- In diesem Fall können die unterschiedlichen Abteilungen und der Prozentsatz der Prämie, der mit der Leistung der einzelnen Abteilungen verbunden ist, für die Registrierung für variable Vergütung des Mitarbeiters festgelegt werden. Weitere Informationen finden Sie im Abschnitt" Registrierungs für variable Vergütung". 

Die Hebelwirkung wird nur verwendet, wenn beim Ausführen des Vergütungsprozesses die Option **Leistungsbezogene Bezahlung** ausgewählt wird. 

Mit der Registerkarte **Ebenenaußerkraftsetzungen** können Sie den Standardprozentsatz oder die Anzahl Einheiten basierend auf der Grundlage der Vergütungsstufe des Mitarbeiters überschreiben. Wenn Sie **Ebenen überschreiben aktivieren** für Mitarbeiter, die im Plan für variable Vergütung registriert sind auf **Ja** festsetzen, nimmt das System Stufe der Stelle eines Mitarbeiters und sucht sie dann in der Ebenenaußerkraftsetzungstabelle, um den prozentualen Anteil oder die Anzahl der Einheiten für diese Ebene zu bestimmen. Wird die Ebene nicht in der Ebene der Außerkraftsetzungstabelle gefunden, wird der Standardprozentsatz oder die Anzahl der Einheiten von der Registerkarte **Allgemein** verwendet. Der Prozentsatz und die Anzahl von Einheiten können in der Registrierung des Mitarbeiters im Plan für variable Vergütung ebenfalls überschrieben werden.

## <a name="variable-compensation-enrollment"></a>Registrierung für variable Prämien
### <a name="determine-who-is-eligible-for-the-plan"></a>Bestimmen der Berechtigung für einen Plan

Wenn Sie Mitarbeiter für einen Plan für variable Vergütung registrieren möchten, müssen Sie als Erstes bestimmen, wer für die im Plan angegebene Vergütung berechtigt ist. Erst wenn Sie die Berechtigung bestimmt haben, können Sie Mitarbeitern den Plan zuweisen. Um die Berechtigung einzurichten, öffnen Sie die Seite **Berechtigungsregeln**. Hier erstellen Sie eine neue Berechtigungsregel für den Plan und legen die Kriterien fest, die ein Mitarbeiter erfüllen muss, um für den Vergütungsplan berechtigt zu sein. Sie können die Berechtigung nach Abteilung, Gewerkschaft, Vergütungsregion (Standort), Stelle, Stellenfunktion, Stellentyp oder Vergütungsstufe begrenzen. Mitarbeiter können nur für einen Vergütungsplan registriert werden, wenn sie **alle** Kriterien erfüllen, die über die Berechtigungsregel festgelegt wurden. 

**Hinweis:** Berechtigungsregeln bestimmen die Berechtigung sowohl für Pläne für eine feste Vergütung als auch für Pläne für eine variable Vergütung. Die Berechtigungsregeln verwenden die folgenden Felder für die Datensätze "Stelle", "Position" und "Mitarbeiter", um festzustellen, ob ein Mitarbeiter für einen Vergütungsplan berechtigt ist:

-   Auf der Seite **Stelle**:
    -   Feld **Stelle**
    -   Die Felder **Funktion** und **Stellentyp** auf der Registerkarte **Stellenklassifizierung**
    -   Das Feld **Ebene** auf der Registerkarte **Vergütung**
-   Auf der Seite **Positionen**: Die Felder **Abteilung** und **Vergütungsregion**
-   Auf der Seite **Mitarbeiter**: Die Angaben zu Gewerkschaften, die für diesen Mitarbeiter gelten, unter **Persönliche Informationen** &gt; **Gewerkschaften** auf der Registerkarte ****Arbeitskraft****.

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Aktivieren der Registrierung für den Plan für variable Vergütung

Legen Sie auf der Seite **Pläne für variable Vergütung** die Option **Registrierung aktivieren** auf **Ja** fest, damit berechtigte Mitarbeiter im Plan registriert werden können.

### <a name="enroll-the-employee"></a>Registrieren des Mitarbeiters

Nun können Sie Mitarbeiter in einem Plan für variable Vergütung registrieren. Um einen Mitarbeiter zu registrieren, wählen Sie auf der Seite **Mitarbeiter** den Mitarbeiter aus. Klicken Sie anschließend im Aktivitätsbereich auf **Vergütung**&gt; **Variable Planregistrierung**. 

**Hinweis:** **Registrierung** muss für den Plan für variable Vergütung auf **Ja** festgelegt werden. Das Feld **Plan** zeigt nur den Vergütungspläne, für die ein Mitarbeiter laut den Berechtigungsregeln berechtigt ist, und die für den jeweiligen Plan eingerichtet wurden. Wenn für einen Plan keine Berechtigungsregel eingerichtet wurde, sind keine Mitarbeiter für diesen Plan berechtigt. 

Stellen Sie sicher, dass das Feld **Effektives Datum** korrekt festgelegt ist. Stellen Sie sicher, dass das Feld Gültigkeitsdatum die **zusammengesetzte** Berechnungsmethode  verwendet. Das effektive Gültigkeitsdatum der Registrierung wird möglicherweise bei der Berechnung der Prämie für den Mitarbeiter berücksichtigt. 

Sie können die Registerkarte **Überschreibung** verwenden, um bestimmte Werte für den Mitarbeiter zu überschreiben. Wenn beispielsweise **Einstellungsregel** **Prozent** auf den Vergütungsplan festgelegt wird, und ein anderes Einstellungsdatum sollte bei der Berechnung des Prozentsatzes des Mitarbeiters verwendet werden können Sie das Einstellungsatum im Feld **Einstellungsdatum** definieren. Sie können entweder den **Prämienprozent**-Wert oder die **Anzahl der Einheiten** für einen bestimmten Mitarbeiter, abhängig von den Planeinstellungen überschreiben. Diese Werte werden immer noch durch die Einstellungsregel, die Leistungsfaktoren und andere Einstellungen für den Plan berücksichtigt. 

**Organisatorische Überschreibungen** werden verwendet, um die Prämie eines Mitarbeiters auf die Leistung einer oder mehreren Abteilungen zu basieren. Der Prozentsatz, der über die Abteilungen hinweg zugewiesen wird, sollte insgesamt 100 Prozent betragen. Die Einzelleistung des Mitarbeiters wird auch berücksichtigt. Diese Einstellungen werden nur verwendet, wenn beim Ausführen des Vergütungsprozesses die Option **Leistungsbezogene Bezahlung** ausgewählt wird.

<a name="see-also"></a>Siehe auch
--------

[Vergütungspläne](compensation-plans.md)




