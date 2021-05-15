---
title: Callcenterkataloge
description: Dieses Thema beschreibt die spezifische Funktionalität für Callcenter für Kataloge in Dynamics 365 Commerce.
author: josaw1
ms.date: 05/15/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 3758ff51de8217a209b40d7dd461e42ea9632f0a
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936881"
---
# <a name="call-center-catalogs"></a>Callcenterkataloge

[!include [banner](includes/banner.md)]

Dieses Thema beschreibt die spezifische Funktionalität für Callcenter für Katalogfunktionen in Dynamics 365 Commerce.

Die Katalogfunktionen in Commerce können für verschiedene Zwecke genutzt werden. Ursprünglich wurden die Katalogfunktionen für die Unterstützung von E-Commerce-Integrationen von Drittanbietern entwickelt. Durch die Einrichtung des Katalogs konnten Unternehmen eine Gruppierung von Produkten und Attributen erstellen, die extern für die Nutzung durch eine E-Commerce-Lösung von einem Drittanbieters veröffentlicht werden konnten.

Als die Unterstützung von Callcenter-Kanälen hinzugefügt wurde, wurde das Katalogkonzept um zusätzliche Funktionen zur Unterstützung und Verwaltung von Funktionen im Zusammenhang mit herkömmlichen Direktmarketing-Katalogen erweitert. Ein Direct-to-Consumer-Unternehmen produziert oft gedruckte Kataloge, die dann an ein oder mehrere Kundensegmente verschickt werden. Diese Kataloge haben in der Regel spezifische Aktionen oder Angebote, die nur dann berücksichtigt werden, wenn der Kunde bei der Auftragserstellung einen Katalog-Identifikationscode angibt.

Direct-to-Consumer-Marketing-Unternehmen sind sehr darauf ausgerichtet, die Reaktion auf diese Kataloge zu verfolgen, um sicherzustellen, dass die Kosten für die Produktion und den Versand gerechtfertigt sind. Um die Antwort zu verfolgen, wird traditionell ein Code auf die Rückseite des Katalogs gedruckt und dieser Code wird dann angefordert und angewendet, wenn der Katalogempfänger anruft, um eine Bestellung per Telefon aufzugeben (oder jetzt kann der Code traditionellerweise eingegeben werden, wenn der Kunde eine Bestellung online aufgibt). Während es verschiedene Branchenbegriffe gibt, die verwendet wurden, um diesen Katalogverfolgungscode zu identifizieren (einschließlich Schlüsselcode, Promo-Code, Katalogcode, Quellcode), bezeichnen wir den Code in Commerce als **Quellcode-ID**.

## <a name="basic-catalog-setup"></a>Grundlegende Katalogeinrichtung

Gehen Sie zu **Einzelhandel und Handel**\> **Kataloge und Sortimente** \> **Alle Kataloge**, um Ihren Katalog zu konfigurieren.

Wenn Sie einen neuen Katalog anlegen, müssen Sie diesen zunächst mit einem oder mehreren Kanälen verknüpfen. Dies geschieht im Inforegister **Commerce-Kanäle** im Formular **Katalogeinrichtung**. Klicken Sie auf **Hinzufügen** und wählen Sie einen oder mehrere Kanäle aus. Nur Artikel, die mit dem ausgewählten Kanal [Sortimente](/dynamics365/unified-operations/retail/assortments) verknüpft sind, können bei der Erstellung des Katalogs verwendet werden.

Um Produkte in einen Katalog aufzunehmen, muss eine Navigationshierarchie gewählt werden. Die Navigationshierarchie unterstützt die Kategoriestruktur für den Katalog. Sie müssen aus einer der Navigationshierarchien wählen, die mit den ausgewählten Kanäle auf dem Inforegister **Commerce-Kanäle** der Seite **Katalog** verknüpft sind. Wenn ein Navigationskanal vorher nicht mit einem Kanal verknüpft war, gehen Sie zu **Einzelhandel und Handel** \>**Kanaleinrichtung**\>**Kanalkategorien und Produktattribute**, um eine Navigationshierarchievorgabe mit jedem Ihrer Einzelhandelskanäle zu verknüpfen.

Klicken Sie auf der Menüregisterkarte **Kataloge** auf der Seite **Katalogeinrichtung** auf **Produkte hinzufügen**, um die Produkte zu konfigurieren, die dem Katalog hinzugefügt werden sollen, oder wählen Sie einen Knoten in der Navigationshierarchie aus (die Auswahl eines Knotens ändert die Bildschirmdarstellung und ermöglicht Ihnen, Produkte direkt zu einer Kategorie innerhalb des Katalogs hinzuzufügen)

