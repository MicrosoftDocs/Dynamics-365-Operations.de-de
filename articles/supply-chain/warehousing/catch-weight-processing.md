---
title: Artikelgewichtsproduktverarbeitung mit Lagerortverwaltung
description: In diesem Thema wird beschrieben, wie Arbeitsvorlagen und Lagerplatzrichtlinien verwendet werden, um festzustellen, wie und wo Arbeit am Lagerort ausgeführt wird.
author: perlynne
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: ced22a144e57b624ceacb8bb5c3032218db3a0eb
ms.sourcegitcommit: bacec397ee48ac583596be156c87ead474ee07df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "777271"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Artikelgewichtsproduktverarbeitung mit Lagerortverwaltung

[!include [banner](../includes/banner.md)]

## <a name="feature-exposure"></a>Funktionsbereitstellung

Um die Lagerortverwaltung für die Artikelgewichtsproduktverarbeitung zu verwenden, müssen Sie einen Lizenzkonfigurationsschlüssel verwenden, um die Funktionen zu aktivieren. (Gehen Sie zu **Systemadministration \> Einrichten \> Lizenzkonfiguration**. Erweitern Sie dann auf der Registerkarte **Konfigurationsschlüssel** die Option **Art \> Lagerort- und Transportverwaltung**, und aktivieren Sie das Kontrollkästchen für **Artikelgewicht für Lagerort**).

> [!NOTE]
> Sowohl der **Lagerort und Transportverwaltung**-Lizenzkonfigurationsschlüssel als auch die **Prozessverteilungsartikelgewicht \> Lizenzkonfigurationsschlüssel** müssen ebenfalls aktiviert werden.

Nachdem der Lizenzkonfigurationsschlüssel aktiviert ist, können Sie beim Erstellen eines freigegebenen Produkts **Artikelgewicht** auswählen. Sie können das freigegebene Produkt auch einer Lagerdimensionsgruppe zuordnen, für die der **Lagerortverwaltungsprozesse verwenden**-Parameter ausgewählt ist.

Bevor Sie das Produkt in der Lagerortverwaltung verwenden können, müssen Sie einige produktspezifische Grundeinstellungen für das Artikelgewicht vornehmen:

- Definieren Sie die nominelle Gewichtsumrechnung zwischen der Artikelgewichtseinheit (Box) und der Lagereinheit (Kilogramm \[kg\]) als Teil einer Einheitumrechnungsdefinition.
- Definieren Sie die Mindest- und Höchstgewichtstoleranzen als Teil der Artikelgewichtseinheits-Einstellung.
- Richten Sie eine Einheitsnummernkreisgruppe ein, in der die Artikelgewichtseinheit als niedrigste Lagermengeneinheit (SKU) definiert wird.
- Richten Sie eine Artikelgewichtsartikel-Handhabungsrichtlinie ein.

