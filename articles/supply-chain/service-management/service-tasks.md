---
title: Übersicht der Serviceaufgaben
description: Serviceaufgaben dienen zum Beschreiben der Aufgabe, die im Zuge eines Serviceauftrags auszuführen ist. Diese Informationen stehen sowohl dem Techniker als auch dem Debitor zur Verfügung.
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd7e5293ef506c6d785b420824f2c2a2c96112f7
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865893"
---
# <a name="service-tasks-overview"></a>Übersicht der Serviceaufgaben

[!include [banner](../includes/banner.md)]

Serviceaufgaben dienen zum Beschreiben der Aufgabe, die im Zuge eines Serviceauftrags auszuführen ist.
Diese Informationen stehen sowohl dem Techniker als auch dem Debitor zur Verfügung.

Die Erstellung von Serviceaufgaben erfolgt im Formular **Serviceaufgaben**. Durch Erstellen von Serviceaufgabenbeziehungen werden die Serviceaufgaben einer bestimmten Servicevereinbarung oder einem bestimmten Serviceauftrag zugeordnet. Zusammen mit einer Serviceaufgabenbeziehung können Sie auch Folgendes erstellen:

-  Interne Hinweise für die Aufgabe (beispielsweise ausführliche technische Informationen, die dem Techniker bekannt sein müssen).

-  Externe Hinweise für den Debitor. Hier kann beispielsweise eine allgemein verständlichere Beschreibung der Aufgabe angegeben werden, die im Rahmen der zwischen Debitor und Serviceunternehmen bestehenden Vereinbarung ausgeführt wird.

Nach dem Einrichten einer Serviceaufgabenbeziehung zwischen einer Serviceaufgabe und einem Serviceauftrag oder einer Servicevereinbarung kann die entsprechende Serviceaufgabe beim Erstellen von Serviceauftrags- oder Servicevereinbarungspositionen für den aktuellen Serviceauftrag bzw. für die aktuelle Servicevereinbarung angegeben werden.

Wird ein Serviceauftrag auf Basis einer Servicevereinbarung erstellt, können Serviceauftragspositionen mithilfe der den einzelnen Servicevereinbarungspositionen zugewiesenen Serviceaufgaben zu Serviceaufträgen gruppiert werden.

## <a name="create-a-service-task"></a>Erstellen von Serviceaufgaben

1. Klicken Sie auf **Dienstleistungsverwaltung** \> **Einrichtung** \> **Dienstleistungsaufgaben**.
2. Erstellen Sie eine neue Position.
3. Geben Sie die Servicekennung sowie eine Beschreibung ein.

## <a name="example"></a>Beispiel

Ein Techniker soll vor Ort zwei Aufgaben an einem Getriebe ausführen (Serviceobjekt: "GB-1234"). Für den Debitor wird eine Servicevereinbarung erstellt, und den Aufgaben werden mehrere Buchungen zugeordnet. Im Anschluss sind die Servicevereinbarung sowie die Vereinbarungspositionen für die beiden Aufgaben aufgeführt:

### <a name="service-agreement"></a>Servicevertrag

| Project | Servicevertrag | Beschreibung                                  | Gruppieren   |
|---------|-------------------|----------------------------------------------|---------|
| 9012    | 000008\_001       | Inspektion und routinemäßige Erneuerung – GB-1234 | Zulage |

### <a name="service-agreement-lines"></a>Servicevertragspositionen

| Beschreibung             | Buchungsart | Serviceobjekt | Serviceaufgabe |
|-------------------------|------------------|----------------|--------------|
| Inspektion und Reinigung | Stunde             | GB-1234        | I/R – GB1234 |
| Anfahrt                  | Expense          | GB-1234        | I/R – GB1234 |
| Material               | Artikel             | GB-1234        | I/R – GB1234 |
| Routinemäßige Erneuerung     | Stunde             | GB-1234        | RE – GB1234  |
| GR-1                    | Artikel             | GB-1234        | RE – GB1234  |
| GR-5                    | Artikel             | GB-1234        | RE – GB1234  |

Den Servicevereinbarungspositionen der beiden Einzelaufgaben sind zwei Serviceaufgaben zugeordnet. Durch diese Serviceaufgaben ergeben sich die Buchungen für den jeweiligen Einzelvorgang. Im ersten Fall steht die Serviceaufgabe "I/R – GB1234" für alle Servicevereinbarungspositionen, die die Inspektion und Reinigung des Objekts "GB-1234" betreffen. Im zweiten Fall sind steht die Serviceaufgabe "RA – GB1234" für alle Servicevereinbarungspositionen für die routinemäßige Erneuerung.

Die Verknüpfung der Serviceaufgaben mit der jeweiligen Vereinbarung erfolgt durch die folgenden Serviceaufgabenbeziehungen:

### <a name="service-tasks"></a>Serviceaufgaben

| Serviceaufgabe | Beschreibung                             | Interner Hinweis                                                                                                                 | Externer Hinweis                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| I/R – GB1234 | Inspektion des Getriebes "GB-1234"           | Sichtprüfung sowie mechanische Prüfung und Reinigung des Getriebes "GB-1234"                                                              | Routinemäßige Getriebeinspektion |
| RE – GB1234  | Routinemäßige Erneuerung von Teilen in "GB-1234" | Routinemäßige Erneuerung der Komponenten "GR-1" und "GR-5". Bei vor 2002 gefertigten Getrieben muss auch die Komponente "GR-2" getauscht werden. | Routinemäßige Erneuerung von Teilen  |

## <a name="group-service-orders"></a>Gruppen-Serviceaufträge

Bei der automatischen Erstellung von Serviceaufträgen können Serviceaufgaben als Gruppierungskriterien verwendet werden. Sollen Serviceaufträge nach Serviceaufgaben gruppiert werden, legen Sie in der Servicevereinbarung fest, dass für die auf der Servicevereinbarung basierenden Serviceaufträge die Serviceaufgabenkennung als anfängliche Gruppierungskriterien verwendet werden sollen.

**Gruppieren nach Serviceaufgabe**

1. Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.
2. Auf der Registerkarte **Einstellungen** wählen Sie **Nach Serviceaufgabe** im Feld **Serviceaufträge kombinieren** aus.


