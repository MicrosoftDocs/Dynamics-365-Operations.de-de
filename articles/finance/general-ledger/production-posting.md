---
title: Buchung von Produktionsaufträgen
description: In diesem Thema finden Sie Informationen zu den verschiedenen Arten der Buchung von Produktionsaufträgen.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, ProjCategory, CostSheetDesigner
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: cd1b6c49e59f9480fd831ad5ff143033ca09792c
ms.sourcegitcommit: 5b55f2913e736d12e40c227bf3ce3a9abec815bd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2022
ms.locfileid: "8802992"
---
# <a name="production-postings"></a>Produktionsbuchungen

Dieses Thema informiert Sie über die verschiedenen Arten von Buchungen im Produktionsauftragsprozess.


## <a name="material-consumption"></a>Materialverbrauch

Materialien werden während der Produktion als verbraucht erfasst, wenn die Produktionskommissionierlistenerfassung gebucht wird. Damit werden Transaktionen erstellt, die den Lagerbestand abziehen. In den **Produktionsparametern** können Sie angeben, ob der Wert von Rohstoffen, die sich in Arbeit befinden (RIF genannt), im Sachkonto gebucht werden soll.

Der Wert von Rohstoffen in Arbeit (RIF) wird auf die Konten **Geschätzte Kosten für verbrauchte Materialien** und **Geschätzte Kosten für verbrauchte Materialien, RIF** gebucht. Der Prozess der Kommissionierliste für den Produktionsauftrag ist eine physische Aktualisierung der mit dem Produktionsauftrag verbundenen Transaktionen im Bestand. Wenn ein Produktionsauftrag als beendet registriert wird, werden die physischen Transaktionen storniert und die zugehörigen Bestandstransaktionen werden finanziell aktualisiert. Wenn das Endjournal gebucht wird, werden die Buchungsarten **Verbrauchskosten** und **Verbrauchskosten, RIF** verwendet.

Die Registerkarte **Produktion** auf der Seite **Bestandsbuchungsprofile** steuert, wie Produktionsaufträge im Hauptbuch gebucht werden. Dies wird verwendet, wenn das Feld **Sachkonto-Buchung** entweder auf **Artikel und Ressource** oder **Artikel und Kategorie** auf der Seite **Produktionssteuerungsparameter** festgelegt ist. 

Damit ein Erfassungsblatt für eine Kommissionierliste zu einem Fertigungsauftrag ins Hauptbuch gebucht werden kann, müssen folgende Bedingungen erfüllt sein:

-   Das Kontrollkästchen **Kommissionierliste im Sachkonto buchen** muss auf der Seite **Produktionssteuerungsparameter** aktiviert werden. Diese Einstellung kann für einen bestimmten Standort auf der Seite **Produktionssteuerungsparameter nach Standort** außer Kraft gesetzt werden.
-   Das Ankreuzfeld **Physikalischen Bestand buchen** muss auf der Seite **Artikelmodellgruppen** für den in der Bestellzeile ausgewählten Artikel markiert sein.
-   Die Hauptkonten müssen auf der Seite **Bestandsbuchungsprofil** für folgende Buchungsarten angegeben werden:
    -   **Vorkalkulierte Kosten für verbrauchte Materialien**
    -   **Vorkalkulierte Kosten für verbrauchte Materialien, RIF**

## <a name="time-consumption"></a>Zeitaufwand

Die Zeit, die Arbeitskräfte für Aufträge in der Produktion aufwenden, wird im **Kartenjournal** oder im **Jobkartenjournal** erfasst. Wenn diese Erfassungen gebucht werden, wird die Sachkonto-Buchung auf ein spezielles Konto für Ressourcen, die sich in Arbeit befinden (RIF), verarbeitet. Diese Buchung repräsentiert den Wert der Zeit, die im Produktionsauftrag entlohnt wird. Nachdem der Produktionsauftrag als Fertig erfasst wurde, werden die RIF-Konten ausgeglichen.

