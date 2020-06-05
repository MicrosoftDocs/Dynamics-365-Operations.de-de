---
title: Verpacken in Container einrichten
description: In diesem Thema wird beschrieben, wie Containerisierung von Ladungen in der Lagerortverwaltung automatisiert wird.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0f042e6ffe5ecf01b9e5044fc83d081528fbc56
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383296"
---
# <a name="set-up-containerization"></a>Verpacken in Container einrichten

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie Containerisierung von Ladungen in der Lagerortverwaltung automatisiert wird. Automatisierte Containerisierung erstellt Container und die Entnahmearbeit für Lieferungen, wenn eine Welle verarbeitet wird und Arbeitspositionen in Mengen aufgeteilt werden können, die in die Container passen. Dies unterstützt Lagerarbeiter dabei, die Artikel direkt zur Verpackung in den ausgewählten Container zu entnehmen. Verglichen mit dem manuellen Verpackungsprozess, werden Aufgaben wie das Erstellen von Containern, das Zuweisen von Artikeln und das Abschließen von Containern vom System automatisiert. Bei dieser Prozedur wird das USMF-Demo-Unternehmen verwendet und sie wird von einem Lagerortleiter ausgeführt.


## <a name="set-up-a-wave-template"></a>Richten Sie eine Wellenvorlage ein
1. Wechseln Sie im Navigationsbereich zu **Module > Lagerortverwaltung > Einstellungen > Wellen > Wellenvorlagen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Wellenvorlagenname** einen Wert ein.
4. Geben Sie im Feld **Wellenvorlagenbeschreibung** einen Wert ein.
5. Geben Sie im Feld **Standort** einen Wert ein, oder wählen Sie einen Wert aus.
6. Geben Sie im Feld **Lagerort** einen Wert ein, oder wählen Sie einen Wert aus.
7. Erweitern Sie den Abschnitt **Methoden**. Der Bereich **Ausgewählte Methoden** führt die Methoden für den ausgewählten Wellenvorlagentyp auf. Die Wellenvorlage muss die Containerisierungsmethode enthalten.  
8. Geben Sie im Feld **Wellenschrittcode** einen Wert ein. Geben Sie einen Wellenschrittcode für die hinzugefügte Methode ein. Das kann jeder beliebige Code sein. Es ist möglich, die Methode mehrmals hinzuzufügen und verschiedene Wellenschrittcodes zuzuweisen. Dazu wählen Sie **Wiederholbar** für diese Methode auf der Seite **Wellenverarbeitungsmethoden** aus.  
9. Wählen Sie **Speichern**.
10. Schließen Sie die Seite.

## <a name="set-up-a-container-type"></a>Einrichten eines Containertyps
1. Wechseln Sie im Navigationsbereich zu **Module > Lagerortverwaltung > Einstellungen > Container > Containertypen**. Sie können Ihre Container auf der Seite **Containertypen** definieren. Sie können die physischen Dimensionen von Containern konfigurieren, einschließlich Verpackungsgewicht, Höchstgewicht, maximales Volumen, Länge, Breite und Höhe. In diesem Beispiel haben wir drei verschiedene Größen von Feldern.  
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Containertypcode** einen Wert ein.
4. Geben Sie im Feld **Verpackungsgewicht** eine Zahl ein.
5. Geben Sie im Feld **Höchstgewicht** eine Zahl ein.
6. Geben Sie im Feld **Volumen** eine Zahl ein.
7. Geben Sie im Feld **Länge** eine Zahl ein.
8. Geben Sie im Feld **Breite** eine Zahl ein.
9. Geben Sie im Feld **Höhe** eine Zahl ein.
10. Geben Sie im Feld **Beschreibung** einen Wert ein.
11. Wählen Sie **Speichern**.
13. Wiederholen Sie die Schritte 2 bis 11 zwei weitere Male, um insgesamt drei Containertypen zu erstellen.
14. Schließen Sie die Seite.

