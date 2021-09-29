---
title: Die genaue Preis- und Rabattberechnung für eine verbesserte Leistung verzögern
description: In diesem Thema wird die verzögerte Preisberechnungsfunktion beschrieben, die in Microsoft Dynamics 365 Commerce Point of Sale (POS) und Callcenter verfügbar ist.
author: boycezhu
ms.date: 09/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 8c4264c3a4c71e6aab0e1ef8d7d8cfffad065a46
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488362"
---
# <a name="delay-exact-price-and-discount-calculation-for-improved-performance"></a>Die genaue Preis- und Rabattberechnung für eine verbesserte Leistung verzögern

[!include [banner](includes/banner.md)]

In diesem Thema wird die verzögerte Preisberechnungsfunktion beschrieben, die in Microsoft Dynamics 365 Commerce Point of Sale (POS) und Callcenter verfügbar ist.

Dynamics 365 Commerce unterstützt die Erstellung von Mehrzeilenrabatten, die angewendet werden, wenn mehrere Verkaufszeilen eines Kundenauftrags oder Verkaufsangebots kombiniert werden. Diese Rabatte umfassen Mix-and-Match-, Schwellenwert- und Mengenrabatte.

Immer wenn einer Bestellung eine neue Position hinzugefügt wird, wertet das Commerce-Preismodell den gesamten Warenkorb aus, um festzustellen, ob einer dieser Rabatte für mehrere Positionen angewendet werden kann. Aufgrund dieser Neuberechnung kann das Hinzufügen neuer Positionen die Leistung beeinträchtigen, wenn ein Kundenauftrag größer wird.

Business-to-Business-(B2B-)Unternehmen und einige Business-to-Consumer-(B2C-)Unternehmen haben jedoch oft große Auftragsgrößen. Daher kann es zeitaufwändig sein, zu warten, bis das Preismodul eine Neuberechnung durchführt, nachdem jeder Artikel in den Warenkorb gelegt wurde. Darüber hinaus ist es bei großen Bestellungen normalerweise nicht sehr wichtig, dass der genaue Preis und der Rabatt jedes Mal angezeigt werden, wenn ein Artikel in den Warenkorb gelegt wird. Es ist wichtiger, dass Benutzer Artikel schnell hinzufügen können. Die Funktion, die genaue Preis- und Rabattberechnung zu verzögern, bis ein Benutzer sie anfordert oder eine Bestellung abgeschlossen ist, kann die Leistung erheblich verbessern. Es kann auch die Zeit verkürzen, die erforderlich ist, um eine Bestellung abzuschließen.

Die Funktion zur Verzögerung der genauen Preis- und Rabattberechnung ist seit langem im POS verfügbar. Ab der Commerce-Version 10.0.22 ist es auch für Callcenter verfügbar.

## <a name="enable-delayed-price-and-discount-calculation-for-pos"></a>Die verzögerte Preis- und Rabattberechnung für POS aktivieren

Gehen Sie wie folgt vor, um die verzögerte Preis- und Rabattrechnung für POS zu aktivieren.

1. Navigieren Sie in der Commerce-Zentrale zum Funktionsprofil, das dem physischen Geschäft zugeordnet ist.
1. Aktivieren Sie im Inforegister **Betrag** die Konfiguration **Mehrere Artikelrabatte manuell berechnen**.
1. Öffnen Sie den Bildschirm-Layoutdesigner für die Register, in denen die verzögerte Berechnung aktiviert werden soll.
1. Fügen Sie eine Schaltfläche für den Vorgang **Summe berechnen** im gewünschten Schaltflächenraster hinzu.
1. Führen Sie die Aufträge **1070** und **1090** aus.

Wenn Artikel zu einer Transaktion hinzugefügt werden, werden mehrzeilige Rabatte nicht berechnet, es sei denn, der Kassierer wählt die Schaltfläche **Summe berechnen** aus. Nach Auswahl von **Summe berechnen** für eine Transaktion werden immer mehrzeilige Rabatte dafür berechnet. Der Kassierer muss die Schaltfläche nicht erneut auswählen, auch wenn weitere Artikel in den Warenkorb gelegt werden. Das System erlaubt dem Kassierer nicht, die Zahlung zu erfassen, bis **Summe berechnen** ausgewählt ist.

## <a name="enable-delayed-price-and-discount-calculation-for-call-center"></a>Die verzögerte Preis- und Rabattberechnung für Callcenter aktivieren

Gehen Sie wie folgt vor, um die verzögerte Preis- und Rabattrechnung für Callcenter zu aktivieren.

1. Navigieren Sie in Commerce-Zentralen zu **Arbeitsplätze \> Funktionsverwaltung**.
1. Aktivieren Sie die Funktion **Unbeabsichtigte Preisberechnungen für Commerce-Aufträge verhindern**. Diese Funktion ist eine Voraussetzung für die verzögerte Preis- und Rabattberechnung.

    > [!NOTE]
    > Für neue Bereitstellungen ist die Funktion **Unbeabsichtigte Preisberechnungen für Commerce-Aufträge verhindern** standardmäßig aktiviert.

1. Navigieren Sie zu **Commerce-Parameter \> Preise und Rabatte**.
1. Aktivieren Sie im Abschnitt **Sonstiges** die Konfiguration **Mehrzeilige Preise und Rabatte manuell berechnen**.

Wenn jetzt ein Kundenauftrag oder ein Angebot im Call Center erstellt oder bearbeitet wird, verzögert sich die genaue Preis- und Rabattberechnung dafür. Das Preismodul berücksichtigt nur die hinzugefügte oder bearbeitete Verkaufsposition und ignoriert alle anderen Verkaufspositionen. Der Nettobetrag für einen Artikel beinhaltet die Preisberechnung und einfache Rabatte (Rabattprozentsatz oder Rabatt auf einen einzelnen Artikel). Mix-and-Match-, Schwellenwert- und Mengenrabatte werden jedoch nicht angewendet. Callcenter-Benutzer, die den genauen Preis einschließlich aller Rabatte anzeigen möchten, können eine von drei Schaltflächen auswählen: **Neu berechnen**, **Summen** oder **Vollständig**.

> [!NOTE]
> Bei Callcenter-Aufträgen zeigt das System eine Warnmeldung an, um den Benutzer daran zu erinnern, dass er die Schaltfläche **Neu berechnen**, **Summen** oder **Vollständig** auswählen muss, um die genaue Preis- und Rabattberechnung durchzuführen. Für Bestellungen, bei denen die Schaltfläche **Vollständig** verfügbar ist, gibt es für den Callcenter-Benutzer keine Möglichkeit, die genaue Preis- und Rabattberechnung auszulassen, da er **Vollständig** auswählen muss, um die Auftragserfassung abzuschließen. Für Bestellungen, bei denen die Schaltfläche **Vollständig** nicht verfügbar ist, gibt es keine Aktion, die den Abschluss der Auftragserfassung anzeigt. Daher ist der Callcenter-Benutzer dafür verantwortlich, entweder **Neu berechnen** oder **Summen** auszuwählen, bevor er die Auftragserfassung abschließt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
