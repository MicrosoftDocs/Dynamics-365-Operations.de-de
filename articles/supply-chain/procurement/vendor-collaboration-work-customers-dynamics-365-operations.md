---
title: Kreditorenzusammenarbeit mit Debitoren
description: In diesem Thema wird beschrieben, wie Sie Kreditorenzusammenarbeit verwenden können, um mit Bestellungen zu arbeiten und Lieferungsbestand zu überwachen.
author: TaylorVH
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart, VendVendorProfileCard, PurchVendorPortalAllResponse, PurchVendorPortalPendingResponsesPart, PurchVendorPortalResponses, PurchVendorPortalConfirmedOpenOrdersPart
audience: Application User
ms.reviewer: roschlom
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: v-savanh
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8f5ec8113397cb0e2ece91611c62584bbd953853f0857e53764ac41450b28bae
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715793"
---
# <a name="vendor-collaboration-with-customers"></a>Kreditorenzusammenarbeit mit Debitoren

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Kreditorenzusammenarbeit verwenden können, um mit Debitoren in Microsoft Dynamics 365 Supply Chain Management zu arbeiten. Kreditoren können eine Serie von Geschäftsprozesse aus den folgenden Arbeitsbereichen ausführen:

- **Bestellungsbestätigung** – Überwachen von Bestellungen und auf sie antworten.
- **Kreditorenangebotsabgabe** – Angebotsanforderungen anzeigen und durch Eingeben von Angeboten auf sie antworten.
- **Kreditoreninformationen** – Kreditorenmasterdaten anzeigen und aktualisieren.
- **Rechnungsstellung** – Mit Rechnungen arbeiten. In diesem Thema wird der Arbeitsbereich **Rechnungsstellung** nicht behandelt. Weitere Informationen über diesen Arbeitsbereich finden Sie unter [Arbeitsbereich für Kreditorenzusammenarbeitsrechnungsstellung](../../finance/accounts-payable/vendor-portal-invoicing-workspace.md).

Kreditoren können außerdem Informationen zu Lieferungsbestand überwachen.

## <a name="working-with-pos-in-the-purchase-order-confirmation-workspace"></a>Arbeiten mit Bestellungen im Arbeitsbereich für die Bestellungsbestätigung

Im Arbeitsbereich **Bestellbestätigung** können Sie auf die Einkaufsbestellungen (POs) reagieren, die Ihnen zur Überprüfung zugesandt wurden. Er ermöglicht es Ihnen außerdem, Informationen zu Bestellungen, die eine Aktivität vom Debitor erfordern und Bestellungen, die bestätigt wurden aber noch offen sind, anzuzeigen.

Es gibt drei Listen im Arbeitsbereich **Bestellungsbestätigung**:

- **Bestellungen zur Prüfung** – Diese Liste enthält Bestellungen, die Ihnen gesendet wurden und eine Antwort von Ihnen erfordern. Nachdem Sie reagiert haben, wird die Bestellung nicht mehr in der Liste angezeigt. Wenn der Debitor Ihnen eine neue Version der Bestellung sendet, bevor Sie auf die frühere Version geantwortet haben, wird nur die aktuelle Version angezeigt.
- **Debitorenaktivität abwarten** – Diese Liste zeigt alle Bestellungen an, auf die Sie geantwortet haben, die aber der Debitor noch nicht bestätigt hat. Wenn Sie eine Bestellung akzeptieren, können Sie sie in dieser Liste überwachen, bis der Status auf **Bestätigt** geändert wird. Wenn Sie eine Bestellung zurückweisen oder sie mit Änderungen akzeptieren, können Sie sie hier überwachen, bis der Debitor eine neue Version übermittelt.
- **Bestätigte Bestellungen öffnen** – Diese Liste zeigt alle Bestellungen für Ihr Konto an, die den Status **Bestätigt** haben. Wenn Produkte oder Dienste für die Bestellung vollständig eingegangen sind, verschwindet die Bestellung in der Liste.

Sie können die folgenden Seiten verwenden, um mit Bestellungen zu arbeiten:

