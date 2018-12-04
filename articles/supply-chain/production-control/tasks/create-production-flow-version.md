--- 
title: Eine Produktionsflussversion erstellen
description: Ziel dieser Prozedur ist es, eine neue Produktionsflussversion zu erstellen.
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8903e618a35e66742b5c2ebcb5b6f0da3853fcaf
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---
# <a name="create-a-production-flow-version"></a>Eine Produktionsflussversion erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ziel dieser Prozedur ist es, eine neue Produktionsflussversion zu erstellen. Für diese Prozedur müssen die Produktionsparameter für Lean Manufacturing und die Messungseinheiten der Klasse "Zeit" definiert werden. Sie müssen auch einen Wertstrom und eine Produktionsgruppe definieren. Weitere Informationen zu Produktionsflüssen und Aktivitäten im Lean Manufacturing, finden Sie im Whitepaper Lean Manufactoring für Microsoft Dynamics AX. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-a-production-flow"></a>Einen Produktionsfluss erstellen
1. Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie eine Organisationseinheit vom Typ "Wertstrom" aus. Ein Wertstrom ist eine Organisationseinheit, die alle Aktivitäten und Flüsse des Wertstroms umfasst. Gegenwärtig werden Organisationseinheiten auf eine juristische Person beschränkt und haben keine weitere Funktion.  
7. Klicken Sie im Feld "Produktionsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie eine Produktionsgruppe für den Produktionsfluss. Produktionsgruppen ermöglichen die Definition von Material, Arbeit und RIF-Konten für einen Produktionsprozess. Um den Buchhaltungskontext zu einem Produktionsfluss zuzuordnen, muss eine Produktionsgruppe ausgewählt werden.  
9. Klicken Sie auf "Speichern".

## <a name="create-a-production-flow-version"></a>Eine Produktionsflussversion erstellen
1. Klicken Sie auf Hinzufügen.
2. Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.
    * Bei Bedarf definieren Sie ein Ablaufdatum für die Version. Sie können sie zu jedem beliebigen Zeitpunkt eine Aktualisierung durchführen, auch bei aktiven Versionen. Sie können sie verwenden, um das Ersetzen einer Version zu planen.  
3. Klicken Sie auf "OK".
4. Markieren Sie in der Liste die ausgewählte Zeile.
5. Geben Sie im Feld "Einheiten" einen Wert ein.
6. ResolveChanges the Takt-Einheit.
7. Geben Sie eine Zahl in das Feld "Durchschnittliche Taktzeit" ein.
    * Definieren Sie die durchschnittliche Taktzeit der Version. Für die Taktkontrolle der Produktionsflussversion , definieren Sie die geplante durchschnittliche Taktzeit. Der Takt wird als Menge pro Zeitperiode definiert. Im Beispiel ist die Taktzeit 0,2 Stunden pro 10 Stück. Bei einer Arbeitszeit von 8 Stunden, entspricht dies einer täglichen Durchsatzkapazität von 400 Stück.  
8. Geben Sie im Feld "Menge pro Zyklus" eine Zahl ein.
    * Definieren Sie die Menge pro Zyklus, die der durchschnittlichen Taktzeit zugeordnet ist.  
9. Schalten Sie die Erweiterung des Abschnitts "Version" ein/aus.
10. Geben Sie eine Zahl in das Feld "Minimale Taktzeit" ein.
    * Definieren Sie die Mindesttaktzeit. Die Mindesttaktzeit muss kleiner oder gleich der durchschnittlichen Taktzeit sein.  
11. Geben Sie eine Zahl in das Feld "Maximale Taktzeit" ein.
    * Die maximale Taktzeit muß größer oder gleich der durchschnittlichen Taktzeit sein.  
12. Geben Sie im Feld "Periode für tatsächliche Zykluszeit (Tage)" eine Zahl an.
    * Geben Sie die Anzahl von Tagen der Periode für tatsächliche Zykluszeit an. Die Periode für tatsächliche Zykluszeit ist die Anzahl der Tage, in denen Einzelvorgänge ab der tatsächlichen Minute rückwärts erfasst werden, um die tatsächliche Zykluszeit zu berechnen. Der Wert kann jederzeit geändert werden und wird nur für die Berechnung der tatsächlichen Zykluszeiten verwendet.  
13. Klicken Sie auf "Speichern".