Klicken Sie auf den obersten Knoten der Kataloghierarchie, um in die Kopfansicht des Hauptkatalogs zurückzukehren. Konfigurieren Sie das Gültigkeits- und Ablaufdatum nach Bedarf auf der Seite **Allgemein** Inforegister.

Bevor der Katalog verwendet werden kann, muss er veröffentlicht werden. Klicken Sie auf **Katalog überprüfen** im Menü **Kataloge**, um die Prüfung zu verarbeiten. Dies ist eine notwendige Aktivität und bestätigt, dass die erforderliche Einstellung korrekt ist. Klicken Sie auf **Ergebnisse anzeigen**, um die Details der Prüfung zu sehen. Wenn Fehler gefunden werden, müssen Sie die Daten korrigieren und die Prüfung erneut durchführen, bis die Prüfung abgeschlossen ist.

Nachdem die Prüfung bestätigt wurde, klicken Sie im Menü auf **Workflow**, um den Genehmigungs-Workflow zu starten. Klicken Sie auf **Senden** im Menü **Workflow**, um den Vorgang ausführen. Konfigurieren Sie die Schritte und berechtigten Benutzer für den Workflow von **Einzelhandel und Handel**\>**Headquarters-Einstellungen**\>**Commerce-Workflows**. Der Workflow definiert die Schritte, die notwendig sind, um den Katalog in den Status **Genehmigt** zu bringen. Wenn sich der Katalog im Status **Genehmigt** befindet, können Sie auf die Option **Veröffentlichen** im Menü **Kataloge** klicken, um den Vorgang abzuschließen. Nachdem der Katalog in einem Status **Veröffentlicht** ist, kann er in der Callcenterauftragserfassung verwendet werden und Katalogprozesse senden.

## <a name="use-catalogs-to-drive-sales-order-pricing-and-promotions"></a>Verwenden Sie Kataloge, um Auftragspreiskalkulation und verkaufsfördernde Maßnahmen voranzutreiben

Ein Hauptgrund für die Definition eines Katalogs, der mit einem Call Center verwendet werden soll, ist die Möglichkeit, bestimmte Preise und verkaufsfördernde Maßnahmen für diesen Katalog zu konfigurieren. Kunden, die aus diesem Katalog bestellen, erhalten diese Preise und Aktionen in der Call-Center-Auftragserfassung, wenn die **Quellcodekennung** des Katalogs auf den Auftragskopf oder die Auftragszeilen angewendet wird.

Um katalogspezifische Preise zu konfigurieren, wählen Sie die Option **Preisgruppen** auf der Registerkarte **Kataloge** aus, um eine oder mehrere Preisgruppen mit dem Katalog zu verknüpfen. Alle Handelsvereinbarungen, Preisregulierungserfassungen und Vorzugsrabatte (Schwellenwert, Menge, Mischung und Abgleich), die mit der gleichen Preisgruppe verknüpft sind, werden bei der Bestellung aus diesem Katalog angewendet.

Im Inforegister **Quellcodes** klicken Sie auf **Hinzufügen**, um eine oder mehrere **Quellcodekennung** Bezeichner zu diesem Katalog hinzuzufügen. Dies ist der Code, der bei der Call-Center-Auftragserfassung auf den Auftragskopf (und die Positionen) angewendet wird. Dieser Code wird verwendet, um den Auftrag mit dem Katalog und letztlich mit den Preisgruppen und eventuell konfigurierten Sonderpreisen und Aktionen zu verknüpfen.

## <a name="use-the-source-id-to-track-costs-and-response-rates"></a>Verwenden Sie die Quellenkennung, um Kosten und Rücklaufquoten zu verfolgen.

Bei der Definition der **Quellcodekennung** können Sie diese Kennung optional mit einer **Zielmarktkennung** verknüpfen. Die **Zielmarktkennung** kann unter **Einzelhandel und Handel** \> **Kunden** \> **Zielmarkt** definiert werden. Der Zielmarkt ist eine Liste der Kunden und/oder Interessenten, die zu einem benutzerdefinierten Segment gehören. Die Verknüpfung der Kunden- oder Interessentendaten mit der Quellcodekennung ermöglicht eine bessere Einsicht in die Empfänger des Katalogs. Wenn ein Kunde mit einem Zielmarkt verbunden ist und dieser Zielmarkt mit einer aktiven Quellcodekennung/Katalog verknüpft ist, können Call-Center-Benutzer sehen, welche Kataloge ein Kunde erhalten hat, indem sie den Menüpunkt **Quellcodes** auf der Registerkarte **Kunden** auf der Seite **Kundenservice** auswählen. Während der Auftragserfassung können Call-Center-Benutzer auch die spezifischen Kataloge sehen, die einem Kunden in der Dropdown-Liste **Quelle** auf dem Auftragsauftragskopf gesendet wurden. Das Ändern des Filters von **Alle** auf **Angestrebt** erlaubt dem Benutzer, die spezifischen aktiven Kataloge zu sehen, die dem Kunden gesendet wurde. Dies ist hilfreich, wenn der Kunde seinen Katalog vergessen hat oder den Katalogcode beim Anlegen eines Auftrags nicht finden oder lesen kann.

