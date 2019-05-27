---
title: Verpacken in Container einrichten
description: In dieser Prozedur wird beschrieben, wie Containerisierung von Ladungen in der "Lagerortverwaltung" automatisiert wird.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56fc6adc2a0eeb5b824089ff4b1b781f3a99a34c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558055"
---
# <a name="set-up-containerization"></a>Verpacken in Container einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dieser Prozedur wird beschrieben, wie Containerisierung von Ladungen in der "Lagerortverwaltung" automatisiert wird. Automatisierte Containerisierung erstellt Container und die Entnahmearbeit für Lieferungen, wenn eine Welle verarbeitet wird und Arbeitspositionen in Mengen aufgeteilt werden können, die in die Container passen. Dies unterstützt Lagerarbeiter dabei, die Artikel direkt zur Verpackung in den ausgewählten Container zu entnehmen. Verglichen mit dem manuellen Verpackungsprozess, werden Aufgaben wie das Erstellen von Containern, das Zuweisen von Artikeln und das Abschließen von Containern vom System automatisiert. Bei dieser Prozedur wird das USMF-Demo-Unternehmen verwendet und sie wird von einem Lagerortleiter ausgeführt.


## <a name="set-up-a-wave-template"></a>Richten Sie eine Wellenvorlage ein
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Wellen" > "Wellenvorlagen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Wellenvorlage" einen Wert ein.
4. Geben Sie im Feld "Wellenvorlagenbeschreibung" einen Wert ein.
5. Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.
6. Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.
7. Erweitern Sie den Abschnitt "Methoden".
    * Der Bereich "Ausgewählte Methoden" führt die Methoden für den ausgewählten Wellenvorlagentyp auf. Die Wellenvorlage muss die Containerisierungsmethode enthalten.  
8. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
9. Geben Sie im Feld "Wellenschritt" einen Wert ein.
    * Geben Sie einen Wellenschrittcode für die hinzugefügte Methode ein. Das kann jeder beliebige Code sein. Es ist möglich, die Methode mehrmals hinzuzufügen und verschiedene Wellenschrittcodes zuzuweisen. Dazu wählen Sie "Wiederholbar" für diese Methode auf der Seite "Wellenprozessmethoden" aus.  
10. Klicken Sie auf "Speichern".
11. Schließen Sie die Seite.

## <a name="set-up-a-container-type"></a>Einrichten eines Containertyps
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Container" > "Containertypen".
    * Sie können Ihre Container auf der Seite "Containertypen" definieren. Sie können die physischen Dimensionen von Containern konfigurieren, einschließlich Verpackungsgewicht, Höchstgewicht, maximales Volumen, Länge, Breite und Höhe. In diesem Beispiel haben wir drei verschiedene Größen von Feldern.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Containertypcode" einen Wert ein.
4. Geben Sie im Feld "Verpackungsgewicht" eine Zahl ein.
5. Geben Sie im Feld "Höchstgewicht" eine Zahl ein.
6. Geben Sie im Feld "Volumen" eine Zahl ein.
7. Geben Sie im Feld Länge eine Zahl ein.
8. Geben Sie im Feld "Breite" eine Zahl ein.
9. Geben Sie im Feld "Höhe" eine Zahl ein.
10. Geben Sie im Feld "Beschreibung" einen Wert ein.
11. Klicken Sie auf "Speichern".
12. Klicken Sie auf "Neu".
13. Geben Sie im Feld "Containertypcode" einen Wert ein.
14. Geben Sie im Feld "Beschreibung" einen Wert ein.
15. Geben Sie im Feld "Verpackungsgewicht" eine Zahl ein.
16. Geben Sie im Feld "Höchstgewicht" eine Zahl ein.
17. Geben Sie im Feld "Volumen" eine Zahl ein.
18. Geben Sie im Feld Länge eine Zahl ein.
19. Geben Sie im Feld "Breite" eine Zahl ein.
20. Geben Sie im Feld "Höhe" eine Zahl ein.
21. Klicken Sie auf "Speichern".
22. Klicken Sie auf "Neu".
23. Geben Sie im Feld "Containertypcode" einen Wert ein.
24. Geben Sie im Feld "Beschreibung" einen Wert ein.
25. Geben Sie im Feld "Verpackungsgewicht" eine Zahl ein.
26. Geben Sie im Feld "Höchstgewicht" eine Zahl ein.
27. Geben Sie im Feld "Volumen" eine Zahl ein.
28. Geben Sie im Feld Länge eine Zahl ein.
29. Geben Sie im Feld "Breite" eine Zahl ein.
30. Geben Sie im Feld "Höhe" eine Zahl ein.
31. Klicken Sie auf "Speichern".
32. Schließen Sie die Seite.

