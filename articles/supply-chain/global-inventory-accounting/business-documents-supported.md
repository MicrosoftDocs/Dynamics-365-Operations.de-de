---
title: Geschäftsbelege, die von der Globalen Bestandsbuchhaltung unterstützt werden
description: Dieses Thema listet die Belege auf, die von der Globalen Bestandsbuchhaltung unterstützt werden. Es enthält auch ein detailliertes Beispiel für Einkaufsbestellung Belege.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 47251a7167a00346aed26b9e9535f1b12301e5a6
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860585"
---
# <a name="business-documents-supported-by-global-inventory-accounting"></a>Geschäftsbelege, die von der Globalen Bestandsbuchhaltung unterstützt werden

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Nachdem das Add-In für die Globale Bestandsbuchhaltung vollständig eingerichtet ist, ist es bereit, bestandsbezogene Belege zu verarbeiten, die in Microsoft Dynamics 365 Supply Chain Management eingegeben werden.

## <a name="supported-business-documents"></a>Unterstützte geschäftliche Belege

Es gibt zwei Arten von geschäftlichen Belegen:

- **Dokumente, die eine Erfassung haben** – Zu diesen Belegen gehören Produktzugang, Einkaufsrechnung, Lieferschein und Verkaufsrechnung.
- **Dokumente, die kein Journal haben** – Zu diesen Belegen gehören Zähl-, Bewegungs- und Bestandskorrekturbelege.

Später in diesem Thema werden Bestellungen als Beispiel verwendet, um den Prozess zu veranschaulichen.

Die folgende Tabelle listet die Belege auf, die die aktuelle Version unterstützt.

| Dokumenttyp      | Dokument        |
|--------------------|-----------------|
| Bestellung     | Produktzugang |
| Bestellung     | Rechnung         |
| Auftrag        | Lieferschein    |
| Auftrag        | Rechnung         |
| Lagererfassung | Bewegung        |
| Lagererfassungen | Regulierung      |
| Lagererfassungen | Inventur        |
| Lagererfassungen | Übertrag        |
| Umlagerungsauftrag     | Lieferung        |
| Umlagerungsauftrag     | Empfangen         |

> [!IMPORTANT]
> Die Globale Bestandsbuchhaltung verarbeitet asynchron die Belege, die im Supply Chain Management eingegeben werden. Für problematische Belege werden keine Fehlermeldungen angezeigt.

## <a name="example-purchase-order"></a>Beispiel: Einkaufsbestellung

### <a name="product-receipt"></a>Produktzugang

Buchen Sie Produktzugänge auf die übliche Weise. Wählen Sie auf der Seite **Alle Bestellungen** eine Bestellung aus und wählen Sie dann im Aktionsbereich auf der Registerkarte **Empfang** die Option **Produkteingang**, um die Seite **Produkteingangsjournal** zu öffnen. Für jede Zeile wird ein Vorgang und ein globales Ereignis in der Buchhaltung erzeugt. Wählen Sie daher die Registerkarte **Zeilen** und dann **Inventar \> Ereignisse und Messungen**, um die Seite **Ereignisse und Messungen** zu öffnen.

Die Globale Bestandsbuchhaltung ist ein Buchhaltungssystem, das auf Ereignissen und Messungen basiert. Das Raster der Messlinien auf der Seite **Ereignisse und Messungen** zeigt eine Liste von Messungen an. Jede Messung hat eine Liste von Dimensionen.

Für jedes Ereignis eines Vorgangs gibt es zwei Arten von Messungen:

- **Vorgangsmessungen** – Diese Messungen beschreiben Geschäftsbelege in allgemeiner Form. Eine Messung ist die Produktmenge unter Verwendung der Maßeinheit, die in dem Beleg verwendet wird. Es gibt auch Messungen, die sich auf den Bestandswert auswirken, wie z. B. erweiterter Preis, Rabatt, Rabattprozent und Zeilengebühr.
- **Kennzahlen der Ressourcenbuchhaltung** – Diese Messungen sind aus der Perspektive des Lagermanagement-Registers. Sie beschreiben die Auswirkung des Belegs auf den Bestand in der Maßeinheit des Bestands. Wenn es mehrere Bestandsregistrierungen gibt, gibt es mehrere Zeilen mit Messungen der Ressourcenbuchhaltung.

