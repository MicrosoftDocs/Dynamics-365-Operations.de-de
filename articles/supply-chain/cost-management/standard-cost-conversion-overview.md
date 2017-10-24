---
title: "Standardkostenumrechnung (Überblick)"
description: "Dieser Eintrag stellt eine Prozessübersicht bereit, die Sie beim Einrichten und Ausführen einer Standardkostenumrechnung unterstützt. Die aufgeführten Schritte werden ausgeführt, nachdem Sie die Voraussetzungen für eine Standardkostenumrechnung abgeschlossen haben."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 78212
ms.assetid: d601d9d5-1de3-4868-aff4-534dca01d624
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2e59fd6e137d5f677ed4055385ef88922c8c42ba
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="standard-cost-conversion-overview"></a>Standardkostenumrechnung (Überblick)

[!include[banner](../includes/banner.md)]


Dieser Eintrag stellt eine Prozessübersicht bereit, die Sie beim Einrichten und Ausführen einer Standardkostenumrechnung unterstützt. Die aufgeführten Schritte werden ausgeführt, nachdem Sie die Voraussetzungen für eine Standardkostenumrechnung abgeschlossen haben. 

Mit dem Formular **Standardkostenumrechnungen** wird das Lagermodell für eine Charge ausgewählter Artikel von einem tatsächlichen Nachkalkulationsansatz in einen Standardnachkalkulationsansatz umgerechnet. Der Umrechnungsprozess umfasst als Voraussetzung einen Lagerabschlusses, mehrere Schritte während einer Übergangsperiode, die durch ein Übergangsstartdatum und ein geplantes Umrechnungsdatum definiert ist, und dann das Ausführen der Umrechnung und eines zugehörigen Lagerabschlusses.

-   Lagerabschluss vor der Übergangsperiode − Ein Lagerabschluss stellt eine Voraussetzung dar, da dabei die offenen Buchungen eines Artikels mit der alten Bewertungsmethode ausgeglichen werden. Während der Übergangsperiode können rückdatierte Buchungen wie Rechnungen eingegeben und ausgeführt werden, um die vorherige Periode abzuschließen. Das Lagerabschlussdatum muss einen Tag vor dem Übergangsstartdatum liegen, um eine saubere Trennung von der alten Bewertungsmethode sicherzustellen.
-   Umrechnungsschritte während der Übergangsperiode − Verwenden Sie die Seite **Standardkostenumrechnungen**, um einen Umrechnungsdatensatz zu erstellen, der auch die benutzerdefinierte Kennung für eine neue Nachkalkulationsversion enthält. Sie bestimmen die Artikel, für die eine Umrechnung erforderlich ist, und geben dann die ausstehenden Standardkosten des Artikels in der neu erstellten Nachkalkulationsversion ein. Sie prüfen die ausgewählten Artikel, um Probleme zu erkennen, die eine Umrechnung verhindern könnten. Sie beheben die Probleme und führen dann eine weitere Prüfung aus. Wenn die Artikel erfolgreich alle Prüfungen durchlaufen haben, können Sie den Status des Umrechnungsdatensatzes in **Bereit** ändern. Führen Sie am geplanten Umrechnungsdatum die Umrechnung aus, und schließen Sie optional einen Lagerabschluss ein. Die Lagerumlagerungen eines Artikel während der Übergangsperiode werden gebucht und nach dem alten Lagermodell bewertet. Anschließend werden die Lagerumlagerungen nach Abschluss der Umrechnung neu in Standardkosten bewertet.
-   Lagerabschluss vor der Umrechnung − Der Lagerabschluss kann als Teil der Umrechnungsausführung am geplanten Umrechnungsdatum eingeschlossen oder vor der Umrechnung als separater Schritt ausgeführt werden.

Nach Abschluss der Umrechnung basiert das Lagermodell für jeden Artikel auf den Standardkosten, und die Standardkosten des Artikels sind aktiviert. Nachfolgende Lagerbuchungen werden zu den Standardkosten des Artikels bewertet. Darüber hinaus rechnet das System physische Lagerbuchungen des Artikels für Zugänge und Abgänge in Standardkosten basierend auf dem Umrechnungsdatum um. Außerdem wird der wertmäßige verfügbare Lagerbestand des Artikels in Standardkosten umgerechnet und der Wertunterschied als Lagerneubewertung gebucht. Alle Buchungen, die nach der Umrechung stattfinden, werden zu den Standardkosten des Artikels bewertet. Vor dem Umrechnungsdatum können keine rückdatierten Buchungen eingegeben werden, da ein Lagerabschluss einen Tag vor dem Umrechnungsdatum ausgeführt werden muss. Eine Umrechnung kann nur ausgeführt werden, wenn ein Lagerabschluss einen Tag zuvor ausgeführt wurde. Dieser Lagerabschluss kann nicht storniert werden.

