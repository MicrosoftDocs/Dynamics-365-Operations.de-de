---
title: Lagerplatzbeschränkungen
description: Dieses Thema beschreibt die Funktionalität für Lagerplatz-Bestandsgrenzen.
author: perlynne
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 239b9fa8d8e34a92d453d3387881cff7b0a11f28a3c3b1e19891ea3bd78c3d7c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714161"
---
# <a name="location-stocking-limits"></a>Lagerplatzbeschränkungen

[!include [banner](../includes/banner.md)]

Sie können die Seite **Lagerort-Bestandsgrenzen** (**Lagerortverwaltung \> Einrichten \> Lagerort \> Lagerort-Bestandsgrenzen**) verwenden, um die Ladekapazität an Lagerorten zu steuern, ohne die erweiterten Prozesse für volumetrische Berechnungen von physischen Produkten verwenden zu müssen.

Der Zweck von Lagerplatz-Bestandsgrenzen ist es, die maximale Menge zu ermitteln, die ein Lagerplatz enthalten kann. Sie können die Funktion auf einer von drei Ebenen festlegen, von denen jede ihre eigene Registerkarte auf der Seite **Lagerplatz-Bestandsgrenzen** hat:

- Produkte
- Produktvarianten
- Containertypen

Für jede Ebene können Sie unterschiedliche Feldwerte definieren. Das System bewertet dann die Kapazität eines bestimmten Lagerplatzes, basierend auf den Werten **Menge** und **Einheit** für jede Zeile. Es wählt zuerst den detailliertesten passenden Datensatz aus. Zum Beispiel wird eine Zeile, die einen Wert im Feld **Standortprofil-ID** hat, vor einer Zeile ausgewertet, die nur einen Wert im Feld **Lagerort** hat. Die verbleibende Kapazität wird ebenfalls ausgewertet, basierend auf dem **Menge**-Wert für den verwendeten Lagerplatz-Bestandsgrenzendatensatz.

Im Abschnitt **Produkte** der Seite können Sie die folgenden Feldwerte für die Suche nach Lagerplatz-Bestandsgrenzen definieren:

- Lagerort
- Lagerplatz-Profilkennung
- Ziel
- Verpackungsgrößenkategorie-Kennung
- Artikelnummer
- Einheit

> [!NOTE]
> Sie müssen nicht für jeden Lagerplatz-Bestandslimit-Datensatz einen **Einheit**-Wert definieren. Die Berechnungen der Lagerplatz-Kapazität basieren auf den Einheiten des Bestands. Wenn für einen verwendeten Wert keine Einheitenumrechnung definiert ist, wird der Lagerplatz-Limit-Datensatz übersprungen, als ob ein anderer **Element-Nummer**-Wert für ihn definiert wäre.

## <a name="example--purchase-order-receiving"></a>Beispiel - Eingang einer Einkaufsbestellung

Dieses Beispiel basiert auf einem sauberen *USMF*-Demo-Datensatz, in dem die folgenden Werte auf der Registerkarte **Produktvarianten** der Seite **Lagerplatz-Bestandsgrenzen** festgelegt sind.

| Lagerort | Lagerplatz-Profilkennung | Artikelnummer | Größe | Leistung | Einheit |
|-----------|---------------------|-------------|------|----------|------|
| 24        | FLOOR               | D0013       | Mo    | 300      | St.   |
| 24        | FLOOR               | D0013       | L    | 240      | St.   |
| 24        | FLOOR               | D0013       | Sa    | 360      | St.   |

Für die Produkte sind verschiedene Produktvarianten in Maßeinheiten festgelegt. Diese Varianten sind auf die Lagerplatz-Bestandsgrenzen für drei Paletten (PL) abgestimmt:

- **Größe M:** 1 PL = 100 Stück (Ea)
- **Größe L:** 1 PL = 80 Ea
- **Größe S:** 1 PL = 120 Ea