Es gibt drei Möglichkeiten, den Zeitverbrauch zu buchen, je nachdem, welche Option im Feld **Sachkonto Buchung** auf der Seite **Produktionssteuerungsparameter** ausgewählt wurde.

## <a name="reporting-finished-goods-and-error-quantities"></a>Berichterstellungsendprodukte und -Ausschussmengen

Wenn ein Produktionsauftrag **Als fertiggestellt** gemeldet wird, werden die fertigen Waren, die fertiggestellt wurden, im Bestand über die **Als fertiggestellt** Erfassung aktualisiert. Wenn Sie die RIF-Buchhaltung verwenden, wird eine Sachkonto-Erfassung gebucht, um die RIF-Konten zu reduzieren und den Bestand der fertigen Waren zu erhöhen. Die Erfassung im Journal verwendet die Standardkosten, die für das Produkt definiert wurden. Wenn die Option **Geschätzten Einstandspreis verwenden** auf der Seite **Produktionssteuerungsparameter** ausgewählt ist, werden die geschätzten Kosten aus dem Produktionsauftrag verwendet.

Der Wert der Rohmaterialien in Arbeit (RIF) wird auf die Konten **Geschätzte Herstellkosten** und **Geschätzte Herstellkosten, RIF** gebucht. Der **Bericht als erledigt** Prozess für den Produktionsauftrag ist eine physische Aktualisierung der Bestandstransaktionen, die mit dem Produktionsauftrag zusammenhängen. Wenn ein Produktionsauftrag beendet wird, werden die physischen Transaktionen storniert und die zugehörigen Bestandstransaktionen werden finanziell aktualisiert. Wenn das Endjournal gebucht wird, werden die Buchungsarten **Herstellungskosten** und **Herstellungskosten, RIF** verwendet.

Die Registerkarte **Produktion** auf der Seite **Bestandsbuchungsprofile** dient als Steuerelement für die Buchung von Produktionsaufträgen im Hauptbuch. Dies wird verwendet, wenn das Feld **Sachkonto-Buchung** entweder auf **Artikel und Ressource** oder **Artikel und Kategorie** auf der Seite **Produktionssteuerungsparameter** festgelegt ist. Das Inforegister **Sachkonto** auf der Seite **Produktionsgruppen** kann auch zur Steuerung von Buchungen für Produktionsaufträge verwendet werden, wenn das Feld auf **Produktionsgruppen** festgelegt ist.

Damit eine **Erfassung als fertig** im Hauptbuch für einen Produktionsauftrag gebucht werden kann, müssen die folgenden Bedingungen erfüllt sein:
-   Das Kontrollkästchen **Bericht als erledigt im Ledger buchen** muss auf der Seite **Produktionssteuerungsparameter** markiert sein. Diese Einstellung kann für einen bestimmten Standort auf der Seite **Produktionssteuerungsparameter nach Standort** außer Kraft gesetzt werden.
-   Das Ankreuzfeld **Physikalischen Bestand buchen** muss auf der Seite **Artikelmodellgruppen** für den in der Bestellzeile ausgewählten Artikel markiert sein.
-   Die Hauptkonten müssen auf der Seite **Bestandsbuchungsprofil** für die folgenden Buchungsarten angegeben werden:
    -   **Vorkalkulierte Fertigungskosten**
    -   **Vorkalkulierte Fertigungskosten, RIF**

## <a name="ending-the-production-order"></a>Den Produktionsauftrag beenden

Bevor ein Produktionsauftrag beendet wird, werden die Istkosten für die produzierte Menge berechnet. Alle vorkalkulierten Material-, Arbeits- und Gemeinkosten werden storniert und durch die Istkosten ersetzt. Die Gesamtkosten des fertigen Artikels werden vom Konto **Herstellkosten** abgebucht und dem Konto **Herstellkosten, RIF** gutgeschrieben. Die Materialien, die während des Produktionsauftrags verbraucht wurden, werden dem Konto **Verbrauchte Materialkosten** gutgeschrieben und dem Konto **Materialkosten, RIF** belastet.

