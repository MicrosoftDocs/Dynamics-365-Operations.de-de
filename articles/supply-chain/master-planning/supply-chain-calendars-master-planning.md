---
title: Kalender und Produktprogrammplanung
description: Dieses Thema gibt einen Überblick über die Kalender der Lieferkette und deren Auswirkungen auf die Masterplanung.
author: t-benebo
manager: tfehr
ms.date: 08/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2c32957b0bd234ed14e6333a36a46c6a83ec2e91
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983915"
---
# <a name="calendars-and-master-planning"></a>Kalender und Produktprogrammplanung

[!include [banner](../includes/banner.md)]

Dieses Thema gibt einen Überblick über die Kalender der Lieferkette und deren Auswirkungen auf die Masterplanung.  Die verschiedenen Kalender, die im Produktprogrammpan-Modul verwendet werden, werden erläutert, einschließlich ihrer Auswirkungen auf die Versand- und Zugangsdatumsangaben in den Planaufträgen. Abschließend werden Empfehlungen zur Zuordnung, Verwendung und Aktualisierung der Kalender gegeben.

## <a name="definition-of-a-calendar"></a>Definition eines Kalenders

Sie können einen Kalender definieren, der in Ihrer Organisation verwendet werden soll, und zwar auf der Seite unter **Organisationsadministration > Einrichtung > Kalender > Kalender**. 

Jeder Datumseintrag in einem Kalender kann **offen** oder **geschlossen** oder **Basiskalender** sein. Dies wird in der Spalte **Steuerung** auf der Seite **Arbeitszeiten** angegeben. Für jedes Datum: 
- **Offen** – Zeigt an, dass an dem ausgewählten Tag gearbeitet wird. Der Kalender wird entsprechend der Arbeitszeitvorlage aktualisiert.
- **Geschlossen** – Zeigt an, dass nicht gearbeitet wird. 
- **Basiskalender** – Zeigt an, dass das spezifische Datum die Arbeitszeiten und den Offen/Geschlossen-Status aus dem Basiskalender übernimmt. Wenn der Basiskalender aktualisiert wird, erbt der ausgewählte Kalender daher die Betriebszeiten von ihm. 

Für alle geschlossenen Termine wird das Kontrollkästchen **Keine Abholung** automatisch zugewiesen. Für offene Termine können Sie manuell die Option **Keine Abholung** auswählen. Dies bedeutet, dass die Arbeiten am Datum ausgeführt werden, der Versand jedoch nicht durchgeführt wird. 

## <a name="calendars-that-affect-master-planning"></a>Kalender, die die Masterplanung beeinflussen.

### <a name="calendar-for-a-coverage-group"></a>Kalender für eine Deckungsgruppe
Eine Deckungsgruppe bezeichnet einen gemeinsamen Satz von Parametern für die Wiederbeschaffung der Artikel, die zu der jeweiligen Deckungsgruppe gehören. 

Um einen Kalender für eine Deckungsgruppe hinzuzufügen, gehen Sie zu **Masterplanung > Einrichtung > Deckung > Deckungsgruppen**. Suchen Sie die Deckungsgruppe, der Sie den Kalender zuordnen möchten, und wählen Sie sie dann im Feld **Kalender** aus.

