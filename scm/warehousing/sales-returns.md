---
title: Retouren
description: "Dieser Abschnitt enthält Informationen über den Prozess für Rücklieferungen bereit. Er umfasst Informationen zu einer Rücksendung und ihren Auswirkungen auf Nachkalkulations- und Lagerbestandmengen ein."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: b265a20a271230de5dba6df93900a24aad642885
ms.lasthandoff: 03/31/2017


---

# <a name="sales-returns"></a>Retouren

Dieser Abschnitt enthält Informationen über den Prozess für Rücklieferungen bereit. Er umfasst Informationen zu einer Rücksendung und ihren Auswirkungen auf Nachkalkulations- und Lagerbestandmengen ein.

Debitoren vornehmen Rückgabeartikel unterschiedlichen Gründen ein. So kann ein Artikel fehlerhaft, oder er entspräche möglicherweise nicht den Erwartungen des Debitors. Die Rückholprozessanfänge wenn Kundenprobleme eine Anforderung, einen Artikel zurückzugeben. Nachdem die Anforderung erhalten des Debitors ist, ist eine Rücklieferung im Microsoft Dynamics 365 für Arbeitsgänge erstellt.

## <a name="return-order-process"></a>Rücklieferungsprozess
Die folgende Abbildung zeigt einen Überblick des Rücklieferungsprozesses.  

![salesreturns01 ([]. /media/salesreturns01.jpg)]". /media/salesreturns01.jpg)  

Zwei Typen Rücklieferungsprozess: Systemtestrücklieferung und nur -kredit.

-   ** Systemtestrücklieferung ** – Die Rücklieferung autorisiert die physische Rücklieferung von Produkten.
-   ** " Nur gutschreiben ** – die Rücklieferung ein Debitorenkredit berechtigt, erfordert jedoch nicht an dem die Rückgabe des Debitors die physisch Produkte.

### <a name="physical-return-order-process"></a>Physischer Rücklieferungsprozess

1.  ** Erstellen einer Rücklieferung. ** Formal Dokument die Autorisierung, damit der Debitor alle fehlerhaften oder unerwünschte Produkten zurückgibt. Die Rückgabe erfordert nicht, ob das Unternehmen die zurückgegebenen Produkte akzeptieren oder einen Habenbetrag für den Debitor angeben. Wenn die Rücklieferungen akzeptiert wird, können Sie einen Ersetzungsartikel zu sendenden, Autorisierung, fehlerhafte, bevor der Artikel zurückgegeben wurde.
2.  ** Um Sie am Lagerort zur Prüfung an. ** Verbinden einer ersten und Prüfung eine Prüfung anhand das Rücklieferungsdokument ab. Die Rückgabe unterstützt außerdem Quarantäne der zurückgelieferten Artikel für zusätzliche Prüfung und Qualitätskontrolle.
3.  ** Bestimmen Sie Disposition. ** Hiermit wird der Prüfungsprozess, Fertigmeldung und geben Sie an, wie mit dem zurückgelieferten Produkte ausgeführt werden soll. Im Rahmen dieses Schritts entscheiden Sie, ob Sie den Debitor Produktrücklieferung gutgeschrieben, die abgelehnt oder angenommen, die Produktrücklieferung verschrotten Sie das Produkt aus, und senden Sie anschließend ein Ersatzprodukt an den Debitor.
4.  ** Generieren Sie einen Lieferschein. ** Generieren Sie einen Lieferschein und die Dispositionsentscheidung fest, die Sie treffen in Schritt 3. Erstellen Sie die Logistikprozesse abgeschlossen.
5.  ** Generieren einer Rechnung. ** Schließen Sie die Rücklieferung.

### <a name="credit-only-process"></a>Schreiben Sie nur Prozess gut

1.  ** Erstellen einer Rücklieferung. ** Formal Dokument die Autorisierung, damit der Debitor einer Gutschrift erhält, ohne fehlerhaften oder unerwünschte Produkten zurückzukehren. ** Der Kredit nur ** Dispositionscode autorisiert die Entscheidung, um den Debitor ohne Systemtestrücklieferung gutzuschreiben.
2.  ** Generieren einer Rechnung. ** Generieren Sie die Gutschrift, und schließen Sie die Rücklieferung.

## <a name="return-material-authorization"></a>Rückholmaterialautorisierung
Rückholmaterial-Autorisierung (RMA),das auf Auftragsfunktionen Builds verarbeitet. Die Rücksendungsnummer wird erfasst als Rücklieferung, die als Auftrag erstellt wird und, kann für einen anderen Auftrag, der ihr zugeordnet ist, einen Ersetzungsauftrag bezeichnet. Beide verknüpfen Aufträge in der Rücksendungsnummer.

