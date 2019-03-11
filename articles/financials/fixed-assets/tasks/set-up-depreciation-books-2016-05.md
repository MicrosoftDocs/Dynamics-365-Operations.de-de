---
title: Einrichten von Anlagenabschreibungsbüchern (Mai 2016)
description: Diese Aufgabenanleitung erstellt ein neues Abschreibungsbuch und ordnet es einer Anlagengruppe zu.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1fd53ea1dff9b116d19c525c5d6967ece0993b6f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "355563"
---
# <a name="set-up-depreciation-books-may-2016"></a>Einrichten von Anlagenabschreibungsbüchern (Mai 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Aufgabenanleitung erstellt ein neues Abschreibungsbuch und ordnet es einer Anlagengruppe zu.  Dabei werden die "Buchhalterrolle" und die Demodaten für die juristische Person USMF verwendet.


## <a name="create-a-depreciation-book"></a>Ein Abschreibungsbuch erstellen
1. Wechseln Sie zu "Anlagen" > "Einstellungen" > "Abschreibungsbücher".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Abschreibungsbuch" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Aktivieren oder deaktivieren Sie das Kontrollkästchen "Abschreibung berechnen".
6. Klicken Sie im Feld "Abschreibungsprofil" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Suchen Sie in der Liste das gewünschte Abschreibungsprofil und wählen Sie es aus.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Klicken Sie im Feld "Alternatives Abschreibungsprofil" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
10. Wählen Sie in der Liste das gewünschte Abschreibungsprofil aus.
11. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Das "Außerordentliche Abschreibungsprofil" wird für die zusätzliche Abschreibung einer Anlage unter besonderen Umständen verwendet. Sie können dieses Profil z. B. verwenden, um eine Abschreibung in Folge einer Naturkatastrophe zu erfassen.  
12. Aktivieren oder deaktivieren Sie das Kontrollkästchen "Abschreibungsregulierungen mit Basisregulierungen erstellen".
13. Klicken Sie im Feld "Kalender" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
14. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>Das Abschreibungsbuch einer Anlagengruppe zuordnen
1. Klicken Sie auf "Anlagengruppen".
2. Klicken Sie im Feld "Anlagengruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Wählen Sie im Feld "Abschreibungskonvention" eine Option aus.
6. Geben Sie im Feld "Nutzungsdauer" eine Zahl ein.
    * Beachten Sie, dass der Feldwert "Abschreibungszeiträume" nach der Festlegung der "Nutzungsdauer" berechnet wird.  

