---
title: Provisionen in POS mit Verkaufsgruppen nachverfolgen
description: "Es ist übliche Praxis Umsätze nach Verkäufer für einen Debitor nachzuverfolgen, um zu Unterstützen, Up-Selling und Cross-Selling zu ermöglichen und die Buchung zu verarbeiten."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 92963dff5703376ea44601434fc874728c92f813
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="track-commissions-in-pos-using-sales-groups"></a>Provisionen in POS mit Verkaufsgruppen nachverfolgen

[!INCLUDE [banner](includes/banner.md)]

Es ist übliche Praxis Umsätze nach Verkäufer für einen Debitor nachzuverfolgen, um zu Unterstützen, Up-Selling und Cross-Selling zu ermöglichen und die Buchung zu verarbeiten.

Umsatz nach Verkäufer zu verfolgen ist eine Kennzahl der Mitarbeiterfähigkeiten für Verkauf, Umsatz pro Kassierer wird in Geschwindigkeit und Effizienz gemessen. Der Verkauf, die vom Verkäufer erfasst werden, sind außerdem häufig verwendet für Provisionen oder andere Anreize zu berechnen.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Eine Arbeitskraft so konfigurieren, dass sie ein Verkäufer in POS ist
Ist eine Arbeitskraft einer Verkaufsgruppe hinzugefügt wird, ist dieser für Provision freigegeben und kann als Verkäufer im System identifiziert werden. Eine Arbeitskraft, die keiner Verkaufsgruppe ist, ist nicht berechtigt für Provision und wird nicht als Verkaufsstelle (POS)- Verkäufer in der Anwendung aufgeführt werden. In POS wird die Liste von Verkäufern aus allen Verkaufsgruppen berechnet, die mindestens eine Arbeitskraft enthalten, die dem Shop zugewiesen ist. Die Liste besteht in POS aus einer Kombination von Verkaufgruppenkennung und Name (ID: Name). Eine Standardverkaufsgruppe kann Arbeitskräften zugewiesen werden, um Szenarien zu ermöglichen, in denen der Einzelhändler beschließt, automatisch POS-Positionen für Verkäufer festzulegen. Benutzer können von einer Verkaufsgruppe auswählen, für die die Arbeitskraft gehört.

## <a name="functionality-profile-settings"></a>Funktionsprofileinstellungen
Es gibt mehrere Funktionsprofileinstellungen für eine Filiale, die den Fluss und Prozess in POS für den Verkäufer bestimmen.