Weitere Informationen finden Sie unter [Einrichten und Verwalten von Artikelgewichtsartikeln](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Transaktionsregulierungen

Da das Gewicht des Bestands bei Ankunft am Lagerort vom Gewicht des Bestands bei Entnahme aus dem Lagerort abweichen kann, muss die Artikelgewichtsproduktverarbeitung den Bestand regulieren.

**Beispiel 1**

Während des Produktionsprozesses **Fertigmeldung** wird das Eingangsgewicht eines Ladungsträgers, der acht Boxen eines Artikelgewichtsprodukts enthält, mit 80,1 kg erfasst. Der Ladungsträger wird dann im Bereich für fertiggestellte Güter gelagert, und während des Lagerungszeitraums wird Gewicht in die Luft abgegeben.

Später wird das Gewicht des gleichen Ladungsträgers als Teil eines Auftragskommissionierungsprozesses mit 79,8 kg erfasst. Im System gibt es jetzt also eine Gewichtsdifferenz als Teil des physischen Dimensionssatzes.

In diesem Fall passt das System automatisch die Differenz an, indem eine Transaktion für die fehlenden 0,3 kg gebucht wird.

**Beispiel 2**

In der Definition wird ein Produkt so eingerichtet, dass ein Mindestgewicht von 8 kg und ein Höchstgewicht von 12 kg für die **Box**-Artikelgewichtseinheit toleriert wird.

Es gibt zwei Boxen des Produkts, und sie haben ein erfasstes Gewicht von 16 kg. Wenn ein Lagerarbeiter eine der Boxen entnimmt und wiegt und das Gewicht mit 9 kg erfasst wird, wiegt die verbleibende Box 7 kg. Da 7 kg jedoch unter dem Mindestgewicht liegen, führt das System eine automatische Anpassung durch, um das Gewicht des verfügbaren Bestands um 1 kg zu erhöhen.

Um die Konten so einzurichten, dass diese Regulierungen gebucht werden, gehen Sie zu **Kostenverwaltung \> Einrichtung der Sachkontointegrationsrichtlinien \> Buchung**. Definieren Sie anschließend auf der Registerkarte **Bestand** die folgenden Konten:

- Artikelgewicht - Verlustkonto
- Artikelgewicht - Gewinnkonto

## <a name="catch-weight-item-handling-policy"></a>Artikelgewichtsartikel-Handhabungsrichtlinie

Die Artikelgewichtsartikel-Handhabungsrichtlinie definiert zwei primäre Lagerortverwaltungsflüsse für die Artikel: wann das Gewicht der Artikel erfasst wird, und wie es erfasst wird.

Sie können definieren, wann das Gewicht für die Verkaufs- und Umlagerungsauftragsverarbeitung erfasst wird. Das Gewicht kann bei einem der folgenden Prozesse erfasst werden:

- **Entnahme** – Das Gewicht wird bei den Anfangs-Entnahmearbeitspositionen bei der Auftragsarbeit erfasst.
- **Verpackung** – Das Gewicht wird bei der manuellen Verpackung erfasst. (Sie müssen die Artikel an eine Verpackungsstation senden.)

Wenn das tatsächliche Gewicht an der Verpackungsstation während des Containerverpackungsprozesses erfasst wird, werden die Lagerarbeiter nicht aufgefordert, das Gewicht bei der Entnahmearbeit zu erfassen. Stattdessen wird das Durchschnittsgewicht des physischen Bestands als Gewicht des für den Verpackungsbereich entnommenen Bestands verwendet.

Bei internen Lagerortverwaltungsprozessen wie Inventur- wie und Regulierungskorrekturen kann definiert werden, ob das Gewicht erfasst werden soll oder nicht. Wird es nicht erfasst, wird das nominelle Gewicht verwendet.

Sie können auch definieren, wie das Gewicht erfasst wird. In einem der beiden Hauptflüsse, werden Artikelgewichtsmarkierungen nachverfolgt und verwendet, um das Gewicht zu erfassen. In dem anderen Fluss werden Artikelgewichtsmarkierungen nicht nachverfolgt.

- **Ja** – Der Artikel verwendet Artikelgewichtsmarkierungen. Jede Markierungsnummer stellt eine Artikelgewichtseinheit (Box) dar, und ein Gewicht und andere Informationen werden der Markierung zugeordnet. Für ausgehende Verarbeitungen wird das Gewicht, das der Markierung zugeordnet ist, verwendet.
- **Nein** – Der Artikel verwendet keine Artikelgewichtsmarkierungen. Die Ein- und Ausgangswiegeprozesse basieren auf dem tatsächlichen Gewicht, das bei jedem Prozess erfasst wird.

Der Prozess zur Nachverfolgung von Artikelgewichtsmarkierungen kann für Artikel verwendet werden, deren Gewicht sich während des Lagerungszeitraums nicht verändert. Das Gewicht wird nur beim Eingangslagerort-Prozess erfasst. Während des Ausgangsprozesses werden die Artikelgewichtsmarkierungen nur gescannt, und das jeweilige Gewicht, das den Markierungen zugeordnet wird, wird für die Ausgangstransaktionsverarbeitung verwendet.

### <a name="how-to-capture-catch-weight"></a>So wird das Artikelgewicht aufgezeichnet

Wenn die Artikelgewichtsmarkierungs-Nachverfolgung verwendet wird, muss eine Markierung immer für jede eingegangene Artikelgewichtseinheit erstellt werden, und jede Markierung muss immer einem Gewicht zugeordnet werden.

Beispielsweise ist **Box** die Artikelgewichteinheit, und Sie erhalten eine Palette mit acht Boxen. In diesem Fall müssen acht eindeutige Artikelgewichtsmarkierungen erstellt werden, und ein Gewicht muss jeder Markierung zugeordnet werden. Je nach Eingangsartikelgewichts-Markierung kann entweder das Gewicht aller acht Boxen erfasst werden und das Durchschnittsgewicht dann auf jede Box verteilt werden, oder ein eindeutiges Gewicht kann für jede Box erfasst werden.

Wenn die Artikelgewichtsmarkierungs-Nachverfolgung nicht verwendet wird, kann das Gewicht für jeden Dimensionssatz erfasst werden (z. B. für jeden Ladungsträger und alle Rückverfolgungsangaben). Alternativ kann das Gewicht auf Basis einer aggregierten Ebene erfasst werden, z. B. fünf Ladungsträger (Paletten).

Für die Methoden zur Erfassung des ausgehenden Gewichts können Sie definieren, ob das Wiegen für jede Artikelgewichtseinheit erfolgt (d. h. pro Box), oder ob das Gewicht auf Basis der entnommenen Menge erfasst wird (z. B. drei Boxen). Beachten Sie, dass für den Produktionsauftragspositions-Entnahmeprozess das Durchschnittsgewicht verwendet wird, wenn die Option **Nicht erfasst** verwendet wird.

## <a name="supported-scenarios"></a>Unterstützte Szenarien

Nicht alle Workflows unterstützen die Artikelgewichtsproduktverarbeitung mit Lagerortverwaltung. Die folgenden Einschränkungen gelten derzeit.
 
### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Konfigurieren von Artikelgewichtsprodukten für Lagerortverwaltungsprozesse

- Für Artikelgewichtsprodukte kann die Lagerdimensionsgruppe für Artikel nicht geändert werden (sodass Lagerortverwaltungsprozesse für sie verwendet werden können).
- Nur die Formelverarbeitung wird für Artikelgewichtsprodukte unterstützt (keine Stückliste).
- Artikelgewichtsprodukte können keiner Rückverfolgungsangabengruppe zugeordnet werden, indem die Eigentümerdimension verwendet wird.
- Artikelgewichtsprodukte können nicht als Dienstleistungen verwendet werden.
- Artikelgewichtsprodukte können nur als Teil der Artikelmodellgruppe als "gelagerte Produkte" verwendet werden.
- Artikelgewichtsprodukte können nicht zusammen mit den Funktionen zum Nachverfolgen von "Im Verkaufsprozess aktiv" verwendet werden.
- Artikelgewichtsprodukte können nicht zusammen mit den Funktionen zum Erfassen von Seriennummern verwendet werden. Daher können Produkte nicht von einer "leeren" zu einer Seriennummer als Teil des Entnahme/Verpackungsprozesses übertragen werden.
- Artikelgewichtsprodukte können nicht zusammen mit den Funktionen zum Registrieren von Serien vor Verbrauch verwendet werden.
- Artikelgewichtsprodukte, die für Varianten aktiviert sind, können nicht zusammen mit der Funktion für das Konvertieren von Varianten-Maßeinheiten verwendet werden.
- Artikelgewichtsprodukte können nicht als Einzelhandels-"Produktset" markiert werden.
- Artikelgewichtsprodukte können nur mit einer Einheitsnummernkreisgruppe verwendet werden, die über Artikelgewichts-Handhabungseinheiten verfügt, und bei der die Artikelgewichtseinheit den niedrigsten Nummernkreis aufweist.
- Für Artikelgewichtsprodukte kann die Bestandseinheit nur dann in die Artikelgewichtseinheit umgerechnet werden, wenn die Umrechnung eine nominelle Menge ergibt, die mehr als 1 beträgt.
- Die Einrichtung von Strichcodes für Artikelgewichtsprodukte unterstützt keine Einrichtung für variables Gewicht.
 
### <a name="order-processing"></a>Auftragsverarbeitung

- Die Intercompany-Auftragsverarbeitung wird nicht unterstützt.
- Die Erstellung des Versand-Avis (ASN/Verpackungsstrukturen) unterstützt keine Gewichtsinformationen.
- Die Auftragsmenge muss basierend auf der Artikelgewichtseinheit verwaltet werden.
 
### <a name="inbound-warehouse-processing"></a>Eingangslagerortverarbeitung

- Das Empfangen von Ladungsträgern setzt voraus, dass Gewichte während der Registrierung zugeordnet werden, da die Gewichtsinformationen nicht als Teil des Versand-Avis unterstützt werden. Wenn Artikelgewichtsmarkierungs-Prozesse verwendet werden, muss die Markierungsnummer manuell pro Artikelgewichtseinheit zugewiesen werden.
- Der Empfang gemischter Ladungsträger wird für Artikelgewichtsprodukte nicht unterstützt.
 
### <a name="inventory-and-warehouse-operations"></a>Bestands- und Lagerortbetrieb

- Das manuelle Erstellen von Quarantäneaufträgen wird für Artikelgewichtsprodukte nicht unterstützt.
- Das manuelle Umlagern von Bestand, der einer Arbeit zugeordnet ist, wird für Artikelgewichtsprodukte nicht unterstützt.
- Die Konsolidierung von Ladungsträgern wird für Artikelgewichtsprodukte nicht unterstützt.
- Änderungen am Lagerort-Bestandsstatus als Teil einer regelmäßigen Aufgabe werden für Artikelgewichtsprodukte nicht unterstützt.
- Änderungen am Bestandsstatus, die von einer Abfrage definiert werden, werden für Artikelgewichtsprodukte nicht unterstützt. (Änderungen dem Qualitätsprüfungsauftrags-Bestandsstatus werden ebenfalls nicht unterstützt.)
- Für Artikelgewichtsprodukte kann der Bestandsstatus nicht auf der Seite **Verfügbarer Lagerbestand nach Lagerplatz** geändert werden.
- Für Artikelgewichtsprodukte kann der Bestandsstatus nicht als Teil der Lagerort-App-Umlagerungsarbeit geändert werden.
- Ladungsträgerladungen zur Initialisierung des Lagerortbestands werden nicht für Artikelgewichtsprodukte unterstützt.
- Chargenausgleichprozesse werden nicht für Artikelgewichtsprodukte unterstützt.
- Die Handhabung von negativem physischem Bestand wird nicht für Artikelgewichtsprodukte unterstützt.
- Bestandsmarkierungen werden nicht für Artikelgewichtsprodukte unterstützt.
 
### <a name="outbound-warehouse-processing"></a>Ausgangslagerortverarbeitung

- Die Funktionen zur Clusterkommissionierung werden nicht für Artikelgewichtsprodukte unterstützt.
- Entnahme- und Verpackungs-Lagerortverarbeitungen werden für Artikelgewichtsprodukte nicht unterstützt.
- Für Artikelgewichtsprodukte kann die Arbeit nicht auf der Seite **Arbeit** ausgeführt werden.
- Für Artikelgewichtsprodukte kann Arbeit, die in einer Arbeitsvorlage definiert ist, automatisch ausgeführt werden.
- Die Funktionen zur Stornierung von Arbeit werden nicht für Artikelgewichtsprodukte unterstützt.
- Für Artikelgewichtsprodukte wird die manuelle Verpackungsstationsverarbeitung, bei der Arbeit nach dem Schließen von Containern erstellt wird, nicht unterstützt.
- Die Funktionen zum stückweisen Scannen werden nicht für Artikelgewichtsprodukte unterstützt.
 
### <a name="production-processing"></a>Produktionsverarbeitung

- Für Artikelgewichtsprodukte werden nur Chargenaufträge für Formelprodukte unterstützt.
- Die Kanban-Funktionen werden nicht für Artikelgewichtsprodukte unterstützt.
- Für Artikelgewichtsprodukte können Seriennummern nicht vor dem Verbrauch registriert werden.
- Die Funktionen zur Stornierung von Ladungsträgern werden nicht für Artikelgewichtsprodukte unterstützt.
- Für Artikelgewichtsprodukte kann die Fertigmeldung nach Seriennummer registriert werden.

### <a name="transportation-management-processing"></a>Transportverwaltungsverarbeitung

- Ladungserstellungsworkbenchverarbeitungen werden für Artikelgewichtsprodukte nicht unterstützt.
- Transportanforderungspositionen werden für Artikelgewichtsprodukte nicht unterstützt.
 
### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Andere Einschränkungen und Verhaltensweisen für die Artikelgewichtsproduktverarbeitung mit Lagerortverwaltung

- Wenn Artikelgewichtsmarkierungen als Teil der Lagerort-App-Verarbeitung erfasst werden, kann der Benutzer diesen Prozess nicht im Workflow abbrechen.
- Während der Entnahmeprozesse, in denen der Benutzer nicht aufgefordert wird, Rückverfolgungsangaben zu identifizieren, erfolgt die Gewichts-Zuweisung basierend auf dem Durchschnittsgewicht. Dieses Verhalten tritt auf, wenn z. B. eine Kombination von Rückverfolgungsangaben am gleichen Lagerplatz verwendet wird, und, nachdem ein Benutzer die Entnahme verarbeitet hat, nur ein Rückverfolgungsangabewert am Lagerplatz verbleibt.
- Wenn der Bestand für ein Artikelgewichtsprodukt reserviert wird, das für Lagerortverwaltungsprozesse konfiguriert ist, erfolgt die Reservierung auf Grundlage des Mindestgewichts, das definiert wird, auch wenn diese Menge die letzte verfügbare Handhabungsmenge ist. Dieses Verhalten unterscheidet sich vom Verhalten für Artikel, die nicht für Lagerortverwaltungsprozesse konfiguriert sind.
- Prozesse, die das Gewicht als Teil der Kapazitätsberechnungen verwenden (Wellenschwellenwerte, maximale Arbeitspausen, Container-Höchstwerte, Lagerplatzladekapazitäten usw.), verwenden nicht das tatsächliche Gewicht des Bestands. Stattdessen basieren die Prozesse auf dem physischen Handhabungsgewicht, das für das Produkt definiert wird.
- Retail-Funktionen werden in der Regel nicht für Artikelgewichtsprodukte unterstützt.
 
### <a name="catch-weight-tags"></a>Artikelgewichtsmarkierungen

Derzeit werden die Funktionen für Artikelgewichtsmarkierungen nur als Teil der folgenden Szenarien unterstützt:

- Wenn der Bestellungseingang über die Lagerort-App verarbeitet wird.
- Wenn der Ladungseingang über die Lagerort-App verarbeitet wird.
- Für den Ladungsträgereingang, der einer Bestellungsladung zugeordnet ist, wird die Gewichts-Zuweisung beim Eingangsprozess angefordert. Im Gegensatz dazu wird für den Umlagerungsauftragseingang das Gewicht aus den Lieferdaten für den Umlagerungsauftrag verwendet.
- Für den Umlagerungsauftragsartikel- und -positionseingang, der aus einem Nicht-Lagerortverwaltungsprozess-Lagerort stammt.
- Die Verarbeitung des Rücklieferungseingangs kann Artikelgewichtsmarkierungen erfassen, aber die Verarbeitung wird nicht geprüft, wenn die Markierungen dieselben Markierungen sind, die ursprünglich für eine bestimmte Auftragsposition geliefert wurden.
- Wenn ein geänderter Bestandsstatus mithilfe der Lagerort-App verarbeitet wird.
- Wenn eine Lagerort-Umlagerung mithilfe der Lagerort-App ausgeführt wird.
- Wenn eine ein- und ausgehende Regulierung über die Lagerort-App verarbeitet wird.
- Wenn die Entnahmearbeit für Verkaufsaufträge und Umlagerungsaufträge verarbeitet wird. (Beachten Sie, dass Artikelgewichtsmarkierungen nicht für die Entnahme von Produktionskomponenten erfasst werden können.)
- Wenn entnommene Mengen aus Ladungspositionen reduziert werden, unabhängig davon, ob Container verwendet werden.
- Wenn Produkte an einer Verpackungsstation in Container gepackt werden.
- Wenn Container neu geöffnet werden.
- Wenn Formelprodukte mithilfe der Lagerort-App als fertig gemeldet werden.
- Wenn Transportladungen mithilfe der Lagerort-App verarbeitet werden.
