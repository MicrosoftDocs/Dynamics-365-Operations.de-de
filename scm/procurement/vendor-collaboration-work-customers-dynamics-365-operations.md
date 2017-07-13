---
title: Kreditorenzusammenarbeit mit Debitoren
description: "In diesem Thema wird beschrieben, wie Sie Kreditorenzusammenarbeit verwenden können, um in Microsoft Dynamics 365 for Finance and Operations mit Bestellungen zu arbeiten und Lieferungsbestand zu überwachen."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 41436dab710a5fee0fe0800dff1ebefefa841afc
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017


---

# <a name="vendor-collaboration-with-customers"></a>Kreditorenzusammenarbeit mit Debitoren

[!include[banner](../includes/banner.md)]


In diesem Thema wird beschrieben, wie Sie Kreditorenzusammenarbeit verwenden können, um in Microsoft Dynamics 365 for Finance and Operations mit Bestellungen zu arbeiten und Lieferungsbestand zu überwachen.

In diesem Thema wird beschrieben, wie Sie Kreditorenzusammenarbeit verwenden können, um mit Debitoren in Microsoft for Finance and Operations zu arbeiten. Es enthält zudem Informationen darüber, wie Bestellungen überwacht und auf diese reagiert wird und wie Lieferbestand überwacht wird. Es ist auch möglich, die Kreditor-Kooperation für die Arbeit mit Rechnungen zu verwenden. Weitere Informationen finden Sie unter [Arbeitsbereich für Kreditor-Kooperationsrechungen](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace).

## <a name="working-with-purchase-orders"></a>Mit Bestellungen arbeiten
Der Arbeitsbereich **Bestellungsbestätig** ermöglicht Ihnen, auf Bestellungen zu antworten, die zur Prüfung gesendet wurden. Er ermöglicht es Ihnen außerdem, Informationen zu Bestellungen, die eine Aktivität vom Debitor erfordern und Bestellungen, die bestätigt wurden aber noch offen sind, anzuzeigen. Es gibt drei Listen im Arbeitsbereich **Bestellungsbestätigung**:

-   **Bestellungen zur Prüfung** – Diese Liste enthält Bestellungen, die Ihnen gesendet wurden und eine Antwort von Ihnen erfordern. Nachdem Sie reagiert haben, wird die Bestellung nicht mehr in der Liste angezeigt. Wenn der Debitor Ihnen eine neue Version der Bestellung sendet, bevor Sie auf die frühere geantwortet haben, wird nur die aktuelle Version angezeigt.
-   **Debitorenaktivität abwarten** - Diese Liste ermöglicht es Ihnen, Bestellungen anzuzeigen, auf die Sie geantwortet haben, die aber vom Debitor noch nicht bestätigt wurden. Wenn Sie die Bestellung akzeptiert haben, können Sie sie in dieser Liste überwachen, bis der Status auf **bestätigt** ändert. Wenn Sie die Bestellung zurückgewiesen oder sie mit Änderungen akzeptiert haben, können Sie die Bestellung hier überwachen, bis der Debitor eine neue Version übermittelt.
-   **Bestätigte Bestellungen öffnen** - Diese Liste enthält alle Bestellungen für das Konto, die den Status **Bestätigt** haben. Wenn Produkte oder Dienste für die Bestellung vollständig eingegangen sind, verschwindet die Bestellung in der Liste.

Die folgende Liste zeigt die vier Seiten, die Sie verwenden können, um mit Bestellungen zu arbeiten, wobei zwei die gleichen Informationen wie Listen im Arbeitsbereich enthalten:

-   **Bestellungen zur Prüfung** (siehe oben)
-   **Bestellungskreditoren-Bestätigungsverlauf** - Diese Seite enthält alle Bestellungen allen Versionen von Bestellungen, die an den Kreditor gesendet wurden, sowie alle Antworten, die vom Kreditor zurückgeliefert wurden.
-   **Offene bestätigte Bestellungen** (siehe oben)
-   **Alle bestätigten Bestellungen** - Diese Seite enthält alle Bestellungen, die bestätigt wurden, einschließlich jener, von denen Produkte oder Dienstleistungen empfangen wurden. Sie können diese Liste verwenden, um zu überprüfen, für welche Bestellungen Sie Rechnungen übermitteln können.

