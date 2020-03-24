---
title: Abzüge konfigurieren
description: Verwenden Sie Abzüge in Microsoft Dynamics 365 Human Resources, um zu bestimmen, wie viel ggf. für jeden Vorteil vom Lohnscheck eines Mitarbeiters abzuziehen ist.
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
ms.openlocfilehash: a5287161f352b386ae4e13067f40228d7c1bce62
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092728"
---
# <a name="configure-deductions"></a>Abzüge konfigurieren

[!include [banner](includes/preview-feature.md)]

Verwenden Sie Abzüge in Microsoft Dynamics 365 Human Resources, um zu bestimmen, wie viel ggf. für jeden Vorteil vom Lohnscheck eines Mitarbeiters abzuziehen ist. Abzüge haben ein Gültigkeitsdatum, sodass Sie einen historischen Datensatz der Abzugsinformationen führen können. 

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Abzüge**.

2. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | Abzug | Eine eindeutige ID, mit der der Vorteilsabzug identifiziert wird. |
   | Beschreibung | Eine Beschreibung für den Abzug. |
   | Gültig | Das Startdatum. Das aktuelle Systemdatum ist der Standardwert. |
   | Ablaufdatum | Das Enddatum. Der Standardwert lautet 31.12.2154 (stellvertretend für „endet nie“). |
   | Überschrift | Der Überschriftencode aus dem Lohnsystem, den dieser Abzug für den Mitarbeiteranteil des Abzugs verwendet, wenn die Vorteile für den Lohn verarbeitet werden. Dies wird verwendet, wenn Sie einen Drittanbieter für die Lohnabrechnung verwenden. |
   | Referenz für Lohnabzüge des Mitarbeiters | Der Abzugscode aus dem Lohnsystem, den dieser Abzug für den Mitarbeiteranteil des Abzugs verwendet, wenn Vergütungen für die Lohnabrechnung verarbeitet werden. |
   | Betragsüberschrift | Der Überschriftencode aus dem Lohnsystem, den dieser Abzugsbetrag für den Mitarbeiteranteil des Abzugs verwendet, wenn die Vorteile für den Lohn verarbeitet werden. Dies wird normalerweise verwendet, wenn Sie einen Drittanbieter für die Lohnabrechnung verwenden. |
   | Löschen möglich | Gibt an, ob ein exportierter Wert von Dynamics 365 for Finance and Operations dazu führen kann, dass der Wert im Lohnsystem gelöscht wird. |
   | Gekoppelte Spalten | Gibt an, ob Überschrift und Abzugsbetrag in gekoppelten benachbarten Spalten an das Lohnsystem exportiert werden sollen. |
   | Gültigkeitsdatum ändern | Datum, zu dem die Änderung des Vorteilsabzugs gültig wird. An diesem Datum ändert das System automatisch den Vergütungsabzug und aktualisiert alle Vorteilspläne, die mit diesem Abzug verbunden sind, solange Sie die Verarbeitung von aktualisierten Abzugsänderungen ausführen. |
   | Abzugsänderung abgeschlossen | Das Kontrollkästchen „Abzugsänderung abgeschlossen“ wird automatisch aktiviert, sobald die Änderungen des Vorteilsabzugs durch die Verarbeitung von aktualisierten Abzugsänderungen abgeschlossen wurden. |
   
4. Um Änderungen an der Vorteilssatzeinstellung zu verfolgen und beizubehalten, wählen Sie **Aktionen** und dann **Versionen verwalten** aus.

5. Wählen Sie **Speichern**. 
