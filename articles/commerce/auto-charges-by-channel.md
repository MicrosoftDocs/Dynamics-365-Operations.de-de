---
title: Automatische Belastungen nach Kanal aktivieren und konfigurieren
description: In diesem Thema wird erläutert, wie Sie automatische Gebühren nach Kanal in Microsoft Dynamics 365 Commerce aktivieren und konfigurieren.
author: gvrmohanreddy
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: c38717ca9c57913ea22f2dd7712b49f39d2e556e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349697"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a>Automatische Belastungen nach Kanal aktivieren und konfigurieren

In diesem Thema wird erläutert, wie Sie automatische Gebühren nach Kanal in Microsoft Dynamics 365 Commerce aktivieren und auch konfigurieren.

## <a name="overview"></a>Übersicht

Möglicherweise gibt es Szenarien, in denen Recyclinggebühren oder andere Gebühren auf eine Gruppe von Produkten erhoben werden müssen, die in allen oder einigen Geschäften in einem bestimmten Bundesstaat (z. B. Kalifornien) verkauft werden. Die Funktion **Aktivieren Sie die automatische Filterladung nach Kanal** in Commerce lässt Sie automatische Gebühren nach Kanal festlegen (z. B. einen bestimmten stationären Kanal). Diese Funktion wird in Dynamics 365 Commerce Version 10.0.10 und höher verfügbar.

Um automatische Gebühren nach Kanal zu aktivieren und zu konfigurieren, müssen Sie die folgenden Aufgaben ausführen:

- Aktivieren Sie **Aktivieren Sie die automatische Filterladung nach Kanal**.
- Konfigurieren Sie die Organisationshierarchiezwecke.
- Definieren Sie automatische Gebühren nach Kanal.

> [!NOTE]
> Die Funktion **Aktivieren Sie die automatische Filterladung nach Kanal** funktioniert nur, wenn die erweiterte Funktion zum automatischen Laden ebenfalls aktiviert ist. Informationen zum Aktivieren der erweiterten Funktion für automatische Gebühren finden Sie unter [Erweiterte automatische Omni-Channel-Gebühren](omni-auto-charges.md).

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a>Starten Sie Aktivieren Sie die automatische Filterladung nach Kanal

Führen Sie die folgenden Schritte aus, um automatische Gebühren nach Kanal in Commerce zu aktivieren.

1. Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Datenverwaltung**.
1. Auf der Registerkarte **Nicht aktiviert** in der Liste **Funktionsname** finden und wählen Sei **Aktivieren Sie die automatische Filterladung nach Kanal**.
1. Wählen Sie in der unteren rechten Ecke **Jetzt aktivieren**. Nachdem die Funktion aktiviert wurde, wird sie in der Liste auf der Registerkarte **Alle** angezeigt.
1. Gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**.
1. Suchen und wählen Sie im linken Bereich den Auftrag **1110** (**Globale Konfiguration**).
1. Wählen Sie im Aktionsbereich **jetzt ausführen**, um die Konfigurationsänderungen zu verbreiten.

> [!WARNING]
> Wenn Sie die Funktion **Aktivieren Sie die automatische Filterladung nach Kanal** ausschalten, nachdem Sie sie bereits verwendet haben, wird das Feld unter **Einzelhandelskanalbeziehung** unter **Automatische Aufladung** nicht mehr angezeigt und Sie verlieren alle vorhandenen Konfigurationen. Wenn die Entfernung der Konfiguration **Einzelhandelskanalbeziehung** die Regeln für automatische Gebühren dupliziert, schlägt der Versuch zur Deaktivierung fehl. Überprüfen Sie vor dem Deaktivieren der Funktion unbedingt alle Regeln für automatische Gebühren und nehmen Sie die erforderlichen Änderungen vor.

## <a name="configure-the-organization-hierarchy-purpose"></a>Konfigurieren Sie die Organisationshierarchiezwecke

Ein neuer Zweck der Organisationshierarchie, der **Automatische Gebühr für den Einzelhandel** benannt wird, wurde erstellt, um die Hierarchie für automatische Gebühren nach Kanal zu verwalten.

Führen Sie die folgenden Schritte aus, um einem Organisationshierarchiezweck in Commerce eine Standardhierarchie zuzuweisen.
        
1. Wechseln Sie zu **Organisationsverwaltung \> Organisationen \> Organisationshierarchiezwecke**.
1. Wählen Sie im linken Bereich **Automatische Gebühr für den Einzelhandel** aus.
1. Unter **Zugeordnete Hierarchien** wählen Sie **Hinzufügen**.
1. In dem Dialogfeld **Organisationshierarchien** wählen Sie im Dialogfeld eine Organisationshierarchie aus (z. B. **Einzelhandelsgeschäfte nach Regionen**) und wählen Sie dann **OK**.
1. Unter **Zugeordnete Hierarchien** wählen Sie **Als Standard festlegen**.
1. Gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**.
1. Suchen und wählen Sie im linken Bereich den Auftrag **1040** (**Produkte**).
1. Wählen Sie im Aktivitätsbereich **Jetzt ausführen** aus.
1. Wiederholen Sie die beiden vorherigen Schritte, um Aufträge **1070** (**Kanalkonfiguration**) und **1110** (**Globale Konfiguration**) auszuführen.

