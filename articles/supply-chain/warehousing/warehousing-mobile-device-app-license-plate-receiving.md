---
title: Kennzeichenempfang über die Lagerhaltungs-App
description: In diesem Thema wird erläutert, wie Sie die Lagerhaltungs-App so einrichten, dass die Verwendung eines Kennzeichen-Empfangsprozesses zum Empfangen von Bestand unterstützt wird.
author: perlynne
manager: tfehr
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 82b4f40510d5bbf829508f17f1064886620a4aed
ms.sourcegitcommit: a3cd2783ae120ac6681431c010b9b126a9ca7d94
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410884"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a>Kennzeichenempfang über die Lagerhaltungs-App

In diesem Thema wird erläutert, wie Sie die Lagerhaltungs-App einrichten, so dass sie die Verwendung eines Kennzeichenempfangsprozesses zum Empfangen von Bestand unterstützt.

Mit dieser Funktion können Sie schnell den Eingang des eingehenden Bestands aufzeichnen, der sich auf eine Vorabmitteilung (ASN) bezieht. Das System erstellt automatisch einen Lieferavis, wenn Lagerverwaltungsprozesse zum Versenden eines Transportauftrags verwendet werden. Für den Bestellvorgang kann ein ASNs manuell erfasst oder mithilfe eines eingehenden ASN-Datenentitätsprozesses automatisch importiert werden.

Die ANS-Daten werden mit Ladungen und Sendungen über die *Verpackungsstrukturen* verknüpft, wo Paletten (übergeordnete Kennzeichen) Fälle enthalten können (verschachtelte Kennzeichen).

> [!NOTE]
> Um die Anzahl der Bestandtransaktionen zu verringern, wenn Verpackungsstrukturen mit verschachtelten Kennzeichen verwendet werden, zeichnet das System das physische Inventar auf dem übergeordneten Kennzeichen auf. Um die Verschiebung des physischen Bestands vom übergeordneten Kennzeichen zu den verschachtelten Kennzeichen basierend auf den Daten der Verpackungsstruktur auszulösen, muss das mobile Gerät einen Menüpunkt bereitstellen, der auf dem Arbeitserstellungsprozess *auf verschachtelte Kennzeichen packen* basiert.

## <a name="warehousing-mobile-device-app-processing"></a>Warehousing App-Verarbeitung für mobiles Geräte

Wenn ein Mitarbeiter eine eingehende Kennzeichen-ID scannt, initialisiert das System einen Kennzeichenempfangsprozess. Basierend auf diesen Informationen wird der Inhalt des Kennzeichens (Daten vom Lieferavis) physisch am Ort des eingehenden Docks registriert. Die folgenden Abläufe hängen von Ihren Geschäftsprozessanforderungen ab.

## <a name="work-policies"></a>Arbeitsrichtlinien

Wie bei (zum Beispiel) dem *Als fertig melden* Menüelementprozess für mobile Geräte, unterstützt der Prozess zum Empfang von Kennzeichen mehrere Workflows basierend auf dem definierten Setup.

### <a name="work-policies-with-work-creation"></a>Arbeitsrichtlinien mit Arbeitserstellung

Wenn Sie eingehende Elemente mithilfe einer Arbeitsrichtlinie registrieren, mit der Arbeit erstellt wird, generiert und speichert das System für jede Registrierung weggelegte Arbeitsaufzeichnungen. Wenn Sie den Arbeitsprozess *Kennzeichen erhalten und weglegen* verwenden, dann werden Registrierung und Einlagerung als ein einziger Vorgang unter Verwendung eines einzigen Menüpunkts für mobile Geräte behandelt. Wenn Sie den Prozess *Kennzeichenempfang* verwenden, dann werden die Empfangs- und Einlagerungsprozesse als zwei verschiedene Lagervorgänge mit jeweils einem eigenen Menüpunkt für mobile Geräte behandelt.

### <a name="work-policies-without-work-creation"></a>Arbeitsrichtlinien ohne Arbeitserstellung

Sie können den Kennzeichenempfangsprozess verwenden, ohne Arbeit zu erstellen. Wenn Sie Arbeitsrichtlinien definieren, die einen Arbeitsauftragstyp von *Überweisungsbeleg* und/oder *Bestellung* haben und Sie den Prozess für *Kennzeichen erhalten (und weglegen)* verwenden, werden die folgenden zwei Warehousing-Prozesse für mobile Apps keine Arbeit bereiten. Stattdessen registrieren sie einfach den eingehenden Bestand auf der Kennzeichnung am eingehenden Empfangsdock.

- *Ladungsträger – Empfang*
- *Kennzeichenempfang und -einlagerung*

> [!NOTE]
> - Sie müssen mindestens einen Speicherort für eine Arbeitsrichtlinie im Abschnitt **Lagerorte** bestimmen. Sie können nicht denselben Speicherort für mehrere Arbeitsrichtlinien angeben.
> - Die Option **Etikett drucken** zum Lagern von Menüelementen für mobile Geräte druckt kein Kennzeichenetikett ohne Arbeitserstellung.

Um diese Funktionalität auf Ihrem System verfügbar zu machen, müssen Sie die Funktion *Verbesserungen beim Empfang von Kennzeichen* in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktivieren.

### <a name="receive-inventory-on-a-location-that-doesnt-track-license-plates"></a>Erhalten Sie Bestand an einem Ort, an dem Kennzeichen nicht erfasst werden

