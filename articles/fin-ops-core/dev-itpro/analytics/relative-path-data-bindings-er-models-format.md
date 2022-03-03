---
title: Verwenden Sie einen relativen Pfad in den Datenbindungen von ER-Modellen und -Formaten
description: Mit dem Tool für die elektronische Berichterstellung können Sie elektronische Formatstrukturen definieren und anschließend beschreiben, wie diese Strukturen ausgefüllt werden sollen.
author: NickSelin
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: af3a646e24976d50f83d8564e3006fc2c50d8e2a
ms.sourcegitcommit: 8bcb9c13eccb14e61c39ca6578d135b64090fad2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2022
ms.locfileid: "8313566"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>Verwenden Sie einen relativen Pfad in den Datenbindungen von ER-Modellen und -Formaten

[!include[banner](../includes/banner.md)]

Mit dem Tool für die elektronische Berichterstellung (ER) können Benutzer elektronische Formatstrukturen definieren und anschließend wird beschrieben, wie diese Strukturen ausgefüllt werden sollen, indem Sie Daten und Algorithmen verwenden, die in der Anwendung vorhanden sind. Weitere Informationen finden Sie unter [Elektronische Berichterstellungskonfigurationen (ER) erstellen](electronic-reporting-configuration.md). Um den Datenfluss zum Abrufen der Daten von Finance and Operations zu definieren und diese zur Erstellung eines elektronischen Dokuments zu verwenden, müssen Sie folgende Schritte ausführen:

- Binden Sie Sie konfigurierte Datenquellen an die Elemente des entworfenen domänenspezifischen Datenmodells. Die Modellstruktur und die ausgewählten Datenquellen könnten Teil einer komplexen hierarchische Struktur sein. Deshalb können endgültige Beziehungen ziemlich groß sein und viele Elemente verschiedener Typen enthalten (zum Beispiel Zuordnungen, Tabellen und Methoden,). Die Beziehungen können weniger lesbar und ziemlich komplex sein zum Verstehen und Prüfen, besonders für Nicht-Eigentümer. 
- Binden Sie Datenmodellelemente mit Formatkomponenten, um zu definieren, welche Daten vom Datenmodell der generierten Ausgabe des Formats ausgefüllt werden.

Um die Benutzerfreundlichkeit der EB-Zuordnungs-Designer zu verbessern, ist die Funktion [relativer Pfad](er-formula-language.md#relative-path) freigegeben worden. Standardmäßig wird die Darstellungsoption des relativen Pfades für jede neue Instanz der Anwendung aktiviert, wenn die ER-Designerfahrung aktiviert ist (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service). Wir haben die relativen Pfadparameter implementiert, damit die Benutzer den vollständigen Pfad weiterhin verwenden können, wenn sie mit dieser Darstellung der ER-Bindungen arbeiten.

[![Benutzer-Parameter.](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Wenn der verwendet Parameter des relativen Pfades aktiviert ist, ersetzt ein einzelnes @-Zeichen den Pfad zum übergeordneten Artikel in der aktuellen Bindung des Modellelements. Der vollständige Bindungspfad wird kürzer, wodurch die gesamte Zuordnung einfacher, offensichtlicher und einfacher zum Verstehen wird. In den meisten Fällen wird kein zusätzlicher Bildlauf erforderlich sein im ER-Designer, um alle Berichtsbeziehungen des Datenmodells anzuzeigen.

[![Modellzuordnungsdesigner.](./media/relative-path-02.png)](./media/relative-path-02.png)
 
Wenn Sie beginnen, einen neuen ER-Ausdruck zu entwerfen, müssen Sie nur einem Zeichen eingeben, um eine Bindung für ein Feld des übergeordneten Artikels zu definieren.

[![Formeldesigner.](./media/relative-path-03.png)](./media/relative-path-03.png)
 
Wenn Sie sich dazu entschließen, die Datenquelle des übergeordneten Modellartikels mit der Nutzung des absoluten Pfades zu ändern, müssen Sie diesen Modellartikel sowie alle geschachtelten Artikel manuell auf eine neue Datenquelle binden. Wenn die Verwendung des relativen Pfades aktiviert ist und Sie eine neue Datenquelle auswählen, die an das übergeordnete Element gebunden wird, erhalten Sie eine Option, um alle geschachtelten Elemente dieses übergeordneten Elements mit einem Klick erneut zu binden.

[![Ersetzen der vorhandenen Pfadnachricht.](./media/relative-path-04.png)](./media/relative-path-04.png)
 
Wenn Sie das erneute Binden geschachtelter Artikel bestätigen, wird das übergeordnete Element neu dem Pfad vo jedem geschachtelten Artikel hinzugefügt, das das vorhandenen übergeordneten Element enthält.
Diese Funktion bricht die Abwärtskompatibilität des ER-Frameworks nicht. Alle zuvor entworfenen ER-Konfigurationen arbeiten mit dieser neuen Funktionen, und Aktualisierungen oder Umwandlungen sind erforderlich.

> [!NOTE]
> Alle Änderungen, die durch die Massenänderung von Berichtsbeziehungen geschachtelter Elemente in den Modellzuordnungen eingeführt werden, werden in einen Konfigurationsdelta (Nachverfolgung der Änderungen) korrekt gespeichert. Dies ermöglicht es Debitoren, ihre abgeleitete Version von Modellzuordnungen einer neuen Basisversion zuzuordnen, die mithilfe dieser neuen Funktion geändert wurde.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[EB-Formelsprache](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
