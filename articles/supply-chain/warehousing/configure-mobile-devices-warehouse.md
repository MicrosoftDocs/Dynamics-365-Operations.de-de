---
title: Mobile Geräte für Lagerarbeiten einrichten
description: In diesem Thema wird beschrieben, wie Menüoptionen konfiguriert werden, die Arbeitskräfte zum Ausführen von Arbeit auf einem mobilen Gerät verwenden.
author: Mirzaab
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFSysDirSort, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: 29941
ms.assetid: 6dff6313-dc6e-4f06-9c0c-dab24eefe4da
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9e0f27839d9e6330cc8a11874a5cb1786daf8dc
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902178"
---
# <a name="set-up-mobile-devices-for-warehouse-work"></a>Mobile Geräte für Lagerarbeiten einrichten

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Menüoptionen konfiguriert werden, die Arbeitskräfte zum Ausführen von Arbeit auf einem mobilen Gerät verwenden.

> [!NOTE]
> Dieser Artikel gilt für Funktionen im Modul „Lagerortverwaltung“. Er gilt nicht für Funktionen im Modul "Lagerverwaltung". Die Menüoptionen, die in den Menüs eines Mobilgeräts in einem Lagerort angezeigt werden, werden auf der Seite **Menüelemente des mobilen Geräts** konfiguriert. Da die Menüelemente in unterschiedliche Menüs einbezogen werden können, ist es einfach, Menüstrukturen zu konfigurieren, sodass nur bestimmte Typen von Arbeit für bestimmte Benutzer verfügbar gemacht werden. Sie können Menüelemente so konfigurieren, dass Sie folgende Aufgaben ausführen:

- Verarbeiten einer Abfrage oder Ausführen einer Aktivität, z. B. Drucken einer Beschriftung, Generieren von Kennzeichennummern, Starten eines Produktionsauftrags oder schnelles Suchen nach Informationen zu Artikeln in einem Lagerplatz.
- Erstellen Sie Arbeit, die durch einen anderen Prozess ausgeführt wird. Beispielsweise kann das Empfangen eines Artikels für eine Bestellung Einlagerungsarbeit für einen anderen Arbeiter erzeugen.
- Führen Sie Arbeit aus, die von einem anderen Prozess (vorhandene Arbeit) erstellt wurde, beispielsweise Einlagerungsarbeit für einen Artikel, der für eine Bestellung eingegangen ist.

Um eine Menüoption für eine Aktivität oder eine Abfrage zu erstellen, legen Sie das **Modus** Feld auf **Indirekt** fest. Eine Liste von **Aktivitätscode** Optionen wird dann verfügbar, damit Sie den Typ der Abfrage oder die Aktivität auswählen können, dass die Menüoption dafür ist. Um eine Menüoption zu erstellen um Lagerortarbeit zu generieren, legen Sie das Feld **Modus** auf **Arbeit** fest. Eine Liste von **Arbeitserstellungsprozessen** wird dann verfügbar. Um eine Menüoption zur Verarbeitung vorhandener Lagerortarbeit zu erstellen , legen Sie das Feld **Modus** auf **Work** fest, und legen Sie dann die Option **Vorhandene Arbeit verwenden** auf **Ja** fest. 

> [!NOTE]
> Abhängig vom Modus, den Sie für die Menüoption auswählen, und ob das Menüelement verwendet wird, um vorhandene Arbeit auszuführen, sind zusätzliche Felder für die Menüoption verfügbar. Informationen zu den zusätzlichen Feldauswahlen finden Sie im Abschnitt „Zusätzliche Menüelementoptionen“ in diesem Thema weiter unten.

## <a name="configure-menu-items-for-activities-and-inquiries"></a>Konfigurieren von Menüelementen für Aktivitäten und Abfragen

Wenn das Feld **Modus** für eine Menüoption auf **Indirekt** festgelegt ist, können Sie eine Menüoption erstellen, um eine allgemeine Aktivität oder eine Abfrage auszuführen, die keine Arbeit erstellt. Die Beispiele umfassen Aktivitäten, wie das erneute Drucken von Ladungsträgerbeschriftungen, und eine Abfrage zu den Artikel in einem Lagerplatz. In der folgenden Tabelle sind die Optionen aufgelistet, die zur Verfügung stehen.

