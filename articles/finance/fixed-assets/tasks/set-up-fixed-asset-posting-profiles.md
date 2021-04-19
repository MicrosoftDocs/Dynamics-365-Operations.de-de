---
title: Einrichten von Anlagenbuchungsprofilen
description: Mit dieser Aufgabenanleitung werden "Anlagenbuchungsprofile" eingerichtet.
author: saraschi2
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f02aa936b7d485dd8c76225b5c4de02a238f9352
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813554"
---
# <a name="set-up-fixed-asset-posting-profiles"></a>Einrichten von Anlagenbuchungsprofilen

[!include [banner](../../includes/banner.md)]

Mit dieser Aufgabenanleitung werden "Anlagenbuchungsprofile" eingerichtet.  Dabei werden die "Buchhalterrolle" und die Demodaten für die juristische Person USMF verwendet.  Die Beispiele, die in der Aufgabenanleitung angegeben sind, sind für ein grundlegendes Buchungsprofil, obwohl Buchungsprofile für Ihren speziellen Kontenplans und Ihre Finanzberichterstellungsanforderungen erstellt werden müssen.

1. Wechseln Sie im Navigationsbereich zu **Module > Anlagen > Einstellungen > Anlagenbuchungsprofile**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Buchungsprofil** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein. Sie müssen ein Buchungsprofil für jeden Anlagentransaktionstyp erstellen, den Sie beim Arbeiten mit Anlagen verwenden. Diese Aufgabenanleitung beginnt mit dem Transaktionstyp "Anschaffung".  
5. Klicken Sie in der Symbolleiste auf **Hinzufügen**.
6. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus. Das Feld **Gruppierungen** ermöglicht es Ihnen, das Buchungsprofil bis hinunter zu „Tabelle“ (ein Konto für jede Anlage) oder „Gruppe“ (ein Konto für jede Anlagengruppe) zu definieren. Lassen Sie für diesen Aufgabenleitfaden den Wert auf „Alle“ festgelegt, damit er für alle Anlagen mit dem angegebenen Buch angewendet wird.  
7. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an. Für Anschaffungen können Sie ein Gegenkonto eingeben oder das Feld leer lassen, damit es für die spezifische Buchung ausgefüllt wird.    
8. Wählen Sie im Dropdownmenü unter dem Inforegister **Sachkonten** die Option „Anschaffungsregulierung“ aus. Für Anschaffungsregulierungsbuchungen verwenden wir dieselben Konten, die für Anschaffungsbuchungen verwendet werden.  
9. Klicken Sie auf **Hinzufügen**.
10. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
11. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an. Für Anschaffungsregulierungen können Sie ein Gegenkonto eingeben oder das Feld leer lassen, damit es für die spezifische Buchung ausgefüllt wird.    
12. Wählen Sie im Dropdownmenü unter dem Inforegister **Sachkonten** die Option „Abschreibung“ aus.
13. Klicken Sie auf **Hinzufügen**.
14. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
15. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an.
16. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
17. Wählen Sie im Dropdownmenü unter dem Inforegister **Sachkonten** die Option „Abschreibungsregulierung“ aus. Für Abschreibungsregulierungsbuchungen verwenden wir dieselben Konten, die für Abschreibungsbuchungen verwendet werden.  
18. Klicken Sie auf **Hinzufügen**.
19. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
20. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an.
21. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
22. Wählen Sie im Dropdownmenü unter dem Inforegister **Sachkonten** die Option „Veräußerung“ aus.
23. Klicken Sie auf **Hinzufügen**.
24. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
25. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an. Für Veräußerungen können Sie ein Gegenkonto eingeben oder das Feld leer lassen, damit es für die spezifische Buchung ausgefüllt wird.  
26. Wählen Sie im Dropdownmenü unter dem Inforegister **Sachkonten** die Option „Verschrottung“ aus. Verwenden Sie für „Veräußerung“ und „Verschrottung“ dieselben Konten.  
27. Klicken Sie auf **Hinzufügen**.
28. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
29. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an. Für Veräußerungen können Sie ein Gegenkonto eingeben oder das Feld leer lassen, damit es für die spezifische Buchung ausgefüllt wird.  
30. Erweitern Sie das Inforegister **Abgang**. Sie müssen Veräußerungsbuchungsprofile sowohl für Veräußerung als auch Verschrottung einrichten.  Wir beginnen mit Veräußerungsverkaufstransaktionen.  
31. Klicken Sie auf **Hinzufügen**.
32. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
33. Wählen Sie im Feld **Wert buchen** die Option „Anschaffungswert“ aus.
    * Anschaffungswert adressiert Anschaffungs- und Anschaffungsregulierungswerte für alle Jahre. Sie können auch Konten für diese Transaktionsarten getrennt definieren.  
    * Sie können den Veräußerungsprozess so festlegen, dass er verschiedene Konten verwendet, je nachdem, ob die Veräußerung einen Gewinn oder Verlust ergibt. Ich werde den „Verkaufswerttyp“ auf „Alle“ festlegen, um die gleichen Konten für alle Typen von Veräußerungen zu verwenden.  
34. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an.
35. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
36. Klicken Sie auf **Hinzufügen**.
37. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
38. Wählen Sie im Feld **Wert buchen** die Option „Abschreibung (frühere Jahre)“ aus.  
38. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an.
39. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
40. Klicken Sie auf **Hinzufügen**.
41. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
42. Wählen Sie im Feld **Wert buchen** die Option „Abschreibung (dieses Jahr)“ aus.
43. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an.
44. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
45. Klicken Sie auf **Hinzufügen**.
46. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
47. Wählen Sie im Feld **Wert buchen** die Option „Abschreibungsregulierungen (frühere Jahre)“ aus.
48. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an.
49. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
50. Klicken Sie auf **Hinzufügen**.
51. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
52. Wählen Sie im Feld **Wert buchen** die Option „Abschreibungsregulierungen (dieses Jahr)“ aus.
53. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an.
54. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
55. Klicken Sie auf **Hinzufügen**.
56. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
57. Wählen Sie im Feld **Wert buchen** die Option „Nettobuchwert“ aus.
58. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an.
59. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
60. Wählen Sie im Feld **Veräußerung oder Verschrottung** die Option „Verschrottung“ aus.
61. Klicken Sie auf **Hinzufügen**.
62. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
63. Wählen Sie im Feld **Wert buchen** die Option „Anschaffungswert“ aus.
64. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an.
65. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
66. Klicken Sie auf **Hinzufügen**.
67. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
67. Wählen Sie im Feld **Wert buchen** die Option „Abschreibung (frühere Jahre)“ aus.  
68. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an.
69. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
70. Klicken Sie auf **Hinzufügen**.
71. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
72. Wählen Sie im Feld **Wert buchen** die Option „Abschreibung (dieses Jahr)“ aus.
73. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an.
74. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
75. Klicken Sie auf **Hinzufügen**.
76. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
77. Wählen Sie im Feld **Wert buchen** die Option „Abschreibungsregulierungen (frühere Jahre)“ aus.
78. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an.
79. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
80. Klicken Sie auf **Hinzufügen**.
81. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
82. Wählen Sie im Feld **Wert buchen** die Option „Abschreibungsregulierungen (dieses Jahr)“ aus.
83. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an.
84. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.
85. Klicken Sie auf **Hinzufügen**.
86. Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.
87. Wählen Sie im Feld **Wert buchen** die Option „Nettobuchwert“ aus.
88. Geben Sie im Feld **Hauptkonto** die gewünschten Werte an.
89. Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]