-   ** Rücklieferung ** – Eine Rücksendungsnummer, erstellen Sie erfassen eine Rücklieferung, die ein Auftrag ist, der den vorgesehenen Typ hat, ** zurückgegebener Auftrag. ** Alle Änderungen, die Sie an den Rücksendungsinformationen vornehmen, wird automatisch im Auftrag aktualisiert. Die Rücklieferung den Status aufweist ** ** offen, wird sie nicht in der Liste mit den Aufträgen. Rücksendung Sie verwenden, um den Eingang und Zugang der zurückgelieferten Artikel zu verarbeiten, sowie eine Dispositionsaktivität vom Typ " Entlastung nur zu autorisieren (siehe Abschnitt ** Dispositionscodes und Dispositionsaktivitäten **). Alle anderen Folgeprozesse müssen in der Reihenfolge ausgeführt werden.
-   ** ** Ersetzungsauftrag – Wenn ein Wiederbeschaffungsauftrag an den Debitor gesendet werden muss, die Rücksendungsnummer kann einen weiteren zugehörigen Auftrag enthalten. Sie können den manuell Ersetzungsauftrag erstellt, sodass die Rücksendungsnummer umgehende Lieferung unterstützt. Alternativ kann der beim Zugang Ersetzungsauftrag, Prüfung automatisch erstellt werden, und Zugang werden für den Rücksendungspositionsartikel abgeschlossen, der einen Dispositionscode aus, der angibt Ersatz. Der wurde Ersetzungsauftrag die gleichen Funktionen, die einem Auftrag zugeordnet ist. Beispielsweise können Sie die verwenden, um ein benutzerdefiniertes Produkt als der Ersetzungsartikel zu konfigurieren, einen Produktionsauftrag erstellen, eines zurückgelieferten Artikels zu reparierenden, eine Direktlieferungsbestellung Ersatz zu erstellen, die von einem Kreditor übermittelt, oder andere Zwecke zu unterstützen.

## <a name="create-a-return-order"></a>Erstellen einer Rücklieferung
Die Rücklieferungsprozessanfänge Debitorenkontakte wenn Ihre Organisation, einem fehlerhaften oder unerwünschte Produkt zurücksenden und/oder gutgeschrieben werden. Nachdem die Organisation die Rücklieferung, wird bei der Rücklieferung von einer Rücklieferung angegeben. Diese wird Fokuspunkt der Rücklieferung des internen Verarbeitung von zurückgegebenen Produkts. Die folgende Abbildung zeigt die Verfahren zum Erstellen eine Rücklieferung.  

[![Verfahren zum Erstellen einer Rücklieferung] ". /media/salesreturn02.png)]". /media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Erstellen einer Kopfzeile der Rücklieferung erstellen

Bei der Bearbeitung einer Rücklieferung erstellen, müssen die Informationen in der folgenden Tabelle enthalten sein.

| Feld              | Beschreibung                                              | Kommentare                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Debitorenkonto   | Eine Referenz dem Debitorentabelle                       | Sie müssen ein vorhandenen Debitorenkonto angeben.                                                                                                                                                                                                                                                                                                  |
| Lieferadresse   | Die Adresse, an die der Artikel zurückgegeben wird zu                 | Standardmäßig wird die Adresse der Organisation verwendet. Wenn ein bestimmter Lagerort im Kopf aktiviert ist, wird die Lieferadresse auf die Lieferadresse des Lagerorts geändert. Sie können dieser Adresse auf der Rücklieferungsdetails ** ** Seite ändern.                                                                                                  |
| Standort/Lagerort     | Der Standort oder Lagerort zurückgegeben, die das Produkt erhält) | Die Lieferadresse für die Rücklieferung wird die Lieferadresse auf Grundlage des Standorts oder des Lagerorts bestimmt.                                                                                                                                                                                                                                 |
| Rücksendungsnummer         | Die Kennung, die der Rücklieferung zugeordnet ist              | Die Rücksendungsnummer wird als Alternativschlüssel während des Rücklieferungsprozesses verwendet. Die Rücksendungsnummer, die zugewiesen wird, basiert auf dem Rücksendungsnummernummernkreis, der auf der Seite ** Debitorenparameter ** eingerichtet wird.                                                                                                                              |
| Frist           | Das letzte Datum, an dem ein Artikeleingang zurückgegeben werden kann               | Der Standardwert wird als aktuelles Datum zuzüglich den Gültigkeitszeitraum berechnet. Wenn beispielsweise eine Rücklieferung für nur 90 Tagen ab dem Datum gültig ist, an dem die Rücklieferung erstellt wird, und die Rückgabe wurde am 1. Mai, der Wert im Feld lautet 30-July ** ** erstellt. Der Gültigkeitszeitraum ist auf die Debitorenparameter ** ** Seite festgelegt. |
| Ursachencode für Rückgabe | Der Grund des Debitors für die Rückgabe des Produkts          | Der Ursachencode wird in der Liste mit benutzerdefinierten Ursachencodes ausgewählt. Sie können den Wert in diesem Feld jederzeit aktualisieren.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Erstellen Sie Rücklieferungspositionen

Nachdem Sie den abgeschlossen haben, können Sie Rückholkopf Rückgabepositionen erstellen, indem Sie eine der folgenden Methoden:

-   Geben Sie die Nummer manuell die Artikeldetails, die Menge und andere Informationen für jede Rückgabeposition ein.
-   Erstellen einer Rückgabeposition, indem Sie die, ** Suchreihenfolge ** Funktion gruppiert werden. Es wird empfohlen, diese Funktion verwenden, wenn Sie einer Rücklieferung erstellen. ** Die Suchreihenfolge ** Funktion wird eine Referenz aus der Rückgabeposition an der fakturierten Auftragsposition ein und ruft Positionsdetails wie Artikelnummer, Menge, Preis, Rabatt und Kostenwerte aus der Auftragsposition aus. Die Bezugshilfen sicherzustellen, dass, wenn das Unternehmen z Produkt zurückgegeben, wird es an denselben Einheitenkosten bewertet, dass er an verkauft wurde. Die Referenz auch geprüft, dass Rücklieferungen nicht für eine Menge erstellt werden, für die die Menge überschreitet, die in der Rechnung verkauft wurde.

