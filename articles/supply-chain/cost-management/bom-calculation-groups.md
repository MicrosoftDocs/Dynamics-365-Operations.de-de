---
title: Stücklistenkalkulationsgruppen
description: Dieser Artikel enthält Informationen zu Herstellungskostenkalkulationsgruppen und wie man sie einrichtet. Um eine Herstellkostenkalkulation auszuführen, müssen Sie entweder Berechnungsgruppen einrichten und sie einzelnen Artikeln zuweisen oder eine Standardberechnungsgruppe festlegen. Die Berechnungseinstellungen einer Berechnungsgruppe dienen dann auf der Seite "Herstellkostenkalkulation" als Standardwerte zum Zeitpunkt der Herstellkostenkalkulation.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcGroup, BOMCalcTable, BOMCalcTrans, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94063
ms.assetid: 63e1b7dc-c2c5-41b0-81ed-e3e02d1b39e0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1978873601608b5d2b67fa4229f61afa46d7e5cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011896"
---
# <a name="bom-calculations-groups"></a>Stücklistenkalkulationsgruppen

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Herstellungskostenkalkulationsgruppen und wie man sie einrichtet. Um eine Herstellkostenkalkulation auszuführen, müssen Sie entweder Berechnungsgruppen einrichten und sie einzelnen Artikeln zuweisen oder eine Standardberechnungsgruppe festlegen. Die Berechnungseinstellungen einer Berechnungsgruppe dienen dann auf der Seite "Herstellkostenkalkulation" als Standardwerte zum Zeitpunkt der Herstellkostenkalkulation. 

Auf der Seite **Parameter für Lager- und Lagerortverwaltung** ist eine Standardberechnungsgruppe erforderlich oder auf der Seite **Details für freigegebene Produkte** eine produktspezifische Berechnungsgruppe. Das System sucht zuerst nach Berechnungsgruppeneinstellungen auf der Seite **Produktdetails freigeben**. Wenn dort keine Berechnungsgruppe gefunden wird, sucht  esauf der Seite **Parameter für Lager- und Lagerortverwaltung**. Wenn das System keine Berechnungsgruppe findet, erhält der Benutzer während der Berechnung eine Fehlermeldung. Eine Berechnungsgruppe enthält Richtlinien für das Einstandspreismodell, das Verkaufspreismodell und die Prüfliste der Warnungen. Die Berechnungseinstellungen einer Berechnungsgruppe dienen auf der Seite **Herstellkostenkalkulation** als Standardwerte zum Zeitpunkt der Herstellkostenkalkulation.

## <a name="purposes-of-bom-calculation-groups"></a>Zwecke der Herstellkostenkalkulationsgruppen
Sie weisen eine Herstellkostenkalkulationsgruppe Artikeln aus mehreren Gründen zu:

-   Mithilfe des Felds **Einstandspreismodell**, geben Sie die Quelle der Kostenbeitragsdaten einer eingekauften Komponente bei der Berechnung der geplanten Kosten eines produzierten Artikels an. Einige Hersteller verwenden zur Berechnung geplanter Kosten die Einkaufspreis-Handelsvereinbarungen für eingekaufte Komponenten oder eine andere Grundlage (beispielsweise die Einkaufspreisdatensätze in einer Nachkalkulationsversion).
-   Mithilfe des Felds **Verkaufspreismodell** geben Sie die Art und Weise an, in der die Daten des Artikels zur Berechnung eines vorgeschlagenen Verkaufspreises verwendet werden sollen. Sie können entweder den Artikelverkaufspreis oder die Kostengruppe angeben. Einige Hersteller möchten für produzierte Artikel zunächst einen vorgeschlagenen Verkaufspreis berechnen. Der berechnete Verkaufspreis kann einen Ansatz mit flexiblen Preisen widerspiegeln, der auf dem Verkaufspreisdatensatz der Komponente basiert. Der berechnete Verkaufspreis kann auch einen Kosten-plus-Aufschlag-Ansatz auf Basis der Kosten und des zutreffenden Rentabilitätsprozentwerts der Komponente darstellen, die der Kostengruppe des Artikels zugeordnet ist.
-   Mithilfe des Felds **Stücklistenauflösung beenden** geben Sie an, dass ein produzierter Artikel in der Kostenaufschlüsselung der Herstellkostenkalkulation als eingekaufter Artikel behandelt werden soll. Ein typisches Szenario umfasst eingekaufte Artikel, die gelegentlich auch produziert werden, oder produzierte Artikel, die jetzt eingekauft werden. Der Artikel wird zunächst als produzierter Artikel festgelegt, um die Stückliste und die Arbeitsplaninformationen zu definieren und die Produktionsaufträge für den Artikel zu unterstützen. Aufgrund der Markierung **Stücklistenauflösung beenden** werden Stückliste und Arbeitsplan des Artikels jedoch nicht für die Kostenberechnung herangezogen. Stattdessen werden für die Herstellkostenkalkulation die angegebenen Kosten des Artikels verwendet.