Wenn Sie beim Ausführen der Nachkalkulation das Kontrollkästchen **Auftrag beenden** aktivieren, wird der Status des Produktionsauftrags auf **Beendet** geändert. Mit diesem Status wird sichergestellt, dass für einen abgeschlossenen Produktionsauftrag keine weiteren Kosten mehr gebucht werden können. Sie können festlegen, dass der Wert von Fehlermengen, die als fertig gemeldet werden, den Warenmengen, die als fertig gemeldet werden, zugeordnet werden soll. Alternativ können Sie auch festlegen, dass der Wert von Fehlermengen auf ein spezielles Ausschusskonto gebucht wird. 

Um ein bestimmtes Sammelkonto anzugeben, folgen Sie diesen Schritten:
1.  Gehen Sie zu **Produktionssteuerung** > **Einrichtung** > **Produktionssteuerungsparameter**.
2.  Wählen Sie die Registerkarte **Standardaktualisierung**.
3.  Im Feld **Ausschussmethode** wählen Sie **Ausschusskonto**.
4.  Wählen Sie im Feld **Ausschusskonto** das Hauptkonto aus, auf das der Ausschuss für die Fehlermenge gebucht werden soll, wenn der Produktionsauftrag beendet wird. Wählen Sie zum Beispiel ein Aufwandskonto wie 510380: Produktionsschrott.

Damit das Endjournal im Hauptbuch für einen Produktionsauftrag gebucht werden kann, müssen die folgenden Bedingungen erfüllt sein:
-   Die Hauptkonten müssen auf der Seite **Bestandsbuchungsprofil** oder **Produktionsgruppen** für die folgenden Buchungstypen angegeben werden:
    -   **Kosten für verbrauchte Materialien**
    -   **Kosten für verbrauchte Materialien, RIF**
    -   **Fertigungskosten**
    -   **Fertigungskosten, RIF**
-   Die Hauptkonten müssen auf der Seite **Kostenkategorien**, **Ressourcen** oder **Ressourcengruppen** für die folgenden Typen angegeben werden:
    -   **Nachkalkulation von Herstellungskosten**
    -   **Verbrauchte Fertigungskosten, RIF**

## <a name="indirect-costs-for-production-orders"></a>Indirekte Kosten für Produktionsaufträge

Wenn Sie Transaktionen für einen Produktionsauftrag verarbeiten, können Sie indirekte Kosten konfigurieren, um Gemeinkosten oder zusätzliche Gebühren in Ihrem Hauptbuch zu erfassen. Physische Transaktionen für indirekte Kosten werden im Bestand erfasst, wenn Sie ein Kommissionierlisten-Journal oder einen Bericht als fertiges Journal buchen. Finanzielle Transaktionen für indirekte Kosten werden bei der Erfassung des Endjournals im Bestand erfasst.

Sie können indirekte Kosten für Ihren Zeitverbrauch im Zusammenhang mit **Routenkarte** Erfassungen oder **Projektkarte** Erfassungen anerkennen. Diese Transaktionen werden storniert und auf die Finanzkonten gebucht, wenn Sie den Produktionsauftrag beenden. Weitere Informationen finden Sie unter [Nachkalkulationsbögen](/supply-chain/cost-management/costing-sheets.md).

## <a name="controlling-the-level-of-ledger-posting"></a>Steuern der Ebene der Sachkontobuchung

Auf der Seite **Parameter für das Steuerelement Produktion** können Sie über das Feld **Sachkonto-Buchung** die Ebene der Sachkonto-Buchung für Produktionsprozesse festlegen. 

Folgende Felder sind verfügbar:

### <a name="item-and-resource"></a>Artikel und Ressource

