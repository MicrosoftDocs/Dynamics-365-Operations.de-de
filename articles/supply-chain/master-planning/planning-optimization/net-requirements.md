---
title: Bedarfsverläufe und Bedarfsverursacherinformationen mit Planungsoptimierung
description: Dieser Artikel enthält Informationen zu berechneten Bedarfsverläufen und Bedarfsverursacherinformationen in der Planungsoptimierung.
author: t-benebo
ms.date: 7/28/2021
ms.topic: article
ms.search.form: ReqTransOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 259e5793a8dfac67793034d98ccb627fe1947bab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888527"
---
# <a name="net-requirements-and-pegging-information-with-planning-optimization"></a>Bedarfsverläufe und Bedarfsverursacherinformationen mit Planungsoptimierung

[!include [banner](../../includes/banner.md)]

Wenn Sie die Produktprogrammplanung in der Planungsoptimierung ausführen, ist es wichtig, dass Sie die Ergebnisse verstehen, wie die vorhandenen Lieferungen den Bedarf deckt und warum eine bestimmte Lieferung generiert wurde. Sie können die Seite **Bedarfsverlauf** verwenden, um die berechneten Bedarfe, die die Produktprogrammplanung erzeugt, besser zu verstehen.

Die Seite **Bedarfsverlauf** zeigt den Bedarfsverlauf an, den die Planungsoptimierung für das Produkt berechnet hat. Er zeigt auch die Deckungseinstellungen an, die während der Ausführung der Produktprogrammplanung angewendet wurden, eine Aufschlüsselung der Bedarfssummen nach Transaktionstyp und Bedarfsverursacherinformationen.

## <a name="open-the-net-requirements-page"></a>Die Bedarfsverlaufsseite öffnen

Sie können die Seite **Bedarfsverlauf** auf eine der folgenden Arten öffnen:

- Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**. Wählen Sie ein Produkt aus oder öffnen Sie es. Klicken Sie dann im Aktivitätsbereich auf der Registerkarte **Planen** in der Gruppe **Einzelbedarf** auf **Bedarfsverläufe**.
- Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**. Einen Auftrag öffnen. Wählen Sie dann im Inforegister **Auftragspositionen** in der Symbolleiste **Produkt und Beschaffung \> Bedarfsverläufe**.
- Gehen Sie zu **Produktprogrammplanung \> Gesamtplanung \> Geplante Aufträge**. Wählen oder öffnen Sie einen Planauftrag. Klicken Sie dann im Aktivitätsbereich auf der Registerkarte **Anzeige** in der Gruppe **Bedarf** auf **Bedarfsprofil**.

## <a name="use-the-net-requirements-page"></a>Die Bedarfsverlaufsseite benutzen

Die Seite **Bedarfsverlauf** besteht aus oberen und unteren Abschnitten. Der Aktivitätsbereich auf dieser Seite enthält eine Schaltfläche **Aktualisieren**. Wenn diese Schaltfläche ausgewählt wird, wird ein Menü mit Befehlen angezeigt.

### <a name="select-a-master-plan-to-view"></a>Einen Produktprogrammplan zum Anzeigen auswählen

Bevor Sie den Bedarfsverlauf des Produkts überprüfen, wählen Sie unbedingt den entsprechenden Produktprogrammplan im Feld **Planen** oben auf der Seite aus.

### <a name="upper-section"></a>Oberer Abschnitt

Der obere Abschnitt der Seite enthält die folgenden Registerkarten:

- **Übersicht**: Sehen Sie sich den Artikelbedarf der Produktdimensionen an.
- **Artikelabdeckung**: Zeigen Sie die Deckungseinstellungen an, die bei der Bedarfsberechnung verwendet wurden.
- **Zusammenfassung**: Zeigen Sie eine Aufschlüsselung der Bedarfssummen nach Transaktionsart an.
- **Perioden**: Zeigen Sie die Zugänge, Abgänge und voraussichtlich verfügbaren Lagerbestände für jede Periode an, die durch die Periodenvorlage definiert ist. Sie können auch eine grafische Ansicht des voraussichtlich verfügbaren Lagerbestände erhalten.

### <a name="lower-section"></a>Unterer Abschnitt

Der untere Abschnitt der Seite enthält die folgenden Registerkarten:

- **Übersicht**: Zeigen Sie die Liste der Produktbedarfe an, die während der Ausführung der Produktprogrammplanung berechnet wurden, zusammen mit den den Bedarfen entsprechenden Abgangs- und Zugangstransaktionen. Standardmäßig ist die Liste nach Bedarfsdatum sortiert. Wenn Sie einen Einzelbedarf auswählen, zeigt das Inforegister **Bedarfsverursacher** im unteren Bereich entweder die Quelle der Einzelbedarfs oder die Transaktionen an, die den Einzelbedarf erfüllen.
- **Allgemein**: Zeigen Sie detaillierte Informationen zum ausgewählten Einzelbedarf an.
- **Aktivität**: Zeigen Sie Aktivitätsnachrichten für die Bedarfe an.

### <a name="the-action-pane"></a>Der Aktivitätsbereich

Die folgenden Aktivitäten sind im Aktivitätsbereich verfügbar:

- **Aktualisieren \> Produktprogammplanung**: Führen Sie die Produktprogrammplanung direkt von der Seite **Bedarfsverlauf** aus.
- **Aktualisieren \> Absatzplanung**: Führen Sie die Absatzplanung direkt von der Seite **Bedarfsverlauf** aus. Die Planungsoptimierung unterstützt diesen Vorgang noch nicht.
- **Aktualisieren \> Anschlussplanung**: Führen Sie die Anschlussplanung direkt aus der Seite **Bedarfsverlauf** aus. Die Planungsoptimierung unterstützt diesen Vorgang noch nicht.