## <a name="calculation-groups"></a>Berechnungsgruppen
Definieren Sie Berechnungsgruppen unter **Einrichtung der Richtlinien für vordefinierte Kosten** in der Kostenverwaltung. Berechnungsgruppen, die Artikeln zugewiesen sind, geben an, wie sich der Einstands- oder Verkaufspreis der Komponenten entsprechend der Berechnungsgruppe zusammensetzt. Auf der Seite **Berechnungsgruppen** können Sie ein Einstandspreismodell, ein alternatives Einstandspreismodell, ein Verkaufspreismodell und Warnungen definieren.

### <a name="cost-price-model"></a>Einstandspreismodell

Es gibt vier Optionen für das Feld **Einstandspreismodell**:

-   **Artikeleinstandspreis** – Der Einstandspreis aus der Tabelle **Freigegebenes Produkt** oder die Kombination aus Artikeldimensionen wird als Einstandspreis verwendet.
-   **Artikeleinkaufspreis** – Der Einkaufspreis aus dem Feld **Einstandspreis** auf der Registerkarte **Einkauf** der Seite **Freigegebene Produktliste** Seite wird verwendet.
-   **Handelsvereinbarungen** – Sie können Handelsvereinbarungen für bestimmte Kombinationen aus Artikeln und Kreditoren oder für bestimmte Standorte konfigurieren. Wenn Sie nun hier die Option **Handelsvereinbarungen** auswählen, wird die Handelsvereinbarung verwendet, die für den Einkaufspreis, den Artikel und die Standorte zusammen erstellt wurde.
-   **Lagerpreis** – Der aktuelle Lagerwert des Artikels wird zur Berechnung der Einheitenkosten in der Herstellkostenkalkulation verwendet. Ein Einstandspreis pro Einheit wird nur berechnet, wenn die gebuchte Menge und die physische Menge größer als 0 (null) sind.

### <a name="alternative-cost-price"></a>Alternativer Einstandspreis

Das Feld **Alternativer Einstandspreis** besitzt die gleichen Optionen wie das Feld **Einstandspreismodell**. Dieses Feld wird jedoch nur verwendet, wenn kein Preis im primären Einstandspreismodell gefunden werden kann.

### <a name="sales-price-model"></a>Verkaufspreismodell

Es gibt zwei Optionen für die Berechnung des Felds **Verkaufspreise**:

-   **Kostengruppe** – Wenn diese Option ausgewählt ist, wird der Verkaufspreis anhand des Einstandspreises und des Gewinnvorgaben-Prozentsatzes der Kostengruppe berechnet.
-   **Artikelverkaufspreis** – Wenn diese Option ausgewählt ist, wird der Verkaufspreis aus dem Inforegister **Verkaufen** der Tabelle "Freigegebenes Produkt" verwendet.

### <a name="stop-explosion"></a>Stücklistenauflösung beenden