- **Bestellungen zur Prüfung** – Diese Seite enthält die gleichen Informationen wie die Liste **Bestellungen zur Prüfung** im Arbeitsbereich. Sehen Sie die Beschreibung weiter oben in diesem Thema.
- **Kreditorenbestätigungshistorie für Bestellungen** – Diese Seite enthält alle Bestellungen und alle Versionen von Bestellungen, die dem Kreditor gesendet wurden. Außerdem enthält sie alle Antworten, die vom Kreditor zurückgegeben wurden.
- **Bestätigte Bestellungen öffnen** – Diese Seite enthält die gleichen Informationen wie die Liste **Bestätigte Bestellung öffnen** im Arbeitsbereich. Sehen Sie die Beschreibung weiter oben in diesem Thema.
- **Alle bestätigten Bestellungen** – Diese Seite enthält alle Bestellungen, die bestätigt wurden. Die Bestellungen, die auf dieser Seite angezeigt werden, umfassen Bestellungen, bei denen Produkte oder Dienstleistungen eingegangen sind. Sie können diese Liste verwenden, um Bestellungen zu überwachen, für die Sie Rechnungen übermitteln können.

### <a name="responding-to-pos"></a>Auf Bestellungen reagieren

Die Bestellungen, die Ihnen der Debitor zur Prüfung sendet, werden im Arbeitsbereich **Bestellungsbestätigung** auf der Seite **Bestellungen zur Prüfung** angezeigt. Nachdem Sie eine Bestellung geöffnet haben, können Sie diese akzeptieren, ablehnen oder mit Änderungen akzeptieren. Es könnte im Bestellungskopf oder für einzelne Positionen Anhänge geben. Außerden können Sie Informationen zu Ihrer Antwort im Bestellungskopf oder einzelnen Positionen zuzuordnen. Zum Beispiel können einen Ersatzartikel für eine der Positionen vorschlagen.

Sie können die Bestellung als PDF-Datei in der Vorschau anzeigen und drucken, indem Sie die Option **Vorschau anzeigen/Drucken** verwenden. Sie können auch die Aktivität **Dimensionen anzeigen** verwenden, um die folgenden Dimensionsspalten auszublenden oder anzuzeigen: **Standort**, **Lagerort**, **Farbe**, **Größe**, **Stil** und **Konfiguration**. 

Bei Auswahl von **Mit Änderungen akzeptieren** können Sie bestimmte Positionen akzeptieren oder ablehnen. Sie können auch folgende Änderungen an den Positionen vornehmen:

- Ändern von Mengen oder Datumsangaben. Um das bestätigte Lieferdatum für alle Positionen zu aktualisieren, können Sie die Option **Lieferdatum aktualisieren** im Bestellungskopf verwenden.
- Teilen Sie Positionen für verschiedene Lieferdaten und Mengen auf.
- Einen Artikel ersetzen. Geben Sie im Abschnitt **Positionsdetails** eine Artikelbeschreibung und die Artikelnummer im Feld **Extern** ein.

Sie können Preisgestaltungsinformationen oder Gebühren nicht ändern, aber Sie können Hinweise verwenden, um Vorschläge für diese Änderungen zu unterbreiten.

Wenn der Kunde eine neue Version einer Bestellung sendet, hat sie einen Versionssuffix, um anzuzeigen, dass dies eine geänderte Version einer Bestellung ist, die zuvor übermittelt wurde. Die Seite **Kreditorenbestätigungshistorie für Bestellungen** ermöglicht es Ihnen, den Verlauf jedes Auftrags zu verfolgen.

## <a name="monitoring-consignment-inventory"></a>Verfügbarer Lagerbestand überwachen

Wenn Sie Lieferungsbestand verwenden, können Sie die Kreditorenzusammenarbeitschnittstelle verwenden, um Informationen auf den folgenden Seiten anzeigen:

- **Bestellungen, die Lieferbestand verbrauchen** – Bestellungen für Lieferbestand werden erzeugt, wenn das Eigentum am Bestand an den Debitor übergeht. Diese Lieferbestellungen werden nur auf dieser Seite angezeigt. Sie sind nicht in der Seite **Alle bestätigten Bestellungen** enthalten.
- **Produkte vom Lieferbestand erhalten** – Diese Seite enthält alle Transaktionen, bei denen der Besitz der Produkte vom Kreditor an das Unternehmen übertragen wurde, das den Bestand verbraucht. Sie können diese Informationen verwenden für die Rechnungsstellung.
- **Verfügbarer Lieferungsbestand** – Diese Seite zeigt den verfügbaren Lieferungsbestand Ihres Unternehmens, der im Besitz Ihres Unternehmens ist, aber der am Lagerort des Debitors verfügbar ist.

## <a name="working-with-rfqs-in-the-vendor-bidding-workspace"></a>Arbeiten mit Angebotsanforderungen im Arbeitsbereich für Kreditorenangebotsabgabe

