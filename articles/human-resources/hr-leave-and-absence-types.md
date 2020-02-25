---
title: Urlaubs- und Abwesenheitstypen konfigurieren
description: Einrichten von Abwesenheitstypen, die Mitarbeiter in Anspruch nehmen können in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 1748ec2a888a50af9b9260720dfd439adc4686f9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009186"
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

9. Wählen Sie **Speichern**.

## <a name="configure-preview-features"></a>Vorschaufunktionen konfigurieren

Wenn Sie die Vorschaufunktionen für Urlaub und Abwesenheit aktiviert haben, müssen Sie auch die Einstellungen für sie konfigurieren.

[!include [banner](includes/preview-feature-leave-absence.md)]

1. Stellen Sie Rundungsoptionen für die Urlaubsart ein. Optionen umfassen **Keine**, **Oben**, **Unten**, und **Nächste**. Sie können auch die Rundungsgenauigkeit für den Urlaubstyp festlegen.

2. Stellen **Urlaubskorrekturen** für den Abwesenheitstyp ein. Wenn Sie diese Option auswählen, verwendet die Personalabteilung die Anzahl der Feiertage, die auf einen Arbeitstag fallen, um zu bestimmen, wie Freizeit für die Urlaubsart angesammelt werden soll. Wenn beispielsweise der Weihnachtstag auf einen Montag fällt, zieht die Personalabteilung bei der Verarbeitung von Rückstellungen einen Tag von der Urlaubsart ab.

   Sie legen den Urlaub im Arbeitszeitkalender fest. Weitere Informationen finden Sie unter [Einen Arbeitszeitkalender erstellen](hr-leave-and-absence-working-time-calendar.md)

## <a name="see-also"></a>Siehe auch

- [Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)
- [Einen Urlaubs- und Abwesenheitsplan erstellen](hr-leave-and-absence-plans.md)
- [Einen Arbeitszeitkalender erstellen](hr-leave-and-absence-working-time-calendar.md)