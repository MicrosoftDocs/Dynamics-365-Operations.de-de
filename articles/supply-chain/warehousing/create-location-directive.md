---
title: Lagerplatzrichtlinien erstellen
description: In diesem Thema wird erläutert, wie Lagerplatzrichtlinien erstellt werden. Lagerplatzrichtlinien sind benutzerdefinierte Regeln, die dabei helfen, Entnahme- und Einlagerungslagerorte für die Lagerortumlagerung zu identifizieren.
author: Mirzaab
manager: tfehr
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-28
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 4f634b7f526fd198b394af6d3870c43ee560813e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016769"
---
# <a name="create-location-directives"></a>Lagerplatzrichtlinien erstellen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Lagerplatzrichtlinien erstellt werden. Lagerplatzrichtlinien sind benutzerdefinierte Regeln, die dabei helfen, Entnahme- und Einlagerungslagerorte für die Lagerortumlagerung zu identifizieren. In einer Auftragsbuchung bestimmt eine Lagerplatzrichtlinie beispielsweise, wo die Artikel entnommen und wo sie eingelagert werden.

> [!NOTE]
> Dieses Thema gilt für Funktionen im Modul **Lagerortverwaltung**. Es gilt nicht für Funktionen im Modul [Bestandsverwaltung](../inventory/inventory-home-page.md).

Sie können mit Lagerplatzrichtlinien folgende Aufgaben durchführen:

