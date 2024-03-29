---
title: Synchronisieren von Produktbewertungen in Dynamics 365 Commerce
description: In diesem Artikel wird das Synchronisieren von Produktbewertungen in Microsoft Dynamics 365 Commerce beschrieben.
author: gvrmohanreddy
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 7946bcaa9c6f318115640c6b20b00554a117dd38
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282022"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a>Synchronisieren von Produktbewertungen in Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

In diesem Artikel wird das Synchronisieren von Produktbewertungen in Microsoft Dynamics 365 Commerce beschrieben.

Um Produktbewertungen in Mehrkanal-Lösungen, z. B. am Point of Sale (POS) und in Callcentern, zu verwenden, müssen die Produktbewertungen aus dem Dienst Bewertungen und Überprüfungen in die Commerce-Kanaldatenbank importiert werden. Wenn Produktbewertungen in Mehrkanal-Lösungen zur Verfügung gestellt werden, können sie Kunden indirekt bei ihren Interaktionen mit Vertriebspartnern unterstützen.

In diesem Artikel werden folgende Aufgaben beschrieben:

1. Konfigurieren Sie **Produktbewertungsjob synchronisieren** als Batchauftrag zum Synchronisieren von Produktbewertungen aus dem **Bewertungs- und Überprüfungsservice**.
1. Sicherstellen, dass der Batchauftrag für die Produktbewertungssynchronisierung erfolgreich war
1. Bereitstellen von Produktbewertungen am POS

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a>Konfigurieren eines Batchauftrags zum Synchronisieren von Produktbewertungen

> [!IMPORTANT]
> Vor dem Start sicherstellen, dass Version 10.0.6 oder höher von Dynamics 365 Commerce Retail installiert ist.

### <a name="initialize-the-commerce-scheduler"></a>Commerce-Planer initialisieren

Um den Commerce-Planer zu initialisieren, führen Sie die folgenden Schritte aus:

1. Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Commerce-Planer initialisieren**. Suchen Sie alternativ nach „Commerce-Planer initialisieren“.
1. Stellen Sie im Dialogfeld **Commerce-Planer initialisieren** sicher, dass die Option **Vorhandene Konfiguration löschen** auf **Nein** gesetzt ist, und wählen Sie dann **OK** aus.

### <a name="verify-the-retailproductrating-subjob"></a>Den Unterauftrag RetailProductRating prüfen

Um sicherzustellen, dass der Unterauftrag **RetailProductRating** vorhanden ist, befolgen Sie diese Schritte.

1. Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Planer-Unteraufträge**. Suchen Sie alternativ nach „Steuerprogrammunteraufträge“.
1. Finden oder suchen Sie in der Unterauftragsliste den Unterauftrag **RetailProductRating**.

Die folgende Abbildung zeigt ein Beispiel der Seite Unterauftragsdetails in Commerce.