## <a name="set-up-a-container-group"></a>Eine Containergruppe einrichten
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Container" > "Containergruppen".
2. Klicken Sie auf "Neu".
    * Sie können logische Gruppen von Containertypen einrichten. Für jede Gruppe können Sie die Reihenfolge festlegen, in der die Container beladen werden und den Prozentsatz, bis zu dem die Container befüllt werden. Die Größendimensionen des Artikels wird verwendet, um zu bestimmen, ob er in einen Container passt. Der Container, der den Größendimensionen des Artikels am nächsten liegt, wird verwendet. Wenn Sie mehrere Container in einer Gruppe haben, empfiehlt es sich, die Reihenfolge nach Größe anzuordnen, sodass der größte Container der erste ist, Nummer 1 in der Reihenfolge, und der kleinste Container der letzte ist.    
3. Geben Sie im Feld "Containergruppenkennung" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie auf Neu.
6. Markieren Sie in der Liste die ausgewählte Zeile.
7. Geben Sie im Feld "Containertyp" einen Wert ein, oder wählen Sie einen Wert aus.
8. Klicken Sie auf Neu.
9. Markieren Sie in der Liste die ausgewählte Zeile.
10. Geben Sie im Feld "Containertyp" einen Wert ein, oder wählen Sie einen Wert aus.
11. Klicken Sie auf Neu.
12. Markieren Sie in der Liste die ausgewählte Zeile.
13. Geben Sie im Feld "Containertyp" einen Wert ein, oder wählen Sie einen Wert aus.
14. Klicken Sie auf "Speichern".
15. Schließen Sie die Seite.

## <a name="set-up-a-container-build-template"></a>Eine Containererstellungsvorlage einrichten
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Container" > "Containererstellungsvorlagen".
2. Klicken Sie auf "Neu".
    * Die Containererstellungsvorlage basiert darauf, welche der Containerisierungsprozesse ausgeführt werden. Jede Containererstellungsvorlage definiert einen Containerisierungsprozess, der von einer Wellenvorlage verwendet wird. Die Option "Abfrage bearbeiten" ermöglicht es Ihnen, die Bedingungen zu definieren, zu denen die ausgewählte Vorlage verarbeitet wird. Beispielsweise möchten Sie möglicherweise die Containerisierung nur für bestimmte Debitoren, Produkte oder Lagerorte ausführen oder Sie können die entsprechenden Abfragebereiche der Vorlage hinzufügen. Das Feld "Wellenschrittcode" ist, wie eine Containererstellungsvorlage mit den Schritten in einer Wellenvorlage verknüpft ist. Wenn eine Welle ausgeführt wird, bestimmt sie, welche Containererstellungsvorlage(n) verwendet werden, um Containerisierung zu initiieren. Das Feld "Basisabfragetyp" bestimmt, was verpackt wird und auf was die Filterabfrage basieren soll.  
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie im Feld "Containervorlagenkennung" einen Wert ein.
5. Geben Sie im Feld "Containergruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.
6. Geben Sie im Feld "Wellenschritt" einen Wert ein.
7. Aktivieren Sie das Kontrollkästchen "Geteilte Entnahmen zulassen".
8. Klicken Sie auf "Speichern".
9. Klicken Sie auf "Containermischungseinschränkungen".
    * Mischlogikpausen ermöglicht es Ihnen, Regeln für das Verpacken von Zuteilungspositionen in Containern einzurichten. Wenn Sie beispielsweise das Feld "Artikelnummer" hinzufügen, wenn Artikel zu Containern zugewiesen werden, wird ein neuer Container erstellt, wenn es eine neue Artikelnummer gibt. Dies verhindert, dass Arbeitskräfte Zuteilungspositionen für zwei verschiedene Debitoren im gleichen Container verpacken.  
10. Klicken Sie auf "Neu".
11. Wählen Sie im Feld "Tabelle" eine Option aus.
12. Geben Sie im Feld "Feld auswählen" einen Wert ein, oder wählen Sie einen Wert aus.
13. Klicken Sie auf "OK".

