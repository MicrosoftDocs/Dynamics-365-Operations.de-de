---
title: Anpassen der deutschen Protokolldateikonfiguration
description: Im folgenden Verfahren sehen Sie, wie Sie die deutsche Protokolldateikonfiguration durch Hinzufügen einer neuen Tabellengruppe und Auswählen einer Tabelle mit Feldern für die Datenexportdefinition anpassen.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERTableNameLookup, ERModelGDPdUFunctionEditor,  ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Germany
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ba61cbe44fbf6e7e1471b5db8081c186a5b327dd0c9895ee318a92cdd0d93e5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742844"
---
# <a name="customize-german-audit-file-configuration"></a>Anpassen der deutschen Protokolldateikonfiguration

[!include [banner](../../includes/banner.md)]

Im folgenden Verfahren sehen Sie, wie Sie die deutsche Protokolldateikonfiguration durch Hinzufügen einer neuen Tabellengruppe und Auswählen einer Tabelle mit Feldern für die Datenexportdefinition anpassen. 

Diese Aufgabe wurde mithilfe des Demodatenunternehmens DEMF erstellt, mit "Deutschland" als Land/Region für die primäre Adresse für die juristischen Person.

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Klicken Sie auf "Konfigurationen".
3. Klicken Sie auf "Filter anzeigen".
4. Filter hinzufügen
5. Klicken Sie auf Übernehmen.
6. Klicken Sie auf "Modelldesigner".
7. Wählen Sie in der Struktur 'enumTableGroup' aus.
8. Klicken Sie auf Neu.
9. Geben Sie im Feld "Name" einen Wert ein.
10. Geben Sie im Feld "Beschreibung" einen Wert ein.
11. Klicken Sie auf "Modell der Datenquelle zuordnen".
12. Klicken Sie auf Designer.
13. Wählen Sie in der Strukturdarstellung "Dynamics Ax\Tabellendatensätze" aus.
14. Klicken Sie auf "Stamm hinzufügen".
15. Geben Sie im Feld "Name" einen Wert ein.
16. Geben Sie im Feld 'Tabelle' einen Wert ein, oder wählen Sie einen Wert aus.
17. Klicken Sie auf "OK".
18. Wählen Sie in der Struktur "Functions\Table metadata" aus.
19. Klicken Sie auf "Stamm hinzufügen".
20. Geben Sie im Feld "Name" einen Wert ein.
21. Geben Sie im Feld Beschreibung einen Wert ein.
22. Klicken Sie auf "Editor".
23. Wählen Sie in der -Struktur "AssetTable" aus.
24. Klicken Sie auf Hinzufügen.
25. Geben Sie im Feld "Name" einen Wert ein.
26. Erweitern Sie in der Struktur den Knoten 'AssetTable'.
27. Wählen Sie in der Struktur "AssetTable\Fixed asset number(AssetId)" aus.
28. Klicken Sie auf Hinzufügen.
29. Markieren Sie in der Liste die ausgewählte Zeile.
30. Geben Sie im Feld "Name" einen Wert ein.
31. Schließen Sie die Seite.
32. Klicken Sie auf "Ja".
33. Klicken Sie auf "OK".
34. Wählen Sie in der Struktur "TblGroup" aus.
35. Klicken Sie auf "Bearbeiten".
36. Klicken Sie auf Formel bearbeiten.
37. Geben Sie im Feld "expressionAsStringText" einen Wert ein.
38. Erweitern oder reduzieren Sie 'enumTableGroup' in der Struktur.
39. Wählen Sie in der Struktur 'enumTableGroup\Anlagen' aus.
40. Klicken Sie auf Datenquelle hinzufügen.
41. Geben Sie im Feld "expressionAsStringText" einen Wert ein.
42. Wählen Sie in der Struktur '_05Anlagen(TblGroup5)' aus.
43. Klicken Sie auf Datenquelle hinzufügen.
44. Geben Sie im Feld "expressionAsStringText" einen Wert ein.
45. Klicken Sie auf "Speichern".
46. Schließen Sie die Seite.
47. Klicken Sie auf "OK".
48. Schließen Sie die Seite.
49. Klicken Sie auf "Ja".
50. Schließen Sie die Seite.
51. Schließen Sie die Seite.
52. Klicken Sie auf "Status ändern".
53. Klicken Sie auf "Abgeschlossen".
54. Geben Sie im Feld "Beschreibung" einen Wert ein.
55. Klicken Sie auf "OK".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]