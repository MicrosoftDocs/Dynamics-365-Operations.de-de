---
title: Kreditoren, Debitoren und Artikel für den Intercompany-Handel einrichten
description: In diesem Thema wird erläutert, wie Sie Kreditoren, Debitoren und Artikel für den Intercompany-Handel einrichten.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3e1eb7b8673f3af682204b65b33a1d8b61742721
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675036"
---
# <a name="set-up-vendors-customers-and-items-for-intercompany-trade"></a>Kreditoren, Debitoren und Artikel für den Intercompany-Handel einrichten

[!include [banner](../../includes/banner.md)]

Zur Vorbereitung der Organisation für den Intercompany-Handel müssen Sie die Kreditoren und die Debitoren definieren, mit denen Sie intern handeln möchten. Anschließend müssen Sie diese Kreditoren und Debitoren den Artikeln zuordnen, die Sie kaufen oder verkaufen.

1. Gehen Sie zu **Beschaffung \> Kreditoren \> Alle Kreditoren**.
1. Wählen Sie den Kreditor aus, der als Intercompany-Kreditor definiert werden soll.
1. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Allgemein**, und wählen Sie **Intercompany** aus.
1. Geben Sie Intercompany-Einstellungsparameter für das Kreditorenkonto an. Zu diesen Parametern gehören die juristische Person und das Konto des Debitoren, Auftragsrichtlinien, Bestellungsrichtlinien, Wertzuordnung sowie Rahmenbestellungs- und Kaufvertragsrichtlinien. Darüber hinaus geben Sie an, ob Stammdatenwerte vom Kreditorenkonto oder vom Debitorenkonto in der anderen juristischen Person verwendet werden.
1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie auf der Seite mit der Liste **Freigegebene Produkte** die Artikel aus, die dem Kreditor zugewiesen werden sollen, sodass die Artikel für den Intercompany-Handel zur Verfügung stehen. Öffnen Sie für jeden Artikel die Seite **Freigegebene Produktdetails**. Geben Sie auf der Registerkarte **Kauf** im Feld **Kreditor** die Kreditorennummer ein.
1. Gehen Sie zu **Debitorenkonten \> Debitoren \> Alle Debitoren**.
1. Wählen Sie den Debitor aus, der als Intercompany-Kunden definiert werden soll.
1. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Allgemein**, und wählen Sie **Intercompany** aus.
1. Geben Sie Intercompany-Einstellungsparameter für das Debitorenkonto an. Zu diesen Parametern gehören die juristische Person und das Konto des Kreditoren, Bestellungsrichtlinien, Auftragsrichtlinien, Wertzuordnung sowie Kaufvertrags- und Rahmenbestellungsrichtlinien. Darüber hinaus geben Sie an, ob Stammdatenwerte vom Debitorenkonto oder vom Kreditorenkonto in der anderen juristischen Person verwendet werden.
1. Aktivieren Sie auf der Seite **Debitoren** im Inforegister **Rechnung und Lieferung** das Kontrollkästchen **Intercompany-Aufträge erstellen**. Wenn Aufträge direkt an Debitoren geliefert werden sollen, aktivieren Sie das Kontrollkästchen **Direktlieferung**.

    > [!NOTE]
    > Wenn es Artikel gibt, die Ihre Organisation lagert und an Debitoren liefert, sollten Sie Intercompany-Aufträge nicht automatisch erstellen, auch wenn sich der Artikel am Lager befindet. Deaktivieren Sie das Kontrollkästchen **Intercompany-Aufträge erstellen**, um die automatische Erstellung von Aufträgen für Artikel zu deaktivieren, die Sie eventuell gelegentlich auf Lager haben.

1. Wenn die indirekte Erstellung von zusätzlichen Positionen auf Aufträgen zulässig sein soll, aktivieren Sie das Kontrollkästchen **Indirekte Auftragspositionen erstellen**. Ein Benutzer hat dann die Möglichkeit, dem Originalauftrag eines Intercompany-Auftrags Positionen hinzuzufügen.

> [!WARNING]
> Wenn Sie die indirekte Erstellung von Auftragspositionen zulassen, ist damit jedweder Zusatz zum Originalauftrag aus dem Intercompany-Auftrag zulässig. Jeder Zusatz wird bis zum Debitor verarbeitet und wird zum Auftrag und zur Rechnung addiert. Darüber hinaus wird jedes Dokument, das am Verkauf beteiligt sind, automatisch gedruckt und gebucht. Die Benutzer erhalten keinen Warnhinweis zu den Zusätzen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