## <a name="set-up-a-container-group"></a>Eine Containergruppe einrichten
1. Wechseln Sie im Navigationsbereich zu **Module > Lagerortverwaltung > Einstellungen > Container > Containergruppen**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus. Sie können logische Gruppen von Containertypen einrichten. Für jede Gruppe können Sie die Reihenfolge festlegen, in der die Container beladen werden und den Prozentsatz, bis zu dem die Container befüllt werden. Die Größendimensionen des Artikels wird verwendet, um zu bestimmen, ob er in einen Container passt. Der Container, der den Größendimensionen des Artikels am nächsten liegt, wird verwendet. Wenn Sie mehrere Container in einer Gruppe haben, empfiehlt es sich, die Reihenfolge nach Größe anzuordnen, sodass der größte Container der erste ist, Nummer 1 in der Reihenfolge, und der kleinste Container der letzte ist.    
3. Geben Sie im Feld **Containergruppenkennung** einen Wert ein, den Sie zuvor erstellt haben.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Wiederholen Sie die Schritte 2 bis 4 für alle drei Containertypen, die Sie zuvor erstellt haben.
6. Wählen Sie **Speichern**.
7. Schließen Sie die Seite.

## <a name="set-up-a-container-build-template"></a>Eine Containererstellungsvorlage einrichten
1. Wechseln Sie im Navigationsbereich zu **Module > Lagerortverwaltung > Einstellungen > Container > Containererstellungsvorlagen**.
2. Wählen Sie **Neu** aus. Die Containererstellungsvorlage basiert darauf, welche der Containerisierungsprozesse ausgeführt werden. Jede Containererstellungsvorlage definiert einen Containerisierungsprozess, der von einer Wellenvorlage verwendet wird. Die Option **Abfrage bearbeiten** ermöglicht es Ihnen, die Bedingungen zu definieren, zu denen die ausgewählte Vorlage verarbeitet wird. Beispielsweise möchten Sie möglicherweise die Containerisierung nur für bestimmte Debitoren, Produkte oder Lagerorte ausführen oder Sie können die entsprechenden Abfragebereiche der Vorlage hinzufügen. Das Feld **Wellenschrittcode** gibt an, wie eine Containererstellungsvorlage mit den Schritten in einer Wellenvorlage verknüpft ist. Wenn eine Welle ausgeführt wird, bestimmt sie, welche Containererstellungsvorlage(n) verwendet werden, um Containerisierung zu initiieren. Das Feld "Basisabfragetyp" bestimmt, was verpackt wird und auf was die Filterabfrage basieren soll. 
3. Geben Sie im Feld **Containervorlagenkennung** einen Wert ein.
4. Geben Sie im Feld **Containergruppenkennung** einen Wert ein, oder wählen Sie einen Wert aus.
5. Geben Sie im Feld **Wellenschrittcode** einen Wert ein.
6. Aktivieren Sie das Kontrollkästchen **Aufgeteilte Entnahme zulassen**.
7. Wählen Sie **Speichern**.
8. Wählen Sie **Containermischungseinschränkungen** aus. Mischlogikpausen ermöglicht es Ihnen, Regeln für das Verpacken von Zuteilungspositionen in Containern einzurichten. Wenn Sie beispielsweise das Feld **Artikelnummer** hinzufügen, wird beim Zuweisen von Artikeln zu Containern ein neuer Container erstellt, wenn es eine neue Artikelnummer gibt. Dies verhindert, dass Arbeitskräfte Zuteilungspositionen für zwei verschiedene Debitoren im gleichen Container verpacken.  
9. Wählen Sie **Neu** aus.
10. Wählen Sie im Feld **Tabelle** eine Option aus.
11. Geben Sie im Feld **Feldauswahl** einen Wert ein, oder wählen Sie einen Wert aus.
12. Wählen Sie **OK**.