Das Kontrollkästchen **Stücklistenauflösung beenden** wird verwendet, um anzuzeigen, dass ein produzierter Artikel als Einkaufsartikel behandelt werden soll. Normalerweise bleibt das Kontrollkästchen **Stücklistenauflösung beenden** deaktiviert. Aktivieren Sie das Kontrollkästchen, um anzugeben, dass ein hergestellter Artikel zu Herstellkostenkalkulationszwecken als gekaufte Komponente behandelt werden soll, nicht als hergestellte Komponente. Je nach Standort können die Artikelkosten mithilfe von Herstellkostenkalkulationen berechnet werden. Die Auflösung der geplanten Einkaufsbestellungen und Produktionsaufträge wird in der Stückliste angehalten, deren Komponenten der Berechnungsgruppe zugeordnet sind, für die das Kontrollkästchen **Stücklistenauflösung beenden** aktiviert ist. Der Produktprogrammplanungslauf generiert die Bestellvorschläge in der Stückliste selbst und nicht in den Artikeln, die die Stückliste umfasst. Grundsätzlich geben Sie durch Aktivieren dieses Kontrollkästchens an, dass Kosten nicht in die Herstellkostenkalkulation für Artikel hinzugefügt werden, die diese Berechnungsgruppe haben.

### <a name="warnings"></a>Warnungen

Auf dem Inforegister **Warnungen** wählen Sie die Optionen für alle Warnhinweise, die Benutzer erhalten sollen, wenn sie Herstellkostenkalkulationen verwenden. 

Angenommen, Sie aktivieren das Kontrollkästchen **Keine Stückliste**, erhält der Benutzer eine Warnung, wenn keine aktive Stücklistenversion für die Komponenten oder das übergeordnete Element, für das die Herstellkostenkalkulation ausgeführt wird, gefunden wird. Wenn Sie das Kontrollkästchen **Kein Arbeitsplan** aktivieren, erhalten Benutzer eine Warnung, falls keine aktive Arbeitsplanversion gefunden wird. Wenn Sie Ressourcen in Ihren Arbeitsplänen und Vorgängen verwenden, können Sie das System anweisen, diese Ressourcen zu überprüfen. Wenn dann eine Ressource nicht in jeder Zeile der aktiven Arbeitsplanversion gefunden wird, erhält der Benutzer eine Warnung. 

Sie können auch Verbrauch prüfen und bestätigen. Der Verbrauch ist die Menge in einem bestimmten Arbeitsplan. Normalerweise ist es die Zeit, die für einen bestimmten Vorgang in einem Produktionsprozess erforderlich ist. Sie können überprüfen, ob ein Element keinen Einstandspreis hat. Wenn kein aktiver Einstandspreis für einen Artikel vorhanden ist, werden der Herstellkostenkalkulation keine Kosten hinzugefügt. 

Sie können auch das Alter des Einstandspreises prüfen und bestätigen. Geben Sie beispielsweise **60** an, um festzulegen, dass der Einstandspreis pro Einheit nach 60 Tagen neu bewertet werden muss. Wenn diese Grenze erreicht ist, generiert das System eine Warnung. Beispielsweise wurde im Januar dieses Jahres ein Einstandspreis für einen Artikel eingegeben. Wenn es jetzt August ist, mehr als 60 Tage nachdem der Einstandspreis eingegeben wurde, erhält der Benutzer eine Warnung beim Ausführen der Herstellkostenkalkulation. Sei können im Feld **Minimal zulässiger Gewinnspannenbeitrag in Prozent** einen Prozentsatz eingeben. Dieser Wert gibt den Punkt an, ab dem der minimale Deckungsbeitrag nicht erfüllt ist. Wird der Deckungsbeitrag für eine bestimmte Komponente nicht erfüllt, erhält der Benutzer eine Warnung. Daher stellt dieses Feld sicher, dass die Kosten und zusätzlichen Lagerkosten,die möglicherweise für Ihre Artikel notwendig sind, nicht unterschritten werden.

### <a name="default-setup-in-inventory-and-warehouse-management-parameters"></a>Standardeinstellungen in den Parametern für Lager- und Lagerortverwaltung.

Da Berechnungsgruppen erforderlich sind, um Berechnungen durchzuführen, müssen Sie in den Lagerverwaltungsparametern eine Standardberechnungsgruppe einrichten. Diese Einstellung ermöglicht Unternehmen über eine Standardkostengruppe und Gewinnvorgaben für alle Artikel zu verfügen. Werden dann für einen bestimmten Artikel spezielle Berechnungsanforderungen benötigt, kann der Benutzer diesem Artikel eine andere Berechnungsgruppe zuweisen. Normalerweise können Sie keine Berechnungsgruppen für Stücklisten-Komponentenartikel statt für Stücklistenartikel festlegen. Sollten Warnmeldungen angezeigt werden, können Berechnungsgruppen angewendet werden. Eine Berechnungsgruppe, die einem Artikel zugewiesen ist, überschreibt den Standardwert, der in den Lagerverwaltungsparametern eingerichtet ist. 

