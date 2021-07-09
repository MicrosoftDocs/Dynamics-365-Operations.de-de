---
title: Der Kreditor-Code ist für ein bestimmtes Produkt und Datum nicht autorisiert
description: Wenn Sie versuchen, einen geplanten Auftrag zu fixieren oder eine Zeile zu einer Bestellung hinzuzufügen, erhalten Sie eine Fehlermeldung, die besagt, dass der Kreditor-Code für ein Produkt und ein Datum nicht autorisiert ist.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294086"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a>Der Kreditor-Code ist für ein bestimmtes Produkt und Datum nicht autorisiert

Fehlercode: SYP4881415

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, einen geplanten Auftrag zu fixieren oder eine Zeile zu einer Einkaufsbestellung hinzuzufügen, erhalten Sie die folgende Fehlermeldung:

> Der Lieferantencode %1 ist für %2 auf %3 nicht autorisiert.

## <a name="cause"></a>Ursache

Der Fehler tritt auf, weil das Feld **Prüfmethode für genehmigte Kreditor** für das angegebene Produkt auf *Nur Warnung* oder *Nicht zulässig* festgelegt ist und der Kreditor derzeit nicht berechtigt ist, dieses Produkt zu liefern.

## <a name="resolution"></a>Lösung

Um dieses Problem zu beheben, deaktivieren Sie entweder die Lieferantenprüfung für das betreffende Produkt oder genehmigen Sie den Kreditor.

Gehen Sie folgendermaßen vor, um die Lieferantenprüfung für ein Produkt zu deaktivieren.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Öffnen Sie das entsprechende Produkt.
1. Legen Sie auf der Inforegister-Registerkarte **Kauf** das Feld **Zugelassene Methode der Lieferantenprüfung** auf einen anderen Wert als *Nur Warnung* oder *Nicht zugelassen* fest.

Gehen Sie folgendermaßen vor, um einen Kreditor für ein Produkt zu genehmigen.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Öffnen Sie das entsprechende Element.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Einkauf** in der Gruppe **Genehmigter Kreditor** die Option **Einrichten**.
1. Fügen Sie auf der Listenseite **Genehmigter Kreditor** eine Zeile zum Raster hinzu und legen Sie die folgenden Werte dafür fest:

    - **Lieferant** – Wählen Sie den zu genehmigenden Kreditor für das aktuelle Produkt aus.
    - **Gültig ab** – Wählen Sie das erste Datum, für das der Kreditor genehmigt wird.
    - **Ablaufdatum** – Wählen Sie das letzte Datum aus, für das der Kreditor genehmigt ist.

Weitere Informationen finden Sie unter [Lieferanten für bestimmte Produkte genehmigen](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).
