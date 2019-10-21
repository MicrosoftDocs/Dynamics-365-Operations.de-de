---
title: Finanzdimensionen definieren
description: Dieser Aufgabenleitfaden veranschaulicht das Hinzufügen einer Finanzdimension und einer benutzerdefinierten Finanzdimension auf Basis einer Entität.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb2dc5df96198f3c9f68fcac70b2e5dcbe8c8832
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175441"
---
# <a name="define-financial-dimensions"></a>Finanzdimensionen definieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieser Aufgabenleitfaden veranschaulicht das Hinzufügen einer Finanzdimension und einer benutzerdefinierten Finanzdimension auf Basis einer Entität.  Der Leitfaden verwendet das Demounternehmen USMF.


## <a name="create-an-entity-backed-financial-dimension"></a>Erstellen einer Finanzdimension auf Basis einer Entität
1. Gehen Sie zu **Navigationsbereich > Module > Hauptbuch > Kontenplan > Dimensionen > Finanzdimensionen**.
2. Klicken Sie auf **Neu**.
3. Wählen Sie im Formularfeld **Benutzerwerte** eine vom System definierte Entität aus, auf der die Finanzdimension basieren soll. 
4. Geben Sie im Feld **Dimensionsname** einen Wert ein, um die Finanzdimension zu beschreiben. Der Name kann vom der im System definierte Entität abweichen. Er kann jedoch keine Leerzeichen und Sonderzeichen enthalten.
5. Klicken Sie auf **Aktivieren**. "Aktivieren der Finanzdimension" aktualisiert die Tabelle mit dem Finanzdimensionsnamen und entfernt gelöschte Dimensionen. Sie können Dimensionswerte eingegeben, bevor Sie eine Finanzdimension aktivieren, Finanzdimension kölnnen jedoch nicht verwendet werden, bis sie aktiviert sind.  
6. Klicken Sie auf **Schließen** auf der Aktivierungsnachricht.
7. Klicken Sie auf **Aktivieren**. Die Dimensionsaktivierung kann geplant werden, um als Stapelverarbeitung zu einem bestimmten Datum und zu einer Zeit erledigt zu werden.  
8. Klicken Sie im **Aktivitätsbereich** auf **Dimensionswerte**. Einige Dimensionswerte sind unternehmensspezifisch. Sie können prüfen, ob sie unternehmensspezifisch sind, wenn der Unternehmensname in der Dimensionswertliste anzeigt wird.  

## <a name="create-a-custom-financial-dimension"></a>Erstellen einer benutzerdefinierten Finanzdimension
1. Schließen Sie die Seite.
2. Klicken Sie auf **Neu**.
3. Wählen Sie im Feld **Werte verwenden aus** die Option **Benutzerdefinierte Dimension**.
4. Geben Sie im Feld **Dimensionsname** einen Wert ein, um die Finanzdimension zu beschreiben.
    - Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.  
    - Sie können auch eine Kontenmaske angeben. Sie beschränkt die Menge und die Art von Informationen, die für Dimensionswerte eingegeben werden können.   
    - Sie können Zeichen eingeben, die dieselben bleiben für jeden Dimensionswert, wie Buchstaben oder einen Bindestrich. Sie können auch Nummernzeichen (#) und kaufmännische Und-Zeichen (&) als Platzhalter für Buchstaben und Zahlen eingeben, die sich jedes Mal ändern werden, wenn ein Dimensionswert erstellt wird. Verwenden Sie ein Nummernzeichen (#) als Platzhalter für eine Zahl und ein kaufmännisches Und-Zeichen (&) als Platzhalter für einen Buchstaben.  Beispiel: Um den Dimensionswert auf die Buchstaben CC und drei Zahlen einzuschränken, geben Sie CC-### als Formatmaske ein.  
5. Klicken Sie auf **Aktivieren**. "Aktivieren der Finanzdimension" aktualisiert die Tabelle mit dem Finanzdimensionsnamen und entfernt gelöschte Dimensionen. Sie können Dimensionswerte eingegeben, bevor Sie eine Finanzdimension aktivieren, Finanzdimension kölnnen jedoch nicht verwendet werden, bis sie aktiviert sind.     
6. Klicken Sie auf **Aktivieren**. Die Dimensionsaktivierung kann geplant werden, um als Stapelverarbeitung zu einem bestimmten Datum und zu einer Zeit erledigt zu werden.      
7. Klicken Sie im **Aktivitätsbereich** auf **Dimensionswerte**.
8. Klicken Sie auf **Neu**.
9. Geben Sie im Feld **Dimensionswert** einen Namen ein, um den Finanzdimensionswert zu beschreiben.
10. Geben Sie im Textfeld eine **Beschreibung** ein, die den Finanzdimensionswert beschreibt.

