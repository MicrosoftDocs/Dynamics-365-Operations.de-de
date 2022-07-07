---
title: Erstellen von Serviceaufgabenbeziehungen
description: Sie können Serviceaufgaben Servicevereinbarungen oder Serviceaufträgen zuordnen, um die Serviceaufgabe zu beschreiben, die für die Vereinbarung oder den Auftrag ausgeführt werden soll.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51ea26a0f6519d26f5207a7b6c8afbcdfa358be9
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015258"
---
# <a name="create-service-task-relations"></a>Erstellen von Serviceaufgabenbeziehungen    

[!include [banner](../includes/banner.md)]

Sie können Serviceaufgaben Servicevereinbarungen oder Serviceaufträgen zuordnen, um die Serviceaufgabe zu beschreiben, die für die Vereinbarung oder den Auftrag ausgeführt werden soll. Diese Informationen stehen Servicetechnikern und Debitoren zur Verfügung.

## <a name="create-a-relation-with-a-service-agreement"></a>Erstellen einer Beziehung mit einer Servicevereinbarung

1.  Gehen Sie zu **Serviceverwaltung** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.

2.  Wählen Sie eine vorhandene Servicevereinbarung aus, oder erstellen Sie eine neue.

3.  Wählen Sie im Aktivitätsbereich die Schaltfläche **Serviceaufgaben**.

4.  Wählen Sie im Formular **Serviceaufgaben** die Option **Neu**, um eine neue Zeile zu erstellen, und wählen Sie dann eine Serviceaufgabe aus der Liste **Serviceaufgabe**, um die Serviceaufgabe an die Servicevereinbarung anzuhängen.

5.  Geben Sie in die Freitextfelder der Registerkarte **Beschreibung** interne oder externe Hinweise ein.

6.  Schließen Sie das Formular, um den Datensatz zu speichern.

Wiederholen Sie diese Schritte, bis alle erforderlichen Serviceaufgabenbeziehungen für die Servicevereinbarung erstellt wurden. Anschließend können die Serviceaufgaben für beliebige zugeordnete Vereinbarungspositionen angegeben werden.

Eine für eine Servicevereinbarung erstellte Serviceaufgabenbeziehung ist in allen Serviceaufträgen verfügbar, die der Servicevereinbarung zugeordnet sind.

## <a name="create-a-relation-with-a-service-order"></a>Erstellen einer Beziehung mit einem Serviceauftrag

1.  Gehen Sie zu **Serviceverwaltung** \> **Serviceaufträge** \> **Serviceaufträge**.

2.  Wählen Sie einen vorhandenen Serviceauftrag aus, oder erstellen Sie einen neuen.

3.  Wählen Sie im Aktivitätsbereich die Schaltfläche **Serviceaufgaben**.

4.  Wählen Sie im Formular **Serviceaufgaben** die Option **Neu**, um eine neue Zeile zu erstellen, und wählen Sie dann eine Serviceaufgabe aus der Liste **Serviceaufgabe**, um die Serviceaufgaben an den Serviceauftrag anzuhängen.

5.  Geben Sie in die Freitextfelder der Registerkarte **Beschreibung** interne oder externe Hinweise ein.

6.  Schließen Sie das Formular, um den Datensatz zu speichern.

Wiederholen Sie diese Schritte, bis alle erforderlichen Serviceaufgabenbeziehungen für die Servicevereinbarung erstellt wurden. Die Serviceaufgabe, für die die Beziehung erstellt wurde, kann nun beim Erstellen von Serviceauftragspositionen ausgewählt werden.

Für einen Serviceauftrag erstellte Serviceaufgabenbeziehungen sind für den speziellen Serviceauftrag verfügbar.

## <a name="see-also"></a>Siehe auch

[Serviceaufgaben – Übersicht](service-tasks.md)


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]