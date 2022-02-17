---
title: Registrieren eines Mitarbeiters in einem Plan für variable Vergütung
description: Der Leiter für Vergütungen/Bezüge kann Mitarbeiter in einem Plan für variable Vergütung registrieren, um Bargeld- und bargeldlose Prämien für Mitarbeiter zu berechnen.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49a64407778fba5669ad13f239363bffd4b0c7d6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071483"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a>Registrieren eines Mitarbeiters in einem Plan für variable Vergütung


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Der Leiter für Vergütungen/Bezüge kann Mitarbeiter in einem Plan für variable Vergütung registrieren, um Bargeld- und bargeldlose Prämien für Mitarbeiter zu berechnen. Dieses Verfahren setzt voraus, dass ein variabler Vergütungsplan erstellt wurde, bei dem das Feld **Einschreibung aktivieren** auf **Ja** festgelegt wurde, und dass für diesen variablen Vergütungsplan Berechtigungsregeln erstellt wurden. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Um diesen Vorgang zu starten, gehen Sie zu **Personal Resources** > **Arbeiter** > **Mitarbeiter** > **Vergütung** > **Variabler Plan Anmeldung**.

1. Klicken Sie auf **Neu**.
2. Klicken Sie im Feld **Plan** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Plansuche wird gefiltert, um nur die Pläne für variable Vergütung anzuzeigen, für die der Mitarbeiter auf Grundlage der Berechtigungsregeln freigegeben wurde.  
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Schalten Sie die Erweiterung des Abschnitts **Allgemein** um.
5. Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.
6. Klicken Sie auf **Speichern**.
7. Schalten Sie die Erweiterung des Abschnitts **Überschreibungen** ein/aus.
    * Optional kann ein Einstellungsregeldatum festgelegt werden, um das Einstellungsdatum für einen Mitarbeiter zu überschreiben, wenn die Einstellungsregel für den ausgewählten variablen Plan "Prozent" ist.  
    * Wenn der variable Plan ein prozentualer Anteil des Basisplans ist, kann der Prämienprozentsatz für den Mitarbeiter überschrieben werden. Wenn der variable Vergütungsplan ein Einheitenanzahlsplan ist, kann die Anzahl der Einheiten für den Mitarbeiter überschrieben werden.  
    * Wenn dem Mitarbeiter als Pauschalbetrag für seine Zulage gezahlt wird, kann der Betrag hier festgelegt werden.  
8. Schalten Sie die Erweiterung des Abschnitts **Überschreibungen in Organisation** ein/aus.
    * Wenn die Leistung des Mitarbeiters, die Leistung unterschiedlicher Abteilungen oder einer anderen als die der Position des Mitarbeiters zugewiesene Abteilung berücksichtigt werden soll, kann die Abteilung überschrieben werden. Die Spalte **Prozent** sollte sich auf 100 summieren.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