Es ist möglich, mehrere Quellcodekennungen mit einem Katalog zu verknüpfen. Dies ist häufig erforderlich, wenn ein Unternehmen die Antwortgeschwindigkeit nach verschiedenen Segmenten verfolgen möchte. Das Unternehmen gibt verschiedenen Kundensegmenten einen eindeutigen Katalogcode, der es ermöglicht, die Antwortgeschwindigkeit bis auf Segmentebene innerhalb eines bestimmten Katalogereignisses zu verfolgen.

Wenn Sie einen bestimmten **Quellcodekennung** Datensatz auswählen und auf die Option **Details** auf dem Inforegister **Quellcodes** klicken, werden zusätzliche Felder angezeigt, in denen Verkaufsprognosen, Versandkosten und Versanddaten erfasst werden können. Diese Daten sind hilfreich für eine detaillierte Analyse der Effektivität des Katalogs. Benutzer können im Laufe der Zeit zu dieser Seite zurückkehren und die Schaltflächen **Quellcodeanalyse** und **Aktionen vergleichen** verwenden, um analytische Berichte basierend auf aktuellen Verkaufsdaten auszulösen und Kosten und Budget mit Istwerten zu vergleichen.

## <a name="configure-catalog-specific-order-and-item-scripts"></a>Katalogspezifische Bestell- und Artikelskripte konfigurieren

Wenn ein Call-Center-Benutzer einen Auftrag anlegt, kann er Bildschirmskripte verwenden. Diese textbasierten Scripts können zusätzliche Informationen liefern, die der Benutzer dem Kunden mitteilen sollte, oder es können interne Notizen/Erinnerungen sein, die der Call-Center-Benutzer beim Anlegen des Auftrags überprüfen und darauf reagieren sollte.

Es ist oft von Vorteil, unterschiedliche Arten von Skripts für verschiedene Kataloge haben. Auf dem Inforegister **Skripts** können vordefinierten Skripts einem Katalog zugeordnet werden. Mit dem Feld **Zeitmessung** legen Sie fest, ob das Skript am Anfang des Auftrags (sobald die Quellcodekennung im Auftragskopf eingegeben wird) oder am Ende des Auftrags (im Auftragsübersichtsformular) erscheint.

Bei der Auswahl eines Knotens in der Kataloghierarchie und der Arbeit mit den Daten auf dem Inforegister **Produkte** können Benutzer auch katalog- oder artikelspezifische Skripte über die Aktion **Skripte** verknüpfen.

## <a name="configure-catalog-specific-up-sell-and-cross-sell-items"></a>Artikel für weiteren/ergänzenden Katalogverkauf konfigurieren

Die Verknüpfung von weiteren/ergänzenden Verkaufsvorschlägen mit einem Artikel kann über das Produkt-Setup erfolgen, aber in einigen Fällen möchte ein Unternehmen spezielle weitere/ergänzende Verkaufsartikel an Kunden verkaufen, die ein bestimmtes Produkt aus einem bestimmten Katalog bestellen. Wählen Sie im Inforegister **Produkte** einen Artikel aus und klicken Sie auf **Weiterer/ergänzender Verkauf von Artikeln**, um Produkte zu konfigurieren, die an Kunden, die den ausgewählten Artikel aus dem Katalog kaufen, verkauft werden sollen. Während der Call-Center-Auftragserfassung werden katalogspezifische weitere/ergänzende Verkaufsartikel für einen Artikel auf dem Bildschirm angezeigt, anstelle von weiteren/ergänzenden Standardprodukten, die für diesen Artikel über die übliche Produktkonfiguration konfiguriert worden sind.

Weitere/ergänzende Verkaufsartikel können auch die Skriptfunktionen nutzen, um bestimmte Meldungen anzuzeigen, die ein Benutzer sieht, wenn der weitere/ergänzende Verkaufsartikel während der Auftragserfassung angezeigt wird. Scripts, die an weitere/ergänzende Produkte gebunden sind, die speziell für ein Katalogprodukt konfiguriert wurden, werden nur angezeigt, wenn der Quellcode dieses Katalogs in der Call-Center-Auftragserfassung verwendet wird.

