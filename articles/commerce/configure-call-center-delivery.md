---
title: Callcenter-Lieferarten und -Belastungen konfigurieren
description: In diesem Artikel wird beschrieben, wie Sie in Dynamics 365 Commerce Lieferarten und Gebühren für einen Callcenter-Auftrag einrichten.
author: josaw1
ms.date: 04/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f445e9dabd0210951609170369eae63bcc30ce6b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888297"
---
# <a name="configure-call-center-delivery-modes-and-charges"></a>Konfigurieren von Callcenter-Lieferarten und -Belastungen

[!INCLUDE [banner](includes/banner.md)]

Wenn ein Auftrag in Dynamics 365 Commerce erteilt wird und die Person, die den Auftrag eingegeben hat, mit einem Callcenterkanal verknüpft ist, werden Logik und Regeln verwendet, um die Art der Lieferung (Lieferart) zu validieren und die Gebühren für den Auftrag zu berechnen.

Wenn Sie einen Auftrag erstellen, können Sie eine Lieferart im Auftragskopf und den Auftragspositionen auswählen. Standardmäßig wird für alle Auftragspositionen der Lieferungsmodus verwendet, den Sie in der Kopfzeile wählen. Sie können jedoch den Standardlieferungsmodus auf einzelnen Verkaufspositionen nach Bedarf überschreiben. Sie können auch eine Lieferart auf einem Kundendatensatz definieren. Wenn dann Aufträge für den Kunden angelegt werden, wird diese Lieferart standardmäßig auf dem Auftragskopf verwendet.

Commerce verfügt über Funktionen, mit denen Benutzer die Lieferarten, die von einem Kanal verwendet werden können, die Lieferarten, die für ein Produkt verwendet werden können, und die Lieferarten, die für bestimmte Versandziele gültig sind, einschränken können. Zuschläge können auch so definiert werden, dass zusätzliche Gebühren zu einem Auftrag hinzugefügt werden, basierend auf den Lieferarten, die für den Auftrag ausgewählt wurden und dem Gesamtauftragswert.

## <a name="define-delivery-modes"></a>Lieferarten definieren

Bevor Sie festlegen, welche Zustellarten für Callcenter-Aufträge verwendet werden können und die zugehörigen Regeln und Gebühren definieren, müssen Sie die Lieferarten definieren. Gehe zu **Vertrieb und Marketing \> Einstellungen \> Vertrieb \> Lieferarten**. Wählen Sie **Neu**, um eine neue Lieferart zu erstellen. Alternativ können Sie in der Liste eine vorhandene Lieferart auswählen und dann **Bearbeiten** wählen, um Änderungen vorzunehmen.

Im Feld **Lieferart** können Sie je nach Geschäftsanforderung eine beliebige Kombination alphanumerischer Zeichen eingeben. Sie können dann das Feld **Beschreibung** verwenden, um zusätzlichen Kontext bereitzustellen. Die Felder **Gruppe der sonstigen Zuschläge** und **Eillieferung** sind optional und werden später in diesem Artikel näher erläutert.

Fügen Sie auf dem Inforegister **Commerce-Kanäle** einen beliebigen Kanal hinzu, der beim Anlegen von Verkaufstransaktionen in diesem Kanal den Liefermodus verwenden darf.

Auf dem Inforegister **Produkte** können Sie festlegen, für welche Produkte und/oder Produktkategorien die Lieferart verwendet werden kann und für welche nicht. Wenn z.B. ein Produkt aufgrund von Gefahrgutbeschränkungen nicht auf dem Luftweg transportiert werden kann, stellen Sie sicher, dass das Produkt oder die Produktkategorie von allen Lieferarten, die den Lufttransport betreffen, ausgeschlossen ist.

Auf dem Inforegister **Adressen** können Sie angeben, für welche Länder oder Regionen bzw. Staaten die Lieferart verwendet werden kann und für welche nicht. Zum Beispiel sind Bestellungen, die nach Hawaii oder Alaska verschickt werden, nicht für die Lieferung am Boden geeignet. Daher sollten diese Staaten von jeder Lieferart ausgeschlossen werden, die mit einem Bodenlieferdienst verbunden ist, aber in jeder Lieferart eingeschlossen, die mit einem Luftlieferdienst verbunden ist.

