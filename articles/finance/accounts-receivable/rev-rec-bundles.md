---
title: Umsatzerkennungsbündel
description: In diesem Artikel wird die Bündelfunktion erläutert, die Teil der Funktion zur Umsatzerkennung in der Debitorenbuchhaltung ist. Ein Bündel besteht aus einem übergeordneten Artikel und mehreren Komponentenartikeln.
author: kweekley
ms.date: 01/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 62a4d7f36ad0b36edeaec75e9b670e2aad143703
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725818"
---
# <a name="revenue-recognition-bundles"></a>Umsatzerkennungsbündel

[!include [banner](../includes/banner.md)]

In diesem Artikel wird die Bündelfunktion erläutert, die Teil der Funktion zur Umsatzerkennung in der Debitorenbuchhaltung ist. Ein Bündel besteht aus einem übergeordneten Artikel und mehreren Komponentenartikeln. Der übergeordnete Artikel wird in einen Auftrag eingegeben, um die Auftragserfassung effizienter zu gestalten. Danach wird er in die Komponentenartikel aufgelöst. In internen Dokumenten, wie z. B. Lieferscheinen, werden die Komponenten aufgelistet. Externe Dokumente zeigen jedoch nur den übergeordneten Artikel an.

> [!NOTE]
> Microsoft Dynamics 365 Commerce-Kanäle wie Onlineshops, Verkaufsstellen (Point of sale; POS) und Callcenter unterstützen keine Umsatzrealisierung (einschließlich der Paketfunktion). Dies trifft auch auf die Prospect-to-Cash-Lösung für Dynamics 365 Supply Chain Management und Dynamics 365 Sales zu. Artikel, bei denen die Umsatzerkennung konfiguriert wurde, sollten nicht Bestellungen oder Transaktionen hinzugefügt werden, die in Commerce-Kanälen oder in der Prospect-to-Cash-Lösung erstellt wurden.

Um Bündel einzurichten, müssen Sie die Konfigurationsschlüssel für die Umsatzerkennung eingeben. Sie können Bündel allerdings auch dann nutzen, wenn keine Umsatzerkennung eingerichtet wurde. Ebenso können Sie die Umsatzerkennung ohne eingerichtete Bündel in Anspruch nehmen. Bei eingerichteter Umsatzerkennung bestimmen die Komponentenartikel den Umsatzerlöspreis und den Umsatzerlöszeitplan, der bei Berechnung eines Auftrags für Umsatzerkennung oder verzögerte Umsatzerlöse verwendet wird.

Die Einrichtung erfolgt mithilfe von Stücklistenfunktionen. Informationen zum Einrichten von Bündelartikeln finden Sie unter [Einrichtung der Umsatzrealisierung](revenue-recognition-setup.md). Wenn der übergeordnete Artikel als Bündel gekennzeichnet ist, wird er anders verarbeitet als andere Stücklistenartikel. Dies sind die Unterschiede:

- Bündel müssen durch Auswahl des Auftrags aufgelöst werden. Dazu wählen Sie auf der Seite mit dem Auftrag im Aktionsbereich auf der Registerkarte **Verkaufen** die Option **Auftrag bestätigen** aus. Bündelartikel dürfen niemals durch Auswahl der Option **Stücklistenposition** unter **Auflösen** im Menü **Auftragsposition** im Inforegister **Auftragspositionen** aufgelöst werden. Andernfalls wird der Artikel als Stückliste und nicht als Bündel verarbeitet.
- Aufträge mit einem Bündelartikel müssen vor Erstellung von Lieferschein oder Rechnung bestätigt werden.
- Wird ein Bündel durch Bestätigen des Auftrags aufgelöst. wird der übergeordnete Artikel storniert und sein Stückpreis und die zugehörigen Rabatte werden den Komponentenartikeln des Bündels zugewiesen.
- Die Summe der Komponentenartikel muss immer dem Preis des übergeordneten Artikels entsprechen. Daher sind die Felder, die bei Komponentenartikeln aktualisiert oder geändert werden können, eingeschränkt. Beispielsweise kann der Stückpreis nicht manuell geändert werden. Er kann außerdem nicht indirekt geändert werden, indem eine neue Preisvereinbarung in Kraft tritt. Um eine neue Preisvereinbarung zu verhindern, können die Bestandsdimensionen bei Komponentenartikeln nicht geändert werden.
- Wird ein zur externen Verwendung bestimmtes Dokument wie die Auftragsbestätigung oder Rechnung gedruckt, wird der übergeordnete Artikel gedruckt, nicht aber die Komponentenartikel.

