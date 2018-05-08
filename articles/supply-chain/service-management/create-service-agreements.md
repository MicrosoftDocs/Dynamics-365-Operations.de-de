---
title: Erstellen von Servicevereinbarungen
description: "In diesem Thema wird beschrieben, wie mithilfe der Funktionen in den Modulen Servicemanagement und Projektmanagement und Buchhaltung Serviceverträge erstellt werden."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2a46173a3566a56a21add9d42c111d456b1ae7c1
ms.openlocfilehash: 517bc1b9de9b2512f42e4f32b4a19e517e349e8e
ms.contentlocale: de-de
ms.lasthandoff: 02/19/2018

---

# <a name="create-service-agreements"></a>Erstellen von Servicevereinbarungen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie mithilfe der Funktionen in den Modulen Servicemanagement und Projektmanagement und Buchhaltung Serviceverträge erstellt werden.

## <a name="create-a-service-agreement-from-service-management"></a>Erstellen eines Servicevertrags aus der Serviceverwaltung

1. Navigieren Sie zu **Serviceverwaltung**.
2. Klicken Sie auf die Schaltfläche **Dienstleistungsvereinbarung** , um im Formularkopf eine neue Servicevertragsposition zu erstellen. 
3. Klicken Sie auf **Neu**. Geben Sie eine Beschreibung ein, wählen Sie einen Verweis auf ein **Projekt-ID** im Feld  aus, und füllen Sie die restlichen Felder und Positionen für den Servicevertrag aus. Klicken Sie auf **Speichern**.
4. Klicken Sie auf die Registerkarte ,**Beziehung** und wählen Sie Erstellen von **Serviceobjektbeziehungen** oder **Serviceaufgabenbeziehungen** für den Servicevertrag Die Serviceobjekte und -aufgaben, für die eine Beziehung erstellt wurden, können den Positionen der Servicevereinbarung zugeordnet werden.
5. Erstellen Sie Servicevereinbarungspositionen in der unteren Hälfte des Formulars , indem Sie Positionen aus einer Servicevorlage oder aus einer anderen Servicevereinbarung kopieren, oder erstellen Sie die Servicevereinbarungspositionen manuell.

> [!NOTE]
> Beim Kopieren von Positionen aus einer anderen Servicevereinbarung kann angegeben werden, ob auch die Serviceobjekt- und die Serviceaufgabenbeziehungen kopiert werden sollen. Werden diese Beziehungen kopiert, werden sie den für die Servicevereinbarung möglicherweise bereits vorhandenen Beziehungen hinzugefügt. Beim Kopieren von Servicevereinbarungspositionen aus einer Servicevorlage werden die Serviceobjekt- sowie die Serviceaufgabenbeziehungen automatisch entsprechend in die neuen Servicevereinbarungspositionen kopiert.

## <a name="create-service-agreement-lines-manually"></a>Manuelles Erstellen von Servicevertragspositionen

1. Fügen Sie im Formular **Servicevereinbarungen**eine Servicevertragsposition im Raster  hinzu. 
2. Geben Sie die für die Servicevereinbarungsposition erforderlichen Informationen ein. 
3. Drücken Sie **STRG+S**, um die Position zu speichern, und schließen Sie anschließend das Formular.

## <a name="create-a-service-agreement-from-project"></a>Erstellen einer Servicevereinbarung mithilfe des Moduls "Projekt"

1. Auf **Projektverwaltung und -buchhaltung** klicken.
2. **Alle Projekte** anklicken.
3. Wählen Sie in der Liste ein Projekt aus.
4. Klicken Sie im **Aktivitätsbereich** auf **Verwalten**. In der Aktivitätsgruppe **Neu** klicken Sie **Dienst** und wählen Sie **Servicevertrag** aus.
5. Führen Sie die Schritte im Abschnitt **Erstellen eines Servicevertrags** aus der Serviceverwaltung" (siehe vorheriger Kommentar in diesem Thema) aus.


## <a name="related-topics"></a>Verwandte Themen

[Servicevereinbarungen](service-agreements.md)



