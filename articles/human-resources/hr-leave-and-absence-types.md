---
title: Urlaubs- und Abwesenheitstypen konfigurieren
description: Einrichten von Abwesenheitstypen, die Mitarbeiter in Anspruch nehmen können in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e35c5fed886ebf9a453c22b3e04ca9ffe50b6d70
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805203"
---
# <a name="configure-leave-and-absence-types"></a>Urlaubs- und Abwesenheitstypen konfigurieren

[!include [preview banner](../includes/preview-banner.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

1. Wählen Sie im Arbeitsbereich **Urlaub- und Abwesenheit** die Registerkarte **Links** aus.
2. Unter **Installieren**, wählen Sie **Urlaubs- und Abwesenheitstypen**.
3. Wählen Sie **Neu** aus.
4. Geben Sie einen Namen für den Beurlaubstyp ein unter **Typ**, geben Sie eine Beschreibung unter **Beschreibung** aus und wählen Sie im Feld **Workflow-ID** einen Workflow aus. Wählen Sie basierend auf der Urlaubsart einen Antragstyp im Feld **Antragstyp** aus. Wählen Sie beispielsweise **Arbeitsfreie Zeit** oder **Beurlaubung** aus.
5. Unter **Allgemein**, wählen Sie **Keine**, **Geplant**, oder **Nicht geplant** aus der Dropdown-Liste **Kategorie** aus.
6. Wählen Sie einen Einkommenscode aus der **Einkommenscode** Dropdown-Liste aus.
7. Wählen Sie unter **Ursachencode erforderlich** aus, ob ein Ursachencode erforderlich sein soll. Wenn Ursachencodes notwendig sein sollen, müssen Sie diese möglicherweise hinzufügen. Unter **Ursachencodes** wählen Sie **Hinzufügen**, wählen Sie einen Ursachencode und dann das Kontrollkästchen **aktiviert**.
8. Wenn es sich um den Antragstyp **Beurlaubung** lautet, führen Sie die folgenden Schritte aus:

      1. Wählen Sie unter **Unbefristet** aus, ob Benutzer unbefristete Beurlaubungen erstellen können sollen.
      2. Wenn **Unbefristet** aktiviert ist, können Sie auswählen, ob Arbeitnehmer eine Meldung zur Wiederaufnahme der Arbeit einreichen müssen, wenn sie aus dem Urlaub zurückkehren.
      3. Wenn Arbeitnehmer eine Meldung zur Wiederaufnahme der Arbeit einreichen müssen, können Sie **Meldung zur Wiederaufnahme der Arbeit aktivieren** aktivieren. Wenn **Meldung zur Wiederaufnahme der Arbeit** aktiviert ist, wird **Anhang erforderlich** automatisch aktiviert und kann nicht deaktiviert werden.

9. Wenn Benutzer beim Erstellen oder Aktualisieren von Urlaubsanträgen Dokumente hochladen sollen, können Sie **Anhang erforderlich** aktivieren.
10. Wählen Sie unter **Zugriff auf ausgewählte Rollen einschränken** aus, ob Sie den Zugriff einschränken möchten. Wählen Sie dann die Sicherheitsrollen unter **Sicherheitsrollen für diesen Urlaubstyp** aus. Die Sicherheitsrollen werden in dem Workflow definiert, den Sie vorher in diesem Verfahren unter **Workflow-ID** ausgewählt haben.
11. Wählen Sie unter **Kalenderfarbe** aus, welche Farbe in Urlaubs- und Abwesenheitskalendern für diesen Urlaubstyp angezeigt werden soll.
11. Wählen Sie unter **Suspendierungsbeziehungen** aus, ob dieser Urlaubstyp entweder einen anderen Urlaubstyp aussetzt oder von einem anderen Urlaubstyp ausgesetzt werden soll. Wenn ein Antrag auf Beurlaubung für die Art der Aussetzung des Urlaubs gestellt wird, wird automatisch eine Aussetzung der Beurlaubung für die Art der Aussetzung des Urlaubs erstellt.
12. Wählen Sie **Speichern** aus.

## <a name="configure-leave-type-rules"></a>Konfigurieren Sie die Urlaubstypregeln

1. Stellen Sie Rundungsoptionen für die Art von **Urlaub und Abwesenheit** ein. Optionen umfassen **Keine**, **Oben**, **Unten**, und **Nächste**. Sie können auch die Rundungsgenauigkeit für den Urlaubstyp festlegen.
2. Stellen **Urlaubskorrekturen** für den Abwesenheitstyp ein. Wenn Sie diese Option auswählen, wird die Anzahl der Feiertage verwendet, die auf einen Arbeitstag fallen, um zu bestimmen, wie Freizeit für die Urlaubsart angesammelt werden soll. Wenn beispielsweise der Weihnachtstag auf einen Montag fällt, zieht die Personalabteilung bei der Verarbeitung von Rückstellungen einen Tag von der Urlaubsart ab.

   Sie legen den Urlaub im Arbeitszeitkalender fest. Weitere Informationen finden Sie unter [Einen Arbeitszeitkalender erstellen](hr-leave-and-absence-working-time-calendar.md).
   
 3. Einstellen des **Vortragstyps** für den Urlaubstyp. Wenn Sie diese Option auswählen, werden alle Vortragsguthaben auf die angegebene Urlaubsart übertragen. Die Art des Vortragstyps für den Urlaub muss ebenfalls in den Urlaubs- und Abwesenheitsplan aufgenommen werden. 
 
4. Definieren von **Ablaufregeln** für den Urlaubstyp. Wenn Sie diese Option konfigurieren, können Sie die Einheit Tage oder Monate wählen und die Dauer für den Verfall festlegen. Das Gültigkeitsdatum der Verfallsregel wird verwendet, um zu bestimmen, wann der Batchauftrag ausgeführt wird, der den Urlaubsverfall verarbeitet, oder das Datum, an dem die Regel in Kraft tritt. Der Verfall selbst findet immer am Startdatum der Abgrenzungsperiode statt. Wenn z. B. das Abgrenzungszeitraum-Startdatum der 3. August 2021 ist und die Verfallsregel auf 6 Monate festgelegt wurde, wird die Regel basierend auf dem Verfalls-Offset vom Abgrenzungszeitraum-Startdatum verarbeitet, so dass sie am 3. Februar 2022 ausgeführt würde. Zum Zeitpunkt des Ablaufs vorhandene Urlaubsguthaben werden von der Urlaubsart abgezogen und im Urlaubsguthaben ausgewiesen.
 
## <a name="configure-the-required-attachment-per-leave-type"></a>Anhangsanforderung pro Urlaubsart konfigurieren

> [!NOTE]
> Um das Feld **Anhang erforderlich** zu verwenden, müssen Sie zuerst die Funktion **Erforderlichen Anhang für Abwesenheitsanträge konfigurieren** in der Funktionsverwaltung aktivieren. Weitere Informationen zur Aktivierung von Funktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

1. Auf der **Urlaub und Abwesenheit** Seite, auf der **Verknüpfungen** Registerkarte, unter **Installieren** wählen Sie **Urlaubs- und Abwesenheitsarten**.

2. Wählen Sie in der Liste einen **Urlaubs- und Abwesenheitstyp** aus. Verwenden Sie im Abschnitt **Allgemein** das Feld **Anhang erforderlich**, um anzugeben, ob ein Anhang hochgeladen werden muss, wenn ein Mitarbeiter einen neuen Urlaubsantrag für die ausgewählte Urlaubsart stellt. 

Mitarbeiter müssen einen Anhang hochladen, wenn sie einen neuen Urlaubsantrag mit einer Urlaubsart einreichen, in der das Feld **Anhang erforderlich** aktiviert ist. Um den Anhang anzuzeigen, der als Teil eines Abwesenheitsantrags hochgeladen wurde, können Abwesenheitsantragsgenehmiger die **Anhänge** Option für die ihnen zugeordneten Arbeitselemente nutzen. Wenn auf einen Urlaubsantrag über die Personal-App in Microsoft Teams zugegriffen wird, kann die Option **Details anzeigen** für den Abwesenheitsantrag verwendet werden, um dessen Details und eventuelle Anhänge anzuzeigen.

## <a name="configure-leave-units-hoursdays-per-leave-type"></a>Konfigurieren von Einheiten (Stunden/Tage) pro Urlaubsart

> [!NOTE]
> Um die Abwesenheitseinheiten pro Abwesenheitsart zu verwenden, müssen Sie zuerst die Funktion **Urlaubseinheiten pro Urlaubsart konfigurieren** in der Funktionsverwaltung aktivieren. Weitere Informationen zur Aktivierung von Funktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

> [!IMPORTANT]
> Standardmäßig verwenden die Urlaubsarten in einer juristischen Person die Urlaubseinheiten aus der Konfiguration der Urlaubsparameter auf Ebene der juristischen Person.
> 
> Die Urlaubseinheit einer Urlaubs- und Abwesenheitsart kann nur geändert werden, wenn für diese Urlaubsart keine Urlaubsbuchungen vorhanden sind.
> 
> Nachdem die Funktion aktiviert wurde, kann sie nicht wieder deaktiviert werden.

1. Auf der **Urlaub und Abwesenheit** Seite, auf der **Verknüpfungen** Registerkarte, unter **Installieren** wählen Sie **Urlaubs- und Abwesenheitsarten**.

2. Wählen Sie in der Liste einen Urlaubs- und Abwesenheitstyp aus. Dann wählen Sie im Abschnitt **Allgemein** im Feld **Einheit** die Urlaubseinheit aus. Sie können **Stunden** oder **Tage** auswählen.

3. Optional: Wenn Sie **Stunden** in dem Feld **Einheit** ausgewählt haben, können Sie das Feld **Halbtagesdefinition aktivieren** verwenden, um anzugeben, ob Mitarbeiter den ersten halben Tag oder den zweiten halben Tag frei wählen können, wenn sie einen halben Tag Urlaub beantragen.

Mitarbeiter, die einen neuen Urlaubsantrag stellen, können verschiedene Urlaubsarten auswählen, um ihren Urlaubsantrag zu erstellen. Alle Urlaubsarten, die im Rahmen eines einzigen Urlaubsantrags ausgewählt werden, sollten jedoch dieselbe Urlaubseinheit haben. Mitarbeiter können die Urlaubseinheit jede Urlaubsart im **Freizeit anfordern** anzeigen.

## <a name="see-also"></a>Siehe auch

- [Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)
- [Einen Urlaubs- und Abwesenheitsplan erstellen](hr-leave-and-absence-plans.md)
- [Einen Arbeitszeitkalender erstellen](hr-leave-and-absence-working-time-calendar.md)
- [Urlaub aussetzen](hr-leave-and-absence-suspend-leave.md)
- [Einen Workflow zum Kaufen und Verkaufen von Urlaubsanforderungen erstellen](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