** Hinweis: ** Rückgabepositionen, die eine Referenz zu einem Auftrag haben, werden als Korrekturen oder Rückbuchungen von zu, des Verkaufs behandelt. Weitere Informationen finden Sie unter "Die Buchung erfolgt auf das Sachkonto" Bereich, weiter unten in diesem Thema.

### <a name="charges"></a>Belastungen

Gebühren und Zuschläge können der Rücklieferung von einer oder mehrerer der folgenden Methoden hinzugefügt werden:

-   Sie können Belastungen im Kopf der Rücklieferung, der Rücklieferungsposition oder beides manuell hinzufügen.
-   Belastungen können z der Rücklieferung als Funktion für Rückgabeursachencodes automatisch hinzugefügt werden.
-   Zuschläge können mit einer Rücklieferungsposition, auf der Grundlage des Dispositionscodes der Position automatisch hinzugefügt werden.

Zuschläge werden automatisch hinzugefügt, nachdem ein Rückgaben-/Rücklieferungsursachencode oder ein Dispositionscode der Position zugeordnet ist. Wenn der Ursachencode später geändert wird, wird der vorhandene Zuschlagseintrag nicht entfernt, sondern um einen neuen Zuschlagseintrag kann, auf Grundlage des neuen Ursachencode hinzugefügt werden. Wenn Sie Gebühren Rücklieferungspositionen hinzufügen, Belastungen, die berechnet werden, als Prozentsatz der Position oder Auftragswert negativ werden, wenn die Position bzw. der Positions auftrag negativ, es sei denn, der Prozentsatz auch eine negative Zahl ist. Ein Zuschlag, der einen negativen Wert vorhanden, wird einer Gutschrift an den Debitor angezeigt.

### <a name="return-reason-codes"></a>Ursachencodes für Rückgabe

Mithilfe von Ursachencodes den Rücklieferungen zu übernehmen, können Sie unterstützen, Rückholmuster zu vereinfachen analysieren. Ursachencodes finden Sie Informationen darüber fest, warum ein Debitor für den zurückgelieferten Artikeln wünscht. Einige Organisationen haben zahlreiche Ursachencodes. Dies gruppierte Organisation möglicherweise die Ursachencodegruppen Ursachencodes in, um ein besserer Überblick zu erhalten und kumulierte für - Berichte verwendet.

### <a name="disposition-codes-and-disposition-actions"></a>Dispositionscodes und Dispositionsaktivitäten

Ein wichtiger Schritt im Rücklieferungsprozess ist die Verteilung eines Dispositionscodes zuordnen Rücklieferungsposition als Teil der erfassung Artikelzugangs. Der Dispositionscode bestimmt die folgenden Informationen:

-   ** Die finanziellen Auswirkungen ** – muss der Debitor für die zurückgegebenen Artikel gutgeschrieben werden soll und alle Belastungen der Rücklieferungsposition hinzugefügt werden?
-   ** Die Disposition des zurückgegebenen Artikels ** – Der Artikel kann an Lager hinzugefügte werden soll, sollten sie verschrottet werden oder sollte es an den Debitor zurückgegeben werden?
-   ** Die Funktion des zurückgegebenen Artikels ** – ") Ersetzungsartikel an den Debitor ausgestellt werden?

Zusätzlich zum Bestimmen, wie die zurückgegebenen Güter entsorgt werden, Dispositionscodes Zuschläge können veranlassen, der Rückgabeposition angewendet werden. Sie können auch verwendet werden, um Rücklieferungen zu Zwecken der statistischen Analyse zu gruppieren. Dispositionscodes werden als Teil von Rücklieferungen definiert. Muss jedoch jeder Dispositionscode eine der integrierten Dispositionsaktivitäten verweisen. Die folgende Tabelle zeigt die integrierten Dispositionscodes und ihre Aktivitäten auf. ** Wichtig: ** Wenn ein Artikel nicht zurückgegeben wird, aber der Kunde soll noch gutgeschrieben werden, Zuweisen ** nur den Kredit ** Dispositionscode der Rückgabeposition.

