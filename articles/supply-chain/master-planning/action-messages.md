---
title: Aktivitätsmeldungen
description: Eine Aktivitätsmeldung ist ein vom System generierter Vorschlag zum Ändern eines vorhandenen geplanten oder festen Bestellvorschlags.
author: t-benebo
ms.date: 03/18/2022
ms.topic: article
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: e6df6cfd038383b3eeaa3659e0af3e469429f81e
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570253"
---
# <a name="action-messages"></a>Aktivitätsmeldungen

[!include [banner](../includes/banner.md)]

Eine Aktivitätsmeldung ist ein vom System generierter Vorschlag zum Ändern eines vorhandenen geplanten, genehmigten oder festen Bestellvorschlags.

Aktivitätsmeldungen werden vom Produktprogrammplanungslauf bei der Kalkulation in Reaktion auf geänderte Anforderungen generiert. Beispielsweise hat sich möglicherweise das Versanddatum oder die Menge im einem Auftrag geändert, für den Sie bereits eine Bestellung erstellt haben, um den Bedarf für diesen Auftrag zu decken. In diesem Fall werden ein oder mehrere Aktivitätsmeldungen von der Produktprogrammplanberechnung generiert, um die Bestellung zu aktualisieren. Ob die vorgeschlagenen Änderungen vorgenommen werden, entscheiden Sie.

Sie können konfigurieren, wie Aktivitätsmeldungen für eine Dispositionssteuerungsgruppe kalkuliert werden, die einem Artikel zugeordnet wird.

## <a name="select-action-messages"></a>Auswählen von Aktivitätsmeldungen

Im Formular **Dispositionssteuerungsgruppen** können Sie die Aktivitätsmeldungen, die das System generieren soll, und die Dispositionssteuerungsgruppen oder die Artikel auswählen, für die die Nachrichten gelten. In der folgenden Tabelle werden die Aktivitätsmeldungen aufgeführt, die Sie auswählen können.

| Meldung | Description |
|---|---|
| Termin vorziehen | Das System generiert bedarfsweise Aktivitätsmeldungen, um Bestellungen auf ein früheres Datum zu verschieben. Im Feld **Vorverlegungsgrenze** können Sie die maximale Anzahl der Tage zwischen Zugang und Abgang ohne Voraktivität angeben. |
| Verschieben | Das System generiert bedarfsweise Aktivitätsmeldungen, um Bestellungen auf ein späteres Datum zu verschieben. Im Feld **Vorverlegungsgrenze** können Sie die maximale Anzahl der Tage zwischen Zugang und Abgang ohne Verschiebungsaktion angeben. |
| Menge reduzieren | Das System generiert Aktionsmeldungen, wenn Produktionsaufträge, Bestellungen und andere Zugangsbuchungen verringert werden sollten, um Bestandsüberschüsse zu vermeiden. |
| Erhöhen | Das System generiert Aktionsmeldungen, wenn Produktionsaufträge, Bestellungen und andere Zugangsbuchungen erhöht werden sollten, um Bestandsengpässe zu vermeiden. |
| Abgeleitete Aktivitäten | Für Zugangsbuchungen erstellte Aktionsmeldungen werden an alle abgeleiteten Anforderungen weitergegeben, und die erforderlichen Aktionsmeldungen werden für die Zugangsbuchungen generiert, die diese Anforderungen erfüllen. |

In den folgenden Abschnitten finden Sie einige ausführliche Szenarios.

## <a name="increase-and-decrease-actions-with-product-default-order-quantities"></a>Aktionen zum Erhöhen und Verringern mit Standardbestellmengen

Auf der Seite **Standardauftragseinstellungen** für einen Artikel können Sie eine Mindestbestellmenge, eine maximale Bestellmenge und mehrere Werte einrichten. Das System berücksichtigt diese Einstellungen, wenn es Aktionen vorschlägt, um sicherzustellen, dass die Vorschläge niemals zu einer Unterversorgung führen.

Sie haben beispielsweise einen Artikel mit den folgenden Einstellungen auf der Seite **Standardauftragseinstellungen**:

- **Minimale Auftragsmenge:** *0*
- **Maximale Auftragsmenge:** *90*
- **Mehrfach:** *20*

