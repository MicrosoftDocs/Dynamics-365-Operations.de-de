---
title: Strukturen für erweiterte Regeln erstellen und zuweisen
description: In diesem Artikel wird erläutert, wie Sie eine erweiterte Regelstruktur erstellen und einer Kontostruktur zuweisen.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72688642936f9428c96aebb34bf9f240dd48b46b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896318"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Strukturen für erweiterte Regeln erstellen und zuweisen

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie eine erweiterte Regelstruktur erstellen und einer Kontostruktur zuweisen. Dieser Leitfaden verwendet das Demounternehmen USMF.

## <a name="create-an-advanced-rule-structure"></a>Struktur für erweiterte Regeln erstellen
1. Wechseln Sie zu **Navigationsbereich > Module > Hauptbuch > Kontenplan > Strukturen > Erweiterte Regelstrukturen**.
2. Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.
3. Geben Sie im Feld **Erweiterte Regelstruktur** einen Namen zur Beschreibung der Regelstruktur ein.
4. Wählen Sie **OK**.
5. Wählen Sie **Segment hinzufügen** aus.
6. Wählen Sie eine Segmentliste eine Finanzdimension aus. Zum Beispiel **Shop**.  
7. Wählen Sie **Segment hinzufügen** aus.
8. Wählen Sie **Aktivieren** aus.

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>Anwenden einer erweiterten Regelstruktur auf eine Kontostruktur
1. Wechseln Sie zu **Navigationsbereich > Module > Hauptbuch > Kontenplan > Strukturen > Kontostrukturen konfigurieren**.
2. Wählen Sie in der Liste die Kontostruktur aus, auf die Sie die erweiterte Regel anwenden möchten.
3. Wählen Sie **Bearbeiten** aus. Sie können auch **Erweiterte Regeln** auswählen. Sie werden dann aufgefordert, die Kontostruktur im **Entwurfsmodus** einzufügen.  
4. Wählen Sie **Erweiterte Regeln** aus.
5. Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.
6. Geben Sie im Feld **Erweiterte Regel** einen Wert ein.
7. Geben Sie im Feld **Name** einen Wert ein.
8. Wählen Sie **Erstellen** aus.
9. Wählen Sie **Neue Kriterien hinzufügen**.
10. Wählen Sie im Feld **Wo** das Hauptkonto oder eine Finanzdimension aus.
11. Wählen Sie im Feld **Operator** eine Option aus (z. B. **ist zwischen** und **enthält**).
12. Geben Sie im Feld **Wert** einen Wert ein.
13. Geben Sie im Feld **Bis** einen Wert ein.
14. Wählen Sie **Hinzufügen**, um das Dropdown-Dialogfeld zu öffnen.
15. Wählen Sie in der Liste die erweiterte Regelstruktur aus, die Sie verwenden möchten, wenn das eingegebene Kriterium erfüllt wird.
16. Wählen Sie **Hinzufügen** aus.
17. Schließen Sie die Seite.
18. Wählen Sie **Aktivieren** aus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