### <a name="responding-to-purchase-orders"></a>Antworten auf Bestellungen

Die Bestellungen, die Ihnen der Debitor zur Prüfung gesendet hat, werden im Arbeitsbereich **Bestellungsbestätigung** auf der Seite **Bestellungen zur Prüfung** angezeigt. Nachdem Sie eine Bestellung geöffnet haben, können Sie diese akzeptieren, ablehnen oder mit Änderungen akzeptieren. Es kann im Bestellungskopf oder für einzelne Positionen Anlagen geben. Es ist auch möglich für Sie, Informationen zu Ihrer Antwort im Bestellungskopf oder einzelnen Positionen zuzuordnen. Zum Beispiel können einen Ersatzartikel für eine der Positionen vorschlagen. Sie können die Bestellung als PDF-Datei in der Vorschau anzeigen und drucken, indem Sie die Option **Vorschau anzeigen/Drucken** verwenden. Sie können die folgenden Dimensionsspalten mithilfe der Aktivität ausblenden oder anzeigen **Anzeigendimensionen** : Standort, Lagerort, Größe, Farbe, Stil, Konfiguration. Bei Auswahl von **Mit Änderungen akzeptieren** können Sie bestimmte Positionen akzeptieren oder ablehnen. Sie können auch folgende Änderungen an den Positionen vornehmen:

-   Ändern von Mengen oder Datumsangaben. Wenn Sie das bestätigte Lieferdatum für alle Positionen aktualisieren möchten, können Sie die Option **Lieferdatum aktualisieren** im Bestellungskopf verwenden.
-   Aufteilen von Positionen für sonstige Lieferdaten und Mengen.
-   Einen Artikel ersetzen. Um dies zu bewerkstelligen, geben Sie eine Artikelbeschreibung und die Artikelnummer im Feld **Extern** in Abschnitt **Positionsdetails** ein.

Sie können Preisgestaltungsinformationen oder Zuschlägen nicht ändern, doch können Sie Vorschläge für Änderungen dieser mithilfe von Hinweisen vornehmen. Wenn Ihnen der Kunde eine neue Version einer Bestellung sendet, gibt es einen Versionssuffix, um anzuzeigen, dass dies eine geänderte Version einer Bestellung ist, die zuvor mitgeteilt wurde. Die Seite **Bestellungskreditoren-Bestätigungsverlauf** ermöglicht es Ihnen und Ihren Lieferanten, den Verlauf jedes Auftrags zu verfolgen.

## <a name="monitoring-consignment-inventory"></a>Verfügbarer Lagerbestand überwachen
Wenn Sie Lieferungsbestand verwenden, können Sie die Kreditorenzusammenarbeitschnittstelle verwenden, um Informationen zu den folgenden Seiten anzeigen:

-   **Bestellungen, die Lieferbestand verbrauchen** – Bestellungen für Lieferbestand werden erzeugt, wenn das Eigentum am Bestand an den Debitor übergeht. Diese Lieferungsbestellungen werden nur auf der Seite **Bestellungen, die Lieferungsbestands verbrauchen** angezeigt. Sie sind nicht in der Seite **Alle bestätigten Bestellungen** enthalten.
-   **Produkte vom Lieferbestand erhalten** - Diese Seite enthält alle Transaktionen, bei  denen der Besitz der Produkte vom Kreditor an das Unternehmen übertragen wurde. Sie können diese Informationen verwenden für die Rechnungsstellung.
-   **Verfügbarer Lieferungsbestand** - Diese Seite zeigt  den Lieferungsbestand Ihres Unternehmens, der am Lager ist.


<a name="see-also"></a>Siehe auch
--------

[Benutzer für Kreditor-Kooperationen verwalten](manage-vendor-collaboration-users.md)




