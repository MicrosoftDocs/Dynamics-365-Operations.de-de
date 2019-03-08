---
title: Strukturen für erweiterte Regeln erstellen und zuweisen
description: Dieser Aufgabenleitfaden führt Sie durch das Erstellen und Zuweisen einer erweiterten Regelstruktur zu einer Kontostruktur.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd62254c20cf5d77677d03c7d7335fb793d7f5f2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "367040"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Strukturen für erweiterte Regeln erstellen und zuweisen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieser Aufgabenleitfaden führt Sie durch das Erstellen und Zuweisen einer erweiterten Regelstruktur zu einer Kontostruktur. Dieser Leitfaden verwendet das Demounternehmen USMF.


## <a name="create-an-advanced-rule-structure"></a>Struktur für erweiterte Regeln erstellen
1. Wechseln Sie zu "Hauptbuch" > "Kontenplan" > "Strukturen" > "Erweiterte Regelstrukturen".
2. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
3. Geben Sie im Feld "Erweiterte Regelstruktur" einen Namen für die Regelstruktur ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein, um die Struktur zu beschreiben.
5. Klicken Sie auf "OK".
6. Klicken Sie auf "Segment hinzufügen".
7. Wählen Sie eine Segmentliste eine Finanzdimension aus.
    * Beispielsweise "Shop".  
8. Klicken Sie auf "Segment hinzufügen".
9. Klicken Sie in der Liste auf den Link zur erweiterten Regelstruktur, um sie anzuzeigen.
10. Klicken Sie auf Aktivieren.
11. Klicken Sie auf Aktivieren.

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>Anwenden einer erweiterten Regelstruktur auf eine Kontostruktur
1. Schließt das Formular.
2. Schließen Sie die Seite.
3. Wechseln Sie zu Hauptbuch > Kontenplan > Strukturen > Kontostrukturen konfigurieren.
4. Wählen Sie in der Liste die Kontostruktur aus, auf die Sie die erweiterte Regel anwenden möchten.
5. Klicken Sie auf den Namen der Kontostruktur.
6. Klicken Sie auf "Bearbeiten".
    * Sie können auch auf "Erweiterte Regeln" klicken und die Kontostruktur im Entwurfsmodus einfügen.  
7. Klicken Sie auf "Erweiterte Regeln".
8. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
9. Geben Sie im Feld "Erweiterte Regeln" einen Wert ein.
10. Geben Sie im Feld "Name" einen Wert ein.
11. Klicken Sie auf Erstellen.
12. Klicken Sie auf "Neue Kriterien hinzufügen".
13. Wählen Sie im Feld "Wo" "Hauptkonto" oder "Finanzdimension" aus.
14. Wählen Sie im Feld "Operator" eine Option aus (z. B., "liegt zwischen" und "schließt ein").
15. Geben Sie im Feld "Wert" einen Wert ein.
16. Geben Sie im Feld "bis" einen Wert ein.
17. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
18. Wählen Sie in der Liste die erweiterte Regelstruktur aus, die Sie verwenden möchten, wenn das eingegebene Kriterium erfüllt wird.
19. Klicken Sie auf Hinzufügen.
20. Schließen Sie die Seite.
21. Klicken Sie auf Aktivieren.
22. Klicken Sie auf Aktivieren.