|                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              <strong>Profil</strong>              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        <strong>Beschreibung</strong>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <strong>Kassierer als Standard, wenn verfügbar</strong> |                                                                                                                                                                                                                                                                                                                                                                                                     Wenn diese Option aktiviert ist, gibt POS Buchungspositionen automatisch mit der aktuellen Standardverkaufsgruppe des Kassierers auf. Wenn ein Kassierer eine Standardverkaufsgruppe nicht angegeben wurde, wird der Wert nicht festgelegt. Ein Benutzer kann die Verkaufsgruppe jedoch manuell festlegen, indem Sie eine POS-Schaltflächenrasterschaltfläche verwenden.                                                                                                                                                                                                                                                                                                                                                                                                      |
|  <strong>Nachfrage nach Verkäufer</strong>  | Diese Option hat drei mögliche Werte: <strong>Nein ** – Wenn diese Option ausgewählt ist, wird der Benutzer nicht aufgefordert, eine Verkaufsgruppe auszuwählen. Der Wert kann dennoch festgelegt werden, indem eine standardmäßige Verkaufsgruppe eines Kassierers verwendet wird, oder manuell, indem eine POS-Schaltflächen-Rasterschaltfläche verwendet wird. **Beginn der Buchung</strong> – Wenn diese Option ausgewählt ist und entweder die Option <strong>Standard zu Kassierer</strong> nicht aktiviert ist oder der aktuelle Kassierer keine Standardverkaufsgruppe hat, wird der Benutzer dazu aufgefordert, eine Verkaufsgruppe zu Beginn jeder Buchung auszuwählen. Das Auswählen einer Verkaufsgruppe aus dieser Aufforderung erscheint standardmäßig alle nachfolgenden Verkaufsgruppe der ausgewählten Positionen. Ein Benutzer kann die Verkaufsgruppe jedoch manuell festlegen, indem Sie eine POS-Schaltflächenrasterschaltfläche verwenden. <strong>Für jede Position</strong> - Mit dieser Option und ohne Option <strong>Standardwert zum Kassierer</strong> oder der wenn der aktuelle Kassierer hat keine Standardverkaufsgruppe, wird der Benutzer aufgefordert, eine Verkaufsgruppe zu Beginn jeder Buchung auszuwählen. Ein Benutzer kann die Verkaufsgruppe jedoch manuell festlegen, indem Sie eine POS-Schaltflächenrasterschaltfläche verwenden. |
|              <strong>Erforderlich</strong>              |                                                                                                                                                                                                                                                                                                                         Diese Option ist nur relevant, wenn POS konfiguriert wird, um einem Verkäufer zu erforderlich. Wenn der Schlüssel aktiviert ist, wird der Benutzer aufgefordert, eine Verkaufsgruppe auszuwählen, bevor Sie fortfahren möchten. Andernfalls wird der Benutzer aufgefordert, kann jedoch abbrechen und fortfahren, ohne eine Auswahl treffen. Nachdem die Position hinzugefügt ist, wäre ein Benutzer mit ausreichenden Berechtigungen in der Lage die Verkaufsgruppe an der Position noch entfernen. "Verkäufer erzwigen" wird nicht in dieser Situation durchgesetzt.                                                                                                                                                                                                                                                                                                                          |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Anzeigen der Verkäuferinformationen auf dem POS-Buchungs-Bildschirm
Das POS-Buchungs-Bildschirmlayout und die Inhalte sind mit dem Bildschirmlayoutdesigners konfigrierbar und Bildschirmlayouts können zu Shops, Kassen oder Arbeitskräfte zugeordnet werden. Das **Verkäufer** Feld kann der Registerkarte Position des Zugangsbereichs hinzugefügt werden.  Hier werden die Kennung der angegebenen Verkaufsgruppe für jede Position im Feld Buchungsbildschirm angezeigt.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Hinzufügen von Verkäuferarbeitsgängen zu POS-Schaltflächenrastern
POS ermöglicht Benutzern Schaltflächenraster zu konfigurieren, die in den Bildschirmlayouts einbezogen werden, um Zugriff auf POS-Arbeitsgängen bereitzustellen. Die folgenden POS-Vorgängen können zu den Schaltflächenrasterschaltflächen zugewiesen werden,.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vorgang**                             | **Beschreibung**                                                                                                                                                                                                                                                                              |
| Verkäufer für Position festlegen          | Dieser POS-Arbeitsgang zeigt eine Liste aus freigegebenen Verkaufsgruppen (ID : Name) für den Shop. Das Auswählen einer Verkaufsgruppe aus dieser Liste legt den Wert für die aktuelle Buchung fest.                                                                                                            |
| Verkäufer für Position löschen        | Dieser POS-Arbeitsgang entfernt den aktuellen Verkaufsgruppenwert der aktuellen Buchung.                                                                                                                                                                                                  |
| Verkäufer für Buchung festlegen   | Dieser POS-Arbeitsgang zeigt eine Liste aus freigegebenen Verkaufsgruppen (ID : Name) für den Shop. Das Auswählen einer Verkaufsgruppe aus dieser Liste legt den Standardwert für die aktuelle Buchung fest. Alle vorhandenen Positionen ohne zugewiesene Verkaufsgruppe werden sowie alle nachfolgend hinzugefügten Positionen festgelegt. |
| Verkäufer für Buchung löschen | Dieser POS-Arbeitsgang entfernt den aktuellen Standardverkaufsgruppenwert der aktuellen Buchung. Wirkt sich auf keine Positionen aus, die in der Buchung bereits vorhanden sein.                                                                                                                             |

## <a name="calculating-commissions"></a>Berechnen von Provisionen
Provision werden für die Arbeitskräfte in den angegebenen Verkaufsgruppen zum Zeitpunkt der Buchung oder der Auftragsbuchung berechnet. Der Provisionsbetrag wird basierend auf den Provisionsfreigabe der Arbeitskraft bestimmt, die im Formular und Verkaufsgruppe in den zugehörigen Provisionsberechnungseinstellungen für den Debitor und/oder die Produkte für die Buchung definiert.