Wenn Sie die Option **Artikel und Ressource** im Feld **Sachkonto-Buchung** wählen, stammen die Buchungskonten aus der Ressource oder der Ressourcengruppe zum Vorgang in der Route. Konten auf der spezifischen Ressource sind die erste Buchungsoption. Wenn kein Konto angegeben ist, werden die in der Ressourcengruppe angegebenen Konten verwendet. Für jede Zeile eines Vorgangs in einer Route kann eine Ressource als **Kalkulationsressource** angegeben werden. Diese Ressource wird für die Bestimmung des zu verwendenden Kontos verwendet. Diese Option wird allgemein verwendet, wenn eine Organisation den Ressourcen Betriebskosten zuordnet. Die Nachkalkulationen sind oft höher für die Ressourcen und dienen als Entscheidungshilfe bei der Entscheidung „Make versus Buy“. Dies ist die detaillierteste Buchungskonfiguration und lässt die genaueste Steuerung der Buchungen und sehr detaillierte Analysen des Produktionsprozesses zu.

### <a name="item-and-category"></a>Artikel und Kategorie

Wenn Sie die Option **Artikel und Kategorie** im Feld **Nachkalkulation** auswählen, kommen die Nachkalkulationen von der Seite **Kostenkategorie**, die sich auf jede Zeile der Route bezieht. Jede Vorgangszeile in der Route kann drei Nachkalkulationen haben: **Einrichtung** Zeit, **Ausführen** Zeit und die **Menge**. Diese Option wird allgemein verwendet, wenn das Hauptaugenmerk Ihrer Organisation auf Prozesseffizienz und Aktivitätsdauer liegt. Bei dieser Option handelt es sich um eine zusammenfassendere Art der Nachkalkulation, die dennoch eine Möglichkeit bietet, die Kosten in Kategorien zu gruppieren.

### <a name="production-group"></a>Produktionsbuchungsprofil

Wenn Sie die Option **Produktionsgruppen** im Feld **Buchungsgruppe** wählen, stammen die Buchungskonten von der Seite **Produktionsgruppen**. **Produktionsgruppen** werden in der Regel verwendet, wenn mehr als eine Produktionslinie ähnliche Produkte ausführt oder über ähnliche Ausrüstung verfügt. Sie können diese Option nutzen, um die Kosten zwischen zwei verschiedenen Produktionsgruppen zu vergleichen.  
  
> [!NOTE]
> Wenn die Standardmethode zur Berechnung der Nachkalkulation des fertigen Artikels verwendet wird, spiegeln die endgültigen Transaktionen dies wider. Wenn die tatsächlichen Kosten und die nach der Standardmethode berechneten Kosten voneinander abweichen, werden die Differenzen auf das Konto gebucht, das Gewinn oder Verlust ausweist.

### <a name="route-groups-and-ledger-posting"></a>Routengruppen und Sachkonto-Buchung

Für jede Zeile eines Vorgangs in einer Route kann eine **Routengruppe** angegeben werden. Die Felder **Einrichtungszeit**, **Laufzeit** und **Menge** in der Gruppe **Routengruppe** auf der Seite **Schätzung und Erfassung** dienen zur Steuerung, ob die Zeit für die Nachkalkulation bei der Buchung einer **Jobkarte** oder eines **Routenkarten-Journals** auf dem Produktionsauftrag verwendet werden soll. Wenn die Optionen deaktiviert sind, wird im Hauptbuch kein Beleg für den Zeitverbrauch erstellt.

Damit ein **Streckenkarte** oder **Journal für Erfassungen** im Hauptbuch für einen Produktionsauftrag gebucht werden kann, müssen die folgenden Bedingungen erfüllt sein:

-   Das Feld **Einrichtungszeit**, **Laufzeit** oder **Menge** muss in der Gruppe **Schätzung und Nachkalkulation** auf der Seite **Routengruppe** ausgewählt werden.
-   Die Hauptkonten müssen entweder auf der Seite **Kostenkategorie**, **Strecke**, **Streckengruppe** oder **Produktionsgruppen** für die folgenden Buchungsarten angegeben werden:
    -   Vorkalkulierte absorbierte Produktionskosten
    -   Vorkalkulierte, verbrauchte Fertigungskosten, RIF