| Mit der folgenden Option... | Beschreibung |
|---|---|
| Keine | Dieser Standardwert aktiviert keine Aktivität oder Abfrage. |
| Info | Hier werden Informationen zum System angezeigt, wie die Versionsnummer, die Lagerortkennung und die Arbeitskraft, die momentan angemeldet ist. |
| Lagerort ändern | Ändern Sie den Lagerort, an dem eine Arbeitskraft angemeldet ist. |
| Lagerplatzanfrage | Hier werden Informationen zu allen Artikel und Mengen für einen Lagerplatz angezeigt. |
| Ladungsträgeranfrage | Hier wird die Menge von Artikeln auf einem Ladungsträger und der Ort des Ladungsträgers angezeigt. |
| Produktionsauftrag starten | Starten Sie einen Produktionsauftrag. |
| Produktionsausschuss | Geben Sie die Menge des Ausschussmaterials ein, der während der Produktion für jede Stücklistenposition erstellt wurde. |
| Letzte Palette der Produktion | Geben Sie an, dass die letzte Palette von Artikeln für einen Produktionsauftrag produziert wurde und dass der Status des Produktionsauftrags als **Fertig gemeldet** aktualisiert werden muss. Der Status der Rohmaterialien, die nicht während der Produktion verbraucht wurden, wird von **Entnommen** auf **In Auftrag** zurückgesetzt, und die Artikel können in den Bestand zurückgesendet werden. |
| Artikelabfrage | Scannen Sie einen Artikel, um zu bestimmen, wo er sich im Lagerort befindet. Die Abfrage gibt alle Standorte und Mengen für den gescannten Artikel zurück. |
| Etikett erneut drucken | Drucken Sie eine Ladungsträgerbeschriftung erneut. |
| Ladungsträgererstellung | Erstellen Sie einen übergeordneten Ladungsträger, indem Sie mehrere Ladungsträger am gleichen Lagerort kombinieren. Diese Option ist nützlich, wenn Sie mehrere Ladungsträger gleichzeitig verschieben. Nachdem der übergeordnete Ladungsträger verschoben wurde, müssen Sie eine Ladungsträgerauflösung durchführen, bevor Sie Artikel für jeden Ladungsträger auswählen können. <p></p>**Tipp:** Wenn Sie einen übergeordneten Ladungsträger verschieben möchten, müssen Sie ein mobiles Gerät verwenden, das konfiguriert ist, um Arbeit für Bewegungen zu erstellen. |
| Ladungsträgerauflösung | Lösen Sie einen Ladungsträger aus, sodass Sie Artikel aus den Ladungsträgern entnehmen können, die sich im Build befanden. |
| Einchecken durch Fahrer | Wenn Sie Transportverwaltung verwenden, registrieren Sie die Ankunft eines Fahrers, indem sie die ausgehende Ladungskennung, Terminkennung oder Lieferkennung scannen. Diese Option setzt voraus, dass dem Termin eine Ladung zugewiesen wurde und dass der Status der Ladung **Geladen** ist. |
| Auschecken durch Fahrer | Erfassen, dass ein Fahrer den Termin abgeschlossen hat. |
| Nummernkreis-Cache entleeren | Löschen Sie die Nummernkreisnummern aus dem Nummernkreiscache. Diese Aktivität wird normalerweise von einem Systemadministrator durchgeführt, um Zwischenspeicherprobleme zu beheben, wenn mobile Geräte verwendet werden. |
| Chargendisposition ändern | Ermöglichen Sie einer Arbeitskraft, einen Chargendispositionscode für einen Artikel und eine Charge anzugeben. Diese Auswahl aktualisiert den Dispositionscode, der für die Charge angegeben ist. |
| Offene Arbeitsliste anzeigen | Hier wird einem bestimmten Benutzer eine Liste der verfügbaren Arbeit angezeigt. Der Benutzer kann dann auszuführende Arbeit auswählen und wird auf diese verwiesen. Diese Liste ist für die Anzeige auf Tabletgeräten mit einer Bildschirmgröße von 7 Zoll oder mehr bestimmt. Wenn Sie diese Option auswählen, werden die Menüelemente **Abfrage bearbeiten** und **Feldliste** verfügbar. Auf der Seite **Abfrage bearbeiten** können Sie Kriterien für die Arbeit einrichten, die in der Liste angezeigt wird. Auf der Seite **Feldliste** können Sie auswählen, welche Felder in der Arbeitsliste angezeigt werden. Sie können beispielsweise die Anzahl der angezeigten Felder reduzieren, damit der Benutzer die geeigneten Arbeitsaufgaben schneller auswählen können. Sie können im Feld **Datensätze pro Seite** auf dem Inforegister **Allgemeines** außerdem auswählen, wie viele Datensätze pro Seite angezeigt werden. Wenn die Option **Benutzern das Filtern nach Arbeitstransaktionstyp erlauben** ausgewählt wurde, wird ein Steuerelement **Arbeit filtern** in der Arbeitsliste angezeigt, mit dem der Benutzer nach Buchungsart filtern kann. Benutzer sehen nur die Arbeit in der Arbeitsliste, auf die sie gemäß Berechtigungen zugreifen können. Sie müssen sich vergewissern, dass Benutzer die Berechtigung für eine oder mehrere benutzergeleitete Menüoptionen haben, die die bestimmten Arbeitsklassentypen unterstützen, auf die sie zugreifen können müssen. Berechtigungen werden auch verifiziert, wenn ein Benutzer versucht, Arbeit aus der Liste auszuführen.|
| Umlagerungsauftrag aus Kennzeichen erstellen | Ermöglicht Lagerarbeitern das Erstellen und Verarbeiten von Umlagerungsaufträgen direkt über die Warehouse Management Mobile App. Die Lagerarbeiter wählen zunächst den Ziellagerort aus und können dann mit der App ein oder mehrere Kennzeichen scannen. Wenn der Lagerarbeiter **Bestellung abschließen** auswählt, erstellt ein Batchauftrag den erforderlichen Umlagerungsauftrag und die Bestellpositionen basierend auf dem verfügbaren, für diese Kennzeichen registrierten Lagerbestand. Weitere Informationen finden Sie unter [Erstellen von Umlagerungsaufträgen aus der Lagerort-App](create-transfer-order-from-warehouse-app.md)

## <a name="configure-menu-items-to-create-work-for-another-worker-or-process"></a>Konfigurieren von Menüoptionen, um Arbeit für eine andere Arbeitskraft oder einen anderen Prozess zu erstellen

Sie können eine Menüoption einrichten, die Arbeit für eine andere Arbeitskraft erstellt, nachdem eine ursprüngliche Aktion auf dem mobilen Gerät ausgeführt wurde. Wenn z. B. eine Arbeitskraft ein mobiles Gerät verwendet, um einen Artikel zu erhalten, wird Einlagerungsarbeit für eine andere Arbeitskraft erstellt. Wählen Sie zum Einrichten eines Menüelements zum Erstellen von Arbeit auf der Seite **Menüelemente des mobilen Geräts** im Feld **Modus** die Option **Arbeit** aus. In der folgenden Tabelle werden die Optionen im Feld **Arbeitserstellungsprozess** nach Arbeitsauftragstyp angeordnet.