## <a name="1-define-a-standard-cost-conversion-record-and-the-associated-costing-version"></a>1. Festlegen eines Standardkostenumrechnungs-Datensatzes und der zugeordneten Nachkalkulationsversion
Verwenden Sie die **Standardkostenumrechnungen**-Seite, um einen Umrechnungsdatensatz zu erstellen. Sie können einen neuen Umrechnungsdatensatz erst nach Abschluss vorhandener Umrechnungsdatensätze erstellen. Die Dauer der geplanten Übergangsperiode richtet sich nach dem Übergangsstartdatum und dem geplanten Umrechnungsdatum. Eine geplante Übergangsperiode ist mindestens einen Tag lang. Eine geplante Übergangsperiode unterstützt dabei, sicherzustellen, dass der Umwandlungsprozess ausreichend Zeit hat, alle zugehörigen Schritte abzuschließen. Ein Lagerabschluss muss an einem Datum einen Tag vor dem Übergangsstartdatum ausgeführt werden, um sicherzustellen, dass Ausgleiche vor dem Start des Umrechnungsvorgangs abgeschlossen sind. Um sicherzustellen, dass das Übergangsstartdatum und das Lagerabschlussdatum korrekt abgestimmt sind, können Sie entweder das Übergangsdatum auf den Tag nach einem vorhandenen Lagerabschluss ändern oder einen Lagerabschluss durchführen. Wenn Sie einen Umrechnungsdatensatz eingeben, geben Sie auch eine benutzerdefinierte Kennung für eine neue Nachkalkulationsversion ein, die die Standardkosten für umgerechnete Artikel enthält. Die Nachkalkulationsversion wird automatisch beim Speichern des Umrechnungsdatensatzes erstellt.

## <a name="2-review-and-change-the-new-costing-version-for-the-conversion-record"></a>2. Prüfen und Ändern der neuen Nachkalkulationsversion für den Umrechnungsdatensatz
Die neue Nachkalkulationsversion ist für den Umrechnungsdatensatz dediziert, wie im Nachkalkulationstyp **Umrechnung** ausgedrückt. Die dedizierte Nachkalkulationsversion verhält sich wie eine Nachkalkulationsversion für Standardkosten und enthält die Artikelkostendatensätze für Artikel, die dem Umrechnungsdatensatz zugeordnet sind. Die dedizierte Nachkalkulationsversion für einen Umrechnungsdatensatz weist die folgenden Einstellungen auf, die auf den verschiedenen Registerkarten geprüft und je nach Anforderung bearbeitet werden sollten:

-   **Nachkalkulationstyp:** Dieses Feld auf sollte auf **Standardkosten** festgelegt sein.
-   **Version:** − Die Kennung weist die Daten aus, die im Umrechnungsdatensatz für die Kennung der Nachkalkulationsversion eingegeben wurden.
-   **Name:** Standardmäßig ist dieses Feld leer. Sie können einen Namen eingeben.
-   **Sperren:** Dieses Feld auf sollte auf **Nein** festgelegt werden. Sie können Kostendatensätze in die Nachkalkulationsversion eingeben, bis Sie den Status des Umrechnungsdatensatzes in **Bereit** geändert haben. Der Status **Bereit** bedeutet, dass die ausgewählten Artikel geprüft wurden und Änderungen an Kostendatensätzen nicht zulässig sind.
-   **Aktivierung blockieren:** Dieses Feld auf sollte auf **Ja** festgelegt werden. Ein ausstehender Kostendatensatz innerhalb der dedizierten Nachkalkulationsversion kann nicht manuell aktiviert werden. Die Aktivierung erfolgt, wenn Sie die Umrechnung ausführen.
-   **Von Datum:** − Das "Von Datum" entspricht dem im Umrechnungsdatensatz angegebenen geplanten Umrechnungsdatum.
-   **Standort:** Lassen Sie das Feld leer, damit Kostendatensätze für jeden Standort eingegeben werden können.
-   **Preistyp-Feldgruppe zulassen:** Legen Sie dieses Feld auf **Ja** fest, sodass nur Einstandspreisdatensätze eingegeben werden können.
-   **Fallbackprinzip:** Dieses Feld ist auf **Kein** festgelegt. Ändern Sie das Fallbackprinzip auf **Aktiv**, wenn Sie in anderen Nachkalkulationsversionen aktivierte Kostendaten benötigen. Die Kostendaten für Komponenten, Kostenkategorien und indirekte Kosten können z. B. zum Berechnen der Kosten von produzierten Artikeln erforderlich sein.
-   **Fallback-Nachkalkulationsversion:** Lassen Sie dieses Feld leer.