Das folgende Diagramm zeigt die Beziehung der Routengruppe zur Berechnung der Gesamtkosten für jeden Vorgang (Routenzeile) in einer bestimmten Route. Jede Zeile hat eine Routengruppe. Die Routengruppe steuert die Parameter für die Einrichtungszeit, die Ausführungszeit und die Menge. Die Registerkarte **Kostenart** enthält drei Optionen für **Einrichtung**, **Ausführen** und **Menge**, die auf der Grundlage der Einstellung für Routengruppen aktiviert werden. Das Inforegister **Timings** enthält drei Felder, die auf der Routengruppe basieren.

Die Formel, die verwendet wird, basiert darauf, ob die Option in der Routengruppe aktiviert ist. Die Kosten aus der gewählten Kostenkategorie werden mit der Menge multipliziert, die in den Timings eingegeben wurde, um die Gesamtkosten zu berechnen.

:::image type="complex" source="media/RouteGroupRelationship.png" alt-text="Das Verhältnis von Routengruppen zu den kalkulierten Gesamtkosten":::
Das Verhältnis von Routengruppen zu den kalkulierten Gesamtkosten. Jede Zeile hat eine Routengruppe. Die Routengruppe steuert die Parameter für Einrichtungszeit, Ausführungszeit und Menge. Die Registerkarte Kostenkategorie enthält drei Optionen für die Einrichtung, das Ausführen und die Menge, die auf der Grundlage der Einstellung für die Routengruppen aktiviert werden. Das Inforegister Zeitangaben verfügt über drei Felder, die auf der Grundlage der Routengruppe aktiviert und nachkalkuliert werden. Die Formel, die verwendet wird, basiert darauf, ob die Option in der Routengruppe aktiviert ist. Die Kosten aus der ausgewählten Kostenkategorie werden mit der Menge multipliziert, die in den Zeitangaben angegeben ist, um die Gesamtkosten zu berechnen.
:::image-end:::

## <a name="sample-posting-profile-configuration"></a>Beispiel für die Konfiguration eines Buchungsprofils

Die folgende Tabelle zeigt Beispiele für die Standardbuchungsarten mit beispielhaften Hauptkonten und Beschreibungen. 

 - Die Spalte **Soll/Haben** zeigt an, ob die Transaktion typischerweise Soll oder Haben oder in manchen Fällen beides buchen kann. 
 - Die Spalte **Verrechnungskonto** zeigt an, ob die Buchungsart ein Verrechnungskonto ist. Der auf diesem Konto gebuchte Betrag wird automatisch storniert, wenn eine spätere Transaktion gebucht wird. 
 - Bei der Spalte **P/F** steht **P** für physische Buchungen und **F** für Finanzbuchungen. 
 - Die Spalte **Follow** zeigt an, ob das Hauptkonto für eine bestimmte Buchungsart typischerweise mit einer anderen Buchungsart identisch ist. Der Wert in der Spalte gibt die Buchungsart an, die normalerweise verwendet wird.

> [!NOTE]
> Die vorgeschlagenen Hauptkonten und Hauptkontonamen sind Vorschläge. Wir empfehlen Ihnen, mit Ihrem Buchhalter zusammenzuarbeiten, um die beste Konfiguration für Ihre geschäftlichen Anforderungen zu ermitteln.