## <a name="bundles-on-sales-orders"></a>Bündel in Aufträgen

Im USMF-Demounternehmen wurde die Bündelfunktion wie folgt eingerichtet. Beachten Sie, dass alle Einstellungen für die Umsatzerkennung, z. B. die Einrichtung von Umsatzerlöszeitplänen, aus den in diesem Fall verwendeten Artikeln entfernt wurden.

**Übergeordneter Artikel:** Laptopbündel

- **Komponentenartikel:** Eine Menge von 1 des Artikels 1000
- **Komponentenartikel:** Eine Menge von 1 des Artikels S0021
- **Komponentenartikel:** Eine Menge von 1 des Artikels Support

Der *Basisverkaufspreis* der Komponentenartikel ist wesentlicher Bestandteil der Komponenteneinrichtung. Er wird auf im Inforegister **Verkaufen** eines Artikels festgelegt. Der Basisverkaufspreis dient zur Berechnung des Zuteilungsfaktors, wenn der Stückpreis des übergeordneten Artikels den Komponentenartikeln zugewiesen wird. Die Verkaufspreise aus der Handelsvereinbarung werden keinesfalls zu diesem Zweck verwendet.

Für die Komponentenartikel sind folgende Basisverkaufspreise angegeben:

- **1000:** 1.900,00 US-Dollar
- **S0021:** 150,00 US-Dollar
- **Support:** 500,00 US-Dollar

Für den Kunden US-004, Cave Wholesales, wird ein Auftrag eingegeben. Als einzige Position wird der Bündelartikel „Laptop“ eingegeben. Der Standardeinheitspreis für den übergeordneten Artikel ist an zahlreichen Stellen angegeben, so z. B. in der Handelsvereinbarung oder im Basisverkaufspreis. Bei diesem Beispiel wurden 2.300 US-Dollar manuell als Einheitenpreis eingegeben.

[![Bündelartikel „Laptop“ in einem Auftrag.](./media/bundle-01.png)](./media/bundle-01.png)

Weil der Auftrag ein Bündel enthält, muss er bestätigt werden. Die Bestandteile des Bündels werden im Dialogfeld zur Bestätigung aufgeführt.

[![Dialogfeld zur Bestätigung des Auftrags mit Komponentenartikeln.](./media/bundle-02.png)](./media/bundle-02.png)

In der gedruckten Auftragsbestätigung ist allerdings nur der übergeordnete Bündelartikel vermerkt, weil das Dokument an den Kunden geht.

[![Bestätigung mit nur dem übergeordneten Artikel.](./media/bundle-03.png)](./media/bundle-03.png)

Nach Bestätigung des Auftrags wird der übergeordnete Artikel weiterhin im Auftrag angezeigt, sein Status wurde jedoch auf **Storniert** geändert. Zusätzlich wird der Nettobetrag im Feld **Bündelnettobetrag** angegeben. Dieser Betrag ist erforderlich, um die Rechnung zu drucken, denn auf der Rechnung ist der übergeordnete Artikel und nicht die Komponentenartikel aufgeführt.

Die Summe der Komponentenartikel muss dem Wert im Feld **Nettobündelbetrag** entsprechen, weil dieser Wert mit dem Betrag identisch ist, den der Kunde auf der gedruckten Rechnung sieht. Um sicherzustellen, dass die Rechnung mit den Beträgen übereinstimmt, die ins Hauptbuch gebucht werden, sind Änderungen an den Komponentenartikeln eingeschränkt. So können Standort und Lager nicht geändert werden, weil es durch diese Änderungen zu einer Preisänderung aufgrund einer Handelsvereinbarung kommen könnte.

Der Stückpreis aus der Position des übergeordneten Artikels wird den Komponenten folgendermaßen zugewiesen:

**Gesamte Basisverkaufspreise der Komponenten:** 1.900 US-Dollar + 500 US-Dollar + 150 US-Dollar = 2.550 US-Dollar

