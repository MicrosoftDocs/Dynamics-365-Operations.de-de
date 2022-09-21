---
title: Preiseinstellungen
description: Dieser Artikel beschreibt die verschiedenen Einstellungen für die Verwaltung von Preisen und Rabatten in Microsoft Dynamics 365 Commerce headquarters.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-11
ms.openlocfilehash: 79130e0ef285d6bd5e544f2d6a6368c0393fa7fa
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474041"
---
# <a name="pricing-settings"></a>Preiseinstellungen

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die verschiedenen Einstellungen für die Verwaltung von Preisen und Rabatten in Microsoft Dynamics 365 Commerce headquarters. Mit diesen Einstellungen können Organisationen das Preisverhalten in ihrer E-Commerce-Lösung festlegen, um bestimmte Geschäftsanforderungen zu erfüllen.

## <a name="company-level-pricing-settings"></a>Preiseinstellungen auf Unternehmensebene

Die meisten Preiseinstellungen finden sich auf Unternehmensebene und zwar unter **Handelsparameter \> Preise und Rabatte** in der Commerce headquarters.

### <a name="best-price-and-compound-concurrency-control-model"></a>Bester Preis und Steuerelementmodell für Kombinationsparallelität

Die Einstellung **Bester Preis und Steuerelementmodell für Kombinationsparallelität** bestimmt, wie das Preismodul mehrere Rabatte in **Bester Preis** oder **Verbindungs**-Parallelitätsmodus. 

Wenn der Parameter auf **Bester Preis und Verbund innerhalb der Priorität, nie Verbund über Prioritäten hinweg** eingestellt ist, sind alle **Kombinations** rabatte, die dieselbe Preisgestaltungspriorität haben, verbunden. Das kombinierte Ergebnis konkurriert dann mit allen Rabatten vom Typ **Bester Preis**, die dieselbe Preisgestaltungspriorität haben, wird der beste Preis angewendet, und alle Rabatte mit einer niedrigeren Preisgestaltungspriorität werden ignoriert.

Wenn der Parameter auf **Bester Preis nur innerhalb der Priorität, immer im Verbund über Prioritäten hinweg** eingestellt ist, werden alle **Kombinations** rabatte wie **Bester Preis** Rabatte behandelt. Innerhalb einer Preisgestaltungspriorität gewinnt nur ein einziger Rabatt. Wenn dieser einzelne Rabatt ein **Bester Preis** oder **Kombinations** rabatt ist, wird er mit allen anderen **Bester Preis** oder **Kombinations** rabatten kombiniert, die eine niedrigere Preisgestaltungspriorität haben.

### <a name="discount-compound-behavior"></a>Rabattkombinationsverhalten

Die Einstellung **Rabattkombinationsverhalten** bestimmt, wie das Preismodul mehrere Kombinationsrabatte berechnet.

Wenn der Parameter auf **Verbund** einstellt ist, wird ein Rabatt kumulativ zusätzlich zu einem anderen angewendet. Wenn **Verbund auf den ursprünglichen Preis** einstellt ist, werden alle Rabatte unabhängig voneinander behandelt und auf den gleichen ursprünglichen Preis angewendet.

Angenommen Sie möchten zum Beispiel 10 % und 20 % Rabatt für ein Produkt mit einem ursprünglichen Preis von 100 $ zusammensetzen. Wenn Sie den Parameter **Rabattkombinationsverhalten** auf **Verbund** einstellen, beträgt der Endpreis 72 $ (100 $ &times; 90 % &times; 80 %). Wenn Sie ihn auf **Verbund auf den ursprünglichen Preis** einstellen, beträgt der Endpreis 70 $ (100 $ – 10 $ – 20 $).

### <a name="enable-competition-between-exclusive-threshold-and-other-periodic-discounts"></a>Wettbewerb zwischen exklusiven Rabattschwellenwerten und anderen periodischen Rabatten aktivieren

