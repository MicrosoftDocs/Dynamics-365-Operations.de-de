--- 
title: Produktmaster erstellen
description: "Erstellen eines Produktmasters für vordefinierte Varianten."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b783c41459163ab5a0644a1ff5c39b6933bcdb1b
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-master"></a>Produktmaster erstellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Erstellen eines Produktmasters für vordefinierte Varianten. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Prozedur ist für den Produktionsplaner vorgesehen.


## <a name="create-a-new-product-master"></a>Neuen Produktmaster erstellen
1. Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Produktmaster".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Produktnummer" einen Wert ein.
    * Die Nummer muss eindeutig sein. Ein Nummernkreis kann im Feld "Produktnummer" eingegeben werden. In diesem Fall muss der Benutzer keinen Wert eingeben.  
4. Geben Sie im Feld "Produktname" einen Wert ein.
    * Geben Sie einen beschreibenden Namen des Produkts ein. Der Wert ist standardmäßig der Suchname, er kann jedoch auch vom Benutzer geändert werden.  
5. Klicken Sie im Feld "Produktdimensionsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Produktdimensionsgruppe legt fest, welche der 4 Produktdimensionen für die Erstellung der Produktvarianten verwendet werden können. In diesem Beispiel wird eine Gruppe mit Farbe und Größe verwendet.  
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Die Standardkonfigurationstechnologie ist die vordefinierte Variante. Diese wird für dieses Beispiel verwendet.  
8. Klicken Sie auf "OK".

## <a name="select-product-dimension-groups"></a>Produktdimensionsgruppen auswählen
1. Klicken Sie im Feld "Farbgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie im Feld "Größengruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="add-dimension-groups"></a>Dimensionsgruppen hinzufügen
1. Klicken Sie im Aktivitätsbereich auf "Produkt".
2. Klicken Sie auf "Dimensionsgruppen", um das Dropdown-Dialogfeld zu öffnen.
3. Klicken Sie im Feld "Lagerdimensionsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Mit Lagerdimensionsgruppen kann gesteuert werden, wie Artikel im Lagerbestand gespeichert und aus dem Lagerbestand entnommen werden. So kann eine Lagerdimension Standort und Lagerort enthalten.  
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Klicken Sie im Feld "Rückverfolgungsangaben-Gruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Rückverfolgungsangabengruppe bestimmt, welche Rückverfolgungsangaben Sie einem Produkt hinzufügen können. Die Chargennummer und die Seriennummer können z. B. zum Nachverfolgen von Lagerartikeln verwendet werden.  
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Klicken Sie auf "OK".
10. Klicken Sie auf "Speichern".
11. Schließen Sie die Seite.