- **Komponente 1:** 2.300 US-Dollar × (1.900 US-Dollar ÷ 2.550 US-Dollar) = 1.713,73 US-Dollar
- **Komponente 2:** 2.300 US-Dollar × (500 US-Dollar ÷ 2.550 US-Dollar) = 450,98 US-Dollar
- **Komponente 3:** 2.300 US-Dollar × (150 US-Dollar ÷ 2.550 US-Dollar) = 135,29 US-Dollar

Die Summe der Komponenten muss 2.300 US-Dollar entsprechen, was auch der Fall ist (1.713,73 US-Dollar + 450,98 US-Dollar + 135,29 US-Dollar = 2.300 US-Dollar).

Sind für alle Komponentenartikel Änderungen erforderlich, kann der übergeordnete Artikel gelöscht werden. In diesem Fall werden auch die Komponentenartikel gelöscht. Der übergeordnete Artikel kann dann erneut hinzugefügt werden, und die erforderlichen Änderungen können vor Bestätigung des Auftrags erfolgen.

[![Bündelartikel mit Änderungen an den Komponentenartikeln.](./media/bundle-04.png)](./media/bundle-04.png)

Wenn der Auftrag kommissioniert und verpackt wird, sind in den Dokumenten nur die Bündelkomponenten angegeben. In Lieferschein und Rechnung muss das ganze Bündel aufgeführt werden. Andernfalls kann keine Buchung erfolgen. Als Beispiel sind im Dialogfeld drei Komponentenartikel angegeben. Wenn Sie versuchen, einen davon zu löschen, wird eine Fehlermeldung angezeigt, die besagt, dass alle Produkte im Bündel ausgeliefert werden müssen, bevor sie in Rechnung gestellt werden können.

Bündel müssen als komplette Bündel geliefert und in Rechnung gestellt werden. Wenn Sie beispielsweise die Menge des Artikels 1000 auf 4 ändern, aber die Menge der anderen Komponentenartikel bei 5 belassen, können Lieferschein und Rechnung nicht gebucht werden.

Eine Teilmenge kann nur dann geliefert und in Rechnung gestellt werden, wenn die Menge bei allen Bündelkomponenten verringert wird. Beispielsweise wird in einem Auftrag der Bündelartikel „Laptop“ mit der Menge 5 erfasst. Nach Bestätigung des Auftrags werden die drei Komponentenartikel im Auftrag mit je einer Menge von 5 angezeigt. Standardmäßig wird bei Lieferung und Rechnungsstellung die Menge bei jeder Komponente auf 5 festgelegt. Sie können die Menge bei allen drei Komponentenartikeln aber auf 3 verringern. In diesem Fall werden drei vollständige Bündel versandt und in Rechnung gestellt. Die verbleibenden zwei Bündelartikel (jeweils 2 bei allen drei Komponentenartikeln) können später geliefert und in Rechnung gestellt werden.

Im letzten Schritt wird der Auftrag in Rechnung gestellt. Bei der Rechnungsstellung werden im zugehörigen Dialogfeld die Komponentenartikel angezeigt.

[![Dialogfeld zur Rechnungsstellung mit Komponentenartikeln.](./media/bundle-06.png)](./media/bundle-06.png)

Auf der gedruckten Rechnung steht aber nur der übergeordnete Artikel.
 
[![Gedruckte Rechnung mit nur dem übergeordneten Artikel.](./media/bundle-07.png)](./media/bundle-07.png)

Die Rechnungserfassung, die nach dem Buchen erstellt wird, enthält nicht den übergeordneten Artikel aus dem Bündel, weil dieser im Status **Storniert** ist.

[![Rechnungserfassung ohne den übergeordneten Artikel.](./media/bundle-08.png)](./media/bundle-08.png)

Es ist wichtig, dass die Rechnungserfassung nicht den übergeordneten Bündelartikel enthält, weil alle Prozesse, die nach Buchung der Rechnung erfolgen, auf der Rechnungserfassung beruhen. Wenn Sie beispielsweise im Aktionsbereich auf der Registerkarte **Verkaufen** eine Gutschrift erstellen, enthält diese die Komponentenartikel, nicht aber den übergeordneten Artikel.

[![Gutschrift mit Komponentenartikeln, aber ohne übergeordneten Artikel.](./media/bundle-09.png)](./media/bundle-09.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
