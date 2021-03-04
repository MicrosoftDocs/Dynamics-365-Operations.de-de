---
title: Automatische Frachtabstimmung einrichten
description: Dieses Verfahren zeigt, wie Daten für die automatische Frachtabstimmung eingerichtet werden.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f11edc15821faad84485d5b81e4a9ded0b7e974
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428489"
---
# <a name="set-up-automatic-freight-reconciliation"></a>Automatische Frachtabstimmung einrichten

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt, wie Daten für die automatische Frachtabstimmung eingerichtet werden. Dies wird normalerweise von einer Lagerortverwaltung erfolgt. Sie können diese Prozedur im Demodatunternehmen USMF verwenden.


## <a name="set-up-the-freight-bill-type"></a>Frachtbrieftyp einrichten
1. Wechseln Sie zu "Transportverwaltung" > "Einrichtung" > "Frachtabstimmung" > "Frachtbrieftyp".
    * Der Frachtbrieftyp definiert, wie Frachtbriefe und Spediteursrechnungen abgeglichen werden sollen.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Frachtbrieftyp" einen Wert ein.
4. Geben Sie im Feld "Modulklasse" den Typ 'Microsoft.Dynamics.Ax.Tms.dll' ein.
    * Dies ist die Standardtransportverwaltungs-Zuordnungsmodul-Codebibliothek.  
5. Geben Sie im Feld "Modulklasse" den Typ 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer' ein.
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]