![Konfiguration des Hierarchiezwecks der automatischen Organisation für den Einzelhandel.](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a>Definieren Sie automatische Gebühren nach Kanal

Nachdem Sie die Funktion **Aktivieren Sie die automatische Filterladung nach Kanal** aktiviert und den Organisationshierarchiezweck **Automatische Belastung für den Einzelhandel** konfiguriert haben, können automatische Gebühren nach Kanal entweder auf der Ebene der Auftragskopfzeilen oder auf der Ebene der Auftragspositionen definiert werden.

Führen Sie die folgenden Schritte aus, um automatische Gebühren nach Kanal in Commerce zu definieren.

1. Wechseln Sie zu **Debitoren \> Belastungen einrichten \> Auto-Belastungen**.
1. Im linken Bereich im Feld **Ebene** wählen Sie entweder **Kopf** oder **Linie** aus, abhängig von Ihren Geschäftsanforderungen.
1. In dem Feld **Retail Channel-Code** wählen Sie im Feld den entsprechenden Kanalcode aus (z. B. **Tabelle** oder **Gruppe**). Wenn die Standardeinstellung, **Alle** verwendet wird, werden Gebührenregeln auf alle Kanäle angewendet.

    - Wenn Sie **Gruppe** auswählen, stellen Sie sicher, dass eine Gebührengruppe für Einzelhandelskanäle unter **Einzelhandel und Handel \> Kanaleinrichtung \> Gebühren \> Gebührengruppen für Einzelhandelskanäle** erstellt wird.
    - Wenn Sie **Tabelle** auswählen, können Sie einen bestimmten Kanal auswählen (z. B. **San Francisco**) in dem Feld **Einzelhandelskanalbeziehung**.

1. Gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**.
1. Suchen und wählen Sie im linken Bereich den Auftrag **1040** (**Produkte**).
1. Wählen Sie im Aktivitätsbereich **Jetzt ausführen** aus.
1. Wiederholen Sie die beiden vorherigen Schritte, um Aufträge **1070** (**Kanalkonfiguration**) und **1110** (**Globale Konfiguration**) auszuführen.
    
![Automatische Gebühren nach Kanal definiert.](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a>Beispielszenario

Im folgenden Beispiel werden die Schritte beschrieben, die zum Konfigurieren eines Produkts erforderlich sind, damit beim Verkauf des Produkts über einen stationären Kanal in San Francisco Recyclinggebühren erhoben werden. Das Beispiel zeigt auch, wie die automatischen Gebühren in der POS-Anwendung (Commerce Point of Sale) angezeigt werden.

Die Organisation definiert einen Gebührencode, der **RECYCELN** benannt wird, wie in der folgenden Abbildung gezeigt.

![RECYCLE berechnet den Code.](media/Auto-charges-charge-code.png)

Eine automatische Belastung wird auf Positionsebene erstellt. Es weist die folgenden Konfigurationen auf:

- Das Feld **Kontocode** ist festgelegt auf **Alle** festgelegt.
- Das Feld **Artikelcode** ist auf **Tabelle** festgelegt.
- Das Feld **Artikelbeziehung** ist auf Produkt-ID **91001** festgelegt.
- Das Feld **Lieferungscode-Modus** ist auf **Alle** festgelegt.
- Das Feld **Retail Channel Code** ist auf **Tabelle** festgelegt.
- Das Feld **Retail Channel Beziehung** ist auf Geschäft **San Francisco** festgelegt.

Eine automatische Gebührenzeile wird erstellt. Es weist die folgenden Konfigurationen auf:

- Das Feld **Währung** wird mit auf **USD** festgelegt.
- Das Feld **Belstungscode** ist auf **RECYCLE** festgelegt.
- Das Feld **Kategorie** ist auf **Fest** festgelegt.
- Das Feld **Belastung** wird mit auf **$6.25** festgelegt.

![Konfiguration der Zeile automatischen Belastungsebene und automatische Belastung.](media/Auto-charges-recyclingfee-line-fee.png)

In der POS-Anwendung wird ein Auftrag im Shopkanal **San Francisco** erstellt. Die Position **Belastungen** zeigen die Recyclinggebühr von **6,25 $**.

Durch die Auswahl von **Transaktionsoptionen \> Gebühren \> Gebühren verwalten** in der POS-Anwendung können Sie den Gebührencode und die Beschreibung der Recyclinggebühr anzeigen.

![Recyclinggebühr in der POS-Anwendung.](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Erweiterte automatische Omni-Channel-Belastungen](omni-auto-charges.md)

[Kopfbelastungen auf übereinstimmende Verkaufspositionen aufteilen](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]