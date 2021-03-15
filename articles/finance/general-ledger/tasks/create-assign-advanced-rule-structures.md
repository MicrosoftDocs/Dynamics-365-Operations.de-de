---
title: Strukturen für erweiterte Regeln erstellen und zuweisen
description: In diesem Thema wird erläutert, wie Sie eine erweiterte Regelstruktur erstellen und einer Kontostruktur zuweisen.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6a3f7d174c91e357dce8a19ab50a5cd42a85561
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968597"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Strukturen für erweiterte Regeln erstellen und zuweisen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie eine erweiterte Regelstruktur erstellen und einer Kontostruktur zuweisen. Dieser Leitfaden verwendet das Demounternehmen USMF.

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