Artikelkostendaten in der dedizierten Nachkalkulationsversion können nur im Formular **Standardkostenumrechnungen** verwaltet werden. Sie können die Seiten **Einstellungen für Nachkalkulationsversion** oder **Verwaltung der Nachkalkulationsversion** nicht verwenden, um Kosten für die Nachkalkulationsversion während der Umrechnung zu berechnen. Mithilfe dieser Seiten kann die dedizierte Nachkalkulationsversion nach der erfolgreichen Ausführung der Umrechnung verwaltet werden.

## <a name="3-identify-the-items-to-convert-to-standard-cost"></a>3. Bestimmen der Artikel, die in Standardkosten umgerechnet werden
Verwenden Sie die Seite**Standardkostenumrechnungen**, um die einzelnen Artikel, die in Standardkosten umgerechnet werden sollen, zu bestimmen. Sie können mehrere Artikel hinzufügen, indem Sie die Seite **Artikel der Standardkostenumrechnung hinzufügen** verwenden. Allgemein sollten Sie alle produzierten Artikel in einen Umrechnungsdatensatz einbeziehen, damit die Kosten richtig berechnet werden.

## <a name="4-enter-or-calculate-the-pending-standard-cost-for-each-item-that-is-being-converted"></a>4. Eingeben oder Berechnen der ausstehenden Standardkosten für jeden umzurechnenden Artikel
Geben Sie mithilfe der Seite **Artikelpreis** ausstehende Standardkosten in der dedizierten Nachkalkulationsversion für gekaufte Artikel und übertragene Artikel ein. Kostendatensätze sind standortspezifisch, und die ausstehende Kosten eines Artikels müssen für jeden Standort eingegeben werden. Berechnen Sie mithilfe der Seite **Artikelpreis** ausstehende Standardkosten für produzierte Artikel. Die ausstehenden Kosten eines produzierten Artikels müssen für jeden Produktionsstandort berechnet werden, wenn der Standort einen Umlagerungsstandort darstellt. In diesem Fall sollten die ausstehenden Kosten manuell eingegeben werden. Einige Artikel können über die Produktdimension Farbe, Größe oder Konfiguration verfügen. Auf der Seite **Standardkostenumrechnungen** werden im Kontrollkästchen **Einstandspreis nach Variante verwenden** die Standardkosten für jede Kombination von Produktdimensionen angezeigt. Wenn dieses Kontrollkästchen deaktiviert ist, müssen Sie nur ausstehende Kosten für den Artikel eingeben.

## <a name="5-check-and-resolve-any-issues-for-the-items-that-are-being-converted"></a>5. Prüfen und Lösen von Problemen für die umzurechnenden Artikel
Verwenden Sie den Bericht**Prüfoptionen für Standardkostenumrechnung**, um Probleme für die Artikel, die umgerechnet wurden, zu ermitteln. Werden für einen Artikel keine Probleme erkannt, wird der Status im Umrechnungsdatensatz in **Geprüft** geändert. Tritt bei einem Artikel ein Problem auf, muss dieses gelöst und der Bericht erneut ausgeführt werden, bis der Status des Artikels in **Geprüft** geändert wird. Lassen sich Probleme nicht innerhalb eines angemessenen Zeitraums lösen, kann der Artikel optional aus dem Umrechnungsdatensatz gelöscht und später umgerechnet werden.

## <a name="6-change-the-status-of-the-conversion-record-to-ready"></a>6. Ändern des Status des Umrechnungsdatensatzes in "Bereit"
Beim Ändern des Status des Umrechnungsdatensatzes in **Bereit** wird vor der Ausführung einer Standardkostenumrechnung eine letzte Überprüfung ausgeführt. Der Status wird nur dann in **Bereit** geändert, wenn die folgenden Bedingungen erfüllt sind:

-   Jeder Artikel im Umrechnungsdatensatz hat den Status **Geprüft**.
-   Ein Lagerabschluss wurde einen Tag vor dem Übergangsstartdatum ausgeführt. Um sicherzustellen, dass das Übergangsstartdatum und das Lagerabschlussdatum korrekt abgestimmt sind, können Sie entweder das Übergangsdatum auf den Tag nach einem vorhandenen Lagerabschluss ändern oder einen Lagerabschluss durchführen.

## <a name="7-back-up-the-database-before-conversion"></a>7. Datenbank vor der Umrechnung sichern
Die Datensicherung ermöglicht das Wiederherstellen der Datenbank, wenn während der Umrechnung Fehler auftreten.

