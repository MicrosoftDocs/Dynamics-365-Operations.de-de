---
title: Inventory Visibility-Unterstützung für WMS-Artikel
description: Dieser Artikel beschreibt die Unterstützung der Inventory Visibility für Artikel, die für Lagerverwaltungsprozesse aktiviert sind (WMS-Artikel).
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: bed402ecf20c19e81b2687efd90dba600460971a
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762738"
---
# <a name="inventory-visibility-support-for-wms-items"></a>Inventory Visibility-Unterstützung für WMS-Artikel

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Unterstützung der Inventory Visibility für Artikel, die für Lagerverwaltungsprozesse (WMS) aktiviert sind. Die Funktion, die diese Funktion zur Inventory Visibility hinzufügt, trägt den Namen *Erweiterte WMS*.

## <a name="wms-items"></a>WMS-Artikel

Ein WMS-Artikel ist ein Artikel, der für WMS aktiviert ist und in einem Lager verarbeitet wird, das ebenfalls WMS-fähig ist.

Weitere Informationen über WMS und die **Warehouse Management**-Modul in Microsoft Dynamics 365 Supply Chain Management finden Sie in der [Übersicht über die Lagerverwaltung](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Bereich der Funktion

Die erweiterte WMS-Funktion für Inventory Visibility konzentriert sich auf Berechnungen der verfügbaren Menge, die auf verfügbaren Abfragen basieren. Die Funktion ist nicht dazu gedacht, Ihnen die Verwendung von Inventory Visibility zu ermöglichen, um Lagerverarbeitungsaktivitäten im Allgemeinen zu verwalten. Inventory Visibility legt den Benutzern keine lagerhausspezifischen Konzepte offen. Beispiele für diese Konzepte:

- Reservierungshierarchie
- Ob ein Artikel oder Warenlager WMS-fähig ist
- Kennung der Einheitensequenzgruppe
- Lagerspezifische Prozesse wie Sendungen, Ladungen, Wellen und Arbeit

Inventory Visibility leitet diese Informationen basierend auf den Daten ab, die von Supply Chain Management gesendet werden. Die WMS-spezifischen Daten (also Daten aus der `WHSInventReserve`-Tabelle) ist für Benutzer nicht sichtbar.

Wenn Sie die erweiterte WMS-Funktion für Inventory Visibility verwenden, sind alle Abfrageergebnisse identisch mit den Ergebnissen von Abfragen, die direkt in Supply Chain Management durchgeführt werden. Sie sind jedoch nicht mit den Ergebnissen von Abfragen identisch, die mit der mobilen Warehouse Management-App erstellt werden, da die mobile App eine etwas andere Berechnungslogik verwendet.

## <a name="when-to-use-the-feature"></a>Wann Sie die Funktion verwenden sollten

Wir empfehlen, dass Sie die WMS-Funktion für Inventory Visibility in Szenarien verwenden, in denen alle folgenden Bedingungen erfüllt sind:

- Sie synchronisieren Supply Chain Management-Daten mit Inventory Visibility.
- Sie verwenden WMS in Supply Chain Management.
- Benutzer nehmen Reservierungen für WMS-Artikel auf anderen Ebenen unterhalb der Lagerebene vor (z. B. auf Ladungsträgerebene, weil Sie Lagerarbeit verarbeiten).

In anderen Szenarien sind die verfügbaren Abfrageergebnisse gleich, unabhängig davon, ob die erweiterte WMS-Funktion für Inventory Visibility aktiviert ist. Darüber hinaus ist die Leistung besser, wenn Sie die Funktion in diesen Szenarios nicht aktivieren, da weniger Berechnungen und weniger Overhead anfallen.

## <a name="enable-the-wms-feature-for-inventory-visibility"></a>Die WMS-Funktion für Bestandsanzeige aktivieren

Gehen Sie folgendermaßen vor, um die WMS-Funktion für Inventory Visibility zu aktivieren.

1. Melden Sie sich bei Supply Chain Management als Administrator an.
1. Öffnen Sie den Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und aktivieren Sie die folgenden Funktionen in dieser Reihenfolge:

    1. *Integration der Bestandssichtbarkeit*
    1. *Lagerortartikel in Bestandsanzeige aktivieren*

1. Gehen Sie zu **Lagerverwaltung \> Einstellungen \> Bestandssichtbarkeit-Integrationsparameter**.
1. Auf der Registerkarte **WMS-Artikel aktivieren** legen Sie die Option **WMS-Artikel aktivieren** auf *Ja* fest.
1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**, und aktivieren Sie dann auf der Registerkarte **Funktionsverwaltung** die Funktion *AdvancedWHS*.
1. Gehen Sie in Supply Chain Management zu **Lagerverwaltung \> Periodische Aufgaben \> Integration der Bestandssichtbarkeit**.
1. Wählen Sie im Aktivitätsbereich **Deaktivieren** aus, um Inventory Visibility vorübergehend zu deaktivieren.
1. Wählen Sie im Aktivitätsbereich **Aktivieren** aus, um Inventory Visibility wieder zu aktivieren. Das Add-In wird neu geladen, und die neue Funktion ist jetzt aktiviert. Ihre WMS-bezogenen Daten werden mit Inventory Visibility synchronisiert.

## <a name="query-on-hand-quantities-of-wms-items"></a>Abfrage verfügbarer Mengen von WMS-Artikeln

Um WMS-Artikel abzufragen, verwenden Sie dieselbe [Anwendungsprogrammierschnittstelle (API) und Nachrichtensyntax](inventory-visibility-api.md), die Sie für Nicht-WMS-Artikel verwenden. Sie müssen nicht angeben, ob ein Artikel ein WMS-Artikel oder ein Nicht-WMS-Artikel ist. Inventory Visibility unterscheidet Artikel automatisch anhand der gespeicherten Daten.

Die Ergebnisse von Abfragen für WMS-Artikel sind im Wesentlichen die gleichen wie die Ergebnisse für Nicht-WMS-Artikel. Der einzige Unterschied besteht darin, dass die folgenden physikalischen Maßnahmen von der `fno`-Datenquelle basierend auf der WMS-Logik in Supply Chain Management berechnet werden:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Alle anderen physikalischen Maße werden genau so berechnet, wie sie sind, wenn die WMS-Funktion für Inventory Visibility deaktiviert ist.

Ausführliche Informationen zur Funktionsweise von Lagerbestandsberechnungen für WMS-Artikel finden Sie im Whitepaper zu [Reservierungen in Warehouse Management](https://www.microsoft.com/download/details.aspx?id=43284).

## <a name="on-hand-list-view-and-data-entity-for-wms-items"></a>Verfügbare Listenansicht und Datenentität für WMS-Artikel

Die Seite **Zusammenfassung der Inventory Visibility vorladen** bietet eine Ansicht für die Entität *Ergebnisse der vorgeladenen Indexabfrage*. Im Gegensatz zur Entität *Bestandsübersicht* bietet die Entität *Bestandsindexabfrage Ergebnisse vorladen* eine Bestandsliste für Produkte zusammen mit ausgewählten Dimensionen. Inventory Visibility synchronisiert die vorgeladenen Zusammenfassungsdaten alle 15 Minuten.

Wenn Sie die Bestandsanzeige mit WMS-Artikeln verwenden und die verfügbare Liste für WMS-Artikel anzeigen möchten, empfehlen wir Ihnen, die *Laden Sie die Zusammenfassung der Inventarsichtbarkeit vorab* Funktion (siehe auch [Laden Sie eine optimierte verfügbare Abfrage vorab](inventory-visibility-power-platform.md#preload-streamlined-onhand-query)) zu aktivieren. Eine entsprechende Datenentität in Dataverse speichert das Ergebnis Ihres Abfragevorabladens, das alle 15 Minuten aktualisiert wird. Der Name der Datenentität lautet `Onhand Index Query Preload Result`.

> [!IMPORTANT]
> Die Dataverse Entität ist schreibgeschützt. Sie können die Daten in den Inventarsichtbarkeitseinheiten anzeigen und exportieren, aber **ändern Sie es nicht**.

Änderungen an WMS-Artikelmengen, die in der Supply Chain Management-Datenquelle (`fno`) gespeichert sind, sind verboten. Dieses Verhalten entspricht dem Verhalten anderer Funktionen von der Bestandsanzeige. Diese Einschränkung wird erzwungen, um Konflikte zu vermeiden.

## <a name="wms-item-compatibility-for-other-functions-in-inventory-visibility"></a>WMS-Artikelkompatibilität für andere Funktionen in der Bestandsanzeige

[Soft-Reservierungen](inventory-visibility-reservations.md) und [Bestandszuordnung](inventory-visibility-allocation.md) von WMS-Artikeln werden unterstützt. Sie können WMS-bezogene physische Maße in unverbindlichen Reservierungs- und Zuteilungsberechnungen einbeziehen.

## <a name="calculate-available-to-promise-quantities"></a>Für Zusage verfügbare Mengen berechnen

Die Lösung unterstützt vollständig [zur Zusage verfügbar (ATP)](inventory-visibility-available-to-promise.md) für WMS-Artikel. Sie können ATP-Berechnungen definieren, ohne sich um WMS-spezifische Details kümmern zu müssen.