Die Deckungsgruppe kann auf verschiedenen Seiten zugeordnet werden: 
    - Auf der Seite **Freigegebene Produktdetails** eines Artikels. Um die Deckungsgruppe für einen Artikel anzuzeigen, gehen Sie zu **Produktinformationsmanagement > Produkte > Freigegebene Produkte** und wählen Sie den Artikel aus, um zur Seite **Details für freigegebene Produkte** zu gelangen. Die Artikel-Deckungsgruppe sehen Sie unter der Registerkarte **Plan**.
    - Auf der Seite **Artikelabdeckung**. Klicken Sie auf der Detailseite der freigegebenen Produkte auf **Artikelabdeckung**, um zur Artikelabdeckung zu gelangen. Auf der Übersichtskarte sehen Sie je nach Betrieb, Lager und Produktdimension unterschiedliche Parameter für die Wiederbeschaffung. Die Deckungsgruppe für jeden Artikel wird von der Deckungsgruppe auf der Seite **Freigegebene Produktdetails** übernommen. Dies kann überschrieben werden, indem Sie auf der Registerkarte **Allgemein** die Einstellung **Bestimmte Einstellungen verwenden** oder **Gruppeneinstellung Überschreiben** verwenden verwenden verwenden.
    - Auf der Seite **Masterplanungsparameter**. Wenn ein Artikel keine auf den vorherigen Seiten eingestellte Deckungsgruppe hat, übernimmt die Masterplanung die auf den Masterplanungsparametern eingestellte allgemeine Deckungsgruppe. Dies ist in der **Masterplanung > Einrichten > Parameter der Masterplanung** im Feld **Allgemeine Deckungsgruppe** eingestellt. 

### <a name="calendar-for-a-vendor"></a>Kalender für einen Lieferanten
Um die Arbeitstage eines Lieferanten anzugeben, können Sie dem Lieferanten auf der Registerkarte **Standardwerte für Bestellungen** für einen Lieferanten einen Einkaufskalender zuordnen. 

Um einen Kalender für einen Lieferanten einzurichten, müssen Sie den Kalender unter **Organisationsverwaltung > Kalender > Kalender** erstellen. Wenn der Kalender angelegt wird, müssen Sie ihn dem Lieferanten zuordnen. Gehen Sie zu **Kreditorenkonten > Lieferanten > Alle Lieferanten** und wählen Sie den Lieferanten aus, dem Sie den Kalender zuordnen möchten. Weisen Sie anschließend auf der Seite des Lieferanten auf der Registerkarte **Standardwerte für Bestellungen** den neuen Einkaufskalender über das Dropdown-Menü zu. 

Der Kalender eines Lieferanten zeigt die Tage, an denen er die Bestellung akzeptiert und die Termine, an denen er die Bestellungen an Ihr Unternehmen liefern kann. Folglich sind die Bestelldaten für Bestellungen beim Lieferanten mit einem Bestellkalender die im Kalender als offen definierten Termine. Die Liefertermine für diese Bestellungen liegen ebenfalls an offenen Kalendertagen und beeinflussen somit die Vorlaufzeit des Einkaufsartikels. 

#### <a name="define-the-lead-time-for-a-purchased-item"></a>Definieren Sie die Vorlaufzeit für einen Einkaufsartikel.

Um die Einkaufsartikelvorlaufzeit (wenn nur Arbeitstage berücksichtigt werden sollen) für einen Artikel anzugeben, müssen Sie zur Seite mit den Standardbestelleinstellungen für das Produkt gehen, die Sie unter **Produktinformationsmanagement > Produkte > Freigegebene Produkte** finden und **Standardauftragseinstellungen** auswählen. 

> [!Note]
> Die **Arbeitstage** unter Einkaufsartikelvorlaufzeit geben die Arbeitstage des Lieferanten an. Wenn Sie z. B. einen Kalender für die Lieferung nur dienstags mit einer Vorlaufzeit von 10 Tagen und Arbeitstagen aktivieren, bedeutet dies, dass es 10 Wochen (10 Dienstage) dauern würde, bis die zu liefernde Position geliefert wird.
Daher ist es in den meisten Fällen nicht empfehlenswert, Arbeitstage für die Vorlaufzeiten der Bestellungen zu wählen.

#### <a name="define-lead-times-from-the-trade-agreements-page"></a>Definieren von Lieferzeiten auf der Seite der Handelsverträge

