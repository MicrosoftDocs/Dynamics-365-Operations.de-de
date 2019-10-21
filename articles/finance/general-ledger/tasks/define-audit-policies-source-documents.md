---
title: Überwachungsrichtlinien für Quelldokumente definieren
description: Dieses Thema erklärt, wie und Überwachungsrichtlinienregeln eingerichtet und ausgeführt werden.
author: ryansandness
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6b0fa28d778a4d9fa1f718b1d50bf1dce00be00
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186117"
---
# <a name="define-audit-policies-for-source-documents"></a>Überwachungsrichtlinien für Quelldokumente definieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Thema erklärt, wie und Überwachungsrichtlinienregeln eingerichtet und ausgeführt werden. Das Beispiel verwendet Spesenabrechnungen mit dem Hotelausgabentyp. Für diese Prozedur wird das Demo-Unternehmen USMF verwendet. Die Wirtschaftsprüferrolle umfasst die richtigen Berechtigungen, um diese Aufgaben auszuführen.

1. Gehen Sie im Navigationsbereich zu **Module > Überwachungs-Workbench > Einstellungen > Richtlinienregeltyp**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Regelname** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Wählen Sie im Feld **Abfragename** **Spesenabrechnungsposition** aus
6. Wählen Sie im Feld **Abfragetyp** **Zusammenführen** aus
7. Wählen Sie im Feld **Juristische Person** die Option **Juristische Person** aus.
8. Wählen Sie im Feld **Dokumentdatumsreferenz** die Option **Änderungsdatum und -uhrzeit** aus
9. Wählen Sie **Speichern**.
10. Gehen Sie im Navigationsbereich zu **Module > Überwachungs-Workbench > Einstellungen > Überwachungsrichtlinien**.
11. Wählen Sie **Neu** aus.
12. Geben Sie im Feld **Name** einen Wert ein.
13. Erweitern Sie den Abschnitt **Richtlinienorganisationen**.
14. Wählen Sie in der Struktur **Contoso Unterhaltungsanlagen USA** aus, und wählen Sie dann **Hinzufügen** aus.
15. Wählen Sie in der Struktur **Contoso Beratung USA** aus, und wählen Sie dann **Hinzufügen** aus.
16. Wählen Sie in der Struktur **Contoso Einzelhandel USA** aus, und wählen Sie dann **Hinzufügen** aus.
17. Reduzieren Sie den Abschnitt **Richtlinienorganisationen**.
18. Erweitern Sie den Abschnitt **Richtlinienregeln**.
19. Suchen Sie in der Liste die zuvor erstellte "Richtlinienregel" und wählen Sie diese aus.
20. Wählen Sie **Richtlinienregel erstellen** aus.
21. Geben Sie im Feld **Gültigkeitsdatum** ein Datum und eine Uhrzeit ein.
22. Wählen Sie **Filter** aus.
23. Wählen Sie in der Liste die Zeile für **Spesenkategorie** aus, und legen Sie die Details zum **Hotel** fest.
24. Geben Sie im Feld **Kriterien** einen Wert ein, oder wählen Sie einen Wert aus.
25. Wählen Sie die Registerkarte **Zusammenführen** aus.
26. Wählen Sie **Hinzufügen** aus.
27. Wählen Sie in der Liste einen Feldwert von **Buchungsbetrag** aus.
28. Geben Sie im Feld **Feld** einen Wert ein, oder wählen Sie einen Wert aus.
29. Wählen Sie im Feld **Funktion zusammenführen** die Option **Summe** aus.
30. Wählen Sie die Registerkarte **Gruppieren nach** aus.
31. Wählen Sie **Hinzufügen** aus.
32. Wählen Sie in der Liste einen Wert von **Mitarbeiter** aus.
33. Wählen Sie **Hinzufügen** aus.
34. Wählen Sie in der Liste einen Wert von **Ausgabenkategorie** aus.
35. Geben Sie im Feld **Feld** einen Wert ein, oder wählen Sie einen Wert aus.
36. Wählen Sie die Registerkarte **Haben** aus.
37. Wählen Sie **Hinzufügen** aus.
38. Wählen Sie **Transaktionsbetrag** aus.
39. Geben Sie im Feld **Feld** einen Wert ein, oder wählen Sie einen Wert aus.
40. Wählen Sie im Feld **Funktion zusammenführen** die Option **Summe** aus.
41. Geben Sie im Feld **Kriterien** `>2000` ein.
42. Wählen Sie **OK**.
43. Wählen Sie **Testen** aus.
44. Geben Sie im Feld **Startdatum für Dokumentauswahl** ein Datum und eine Uhrzeit ein.
45. Geben Sie im Feld **Enddatum für Dokumentauswahl** ein Datum und eine Uhrzeit ein.
46. Wählen Sie **Test ausführen** aus.
47. Wählen Sie im Aktivitätsbereich **Überwachungsrichtlinie** aus.
48. Wählen Sie **Weitere Optionen** aus.
49. Geben Sie im Feld **Startdatum** ein Datum und eine Uhrzeit ein.
50. Geben Sie im Feld **Enddatum** ein Datum und eine Uhrzeit ein.
51. Wählen Sie **Charge** aus.
52. Erweitern Sie den Abschnitt **Im Hintergrund ausführen**.
53. Wählen Sie **Ja** im Feld **Stapelverarbeitung** aus.
54. Wählen Sie **OK**.
55. Gehen Sie im Navigationsbereich zu **Module > Überwachungs-Workbench > Überwachungsanfragen**.
56. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
57. Erweitern Sie den Abschnitt **Zuordnungen**.
58. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.

