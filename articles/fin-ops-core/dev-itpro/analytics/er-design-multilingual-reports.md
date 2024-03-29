---
title: Entwerfen Sie mehrsprachige Berichte in der elektronischen Berichterstellung
description: In diesem Artikel wird erläutert, wie Sie mithilfe von Electronic Reporting (ER) mehrsprachige Berichte entwerfen und erstellen können.
author: kfend
ms.date: 05/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 5575ba3154521e3855ce6b97c5b37d3c4868e3e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285484"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>Entwerfen Sie mehrsprachige Berichte in der elektronischen Berichterstellung

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Übersicht

Als geschäftlicher Benutzer verwenden Sie [Electronic Reporting (ER)](general-electronic-reporting.md) zum Konfigurieren von Formaten für ausgehende Dokumente in Übereinstimmung mit den rechtlichen Anforderungen verschiedener Länder/Regionen. Wenn diese Anforderungen erfordern, dass ausgehende Dokumente in verschiedenen Sprachen für verschiedene Länder oder Regionen generiert werden, können Sie ein einzelnes ER konfigurieren Format das sprachabhängige Ressourcen enthält. Auf diese Weise können Sie das Format wiederverwenden, um ausgehende Dokumente für verschiedene Länder oder Regionen zu generieren. Möglicherweise möchten Sie auch ein einziges ER-Format verwenden, um ein ausgehendes Dokument in verschiedenen Sprachen für entsprechende Kunden, Lieferanten, Tochterunternehmen oder andere Parteien zu generieren.