Die Masterplanung kann so eingerichtet werden, dass sie alle Handelsverträge für Lieferanten umfasst. Handelsverträge sind Festpreis- oder Rabattvereinbarungen, die für einen oder mehrere Kunden oder Lieferanten zum Kauf oder Verkauf einzelner oder mehrerer Produkte abgeschlossen werden. Gehen Sie zu **Masterplanung > Einrichtung > Masterplanungsparameter** und wählen Sie auf der Registerkarte **Planaufträge** die Option **Handelsverträge suchen**, um die Handelsverträge bei der Planung einzubeziehen. Die Masterplanung kann den Lieferanten mit der **Mindestvorlaufzeit** oder mit dem **niedrigsten Stückpreis** auswählen.

### <a name="calendar-for-a-warehouse"></a>Kalender für ein Lager
Sie können einem Lager einen Kalender zuordnen, um die offenen Termine für Wareneingang und -ausgang anzuzeigen. Wenn einem Lager kein Kalender zugeordnet ist, wird davon ausgegangen, dass es alle Tage geöffnet ist. 

> [!Note]
> Die Zuordnung eines Kalenders zu einem Transitlager hat keine Auswirkungen. Transitlager werden zur Unterstützung von Transportaufträgen eingesetzt. Die für die Bestellungen maßgeblichen Versand- oder Zugangstermine ergeben sich aus den offenen Tagen innerhalb des "Von"-Lagers und des "Nach"-Lagers sowie aus der Art des Lieferkalenders.

#### <a name="closed-for-pickup-policy"></a>"Keine Abholung"-Richtlinien
Um anzuzeigen, dass ein Lager für den Wareneingang geöffnet ist, aber keine Abholung möglich ist, können Sie die Richtlinie **Keine Abholung** im Lagerkalender verwenden. Dies gilt auch für Kundenabholungen. 

### <a name="transport-calendar"></a>Transportkalender 
Um die Termine anzugeben, die für den Versand von Transportaufträgen aus einem **Von-Lager** verfügbar sind, können Sie einen **Transportkalender** zuordnen. Sie können einen Transportkalender pro Lieferart oder pro Lieferart und ab Lager einrichten. Der Transportkalender ist unter **Vertrieb und Marketing > Einrichtung > Verteilung > Lieferarten**. Wählen Sie eine Versandart aus und klicken Sie auf die Schaltfläche **Transportkalender**.

Für jedes Lager und jede Lieferart kann eine Zeile angelegt werden, in der der Kalender in der Spalte **Transportkalender** hinzugefügt wird. Es wird der Transportkalender festgelegt, der angewendet wird, wenn Waren aus dem Lager mit der angegebenen Lieferart versandt werden. Um einen Transportkalender auf alle Sendungen anzuwenden, die einen bestimmten Lieferweg verwenden, kann eine Zeile ohne Angabe des Lagers angelegt werden.  Es betrifft alle Sendungen, die die angegebene Lieferart verwenden, unabhängig vom Lager. 

Wenn kein Transportkalender zugeordnet ist, wird davon ausgegangen, dass alle Tage für den Transport geöffnet sind.

### <a name="calendar-for-a-customer"></a>Kalender für einen Kunden
Um die Termine anzugeben, an denen ein Kunde Lieferungen annehmen kann, können Sie dem Kunden einen Empfangskalender zuordnen. Ist einem Kunden kein Kalender zugeordnet, wird davon ausgegangen, dass der Kunde an allen Tagen Aufträge erhalten kann. Dies wirkt sich auf das Zugangsdatum auf den Kundenauftragszeilen aus. Wenn Sie in den Kundenauftragszeilen ein Datum auswählen, das im Kundenkalender nicht "offen" ist, zeigt das System an, dass das Zugangsdatum nicht gültig ist. 

Beachten Sie, dass es möglich ist, nur einen Kalender pro Kunde einzubinden. Wenn Sie für jede verschiedene Adresse eines Kunden einen Kalender einbinden müssen, können Sie pro Adresse einen Kunden anlegen und ihm dann den entsprechenden Kalender zuordnen. 

