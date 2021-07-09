---
title: Vordefinierte Produktvarianten erstellen
description: Diese Prozedur führt Sie durch das Erstellen von Produktvarianten für einen Produktmaster mithilfe der Kombinationen von Produktdimensionen.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 442a5f5b321833c170cfecc4069e62a1254605cd
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270479"
---
# <a name="predefined-product-variants"></a>Vordefinierte Produktvarianten

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a>Beispielszenario: Erstellen von vordefinierten Produktvarianten

Dieses Beispielszenario zeigt, wie Sie Produktvarianten für einen Produktstamm mit einer Kombination von Produktdimensionen erstellen.

### <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Um dieses Szenario mit den hier vorgeschlagenen Werten nachzuvollziehen, müssen Sie Demodaten installiert haben und die juristische Entität *USMF* auswählen.

### <a name="step-1-create-a-product-master"></a>Schritt 1: Erzeugen eines Produktstamms

So erstellen Sie einen Produktstamm:

1. Wechseln Sie zu **Produktinformationsmanagement > Produkte > Produktstämme**.
1. Wählen Sie **Neu** aus.
1. Wenn das Feld **Produktnummer** nicht bereits eine Zahl anzeigt, geben Sie einen Wert ein. Dies ist nur erforderlich, wenn keine Sequenz für dieses Feld festgelegt wurde.
1. Geben Sie einen Namen in das Feld **Produktname** ein.
1. Wählen Sie im Feld **Produktdimensionsgruppe** die Produktdimensionsgruppe *SizeCol* (Größe und Farbe).
1. Wählen Sie **OK**, um den neuen Produktstamm zu erstellen und zu öffnen.

### <a name="step-2-add-product-dimensions"></a>Schritt 2: Produktdimensionen hinzufügen

Dieses Beispiel zeigt, wie Produktdimensionenen manuell eingegeben werden. Sie können auch eine Größen-, Farb- oder Stilgruppe auswählen, die die Werte für die Produktdimensionen enthält, die Sie verwenden möchten.

So fügen Sie Produktdimensionen hinzu:

1. Wenn Ihr neuer Produktstamm noch geöffnet ist, wählen Sie **Produktdimensionen** im Aktivitätsbereich.
1. Öffnen Sie die Registerkarte **Größe** und wählen Sie **Neu** in der Symbolleiste, um dem Raster eine Zeile hinzuzufügen. Legen Sie die folgenden Einstellungen für die neue Zeile fest:
    - **Größe:** Wählen Sie einen Größenwert.
    - **Name:** Geben Sie einen Namen für die Größe ein.
1. Wählen Sie **Neu** in der Symbolleiste und fügen Sie dem Raster eine zweite Größe mit einem neuen **Größe** und **Name** hinzu.
1. Öffnen Sie die Registerkarte **Farben** und wählen Sie **Neu** in der Werkzeugleiste, um dem Raster eine Zeile hinzuzufügen. Legen Sie die folgenden Einstellungen für die neue Zeile fest:
    - **Farbe:** Wählen Sie einen Farbwert.
    - **Name:** Geben Sie einen Namen für die Farbe ein.
1. Wählen Sie **Neu** in der Symbolleiste und fügen Sie dem Raster eine zweite Farbe mit einer neuen **Farbe** und **Name** hinzu.
1. Wählen Sie **Speichern** aus.
1. Schließen Sie die Seite, um zu Ihrem neuen Produktstamm zurückzukehren.

### <a name="step-3-generate-product-variants"></a>Schritt 3: Produktvarianten generieren

> [!NOTE]
> Dieser Abschnitt beschreibt, wie Produktvarianten generiert werden können, wenn die Funktion *Variantenvorschläge Seitenverbesserungen* nicht aktiviert ist. Im nächsten Abschnitt erfahren Sie, wie Sie Produktvarianten erzeugen, wenn diese Funktion verfügbar ist.

Um Produktvarianten zu generieren:

