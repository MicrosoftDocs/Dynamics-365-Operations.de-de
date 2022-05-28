---
title: Übersicht über Momentaufnahmen
description: In diesem Thema wird die Momentaufnahmefunktion beschrieben, mit der Sie eine Cashflow-Planung zur späteren Analyse oder zum Vergleich mit Istdaten speichern können. Wenn Sie eine Cashflow-Planung erstellen, können Sie diese Prognose als „Momentaufnahme“ speichern. Mit dieser Momentaufnahme können Sie dann die Konten bearbeiten, die in der Prognose enthalten waren, oder die Prognose in der Momentaufnahme mit den Istwerten vergleichen.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f84afddb26136797a7d35faf52325702b8e41a45
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725344"
---
# <a name="snapshots-overview"></a>Übersicht über Momentaufnahmen

[!include [banner](../includes/banner.md)]

Mit Momentaufnahmen können Unternehmen Informationen zu ihrer Bargeldposition und Bargeldplanungen zu einem bestimmten Zeitpunkt bearbeiten und speichern. Sie können die Momentaufnahme mit den Ist-Finanzdaten vergleichen, die Abweichung untersuchen und diese Informationen verwenden, um die Cashflow-Planung im Laufe der Zeit zu verbessern. Genauer können Momentaufnahmen folgendermaßen verwendet werden:

- Verfolgen der Bargeldposition und Bargeldplanungen im Laufe der Zeit.
- Filtern der Daten, um eine Teilmenge der juristischen Personen anzuzeigen, für die die Momentaufnahme erstellt wurde.
- Bearbeiten der vom System generierten Bargeldposition und der Bargeldplanung.
- Führen Sie eine Was-wäre-wenn-Analyse durch, um optimistische, pessimistische und höchstwahrscheinliche Ansichten zum Cashflow zu berücksichtigen.
- Vergleichen Sie die tatsächliche finanzielle Leistung mit der Prognose, die in der Momentaufnahme gespeichert ist.

Sie können eine Momentaufnahme erstellen, indem Sie **Neue Momentaufnahme** entweder auf der **Bargeldposition**-Registerkarte oder der **-Bargeldplanung**-Registerkarte im **Cashflow-Planung**-Arbeitsbereich auswählen. Nachdem eine Momentaufnahme erstellt wurde, können die darin enthaltenen Ein- und Abgänge bearbeitet und gespeichert werden. Alle gespeicherten Momentaufnahmen sind auf der **Momentaufnahmen**-Registerkarte verfügbar. Um eine Momentaufnahme zu öffnen, wählen Sie ihren Namen aus.

Die Bargeldein- und -abgänge in Momentaufnahmen können jederzeit bearbeitet werden. Wenn ein Zugangsbetrag oder ein Abgangsbetrag bearbeitet wird, wird der aktualisierte Betrag auf die Liquiditätskonten aufgeteilt, die den ursprünglichen Saldo erstellt haben. Wenn Sie die Bearbeitung einer Momentaufnahme beendet haben, wählen Sie **Schließen**, um die Änderungen zu speichern.

Um die tatsächlichen Finanzergebnisse mit einer Prognose zu vergleichen, die als Momentaufnahme gespeichert wurde, wählen Sie **Mit Istwerten vergleichen** aus. Die Seite **Mit Istwerten vergleichen** zeigt einen Vergleich der tatsächlichen Beträge und der Prognose. Das Diagramm im oberen Bereich der Seite zeigt einen Vergleich der Bargeldeingänge, Bargeldabgänge und des Bankguthabens in den überlappenden Zeiträumen zwischen den beiden Momentaufnahmen. Das Raster im unteren Bereich zeigt einen detaillierten Vergleich der tatsächlichen Bilanz pro Zeitraum und die prognostizierte Bilanz für jeden Liquiditätsbetrag. Die **Varianz**-Spalte im Raster zeigt die Differenz zwischen der tatsächlichen Bilantz in einem Zeitraum und der prognostizierten Bilanz.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