Sie können ER-Datenmodelle und Modellzuordnungen als Datenquellen für konfigurierte ER-Formate konfigurieren, um den Datenfluss zu definieren, der angibt, welche Anwendungsdaten in generierten Dokumenten gespeichert werden. Als EB-Konfigurations-[Anbieter](general-electronic-reporting.md#Provider) können Sie konfigurierte Datenmodelle und Modellzuordnungen sowie Formate als Komponenten einer EB-Lösung zur Generierung spezifischer ausgehender Dokumente [veröffentlichen](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs). Sie können Kunden auch erlauben, [die](general-electronic-reporting-manage-configuration-lifecycle.md), um die veröffentlichte ER-Lösung hochzuladen, damit sie verwendet und angepasst werden kann. Wenn Sie erwarten, dass Kunden andere Sprachen sprechen, können Sie die ER-Komponenten so konfigurieren, dass sie sprachabhängige Ressourcen enthalten. Auf diese Weise kann der Inhalt einer bearbeitbaren ER-Komponente zur Entwurfszeit in der vom Kunden bevorzugten Sprache des Kunden dargestellt werden.

Sie können sprachabhängige Ressourcen als ER-Labels konfigurieren. Sie können diese Beschriftungen dann verwenden, um ER-Komponenten für die folgenden Zwecke zu konfigurieren:

- Zur Entwurfszeit:

    - Präsentieren Sie den Inhalt der konfigurierten ER-Komponenten in der vom Benutzer bevorzugten Sprache.

- Zu Laufzeit:

    - Generieren Sie sprachabhängige Inhalte für ausgehende Dokumente.
    - Geben Sie Warn- und Fehlermeldungen in der vom Benutzer bevorzugten Sprache an.
    - Eingabeaufforderung für erforderliche Felder in der vom Benutzer bevorzugten Sprache.

ER-Beschriftungens können in jeder ER [Konfiguration](general-electronic-reporting.md#Configuration) konfiguriert werden, die verschiedene Komponenten enthält. Die Beschriftungen können unabhängig von der konfigurierten Logik von ER-Datenmodellen, ER-Modellzuordnungen und ER-Formatkomponenten verwaltet werden.

Jede ER-Beschriftung wird durch eine ID identifiziert, die im Umfang der ER-Konfiguration, die dieses Etikett enthält, eindeutig ist. Jede Beschriftung kann Beschriftungstext für jede Sprache enthalten, die in der aktuellen Instanz von Microsoft Dynamics 365 Finance unterstützt wird. Diese unterstützten Sprachen umfassen die Sprachen der bereitgestellten Anpassungen.

## <a name="entry"></a>Erfassung

Wenn Sie ein ER-Datenmodell, eine ER-Modellzuordnung oder ein ER-Format entwerfen, wird die Option **Übersetzen** angezeigt, wenn Sie ein Feld auswählen, das möglicherweise den übersetzbaren Kontext enthält. Wenn Sie diese Option auswählen, können Sie das ausgewählte Feld mit einer ER-Beschriftung im **Textübersetzung** <a name="TextTranslationPane">Bereich</a> auswählen. Sie können eine vorhandene ER-Beschriftung auswählen oder ein neue ER-Beschriftung hinzufügen, falls es noch nicht verfügbar ist. Wenn Sie eine ER-Beschriftung auswählen oder hinzufügen, können Sie verwandten Text für jede Sprache hinzufügen, die in der aktuellen Finanzinstanz unterstützt wird.

Die folgende Abbildung zeigt, wie diese Übersetzung in einem bearbeitbaren ER-Datenmodell durchgeführt wird. In diesem Beispiel ist die **Beschreibung** Attribut des Felds **Bestellung** für das bearbeitbare **Rechnungsmodell** in die Sprachen Deutsch für Österreich (DE-AT) und Japanisch (JA) übersetzt.

![Bereitstellung der Übersetzung eines EB-Etiketts im EB-Datenmodelldesigner.](./media/er-multilingual-labels-refer.png)

Es kann nur Beschriftungstext für Beschriftungen übersetzt werden, die sich in einer bearbeitbaren ER-Komponente befinden. Zum Beispiel, wenn Sie **Übersetzen** auswählen für das Beschriftungs-Attribut einer ER-Modellzuordnungsdatenquelle und dann eine ER-Beschriftung auswählen, das sich im übergeordneten ER-Datenmodell befindet, wird der Inhalt der Beschriftung angezeigt, Sie können diese aber nicht ändern. In diesen Fällen ist das Feld **Übersetzter Text** nicht verfügbar, wie in der folgenden Abbildung gezeigt.

![Überprüfung der bereitgestellten Übersetzung eines EB-Modellzuordnungsdesigners.](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> Sie können die Designer nicht zum Löschen von Beschriftungen verwenden, die in eine bearbeitbare ER-Komponente eingegeben wurden.

## <a name="scope"></a>Bereich

ER-Beschriftungen können in mehreren übersetzbaren Attributen von ER-Komponenten verwendet werden.

### <a name="data-model-component"></a>Datenmodellkomponente

Wenn Sie ein ER-Datenmodell konfigurieren, können Sie ER-Beschriftungen hinzufügen. Die Attribute **Beschriftung** und **Beschreibung** des Modellelements, jedes Modellfeld und jeder <a id="LinkModelEnum"></a>Modellaufzählungswert kann mit einer ER-Beschriftung verknüpft werden, das dem ER-Datenmodell hinzugefügt wird.

![Bereitstellung der Übersetzung für die Attributbeschreibung im EB-Datenmodelldesigner.](./media/er-multilingual-labels-refer.png)

Wenn ein ER-Datenmodell auf diese Weise konfiguriert wird, wird sein Inhalt den Benutzern des ER-Datenmodelldesigners in der von jedem Benutzer bevorzugten Sprache angezeigt. Daher wird die Modellwartung vereinfacht. Die folgenden Abbildungen zeigen, wie diese Funktionalität für Benutzer funktioniert, für die DE-AT und JA als bevorzugte Sprache festgelegt sind.

![Layout des EB-Datenmodelldesigners für einen Benutzer, für den DE-AT als bevorzugte Sprache festgelegt wurde.](./media/er-multilingual-labels-refer-de.png)

![Layout des EB-Datenmodelldesigners für einen Benutzer, für den JA als bevorzugte Sprache festgelegt wurde.](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>Modellzuordnungskomponente

Da die ER-Modellzuordnung auf einem ER-Datenmodell basiert, werden die Beschriftungen der Datenmodellelemente, auf die verwiesen wird, in der vom Benutzer bevorzugten Sprache im Modellzuordnungsdesigner angezeigt. Die folgende Abbildung zeigt, wie die Bedeutung des Felds **Bestellung** in der bearbeitbaren Modellzuordnung anhand der Bezeichnung des Attributs **Beschreibung** erläutert wird, das dem konfigurierten Datenmodell hinzugefügt wurde. Beachten Sie, dass diese Beschriftung in der vom Benutzer bevorzugten Sprache angezeigt wird (in diesem Beispiel DE-AT).

![Layout des EB-Modellzuordnungsdesigners für einen Benutzer, für den DE-AT als bevorzugte Sprache festgelegt wurde.](./media/er-multilingual-labels-show-mapping.png)

Wenn das Attribut **Beschriftung** der **Benutzereingabeparameter** Datenquelle so konfiguriert ist, dass sie mit einer ER-Beschriftung verknüpft ist, wird das Parameterfeld für diese Datenquelle den Benutzern zur Laufzeit im Benutzerdialogfeld in ihrer bevorzugten Sprache angezeigt.

### <a name="format-component"></a>Formatkomponente

Wenn Sie ein ER-Format konfigurieren, können Sie ER-Beschriftungen hinzufügen. Die Attribute **Beschriftung** und **Hilfstext** jeder konfigurierten Datenquelle können mit einer ER-Beschriftung verknüpfen, die dem ER-Format hinzugefügt wird. Die Attribute **Beschriftung** und **Beschreibung** von jedem <a id="LinkFormatEnum"></a>Formataufzälungswert kann auch mit einer ER-Beschriftung verknüpft werden, auf die vom bearbeitbaren ER-Format aus zugegriffen werden kann.

> [!NOTE]
> Sie können diese Attribute auch mit einer ER-Beschriftung des übergeordneten ER-Datenmodells verknüpfen, das die Beschriftung des Modells in jedem für dieses ER-Datenmodell konfigurierten ER-Format wiederverwendet.

Wenn ein ER-Format auf diese Weise konfiguriert wird, wird sein Inhalt den Benutzern des ER-Datenmodelldesigners in der von jedem Benutzer bevorzugten Sprache angezeigt. Daher werden die Formatwartung und die Analyse der konfigurierten Logik vereinfacht.

Da ein ER-Format auf einem ER-Datenmodell basiert, werden die Beschriftungen der Datenmodellelemente, auf die verwiesen wird, in der vom Benutzer bevorzugten Sprache im Modellzuordnungsdesigner angezeigt.

Wenn das Attribut **Beschriftung** der **Benutzereingabeparameter** Datenquelle so konfiguriert ist, dass sie mit einer ER-Beschriftung verknüpft ist, wird das Parameterfeld für diese Datenquelle den Benutzern zur Laufzeit im Benutzerdialogfeld in ihrer bevorzugten Sprache angezeigt. Die folgenden Abbildungen zeigen, wie Sie das Attribut **Beschriftung** der **Benutzereingabeparameter** Datenquelle zur Entwurfszeit für eine ER-Beschriftung verknüpfen, sodass Benutzer zur Laufzeit zur Eingabe des Parameters in verschiedenen vom Benutzer bevorzugten Sprachen (angezeigt für Englisch in den USA (EN-US) und DE-AT) aufgefordert werden.

![Bereitstellung der Übersetzung von Attributen eines Benutzereingabeparameters im EB Operation Designer.](./media/er-multilingual-labels-refer-format.png)

![Zahlungsabwicklung des EB-Anbieters zur Laufzeit für die vom Benutzer bevorzugte Sprache EN-US.](./media/er-multilingual-labels-show-runtime-en.png)

![Zahlungsabwicklung des EB-Anbieters zur Laufzeit für die vom Benutzer bevorzugte Sprache DE-AT.](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>Ausdrücke

Um eine Beschriftung in einem ER [Ausdruck](er-formula-language.md) zu verwenden, müssen Sie die Syntax verwenden **@„\_LABEL: X“**, wobei das Präfix **@** angibt an, dass der Operand auf eine Bezeichnung verweist, **GER\_ETIKETTE** zeigt an, dass ein ER-Etikett beteiligt ist, und **X** ist die ER-Label-ID.

![Konfigurieren eines EB-Ausdrucks, der einen Verweis auf eine EB-Beschriftung im EB-Formel-Designer enthält.](./media/er-multilingual-labels-expression1.png)

Verwenden Sie die Syntax, um auf eine Systembezeichnung (Anwendung) zu verweisen **@„“**, wo das Präfix **@** angibt, dass der Operand auf eine Bezeichnung verweist, und **X** die Systembezeichnungs-ID ist.

![Konfigurieren eines EB-Ausdrucks, der einen Verweis auf eine Anwendungsbeschriftung im EB-Formular-Designer enthält.](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>Modellzuordnung

Ein Ausdruck einer EB-Modellzuordnung kann mithilfe einer Beschriftung konfiguriert werden. Wenn diese Zuordnung von einem EB-Format aufgerufen wird, das zum Generieren eines ausgehenden Dokuments ausgeführt wird, enthält der Kontext der Ausführung einen Sprachcode. Eine konfigurierte Ausdrucksbezeichnung wird mit dem Beschriftungstext ausgefüllt, der für die Sprache dieses Kontexts konfiguriert wurde.

Wenn eine Beschriftung, auf die verwiesen wird, keine Übersetzung für die Sprache des Formatausführungskontexts enthält, der die Modellzuordnung aufruft, wird stattdessen ein Beschriftungstext in der Sprache EN-US verwendet.

#### <a name="format"></a>Formate

Ein Ausdruck eines EB-Formats kann mithilfe einer Beschriftung konfiguriert werden. Wenn diese Zuordnung von einem EB-Format aufgerufen wird, das zum Generieren eines ausgehenden Dokuments ausgeführt wird, enthält der Kontext der Ausführung einen Sprachcode. Eine konfigurierte Ausdrucksbezeichnung wird mit dem Beschriftungstext ausgefüllt, der für die Sprache dieses Kontexts konfiguriert wurde.

![Bereitstellung der Übersetzung einer EB-Beschriftungs des bearbeitbaren EB-Ausdrucks im EB-Formel-Designer.](./media/er-multilingual-labels-refer-in-expression.png)

![Beispiel für eine Datenbindung, die sich auf eine EB-Beschriftung im EB Operation Designer bezieht.](./media/er-multilingual-labels-refer-in-binding.png)

Sie können die **DATEI** Komponente eines EF-Formats zum Generieren des Berichts in der vom Benutzer bevorzugten Sprache konfigurieren.

![Richten Sie die DATEI-Komponente im EB Vorgangs-Designer ein, um den Bericht in der vom Benutzer bevorzugten Sprache zu generieren.](./media/er-multilingual-labels-language-context-user.png)

Wenn Sie ein EB-Format auf diese Weise konfigurieren, wird der Bericht unter Verwendung des entsprechenden Textes der EB-Beschriftungen erstellt. Die folgenden Abbildungen zeigen Beispiele für Berichte für die Benutzersprachen EN-US und DE-AT.

![Vorschau des Berichts, der in der bevorzugten Sprache des EN-US-Benutzers erstellt wurde.](./media/er-multilingual-labels-report-preview-en.png)

![Vorschau des Berichts, der in der bevorzugten Sprache des DE-AT-Benutzers erstellt wurde.](./media/er-multilingual-labels-report-preview-de.png)

Wenn eine Beschriftung, auf die verwiesen wird, keine Übersetzung für die Sprache des Formatausführungskontexts enthält, der eine Modellzuordnung aufruft, wird stattdessen ein Beschriftungstext in der Sprache EN-US verwendet.

> [!TIP]
> Sie können die **ORDNER**-Komponente sowie verschiedene Arten von **DATEI**-Komponenten im bearbeitbaren EB-Format verwenden, um anzugeben, wie eine ausgehende Datei generiert wird. Um eine generierte Datei zu benennen, konfigurieren Sie den ER-[Ausdruck](er-formula-language.md) für den Parameter **Dateiname** der Komponente. Sie können Bezeichnungen im konfigurierten Ausdruck verwenden. Da der Parameter **Dateiname** standardmäßig sprachunabhängig ist, wird der Text aller Beschriftungen, auf die Sie sich in diesem Ausdruck beziehen, zur Laufzeit in der Standardsprache EN-US angezeigt. Ab Version 10.0.28 können Sie jedoch die Funktion **Parameter „Sprachpräferenz“ auf den Ausdruck „Dateiname“ anwenden** aktivieren. Der Ausdruck **Dateiname** berücksichtigt dann den Parameter **Sprachpräferenzen**, wenn er berechnet wird.

## <a name="language"></a>Sprache

EB unterstützt verschiedene Möglichkeiten, eine Sprache für einen generierten Bericht anzugeben. In dem Feld **Spracheinstellungen** in der Registerkarte **Format** können Sie die folgenden Werte auswählen:

- **Firmenpräferenz** – Erstellen Sie einen Bericht in einer vom Unternehmen angegebenen Sprache.

    ![Geben Sie im EB Operation Designer eine vom Unternehmen bevorzugte Sprache als Sprache für einen generierten Bericht an.](./media/er-multilingual-labels-language-context-company.png)

- **Benutzerpräferenz** – Erstellen Sie einen Bericht in der vom Benutzer bevorzugten Sprache.
- **Explizit definiert** – Generieren Sie einen Bericht in einer Sprache, die zur Entwurfszeit angegeben wurde.

    ![Geben Sie im EB Operations Designer eine Entwurfszeit in der vom Unternehmen bevorzugte Sprache als Sprache für einen generierten Bericht an.](./media/er-multilingual-labels-language-context-fixed.png)

- **Definiert zu Runtime** – Generieren Sie einen Bericht in einer Sprache, die zur Runtime angegeben wurde. Wenn Sie diesen Wert auswählen, konfigurieren Sie einen EB-Ausdruck im Feld **Sprache**, der den Sprachcode für die Sprache zurückgibt, z. B. die Sprache des entsprechenden Kunden.

    ![Geben Sie im EB Operation Designer eine Runtime definierte Sprache als Sprache für einen generierten Bericht an.](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="culture-specific-formatting"></a>Kulturspezifische Formatierung

ER unterstützt verschiedene Möglichkeiten, die Kultur für einen generierten Bericht anzugeben. Daher kann die richtige kulturspezifische Formatierung für Datum, Uhrzeit und numerische Werte verwendet werden. Wenn Sie ein ER-Format entwerfen, können Sie auf der Registerkarte **Format** im Feld **Kultureinstellungen** für jede Formatkomponente vom Typ **Gemeinsam\\Datei**, **Excel\\Datei**, **PDF\\Datei** oder **PDF\\Zusammenführung** einen der folgenden Werte auswählen:

- **Benutzerpräferenz** – Formatieren Sie die Werte entsprechend der bevorzugten Kultur des Benutzers. Diese Kultur wird im Feld **Datum, Uhrzeit und Zahlenformat** auf der Registerkarte **Einstellungen** der Seite **Benutzeroptionen** definiert.

    ![Festlegen der bevorzugten Kultur des Benutzers als Kultur eines generierten Berichts im EB Operation Designer.](./media/er-multilingual-labels-culture-context-user-preferred.png)

- **Explizit definiert** – Formatieren Sie die Werte entsprechend der Kultur, die zur Entwurfszeit angegeben ist.

    ![Definieren der Kultur, die zur Entwurfszeit als Kultur eines generierten Reports im EB Operation Designer festgelegt wird.](./media/er-multilingual-labels-culture-context-fixed.png)

- **Zur Laufzeit definiert** – Formatieren Sie die Werte entsprechend der Kultur, die zur Laufzeit angegeben wird. Wenn Sie diesen Wert wählen, konfigurieren Sie auf der Registerkarte **Zuordnung** im Feld **Datums-, Zeit- und Zahlenformat** einen ER-Ausdruck, der den Kulturcode für die Kultur liefert, z. B. die Kultur des entsprechenden Debitors.

    ![Definieren der Kultur, die zur Laufzeit als Kultur eines generierten Reports im EB Operation Designer festgelegt wird.](./media/er-multilingual-labels-culture-context-runtime.png)

> [!NOTE]
> Eine ER-Komponente, für die Sie eine bestimmte Kultur definieren, kann untergeordnete ER-Komponenten enthalten, die so konfiguriert wurden, dass sie einen Textwert ausfüllen. Standardmäßig wird die Kultur der übergeordneten Komponente verwendet, um die Werte dieser Komponenten zu formatieren. Sie können die folgenden integrierten ER-Funktionen verwenden, um Bindungen für diese Komponenten zu konfigurieren und eine alternative Kultur für die Werteformatierung anzuwenden:
>
> - [DATEFORMAT](er-functions-datetime-dateformat.md#syntax-2)
> - [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md#syntax-2)
> - [NUMBERFORMAT](er-functions-text-numberformat.md#syntax-2)
>
> Ab Version 10.0.20 wird das Gebietsschema von Formatkomponenten der Typen **Allgemein\\Datei** und **Excel\\Datei** zur Formatierung von Werten während der [PDF-Konvertierung](electronic-reporting-destinations.md#OutputConversionToPDF) eines generierten Dokuments verwendet.

## <a name="translation"></a>Übersetzung

Sie können einer bearbeitbaren EB-Komponente die erforderlichen EB-Beschriftungen hinzufügen. Wenn eine EB-Beschriftung hinzugefügt wird, kann sie auf zwei Arten übersetzt werden: manuell und automatisch.

### <a name="manual-translation"></a>Manuelle Übersetzung

Wenn Sie eine EB-Beschriftung im **Textübersetzung** [Bereich](#TextTranslationPane) hinzufügen, können Sie sie manuell in alle Sprachen übersetzen, die in der aktuellen Instanz von Finance unterstützt werden. Sie können die bevorzugte Sprache im Feld **Sprache** in der **Systemsprache** auswählen oder im Abschnitt **Benutzersprache** den entsprechenden Text in den entsprechenden Abschnitt im Feld **Übersetzter Text** eingeben und dann **Übersetzen** auswählen. Dieser Vorgang muss für jede erforderliche Sprache und jede von Ihnen hinzugefügte Beschriftung wiederholt werden.

### <a name="automatic-translation"></a>Automatische Übersetzung

Die Konfiguration einer EB-Komponente erfolgt in der Entwurfsversion der EB-Konfiguration, in der sich die bearbeitbare EB-Komponente befindet.

![Die Seite EB-Konfigurationen mit Zugriff auf die Konfigurationsversion im Entwurfsstatus.](./media/er-multilingual-labels-configurations.png)

Wie weiter oben in diesem Artikel beschrieben, können Sie einer bearbeitbaren EB-Komponente die erforderlichen EB-Beschriftungen hinzufügen. Auf diese Weise können Sie den Text der EB-Beschriftung in der Sprache EN-US angeben. Anschließend können Sie die Beschriftungen der EB-Komponente mithilfe der integrierten EB-Funktion exportieren. Wählen Sie die Entwurfsversion einer EB-Konfiguration aus, die die bearbeitbare EB-Komponente enthält, und wählen Sie dann **Austausch \> Beschrichtung exportieren**.

![Auf der Seite EB-Konfigurationen können Sie EB-Beschriftungen aus der ausgewählten Konfigurationsversion exportieren.](./media/er-multilingual-labels-export.png)

Sie können entweder alle Beschriftungen oder die Beschriftungen für eine einzelne Sprache exportieren, die Sie zu Beginn des Exports angegeben haben. Beschriftungen werden als Zip-Datei exportiert, die XML-Dateien enthält. Jede XML-Datei enthält Beschriftungen für eine einzelne Sprache.

![Beispiel der exportierten Datei mit EB-Beschriftungen die Sprache DE-AT.](./media/er-multilingual-labels-in-xml.png)

Dieses Format wird für die automatische Übersetzung von Beschriftungen durch externe Übersetzungsdienste wie [Dynamics 365 Translation service](../lifecycle-services/translation-service-overview.md) verwendet. Wenn Sie die übersetzten Beschriftungen erhalten, können Sie sie wieder in die Entwurfsversion einer EB-Konfiguration importieren, die die EB-Komponenten enthält, denen diese Beschriftung gehören. Wählen Sie die Entwurfsversion einer EB-Konfiguration aus, die die bearbeitbare EB-Komponente enthält, und wählen Sie dann **Austausch \> Beschriftung laden**.

![Auf der Seite EB-Konfigurationen können Sie EB-Beschriftungen aus der ausgewählten Konfigurationsversion importieren.](./media/er-multilingual-labels-load.png)

Übersetzte Beschriftungen werden in die ausgewählte EB-Konfiguration importiert. Übersetzte Beschriftungen, die in dieser EB-Konfiguration vorhanden sind, werden ersetzt. Wenn eine übersetzte Beschriftung in der EB-Konfiguration fehlt, wird sie angehängt.

## <a name="lifecycle"></a>Lebenszyklus

Beschriftungen einer EB-Komponente, die bearbeitet werden können, werden zusammen mit anderen Inhalten für die Komponente in der entsprechenden Version einer EB-Konfiguration gespeichert.

Auf Beschriftungen einer EB-Basiskomponente kann in einer abgeleiteten Version der EB-Komponente verwiesen werden, die Sie erstellen, um Ihre Änderungen einzuführen.

> [!TIP]
> Wenn Sie eine ER-Lösung entwerfen, können Sie Ihre eigene ER-[Datenmodell](er-overview-components.md#data-model-component)-Komponente von der bereitgestellten ableiten. In diesem abgeleiteten Datenmodell können Sie Ihre eigenen ER-Beschriftungen einführen und sie in allen ER-Formaten verwenden, die das Datenmodell als Datenquelle verwenden. Sie können dann Ihre eigene ER-[Format](er-overview-components.md#format-component)-Komponente von derjenigen ableiten, die bereitgestellt wird, indem Sie Ihr abgeleitetes ER-Datenmodell anstelle des bereitgestellten auswählen. Ab Version 10.0.28 können Sie die Funktion **Erweiterter Zugriff auf Beschriftungen des aufsteigenden ER-Datenmodells** aktivieren, um auf Beschriftungen eines aufsteigenden ER-Datenmodells in abgeleiteten ER-Formatkomponenten zuzugreifen, auch wenn das ER-Datenmodell, das Sie für die abgeleitete ER-Komponente ausgewählt haben, sich von dem in der Basis-ER-Komponente verwendeten Modell unterscheidet.
>
> Wenn derselbe Beschriftungsname in Ihrer abgeleiteten Komponente und ihren aufsteigenden Komponenten verwendet wird, wird Ihre Übersetzung dieser Beschriftung als die relevanteste verwendet.

Die EB-Versionierung steuert die Zuordnung der Beschriftung zu einem beliebigen Attribut in einer EB-Komponente. Änderungen an der Beschriftungszuordnung werden in der Liste der Änderungen (Delta) einer bearbeitbaren EB-Komponente aufgezeichnet, die als abgeleitete Version der bereitgestellten EB-Komponente erstellt wurde. Diese Änderungen werden überprüft, wenn eine abgeleitete Version auf eine neue Basisversion zurückgesetzt wird.

## <a name="functions"></a>Funktionen

Dies eingebaute [LISTOFFIELDS](er-functions-list-listoffields.md) EB-Funktion kann auf EB-Beschriftungen zugreifen, die für einige Elemente von EB-Komponenten konfiguriert wurden.

Wie weiter oben in diesem Artikel beschrieben, können die Attribute **Beschriftung** und **Beschreibung** von jedem [Modell](#LinkModelEnum) oder [Format](#LinkFormatEnum) des EB-Enumerationswerts mit einer EB-Beschriftung verlinkt werden, auf die die entsprechende EB-Komponente Zugriff hat. Sie können einen EB-Ausdruck konfigurieren, in dem Sie die Funktion **LISTOFFIELDS** mithilfe der EB-Enumeration als Argument aufrufen. Dieser Ausdruck gibt eine Liste zurück, die einen Datensatz für jeden Wert einer EB-Enumeration enthält, die als Argument dieser Funktion definiert wurde. Jeder Datensatz enthält den Wert einer EB-Beschriftung, der mit einem EB-Enumerationswert verknüpft ist:

- Der Wert einer EB-Beschriftung ist mit den Attributten der **Beschriftung** verknüpft, die im Feld **Beschriftung** des zurückgegebenen Datensatzes gespeichert sind.
- Der Wert einer EB-Beschriftung ist mit den Attributten der **Beschreibung** verknüpft, die im Feld **Beschreibung** des zurückgegebenen Datensatzes gespeichert sind.

## <a name="performance"></a><a name=performance></a>Leistung

Wenn Sie eine ER-Formatkomponente konfigurieren, um einen Bericht in Ihrer bevorzugten [Sprache](#language) zu generieren oder um ein eingehendes Dokument zu importieren, dessen Inhalt auf die von Ihnen bevorzugte Sprache hin analysiert wird, empfehlen wir, dass Sie die Funktion **Bevorzugte Sprache des aktuellen Benutzers für ER-Ausführungen zwischenspeichern** im Arbeitsbereich [Funktionsverwaltung](../../fin-ops/get-started/feature-management/feature-management-overview.md) aktivieren. Diese Funktion trägt zur Verbesserung der Leistung bei, insbesondere für ER-Formatkomponenten, die mehrere Verweise auf Beschriftungen in ER-Formeln und -Bindungen enthalten sowie zahlreiche [Validierungsregeln](general-electronic-reporting-formula-designer.md#TestFormula) zum Generieren von Benutzernachrichten in Ihrer bevorzugten Sprache.

Wenn Sie den Status einer ER-Konfigurationsversion von **Entwurf** auf **Fertig** ändern, werden diese Labels in der Anwendungsdatenbank gespeichert, wenn die Konfigurationsversion ER-Labels enthält. Das Speicherschema hängt vom Status der Funktion **Beschleunigen der Speicherung von ER Labels** ab:

- Wenn die Funktion nicht aktiviert ist, werden alle Labels im Feld **LABELXML** der Tabelle **ERSOLUTIONVERSIONTABLE** als ein einziges XML-Snippet gespeichert.
- Wenn die Funktion aktiviert ist, wird für jede Sprache ein eigener Datensatz in der Tabelle **ERSOLUTIONVERSIONLABELSTABLE** erstellt. Das Feld **CONTENTS** dieser Tabelle speichert Labels pro Sprache als komprimiertes XML-Snippet.

Wir empfehlen Ihnen, die Funktion **Beschleunigung der Speicherung von ER-Labels** im Arbeitsbereich **Funktionsverwaltung** zu aktivieren. Diese Funktion trägt dazu bei, die Auslastung der Netzwerkbandbreite und die Gesamtleistung des Systems zu verbessern, da in den meisten Fällen ER-Etiketten in einer einzigen Sprache verwendet werden, wenn Sie mit einer einzigen ER-Konfiguration arbeiten.

Um das ausgewählte Speicherschema für die Aufbewahrung der Beschriftungen aller ER-Konfigurationen in der aktuellen Finance-Instanz anzuwenden, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Organisationsverwaltung** > **Periodisch** > **Das ausgewählte Schema zum Speichern von Labels für alle ER-Konfigurationen anwenden**.
2. Wählen Sie **OK** aus.


## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)
- [Elektronische Berichterstellungsfunktion erweitern](er-formula-language.md#Functions)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
