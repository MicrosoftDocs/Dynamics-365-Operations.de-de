---
title: "Externe Kataloge für PunchOut eProcurement verwenden"
description: "In diesem Thema wird erläutert, wie Sie externe Kataloge verwenden können, um Anforderungen zu erstellen und zu senden."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 035c5d15e5508c78dd66a349defd534bfecc96bb
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a>Externe Kataloge für PunchOut eProcurement verwenden
Wenn Sie externe Kataloge für PunchOut E-Procurement verwenden, müssen Sie Informationen zu den Produkten Ihrer Kreditoren in den eigenen Masterdaten nicht verwaltet. Stattdessen wird der Einkaufskorb auf der Website des Kreditors auf Anforderungspositionen konvertiert, die die korrekte Produktinformationen haben. 

Sie sollten die Verwaltung von Beschreibungen und Preisen der Produkte der Kreditoren in den eigenen Produktmasterdaten vermeiden. Nutzen Sie stattdessen externe Kataloge für PunchOut E-Procurement. Wenn Mitarbeiter Anforderungen erstellen, können sie auf die externe Katalogwebsite eines Kreditors zugreifen (das heißt, wenn sie das System verlassen und auf die Seite des Kreditors gehen). Die Produkte, die dem Einkaufskorb auf der Website des Kreditors hinzugefügt werden, können auf dann in Anforderungspositionen konvertiert werden. Deshalb erhalten Sie die korrekten Produktinformationen ab: Produktkennung, Name, Preis, usw.

Wenn Sie externe Kataloge verwenden, muss ein Mitarbeiter die Anforderung auf der Seite **Eigene Bestellanforderungen** erstellen.

Der Mitarbeiter, der eine Bestellanforderung erstellt, ist der Antragsteller der Bestellanforderung. Als Antragsteller können Sie die folgenden Aufgaben durchführen.

Verwenden Sie die **Externe Kataloge** Positionsaktivität, um eine Seite zu öffnen, die alle externen Kataloge enthält, die für die jeweilige anfordernde Person, die einkaufende juristische Person und die empfangende Organisationseinheit verfügbar sind.

Abhängig von Ihren Berechtigungen ändern Sie die anfordernde Person, die juristische Person und die empfangende Organisationseinheit. Eine Änderung in diesen Werten ändert möglicherweise die Liste der externen Kataloge, die für eine anfordernde Person bereitstehen. Die externen Kataloge, die verfügbar sind, hängen von der aktuellen aktiven Einkaufsrichtlinien für die kaufende juristische Person und die empfangende Organisationseinheit ab. Diese Richtlinie kann Zugriffe auf bestimmte Beschaffungskategorien gestatten oder verhindern. Daher kann die Liste der externen Kataloge, die diesen Beschaffungskategorien zugeordnet sind, betroffen sein.

Weitere Informationen zum Einrichten von Richtlinien finden Sie unter [Einkaufsrichtlinien](../procurement/purchase-policies.md)

- Wenn Sie externe Kataloge für bestimmte Beschaffungskategorien suchen, geben Sie Text im Feld "Katalogsuchgebiete" ein.
- Um Produkte aus dem externen Katalog eines Lieferanten auf der Website des Kreditors hinzuzufügen, klicken auf den externen Katalog. Fügen Sie dann Produkte zum Einkaufskorb hinzu und gehen Sie zur Kasse. Die Einkaufskorbpositionen werden an Microsoft Dynamics 365 übertragen.

Sind mehrere Optionen für Beschaffungskategorien vorhanden, wählen Sie die gewünschte Beschaffungskategorie aus, bevor Sie die Positionen der Bestellanforderung hinzufügen.
Nachdem Positionen zu einer Anforderung hinzugefügt wurden, können Sie mehrere Positionen hinzufügen, ohne externe Kataloge zu verwenden. Alternativ können Sie fortfahren, um externe Kataloge zu verwenden, um Positionen hinzuzufügen.

Wenn die Bestellanforderung bereit ist, verwenden Sie die Aktivität **Workflow** > **Übermitteln**, zur Genehmigung.