## <a name="example-scenario"></a>Beispielszenario

Dieses Beispiel zeigt, wie Bedarfsverursacherinformationen auf der Seite **Bedarfsverlauf** dargestellt werden.

### <a name="prerequisites"></a>Voraussetzungen

Bevor Sie das Szenario bearbeiten, müssen die folgenden Voraussetzungen erfüllt sein:

1. Sie müssen in einem System arbeiten, in dem die Standard-Beispieldaten verfügbar sind, und Sie müssen die juristische Person auf *USMF* festlegen.
2. Dieses Beispiel verwendet das Produkt *1000*, das Teil der USMF-Beispieldaten ist. Stellen Sie sicher, dass dieses Produkt verfügbar und wie folgt eingerichtet ist:

    - **Standardauftragstyp:** *Bestellung*
    - **Verfügbarer Bestand:** *10,00*

3. Erstellen Sie einen Auftrag mit der Menge *25,00* des Produkts *1000*. Verwenden Sie die Lagerdimensionen, wo sich der verfügbare Lagerbestand befindet.
4. Führen Sie die Produktprogrammplanung für den Produktprogrammplan *DynPlan* durch.

### <a name="review-the-calculated-requirements"></a>Die berechneten Bedarfe überprüfen

Als Nächstes öffnen Sie die Seite **Bedarfsverlauf** für das Produkt *1000*, um zu überprüfen, wie berechnete Bedarfe miteinander korrespondieren.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie das Produkt mit deren **Artikelnummer** den Wert *1000* hat.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Planen** in der Gruppe **Einzelbedarf** auf **Bedarfsverläufe**.
1. Stellen Sie auf der Seite **Bedarfsverlauf** das Feld **Planen** auf *DynPlan*.
1. Bestätigen Sie in der Registerkarte **Übersicht** im unteren Teil der Seite, ob Folgendes als Zeilen im Raster aufgeführt ist.

    | Referenz | Bedarfsmenge | Kumuliert |
    |---|---|---|
    | Bestand | 10.00 | 10.00 |
    | Geplante Einkaufsbestellungen | 15.00 | 25.00 |
    | Auftrag | -25,00 | (Leer) |

    > [!NOTE]
    > Das Feld **Bedarfsmenge** stellt die Gesamtmenge dar, die der Bedarf entweder benötigt (bei negativem Wert) oder liefert (bei positivem Wert). Das Feld **Kumuliert** stellt die gesamten Zugangs- und Abgangsmengen dar, die sich über die ausgewählte Periode angesammelt haben.

1. Wählen Sie die Bedarfsposition *Bestand* aus und überprüfen Sie dann auf dem Inforegister **Bedarfsverursacher** die Bedarfe, die von diesem Angebot abgedeckt werden. Dort sollte die folgende Zeile erscheinen.

    | Referenz | Bedarfsmenge | Abgedeckte Menge |
    |---|---|---|
    | Auftrag | -25,00 | -10,00 |

    Der verfügbare Lagerbestand deckt teilweise den Bedarf aus dem Auftrag.

    ![Bedarfsverursacherinformationen für den verfügbaren Lagerbestand](media/pegging-on-hand.png "Bedarfsverursacherinformationen für den verfügbaren Lagerbestand")

1. Wählen Sie die Bedarfsposition *geplante Einkaufsbestellung* aus und überprüfen Sie dann auf dem Inforegister **Bedarfsverursacher** die Bedarfe, die von diesem Angebot abgedeckt werden. Dort sollte die folgende Zeile erscheinen.

    | Referenz | Bedarfsmenge | Abgedeckte Menge |
    |---|---|---|
    | Auftrag | -25,00 | -15,00 |

    Da der Auftrag bereits teilweise gedeckt ist, legt das System für die verbleibende ungedeckte Menge eine geplante Einkaufsbestellung an.

    ![Bedarfsverursacherinformation für die geplante Einkaufsbestellung](media/pegging-planned-purchase-order.png "Bedarfsverursacherinformation für die geplante Einkaufsbestellung")

1. Wählen Sie die Bedarfsposition *Auftrag* aus und überprüfen Sie dann auf dem Inforegister **Bedarfsverursacher** die Bedarfe, die diese Nachfrage abdecken. Dort sollten die folgenden Zeilen erscheinen.

    | Referenz | Bedarfsmenge | Abgedeckte Menge |
    |---|---|---|
    | Bestand | 10.00 | 10.00 |
    | Geplante Einkaufsbestellungen | 15.00 | 15.00 |

    ![Bedarfsverursacherinformation für den Auftrag](media/pegging-planned-purchase-order.png "Bedarfsverursacherinformation für den Auftrag")

> [!NOTE]
> Da die Planungsoptimierung einige Funktionen noch nicht unterstützt, sind die Bedarfstypen *Sicherheitslagerbestand* und *Abgelaufene Charge* nicht auf der Seite **Bedarfsverlauf** enthalten. Weitere Informationen finden Sie unter [Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md).
>
> Wenn Sie das integrierte Produktprogrammplanungsmodul verwenden, werden chargengesteuerte Produkte unterstützt. Bei chargengesteuerten Produkten wird der abgelaufene verfügbare Lagerbestand auf der Seite **Bedarfsverlauf** angezeigt, aber er ist nicht mit Bedarfsanforderungen verknüpft. Abgelaufene verfügbare Positionen dieses Typs werden als Bedarfspositionen *Abgelaufene Charge* auf der Seite **Bedarfsverlauf** angezeigt.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
