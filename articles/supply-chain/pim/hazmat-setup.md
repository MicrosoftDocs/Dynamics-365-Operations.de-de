---
title: Gefahrengüter einrichten
description: In diesem Thema wird erläutert, wie Sie die Daten einrichten, die zur Klassifizierung von Artikeln als gefährliche Materialien erforderlich sind. Wenn Sie einen Kundenauftrag erstellen, der einen Artikel enthält, der als Gefahrgut eingestuft ist, generiert das System beim Versand eine Gefahrstoffdokumentation für diesen Kundenauftrag.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: b049559b64045e80a40afd99bac30a9cfe1d0580
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428888"
---
# <a name="set-up-hazardous-materials"></a>Gefahrengüter einrichten

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Um die Gefahrstofffunktionalität nutzen zu können, müssen Sie zunächst die Daten einrichten, die zur Klassifizierung von Artikeln als Gefahrgüter erforderlich sind. Wenn Sie dann einen Auftrag erstellen, der einen Artikel enthält, der als Gefahrgut eingestuft ist, generiert das System beim Versand eine Gefahrstoffdokumentation für diesen Kundenauftrag.

## <a name="turn-on-the-hazardous-materials-feature-for-your-system"></a>Aktivieren Sie die Gefahrstofffunktion für Ihr System

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** *Produktinformationsverwaltung*
- **Funktionsname:** *Produktinformationen zu Gefahrstoffen und Versanddokumentation*

## <a name="hazardous-material-regulations"></a>Gefahrstoffvorschriften

Um die Gefahrstoffprozesse nutzen zu können, müssen Sie zunächst eine Vorschrift erstellen. Vorschriften definieren, wie der gedruckte Versandtext für einen Artikel erstellt wird. Sie definieren auch die zugeordneten Lieferarten.

Hier sind einige allgemeine Vorschriften:

- **ADR** – Vorschriften, die sich auf die internationale Beförderung gefährlicher Güter auf dem Landweg beziehen
- **CFR 49** – Vorschriften der Vereinigten Staaten für die Beförderung gefährlicher Güter
- **IMDG** – Der IMDG-Code (International Marine Dangerous Goods)
- **IATA** – Die Gefahrgutbestimmungen der International Air Transport Association (IATA)

Mithilfe diesen Vorschriften können Sie festlegen, welche Informationen angezeigt werden sollen, wenn Sie den Versandtext für einen Artikel drucken. Sie können so viele Vorschriften definieren, wie Sie einhalten müssen.

> [!IMPORTANT]
> Die Funktionalität zum Einrichten von Informationscodes, die sich auf gefährliche Materialien beziehen, macht Ihr Unternehmen nicht konform mit den Vorschriften. Es ist nur ein Tool, mit dem Sie Prozesse für Ihr Unternehmen erstellen können.

In der Regel ist eine Vorschrift für ein bestimmtes Transportmittel verfügbar, z. B. Seefracht, Straßenfracht oder Luftfracht. Daher können Sie jede Vorschrift einer Lieferart zuordnen. Die Lieferart wird verwendet, wenn bestimmte Dokumente in der Lagerverwaltung gedruckt werden. In der Lagerverwaltung ist jede Lieferung mit einem Spediteur und einem Spediteurdienst verknüpft, die im Modul **Transport** eingerichtet sind. Die Lieferart ist dem Spediteur und Spediteurdienst zugeordnet. Wenn Sie einen Bericht ausführen, wird die Lieferart verwendet, um den Versanddrucktext zu finden, der einem zugelassenen Artikel zugeordnet ist.

Diese Einrichtungsdaten sind nicht für jede juristische Person (Unternehmen) spezifisch. Daher können Sie über einen gemeinsamen Satz Gefahrstoffinformationen verfügen, die von allen Ihren juristischen Personen geteilt werden.

Für jede Vorschrift können Sie eine Materialliste definieren und als Vorlagenliste verwenden, die freigegebenen Artikeln zugeordnet ist. Für jede Vorschrift können Sie auch eine Druckeinrichtung definieren. In einer Druckeinrichtung können Sie definieren, wie der Versandtext für einen Artikel erstellt wird. Die Druckeinrichtung wird verwendet, um den Versanddrucktext für einen zugelassenen Artikel zu erstellen.

