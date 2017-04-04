---
title: "Zusätzliche Anschaffungsabschreibung"
description: "In diesem Artikel wird beschrieben, wie die Abschreibung für zusätzliche Anschaffungen in Deutschland berechnet wird und gibt ein Beispiel. Anschaffungregulierungen für Anlagen müssen so kalkuliert werden, als ob die Regulierungen am ersten Tag des Geschäftsjahres vorgenommen wurden, unabhängig davon, wann die Regulierungsbuchungen tatsächlich erstellt wurden."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12791
ms.assetid: b8e17c7a-917c-4016-87a5-27c34ccde941
ms.search.region: Germany
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: d4e256c47e57054be000d1d49dc672f0de4c1577
ms.lasthandoff: 03/31/2017


---

# <a name="additional-acquisition-depreciation"></a>Zusätzliche Anschaffungsabschreibung

In diesem Artikel wird beschrieben, wie die Abschreibung für zusätzliche Anschaffungen in Deutschland berechnet wird und gibt ein Beispiel. Anschaffungregulierungen für Anlagen müssen so kalkuliert werden, als ob die Regulierungen am ersten Tag des Geschäftsjahres vorgenommen wurden, unabhängig davon, wann die Regulierungsbuchungen tatsächlich erstellt wurden.

Anschaffungregulierungen für Anlagen müssen so kalkuliert werden, als ob die Regulierungen am ersten Tag des Geschäftsjahres vorgenommen wurden, unabhängig davon, wann die Regulierungsbuchungen tatsächlich erstellt wurden. Die folgende Formel wird verwendet, um den Grundbetrag der Anlage zur Abschreibung zu berechnen: Nettobuchwert der Anlage am letzten Tag des vorherigen Geschäftsjahres + alle Anschaffungsänderungen für die Anlage im aktuellen Jahr.

## <a name="example"></a>Beispiel
Im Jahre 2015 erwarb Ihre Organisation eine Anlage für 60.000. Ihre Organisation verwendet die Abschreibungsmethode "Verbleibende lineare Nutzungsdauer" über fünf Jahre. Im Jahre 2015 wenn Sie den Abschreibungsvorschlag jeden Monat 1.000 verarbeiten, wird als der Monatsabschreibungsbetrag berechnet (60.000 × 12\]\[5). Im März 2016 buchen Sie eine zusätzliche Anschaffung für die Anlage. Der Betrag der zusätzlichen Anschaffung beträgt 12.000. Sie können die Anschaffung müssen zusätzliche, als ob sie am 1. Januar 2016 gebucht wurde. Daher ist hier, wie die monatliche Abschreibung von 12.000 für die restlichen vier Jahre berechnet werden muss: 12.000 ÷ (4 × 12) = 250,welche die tatsächliche Abschreibung der zusätzlichen Anschaffung nur im Monat beginnen kann, wenn die zusätzlichen Anschaffung aufgetreten ist (für). Daher müssen die Abschreibungsbeträge für Januar und Februar dem Abschreibungsbetrag für März hinzugefügt werden. In der folgenden Tabelle werden die Monatsabschreibungsbeträge für die ursprüngliche Anschaffung und die Anschaffungsregulierung für die ersten fünf Monate des Jahres angezeigt.

| Monat         | Monatsabschreibungsbetrag für die ursprüngliche Anschaffung in Höhe von 60.000 | Monatsabschreibungsbetrag für die Anschaffungsregulierung in Höhe von 12.000 | Gesamtabschreibungsbetrag |
|---------------|-----------------------------------------------------------------|-------------------------------------------------------------------|---------------------------|
| Januar 2016  | 1.000                                                           | 0                                                                 | 1.000                     |
| Februar 2016 | 1.000                                                           | 0                                                                 | 1.000                     |
| März 2016    | 1.000                                                           | 250 für Januar, 250 für Februar und 250 für März              | 1,750                     |
| April 2016    | 1.000                                                           | 250                                                               | 1,250                     |
| Mai 2016      | 1.000                                                           | 250                                                               | 1,250                     |




