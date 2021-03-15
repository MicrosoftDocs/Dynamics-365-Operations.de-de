---
title: Waren zur doppelten Verwendung
description: In diesem Thema wird erläutert, wie Produkte nachverfolgt werden, die als Waren mit doppeltem Verwendungszweck identifiziert wurden, Zertifikatsnummern für jedes relevante Produkt und Zielland gespeichert werden und gültige Zertifikatsnummern auf relevanten Rechnungen, Lieferscheinen und/oder Aufträgen gedruckt werden.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COODualUseCerts, COORules, COODualUseCountries
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 4623b6eaa18b65f0f61cb8c227115d59f3ff9c08
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007697"
---
# <a name="dual-use-goods"></a>Waren zur doppelten Verwendung

[!include [banner](../includes/banner.md)]

Waren zur doppelten Verwendung sind typischerweise Artikel, die sowohl zivile als auch militärische Anwendungen haben. Beispielsweise kann eine Chemikalie entweder als Dünger oder als Sprengstoff verwendet werden. In vielen Ländern gelten besondere Vorschriften für den Export, Import und Transport von Waren mit doppelter Verwendung. Daher ist es wichtig, dass Unternehmen, die am internationalen Handel mit Waren mit doppelter Verwendung beteiligt sind, die verschiedenen Richtlinien und Zertifikate im Auge behalten.

Die Funktion für die doppelte Verwendung unterstützt Unternehmen bei der Nachverfolgung von Produkten, die als Waren mit doppelter Verwendung identifiziert wurden. Die Funktion speichert Zertifikatsnummern für jedes relevante Produkt und Zielland und druckt gültige Zertifikatsnummern auf relevanten Rechnungen, Lieferscheinen und/oder Aufträgen. Dies hilft sicherzustellen, dass Ihre Produkte beim Versand immer aktuelle Zertifizierungen enthalten.

Bedenken Sie folgendes Szenario:

1. Die Seite **Ländereinstellungen für die doppelte Verwendung** in Ihrem System gibt an, dass für Lieferungen nach Frankreich eine Zertifizierung erforderlich ist.
2. Die Seite **Freigegebene Produktdetails** für Produkt X-100 gibt an, dass es sich um eine Ware mit doppelter Verwendung handelt. Code, Kategorie, Gruppe und Regime geben die Exportkontrollklassifizierung an, zu der das Produkt gehört.
3. Die Seite **Zertifikate für doppelte Verwendung** umfasst ein Zertifikat für Produkt X-100, wenn es nach Frankreich geliefert wird. Dieses Zertifikat läuft am 1. Januar 2020 ab.
4. Am 17. Juni 2020 erstellen Sie einen Auftrag für ein Kundenunternehmen mit Sitz in Frankreich, und der Auftrag enthält das Produkt X-100.
5. Wenn Sie den Auftrag speichern, ermittelt das System die folgenden Informationen:

    1. Enthält der Auftrag Produkte, bei denen es sich um Waren mit doppelter Verwendung handelt?
    2. Wenn der Auftrag Waren mit doppelter Verwendung enthält, benötigt das Zielland Zertifikate für die doppelte Verwendung?
    3. Wenn das Land Zertifikate für die doppelte Verwendung vorschreibt, gibt es für jede Ware mit doppelter Verwendung ein gültiges Zertifikat für das Zielland?

6. Der Auftrag umfasst das Produkt X-100, das Produkt wird nach Frankreich geliefert und für das Produkt liegt ein französisches Zertifikat vor. Das Zertifikat ist jedoch abgelaufen. Daher erhalten Sie die folgende Warnmeldung: „Zertifkate für die doppelte Verwendung für mindestens einen Artikel mit doppelter Verwendung in diesem Auftrag sind nicht gültig. Möchten Sie mit der Bestätigung fortfahren?“

In diesem Thema wird erläutert, wie Sie alle Einstellungen konfigurieren, die zum Einrichten von Waren mit doppelter Verwendung und zum Unterstützen dieses Szenarios erforderlich sind.

## <a name="define-dual-use-requirements-for-each-relevant-country"></a>Definieren Sie Anforderungen für die doppelte Verwendung für jedes relevante Land

Verschiedene Länder haben unterschiedliche Anforderungen für Waren mit doppelter Verwendung. Sie verwenden die Seite **Ländereinstellungen für die doppelte Verwendung**, um die Länder nachzuverfolgen, die ein Zertifikat benötigen und nicht. Die Informationen, die Sie hier angeben, werden beim Erstellen von Aufträgen überprüft und Sie werden daran erinnert, die erforderlichen Zertifizierungen bereitzustellen.

Führen Sie diese Schritte aus, um die Informationen zu Anforderungen für die doppelte Verwendung für verschiedene Länder einzurichten.

1. Gehen Sie zu **Produktinformationsverwaltung \> Setup \> Produktkonformität \> Produkte mit doppelter Verwendung \> Ländereinstellungen für doppelte Verwendung**.
2. Wählen Sie vorhandene Ländereinstellungen zum Bearbeiten aus oder wählen Sie **Neu** im Aktivitätsbereich aus, um neue Ländereinstellungen zu erstellen.
3. Legen Sie die folgenden Werte für die ausgewählten oder neuen Ländereinstellungen fest.

    | Feld | Beschreibung |
    |---|---|
    | Land/Region | Wählen Sie das Land aus, für das Sie Anforderungen nachverfolgen. |
    | Zertifikat erforderlich | Aktivieren Sie dieses Kontrollkästchen für Länder, die eine Zertifizierung für Waren mit doppelter Verwendung vorschreiben. Deaktivieren Sie es für Länder, die diese Zertifizierung nicht vorschreiben. |