Im Arbeitsbereich **Lieferantenausschreibung** können Sie die Anfragen (RFQs) anzeigen, auf die Ihr Unternehmen zur Beantwortung eingeladen wurde. Sie können auch auf die Angebotsanforderungen antworten. 

Der Arbeitsbereich zeigt auch alle Angebotsanforderungen an, die Sie verloren oder gewonnen haben. Wenn das System für den öffentlichen Sektor konfiguriert ist, zeigt der Arbeitsbereich außerdem die öffentlich zugänglichen Ausschreibungen an.

### <a name="viewing-rfqs"></a>Angebotsanforderungen anzeigen

Öffnen Sie den Arbeitsbereich **Kreditorenangebotsabgabe**, um auf die folgenden Informationen zuzugreifen:

- Wählen Sie **Neue Angebotseinladungen**, um die Angebotsanforderungen anzuzeigen, bei denen Ihr Unternehmen eingeladen wurde, darauf zu antworten. Von hier aus können Sie eine Angebotsanforderung anzeigen und den Angebotsprozess beginnen. Sie können auch ergänzte Angebotsanforderungen anzeigen, für die ein neues Angebot übermittelt werden muss.
- Wählen Sie **Zurückgegebene Angebote** aus, um die Angebotsanforderungen zu sehen, die der Debitor an Sie zurückgegeben hat, damit Sie weitere Informationen angeben können oder das Angebot aktualisieren können.
- Wählen Sie **Angebote in Bearbeitung**, um die Angebotsanforderungen, anzuzeigen, an denen Sie oder eine Kontaktperson, die Ihr Unternehmen vertritt, gearbeitet haben, aber die noch nicht übermittelt wurden.
- Wählen Sie **Zugesprochene Angebote**, um zu sehen, wenn der Debitor mindestens einer Position in Ihrem Angebot zugesprochen hat.
- Wählen Sie **Verlorene Angebote** aus, um Angebote anzuzeigen, in denen alle Positionen abgelehnt wurden.
- Wählen Sie den Link **Angebotsanforderungen** aus, um eine Liste aller Angebotsanforderungseinladungen des Kreditors anzuzeigen sowie aller Angebote, die übermittelt wurden. Die Seite **Angebotsanforderungen** listet alle Angebotsanforderungen auf, an denen ein Lieferant beteiligt war. Sie können nach Status suchen.
- Wählen Sie den Link **Abgelehnte Angebote** aus, um eine Liste aller Angebotsanforderungen anzuzeigen, bei denen die Kontaktperson eines Kreditors es abgelehnt hat, ein Angebot zu unterbreiten.

### <a name="working-with-rfqs-that-are-publicly-available"></a>Mit Angebotsanforderungen arbeiten, die öffentlich verfügbar sind

Personen, die im öffentlichen Sektor arbeiten, können offene und abgelaufene Angebotsanforderungen sehen, die für die Öffentlichkeit verfügbar gemacht wurden.

- Wählen Sie den Link **Offene veröffentlichte Angebotsanforderungen** aus, um eine Liste offener Angebotsanforderungen anzuzeigen, die für die Öffentlichkeit verfügbar sind. Eine offene Angebotsanforderung ist eine Angebotsanforderung, die noch nicht abgelaufen ist. Sie können das Ablaufdatum und -uhrzeit im Kopf der Angebotsanforderung finden.

    Wenn Sie eingeladen wurden, ein Angebot zu unterbreiten, können Sie die gleiche Angebotsanforderung auf der Seite **Neue Angebotseinladungen** finden. Manchmal möchten Sie vielleicht auf eine offene Angebotsanforderung hin ein Angebot unterbreiten, aber Sie sind nicht zum bieten eingeladen worden. In diesem Fall könnten Sie möglicherweise sich selbst einladen, vorausgesetzt der Debitor hat die Selbsteinladung für die Angebotsanforderungsanfrage aktiviert.

    Erhöhen Sie den Zugriff auf den Link **Veröffentlichte Ausschreibungen öffnen**, indem Sie die Funktion **Link „Veröffentlichte Ausschreibungen öffnen“ als Kachel anzeigen** einschalten. Diese Funktion wandelt den Link in eine Kachel um und verschiebt ihn an einen prominenten Lagerplatz, sodass er leicht zu finden ist.