Die Dimensionen sind wie folgt organisiert:

- **Dualität** – Die Dualität beschreibt die Agenten, die an den wirtschaftlichen Ereignissen teilnehmen. Für externe Geschäftsbelege beschreiben die primären Dimensionen die juristische Entität, in der der Beleg erfasst wird, während die dualen Dimensionen den Kreditor, Debitor usw. beschreiben. Bei internen Belegen (z. B. Umlagerungsaufträgen) beschreiben die dualen Dimensionen den Gegenlagerort.
- **Dimensionstyp** – Dimensionstypen kategorisieren die Dimensionen.
- **Dimension** – Der Name der Dimension.
- **Dimensionswert** – Der Wert der Dimension.

### <a name="global-inventory-accounting-event"></a>Globale Bestandsbuchhaltung Ereignis

Die Globale Bestandsbuchhaltung nimmt die operativen Ereignisse und Messungen als Eingabe. Sie führt dann die entsprechende Buchhaltung für jedes zugehörige Sachkonto durch, basierend auf der angehängten Währung und Konvention. Sie können **Globale Bestandsbuchhaltung Ereignisse und Messungen** wählen, um das Ereignis Globale Bestandsbuchhaltung anzuzeigen. Das Ereignis Globale Bestandsbuchhaltung folgt der gleichen Methodik wie die Vorgänge, verwendet aber andere Messungen. Es gibt drei Hauptarten von Messungen: Produktkostenmenge, Produktkosten und Abweichung.

Untergeordnete Sachkonten werden verwendet, um die Messungen weiter zu klassifizieren. Es kann mehrere Sachkonten geben. Diese Sachkonten sind mit der juristischen Entität verknüpft, in der der Beleg erfasst wird. Sie können die Ereignisse und Messungen für jedes Sachkonto anzeigen, indem Sie den Wert des Feldes **Sachkonto** ändern.

### <a name="cost-element"></a>Kostenelement

Basierend auf der Richtlinie für Kostenarten, die mit dem Sachkonto verknüpft ist, ordnet das System jeder Messung für ein kalkuliertes Ereignis, das sich auf die Kosten des Bestands auswirkt, eine Kostenart zu. Zu diesen Messungen gehören der erweiterte Preis, der Rabatt, der Rabattprozentsatz und die Zeilengebühr.

### <a name="measurement-line-details"></a>Details zu Messposition

Die Registerkarte **Übersicht** zeigt die Details der angehängten Richtlinien. Die Dimensionen des Kostenträgers zeigen das Kostenobjekt, basierend auf der Richtlinie für den Kostenträger. Die Dimensionen der spezifischen Identifikation zeigen die Batch-Nummer, wenn die Annahme des Kostenflusses *Spezifisch – Batch* ist.

### <a name="purchase-invoice"></a>Einkaufsrechnung

Buchen Sie die Rechnung auf die übliche Weise. Wählen Sie dann im Aktionsbereich auf der Registerkarte **Rechnung** in der Gruppe **Journale** die Option **Rechnung**, um das Rechnungsjournal zu öffnen. Für jede Zeile wird ein Vorgang und ein Ereignis der Globalen Bestandsbuchhaltung erzeugt. Wählen Sie daher die Registerkarte **Zeilen** und dann **Inventar \> Ereignisse und Messungen**, um die Seite **Ereignisse und Messungen** zu öffnen. Die Seite **Ereignisse und Messungen** zeigt denselben Kennzahlentyp. Da die Seite jedoch eine andere Kennzahlen-Rolle und einen anderen Kennzahlen-Modifikator anzeigt, sind die Auswirkungen auf den Bearbeiter (juristische Entität) unterschiedlich.

Wählen Sie **Ereignisse und Messungen der Globalen Bestandsbuchhaltung**, um das Ereignis Globale Bestandsbuchhaltung anzuzeigen. Die Bestandsmenge und die Kosten fließen jetzt aus dem untergeordneten Sachkonto *Wareneingang nicht kalkulierter Bestand* heraus und in das untergeordnete Sachkonto *Kosten für gekaufte Waren*.
