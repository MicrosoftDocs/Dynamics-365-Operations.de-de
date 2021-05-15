---
title: Verwalten von Maßeinheiten
description: Dieses Thema beschreibt, wie Sie eine Maßeinheit definieren, Übersetzungen für die Einheit und ihre Beschreibung bereitstellen und Umrechnungsregeln für verwandte Einheiten definieren.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921340"
---
# <a name="manage-units-of-measure"></a>Verwalten von Maßeinheiten

[!include [banner](../../includes/banner.md)]

Dieses Thema beschreibt, wie Sie eine Maßeinheit definieren, Übersetzungen für die Einheit und ihre Beschreibung bereitstellen und Umrechnungsregeln für verwandte Einheiten definieren.

## <a name="open-the-units-page"></a>Öffnen Sie die Seite Einheiten

Um die Maßeinheiten zu erstellen und mit ihnen zu arbeiten, die in Ihrem System verfügbar sind, gehen Sie zu **Organisationsverwaltung \> Einrichten \> Einheiten \> Einheiten**.

Die restlichen Abschnitte dieses Themas beschreiben, was Sie auf der Seite **Einheiten** tun können.

## <a name="create-standard-units-and-conversions"></a>Erstellen Sie Standardeinheiten und Umrechnungen

Wenn Ihr System nicht bereits die am häufigsten verwendeten Maßeinheiten für das metrische System und/oder das US Customary System (USCS) enthält, kann der Assistent zum Einrichten von Einheiten Ihnen helfen, schnell mit den grundlegenden Definitionen und Umrechnungen von Maßeinheiten zu beginnen. Um den Assistenten abzuschließen, wählen Sie **Assistent zur Erstellung von Einheiten** im Aktivitätsbereich und folgen dann den Anweisungen auf dem Bildschirm.

## <a name="create-or-edit-a-unit-of-measure"></a>Erstellen oder bearbeiten Sie eine Maßeinheit

Um eine Maßeinheit zu erstellen oder zu bearbeiten, gehen Sie folgendermaßen vor.

1. Führen Sie einen dieser Schritte aus:

    - Um eine vorhandene Einheit zu bearbeiten, wählen Sie sie im Listenbereich aus.
    - Um eine neue Einheit zu erstellen, wählen Sie **Neu** im Aktivitätsbereich.

1. Legen Sie in der Kopfzeile des Datensatzes die folgenden Felder fest:

    - **Einheit** – Geben Sie die ID oder das Symbol ein, das verwendet werden soll, um auf die Einheit in der Systemsprache zu verweisen. Diese ID oder dieses Symbol ist normalerweise eine allgemeine Abkürzung für die Einheit, z. B. *ea* für jedes oder *cm* für Zentimeter.
    - **Beschreibung** – Geben Sie einen beschreibenden Namen für die Einheit in der Systemsprache ein. Dieser Name ist normalerweise der vollständige Name der Einheit, z. B. *Einheit* oder *Zentimeter*.

1. Legen Sie im Inforegister **Allgemein** die folgenden Felder fest:<!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - **Einheitsklasse** – Wählen Sie die Eigenschaft, die die Einheit misst (z. B. Länge, Fläche, Masse oder Menge).
    - **System der Einheiten** – Wählen Sie das Messsystem, zu dem die Einheit gehört (*Metrische Einheiten* oder *Gewöhnliche Einheiten der Vereinigten Staaten*).
    - **Basiseinheit** – Legen Sie diese Option auf *Ja* fest, um die aktuelle Einheit als Basiseinheit für ihre Einheitenklasse zu verwenden. In diesem Fall müssen Sie nur den Umrechnungsfaktor zwischen der Basiseinheit und jeder zusätzlichen Einheit in der Einheitenklasse angeben. Das System kann dann zwischen allen Einheiten in dieser Einheitenklasse umrechnen. Daher ist es einfacher, Konvertierungen festzulegen.

        Wenn z.B. Gallone die Basiseinheit für die Einheitenklasse *Volumen* ist, müssen Sie nur Umrechnungsfaktoren von Quart zu Gallone und von Pint zu Gallone festlegen. Das System kann dann auch von quart in pint umrechnen.

        Sie können nur eine Basiseinheit pro Einheitenklasse haben.

    - **Systemeinheit** – Legen Sie diese Option auf *Ja* fest, um die aktuelle Einheit als angenommene Einheit für alle nicht spezifizierten Messungen in ihrer Einheitenklasse zu verwenden. Wenn z. B. ein Feld, das zur Eingabe einer Menge verwendet wird, die Angabe einer Einheit nicht zulässt (oder wenn der Benutzer keine Einheit auswählt), verwendet das System die Einheit, die als Systemeinheit für die Einheitenklasse *Menge* festgelegt ist. Sie können nur eine Systemeinheit pro Einheitenklasse haben.
    - **Dezimalpräzision** – Geben Sie die Anzahl der Dezimalstellen an, auf die Werte, die für die aktuelle Einheit angegeben oder in diese umgerechnet werden, gerundet werden sollen.

1. Wählen Sie im Aktionsbereich **Speichern** aus.

