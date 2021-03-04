---
title: Lean Manufacturing-Arbeitsgruppe definieren
description: Eine Arbeitsgruppe ist ein Form einer Ressourcengruppen, die in den Lean Manufacturing-Verarbeitungsaktivitäten verwendet werden kann.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, InventLocationIdLookup, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4f460fb42be5cbeda55a82e536e2a83cd2f6b608
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428406"
---
# <a name="define-lean-manufacturing-work-cells"></a>Lean Manufacturing-Arbeitsgruppe definieren

[!include [banner](../../includes/banner.md)]

Eine Arbeitsgruppe ist ein Form einer Ressourcengruppen, die in den Lean Manufacturing-Verarbeitungsaktivitäten verwendet werden kann. Arbeitsgruppen haben Eingangs- und Ausgangslagerplätze und eine Kapazitätsdefinition auf Basis eines Produktionsflussmodells. Weitere Informationen zu den grundlegende Konzepten von Lean-Manufacturing-Arbeitsgruppen und Kapazitätsberechnungen finden Sie in den Whitepapers zum Lean-Manufacturing. Das Demodatenunternehmen in dieser Prozedur ist USMF.


## <a name="create-a-work-cell"></a>Erstellen Sie eine Arbeitsgruppe. 
1. Wechseln Sie zu Organisationsverwaltung > Ressourcen > Ressourcengruppen.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Ressourcengruppe" einen Wert ein.
    * Die Arbeitsgruppenkennung ist normalerweise ein systematischer Code und muss für die juristische Person eindeutig sein.  
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * die Beschreibung enthält den Namen oder den Titel der Arbeitsgruppe.  
5. Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Eine Arbeitsgruppe befindet sich an einem bestimmten Lagerort. Der Lagerort für Warenausgang und Wareneingang sowie der Lagerplatz müssen an diesem Lagerort befinden.  
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Klicken Sie im Feld "Produktionseinheit" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie eine Produktionseinheit aus, zu der diese Arbeitsgruppe gehört.  
9. Markieren Sie das Kontrollkästchen "Arbeitsgruppe".
    * Um eine Ressourcengruppe als Lean-Arbeitsgruppe nutzen zu können, muss das Kontrollkästchen "Arbeitsgruppe" ausgewählt werden.  Beachten Sie, dass diese Eigenschaft nicht geändert werden kann, sobald die Ressourcengruppe erstellt wurde.  
10. Klicken Sie im Feld "Eingangslagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Für die Kalkulation und die Materialsteuerung ist das Material, das im Fertigungsbereich bereitgestellt wird, normalerweise einem bestimmten virtuellen Lagerort zugewiesen. Wenn Sie jedoch die Lagerplätze über Lagerarbeit auffüllen möchten, müssen sie Teil des empfangenden Rohmateriallagerorts sein.  
12. Klicken Sie im Feld "Lagerplatz für Wareneingang" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
13. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Beachten Sie bei einer Verarbeitungsaktivität, dass der Eingangslagerplatz allgemeinen überschrieben oder für ein bestimmtes Produkt oder eine Produktvariante überschrieben werden kann, indem er Kommissionieraktivitäten definiert werden, die die Verarbeitungsaktivität versorgen. Die Lagerplatz für Wareneingang einer Arbeitsgruppe können nicht über Ladungsträger gesteuert werden.  
14. Klicken Sie im Feld "Ausgangslagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
15. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Bei mehreren Produktionsflussaktivität oder Produktionspositionen ist dieses häufig der Eingangslagerort der nächsten Arbeitsgruppe oder der Verkaufs- oder Transitlagerort, an den ein Produkt in der Regel nach dem Produktionsprozess übertragen wird. Denken Sie bei der Modellierung von Lean Manufacturing-Verarbeitungen daran, dass der Transport normalerweise genauso überflüssig ist wie die Berichterstellung zum Transport.  
16. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
17. Klicken Sie im Feld "Lagerplatz für Warenausgang" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * In einem Produktionsfluss mit mehreren Verarbeitungsaktivitäten handelt es sich häufig um den Lagerplatz für den Wareneingang der nächsten Arbeitsgruppe.  
18. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
19. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
20. Erweitern oder reduzieren Sie den Abschnitt "Arbeitsgang".
    * Eine Ausführungszeitkategorie muss bereitgestellt werden, um die Kostenberechnung und die Verarbeitung von Lean-Kaban-Vorgängen zu ermöglichen.  