Wenn der Parameter **Wettbewerb zwischen exklusiven Rabattschwellenwerten und anderen periodischen Rabatten aktivieren** auf **Ja** eingestellt ist, lässt das Preismodul exklusive Rabattschwellenwerte mit exklusiven Nicht-Rabattschwellenwerten konkurrieren. Die Preisgestaltungspriorität gilt weiterhin. Das Verhalten von Rabattschwellenwerten vom Typ **Bester Preis** und **Verbund** bleibt unverändert. Mit anderen Worten, sie konkurrieren nicht mit den Rabattschwellenwerten

### <a name="manual-line-discount-and-system-discount"></a>Manueller Positionsrabatt und Systemrabatt

Die Einstellung **Manueller Positionsrabatt und Systemrabatt** bestimmt, wie das Preismodul einen manuellen Positionsrabatt und einen Systemrabatt auf dieselbe Position anwendet. Der manuelle Positionsrabatt kann auf den Systemrabatt aufgeschlagen werden oder den Systemrabatt ersetzen. Wenn der manuelle Positionsrabatt und der Systemrabatt kombiniert werden, berücksichtigt die Berechnungslogik die Einstellung **Rabattkombinationsverhalten**. Ein manueller Rechnungsrabatt, der für die gesamte Bestellung gilt, berücksichtigt diese Einstellung nicht.

### <a name="keep-items-on-the-same-sales-line-for-discount-price-rounding"></a>Artikel in der gleichen Verkaufszeile für das Runden von Preisrabatten behalten

Manchmal kann der Betrag eines Mengenrabatts nicht gleichmäßig durch die anrechenbare Menge geteilt werden (z. B. wenn der Rabattbetrag 10 $ Abzug für drei gekaufte Einheiten beträgt). In diesen Fällen bestimmt die Einstellung **Artikel in der gleichen Vertriebszeile für das Runden von Preisrabatten behalten**, wie das Preismodul den Rabattbetrag anwendet und verteilt. Wenn der Parameter auf **Ja** eingestellt ist, wird der Rabattbetrag als Ganzes angewendet und nicht geteilt. Wenn es auf **Nein** festgelegt ist, wird der Rabattbetrag auf die anrechenbare Menge aufgeteilt und gerundet. Beispielsweise wird ein Rabattbetrag von 10 $ Rabatt für drei Einheiten 3,33 $ Rabatt für die erste Einheit, 3,33 $ Rabatt für die zweite Einheit und 3,34 $ Rabatt für die dritte Einheit aufgeteilt.

### <a name="apply-discounts-to-key-in-price-products"></a>Rabatte auf „Preis eingeben“-Produkte anwenden

Die Einstellung **Rabatte auf „Preis eingeben“-Produkte anwenden** legt fest, ob Rabatte zusammen mit Preisen vom Typ „Preis eingeben“ angewendet werden können, die in der Verkaufsstelle (POS) eingegeben werden. Die Einstellung **Preis eingeben** in der Produktkonfiguration bestimmt, ob und wie ein Produkt „Preis eingeben“ unterstützt.

### <a name="apply-discounts-to-price-overrides"></a>Rabatte auf Preisüberschreibungen anwenden

Die Einstellung **Rabatte auf Preisüberschreibungen anwenden** bestimmt, ob Rabatte zusammen mit Preisüberschreibungen angewendet werden können.

### <a name="distribute-discounts-for-least-expensive-discounts"></a>Rabatte für die günstigsten Rabatte verteilen

Für Rabatte für Angebots-Sortiment, die den Berechnungstyp „am günstigsten“ verwenden, bestimmt die Einstellung **Rabatte für die günstigsten Rabatte verteilen**, ob das Preismodul den Rabatt auf die Positionen verteilt.

Wenn der Parameter auf **Nein** eingestellt ist, wird der Rabatt nur auf die günstigsten Positionen angewendet. Zum Beispiel ist bei einem Rabatt für Angebots-Sortiment vom Typ „Kauf 2, bekomme 1 gratis“ der günstigste Artikel kostenlos und die anderen beiden Artikel bleiben zum vollen Preis. In diesem Fall erhält ein Kunde, der beide Artikel zum vollen Preis zurückgibt, den dritten Artikel trotzdem kostenlos. Dieses Szenario könnte zu einem Verlust für den Einzelhändler führen.

