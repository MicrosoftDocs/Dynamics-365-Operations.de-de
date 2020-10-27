---
title: Urlaubs- und Abwesenheitstypen konfigurieren
description: Einrichten von Abwesenheitstypen, die Mitarbeiter in Anspruch nehmen können in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
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
ms.openlocfilehash: 6e6ca7d04b86232ba48474fcbe288a18995661ae
ms.sourcegitcommit: 6a89816f94c8cdcae6e56fa89843eb99c28b21fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/07/2020
ms.locfileid: "3969021"
---
# <a name="configure-leave-and-absence-types"></a>Urlaubs- und Abwesenheitstypen konfigurieren

Abwesenheitstypen in Dynamics 365 Human Resources definieren die verschiedenen Arten von Abwesenheitszeiten, die Mitarbeiter melden können. Sie können die Abwesenheitstypen an die Bedürfnisse Ihrer Organisation anpassen. Beispiele für Abwesenheitstypen sind:

- Entlohnte Zeit (PTO)
- Unbezahlter Sonderurlaub
- Bezahlter Urlaub
- Krankheitsbedingte Abwesenheit
- Medizinischer Urlaub
- Familienurlaub
- Kurzfristige Behinderung
- Trauerurlaub

## <a name="add-a-leave-type"></a>Fügen Sie einen Abwesenehitstyp hinzu

1. Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.

2. Unter **Installieren**, wählen Sie **Urlaubs- und Abwesenheitstypen**.

3. Wählen Sie **Neu** aus.

4. Geben Sie einen Namen für den Abwesenheitstyp ein unter **Typ** wählen Sie einen Workflow aus unter **Workflow-ID** und geben Sie eine Beschreibung ein unter **Beschreibung**.

5. Unter **Allgemein**, wählen Sie **Keine**, **Geplant**, oder **Nicht geplant** aus der Dropdown-Liste **Kategorie** aus.

6. Wählen Sie einen Einkommenscode aus der **Einkommenscode** Dropdown-Liste aus.

7. Unter **Ursachencode erforderlich** wählen Sie, ob Sie einen Ursachencode benötigen möchten. Wenn Sie Ursachencodes benötigen, müssen Sie diese möglicherweise hinzufügen. Unter **Ursachencodes** wählen Sie **Hinzufügen**, wählen Sie einen Ursachencode und dann das Kontrollkästchen **aktiviert**.

8. Unter **Beschränken Sie den Zugriff auf ausgewählte Rollen** wählen Sie, ob Sie den Zugriff einschränken möchten. Wählen Sie dann die Sicherheitsrollen unter **Sicherheitsrollen für diesen Urlaubstyp**. Die Sicherheitsrollen werden in dem Workflow definiert, den Sie unter **Workflow-ID** früher in diesem Verfahren ausgewählt haben.

9. Wählen Sie unter **Kalenderfarbe** aus, welche Farbe in Urlaubs- und Abwesenheitskalendern für diesen Urlaubstyp angezeigt werden soll. 

10. Unter **Suspendierungsbeziehungen** wählen Sie, ob dieser Urlaubstyp entweder einen anderen Urlaubstyp aussetzt oder von einem anderen Urlaubstyp ausgesetzt werden soll. Wenn ein Antrag auf Beurlaubung für die Art der Aussetzung des Urlaubs gestellt wird, wird automatisch eine Aussetzung der Beurlaubung für die Art der Aussetzung des Urlaubs erstellt. 

10. Wählen Sie **Speichern** aus.

## <a name="configure-leave-type-rules"></a>Konfigurieren Sie die Urlaubstypregeln

1. Stellen Sie Rundungsoptionen für die Urlaubsart ein. Optionen umfassen **Keine**, **Oben**, **Unten**, und **Nächste**. Sie können auch die Rundungsgenauigkeit für den Urlaubstyp festlegen.

2. Stellen **Urlaubskorrekturen** für den Abwesenheitstyp ein. Wenn Sie diese Option auswählen, verwendet die Personalabteilung die Anzahl der Feiertage, die auf einen Arbeitstag fallen, um zu bestimmen, wie Freizeit für die Urlaubsart angesammelt werden soll. Wenn beispielsweise der Weihnachtstag auf einen Montag fällt, zieht die Personalabteilung bei der Verarbeitung von Rückstellungen einen Tag von der Urlaubsart ab.

   Sie legen den Urlaub im Arbeitszeitkalender fest. Weitere Informationen finden Sie unter [Einen Arbeitszeitkalender erstellen](hr-leave-and-absence-working-time-calendar.md)
   
 3. Einstellen des **Vortragstyps** für den Urlaubstyp. Wenn Sie diese Option auswählen, werden alle Vortragsguthaben auf die angegebene Urlaubsart übertragen. Die Art des Vortragstyps für den Urlaub muss ebenfalls in den Urlaubs- und Abwesenheitsplan aufgenommen werden. 
 
 4. Definieren von **Ablaufregeln** für den Urlaubstyp. Wenn Sie diese Option konfigurieren, können Sie die Einheit der Tage oder Monate auswählen und die Dauer für den Ablauf festlegen. Sie können auch das Datum des Inkrafttretens der Ablaufregel festlegen. Zum Zeitpunkt des Ablaufs vorhandene Urlaubsguthaben werden von der Urlaubsart abgezogen und im Urlaubsguthaben ausgewiesen. 
 
 
## <a name="see-also"></a>Siehe auch

- [Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)
- [Einen Urlaubs- und Abwesenheitsplan erstellen](hr-leave-and-absence-plans.md)
- [Einen Arbeitszeitkalender erstellen](hr-leave-and-absence-working-time-calendar.md)
- [Urlaub aussetzen](hr-leave-and-absence-suspend-leave.md)