1. Wenn Ihr neuer Produktstamm noch geöffnet ist, wählen Sie **Produktvarianten** im Aktivitätsbereich.
1. Wählen Sie **Variantenvorschläge** im Aktivitätsbereich.
1. Das System generiert eine Liste mit allen möglichen Kombinationen der Größen und Farben, die Sie für das Produkt definiert haben. Wählen Sie **Alles auswählen** in der Symbolleiste.
    - Wählen Sie in diesem Beispiel alle möglichen Varianten aus. Wenn Sie nur eine Teilmenge der möglichen Kombinationen von Produktdimensionen verwenden möchten, aktivieren Sie bei Bedarf nur die erforderlichen Kontrollkästchen.  
1. Wählen Sie **Erstellen** aus.
1. Wählen Sie **Speichern** aus.

## <a name="improved-variant-suggestions"></a>Verbesserte Variantenvorschläge

Die Funktion *Verbesserungen auf der Seite für Variantenvorschläge* verbessert die Seite **Variant suggestions**, um Probleme mit der Leistung und der Benutzerfreundlichkeit für Firmen zu beheben, die eine hohe Anzahl von Produktdimensions-Kombinationen haben. Der verbesserte Prozess zur Auswahl der Werte für die Produktdimensionen, für die Variantenvorschläge generiert werden sollen, macht es schneller und einfacher, den relevanten Satz von Produktvarianten festzulegen und freizugeben.

Die folgenden Verbesserungen werden durch diese Funktion hinzugefügt:

- **Aufgeschobene Generierung von Variantenvorschlägen:** Die Seite **Variantenvorschläge** zeigt keine Vorschläge mehr an, wenn Sie sie zum ersten Mal öffnen. Stattdessen müssen Sie explizit auswählen, welche Werte Sie benötigen und dann die Schaltfläche **Vorschlagen** wählen, um die Kombinationen zu generieren. Dadurch wird der Prozess sichtbarer und interaktiver.
- **Auswahl von Dimensions-Werten:** Wenn Sie viele Dimensions-Werte haben, sind Sie typischerweise daran interessiert, Variantenvorschläge zu generieren, die nur einige von ihnen enthalten (z. B. bei der Einführung eines neuen Satzes von Farben oder Stilen). Mit dem verbesserten Design können Sie die Dimensionswerte auswählen, für die Sie Produktvariantenvorschläge generieren möchten. Dies erhöht die Relevanz der vorgeschlagenen Varianten erheblich und verbessert sowohl die Systemleistung als auch die Benutzerproduktivität.

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a>Schalten Sie die Funktion Variantenvorschläge Seitenverbesserungen ein

Bevor Sie die Funktion *Variantenvorschläge Seitenverbesserungen* verwenden können, muss sie in Ihrem System eingeschaltet sein. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** *Produktinformationsverwaltung*
- **Funktionsname:** *Variantenvorschläge Seite Verbesserungen*

### <a name="work-with-the-improved-variant-suggestions"></a>Arbeit mit den verbesserten Variantenvorschlägen

So generieren Sie Produktvariantenvorschläge, wenn die Funktion *Variantenvorschläge Seitenverbesserungen* aktiviert ist:

1. Öffnen oder erstellen Sie einen Produktstamm und fügen Sie ihm die erforderlichen Produktdimensionen hinzu, wie im vorherigen Abschnitt beschrieben.
1. Wählen Sie bei geöffnetem Produktstamm **Produktvarianten** im Aktivitätsbereich.
1. Wählen Sie **Variantenvorschläge** im Aktivitätsbereich.
1. Wählen Sie die Werte aus, die Sie für die einzelnen Dimensionen verwenden wollen.
1. Wählen Sie in der oberen Symbolleiste **Vorschlagen**.
1. Das System generiert eine Liste mit allen möglichen Kombinationen der von Ihnen gewählten Größen und Farben. Aktivieren Sie im Inforegister **Vorgeschlagene Varianten** das Kontrollkästchen für jede Produktdimensions-Kombination, die Sie verwenden möchten, oder wählen Sie **Alle auswählen** in der Symbolleiste, um alle auszuwählen.  
1. Wählen Sie **Erstellen**, um die Varianten zum aktuellen Produktstamm hinzuzufügen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