Das gewünschte Zugangsdatum auf den Kundenauftragszeilen wird durch den Kundenkalender und die Steuerung des Liefertermins beeinflusst. Weitere Informationen zur Berechnung des frühesten Liefertermins finden Sie unter [Lieferterminzusage](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/delivery-dates-available-promise-calculations).

### <a name="shipping-calendar-for-a-legal-entity"></a>Versandkalender für eine juristische Person
Um die Daten anzugeben, an denen eine juristische Person Waren versenden kann, können Sie unter **Organisationsverwaltung > Organisationen > Juristische Personen** einen Versandkalender einrichten. Wählen Sie die juristische Person aus und fügen Sie den Kalender auf der Registerkarte **Außenhandel und Logistik** im Feld **Versandkalender** hinzu. Der Versandkalender dient als Quelle für Standardwerte für alle Lagerkalender der juristischen Person. 

## <a name="how-calendars-affect-dates-in-planning"></a>Wie Kalender Termine in der Planung beeinflussen

### <a name="order-date-of-a-planned-purchase-order"></a>Bestelldatum einer geplante Einkaufsbestellung 
Das Bestelldatum in einer geplante Einkaufsbestellung gibt das Datum an, an dem der Auftrag erteilt wird. Es handelt sich um ein offenes Datum sowohl im Lieferantenkalender als auch im Kalender der Deckungsgruppen. Manchmal benötigen Lieferanten einige Tage Marge zwischen dem Eingang der Bestellung und dem Versand der Ware. Diese Daten werden in den Margentagen des Lieferanten angegeben. Wenn der Einkaufsartikel jedoch einer Deckungsgruppe mit Margentagen zugeordnet ist, überschreiben diese Margentage die Margentage des Lieferanten.

### <a name="delivery-date-of-a-planned-purchase-order"></a>Lieferdatum einer geplante Einkaufsbestellung
Das Eingangsdatum eines Kaufs gibt das Datum an, an dem Sie die Ware erhalten. Es wird ein offenes Datum im Kalender sein. Die Kalender werden wie folgt berücksichtigt (in der Reihenfolge von höchster bis niedrigster Priorität): 
1. Kalender des Lieferanten
1. Kalender der Deckungsgruppe
1. Lagerkalender für das empfangende Lager

Beachten Sie, dass der Kalender der Deckungsgruppe auf verschiedenen Seiten eingestellt werden kann und in der folgenden Reihenfolge Priorität hat:
1. Artikel-Deckungsgruppe auf der Seite **Artikel-Deckung**
1. Artikeldeckungsgruppe auf der Seite **Details für freigegebene Produkte verwalten**
1. Standardartikeldeckungsgruppe in den **Masterplanungsparametern**

### <a name="shipping-date-of-a-planned-transfer-order"></a>Lieferdatum eines geplanten Transportauftrags
Bei der Erstellung eines Transportauftrags zwischen zwei Lagern werden das Versanddatum und das Eingangsdatum sowie das Lager "von" und das Lager "bis" im Kopf des Transportauftrags berücksichtigt. Die Differenz zwischen diesen beiden Daten ist die erwartete Transportzeit (in Tagen) zwischen den Lagern.

Das Versanddatum eines geplanten Transportauftrags gibt das Datum an, an dem die Ware aus dem Lager "Von" versandt wird. Die Kalender, die zur Angabe des verfügbaren Versanddatums verwendet werden, sind nach Priorität geordnet: 
1. Lagerkalender des "Von"-Lagers
1. Deckungsgruppenkalender (siehe Fallback-Auftrag für diesen Kalender oben) Wenn ein Lagerkalender eingestellt ist, ist das Versanddatum ein offenes Datum im Kalender. Wenn es keinen Lagerkalender gibt, wird der Kalender der Deckungsgruppe verwendet. 