- Wählen Sie den Link **Geschlossene veröffentlichte Angebotsanforderungen** aus, um eine Liste geschlossener Angebotsanforderungen anzuzeigen, die für die Öffentlichkeit verfügbar sind. Eine geschlossene Angebotsanforderung ist eine Angebotsanforderung, die abgelaufen ist. Sie können das Ablaufdatum und -uhrzeit im Kopf der Angebotsanforderung finden.

    Eine geschlossene Angebotsanforderung zeigt alle Kreditorenangebote bis hinunter zur Positionsebene an. Während Angebote gewährt oder abgelehnt werden, spiegeln sich diese Informationen in der geschlossen Angebotsanforderung wider. Alle Anhänge, die im Angebot enthalten sind, sind auch verfügbar.

> [!NOTE]
> Diese Funktionalität ist nur verfügbar, wenn die Konfiguration Öffentlicher Sektor eingeschaltet ist.

### <a name="bidding"></a>Angebot unterbreiten

- Wählen Sie **Geben**, um mit der Abgabe eines Angebots für eine Anfrage zu beginnen.

    Wenn für Angebotsfelder in den Kopfzeilen und Positionen einer Angebotsanforderung die Bearbeitung aktiviert ist, können Sie Ihr Angebot direkt im Positionsraster eingeben. Sie müssen auch jegliche zusätzlichen Angebotsinformationen berücksichtigen, die in den Positionsdetails hinzugefügt werden sollten.

    Wenn Sie damit beginnen, an einem Angebot zu arbeiten, wird es im Abschnitt **Angebote in Bearbeitung** angezeigt.

    Zu jedem Zeitpunkt vor dem Ablaufdatum können Sie ein Angebot speichern. Sie können dann später zurückkehren, um das Angebot fertig zu stellen und zu senden. Nachdem Sie ein Angebot gesendet haben, können Sie es bis zum Ablaufdatum erneut aufrufen und aktualisieren.

- Wählen Sie **Aus Angebotsanforderung zurücksetzen**, um die Daten zurückzusetzen, die Sie für ein Angebot eingegeben haben, und um die ursprünglichen Angebotsanforderung wiederherzustellen. Sie können den Kopf oder die Position zurücksetzen.
- Wählen Sie im Positionsraster **Alternative hinzufügen** oder **Alternative entfernen** aus, um mit Alternativen zu arbeiten.

    Manche Angebotsanforderungen lassen alternative Angebote zu. Sie können alternative Angebote nur für Positionen des Typs **Kategorie** angeben, da bestimmte Artikel nicht als Alternativen hinzugefügt werden können. 

- Wählen Sie **Angebotsanforderungsanhang** oder **Angebotsanforderungspositionsanhang** aus, um jeglichen Anhang zu öffnen, den der Debitor zur Angebotsanforderung hinzugefügt hat. Wählen Sie **Angebotsanhänge** oder **Angebotspositionsanhänge** aus, um Anhänge zusammen mit dem Angebot hochzuladen.

    Es kann möglicherweise Fragebögen geben, die Sie beantworten müssen, bevor Sie ein Angebot übermitteln dürfen.

- Wählen Sie **Ablehnen** aus, wenn Sie kein Angebot unterbreiten möchten. Nachdem Sie **Ablehnen** ausgewählt haben, können Sie die Aktivität nicht rückgängig machen und ein Angebot unterbreiten.

Wenn eine Angebotsanforderung ergänzt wird, müssen Sie ein neues Angebot unterbreiten. Sie können Informationen zur Ergänzung auf der Registerkarte **Ergänzungen** auf der Angebotsanforderungsseite finden. Ergänzte Angebotsanforderungen werden auf der Seite **Neue Angebotseinladungen** angezeigt.

## <a name="accessing-vendor-master-data-in-the-vendor-information-workspace"></a>Zugreifen auf Kreditormasterdaten im Arbeitsbereich für Kreditorinformationen

Als Kreditor können Sie auf einen Teil der Informationen zugreifen, die der Debitor im Keditormasterdatensatz verwaltet. Daher können Sie die Informationen auf dem neuesten Stand halten. Um die Informationen zu aktualisieren, müssen Sie eine (externe) Rolle als Kreditorenadministrator haben.

Die Informationen, auf die zugegriffen werden kann, sind der Name des Kreditors, die Adressen, Kontaktinformationen, Kontaktpersonen und ihre Kontaktinformationen, Kennungsnummern, Steuernummern, Beschaffungskategorien, in denen der Kreditor an den Debitor verkaufen darf, sowie Informationen über Zertifizierungen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Benutzer für Kreditorenzusammenarbeit verwalten](manage-vendor-collaboration-users.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]