| Buchungstyp  | Hauptkontobeispiel | Hauptkonto-Namenbeispiel| Kontotyp | Soll/Haben? | Clearingkonto | Physisch oder wertmäßig | Folgen | Description |
|---------------|----------------------|--------------------------|--------------|----------------|------------------|-----------------------|--------|------------|
| Vorkalkulierte Kosten für verbrauchte Materialien      | 140100               | Materialbestand        | Anlage        | Gutschrift         | Y                | P                     | Kosten für verbrauchte Materialien                | Dieses Konto wird verwendet, wenn Sie ein Erfassungsjournal für eine Kommissionierliste für einen Produktionsauftrag buchen. Die Gegenbuchung zu diesem Konto sind die geschätzten Materialkosten, RIF. Der Betrag auf diesem Konto wird automatisch storniert, wenn der Produktionsauftrag beendet wird. Dieses Konto stellt das Bestandskonto in der Bilanz dar.       |
| Vorkalkulierte Kosten für verbrauchte Materialien, RIF | 150150               | Produktion RIF - Materialien | Anlage        | Belastung          | Y                | P                     | Vorkalkulierte Fertigungskosten, RIF          | Dieses Konto wird verwendet, wenn Sie ein Erfassungsjournal für eine Kommissionierliste für einen Produktionsauftrag buchen. Die Gegenbuchung zu diesem Konto sind die geschätzten Kosten für verbrauchte Materialien. Der Betrag auf diesem Konto wird automatisch storniert, wenn ein Produktionsauftrag beendet wird. Dieses Konto stellt das RIF in Ihrer Bilanz dar.                  |
| Vorkalkulierte Fertigungskosten               | 140200               | Bestand an fertigen Waren   | Anlage        | Belastung          | Y                | P                     | Fertigungskosten                         | Dieses Konto wird verwendet, wenn Sie einen Bericht als fertiges Journal für einen Produktionsauftrag buchen. Die Gegenbuchung zu diesem Konto sind die geschätzten Herstellkosten, RIF. Der Betrag auf diesem Konto wird automatisch storniert, wenn der Produktionsauftrag beendet wird. Dieses Konto stellt das Bestandskonto in der Bilanz dar. |
| Vorkalkulierte Fertigungskosten, RIF          | 150150               | Produktion RIF - Materialien | Anlage        | Gutschrift         | Y                | P                     | Fertigungskosten, RIF                    | Dieses Konto wird verwendet, wenn Sie einen Bericht als fertiges Journal für einen Produktionsauftrag buchen. Die Gegenbuchung zu diesem Konto sind die geschätzten Herstellkosten. Der Betrag auf diesem Konto wird automatisch storniert, wenn ein Produktionsauftrag beendet wird. Dieses Konto stellt das RIF in Ihrer Bilanz dar.                     |
| Kosten für verbrauchte Materialien                | 140100               | Materialbestand        | Anlage        | Gutschrift         | N                 | Fr                     | Vorkalkulierte Kosten für verbrauchte Materialien      | Dieses Konto wird verwendet, um die Materialien zu verbuchen, die bei der Beendigung des Produktionsauftrags verbraucht werden. Die Gegenbuchung zu diesem Konto ist die Nachkalkulation für verbrauchte Materialien, RIF.                                                                                                    |
| Kosten für verbrauchte Materialien, RIF           | 150150               | Produktion RIF - Materialien | Anlage        | Belastung          | N                 | Fr                     | Vorkalkulierte Kosten für verbrauchte Materialien, RIF | Dieses Konto wird verwendet, um die Materialien im RIF zu erfassen, die bei der Beendigung des Produktionsauftrags verbraucht werden. Die Gegenbuchung zu diesem Konto sind die verbrauchten Materialkosten.                                                |
| Fertigungskosten                         | 140200               | Bestand an fertigen Waren   | Anlage        | Belastung          | N                 | Fr                     | Vorkalkulierte Fertigungskosten               | Dieses Konto wird verwendet, um die Kosten für die fertige Ware zu erfassen, die durch einen Produktionsauftrag hergestellt wird, wenn Sie den Produktionsauftrag beenden. Die Gegenbuchung zu diesem Konto ist das Konto Herstellkosten, RIF.                                                                  |
| Fertigungskosten, RIF                    | 150150               | Produktion RIF - Materialien | Anlage        | Gutschrift         | N                 | Fr                     | Vorkalkulierte Fertigungskosten, RIF          | Dieses Konto wird verwendet, um die Kosten für die fertige Ware im RIF zu erfassen, die durch einen Produktionsauftrag produziert wird, wenn Sie den Produktionsauftrag beenden. Die Gegenbuchung zu diesem Konto ist das Konto Herstellkosten.                                     |

> [!NOTE]
> Der **Magerer RIF-Eingang** und das **Magerer RIF-Verrechnungskonto** werden mit der Nachkalkulation für die schlanke Fertigung eingesetzt. Weitere Informationen finden Sie unter [Nachkalkulation](/supply-chain/cost-management/backflush-costing.md).

