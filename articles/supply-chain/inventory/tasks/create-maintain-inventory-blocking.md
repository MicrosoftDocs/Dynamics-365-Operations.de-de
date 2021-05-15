---
title: Dient zum Erstellen und Verwalten einer Sperrung von Lagerbestand
description: Dieses Thema beschreibt, wie Sie eine Bestandssperre verwenden können, um zu verhindern, dass physische Lagerbestände durch andere ausgehende Quelldokumente reserviert werden.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956157"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Dient zum Erstellen und Verwalten einer Sperrung von Lagerbestand

[!include [banner](../../includes/banner.md)]

Dieses Thema beschreibt, wie Sie eine Bestandssperre verwenden können, um zu verhindern, dass physische Lagerbestände durch andere ausgehende Quelldokumente reserviert werden. Bevor Sie die Vorgänge in diesem Thema starten, müssen Sie ein Element haben, für das physischer Lagerbestand vorhanden ist.

## <a name="block-inventory"></a>Lagerbestand sperren

Um einen Datensatz zur Bestandssperrung zu erstellen, so dass der Bestand gesperrt wird, folgen Sie diesen Schritten.

1. Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Bestandssperrung**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie in der Kopfzeile des neuen Bestandssperrungs-Datensatzes das Feld **Elementnummer** auf das Element fest, das Sie sperren wollen, und geben Sie eine Beschreibung ein.
1. Geben Sie auf der Registerkarte **Allgemein** Inforegister im Feld **Menge** die Anzahl der zu blockierenden Elemente ein.
1. Geben Sie auf dem Inforegister **Bestandsdimensionen** den Standort und den Lagerort an, an dem sich die zu sperrenden Elemente derzeit befinden.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Aktualisieren Sie die Bedingungen der Sperrung von Lagerbestand

Um einen Datensatz zur Bestandssperrung zu aktualisieren, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Bestandssperrung**.
1. Wählen Sie im Listenbereich den entsprechenden Bestandssperrungs-Datensatz aus.
1. Bearbeiten Sie den Datensatz wie gewünscht. Sie können z. B. den Wert des Feldes **Erwartetes Datum** ändern, um anzugeben, wann der gesperrte Bestand voraussichtlich für die Reservierung verfügbar sein wird. Wenn die Option **Erwartete Zugänge** ausgewählt ist, wird das Datum auf der erwarteten Transaktion angezeigt. (Die Option **Erwartete Zugänge** ist standardmäßig ausgewählt, wenn Sie einen Datensatz für die Bestandssperrung manuell erstellen.)
1. Wählen Sie im Aktionsbereich **Speichern** aus.

## <a name="unblock-inventory"></a>Bestand entsperren

Um einen Bestandssperrungs-Datensatz zu entfernen, so dass der Bestand freigegeben wird, gehen Sie wie folgt vor.

1. Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Bestandssperrung**.
1. Wählen Sie im Listenbereich den entsprechenden Bestandssperrungs-Datensatz aus.
1. Wählen Sie im Aktivitätsbereich **Löschen**.
1. Sie werden aufgefordert, den Vorgang zu bestätigen. Wählen Sie **Ja** aus, um fortzufahren.
1. Schließen Sie die Seite.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