## <a name="validate-delivery-modes-for-a-call-center-order"></a>Lieferarten für einen Callcenter-Auftrag überprüfen

Nachdem die Lieferarten definiert sind, müssen Sie den Batchauftrag **Lieferarten verarbeiten** ausführen. Dieser Job stellt die Lieferarten zur Verfügung, damit sie in Auftragsprozessen für Kanäle verwendet werden können. Um den Job **Lieferarten verarbeiten** auszuführen, gehen Sie zu **Retail and Commerce \> Retail and Commerce \> Lieferarten verarbeiten**. Dieser Einzelvorgang sollte immer dann ausgeführt werden, wenn neue Lieferarten zu einem Kanal hinzugefügt oder Änderungen an bestehenden Lieferarten/Kanalbeziehungen vorgenommen werden.

Nachdem Sie den Batchauftrag **Lieferarten verarbeiten** ausführen, können Sie zu **Retail and Commerce \> Kanäle \> Callcenter \> Alle Callcenter** wechseln. Auf der Seite **Alle Callcenter** im Aktivitätsbereich auf der Registerkarte **Einrichtung** wählen Sie **Lieferarten**. Die Seite **Lieferarten** listet alle gültigen Lieferarten für den ausgewählten Callcenterkanal auf. Um bestehende Lieferarten zu bearbeiten oder neue Lieferarten hinzuzufügen, wählen Sie **Lieferarten verwalten**. Beachten Sie, daß der Einzelvorgang **Lieferarten verarbeiten** bei jeder Änderung ausgeführt werden muß.

## <a name="define-charges-for-delivery-services"></a>Gebühren für Lieferdienste definieren

Wenn Aufträge für Kunden angelegt werden, möchte ein Unternehmen möglicherweise Gebühren hinzufügen, die automatisch auf der Grundlage der für den Auftrag ausgewählten Lieferarten berechnet werden. Diese Gebühren können so konfiguriert werden, dass sie für alle Kunden und Lieferarten gleich sind. Alternativ können die Gebühren je nach Kunde und/oder Lieferart, die für den Auftrag ausgewählt wurden, variieren.

Um die Gebühren zu definieren, gehen Sie zu **Retail and Commerce \> Kanaleinstellungen \> Gebühren \> Auto-Belastungen**. Wählen Sie **Neu** aus, um neue Gebühren hinzuzufügen. Alternativ können Sie einen vorhandenen Eintrag markieren und dann **Bearbeiten** wählen.

Gebühren können so definiert werden, dass sie entweder auf der Ebene des Auftragskopfes oder der Auftragspositionen berechnet werden. Verwenden Sie das Feld **Ebene**, um die gewünschte Ebene auszuwählen.

Gebühren können für einen bestimmten Kunden, eine Gruppe von Kunden oder alle Kunden definiert werden. Wählen Sie im Feld **Kontocode** **Tabelle**, um Gebühren zu definieren, die nur für einen bestimmten Kunden gelten. Wählen Sie **Gruppe**, um Gebühren für eine bestimmte Kundengruppe zu definieren. Wählen Sie **Alle**, um die Gebühren auf jeden Kunden anzuwenden, der einen Auftrag mit der entsprechenden Lieferart erteilt. Wenn Sie **Tabelle** oder **Gruppe** im Feld **Kontocode** gewählt haben, wählen Sie den Kunden oder die Kundengruppe im Feld **Kontenbeziehung** aus.

Zuschläge können so konfiguriert werden, dass sie für eine bestimmte Lieferart, eine Lieferartgruppe oder alle Lieferarten angewendet werden. Wenn Sie **Tabelle** im Feld **Lieferartcode** auswählen, müssen Sie eine bestimmten Lieferart im Feld **Lieferartbeziehung** auswählen. Wenn Sie **Gruppe** wählen, müssen Sie eine Lieferartgruppe im Feld **Lieferartbeziehung** auswählen. Lieferungsmodusgruppen werden unter **Retail and Commerce \> Kanaleinstellung \> Gebühren \> Gruppe für sonstige Lieferzuschläge** definiert. Sie können dann auf der Seite **Lieferarten** mit einer oder mehreren Lieferarten verknüpft werden. Wenn Sie bei der Definition von Gebühren eine Gruppe auswählen, verwendet jede Lieferart, die mit der ausgewählten Liefergruppe verknüpft ist, diese Gebühren. Wenn Sie schließlich **Alle** im Feld **Lieferartcode** wählen, verwenden alle Lieferarten die Gebühren. Daher wählen Sie keinen Wert im Feld **Lieferartbeziehung** aus.