### <a name="receipt-date-of-a-planned-transfer-order"></a>Zugangsdatum eines geplanten Transportauftrags
Das Zugangsdatum für einen Transportauftrag gibt das Datum an, an dem die Ware im Lager "Nach" eingetroffen ist.

Die Kalender, die für die Angabe des Zugangsdatums verwendet werden, sind die nach Priorität geordneten Kalender: 
1. Kalender der Deckungsgruppe 
1. Lagerkalender des "Nach"-Lagers Wenn ein Abdeckungskalender eingestellt ist, ist das Zugangsdatum ein offenes Datum im Kalender. Wenn kein Deckungsgruppen-Kalender gesetzt ist, wird der Lagerkalender verwendet. 

Bei der Ermittlung der Versand- und Empfangsdaten für den geplanten Transfer werden auch die vom Benutzer festgelegten Margen für Versand und Empfang berücksichtigt. 

## <a name="using-calendars-in-master-planning"></a>Verwendung von Kalendern in der Masterplanung

### <a name="assignment-of-scm-calendars"></a>Zuordnung von SCM-Kalendern
Es ist wichtig, die Kalender so einzustellen, dass sie die Arbeitstage des Unternehmens identifizieren. Die beste Implementierung ist es, für jedes Element einen Kalender mit unterschiedlichen Arbeitstagen festzulegen. Mit anderen Worten, alle externen Kalender (Kunde, Lieferant) und alle internen (Lager, Deckungsgruppe und Lieferart), die sich auf das Unternehmen beziehen.

### <a name="recommendation-on-warehouse-calendars"></a>Empfehlung zu Lagerkalendern
Es wird empfohlen, einen Kalender pro Lager zu verwenden, um die spezifischen Änderungen, die nur das Lager betreffen, zu berücksichtigen. Beispielsweise könnten zwei oder mehr Lager die gleichen Arbeitstage, aber eine andere Abholrichtlinie haben. In diesem Fall ist ein Kalender für jedes der Lager mit seiner jeweiligen Abholrichtlinie die beste Implementierung für das System, um die besten Termine für geplante Kauf-, Transport- und Fertigungsaufträge zu erhalten. Wenn keine Lagerkalender eingestellt sind, kann der Kalender der juristischen Person als Quelle für die Standardeinstellungen für den Lagerkalender verwendet werden. 

### <a name="recommendation-of-coverage-group-calendars"></a>Empfehlung zu Deckungsgruppenkalendern
Bezüglich des Deckungsgruppenkalenders ist zu beachten, dass dieses in der Masterplanung ein übergeordnetes Verhalten in Bezug auf Zugangsdaten aufweist. Es wird daher empfohlen, es mit Vorsicht zu verwenden. Dies ist insbesondere dann sinnvoll, wenn der Nachschub an bestimmten Tagen in der Woche erfolgen soll. 

### <a name="updating-scm-related-calendars"></a>Aktualisierung von SCM-bezogenen Kalendern
Es ist zwar wichtig, dass alle relevanten Kalender an ihrem jeweiligen Ort (Lieferant, Kunde, Lager, Lieferart oder Deckungsgruppe) zugeordnet sind, aber die Aktualisierung ist ebenso wichtig, damit sie die Änderungen berücksichtigen. Das System definiert die Produktions-, Transfer-, Einkaufs- und Kundenauftragsdaten abhängig von der Kombination der zugeordneten Kalender. Es ist eine bewährte Vorgehensweise, um zu klären, wer für die Zuordnung und Aktualisierung der Kalender in den entsprechenden Bereichen verantwortlich ist. Im Falle einer Panne oder einer anderen ungewöhnlichen Änderung der Arbeitstage ist es unerlässlich, die Kalender entsprechend zu aktualisieren. Alle kalenderabhängigen Aufgaben, wie z.B. die Masterplanung und Produktionsplanung, müssen bei der Aktualisierung von Kalendern erneut ausgeführt werden. 