21. Klicken Sie im Feld "Bearbeitungszeitkategorie" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
22. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * In der Standardkostenberechnung und bei der Nachkalkulation der Produktionskosten wird die Kostenkategorie für die Bearbeitungszeit verwendet.  
23. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
24. Erweitern oder reduzieren Sie den Abschnitt "Kalender".
25. Klicken Sie auf Hinzufügen.
26. Klicken Sie im Feld "Kalender" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
27. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * In der Regel verwenden Arbeitsgruppen eines bestimmten Standort den gleichen Arbeitszeitkalender. Wenn Arbeitsgruppen einzelne Arbeitszeiten verwenden können, müssen Sie möglicherweise einen speziellen Arbeitszeitkalender für die Arbeitsgruppe erstellen. Beachten Sie, dass der Kalender eine Standardarbeitszeit aufweisen sollte, wenn er für eine Lean-Arbeitsgruppe verwendet wird. Die Kapazitätsdefinition normalerweise der Standardarbeitszeit eines Arbeitstags zugeordnet.  
28. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
29. Erweitern oder reduzieren Sie den Abschnitt "Arbeisgruppenkapazität".
30. Klicken Sie auf Hinzufügen.
31. Klicken Sie im Feld "Produktionsflussmodell" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
32. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Dies Verfahren erfordert den Produktionsflussmodelltyp "Durchsatz" damit die Definition der Durchsatzkapazität angezeigt werden kann.  
33. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
34. Wählen Sie im Feld "Kapazitätsperiode" eine Option aus.
    * Die Optionen sind: Standardarbeitstag - Die Kapazität wird durch die Länge des Standardarbeitstags des Arbeitszeitkalenders für die Arbeitsgruppe ausgedrückt. Für jeden Tag wird die tatsächliche Arbeitszeit aus dem Kalender bestimmt und die effektive verfügbare Kapazität wird auf dieser Grundlage berechnet.   Woche - Eine wöchentliche Kapazität. Es gibt keine Anpassung durch die tatsächliche Arbeitszeit.   Monat - Eine Monatskapazität. Es gibt keine Anpassung durch die tatsächliche Kapazität.   Normalerweise wird der Standardarbeitstag für tägliche Perioden verwendet und die wöchentliche Kapazität wird für wöchentliche Kapazitätsperioden verwendet.  
35. Geben Sie im Feld "Durchschnittliche Durchsatzmenge" eine Zahl ein.
    * Beachten Sie, dass ein Lean-Arbeitsgang in einer idealen Umgebung niemals für die maximale Kapazität eingerichtet wird. Stattdessen sollte die Kapazität immer für Arbeitsgänge unter typische Umstände definiert werden.  
36. Klicken Sie im Feld "Einheit" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
37. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
38. "Auflösen" verändert die Einheit.

## <a name="add-a-financial-dimension"></a>Finanzdimension hinzufügen
1. Erweitern oder Reduzieren Sie den Abschnitt "Finanzdimensionen'.
    * Beachten Sie, dass die Finanzdimensionen, die im Produktionsfluss definiert werden, die Finanzdimension einer bestimmten Arbeitsgruppe überschreiben.    Die auswählbaren Finanzdimensionen hängen von der Konfiguration der Finanzdimensionen Ihres Systems ab. Die folgenden Schritte nutzen die Demodaten im Unternehmen USMF. Bei der Nutzung anderer Daten sind die Schritte nicht zutreffend.  
2. Klicken Sie im Feld "Kostenstelle" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Die Dimensionen, die für Lean-Arbeitgruppe ausgewählt werden müssen, hängen von der Implementierung von Finanzdimensionen im Buchhaltungsmodell für eine bestimmte juristische Person ab.  
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Klicken Sie im Feld "ItemGroup" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="save"></a>Speichern
1. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]