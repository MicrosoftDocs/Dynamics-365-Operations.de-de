---
title: Registrieren eines Mitarbeiters in einem Plan für variable Vergütung
description: Der Leiter für Vergütungen/Bezüge kann Mitarbeiter in einem Plan für variable Vergütung registrieren, um Bargeld- und bargeldlose Prämien für Mitarbeiter zu berechnen.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a173403e79212be5e4aac36d99f349da159e08
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112678"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a>Registrieren eines Mitarbeiters in einem Plan für variable Vergütung

Der Leiter für Vergütungen/Bezüge kann Mitarbeiter in einem Plan für variable Vergütung registrieren, um Bargeld- und bargeldlose Prämien für Mitarbeiter zu berechnen. Für dieses Verfahren wird vorausgesetzt, dass ein Plan für variable Vergütung mit dem Feld "Registrierung aktivieren" auf "Ja" festgelegt wurde und dass Berechtigungsregeln für diesen Plan für variable Vergütung erstellt wurden. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Um das Verfahren zu starten, gehen Sie zu "Personalverwaltung" > "Arbeitskräfte" > "Mitarbeiter" > "Vergütung" > "Variabler Plan registrieren".

1. Klicken Sie auf "Neu".
2. Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Plansuche wird gefiltert, um nur die Pläne für variable Vergütung anzuzeigen, für die der Mitarbeiter auf Grundlage der Berechtigungsregeln freigegeben wurde.  
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Schalten Sie die Erweiterung des Abschnitts "Allgemein" ein/aus.
5. Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.
6. Klicken Sie auf "Speichern".
7. Schalten Sie die Erweiterung des Abschnitts "Überschreibungen" ein/aus.
    * Optional kann ein Einstellungsregeldatum festgelegt werden, um das Einstellungsdatum für einen Mitarbeiter zu überschreiben, wenn die Einstellungsregel für den ausgewählten variablen Plan "Prozent" ist.  
    * Wenn der variable Plan ein prozentualer Anteil des Basisplans ist, kann der Prämienprozentsatz für den Mitarbeiter überschrieben werden. Wenn der variable Vergütungsplan ein Einheitenanzahlsplan ist, kann die Anzahl der Einheiten für den Mitarbeiter überschrieben werden.  
    * Wenn dem Mitarbeiter als Pauschalbetrag für seine Zulage gezahlt wird, kann der Betrag hier festgelegt werden.  
8. Schalten Sie die Erweiterung des Abschnitts "Überschreibungen in Organisation" ein/aus.
    * Wenn die Leistung des Mitarbeiters, die Leistung unterschiedlicher Abteilungen oder einer anderen als die der Position des Mitarbeiters zugewiesene Abteilung berücksichtigt werden soll, kann die Abteilung überschrieben werden. Die Spalte "Prozent" sollte sich auf 100 summieren.  