Um die Vorschriften zu Gefahrstoffen einzurichten, wechseln Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstoffvorschrift**. Auf der Seite **Gefahrstoffvorschrift** können Sie eine beliebige Anzahl von Vorschriften erstellen und diese jeweils konfigurieren, indem Sie die Felder verwenden, die in den folgenden Unterabschnitten beschrieben werden.

### <a name="hazardous-material-regulation-header"></a>Gefahrstoffvorschrift – Kopfzeile

Jede Vorschrift hat einen Code und eine Beschreibung. In der folgenden Tabelle werden die Felder beschrieben, die in der Kopfzeile zur Verfügung stehen.

| Feld | Beschreibung |
|---|---|
| Bestimmungscode | Geben Sie einen Code ein, um den Gefahrstoff-Vorschriftsdatensatz zu identifizieren. |
| Beschreibung | Geben Sie eine Beschreibung der Gefahrstoffvorschrift ein. |

### <a name="print-setup-fasttab"></a>Druckeinrichtung – Inforegister

Jede Vorschrift kann eine beliebige Anzahl von Druckeinrichtungen haben. Sie definieren die Druckeinrichtungen im Inforegister **Druckeinrichtung**. In der folgenden Tabelle werden die Felder beschrieben, die für jede Druckeinrichtung zur Verfügung stehen.

