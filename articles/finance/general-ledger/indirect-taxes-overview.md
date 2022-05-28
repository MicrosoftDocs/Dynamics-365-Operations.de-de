---
title: Mehrwertsteuerüberblick
description: Dieser Artikel enthält eine Übersicht über das Mehrwertsteuersystem. Er erklärt die Elemente zur Einrichtung der Mehrwertsteuer und wie sie zusammenarbeiten.
author: kailiang
ms.date: 10/28/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19d235a761ffdfcfb945f7f6213dc8ec44f73aab
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727593"
---
# <a name="sales-tax-overview"></a>Mehrwertsteuerüberblick

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält eine Übersicht über das Mehrwertsteuersystem. Er erklärt die Elemente zur Einrichtung der Mehrwertsteuer und wie sie zusammenarbeiten.

## <a name="overview"></a>Überblick

Das Mehrwertsteuerframework unterstützt verschiedene Varianten von indirekten Steuern, wie etwa Mehrwertsteuer, Mehrwertsteuer (VAT), Waren und GST (Goods and Services Tax bezogene), Gebühren und Quellensteuer. Diese Steuern werden während des Einkaufs und der Verkaufsbuchungen berechnet und angegeben. In regelmäßigen Abständen muss Mehrwertsteuer gemeldet werden und an die Steuerbehörde abgeführt werden. 

Das folgende Diagramm zeigt die Entitäten der Steuereinrichtung und wie sie zugeordnet sind.