Der Standardparameter kann unter **Kostenmanagement** &gt; **Einrichtung der Bestandsbuchhaltungsrichtlinien** &gt; **Parameter** &gt; **Bestandsbuchhaltung**  &gt; **Berechnungsgruppe** eingerichtet werden. Wenn Sie eine Standardkonfigurationsgruppe einrichten, können Sie auch Warnbedingungen konfigurieren, die Benutzer während des Vorgangs der Stücklistenberechnung bestätigen müssen, sollte die ausgewählte Komponente Berechnungsfehler verursachen.

### <a name="view-warning-messages-on-the-complete-page"></a>Anzeigen von Warnmeldungen auf der Seite "Abschließen"

Eine Herstellkostenkalkulation generiert Warnmeldungen. Sie können Warnungen zum ausgewählten Artikel anzeigen. Beispielsweise erstellen Sie in Vertrieb und Marketing einen neuen Auftrag für Artikel D0001. Klicken Sie dann in der Auftragsposition im Menü **Position aktualisieren** auf **Auf Basis von Stückliste/Formel berechnen**, um Berechnungsdetails und Warnungen anzeigen. Sie können die Ergebnisse der Herstellkostenkalkulation auf der Seite **Abschliessen** anzeigen. Nur zwei der Warnbedingungen beziehen sich auf produzierte Artikel, vier der Warnbedingungen beziehen sich auf beliebige Artikel:
-   Kennzeichnung, wenn ein produzierter Artikel über keine aktive Stückliste verfügt.
-   Kennzeichnung, wenn ein produzierter Artikel über keinen aktive Arbeitsplan verfügt
-   Kennzeichung, wenn der Artikel in einer Stücklistenposition die Menge "0" (Null) besitzt.
-   Kennzeichnung, wenn der Artikel in einer Stücklistenposition den Kostenwert "0" (Null) oder keinen Kostendatensatz besitzt
-   Kennzeichnung, wenn der Artikel in einer Stücklistenposition veraltete Kosten besitzt. Die Warnung beinhaltet einen Vergleich des Berechnungsdatums mit den angegebenen Tagen für ein Kostenhöchstalter.
-   Kennzeichnung, wenn von dem Artikel in einer Stücklistenposition der gewünschte Rentabilitätsprozentwert nicht erreicht wird

Sie können mehrere Herstellkostenkalkulationsgruppen je nach Bedarf an Variationen für Warnmeldungen definieren. So kann beispielsweise bereits eine einzelne Herstellkostenkalkulationsgruppe mit Warnbedingungen für eine aktive Stückliste, für eine Nullmenge bei einer Komponente sowie für den Kostenwert "0" (Null) bei einer Komponente ausreichend sein. Beim Starten einer Herstellkostenkalkulation können die Warnbedingungen, die der Herstellkostenkalkulationsgruppe zugeordnet sind, optional außer Kraft gesetzt werden. Sie können auch Warnbedingung hinzufügen oder entfernen. So kann beispielsweise die Warnbedingung für einen aktiven Arbeitsplan entfernt werden, wenn in einer bestimmten Situation keine Arbeitsplandaten vorliegen. **Hinweis:** Zeit und Anwesenheit enthält eine **Berechnungsgruppen**-Seite, jedoch besitzt diese Seite keine Beziehung zu den Herstellkostenkalkulationsgruppen. Arbeitskräfte können in Zeit und Anwesenheit Berechnungsgruppen zugewiesen werden, die die Gruppierung von Arbeitskräften widerspiegeln, die dem gleichen Supervisor oder Manager zugeordnet sind. Die Berechnung der Erfassungen von Arbeitskräften kann entweder automatisch erfolgen oder manuell von einem Supervisor oder Manager vorgenommen werden.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]