---
title: Momentaufnahmenübersicht (Vorschau)
description: In diesem Thema wird die Momentaufnahmefunktion beschrieben, mit der Sie eine Cashflow-Planung zur späteren Analyse oder zum Vergleich mit Istdaten speichern können. Wenn Sie eine Cashflow-Planung erstellen, können Sie diese Prognose als „Momentaufnahme“ speichern. Mit dieser Momentaufnahme können Sie dann die Konten bearbeiten, die in der Prognose enthalten waren, oder die Prognose in der Momentaufnahme mit den Istwerten vergleichen.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 23df01603e74847f6f01a1eaa84b8fd3bb1d6e59
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337207"
---
# <a name="snapshots-overview-preview"></a>Momentaufnahmenübersicht (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Mit Momentaufnahmen können Unternehmen Informationen zu ihrer Bargeldposition und Bargeldplanungen zu einem bestimmten Zeitpunkt bearbeiten und speichern. Sie können die Momentaufnahme mit den Ist-Finanzdaten vergleichen, die Abweichung untersuchen und diese Informationen verwenden, um die Cashflow-Planung im Laufe der Zeit zu verbessern. Genauer können Momentaufnahmen folgendermaßen verwendet werden:

- Verfolgen der Bargeldposition und Bargeldplanungen im Laufe der Zeit.
- Filtern der Daten, um eine Teilmenge der juristischen Personen anzuzeigen, für die die Momentaufnahme erstellt wurde.
- Bearbeiten der vom System generierten Bargeldposition und der Bargeldplanung.
- Führen Sie eine Was-wäre-wenn-Analyse durch, um optimistische, pessimistische und höchstwahrscheinliche Ansichten zum Cashflow zu berücksichtigen.
- Vergleichen Sie die tatsächliche finanzielle Leistung mit der Prognose, die in der Momentaufnahme gespeichert ist.

Sie können eine Momentaufnahme erstellen, indem Sie **Neue Momentaufnahme** entweder auf der **Bargeldposition**-Registerkarte oder der **-Bargeldplanung**-Registerkarte im **Cashflow-Planung**-Arbeitsbereich auswählen. Nachdem eine Momentaufnahme erstellt wurde, können die darin enthaltenen Ein- und Abgänge bearbeitet und gespeichert werden. Alle gespeicherten Momentaufnahmen sind auf der **Momentaufnahmen**-Registerkarte verfügbar. Um eine Momentaufnahme zu öffnen, wählen Sie ihren Namen aus.

Die Bargeldein- und -abgänge in Momentaufnahmen können jederzeit bearbeitet werden. Wenn ein Zugangsbetrag oder ein Abgangsbetrag bearbeitet wird, wird der aktualisierte Betrag auf die Liquiditätskonten aufgeteilt, die den ursprünglichen Saldo erstellt haben. Wenn Sie die Bearbeitung einer Momentaufnahme beendet haben, wählen Sie **Schließen**, um die Änderungen zu speichern.

Um mehrere Momentaufnahmen zu vergleichen, wählen Sie **Momentaufnahmen vergleichen** aus. Sie können zwei Momentaufnahmen gleichzeitig vergleichen. Wählen Sie die beiden zu vergleichenden Momentaufnahmen und dann **OK**. Die Seite **Momentaufnahmen vergleichen** zeigt einen Vergleich der ausgewählten Momentaufnahmen. Das Diagramm im oberen Bereich der Seite zeigt einen Vergleich der Bargeldeingänge, Bargeldabgänge und des Bankguthabens in den überlappenden Zeiträumen zwischen den beiden Momentaufnahmen. Das Raster im unteren Bereich zeigt einen detaillierten Vergleich der beiden Prognosen für jeden Liquiditätsbetrag. Die **Varianz**-Spalte im Raster zeigt die Differenz zwischen den Salden in einem Zeitraum.

Um die tatsächlichen Finanzergebnisse mit einer Prognose zu vergleichen, die als Momentaufnahme gespeichert wurde, wählen Sie **Mit Istwerten vergleichen** aus. Die Seite **Momentaufnahme vergleichen** zeigt einen Vergleich der tatsächlichen Beträge und der Prognose. Das Diagramm im oberen Bereich der Seite zeigt einen Vergleich der Bargeldeingänge, Bargeldabgänge und des Bankguthabens in den überlappenden Zeiträumen zwischen den beiden Momentaufnahmen. Das Raster im unteren Bereich zeigt einen detaillierten Vergleich der tatsächlichen Bilanz pro Zeitraum und die prognostizierte Bilanz für jeden Liquiditätsbetrag. Die **Varianz**-Spalte im Raster zeigt die Differenz zwischen der tatsächlichen Bilantz in einem Zeitraum und der prognostizierten Bilanz.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
