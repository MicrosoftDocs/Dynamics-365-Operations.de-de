--- 
title: Einrichten von Anlagenbuchungsprofilen
description: Mit dieser Aufgabenanleitung werden "Anlagenbuchungsprofile" eingerichtet.
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b9766d96d16429d0ce0864695a3157f54cad4054
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-fixed-asset-posting-profiles"></a>Einrichten von Anlagenbuchungsprofilen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Mit dieser Aufgabenanleitung werden "Anlagenbuchungsprofile" eingerichtet.  Dabei werden die "Buchhalterrolle" und die Demodaten für die juristische Person USMF verwendet.  Die Beispiele, die in der Aufgabenanleitung angegeben sind, sind für ein grundlegendes Buchungsprofil, obwohl Buchungsprofile für Ihren speziellen Kontenplans und Ihre Finanzberichterstellungsanforderungen erstellt werden müssen.

1. Wechseln Sie zu Anlagen > Einstellungen > Anlagenbuchungsprofile.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Buchungsprofil" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Sie müssen ein Buchungsprofil für jeden Anlagentransaktionstyp erstellen, den Sie beim Arbeiten mit Anlagen verwenden.  Diese Aufgabenanleitung beginnt mit dem Transaktionstyp "Anschaffung".  
5. Klicken Sie auf Hinzufügen.
6. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
    * Das Feld "Gruppierungen" ermöglicht es Ihnen, das Buchungsprofil hinunter zur "Tabelle" (ein Konto, das für jede Anlage eingerichtet wird) oder "Gruppe" (ein Konto, das für jede Anlagengruppe eingerichtet ist) zu definieren.  Für diesen Aufgabenleitfaden lasse ich den Wert auf „Alle” festgelegt, damit er für alle Anlagen mit dem angegebenen Buch angewendet wird.  
7. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
    * Für "Anschaffungen" können Sie ein Gegenkonto eingeben oder es leer lassen, damit es für die spezielle Transaktion ausgefüllt wird.    
8. Wählen Sie im Feld "Transaktionstyp" die Option "Anschaffungsregulierung" aus.
    * Für "Anschaffungsregulierungstransaktionen" verwenden wir dieselben Konten, die für "Anschaffungstransaktionen" verwendet werden.  
9. Klicken Sie auf Hinzufügen.
10. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
11. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
    * Für "Anschaffungsregulierungen" können Sie ein Gegenkonto eingeben oder es leer lassen, damit es für die spezielle Transaktion ausgefüllt wird.    
12. Wählen Sie im Feld "Transaktionstyp" die Option "Abschreibung" aus.
13. Klicken Sie auf Hinzufügen.
14. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
15. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
16. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.
17. Wählen Sie im Feld "Transaktionstyp" die Option "Abschreibungsregulierung" aus.
    * Für "Abschreibungsregulierungstransaktionen" verwenden wir dieselben Konten, die für "Abschreibungstransaktionen" verwendet werden.  
18. Klicken Sie auf Hinzufügen.
19. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
20. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
21. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.
22. Wählen Sie im Feld "Transaktionstyp" die Option "Veräußerung" aus.
23. Klicken Sie auf Hinzufügen.
24. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
25. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
    * Für "Veräußerungen" können Sie ein Gegenkonto eingeben oder es leer lassen, damit es für die spezielle Transaktion ausgefüllt wird.  
26. Wählen Sie im Feld "Transaktionstyp" die Option "Verschrottung" aus.
    * Wir verwenden dieselben Konten für "Veräußerung" und "Verschrottung".  
27. Klicken Sie auf Hinzufügen.
28. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
29. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
    * Für "Veräußerungen" können Sie ein Gegenkonto eingeben oder es leer lassen, damit es für die spezielle Transaktion ausgefüllt wird.  
30. Erweitern Sie den Abschnitt „Abgang”.
    * Sie müssen Veräußerungsbuchungsprofile sowohl für Veräußerung als auch Verschrottung einrichten.  Wir beginnen mit Veräußerungsverkaufstransaktionen.  
31. Klicken Sie auf Hinzufügen.
32. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
33. Wählen Sie im Feld "Buchungswert" die Option "Anschaffungswert" aus.
    * Anschaffungswert adressiert Anschaffungs- und Anschaffungsregulierungswerte für alle Jahre.  Sie können auch Konten für diese Transaktionsarten getrennt definieren.  
    * Sie können den Veräußerungsprozess so festlegen, dass er verschiedene Konten verwendet, je nachdem, ob die Veräußerung einen Gewinn oder Verlust ergibt.  Ich werde den "Verkaufswerttyp" auf "Alle" festlegen, um die gleichen Konten für alle Typen von Veräußerungen zu verwenden.  
34. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
35. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.
36. Klicken Sie auf Hinzufügen.
37. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie im Feld "Wert buchen" die Option "Abschreibung (frühere Jahre)" aus.  
38. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
39. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.
40. Klicken Sie auf Hinzufügen.
41. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
42. Wählen Sie im Feld "Wert buchen" die Option "Abschreibung (dieses Jahr)" aus.
43. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
44. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.
45. Klicken Sie auf Hinzufügen.
46. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
47. Wählen Sie im Feld "Wert buchen" die Option "Abschreibungsregulierungen (frühere Jahre)" aus.
48. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
49. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.
50. Klicken Sie auf Hinzufügen.
51. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
52. Wählen Sie im Feld "Wert buchen" die Option "Abschreibungsregulierungen (dieses Jahr)" aus.
53. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
54. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.
55. Klicken Sie auf Hinzufügen.
56. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
57. Wählen Sie im Feld "Buchungswert" die Option "Nettobuchwert" aus.
58. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
59. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.
60. Wählen Sie im Feld "Veräußerung oder Verschrottung" die Option "Verschrottung" aus.
61. Klicken Sie auf Hinzufügen.
62. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
63. Wählen Sie im Feld "Buchungswert" die Option "Anschaffungswert" aus.
64. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
65. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.
66. Klicken Sie auf Hinzufügen.
67. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie im Feld "Wert buchen" die Option "Abschreibung (frühere Jahre)" aus.  
68. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
69. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.
70. Klicken Sie auf Hinzufügen.
71. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
72. Wählen Sie im Feld "Wert buchen" die Option "Abschreibung (dieses Jahr)" aus.
73. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
74. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.
75. Klicken Sie auf Hinzufügen.
76. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
77. Wählen Sie im Feld "Wert buchen" die Option "Abschreibungsregulierungen (frühere Jahre)" aus.
78. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
79. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.
80. Klicken Sie auf Hinzufügen.
81. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
82. Wählen Sie im Feld "Wert buchen" die Option "Abschreibungsregulierungen (dieses Jahr)" aus.
83. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
84. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.
85. Klicken Sie auf Hinzufügen.
86. Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.
87. Wählen Sie im Feld "Buchungswert" die Option "Nettobuchwert" aus.
88. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
89. Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.


