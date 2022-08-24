---
title: Suchdatenquellen für die Verwendung anwendungsspezifischer EB-Parameter konfigurieren
description: In diesem Artikel wird erläutert, wie Sie Suchdatenquellen in elektronische Berichterstellungsformate (EB-Formate) konfigurieren können, um anwendungsspezifische EB-Parameter zu verwenden.
author: kfend
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.custom: ''
ms.assetid: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
ms.openlocfilehash: f3ce5837b1d20860588848a1b518b3d801a05db4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285120"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a>Suchdatenquellen für die Verwendung anwendungsspezifischer EB-Parameter konfigurieren 

[!include[banner](../includes/banner.md)]

Mit der anwendungsspezifischen Parameterfunktion zur [elektronischen Berichtserstellung (EB)](general-electronic-reporting.md) können Sie die Datenfilterung in einem EB-Format konfigurieren, damit sie auf einer Gruppe von abstrakten Regeln basiert. Diese Gruppe von Regeln kann so konfiguriert werden, dass sie die Datenquellen vom Typ **Suche** nutzt, die in einem EB-Format verfügbar sind. Sie können echte Regeln über die EB-Komponentendesigner hinaus angeben, indem sie die Benutzeroberfläche, die automatisch anhand der Einstellungen der **Such**-Datenquellen des entsprechenden EB-Formats erzeugt wird, und die aktuellen Daten der juristischen Person verwenden. Auf die angegebenen Regeln wird schließlich von der **Such**-Datenquelle des EB-Formats zugegriffen, wenn dieses EB-Format ausgeführt wird.

> [!NOTE]
> Verwenden Sie die konfigurierten Datenquellen des bearbeitbaren EB-Formats, um anzugeben, welche Anwendungsdaten zum Konfigurieren echter Regeln verwendet werden.

Verwenden Sie den [EB-Vorgangsdesigner](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base), um eine Datenquelle vom Typ **Suche** in Ihr EB-Format aufzunehmen. Die Datenquelle muss so konfiguriert sein, dass sie beschreibt, wie Ihre abstrakten Regeln aussehen, einschließlich Folgendem:

   - Der Parametersatz eines bestimmten Datentyps, dessen Wert zur Angabe einer einzelnen Regel angegeben wird.
   - Der Werttyp eines bestimmten Datentyps, der von einer einzelnen Regel zurückgegeben wird, wenn diese Regel unter anderem als am besten geeignet angesehen wird.

Sie können die folgenden Arten von **Such**-Datenquellen konfigurieren, je nach dem Typ des Werts, der von einer konfigurierten Regel zurückgegeben wird:

   - Verwenden Sie den Typ **Datenmodell\Suche**, wenn ein Modellenumerationswert zurückgegeben werden muss.
   - Verwenden Sie den Typ **Dynamics 365 Operations\Suche**, wenn ein Anwendungsenumerationswert oder ein Anwendungswert vom [erweiterten Datentyp](../extensibility/extensible-edts.md) zurückgegeben werden muss.
   - Verwenden Sie den Typ **Formatenumeration\Suche**, wenn ein Formateneumerationswert zurückgegeben werden muss.

Die folgende Abbildung zeigt, wie eine Formatenumeration im EB-Beispielformat konfiguriert werden kann.

   ![Anzeigen einer Formatenumeration als Basis für die konfigurierte Suchdatenquelle.](./media/er-lookup-data-sources-img1.gif)

Die folgende Abbildung zeigt die Formatkomponenten, die so konfiguriert wurden, dass unterschiedliche Steuertypen in einem anderen Abschnitt eines generierten Berichts gemeldet werden.

   ![Anzeigen der Formatabschnitte, um verschiedene Arten von Steuern separat zu melden.](./media/er-lookup-data-sources-img2.png)

Die folgende Abbildung zeigt, wie der EB-Vorgangsdesigner das Hinzufügen einer Datenquelle vom Typ **Formatenumeration\Suche** ermöglicht.  Die hinzugefügte Datenquelle ist so konfiguriert, dass sie einen Wert der `List of taxation levels`-Formatenumeration zurückgibt.

   ![Hinzufügen einer EB-Datenquelle vom Typ Formatenumeration\Suche.](./media/er-lookup-data-sources-img3.gif)

Die folgende Abbildung zeigt, wie die hinzugefügte Datenquelle für die Verwendung des Felds **Code** der Datensatzliste **Model.Data.Tax** der Datenquelle **Modell** als Parameter konfiguriert wird, der für jede konfigurierte Regel angegeben werden muss.

![Konfigurieren von Parametern der hinzugefügten Datenquelle vom Typ Formatenumeration\Suche.](./media/er-lookup-data-sources-img4.gif)

Die hinzugefügte Datenquelle `Model.Data.Tax` ist so konfiguriert, dass für jede konfigurierte Regel ein Steuercode angegeben wird, indem auf Datensätze der Anwendungstabelle **TabTable** zurückgegriffen wird.

   ![Eine Suchdatenquelle vom Typ Formatenumeration\Suche für ein einzelnes Unternehmen überprüfen.](./media/er-lookup-data-sources-img5.gif)

Sie können die Suchregeln für das ausgewählte EB-Format mithilfe der Benutzeroberfläche einrichten, die automatisch an der Struktur der konfigurierten Datenquelle ausgerichtet wird. Derzeit erfordert diese Benutzeroberfläche, dass Sie für jede Regel den zurückgegebenen Wert als `List of taxation levels`-Formatenumerationswert sowie den Steuercode als Parameter festlegen.

   ![Regeln für die konfigurierte Datenquelle einrichten.](./media/er-lookup-data-sources-img6.gif)

