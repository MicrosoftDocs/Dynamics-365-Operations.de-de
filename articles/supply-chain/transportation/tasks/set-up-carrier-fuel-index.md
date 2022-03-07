---
title: Spediteur-Kraftstoffindex einrichten
description: Dieses Handbuch zeigt, wie eine Kraftstoffindex-Region, ein Kraftstoffindex und einen Spediteur-Kraftstoffindex erstellt wird.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFuelIndexRegion,TMSCarrierFuelIndexTable,TMSFuelIndex
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1e972f2ba8211c47b11a4b83dac9ff60f813b1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837581"
---
# <a name="set-up-a-carrier-fuel-index"></a>Spediteur-Kraftstoffindex einrichten

[!include [banner](../../includes/banner.md)]

Dieses Handbuch zeigt, wie eine Kraftstoffindex-Region, ein Kraftstoffindex und einen Spediteur-Kraftstoffindex erstellt wird. Die Kraftstoffindex-Region gibt an, für welche Region der Kraftstoffindex gelten soll, und der Kraftstoffindex gibt einen Kraftstoffpreis für einen bestimmten Zeitraum an. Um die Änderung der Kraftstoffpreise im Laufe der Zeit wiederzugeben, können Sie einem Spediteur mehrere Kraftstoffindizes zuordnen.  Diese Aufgaben werden in der Regel von einem Transportkoordinator durchgeführt. Sie können diese Prozedur im Demodatenunternehmen USMF oder mit eigenen Daten verwenden.


## <a name="create-a-fuel-index-region"></a>Erstellen einer Kraftstoffindex-Region
1. Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Kraftstoffindizes" > "Kraftstoffindex-Regionen".
    * Zunächst müssen Sie die verschiedenen Regionen erstellen, in denen Sie arbeiten, und verschiedene Benzinzuschläge berechnen.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Region" einen Wert ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Klicken Sie auf "Speichern".

## <a name="create-a-fuel-index"></a>Erstellen eines Kraftstoffindex
1. Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Kraftstoffindizes" > "Kraftstoffindizes".
    * Für die eingerichteten Regionen müssen Sie die aktuellen Preise für den Kraftstoff eingeben.  
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Region" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Geben Sie im Feld "Preis pro Liter" eine Zahl ein.
6. Geben Sie im Feld "Effektives Startdatum und -uhrzeit" ein Datum und eine Uhrzeit ein.
7. Klicken Sie auf "Speichern".

## <a name="create-a-carrier-fuel-index"></a>Erstellen eines Spediteur-Kraftstoffindex
1. Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Kraftstoffindizes" > "Spediteur-Kraftstoffindizes".
2. Klicken Sie auf "Neu".
3. Geben Sie einen Wert in das Feld "Spediteur-Kraftstoffindex" ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie auf Neu.
6. Geben Sie im Feld "Effektives Startdatum und -uhrzeit" ein Datum und eine Uhrzeit ein.
7. Geben Sie im Feld "PPG von" eine Zahl ein.
    * In diesem Beispiel können Sie das Feld "PPG von" auf "1,95" festlegen.  
8. Geben Sie im Feld "PPG bis" eine Zahl ein.
    * In diesem Beispiel können Sie das Feld "PPG bis" auf "2" festlegen.  
9. Geben Sie im Feld "Prozentsatz" eine Zahl ein.
    * In diesem Beispiel können Sie "Prozentsatz" auf "3" festlegen.  
10. Klicken Sie im Feld "Währung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
12. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
13. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]