Wenn Bedarf für eine Menge von 60 Stück dieses Artikels besteht, erstellt die Produktprogrammplanung eine geplante Einkaufsbestellung für 60 Stück. Wenn die Nachfrage um 30 erhöht wird, schlägt die Produktprogrammplanung eine Erhöhung um 40 vor, da dies das Vielfache von 20 respektiert und niemals zu einer Unterversorgung führt.

## <a name="action-messages-for-orders-related-to-safety-stock"></a>Aktionsmeldungen für Bestellungen im Zusammenhang mit Sicherheitsbeständen

Aktionsmeldungen für Bestellungen für den Sicherheitsbestand schlagen niemals vor, die Menge unterhalb der Menge zu verringern, die für den Sicherheitsbestand erforderlich ist. Mit anderen Worten: Wenn es einen Auftrag gibt, der Sicherheitsbestand und Kundenbedarf erfüllt, und der Bedarf verringert oder storniert wird, schlägt die Produktprogrammplanung vor, den Planauftrag um den verringerten Bedarf zu reduzieren. Es wird jedoch niemals ein Wert vorgeschlagen, der niedriger ist als der erforderliche Sicherheitsbestand.

Das System schlägt keine Verschiebungsmaßnahmen für die Lieferung von Sicherheitsbeständen vor, da davon ausgegangen wird, dass die Sicherheitsbestände zum erforderlichen Zeitpunkt und am erforderlichen Datum bereitgestellt werden müssen.

### <a name="advance-and-postpone-actions-related-to-boms"></a>Aktionen im Zusammenhang mit Stücklisten vorziehen und verschieben

Aktionen, die sich auf Komponenten von Stücklisten beziehen, müssen vor den Aktionen ihrer übergeordneten Elemente angewendet werden, da weitere Aufträge betroffen sein können, die sich auf Stücklisten höherer Ebenen beziehen. Anschließend müssen Sie die Produktprogrammplanung erneut ausführen, um die entsprechenden Aktionen neu zu berechnen und vorzuschlagen.

Sie haben zum Beispiel folgende Situation:

- Das Endprodukt *FG* des Typs *Produktion* hat eine Stückliste, die Rohmaterial *RM* enthält.
- Das heutige Datum ist der 21. Januar.
- Ein vorhandener, freigegebener Fertigungsauftrag für *FG* ist für den 25. Januar geplant.
- Um den vorhandenen Fertigungsauftrag zu unterstützen, hat die Produktprogrammplanung eine geplante Einkaufsbestellung für das erforderliche Rohmaterial *RM* erstellt. Diese Bestellung hat ein Bedarfsdatum vom 25. Januar.
- Ein neuer Auftrag für *FG* wird heute angelegt. Er hat das Bedarfsdatum von heute (12. Januar).
- Der 21. Januar ist im *RM*-Kalender für die Lieferung geschlossen, aber der 22. Januar ist offen.

Wenn die Produktprogrammplanung ausgeführt wird, generiert sie vorgezogene Aktivitätsmeldungen, die vorschlagen, die zuvor geplante Produktion nach oben zu verschieben, damit Sie den heutigen Auftrag erfüllen können.

- Um dem neuen Bedarf gerecht zu werden, schlägt sie vor, den Fertigungsauftrag für *FG* auf den 21. Januar zu verschieben. (Dieser Vorschlag wird ohne Berücksichtigung des Abschlussdatums für *RM* gemacht.)
- Da *RM* für den Fertigungsauftrag noch benötigt wird, schlägt sie vor, auch die geplante Einkaufsbestellung nach oben zu verschieben. Diesmal überprüft sie jedoch den *RM*-Kalender. Daher schlägt sie vor, die geplante Einkaufsbestellung für *RM* auf den 22. Januar zu verschieben (da der 21. Januar geschlossen ist).

Wie Sie sehen, kommt das benötigte Rohmaterial *RM* nun zu spät für die geplante Produktion *FG* an. Daher müssen Sie die Voraktivität zuerst auf die geplante Einkaufsbestellung für *RM* anwenden und dann die Produktprogrammplanung erneut ausführen. An diesem Punkt generiert die Produktprogrammplanung eine neue Aktivitätsmeldung, die vorschlägt, den Fertigungsauftrag für *FG* auf den 22. Januar zu verschieben.