<table>
<thead>
<tr class="header">
<th>Dispositionscode</th>
<th>Finanzielle Auswirkungen</th>
<th>Auswirkungen für Logistik</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nur gutschreiben</td>
<td><ul>
<li>Der Debitor wird der Verkaufspreis minus sämtlicher Gebühren oder Zuschlägen gutgeschrieben.</li>
<li>Verlust von die Verschrottung des Artikels wird im Sachkonto gebucht.</li>
</ul></td>
<td>Der Artikel sollte nicht zurückgegeben werden. Diese Dispositionsaktivität ist für die folgenden Fälle erstellt:
<ul>
<li>Es gibt genügend Vertrauenswürdigkeit unter den Parteien.</li>
<li>Die Kosten des Zurückgebens des fehlerhaften Artikels wurden kostspielig.</li>
<li>Die Artikel können nicht direkt wieder dem Lager zulässig sind. Aufgrund anderen Bedingungen ist eine Systemtestrücklieferung nicht erforderlich.</li>
</ul></td>
</tr>
<tr class="even">
<td>Entlastung</td>
<td><ul>
<li>Der Debitor wird der Verkaufspreis minus sämtlicher Gebühren oder Zuschlägen gutgeschrieben.</li>
<li>Der Lagerwert wird durch die Kosten des zurückgegebenen Artikels erhöht.</li>
</ul></td>
<td>Der Artikel wird zurückgegeben wird und wieder in Lager hinzugefügte.</td>
</tr>
<tr class="odd">
<td>Ersatz und Entlastung</td>
<td><ul>
<li>Der Debitor wird der Verkaufspreis minus sämtlicher Gebühren oder Zuschlägen gutgeschrieben.</li>
<li>Lagerwert wird durch die Kosten des zurückgegebenen Artikels erhöht.</li>
<li>Ein Auftrag separater für eine Ersetzung erstellt wird und wird separat behandelt.</li>
</ul></td>
<td>Der Artikel wird zurückgegeben wird und wieder in Lager hinzugefügte.</td>
</tr>
<tr class="even">
<td>Ersatz und Aussonderung</td>
<td><ul>
<li>Debitor wird den Verkaufspreis, weniger eventuelle Gebühren oder Zuschlägen gutgeschrieben.</li>
<li>Verlust von die Verschrottung des Artikels wird im Sachkonto gebucht.</li>
<li>Ein Auftrag separater für eine Ersetzung erstellt wird und wird separat behandelt.</li>
</ul></td>
<td>Der Artikel zurückgeliefert und verschrottet wird.</td>
</tr>
<tr class="odd">
<td>Rückgabe an den Debitor</td>
<td>Keine, außer für Gebühren oder Zuschlägen.</td>
<td>Der Artikel wird zurückgegeben, jedoch an den Debitor nach Prüfung. Diese Dispositionsaktivität wird unter Umständen verwendet, wenn der Artikel absichtlich beschädigt wurde oder wenn die Gewährleistung storniert wurde.</td>
</tr>
<tr class="even">
<td>Ausschuss</td>
<td><ul>
<li>Der Debitor wird der Verkaufspreis minus sämtlicher Gebühren oder Zuschlägen gutgeschrieben.</li>
<li>Verlust von die Verschrottung des Artikels wird im Sachkonto gebucht.</li>
</ul></td>
<td>Der Artikel zurückgegeben oder verschrottet wird.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Zugang am Lagerort zur Prüfung
Bevor Sie zurückgelieferte Artikel im Lager physisch eingegangene können, indem Sie einen Lieferschein buchen, müssen die Artikel Eingangserfassung und eine optionale Prüfung durchlaufen. Die folgende Abbildung zeigt einen Überblick über. werden Die Abschnitte, die jeden Schritt folgen, beschreiben, der in der Abbildung dargestellt wird.  

[](![Wareneingang . /media/salesreturn03.png)]". /media/salesreturn03.png)  

Der Prozess umfasst mehrere andere Abweichungen, die nicht in diesem Thema abgedeckt werden. Nachfolgend sind einige dieser Abweichungen:

-   Verwenden Sie nicht die Wareneingangsübersicht ** ** Liste, um eine Wareneingangserfassung. Stattdessen Erstellen Sie manuell die Wareneingangserfassung entsprechend. Rücklieferungen haben ** Auftrag ** als die Referenz.
-   Wenn Sie die Lagerortverwaltung verwenden, generieren Sie Palettentransporte. Die Rückgabeposition hat den Status ** angekommen ** während des Palettentransports.
-   Erfassen des Eingangs " Zurückgelieferter Artikel direkt von der Rücklieferungsposition, indem Sie die Erfassung ** ** Funktion gruppiert werden.

Während des werden werden Rücklieferungen mit dem allgemeinen Prozess für Lagerorteingänge integriert. Wareneingang Der unterstützt außerdem die Erstellung von Quarantäneaufträgen für zurückgelieferte Artikel, die eine separate Prüfung durchmachen müssen.

### <a name="identify-products-in-the-arrival-overview-list"></a>Hier können Sie Produkte in der Wareneingangsübersichtliste

** Die Wareneingangsübersicht ** Seite werden alle geplanten eingehenden Wareneingängen auf. ** Hinweis: ** Anzeigen der Rücklieferungen müssen separat verarbeitet werden aus anderen Typen Eingangsbuchungen. Nachdem ein eingehendes Paket für die Wareneingangsübersicht ** ** Seite, (beispielsweise im Rücksendungsdokuments begleitenden), im Aktivitätsbereich, um Anfangseingang ** gekennzeichnet haben ** um eine Wareneingangserfassung zu erstellen und zu initialisieren, die den Zugang übereinstimmt.

### <a name="edit-the-arrival-journal"></a>Bearbeiten Sie die Wareneingangserfassung

Mit der Quarantäneverwaltung ** ** Option Ja ** ** festlegen, können Sie für einen Quarantäneauftrag die Rückgabeposition erstellen. Wenn eine Position dagegen zur Untersuchung in Quarantäne geschickt wurde, können Sie einem Dispositionscode nicht möglich. ** Hinweis: ** Ist die Quarantäneverwaltung ** ** ** Option Ja ** in der Lagersteuerungsgruppe des Artikels, die Quarantäneverwaltung ** ** Option auf der ** Erfassungspositionen ** Seite für die markierten Wareneingangserfassungsposition nicht geändert werden. Wenn die Position in Quarantäne geschickt wird, müssen Sie im jeweiligen Quarantänelagerort angeben. Wenn die Eingangsposition nicht zur Prüfung übermittelt wird, muss der Lagerorteingangssekretär dem Dispositionscode direkt in der Empfangserfassungsposition die Wareneingangserfassung angeben und dann gebucht werden. Wenn der gleiche Dispositionscode nicht auf die gesamte Menge der Rückgabeposition zugewiesen wird oder wenn die gesamte Menge der Position nicht erhalten wurde, muss die Position aufteilen. Wenn Sie diese einer Wareneingangserfassungsposition, zudem der Rückgabeposition (SalesLine **** eine Loskennung ) und neue teilten erstellen. Sie können die Position verteilen, indem Sie die Menge der Empfangserfassungsposition reduzieren. Wenn die Erfassung gebucht ist, wird eine neue, dessen Status erstellt Rückgabeposition ** erwartet ** für die Restmenge hat. Sie können die Position auch aufgeteilt, indem Sie ** Funktionen ** ** &gt; ** Teilen auf klicken.

