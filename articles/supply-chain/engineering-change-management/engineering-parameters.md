---
title: Parameter für die Verwaltung für technische Änderungen
description: In diesem Thema wird erklärt, wie Sie die Funktionen der Verwaltung für technische Änderungen für Microsoft Dynamics 365 Supply Chain Management konfigurieren.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 34c2cd1bb7bfaac50f8816e7eecabf754bc714c3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832225"
---
# <a name="engineering-change-management-parameters"></a>Parameter für die Verwaltung für technische Änderungen

[!include [banner](../includes/banner.md)]

Die Seite **Parameter für die Verwaltung technischer Änderungen** enthält Einrichtungsparameter, die das Standardverhalten ändern, das sich auf die Struktur des Freigabeprodukts und die Prozesse der Verwaltung für technische Änderungen bezieht.

## <a name="open-the-engineering-change-management-parameters-page"></a>Öffnen Sie die Seite Parameter für technische Änderungsverwaltung

Um die Seite **Parameter für die Verwaltung für technische Änderungen** zu öffnen, gehen Sie zu **Verwaltung für technische Änderungen \> Einrichten \> Parameter für die Verwaltung für technische Änderungen**. Sie können dann die Felder wie in den übrigen Abschnitten dieses Themas beschrieben festlegen.

## <a name="release-control-tab"></a>Registerkarte Freigabekontrolle

Die folgende Tabelle beschreibt die Felder, die auf der Registerkarte **Freigabesteuerung** der Seite **Parameter für technische Änderungen** zur Verfügung stehen. Diese Felder beeinflussen den Prozess der Freigabe der Produktstruktur.

| Feld | Beschreibung |
|---|---|
| Artikelnummernregel | Wählen Sie aus, wie die Elementnummer definiert werden soll, wenn das Produkt für eine juristische Entität freigegeben wird. Wählen Sie *Engineering-Produktnummer*, wenn die Produktnummer in der empfangenden juristischen Entität mit der Produktnummer in der Engineering-Firma übereinstimmen soll. Wählen Sie *Lokale Element-Nummernfolge*, wenn das Produkt die nächste Nummer in der Nummernfolge für Produktnummern in der empfangenden juristischen Entität nehmen soll. |
| Stücklistennamensregel | Wählen Sie aus, wie der Name der Stückliste definiert wird, wenn das Produkt in einer juristischen Entität empfangen (freigegeben) wird. Wählen Sie entweder *Eingangsname* oder *Empfangende Elementnummer*. |
| Arbeitsplannamensregel | Wählen Sie, wie der Arbeitsplan definiert werden soll, wenn der Arbeitsplan eines Produkts in einer juristischen Entität empfangen (freigegeben) wird. Wählen Sie entweder *Eingangsname* oder *Empfangende Elementnummer*. |
| Stücklistenprüfung durchführen | Wählen Sie, ob eine Stückliste geprüft werden soll, wenn das Produkt in einer juristischen Entität empfangen (freigegeben) wird. |
| Freigabeverhalten der inaktiven Stückliste | Wählen Sie, ob ein Produkt freigegeben werden kann, wenn es eine inaktive Stückliste hat. Wählen Sie *Akzeptieren*, *Nur Warnung*, oder *Nicht erlaubt*. |
| Freigabeverhalten des inaktiven Arbeitsplans | Wählen Sie, ob ein Produkt freigegeben werden kann, wenn es einen inaktiven Arbeitsplan hat. Wählen Sie *Akzeptieren*, *Nur Warnung*, oder *Nicht erlaubt*.|
| Produktakzeptanz | Wählen Sie, ob ein zusätzlicher Schritt zur Annahme erforderlich ist, bevor das Produkt in der juristischen Entität freigegeben werden kann. Wählen Sie *Manuell*, um den Abnahmeschritt hinzuzufügen. In diesem Fall wird die Seite **Produktfreigaben öffnen** die Produkte anzeigen. Wählen Sie *Automatisch*, um das Produkt direkt auf der Seite **Freigegebene Produkte** in der juristischen Entität anzuzeigen, unmittelbar nachdem das Produkt zusammen mit seiner Freigabeproduktstruktur freigegeben wurde. |

## <a name="engineering-change-management-tab"></a>Registerkarte Verwaltung für technische Änderungen

Die folgende Tabelle beschreibt die Felder, die auf der Registerkarte **Verwaltung für technische Änderungen** der Seite **Parameter für die Änderungsverwaltung** verfügbar sind. Diese Einstellungen wirken sich auf den Prozess der Verwaltung für technische Änderungen aus.

| Feld | Beschreibung |
|---|---|
| Kategorie | Die Standardkategorie, die verwendet wird, wenn eine Änderungsanforderung erstellt wird. |
| Priorität | Die Standardpriorität, die verwendet wird, wenn ein Änderungsantrag erstellt wird. |
| Schweregradregel | Wählen Sie aus, wie der Schweregrad einer Änderungsanforderung festgelegt werden soll. Wählen Sie *Manuell*, wenn der Benutzer einen Wert in das Feld **Schweregrad** eingeben soll. Wählen Sie *Berechnen*, wenn das System den Wert des Felds **Schweregrad** berechnen soll, wenn Sie **Schweregrad berechnen** im Aktivitätsbereich des Änderungsauftrags wählen. In diesem Fall verwendet das System die Schweregradregeln, die auf der Seite **Schweregrad-Regelsatz** festgelegt sind. Wählen Sie *Automatisch berechnen*, damit der Wert des Feldes **Schweregrad** automatisch berechnet und entsprechend der festgelegten Schweregrad-Regeln ausgefüllt wird. |
| Betroffene Produkte erneut freigeben | Dieses Feld ist anwendbar, wenn Sie Produkte über einen Änderungsauftrag neu freigeben. Im Dialogfeld **Wiederfreigaben** können Sie wählen, ob alle Produkte oder nur die betroffenen Produkte vorgeschlagen werden sollen. |
| Freizugebende Stücklistenebenen | Die Tiefe der Stücklistenebene, die freigegeben werden soll. Wenn die Stückliste mehr Ebenen hat (d.h. tiefer ist) als der hier angegebene Wert, werden nur die Ebenen bis zum angegebenen Wert freigegeben. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]