## <a name="create-dual-use-categories"></a>Kategorien für die doppelte Verwendung erstellen

Waren mit doppelter Verwendung müssen häufig nach ihrer Export Control Classification Number (Ausfuhrkontrollklassifizierungsnummer; ECCN) kategorisiert werden. Die ECCN ist ein alphanumerischer Code, der Artikel anhand von Faktoren wie Ware und Technologie kategorisiert. Mithilfe der Seite **Kategorien für doppelte Verwendung** können Sie für Berichterstellungszwecke eine Liste der Kategorien erstellen, die Sie verwenden.

Um Kategorien für doppelte Verwendung einzurichten, folgen Sie diesen Schritten.

1. Gehen Sie zu **Produktinformationsverwaltung \> Setup \> Produktkonformität \> Produkte mit doppelter Verwendung \> Kategorien für doppelte Verwendung**.
2. Wählen Sie eine vorhandene Kategorie zum Bearbeiten aus oder wählen Sie **Neu** im Aktivitätsbereich aus, um ein neue Kategorie zu erstellen.
3. Legen Sie die folgenden Werte für die ausgewählte oder neue Kategorie fest.

    | Felder | Beschreibung |
    |---|---|
    | Code für doppelte Verwendung | Geben Sie den vollständigen ECCN-Code ein (z. B. *3A001*).|
    | Kategorie für doppelte Verwendung | Geben Sie den Kategorieteil der Handelskontrollliste (Commerce Control List; CCL) des ECCN-Code ein. Zum Beispiel für den ECCN-Code *3A001* ist dieser Wert *3*. |
    | Gruppe für doppelte Verwendung | Geben Sie den Produktgruppenteil des ECCN-Codes ein. Zum Beispiel für den ECCN-Code *3A001* ist dieser Wert *A*. |
    | System zur doppelten Verwendung | Geben Sie den Systemcode für den Artikel ein. Dieser Code gibt den Grund an, warum der Artikel als Ware zur doppelten Verwendung eingestuft wird. Zum Beispiel für den ECCN-Code *3A001* ist dieser Wert *001*. |

## <a name="apply-dual-use-categories-to-products"></a>Wenden Sie Kategorien der doppelten Verwendung auf Produkte an

Führen Sie die folgenden Schritte aus, um ein Produkt als Ware zur doppelten Verwendung zu identifizieren und eine Kategorie der doppelten Verwendung darauf anzuwenden.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie ein Produkt aus oder erstellen Sie es, um seine Seite **Freigegebene Produktdetails** zu öffnen.
1. Auf dem Inforegister **Außenhandel** legen Sie die Option **Produkte zur doppelten Verwendung** auf **Ja** fest, um das aktuelle Produkt als Ware zur doppelten Verwendung zu identifizieren.
1. Legen Sie das Feld **Code für doppelte Verwendung** auf den Code fest, der für das aktuelle Produkt gilt. (Sie haben diesen Code auf der Seite **Kategorien der doppelten Verwendung** definiert.)

Dieses Setup wird überprüft, wenn Sie einen Auftrag erstellen.

## <a name="set-up-dual-use-certificates"></a>Zertifikate für doppelte Verwendung einrichten

Sie verwenden die Seite **Zertifikate für doppelte Verwendung**, um die erforderlichen Zertifikate für doppelte Verwendung für jedes Produkt und Land zu verwalten. Sie können die Details jedes Zertifikats nachverfolgen, z. B. das Land und die Gültigkeitsdatumsangaben. Sie können auch Optionen festlegen, um anzugeben, wo diese Informationen gedruckt werden sollen. Beispielsweise können die Informationen auf der Rechnung, dem Lieferschein und/oder dem Auftrag gedruckt werden. Dieses Setup wird überprüft, wenn Sie einen Auftrag erstellen.

1. Gehen Sie zu **Produktinformationsverwaltung \> Setup \> Produktkonformität \> Produkte mit doppelter Verwendung \> Zertifikate für doppelte Verwendung**.
2. Wählen Sie ein vorhandenes Zertifikat zum Bearbeiten aus oder wählen Sie **Neu** im Aktivitätsbereich aus, um ein neues Zertifikat zu erstellen.
3. Legen Sie die folgenden Werte für das ausgewählte oder neue Zertifikat fest.

    | Feld | Beschreibung |
    |---|---|
    | Artikelnummer | Wählen Sie die Artikelnummer der Ware zur doppelten Verwendung aus, für die dieses Zertifikat gilt. |
    | Land/Region | Das Zielland oder die Zielregion, in der Sie dieses Zertifikat verwenden müssen. |
    | Zertifikatnummer | Die Nummer, die auf dem Zertifikat angezeigt wird, das dem Lieferanten oder Kunden ausgestellt wird. |
    | In Kraft | Wählen Sie das erste Datum aus, an dem das aktuelle Zertifikat gültig ist.|
    | Ablaufdatum | Wählen Sie das letzte Datum aus, an dem das aktuelle Zertifikat gültig ist. |
    | Auf Rechnung drucken | Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Rechnungen zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind. |
    | Auf Lieferscheinen drucken | Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Lieferscheine zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind. |
    | Auf Auftrag drucken | Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Aufträge zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]