### <a name="process-the-quarantine-order"></a>Verarbeiten Sie den Quarantäneauftrag

Wenn die zurückgegebenen Produkte zur Prüfung am Quarantänelagerort gesendet werden, wird dennoch das zusätzliche Verarbeitung in einen Quarantäneauftrag abgeschlossen. Ein Quarantäneauftrag wird für jede Eingangsposition erstellt, die in Quarantäne geschickt wird. Der Dispositionscode gibt das Ergebnis des Prüfprozesses an. Sie können einen Quarantäneauftrag aufgeteilt werden, während Sie derzeit die Wareneingangserfassung aufteilbare. Wenn Sie den Quarantäneauftrag aufgeteilt, können entsprechende eine Teilung der Rückgabeposition führen. Nachdem der Dispositionscode eingegeben ist, schließen Sie den Quarantäneauftrag ab, indem Sie entweder die ** Ende ** ** die Funktion oder melden Sie fertig ** Funktion gruppiert werden. Wenn Sie auswählen **, melden Sie die Fertigmeldung ** Personalbeschaffung, wird ein im ausgewählten Lagerort erstellt. Sie können den Eingang dann verarbeiten, indem die Wareneingangsübersicht ** ** Seite. Wenn der Zugang für einen Quarantäneauftrag zurückgeht, können Sie den Standarddispositionscode nicht ändern, der für die Prüfung zugewiesen wird. Wenn Sie den Quarantäneauftrag, die Sie abschließen, indem ** Ende ** Funktion verwenden, wird das Los automatisch erfasst. Manchmal kann ein Artikel aus der Quarantäne zurück an die Versand- und Empfangsabteilung gesendet. Beispielsweise verfügt möglicherweise der Quarantäneprüfer nicht, wo der Artikel im Lager werden. In diesem Fall muss der entsprechende Lieferschein aktualisierten, um nach dem Dispositionscode korrekt zu erfassen und zu bearbeiten, der aufgrund Quarantäne angegeben wird. Empfangsbestätigung kann an den Debitor gesendet werden, wenn der Rückgabeposition erfasst wird. ** Der Rückgabebestätigung ** Bericht ähnelt das Rücklieferungsdokument. ** Rückgabebestätigung ** Der Bericht ist oder erfasst journalisiert nicht anderweitig im System, und es ist kein obligatorischer Schritt im Rücklieferungsprozess.

## <a name="replace-a-product"></a>Ersetzen Sie ein Produkt
Zwei Methoden zum Verwalten die derzeit:

-   ** Ehrliche Ersatz ** – ersetzen Sie ein Produkt zurückgegeben, bevor das Produkt der Debitor erhält.
-   ** Ersatz durch Dispositionscode ** – Erstellen automatisch eine neue Ersetzungsauftragposition.

### <a name="up-front-replacement"></a>Vorabersatz

In der ehrlichen Ersatz kann Ersetzungsartikel der an den Debitor geliefert werden, bevor der Artikel zurückgegeben wird. Diese Methode eignet sich, wenn zum Beispiel der Artikel ein Maschinenteil ist, die nicht entfernt werden kann, es sei denn, dass ein Ersatzteil verfügbar ist, den Ort zu ergreifen oder wenn Sie gerade den Debitor das Ersatzprodukt verfügen soll so schnell wie möglich. Der ehrliche ist ein unabhängiger Ersetzungsauftrag Auftrag. Die Kopfdaten werden vom Debitor initialisiert, und Positionsinformationen werden aus der Rücklieferung initialisiert. Sie können den unabhängig Ersetzungsauftrag der Rücklieferung verarbeitet, bearbeiten und löschen. Wenn Sie einen Ersetzungsauftrag löschen, werden Sie darüber benachrichtigt, dass der Auftrag als Ersetzungsauftrag erstellt wurde. Die folgende Abbildung veranschaulicht den Prozess für ehrliche Ersatz an.  

