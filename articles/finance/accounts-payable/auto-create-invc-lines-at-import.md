---
title: Generieren Sie Rechnungszeilen, wenn Sie Kreditorenrechnungen importieren
description: In diesem Artikel wird die Funktionalität zum automatischen Generieren von Rechnungszeilen auf Kreditorenrechnungen beschrieben, wenn Rechnungen importiert werden.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 5cb2c1234de03e9777921c18e4cbb81eec7feef9
ms.sourcegitcommit: 9c637bcf4e2eb8f711290a861492f038feaf1568
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9462273"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Generieren Sie Rechnungszeilen, wenn Sie Kreditorenrechnungen importieren

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Artikel wird die Funktionalität zum automatischen Generieren von Rechnungszeilen auf Kreditorenrechnungen beschrieben, wenn Rechnungen importiert werden.

Manchmal enthalten Kreditorenrechnungen begrenzte Informationen, wie z. B. Empfängerinformationen und Zwischensummen. Sie enthalten jedoch keine Informationen zu Einzelposten. Wenn Sie Rechnungen importieren, werden die Rechnungszeilen automatisch generiert, basierend auf den Informationen der entsprechenden Bestellung.

Gehen Sie folgendermaßen vor, um die automatische Erstellung von Rechnungszeilen zu aktivieren.

1.  Wechseln Sie zu **Kreditoren \> Einstellung \> Kreditorenparameter**.
2.  Legen Sie auf der Registerkarte **Automatisierung der Kreditorenrechnung** unter **Automatische Zeilenerstellung für importierte Rechnungen** die Option **Rechnungsposten automatisch erstellen** auf **Ja** fest. 
4.  Wählen Sie im Feld **Standardmenge für die automatische Erstellung von Rechnungszeilen wählen** die Menge, die für die automatische Erstellung von Rechnungszeilen verwendet werden soll:

    - **Bestellte Menge** - Die Zeilen werden aus den Zeilen der Bestellung generiert. Dieser Wert ist der Standardwert.
    - **Produkteingangsmenge** - Die Bestellnummer wird verwendet, um die entsprechenden Produktzugänge zu finden. Es verwendet dann die Produkteingangsmengen, um Rechnungszeilen zu generieren.

## <a name="data-entity-changes"></a>Datenentitätsänderungen

Um die in diesem Artikel beschriebene Funktionalität zu unterstützen, wurde die Datenentität **Kopf der Kreditorenrechnung** erweitert. Drei Felder wurden hinzugefügt:

- **HeaderOnlyImport** - Dieses Feld muss auf **Ja** festgelegt werden, um Zeilen für Rechnungsköpfe zu generieren.
- **PurchIdRange** – Die Liste der Bestellnummern. Die Rechnungsnummern können ein Bereich sein, z. B. **PO0001..PO0009** (wobei Anfang und Ende des Bereichs durch zwei Punkte getrennt sind) oder diskrete Werte, wie **PO0001, PO0003, PO0006**. Alle Bestellungen müssen im Rechnungskopf zu demselben Kreditorenkonto gehören. Andernfalls erhalten Sie folgende Fehlermeldung: „Fehler beim Generieren von Rechnungsposten. Bestellungen haben unterschiedliche Lieferantenkonten.“
- **PackingslipRange** – Die Liste der Produktzugangsnummern. Kreditorenrechnungszeilen können aus Produkteingängen erstellt werden. Produkteingangsnummern sind jedoch normalerweise nicht auf Kreditorenrechnungen enthalten. Geben Sie die Produkteingangsnummern nur in dieses Feld ein, wenn Sie eindeutig erkennen können, welche Produkteingänge für welche Rechnungen gelten. Rechnungszeilen können auf Grundlage von Produkteingängen generiert werden. Wenn dieses Feld verwendet wird, wird die Einstellung des Feldes **Wählen Sie die Standardmenge für die automatische Erstellung von Rechnungszeilen** auf der Seite **Parameter für Debitorenrechnungen** ignoriert. 

**Einschränkung**: Wenn Sie mehrere Produkteingangsnummern eingeben, werden mehrere ausstehende Kreditorenrechnungen mit derselben Rechnungsnummer erstellt. Sie müssen diese manuell konsolidieren, bevor Sie die Rechnung weiterverarbeiten. In zukünftigen Versionen planen wir, die Rechnungen automatisch zu konsolidieren, so dass diese Einschränkung aufgehoben wird.

Alle Produkteingänge müssen im Rechnungskopf zu demselben Kreditorenkonto gehören.

## <a name="result"></a>Ergebnis

Wenn Zeilen erfolgreich erstellt werden, wird die folgende Nachricht im Verlauf der Automatisierung der Lieferantenrechnung protokolliert: „Automatisch Rechnungszeilen erstellen: Erfolgreich.“

Wenn die Zeilen nicht erstellt werden, wird die folgende Fehlermeldung protokolliert: „Automatisch Rechnungszeilen erstellen: Fehlgeschlagen.“
