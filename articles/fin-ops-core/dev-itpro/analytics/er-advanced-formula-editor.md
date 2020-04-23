---
title: Erweiterter Formeleditor für elektronische Berichterstellung
description: In diesem Thema wird beschrieben, wie der erweiterte Formeleditor zum Konfigurieren von Ausdrücken in ER-Modellzuordnungen und Formatkomponenten verwendet werden kann.
author: NickSelin
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: d9911c858d6832aa70378d37e0fd5cf7d7831b1b
ms.sourcegitcommit: dce8c5d3b2fc4a752d676cf9ba91e0dea2fa80d8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/10/2020
ms.locfileid: "3257060"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="5d6d1-103">Erweiterter Formeleditor für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="5d6d1-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d6d1-104">Neben dem [Elektronische Berichterstellung](general-electronic-reporting.md)-[Formeleditor](general-electronic-reporting-formula-designer.md) können Sie den erweiterten Formeleditor für elektronische Berichterstellung verwenden, um die Konfiguration von ER-Ausdrücken zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="5d6d1-105">Der erweiterte Editor ist browserbasiert und wird vom [Monaco-Editor](https://microsoft.github.io/monaco-editor) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="5d6d1-106">Die am häufigsten verwendeten erweiterten Editorfunktionen werden in diesem Thema beschrieben:</span><span class="sxs-lookup"><span data-stu-id="5d6d1-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="5d6d1-107">Automatische Codeformatierung</span><span class="sxs-lookup"><span data-stu-id="5d6d1-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="5d6d1-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="5d6d1-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="5d6d1-109">Code-Abschluss</span><span class="sxs-lookup"><span data-stu-id="5d6d1-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="5d6d1-110">Code-Navigation</span><span class="sxs-lookup"><span data-stu-id="5d6d1-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="5d6d1-111">Code-Strukturierung</span><span class="sxs-lookup"><span data-stu-id="5d6d1-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="5d6d1-112">Suchen und ersetzen</span><span class="sxs-lookup"><span data-stu-id="5d6d1-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="5d6d1-113">Daten einfügen</span><span class="sxs-lookup"><span data-stu-id="5d6d1-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="5d6d1-114">Syntaxfärbung</span><span class="sxs-lookup"><span data-stu-id="5d6d1-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="5d6d1-115"><a name="ActivateAdvEditor">Erweiterten Formeleditor aktivieren</a></span><span class="sxs-lookup"><span data-stu-id="5d6d1-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="5d6d1-116">Führen Sie die folgenden Schritte aus, um den erweiterten Formeleditor in Ihrer Instanz von Microsoft Dynamics 365 Finance zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="5d6d1-117">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="5d6d1-118">Wählen Sie auf der Seite **Konfigurationen**  im Aktivitätsbereich auf der Registerkarte **Konfigurationen**  in der Gruppe **Erweiterte Einstellungen**   **Benutzerparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="5d6d1-119">Setzen Sie im Dialogfeld **Benutzerparameter** im Abschnitt für die **Ausführungsnachverfolgung** den Parameter für **Erweiterten Formeleditor aktivieren** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="5d6d1-120">[![ER-Konfigurationsseite](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="5d6d1-120">[![ER configurations page](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="5d6d1-121">Beachten Sie, dass dieser Parameter benutzerspezifisch und unternehmensspezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-121">Be aware that this parameter is user specific and company specific.</span></span>

## <a name=""></a><span data-ttu-id="5d6d1-122"><a name="Autoformatting">Automatische Codeformatierung</a></span><span class="sxs-lookup"><span data-stu-id="5d6d1-122"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="5d6d1-123">Wenn Sie einen komplexen Ausdruck schreiben, der aus mehreren Codezeilen besteht, erfolgt die Einrückung einer neuen eingegebenen Zeile automatisch anhand der Einrückung der vorherigen Zeile.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-123">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="5d6d1-124">Sie können Zeilen auswählen und deren Einrückung durch Eingabe von **TAB** oder **UMSCHALT + TAB** ändern.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-124">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="5d6d1-125">[![ER-Formeleditor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="5d6d1-125">[![ER formula editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="5d6d1-126">Mit der automatischen Formatierung können Sie den gesamten Ausdruck gut formatieren, um die weitere Verwaltung sowie das Verständnis der konfigurierten Logik zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-126">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="5d6d1-127"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="5d6d1-127"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="5d6d1-128">Der Editor bietet eine Wortvervollständigung, um das Schreiben von Ausdrücken zu beschleunigen und Tippfehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-128">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="5d6d1-129">Wenn Sie mit dem Hinzufügen von neuem Text beginnen, bietet der Editor automatisch eine Liste von Funktionen an, die von ER-Funktionen unterstützt werden, die die von Ihnen eingegebenen Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-129">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="5d6d1-130">Sie können IntelliSense auch an einer beliebigen Stelle eines konfigurierten Ausdrucks durch Eingabe von **STRG + LEERZEICHEN** auslösen.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-130">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="5d6d1-131">[![ER-Formeleditor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="5d6d1-131">[![ER formula editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="5d6d1-132"><a name="CodeCompletion">Code-Abschluss</a></span><span class="sxs-lookup"><span data-stu-id="5d6d1-132"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="5d6d1-133">Der Editor unterstützt den Codeabschluss automatisch durch:</span><span class="sxs-lookup"><span data-stu-id="5d6d1-133">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="5d6d1-134">Einfügen einer schließenden Klammer, wenn eine öffnende Klammer eingegeben wird, wobei der Cursor in den Klammern verbleibt.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-134">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="5d6d1-135">Einfügen des zweiten Anführungszeichens bei der Eingabe des ersten, wobei der Cursor innerhalb der Anführungszeichen bleibt.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-135">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="5d6d1-136">Einfügen des zweiten doppelten Anführungszeichens bei der Eingabe des ersten, wobei der Cursor innerhalb der Anführungszeichen bleibt.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-136">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="5d6d1-137">[![ER-Formeleditor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="5d6d1-137">[![ER formula editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="5d6d1-138">Wenn Sie auf die eingegebene Klammer zeigen, wird die zweite Klammer dieses Paares automatisch markiert, um das von ihnen unterstützte Konstrukt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-138">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="5d6d1-139"><a name="CodeNavigation">Code-Navigation</a></span><span class="sxs-lookup"><span data-stu-id="5d6d1-139"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="5d6d1-140">Sie können die erforderlichen Symbole oder Zeilen finden, indem Sie den Befehl für **Gehe zu** über die Befehlspalette oder das Kontextmenü eingeben.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-140">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="5d6d1-141">Beispiel: Gehen Sie wie folgt vor, um zur Zeile **8** zu springen:</span><span class="sxs-lookup"><span data-stu-id="5d6d1-141">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="5d6d1-142">Drücken Sie **STRG+G**, geben Sie den Wert **8** ein, drücken Sie dann die **Eingabetaste**.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-142">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="5d6d1-143">– oder –</span><span class="sxs-lookup"><span data-stu-id="5d6d1-143">-or-</span></span>

- <span data-ttu-id="5d6d1-144">Drücken Sie **F1**, geben Sie **G** ein, wählen Sie **Gehe zu Position** aus, geben Sie **8** ein und drücken Sie die **Eingabetaste**.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-144">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="5d6d1-145">[![ER-Formeleditor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="5d6d1-145">[![ER formula editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="5d6d1-146"><a name="CodeStructuring">Code-Strukturierung</a></span><span class="sxs-lookup"><span data-stu-id="5d6d1-146"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="5d6d1-147">Der Code für einige Funktionen, wie [IF](er-functions-logical-if.md) oder [CASE](er-functions-logical-case.md) wird automatisch strukturiert.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-147">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="5d6d1-148">Sie können einen oder alle Faltungsbereiche dieses Codes erweitern und reduzieren, um den bearbeitbaren Teil eines Ausdrucks zu verkleinern, damit Sie sich nur auf den Teil des Code konzentrieren können, der Ihrer Aufmerksamkeit bedarf.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-148">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="5d6d1-149">Hierfür können die Befehle zum Umschalten zwischen Falten und Auffalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-149">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="5d6d1-150">Beispiel: Gehen Sie folgendermaßen, um alle Regionen zu falten:</span><span class="sxs-lookup"><span data-stu-id="5d6d1-150">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="5d6d1-151">Drücken Sie **STRG+K**</span><span class="sxs-lookup"><span data-stu-id="5d6d1-151">Press **Ctrl+K**</span></span>

  <span data-ttu-id="5d6d1-152">– oder –</span><span class="sxs-lookup"><span data-stu-id="5d6d1-152">-or-</span></span>

- <span data-ttu-id="5d6d1-153">Drücken Sie **F1** und **FO**, wählen Sie **Alle falten** aus und drücken Sie die **Eingabetaste**</span><span class="sxs-lookup"><span data-stu-id="5d6d1-153">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="5d6d1-154">Gehen Sie folgendermaßen, um alle Regionen aufzufalten:</span><span class="sxs-lookup"><span data-stu-id="5d6d1-154">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="5d6d1-155">Drücken Sie **STRG+J**</span><span class="sxs-lookup"><span data-stu-id="5d6d1-155">Press **Ctrl+J**</span></span>

  <span data-ttu-id="5d6d1-156">– oder –</span><span class="sxs-lookup"><span data-stu-id="5d6d1-156">-or-</span></span>
  
- <span data-ttu-id="5d6d1-157">Drücken Sie **F1** geben Sie **UN** ein, wählen Sie **Alle auffalten** aus und drücken Sie die **Eingabetaste**</span><span class="sxs-lookup"><span data-stu-id="5d6d1-157">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="5d6d1-158">[![ER-Formeleditor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="5d6d1-158">[![ER formula editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="5d6d1-159"><a name="FindAndReplace">Suchen und ersetzen</a></span><span class="sxs-lookup"><span data-stu-id="5d6d1-159"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="5d6d1-160">Um einen bestimmten Text zu finden, wählen Sie den Text in Ihrem Ausdruck aus und gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="5d6d1-160">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="5d6d1-161">Drücken Sie **STRG+F** und dann **F3**, um das nächste Vorkommen des ausgewählten Textes zu finden, oder drücken Sie **UMSCHALT+F3**, um das vorherige Vorkommen zu finden.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-161">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="5d6d1-162">– oder –</span><span class="sxs-lookup"><span data-stu-id="5d6d1-162">-or-</span></span>
  
- <span data-ttu-id="5d6d1-163">Drücken Sie **F1**, geben Sie **F** ein und wählen Sie anschließend die erforderliche Option aus, um den ausgewählten Text zu suchen.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-163">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="5d6d1-164">Um einen bestimmten Text zu ersetzen, wählen Sie den Text in Ihrem Ausdruck aus und gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="5d6d1-164">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="5d6d1-165">Drücken Sie **STRG+H**.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-165">Press **Ctrl+H**.</span></span> <span data-ttu-id="5d6d1-166">Geben Sie den alternativen Text ein und wählen Sie die Ersetzungsoption aus, um entweder den ausgewählten Text oder alle Vorkommen dieses Texts im aktuellen Ausdruck zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-166">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="5d6d1-167">– oder –</span><span class="sxs-lookup"><span data-stu-id="5d6d1-167">-or-</span></span>
  
- <span data-ttu-id="5d6d1-168">Drücken Sie **F1**, geben Sie **R** ein und wählen Sie anschließend die erforderliche Option aus, um den ausgewählten Text zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-168">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="5d6d1-169">Geben Sie den alternativen Text ein und wählen Sie die Ersetzungsoption aus, um entweder den ausgewählten Text oder alle Vorkommen dieses Texts im aktuellen Ausdruck zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-169">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="5d6d1-170">Um alle Vorkommen eines bestimmten Texts zu ändern, wählen Sie den Text in Ihrem Ausdruck aus und gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="5d6d1-170">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="5d6d1-171">Drücken Sie **STRG+F2** und geben Sie dann den alternativen Text ein.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-171">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="5d6d1-172">– oder –</span><span class="sxs-lookup"><span data-stu-id="5d6d1-172">-or-</span></span>
  
- <span data-ttu-id="5d6d1-173">Drücken Sie **F1**, geben Sie **C** ein und wählen Sie anschließend die erforderliche Option aus, um den ausgewählten Text zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-173">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="5d6d1-174">Geben Sie den alternativen Text ein.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-174">Enter the alternative text.</span></span>

<span data-ttu-id="5d6d1-175">[![ER-Formeleditor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="5d6d1-175">[![ER formula editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="5d6d1-176"><a name="DataPasting">Einfügen von Datenquellen und Funktionen</a></span><span class="sxs-lookup"><span data-stu-id="5d6d1-176"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="5d6d1-177">Sie können **Datenquelle hinzufügen** auswählen, sodass beim aktuellen Ausdruck eine Datenquelle eingefügt wird, die derzeit im linken **Datenquelle**-Bereich auswählt ist.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-177">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="5d6d1-178">Sie können auch **Funktion hinzufügen** auswählen, sodass beim aktuellen Ausdruck eine Funktion eingefügt wird, die derzeit im rechten **Funktionen**-Bereich auswählt ist.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-178">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="5d6d1-179">Wenn Sie den ER-Formeleditor verwenden, wird eine ausgewählte Funktion oder ausgewählte Datenquelle immer an das Ende des konfigurierten Ausdrucks angefügt.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-179">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="5d6d1-180">Wenn Sie den erweiterten ER-Formeleditor verwenden, kann eine ausgewählte Funktion oder ausgewählte Datenquelle an einen beliebigen Teil des konfigurierten Ausdrucks angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-180">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="5d6d1-181">Sie müssen den Cursor verwenden, um anzugeben, wo Sie die Daten einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-181">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="5d6d1-182">[![ER-Formeleditor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="5d6d1-182">[![ER formula editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="5d6d1-183"><a name="SyntaxColorization">Syntaxfärbung</a></span><span class="sxs-lookup"><span data-stu-id="5d6d1-183"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="5d6d1-184">Gegenwärtig werden verschiedene Farben verwendet, um die folgenden Teile von Ausdrücken hervorzuheben:</span><span class="sxs-lookup"><span data-stu-id="5d6d1-184">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="5d6d1-185">Der Text in doppelten Klammern, der eine Beschriftungs-ID einer Textkonstante darstellen kann.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-185">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="5d6d1-186">[![ER-Formeleditor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="5d6d1-186">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="5d6d1-187">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="5d6d1-187">Limitations</span></span>

<span data-ttu-id="5d6d1-188">Der Editor wird derzeit in folgenden Webbrowsern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5d6d1-188">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="5d6d1-189">Chrom</span><span class="sxs-lookup"><span data-stu-id="5d6d1-189">Chrome</span></span>
- <span data-ttu-id="5d6d1-190">Edge</span><span class="sxs-lookup"><span data-stu-id="5d6d1-190">Edge</span></span>
- <span data-ttu-id="5d6d1-191">Firefox</span><span class="sxs-lookup"><span data-stu-id="5d6d1-191">Firefox</span></span>
- <span data-ttu-id="5d6d1-192">Opera</span><span class="sxs-lookup"><span data-stu-id="5d6d1-192">Opera</span></span>
- <span data-ttu-id="5d6d1-193">Safari</span><span class="sxs-lookup"><span data-stu-id="5d6d1-193">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d6d1-194">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5d6d1-194">Additional resources</span></span>

- [<span data-ttu-id="5d6d1-195">Überblick über die elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="5d6d1-195">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="5d6d1-196">Formeldesigner in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="5d6d1-196">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="5d6d1-197">Monaco-Editor</span><span class="sxs-lookup"><span data-stu-id="5d6d1-197">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)