Wenn der Parameter auf **Ja** eingestellt ist, verteilt das Preismodul den Rabatt auf alle zutreffenden Positionen. Diese Einstellung kann dazu beitragen, den Verlust bei Rückgaben zu reduzieren.

### <a name="manually-calculate-multi-line-prices-and-discounts"></a>Manuelle Berechnung von Mehrzeilenpreisen und -rabatten

Die Einstellung **Mehrzeilige Preise und Rabatte manuell berechnen** steuert, ob das Preismodul eine verzögerte Preis- und Rabattberechnung für die POS-Anwendung und den Callcenter-Kanal verwendet. Wenn der Parameter auf **Ja** eingestellt ist, berechnet das Preismodul nicht sofort mehrzeilige Rabatte (z. B. Mengenrabatte, Rabattschwellenwerte und Rabatte für Angebots-Sortiment), wenn ein Auftrag in der POS-Anwendung oder im Callcenter-Kanal erstellt oder bearbeitet wird.

> [!NOTE]
> In Commerce-Version 10.0.30 und früher steuert die Einstellung **Mehrzeilige Preise und Rabatte manuell berechnen** nur den Callcenter-Kanal. Eine separate Einstellung **Mehrere Artikelrabatte manuell berechnen** im Funktionsprofil steuert das Preisberechnungsverhalten in der POS-Anwendung. In Commerce-Version 10.0.31 werden die beiden Einstellungen zu einer Einstellung auf Unternehmensebene konsolidiert.

### <a name="retention-period-in-days"></a>Aufbewahrungszeitraum in Tagen

Die Einstellung **Aufbewahrungsdauer in Tagen** gibt an, wie viele Tage nach dem Ablaufdatum (falls ein Ablaufdatum festgelegt ist) oder dem Deaktivierungsdatum (falls kein Ablaufdatum festgelegt ist) ein Rabatt systematisch gelöscht werden soll. Wenn der Parameter auf **0** (null) eingestellt ist, erfolgt keine automatische Löschung.

> [!NOTE]
> In Commerce-Version 10.0.30 und früher heißt diese Einstellung **Anzahl der Tage, nach denen die abgelaufenen Rabatte gelöscht werden sollen**.

### <a name="coupon-bar-code"></a>Couponstrichcode

Die Einstellung **Couponstrichcode** legt fest, welcher Strichcode zum Generieren von Couponstrichcodes verwendet wird. Die Benutzer können einen der vordefinierten Strichcodes auswählen, die auf der Seite **Strichcode einrichten** konfiguriert sind. Weitere Informationen zu Strichcodes und Strichcodemasken finden Sie unter [Strichcodes einrichten](set-up-bar-codes.md) und [Strichcodemasken einrichten](set-up-bar-code-masks.md).

### <a name="coupon-code-must-be-manually-applied-to-return-transactions"></a>Couponcode muss bei Retourenbuchungen manuell angewendet werden

Die Einstellung **Couponcode muss bei Retourenbuchungen manuell angewendet werden** gilt nur für Retourenbuchungen, für die kein Kaufbeleg bereitgestellt wird. Stellen Sie den Parameter auf **Nein**, ob Couponcodes automatisch auf die Buchung angewendet werden sollen. Stellen Sie ihn auf **Ja**, wenn Couponcodes manuell zur Buchung hinzugefügt werden müssen.

### <a name="use-sales-agreements-set-up-for-the-organization"></a>Für die Organisation festgelegte Kaufverträgen verwenden

Für Business-to-Business-(B2B-)Aufträge, wenn der Parameter **Für die Organisation festgelegte Kaufverträgen verwenden** auf **Ja** gesetzt ist, verwendet das Preismodul die Kaufverträge, die für die Organisation in der Kundenhierarchie des Benutzers definiert sind, um den vertragsbasierten Preis zu bestimmen. Wenn der Parameter auf **Nein** eingestellt ist oder wenn die Kundenhierarchie nicht festgelegt ist, sucht das Preismodul nach Kaufverträgen, die für den Benutzer festgelegt sind, um den vertragsbasierten Preis zu bestimmen. Weitere Informationen zu Kundenhierarchien für B2B-E-Commerce finden Sie unter [B2B-Geschäftspartner mithilfe von Kundenhierarchien verstehen](b2b/partners-customer-hierarchies.md).