## <a name="define-unit-translations"></a>Einheitenübersetzungen definieren

Um Übersetzungen für die ID oder das Symbol und die Beschreibung für eine Maßeinheit zu definieren, gehen Sie wie folgt vor.

1. Erstellen oder wählen Sie die Einheit, für die Sie Übersetzungen erstellen möchten.
1. Wählen Sie im Aktivitätsbereich **Einheiten-Texte**.

    Die Seite **Einheitentexte** erscheint. Sie verwenden diese Seite, um Übersetzungen für die ID oder das Symbol für die gewählte Einheit zu definieren. Diese Übersetzungen können dann auf externen Dokumenten in kunden- oder kreditorenspezifischen Sprachen verwendet werden.

1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie im Feld **Sprache** die Sprache aus, in die die ID oder das Symbol der Einheit übersetzt werden soll.
1. Geben Sie im Feld **Text** die Übersetzung der ID oder des Symbols der Einheit in der gewählten Sprache ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Schließen Sie die Seite.
1. Wählen Sie auf der Seite **Aktivitätsbereich** die Option **Übersetzte Einheitenbeschreibungen**.

    Die Seite **Übersetzte Einheitenbeschreibungen** erscheint. Sie verwenden diese Seite, um sprachspezifische Beschreibungen für die ausgewählte Einheit zu definieren.

1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie im Feld **Sprache** die Sprache, in die die Beschreibung der Einheit übersetzt werden soll.
1. Geben Sie im Feld **Beschreibung** die Übersetzung der Beschreibung der Einheit in der gewählten Sprache ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Schließen Sie die Seite.

## <a name="define-unit-conversion-rules"></a>Definieren Sie Einheitenumrechnungsregeln

Um Regeln für Umrechnungen zwischen Maßeinheiten zu definieren, folgen Sie diesen Schritten.

1. Erstellen oder wählen Sie die Einheit, für die Sie Umrechnungsregeln definieren wollen.
1. Wählen Sie im Aktivitätsbereich **Einheiten-Umwandlungen**.

    Die Seite **Einheiten-Umrechnungen** erscheint. Sie verwenden diese Seite, um Regeln für die Konvertierung der ausgewählten Einheit in und aus anderen Einheiten der Einheitenklasse zu definieren.

1. Wählen Sie eine der folgenden Registerkarten, je nach Art der Konvertierung, die Sie festlegen wollen:

    - **Standard-Konvertierungen** – Legen Sie Standard-Konvertierungsregeln für alle Produkte fest.
    - **Klassenübergreifende Konvertierungen** – Legen Sie produktspezifische Konvertierungsregeln für Einheiten in derselben Einheitsklasse fest.
    - **Klassenübergreifende Umrechnungen** – Legen Sie produktspezifische Umrechnungsregeln für Einheiten über Einheitenklassen hinweg fest.

1. Führen Sie einen dieser Schritte aus:

    - Um eine neue Konvertierung zu erstellen, wählen Sie **Neu** in der Symbolleiste.
    - Um eine vorhandene Konvertierung zu bearbeiten, wählen Sie die Konvertierung im Raster aus und wählen dann **Bearbeiten** in der Symbolleiste.

1. Legen Sie in der erscheinenden Dropdown-Dialogbox die folgenden Felder fest:

    - **Produkt** – Wählen Sie das spezifische Produkt, für das die Konvertierung gilt. Dieses Feld ist nur für klasseninterne und klassenübergreifende Konvertierungen verfügbar.
    - **Formelauslegung** – Lassen Sie dieses Feld auf *Einfach* festgelegt, um eine einfache Umrechnung mit einem einzigen Faktor anzugeben. Legen Sie es auf *Erweitert* fest, um eine komplexere Gleichung einzurichten. Das Format für erweiterte Gleichungen variiert je nach Einheitenklasse.
    - **Aus Einheit** – In diesem Feld wird die gewählte Einheit angezeigt. Normalerweise sollten Sie den Wert nicht ändern. (Wenn Sie den Wert ändern, müssen Sie die Seite **Einheiten-Umrechnungen** für die gewählte Einheit öffnen, um Ihre neue Umrechnung nach dem Speichern zu sehen.)
    - **Zur Einheit** – Wählen Sie die Einheit, in die umgerechnet werden soll.
    - **Rundung** – Wählen Sie, wie Brüche gerundet werden sollen, basierend auf dem **Dezimalpräzisionswert** der ausgewählten Einheit (*Zum nächsten*, *Aufwärts* oder *Abwärts*).
    - **Umrechnungsformel** – Geben Sie in den übrigen Feldern oben im Dropdown-Dialogfeld die Formel für die Umrechnung zwischen den beiden Einheiten an. Die verfügbaren Felder variieren, abhängig von der gewählten Einheitsklasse und dem Formel-Layout.

1. Wählen Sie **OK**.
1. Schließen Sie die Seite.

> [!TIP]
> Sie können auch Einheiten-Umrechnungen pro Produktvariante festlegen. Weitere Informationen finden Sie unter [Umrechnung von Maßeinheiten pro Produktvariante](../uom-conversion-per-product-variant.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