Es ist möglich, einen Lagerort zu verwenden, der einem Standortprofil zugewiesen ist, auch wenn **Verwenden Sie die Kennzeichenverfolgung** nicht eingeschaltet ist. Wenn Sie Bestand erhalten, können Sie den vorhandenen Bestand daher direkt an einem Standort registrieren, ohne dass eine Arbeit erstellt werden muss.

## <a name="add-mobile-device-menu-items-for-each-receiving-location-in-a-warehouse"></a>Fügen Sie für jeden Empfangsort in einem Lager Menüelemente für Mobilgeräte hinzu

Mit der Funktion *Verbesserungen beim Empfang von Kennzeichen* können Sie an jedem Ort in einem Lager empfangen, indem Sie der mobilen Lagerort-App standortspezifische Kennzeichen hinzufügen, die Menüelemente empfangen (und weglegen). Bisher unterstützte das System den Empfang nur am Standardort, der für jedes Lager definiert ist. Wenn diese Funktion aktiviert ist, bieten die Menüelemente für mobile Geräte zum Empfangen (und Weglegen) von Kennzeichen jetzt die **Standarddaten verwenden** Option, mit der Sie für jeden Menüpunkt einen benutzerdefinierten Bis-Speicherort auswählen können. (Diese Option war bereits für einige andere Arten von Menüelementen verfügbar.)

Um diese Funktionalität auf Ihrem System verfügbar zu machen, müssen Sie die Funktion *Verbesserungen beim Empfang von Kennzeichen* in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktivieren.

## <a name="show-or-skip-the-receiving-summary-page"></a>Zeigen Sie die empfangende Zusammenfassungsseite an oder überspringen Sie sie

Sie können die Funktion *Steuern Sie, ob auf Mobilgeräten eine Empfangsübersichtsseite angezeigt werden soll* verwenden, um einen zusätzlichen detaillierten Warehouse-App-Ablauf als Teil des Kennzeichenempfangsprozesses zu nutzen.

Wenn diese Funktion aktiviert ist, bieten Menüelemente für mobile Geräte zum Empfangen von Kennzeichen oder zum Empfangen und Einlagerungen eine Einstellung **Empfangsübersichtsseite anzeigen** an. Diese Einstellung bietet folgende Optionen:

- **Eine detaillierte Zusammenfassung anzeigen** – Während des Empfangs des Kennzeichens wird den Mitarbeitern eine zusätzliche Seite mit den vollständigen ASN-Informationen angezeigt.
- **Überspringen Sie die Zusammenfassung** – Die Mitarbeiter sehen nicht die vollständigen ASN-Informationen. Lagerarbeiter können während des Empfangsprozesses auch keinen Dispositionscode festlegen oder Ausnahmen hinzufügen.

Um diese Funktionalität auf Ihrem System verfügbar zu machen, müssen Sie die Funktion *Steuern Sie, ob auf Mobilgeräten eine Empfangsübersichtsseite angezeigt werden soll* aktivieren in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Verhindern Sie, dass Kennzeichen mit Transportauftragsversand in anderen Lagern als dem Ziellager verwendet werden

Ein Kennzeichenempfangsprozess kann nicht verwendet werden, wenn ein ASN eine Kennzeichen-ID enthält, die bereits vorhanden ist und physische Daten an einem anderen Lagerort als dem Lagerort enthält, an dem die Kennzeichenregistrierung erfolgt.

Für Transportauftragsszenarien, in denen das Transitlager keine Kennzeichen erfasst (und daher auch keinen physischen Lagerbestand pro Kennzeichen erfasst), können Sie die Funktion *Verhindern Sie, dass Versandkennzeichen für Transportaufträge in anderen Lagern als dem Ziellager verwendet werden* verwenden, um physische Aktualisierungen von unterwegs befindlichen Kennzeichen zu verhindern.

Um diese Funktionalität auf Ihrem System verfügbar zu machen, müssen Sie die Funktion aktivieren *Verhindern Sie, dass Versandkennzeichen für Transportaufträge in anderen Lagern als dem Ziellager verwendet werden* in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Führen Sie die folgenden Schritte aus, um die Funktionalität zu verwalten, wenn diese Funktion verfügbar ist.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.
1. Auf der Registerkarte **Allgemeines** im Inforegister **Kennzeichnung** legen Sie das Feld **Kennzeichenrichtlinie für Transitlager** auf einen der folgenden Werte fest:

    - **Wiederverwendung von nicht verfolgtem Kennzeichen zulassen** – Das System funktioniert genauso wie wenn die Funktion *Verhindern Sie, dass Versandkennzeichen für Transportaufträge in anderen Lagern als dem Ziellager verwendet werden* nicht verfügbar ist. Dieser Wert ist die Standardeinstellung, wenn Sie die Funktion zum ersten Mal aktivieren.
    - **Verhindern Sie die Wiederverwendung von nicht verfolgten Kennzeichen** – Bis zum Eingang des Überweisungsauftrags sind im Ziellager nur Aktualisierungen zulässig, die sich auf ein versendetes Kennzeichen beziehen.

## <a name="more-information"></a>Weitere Informationen

Weitere Informationen zu Menüelementen für Mobilgeräte finden Sie unter [Richten Sie mobile Geräte für die Lagerarbeit ein](configure-mobile-devices-warehouse.md).

Weitere Informationen zum *Als fertig melden* Produktionsszenario finden sie unter [Übersicht über die Lagerarbeitsrichtlinien](warehouse-work-policies.md).

Weitere Informationen über eingehende Auslastungverwaltung finden Sie unter [Lagerortverwaltung von eingehender Auslastung für Bestellungen](inbound-load-handling.md).