[![Diagramm, das einen Überblick über die Steuerstruktur gibt.](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

Für jede Mehrwertsteuer, die ein Unternehmen berechnet, muss ein Mehrwertsteuercode definiert werden. Ein Mehrwertsteuercode speichert die Steuersätze und die Berechnungsregeln für die Mehrwertsteuer. 

Jeder Mehrwertsteuercode muss mit einem Mehrwertsteuer-Ausgleichszeitraum verknüpft werden. Mehrwertsteuer-Abrechnungszeiträume definieren die Intervalle, zu denen die Mehrwertsteuer deklariert werden und abgeführt werden muss. Jeder Mehrwertsteuer-Abrechnungszeitraum muss einer Mehrwertsteuerbehörde zugewiesen werden. Eine Mehrwertsteuerbehörde stellt die Entität dar, an die die Mehrwertsteuer deklariert und entrichtet wird. Sie definieren auch das Layout für die Mehrwertsteuererklärung. Mehrwertsteuerbehörden können Kreditorenkonten zugeordnet werden. Weitere Informationen finden Sie unter [Einrichten der Mehrwertsteuerabrechnungsperioden](tasks/set-up-sales-tax-settlement-periods.md)

Jeder Mehrwertsteuercode muss mit einer Sachkontobuchungsgruppe verknüpft werden. Eine Sachkontobuchungsgruppe gibt die Hauptkonten an, für die Beträge für Mehrwertsteuercodes gebucht werden. 

Optionale Mehrwertsteuererklärungscodes können definiert werden. Diese können Mehrwertsteuercodes für verschiedene Betragstypen zugewiesen werden, die für den Mehrwertsteuercode berechnet werden. Der Bericht **Umsatzsteuerzahlung nach Code** zeigt Summen pro Umsatzsteuer-Meldekennzeichen für eine bestimmte Umsatzsteuerabrechnungsperiode und ein bestimmtes Intervall. 

Jede Buchung, für die Mehrwertsteuer berechnet und gebucht werden muss, muss eine Mehrwertsteuergruppe und eine Artikel-Mehrwertsteuergruppe haben. Mehrwertsteuergruppen werden der Partei (beispielsweise Debitor oder Kreditor) der Buchung zugeordnet, während Artikel-Mehrwertsteuergruppen der Ressource (beispielsweise Artikel oder Beschaffungskategorie) der Buchung zugeordnet sind. Steuergruppen enthalten eine Liste der Steuercodes. Die Steuercodes, die in der Mehrwertsteuergruppe und in der Artikel-Mehrwertsteuergruppe für eine Buchung vorhanden sind, sind der Steuercode, der für diese Buchung gilt. 

In der folgenden Tabelle beschreibt die Entitäten und die Reihenfolge für die Steuereinrichtung.

| Einrichtungsaktivität                                                  | Erforderlich/Optional und Beschreibung                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hauptkonten erstellen.                                           | Erforderlich. Vor dem Einrichten der Mehrwertsteuerfunktion müssen Sie die Hauptkonten erstellen, die das Unternehmen zum Bezahlen und Erfassen von Steuern verwendet.                                                                                                                                                                             |
| Richten Sie Sachkontobuchungsgruppen für Mehrwertsteuer ein.                     | Erforderlich. Sachkontobuchungsgruppen definieren die Hauptkonten für die Erfassung und Zahlung von Mehrwertsteuern.   Weitere Informationen finden Sie unter [Sachkontobuchungsgruppen für Umsatzsteuer einrichten](tasks/set-up-ledger-posting-groups-sales-tax.md).                                                                                 |
| Einrichten von Mehrwertsteuerbehörden.                                   | Erforderlich. Mehrwertsteuerbehörden sind die Entitäten, denen Steuern gemeldet werden und an die abgeführt werden muss.    Weitere Informationen finden Sie unter [Einrichten der Mehrwertsteuerbehörden](tasks/set-up-sales-tax-authorities.md)                                                                                                                                          |
| Einrichten von Mehrwertsteuer-Abrechnungszeiträumen.                            | Erforderlich. Mehrwertsteuer-Abrechnungszeiträume enthalten Informationen darüber, wann und wie oft Mehrwertsteuer gemeldet und abgeführt werden muss. Sie werden zu einer Mehrwertsteuerbehörde zugeordnet.                                                                                                                                                       |
| Einrichten von Mehrwertsteuer-Erklärungscodes.                               | Diese Angabe ist optional. Mehrwertsteuer-Erklärungscodes können zu Mehrwertsteuercodes zugeordnet werden, um Beträge für mehrere Mehrwertsteuercodes unter einem Mehrwertsteuer-Erklärungscode zu melden. Weitere Informationen finden Sie unter [Einrichten der Mehrwertsteuer-Berichterstattungscodes](tasks/set-up-sales-tax-reporting-codes.md)                                         |
| Einrichten von Mehrwertsteuercodes.                                         | Erforderlich. Der Mehrwertsteuercode enthält die Steuersätze und die Berechnungsregeln für die Mehrwertsteuer. Mehrwertsteuercodes werden einem Mehrwertsteuer-Abrechnungszeitraum und eine Sachkontobuchungsgruppe zugeordnet. Weitere Informationen finden Sie unter [Einrichten der Mehrwertsteuer-Berichterstattungscodes](tasks/set-up-sales-tax-codes.md)                                |
| Mehrwertsteuergruppen einrichten.                                        | Erforderlich. Mehrwertsteuergruppen enthalten eine Liste der Verkaufscodes, die für die Partei (Debitor oder Kreditor) einer Buchung gelten. Für eine bestimmte Buchung legen die Überschneidung von Mehrwertsteuercodes in der Mehrwertsteuergruppe die Artikel-Mehrwertsteuergruppe für die Buchung fest.                  |
| Artikel-Mehrwertsteuergruppen einrichten.                                   | Erforderlich. Artikel-Mehrwertsteuergruppen enthalten eine Liste der Verkaufscodes, die für die Ressource (Produkt, Service, usw.) einer Buchung gelten. Für eine bestimmte Buchung legen die Überschneidung von Mehrwertsteuercodes in der Mehrwertsteuergruppe die Artikel-Mehrwertsteuergruppe für die Buchung fest. Weitere Informationen zum Einrichten von Steuergruppen finden Sie unter [Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen einrichten](tasks/set-up-sales-tax-groups-item-sales-tax-groups.md). |
| Einrichten von Mehrwertsteuerparametern auf den Anwendungsparameterseiten. | Erforderlich. Verschiedene Bereiche, wie Hauptbuch, Debitoren und Kreditoren, müssen Parameter für die Berechnung indirekter Steuern einrichten. Obwohl die meisten dieser Parameter Standardwerte haben, müssen diese geändert werden, um die Anforderungen des Unternehmens zu erfüllen.                                          |

## <a name="sales-tax-on-transactions"></a>Mehrwertsteuer auf Buchungen
Für jede Buchung (Auftrag/Einkaufsbelegpositionen, Erfassungen, usw.) müssen Sie eine Mehrwertsteuergruppe und eine Artikel-Mehrwertsteuergruppe eingeben, um die Mehrwertsteuer berechnen. Standardgruppen werden in den Masterdaten (beispielsweise Debitor, Kreditor, Artikel und Beschaffungskategorie) angegeben. Sie können jedoch die Gruppen einer Buchung manuell ändern. Beide Gruppen enthalten eine Liste der Mehrwertsteuercodes, und die Überschneidung der beiden Listen von Mehrwertsteuercodes bestimmt die Liste der geltenden Mehrwertsteuercodes für die Buchung. 

Bei jeder Buchung können Sie die berechnete Mehrwertsteuer suchen, indem Sie die Seite **Mehrwertsteuerbuchung** öffnen. Sie können die Mehrwertsteuer für eine Dokumentposition oder für das gesamte Dokument suchen. Für bestimmte Dokumente (z. B. Kreditorenrechnung und allgemeine Erfassungen) können Sie die berechnete Mehrwertsteuer anpassen, wenn im Originaldokument abweichende Beträge angezeigt werden.

## <a name="sales-tax-settlement-and-reporting"></a>Mehrwertsteuerausgleich und -erklärung
Die Mehrwertsteuer muss in den geregelten Intervallen an die Steuerbehörden gemeldet und abgeführt werden (monatsweise, quartalsweise, usw.). Sie können Steuerkonten für das Intervall ausgleichen und die Salden im Steuerverrechnungskonto (wie in den Sachkontobuchungsgruppen angegeben) ausgleichen. Sie können diese Funktion unter **Mehrwertsteuer abrechnen und buchen** Seite zugreifen. Sie müssen den Mehrwertsteuer-Abrechnungszeitraum angegeben, dass Mehrwertsteuer für ausgeglichen werden soll. 

Nachdem die Mehrwertsteuer bezahlt wurde, sollte der Saldo im Mehrwertsteuer-Abrechnungskonto gegen das Bankkonto ausgeglichen sein. Wenn die Mehrwertsteuerbehörde, die im Mehrwertsteuer-Abrechnungszeitraum angegeben ist, ist einem Kreditorenkonto zugeordnet. Der Mehrwertsteuersaldo wird als offene Kreditorenrechnung gebucht und kann im regulären Zahlungsvorschlag einbezogen werden.

## <a name="conditional-sales-tax"></a>Mehrwertsteuer nach vereinnahmten Geldern
Die Mehrwertsteuer nach vereinnahmten Geldern ist eine Mehrwertsteuer, die proportional zu dem tatsächlichen Betrag gezahlt wird, der auf eine Rechnung hin bezahlt wird. Im Gegensatz dazu wird die Standardmehrwertsteuer zur Zeit der Rechnungsstellung berechnet. Mehrwertsteuer nach vereinnahmten Geldern muss bezahlt an die Mehrwertsteuerbehörde abgeführt werden, wenn die Zahlung gebucht wird, nicht wenn die Rechnung gebucht wird. Wenn die Rechnung gebucht wird, muss diese Buchung im Bericht des Mehrwertsteuerbuchs erfasst werden. Die Buchung muss jedoch von der Mehrwertsteuervoranmeldung ausgeschlossen werden. 

Wenn Sie das Kontrollkästchen "Mehrwertsteuer nach vereinnahmten Geldern" im Formular "Hauptbuchparameter" auswählen, kann keine Mehrwertsteuer abgezogen werden, bis Sie die Rechnung bezahlt haben. Dies ist in einigen Ländern eine gesetzliche Bestimmung.

> [!NOTE]
> Beim Auswählen des Kontrollkästchens "Mehrwertsteuer nach vereinnahmten Geldern" müssen Mehrwertsteuercodes und Mehrwertsteuergruppen eingerichtet und auch Sachkontobuchungsgruppen zur Unterstützung der Funktion erstellt werden. |

###  <a name="example"></a>Beispiel

Sie begleichen Ihre Mehrwertsteuer jeden Monat. Am 15. Juni erstellen Sie eine Rechnung über 10.000 EUR plus Mehrwertsteuer erstellt.
-   Die Mehrwertsteuer beträgt 25 Prozent oder 25 EUR.
-   Die Zahlung ist am 30. Juli fällig.

In der Regel würden Sie 2.500 EUR im Juni an die Steuerbehörde überweisen müssen, wenn die Rechnung im Juni gebucht wird, obwohl die Zahlung noch nicht eingegangen ist. 

Wenn Sie jedoch eine Mehrwertsteuer nach vereinnahmten Geldern anwenden, begleichen Sie die Steuer erst, wenn Sie die Zahlung vom Debitor am 30. Juli erhalten.

### <a name="postdated-check"></a>Vordatierter Scheck

Wenn Sie vordatierte Schecks als Zahlungsmethode verwenden, wenn die Zahlung erstellt wird, wird das Bankkonto nicht ausgeglichen. In einigen Ländern wird die Mehrwertsteuer zu 'realisierten' Verbindlichkeiten, wenn die Zahlung bei der Bank eingeht, was bedeutet, dass der vordatierte Scheck ausgeglichen wird. Sie können es aktivieren, indem Sie **Die bedingte Steuer realisieren, wenn vordatierte Schecks gezogen werden** in **Bargeld- und Bankverwaltung > Einstellungen > Bargeld- und Bankverwaltungsparameter > Vordatierte Schecks** auswählen.

Weitere Informationen finden Sie unter [Einrichten der Quellensteuer](tasks/set-up-withholding-tax.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
