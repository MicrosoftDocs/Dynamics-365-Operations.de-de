---
title: Automatische Erstellung von Serviceaufträgen
description: Sie können Serviceaufträge für einen oder mehrere Serviceverträge erstellen.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db9d337166f05f80cfdb9d4b82533117daa871e9
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014695"
---
# <a name="create-service-orders-automatically"></a>Automatische Erstellung von Serviceaufträgen    

[!include [banner](../includes/banner.md)]


Sie können Serviceaufträge für einen oder mehrere Serviceverträge erstellen. Bei der Erstellung können die Serviceaufträge im Formular **Serviceaufträge** angezeigt werden.

Serviceaufträge werden nur für den Gültigkeitszeitraum des Servicevertrags erstellt. Liegt das Intervall, das Sie im Formular **Serviceaufträge erstellen** angeben, vor dem Startdatum oder nach dem Enddatum des Servicevertrags, werden Serviceaufträge nur für den Bereich des Intervalls erstellt, der innerhalb des Zeitraums des Servicevertrags liegt.

Werden Serviceaufträge manuell oder automatisch anhand der Servicevertragsposition erstellt, muss der Serviceauftrag in das Zeitintervall fallen, das durch das Start- und Enddatum für die Position definiert wird, sofern Sie kein Enddatum für die Position angeben.

## <a name="create-service-orders-automatically-for-a-service-agreement"></a>Automatisches Erstellen von Serviceaufträgen für einen Servicevertrag

1.  Klicken Sie auf **Serviceverwaltung** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.

2.  Wählen Sie einen Servicevertrag aus.

3.  Klicken Sie auf der Registerkarte **Liefern** und dann auf **Geplante Serviceaufträge**.

4.  Geben Sie Datumsangaben in die Felder **Von Datum** und **Bis Datum** ein, um die Serviceperiode zu definieren.

5.  Aktivieren Sie das Kontrollkästchen **Infolog anzeigen**, um eine Liste der erstellten Serviceaufträge anzuzeigen.

6.  Wählen Sie Buchungsarten in der Feldgruppe **Buchungsarten einschließen** aus. Die Buchungsarten stehen für die Positionen, die im Servicevertrag erstellt werden. Abhängig vom Serviceintervall, das für die Servicevertragsposition angegeben wurde, erzeugt jede ausgewählte Buchungsart mehrere Serviceaufträge.

7.  Aktivieren Sie das Kontrollkästchen **Fortlaufend**, um die Serviceaufträge zu erstellen, die in einer fortlaufenden Reihe von Serviceaufträgen fehlen.

8.  Klicken Sie auf **OK**.

## <a name="create-service-orders-automatically-for-several-service-agreements"></a>Automatisches Erstellen von Serviceaufträgen für mehrere Serviceverträge

1.  Klicken Sie auf **Serviceverwaltung** \> **Periodisch** \> **Serviceaufträge** \> **Serviceaufträge erstellen**.

2.  Klicken Sie auf **Auswählen**, um eine Auswahl zum Hinzufügen oder Entfernen von Kriterien für die Erstellung von Serviceaufträgen zu treffen.

3.  Klicken Sie auf **OK**.

## <a name="see-also"></a>Siehe auch

[Serviceaufträge](service-orders.md)

[Automatisches Erstellen von Serviceaufträgen](auto-create-service-orders.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]