<table>
<tbody>
<tr>
<th>Arbeitsauftragstyp</th>
<th>Mit der folgenden Option...</th>
<th>Beschreibung</th>
</tr>
<tr>
<td rowspan="8">Bestellung</td>
<td>Bestellposition – Empfang</td>
<td>Erfassen Sie den Eingang einer Menge eines Artikels, indem Sie die Bestellnummer und Bestellpositionsnummer verwenden und Einlagerungsarbeit für eine andere Arbeitskraft erstellen.</td>
</tr>
<tr>
<td>Bestellposition – Empfang und Einlagerung</td>
<td>Erfassen Sie den Eingang einer Menge eines Artikels, indem Sie die Bestellnummer und Bestellpositionsnummer verwenden und die Artikel einlagern. Die gleiche Arbeitskraft führt beide Aktivitäten aus.</td>
</tr>
<tr>
<td>Bestellungsartikel – Empfang</td>
<td>Erfassen Sie den Eingang einer Menge eines Artikels für eine Bestellung, indem Sie die Bestellnummer und Artikelnummer registrieren und Einlagerungsarbeit für eine andere Arbeitskraft erstellen.</td>
</tr>
<tr>
<td>Bestellungsartikel – Empfang und Einlagerung</td>
<td>Erfassen Sie den Eingang einer Menge eines Artikels für eine Bestellung, indem Sie die Bestellnummer und die Artikelnummer registrieren und den Artikel einlagern. Die gleiche Arbeitskraft führt beide Aktivitäten aus.</td>
</tr>
<tr>
<td>Ladungsträger – Empfang</td>
<td>Empfangen Sie einen Versand-Avis (ASN), indem Sie die Ladungsträgerkennung verwenden.</td>
</tr>
<tr>
<td>Kennzeichenempfang und -einlagerung</td>
<td>Empfangen Sie einen Versand-Avis (ASN) und legen Sie diesen zur Seite, indem Sie die Ladungsträgerkennung verwenden.</td>
</tr>
<tr>
<td>Artikelempfang aus Ladung</td>
<td>Erfassen Sie den Eingang einer Menge einer Ladung, indem Sie die Ladungskennung verwenden und Einlagerungsarbeit für eine andere Arbeitskraft erstellen. Die Artikelnummer und die Produktdimensionen stimmen mit dem Beleg an die Bestellpositionen überein.</td>
</tr>
<tr>
<td>Artikelempfang und -einlagerung aus Ladung</td>
<td>Erfassen Sie den Eingang einer Ladung, indem Sie die Ladungskennung verwenden und die Artikel einlagern. Die Artikelnummer und die Produktdimensionen stimmen mit dem Beleg an die Bestellpositionen überein. Die gleiche Arbeitskraft führt beide Aktivitäten aus.</td>
</tr>
<tr>
<td rowspan="2">Rücklieferung</td>
<td>Rücklieferungsempfang</td>
<td>Erfassen Sie den Eingang einer Menge eines Artikels, indem Sie die Rücklieferungsnummer registrieren und Einlagerungsarbeit für eine andere Arbeitskraft erstellen.</td>
</tr>
<tr>
<td>Rücklieferungsempfang und -einlagerung</td>
<td>Erfassen Sie den Eingang einer Menge eines Artikels, indem Sie die Rücklieferungsnummer registrieren und Artikel einlagern. Die gleiche Arbeitskraft führt beide Aktivitäten aus.</td>
</tr>
<tr>
<td rowspan="6">Umlagerungsauftrag</td>
<td>Artikelempfang des Umlagerungsauftrags</td>
<td>Erfassen Sie den Eingang einer Menge eines Artikels, und erstellen Sie Einlagerungsarbeit für eine andere Arbeitskraft.

<strong>Hinweis:</strong> Verwenden Sie diese Option nur, wenn die Artikel aus einem Lagerort versendet wurden, der nicht für Lagerortverwaltungsprozesse aktiviert ist.</td>
</tr>
<tr>
<td>Artikelempfang und -einlagerung für Umlagerungsauftrag</td>
<td>Erfassen Sie den Eingang einer Menge eines Artikels, und lagern Sie die Artikel ein. Die gleiche Arbeitskraft führt beide Aktivitäten aus.

<strong>Hinweis:</strong> Verwenden Sie diese Option nur, wenn die Artikel aus einem Lagerort versendet wurden, der nicht für Lagerortverwaltungsprozesse aktiviert ist.</td>
</tr>
<tr>
<td>Umlagerungsauftrags-Positionsempfang</td>
<td>Erfassen Sie den Eingang einer Menge eines Artikels, und erstellen Sie Einlagerungsarbeit für eine andere Arbeitskraft.</td>
</tr>
<tr>
<td>Umlagerungsauftragsposition – Empfang und Einlagerung</td>
<td>Erfassen Sie den Eingang einer Menge eines Artikels, und lagern Sie die Artikel ein. Die gleiche Arbeitskraft führt beide Aktivitäten aus.</td>
</tr>
<tr>
<td>Ladungsträger – Empfang</td>
<td>Empfangen Sie einen Versand-Avis (ASN), indem Sie die Ladungsträgerkennung verwenden.</td>
</tr>
<tr>
<td>Kennzeichenempfang und -einlagerung</td>
<td>Empfangen Sie einen Versand-Avis (ASN) und legen Sie diesen zur Seite, indem Sie die Ladungsträgerkennung verwenden.</td>
</tr>
<tr>
<td rowspan="4">Produktion</td>
<td>Fertigmeldung</td>
<td>Erfassen Sie eine Menge eines Fertigartikels, der für eine Produktion fertiggestellt wurde, und erstellen Sie Einlagerungsarbeit für eine andere Arbeitskraft. Die Menge kann einige oder alle Mengen handeln, die für die Produktion eingeplant wurde.</td>
</tr>
<tr>
<td>Fertig melden und einlagern</td>
<td>Erfassen Sie eine Menge eines Fertigartikels, der für eine Produktion fertiggestellt wurde, und lagern Sie die Artikel ein. Die Menge kann einige oder alle Mengen handeln, die für die Produktion eingeplant wurde. Die gleiche Arbeitskraft führt beide Aktivitäten aus.</td>
</tr>
<tr>
<td>Kanban</td>
<td>Geben Sie an, dass ein Kanban abgeschlossen ist, und erstellen Sie Einlagerungarbeit für eine andere Arbeitskraft.</td>
</tr>
<tr>
<td>Kanban-Einlagerung</td>
<td>Geben Sie an, dass ein Kanban abgeschlossen ist, und lagern Sie die Artikel ein. Die gleiche Arbeitskraft führt beide Aktivitäten aus.</td>
</tr>
<tr>
<td rowspan="5">Bestand</td>
<td>Bewegung</td>
<td>Registrieren Sie, dass Artikel von einem Lagerplatz zu einem anderen bewegt wurden. Die Arbeitskraft gibt den Speicherort an, von dem die Artikel bewegt wurden und wohin sie bewegt werden.</td>
</tr>
<tr>
<td>Quarantäne</td>
<td>Ändern Sie den Status des verfügbaren Lagerbestands für einen Ladungsträger oder einen Lagerplatz, um beschädigte oder fehlende Lagerartikel nicht verfügbar zu machen.</td>
</tr>
<tr>
<td>Bewegung durch Vorlage</td>
<td>Verschieben Sie Artikel von einem Lagerplatz in einen anderen in einer halbautomatisierten Weise. Die Arbeitskraft wählt den Lagerplatz aus, von dem Artikel verschoben werden sollen. Das System verwendet die Lagerplatzdirektive, um zu bestimmen, wohin die Artikel verschoben werden.</td>
</tr>
<tr>
<td>Lagerortumlagerung</td>
<td>Registrieren Sie, dass Artikel von einem Lagerort zu einem anderen übertragen wurden. Diese Option setzt voraus, dass die Arbeitskraft Arbeit in beiden Lagerorten ausführen kann.

