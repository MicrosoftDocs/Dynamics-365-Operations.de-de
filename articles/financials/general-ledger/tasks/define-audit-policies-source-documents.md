--- 
title: "Überwachungsrichtlinien für Quelldokumente definieren"
description: "Diese Prozedur zeigt, wie und Überwachungsrichtlinienregeln eingerichtet und ausgeführt werden."
author: ryansandness
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4b05f744120e940bfea3e92b8aac3e41fc8151d9
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="define-audit-policies-for-source-documents"></a>Überwachungsrichtlinien für Quelldokumente definieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie und Überwachungsrichtlinienregeln eingerichtet und ausgeführt werden. Das Beispiel verwendet Spesenabrechnungen mit dem Hotelausgabentyp. Für diese Prozedur wird das Demo-Unternehmen USMF verwendet. Die Wirtschaftsprüferrolle umfasst die richtigen Berechtigungen, um diese Aufgaben auszuführen.

1. Wechseln Sie zu "Überwachungsworkbench" > "Einstellung" > "Richtlinienregeltyp".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Regelname" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie im Feld "Abfragename" die Position "Spesenabrechnung" aus
6. Wählen Sie im Abfragetypfeld "Zusammenführen" aus
7. Wählen Sie im Feld "Juristische Person" die Option "Juristische Person" aus
8. Wählen Sie im Feld "Dokumentdatumsreferenz" die Option "Änderungsdatum und -uhrzeit" aus
9. Klicken Sie auf "Speichern".
10. Wechseln Sie zu "Überwachungsworkbench" > "Einstellung" > "Überwachungsrichtlinien".
11. Klicken Sie auf "Neu".
12. Geben Sie im Feld "Name" einen Wert ein.
13. Erweitern Sie den Abschnitt "Richtlinienorganisationen".
14. Wählen Sie in der Struktur "Contoso Unterhaltungsanlagen USA" aus.
15. Klicken Sie auf Hinzufügen.
16. Wählen Sie in der Struktur "Contoso Beratung USA" aus.
17. Klicken Sie auf Hinzufügen.
18. Wählen Sie in der Struktur "Contoso Einzelhandel USA" aus.
19. Klicken Sie auf Hinzufügen.
20. Reduzieren Sie den Abschnitt "Richtlinienorganisationen".
21. Erweitern Sie den Abschnitt "Richtlinienregeln".
22. Suchen Sie in der Liste die zuvor erstellte "Richtlinienregel" und wählen Sie diese aus.
23. Klicken Sie auf "Richtlinienregel erstellen".
24. Geben Sie im Feld "Gültigkeitsdatum" ein Datum und eine Uhrzeit ein.
25. Klicken Sie auf "Filter".
26. Wählen Sie in der Liste die Zeile für "Ausgabenkategorie" aus, und legen Sie die Details zum "Hotel" fest
27. Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.
28. Klicken Sie auf die Registerkarte "Zusammenführen".
29. Klicken Sie auf Hinzufügen.
30. Wählen Sie in der Liste einen Feldwert von "Transaktionsbetrag" aus
31. Geben Sie im Feld "Feld" einen Wert ein, oder wählen Sie einen Wert aus.
32. Wählen Sie im Feld "Funktion zusammenführen" die Option "Summe" aus.
33. Klicken Sie auf die Registerkarte "Gruppieren nach".
34. Klicken Sie auf Hinzufügen.
35. Wählen Sie in der Liste einen Wert von "Mitarbeiter" aus  
36. Klicken Sie auf Hinzufügen.
37. Wählen Sie in der Liste einen Wert von "Ausgabenkategorie" aus
38. Geben Sie im Feld "Feld" einen Wert ein, oder wählen Sie einen Wert aus.
39. Klicken Sie auf die Registerkarte "Haben".
40. Klicken Sie auf Hinzufügen.
41. Wählen Sie den "Transaktionsbetrag" aus
42. Geben Sie im Feld "Feld" einen Wert ein, oder wählen Sie einen Wert aus.
43. Wählen Sie im Feld "Funktion zusammenführen" die Option "Summe" aus.
44. Geben Sie im Feld "Kriterien" den Wert ">2000" ein.
45. Klicken Sie auf "OK".
46. Klicken Sie auf Test.
47. Geben Sie im Feld "Startdatum für Dokumentauswahl" ein Datum und eine Uhrzeit ein.
48. Geben Sie im Feld "Enddatum für Dokumentauswahl" ein Datum und eine Uhrzeit ein.
49. Klicken Sie auf "Test ausführen".
50. Klicken Sie im Aktivitätsbereich auf "Überwachungsrichtlinie".
51. Klicken Sie auf "Zusätzliche Optionen".
52. Geben Sie im Feld "Startdatum" ein Datum und eine Uhrzeit ein.
53. Geben Sie im Feld "Enddatum" ein Datum und eine Uhrzeit ein.
54. Klicken Sie auf "Charge".
55. Erweitern Sie den Abschnitt "Ausführen im Hintergrund".
56. Wählen Sie "Ja" im Feld "Stapelverarbeitung" aus.
57. Klicken Sie auf "OK".
58. Wechseln Sie zu "Überwachungsworkbench" > "Überwachungsanfragen".
59. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
60. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
61. Erweitern Sie den Abschnitt "Zuordnungen".
62. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
63. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.


