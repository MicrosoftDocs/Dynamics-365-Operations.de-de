---
title: Externe Kataloge für PunchOut-E-Procurement verwenden
description: In diesem Thema wird erläutert, wie Sie externe Kataloge verwenden können, um Anforderungen zu erstellen und zu senden.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests, CatExternalCatalogBasketWizard, CatExternalCatalogPunchoutDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b236a17a7f93bfeb60d64fa25745bd1b4cb1b34b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578031"
---
# <a name="use-external-catalogs-for-punchout-e-procurement"></a>Externe Kataloge für PunchOut-E-Procurement verwenden

[!include [banner](../includes/banner.md)]

Wenn Sie externe Kataloge für PunchOut E-Procurement verwenden, müssen Sie Informationen zu den Produkten Ihrer Kreditoren in den eigenen Masterdaten nicht verwaltet. Stattdessen wird der Einkaufskorb auf der Website des Kreditors auf Anforderungspositionen konvertiert, die die korrekte Produktinformationen haben. 

Sie sollten die Verwaltung von Beschreibungen und Preisen der Produkte der Kreditoren in den eigenen Produktmasterdaten vermeiden. Nutzen Sie stattdessen externe Kataloge für PunchOut E-Procurement. Wenn Mitarbeiter Anforderungen erstellen, können sie auf die externe Katalogwebsite eines Kreditors zugreifen (das heißt, wenn sie das System verlassen und auf die Seite des Kreditors gehen). Die Produkte, die dem Einkaufskorb auf der Website des Kreditors hinzugefügt werden, können auf dann in Anforderungspositionen konvertiert werden. Deshalb erhalten Sie die korrekten Produktinformationen ab: Produktkennung, Name, Preis, usw.

Wenn Sie externe Kataloge verwenden, muss ein Mitarbeiter die Anforderung auf der Seite **Eigene Bestellanforderungen** erstellen.

Der Mitarbeiter, der eine Bestellanforderung erstellt, ist der Antragsteller der Bestellanforderung. Als Antragsteller können Sie die folgenden Aufgaben durchführen.

Verwenden Sie die **Externe Kataloge** Positionsaktivität, um eine Seite zu öffnen, die alle externen Kataloge enthält, die für die jeweilige anfordernde Person, die einkaufende juristische Person und die empfangende Organisationseinheit verfügbar sind.

Abhängig von Ihren Berechtigungen ändern Sie die anfordernde Person, die juristische Person und die empfangende Organisationseinheit. Eine Änderung in diesen Werten ändert möglicherweise die Liste der externen Kataloge, die für eine anfordernde Person bereitstehen. Die externen Kataloge, die verfügbar sind, hängen von der aktuellen aktiven Einkaufsrichtlinien für die kaufende juristische Person und die empfangende Organisationseinheit ab. Diese Richtlinie kann Zugriffe auf bestimmte Beschaffungskategorien gestatten oder verhindern. Daher kann die Liste der externen Kataloge, die diesen Beschaffungskategorien zugeordnet sind, betroffen sein.

Weitere Informationen zu Policen finden Sie unter [Einkaufsübersicht ](../procurement/purchase-policies.md).

- Wenn Sie externe Kataloge für bestimmte Beschaffungskategorien suchen, geben Sie Text im Feld "Katalogsuchgebiete" ein.
- Um Produkte aus dem externen Katalog eines Lieferanten auf der Website des Kreditors hinzuzufügen, klicken auf den externen Katalog. Fügen Sie dann Produkte zum Einkaufskorb hinzu und gehen Sie zur Kasse. Die Einkaufskorbpositionen werden an Microsoft Dynamics 365 übertragen.

Sind mehrere Optionen für Beschaffungskategorien vorhanden, wählen Sie die gewünschte Beschaffungskategorie aus, bevor Sie die Positionen der Bestellanforderung hinzufügen.
Nachdem Positionen zu einer Anforderung hinzugefügt wurden, können Sie mehrere Positionen hinzufügen, ohne externe Kataloge zu verwenden. Alternativ können Sie fortfahren, um externe Kataloge zu verwenden, um Positionen hinzuzufügen.

Wenn die Bestellanforderung bereit ist, verwenden Sie die Aktivität **Workflow** > **Übermitteln**, zur Genehmigung.

### <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Externen Katalog für PunchOut-E-Procurement einrichten](set-up-external-catalog-for-punchout.md)
- [cXML-Einkaufserweiterungen](purchasing-cxml-enhancements.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]