<strong>Hinweis:</strong> Diese Menüoption erfordert eine standardmäßige Umlagerungserfassung, in der das Feld für das <strong>Ziehen des Belegs</strong> auf <strong>Buchung</strong> festgelegt ist.</td>
</tr>
<tr>
<td>Ladungsträgerladung</td>
<td>Verwenden Sie diese Option, wenn&#39;Sie den Lagerort zum ersten Mal einrichten. Scannen Sie alle Ladungsträger in allen Lagerplätzen am Lagerort. Die Lagerplätze müssen von einem Ladungsträger gesteuert sein. Sie können&#39;diese Option nicht verwenden, wenn in der Bestandsreservierungshierarchie über <strong>Lagerplatz</strong> <strong>Seriennummer</strong> oder <strong>Chargennummer</strong> aufgeführt wird.</td>
</tr>
<tr>
<td rowspan="3">Inventur</td>
<td>Regulierung eingehend</td>
<td>Erhöhen Sie die Artikelmenge im Bestand. Geben Sie den Lagerort, den Ladungsträger, den Artikel, die Menge, die Maßeinheit und den Status an.</td>
</tr>
<tr>
<td>Regulierung ausgehend</td>
<td>Senken Sie die Artikelmenge im Bestand. Geben Sie den Lagerort, den Ladungsträger, den Artikel, die Menge, die Maßeinheit und den Status des Bestands an.</td>
</tr>
<tr>
<td>Permanente Lagerplatzinventur</td>
<td>Starten Sie eine Inventur für einen Lagerplatz. Die Arbeitskraft muss alle Artikel im Lagerplatz zählen. Wenn das Ergebnis einer Inventur niedriger ist als die erwartete Menge, gilt die fehlende Menge als Verlust.</td>
</tr>
</tbody>
</table>

## <a name="configure-menu-items-to-process-existing-work"></a>Konfigurieren von Menüoptionen, um vorhandene Arbeit zu verarbeiten
Neben der Einrichtung der Menüelemente zum Erstellen von Lagerarbeit können Sie Menüelemente zur Verarbeitung der Arbeit einrichten, die bereits erstellt wurde. Legen Sie das Feld **Modus** auf **Arbeit** fest, und wählen Sie die Option **Vorhandene Arbeit verwenden** aus. Einige zusätzliche Optionen sind anschließend auf der Registerkarte **Allgemeines** verfügbar. Sie können den Zugriff auf die Menüoption steuern, indem Sie mindestens eine Arbeitsklasse auf dem Inforegister **Arbeitsklasse** zuweisen. Die Arbeitsklassen definieren die Arbeit, die die Menüoption verarbeiten kann. Die Arbeitsklasse kann auch verwendet werden, um den Zugriff auf die bestimmten Benutzerrollen oder zum separaten Verarbeiten für unterschiedliche Arten von Arbeitsgängen zu gewähren. In der folgenden Tabelle werden die Optionen beschrieben, die zur Verfügung stehen. Die Option kann mit dem Feld **Ausgeführt von** auf der Seite **Menüoptionen des mobilen Geräts** aktiviert werden. 

<table>




