---
title: Artikelgewichtsproduktverarbeitung mit Lagerortverwaltung
description: In diesem Thema wird beschrieben, wie Arbeitsvorlagen und Lagerplatzrichtlinien verwendet werden, um festzustellen, wie und wo Arbeit am Lagerort ausgeführt wird.
author: perlynne
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy, TMSLoadBuildWorkbench, WHSCatchWeightTagRegistration, WHSCatchWeightTagFullDimDiscrepancies, WHSCatchWeightTagChangeWeightDropDownDialog, WHSCatchWeightLinkWorkLineTagDropDownDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8e56688aac445b84d5a9c0df289d48ffefd5767f673f2329f69582e820c27820
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738148"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Artikelgewichtsproduktverarbeitung mit Lagerortverwaltung

[!include [banner](../includes/banner.md)]

## <a name="feature-exposure"></a>Funktionsbereitstellung

Um die Lagerortverwaltung für die Artikelgewichtsproduktverarbeitung zu verwenden, müssen Sie einen Lizenzkonfigurationsschlüssel verwenden, um die Funktionen zu aktivieren. Gehen Sie zu **Systemadministration \> Einrichten \> Lizenzkonfiguration**. Erweitern Sie dann auf der Registerkarte **Konfigurationsschlüssel** **Handel \> Lager- und Transportverwaltung**, und markieren Sie das Kontrollkästchen für **Artikelgewicht für Lager**.

> [!NOTE]
> Sowohl der **Lagerort und Transportverwaltung**-Lizenzkonfigurationsschlüssel als auch die **Prozessverteilungsartikelgewicht \> Lizenzkonfigurationsschlüssel** müssen ebenfalls aktiviert werden. Um die Konfigurationsschlüssel für das Artikelgewicht festzulegen, müssen Sie die Funktion auch mit dem Arbeitsbereich **Funktionsverwaltung** aktivieren. Die Hauptfunktion, die aktiviert werden muss, ist **Artikelgewichtsproduktverarbeitung mit Lagerortverwaltung**. Zwei verwandte, aber optionale Funktionen, die Sie möglicherweise einschalten möchten, sind **Lagerstatusänderungen für Produkte mit Artikelgewicht** und **Benutzen Sie vorhandene Artikelgewichtkennzeichnungen, wenn Sie Produktionsaufträge als abgeschlossen melden**.

Nachdem der Lizenzkonfigurationsschlüssel aktiviert ist, können Sie beim Erstellen eines freigegebenen Produkts **Artikelgewicht** auswählen. Sie können das freigegebene Produkt auch einer Lagerdimensionsgruppe zuordnen, für die der **Lagerortverwaltungsprozesse verwenden**-Parameter ausgewählt ist.

Bevor Sie das Produkt in der Lagerortverwaltung verwenden können, müssen Sie einige produktspezifische Grundeinstellungen für das Artikelgewicht vornehmen:

- Definieren Sie die nominelle Gewichtsumrechnung zwischen der Artikelgewichtseinheit (Box) und der Lagereinheit (Kilogramm \[kg\]) als Teil einer Einheitumrechnungsdefinition.
- Definieren Sie die Mindest- und Höchstgewichtstoleranzen als Teil der Artikelgewichtseinheits-Einstellung.
- Richten Sie eine Einheitsnummernkreisgruppe ein, in der die Artikelgewichtseinheit als niedrigste Lagermengeneinheit (SKU) definiert wird.
- Richten Sie eine Artikelgewichtsartikel-Handhabungsrichtlinie ein.