![Details des Unterauftrags RetailProductRating.](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> Wenn Sie den Unterauftrag **RetailProductRating** nicht finden, haben Sie vielleicht den Auftrag **Synchronisieren von Produktbewertungen** und den Auftrag **1040 CDX** ausgeführt, bevor Sie den Commerce-Planer initialisiert haben. Befolgen Sie in diesem Fall die Schritte, um den Auftrag **Vollständige Datensynchronisierung** auszuführen.

> 1. Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Kanaldatenbank**. Suchen Sie alternativ nach „Kanaldatenbank“.
> 1. Wählen Sie die zu synchronisierende Kanaldatenbank aus.
> 1. Wählen Sie **Vollständige Datensynchronisierung** im Aktivitätsbereich aus.
> 1. Wählen Sie im Dropdown-Dialogfeld **Vertriebsplan auswählen** die Option **1040 - Produkte** und dann **OK** aus.
> 1. Wiederholen Sie die Schritte der vorherigen Prozedur, um zu prüfen, ob der Unterauftrag **RetailProductRating** erstellt wurde.

### <a name="import-product-ratings"></a>Produktbewertungen importieren

Führen Sie die folgenden Schritte aus, um Produktbewertungen aus dem Bewertungs- und Überprüfungsdienst in Commerce zu importieren.

1. Navigieren Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Produktbewertungsauftrag synchronisieren**. Suchen Sie alternativ nach „Produktbewertungsauftrag synchronisieren“.
1. Wählen Sie im Dialogfeld **Produktbewertungen** auf dem Inforegister **Im Hintergrund ausführen** die Option **Wiederholung** aus.
1. Legen Sie im Dialogfeld **Wiederholung definieren** ein Wiederholungsmuster fest. (Der empfohlene Wert beträgt zwei Stunden.) Planen Sie keine Wiederholung, die kürzer als eine Stunde ist.
1. Wählen Sie **OK**.
1. Legen Sie die Option **Stapelverarbeitungsvorgang** auf **Ja** fest. Diese Einstellung stellt sicher, dass Sie die Protokolle überwachen und den Status von Batchaufträgen überprüfen können.
1. Wählen Sie **OK** aus, um den Batchauftrag zu planen.

Die folgende Abbildung zeigt ein Beispiel der Batchauftragskonfiguration in Commerce.

![Konfiguration des Batchauftrags zum Synchronisieren von Produktbewertungen.](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Sicherstellen, dass der Batchauftrag für die Produktbewertungssynchronisierung erfolgreich war

Um sicherzustellen, dass der Batchauftrag **Produktbewertungen synchronisieren** erfolgreich war, befolgen Sie diese Schritte.

1. Navigieren Sie zu **Einzelhandel und Handel \> Systemadministrator \> Abfragen \> Batchaufträge** oder bei Verwendung einer Commerce-Lagermengeneinheit stattdessen zu **Einzelhandel und Handel \> Abfragen und Berichte \> Batchaufträge**. Suchen Sie alternativ nach „Batchaufträge“.
1. Um die Details des Batchauftrags in der Batchauftragsliste anzuzeigen, suchen Sie in der Spalte **Auftragsbeschreibung** nach einer Beschreibung mit „Produktbewertungen abrufen“.
1. Wählen Sie die Auftrags-ID aus, um die Details des Batchauftrags anzuzeigen, z. B. das geplante Startdatum/die geplante Startzeit und den Wiederholungstext.

Die folgende Abbildung zeigt ein Beispiel für die Batchauftragsdetails in Commerce, wenn die Ausführung des Batchauftrags in zweistündigen Intervallen geplant ist.

![Details des Batchauftrags zum Synchronisieren von Produktbewertungen.](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Bereitstellen von Produktbewertungen am POS

Die Bewertungs- und Prüfungslösung in Dynamics 365 Commerce ist eine Mehrkanallösung. Produktbewertungen werden jedoch standardmäßig nicht am POS angezeigt. Damit Kunden in Geschäften Bewertungen und Beurteilungen sehen können, wenn sie von Vertriebspartnern unterstützt werden, müssen Sie die Produktbewertungen am POS aktivieren.

Gehen Sie folgendermaßen vor, um Produktbewertungen am POS zu aktivieren.

1. Gehen Sie zu **Einzelhandel und Handel \> Commerce-Einrichtung \> Parameter \> Commerce-Parameter**. Suchen Sie alternativ nach „Commerce-Parametern“.
1. Wählen Sie auf der Registerkarte **Konfigurationsparameter** die Option **Neu** aus.
1. Geben Sie einen Namen, wie **RatingsAndReviews.EnableProductRatingsForRetailStores**, ein, und setzen Sie den Wert auf **true**.
1. Wählen Sie **Speichern**.
1. Gehen Sie zu **Einzelhandel und Handel \> Einzelhandel und Handel IT \> Vertriebsplan**. Suchen Sie alternativ nach „Vertriebsplan“.
1. Wählen Sie in der Auftragsliste **1110** (**globale Konfiguration**) und dann **Jetzt ausführen** aus.
1. Überprüfen Sie nach erfolgreicher Ausführung des Auftrags, ob die Produktbewertungen jetzt am POS angezeigt werden.

Die folgende Abbildung zeigt ein Beispiel für die Konfiguration der Commerce-Parameter zum Aktivieren der Produktbewertungen am POS.

![Konfiguration der Commerce-Parameter für Produktbewertungen am POS.](media/rnr-hq-enable-ratings-in-pos.png)

Die folgende Abbildung zeigt ein Beispiel für Produktbewertungen am POS.

![Produktbewertungen am POS.](media/rnr-pos-catalog-ratings.png)

Die folgende Abbildung zeigt ein Beispiel für Produktbewertungen in Callcenter-Kanälen.

![Produktbewertungen in einem Callcenterkanal.](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Bewertungen und Prüfungen](ratings-reviews-overview.md)

[Nutzung von Bewertungen und Prüfungen aktivieren](opt-in-ratings-reviews.md)

[Bewertungen und Prüfungen verwalten](manage-reviews.md)

[Bewertungen und Prüfungen konfigurieren](configure-ratings-reviews.md)

[Produktbewertungen synchronisieren](sync-product-ratings.md)

[Manuelle Veröffentlichung von Bewertungen und Prüfungen durch einen Moderator aktivieren](manual-publish-rating-reviews.md)

[Bewertungen und Rezensionen importieren und exportieren](import-export-reviews.md)

[Authentifizierung zwischen Diensten konfigurieren](service-to-service-auth.md)

[Häufig gestellte Fragen zu Bewertungen und Prüfungen](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
