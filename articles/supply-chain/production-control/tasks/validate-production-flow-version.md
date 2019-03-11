---
title: Produktionsfluss und Version überprüfen
description: Die Prozedur zeigt, wie ein neuer Produktionsfluss und eine erste Version für Lean Manufacturing erstellt werden.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ae4c5f55d317a99e23ba6e76fc50ddece1e55a1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "352849"
---
# <a name="validate-a-production-flow-and-version"></a>Produktionsfluss und Version überprüfen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Die Prozedur zeigt, wie ein neuer Produktionsfluss und eine erste Version für Lean Manufacturing erstellt werden. Voraussetzungen: Die Produktionsparameter für Lean Manufacturing und die Maßeinheiten der Klasse "Zeit" müssen definiert werden. Sie müssen einen Wertstrom und ein Produktionsbuchungsprofil definieren. Informationen finden Sie in den Whitepapers zu Lean Manufacturing, um sich mit den Konzepten von Produktionsflüssen und Aktivitäten vertraut zu machen. Diese Prozedur bezieht sich auf die juristische Person USMF in den Demodaten. Jedoch angenommen, dass die juristische Person für Lean Manufacturing konfiguriert ist, können andere juristische Personen verwendet werden.


## <a name="create-a-production-flow"></a>Einen Produktionsfluss erstellen
1. Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Ein Wertstrom ist eine Organisationseinheit, die alle Aktivitäten und Flüsse des Wertstroms umfasst.   Gegenwärtig werden Organisationseinheiten auf eine juristische Person beschränkt und haben keine weitere Funktion.  
7. Klicken Sie im Feld "Produktionsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Produktionsgruppen ermöglichen die Definition von Material, Arbeit und RIF-Konten für einen Produktionsprozess. Um den Buchhaltungskontext zu einem Produktionsfluss zuzuordnen, muss eine Produktionsgruppe ausgewählt werden.  
9. Klicken Sie auf "Speichern".

## <a name="create-a-production-flow-version"></a>Eine Produktionsflussversion erstellen
1. Klicken Sie auf Hinzufügen.
2. Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.
    * Sie können das Ablaufdatum der Version auch für aktive Versionen zu einem beliebigen Zeitpunkt aktualisieren. Verwenden Sie den Ablauf der Version, um eine Phase außerhalb einer Version zu planen.  
3. Klicken Sie auf "OK".
4. Markieren Sie in der Liste die ausgewählte Zeile.
5. Geben Sie im Feld "Einheiten" einen Wert ein.
6. Wählen Sie die Takteinheit.
7. Geben Sie eine Zahl in das Feld "Durchschnittliche Taktzeit" ein.
    * Für die Taktkontrolle der Produktionsflussversion , definieren Sie die geplante durchschnittliche Taktzeit.   Der Takt wird als Menge pro Zeitperiode definiert.  Im vorliegenden Beispiel ist die Taktzeit 0,2 Stunden pro 10 Stück. Bei einer Arbeitszeit von 8 Stunden, entspricht dies einer täglichen Durchsatzkapazität von 400 Stück.  
8. Geben Sie im Feld "Menge pro Zyklus" eine Zahl ein.
9. Erweitern oder reduzieren Sie den Abschnitt "Versionsdetails".
10. Geben Sie eine Zahl in das Feld "Minimale Taktzeit" ein.
    * Die Mindesttaktzeit muss kleiner oder gleich der durchschnittlichen Taktzeit sein.  
11. Geben Sie eine Zahl in das Feld "Maximale Taktzeit" ein.
    * Die maximale Taktzeit muß größer oder gleich der durchschnittlichen Taktzeit sein.  
12. Geben Sie eine Anzahl von Tagen der Periode für tatsächliche Zykluszeit an.
    * Die Periode für tatsächliche Zykluszeit ist die Anzahl der Tage, in denen Einzelvorgänge ab der tatsächlichen Minute rückwärts erfasst werden, um die tatsächliche Zykluszeit zu berechnen. Der Wert kann jederzeit geändert werden und wird nur für die Berechnung der tatsächlichen Zykluszeiten verwendet.  
13. Klicken Sie auf "Speichern".