[ehrlicher Ersetzungsprozess ![https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)!["( https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png) ]  

Die Rückgabe umfasst eine Referenz zum. Ersetzungsauftrag Wenn für ein ehrlicher Ersetzungsauftrag eine Rücklieferung erstellt, bevor der fehlerhaften Artikel zurückgegeben wird, können von Dispositionscodes für Ersatz nicht auswählen, nachdem der fehlerhaften Artikel zurückgegeben wurde.

### <a name="replacement-by-disposition-code"></a>Ersetzung von Dispositionscodes

Wenn Sie einen Wiederbeschaffungsartikel an den Debitor versendet und ** Sie ersetzen Sie und zum Auswählen oder verschrotten ** ** Komponente "und" Entlastung " ** Dispositionsaktivität auf der Rücklieferung werden, verwenden Sie den Prozess, der in der folgenden Abbildung dargestellt wird.  

[![Ersetzungsprozess, wenn ein Dispositionscode verwendet wird( https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)]( https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png) ]  

Der Ersetzungsartikel geliefert wird, indem ein unabhängiger Auftrag den Ersetzungsauftrag, verwendet. Dieser Auftrag wird erstellt, wenn der Lieferschein für die Rücklieferung generiert wird. Der Auftragskopf verwendet Informationen des Debitors, der der Rücklieferung auf den verwiesen wird. Die Positionsinformationen werden aus den Informationen gesammelt, die auf die Seite ** Ersetzungsartikel ** eingegeben wird. ** Die Ersetzungsartikel ** Seite muss vertretene Positionen sein, die Dispositionsaktivitäten haben, die beginnen mit dem Begriff "Ersetzen". Allerdings wird weder die Menge dennoch die Identität des Wiederbeschaffungsartikel geprüft oder abgelehnt. Dieses Verhalten ermöglicht Fälle, in denen der Debitor jedoch den gleichen Artikel in einer anderen Konfiguration oder in eine Größe wünscht, und auch Anfragen zu, in denen Debitoren einen vollständig anderen Artikel wünscht. Standardmäßig wird ein identischer Artikel auf die Seite ** Ersetzungsartikel ** eingegeben. Sie können jedoch einen anderen Artikel auswählen, vorausgesetzt, dass die Funktion eingerichtet wurde. ** Hinweis: ** Den Ersetzungsauftrag Sie können bearbeitet und gelöscht werden, wenn dieser erstellt hat.

## <a name="generate-a-packing-slip"></a>Generieren Sie einen Lieferschein
Bevor zurückgelieferte Artikel im Lager entgegengenommen werden können, muss der Lieferschein für den Auftrag aktualisieren, dass die Artikel gehören. So wie die Rechnungsaktualisierung die Aktualisierung für die Finanzbuchung darstellt, ist die Lieferscheinaktualisierung die physische Aktualisierung des Lagerdatensatzes. Das bedeutet, wird dieser Prozess die Änderungen werden in das Lager übernommen. Bei Retouren werden die der Dispositionsaktivität zugeordneten Schritte bei der Lieferscheinaktualisierung implementiert. Wenn der Lieferschein generieren, folgende Ereignisse treten auf:

-   Am Lagerort ist die Standardmethode verwendet, um einen physischen Beleg auszuführen. Sachkontobuchungen werden generiert, falls die Lagersteuerungsgruppe (** Beitragsphysischer bestand ** ) und die Debitorenparameter (** Buchen von Lieferscheinen im Sachkonto **) werden ordnungsgemäß festgelegt.
-   Artikel, die einer Dispositionsaktivität markiert wurden, die das Wort "Ausschuss" enthält, werden und der Bestandsverlust wird auf das Sachkonto zu Ausschuss.
-   Artikel, die über die markiert wurden ** Rücklieferung zum Debitor ** Dispositionsaktivität, werden an den Debitor geliefert und empfangen. Diese Artikel haben keine Auswirkung auf Lager.
-   Ein Ersetzungsauftrag erstellt wird. Dieser Auftrag basiert auf Informationen zu den Ersetzungsartikel ** ** Seite.

Sie können den Lieferschein nur für Positionen, für den Sie registriert haben den Retourestatus ** **, und nur für die gesamte Menge der Rückgabeposition generieren. Wenn mehrere Positionen auf der Rücklieferung des ** registriert ** Status haben, können Sie den Lieferschein für eine Teilmenge der Positionen generieren, indem Sie die Positionen aus anderen der ** Lieferschein ** Seite löschen. Partielle Rücklieferungen werden in Bezug auf Rücklieferungspositionen, nicht im Bezug auf Rücklieferungen definiert. Wenn also gesamte Menge erhalten, die in einer Rücklieferungsposition angegebene ist, Sie erhalten jedoch kein Artikel aus den anderen Positionen in der Rücklieferung, Lieferung sind keine Teillieferung. Wenn eine Rücklieferungsposition setzt voraus, dass 10 Einheiten eines Artikels zurückgeliefert werden, aber Sie dagegen Einheiten, die Lieferung bilden eine Teillieferung. Wenn nicht alle erwarteten Rückgabeartikel eingegangen sind, können Sie die Lieferung ruhen lassen und auf den Eingang der restlichen zurückgelieferten Menge warten, dass am. Alternativ können Sie die Teillieferung erfassen und buchen. Im Rahmen des Prozesses für das Buchen von Lieferscheinen, kann die Lieferschein-Referenznummer aus den Versanddokumenten des Debitors den Auftragspositionen zugeordnet werden. Diese Zuordnung ist optional und dient lediglich Referenzzwecken Referenz. Sie erstellt führt nicht zu Buchungsaktualisierungen. Im Allgemeinen können Sie den Lieferscheinprozess überspringen und Fakturierung direkt eingeben. In diesem Fall sind die Schritte, die während der Buchung generierung ausgeführt werden, werden bei der Fakturierung abgeschlossen.

## <a name="generate-an-invoice"></a>Rechnung generieren
Obwohl ** die Rücklieferung ** Seite die Informationen und Aktivitäten enthält, die erforderlich sind, um die logistischen besondere Aspekte der Rücklieferung zu können, müssen Sie die Reihenfolge ** ** Seite befindet, ermöglicht den den Fakturierungsprozess abzuschließen. Ihre Organisation kann Rücklieferungen und Aufträge dann gleichzeitig fakturieren, und die gleiche Person kann den den Fakturierungsprozess abschließen, nach Bedarf. Wählen Sie die Rücklieferung aus der ** Auftrag ** Seite anzuzeigen, klicken Sie auf den Link für die Auftragsnummer den zugehörigen Auftrag wird. Sie können die auf der Rücklieferung ** alle Aufträge ** Seite auch finden. Rücklieferungen werden Aufträge, den Auftragstyp haben Sie ** zurückgegebener Auftrag **.

### <a name="credit-correction"></a>Habenkorrektur

Als Teil des Rechnungsstellungsprozesses Überprüft, ob sonstige Zuschläge auf Richtigkeit. Sollen die Sachkontobuchungen zu Korrekturen als Storno bezeichnet () werden, sollten Sie die Option auf ** Kreditkorrektur ** ** andere ** der Registerkarte der Buchungsrechnung ** ** Seite zu verwenden wenn Sie die Rechnung/eine Gutschrift buchen. ** Hinweis: ** Standardmäßig, ist der Habenkorrektur ** ** Option aktiviert, wenn die ** Gutschrift als Korrektur ** Option auf der Seite ** Debitorenparameter ** aktiviert wurde. Es wird jedoch empfohlen, dass Sie nicht Rücklieferungen mit Storno buchen.

## <a name="create-intercompany-return-orders"></a>Erstellen von Intercompany-Rücklieferungen
Rücklieferungen können zwischen zwei Unternehmen innerhalb Ihrer Organisation abgeschlossen werden. Die folgenden Szenarien werden unterstützt:

-   Einfaches Intercompany kehrt zwischen zwei Unternehmen zurück, die in einer Intergesellschaftsrelation teilnehmen
-   Eine Intercompany-Kette, die eingerichtet ist, wenn ein Debitorenrücklieferungsauftrag im verkaufende Unternehmen erstellt wird
-   Eine Intercompany-Kette, die eingerichtet ist, wenn ein Kreditorenrücklieferungsauftrag im das Käuferunternehmen erstellt wird
-   Direktlieferungslieferung kehrt zwischen einem externen Debitor und zwei Unternehmen zurück, die in einer Intergesellschaftsrelation teilnehmen

### <a name="setup"></a>Einstellung

Die folgende Abbildung den erforderlichen Mindesteinstellungen, die erforderlich ist, sodass zwei Unternehmen in einer Intergesellschaftsrelation teilnehmen und den Intercompany-Handel nutzen.  

[![Minimum setup](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)  

Im folgenden Szenario ist das CompBuy kaufende Unternehmen, und CompSell Das verkaufende Unternehmen ist. Normalerweise versendet das Verkaufsunternehmen Waren entweder an das Käuferunternehmen oder niedriger, auf den Direktlieferungslieferungsszenarien, direkt an den Endkunden. In CompBuy wird der Kreditor IS \_als CompSell Intercompany-Endpunkt definiert, der dem Unternehmen CompSell zugeordnet ist. Gleichzeitig in CompSell, wird der Debitor IS \_als CompBuy Intercompany-Endpunkt definiert, der dem Unternehmen CompBuy zugeordnet ist. Die Richtliniendetails und -Wertzuordnungen der geeigneten Schritte muss in beiden Unternehmen definiert werden. In einem Direktlieferungslieferungsszenario wird eine Intercompany-Rücklieferung, die auch ein Intercompany-Auftrag ist, im verkaufende Unternehmen erstellt. Die Rücksendungsnummer der Intercompany-Rücklieferung kann vom Rücksendungsnummernummernkreis in CompSell entnommen werden, oder sie kann aus der Rücksendungsnummer kopiert werden, die der ursprünglichen Rücklieferung im CompBuy zugewiesen wird. Die auf der Rücksendungsnummereinstellungen ** PurchaseRequisition ** Aktivitätsrichtlinie in CompBuy bestimmen diese Aktivitäten. Wenn die Rücksendungsnummer synchronisiert wurde, sollten Sie planen, das von Nummerkonflikten Risiko zu minimieren, wenn die zwei Unternehmen den gleichen Nummernkreis verwenden.

### <a name="simple-intercompany-returns"></a>Einfache Intercompanyrücklieferungen

Dieses Szenario umfasst zwei Unternehmen in derselben Organisation, wie in der folgenden Abbildung dargestellt mit ein.  

[![( einfache Intercompanyrücklieferung![https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)( https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png) ]  

Die kann Auftragskette eingerichtet werden, wenn ein Kreditorenrücklieferungsauftrag im das Käuferunternehmen erstellt wird, oder ein Debitorenrücklieferungsauftrag im verkaufende Unternehmen erstellt wird. Dynamics 365 für Arbeitsgänge erstellt den entsprechenden Auftrag im anderen Unternehmen und wird sichergestellt, dass die Kopf- und Positionsinformationen zum Kreditorenrücklieferungsauftrag die Einstellungen für den Debitorenrücklieferungsauftrag widerspiegeln. Die Rückgabe, die eingerichtet wird, kann die Referenz (entweder ** Suchreihenfolge ** ) zu einer Bestandskunderechnung einbeziehen oder ausschließen. Die Lieferscheinen und Rechnungen der beiden Aufträge können einzeln verarbeitet werden. Sie müssen beispielsweise einen Lieferschein für den Kreditorenrücklieferungsauftrag nicht generieren, bevor Sie den Lieferschein für den Debitorenrücklieferungsauftrag generieren.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Direktlieferungslieferungsrücklieferungen unter drei Parteien

Dieses Szenario kann festgestellt werden, ob ein vorheriger Verkauf des ** Direktlieferung ** Typs abgeschlossen wurde und wenn eine Rechnung für den Debitor im Unternehmen vorhanden ist, das auf den Debitor gesteuert wird. In der folgenden Abbildung ist das Unternehmen CompBuy und zuvor fakturierten Produkte an den Debitor Extern verkauft. Die Produkte direkt wurden vom Unternehmen CompSell an den Debitor zu einer Intercompany-Auftragskette versendet.  

[Direktlieferungslieferung ![zwischen Parteien basierend drei] zurücksetzen( https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)( https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png) ]  

Wenn der Debitor Extern Produkten zurückgeben möchte, wird eine RMA02 (Rücklieferung) für den Debitor im Unternehmen CompBuy erstellt. Um die Intercompany-Kette zu bilden, muss der Rücklieferung für Direktlieferung markiert werden. Bei Verwendung ** Suchreihenfolge **, um die Entnahme zu Debitorenrechnung, um zurück einer Intercompany-Auftragskette, arbeiten, die sich aus den folgenden Dokumenten wird eingerichtet besteht:

-   ** Ursprüngliche Rücklieferung: ** RMA02 (Unternehmen CompBuy)
-   **: Bestellung** PO02 (Unternehmen CompBuy)
-   ** Intercompany-Rücklieferung: ** Rücksendungsnummer \_00032 (Unternehmen CompSell)

Nachdem die Direktlieferungsintercompany-kette erstellt wurde, müssen alle physischen Handhaben und Verarbeiten die Rücklieferungen im Kontext der Rücksendungsnummer Intercompany-Rücklieferung,\_00032\_im Unternehmen CompSell. Die hinzugefügten Produkte können nicht im CompBuy Unternehmen eingehen. Wenn der Dispositionscode ein Intercompany-Rücklieferung zugewiesen ist, besitzt Verwendung mit der ursprünglichen Rücklieferung, korrekte Fakturierung des ursprünglichen Auftrags erstellt synchronisiert.

## <a name="post-to-the-ledger"></a>In das Sachkonto
Die Sachkontobuchungen, die generiert werden, wenn die Rücklieferung fakturiert wird, werden durch verschiedene wichtige Einstellungen und Parameter auswirkt:

-   ** Rücklieferungseinstandspreis ** - für Lagermodelle unterschiedlich ** Standardkosten **, der Rücklieferungseinstandspreis ** ** Parameter bestimmt die Kosten des Artikels, falls er wieder dem Bestand zu Ausschuss oder angenommen hat. Um eine korrekte Bewertung der Lagerbestände zu berechnen, ist es wichtig die Sie legen den ** Rücklieferungseinstandspreis ** Parameter korrekt. Bei Verwendung ** Suchreihenfolge **, um einer Rücklieferungsposition erstellt, die eine Referenz zu einer Debitorenrechnung hat, wird der Rücklieferungseinstandspreis ** ** Wert entspricht dem Einstandspreis des Artikels, der verkauft wird. Andernfalls wird der Einstandspreiswert von den im Artikel oder manuell eingegeben.
-   ** Haben Korrektur/Storno ** – der Habenkorrektur ** ** Parameter auf der Buchungsrechnung ** ** Seite abhängig, ob Buchungen als positive Einträge (DR/CR )erfasst werden sollen, z oder korrigierend, negative Einträge.

In den Beispielen, die zu befolgen sind, wird der Rücklieferungseinstandspreis als Inv ** dargestellt. ** Einstandspreis.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Beispiel 1: Die Rückgabe verweist keine Debitorenrechnung

Die Rückgabe verweist keine Debitorenrechnung. Die zurückgelieferten Artikel erfolgt. ** Kreditkorrektur ** Der Parameter ist nicht aktiviert, wenn die Rücklieferungsrechnung oder Gutschrift, generiert wird.  

[![Rücklieferung enthalten keinen Debitor invoic] (https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png) (https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)]  

** Hinweis: ** Der Artikelmaster-Preis wird als Standardwert für den ** Rücklieferungseinstandspreis ** Parameter verwendet. Der Standardpreis unterscheidet sich von dem Einstandspreis zum Zeitpunkt des Lagerabgangs. Daher ist die Auswirkungen, dass ein Verlust von 3 verursacht wurde. Darüber hinaus enthält die Rücklieferung nicht den Rabatt, dem Debitor im Auftrag der angegeben wurde. Daher wird eine übermäßiger Haben auf.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Beispiel 2: Habenkorrektur ist für die Rücklieferung ausgewählt

Beispiel 2 sind gleich wie beispielsweise 1, aber der Habenkorrektur ** ** Parameter ist aktiviert, wenn die Rücklieferungsrechnung generiert wird.  

[![Rücklieferung, in der ausgewählt Habenkorrektur ist https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)]"( https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png) ]  

** Hinweis: ** Die Sachkontobuchungen werden negative als Korrekturen eingegeben.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Beispiel 3: Die Rücklieferungsposition wird erstellt, indem die Suchenauftragsfunktion verwendet

In diesem Beispiel wird die Rücklieferungsposition erstellt, indem die Suchreihenfolge ** ** Funktion verwendet. ** Kreditkorrektur ** Der Parameter ist nicht aktiviert, wenn die Rechnung erstellt wird.  

[![Rücklieferungsposition, die erstellt wird, indem Suchreihenfolge verwendet]( https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)( https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png) ]  

** Hinweis: ** ** Rabatt ** und ** Rücklieferungseinstandspreis ** werden ordnungsgemäß festgelegt. Aus diesem Grund tritt eine genaue Stornierung auf der Debitorenrechnung.