Im Abschnitt **Positionen** können Sie je nach Bedarf eine oder mehrere Gebühren pro Währung definieren. Gebühren müssen mit einem Code für Belastungen verknüpft sein, der die Regeln für die wertmäßigen Buchungen der Gebühr festlegt. Das Feld **Kategorie** wird verwendet, um festzulegen, wie Gebühren berechnet werden. Zum Beispiel, wenn Kunden eine Pauschale von $9.95 berechnet werden soll, um eine Bestellung durch eine bestimmte Lieferart versenden zu lassen, verwenden Sie die Kategorie **Fest**. Wenn das Unternehmen beschließt, den Kunden einen Prozentsatz der Auftragssumme in Rechnung zu stellen, um die Lieferzuschläge zu decken, verwenden Sie die Kategorie **Prozent**. Die tatsächliche Gebühr für den Kunden wird im Feld **Wert der sonstigen Zuschläge** definiert.

Unternehmen konfigurieren oft gestaffelte Gebühren. In diesem Fall richtet sich der Betrag, den der Kunde für die Lieferung bezahlt, nach dem Auftragswert. Um abgestufte Gebühren zu konfigurieren, geben Sie Werte in die Felder **Von-Betrag** und **Bis-Betrag** ein, zusätzlich zur Definition der Gebühr selbst im Feld **Wert der sonstigen Zuschläge**. Zum Beispiel, für Aufträge, die einen Wert von weniger als $50 haben, berechnet ein Einzelhändler $5.95 für den Bodenversand. Für Aufträge, deren Wert gleich oder größer als $50, aber kleiner als $100 ist, berechnet der Einzelhändler $7,95. Für Aufträge, deren Wert gleich oder höher als $100 ist, bietet der Händler kostenlosen Versand an. Die folgende Abbildung zeigt die Konfiguration dieser Gebühren.

![Beispiel für feste abgestufte Gebühren.](media/fixedtieredcharges.png)

Sie können eine Mischung aus Kategorien für Gebühren verwenden, je nach Ihren geschäftlichen Anforderungen. Zum Beispiel, für alle Aufträge, die einen Wert von weniger als $100 haben, gibt es eine feste Gebühr von $9.95 für den Versand. Für Aufträge, deren Wert gleich oder größer als $100 ist, werden die Versandkosten in Höhe von 5 Prozent des Auftragswertes berechnet. Die folgende Abbildung zeigt die Konfiguration dieser Gebühren.

![Beispiel für gemischte abgestufte Gebühren.](media/mixedtieredcharges.png)

## <a name="apply-delivery-modes-during-order-entry-in-a-call-center"></a>Lieferarten bei der Auftragserfassung in einem Callcenter anwenden

Wenn ein neuer Auftrag erstellt wird, muss ein Wert im Feld **Lieferart** auf dem Inforegister **Lieferung** im Auftragskopf angegeben werden. Dieses Feld kann automatisch ausgefüllt werden, basierend auf Standardwerten aus dem Kundendatensatz.

Die auf dem Auftragskopf definierte Lieferart wird beim Anlegen automatisch in die Auftragspositionen übernommen. Sie können jedoch die Einstellung der Lieferart für einen bestimmten Positionsartikel auf der Registerkarte **Lieferung** im Abschnitt **Positionsdetails** auf der Auftragserfassungsseite ändern.

Wenn die gewählte Lieferart für das Produkt oder die Lieferadresse, die für den Auftrag oder Auftragsposition definiert ist, nicht gültig ist, erhalten Sie eine Fehlermeldung. Sie müssen dann eine Lieferart auswählen, die zur Unterstützung dieser Produkt- oder Adresskonfiguration definiert wurde.