## <a name="channel-level-pricing-settings"></a>Preiseinstellungen auf Kanalebene

Die folgenden Einstellungen ermöglichen es Organisationen, das Preisverhalten in bestimmten Verkaufskanälen zu steuern.

### <a name="enable-order-price-control"></a>Auftragspreissteuerung aktivieren

Der Parameter **Auftragspreissteuerung aktivieren** befindet sich auf dem Inforegister **Allgemein** der Seite **Callcenter-Konfiguration**. Die Einstellung bestimmt, ob das Preismodul eine Einschränkung für den Preisüberschreibungsvorgang im Callcenter-Kanal erzwingt. Es funktioniert in Verbindung mit der Einstellung **Preisregulierung zulassen** auf Produktebene.

Wenn die Auftragspreissteuerung deaktiviert ist, kann jeder Callcenter-Benutzer Preisänderungen an Verkaufspositionen im Callcenter-Kanal vornehmen, unabhängig davon, ob entsprechende Produkte eine Preisregulierung zulassen.

Wenn die Auftragspreissteuerung aktiviert ist, lassen nur Produkte, bei denen der Paramter **Preisregulierung zulassen** auf **Ja** eingestellt Preisüberschreibungen in Verkaufsaufträgen für Callcenter-Kanäle zu und in den entsprechenden Verkaufspositionen muss ein Ursachencode angegeben werden. Ein Callcenter-Benutzer kann den Verkaufspreis nur bis zum Wert **Kostenaufschlag in Prozent** ändern, der unter **Einzelhandel und Handel \> Kanaleinstellung \> Callcenter-Einstellung \> Berechtigungen überschreiben**. Wenn eine Preisüberschreibung diesen Prozentsatz überschreitet, muss der Benutzer eine Anforderung stellen, die dann durch einen voreingestellten Handelsworkflow zur Bewertung und Genehmigung verarbeitet wird. Weitere Informationen über das Erstellen von Handelsworkflows finden Sie unter [Workflow-Systemübersicht](/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system).

## <a name="product-level-pricing-settings"></a>Preiseinstellungen auf Produktebene

Die folgenden Einstellungen erzwingen Preisregeln auf Produktebene und befinden sich auf der Seite **Produktkonfiguration** der Organisation.

### <a name="allow-price-adjust"></a>Preisregulierung zulassen

Wenn der Parameter **Preisregulierung zulassen** auf **Ja** eingestellt ist, kann eine Preisüberschreibung auf das Produkt in Verkaufsaufträgen für Callcenter-Kanäle angewendet werden.

### <a name="key-in-price"></a>Preis eingeben

Die Einstellung **Preis eingeben** legt fest, ob eine Preiseingabe obligatorisch ist, wenn ein Produkt zu einer Verkaufsbuchung in POS hinzugefügt wird. Es definiert auch entsprechende Preiswertbeschränkungen.

### <a name="zero-price-valid"></a>Nullpreis gültig

Die Einstellung **Nullpreis gültig** legt fest, ob voreingestellte, vom System berechnete oder manuell angepasste Verkaufspreise für ein Produkt 0 (null) sein können. Stellen Sie den Parameter auf **Ja** fest, wenn ein Preis von null erlaubt ist. Diese Einstellung kann auch auf der Ebene der Kategorie aus der Handelsprodukthierarchie heraus angegeben werden.

### <a name="prevent-all-discounts"></a>Alle Rabatte verhindern

Wenn Sie den Parameter auf **Alle Rabatte verhindern** auf **Ja** einstellen, verhindern Sie, dass irgendwelche Rabatte (einschließlich manueller Rabatte) auf ein Produkt angewendet werden. Diese Einstellung kann auch auf der Ebene der Kategorie aus der Handelsprodukthierarchie heraus angegeben werden.

