---
title: Produktionsbuchungen
description: Dieser Artikel enthält Informationen über die unterschiedlichen Arten von Buchungen im Produktionsprozess fest.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemGroup, ProjCategory, WrkCtrResourceGroup, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 54591
ms.assetid: 0917fe64-f643-46ae-98ff-5013b266a067
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 20a94ed3c64e81013edfa10e060dd32e04d12577
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214480"
---
# <a name="production-posting"></a>Produktionsbuchungen

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen über die unterschiedlichen Arten von Buchungen im Produktionsprozess fest.

Aktivitäten rund um Produktionsbuchungen folgen Produktionsprozessen, die in den Bereichen nachfolgend beschrieben werden.

## <a name="material-consumption"></a>Materialverbrauch
Materialien werden während der Produktion als verbraucht erfasst, wenn die Produktionskommissionierlistenerfassung gebucht wird. Dieser Prozess generiert Abgangsbuchungen, die den verfügbaren Lagerbestand abziehen. In den Produktionsparametern können Sie angeben, ob der Wert von Rohmaterialien, die sich in Bearbeitung befinden (Ressource in Fertigung \[WIP\]) im Sachkonto gebucht werden soll. Der Wert von Rohmaterialien, die sich in Bearbeitung befinden (RIF) wird dann in ein dediziertes Kommissionierlistenkonto und in ein dediziertes Kommissionierlistengegenkonto gebucht.

## <a name="time-consumption"></a>Zeitaufwand
Die Zeit, die Arbeitskräfte für Produktions-Einzelvorgänge arbeiten, wird in der Arbeitsplanlisten-Erfassung oder in der Einzelvorgangslisten-Erfassung erfasst. Wenn diese Erfassungen gebucht werden, werden sie von der Sachkontobuchung in einem dedizierten Konto für Ressourcen verarbeitet, die in Bearbeitung sind (RIF). Diese Buchung repräsentiert den Wert der Zeit, die im Produktionsauftrag entlohnt wird. Nachdem der Produktionsauftrag als Fertig erfasst wurde, werden die RIF-Konten ausgeglichen.

## <a name="reporting-finished-goods-and-error-quantities"></a>Berichterstellungsendprodukte und -Ausschussmengen
Wenn ein Produktionsauftrag als fertig gemeldet wird, wird die Menge der fertigen Güter, die fertig gestellt wurden, im Lagerbestand durch die Fertigmeldungs-Erfassung aktualisiert. Bei Verwendung der RIF-Buchführung, die sich in den Produktionsparametern einstellen lässt, wird eine Sachkontenerfassung erstellt, mit der die RIF-Konten belastet und der Bestand an fertig gestellten Gütern vergrößert wird. Die Erfassung verwendet die Standardkosten, die für das Produkt definiert sind.

## <a name="ending-the-production-order"></a>Den Produktionsauftrag beenden
Vor dem Beenden eines Produktionsauftrags werden die tatsächlichen Kosten für die produzierte Menge berechnet. Alle vorkalkulierten Material-, Arbeits- und Gemeinkosten werden storniert und durch die Istkosten ersetzt. Die Gesamtkosten des fertigen Artikels werden als Sollbuch auf dem Lagerkonto Zugang und als Habenbuch auf dem Lagerkonto Abgänge erfasst. Wenn Sie beim Ausführen der Kostenberechnung das Kontrollkästchen **Abschluss-Einzelvorgang** auswählen, ändert sich der Produktionsauftragsstatus zu **Abgeschlossen**. Mit diesem Status wird sichergestellt, dass für einen abgeschlossenen Produktionsauftrag keine weiteren Kosten mehr gebucht werden können. Sie können angeben, dass der Wert aus Ausschussmengen, die bei der Fertigmeldung fertig gestellten so gemeldet werden, um in die Gutmengen zugewiesen werden soll, die als abgeschlossen gemeldet werden. Alternativ können Sie angeben, dass der Wert von Ausschussmengen in ein dediziertes Ausschusskonto gebucht werden soll.

## <a name="controlling-the-level-of-ledger-posting"></a>Steuern der Ebene der Sachkontobuchung
In den **Produktionssteuerungsparametern** können Sie das Feld **Sachkontobuchung** verwenden, um die Ebene der Sachkontobuchung für Produktionsprozesse festzulegen. Folgende Werte sind verfügbar:

-   **Artikel und Ressource** - Verwenden Sie die Sachkonten, die in den Artikelgruppen für Rohmaterialen und Fertigerzeugnisse eingerichtet werden. RIF für Zeitverbrauch wird aus der Ressource oder von der Ressourcengruppe aus den Arbeitsplan-Arbeitsgängen übernommen.
-   **Artikel und Kategorie** - Verwenden Sie die Sachkonten, die in den Artikelgruppen für Rohmaterialen und Fertigerzeugnisse eingerichtet werden. RIF für Zeitverbrauch wird von Kostenkategorien entnommen, der den Arbeitsplan-Arbeitsgängen zugeordnet sind.
-   **Produktionsbuchungsprofile** - Verwenden Sie die Sachkonten, die auf den Produktionsgruppen für Material eingerichtet werden und Zeiteinsatz. Die Produktionsgruppen werden mit den freigegebenen Produkten zugeordnet und zu den Produktionsaufträgen kopiert, wenn diese Aufträge erstellt werden. Die Buchung in den Produktionsaufträgen folgt dann den Produktionsgruppen, die dem Produktionsauftrag zugeordnet sind.

**Hinweis:** Wenn die Standardmethode für die Berechnung der Kosten des Fertigartikels verwendet wurde, wird dies auch in der Abschlussbuchung wiedergegeben. Ergibt sich bei Verwendung der Standardmethode ein Unterschied zwischen den Istkosten und den berechneten Kosten, so wird dieser auf dem Konto als Gewinn oder Verlust gebucht.



