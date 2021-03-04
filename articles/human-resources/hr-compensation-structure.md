---
title: Entwicklung einer Vergütungsstruktur
description: Dieser Artikel führt Sie durch die Erstellung eines festen Vergütungsplans und die Anmeldung von Mitarbeitern in den Plan durch die Regeln für die Anspruchsberechtigung.
author: andreabichsel
manager: AnnBe
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 124d0f7f83feebabf622f00732c25bfa0f6eccdd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418704"
---
# <a name="develop-a-compensation-structure"></a>Entwicklung einer Vergütungsstruktur

Dieser Artikel führt Sie durch die Erstellung eines festen Vergütungsplans und die Anmeldung von Mitarbeitern in den Plan durch die Regeln für die Anspruchsberechtigung. Dieser Artikel verwendet die USMF-Demodaten und gilt für Vergütungs- und Leistungsmanager.

## <a name="create-a-fixed-compensation-plan"></a>Erstellen eines festen Vergütungsplans

1. Wählen Sie **Vergütungsmanagement**.

2. Wählen Sie **Feste Vergütungspläne**.

3. Wählen Sie **Neu** aus.

4. Geben Sie in das Feld **Plan** einen Wert ein.

5. Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.

6. Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.

7. Wählen Sie im Feld **Typ** aus, ob es sich bei dem festen Vergütungsplan um einen Plan **Band**, **Grad** oder **Schritt** handelt.

8. Das Ankreuzfeld **Empfehlung erlaubt** dient als Standardwert für alle Maßnahmen, die diesem Plan in einem Prozessereignis hinzugefügt werden. Das Zulassen von Empfehlungen bietet Ihnen die Möglichkeit, den berechneten Richtbetrag zu überschreiben, wenn die Vergütung verarbeitet wird.

9. Mit dem Feld **Bereichstoleranz außerhalb des Bereichs** können Sie angeben, wie Sie Vergütungsbeträge behandeln wollen, die außerhalb des für die gegebene Ebene angegebenen Bereichs der Vergütungsstruktur liegen. Wenn Sie das Feld **Bereichstoleranz außerhalb des Bereichs** auf **Keine** setzen, können Sie jeden beliebigen Vergütungsbetrag verwenden. **Weiche Toleranz** warnt die Benutzer, wenn der Ausgleichsbetrag unter dem Minimum oder über den maximalen Bezugspunktbeträgen für diese Ebene liegt. Benutzer können die Warnung ignorieren und fortfahren. **Harte Toleranz** erzeugt einen Fehler, wenn die Vergütung eines Mitarbeiters außerhalb des minimalen und maximalen Bezugspunktbetrags für diese Stufe liegt, und passt die Vergütung des Mitarbeiters automatisch so an, dass sie in den Bereich fällt.

10. Das Feld **Einstellungsregel** berechnet die Vergütung eines Mitarbeiters während eines Prozessereignisses. Das Feld **Einstellungsregel** von **Prozent** berechnet eine Erhöhung, die anteilig für die Dauer der Beschäftigung des Mitarbeiters in dem Zyklus berechnet wird.

11. Geben Sie im Feld **Währung** einen Wert ein.

12. Geben Sie in das Feld **Lohnratenumwandlung** einen Wert ein oder wählen Sie einen Wert aus.

13. Erweitern Sie den Abschnitt **Bereichsausnutzungsmatrix**. Fügen Sie optional Bereichsauslastungsdatensätze hinzu, damit Mitarbeiter schneller zu ihrem Mittelwert gelangen und langsamer den Maximalwert ihres Bereichs erreichen.

14. Wählen Sie **Speichern**. Dadurch wird die Drucktaste **Vergütung** eingerichtet und Sie können mit der Definition Ihrer Vergütungsstruktur für den Plan fortfahren.