<thead>
<tr class="header">
<th>Option</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nichts</td>
<td>Dieser Standardwert verarbeitet&#39;keine Arbeit.</td>
</tr>
<tr class="even">
<td>Systemgeleitet</td>
<td>Das Supply Chain Management steuert den Typ der Arbeit, die einer Arbeitskraft zugewiesen wird, und die Reihenfolge, in der die Arbeitskraft die Arbeit ausführt. Wenn Sie diese Option auswählen, können Sie im Aktivitätsbereich <strong>Systemzugewiesene Arbeit</strong> auswählen, um die Seite <strong>Systemzugewiesene Sortierreihenfolge</strong> anzuzeigen, auf der Sie Sortierkriterien für die Arbeit einrichten können. Die Sortierkriterien steuern die Reihenfolge, in dem die Arbeitskraft die Arbeit ausführt. Sie können beliebig viele Kriterien hinzufügen.</td>
</tr>
<tr class="odd">
<td>Benutzergeleitet</td>
<td>Die Arbeitskraft wählt die Arbeit, die ausgeführt werden soll, und die Reihenfolge, in der sie ausgeführt werden soll.</td>
</tr>
<tr class="even">
<td>Benutzergruppierung</td>
<td>Die Arbeitskraft gruppiert Arbeit manuell. Diese Option ist beispielsweise hilfreich, wenn eine Arbeitskraft mehrere Artikel in einem Lagerplatz gleichzeitig entnehmen kann. Nachdem die Arbeitskraft die Entnahme aller erforderlichen Artikel beendet hat, kann sie die Artikel einlagern.</td>
</tr>
<tr class="odd">
<td>Systemgruppierung</td>
<td>Das Supply Chain Management gruppiert Arbeit für die Arbeitskraft basierend auf einem angegebenem Feld. Beispielsweise wird Entnahmearbeit gruppiert, wenn eine Arbeitskraft eine Lieferkennung, Ladungskennung oder einen beliebigen Wert scannt, der jede Arbeitseinheit verknüpfen kann. Wählen Sie diese Option auswählen, sind die folgenden Felder erforderlich:
<ul>
<li><strong>Systemgruppierungsfeld</strong> – Wählen Sie das Feld aus, das die Arbeitskraft scannt, um die Arbeit zu gruppieren.</li>
<li><strong>Systemgruppierungsbezeichnung</strong> – Geben Sie Text ein, um die Arbeitskraft darüber zu informieren, was zu scannen ist, um die Arbeit zu gruppieren.</li>
</ul></td>
</tr>
<tr class="even">
<td>Benutzergeleitet – überprüft</td>
<td>Die Arbeitskraft wählt die Arbeit aus, die ausgeführt werden soll, wenn Arbeit mit einer größeren Entität verbunden ist, wie Ladung oder Lieferung. Die Arbeitskraft bestimmt, in welcher Reihenfolge die Artikel entnommen werden. Wählen Sie diese Option auswählen, sind die folgenden Felder erforderlich:
<ul>
<li><strong>Überprüftes benutzergeleitetes Feld</strong> – Wählen Sie das Feld aus, das die Arbeitskraft scannt, um die Arbeit zu gruppieren.</li>
<li><strong>Überprüfte benutzergeleitete Beschriftung</strong> – Geben Sie den Text ein, der die Arbeitskraft darüber informiert, was zu scannen ist, wenn Entnahmearbeit vom System gruppiert wird.</li>
</ul>
Diese Option ist beispielsweise hilfreich, wenn mehrere Paletten für eine Ladung bereitgestellt werden. Wenn Sie im Feld <strong>Benutzergeleitet – überprüft</strong> die Option <strong>LoadId</strong> auswählen, kann die Arbeitskraft eine beliebige Palette auswählen, die der Ladung zugeordnet ist. Der Arbeitskraft wird eine Fehlermeldung angezeigt, wenn sie oder er einen Artikel scannt, der nicht&#39;der Ladung zugeordnet ist.</td>
</tr>
<tr class="odd">
<td>Clusterkommissionierung</td>
<td>Die Arbeitskraft gruppiert Arbeit in Cluster. Cluster ermöglichen Arbeitskräften, Artikel aus einem einzelnen Lagerplatz für mehrere Arbeitsaufträge gleichzeitig zu entnehmen.</td>
</tr>
<tr class="even">
<td>Permanente Inventur-Gruppierung</td>
<td>Die Arbeitskraft wählt eine Zone, einen Arbeitspool oder einen Lagerplatz aus, und das Supply Chain Management weist Arbeit auf Grundlage der Auswahl zu. Wenn Sie diese Option auswählen, können Sie im Aktivitätsbereich auf <strong>Permanente Inventur</strong> klicken, um zusätzliche Informationen anzuzeigen, und Sie können die Häufigkeit angeben, in der die Arbeitskraft die Inventur wiederholen muss, wenn ein Differenz gefunden wird.</td>
</tr>
 <tr class="odd">
<td>Transportladung</td>
<td>Diese ‭Funktion ermöglicht es mehreren Lagerarbeitern, eine Bestand von der selben oder einer anderen Ladung auf den gleichen LKW zu laden, der vollständig oder teilweise gelieferten ist.</td>
</tr>
</tbody>
</table>

## <a name="additional-menu-item-options"></a>Zusätzliche Menüelementoptionen
Zusätzliche Menüelementoptionen sind auf der Seite **Menüelemente des mobilen Geräts** verfügbar. Die Optionen variieren abhängig vom Prozess, für den Sie die Menüoption konfigurieren. 

Diese Optionen werden in der folgenden Tabelle näher erläutert.

<table>




