---
title: Überschreiben des Standardreservierungsprinzips für Materialien in der Produktion
description: In diesem Artikel wird beschrieben, wie Sie für jede Artikelmodellgruppe ein Standardreservierungsprinzip festlegen, sodass für jeden Artikel, der Teil einer Stückliste oder einer Chargenauftragsformel für die Produktion ist, automatisch unterschiedliche Reservierungsprinzipien angewendet werden können.
author: johanhoffmann
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 87f10efd7eebdc034af3f7c9081d2674a6190b38
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334594"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a>Überschreiben des Standardreservierungsprinzips für Materialien in der Produktion

[!include [banner](../includes/banner.md)]

Mit der Funktion *Standardreservierung für Produktion überschreiben* können Sie ein Standardreservierungsprinzip für jede Artikelmodellgruppe festlegen. Daher können für jeden Artikel, der Teil einer Stückliste oder einer Chargenauftragsformel für die Produktion ist, automatisch unterschiedliche Reservierungsprinzipien angewendet werden. Sie können auswählen, ob jede Artikelmodellgruppe das für einen Auftrag festgelegte Standardreservierungsprinzip überschreiben und welches Reservierungsprinzip stattdessen verwendet werden soll (*Manuell*, *Kalkulation*, *Planung*, *Veröffentlichung* oder *Start*).

Wenn Sie einen neuen Produktionsauftrag oder Stapelauftrag erstellen, werden Sie aufgefordert, das Reservierungsprinzip auszuwählen, das auf diesen Auftrag und alle seine Stücklisten- oder Formelpositionen angewendet werden soll. Wenn die Funktion *Standardreservierung für Produktion überschreiben* verwendet wird, können einige oder alle Stücklisten- oder Formelpositionen dieses Reservierungsprinzip überschreiben und stattdessen das Reservierungsprinzip verwenden, das für die entsprechende Artikelmodellgruppe festgelegt wurde.

Wenn es beispielsweise um Rohstoffe oder Substanzen geht, die Kommissionierarbeiten erfordern, ist für Stücklisten- oder Formelpositionen, die für diese Produkte erstellt werden, eine physische Reservierung erforderlich, da die physische Reservierung eine Voraussetzung für die Generierung von Lagerarbeiten ist. Wenn die Reservierung automatisch erfolgen soll, wählen Sie normalerweise eines der folgenden Reservierungsprinzipien aus: *Kalkulation*, *Planung*, *Veröffentlichung* oder *Start*. Wenn es jedoch um Rohstoffe oder Substanzen geht, für die keine Kommissionierarbeiten erforderlich sind, da diese direkt von einem Lagerort bezogen werden, wählen Sie normalerweise das Reservierungsprinzip *Manuell* aus, das keine physischen Reservierungen vornimmt oder Kommissionierarbeiten generiert.

## <a name="turn-the-override-default-production-reservation-feature-on-or-off"></a>Funktion „Standardproduktionsreservierung überschreiben“ ein- oder ausschalten

Um diese Funktion nutzen zu können, muss sie für Ihr System aktiviert werden. Ab Supply Chain Management Version 10.0.25 ist die Funktion standardmäßig aktiviert. Ab Supply Chain Management Version 10.0.29 ist die Funktion obligatorisch und kann nicht deaktiviert werden. Wenn Sie eine ältere Version als 10.0.29 ausführen, können Administratoren diese Funktionalität ein- oder ausschalten, indem sie nach der Funktion *Standardproduktionsreservierung überschreiben* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a>Zuweisen einer Artikelmodellgruppe zu einer Produktionsreservierungsrichtlinie

1. Wechseln Sie zu **Kostenverwaltung \> Einrichtung der Bestandsbuchhaltungsrichtlinien \> Artikelmodellgruppen**.
1. Erstellen Sie eine Artikelmodellgruppe aus oder erstellen Sie eine.
1. Aktivieren Sie im Inforegister **Bestandrichtlinie** das Kontrollkästchen **Standardreservierung für Produktion überschreiben**.
1. Wählen Sie im Feld **Reservierung** das Reservierungsprinzip für Artikel aus, die zur ausgewählten Modellgruppe gehören. (Bei diesen Artikeln handelt es sich um solche, die sich in einer Stücklisten- oder Formelposition befinden.)

    - **Manuell** – Artikel in der Modellgruppe werden nicht automatisch physisch für die Produktion reserviert. Sie können jedoch nach Bedarf manuell reserviert werden.
    - **Kalkulation** – Artikel in der Modellgruppe werden bei der Kalkulation des Produktionsauftrags physisch reserviert.
    - **Planung** – Artikel in der Modellgruppe werden bei der Planung des Produktionsauftrags physisch reserviert.
    - **Veröffentlichung** – Artikel in der Modellgruppe werden bei der Freigabe des Produktionsauftrags physisch reserviert.
    - **Start** – Artikel in der Modellgruppe werden beim Start des Produktionsauftrags physisch reserviert.

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a>Beispiel: Verwendung von Reservierungsprinzipien in einem Sammel- und Verpackungsszenario

In einem 1.000-Liter-Mischer wird ein Massenschmierstoff hergestellt. Nachdem der Massenschmierstoff fertig ist, wird er zu mehreren Abfüllstationen abgepumpt, an denen Flaschen unterschiedlicher Größe befüllt werden. Nach dem Befüllen werden die Flaschen in Kartons verpackt. Diese Kartons werden dann auf Paletten geladen.

In diesem Szenario wird ein Chargenauftrag zur Herstellung von 1.000 Litern Massenschmierstoff erstellt. (Dieser Auftrag ist der Sammelauftrag.) Wenn dieser Chargenauftrag abgeschlossen ist, wird er am Materialeingangsstandort der Abfüllstationen als erledigt gemeldet. Anschließend wird ein Chargenauftrag zum Befüllen und Verpacken der einzelnen Flaschengrößen erstellt. (Diese Aufträge sind die Verpackungsaufträge.) Die Verpackungsaufträge haben eine Formel, die aus dem Massenschmierstoff, einer leeren Flasche, einem Etikett und anderen Verpackungsmaterialien besteht. Da der Massenschmierstoff direkt vom Mischtank zu den Abfüllstationen fließt, ist keine Lagerarbeit erforderlich, um diese Substanz zu entnehmen, und der Massenschmierstoff wird direkt am Eingangsstandort verbraucht. Daher ist das Reservierungsprinzip auf *Manuell* festgelegt. Die anderen Materialien werden durch Kommissionierarbeiten zur Abfüllstation gebracht. Daher ist das Reservierungsprinzip für diese Positionen beispielsweise auf *Veröffentlichung* festgelegt, damit die Reservierung automatisch erfolgt, wenn der Verpackungsauftrag freigegeben wird.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]