- Einlagern eingehender Artikel
- Entnahme und Phaseneinteilung für Artikel für ausgehende Buchungen
- Entnahme und Einlagerung von Rohmaterial für die Produktion
- Auffüllen von Lagerplätzen

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie eine Standortanweisung erstellen können, müssen Sie diese Schritte ausführen, um sicherzustellen, dass die Voraussetzungen erfüllt sind.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerorte**.
1. Erstellen Sie einen Lagerort.
1. Setzen Sie auf dem Inforegister **Lagerort** die Option **Lagerortverwaltungsprozesse verwenden** auf *Ja*.
1. Erstellen Sie Lagerplätze, Lagerplatztypen, Lagerplatzprofile und Lagerplatzformate. Weitere Informationen finden Sie unter [Konfigurieren von Standorten in einem WMS-aktivierten Lagerort](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Erstellen Sie Standorte, Zonen und Zonengruppen. Weitere Informationen finden Sie unter [Einrichten eines Lagerorts](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) und [Konfigurieren von Standorten an einem WMS-aktivierten Lagerort](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="setup"></a>Setup

### <a name="create-location-directives"></a>Lagerplatzrichtlinien erstellen

Gehen Sie folgendermaßen vor, um eine Lagerplatzrichtlinie zu erstellen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Legen Sie im Listenbereich für das Feld **Arbeitsauftragstyp** den Typ der Lagerbuchung fest, für den Sie eine Lagerplatzrichtlinie erstellen.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Lagerplatzrichtlinie zu erstellen.
1. Legen Sie für die neue Lagerplatzrichtlinie die Felder wie in der folgenden Tabelle beschrieben fest.

    | Feld | Beschreibung |
    |---|---|
    | Laufende Nummer | Geben Sie eine Ganzzahl für die Sequenzposition der Lagerplatzrichtlinie an. Folgepositionen bestimmen, wann die einzelnen Lagerplatzrichtlinien für den ausgewählten Arbeitsauftragstyp verarbeitet wird. |
    | Name | Geben Sie einen Namen für die Lagerplatzrichtlinie ein. | 
    | Arbeitstyp | Wählen Sie die Art der auszuführenden Arbeit aus. Die Liste der Werte basiert auf dem Typ der Lagerbuchung, den Sie im Feld **Arbeitsauftragstyp** ausgewählt haben. Folgende Werte können verfügbar sein:<ul><li>**Einlagern** – Mit der Standortrichtlinie wird versucht, den bestmöglichen Lagerplatz zu finden, um Bestand einzulagern oder zu suchen, der durch Eingangs-, Produktions- oder Bestandsanpassungen in das System gelangt. Über die Lagerplatzrichtlinie wird auch der Ort für die Lagerung an einem bestimmten Platz oder die endgültige Versandort im ausgehenden Fluss definiert.</li><li>**Entnehmen** – Mit der Standortrichtlinie wird versucht, die besten Standorte zu finden, an denen Bestand physisch reserviert werden kann (Arbeitsaufträge erstellen). Die Entnahme kann abgeschlossen werden (Entnahmearbeitsposition kann also geschlossen werden), auch wenn die Arbeit nicht abgeschlossen ist. Der Benutzer kann die physische Entnahme durchführen. Im System ist diese Aktion ein Entnahmeschritt. Der Benutzer kann dann die Arbeit auf dem mobilen Gerät abbrechen und die Arbeit (zum Beispiel Einlagern) später durchführen. Allerdings wird die Arbeitskopfzeile geschlossen, wenn die letzte Einlagerung abgeschlossen ist.</li><li>**Inventur** , **Anpassungen** , **Benutzerdefiniert** , **Bestandsstatusänderung** , **Ladungsträgererstellung** , **Drucken** , **Statusänderung** und **Zu verschachtelten Ladungsträgern packen** – Diese Werte können in keiner Lagerplatzdirektive verwendet werden.</li></ul> |
    | Standort | Wählen Sie den Standort aus, an dem die Arbeit abgeschlossen werden soll. |
    | Lagerort | Wählen Sie den Lagerplatzstandort aus, an dem die Arbeit durchgeführt werden soll. |
    | Richtliniencode | Wählen Sie einen Anweisungscode aus, um die Auswahl der Standortanweisungen zu steuern, die sich auf die Arbeitsvorlageneinfügelinien beziehen, denen dieser Code zugewiesen ist. Auf der Seite **Richtliniencode** können Sie neue Codes erstellen, mit denen eine Arbeitsvorlage mit einer Lagerplatzrichtlinie verbunden werden kann. Sie können mit dieser Seite auch die Verknüpfung zwischen einer Arbeitsvorlagenposition und einer Lagerplatzrichtlinie festlegen (zum Beispiel Frachttür oder Lagerplatz). Informationen zum Konfigurieren eines Richtliniencodes mit einer Arbeitsvorlage finden Sie in [Steuern des Lagerplatzes mithilfe von Arbeitsvorlagen und Lagerplatzrichtlinien](control-warehouse-location-directives.md).<p>Beachten Sie, dass bei festgelegtem Code das System die Lagerplatzdirektive nicht nach Nummernkreis suchen wird, wenn Arbeit erstellt wird, die Suche erfolgt nach Direktivencode. Das bedeutet, dass Sie in Bezug auf die Verwendung der Lagerplatzvorlage für einen bestimmten Schritt in einer Arbeitsvorlage wie die Bereitstellung von Material spezifischer sein können.</p> |
    | Dispositionscode | Wählen Sie einen Dispositionscode aus, um die Einlagerung empfangener Artikel zu einem Lagerplatz umzuleiten. (Weitere Informationen finden Sie unter [Dispositionscodes einrichten](tasks/set-up-dispositions-codes.md).) Dieses Feld ist nur verfügbar, wenn das Feld **Arbeitsauftragsart** auf *Bestellungen* , *Rücklieferungen* oder *Einlagerung von Fertigungserzeugnissen* eingestellt ist. |
    | Mehrfach-SKU | Legen Sie für diese Option *Ja* fest, wenn Sie mehrere Lagermengeneinheiten (SKUs) für einen Lagerplatz festlegen möchten. Diese Option muss beispielsweise für die Frachttür auf *Ja* gesetzt sein.<p>Wenn die Option **Mehrfach-SKU** auf *Ja* gesetzt ist, wird der Einlieferungslagerplatz in Arbeit angegeben (wie erwartet). Der Einlieferungslagerplatz kann mehrere Einlieferungen jedoch nur durchführen, wenn die Arbeit verschiedene SKUs enthält, die ausgewählt und eingeliefert werden müssen, und nicht, ob die Arbeit nur eine einzige SKU enthält, die eingeliefert werden muss.</p><p>Wenn die Option **Multiple SKU** auf *Nein* gesetzt ist, wird der Einlieferungsplagerplatz nur festgelegt, wenn nur ein SKU-Typ der Einlieferung vorhanden ist.</p><p>Um beide Ansätze zu verwenden, müssen Sie zwei Zeilen mit der gleichen Struktur und Einrichtung angeben, aber die Option **Mehrfach-SKU** für eine der Zeilen auf *Ja* und die andere auf *Nein* setzen. Zwei gleiche Lagerplatzanweisungen sind also für Einlagerungsvorgänge erforderlich, obwohl Sie in der Arbeits-ID nicht zwischen Einzel- und Mehrfach-SKUs unterscheiden müssen. Sie müssen außerdem einen Einlagerungsvorgang für die Entnahme einrichten, wenn Sie einen Auftrag mit mehreren Artikeln haben.</p><p>**Hinweis:** Wenn Sie die Option **Mehrfach-SKU** für eine Lagerplatzrichtlinie des Arbeitstyps auf *Einlagern* auf *Ja* setzen, wählt das System unabhängig von anderen Einschränkungen, die in den Zeilen erstellt wurden, immer die erste Zeile der Lagerplatzrichtlinie aus.</p> |

1. Optional: Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten** aus und legen Sie die Lagerorte fest oder bestimmen Sie Einschränkungen für die Auswahl einer bestimmten Lagerplatzrichtlinie.
1. Wählen Sie auf dem Inforegister **Positionen** eine oder mehrere Positionen, um Einheiten anzugeben und Mengen an einem Lagerort zu suchen oder zu reservieren.
1. Legen Sie auf jeder neuen Zeile die Felder wie in der folgenden Tabelle beschrieben fest.

    | Feld | Beschreibung |
    |---|---|
    | Laufende Nummer | Geben Sie eine Ganzzahl für die Sequenzposition der Lagerplatzrichtlinie an. Folgepositionen bestimmen, wann die einzelnen Lagerplatzrichtlinien für den ausgewählten Arbeitsauftragstyp verarbeitet werden. |
    | Von Menge | Definieren Sie den beginnenden Mengenbereich, für den der mittlere Rasternummernkreis ausgewählt werden soll. Geben Sie die Menge in der Maßeinheit an, die im Feld **Maßeinheit** ausgewählt ist. |
    | Bis Menge | Definieren Sie den abschließenden Mengenbereich, für den der mittlere Rasternummernkreis ausgewählt werden soll. Geben Sie die Menge in der Maßeinheit an, die im Feld **Maßeinheit** ausgewählt ist. |
    | Einheit | Hier wird die Maßeinheit für die Artikel ausgewählt.<p>Sie können eine Mindestmenge und eine Höchstmenge angeben, für die die Richtlinie gelten soll. Sie können auch festlegen, dass die Direktive für eine bestimmte Bestandseinheit verwendet werden soll. Das Feld **Einheit** wird nur für Mengenbewertungen verwendet.</p><p>Um festzustellen, ob eine Standortrichtlinie gilt, wertet das System die Mengen mithilfe des Werts von **Einheit** aus, der in der Zeile angegeben ist. Beim Verwenden einer Lagerplatzrichtlinienposition versucht das System, die Bedarfseinheit in die Einheit zu konvertieren, die auf der Position angegeben wird. Wenn die Einheitenumrechnung nicht vorhanden ist, fährt das System mit der nächsten Position fort.</p> |
    | Menge suchen | Dieses Feld ist nur gültig, wenn Sie versuchen, eine Menge im Lager zu finden oder einzulagern. Mit anderen Worten, es ist nur für *Einlagerungen* relevant. Wählen Sie die Methode aus, mit der ausgewertet wird, ob sich die Menge in dem Bereich befindet, der in den Feldern **Von Menge** und **Nach Menge** festgelegt ist. Wenn die Lagerplatzrichtlinie für eine eingehende Buchung gilt, wählen Sie eine der folgenden Optionen aus:<ul><li>**Ladungsträgermenge** – Beim Auswerten, ob eine Menge im Zielmengenbereich liegt, verwenden Sie die Menge auf dem empfangenen Ladungsträger.</li><li>**Vereinheitlichte Menge** – Beim Auswerten, ob eine Menge im Zielmengenbereich liegt, nutzen Sie die Menge, die bei der Transaktion vereinheitlicht wurde. Wenn Sie an einem Lagerort z. B. eine Menge von 1000 empfangen und diese in 10 Ladungsträger von jeweils 100 unterteilen können, können Sie eine Menge von 1000 Artikeln anstelle der Ladungsträgermenge von 100 verwenden.</li><li>**Restliches Menge** – Beim Auswerten, ob eine Menge im Zielmengenbereich liegt, nutzen Sie die verbleibende Menge, die von der Bestellposition empfangen wird, die gerade geprüft wird.</li><li>**Erwartete Menge** – Beim Auswerten, ob eine Menge im Zielmengenbereich liegt, nutzen Sie die Gesamtmenge der Bestellposition unabhängig von der Menge, die bereits empfangen wurde.</li></ul> |

1. Optional: Im Inforegister **Positionen** können Sie die folgenden zusätzlichen Felder festlegen.

    | Feld | Beschreibung |
    |---|---|
    | Nach Einheit einschränken | Aktivieren Sie dieses Kontrollkästchen, um die Maßeinheiten einzuschränken, die als gültige Auswahlkriterien für die Lagerplatzrichtlinien gelten. Wenn Maßeinheiten angegeben wurden, werden nur Positionen als gültig für die Positionsauswahl betrachtet, bei denen die Einheit mit mindestens einer Einheit übereinstimmt, die für die Einheitsnummernkreisgruppe definiert ist.<p>Beispielsweise ist die Einheit auf Paletten beschränkt und der Artikel ist einer Einheitensequenzgruppe zugeordnet, die die Einheit *Paletten* enthält. In diesem Fall werden die Artikel als gültige Option für die Lagerplatzrichtlinie betrachtet.</p><p>Das Kontrollkästchen **Nach Einheiten einschränken** bestimmt nicht die Einheit oder Einheiten, die auf Arbeitspositionen angewendet werden. Die Einheitsbeschränkung gilt nur für die Einheiten, die über die Einheitsnummernkreisgruppe verfügbar gemacht werden.</p><p>Zum Beispiel wird eine Position mit einer Einheitsnummernkreisgruppe verknüpft, die die Einheiten *Paletten* und *Stk.* enthält. Es wurde eine Maßeinheit definiert, in der 1 Palette = 100 Stück ist, und die Lagerplatzrichtlinie verwendet die Funktion **Nach Einheit einschränken** nur für Paletten. Außerdem wurde eine Arbeitsvorlage definiert, die die Erstellung der Arbeitskopfzeile auf 50 Stück begrenzt. In diesem Fall werden Arbeitspositionen mit 50 Stück erstellt.</p><p>Führen Sie die folgenden Schritte aus, um die Maßeinheit für die Einschränkung anzugeben</p><ol><li>Wählen Sie auf dem Inforegister **Positionen** die Option **Nach Einheit einschränken** aus. Diese Schaltfläche wird erst verfügbar, nachdem Sie das Kontrollkästchen **Nach Einheit einschränken** in der Position und dann **Sparen** ausgewählt haben.</li><li>Wählen Sie im Feld **Einheit** die Maßeinheit, nach der beschränkt werden soll, für die Erfassungs- und Einlagerungsabläufe aus.</li></ol> |
    | Aufrunden zur Einheit | Wählen Sie diese Option aus, um festzulegen, dass die Rohmaterialentnahme auf ein Vielfaches der Handhabungseinheit aufgerundet wird, wie im Feld **Nach Einheit einschränken** angegeben. Dieses Feld gilt nur für Rohmaterialentnahme und Lagerplatzrichtlinien des Typs *Entnehmen*. |
    | Verpackungsmenge suchen | Aktivieren Sie dieses Kontrollkästchen, wenn eine Verpackungseinheitenmenge auf der Seite **Auftrag** angegeben ist. Wenn Sie dieses Kontrollkästchen aktivieren, werden nur die Standorte mit dieser Verpackungseinheitenmenge ausgewählt. |
    | Aufteilung zulassen | Aktivieren Sie dieses Kontrollkästchen, um die Menge auf mehrere Lagerplätze aufzuteilen. |
    | Vorlage für sofortige Wiederbeschaffung | Erstellen Sie eine Verbindung mit einer Wiederbeschaffungsvorlage, damit die Wiederbeschaffung sofort gestartet wird, wenn Artikel nicht zugewiesen sind. Wenn das Feld leer gelassen wird, beginnt die Artikelauffüllung erst, wenn alle Positionen der Lagerplatzrichtlinie verarbeitet wurden.<p>Dieses Feld ist nur für ausgewählte Arbeitsauftragstypen verfügbar, für die Nachschub zulässig ist, z. B. *Aufträge* und *Rohmaterialentnahme*.</p> |

1. Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus und legen Sie den Lagerplatz oder den Bereich von Lagerplätzen fest.
1. Das Feld **Laufende Nummer** zeigt die Reihenfolge an, in der die Feld zeigt die Reihenfolge an, in der die Lagerplatzrichtlinie für den ausgewählten Arbeitstyp verarbeitet wird. Sie können die Reihenfolge ändern. Seien Sie jedoch vorsichtig mit laufenden Nummern für Aktionen mit Lagerplatzrichtlinien, da Aktionen mit Lagerplatzrichtlinien immer in dieser Reihenfolge ausgeführt werden.
1. Geben Sie im Feld **Name** den Namen der Lagerplatzrichtlinienaktion ein. Seien Sie genau, damit klar ist, was die Aktion ist.
1. Optional: Wählen Sie **Abfrage bearbeiten** aus, wenn Sie die Lagerort-Lagerplätze und andere Kriterien ändern möchten.
1. Optional: Sie können die folgenden zusätzlichen Felder für eine Lagerplatzrichtlinie festlegen.

    | Feld | Beschreibung |
    |---|---|
    | Verwendung fester Lagerplätze | Bestimmt, welche Lagerplätze die Lagerplatzrichtlinie berücksichtigen soll.<ul><li>**Feste und nicht feste Lagerplätze** – Die Lagerplatzrichtlinie berücksichtigt alle Lagerplätze.</li><li>**Nur feste Lagerplätze für das Produkt** – In der Lagerplatzrichtlinie werden nur feste Lagerplätze für Produkte berücksichtigt.</li><li>**Nur feste Lagerplätze für die Produktvariante** – In der Lagerplatzrichtlinie werden nur feste Lagerplätze für Produktvarianten berücksichtigt.</li></ul> |
    | Negativen Bestand zulassen | Aktivieren Sie dieses Kontrollkästchen, um einen negativen Bestand am angegebenen Lagerplatz zu ermöglichen. |
    | Charge aktiviert | Aktivieren Sie dieses Kontrollkästchen, um Chargenstrategien für die Artikel zu verwenden, für die Chargen aktiviert sind. Wenn dieses Kontrollkästchen aktiviert und das Feld **Strategie** auf *Keine* gesetzt ist, fährt das System mit der nächsten Aktivitätszeile fort. |
    | Strategie | Wählen Sie die Strategie aus, die von der Standortrichtlinie verwendet werden soll:<ul><li>**Keine** – Es wird keine Strategie angewendet.</li><li>**Packmenge anpassen** – Mit dieser Strategie wird geprüft, ob ein Entnahmeort die angegebene Packmenge ermöglicht. Diese Strategie ist nur gültig, wenn das Feld **Arbeitstyp** auf *Entnehmen* gesetzt ist.</li><li>**Konsolidieren** – Mit dieser Strategie werden Artikel an einem bestimmten Lagerplatz konsolidiert, wenn ähnliche Artikel bereits verfügbar sind. Diese Strategie ist nur gültig, wenn das Feld **Arbeitstyp** auf *Einlagern* gesetzt ist. In einer typischen Einrichtung für Einlagern versucht das System eine Konsolidierung in der ersten Aktivitätsposition und dann, in der zweiten Aktionsposition, die Einlagerung ohne Konsolidierung. Durch Konsolidieren von Waren wird die spätere Entnahme effizienter.</li><li>**FEFO-Chargenreservierung** – Diese Strategie wird verwendet, wenn Bestand mithilfe eines Chargenablaufdatums zur Chargenreservierung zugeordnet wird. Die FEFO-Chargenreservierungsstrategie (First Expiry, First Out) wird auch verwendet, wenn Bestand mithilfe des Ablaufdatums und des Chargenmindesthaltbarkeitsdatums gesucht wird. Sie können diese Strategie nur für Artikel verwenden, die für Chargen aktiviert sind. Diese Strategie ist nur gültig, wenn das Feld **Arbeitstyp** auf *Entnehmen* gesetzt ist. Wenn Sie diese Strategie auswählen, überschreiben Sie alle Abfragesortierungen für angewendete Chargennummern.</li><li>**Auf vollständige LP aufrunden** – Diese Strategie rundet die Bestandsmenge auf, sodass sie der Ladungsträgermenge entspricht, die den zu entnehmenden Artikeln zugewiesen ist. Diese Strategie kann nur für Wiederbeschaffungstypen von Lagerplatzrichtlinien verwendet werden, und auch nur dann, wenn das Feld **Arbeitstyp** auf *Entnehmen* gesetzt ist.</li><li>**Leerer Lagerplatz ohne eingehende Arbeit** – Diese Strategie wird verwendet, um leere Lagerplätze zu suchen. Ein Lagerplatz wird als leer angesehen, wenn er keinen physischen Bestand und keine erwartete eingehende Arbeit hat. Diese Strategie ist nur gültig, wenn das Feld **Arbeitstyp** auf *Einlagern* gesetzt ist.</li></ul> |

## <a name="example-of-the-use-of-location-directives"></a>Beispiel für die Verwendung von Lagerplatzrichtlinien

Im vorliegenden Beispiel berücksichtigen wir einen Bestellprozess, in dem die Lagerplatzrichtlinie die freie Kapazität innerhalb eines Lagerorts für Lagerartikel finden muss, die gerade an der empfangenden Rampe erfasst wurden. Zuerst müssen Sie die freie Kapazität am Lagerort finden, indem der vorhandene verfügbare Lagerbestand konsolidiert wird. Falls die Konsolidierung nicht möglich ist, wird ein leerer Lagerplatz gesucht.

Für dieses Szenario müssen zwei Lagerplatzrichtlinien-Aktivitäten definiert werden. Die erste Aktivität in der Folge muss die Strategie **Konsolidieren** verwenden, die zweite sollte die Strategie **Leerer Lagerplatz ohne eingehende Arbeit** verwenden. Wenn Sie keine dritte Aktivität definieren, um ein Überlaufszenario zu behandeln, sind zwei Ergebnisse möglich, wenn es keine Kapazität mehr am Lagerort gibt: Arbeit kann erstellt werden, auch wenn keine Lagerplätze definiert sind, oder der Arbeitserstellungsprozess kann fehlschlagen. Das Ergebnis wird durch die Einstellung auf der Seite **Lagerplatzrichtlinienfehler** bestimmt, auf der Sie entscheiden, ob die Option **Arbeit bei Lagerplatzrichtlinienfehler anhalten** für jeden Arbeitsauftragstyp auswählt wird.

## <a name="next-step"></a>Nächster Schritt

Wenn Sie Lagerplatzrichtlinien erstellt haben, können Sie jeden Richtliniencode zu einem Arbeitsvorlagencode zur Arbeitserstellung zuordnen. (Weitere Informationen finden Sie unter [Steuern von Lagerarbeit mithilfe von Arbeitsvorlagen und Lagerplatzrichtlinien](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).)

## <a name="technical-information-for-system-admins"></a>Technische Informationen für Systemadministratoren

Wenn Sie keinen Zugriff auf die Seiten für die Durchführung dieser Aufgabe haben, wenden Sie sich mit den Informationen aus der folgenden Tabelle an Ihren Systemadministrator.

| Kategorie | Voraussetzung |
|---|---|
| Konfigurationsschlüssel | Gehen Sie zu **Systemadministration \> Einrichten \> Lizenzkonfiguration**. Erweitern Sie den Lizenzschlüssel **Geschäft** und wählen Sie den Konfigurationsschlüssel **Lagerort und Transportverwaltung** aus. |
