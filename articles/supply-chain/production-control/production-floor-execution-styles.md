---
title: Produktionsausführungsoberfläche entwerfen
description: In diesem Artikel wird erläutert, wie Formularsteuerelemente so konfiguriert werden, dass die standardmäßigen Ausführungsstile der Produktionsumgebung auf sie angewendet werden.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: ad6ecd591353fe8ddc1a5b9049d65491fb58e98a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859139"
---
# <a name="style-the-production-floor-execution-interface"></a>Produktionsausführungsoberfläche entwerfen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Formularsteuerelemente so konfiguriert werden, dass die standardmäßigen Ausführungsstile der Produktionsumgebung auf sie angewendet werden.

## <a name="forms-and-dialogs"></a>Formulare und Dialoge

Stile können nur dann auf ein Formular oder Dialogfeld angewendet werden, wenn die folgenden Voraussetzungen erfüllt sind:

- Wenn das Formular dem bestehenden Berichtsfortschrittsformular ähneln soll, muss der Name Ihres Formulars oder Dialogs mit `JmgProductionFloorExecutionCustomInputDialog` beginnen.
- Das Formular oder Dialogfeld kann ein Detailformularteil enthalten. Um Stile darauf anzuwenden, muss der Name des Detailformularteils mit `JmgProductionFloorExecutionCustomDetailsDialog` beginnen.
- Soll das Formular oder der Dialog eine einfache Ansicht haben, dann muss der Name der einfachen Ansicht mit `JmgProductionFloorExecutionCustomDialog` beginnen. Beispiele für Formulare mit einfacher Ansicht sind das Startformular und das Formular für indirekte Aktivitäten.
- Alle Steuerelemente im Dialogfeld müssen wie in diesem Artikel beschrieben konfiguriert werden.

> [!IMPORTANT]
> Die in den ersten beiden Aufzählungspunkten dieser Liste genannten Funktionen erfordern Supply Chain Management Version 10.0.19 oder höher.

Stile können nur dann auf die Schaltfläche **OK** in einem Dialog angewendet werden, wenn die folgenden Voraussetzungen erfüllt sind:

- Die Schaltfläche ist in einer Formulargruppe enthalten.
- Der Gruppenname beginnt mit `OkButtonGroup`.

Stile können nur dann auf die Schaltfläche **Abbrechen** in einem Dialogfeld angewendet werden, wenn die folgenden Voraussetzungen erfüllt sind:

- Die Schaltfläche ist in einer Formulargruppe enthalten.
- Der Gruppenname beginnt mit `CancelButtonGroup`.

### <a name="header"></a>Übergeordnet

Die folgende Abbildung zeigt einen typischen Formular- oder Dialogkopf.

![Typische Formular- oder Dialogkopfzeile.](media/pfe-styles-header.png "Typische Formular- oder Dialogkopfzeile")

In Visual Studio werden Kopfzeilen mithilfe einer Struktur wie der in der folgenden Abbildung gezeigten erstellt.

![Typische Codestruktur zum Erstellen eines Headers.](media/pfe-styles-header-code-structure.png "Typische Codestruktur zum Erstellen eines Headers")

Verwenden Sie Code wie das folgende Beispiel, um Ihrer Kopfzeile Text hinzuzufügen.

```xpp
private void setCaption()
{
    HeaderFieldWithSeparatorText1.text("Report Progress");
    HeaderFieldWithSeparatorText2.text(ProdId);

    …

    HeaderFieldText.text(OprNum);
}
```

Wenden Sie beim Schreiben Ihres Headercodes die folgenden Regeln an:

- Der Name der Hauptgruppe muss `TableRowHeaderGroup` lauten.
- Jeder Textblock (durch Aufzählungszeichen getrennt) muss mit `HeaderFieldWithSeparatorText` beginnen.
- Der letzte Textname muss mit `HeaderFieldText` beginnen.
- `CaptionImage` kann übersprungen werden.

### <a name="progress-indicator"></a>Fortschrittsanzeige

Sie können eine Fortschrittsanzeige einfügen, die rechts neben der Kopfzeile angezeigt wird. Die folgende Abbildung zeigt eine Fortschrittsanzeige.

![Typische Fortschrittsanzeige.](media/pfe-styles-header-progress.png "Typische Fortschrittsanzeige")

Um die Fortschrittsanzeige anzuzeigen, muss das Textfeld `ShowProgress` benannt werden.

## <a name="grid"></a>Raster

Stile werden automatisch angewendet. Es ist keine spezielle Konfiguration erforderlich.

Das Raster sollte einen `TabularView`-Stil haben, und die `run()`-Methode im benutzerdefinierten Formular muss überschrieben werden, da ein neues Raster noch nicht unterstützt wird. Fügen Sie den folgenden Code hinzu.

