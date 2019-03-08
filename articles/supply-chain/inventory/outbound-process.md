---
title: Ausgangsprozess
description: Dieses Thema enthält einen Überblick über den ausgehenden Prozess in der Lagerverwaltung.
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 5ac3260f128acbc819d7207f68f17adb085da11c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "334380"
---
# <a name="outbound-process"></a>Ausgangsprozess

[!include [banner](../includes/banner.md)]

Dieses Thema enthält einen Überblick über den ausgehenden Prozess in der Lagerverwaltung.

## <a name="output-orders"></a>Abgangsaufträge

Abgangsaufträge werden auch verwendet, um Auftragspositionen und Umlagerungsauftragspositionen mit den ausgehenden Entnahmevorgängen zu verknüpfen, die die Kommissionierlisten verwenden.

Wenn Kommissionierlisten entweder von Aufträgen oder von Umlagerungsaufträgen generiert werden, werden Abgangsaufträge und Lieferungen automatisch erstellt. Eine Kommissionierliste hat eine 1:1-Beziehung mit einer Lieferung. Umlagerungsauftragslieferung oder der Lieferschein der Lieferung können von der Lieferung verarbeitet werden. 

Bei der folgenden Abbildung handelt es sich um eine Übersicht über den Prozess bei ausgehenden Aufträgen. 

[![Hier wird ein Überblick über die ausgehende Auftragsbearbeitung angezeigt](./media/outbound-order.png)](./media/outbound-order.png)

Sie können anhand von Ausgangsregeln festlegen, wie der Ausgangsprozess verarbeitet werden soll. Sie können einen Workflow zur Steuerung des Überprüfungsverfahrens verwenden. Sie können die Regeln verwenden, um zu steuern, in welcher Phase in der Fertigung gesendet werden kann. Die folgenden Einstellungen legen fest, wie ausgehende Verarbeitungen behandelt werden sollen.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>Standardstatus für Verkaufsaufträge und Umlagerungsaufträge verwenden 

Gehen Sie zu **Debitor** \> **Einstellungen** \> **Debitorenparameter**, und dann **Aktualisierungen** und wählen Sie einen Wert im Feld **Status der Entnahmeroute** aus.

[![Standardstatus für Verkaufsaufträge und Umlagerungsaufträge verwenden](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

Wenn das Feld **Status der Entnahmeroute** auf **Abgeschlossen** festgelegt ist, findet die Entnahme automatisch als Teil des Prozesses Generieren von Kommissionierlisten statt. Ist das Feld auf **Aktiviert** festgelegt, müssen die Kommissionierlistenpositionen manuell aktualisiert werden.

Die gleiche Einrichtung gilt für Umlagerungsaufträge. Gehen Sie zu **Lagerverwaltung** \> **Einstellungen** \> **Parameter für Lager- und Lagerortverwaltung**, und dann **Transport** und wählen Sie einen Wert im Feld **Status der Entnahmeroute** aus.

[![Standardstatus für Verkaufsaufträge und Umlagerungsaufträge verwenden](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>Lagerabgangsauftrag beenden

Gehen Sie zu **Lagerverwaltung** \> **Einstellungen** \> **Parameter für Lager- und Lagerortverwaltung** und klicken Sie dann auf der Registerkarte **Allgemeines**, wählen Sie die Option **Lagerabgangsauftrag beenden** aus.

[![Lagerabgangsauftragsoption beenden](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

Wenn der Lagerarbeiter die Kommissionierlistenmengen verringert, werden die entsprechenden Lagerauftragsmengen aus der Lieferung entfernt. Wenn die Kommissionierliste zu einem bestimmten Zeitpunkt aktualisiert wird, werden die verbleibenden Mengen wieder an den Auftrag gemeldet, wenn die Option **Lagerabgangsauftrag beenden** auf **Ja** festgelegt ist. Wenn die Option **Lagerabgangsauftrag beenden** auf **Nein** festgelegt ist, werden die verbleibenden Mengen als offene Abgangsauftragsmenge betrachtet und müssen einer neuen Kommissionierliste als Teil der Funktion **Offene Abgangsaufträge** hinzugefügt werden. 

[![Öffnen Sie Abgangsauftragsbefehl im Feld Funktionsmenü](./media/open-output-order.png)](./media/open-output-order.png)

[![Öffnen Sie Abgangsauftragsbefehl im Feld Funktionsmenü](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>Menge verringern

Der dritte Parameter, den Sie als Teil des Prozesses Generieren von Kommissionierlisten verwenden können, ist der Parameter **Menge verringern**. Die Einstellung dieses Parameters arbeitet mit den **Reservierungs**-Einstellungen, die den Reservierungsprozess als Teil der Freigabe am Lagerort auslösen.

[![Mengenparameter verringern](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>Beispiel eines ausgehenden Prozesses für einen Auftrag

Bei diesem Beispiel gibt es einen Auftrag für zwei Artikel. Während der Generierung von Kommissionierlisten legen Sie den Parameter **Menge verringern** fest. Daher geben Sie Entnahmepositionen nur für verfügbaren Lagerbestand. frei und erstellen diese. Die Entnahme muss über einen Registrierungsprozess für Kommissionierlisten (**Status der Entnahmeroute**)**Aktiviert** = gemeldet werden.

Der Lagerbestand, der noch nicht reserviert wurde, wird für die Generierung von Kommissionierlisten reserviert. Der nicht verfügbare Bestand kann entweder vom Auftrag entfernt oder dem Lagerort für ausgehende Verarbeitung später freigegeben werden, wenn Artikel für Entnahme verfügbar ist.

[![Kommissionierliste aktualisieren](./media/update-picking-list.png)](./media/update-picking-list.png)

Nachdem alle Entnahmepositionen **Entnahmelistenregistrierung** auf der Seite entnommen wurden, wird die zugehörige Lieferung abgeschlossen. Der Prozess für Auftragslieferscheine kann dann basierend auf dem entnommenen Bestand initialisiert werden.

[![Ausgehende Lieferungen aktualisieren](./media/outbound-shipments.png)](./media/outbound-shipments.png)