## <a name="calculation-of-delivery-charges-during-entry-of-order"></a>Berechnung der Lieferzuschläge bei der Auftragserfassung

Wenn die Einstellung **Auftragsabschluss aktivieren** für Ihren Callcenterkanal aktiviert ist, werden die Versandgebühren für Aufträge automatisch berechnet, wenn der Benutzer **Abgeschlossen** wählt. Die folgende Meldung erscheint oben auf der Seite **Auftragszusammenfassung**: "Abgestufte Belastungen berechnet." Die berechneten Gebühren werden zum Wert des Feldes **Summe Verkäufe** addiert. Auf dem Inforegister **Betrag** zeigt das Feld **Gebühren** den Gesamtbetrag aller Gebühren an, die für den Auftrag und die Positionen berechnet wurden. Um eine detailliertere Aufschlüsselung der Gebühren zu sehen, wählen Sie **Auftrag** auf der Seite **Auftragszusammenfassung** und wählen Sie dann die Option **Gebühren**, um die Gebühren anzuzeigen, hinzuzufügen oder zu bearbeiten. Beachten Sie, dass die Berechnung der Lieferzuschläge auf dem Auftragskopf auf der Grundlage der Lieferart erfolgt, die mit dem Kopf verknüpft ist. Zustellgebühren auf Positionsebene sind auf Grundlage der Lieferart berechnet, die für die Verkaufsposition konfiguriert ist. Wenn mehrere Lieferarten für verschiedene Positionen verwendet werden, könnten mehrfache Gebühren angewendet und hinzugefügt werden. Der Gesamtbetrag wird dann im Feld **Gebühren** auf der Seite **Auftragszusammenfassung** angezeigt.

Ist die Einstellung **Auftragsabschluss aktivieren** ausgeschaltet, muss der Benutzer die Berechnung der Gebühren manuell anstoßen. Auf der Seite **Auftrag** im Aktivitätsbereich, auf der Registerkarte **Verkaufen** in der Gruppe **Berechnen** wählen Sie **Abgestufte Belastungen** aus. Die Meldung "Abgestufte Belastungen berechnet" erscheint. Sie können dann die Option **Gebühren** auf der Registerkarte **Verkaufen** wählen, um die berechneten Gebühren anzuzeigen, zu bearbeiten oder zu löschen.

## <a name="use-expedited-delivery-modes-on-call-center-orders"></a>Verwenden Sie beschleunigte Lieferarten bei Callcenteraufträgen

Sie können optional einen Eillieferungscode mit jeder von Ihnen konfigurierten Lieferart verknüpfen. Dieser Code wird als Sortier- und Berichtstool für die Priorisierung verwendet. Es fallen derzeit keine zusätzlichen Gebühren für den Auftrag an. Um Eillieferungscodes einzurichten, gehen Sie zu **Vertrieb und Marketing \> Einrichten \> Vertrieb \> Eillieferungscodes**.

Bei Bestellungen, die beispielsweise am nächsten Tag per Luftfracht verschickt werden, muss die Kommissionierung täglich bis 13 Uhr im Lager erfolgen. In diesem Fall kann ein Eillieferungscode erstellt werden, der mit jeder im System konfigurierten Lieferart für den nächsten Tag verknüpft werden kann. Wenn das Lager seine Entnahmeserie erzeugt, kann der entsprechende Eillieferungscode im Feld **Eillieferung** als Filter verwendet werden, so dass die Entnahme nur für Aufträge durchgeführt wird, die Lieferarten haben, die mit diesem Code verknüpft sind.

Zusätzlich kann bei der Eingabe eines Callcenterauftrags ein Eillieferungscode entweder manuell auf den Auftragskopf oder auf eine einzelne Auftragspositionen angewendet werden. Auch hier kann der Code für Sortier- oder Berichtszwecke verwendet werden. Manchmal muss ein Auftrag wegen eines Kundenserviceproblems sorgfältig behandelt werden. In diesem Fall kann ein spezieller Eillieferungscode auf den Auftragskopf oder die Auftragszeilen angewendet werden, um den Auftrag während des Ausführungsprozesses zu identifizieren und zu priorisieren.


[!INCLUDE[footer-include](../includes/footer-banner.md)]