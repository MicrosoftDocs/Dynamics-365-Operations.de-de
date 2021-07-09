---
title: Erweiterter Formeleditor für elektronische Berichterstellung
description: In diesem Thema wird beschrieben, wie der erweiterte Formeleditor zum Konfigurieren von Ausdrücken in ER-Modellzuordnungen und Formatkomponenten verwendet werden kann.
author: NickSelin
ms.date: 06/17/2021
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
ms.openlocfilehash: f7f80928e1d3f5d4892f72d4bd2fd09b70a26c1f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270706"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="c33f8-103">Erweiterter Formeleditor für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="c33f8-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c33f8-104">Neben dem [Elektronische Berichterstellung](general-electronic-reporting.md)-[Formeleditor](general-electronic-reporting-formula-designer.md) können Sie den erweiterten Formeleditor für elektronische Berichterstellung verwenden, um die Konfiguration von ER-Ausdrücken zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="c33f8-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="c33f8-105">Der erweiterte Editor ist browserbasiert und wird vom [Monaco-Editor](https://microsoft.github.io/monaco-editor) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c33f8-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="c33f8-106">Die am häufigsten verwendeten erweiterten Editorfunktionen werden in diesem Thema beschrieben:</span><span class="sxs-lookup"><span data-stu-id="c33f8-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="c33f8-107">Automatische Codeformatierung</span><span class="sxs-lookup"><span data-stu-id="c33f8-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="c33f8-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="c33f8-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="c33f8-109">Code-Abschluss</span><span class="sxs-lookup"><span data-stu-id="c33f8-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="c33f8-110">Code-Navigation</span><span class="sxs-lookup"><span data-stu-id="c33f8-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="c33f8-111">Code-Strukturierung</span><span class="sxs-lookup"><span data-stu-id="c33f8-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="c33f8-112">Suchen und ersetzen</span><span class="sxs-lookup"><span data-stu-id="c33f8-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="c33f8-113">Daten einfügen</span><span class="sxs-lookup"><span data-stu-id="c33f8-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="c33f8-114">Syntaxfärbung</span><span class="sxs-lookup"><span data-stu-id="c33f8-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="c33f8-115"><a name="ActivateAdvEditor">Erweiterten Formeleditor aktivieren</a></span><span class="sxs-lookup"><span data-stu-id="c33f8-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="c33f8-116">Führen Sie die folgenden Schritte aus, um den erweiterten Formeleditor in Ihrer Instanz von Microsoft Dynamics 365 Finance zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c33f8-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="c33f8-117">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="c33f8-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="c33f8-118">Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="c33f8-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="c33f8-119">Setzen Sie im Dialogfeld **Benutzerparameter** im Abschnitt **Ausführungsnachverfolgung** den Parameter **Erweiterten Formeleditor aktivieren** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c33f8-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="c33f8-120">[![Dialogfeld „Benutzerparameter“, Parameter „Erweiterten Formeleditor aktivieren“ hervorgehoben](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="c33f8-120">[![User parameters dialog box, Enable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="c33f8-121">Beachten Sie, dass dieser Parameter benutzerspezifisch und unternehmensspezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="c33f8-121">Be aware that this parameter is user specific and company specific.</span></span>

<span data-ttu-id="c33f8-122">Ab Microsoft Dynamics 365 Finance-Version 10.0.19 können Sie steuern, welcher ER-Formel-Editor standardmäßig angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="c33f8-122">Starting in Microsoft Dynamics 365 Finance version 10.0.19, you can control what ER formula editor is offered by default.</span></span> <span data-ttu-id="c33f8-123">Führen Sie die folgenden Schritte aus, um den erweiterten Formeleditor für alle Benutzer und Firmen der aktuellen Finance-Instanz zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c33f8-123">Complete the following steps to enable the advanced formula editor for all users and companies of the current Finance instance.</span></span>

1.  <span data-ttu-id="c33f8-124">Öffnen Sie den Arbeitsbereich **Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="c33f8-124">Open the **Feature management** workspace.</span></span>
2.  <span data-ttu-id="c33f8-125">Suchen Sie die Funktion **Erweiterten Formeleditor als Standard für alle Benutzer festlegen** in der Liste und wählen Sie dann **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="c33f8-125">Find and select the feature **Set the ER advanced formula editor as the default one for all users** in the list, and then select **Enable now**.</span></span>
3.  <span data-ttu-id="c33f8-126">Gehen Sie zu **Organisationsverwaltung** > **Elektronisches Berichtswesen** > **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="c33f8-126">Go to **Organization administration** > **Electronic reporting** > **Configurations**.</span></span>
4.  <span data-ttu-id="c33f8-127">Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="c33f8-127">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
5.  <span data-ttu-id="c33f8-128">Suchen Sie im Dialogfeld **Benutzerparameter** den Parameter **Erweiterten Formeleditor deaktivieren** und überprüfen Sie, dass er auf **Nein** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c33f8-128">In the **User parameters** dialog box, find the **Disable advanced formula editor** parameter and verify that it is set to **No**.</span></span>

<span data-ttu-id="c33f8-129">[![Dialogfeld „Benutzerparameter“, Parameter „Erweiterten Formeleditor deaktivieren“ hervorgehoben](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span><span class="sxs-lookup"><span data-stu-id="c33f8-129">[![User parameters dialog box, Disable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span></span>

> [!NOTE]
> <span data-ttu-id="c33f8-130">Die Werte der Parameter **Erweiterten Formeleditor aktivieren** und **Erweiterten Formeleditor deaktivieren** werden für jeden Benutzer getrennt gehalten und im Dialogfeld **Benutzerparameter** in Abhängigkeit vom Status der Funktion **Erweiterten Formeleditor als Standard für alle Benutzer festlegen** angeboten.</span><span class="sxs-lookup"><span data-stu-id="c33f8-130">The values of the parameters **Enable advanced formula editor** and **Disable advanced formula editor** are kept separate for each user and offered on the **User parameters** dialog box depending on the status of the **Set the ER advanced formula editor as the default one for all users** feature.</span></span>

## <a name=""></a><span data-ttu-id="c33f8-131"><a name="Autoformatting">Automatische Codeformatierung</a></span><span class="sxs-lookup"><span data-stu-id="c33f8-131"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="c33f8-132">Wenn Sie einen komplexen Ausdruck schreiben, der aus mehreren Codezeilen besteht, erfolgt die Einrückung einer neuen eingegebenen Zeile automatisch anhand der Einrückung der vorherigen Zeile.</span><span class="sxs-lookup"><span data-stu-id="c33f8-132">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="c33f8-133">Sie können Zeilen auswählen und deren Einrückung durch Eingabe von **TAB** oder **UMSCHALT + TAB** ändern.</span><span class="sxs-lookup"><span data-stu-id="c33f8-133">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="c33f8-134">[![ER-Formel-Editor-Gif mit Zeilenauswahl und Änderung der Einrückung](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="c33f8-134">[![ER formula editor gif showing selecting lines and changing the indentation](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="c33f8-135">Mit der automatischen Formatierung können Sie den gesamten Ausdruck gut formatieren, um die weitere Verwaltung sowie das Verständnis der konfigurierten Logik zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="c33f8-135">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="c33f8-136"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="c33f8-136"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="c33f8-137">Der Editor bietet eine Wortvervollständigung, um das Schreiben von Ausdrücken zu beschleunigen und Tippfehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="c33f8-137">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="c33f8-138">Wenn Sie mit dem Hinzufügen von neuem Text beginnen, bietet der Editor automatisch eine Liste von Funktionen an, die von ER-Funktionen unterstützt werden, die die von Ihnen eingegebenen Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c33f8-138">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="c33f8-139">Sie können IntelliSense auch an einer beliebigen Stelle eines konfigurierten Ausdrucks durch Eingabe von **STRG + LEERZEICHEN** auslösen.</span><span class="sxs-lookup"><span data-stu-id="c33f8-139">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="c33f8-140">[![ER Formel-Editor gif zeigt das Auslösen von IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="c33f8-140">[![ER formula editor gif showing triggering IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="c33f8-141"><a name="CodeCompletion">Code-Abschluss</a></span><span class="sxs-lookup"><span data-stu-id="c33f8-141"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="c33f8-142">Der Editor unterstützt den Codeabschluss automatisch durch:</span><span class="sxs-lookup"><span data-stu-id="c33f8-142">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="c33f8-143">Einfügen einer schließenden Klammer, wenn eine öffnende Klammer eingegeben wird, wobei der Cursor in den Klammern verbleibt.</span><span class="sxs-lookup"><span data-stu-id="c33f8-143">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="c33f8-144">Einfügen des zweiten Anführungszeichens bei der Eingabe des ersten, wobei der Cursor innerhalb der Anführungszeichen bleibt.</span><span class="sxs-lookup"><span data-stu-id="c33f8-144">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="c33f8-145">Einfügen des zweiten doppelten Anführungszeichens bei der Eingabe des ersten, wobei der Cursor innerhalb der Anführungszeichen bleibt.</span><span class="sxs-lookup"><span data-stu-id="c33f8-145">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="c33f8-146">[![ER Formel-Editor gif zeigt, dass der Editor automatisch Code-Vervollständigung anbietet](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="c33f8-146">[![ER formula editor gif showing the editor automatically providing code completion](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="c33f8-147">Wenn Sie auf die eingegebene Klammer zeigen, wird die zweite Klammer dieses Paares automatisch markiert, um das von ihnen unterstützte Konstrukt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c33f8-147">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="c33f8-148"><a name="CodeNavigation">Code-Navigation</a></span><span class="sxs-lookup"><span data-stu-id="c33f8-148"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="c33f8-149">Sie können die erforderlichen Symbole oder Zeilen finden, indem Sie den Befehl für **Gehe zu** über die Befehlspalette oder das Kontextmenü eingeben.</span><span class="sxs-lookup"><span data-stu-id="c33f8-149">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="c33f8-150">Beispiel: Gehen Sie wie folgt vor, um zur Zeile **8** zu springen:</span><span class="sxs-lookup"><span data-stu-id="c33f8-150">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="c33f8-151">Drücken Sie **STRG+G**, geben Sie den Wert **8** ein, drücken Sie dann die **Eingabetaste**.</span><span class="sxs-lookup"><span data-stu-id="c33f8-151">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="c33f8-152">– oder –</span><span class="sxs-lookup"><span data-stu-id="c33f8-152">-or-</span></span>

- <span data-ttu-id="c33f8-153">Drücken Sie **F1**, geben Sie **G** ein, wählen Sie **Gehe zu Position** aus, geben Sie **8** ein und drücken Sie die **Eingabetaste**.</span><span class="sxs-lookup"><span data-stu-id="c33f8-153">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="c33f8-154">[![ER Formeleditor gif zeigt, wie man Teile eines Ausdrucks mit Hilfe der Befehlspalette lokalisiert](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="c33f8-154">[![ER formula editor gif showing how to locate parts of an expression using the command palette](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="c33f8-155"><a name="CodeStructuring">Code-Strukturierung</a></span><span class="sxs-lookup"><span data-stu-id="c33f8-155"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="c33f8-156">Der Code für einige Funktionen, wie [IF](er-functions-logical-if.md) oder [CASE](er-functions-logical-case.md) wird automatisch strukturiert.</span><span class="sxs-lookup"><span data-stu-id="c33f8-156">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="c33f8-157">Sie können einen oder alle Faltungsbereiche dieses Codes erweitern und reduzieren, um den bearbeitbaren Teil eines Ausdrucks zu verkleinern, damit Sie sich nur auf den Teil des Code konzentrieren können, der Ihrer Aufmerksamkeit bedarf.</span><span class="sxs-lookup"><span data-stu-id="c33f8-157">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="c33f8-158">Hierfür können die Befehle zum Umschalten zwischen Falten und Auffalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c33f8-158">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="c33f8-159">Beispiel: Gehen Sie folgendermaßen, um alle Regionen zu falten:</span><span class="sxs-lookup"><span data-stu-id="c33f8-159">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="c33f8-160">Drücken Sie **STRG+K**</span><span class="sxs-lookup"><span data-stu-id="c33f8-160">Press **Ctrl+K**</span></span>

  <span data-ttu-id="c33f8-161">– oder –</span><span class="sxs-lookup"><span data-stu-id="c33f8-161">-or-</span></span>

- <span data-ttu-id="c33f8-162">Drücken Sie **F1** und **FO**, wählen Sie **Alle falten** aus und drücken Sie die **Eingabetaste**</span><span class="sxs-lookup"><span data-stu-id="c33f8-162">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="c33f8-163">Gehen Sie folgendermaßen, um alle Regionen aufzufalten:</span><span class="sxs-lookup"><span data-stu-id="c33f8-163">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="c33f8-164">Drücken Sie **STRG+J**</span><span class="sxs-lookup"><span data-stu-id="c33f8-164">Press **Ctrl+J**</span></span>

  <span data-ttu-id="c33f8-165">– oder –</span><span class="sxs-lookup"><span data-stu-id="c33f8-165">-or-</span></span>
  
- <span data-ttu-id="c33f8-166">Drücken Sie **F1** geben Sie **UN** ein, wählen Sie **Alle auffalten** aus und drücken Sie die **Eingabetaste**</span><span class="sxs-lookup"><span data-stu-id="c33f8-166">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="c33f8-167">[![ER formula editor gif zeigt, wie der Code aufgefaltet wird](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="c33f8-167">[![ER formula editor gif showing code being unfolded](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="c33f8-168"><a name="FindAndReplace">Suchen und ersetzen</a></span><span class="sxs-lookup"><span data-stu-id="c33f8-168"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="c33f8-169">Um einen bestimmten Text zu finden, wählen Sie den Text in Ihrem Ausdruck aus und gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="c33f8-169">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="c33f8-170">Drücken Sie **STRG+F** und dann **F3**, um das nächste Vorkommen des ausgewählten Textes zu finden, oder drücken Sie **UMSCHALT+F3**, um das vorherige Vorkommen zu finden.</span><span class="sxs-lookup"><span data-stu-id="c33f8-170">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="c33f8-171">– oder –</span><span class="sxs-lookup"><span data-stu-id="c33f8-171">-or-</span></span>
  
- <span data-ttu-id="c33f8-172">Drücken Sie **F1**, geben Sie **F** ein und wählen Sie anschließend die erforderliche Option aus, um den ausgewählten Text zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c33f8-172">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="c33f8-173">Um einen bestimmten Text zu ersetzen, wählen Sie den Text in Ihrem Ausdruck aus und gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="c33f8-173">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="c33f8-174">Drücken Sie **STRG+H**.</span><span class="sxs-lookup"><span data-stu-id="c33f8-174">Press **Ctrl+H**.</span></span> <span data-ttu-id="c33f8-175">Geben Sie den alternativen Text ein und wählen Sie die Ersetzungsoption aus, um entweder den ausgewählten Text oder alle Vorkommen dieses Texts im aktuellen Ausdruck zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="c33f8-175">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="c33f8-176">– oder –</span><span class="sxs-lookup"><span data-stu-id="c33f8-176">-or-</span></span>
  
- <span data-ttu-id="c33f8-177">Drücken Sie **F1**, geben Sie **R** ein und wählen Sie anschließend die erforderliche Option aus, um den ausgewählten Text zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="c33f8-177">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="c33f8-178">Geben Sie den alternativen Text ein und wählen Sie die Ersetzungsoption aus, um entweder den ausgewählten Text oder alle Vorkommen dieses Texts im aktuellen Ausdruck zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="c33f8-178">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="c33f8-179">Um alle Vorkommen eines bestimmten Texts zu ändern, wählen Sie den Text in Ihrem Ausdruck aus und gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="c33f8-179">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="c33f8-180">Drücken Sie **STRG+F2** und geben Sie dann den alternativen Text ein.</span><span class="sxs-lookup"><span data-stu-id="c33f8-180">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="c33f8-181">– oder –</span><span class="sxs-lookup"><span data-stu-id="c33f8-181">-or-</span></span>
  
- <span data-ttu-id="c33f8-182">Drücken Sie **F1**, geben Sie **C** ein und wählen Sie anschließend die erforderliche Option aus, um den ausgewählten Text zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c33f8-182">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="c33f8-183">Geben Sie den alternativen Text ein.</span><span class="sxs-lookup"><span data-stu-id="c33f8-183">Enter the alternative text.</span></span>

<span data-ttu-id="c33f8-184">[![ER Formel-Editor gif zeigt das Suchen und Ersetzen](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="c33f8-184">[![ER formula editor gif showing find and replace](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="c33f8-185"><a name="DataPasting">Einfügen von Datenquellen und Funktionen</a></span><span class="sxs-lookup"><span data-stu-id="c33f8-185"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="c33f8-186">Sie können **Datenquelle hinzufügen** auswählen, sodass beim aktuellen Ausdruck eine Datenquelle eingefügt wird, die derzeit im linken **Datenquelle**-Bereich auswählt ist.</span><span class="sxs-lookup"><span data-stu-id="c33f8-186">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="c33f8-187">Sie können auch **Funktion hinzufügen** auswählen, sodass beim aktuellen Ausdruck eine Funktion eingefügt wird, die derzeit im rechten **Funktionen**-Bereich auswählt ist.</span><span class="sxs-lookup"><span data-stu-id="c33f8-187">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="c33f8-188">Wenn Sie den ER-Formeleditor verwenden, wird eine ausgewählte Funktion oder ausgewählte Datenquelle immer an das Ende des konfigurierten Ausdrucks angefügt.</span><span class="sxs-lookup"><span data-stu-id="c33f8-188">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="c33f8-189">Wenn Sie den erweiterten ER-Formeleditor verwenden, kann eine ausgewählte Funktion oder ausgewählte Datenquelle an einen beliebigen Teil des konfigurierten Ausdrucks angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c33f8-189">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="c33f8-190">Sie müssen den Cursor verwenden, um anzugeben, wo Sie die Daten einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="c33f8-190">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="c33f8-191">[![ER Formeleditor gif zeigt das Hinzufügen einer Datenquelle und das Einfügen einer Funktion](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="c33f8-191">[![ER formula editor gif showing adding a data source and pasting a function](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="c33f8-192"><a name="SyntaxColorization">Syntaxfärbung</a></span><span class="sxs-lookup"><span data-stu-id="c33f8-192"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="c33f8-193">Gegenwärtig werden verschiedene Farben verwendet, um die folgenden Teile von Ausdrücken hervorzuheben:</span><span class="sxs-lookup"><span data-stu-id="c33f8-193">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="c33f8-194">Der Text in doppelten Klammern, der eine Beschriftungs-ID einer Textkonstante darstellen kann.</span><span class="sxs-lookup"><span data-stu-id="c33f8-194">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="c33f8-195">[![ER-Formeleditor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="c33f8-195">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="c33f8-196">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="c33f8-196">Limitations</span></span>

<span data-ttu-id="c33f8-197">Der Editor wird derzeit in folgenden Webbrowsern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c33f8-197">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="c33f8-198">Chrom</span><span class="sxs-lookup"><span data-stu-id="c33f8-198">Chrome</span></span>
- <span data-ttu-id="c33f8-199">Edge</span><span class="sxs-lookup"><span data-stu-id="c33f8-199">Edge</span></span>
- <span data-ttu-id="c33f8-200">Firefox</span><span class="sxs-lookup"><span data-stu-id="c33f8-200">Firefox</span></span>
- <span data-ttu-id="c33f8-201">Opera</span><span class="sxs-lookup"><span data-stu-id="c33f8-201">Opera</span></span>
- <span data-ttu-id="c33f8-202">Safari</span><span class="sxs-lookup"><span data-stu-id="c33f8-202">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c33f8-203">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c33f8-203">Additional resources</span></span>

- [<span data-ttu-id="c33f8-204">Überblick über die elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="c33f8-204">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="c33f8-205">Formeldesigner in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="c33f8-205">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="c33f8-206">Monaco-Editor</span><span class="sxs-lookup"><span data-stu-id="c33f8-206">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