```xpp
public void run()
{
    super();
    // To opt out a page from the new grid
    this.forceLegacyGrid();
}
```

Um Daten in einer Hauptansicht zu aktualisieren, möchten Sie vielleicht etwas wie `this.parmParentForm().updateLayout();` in einer `click`-Methode Ihrer Aktivität verwenden. (Ein Beispiel finden Sie in der `JmgProductionFloorExecutionReportFeedbackAction`-Klasse.) Stellen Sie nur sicher, dass `parmDataSource` in der `init`-Methode Ihres neuen Formulars (`formCaller.parmDataSource(this.dataSource(1));`) festgelegt ist. Sehen Sie sich als Beispiel das `JmgProductionFloorExecutionMainGrid`-Formular an.

## <a name="card-view"></a>Kartenansicht

Stile können nur dann auf Kartenanzeigesteuerungen angewendet werden, wenn die folgenden Voraussetzungen erfüllt sind:

- Jede Kartenansicht ist in einer Formulargruppe enthalten.
- Der Gruppenname beginnt mit `CardGroup` (z. B. `CardGroupJobsView`).

Die folgende Abbildung zeigt eine Kartenansicht, die keine Steuerelemente enthält.

![Kartenansicht ohne Elemente.](media/pfe-styles-empty-card.png)

Die folgenden Abbildungen zeigen Kartenansichten, die Steuerelemente enthalten.

![Karte mit Elementen, die Hz anzeigen.](media/pfe-styles-elements.png)