## <a name="8-perform-the-conversion-when-the-conversion-record-has-a-ready-status"></a>8. Ausführen der Umrechnung, wenn der Umrechnungsdatensatz den Status "Bereit"aufweist.
Für die Umrechnung ist es erforderlich, dass ein Lagerabschluss einen Tag vor dem geplanten Übergangsdatum ausgeführt wird. Diese Anforderung stellt sicher, dass rückdatierte Buchungen nicht innerhalb der Übergangsperiode eingegeben werden können. Wenn noch kein Lagerabschluss ausgeführt wurde, werden Sie vom System gefragt, ob dieser als Teil des Umrechnungsvorgangs ausgeführt werden soll. Der Umrechnungsvorgang bearbeitet jeweils einen Artikel. Er beginnt mit den niedrigsten Artikeln in einer Produktstruktur, basierend auf dem Code der unteren Ebene des Artikels. Wenn ein Artikel umgerechnet wurde, wird sein Status im Umrechnungsdatensatz in **Konvertiert** geändert. Wenn der Umrechnungsvorgang unterbrochen wird, weist jeder Artikel, der noch nicht erfolgreich umgerechnet wurde, weiter den Status **Geprüft** aus. Der erfolgreiche Abschluss des Umrechnungsvorgangs wirkt sich wie folgt aus.

-   Der Status des Umrechnungsdatensatzes ändert sich von **Bereit** in **Abgeschlossen**, und der Status jedes ausgewählten Artikels ändert sich von **Geprüft** in **Konvertiert**.
-   Die Artikelmodellgruppe für umgerechnete Artikel wird geändert, sodass sie einer neuen Gruppe mit einem Standardkosten-Lagermodell entspricht.
-   Die Standardkosten für die umgerechneten Artikel wurden in der dedizierten Nachkalkulationsversion aktiviert.
-   Der Nachkalkulationstyp der Nachkalkulationsversion ändert sich von **Umrechnung** in **Standardkosten**, und die Nachkalkulationsversion agiert nun wie jede andere Nachkalkulationsversion für Standardkosten.

## <a name="9-validate-and-reconcile-the-inventory-values-for-the-converted-items"></a>9. Prüfen und Abstimmen der Lagerwerte für die umgerechneten Artikel
Mit dem Bericht **Aufstellung zur Abweichungsanalyse** können Sie Neubewertungsabweichungen analysieren und mit dem Bericht **Lagerwert** können Sie Lagerwerte an einem bestimmten Datum anzeigen.

-   Analysieren von Neubewertungsabweichungen. Mithilfe des Berichts **Aufstellung zur Abweichungsanalyse** können Sie Lagerneubewertungsabweichungen für die umgerechneten Artikel anzeigen. Sie können auch die Seite **Standardkostenbuchungen** verwenden, um die Lagerneubewertungsbuchungen für die umgerechneten Artikel mit Lagerbestand anzuzeigen.
-   Analysieren des Lagerwerts vor dem Übergangsstartdatum. Mithilfe des Berichts **Lagerwert** können Sie Lagerwerte für die umgerechneten Artikel anzeigen. Verwenden Sie für das "Bis Datum" im Bericht ein Datum, das einen Tag vor dem Übergangsstartdatum liegt.
-   Analysieren des Lagerwerts vor dem Umrechnungsdatum. Mithilfe des Berichts **Lagerwert** können Sie Lagerwerte für die umgerechneten Artikel anzeigen. Verwenden Sie für das "Bis Datum" im Bericht ein Datum, das dem Tag vor dem Übergangsstartdatum entspricht.
-   Analysieren des Lagerwerts am Umrechnungsdatum. Mithilfe des Berichts **Lagerwert** können Sie Lagerwerte am Umrechnungsdatum anzeigen. Sowohl das Von-Datum als auch das Bis-Datum des Berichts sollte dem Umrechnungsdatum entsprechen. Die Berichtsauswahlkriterien sollten die umgerechneten Artikel reflektieren.
-   Analysieren rückdatierter Lagerumlagerungen. Mithilfe des Berichts **Lagerwert** können Sie rückdatierte Lagerumlagerungen anzeigen, die nach der Umrechnung eingegeben wurden. Das Von-Datum und Bis-Datum des Berichts sollten dem Übergangsstartdatum und dem Umrechnungsdatum (minus ein Tag) entsprechen. Die Berichtsauswahlkriterien sollten die umgerechneten Artikel reflektieren. Der Bericht zeigt Lagerumlagerungen an, die während der Übergangsperiode zu Standardkosten vorgenommen wurden.


<a name="see-also"></a>Siehe auch
--------

[Voraussetzungen für eine Standardkostenumrechnung](prerequisites-standard-cost-conversion.md)




