---
title: Ein freigegebenes Produkt für ein einzelnes Unternehmen erstellen
description: In dieser Prozedur wird erläutert, wie ein einzelnes freigegebenes Produkt im Rahmen einer einzelnen gültigen Einheit erstellt wird.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90924c853793a3d70f2f2d46d8a154a19bd7d6bb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985508"
---
# <a name="create-a-released-product-for-a-single-company"></a>Ein freigegebenes Produkt für ein einzelnes Unternehmen erstellen

[!include [banner](../../includes/banner.md)]

In dieser Prozedur wird erläutert, wie ein einzelnes freigegebenes Produkt im Rahmen einer einzelnen gültigen Einheit erstellt wird. Nachdem das freigegebene Produkt erstellt wurde, ist es sofort in ausschließlich dieser Einheit verfügbar. Sie können diese Prozedur im Demodatenunternehmen USMF ausführen. Diese Aufgabe wird in der Regel von einem Produktdesigner ausgeführt.


## <a name="create-a-released-product"></a>Freigegebenes Produkt erstellen
1. Wechseln Sie zu "Freigegebene Produkte".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Produktnummer" einen Wert ein.
    * Wenn eine Produktnummer nicht automatisch im Feld "Produktnummer" eingegeben wird, geben Sie eine eindeutige Produktnummer ein. Dieser Schritt ist nur erforderlich, wenn kein Nummernkreis für Produktnummern eingerichtet wurde.  
4. Geben Sie im Feld "Produktname" einen Wert ein.
    * Der Produktname wird als Suchbegriff beibehalten. Bei Bedarf können Sie auswählen, den Suchbegriff zu ändern.  
5. Klicken Sie im Feld "Artikelmodellgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Artikelmodellgruppen enthalten Einstellungen, die bestimmen, wie Artikel beim Artikelzugang und -abgang gesteuert und gehandhabt werden. Die Einstellungen bestimmen auch, wie der Verbrauch von Artikeln berechnet wird.  
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie im Feld "Artikelgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Artikelgruppen werden verwendet, um den Bestand zu verwalten, indem Sie Lagerartikel auf der Grundlage von Artikelmerkmalen in Gruppen einteilen. Um z. B. einzustellen, wie Informationen zu den Hauptkonten gebucht werden, können Sie eine Reihe verschiedener Artikelgruppen erstellen, die speziellen Hauptkonten zugeordnet sind. Auf diese Weise können Sie den Bestand von Artikeln in verschiedenen Phasen verfolgen.  
9. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
10. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
11. Klicken Sie im Feld "Lagerdimensionsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Mit Lagerdimensionsgruppen kann gesteuert werden, wie Artikel im Lagerbestand gespeichert und aus dem Lagerbestand entnommen werden. So kann eine Lagerdimension Standort und Lagerort sein.  
12. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
13. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
14. Klicken Sie im Feld "Rückverfolgungsangaben-Gruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Rückverfolgungsangabengruppe bestimmt, welche Rückverfolgungsangaben Sie einem Produkt hinzufügen können. Die Chargennummer und die Seriennummer können z. B. zum Nachverfolgen von Lagerartikeln verwendet werden.  
15. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
16. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
17. Klicken Sie im Feld "Lagereinheit" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Lagereinheit bestimmt, wie das Produkt mengenmäßig bestimmt wird, wenn es im Lagerbestand gespeichert wird.  
18. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
19. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
20. Klicken Sie im Feld "Bestelleinheit" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Bestelleinheit bestimmt, wie das Produkt mengenmäßig bestimmt wird, wenn es von einem Lieferant erworben wird.  
21. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
22. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
23. Klicken Sie im Feld "Verkaufseinheit" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Verkaufseinheit bestimmt, wie das Produkt mengenmäßig bestimmt wird, wenn es einem Debitor verkauft wird.  
24. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
25. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
26. Klicken Sie im Feld "Stücklisteneinheit" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Stücklisteneinheit bestimmt, wie das Produkt mengenmäßig bestimmt wird, wen es in einer Stückliste (BOM) einbezogen werden soll.  
27. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
28. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
29. Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Artikel-Mehrwertsteuergruppe in der Vertriebsbesteuerungsgruppe bestimmt, wie die Mehrwertsteuer für jeden Artikel berechnet wird.  
30. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
31. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
32. Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Artikel-Mehrwertsteuergruppe in der Umsatzsteuergruppe bestimmt, wie die Umsatzsteuer für jeden Artikel berechnet wird.  
33. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
34. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
35. Klicken Sie auf "OK".

## <a name="add-product-characteristics"></a>Physische Produktmerkmale hinzufügen
1. Erweitern oder reduzieren Sie den Abschnitt Bestand verwalten.
2. Geben Sie im Feld "Nettogewicht" eine Zahl ein.
3. Geben Sie im Feld "Verpackungsgewicht" eine Zahl ein.
4. Geben Sie im Feld "Bruttotiefe" eine Zahl ein.
5. Geben Sie im Feld "Bruttobreite" eine Zahl ein.
6. Geben Sie im Feld "Bruttohöhe" eine Zahl ein.
7. Geben Sie im Feld "Volumen" eine Zahl ein.

## <a name="add-financial-dimensions"></a>Finanzdimensionen hinzufügen
1. Erweitern oder Reduzieren Sie den Abschnitt "Finanzdimensionen'.
2. Klicken Sie im Feld "Unternehmenseinheit" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Klicken Sie im Feld "Kostenstelle" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie im Feld "Abteilung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
9. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
10. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
11. Klicken Sie im Feld "ItemGroup" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
12. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
13. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