> [!NOTE]
> Diese Einstellung schränkt nicht den Preisüberschreibungsvorgang ein, da dieser Vorgang den Preis festlegt und nicht als Rabatt behandelt wird.

### <a name="prevent-manual-discounts"></a>Manuelle Rabatte verhindern

Wenn Sie den Parameter auf **Manuelle Rabatte verhindern** auf **Ja** einstellen, verhindern Sie, dass manuelle Positions- oder Buchungsrabatte auf ein Produkt angewendet werden. Alle anderen Rabatte können weiterhin angewendet werden. Diese Einstellung kann auch auf der Ebene der Kategorie aus der Handelsprodukthierarchie heraus angegeben werden.

> [!NOTE]
> Diese Einstellung schränkt nicht den Preisüberschreibungsvorgang ein, da dieser Vorgang den Preis festlegt und nicht als Rabatt behandelt wird.

### <a name="prevent-retail-discounts"></a>Einzelhandelsrabatte verhindern

Wenn der Parameter **Einzelhandelsrabatte verhindern** auf **Ja** eingestellt ist, können keine **einfachen** oder **Mengen** rabatte, Rabatt **schwellenwerte**, Rabatte für **Angebotssortiment** und **Versand** rabatte können nicht auf ein Produkt angewendet werden. Alle anderen Rabatte (einschließlich manueller Rabatte) können weiterhin angewendet werden.

### <a name="prevent-tender-based-discounts"></a>Zahlungsmittelbasierte Rabatte verhindern

Wenn der Parameter **Zahlungsmittelbasierte Rabatte verhindern** auf **Ja** eingestellt ist, kann auf das Produkt kein **zahlungsmittelbasierter** Rabatt angewendet werden. Alle anderen Rabatte (einschließlich manueller Rabatte) können weiterhin angewendet werden.

Einzelhändler entscheiden sich häufig, einige Produkte, wie neue Artikel oder gefragte Artikel, von artikelbasierten Rabatten (wie einfachen Rabatten und Mengenrabatten) auszunehmen. Vielleicht möchten sie aber trotzdem zahlungsmittelbasierte Rabatte anwenden, wenn der Kunden jedoch mit dem bevorzugten Zahlungsmittel bezahlt. Um dieses Ergebnis zu erreichen, können Einzelhändler die Parameter **Alle Rabatte verhindern** und **Zahlungsmittelbasierte Rabatte** auf **Nein** festlegen und die Parameter **Einzelhandelsrabatte verhindern** und **Manuelle Rabatte verhindern** auf **Ja**.

## <a name="deprecated-or-removed-settings"></a>Veraltete und entferne Einstellungen

Die folgenden Preiseinstellungen wurden entfernt bzw. sollen demnächst aus Dynamics 365 Commerce entfernt werden.