<thead>
<tr class="header">
<th>Feld</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Aufteilung der Arbeit zulassen</td>
<td>Aktivieren Sie diese Option um Benutzern zu ermöglichen, Artikel für einen Arbeitsauftrag in mehr als einen Zielladungsträger zu platzieren. Diese Option ist nützlich, wenn ein Zielladungsträger voll ist und die Arbeitskraft die übrigen Artikel einem anderen Ladungsträger hinzufügen muss. Die Arbeitskraft kann <strong>Voll</strong> auswählen, um anzugeben, dass der Ladungsträger voll ist und keine Entnahmearbeit mehr dafür entgegen nehmen. Der Einlagerungsort für die entnommenen Artikel wird dann angezeigt, und die Entnahmearbeit, die bereits abgeschlossen wurde, wird an einen neuen Arbeitsauftrag verschoben. Die verbleibende Entnahmearbeit für den Zielladungsträger bleibt weiterhin im Originalarbeitsauftrag.</td>
</tr>
<tr class="even">
<td>Verankern</td>
<td>Aktivieren Sie diese Option, um Arbeitskräften zu ermöglichen, einen Lagerplatz anzugeben, der den vorgeschlagenen Bereitstellungs- oder Ladungslagerplatz überschreibt. Alle verbleibende Entnahmearbeit wird an den neuen Lagerplatz weitergeleitet. Diese Option ist beispielsweise hilfreich, wenn eine Arbeitskraft Artikel für Auftrag 1 in einen Bereitstellungslagerplatz bei Rampe 1 platzieren muss, dies jedoch nicht kann, da eine vorherige Ladung nicht vom Lagerplatz entfernt wurde. Anstatt auf den Staginglagerplatz des Docks 1 zu warten, kann die Arbeitskraft festlegen, dass sie den Staginglagerplatz Dock 2 verwendet. In diesem Fall wird die Arbeitskraft den vorgeschlagenen bereitgestellten Lagerplatz überschreiben. Der Einlagerungsort für alle verbleibenden Artikel für den Arbeitsauftrag wird dann auf Bereitstellungslagerplatz für Rampe 2 aktualisiert. Wenn Sie diese Option auswählen, muss auch das Feld <strong>Anker von</strong> festgelegt werden.</td>
</tr>
<tr class="odd">
<td>Anker von</td>
<td>Wenn Sie Verankern&#39;verwenden, müssen Sie angeben, ob Sie nach Lieferdatum oder nach Ladung verankern möchten.</td>
</tr>
<tr class="even">
<td>Überwachungsvorlagenkennung</td>
<td>Wählen Sie die Arbeitsauditvorlage aus, die den Arbeitsprozess für dieses Menüelement unterbricht, damit ein anderer Arbeitsgang ausgeführt werden kann. Wenn beispielsweise dieses Menüelement für eingehende Arbeit ist, kann die Auditvorlage vorschreiben, dass die Arbeitskraft die Temperatur im Liefercontainer prüft. Der Zeitpunkt, zu dem der Prozess unterbrochen wird, wird auf der Auditvorlage angegeben. Dieser Punkt kann beispielsweise der Start oder Abschluss der Arbeit sein oder eine Statusänderung.</td>
</tr>
<tr class="odd">
<td>Clusterprofilkennung</td>
<td>Wählen Sie das Clusterprofil aus, das für die Clusterentnahme zu verwenden ist. Das Clusterprofil umfasst Einstellungen, wie ob Cluster automatisch erstellt werden, die Namen von Positionen und die Anzahl von Arbeitseinheiten, die zugewiesen werden können, wann Cluster in individuelle Einheiten aufgeschlüsselt werden und ob Überprüfung erforderlich ist. Dieses Feld ist nur verfügbar, wenn <strong>Clusterkommissionierung</strong> im Feld <strong>Geleitet von</strong> ausgewählt ist.</td>
</tr>
<tr class="even">
<td>Gesamte Artikelmenge zuerst zählen</td>
<td>Aktivieren Sie diese Option, um für eine Arbeitskraft festzulegen, die Gesamtmenge zuerst während einer Inventur zu zählen. Wenn ein Unterschied gefunden wird, muss die Arbeitskraft zusätzliche Informationen bereitstellen, wie Kennzeichennummer, Chargennummer und Seriennummern.</td>
</tr>
<tr class="odd">
<td>Bewegung erstellen</td>
<td>Aktivieren Sie diese Option, um einer Arbeitskraft zu ermöglichen, Arbeit für eine Bewegung zu erstellen, ohne von der Arbeitskraft zu erfordern, die Arbeit sofort auszuführen. Diese Option ist beispielsweise hilfreich, wenn eine Qualitätsprüfung abgeschlossen wurde, und der Inspektor möchte, dass der Artikel aus dem Qualitätsinspektionsbereich entfernt wird.</td>
</tr>
<tr class="even">
<td>Richtliniencode</td>
<td>Um eine bestimmte Lagerplatzdirektive zu verwenden, wählen Sie den Richtliniencode aus, der der Lagerplatzdirektive zugeordnet ist. Dieses Feld ist verfügbar, wenn Sie Arbeit erstellen und der Arbeitserstellungsprozess <strong>Bewegung durch Vorlage</strong> ist.</td>
</tr>
<tr class="odd">
<td>Schwellenwerte für permanente Inventur deaktivieren</td>
<td>Aktivieren Sie diese Option, um die Inventurschwellenwerte zu ignorieren. Wenn Sie diese Option aktivieren, wird Inventurarbeit nicht&#39;erstellt, wenn Schwellenwerte überschritten werden.</td>
</tr>
<tr class="even">
<td>Den Chargendispositionscode anzeigen</td>
<td>Aktivieren Sie dieses Kontrollkästchen, um Chargendispositionscodes anzuzeigen. Sie können beispielsweise Chargendispositionscodes anzeigen, wenn Sie eine zurückgegebene Charge empfangen. Arbeitskräfte können dann den Status oder die Qualität einer Charge überprüfen und den entsprechenden Code auswählen. Die Regeln im Chargendispositionscode bestimmen, ob die Charge für andere Lagerortprozesse verfügbar ist. Wenn Sie diese Option nicht&#39;auswählen, wird einer der folgenden Chargendispositionscodes verwendet:
<ul>
<li>Wenn Sie eine neue Chargennummer empfangen, wird der standardmäßige Chargendispositionscode verwendet, der auf der Artikelmodellgruppe angegeben ist.</li>
<li>Der Chargendispositionscode, der bereits der Charge zugeordnet ist, wird verwendet.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Dispositionscode anzeigen</td>
<td>Aktivieren Sie diese Option, um Dispositionscodes anzuzeigen. Sie können beispielsweise Dispositionscodes anzeigen, wenn Sie zurückgegebene Artikel empfangen. Arbeitskräfte können dann den Status oder die Qualität der Artikel überprüfen und den entsprechenden Code auswählen. Die Regeln im Dispositionscode bestimmen, ob die Artikel für andere Lagerortprozesse verfügbar ist.</td>
</tr>
<tr class="even">
<td>Bestandsstatus anzeigen</td>
<td>Aktivieren Sie diese Option, um den Status des Artikels im Bestand anzuzeigen. Diese Option ist für alle Menüoptionen verfügbar, die vorhandene Arbeit verwenden, außer Zykluszählung.</td>
</tr>
<tr class="odd">
<td>Übersicht des Entnahmebildschirms anzeigen</td>
<td>Aktivieren Sie diese Option, um eine Zusammenfassung der Entnahmearbeit für den ausgewählten Arbeitsauftrag anzuzeigen. Die Zusammenfassung wird angezeigt, bis die erste Arbeitsposition für den Arbeitsauftrag verarbeitet wurde.</td>
</tr>
<tr class="even">
<td>Ladungsträger generieren</td>
<td>Aktivieren Sie diese Option, um eine eindeutige Kennzeichennummer basierend auf der Nummernkreisauswahl zu generieren. So können Sie beispielsweise eine Kennzeichennummer für Artikel generieren, die für Bestellungen eingegangen sind.</td>
</tr>
<tr class="odd">
<td>Gruppeneinlagerung</td>
<td>Aktivieren Sie diese Option, um die Entnahmearbeit zu gruppieren. Diese Option ist verfügbar, wenn die Arbeit entweder von der Arbeitskraft oder vom Supply Chain Management gruppiert wurde. Wenn die Arbeitskraft alle Entnahmearbeit in der Gruppe beendet hat, wird Entnahmearbeit für die gleiche Gruppe erstellt.</td>
</tr>
<tr class="even">
<td>Lagerregulierungstypen</td>
<td>Wählen Sie den Lagerregulierungstyp aus, der die Lagerinventurerfassung bestimmt, die verwendet wird, um die Anpassung zu buchen, und ob Reservierungen entfernt werden. Dieses Feld ist nur für die Arbeitserstellungsprozesse <strong>Regulierung eingehend</strong> oder <strong>Regulierung ausgehend</strong> verfügbar.</td>
</tr>
<tr class="odd">
<td>Chargennummer überschreiben</td>
<td>Aktivieren Sie diese Option, um Arbeitskräften, die eine Menge als fertig für einen Produktionsauftrag melden, eine Chargennummer einzugeben, die sich von der Chargennummer unterscheidet, die dem Produktionsauftrag zugeordnet ist.</td>
</tr>
<tr class="even">
<td>Zielladungsträger überschreiben</td>
<td>Aktivieren Sie dieses Kontrollkästchen, um Arbeitskräften zu ermöglichen, eine Zielkennzeichennummer anzugeben, die sich vom vorgeschlagenen Zielladungsträger unterscheidet. Verwenden Sie diese Option, wenn die erste Entnahme für einen Arbeitsauftrag für die gesamte Menge eines Artikels auf einem Ladungsträger ist. Diese Option ist beispielsweise hilfreich, wenn eine Palette wiederverwendet wird.</td>
</tr>
<tr class="odd">
<td>Entnehmen und verpacken</td>
<td>Aktivieren Sie diese Option, um Arbeitskräften zu erlauben, Arbeit für einen Auftrag oder eine Ladung in einer einzigen Arbeitseinheit zu kombinieren. Eine Arbeitskraft kann Arbeit nur für den Auftrag oder die Ladung ausführen. Diese Option ist beispielsweise hilfreich, wenn Sie eine Menge für einen Auftrag erhöhen müssen, nachdem die Ladung, die Lieferung und die Arbeit für den Auftrag erstellt wurde. Diese Option ist verfügbar, wenn das Menüelement vorhandene Arbeit verwendet, und die Arbeit vom Benutzer oder dem System weitergeleitet wird.</td>
</tr>
<tr class="even">
<td>Älteste Stapelverarbeitung wählen entnehmen</td>
<td>Geben Sie an, ob die Arbeitskraft zuerst die älteste Charge in einem Lagerplatz entnehmen muss. Die folgenden Optionen sind verfügbar:
<ul>
<li><strong>Keine</strong> – Die Arbeitskraft kann jede Charge im Lagerplatz entnehmen. Die Arbeitskraft erhält keine Meldung.</li>
<li><strong>Warnen</strong> – Die Arbeitskraft kann jede Charge im Lagerplatz entnehmen, es wird jedoch eine Warnmeldung angezeigt, wenn die Charge nicht&#39;die älteste ist.</li>
<li><strong>Erzwingen</strong> – Die Arbeitskraft muss zuerst die älteste Charge im Lagerplatz entnehmen. Der Arbeitskraft wird eine Fehlermeldung angezeigt, wenn eine Charge nicht&#39;die älteste Charge ist. <strong>Hinweis:</strong> Diese Option ist nur relevant, wenn <strong>Chargennummer</strong> in der Reservierungshierarchie ist, die dem Artikel zugewiesen ist, niedriger ist als <strong>Lagerplatz</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Etikett drucken</td>
<td>Aktivieren Sie diese Option, um Arbeitskräften das Drucken von Ladungsträgerbeschriftungen zu ermöglichen.</td>
</tr>
<tr class="even">
<td>Systemgruppierungsfeld</td>
<td>Wählen Sie das Feld aus, das bestimmt, wie das Supply Chain Management Entnahmearbeit für Arbeitskräfte gruppiert. Wenn Sie beispielsweise das Feld <strong>ShipmentId</strong> auswählen, scannt die Arbeitskraft die Lieferkennung, um die Entnahmearbeit zu gruppieren. Alle Arbeit für die Lieferung wird dann der Arbeitskraft zugewiesen. Dieses Feld setzt voraus, dass Sie eine Menüoption erstellen, um vorhandene Arbeit zu nutzen, die vom System gruppiert wird. Sie müssen außerdem Text im Feld <strong>Systemgruppierungsbezeichnung</strong> eingeben, um die Arbeitskraft darüber zu informieren, was zu scannen ist.</td>
</tr>
<tr class="odd">
<td>Systemgruppierungsbezeichnung</td>
<td>Geben Sie den Text ein, der die Arbeitskraft darüber informiert, was zu scannen ist, wenn Entnahmearbeit vom Supply Chain Management gruppiert wird. Wenn Sie&#39;beispielsweise das Feld <strong>ShipmentId</strong> verwenden, um Entnahmearbeit nach Lieferung zu gruppieren, können Sie <strong>Lieferkennung</strong> in das Feld eingeben. Dieses Feld setzt voraus, dass Sie eine Menüoption erstellen, um vorhandene Arbeit zu nutzen, die vom System gruppiert wird. Sie müssen auch das Feld auswählen, um nach <strong>Systemgruppierung</strong> zu gruppieren.</td>
</tr>
<tr class="even">
<td>Standarddaten verwenden</td>
<td>Aktivieren Sie diese Option, um die Schaltfläche <strong>Standarddaten</strong> im Aktivitätsbereich zu aktivieren, in dem Sie Felder auswählen können, um Daten anzuzeigen, die eine Arbeitskraft in der Regel bei der täglichen Arbeit benötigt. Diese Option ist beispielsweise hilfreich, wenn eine Arbeitskraft häufig Artikel aus dem gleichen Lagerplatz entnimmt. Sie können das Feld <strong>Vom Lagerplatz</strong> auswählen, um den Lagerplatz standardmäßig anzuzeigen.</td>
</tr>
<tr class="odd">
<td>Überprüftes benutzergeleitetes Feld</td>
<td>Wählen Sie das Feld aus, das die Arbeitskraft scannt, um die Arbeit zu gruppieren. Wenn Sie zum Beispiel <strong>LoadId</strong> auswählen, kann eine Arbeitskraft jede Arbeit entnehmen, die einer ausgewählten Ladung zugeordnet ist. Sie müssen außerdem Text im Feld <strong>Überprüfte benutzergeleitete Beschriftung</strong> eingeben, um die Arbeitskraft darüber zu informieren, was zu scannen ist.</td>
</tr>
<tr class="even">
<td>Überprüfte benutzergeleitete Beschriftung</td>
<td>Geben Sie den Text ein, der die Arbeitskraft darüber informiert, was zu scannen ist, wenn Entnahmearbeit vom einem validierten benutzergesteuerten Feld gruppiert wird. Wenn Sie beispielsweise das Feld <strong>LoadId</strong> verwenden, um Entnahmearbeit für eine Ladung zu gruppieren, können Sie <strong>Lieferkennung</strong> in das Feld eingeben.</td>
</tr>
<tr class="odd">
<td>Arbeitsvorlagencode</td>
<td>Wählen Sie die Arbeitsvorlage aus, die die Arbeit für einen Prozess erstellt. Wenn Sie zum Beispiel einen Artikel für eine Bestellung erhalten, wird die Entnahmearbeit auf Grundlage der Arbeitsvorlage generiert. Wenn Sie keine&#39;Arbeitsvorlage auswählen, weist das Supply Chain Management eine Vorlage auf Grundlage von Abfragekriterien zu. Weitere Informationen zu Arbeitsvorlagen, finden Sie unter <a href="control-warehouse-location-directives.md">Steuern von Lagerarbeit mithilfe von Arbeitsvorlagen und Lagerplatzrichtlinien</a>.</td>
<tr class="even">
<td>Arbeitspositionsliste anzeigen</td>
<td>Wählen Sie eine Option aus, wie Arbeitskräfte die Positionen für die aktuell ausgewählte Kommissionierarbeit anzeigen und mit ihnen interagieren können. Weitere Informationen zu dieser Option finden Sie unter <a href="pick-line-overview.md">Richten Sie einen Menüpunkt für mobile Geräte ein, um eine Übersicht über die Entnahmepositionen bereitzustellen</a>.</td>
</tr>
</tbody>
</table>

