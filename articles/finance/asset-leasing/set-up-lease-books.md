---
title: Leasingbücher einrichten
description: In diesem Thema werden die Informationen beschrieben, die in Leasingbüchern verwaltet werden. Leasingbücher enthalten die Rechnungslegungsgrundsätze, die bestimmen, wie ein Mietvertrag im System bilanziert wird.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4443773"
---
# <a name="set-up-lease-books"></a>Leasingbücher einrichten

[!include [banner](../includes/banner.md)]

Leasingbücher enthalten die Rechnungslegungsgrundsätze, die bestimmen, wie ein Mietvertrag im System bilanziert wird. Neben der Bilanzierung auf Cash-Basis unterstützt Anlagenleasing die folgenden Standards:

- Allgemein anerkannte Rechnungslegungsgrundsätze in den USA (US-GAAP)
- Thema 842 zur Kodifizierung von Rechnungslegungsstandards (ASC 842)
- ASC 840
- Internationaler Financial Reporting-Standard 16 (IFRS 16)
- International Buchführungsstandard 17 (IAS 17)

Gehen Sie folgendermaßen vor, um einen Mietvertrag zu erstellen.

1. Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Leasingbücher**.
2. Wählen Sie **Neu** aus, um ein Buch hinzuzufügen.
3. Stellen Sie die folgenden Felder ein.

    | Name                                     | Beschreibung |
    |------------------------------------------|-------------|
    | Buchungsebene                            | Wählen Sie die zu verwendende Buchungsebene aus. Jedes Buch, das einem Mietvertrag beigefügt ist, wird für eine bestimmte Buchungsebene eingerichtet. Jede Buchungsebene hat unterschiedliche Buchungszwecke. |
    | Mietvertragstyp                               | Wählen Sie aus, ob der Mietvertrag automatisch klassifiziert werden soll oder ob es als Finanzierungsleasing oder Ausrüstungs-Leasingvertrag vordefiniert werden soll. |
    | Buchhaltungsframework                     | Wählen Sie das Framework aus dass dem Buch zugeordnet ist. |
    | Einrichten von Mietdauer/Nutzungsdauer          | Das System klassifiziert den Mietvertrag als ein Finanzierungsleasing, wenn die Mietvertragsgart auf **Automatisch** eingestellt ist und das Verhältnis der Mietdauer zur Nutzungsdauer der Anlage größer oder gleich dem im Feld eingegebenen Prozentsatz ist.  |
    | Einrichtung von Barwert/Anlagenzeitwert   | Geben Sie eine ganze Zahl ein, um den Schwellenwert zu definieren, der den Mietvertragstyp bestimmt. Wenn der Barwert zukünftiger Mindestmietzahlungen höher ist als der benutzerdefinierte Wert aus der Buchkonfiguration, und wenn die Mietvertragsklassifizierung des Buches auf „Automatisch“ eingestellt ist, klassifiziert das System den Mietvertrag als Finanzierungsleasing. |
    | Kurzfristiger Schwellenwert                     | Geben Sie die Anzahl der Monate ein, die als Schwellenwert für kurzfristige Mietverträge verwendet werden sollen. Wenn die Laufzeit des Mietvertrags kleiner oder gleich der Anzahl der Monate ist, die Sie hier eingeben, klassifiziert das System den Mietvertrag als kurzfristigen Mietvertrag, und die Behandlung der zurückgestellten Miete wird angewendet. |
    | Schwellenwert für geringen Wert                      | Geben Sie einen Betrag ein, der als Schwellenwert für Leasingobjekte mit geringem Wert verwendet werden soll. Wenn der Zeitwert der Anlage kleiner oder gleich des hier eingegebenen Werts ist, klassifiziert das System den Mietvertrag als Leasingobjekt von geringem Wert, und die Behandlung der zurückgestellten Miete wird angewendet. |
    | An Kreditor bezahlen                            | Setzen Sie diese Option auf **Ja**, damit Mietzahlungen als Rechnung auf das in jedem Mietvertrag angegebene Kreditorenkonto gebucht werden können. Wenn eine Mietzahlung gebucht wird, wird das Kreditorenkonto gutgeschrieben. Wenn diese Option auf **Nein** gesetzt ist, wird stattdessen das Konto gutgeschrieben, das für die **Mietzahlung**-Buchungsart auf der **Leasingbuchungsparameter**-Seite angegeben ist. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]