| Einstellung | Gründung für das Veralten oder Entfernen | Veralteter oder entfernter Status |
|---------|-----------------------------------|-------------------------------|
| Abwicklung sich überschneidender Rabatte | Wir haben diese Einstellung in den Handelsparametern bereitgestellt, damit Sie steuern können, wie das Preismodul nach der besten anzuwendenden Rabattkombination sucht und diese bestimmt. Die Option **Bester Rabatt** erzwingt während der Preiskalkulation alle möglichen Rabattkombinationen. Die Option **Optimale Leistung** eine optimierte Option, die einen erweiterten Heuristikalgorithmus und die Methode Schwellenwertklassifizierung verwendet, um die beste Rabattkombination rechtzeitig zu priorisieren, zu bewerten und zu bestimmen. Die Option **Ausgeglichene Kalkulation** in der aktuellen Codebasis funktioniert genauso wie die Option **Beste Leistung**. Daher ist es im Wesentlichen eine duplizierte Option. Um die Leistung zu verbessern, wurde das Preismodul so aktualisiert, dass es nur **Beste Leistung** als Standardoption verwendet. Daher ist diese Einstellung nicht mehr anwendbar. | Sie ist seit Release 10.0.21 veraltet und wird im Oktober 2022 entfernt. |
| Lassen Sie Preisregulierungen zu, um den Produktpreis zu erhöhen | Wir haben diese Einstellung bereitgestellt, um zu steuern, ob die Preisregulierungsfunktion Produktpreises erhöhen kann. Wenn der Parameter deaktiviert ist, können Organisationen die Preisregulierungsfunktion nur verwenden, um den Stückpreis eines Produkts so festlegen, dass er niedriger ist als der Grundpreis und der Verkaufspreis laut Kaufvertrag. Wir haben diese Einstellung veralten lassen, da die Preisregulierungsfunktion aktualisiert wurde, sodass sie Anpassungen in zwei Richtungen (Erhöhung oder Senkung) standardmäßig unterstützt. | Sie ist seit Release 10.0.30 veraltet und wird im Oktober 2023 entfernt. |
| Preisbericht für Einzelhandelsgeschäft aktivieren | Wir haben diese Einstellung bereitgestellt, damit Sie steuern können, ob die Funktion **Preisbericht** für die Verwendung auf der Seite „Shopkonfiguration“ verfügbar ist. Wir haben diese Einstellung veralten lassen, da die Seite „Shopkonfiguration“ aktualisiert wurde, sodass die Funktion **Preisbericht** standardmäßig zur Verfügung steht. | Sie ist seit Release 10.0.31 veraltet und wird im Oktober 2023 entfernt. |
| Das heutige Datum verwenden, um die Preise zu berechnen | Das Preismodul für Dynamics 365 Supply Chain Management unterstützt die Preiskalkulation basierend auf dem angeforderten Lieferdatum und dem angeforderten Wareneingangsdatum zusammen mit dem heutigen Datum. Das Preismodul von Commerce unterstützt nur die Preiskalkulation basierend auf dem heutigen Datum. Für Kunden, die sowohl Supply Chain Management- als auch Commerce-Funktionen verwenden, haben wir diese Einstellung bereitgestellt und empfohlen, dass Kunden sie immer auf **Ja** einstellen, sodass die beiden Preismodule zusammenarbeiten können. Wir haben diese Einstellung veralten lassen, da sie das Kalkulationsverhalten nicht grundlegend ändert und deshalb redundant ist. | Sie ist seit Release 10.0.31 veraltet und wird im Oktober 2023 entfernt. |
| Maximaler Preis | Wir haben diese Einstellung im Funktionsprofil bereitgestellt, um zu steuern, ob in bestimmten Geschäften nur Produkte über POS verkauft werden können, deren Verkaufspreis unter dem angegebenen Höchstpreis liegt. Wir haben diese Einstellung wegen geringer Featurenutzung verworfen. | Sie ist seit Release 10.0.31 veraltet und wird im Oktober 2023 entfernt. |
| Rabatte auf Preis je Einheit anwenden | Diese Einstellung sollte steuern, ob Preise und Rabatte bei der Preiskalkulation auf Stückpreisebene oder auf Verkaufspositionsebene gerundet werden. Wir haben es verworfen, weil es nirgendwo in der aktuellen Codebasis verwendet wird. | Sie ist seit Release 10.0.31 veraltet und wird im Oktober 2023 entfernt. |
| Mehrere Artikelrabatte manuell berechnen | Wir haben diese Einstellung bereitgestellt, um zu steuern, ob das Preismodul eine verzögerte Preiskalkulation für den Einzelhandelskanal verwendet. Wenn der Parameter auf **Ja** eingestellt ist, berechnet das Preismodul nicht sofort mehrzeilige Rabatte (z. B. Mengenrabatte, Rabattschwellenwerte und Rabatte für Angebots-Sortiment), wenn ein Auftrag in der POS-Anwendung erstellt oder bearbeitet wird. Wir haben uns entschieden, diese Einstellung mit einer ähnlichen Einstellung in den Handelsparametern zu konsolidieren, um eine Omnichannel-Steuerung zu ermöglichen. | Sie ist seit Release 10.0.31 veraltet und wird im Oktober 2023 entfernt. |

Eine vollständige Liste der entfernten oder veralteten Funktionen in Dynamics 365 Commerce finden Sie unter [Entfernte oder veraltete Funktionen in Dynamics 365 Commerce](get-started/removed-deprecated-features-commerce.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
