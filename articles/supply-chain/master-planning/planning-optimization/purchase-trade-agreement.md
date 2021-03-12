---
title: Produktprogrammplanung mit Kaufverträgen
description: In diesem Thema wird beschrieben, wie die Planungsoptimierung den Lieferanten und/oder die Vorlaufzeit für einen geplanten Auftrag basierend auf dem besten Preis oder der besten Vorlaufzeit in Kaufverträgen ermitteln kann.
author: ChristianRytt
manager: tfehr
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e060f20b65153a7bbe70996e6ff4c3930468348a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992244"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Produktprogrammplanung mit Kaufverträgen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie die Planungsoptimierung den Lieferanten und/oder die Vorlaufzeit für einen Planauftrag basierend auf dem besten Preis oder der besten Vorlaufzeit in Kaufverträgen für ein bestimmtes Produkt ermitteln kann.

## <a name="turn-on-the-purchase-trade-agreements-for-planning-optimization-feature"></a>Aktivieren Sie die Funktion Kaufverträge für die Funktion Planungsoptimierung

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit der Einstellung [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:

- **Modul:** *Produktprogrammplanung*
- **Funktionsname:** *Kaufverträge für die Planungsoptimierung*

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Bereiten Sie Ihr System vor, um Kaufverträge während der Masterplanung zu bewerten

Führen Sie die folgenden Schritte aus, um Ihr System für die Anwendung der Planungsoptimierung zu konfigurieren, mit der Kaufverträge bewertet werden.

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Produktprogrammplanparameter**. Auf der Registerkarte **Geplanter Auftragen** im Abschnitt **Lieferant** stellen Sie die folgenden Werte ein:

    - **Kaufvertrag finden** – Setzen Sie diese Option auf **Ja**, um Kaufverträge in der Produktprogrammplanung einzubeziehen.
    - **Suchkriterium** – Wählen Sie den Faktor aus, den Sie für jeden Kaufvertrag priorisieren möchten: **Minimale Vorlaufzeit** oder **Niedrigster Stückpreis**.

1. Gehen Sie zu **Beschaffung \> Installieren \> Preise und Rabatte \> Preis/Rabatt aktivieren** und stellen Sie sicher, dass die Option **Lieferant** auf **Ja** festgelegt ist.
1. Gehen Sie zu **Produktinformationsmanagement \> Installieren \> Dimensions- und Variantengruppen \> Speicherdimensionsgruppen** und wählen Sie eine Speicherdimensionsgruppe aus, die für Produkte gilt, für die die Produktprogrammplanung Kaufverträge bewerten soll. Stellen Sie sicher, dass jede relevante Speicherdimension in dieser Gruppe ein Häkchen in der Spalte **Für Kaufpreise** hat. Wiederholen Sie diesen Schritt für jede andere relevante Speicherdimensionsgruppe.

## <a name="prepare-a-released-product-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Bereiten Sie Ihre freigegebenen Produkte vor, um Kaufverträge während der Produktprogrammplanung zu bewerten

Nachdem Sie Ihr System wie im vorherigen Abschnitt beschrieben vorbereitet haben, sollten Sie die folgenden Schritte ausführen, um sicherzustellen, dass jedes Produkt, das Sie mit dieser Funktion verwenden möchten, korrekt eingerichtet ist.

1. Wechseln Sie **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte** und öffnen Sie ein Zielprodukt.
1. Auf dem Inforegister **Kauf** stellen Sie sicher, dass kein Lieferant dem Feld **Lieferant** zugewiesen ist.
1. Wählen Sie im Aktivitätenbereich in der Registerkarte **Plan** in der Gruppe **Abdeckung** **Artikelabdeckung**, um die Seite **Artikelabdeckung** zu öffnen. Überprüfen Sie die folgenden Einstellungen:

    - Auf der Registerkarte **Allgemein** können Sie Herstellerüberschreibungen einrichten. Wenn Sie möchten, dass die Planungsoptimierung Kaufverträge zur Auswahl eines Lieferanten verwenden soll, sollten Sie Lieferantenüberschreibungen verhindern, indem Sie das Kontrollkästchen **Verwenden Sie eine bestimmte Einstellung** deaktivieren.
    - Auf der Registerkarte **Vorlaufzeit** können Sie Vorlaufzeitüberschreibungen einrichten. Wenn die Planungsoptimierung Kaufverträge zur Auswahl von Vorlaufzeiten verwenden soll, sollten Sie Vorlaufzeitüberschreibungen verhindern. Deaktivieren Sie das Kontrollkästchen für jede Art von Vorlaufzeit, die Sie mithilfe von Kaufverträgen auswählen möchten (**Kauf**, **Produktion** und/oder **Übertragung**).

1. Schließen Sie die Seite **Artikelabdeckung**, um zur Detailseite für das ausgewählte Produkt zurückzukehren.
1. Im Aktionsbereich auf der Registerkarte **Plan** in der Gruppe **Prognose** wählen Sie **Beschaffungsplanung**, um die Seite **Beschaffungsplanung** zu öffnen. Stellen Sie sicher, dass keine Zeile, die hier angezeigt wird, einen Wert in der Spalte **Lieferantenkonto** hat.
1. Schließen Sie die Seite **Beschaffungsplanung**, um zur Detailseite für das ausgewählte Produkt zurückzukehren.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Kauf** in der Gruppe **Kaufvertrag** auf **Kaufvertrag anzeigen**. Stellen Sie sicher, dass alle relevanten Kaufverträge aufgelistet sind. Stellen Sie auch sicher, dass die Option **Vorlaufzeit ignorieren** auf **Nein** festgelegt ist für jede Vereinbarung, bei der die Planungsoptimierung die für diese Vereinbarung angegebene Vorlaufzeit verwenden soll.
1. Wählen Sie im Aktivitätenbereich in der Registerkarte **Plan** in der Gruppe **Auftragseinstellungen** **StandardAuftragseinstellungen** aus, um die Seite **Artikelabdeckung** zu öffnen. Auf dem Inforegister **Auftrag** zeigen Sie den Wert vom Feld **Kaufvorlaufzeit** an. Wenn keine Vorlaufzeitüberschreibung für die Artikelabdeckung definiert ist, verwendet die Planungsoptimierung diesen Wert, wenn Kaufverträge ausgewählt werden, bei denen die **Vorlaufzeit ignorieren** Option auf **Ja** festgelegt ist. Daher sollten Sie diesen Wert nach Bedarf anpassen.
1. Wiederholen Sie diese Schritte für jedes relevante Produkt.

> [!NOTE]
> Die Währung in der Kaufvertragszeile muss mit der Währung des ausgewählten Lieferanten übereinstimmen. Die Produktprogrammplanung enthält nur Informationen aus Kaufverträgen, bei denen die Währung mit der Währung des Lieferanten übereinstimmt.

## <a name="examples-of-how-planning-optimization-finds-vendor-and-lead-times"></a>Beispiele dafür, wie die Planungsoptimierung Lieferanten- und Vorlaufzeiten ermittelt

Die folgende Tabelle enthält Beispiele, die zeigen, wie sich verschiedene Einstellungen für ein freigegebenes Produkt und die damit verbundenen Kaufverträge auf die Werte auswirken, die für die resultierende geplante Auftrag gefunden werden. Der Wert **Fett gedruckt** in den beiden Spalten ganz rechts sind die Werte, die von der Planungsoptimierung ausgewählt werden. Die **_fett und kursiv_* _ gedruckten Werte in den anderen Spalten sind die Einstellungen, die die resultierenden Werte für jede Zeile erzeugt haben.

| Freigegebenes Produkt: Lieferant | Standardmäßige Auftragseinstellung: Vorlaufzeit | Artikelabdeckung: Lieferant überschreiben | Artikelabdeckung: Vorlaufzeit überschreiben | Kaufvertrag: Lieferant | Kaufvertrag: Lieferzeit | Kaufvertrag: Vorlaufzeit ignorieren | Resultierender Anbieter | Resultierende Vorlaufzeit |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| _*_US001_*_ | _*_1_*_ | Nr. | Nr. | US003 | 3 | Nr. | _ *US001** | **1** |
| US001 | 1 | **_Ja: US002_* _ | _*_Ja: 2_*_ | US003 | 3 | Nr. | _ *US002** | **2** |
| *(Leer)* | 1 | Nr. | Nr. | ***US003** _ | _*_3_*_ | Nr. | _ *US003** | **3** |
| *(Leer)* | ***1** _ | Nr. | Nr. | _*_US003_*_ | 3 | Ja | _ *US003** | **1** |
| *(Leer)* | ***1** _ | _*_Ja: US002_*_ | Nr. | US003 | 3 | Nr. | _ *US002** | **1** |
| *(Leer)* | ***1** _ | _*_Ja: US002_*_ | Nr. | US003 | 3 | Nr. | _ *US002** | **1** |
| *(Leer)* | 1 | Nr. | Ja: 2 | ***US003** _ | _*_3_*_ | Nr. | _ *US003** | **3** |
| *(Leer)* | 1 | Nr. | ***Ja: 2** _ | _*_US003_*_ | 3 | Ja | _ *US003** | **2** |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Kaufverträge](../../procurement/purchase-agreements.md)