Die folgende Abbildung zeigt, wie `Model.Data.Summary.LevelByLookup`-Datenquelle vom Typ **Berechnetes Feld** konfiguriert werden kann, um die konfigurierte **Such**-Datenquelle mit den erforderlichen Parametern aufzurufen. Um diesen Aufruf zur Laufzeit zu verarbeiten, durchsucht EB die Liste der konfigurierten Regeln in der definierten Reihenfolge, um die erste Regel zu finden, die die angegebenen Bedingungen erfüllt. In diesem Beispiel enthält die Regel den Steuercode, der mit dem angegebenen übereinstimmt. Als Ergebnis wird die am besten geeignete Regel gefunden und der für die gefundene Regel konfigurierte Aufzählungswert wird von dieser Datenquelle zurückgegeben.

> [!NOTE]
> Eine Ausnahme wird ausgelöst, wenn keine zutreffende Regel gefunden wird. Um diese Ausnahmen zu vermeiden, konfigurieren Sie zusätzliche Regeln am Ende der Regelliste, um Fälle zu behandeln, in denen ein nicht konfigurierter oder kein Wert angegeben wird. Verwenden Sie die Optionen **\*Nicht leer**\* und **\*Leer**\* entsprechend.  
>
> ![Fügen Sie eine Datenquelle hinzu, um die konfigurierte Suchdatenquelle aufzurufen.](./media/er-lookup-data-sources-img7.png)

Wenn Sie die Option **Unternehmensüberprüfend** für die bearbeitbare Suchdatenquelle auf **Ja** setzen, fügen Sie dem Parametersatz dieser Datenquelle einen neuen erforderlichen **Unternehmen**-Parameter hinzu. Der Wert des **Unternehmen**-Parameter muss zur Laufzeit angegeben werden, wenn die Suchdatenquelle aufgerufen wird. Wenn der Buchungskreis zur Laufzeit angegeben wird, werden die für dieses Unternehmen konfigurierten Regeln verwendet, um die am besten geeignete Regel zu finden, und der entsprechende Wert wird zurückgegeben. Die folgende Abbildung zeigt, wie Sie dies tun können und wie der Parametersatz der bearbeitbaren Datenquelle geändert wird.

   ![Eine unternehmensübergreifende Suchdatenquelle vom Typ Formatenumeration\Suche überprüfen.](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> Wählen Sie jedes Unternehmen separat aus, um die Regeln für diese Suchdatenquelle im bearbeitbaren EB-Format zu konfigurieren. Zur Laufzeit wird eine Ausnahme ausgelöst, wenn die unternehmensübergreifende Suche mit dem Code des Unternehmens aufgerufen wird, für das die Sucheinstellung nicht abgeschlossen wurde.
>
> Stellen Sie sicher, dass Sie Berechtigungen für einen Benutzer erteilen, der das EB-Format mit der unternehmensübergreifenden **Such**-Datenquelle ausführt, um auf die Daten aller Unternehmen zuzugreifen, die unter diese Datenquelle fallen. Andernfalls wird zur Laufzeit eine Ausnahme ausgelöst.

Ab Version 10.0.19 sind die erweiterten Funktionen der **Such**-Datenquellen verfügbar. Wenn Sie die Option **Erweitert** für die bearbeitbare Suchdatenquelle auf **Ja** stellen, wird die konfigurierte Suchdatenquelle in die strukturierte Datenquelle umgewandelt, die die zusätzlichen Funktionen zum Analysieren des konfigurierten Regelsatzes bietet. Die folgende Abbildung zeigt dieser Transformation.

   ![Die struktierte Suchdatenquelle vom Typ Formatenumeration\Suche überprüfen.](./media/er-lookup-data-sources-img9.gif)

- Das Unterlement **Suche** ist als Funktion konzipiert, um die am besten geeignete Regel aus dem Satz konfigurierbarer Regeln basierend auf dem bereitgestellten Parametersatz zu finden.
- Das Unterelement **IsLookupResultSet** dient als Funktion zum Akzeptieren des angegebenen Werts der Basisenumerationsdatenquelle und zum Zurückgeben des *booleschen* Werts **wahr**, wenn der Regelsatz mindestens eine Regel enthält, für die der angegebene Enumerationswert als zurückgegebener Wert konfiguriert wurde. Diese Funktion gibt den *booleschen* Wert **falsch** zurück, wenn keine Regeln konfiguriert sind, um den angegebenen Enumerationswert zurückzugeben.
- Das Unterelement **Einstellung** ist als eine Funktion konzipiert, die den Satz konfigurierter Regeln als Datensätze einer Datensatzliste zurückgibt. Die zurückgegebenen Werte und der Parametersatz der konfigurierten Regeln werden in jedem zurückgegebenen Datensatz als Felder der relevanten Datentypen dargestellt:

    - Der zurückgegebene Wert wird als Feld **Suchergebnis** dargestellt.
    - Die konfigurierten Parameter werden als Felder mit Parameternamen dargestellt (in diesem Beispiel das Feld **Code**).

Weitere Informationen zur Konfiguration der **Such**-Datenquelle finden Sie unter [EB-Formate zur Verwendung von Parametern konfigurieren, die pro juristischer Person angegeben werden](er-app-specific-parameters-configure-format.md). Informationen zum Festlegen der Suchregeln finden Sie unter [Parameter eines EB-Formats pro juristischer Person einrichten](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[ER-Formate zur Verwendung von Parametern konfigurieren, die pro juristischer Person angegeben werden](er-app-specific-parameters-configure-format.md)

[Parameter eines ER-Formats pro juristischer Person einrichten](er-app-specific-parameters-set-up.md)
