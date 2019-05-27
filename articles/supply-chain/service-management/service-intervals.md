---
title: Serviceintervalle
description: Durch das Servicevereinbarungsintervall wird die Häufigkeit angegeben, mit der bei der automatischen Erstellung von Serviceaufträgen Serviceauftragspositionen für Servicevereinbarungspositionen erstellt werden.
author: ShylaThompson
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10078cbd02209126e9655b823fcf844b692a4794
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562648"
---
# <a name="service-intervals"></a>Serviceintervalle

[!include [banner](../includes/banner.md)]

Durch das Servicevereinbarungsintervall wird die Häufigkeit angegeben, mit der bei der automatischen Erstellung von Serviceaufträgen Serviceauftragspositionen für Servicevereinbarungspositionen erstellt werden.

Bei der automatischen Erstellung von Serviceaufträgen werden Serviceauftragspositionen ab dem Startdatum der Vereinbarungsposition gemäß dem Intervall erstellt, das für die Servicevereinbarungsposition festgelegt wurde.

Ist im Formular **Intervall**das Feld  einer Servicevereinbarungsposition auf der Seite **Servicevereinbarung**leer, handelt es sich bei der Position um ein einmaliges Ereignis, und die Position wird nicht zur wiederholten Erstellung von Serviceaufträgen verwendet.

## <a name="example"></a>Beispiel

Dieses Beispiel veranschaulicht, wie sich ein Serviceintervall auf die Servicevertrags- und Serviceauftragspositionen in einem Serviceauftrag auswirkt.

### <a name="create-a-service-agreement"></a>Erstellen Sie eine Servicevereinbarung.

Erstellen Sie zunächst eine Servicevereinbarung und setzen die Option **Serviceaufträge kombinieren** auf **Nach Servicevertrag** fest.

1. **Servicevereinbarungen** anklicken
2. Klicken Sie im **Aktivitätsbereich** auf der Registerkarte **Servicevereinbarung** in der Gruppe **Neu** auf **Servicevereinbarung**, um einen neuen Servicevertrag zu erstellen.
3. Geben Sie auf dem Inforegister **Projekt-ID** eine Beschreibung ein, wählen Sie im Feld **Anfangsdatum** ein Projekt aus, und geben Sie ein Datum ein.
4. Wählen Sie im Feld **Serviceaufträge kombinieren** **Nach Servicevertrag** aus.

Die folgende Servicevereinbarung wurde erstellt:

| Project      | Startdatum                                                                         |
|--------------|------------------------------------------------------------------------------------|
| Ihr Projekt | Das für das Projekt angegebene Datum. In diesem Beispiel wird das aktuelle Datum verwendet. |

### <a name="create-a-service-agreement-line"></a>Erstellen einer Servicevertragsposition

Erstellen Sie im nächsten Schritt eine Servicevertragsposition mit der Buchungsart  **Stunde**.

Um diesen Teil des Beispiels abzuschließen, muss im Formular **Serviceintervall** ein Serviceintervall mit einer Dauer von 10 Tagen erstellt werden. 

1. Wählen Sie den soeben erstellten Servicevertrag aus. 
2. Klicken Sie auf dem Inforegister **Zeilen** auf die Schaltfläche **Hinzufügen**, um im unteren Bereich des Formulars **Servicevereinbarung** eine neue Position zu erstellen.
3. Wählen Sie im Feld **Transaktionstyp** **Stunde** aus.
4. Wählen Sie im Feld **Arbeitskraft** die Arbeitskraft aus, die den Service erbringt.
5. Wählen Sie im Feld **Serviceinterfall** das Serviceintervall von 10 Tagen aus.

Sie haben nun eine Servicevertragsposition mit den folgenden Informationen erstellt:

| Buchungsart | Eintrittstermin                               | Serviceintervall |
|------------------|------------------------------------------|------------------|
| Stunde             | Das aktuelle Datum.                        | Alle 10 Tage    |
| Arbeitskraft           | Die Arbeitskraft, die den Service durchführt. |                  |

Für die Position wurde kein Zeitfenster angegeben. 

### <a name="create-planned-service-orders"></a>Erstellen von geplanten Serviceaufträgen

Sie können nun geplante Serviceaufträge und Serviceauftragspositionen für den kommenden Monat erstellen.

1. Klicken Sie auf der Seite **Servicevereinbarung** auf der Registerkarte **Aktivität** in der Gruppe **Bereitstellung** auf **Geplant Servicevereinbarungen**.
2. Geben Sie im Formular **Serviceaufträge erstellen** das aktuelle Datum im Feld **Datum ab** und im Feld **Datum bis** ein Datum an, das einen Monat hinter dem aktuellen Datum liegt.
3. Setzen Sie den Schieberegler **Stunde** auf **Ja** fest. 
4. Klicken Sie auf **OK**.

Da für den Serviceauftrag keine Gruppierung vorhanden ist (definiert unter Option**Nach Servicevereinbarung** im Feld **Serviceaufträge kombinieren**), wird pro Serviceauftrag jeweils eine Serviceauftragsposition erstellt.

### <a name="service-orders-created"></a>Erstellte Serviceaufträge

Drei Serviceauftragspositionen wurden in dem Zeitrahmen erstellt, den Sie im Dialogfeld **Serviceauftrag erstellen** angegeben haben. Sie können die Serviceauftragspositionen im Formular **Servicevereinbarungen**  (**Aktivitätsbereich** \> **Lieferung**\>**Ansicht** Schaltfläche ) anzeigen.

## <a name="related-topics"></a>Verwandte Themen

[Einrichten von Serviceintervallen](set-up-service-intervals.md)  