| Feld | Beschreibung |
|---|---|
| Sequenz | Definieren Sie die Reihenfolge, in der Felder im Versandtext referenziert werden. |
| Feld drucken | Wählen Sie das Feld aus, auf das im Versandtext verwiesen werden soll. Nicht alle Felder für das Gefahrgut können gedruckt werden. Es sind nur die allgemeinen Felder verfügbar, die zur Definition des Versandtextes in den verschiedenen Vorschriften verwendet werden. Sie sollten das erste Druckfeld als Feldtrennzeichen mit einem definieren **Reihenfolge**-Wert von *0* (Null) definieren, damit es als Trennzeichen zwischen anderen Feldern verwendet werden kann. Es ist nur ein Verweis auf das Feldtrennzeichen erforderlich.<p>Folgende Werte sind verfügbar:</p><ul></li><li>**Feldtrennzeichen** – Dieses Druckfeld wird als Feldtrennzeichen für den Text verwendet. Es ist nur ein Feldtrennzeichen in der Sequenz erforderlich. Normalerweise sollten Sie den Wert **Sequenz** für dieses Druckfeld auf *0* (Null) festlegen. Das System sucht nach einem Feldtrennzeichen und verwendet das erste, das es in der Liste findet. Der in der Zeichenfolge verwendete Textwert stammt aus dem Feld **Drucken nach**.</li><li>**Kennung** – Bei diesem Druckfeld wird der [Identifizierungscode und/oder Beschreibung](#identification) in den Drucktext gesetzt.</li><li>**Klasse** – Bei diesem Druckfeld wird der [Klassencode und/oder Beschreibung](#classes) in den Drucktext gesetzt.</li><li>**Sparte** – Bei diesem Druckfeld wird der [Spartencode und/oder Beschreibung](#divisions) in den Drucktext gesetzt.</li><li>**Verpackungsgruppe** – Bei diesem Druckfeld wird der [Verpackungsgruppencode und/oder Beschreibung](#packing-group) in den Drucktext gesetzt.</li><li>**Tunnelcode und/oder Beschreibung** – Bei diesem Druckfeld wird der [Tunnelcode und/oder Beschreibung](#tunnel) in den Drucktext gesetzt.</li><li>**Richtiger Versandname** – Bei diesem Druckfeld wird der [richtige Versandname](hazmat-items.md#hazmat-description) in den Drucktext gesetzt.</li><li>**Technischer Name** – Bei diesem Druckfeld wird der [technische Name und/oder Beschreibung](#technical-name) in den Drucktext gesetzt.</li><li>**Transportkategorie** – Bei diesem Druckfeld wird der [Transportkategoriecode und/oder Beschreibung](#transport-category) in den Drucktext gesetzt.</li><li>**Verstauung** – Bei diesem Druckfeld wird der [Verstauungscode und/oder Beschreibung](#stowage) in den Drucktext gesetzt.</li><li>**Fester Text** – Dieses Druckfeld gibt den Text ein, der im Feld **Fester Text** für diese Zeile definiert ist.</li><li>**Etikettcode und/oder Beschreibung** – Bei diesem Druckfeld wird der [Etikettcode und/oder Beschreibung](#label) in den Drucktext gesetzt.</li><li>**Luftfrachtverpackung** – Bei diesem Druckfeld wird der [Luftfrachtverpackunganleitungs-Code und/oder Beschreibung](#packing-instruction) in den Drucktext gesetzt.</li><li>**Begrenzte Menge** – Dieses Druckfeld prüft, ob der Artikel als [Artikel in begrenzter Menge](hazmat-items.md#material-management) gekennzeichnet ist und wenn dies der Fall ist, gibt es den Text ein, der im Feld **Fester Text** für diese Zeile definiert ist.</li><li>**Verpackungsbeschreibung** – Bei diesem Druckfeld wird die [Verpackungsbeschreibung](#packing-description) in den Drucktext gesetzt.</li></ul> |
| Drucken vor | Geben Sie den Text ein, der vor dem Inhalt gedruckt werden soll, der durch die Einstellung **Feld drucken** definiert ist. |
| Drucken nach | Geben Sie den Text ein, der nach dem Inhalt gedruckt werden soll, der durch die Einstellung **Feld drucken** definiert ist. |
| Mit Vorherigen drucken | Aktivieren Sie dieses Kontrollkästchen, um zu verhindern, dass das Feldtrennzeichen zwischen dem vorherigen Feld und diesem Feld gedruckt wird. Verwenden Sie dieses Kontrollkästchen für Druckfelder, die entweder optional sind oder in einem anderen Druckfeld enthalten sind. |
| Fester Text | Wenn Sie das Feld **Feld drucken** auf **Fester Text** oder **Begrenzte Menge** festlegen, geben Sie den Text ein, der gedruckt werden soll. |
| In Druck einbeziehen | Wählen Sie aus, welcher Wert oder welche Werte aus dem ausgewählten Druckfeld für diese Zeile gedruckt werden sollen. Sie können den Code, die Beschreibung oder sowohl den Code als auch die Beschreibung drucken. |

### <a name="mode-of-delivery-fasttab"></a>Lieferart – Inforegister

Die Vorschrift ist eine freigegebene Tabelle und ist nicht für jede juristische Person spezifisch. Lieferarten sind jedoch spezifisch für jede juristische Person. Wenn Sie daher eine Lieferart einrichten, müssen Sie die Beziehung zwischen der Vorschrift, der juristischen Person und der Lieferart auswählen.

In der folgenden Tabelle werden die Felder beschrieben, die im Inforegister **Lieferart** verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Firma | Wählen Sie eine juristische Person aus, die dieser Vorschrift zugeordnet werden soll. |
| Lieferart | Wählen Sie basierend auf der von Ihnen ausgewählten juristischen Person die Lieferart aus, die mit der Vorschrift verknüpft werden soll. |

### <a name="country-fasttab"></a>Land – Inforegister

Zu Referenzzwecken können Sie die Länder oder Regionen auflisten, für die die Vorschrift relevant ist. Wenn jedoch Lieferberichte ausgeführt werden, wird nur die Lieferart verwendet, um die Vorschrift zu bestimmen. Wenn Sie eine Lagerlieferung überprüfen, gibt es keine direkte Verknüpfung zur Lieferart. Die Lieferung kann einem Spediteur und einem Spediteurdienst zugeordnet werden. Wenn Sie einen Spediteurdienst definieren, müssen Sie ihn der Lieferart zuordnen. Diese Beziehung wird in Versandberichten wie dem Frachtbrief verwendet, um den Versanddrucktext für einen Artikel zu finden.

In der folgenden Tabelle wird das Feld beschrieben, das im Inforegister **Land** verfügbar ist.

| Feld | Beschreibung |
|---|---|
| Land/Region | Wählen Sie ein Land/Region aus, um es der Vorschrift zuzuordnen. |

## <a name="material-codes"></a><a name="hazmat-codes"></a>Materialcodes

Materialcodes legen Einstellungen fest, die sich auf eine bestimmte gefährliche Komponente beziehen, die in einem zugelassenen Produkt enthalten sein kann. Jeder Materialcode gehört zu einer bestimmten Gefahrstoffvorschrift, und seine Definition muss dieser Vorschrift entsprechen. Wenn Sie einen Materialcode auf ein zugelassenes Produkt anwenden, indem Sie das Feld **Materialcode** verwenden, werden die Einstellungen für Gefahrstoffe des Materialcodes autoamtisch auf dieses Produkt angewendet. Daher ist das Einrichten zugelassener Produkte schneller und weniger fehleranfällig.

Befolgen Sie diese Schritte, um Ihre Gefahrstoffdefinitionen zu verwalten.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstoffvorschrift**.
2. Wählen Sie die Vorschrift aus, für die eine Gefahrstoffdefinition erstellt werden soll.
3. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Setup** die Option **Gefahrstoffe** aus.
4. Im Feld **Materialcode** geben Sie einen Materialcode für die Gefahrstoffdefinition ein. Sie wählen diesen Wert aus, wenn Sie den Materialcode auf ein zugelassenes Produkt anwenden.

    Das Feld **Vorschriftscode** ist schreibgeschützt und zeigt die Vorschrift an, die Sie in Schritt 2 ausgewählt haben.

5. Verwenden Sie die verbleibenden Felder auf dieser Seite, um jeden Gefahrstoff zu erstellen und einzurichten, das für Ihre ausgewählte Vorschrift gilt. Die verfügbaren Felder sind eine Teilmenge der Gefahrstofffelder, die für einzelne zugelassene Produkte verfügbar sind. Weitere Informationen finden Sie unter [Gefahrstoffe in Produkten, Aufträgen, Lieferungen und Ladungen](hazmat-items.md).

## <a name="hazardous-material-classification-groups"></a><a name="classification-groups"></a>Gefahrstoffklassifizierungsgruppen

Jede Gefahrstoffklassifizierungsgruppe definiert eine Gruppe von Feldwerten, die eine Vorlage erstellen. Sie können diese Vorlage später verwenden, wenn Sie Gefahrstoffinformationen für einen zugelassenen Artikel einrichten.

Wenn Sie den Code für eine Gefahrstoffklassifizierungsgruppe einem zugelassenen Artikel zuweisen, werden die Informationen, die dieser Klassifizierungsgruppe zugeordnet sind, in die entsprechenden Felder des Artikels kopiert. Daher können Sie die Einrichtungsprozesse vereinfachen, indem Sie eine Reihe zusammengehöriger Feldwerte erstellen, die Sie häufig zusammen verwenden.

Diese Einrichtungsdaten sind nicht für jede juristische Person spezifisch. Daher können Sie über einen gemeinsamen Satz Gefahrstoffinformationen verfügen, die von allen Ihren juristischen Personen geteilt werden.

Um die Klassifizierungsgruppen zu Gefahrstoffen einzurichten, wechseln Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstoff-Klassifizierungsgruppe**. Auf der Seite **Gefahrstoff-Klassifizierungsgruppe** können Sie eine beliebige Anzahl von Gruppen erstellen und diese jeweils konfigurieren, indem Sie die Felder verwenden, die in der folgenden Tabelle beschrieben werden.

| Feld | Beschreibung |
|---|---|
| Gruppencode | Geben Sie einen Code zum Identifizieren der Gruppe ein. |
| Beschreibung | Geben Sie eine Beschreibung der Gruppe ein. |
| Klassencode | Ordnen Sie der Gruppe einen [Klassencode](#classes) für Gefahrstoffe zu. |
| Spartencode | Ordnen Sie der Gruppe einen [Spartencode](#divisions) für Gefahrstoffe zu. |
| Verpackungsgruppencode | Ordnen Sie der Gruppe ein [Verpackungsgruppencode](#packing-group) zu. |
| Transportkategoriecode | Ordnen Sie der Gruppe ein [Transportkategoriecode](#transport-category) zu. |
| Multiplikator | Geben Sie den Gefahrstoffmultiplikator ein, der für die ausgewählte Klasse und Aufteilung der Gefahrstoffe gemäß den geltenden Vorschrift gilt. Dieser Multiplikator wird als Teil der Formel verwendet, die die Summe der *Gefahrstoffpunkte* berechnet, die in einer Ladung oder Lieferung enthalten sind. Weitere Informationen zu Gefahrstoffpunkten und diesem Multiplikator finden Sie unter [Materialverwaltung – Inforegister](hazmat-items.md#material-management). |

## <a name="hazardous-material-classes"></a><a name="classes"></a>Gefahrstoffklassen

Eine Gefahrstoffklasse wird normalerweise der Liste von Klassen zugeordnet, die in der Vorschrift enthalten sind, der Sie entsprechen. Beispielsweise listet die US-Verordnung CFR 49 „Klasse 3“ als entflammbare und brennbare Flüssigkeiten auf. Sie können die Klassen einrichten, die für die Materialien relevant sind, die Sie klassifizieren müssen.

Jede Klasse wird einer Materialeinrichtung in der Materialliste zugeordnet, die sich auf die Vorschrift bezieht. Sie weisen jedem zugelassenen Artikel nach Bedarf eine Klasse zu, um die Gefährlichkeit eines Produkts zu beschreiben.

Diese Einrichtungsdaten sind nicht für jede juristische Person spezifisch. Daher können Sie über einen gemeinsamen Satz Gefahrstoffinformationen verfügen, die von allen Ihren juristischen Personen geteilt werden.

Gefahrstoffklassen wirken auf folgende Weise mit Abteilungen, Gruppen und Kompatibilitätsgruppen zusammen:

- Wenn Sie einem zugelassenen Artikel eine Gefahrstoffklasse zuordnen, müssen Sie auch eine [Gefahrstoffsparte](#divisions) zuweisen.
- Sie können Gefahrstoffklassen zusammen mit [Gefahrstoffklassifizierungsgruppen](#classification-groups) verwenden, um eine Vorlage von Codes zu erstellen, um Artikel einzurichten.
- Sie können [Gefahrstoffkompatibilitätsgruppen](#compatibility-groups) verwenden, um festzustellen, welche Gefahrstoffklassen und Sparten zusammen versendet werden können.

Um Gefahrstoffklassen einzurichten, wechseln Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstoffklasse**. Auf der Seite **Gefahrstoffklasse** können Sie eine beliebige Anzahl von Klassen erstellen und diese jeweils konfigurieren, indem Sie die Felder verwenden, die in der folgenden Tabelle beschrieben werden.

| Feld | Beschreibung |
|---|---|
| Klassencode | Geben Sie einen Code zum Identifizieren dieser Klasse ein. Sie definieren diesen Code für den Artikel. Es wird dann in Suchlisten verwendet, wenn Sie einem zugelassenen Artikel eine Gefahrstoffklasse zuweisen. |
| Beschreibung | Geben Sie eine Beschreibung der Klasse ein. |

## <a name="hazardous-material-divisions"></a><a name="divisions"></a>Gefahrstoffsparten

Eine Gefahrstoffsparte ist eine Teilmenge einer Gefahrstoffklasse. Sie müssen jedem Produkt, das gefährliche Materialien enthält, sowohl eine Sparte als auch eine Klasse zuweisen.

Erstellen Sie für Klassen ohne Sparten eine Sparte, in der sich der Code *0* befindet. Beispielsweise haben radioaktive Materialien der Klasse 7 in der IATA-Verordnung keine Untersparten. In diesem Fall erstellen Sie eine Sparte *0*, die Sie einem zugelassenen Produkt zuordnen können, wenn Sie die Klasse zuweisen.

Diese Einrichtungsdaten sind nicht für jede juristische Person spezifisch. Daher können Sie über einen gemeinsamen Satz Gefahrstoffinformationen verfügen, die von allen Ihren juristischen Personen geteilt werden.

Gefahrstoffsparten wirken auf folgende Weisen mit Klassen, Gruppen und Kompatibilitätsgruppen zusammen:

- Wenn Sie einem zugelassenen Artikel eine Gefahrstoffsparte zuordnen, müssen Sie auch eine [Gefahrstoffklasse](#classes) zuweisen.
- Sie können Gefahrstoffsparten zusammen mit [Gefahrstoffklassifizierungsgruppen](#classification-groups) verwenden, um eine Vorlage von Codes zu erstellen, um Artikel einzurichten.
- Sie können [Gefahrstoffkompatibilitätsgruppen](#compatibility-groups) verwenden, um festzustellen, welche Gefahrstoffklassen und Sparten zusammen versendet werden können.

Um Gefahrstoffsparten einzurichten, wechseln Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstoffsparte**. Auf der Seite **Gefahrstoffsparte** können Sie eine beliebige Anzahl von Sparten erstellen und diese jeweils konfigurieren, indem Sie die Felder verwenden, die in der folgenden Tabelle beschrieben werden.

| Feld | Beschreibung |
|---|---|
| Division | Geben Sie einen Code ein, der als Referenznummer für die Sparte verwendet werden soll. |
| Beschreibung | Geben Sie eine Beschreibung der Sparte ein. |
| Klasse  | Suchen Sie nach der Klasse, zu der die Sparte gehört, und weisen Sie sie zu. |

## <a name="hazardous-material-compatibility-groups"></a><a name="compatibility-groups"></a>Gefahrstoffkompatibilitätsgruppen

Gefahrstoffkompatibilitätsgruppen bestimmen, welche Gefahrstoffklassen und Sparten zusammen versendet werden können. Wenn Bediener Lagerladungen oder Lieferungen erstellen, können sie eine Kompatibilitätsprüfung durchführen, die eine Warnung ausgibt, wenn die Ladung oder Lieferung Artikel enthält, die nicht alle zur gleichen Kompatibilitätsgruppe gehören.

Diese Einrichtungsdaten sind nicht für jede juristische Person spezifisch. Daher können Sie über einen gemeinsamen Satz Gefahrstoffinformationen verfügen, die von allen Ihren juristischen Personen geteilt werden.

Um die Kompatibilitätsgruppen zu Gefahrstoffen einzurichten, wechseln Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstoffvorschrift-Kompatibilitätsgruppe**. Auf der Seite **Gefahrstoff-Kompatibilitätsgruppe** können Sie eine beliebige Anzahl von Kompatibilitätsgruppen erstellen und diese jeweils konfigurieren, indem Sie die Felder verwenden, die in den folgenden Unterabschnitten beschrieben werden.

### <a name="hazardous-material-compatibility-group-header"></a>Gefahrstoffkompatibilitätsgruppen-Kopfzeile

Jede Kompatibilitätsgruppe hat einen Code und eine Beschreibung. In der folgenden Tabelle werden die Felder beschrieben, die in der Kopfzeile zur Verfügung stehen.

| Feld | Beschreibung |
|---|---|
| Kompatibilitätsgruppe | Geben Sie einen Code zum Identifizieren der Kompatibilitätsgruppe ein |
| Beschreibung | Geben Sie eine Beschreibung der Kompatibilitätsgruppe ein. |

### <a name="compatibility-group-details"></a>Kompatibilitätsgruppendetails

Jede Kompatibilitätsgruppe legt eine Liste von Klassen und Sparten von Gefahrstoffen fest, die zusammen versendet werden können.

| Feld | Beschreibung |
|---|---|
| Klasse  | Wählen Sie eine Gefahrstoffklasse aus, die mit allen anderen Klassen in der Gruppe kompatibel ist. |
| Division | Wählen Sie eine Gefahrstoffsparte aus, die zur ausgewählten Klasse gehört. |

## <a name="hazardous-material-specification-values"></a>Werte der Gefahrstoffspezifikation

Microsoft Dynamics 365 Supply Chain Management stellt verschiedene Typen von Gefahrstoffspezifikationen bereit. Für jeden Typ müssen Sie für jedes relevante Feld einen zentralen Wertesatz einrichten. Benutzer können dann unter diesen Werten auswählen, wenn sie Gefahrstoffdefinitionen oder zugelassene Produkte konfigurieren. Supply Chain Management bietet eine Sammlung von Seiten, auf denen Sie die Werte bestimmen können. Jede Seite ist einem Spezifikationstyp zugeordnet. Eine Beschreibung der verfügbaren Spezifikationen und Informationen zum Festlegen der dafür verfügbaren Werte finden Sie in den folgenden Unterabschnitten.

Ein Beispiel für eine Gefahrstoffspezifikation ist der _Verstauungscode_, der angibt, wie ein bestimmtes Material während des Transports verstaut werden kann. Mithilfe der Informationen in diesem Abschnitt erstellen Sie eine zentrale Sammlung von Verstauungscodes. Diese Sammlung wird dann den Benutzern in einer Dropdownliste angezeigt, wenn sie den Verstauungscode für ein zugelassenes Produkt festlegen.

Diese Gefahrstoffspezifikationswerte sind nicht für jede juristische Person spezifisch. Daher können Sie eine Reihe gemeinsamer Werte verwenden, die von allen Ihren juristischen Personen gemeinsam genutzt werden.

Sie verwenden [Materialcodes](#hazmat-codes), um allgemeine Sammlungen von Einstellungen für jede Spezifikation zu erstellen, wie sie für eine bestimmte Vorschrift gelten. Sie können dann bei Bedarf den entsprechenden Code auf jedes zugelassene Produkt anwenden. Informationen über die Vorgehensweise zum Anwenden eines Gefahrstoffcodes auf ein bestimmtes zugelassenes Produkt und zum Konfigurieren einzelner Einstellungen dieses Produkts für die hier beschriebenen Spezifikationen finden Sie unter [Gefahrstoffe in Produkten, Bestellungen, Lieferungen und Ladungen](hazmat-items.md).

### <a name="hazardous-material-emergency-response"></a>Gefahrengüter-Notrufmaßnahmen

Die Spezifikation *Notfallreaktion bei Gefahrstoffen* gibt an, was zu tun ist, wenn beim Transport eines Produkts, das ein bestimmtes gefährliches Material enthält, etwas schief geht.

Um Werte für diese Spezifikation einzurichten, gehen Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstoff-Notfallreaktion**. Auf der Seite **Notfallreaktion bei Gefahrstoffen** können Sie eine beliebige Anzahl von Werten erstellen und diese mit einem Klassifizierungscode und einer kurzen Beschreibung konfigurieren.

### <a name="hazardous-material-identification"></a><a name="identification"></a>Gefahrengüterkennung

Die Spezifikation *Gefahrstoffkennung* identifiziert die Klasse oder Art eines Gefahrstoffs. Der Wert ist normalerweise ein Code, der auf dem Standard der Vereinten Nationen (UN) beruht. Jede Klasse wird durch einen Code und eine Beschreibung identifiziert und kann die Transportmethoden einschränken. Um beispielsweise einen entflammbaren Artikel oder Material zu identifizieren, erstellen Sie eine Gefahrstoffklasse, die den Code *FL* verwendet sowie die Beschreibung *Entflammbar*. Sie geben außerdem an, dass die Klasse nicht auf dem Luftweg transportiert werden darf.

Um Werte für diese Spezifikation einzurichten, gehen Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstoffkennung**. Auf der Seite **Gefahrstoffkennung** können Sie eine beliebige Anzahl von Werten erstellen und diese jeweils konfigurieren, indem Sie die Felder verwenden, die in der folgenden Tabelle beschrieben werden.

| Feld | Beschreibung |
|---|---|
| Kennung | Geben Sie einen Code ein, der als Referenznummer verwendet werden soll, um diese Klasse als Gefahrstoff zu identifizieren. |
| Beschreibung | Geben Sie eine Beschreibung dieser Klasse ein. |
| Vom Lufttransport einschränken | Aktivieren Sie dieses Kontrollkästchen, um anzuzeigen, dass diese Gefahrgstoffklasse nicht auf dem Luftweg transportiert werden darf. |
| Vom Seetransport einschränken | Aktivieren Sie dieses Kontrollkästchen, um anzuzeigen, dass diese Gefahrgstoffklasse nicht auf dem Seeweg transportiert werden darf. |

### <a name="hazardous-material-label"></a><a name="label"></a>Gefahrengüterbeschriftung

Die Spezifikation *Gefahrstoffetikett* identifiziert das Gefahrgutetikett, das auf den relevanten zugelassenen Produkten angebracht werden muss. Die Etiketten selbst beschreiben, wie mit dem Produkt umgegangen werden soll. Zum Beispiel haben Sie ein Produkt, das ein giftiges Gas enthält. In diesem Fall richten Sie einen Etikettencode ein, der das Giftgasetikett darstellt. Sie bauen Ihren Geschäftsprozess auch so auf, dass er diesen Wert beim Versand von Produkten nachschlägt.

Um Werte für diese Spezifikation einzurichten, gehen Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstoffetikett**. Auf der Seite **Gefahrstoffetikett** können Sie eine beliebige Anzahl von Etiketten erstellen und diese jeweils mit einem identifizierenden Code und einer kurzen Beschreibung konfigurieren.

### <a name="hazardous-material-packing-descriptions"></a><a name="packing-description"></a>Gefahrengüter-Verpackungsbeschreibungen

Die Spezifikation *Beschreibungen der Gefahrstoffverpackung* gibt an, wie ein gefährlicher Artikel verpackt werden muss. Beispielsweise muss es möglicherweise in einer bestimmten Art von Stahltrommel oder einer anderen Art von Spezialverpackung verpackt werden.

Um Werte für diese Spezifikation einzurichten, gehen Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstoff-Verpackungsbeschreibungen**. Auf der Seite **Gefahrstoff-Verpackungsbeschreibungen** können Sie eine beliebige Anzahl von Verpackungsbeschreibungen erstellen und diese jeweils mit einem identifizierenden Code und einer kurzen Beschreibung konfigurieren.

### <a name="hazardous-material-packing-group"></a><a name="packing-group"></a>Gefahrengüter-Verpackungsgruppe

Die Spezifikation *Gefahrstoff-Verpackungsgruppe* identifiziert die Verpackungsgruppe für einen gefährlichen Artikel. Anhand der Verpackungsgruppe können Sie einen Code und eine Beschreibung definieren, um anzugeben, wie Gefahrgutartikel während des Transports oder der Lieferung verpackt werden müssen. Die Verpackungsgruppe wird dem Artikel über die Seite **Artikelgefahrstoffe** zugewiesen.

Um Werte für diese Spezifikation einzurichten, gehen Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstoff-Verpackungsgruppe**. Auf der Seite **Gefahrstoff-Verpackungsgruppe** können Sie eine beliebige Anzahl von Verpackungsgruppen erstellen und diese jeweils mit einem identifizierenden Code und einer kurzen Beschreibung konfigurieren.

### <a name="hazardous-material-packing-instruction"></a><a name="packing-instruction"></a>Gefahrengüter-Verpackungsanweisung

Die Spezifikation *Gefahrstoff-Verpackungsanweisung* identifiziert Verpackungsanweisungen, die befolgt werden müssen, wenn ein bestimmter gefährlicher Artikel für den Transport auf dem Luftweg vorbereitet wird.

Um Werte für diese Spezifikation einzurichten, gehen Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstoff-Verpackungsanweisung**. Auf der Seite **Gefahrstoff-Verpackungsanweisung** können Sie eine beliebige Anzahl von Verpackungsanweisungsbezeichnern erstellen und diese jeweils mit einem identifizierenden Code und einer kurzen Beschreibung konfigurieren.

### <a name="hazardous-material-stowage"></a><a name="stowage"></a>Gefahrengüterverladung

Die Spezifikation *Gefahrstoffverstauung* gibt an, wie ein Produkt auf einem Schiff gelagert werden muss, wenn es per Seefracht transportiert wird.

Um Werte für diese Spezifikation einzurichten, gehen Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstoffverstauung**. Auf der Seite **Gefahrstoffverstauung** können Sie eine beliebige Anzahl von Verstauungsbezeichnern erstellen und diese jeweils mit einem identifizierenden Code und einer kurzen Beschreibung konfigurieren.

### <a name="hazardous-material-transport-category"></a><a name="transport-category"></a>Gefahrengütertransport-Kategorie

Die Spezifikation *Gefahrgut-Transportkategorie* wird normalerweise verwendet, um ähnliche gefährliche Produkte in Berichten zu gruppieren. Beispielsweise werden Transportkategorien im Bericht **Lieferungsübersicht** verwendet, den Sie aus dem Lagerversand-Datensatz ausdrucken können.

Um Werte für diese Spezifikation einzurichten, gehen Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstoff-Transportkategorie**. Auf der Seite **Gefahrstoff-Transportkategorie** können Sie eine beliebige Anzahl von Transportkategorien erstellen und diese jeweils mit einem Anzeigename und einer kurzen Beschreibung konfigurieren.

### <a name="hazardous-material-technical-name"></a><a name="technical-name"></a>Technischer Name für Gefahrengüter

Die Spezifikation *Technischer Name des Gefahrstoffs* kann verwendet werden, um einen häufig verwendeten oder internen Firmennamen bereitzustellen, der jedes Material beschreibt.

Um Werte für diese Spezifikation einzurichten, gehen Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Technischer Name des Gefahrstoffs**. Auf der Seite **Technischer Name des Gefahrstoffs** können Sie eine beliebige Anzahl technischer Namen erstellen und diese jeweils mit einem Anzeigename und einer kurzen Beschreibung konfigurieren.

### <a name="hazardous-material-tunnel"></a><a name="tunnel"></a>Gefahrengütertunnel

Die Spezifikation *Gefahrstofftunnel* begrenzt die Arten von Tunneln, durch die ein gefährliches Material transportiert werden kann, indem die Arten von Tunneln identifiziert werden, die verwendet werden müssen. Tunnelkategorien werden durch geltende Vorschriften für den Gefahrguttransport festgelegt. Diese Spezifikation gilt normalerweise nur für den Straßentransport.

Um Werte für diese Spezifikation einzurichten, gehen Sie zu **Produktinformationsverwaltung \> Setup \> Gefahrstoff-Versanddokumentation \> Gefahrstofftunnel**. Auf der Seite **Gefahrstofftunnel** können Sie eine beliebige Anzahl von Tunnelbezeichnern erstellen und diese jeweils mit einem identifizierenden Code und einer kurzen Beschreibung konfigurieren.
