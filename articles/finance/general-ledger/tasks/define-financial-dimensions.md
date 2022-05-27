---
title: Finanzdimensionen definieren
description: Diese Prozedur zeigt, wie Sie eine mit Entitäten hinterlegte Finanzdimension und eine angepasste Finanzdimension hinzufügen.
author: aprilolson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10a991938f68c0ade19999e48a02f032c92a6779
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716942"
---
# <a name="define-financial-dimensions"></a>Finanzdimensionen definieren

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt, wie Sie eine mit Entitäten hinterlegte Finanzdimension und eine angepasste Finanzdimension hinzufügen. Der Leitfaden verwendet das Demounternehmen USMF.

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
1. Klicken Sie auf **Neu**.
2. Wählen Sie im Feld **Werte verwenden aus** die Option **Benutzerdefinierte Dimension**.
3. Geben Sie im Feld **Dimensionsname** einen Wert ein, um die Finanzdimension zu beschreiben.
    - Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.  
    - Sie können auch eine Kontenmaske angeben. Sie beschränkt die Menge und die Art von Informationen, die für Dimensionswerte eingegeben werden können.   
    - Sie können Zeichen eingeben, die dieselben bleiben für jeden Dimensionswert, wie Buchstaben oder einen Bindestrich. Sie können auch Nummernzeichen (#) und kaufmännische Und-Zeichen (&) als Platzhalter für Buchstaben und Zahlen eingeben, die sich jedes Mal ändern werden, wenn ein Dimensionswert erstellt wird. Verwenden Sie ein Nummernzeichen (#) als Platzhalter für eine Zahl und ein kaufmännisches Und-Zeichen (&) als Platzhalter für einen Buchstaben.  Beispiel: Um den Dimensionswert auf die Buchstaben CC und drei Zahlen einzuschränken, geben Sie CC-### als Formatmaske ein.  
4. Klicken Sie auf **Aktivieren**. "Aktivieren der Finanzdimension" aktualisiert die Tabelle mit dem Finanzdimensionsnamen und entfernt gelöschte Dimensionen. Sie können Dimensionswerte eingegeben, bevor Sie eine Finanzdimension aktivieren, Finanzdimension kölnnen jedoch nicht verwendet werden, bis sie aktiviert sind.     
5. Klicken Sie auf **Aktivieren**. Die Dimensionsaktivierung kann geplant werden, um als Stapelverarbeitung zu einem bestimmten Datum und zu einer Zeit erledigt zu werden.      
6. Klicken Sie im **Aktivitätsbereich** auf **Dimensionswerte**.
7. Klicken Sie auf **Neu**.
8. Geben Sie im Feld **Dimensionswert** einen Namen ein, um den Finanzdimensionswert zu beschreiben.
9. Geben Sie im Textfeld eine **Beschreibung** ein, die den Finanzdimensionswert beschreibt.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