![Karte mit Elementen für eine Wartungsanfrage.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Visitenkarte

Stile können nur dann auf Visitenkarten angewendet werden, wenn die folgenden Voraussetzungen erfüllt sind:

- Jede Visitenkarte ist in einer Formulargruppe enthalten.
- Der Gruppenname beginnt mit `BusinessCardGroup` (z. B. `BusinessCardGroupJobsList`).

Legen Sie die folgenden Eigenschaften auf der Visitenkarte fest:

- **Stil:** *list*
- **Erweiterter Stil:** *cardList*
- **Mehrfachauswahl:** *Nein*
- **Spaltenetiketten anzeigen:** *Nein*

![Visitenkarte.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Optionsschaltfläche

Stile können nur dann auf Optionsfelder angewendet werden, wenn die folgenden Voraussetzungen erfüllt sind:

- Jedes Optionsfeld ist in einer Formulargruppe enthalten.
- Der Gruppenname beginnt mit `RadioTextBelow` oder `RadioTextRight`, je nachdem, wo der Text erscheinen soll.

Legen Sie die folgenden Eigenschaften auf die Optionsfelder fest:

- **Umschaltfläche:** *Überprüfen*
- **Umschaltwert:** *Ein*, wenn das Optionsfeld ausgewählt werden soll; andernfalls *Aus*

Die folgende Abbildung zeigt ein Beispiel, bei dem der Text unter den Optionsfeldern angezeigt wird.

![Optionsfelder mit Text darunter.](media/pfe-styles-radio-text-below.png)

Die folgende Abbildung zeigt ein Beispiel, bei dem der Text rechts neben den Optionsfeldern angezeigt wird.

![Optionsfelder mit Text rechts.](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a>Optionsfelder in Internet Explorer

Optionsfeldstile werden nicht unterstützt in Internet Explorer. Die folgende Abbildung zeigt, wie Optionsfelder aussehen in Internet Explorer.

![Optionsfelder in Internet Explorer.](media/pfe-styles-browser.png)

## <a name="buttons"></a>Knöpfe

Stile können nur dann auf Schaltflächen angewendet werden, wenn die folgenden Voraussetzungen erfüllt sind:

- Jede Schaltflächengruppe ist in einer Formulargruppe enthalten. Alle Schaltflächen in der Gruppe haben den gleichen Stil.
- Es gibt keine Anforderungen an den Namen der Gruppe.

Legen Sie die folgenden Eigenschaften auf die Schaltflächen fest:

- **Tastenanzeige:** *TextWithImageLeft*
- **Normales Bild:** Diese Eigenschaft darf nicht leer sein. Verwenden Sie für dieses Beispiel *CoffeeScript*.
- **Text:** Diese Eigenschaft darf nicht leer sein. Verwenden Sie für dieses Beispiel *Start Break*.
- **Breite:** *Auto* oder *SizeToContent*
- **Höhe:** *Auto* oder *SizeToContent*

### <a name="primary-button"></a>Primäre Schaltfläche

Stile können nur dann auf eine primäre Schaltfläche angewendet werden, wenn die folgenden Voraussetzungen erfüllt sind:

- Die Schaltfläche ist in einer Formulargruppe enthalten.
- Der Gruppenname beginnt mit `DefaultButtonGroup` oder `PrimaryButtonGroup` (z. B. `DefaultButtonGroup10`).

![Primäre Schaltfläche.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Sekundäre Schaltfläche

Stile können nur dann auf eine sekundäre Schaltfläche angewendet werden, wenn die folgenden Voraussetzungen erfüllt sind:

- Die Schaltfläche ist in einer Formulargruppe enthalten.
- Die Gruppe heißt **Rechter Bereich**, oder der Gruppenname beginnt mit `SecondaryButtonGroup`.

![Sekundäre Schaltfläche.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Schaltfläche für die dritte Gruppe

Stile können nur dann auf eine Drittgruppenschaltfläche angewendet werden, wenn die folgenden Voraussetzungen erfüllt sind:

- Die Schaltfläche ist in einer Formulargruppe enthalten.
- Die Gruppe heißt **Linker Bereich**, oder der Gruppenname beginnt mit `ThirdButtonGroup`.

![Schaltfläche für die dritte Gruppe.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Schaltfläche für die vierte Gruppe

Stile können nur dann auf eine Viertgruppenschaltfläche angewendet werden, wenn die folgenden Voraussetzungen erfüllt sind:

- Die Schaltfläche ist in einer Formulargruppe enthalten.
- Der Gruppenname beginnt mit `FourthButtonGroup`.

Legen Sie die folgenden Eigenschaften auf die Schaltfläche fest:

- **Tastenanzeige:** *TextOnly*
- **Normales Bild:** Diese Eigenschaft muss leer sein.
- **Text:** Diese Eigenschaft darf nicht leer sein. Verwenden Sie zum Beispiel *Anzeigen* oder *Bearbeiten*.
- **Breite:** *Auto*
- **Höhe:** *Auto*

![Schaltfläche für die vierte Gruppe.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Schaltfläche Flach

Stile können nur dann auf eine flache Schaltfläche angewendet werden, wenn die folgenden Voraussetzungen erfüllt sind:

- Die Schaltfläche ist in einer Formulargruppe enthalten.
- Der Gruppenname beginnt mit `FlatButtonGroup`.

Legen Sie die folgenden Eigenschaften auf die Schaltfläche fest:

- **Tastenanzeige:** *ImageOnly*
- **Normales Bild:** Diese Eigenschaft darf nicht leer sein. Verwenden Sie für dieses Beispiel *CoffeeScript*.
- **Text:** Diese Eigenschaft muss leer sein.
- **Breite:** *Auto* oder *SizeToContent*
- **Höhe:** *Auto* oder *SizeToContent*

![Schaltfläche Flach.](media/pfe-styles-flat-button.png)

### <a name="continue-button"></a>Weiter-Schaltfläche

Stile können nur dann auf eine Weiter-Schaltfläche angewendet werden, wenn die folgenden Voraussetzungen erfüllt sind:

- Die Schaltfläche ist in einer Formulargruppe enthalten.
- Der Gruppenname beginnt mit `ContinueButtonGroup`.

Legen Sie die folgenden Eigenschaften auf die Schaltfläche fest:

- **Tastenanzeige:** *ImageOnly*
- **Normales Bild:** *Vorwärts*
- **Text:** Diese Eigenschaft muss leer sein.
- **Breite:** *Auto* oder *SizeToContent*
- **Höhe:** *Auto* oder *SizeToContent*

![Weiter-Schaltfläche.](media/pfe-styles-continue-button.png)

## <a name="combo-box"></a>Eingabe-Listenfeld

Ein Kombinationsfeld ist eine Kombination aus drei Steuerelementen: einem Eingabesteuerelement, einer Schaltfläche zum Löschen des Eingabesteuerelements und einer Schaltfläche zum Ausführen einer Suche.

Stile können nur dann auf ein Kombinationsfeld angewendet werden, wenn die folgenden Voraussetzungen erfüllt sind:

- Das Kombinationsfeld ist in einer Formulargruppe enthalten.
- Der Gruppenname beginnt mit `Combobox`.
- Innerhalb der Gruppe ist das erste Steuerelement ein `AxFormStringControl`-Steuerelement. Dieses Steuerelement zeigt den aktuellen Wert an, und hier gibt der Benutzer den erforderlichen Wert ein.
- Das zweite Steuerelement ist ein `CommonButton`-Steuerelement, und sein Name beginnt mit `ClearButton`. Diese Schaltfläche muss Code enthalten, der die `enable`-Eigenschaft verwendet, um die Schaltfläche anzuzeigen oder auszublenden. Zum Ein- oder Ausblenden der **Löschen**-Schaltfläche während der Benutzer Informationen in das Eingabesteuerelement eingibt, können Sie den folgenden Code verwenden.

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    Sie sollten eine Methode haben, bei der die Daten im Eingabesteuerelement festgelegt werden. Aktivieren Sie die **Löschen**-Schaltfläche in dieser Methode. Hier ist ein Beispiel.

    ```xpp
    public void setSerialId(str _serialId)
    {
        JmgTmpJobBundleProdFeedback.InventSerial = _serialId;
        ClearButtonSerial.enabled(_serialId? true : false);

        if (_serialId)
        {
            this.addSerialNumber();
        }
    }
    ```

    Verwenden Sie den folgenden Code für die `clicked`-Methode der **Löschen**-Schaltfläche.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Stellen Sie den Wert des Eingangsreglers, `AxFormStringControl`, ein, wenn das Formular mit der `init`-Methode initialisiert wird. Wenn der Wert nicht leer ist, aktivieren Sie die **Löschen**-Schaltfläche. Wenn der Wert leer ist, deaktivieren Sie die **Löschen**-Schaltfläche.

- Das dritte Steuerelement ist ein `CommonButton`-Steuerelement, und sein Name beginnt mit `SearchButton`.

Die folgende Abbildung zeigt zwei Kombinationsfeld-Steuerelemente. Das Kombinationsfeld auf der linken Seite enthält ein leeres Textfeld, und die **Löschen**-Schaltfläche ist deaktiviert. Das Kombinationsfeld auf der rechten Seite enthält Text im Textfeld, und die **Löschen**-Schaltfläche ist aktiviert.

![Kombinationsfelder mit und ohne Löschen-Schaltfläche.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Schnellfilter

Das Schnellfilter-Steuerelement fügt der Seite ein Suchfeld hinzu. Sie können Stile auf einen Schnellfilter anwenden, sofern die folgenden Voraussetzungen erfüllt sind:

- Der Schnellfilter ist in einer Formulargruppe enthalten.
- Der Gruppenname beginnt mit `SearchInputGroup`.
- Innerhalb der Gruppe ist das erste Steuerelement ein `QuickFilter`-Steuerelement. (In diesem Steuerelement gibt der Benutzer die Suchzeichenfolge ein.)
- Das zweite Steuerelement ist ein `FormStaticTextControl`, das `NumberOfResults` heißt. (Dieses Steuerelement ist optional. Es zeigt die Anzahl der gefundenen Artikel an, falls enthalten.)
- Das dritte Steuerelement ist ein `CommonButton`-Steuerelement, und sein Name beginnt mit `ClearButton`.

Die folgende Abbildung zeigt zwei Schnellfilter-Steuerelemente. Der Schnellfilter auf der linken Seite hat einen leeren Schnellfilter und die Anzahl der Ergebnisse ist nicht sichtbar. Der Schnellfilter auf der rechten Seite enthält einen Suchstring und zeigt die Anzahl der Ergebnisse an.

![Beispiele für ein schnelles Filtersteuerelement mit und ohne Suchzeichenfolge.](media/pfe-styles-quick-filter.png "Beispiele für ein schnelles Filtersteuerelement mit und ohne Suchzeichenfolge")

## <a name="center-align-elements-on-a-tab"></a>Elemente auf einer Registerkarte zentrieren

Um Elemente in der Mitte einer Registerkarte auszurichten, muss der Gruppenname mit `TabContentGroup` beginnen, und die Gruppe muss die folgenden Eigenschaften aufweisen:

- **Breitenmodus:** `SizeToAvailable`
- **Höhenmodus:** `SizeToAvailable`

## <a name="align-a-grid-detail-part-and-quick-filter"></a>Raster, Detailteils und Schnellfilter ausrichten

Um ein benutzerdefiniertes Raster, einen Detailteil und einen Schnellfilter so anzuordnen, dass sie dem Standarddesign ähneln, beachten Sie beim Zusammensetzen die folgenden Punkte:

- Wenn das Raster über einen Schnellfilter verfügt, sollten sich sowohl das Raster als auch der Schnellfilter in der Gruppe befinden, deren Name mit `GridGroup` beginnt.
- Um Stile auf einen Detailteil anzuwenden, muss der Gruppenname mit `DetailInformationGroup` beginnen.

Die folgende Abbildung zeigt ein typisches Raster mit einem Schnellfilter und einem Detailteil auf der rechten Seite.

![Typisches Raster, das einen Schnellfilter und Detailteil enthält.](media/pfe-styles-align-grid.png "Typisches Raster, das einen Schnellfilter und Detailteil enthält")

In Visual Studio kann ein Raster, Detailteil und Schnellfilter mithilfe einer Struktur wie der in der folgenden Abbildung gezeigten erstellt werden.

![Typische Codestruktur, die ein Raster, einen Detailteil und Schnellfilter ausrichtet.](media/pfe-styles-header-code-structure2.png "Typische Codestruktur, die ein Raster, einen Detailteil und Schnellfilter ausrichtet")

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Produktionsausführungsoberfläche anpassen](production-floor-execution-customize.md)
- [Produktionsausführungsoberfläche entwerfen](production-floor-execution-tabs.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
