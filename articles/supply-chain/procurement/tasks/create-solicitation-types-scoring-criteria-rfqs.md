---
title: Ausschreibungstypen und Bewertungskriterien für Angebotsanforderungen erstellen
description: Dieser Leitfaden zeigt Ihnen, wie man einen Ausschreibungstyp erstellt und diesen einer Bewertungsmethode zuordnet.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf196711799b78d7f4106b6693127d7f356b1d4e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262212"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>Ausschreibungstypen und Bewertungskriterien für Angebotsanforderungen erstellen

[!include [banner](../../includes/banner.md)]

Dieser Leitfaden zeigt Ihnen, wie man einen Ausschreibungstyp erstellt und diesen einer Bewertungsmethode zuordnet. Er zeigt auch, wie man den Ausschreibungstyp auf eine Angebotsanforderung anwendet, wodurch die Standardbewertungsmethode festgelegt wird. Diese Aufgaben werden normalerweise von einem Einkaufsleiter ausgeführt. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden. Sie müssen eine Bewertungsmethode verfügbar haben, bevor Sie beginnen.


## <a name="create-a-solicitation-type"></a>Erstellt eines neuen Anforderungstyps
1. Wechseln Sie zu Beschaffung > Einstellungen > Angebotsanforderung > Anforderungstyp.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie im Feld "Bewertungsmethode" die Bewertungsmethode aus, die Sie für diesen Ausschreibungstyp verwenden möchten.
6. Klicken Sie auf "Speichern".
7. Schließen Sie die Seite.

## <a name="use-the-solicitation-type"></a>Den Ausschreibungstyp verwenden
1. Wechseln Sie zu "Beschaffung" > "Angebotsanforderungen" > "Alle Angebotsanforderungen".
2. Klicken Sie auf "Neu".
3. Wählen Sie im Feld "Ausschreibungstyp" den Ausschreibungstyp aus, den Sie gerade erstellt haben. 
    *   
4. Klicken Sie auf "OK".
5. Klicken Sie auf "Bewertungskriterien".
    * Die Bewertungskriterien, die angezeigt werden, sind diejenigen von der Bewertungsmethode, die Sie dem Ausschreibungstyp zugeordnet haben. Auf dieser Seite können Sie auswählen, Kriterien hinzuzufügen oder zu löschen. Es ist auch möglich, neue Kriterien hinzuzufügen, indem Sie diese aus anderen Bewertungsmethoden kopieren.  
6. Klicken Sie auf "Kriterien kopieren".
7. Geben Sie im Feld "Bewertungsmethode" einen Wert ein, oder wählen Sie einen Wert aus.
8. Klicken Sie auf "OK".
9. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]