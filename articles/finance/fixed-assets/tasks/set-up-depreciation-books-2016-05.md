---
title: Abschreibungsbücher einrichten
description: Bei diesem Verfahren wird ein neues Abschreibungsbuch erstellt und einer Anlagegruppe zugeordnet.
author: moaamer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a4713d949fe119cde1b1187a7c485d291281a8f
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725651"
---
# <a name="set-up-depreciation-books"></a>Abschreibungsbücher einrichten 

[!include [banner](../../includes/banner.md)]

Bei diesem Verfahren wird ein neues Abschreibungsbuch erstellt und einer Anlagegruppe zugeordnet. 

## <a name="create-a-depreciation-book"></a>Ein Abschreibungsbuch erstellen
1. Wechseln Sie zu "Anlagen" > "Einstellungen" > "Abschreibungsbücher".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Abschreibungsbuch" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Aktivieren oder deaktivieren Sie das Kontrollkästchen "Abschreibung berechnen".
6. Klicken Sie im Feld "Abschreibungsprofil" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Suchen Sie in der Liste das gewünschte Abschreibungsprofil und wählen Sie es aus.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Klicken Sie im Feld "Alternatives Abschreibungsprofil" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
10. Wählen Sie in der Liste das gewünschte Abschreibungsprofil aus.
11. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Das "Außerordentliche Abschreibungsprofil" wird für die zusätzliche Abschreibung einer Anlage unter besonderen Umständen verwendet. Sie können dieses Profil z. B. verwenden, um eine Abschreibung in Folge einer Naturkatastrophe zu erfassen.  
12. Aktivieren oder deaktivieren Sie das Kontrollkästchen "Abschreibungsregulierungen mit Basisregulierungen erstellen".
13. Klicken Sie im Feld "Kalender" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
14. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>Das Abschreibungsbuch einer Anlagengruppe zuordnen
1. Klicken Sie auf "Anlagengruppen".
2. Klicken Sie im Feld "Anlagengruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Wählen Sie im Feld "Abschreibungskonvention" eine Option aus.
6. Geben Sie im Feld "Nutzungsdauer" eine Zahl ein.
    * Beachten Sie, dass der Feldwert "Abschreibungszeiträume" nach der Festlegung der "Nutzungsdauer" berechnet wird.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