15. Wählen Sie **Vergütung einrichten**. Sie können eine Vergütungsstruktur mit einer dieser drei Methoden anlegen:

    - Erstellen Sie eine völlig neue Struktur, indem Sie eine Reihe von Bezugspunkten auswählen und die Ebenen hinzufügen, um Ihre eigene Struktur zu erstellen.
    - Kopieren Sie eine Vergütungsstruktur aus einem bestehenden Plan als Ausgangspunkt und ändern Sie sie für den neuen Plan.
    - Wählen Sie ein bestehendes Vergütungsraster aus. Wenn ein anderer Plan bereits das Vergütungsgitter verwendet, spiegelt der andere Plan ebenfalls alle Änderungen wider, die Sie am Gitter vornehmen.

16. Wählen Sie **Neues aus vorhandener Vergütungsmatrix erstellen**.

17. Geben Sie in das Feld **Kopieren von Raster** einen Wert ein oder wählen Sie ihn aus. Optional können Sie den Namen des neuen Vergütungsrasters, das Sie anlegen, ändern, indem Sie das ausgewählte Raster kopieren.

18. Wählen Sie **OK**.

19. Wählen Sie **Massenänderung**. Mit **Massenänderung** können Sie die Beträge der Vergütungsmatrix beibehalten, indem Sie eine prozentuale oder pauschale Betragserhöhung auf eine oder mehrere Ebenen oder Bezugspunkte anwenden.

20. Geben Sie in das Feld **Anpassungsbetrag** eine Zahl ein.

21. Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.

22. Klicken Sie auf **Anwendung auf Raster**.

23. Schließen Sie die Seite. Nachdem Sie die Vergütungsstruktur angelegt haben, können Sie auswählen, welcher der Referenzpunkte als Kontrollpunkt für den festen Vergütungsplan verwendet werden soll. Der Kontrollpunkt wird zur Berechnung des Kompensationsverhältnisses eines Mitarbeiters verwendet.

24. Geben Sie in das Feld **Kontrollpunkt** einen Wert ein oder wählen Sie einen Wert aus.

25. Schließen Sie die Seite.

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a>Legen Sie eine Zulässigkeitsregel für den festen Vergütungsplan an.

Sie können einem Mitarbeiter erst dann einen festen Vergütungsplan zuordnen, wenn Sie die Zulässigkeitsregeln für den Plan definiert haben.  

1. Wählen Sie **Zulässigkeitsregeln**.

2. Wählen Sie **Neu** aus.

3. Geben Sie in das Feld **Zulässigkeit** einen Wert ein.

4. Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.

5. Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein. Sowohl feste als auch variable Vergütungspläne verwenden Zulässigkeitsregeln. Wählen Sie im Feld **Typ** die Art des Plans aus.

6. Geben Sie im Feld **Plan** einen Wert ein oder wählen Sie ihn aus. Wählen Sie die Kriterien aus, die ein Mitarbeiter erfüllen muss, um für den Vergütungsplan berechtigt zu sein. Die Kriterien können umfassen:

    - **Abteilung**
    - **Gewerkschaft**
    - **Standort** (**Vergütungsregion**)
    - **Job**
    - **Funktion**
    - **Stellentyp**
    - **Vergütungsstufe**
    
    Der Mitarbeiter muss alle angegebenen Kriterien erfüllen, um für den Vergütungsplan berechtigt zu sein. Wenn Sie keine Kriterien angeben, sind alle Mitarbeiter für den Vergütungsplan berechtigt. Wenn ein Mitarbeiter die in der Zulässigkeitsregel angegebenen Kriterien nicht erfüllt oder keine Zulässigkeitsregel für einen Vergütungsplan angegeben wurde, erscheint der Vergütungsplan nicht in der Nachschlagsliste, wenn Sie einen Satz für eine feste Vergütung für einen Mitarbeiter anlegen.

7. Schließen Sie die Seite.

8. Schließen Sie die Seite.



[!INCLUDE[footer-include](../includes/footer-banner.md)]