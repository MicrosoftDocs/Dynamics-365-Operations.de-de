---
title: Inventory Visibility-Unterstützung für WHS-Artikel
description: Dieser Artikel beschreibt die Unterstützung von Inventory Visibility (Bestandsanzeige) für Artikel, die für erweiterte Lagerprozesse (WHS-Artikel) aktiviert sind.
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: ec2254d6cf203216acea88fdfb54ad491abdeb49
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895669"
---
# <a name="inventory-visibility-support-for-whs-items"></a>Inventory Visibility-Unterstützung für WHS-Artikel

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Unterstützung von Inventory Visibility (Bestandsanzeige) für Artikel, die für erweiterte Lagerprozesse (WHS-Artikel) aktiviert sind. Die Funktion, die diese Funktion zur Inventory Visibility hinzufügt, trägt den Namen *Erweiterte WHS*.

## <a name="whs-items"></a>WHS-Artikel

Ein WHS-Artikel ist ein Artikel, der für erweiterte Lagerortprozesse (Advanced Warehouse Processes, WHS) aktiviert ist und in einem Lager verarbeitet wird, das ebenfalls WHS-fähig ist.

Weitere Informationen über WHS und die **Warehouse Management**-Modul in Microsoft Dynamics 365 Supply Chain Management finden Sie in der [Übersicht über die Lagerverwaltung](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Bereich der Funktion

Die erweiterte WHS-Funktion für Inventory Visibility konzentriert sich auf Berechnungen der verfügbaren Menge, die auf verfügbaren Abfragen basieren. Die Funktion ist nicht dazu gedacht, Ihnen die Verwendung von Inventory Visibility zu ermöglichen, um Lagerverarbeitungsaktivitäten im Allgemeinen zu verwalten. Inventory Visibility legt den Benutzern keine lagerhausspezifischen Konzepte offen. Beispiele für diese Konzepte:

- Reservierungshierarchie
- Ob ein Artikel oder Warenlager WHS-fähig ist
- Kennung der Einheitensequenzgruppe
- Lagerspezifische Prozesse wie Sendungen, Ladungen, Wellen und Arbeit

Inventory Visibility leitet diese Informationen basierend auf den Daten ab, die von Supply Chain Management gesendet werden. Die WHS-spezifischen Daten (also Daten aus der `WHSInventReserve`-Tabelle) ist für Benutzer nicht sichtbar.

Wenn Sie die erweiterte WHS-Funktion für Inventory Visibility verwenden, sind alle Abfrageergebnisse identisch mit den Ergebnissen von Abfragen, die direkt in Supply Chain Management durchgeführt werden. Sie sind jedoch nicht mit den Ergebnissen von Abfragen identisch, die mit der mobilen Warehouse Management-App erstellt werden, da die mobile App eine etwas andere Berechnungslogik verwendet.

## <a name="when-to-use-the-feature"></a>Wann Sie die Funktion verwenden sollten

Wir empfehlen, dass Sie die erweiterte WHS-Funktion für Inventory Visibility in Szenarien verwenden, in denen alle folgenden Bedingungen erfüllt sind:

- Sie synchronisieren Supply Chain Management-Daten mit Inventory Visibility.
- Sie verwenden WHS in Supply Chain Management.
- Benutzer nehmen Reservierungen für WHS-Artikel auf anderen Ebenen als der Lagerebene vor (z. B. weil Sie Lagerarbeit verwenden).

In anderen Szenarien sind die verfügbaren Abfrageergebnisse gleich, unabhängig davon, ob die erweiterte WHS-Funktion für Inventory Visibility aktiviert ist. Darüber hinaus ist die Leistung besser, wenn Sie die Funktion in diesen Szenarios nicht aktivieren, da weniger Berechnungen und weniger Overhead anfallen.

## <a name="enable-the-advanced-whs-feature-for-inventory-visibility"></a>Die erweiterte WHS-Funktion für Inventory Visibility aktivieren

Gehen Sie folgendermaßen vor, um die erweiterte WHS-Funktion für Inventory Visibility zu aktivieren.

1. Melden Sie sich bei Supply Chain Management als Administrator an.
1. Öffnen Sie den Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und aktivieren Sie die folgenden Funktionen in dieser Reihenfolge:

    1. *Integration der Bestandssichtbarkeit*
    1. *Lagerortartikel in Bestandsanzeige aktivieren*

1. Gehen Sie zu **Bestandsverwaltung \> Einrichtung \> Bestandssichtbarkeit-Integrationsparameter**.
1. Auf der Registerkarte **WHS-Artikel aktivieren** legen Sie die Option **WHS-Artikel aktivieren** auf *Ja* fest.
1. Melden Sie sich bei Power Apps an.
1. Öffnen Sie die Seite **Konfiguration**, und aktivieren Sie dann auf der Registerkarte **Funktionsverwaltung** die Funktion *AdvancedWHS*.
1. Gehen Sie in Supply Chain Management zu **Lagerverwaltung \> Periodische Aufgaben \> Integration der Bestandssichtbarkeit**.
1. Wählen Sie im Aktivitätsbereich **Deaktivieren** aus, um Inventory Visibility vorübergehend zu deaktivieren.
1. Wählen Sie im Aktivitätsbereich **Aktivieren** aus, um Inventory Visibility wieder zu aktivieren. Das Add-In wird neu geladen, und die neue Funktion ist jetzt aktiviert. Ihre WHS-bezogenen Daten werden mit Inventory Visibility synchronisiert.

## <a name="query-on-hand-quantities-of-whs-items"></a>Abfrage verfügbarer Mengen von WHS-Artikeln

Um WHS-Artikel abzufragen, verwenden Sie dieselbe [Anwendungsprogrammierschnittstelle (API) und Nachrichtensyntax](inventory-visibility-api.md), die Sie für Nicht-WHS-Artikel verwenden. Sie müssen nicht angeben, ob ein Artikel ein WHS-Artikel oder ein Nicht-WHS-Artikel ist. Inventory Visibility unterscheidet Artikel automatisch anhand der gespeicherten Daten.

Die Ergebnisse von Abfragen für WHS-Artikel sind im Wesentlichen die gleichen wie die Ergebnisse für Nicht-WHS-Artikel. Der einzige Unterschied besteht darin, dass die folgenden physikalischen Maßnahmen von der `fno`-Datenquelle basierend auf der WHS-Logik in Supply Chain Management berechnet werden:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Alle anderen physikalischen Maße werden genau so berechnet, wie sie sind, wenn die erweiterte WHS-Funktion für Inventory Visibility deaktiviert ist.

Ausführliche Informationen zur Funktionsweise von Lagerbestandsberechnungen für WHS-Artikel finden Sie im Whitepaper zu [Reservierungen in Warehouse Management](https://www.microsoft.com/download/details.aspx?id=43284).

Die Datenentitäten, die in Dataverse exportiert werden, können die Mengen für WHS-Artikel noch nicht aktualisieren. Die in den Datenentitäten angezeigten Mengen sind sowohl für Nicht-WHS-Artikel als auch für Mengen, die nicht von der WHS-Logik betroffen sind (d. h. Maßnahmen außer `AvailPhysical`, `AvailOrdered`, `ReservPhysical` und`ReservOrdered` in der `fno`-Datenquelle), korrekt.

Änderungen an WHS-Artikelmengen, die in der Supply Chain Management-Datenquelle gespeichert sind, sind verboten. Wie bei anderen Funktionen von Inventory Visibility wird diese Einschränkung erzwungen, um Konflikte zu vermeiden.

## <a name="soft-reservations-on-whs-items-in-inventory-visibility"></a>Unverbindliche Reservierung für WHS-Artikel in Inventory Visibility

Im Allgemeinen werden [unverbindliche Reservierungen](inventory-visibility-reservations.md) für WHS-Artikel unterstützt. Sie können WHS-bezogene physische Maße in unverbindlichen Reservierungsberechnungen einbeziehen. 

Bei einer bekannten Einschränkung wird die Berechnung *zur Reservierung verfügbar* derzeit für WHS-Artikel nicht unterstützt. Wenn daher eine Reservierung über den aktuellen Dimensionen besteht, bei der eine unverbindliche Reservierung auftritt, ist die Berechnung *zur Reservierung verfügbar* falsch. Unverbindliche Reservierungen sind nicht davon betroffen, wenn die Option **ifCheckAvailForReserv** in der [unverbindlichen Reservierungs-API](inventory-visibility-api.md#create-one-reservation-event) deaktiviert ist.

Diese Einschränkung gilt auch für Funktionen und Anpassungen, die auf unverbindlichen Reservierungen (z. B. Zuteilung) basieren.

## <a name="calculate-available-to-promise-quantities"></a>Für Zusage verfügbare Mengen berechnen

Die Lösung unterstützt [verfügbar für Zusage (VfZ)](inventory-visibility-available-to-promise.md) vollständig für WHS-Artikel. Sie können VfZ-Berechnungen definieren, ohne sich um WHS-spezifische Details kümmern zu müssen.
