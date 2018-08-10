--- 
title: "Abschreibungsbücher einrichten "
description: Diese Aufgabenanleitung erstellt ein neues Abschreibungsbuch und ordnet es einer Anlagengruppe zu.
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d06d5f92e91e33dc752bf45ab890c37dfea3888d
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-depreciation-books"></a>Abschreibungsbücher einrichten  

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


