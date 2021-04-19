---
title: Erweiterter Formeleditor für elektronische Berichterstellung
description: In diesem Thema wird beschrieben, wie der erweiterte Formeleditor zum Konfigurieren von Ausdrücken in ER-Modellzuordnungen und Formatkomponenten verwendet werden kann.
author: NickSelin
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: d18aeedb2f21176ffe964b926168d4bf088a093b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751207"
---
# <a name="electronic-reporting-advanced-formula-editor"></a>Erweiterter Formeleditor für elektronische Berichterstellung

[!include [banner](../includes/banner.md)]

Neben dem [Elektronische Berichterstellung](general-electronic-reporting.md)-[Formeleditor](general-electronic-reporting-formula-designer.md) können Sie den erweiterten Formeleditor für elektronische Berichterstellung verwenden, um die Konfiguration von ER-Ausdrücken zu vereinfachen. Der erweiterte Editor ist browserbasiert und wird vom [Monaco-Editor](https://microsoft.github.io/monaco-editor) unterstützt. Die am häufigsten verwendeten erweiterten Editorfunktionen werden in diesem Thema beschrieben:

- [Automatische Codeformatierung](#Autoformatting)
- [IntelliSense](#IntelliSense)
- [Code-Abschluss](#CodeCompletion)
- [Code-Navigation](#CodeNavigation)
- [Code-Strukturierung](#CodeStructuring)
- [Suchen und ersetzen](#FindAndReplace)
- [Daten einfügen](#DataPasting)
- [Syntaxfärbung](#SyntaxColorization)

## <a name=""></a><a name="ActivateAdvEditor">Erweiterten Formeleditor aktivieren</a>

Führen Sie die folgenden Schritte aus, um den erweiterten Formeleditor in Ihrer Instanz von Microsoft Dynamics 365 Finance zu verwenden.

1.  Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2.  Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3.  Setzen Sie im Dialogfeld **Benutzerparameter** im Abschnitt **Ausführungsnachverfolgung** den Parameter **Erweiterten Formeleditor aktivieren** auf **Ja**.

[![ER-Konfigurationsseite](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)

> [!NOTE]
> Beachten Sie, dass dieser Parameter benutzerspezifisch und unternehmensspezifisch ist.

## <a name=""></a><a name="Autoformatting">Automatische Codeformatierung</a>

Wenn Sie einen komplexen Ausdruck schreiben, der aus mehreren Codezeilen besteht, erfolgt die Einrückung einer neuen eingegebenen Zeile automatisch anhand der Einrückung der vorherigen Zeile. Sie können Zeilen auswählen und deren Einrückung durch Eingabe von **TAB** oder **UMSCHALT + TAB** ändern.

[![ER-Formeleditor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)

Mit der automatischen Formatierung können Sie den gesamten Ausdruck gut formatieren, um die weitere Verwaltung sowie das Verständnis der konfigurierten Logik zu vereinfachen.

## <a name=""></a><a name="IntelliSense">IntelliSense</a>

Der Editor bietet eine Wortvervollständigung, um das Schreiben von Ausdrücken zu beschleunigen und Tippfehler zu vermeiden. Wenn Sie mit dem Hinzufügen von neuem Text beginnen, bietet der Editor automatisch eine Liste von Funktionen an, die von ER-Funktionen unterstützt werden, die die von Ihnen eingegebenen Zeichen enthalten. Sie können IntelliSense auch an einer beliebigen Stelle eines konfigurierten Ausdrucks durch Eingabe von **STRG + LEERZEICHEN** auslösen.

[![ER-Formeleditor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)

## <a name=""></a><a name="CodeCompletion">Code-Abschluss</a>

Der Editor unterstützt den Codeabschluss automatisch durch:

- Einfügen einer schließenden Klammer, wenn eine öffnende Klammer eingegeben wird, wobei der Cursor in den Klammern verbleibt.
- Einfügen des zweiten Anführungszeichens bei der Eingabe des ersten, wobei der Cursor innerhalb der Anführungszeichen bleibt.
- Einfügen des zweiten doppelten Anführungszeichens bei der Eingabe des ersten, wobei der Cursor innerhalb der Anführungszeichen bleibt.

[![ER-Formeleditor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)

Wenn Sie auf die eingegebene Klammer zeigen, wird die zweite Klammer dieses Paares automatisch markiert, um das von ihnen unterstützte Konstrukt anzuzeigen.

## <a name=""></a><a name="CodeNavigation">Code-Navigation</a>

Sie können die erforderlichen Symbole oder Zeilen finden, indem Sie den Befehl für **Gehe zu** über die Befehlspalette oder das Kontextmenü eingeben.

Beispiel: Gehen Sie wie folgt vor, um zur Zeile **8** zu springen:

- Drücken Sie **STRG+G**, geben Sie den Wert **8** ein, drücken Sie dann die **Eingabetaste**.

  – oder –

- Drücken Sie **F1**, geben Sie **G** ein, wählen Sie **Gehe zu Position** aus, geben Sie **8** ein und drücken Sie die **Eingabetaste**.

[![ER-Formeleditor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)

## <a name=""></a><a name="CodeStructuring">Code-Strukturierung</a>

Der Code für einige Funktionen, wie [IF](er-functions-logical-if.md) oder [CASE](er-functions-logical-case.md) wird automatisch strukturiert. Sie können einen oder alle Faltungsbereiche dieses Codes erweitern und reduzieren, um den bearbeitbaren Teil eines Ausdrucks zu verkleinern, damit Sie sich nur auf den Teil des Code konzentrieren können, der Ihrer Aufmerksamkeit bedarf. Hierfür können die Befehle zum Umschalten zwischen Falten und Auffalten verwendet werden.

Beispiel: Gehen Sie folgendermaßen, um alle Regionen zu falten:

- Drücken Sie **STRG+K**

  – oder –

- Drücken Sie **F1** und **FO**, wählen Sie **Alle falten** aus und drücken Sie die **Eingabetaste**

Gehen Sie folgendermaßen, um alle Regionen aufzufalten:

- Drücken Sie **STRG+J**

  – oder –
  
- Drücken Sie **F1** geben Sie **UN** ein, wählen Sie **Alle auffalten** aus und drücken Sie die **Eingabetaste**

[![ER-Formeleditor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)

## <a name=""></a><a name="FindAndReplace">Suchen und ersetzen</a>

Um einen bestimmten Text zu finden, wählen Sie den Text in Ihrem Ausdruck aus und gehen Sie wie folgt vor:

- Drücken Sie **STRG+F** und dann **F3**, um das nächste Vorkommen des ausgewählten Textes zu finden, oder drücken Sie **UMSCHALT+F3**, um das vorherige Vorkommen zu finden.

  – oder –
  
- Drücken Sie **F1**, geben Sie **F** ein und wählen Sie anschließend die erforderliche Option aus, um den ausgewählten Text zu suchen.

Um einen bestimmten Text zu ersetzen, wählen Sie den Text in Ihrem Ausdruck aus und gehen Sie wie folgt vor:

- Drücken Sie **STRG+H**. Geben Sie den alternativen Text ein und wählen Sie die Ersetzungsoption aus, um entweder den ausgewählten Text oder alle Vorkommen dieses Texts im aktuellen Ausdruck zu ersetzen.

  – oder –
  
- Drücken Sie **F1**, geben Sie **R** ein und wählen Sie anschließend die erforderliche Option aus, um den ausgewählten Text zu ersetzen. Geben Sie den alternativen Text ein und wählen Sie die Ersetzungsoption aus, um entweder den ausgewählten Text oder alle Vorkommen dieses Texts im aktuellen Ausdruck zu ersetzen.

Um alle Vorkommen eines bestimmten Texts zu ändern, wählen Sie den Text in Ihrem Ausdruck aus und gehen Sie wie folgt vor:

- Drücken Sie **STRG+F2** und geben Sie dann den alternativen Text ein.

  – oder –
  
- Drücken Sie **F1**, geben Sie **C** ein und wählen Sie anschließend die erforderliche Option aus, um den ausgewählten Text zu ändern. Geben Sie den alternativen Text ein.

[![ER-Formeleditor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)

## <a name=""></a><a name="DataPasting">Einfügen von Datenquellen und Funktionen</a>

Sie können **Datenquelle hinzufügen** auswählen, sodass beim aktuellen Ausdruck eine Datenquelle eingefügt wird, die derzeit im linken **Datenquelle**-Bereich auswählt ist. Sie können auch **Funktion hinzufügen** auswählen, sodass beim aktuellen Ausdruck eine Funktion eingefügt wird, die derzeit im rechten **Funktionen**-Bereich auswählt ist. Wenn Sie den ER-Formeleditor verwenden, wird eine ausgewählte Funktion oder ausgewählte Datenquelle immer an das Ende des konfigurierten Ausdrucks angefügt. Wenn Sie den erweiterten ER-Formeleditor verwenden, kann eine ausgewählte Funktion oder ausgewählte Datenquelle an einen beliebigen Teil des konfigurierten Ausdrucks angefügt werden. Sie müssen den Cursor verwenden, um anzugeben, wo Sie die Daten einfügen möchten.

[![ER-Formeleditor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)

## <a name=""></a><a name="SyntaxColorization">Syntaxfärbung</a>

Gegenwärtig werden verschiedene Farben verwendet, um die folgenden Teile von Ausdrücken hervorzuheben:

- Der Text in doppelten Klammern, der eine Beschriftungs-ID einer Textkonstante darstellen kann.

[![ER-Formeleditor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)

## <a name="limitations"></a>Einschränkungen

Der Editor wird derzeit in folgenden Webbrowsern unterstützt:

- Chrom
- Edge
- Firefox
- Opera
- Safari

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)
- [Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)
- [Monaco-Editor](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]