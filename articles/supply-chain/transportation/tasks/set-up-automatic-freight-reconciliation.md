--- 
title: Automatische Frachtabstimmung einrichten
description: "Dieses Verfahren zeigt, wie Daten für die automatische Frachtabstimmung eingerichtet werden."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 97f0c4d8fe06ab2fc252b9543cb688306214c79f
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-automatic-freight-reconciliation"></a>Automatische Frachtabstimmung einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie Daten für die automatische Frachtabstimmung eingerichtet werden. Dies wird normalerweise von einer Lagerortverwaltung erfolgt. Sie können diese Prozedur im Demodatunternehmen USMF verwenden.


## <a name="set-up-the-freight-bill-type"></a>Frachtbrieftyp einrichten
1. Wechseln Sie zu "Transportverwaltung" > "Einrichtung" > "Frachtabstimmung" > "Frachtbrieftyp".
    * Der Frachtbrieftyp definiert, wie Frachtbriefe und Spediteursrechnungen abgeglichen werden sollen.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Frachtbrieftyp" einen Wert ein.
4. Geben Sie im Feld "Modulassembly" 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer' ein.
    * Dies ist die Standardtransportverwaltungs-Zuordnungsmodul-Codebibliothek.  
5. Geben Sie im Feld "Modulklasse" 'Microsoft.Dynamics.Ax.Tms.dll' ein.
    * Dies ist die Standardtransportverwaltungs-Zuordnungsmodul-Klasse.  
6. Klicken Sie auf "Neu".
7. Wählen Sie im Feld "Beschreibung" den Wert aus, der auf dem Frachtbrief und der Spediteursrechnung übereinstimmen sollten.  
8. Wählen Sie "Ja" im Feld "Abgleich erforderlich" aus.
    * Wenn Sie dieses Feld auf "Ja" festgelegt haben, heißt dies, dass der Wert, der im Feld "Beschreibung" ausgewählt ist, dem Frachtbrief und der Spediteursrechnung entsprechen muss. Wenn Sie es auf "Nein" festlegen, kann das Feld für einen der Werte leer sein.  
9. Klicken Sie auf "Speichern".

## <a name="set-up-the-freight-bill-type-assignment"></a>Frachtbrieftypzuweisung einrichten
1. Schließen Sie die Seite.
2. Wechseln Sie zu "Transportverwaltung" > "Einrichtung" > "Frachtabstimmung" > "Frachtbrieftyp-Zuweisungen".
    * Die Frachtbrieftyp-Zuweisung wird verwendet, um anzugeben, welcher Frachtbrieftyp für einen bestimmten Spediteur verwendet wird.   
3. Klicken Sie auf "Neu".
4. Geben Sie im Feld 'Modus' einen Wert ein, oder wählen Sie einen Wert aus.
5. Geben Sie im Feld 'Spediteur' einen Wert ein, oder wählen Sie einen Wert aus.
6. Wählen Sie im Frachtbrieftyp-Feld den Frachtbrieftyp aus, den Sie eben erstellt haben.
7. Schließen Sie die Seite.

## <a name="set-up-the-audit-master"></a>Überwachungsmaster einrichten
1. Wechseln Sie zu "Transportverwaltung" > "Einrichtung" > "Frachtabstimmung" > "Überwachungsmaster".
    * Der Überwachungsmaster definiert die Toleranzgrenzen für die automatische Frachtabstimmung. Er gibt an, um wie viel die Geldbeträge auf dem Frachtbrief und in der Spediteursrechnung abweichen können, und noch eine Abstimmung zuzulassen. Er definiert auch, wie Abweichungen behandelt werden.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Überwachungsmasterkennung" einen Wert ein.
4. Wählen Sie im Spediteur-Feld den gleichen Spediteur aus, die Sie eben verwendet haben.
5. Wählen Sie im Frachtbrieftyp-Feld den Frachtbrieftyp aus, den Sie eben erstellt haben.
6. Erweitern Sie den Abschnitt "Toleranz".
7. Geben Sie im Feld "Minimale Toleranzstufe" eine Zahl ein.
8. Geben Sie im Feld "Maximale Toleranzstufe" eine Zahl ein.
9. Erweitern Sie den Abschnitt Ergebnis.
10. Geben Sie im Feld "Überzahlungs-Ursachencode" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Geldbeträge auf dem Frachtbrief und der Spediteursrechnung abweichen, enthalten die Über- oder Unterzahlungsursachencodes die Konten, für die die Differenz erfasst werden soll, sofern die Differenz innerhalb der Toleranzebenen ist.  
11. Geben Sie im Feld "Unterzahlungs-Ursachencode" einen Wert ein, oder wählen Sie einen Wert aus.
12. Schließen Sie die Seite.


