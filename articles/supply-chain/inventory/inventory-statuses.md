---
title: Bestandsstatus
description: In diesem Artikel wird beschrieben, wie Sie den Bestandsstatus verwenden können, um Bestand zu kategorisieren und zu verfolgen.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus, WHSWarehouseStatusChange
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eca9d3e4e15d11d2a9a1b531028de230ffc43913
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594601"
---
# <a name="inventory-statuses"></a>Bestandsstatus

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie den Bestandsstatus verwenden können, um Bestand zu kategorisieren und zu verfolgen.

## <a name="set-up-and-use-inventory-statuses"></a>Bestands-Status festlegen und verwenden

Sie können Bestandsstatus verwenden, um den Bestand in Kategorien einzuteilen. Sie können dann geeignete Aktionen initiieren, wie Wiederbeschaffung oder Aufräumarbeit.

Beispiele für Methoden zur Verwendung von Bestandsstatus:

- Erstellen von Bestandsstatus für verfügbaren Lagerbestand und eingehende und ausgehende Transaktionen.
- Angeben eines standardmäßigen Bestandstatus für Lagerorttransaktionen.
- Ändern eines Bestandsstatus für Artikel vor dem Wareneingang, während des Wareneingangs oder wenn die Artikel während der Lagerumlagerung eingelagert werden.
- Verwenden eines Bestandsstatus für die Preisgestaltung von Artikeln, die zurückgegeben werden und um Artikeldeckung während der Produktprogrammplanung zu planen.

Ein Bestandsstatus ist eine der Dimensionen in der Lagerdimensionsgruppe. Bestandsstatus können als verfügbar oder nicht verfügbar kategorisiert werden, und Sie können den Parameter **Sperrung von Lagerbestand** verwenden, um Artikel zu sperren, die einen Bestandsstatus von "nicht verfügbar" haben. Artikel mit einem gesperrten Status gelten als physischer Bestand und können nicht für einen Produktionsauftrag, einen Auftrag, einen Umlagerungsauftrag oder für eine ausgehende Transaktion verwendet werden.

Sie können Lagerortartikel, die den Bestandsstatus verfügbar oder nicht verfügbar aufweisen, für eingehende Arbeit verwenden. Sie erstellen beispielsweise einen verfügbaren Status namens *Bereit*, einen nicht verfügbaren Status namens *Beschädigt* und einen gesperrten Status namens *Gesperrt*. Wenn Sie eine Bestellung für empfangene oder zurückgelieferte Artikel erstellen und irgendwelche Artikel beschädigt sind, können Sie den Lagerstatus dieser Artikel auf der Bestellposition auf *Beschädigt* ändern. Nach Erhalt dieser Artikel wird der Status automatisch auf *Gesperrt* gesetzt. Wenn Sie die beschädigten Artikel mit einem mobilen Gerät scannen, kann Supply Chain Management Lagerplatzdirektiven und Arbeitsvorlagen verwenden, um Informationen zu einem geeigneten Lagerplatz oder eine Reihe von Lagerplätzen anzeigen, wo Sie diese Artikel lagern können. Für zurückgelieferte Artikel wird der Seite *Lagerbuchungen* ein Abgangstyp **Reservierung** erstellt.

Für ausgehende Arbeit verwenden Sie Artikel, die den Bestandsstatus "verfügbar" aufweisen. Wenn Sie Artikel haben, die den Status *Beschädigt* aufweisen, und die Produktprogrammplan auf diese Artikel ausgeführt wird, werden die Artikel als fehlend betrachtet, und der Bestand wird automatisch aufgefüllt.

Nachdem Sie Bestandsstatus eingerichtet haben, können Sie den standardmäßigen Bestandsstatus für einen Standort, einen Artikel und einen Lagerort festlegen. Sie können auch einen Standardstatus für Verkauf, Umlagerung und Bestellungen festlegen. Beim Standardstatus für Aufträge und ausgehende Umlagerungsaufträge kann die Option **Sperrung von Lagerbestand** nicht auf *Ja* festgelegt sein. Der Bestandsstatus, der von den Standardeinstellungen auf einem Standort, Lagerort, Artikel, einer Bestellung, einem Umlagerungsauftrag oder einem Auftrag übernommen wird, kann mit dem mobilen Gerät oder auf der Position für Bestellung, Auftrag oder Umlagerungsauftrag geändert werden.

Um Disposition für Artikel mit einem verfügbaren Bestandsstatus zu planen, wählen Sie die Option **Disposition nach Dimensionen** für eine Lagerdimension auf der **Lagerdimensionsgruppen**-Seite aus. Wenn Sie den **Artikeldeckungs**-Assistenten öffnen, erscheinen Artikel mit einem verfügbaren Status auf der Seite **Status**. Um Deckungseinstellungen für diese Artikel zu erstellen, wählen Sie die Bestandsstatuskennung für die verfügbaren Bestandsstatus aus. Basierend auf den Deckungseinstellungen können Sie den Artikelbedarf berechnen und das Angebot und die Nachfrage der verfügbaren Artikeln während der Produktprogrammplanung planen. Sie können keine Artikeldeckungseinstellungen erstellen, die einen gesperrten Bestandsstatus aufweisen. Alternativ können Sie die Seite **Artikeldeckung** verwenden, um die Artikeldeckungsparameter zu erstellen oder zu ändern.

## <a name="change-inventory-statuses"></a>Ändern von Bestandszuständen

Sie können Bestandsstatus entweder über die Seite **Bestand nach Lagerplatz** oder über die periodische Aufgabe *Bestandsstatus ändern* ändern.

- Wenn Sie die periodische Aufgabe *Bestand ändern* verwenden, können Sie auswählen, welche Datensätze einbezogen werden sollen und die Aufgabe so festlegen, dass sie im Batch im gewünschten Intervall läuft.
- Um den Bestand als Ad-hoc-Prozess zu ändern, gehen Sie auf die Seite **Bestand nach Lagerplatz**, wählen die relevanten Datensätze aus und wählen dann die Schaltfläche **Bestand ändern**.

> [!NOTE]
> Mit der Funktion *Ändern des Bestandsstatus von Elementen, die von Tracking-Dimensionen gesteuert werden*, können Sie den Bestandsstatus von Elementen ändern, die von Tracking-Dimensionen gesteuert werden, einschließlich der Möglichkeit, nur ausgewählte Datensätze zu aktualisieren. Verwenden Sie [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um die Funktion nach Bedarf zu aktivieren. Wenn die Funktion aktiviert ist, können Sie Folgendes tun:
>
> - Auf der Seite **Bestand nach Lagerplatz** können Sie mit der Schaltfläche **Dimensionen anzeigen** Zeilen auf Basis der angezeigten Dimensionen gruppieren und den Status für die ausgewählten Zeilen ändern.
> - Auf der Seite **Bestand nach Lagerplatz** können Sie mehrere Datensätze auswählen und dann die Schaltfläche **Status des Bestands ändern** verwenden, um alle auf einmal zu ändern.
> - Auf der Seite **Bestandsstatus ändern** können Sie nach Dimensionen der Verfolgung filtern.