## <a name="catalog-page-analysis"></a>Katalogseitenanalyse

Auf der Registerkarte **Kataloge** stehen Optionen zur Verfügung, um **Katalogseiten** zu konfigurieren. Mit dieser Funktion können Sie bestimmte Seiten und Seitentypen für den gedruckten Katalog und die ihnen zugeordneten Kosten definieren.

Wenn Sie die Produkte im Katalog konfigurieren, verwenden Sie die Aktivität **Produktseitenlayout**, um die spezifischen Seiten, den Prozentsatz der Seite und die Position der Seitendetails für den Artikel zu definieren. Die Konfiguration dieser Daten ermöglicht es den Benutzern, die Vorteile des **Katalogbereichsanalyse-Bericht** zu nutzen. Dieser Bericht wird gefunden, indem Sie zu **Einzelhandel und Handel** \> **Callcenter-Berichte** \> **Katalogbereichsanalyse**-Bericht navigieren. Dieser Bericht analysiert die Verkäufe gegen den Katalog (Aufträge, bei denen die Quellkennung für den Katalog an den Auftragskopf oder die Auftragszeile gebunden war) und die damit verbundenen Seiten- und Kostenanteile, um einen traditionellen Direktmarketing- **Quadratzollanalyse**-Bericht zu erstellen.

## <a name="catalog-requests"></a>Kataloganforderungen

Da Kataloge in Commerce konfiguriert und veröffentlicht werden, kann die Funktion **Katalog senden** genutzt werden. Diese Funktion ist auf den Seiten **Kundensuche** und **Kundendienst** verfügbar. Nach der Auswahl eines Kundendatensatzes über **Kundensuche** oder während der Anzeige eines ausgewählten Kundenkontos über **Kundenservice** kann der Benutzer die Option **Katalog senden** auswählen, die ein Dialogfeld öffnet, in dem der Benutzer aus einer Liste aller veröffentlichten und aktiven Kataloge auswählen kann. Ein Benutzer kann einen Katalog und eine Menge sowie eine bestimmte Quellcodekennung zum Versenden auswählen. Wenn sie auf die Schaltfläche **Senden** klicken, wird eine Anforderung gespeichert, die dann durch Drucken des Berichts **Kataloganforderungen** verwaltet werden kann. Dieser Bericht wird gefunden, indem Sie zu **Einzelhandel und Handel** \> **Callcenter-Berichte** \> **Bericht „Kataloganforderungen”** navigieren. Er listet alle Kataloganforderungen auf, einschließlich des Kundennamens und der Adressdaten des Kunden, der den Katalog angefordert hat. Dieser Report kann intern verwendet werden oder die Daten können auch an eine dritte Partei übermittelt werden, die externe Prozesse zur physischen Versendung des Katalogs an den Kunden unterstützt.

## <a name="additional-features"></a>Zusätzliche Funktionen

Auf der Registerkarte **Kataloge** sind auch Optionen zur Konfiguration eines **Zahlungsplans** und **Kostenlose Produkte** verfügbar. Wenn die mit dem Katalog verknüpfte Quellcodekennung bei der Call-Center-Auftragserfassung verwendet wird, hat der Kunde Anspruch auf die kostenlosen Produkte oder die Nutzung der spezifischen Katalog-Zahlungspläne wie definiert. Wenn es notwendig ist, den Kunden darauf zu beschränken, nur aus den mit seinem Katalog verknüpften Zahlungsplänen auswählen zu können und nicht aus allen aktiven Zahlungsplänen im System, kann das Kontrollkästchen **Nur Katalogpläne zulassen** für eine oder mehrere der definierten Quellcodekennungen aktiviert werden, um diese Einschränkung durchzusetzen.

## <a name="additional-notes"></a>Weitere Hinweise

Derzeit wird eine Quellcodekennung für einen Kundenauftrag im Call Center verwendet, um Preise, Aktionen, Skripte und weitere/ergänzende Verkäufe, die katalogspezifisch sind, zu steuern. Das System verbietet oder verhindert nicht, daß ein Produkt, das nicht im Katalog enthalten ist, auf dem Auftrag bestellt wird. Wenn ein Artikel bestellt wird, der nicht Teil des Katalogs ist, verwendet das System zunächst die **Preisgruppe** die auf dem Callcenterkanal definiert ist (**Einzelhandel und Handel** \>**Kanäle** \> **Callcenter** \> **Alle Callcenter**) für Artikelpreise oder Aktionen. Wenn kein bestimmter Kanalpreis gefunden wird, wird der Basisverkaufspreis des Artikels verwendet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]