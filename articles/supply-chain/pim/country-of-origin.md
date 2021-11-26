---
title: Ursprungsland
description: Viele Organisationen stellen ihren Lieferanten Zertifikate aus, um sicherzustellen, dass die Produkte bestimmten Zertifizierungsstandards entsprechen. Diese Zertifikate hängen häufig vom Herkunftsland ab. Dieses Thema enthält Informationen zur Herkunftslandfunktion, mit der Sie ein Produkt mit seinem Herkunftsland verknüpfen und die Produktzertifizierungen verfolgen können.
author: t-benebo
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: a2740f6b1ccb52073b013e613d8ab779cc088180
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777620"
---
# <a name="country-of-origin"></a>Ursprungsland

[!include [banner](../includes/banner.md)]

Viele Organisationen stellen ihren Lieferanten Zertifikate aus, um sicherzustellen, dass die Produkte bestimmten Zertifizierungsstandards entsprechen. Diese Zertifikate hängen häufig vom Herkunftsland ab. Mit der Herkunftslandfunktion können Sie ein Produkt mit seinem Herkunftsland verknüpfen und seine Produktzertifizierungen nachverfolgen.

## <a name="turn-on-the-country-of-origin-feature"></a>Aktivieren der Herkunftslandfunktion

Ab Supply Chain Management Version 10.0.21 ist diese Funktion standardmäßig aktiviert. Administratoren können die Seite [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu überprüfen und sie bei Bedarf zu aktivieren oder zu deaktivieren. Hier wird die Funktion als aufgeführt:

- **Modul:** *Produktinformationsverwaltung*
- **Funktionsname:** *Funktion zur Verwaltung des Herkunftslandes*

## <a name="configure-source-and-destination-countries"></a>Quell- und Zielländer konfigurieren

Bevor Sie ein Zertifikat für ein Produkt ausstellen, müssen Sie das Produkt mit seinem Zielland und seinem Herkunftsland verknüpfen.

1. Gehen Sie zu **Produktinformationsverwaltung \> Setup \> Produktkonformität \> Herkunftsland \> Regeln für das Herkunftsland**.
2. Wählen Sie ein vorhandenes Länder-Setup zum Bearbeiten aus oder wählen Sie **Neu** im Aktivitätsbereich aus, um ein neues Länder-Setup zu erstellen.
3. Legen Sie die folgenden Werte für das ausgewählte oder neue Land fest.

    | Feld | Beschreibung |
    |---|---|
    | Artikelnummer | Wählen Sie die Artikelnummer des Produkts aus. |
    | Zielland | Wählen Sie das Land aus, in das Sie das Produkt liefern. |
    | Ursprungsland | Wählen Sie das Land aus, aus dem Sie das Produkt senden. |

Mit diesem Setup können Sie einen Stücklistenbericht (BOM-Bericht) erstellen, in dem Sie das Herkunftsland für jedes Teil angeben können, für das Quell- und Zielländer angegeben sind. Dieser Bericht hilft Ihnen dabei, ein ganzheitliches Bild davon zu erhalten, woher Ihre Teile kommen und wohin sie gehen.

## <a name="keep-track-of-vendor-certificates"></a>Lieferantenzertifikate nachverfolgen

Sie können die Seite **Lieferantenzertifikate des Herkunftslandes** verwenden, um Zertifikate nachzuverfolgen, die Sie an Lieferanten ausstellen.

Sie müssen entscheiden, welche Zertifikatdokumente Sie ausstellen und wie Sie sie den Kunden melden. Mit dieser Funktion können Sie Ihre Zertifikate besser nachverfolgen. Außerdem können Sie damit auswählen, ob die relevanten Zertifikatsnummern auf Rechnungen, Lieferscheinen und/oder Auftragsbestätigungen erscheinen.

Gehen Sie zum Einrichten Ihrer Zertifikatsinformationen folgendermaßen vor.

1. Gehen Sie zu **Produktinformationsverwaltung \> Setup \> Produktkonformität \> Herkunftsland \> Kreditorenzertifikate des Herkunftslands**.
2. Wählen Sie ein vorhandenes Zertifikat-Setup zum Bearbeiten aus oder wählen Sie **Neu** im Aktivitätsbereich aus, um ein neues Zertifikat-Setup zu erstellen.
3. Legen Sie die folgenden Einstellungen für das ausgewählte oder neue Zertifikat fest.

    | Feld | Beschreibung |
    |---|---|
    | Kreditorenkonto | Wählen Sie den Lieferanten aus, an den Sie das Zertifikat ausgestellt haben. |
    | Artikelnummer | Wählen Sie den Artikel aus, für den Sie das Zertifikat ausgestellt haben. |
    | Land/Region | Das Zielland oder die Zielregion, in der Sie dieses Zertifikat verwenden müssen. |
    | Zertifikatnummer | Geben Sie die Kennnummer des von Ihnen ausgestellten Zertifikats ein. |
    | In Kraft | Wählen Sie das erste Datum aus, an dem das aktuelle Zertifikat gültig ist.|
    | Ablaufdatum | Wählen Sie das letzte Datum aus, an dem das aktuelle Zertifikat gültig ist. |
    | Auf Rechnung drucken | Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Rechnungen zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind. |
    | Auf Lieferscheinen drucken | Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Lieferscheine zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind. |
    | Auf Auftrag drucken | Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Aufträge zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind. |

## <a name="include-the-country-of-origin-on-bom-reports"></a>Nehmen Sie das Herkunftsland in Stücklistenberichte auf

Wenn Sie einen Stücklistenbericht erstellen, können Sie das Herkunftsland für jeden Teil einbeziehen, für den Sie Quell- und Zielländer auf der Seite **Regeln für das Herkunftsland** angegeben haben.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie ein Produkt aus oder erstellen Sie es, um seine Seite **Freigegebene Produktdetails** zu öffnen.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Techniker** in der Gruppe **Stückliste** die Option **Designer** aus.
1. Wählen Sie auf der Seite, die angezeigt wird, im Aktivitätsbereich die Option **Stückliste \> Drucken** aus.
1. Legen Sie im Dialogfeld **Stücklistenpositionen** das Feld **Zielland** auf das Zielland fest, das Sie in Ihrem Bericht anzeigen möchten.
1. Wählen Sie **OK**.

Ein Bericht mit Informationen zum Herkunftsland jedes Teils wird generiert und angezeigt. Hier ist ein Beispiel des Berichts.

![Herkunftslandbericht.](media/country-of-origin-report.png "Herkunftslandbericht")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]