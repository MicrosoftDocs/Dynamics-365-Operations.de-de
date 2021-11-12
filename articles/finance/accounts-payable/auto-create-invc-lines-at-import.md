---
title: Generieren Sie Rechnungszeilen, wenn Sie Kreditorenrechnungen importieren
description: In diesem Thema wird die Funktionalität zum automatischen Generieren von Rechnungszeilen auf Kreditorenrechnungen beschrieben, wenn Rechnungen importiert werden.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 87dec3c142ae296975ab98432421be4548085c80
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647889"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Generieren Sie Rechnungszeilen, wenn Sie Kreditorenrechnungen importieren

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Thema wird die Funktionalität zum automatischen Generieren von Rechnungszeilen auf Kreditorenrechnungen beschrieben, wenn Rechnungen importiert werden.

Manchmal enthalten Kreditorenrechnungen begrenzte Informationen, wie z. B. Empfängerinformationen und Zwischensummen. Sie enthalten jedoch keine Informationen zu Einzelposten. Wenn Sie Rechnungen importieren, kann das System basierend auf Informationen zur entsprechenden Bestellung automatisch Rechnungszeilen generieren.

Gehen Sie folgendermaßen vor, um die automatische Erstellung von Rechnungszeilen zu aktivieren.

1.  Wechseln Sie zu **Kreditoren \> Einstellung \> Kreditorenparameter**.
2.  Legen Sie auf der Registerkarte **Automatisierung der Kreditorenrechnung** unter **Automatische Zeilenerstellung für importierte Rechnungen** die Option **Rechnungsposten automatisch erstellen** auf **Ja** fest. 
4.  Wählen Sie im Feld  **Die Standardmenge für die automatische Erstellung von Rechnungszeilen auswählen** die Menge aus, die das System zum automatischen Generieren von Rechnungszeilen verwenden soll:

    - **Bestellte Menge** – Das System generiert Zeilen aus Bestellzeilen. Dieser Wert ist der Standardwert.
    - **Produkteingangsmenge** – Das System verwendet Bestellnummern, um die relevanten Produkteingänge zu finden. Es verwendet dann die Produkteingangsmengen, um Rechnungszeilen zu generieren.

## <a name="data-entity-changes"></a>Datenentitätsänderungen

Um die in diesem Thema beschriebene Funktionalität zu unterstützen, wurde die Datenentität **Kopf der Kreditorenrechnung** erweitert. Drei Felder wurden hinzugefügt:

- **HeaderOnlyImport** – Dieses Feld muss auf **Ja** gesetzt werden, damit das System Zeilen für Rechnungsköpfe generiert.
- **PurchIdRange** – Die Liste der Bestellnummern. Die Rechnungsnummern können ein Bereich sein, z. B. **INV0001..INV0009** (wobei Anfang und Ende des Bereichs durch zwei Punkte getrennt sind) oder diskrete Werte, wie **INV0001, INV0003, INV0006**. Alle Bestellungen müssen im Rechnungskopf zu demselben Kreditorenkonto gehören. Andernfalls erhalten Sie folgende Fehlermeldung: „Fehler beim Generieren von Rechnungsposten. Bestellungen haben unterschiedliche Lieferantenkonten.“
- **PackingslipRange** – Die Liste der Produktzugangsnummern. Kreditorenrechnungszeilen können aus Produkteingängen erstellt werden. Produkteingangsnummern sind jedoch normalerweise nicht auf Kreditorenrechnungen enthalten. Geben Sie die Produkteingangsnummern nur in dieses Feld ein, wenn Sie eindeutig erkennen können, welche Produkteingänge für welche Rechnungen gelten. Rechnungszeilen können auf Grundlage von Produkteingängen generiert werden. Und wenn dieses Feld verwendet wird, wird die Einstellung des Felds  **Standardmenge für die automatische Erstellung von Rechnungsposten auswählen** auf der Seite **Kreditorenparameter** ignoriert. 

**Einschränkung**: Wenn Sie mehrere Produkteingangsnummern eingeben, werden mehrere ausstehende Kreditorenrechnungen mit derselben Rechnungsnummer erstellt. Sie müssen diese manuell konsolidieren, bevor Sie die Rechnung weiterverarbeiten. In zukünftigen Versionen planen wir, dass das System die Rechnungen automatisch konsolidieren kann, sodass die Einschränkung aufgehoben wird.

Alle Produkteingänge müssen im Rechnungskopf zu demselben Kreditorenkonto gehören.

## <a name="result"></a>Ergebnis

Wenn das System erfolgreich Zeilen generiert, wird die folgende Meldung in der Historie der Kreditorenrechnungsautomatisierung protokolliert: „Rechnungszeilen automatisch erstellen: Erfolgreich.“

Wenn das System keine Zeilen generieren kann, wird die folgende Fehlermeldung protokolliert: „Rechnungszeilen automatisch erstellen: fehlgeschlagen.“