## <a name="require-workers-to-confirm-the-product-location-or-quantity-when-they-pick-items"></a>Erfordern von Arbeitskräften, das Produkt, den Lagerplatz oder die Menge zu bestätigen, wenn sie Artikel entnehmen

Sie können Arbeitsbestätigungen einrichten, die eine Arbeitskraft auffordern, ein mobiles Gerät zu verwenden, um den Lagerplatz oder die Menge zu erfassen, wenn Arbeit am Lagerort ausgeführt wird. Arbeitsbestätigungen helfen dabei, sicherzustellen, dass die Arbeitskraft am richtigen Lagerplatz ist oder die richtige Menge der Artikel bearbeitet. Sie können auch aktivieren, dass das Supply Chain Management die Registrierung der Arbeitskraft automatisch bestätigt. Wenn Sie Autobestätigung aktivieren, können Sie keine Bestätigungen für Lagerplatz oder Menge anfordern. Arbeitsbestätigungen beinhalten auch Produkte und Produktvarianten. Darüber hinaus können Sie Bestätigungen erfassen, indem Sie einen Strichcode scannen. Um Produkte und Produktvarianten zu bestätigen, müssen Sie eine Kennung für das Produkt oder die Produktvariante eingeben. Diese Kennung kann eine Produktkennung, Produktsuchkennung, externe Kennung, GTIN oder ein Strichcode sein. Nachdem Sie die Kennung eingeben oder den Strichcode gescannt haben, werden die Dimensionen für die Produktvariante im mobilen Gerät angezeigt. 