Weitere Informationen finden Sie unter [Einrichten und Verwalten von Artikelgewichtsartikeln](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Transaktionsregulierungen

Da das Gewicht des Bestands bei Ankunft am Lagerort vom Gewicht des Bestands bei Entnahme aus dem Lagerort abweichen kann, muss die Artikelgewichtsproduktverarbeitung den Bestand regulieren.

> [!NOTE]
> Die Aktivität des Mobilgeräts löst die Transaktionsanpassungen nur aus, wenn die ausgehende Gewichtsabweichungsmethode der Richtlinie zur Handhabung von Gegenständen mit Artikelgewicht **Gewichtsabweichung zulassen** lautet.

### <a name="example-1"></a>Beispiel 1

Während des Produktionsprozesses **Fertigmeldung** wird das Eingangsgewicht eines Ladungsträgers, der acht Boxen eines Artikelgewichtsprodukts enthält, mit 80,1 kg erfasst. Der Ladungsträger wird dann im Bereich für fertiggestellte Güter gelagert, und während des Lagerungszeitraums wird Gewicht in die Luft abgegeben.

Später wird das Gewicht des gleichen Ladungsträgers als Teil eines Auftragskommissionierungsprozesses mit 79,8 kg erfasst. Im System gibt es jetzt also eine Gewichtsdifferenz als Teil des physischen Dimensionssatzes.

In diesem Fall passt das System automatisch die Differenz an, indem eine Transaktion für die fehlenden 0,3 kg gebucht wird.

### <a name="example-2"></a>Beispiel 2

In der Definition wird ein Produkt so eingerichtet, dass ein Mindestgewicht von 8 kg und ein Höchstgewicht von 12 kg für die **Box**-Artikelgewichtseinheit toleriert wird.

Es gibt zwei Boxen des Produkts, und sie haben ein erfasstes Gewicht von 16 kg. Wenn ein Lagerarbeiter eine der Boxen entnimmt und wiegt und das Gewicht mit 9 kg erfasst wird, wiegt die verbleibende Box 7 kg. Da 7 kg jedoch unter dem Mindestgewicht liegen, führt das System eine automatische Anpassung durch, um das Gewicht des verfügbaren Bestands um 1 kg zu erhöhen.

Um die Konten so einzurichten, dass diese Regulierungen gebucht werden, gehen Sie zu **Kostenverwaltung \> Einrichtung der Sachkontointegrationsrichtlinien \> Buchung**. Definieren Sie anschließend auf der Registerkarte **Bestand** die folgenden Konten:

- Artikelgewicht - Verlustkonto
- Artikelgewicht - Gewinnkonto

## <a name="catch-weight-item-handling-policy"></a>Artikelgewichtsartikel-Handhabungsrichtlinie

Die Artikelgewichtsartikel-Handhabungsrichtlinie definiert zwei primäre Lagerortverwaltungsflüsse für die Artikel: wann das Gewicht der Artikel erfasst wird, und wie es erfasst wird.

Sie können definieren, wann das Gewicht für die Verkaufs- und Umlagerungsauftragsverarbeitung erfasst wird. Das Gewicht kann bei einem der folgenden Prozesse erfasst werden:

- **Entnahme** – Das Gewicht wird bei den Anfangs-Entnahmearbeitspositionen bei der Auftragsarbeit erfasst.
- **Verpackung** – Das Gewicht wird bei der manuellen Verpackung erfasst. (Sie müssen die Artikel an eine Verpackungsstation senden.)

Wenn das tatsächliche Gewicht an der Verpackungsstation während des Containerverpackungsprozesses erfasst wird, werden die Lagerarbeiter nicht aufgefordert, das Gewicht bei der Entnahmearbeit zu erfassen. Stattdessen wird das Durchschnittsgewicht des physischen Bestands als Gewicht des für den Verpackungsbereich entnommenen Bestands verwendet. Dieses Konzept gilt auch für das Erfassen von Artikelgewichten, die über Tags verfolgt werden. Bei mit Tags verfolgten Elementen bestimmen diese Parameter, wann das Tag erfasst wird. Das Etikett kann entweder zum Zeitpunkt der Entnahme mithilfe des Mobilgeräts oder beim manuellen Verpacken erfasst werden.

> [!NOTE]
> Da die Option **Verpackung** bewirkt, dass das Inventar mit dem durchschnittlich ausgewählten Gewicht aktualisiert wird, kann dies eine Diskrepanz auslösen, die eine Anpassung des Gewinns/Verlusts des Artikelgewichts und/oder eine Differenz zwischen dem vorhandenen Inventargewicht und dem Gewicht des Artikelgewichtstags verursachen kann.

Bei internen Lagerortverwaltungsprozessen wie Inventur und Regulierungskorrekturen können Sie definieren, ob das Gewicht erfasst werden soll. Wird es nicht erfasst, wird das nominelle Gewicht verwendet. Mit anderen Optionen können Sie das Gewicht pro Artikelgewichtseinheit und pro Zählmenge erfassen.

Sie können auch definieren, wie das Gewicht erfasst wird. In einem der beiden Hauptflüsse, werden Artikelgewichtsmarkierungen nachverfolgt und verwendet, um das Gewicht zu erfassen. In dem anderen Fluss werden Artikelgewichtsmarkierungen nicht nachverfolgt.

- **Ja** – Der Artikel verwendet Artikelgewichtsmarkierungen. Jede Markierungsnummer stellt eine Artikelgewichtseinheit (Box) dar, und ein Gewicht und andere Informationen werden der Markierung zugeordnet. Für ausgehende Verarbeitungen wird das Gewicht, das der Markierung zugeordnet ist, verwendet.
- **Nein** – Der Artikel verwendet keine Artikelgewichtsmarkierungen. Die Ein- und Ausgangswiegeprozesse basieren auf dem tatsächlichen Gewicht, das bei jedem Prozess erfasst wird.

Der Prozess zur Nachverfolgung von Artikelgewichtsmarkierungen kann für Artikel verwendet werden, deren Gewicht sich während des Lagerungszeitraums nicht verändert. Das Gewicht wird nur beim Eingangslagerort-Prozess erfasst. Während des Ausgangsprozesses werden die Artikelgewichtsmarkierungen nur gescannt, und das jeweilige Gewicht, das den Markierungen zugeordnet wird, wird für die Ausgangstransaktionsverarbeitung verwendet.

Ein weiterer wichtiger Parameter, der sich auf die Verarbeitung von Artikelgewichtstags bezieht, ist **Dimensionsrückverfolgungsmethode des Artikelgewichtstags**. Tags können entweder teilweise oder vollständig verfolgt werden. Wenn ein Tag teilweise nachverfolgt wird, werden die Produktdimensionen, die Rückverfolgungsangaben und der Inventarstatus nachverfolgt. Wenn ein Tag vollständig nachverfolgt wird, werden die Produktdimensionen, die Rückverfolgungsangaben und **alle** Lagerdimensionen nachverfolgt.

Wenn ein Element mit einem Tag verfolgt wird, gibt es außerdem einen Parameter **Erfassungsmethode für ausgehende Tags**. Sie können diesen Parameter so einstellen, dass Sie bei ausgehenden Transaktionen auf dem Mobilgerät immer zur Eingabe des Tags aufgefordert werden. Alternativ können Sie den Parameter so einstellen, dass Sie nur dann zur Eingabe von Tags aufgefordert werden, wenn diese erforderlich sind. Beispielsweise befinden sich auf einem bestimmten Kennzeichen fünf Tags mit Artikelgewicht im Inventar, und Sie haben angegeben, dass Sie alle fünf Tags vom Kennzeichen auswählen möchten. Wenn in diesem Fall der Parameter **Erfassungsmethode für ausgehende Tags** auf **Tag nur bei Bedarf anfordern** gesetzt ist, werden die fünf Tags automatisch ausgewählt. Sie müssen nicht jedes Tag scannen. Wenn der Parameter auf **Immer nach dem Tag fragen** eingestellt ist, müssen Sie jedes Tag scannen, auch wenn alle fünf Tags ausgewählt werden.

> [!NOTE]
> Tags werden in der Regel nur über die Menüelemente des Mobilgeräts erfasst und aktualisiert. Dennoch gibt es einige Szenarien, in denen Tags an anderer Stelle erfasst werden (z. B. von der manuellen Packstation). Im Allgemeinen sollten jedoch die Menüelemente für mobile Geräte für alle Lagerplatzaktivitäten verwendet werden, wenn Tags verwendet werden.

### <a name="how-to-capture-catch-weight"></a>So wird das Artikelgewicht aufgezeichnet

**Wenn die Artikelgewichtstag-Rückverfolgung verwendet wird**, muss ein Tag immer für jede eingegangene Artikelgewichtseinheit erstellt werden, und jedes Tag muss immer einem Gewicht zugeordnet werden.

Beispielsweise ist **Box** die Artikelgewichteinheit, und Sie erhalten eine Palette mit acht Boxen. In diesem Fall müssen acht eindeutige Artikelgewichtsmarkierungen erstellt werden, und ein Gewicht muss jeder Markierung zugeordnet werden. Je nach Eingangsartikelgewichts-Markierung kann entweder das Gewicht aller acht Boxen erfasst werden und das Durchschnittsgewicht dann auf jede Box verteilt werden, oder ein eindeutiges Gewicht kann für jede Box erfasst werden.
Wenn Sie die Funktion **Bestehende Artikelgewicht-Tags verwenden, wenn Sie Produktionsaufträge als abgeschlossen melden**, wobei der Prozess über einen Menüpunkt des Mobilgeräts aktiviert ist, wird der Bestand auf der Grundlage der vorhandenen Artikelgewicht-Tag-Informationen aktualisiert. Daher fordert die Warehouse Management Mobile App nicht dazu auf, die Daten der Artikelgewicht-Tags als Teil eines Produktionsberichts als fertigen Vorgang zu erfassen.

**Wenn die Artikelgewichtstag-Rückverfolgung nicht verwendet wird**, kann das Gewicht für jeden Dimensionssatz erfasst werden (z. B. für jeden Ladungsträger und alle Rückverfolgungsangaben). Alternativ kann das Gewicht auf Basis einer aggregierten Ebene erfasst werden, z. B. fünf Ladungsträger (Paletten).

Für die Methoden zur Erfassung des Ausgangsgewichts können Sie mit der Option **Pro Artikelgewichtseinheit** den Wiegevorgang festlegen, der für jede Artikelgewichtseinheit erfolgen soll (z. B. pro Kiste). Mit der Option **Pro Kommissioniereinheit** können Sie festlegen, dass das Gewicht basierend auf der zu kommissionierenden Menge erfasst werden soll (z. B. drei Kästchen). Beachten Sie, dass für die Entnahme der Produktionsauftragsposition und für interne Verschiebungsprozesse das Durchschnittsgewicht verwendet wird, wenn die Option **Nicht erfasst** verwendet wird.

In der Richtlinie zur Handhabung von Gegenständen mit Artikelgewicht sind mehrere Methoden zur Gewichtserfassung definiert. Jeder Parameter der Gewichtserfassungsmethode wird von verschiedenen Transaktionen verwendet. Die folgende Tabelle fasst zusammen, welche Parameter von welchen Transaktionen verwendet werden.

| Methode                                     | Buchung                                |
|--------------------------------------------|--------------------------------------------|
| Ausgangsgewichts-Erfassungsmethode           | Verkaufskommissionierung, Transferkommissionierung            |
| Erfassungsmethode für Produktionsentnahmegewicht | Produktionskommissionierung, Produktionsverbrauch |
| Umlagerungsgewichts-Erfassungsmethode           | Bewegung                                   |
| Wann Gewichtskorrekturen erfasst werden sollen       | Anpassungen, Zählen                      |
| Inventur Gewichts-Erfassungsmethode           | Inventur                                   |
| Erfassungsmethode Lagerort-Umlagerungsgewicht | Lagerortumlagerung                         |

Um zu verhindern, dass bei den Entnahmevorgängen der Lagerortverwaltung Gewichte erfasst werden, die zu Artikelgewichtgewinn-/ oder Verlustregulierungen führen, können Sie die Methode der Ausgangsgewichtsabweichung verwenden. Die ausgehende Gewichtsabweichungsmethode gilt für die folgenden Prozesse auf Mobilgeräten: Verkaufskommissionierung, Umlagerungskommissionierung, Produktionskommissionierung, Bewegungen, Zählung und Lagerumlagerung. Sie können Sie Option **Gewichtsabweichung einschränken** verwenden, wenn das Gewicht des Gegenstands mit Artikelgewicht während der Lagerung im Lager nicht schwankt und keine Gewinn-/Verlustanpassungen für das Artikelgewicht erforderlich sind. Sie können die Option **Gewichtsabweichung zulassen** verwenden, wenn das Gewicht schwanken kann und wenn Gewinn-/Verlustanpassungen für das Artikelgewicht erforderlich sind, wenn eine Gewichtsschwankung erfasst wird.

## <a name="unsupported-scenarios"></a>Nicht unterstützte Szenarien

Nicht alle Workflows unterstützen die Artikelgewichtsproduktverarbeitung mit Lagerortverwaltung. Die folgenden Einschränkungen gelten derzeit. Sie gelten für alle Gegenstände mit Artikelgewicht, unabhängig davon, ob sie mit Tags versehen sind.

### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Konfigurieren von Artikelgewichtsprodukten für Lagerortverwaltungsprozesse

- Nur die Formelverarbeitung wird für Artikelgewichtsprodukte unterstützt (keine Stückliste).
- Artikelgewichtsprodukte können keiner Rückverfolgungsangabengruppe zugeordnet werden, indem die Eigentümerdimension verwendet wird.
- Artikelgewichtsprodukte können nicht als Dienstleistungen verwendet werden.
- Artikelgewichtsprodukte können nur als Teil der Artikelmodellgruppe als "gelagerte Produkte" verwendet werden.
- Artikelgewichtsprodukte können nicht zusammen mit den Funktionen zum Nachverfolgen von "Im Verkaufsprozess aktiv" verwendet werden.
- Artikelgewichtsprodukte können nicht zusammen mit den Funktionen zum Erfassen von Seriennummern verwendet werden. Daher können Produkte nicht von einer "leeren" zu einer Seriennummer als Teil des Entnahme/Verpackungsprozesses übertragen werden.
- Artikelgewichtsprodukte können nicht zusammen mit den Funktionen zum Registrieren von Serien vor Verbrauch verwendet werden.
- Artikelgewichtsprodukte, die für Varianten aktiviert sind, können nicht zusammen mit der Funktion für das Konvertieren von Varianten-Maßeinheiten verwendet werden.
- Artikelgewichtsprodukte können nicht als Commerce-„Produktset“ markiert werden.
- Artikelgewichtsprodukte können nur mit einer Einheitsnummernkreisgruppe verwendet werden, die über Artikelgewichts-Handhabungseinheiten verfügt, und bei der die Artikelgewichtseinheit den niedrigsten Nummernkreis aufweist.
- Für Artikelgewichtsprodukte kann die Bestandseinheit nur dann in die Artikelgewichtseinheit umgerechnet werden, wenn die Umrechnung eine nominelle Menge ergibt, die mehr als 1 beträgt.
- Die Einrichtung von Strichcodes für Artikelgewichtsprodukte unterstützt keine Einrichtung für variables Gewicht.

### <a name="order-processing"></a>Auftragsverarbeitung

- Die Erstellung des Versand-Avis (ASN/Verpackungsstrukturen) unterstützt keine Gewichtsinformationen.
- Die Auftragsmenge muss basierend auf der Artikelgewichtseinheit verwaltet werden.

### <a name="inbound-warehouse-processing"></a>Eingangslagerortverarbeitung

- Das Empfangen von Ladungsträgern setzt voraus, dass Gewichte während der Registrierung zugeordnet werden, da die Gewichtsinformationen nicht als Teil des Versand-Avis unterstützt werden. Wenn Artikelgewichtsmarkierungs-Prozesse verwendet werden, muss die Markierungsnummer manuell pro Artikelgewichtseinheit zugewiesen werden.
- Eingehende Qualitätsprüfungen werden für Artikelgewichtprodukte nicht unterstützt. Wenn konfiguriert, wird die Qualitätsprüfung übersprungen.

### <a name="inventory-and-warehouse-operations"></a>Bestands- und Lagerortbetrieb

- Das manuelle Erstellen von Quarantäneaufträgen wird für Artikelgewichtsprodukte nicht unterstützt.
- Das manuelle Umlagern von Bestand, der offener Arbeit zugeordnet ist, wird für Artikelgewichtsprodukte nicht unterstützt.
- Ladungsträgerladungen zur Initialisierung des Lagerortbestands werden nicht für Artikelgewichtsprodukte unterstützt.
- Chargenausgleichprozesse werden nicht für Artikelgewichtsprodukte unterstützt.
- Die Handhabung von negativem physischem Bestand wird nicht für Artikelgewichtsprodukte unterstützt.
- Bestandsmarkierungen werden nicht für Artikelgewichtsprodukte unterstützt.

### <a name="outbound-warehouse-processing"></a>Ausgangslagerortverarbeitung

- Die Funktionen zur Clusterkommissionierung werden nicht für Artikelgewichtsprodukte unterstützt.
- Entnahme- und Verpackungs-Lagerortverarbeitungen werden für Artikelgewichtsprodukte nicht unterstützt.
- Für Artikelgewichtsprodukte kann Arbeit, die in einer Arbeitsvorlage definiert ist, nicht automatisch ausgeführt werden.
- Für Artikelgewichtsprodukte unterstützt das System keine manuelle Verpackungsstationsverarbeitung, bei der Entnahmearbeit bei gepackten Containern nach dem Schließen von Containern erstellt wird.
- Die Funktionen zum stückweisen Scannen werden nicht für Artikelgewichtsprodukte unterstützt.

### <a name="production-processing"></a>Produktionsverarbeitung

- Für Artikelgewichtsprodukte werden nur Chargenaufträge für Formelprodukte unterstützt.
- Die Kanban-Funktionen werden nicht für Artikelgewichtsprodukte unterstützt.
- Für Artikelgewichtsprodukte können Seriennummern nicht vor dem Verbrauch registriert werden.
- Die Funktionen zur Stornierung von Ladungsträgern von der Produktion werden nicht für Artikelgewichtsprodukte unterstützt.
- Für Artikelgewichtsprodukte kann die Fertigmeldung nicht nach Seriennummer registriert werden.

### <a name="transportation-management-processing"></a>Transportverwaltungsverarbeitung

- Ladungserstellungsworkbenchverarbeitungen werden für Artikelgewichtsprodukte nicht unterstützt.
- Transportanforderungspositionen werden für Artikelgewichtsprodukte nicht unterstützt.

### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Andere Einschränkungen und Verhaltensweisen für die Artikelgewichtsproduktverarbeitung mit Lagerortverwaltung

- Während der Entnahmeprozesse, in denen der Benutzer nicht aufgefordert wird, Rückverfolgungsangaben zu identifizieren, erfolgt die Gewichts-Zuweisung basierend auf dem Durchschnittsgewicht. Dieses Verhalten tritt auf, wenn z. B. eine Kombination von Rückverfolgungsangaben am gleichen Lagerplatz verwendet wird, und, nachdem ein Benutzer die Entnahme verarbeitet hat, nur ein Rückverfolgungsangabewert am Lagerplatz verbleibt.
- Wenn der Bestand für ein Artikelgewichtsprodukt reserviert wird, das für Lagerortverwaltungsprozesse konfiguriert ist, erfolgt die Reservierung auf Grundlage des Mindestgewichts, das definiert wird, auch wenn diese Menge die letzte verfügbare Handhabungsmenge ist. Dieses Verhalten unterscheidet sich vom Verhalten für Artikel, die nicht für Lagerortverwaltungsprozesse konfiguriert sind. Es gibt eine Ausnahme von dieser Einschränkung. Bei der Produktionskommissionierung wird das tatsächliche Gewicht verwendet, wenn die letzte Handhabungsmenge eines seriennummerngesteuerten Artikelgewichtsprodukts kommissioniert wird.
- Prozesse, die das Gewicht als Teil der Kapazitätsberechnungen verwenden (Wellenschwellenwerte, maximale Arbeitspausen, Container-Höchstwerte, Lagerplatzladekapazitäten usw.), verwenden nicht das tatsächliche Gewicht des Bestands. Stattdessen basieren die Prozesse auf dem physischen Handhabungsgewicht, das für das Produkt definiert wird.
- Die Commerce-Funktion wird in der Regel nicht für Artikelgewichtsprodukte unterstützt.
- Bei Produkten mit Artikelgewicht kann der Lagerstatus von **Lagerstatusänderung** nicht aktualisiert werden.

### <a name="catch-weight-tags"></a>Artikelgewichtsmarkierungen

Ein Artikelgewicht-Tag kann mithilfe eines Warehouse Management Mobile App-Prozesses, manuell im Formular über **Lagerortmanagement > Abfragen und Berichte > Artikelgewicht-Tag** oder mithilfe eines Datenentitätsprozesses erstellt werden. Wenn ein Artikelgewichtstag einer eingehenden Quelldokumentposition zugeordnet wird, z. B. Bestellposition, wird das Tag registriert. Wenn die Zeile für die Ausgangsverarbeitung verwendet wird, wird das Tag im Auslieferungszustand aktualisiert. Sie können alle historischen Registrierungsereignisse für Artikelgewicht-Tags über die Option **Artikelgewicht-Tag-Registrierung** von der Seite **Artikelgewicht-Tag** aus anzeigen.

Du kannst den die Option **Tag erfasstes Gewicht ändern**, um den Gewichtswerts für ein Artikelgewichts-Tag manuell zu aktualisieren. Beachten Sie, dass das Gewicht für den vorhandenen Bestand im Rahmen dieses manuellen Vorgangs nicht angepasst wird. Sie können jedoch problemlos die Seite **Vorliegende Unstimmigkeiten bei Artikeln mit Artikelgewichts-Tags** verwenden, um etwaige Unstimmigkeiten zwischen den derzeit aktiven Artikelgewichts-Tags und dem aktuellen Bestand nachzuschlagen.

Weitere manuelle Optionen sind **Tag registrieren** für eine Quelldokumentposition und **Arbeit registrieren** für bestehende Lagerortarbeit.

Zusätzlich zu den Einschränkungen, die derzeit für Artikelgewichtsprodukte gelten, gelten für Artikelgewichtsprodukte mit Tags weitere derzeit geltende Einschränkungen.

- Alle manuellen Aktualisierungen des Inventars (d. h. Aktualisierungen, die nicht über ein mobiles Gerät durchgeführt werden) müssen entsprechende manuelle Aktualisierungen der zugehörigen Artikelgewichtstags enthalten, da diese Aktualisierungen nicht automatisch durchgeführt werden. Zum Beispiel aktualisieren manuelle Anpassungsjournale das Inventar, nicht jedoch die zugehörigen Artikelgewichtstags.
- Sie müssen die Artikelgewichtstags manuell aktualisieren, um die Bewegungen der Wiederbeschaffungsarbeit widerzuspiegeln. Dies liegt daran, dass das System bei der Wiederbeschaffungsarbeit keine Gewichte erfassen kann und stattdessen das Durchschnittsgewicht erfasst.
- Der Empfang gemischter Ladungsträger wird für mit Tags versehene Gegenstände mit Artikelgewicht nicht unterstützt.
- Die Verarbeitung des Eingangs von Kundenrücksendungen kann Artikelgewichtstags erfassen. Der Prozess überprüft jedoch nicht, ob es sich bei dem zurückgegebenen Tag um das gleiche Tag handelt, das ursprünglich für einen Auftrag geliefert wurde.
- Das Menüelement des Mobilgeräts mit dem Aktivitätscode **Materialverbrauch registrieren** unterstützt derzeit nicht die Aufzeichnung von Artikelgewichtstags.
- Obwohl Zählvorgänge für mit Tags versehene Gegenstände mit Artikelgewicht unterstützt werden, sind sie begrenzt. Beispielsweise können Sie die Optionen für mobile Geräte zum Zählen von mit Tags versehenen Gegenständen mit Artikelgewicht verwenden und das Durchschnittsgewicht wird verwendet. Artikelgewichtstags werden jedoch von der Zähltransaktion nicht automatisch aktualisiert. Nach Abschluss der Zählungstransaktion müssen die Artikelgewichtstags manuell aktualisiert werden, damit sie den Bestand widerspiegeln. Wenn Gegenstände, die sich ursprünglich nicht an einem Ort befanden, zu diesem Ort gezählt werden, wird das Nenngewicht verwendet.
- Die Kennzeichenkonsolidierung unterstützt derzeit keine mit Tags versehenen Gegenstände mit Artikelgewicht.
- Die Funktion zum Stornieren von Arbeit wird für mit Tags versehenene Gegenstände mit Artikelgewicht, die mit Tagnummern rückverfolgt werden, nicht unterstützt.

> [!NOTE]
> Die vorstehenden Informationen zu Artikelgewichtstags sind nur gültig, wenn das Artikelgewichtsprodukt über eine Methode zur Verfolgung der Dimension von Artikelgewichtstags verfügt, die vollständig verfolgt wird (d. h. der Parameter der **Dimensionsrückverfolgungsmethode des Artikelgewichtstags** in der Richtlinie zur Handhabung von Gegenständen mit Artikelgewicht ist auf **Produktdimensionen, Rückverfolgungsangaben und alle Lagerdimensionen** gesetzt). Wenn der Gegenstand mit dem Artikelgewicht nur teilweise mit Tags verfolgt wird (d. h. wenn der Parameter **Dimensionsrückverfolgungsmethode des Artikelgewichtstags** in der Richtlinie zur Handhabung von Gegenständen mit Artikelgewicht auf **Produktdimensionen, Rückverfolgungsangaben und Inventarstatus** gesetzt ist) gelten zusätzliche Einschränkungen. Da in diesem Fall die Sichtbarkeit zwischen Tag und Inventar verloren geht, werden einige zusätzliche Szenarien nicht unterstützt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]