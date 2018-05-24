---
title: Erstellen von Serviceaufgabenbeziehungen
description: "Sie können Serviceaufgaben Servicevereinbarungen oder Serviceaufträgen zuordnen, um die Serviceaufgabe zu beschreiben, die für die Vereinbarung oder den Auftrag ausgeführt werden soll."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0892161605401420c0817b3b644271357446a99b
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-task-relations"></a>Erstellen von Serviceaufgabenbeziehungen    

[!include [banner](../includes/banner.md)]

Sie können Serviceaufgaben Servicevereinbarungen oder Serviceaufträgen zuordnen, um die Serviceaufgabe zu beschreiben, die für die Vereinbarung oder den Auftrag ausgeführt werden soll. Diese Informationen stehen Servicetechnikern und Debitoren zur Verfügung.

## <a name="create-a-relation-with-a-service-agreement"></a>Erstellen einer Beziehung mit einer Servicevereinbarung

1.  Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.

2.  Wählen Sie eine vorhandene Servicevereinbarung aus, oder erstellen Sie eine neue.

3.  Klicken Sie im Aktivitätsbereich auf die Schaltfläche **Serviceaufgaben**.

4.  Drücken Sie im Formular **Serviceaufgaben** die Tastenkombination STRG+N, um eine neue Position zu erstellen. Wählen Sie in der Liste **Serviceaufgaben** dann eine Serviceaufgabe aus, um die Serviceaufgabe der Servicevereinbarung zuzuordnen.

5.  Geben Sie in die Freitextfelder der Registerkarte **Beschreibung** interne oder externe Hinweise ein.

6.  Schließen Sie das Formular, um den Datensatz zu speichern.

Wiederholen Sie diese Schritte, bis alle erforderlichen Serviceaufgabenbeziehungen für die Servicevereinbarung erstellt wurden. Anschließend können die Serviceaufgaben für beliebige zugeordnete Vereinbarungspositionen angegeben werden.

Eine für eine Servicevereinbarung erstellte Serviceaufgabenbeziehung ist in allen Serviceaufträgen verfügbar, die der Servicevereinbarung zugeordnet sind.

## <a name="create-a-relation-with-a-service-order"></a>Erstellen einer Beziehung mit einem Serviceauftrag

1.  Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.

2.  Wählen Sie einen vorhandenen Serviceauftrag aus, oder erstellen Sie einen neuen.

3.  Klicken Sie im Aktivitätsbereich auf die Schaltfläche **Serviceaufgaben**.

4.  Drücken Sie im Formular **Serviceaufgaben** die Tastenkombination STRG+N, um eine neue Position zu erstellen. Wählen Sie in der Liste **Serviceaufgaben** dann eine Serviceaufgabe aus, um die Serviceaufgabe der Servicevereinbarung zuzuordnen.

5.  Geben Sie in die Freitextfelder der Registerkarte **Beschreibung** interne oder externe Hinweise ein.

6.  Schließen Sie das Formular, um den Datensatz zu speichern.

Wiederholen Sie diese Schritte, bis alle erforderlichen Serviceaufgabenbeziehungen für die Servicevereinbarung erstellt wurden. Die Serviceaufgabe, für die die Beziehung erstellt wurde, kann nun beim Erstellen von Serviceauftragspositionen ausgewählt werden.

Für einen Serviceauftrag erstellte Serviceaufgabenbeziehungen sind für den speziellen Serviceauftrag verfügbar.

## <a name="see-also"></a>Siehe auch

[Serviceaufgaben](service-tasks.md)


  