In der folgenden Tabelle werden die verschiedenen Arbeitstypen beschrieben, bei denen Sie Arbeitsbestätigungen verwenden können.

| Mit der folgenden Option... | Beschreibung |
|------------------------|----------------------------------------------------------------------------|
| Entnahme | Erfordern einer Bestätigung, wenn Artikel entnommen werden. |
| Einlagern | Erfordern einer Bestätigung, wenn Artikel in einem Lagerplatz platziert werden. |
| Inventur | Erfordern einer Bestätigung während der Zykluszählung. |
| Regulierungen | Erfordern einer Bestätigung, wenn Lagermengen angepasst werden. |
| Benutzerdefiniert | Erfordern einer Bestätigung für Maßarbeit. |
| Quarantäne | Erfordern einer Bestätigung, wenn Artikeln unter Quarantäne gestellt werden. |
| Ladungsträgererstellung | Erfordern einer Bestätigung, wenn die Artikel konsolidiert werden, um einen Ladungsträger zu erstellen. |
| Drucken | Erfordern einer Bestätigung, wenn Sie Ladungsträgerbeschriftungen drucken. |
| Statusänderung | Erfordern einer Bestätigung, wenn Sie den Status des Bestands ändern. |

> [!NOTE]
> Produktbestätigungen können nur bei Entnahmen und Einlagerungen erforderlich gemacht werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Richten Sie eine Menüoption des mobilen Geräts für das Abschließen der Arbeit von Typ Bestellung](tasks/set-up-mobile-device-menu.md)
- [Eine Menüoption für das mobile Gerät einrichten, um die eingegangenen Artikel zu erfassen](tasks/set-up-mobile-device-menu-item-register-received-items.md)
- [Bestandsstatus](../inventory/inventory-statuses.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