Daher kann jeder Lagerplatz, bei dem der Wert **Lageprofil-ID** auf *FLOOR* festgelegt ist, *3* *PL* der Elementnummer *D0013* tragen.

### <a name="prepare-for-the-example"></a>Vorbereiten des Beispiels

In diesem Beispiel werden Sie einen Flow für den Empfang einer Einkaufsbestellung für zwei Zeilen ausführen. Zuvor müssen Sie jedoch die Demo-Daten wie folgt aktualisieren, um sicherzustellen, dass die Lagerplätze gemischte Positionen zulassen, nur die leeren Lagerplätze *FL-002* bis *FL-004* verwendet werden und keine offene Eingangsarbeit vorhanden ist.

1. Für den Lagerplatz *FL-001* ändern Sie den Wert des Feldes **Lagerplatzprofil** von *FLOOR* auf *FLOOR-05*.
1. Legen Sie für das Standortprofil *FLOOR* die Option **Gemischte Elemente zulassen** auf *Ja* fest.
1. Erstellen Sie eine Einkaufsbestellung, die die folgenden zwei Zeilen enthält.

    | Lagerort | Artikelnummer | Größe | Leistung | Einheit |
    |-----------|-------------|------|----------|------|
    | 24        | D0013       | Sa    | 4        | PL   |
    | 24        | D0013       | L    | 4        | PL   |

### <a name="process-the-example"></a>Verarbeiten Sie das Beispiel

Sie erhalten zunächst eine Menge von *4* der Einheit *PL* in der Größe *S* und überprüfen die eingelagerten Zeilenplätze für die erstellte Arbeit. Sie erhalten dann eine Menge von *4* der Einheit *PL* in der Größe *L* und überprüfen die Lagerplätze für die erstellte Arbeit.

1. Melden Sie sich in der Warehouse Management Mobile App an, indem Sie *24* als Benutzer-ID und *1* als Kennwort verwenden.
1. Wählen Sie **Eingang** \> **Empfang**.
1. Empfangen Sie *4* *PL* der Elementnummer *D0013* in Größe *S*.
1. Überprüfen Sie die erstellte Einlagerungsarbeit. Sie sollten das folgende Ergebnis sehen:

    - 3 PL -\> FL-002
    - 1 PL -\> FL-003

1. Erhalten Sie *4* *PL* von Element Nummer *D0013* in Größe *L*.
1. Überprüfen Sie die erstellte Einlagerungsarbeit. Sie sollten das folgende Ergebnis sehen:

    - 1 PL -\> FL-003
    - 3 PL -\> FL-004

Aus den Ergebnissen können Sie schließen, dass das System nicht die richtigen Lagerplätze zugewiesen hat. Warum hat das System sonst im letzten Schritt nur *1* *PL* der Größe *L* zum Lagerplatz *FL-003* hinzugefügt und nicht *2* *PL*? Das heißt, warum gibt es nicht eine Summe von *3* *PL* für die Einlagerung an diesen Lagerplatz?

Um diesen offensichtlichen Fehler zu erklären, müssen Sie die Auswahlkriterien für die Lagerplatz-Einlagerungsgrenzen verstehen. Das System wählt den detailliertesten übereinstimmenden Datensatz aus. In diesem Beispiel ist der detaillierteste übereinstimmende Datensatz die Zeile, bei der der **Größe** Wert *L*, der **Menge** Wert *240* und der **Einheit** Wert *Ea* ist. Da Sie bereits offene Arbeit aus dem vorherigen Empfang einer Menge von *120* *Ea* der Größe *S* haben, wird die verbleibende Kapazität berechnet als *240* - *120* = *120* *Ea*. Daher kann die Restkapazität nur *1* *PL* von *80* *Ea* sein.

> [!NOTE]
> Sie können Lagerplatz-Bestandsgrenzen nicht verwenden, um z. B. die Wiederbeschaffung von Elementen zu steuern, die am selben Lagerplatz unterschiedliche Mengen haben. Verwenden Sie in diesem Fall eine *Wiederbeschaffung-Vorlage*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]