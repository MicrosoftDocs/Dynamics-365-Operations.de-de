---
title: Erträge in POS erstellen
description: In diesem Thema wird beschrieben, wie Sie Retouren für Cash-and-Carry-Transaktionen oder Kundenbestellungen in der Microsoft Dynamics 365 Commerce Point-of-Sale-Anwendung (POS) initiieren.
author: hhainesms
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.20
ms.openlocfilehash: c8e06c0d83e3bc2f5efea1e3a8124c700706aa2e
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648987"
---
# <a name="create-returns-in-pos"></a>Erträge in POS erstellen

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Retouren für Cash-and-Carry-Transaktionen oder Kundenbestellungen in der Microsoft Dynamics 365 Commerce Point-of-Sale-App (POS) initiieren.

> [!NOTE]
> In der Commerce-Version 10.0.20 und höher wird eine neue Funktion mit dem Namen **Einheitliche Retourenbearbeitungserfahrung in POS** verfügbar. Diese Funktion bietet einen konsistenteren und einheitlicheren Rückgabeprozess in POS, unabhängig von der Transaktionsart (Barzahlungstransaktion oder Kundenbestellung) oder dem ursprünglichen Kanal, in dem die Bestellung erstellt wurde. Wir empfehlen allen Unternehmen, diese neue Funktion zu aktivieren, um die Gesamtzuverlässigkeit der Retourenabwicklung über POS zu verbessern.
>
> Nachdem die Funktion aktiviert wurde, kann sie nicht mehr deaktiviert werden.

## <a name="process-returns-by-using-the-return-transaction-operation"></a>Verarbeiten von Rückgaben mithilfe der Rückgabetransaktionsoperation

Wir empfehlen, dass Sie die Retourentransaktion zu Ihrem POS-[Bildschirmlayout](pos-screen-layouts.md) hinzufügen. In Versionen vor der Commerce-Version 10.0.20 unterstützt die Retourentransaktionsoperation die Verarbeitung von Retouren nur für Cash-and-Carry-Transaktionen korrekt. Nach dem Einschalten der Funktion **Einheitliche Retourenbearbeitungserfahrung für POS** In der Commerce-Version 10.0.20 oder höher unterstützt die Retourentransaktionsoperation auch die Verarbeitung von Retouren, die aus Kundenaufträgen stammen, wie z. B. bereits fakturierte Bestellungen „Abholung“ oder „Lieferung nach Hause“.

In der Rückgabetransaktionsoperation können Benutzer nach einer Barzahlungstransaktion oder einer Kundenbestellung für die Rückgabe suchen, indem sie eines der folgenden vier Suchkriterien eingeben. Benutzer können diese Kriterien mithilfe einer Gerätetastatur, einer Bildschirmtastatur oder eines Strichcode-Scanners eingeben.

- Eingangskennung
- Bestellnummer
- Kanalreferenz-ID (auch als Auftragsbestätigungs-ID bekannt)
- Rechnungskennung

Wird eine Transaktion oder Bestellung gefunden, die den Suchkriterien entspricht, wird die Seite **retournierbaren Produkte** angezeigt. Dort können Benutzer angeben, welche Artikel zurückgegeben werden. Sie können auch Retourenmengen und Ursachencodes eingeben.

Für jede Bestellposition in der Liste der Rückgabeprodukte zeigt POS Informationen über die ursprüngliche Einkaufsmenge und die Mengen aus allen zuvor bearbeiteten Retouren an. Die Rücksendemenge, die ein Benutzer für eine Auftragsposition eingibt, muss kleiner oder gleich dem Wert im Feld **Zur Rückgabe verfügbar** sein.

![Seite für retournierbare Produkte.](media/returnslist.png)

Wenn ein Benutzer während der Retourenbearbeitung das physische Produkt besitzt und dieses Produkt einen Strichcode hat, kann der Benutzer den Strichcode scannen, um die Rücksendung zu registrieren. Jeder Scan des Barcodes erhöht die Retourenmenge um eine Position. Wenn das Strichcode-Etikett jedoch eine eingebettete Menge enthält, wird diese Menge in das Feld **Wird zurückgegeben** eingegeben.

Benutzer können auch manuell Elemente auswählen, die auf der Seite **Retournierbare Produkte** zurückgegeben werden und aktualisieren dann das Feld **Wird zurückgegeben**, indem Sie den Detailbereich auf der rechten Seite verwenden.

Wenn die maximal verfügbare Menge **Wird zurückgegeben** für eine Transaktion angegeben wird, kann der Benutzer den Vorgang **Alle auswählen** in der POS-App-Leiste auswählen, um die maximale Mehrwegmenge auf allen Positionen einzustellen.

Für jede Position mit einer Menge **Wird zurückgegeben** muss der Benutzer im Detailbereich einen Rückgabegrund auswählen. Bei Rückgaben von Bar- und Mitnahmetransaktionen werden die Rückgabegrundcodes als Infocodes im Funktionsprofil der Filiale konfiguriert. Für Retouren von Kundenbestellungen werden die Retourengrundcodes auf der Seite **Rückgabegrundcodes** in der Dynamics 365 Commerce-Zentralverwaltung konfiguriert.

Nachdem die Rücksendemenge und der Ursachencode für jeden zurückzusendenden Artikel festgelegt wurden, kann der Benutzer die Option **Rückgabe** in der POS-App-Leiste auswählen, um mit der Verarbeitung fortzufahren. Es erscheint die POS-Transaktionsseite, auf der die auf der vorherigen Seite ausgewählten retournierbaren Artikel in den Warenkorb gelegt wurden. Die Mengen **Wird zurückgegeben** für die Artikel erscheinen als negative Mengenzeilen in der Transaktion, und die Gesamtrückerstattung wird berechnet.

Benutzer können einer Rücksendetransaktion Positionen hinzufügen, wenn sie einen Umtauschauftrag erstellen. Benutzer können einer Retourentransaktion auch weitere Ad-hoc-Rückgabeartikel hinzufügen, indem sie den Vorgang **Produkt zurückgeben** für eine ausgewählte Verkaufszeile mit positiver Menge verwenden, die hinzugefügt wurde.

> [!NOTE]
> Der POS-Vorgang **Produkt zurückgeben** bietet keine Validierung gegenüber einer ursprünglichen Transaktion und ermöglicht die Rückgabe jedes Produkts. Daher empfehlen wir, dass nur autorisierte Benutzer diesen Vorgang ausführen dürfen oder dass eine Managerüberschreibung erforderlich ist, wenn dieser Vorgang verwendet wird.

Wenn eine Rückerstattung an der Kasse fällig ist, können Organisationen [Rückerstattungsrichtlinien](refund_policy_returns.md) konfigurieren, die die Zahlungsmethoden einschränken, die zur Rückerstattung von Kunden verwendet werden können. Wenn die ursprüngliche Transaktion mit einer Kreditkarte bezahlt wurde, haben Benutzer je nach Zahlungsabwickler und Systemkonfiguration möglicherweise die Möglichkeit, [eine Rückerstattung auf die ursprüngliche Karte auszustellen](dev-itpro/linked-refunds.md). In diesem Fall kann die Rückerstattung bearbeitet werden, ohne dass der Kunde seine Kreditkarte erneut durchziehen muss. Das ursprüngliche Zahlungstoken wird verwendet, um die Rückerstattung zu veranlassen.

## <a name="other-return-options-in-pos"></a>Andere Rückgabemöglichkeiten im POS

Wenn die Funktion **Einheitliche Retourenbearbeitungserfahrung in POS** aktiviert ist, können Benutzer auch den Vorgang **Erfassung anzeigen** im POS verwenden, um eine Retoure für eine Cash-and-Carry-Transaktion oder eine Kundenbestellung auszulösen. Sie können dann eine Transaktion in der Erfassung auswählen und dann den Vorgang **Rückgabe** in der POS-App-Leiste auswählen. Dieser Vorgang ist nur verfügbar, wenn der Auftrag retournierbare Positionen enthält. Es initiiert die gleiche Benutzererfahrung wie der Vorgang **Retourenbuchung**.

Benutzer können auch den Vorgang **Auftrag zurückrufen** im POS zum Suchen und Abrufen von Kundenaufträgen verwenden. (Dieser Vorgang kann nicht für Cash-and-Carry-Transaktionen verwendet werden). In diesem Fall wird nach Auswahl eines Kundenauftrags der Vorgang **Rückgabe** über die POS-App-Leiste ausgewählt, kann eine Retoure für die Kundenbestellung veranlasst werden. Dieser Vorgang ist nur verfügbar, wenn der Auftrag retournierbare Positionen enthält. Es initiiert die gleiche Benutzererfahrung wie der Vorgang **Retourenbuchung** oder **Erfassung anzeigen**.

## <a name="return-orders-are-posted-to-commerce-headquarters-as-sales-orders"></a>Rücklieferungen werden als Kundenaufträge an die Commerce-Zentralverwaltung gebucht 

Wenn die Funktion **Einheitliche Retourenbearbeitungserfahrung in POS** aktiviert ist, werden alle in POS erstellten Retouren als Kundenaufträge mit negativen Zeilen an die Commerce-Zentralverwaltung geschrieben. In Versionen vor der Veröffentlichungder Commerce-Version 10.0.20 können Benutzer auswählen, ob Retouren als Kundenaufträge mit negativen Zeilen gebucht werden sollen oder ob es sich um Retouren handelt, die durch den Prozess der Warenrücksendung (RMA) erstellt werden. 

In der Funktion **Einheitliche Retourenbearbeitungserfahrung in POS** wurde die Option, den RMA-Prozess zum Erstellen von Retouren in POS zu verwenden, eingestellt. Nachdem diese Funktion aktiviert ist, werden alle Retouren als Kundenaufträge mit negativen Positionen erstellt.

## <a name="offline-return-processing-improvements"></a>Verbesserungen bei der Offline-Rücksendungsverarbeitung

In den meisten Fällen versucht das System, wenn eine Retoure im POS verarbeitet wird, einen Echtzeit-Service-Aufruf (RTS) an die Commerce-Zentralverwaltung zu senden, um die aktuellen Mengen zu überprüfen, die für die Retoure verfügbar sind. Diese Validierung hilft, betrügerische Szenarien zu vermeiden, in denen ein Kunde versucht, denselben Artikel an mehreren Standorten zurückzugeben.

Um Situationen zu handhaben, in denen der RTS-Aufruf aufgrund von Netzwerk- oder Konnektivitätsproblemen nicht durchgeführt werden kann, wurde ein Prozess eingeführt, um die Rücksendemengendaten von der Commerce-Zentralverwaltung regelmäßig mit der Kanaldatenbank eines Geschäfts zu synchronisieren. Dieses kanalseitige Retouren-Tracking trägt dazu bei, dass die **zur Rückgabe verfügbaren** Mengen, die in POS angezeigt werden, einigermaßen genau sind, auch wenn POS offline ist. Es stellt auch sicher, dass POS weiterhin die kanalseitigen Informationen validieren kann, um betrügerische Rücksendungen zu verhindern.

Um den Offline-Rückgabeprozess in geeigneter Weise zu nutzen, sollten Organisationen den Stapelverarbeitungsauftrag **Retourenmengen aktualisieren** in der Commerce-Zentralverwaltung planen, damit er häufig ausgeführt wird. Wir empfehlen, dass dieser Job mit der gleichen Häufigkeit ausgeführt wird wie der P-Job, der neue Transaktionen von Commerce-Kanälen in die Commerce-Zentrale zieht.

Der Einzelvorgang **Retourenmengen aktualisieren** berechnet die zur Rückgabe verfügbare Menge für alle Kundenaufträge, die sich in der Commerce-Zentralverwaltung befinden. Die vom Job berechneten Daten müssen dann an Kanaldatenbanken gesendet werden, damit die Filialkanäle aktualisiert werden können. Der Verteilungsauftrag **Retourenmengen** (1200) wird zu diesem Zweck verwendet. Da die Daten über die Rückgabemenge von der Commerce-Zentralverwaltung synchronisiert werden, kann POS, wenn eine Retoure in POS verarbeitet wird, aber der RTS-Aufruf nicht durchgeführt werden kann, die kanalseitigen Retoureninformationen verwenden, um die **zur Rückgabe verfügbaren** Mengen für eine bestimmte Verkaufszeile verwenden.

Wenn keine RTS-Aufrufe getätigt werden können und POS kanalseitige Daten für die Rückgabevalidierung verwendet, informiert eine Warnmeldung die Benutzer darüber, dass sie eine „Offline“-Rücksendung erstellen. Daher sind sie sich bewusst, dass die **zur Rückgabe verfügbare** im POS angezeigte Menge möglicherweise veraltet und nicht mehr korrekt ist, je nachdem, wann der Einzelvorgang **Retourenmengen aktualisieren** zuletzt verarbeitet und mit dem Kanal synchronisiert wurde.

Beispiel: Ein Kunde hat kürzlich eine Retoure für eine Bestellposition in einem anderen Kanal bearbeitet, aber diese Daten wurden noch nicht über den Kanal **Retourenmengen aktualisieren** mit den Kanaldatenbanken synchronisiert. Der Kunde geht dann in ein anderes Geschäft und versucht den gleichen Artikel erneut zurückzugeben. Wenn das Geschäft in diesem Fall den RTS-Anruf an die Commerce-Zentrale nicht durchführen kann, um Echtzeit-Rückgabedaten abzurufen, lässt POS die erneute Rückgabe des Artikels zu. Der Benutzer wird jedoch gewarnt, dass die Informationen, die zur Validierung der Rückgabe verwendet werden, möglicherweise veraltet sind. Die Nachricht, die der Benutzer erhält, ist nur eine Warnmeldung. Es hindert den Benutzer nicht daran, die Rücksendung weiter zu bearbeiten.

Wenn die kanalseitigen Informationen aus irgendeinem Grund nicht aktuell sind und eine Offline-Rücksendung für eine Menge verarbeitet wird, die die tatsächliche **zur Rückgabe verfügbare** Menge überschreitet, kann ein Fehler generiert werden, wenn die Kontoauszugsbuchung ausgeführt wird, um die Transaktion in der Commerce-Zentralverwaltung zu erstellen.

> [!NOTE]
> Wenn die Funktion **Einheitliche Retourenbearbeitungserfahrung in POS** aktiviert ist, stehen neue optionale Funktionen zur Verfügung, die die Validierung von Produktrücksendungen mit Seriennummer unterstützen. Weitere Informationen finden Sie unter [Seriennummergesteuerte Produkte am Point of Sale (POS) zurückgeben](POS-serial-returns.md).

## <a name="version-details"></a>Versionsdetails

Die folgende Liste enthält die Mindestversionsanforderungen für die verschiedenen Komponenten.
- Commerce-Zentrale: Version 10.0.20
- Commerce Scale Unit (CSU): Version 9.30
- Point of Sale (POS): Version 9.30

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Richtige Steuerberechnung für Retouren mit Teilmengen aktivieren

Diese Funktion stellt sicher, dass bei der Retoure eines Auftrags über mehrere Rechnungen die Steuern letztendlich dem ursprünglich berechneten Steuerbetrag entsprechen.

1. Suchen Sie im Arbeitsbereich **Funktionsverwaltung** nach **Richtige Steuerberechnung für Retouren mit Teilmengen aktivieren**.
1. Wählen Sie die Funktion **Richtige Steuerberechnung für Retouren mit Teilmengen aktivieren** und dann **Aktivieren** aus.

## <a name="set-up-return-locations-for-retail-stores"></a>Rückgabeorte für Einzelhandelsgeschäfte einrichten

Mit Commerce können Sie Rückgabeorte einrichten, die auf Einzelhandels-Infocodes und Vertriebs- und Marketingursachencodes basieren. Kassierer geben häufig den Grund für die Rückgabe an, wenn Kunden Einkäufe zurückgeben. Sie können festlegen, dass zurückgegebene Produkte verschiedenen Rückgabeorten im Bestand zugewiesen werden sollen, basierend auf Infocodes und Ursachencodes, die Kassierer am POS-Register auswählen.

Beispiel: Ein Kunde gibt ein defektes Produkt zurück, und der Kassierer bearbeitet die Retourenbuchung. Wenn Retail POS den Infocode für Retouren anzeigt, wählt der Kassierer den Untercode für fehlerhafte Retouren aus. Das zurückgegebene Produkt wird dann automatisch einem bestimmten Rückgabeort zugewiesen.

Ein Rückgabeort kann ein Lagerort, ein Lagerplatz in einem Lagerort oder auch eine bestimmte Palette sein, abhängig von den Lagerplätzen für Lagerbestände, die Ihre Organisation eingerichtet hat. Sie können jeden Rückgabeort einem oder mehreren Einzelhandels-Infocodes und Vertriebs- und Marketingursachencodes zuordnen.

### <a name="prerequisites"></a>Voraussetzungen

Bevor Sie Rückgabeorte einrichten können, müssen Sie die folgenden Elemente einrichten:

- **Einzelhandels-Infocodes** – Aufforderungen am POS-Register, die im **Einzelhandel**-Modul eingerichtet werden. Weitere Informationen finden Sie unter [Einrichten von Infocodes](/dynamicsax-2012/appuser-itpro/setting-up-info-codes).
- **Vertriebs- und Marketingursachencodes** – Aufforderungen am POS-Register, die im **Vertrieb und Marketing**-Modul eingerichtet werden. Weitere Informationen finden Sie unter [Einrichten von Ursachencodes](/dynamicsax-2012/appuser-itpro/set-up-return-reason-codes).
- **Lagerplätze für Lagerbestand** – Die Orte, an denen Lagerbestand aufbewahrt wird. Weitere Informationen finden Sie unter [Einrichten von Lagerplätzen für Lagerbestand](/dynamicsax-2012/appuser-itpro/about-locations).
    
### <a name="set-up-return-locations"></a>Rückgabeorte einrichten

Gehen Sie zum Einrichten von Rückgabeorten folgendermaßen vor.

1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellungen \> Lagerorte**, und wählen Sie einen Lagerort aus.
1. Wählen Sie auf dem Inforegister **Einzelhandel** im Feld **Standard-Rückgabeort** den Lagerplatz für den Lagerbestand aus, der für Rückgaben verwendet werden soll, wenn die Infocodes oder Ursachencodes keinen Rückgabeorten zugeordnet sind.
1. Wählen Sie im Feld **Standardrücklieferungspalette** die Palette aus, die für Rückgaben verwendet werden soll, wenn die Infocodes oder Ursachencodes keinen Rückgabeorten zugeordnet sind.
1. Gehen Sie zu **Einzelhandel und Handel \> Lagerverwaltung \> Rückgabeorte**.
1. Wählen Sie **Neu** aus, um eine Rückgabeortrichtlinie zu erstellen.
1. Geben Sie einen eindeutigen Namen und eine Beschreibung für den Rückgabeort ein.

    > [!NOTE]
    > Wenn ein Nummernkreis für Rückgabeorte eingerichtet wurde, wird der Name automatisch eingegeben.

1. Legen Sie auf dem Inforegister **Allgemein** die Option **Etiketten drucken** auf **Ja** fest, um Etiketten für alle Produkte zu drucken, die Rückgabeorten zugewiesen sind.
1. Legen Sie die Option **Lagerbestand sperren** auf **Ja** fest, um zurückgegebene Produkte im Standard-Rückgabeort aus dem Bestand zu nehmen und zu verhindern, dass sie verkauft werden.
1. Gehen Sie wie folgt vor, um bestimmte Einzelhandels-Infocodes und Untercodes Rückgabeorten zuzuordnen:

    1. Wählen Sie auf dem Inforegister **Einzelhandels-Infocodes** **Hinzufügen**.
    1. Wählen Sie im Feld **Infocode** einen Infocode für Rückgaben aus.
    1. Wählen Sie im Feld **Untercode** einen Untercode für den Grund für die Rückgabe aus. Das Feld **Beschreibung** zeigt die Beschreibung für den ausgewählten Untercode.
    1. Wählen Sie im Feld **Store** den Shop aus, in dem der Infocode verwendet wird.
    1. Verwenden Sie die Felder **Lagerort**, **Lagerplatz** und **Palettennummer**, um einen Rückgabeort anzugeben. Um beispielsweise einen bestimmten Ort in einem Shop anzugeben, wählen Sie einen Shop im Feld **Store** und einen Ort im Feld **Lagerplatz** aus.
    1. Aktivieren Sie das Kontrollkästchen **Lagerbestand sperren**, um zurückgegebene Produkte aus dem Bestand zu nehmen und um zu verhindern, dass sie verkauft werden.

1. Gehen Sie wie folgt vor, um bestimmte Vertriebs- und Marketingursachencodes Rückgabeorten zuzuordnen:

    1. Auf dem Inforegister **Vertriebs- und Marketingursachencodes** wählen Sie **Hinzufügen** aus.
    1. Wählen Sie im Feld **Ursachencode** einen Ursachencode für Rückgaben aus. Das Feld **Beschreibung** zeigt die Beschreibung für den ausgewählten Ursachencode.
    1. Wählen Sie im Feld **Store** den Shop aus, in dem der Ursachencode verwendet wird.
    1. Verwenden Sie die Felder **Lagerort**, **Lagerplatz** und **Palettennummer**, um einen Rückgabeort anzugeben. Um beispielsweise eine Palette an einem Ort in einem Lagerort anzugeben, wählen Sie einen Lagerort im Feld **Lagerort** aus, einen Ort im Feld **Lagerplatz** und eine Palette im Feld **Palettennummer**.
    1. Aktivieren Sie das Kontrollkästchen **Lagerbestand sperren**, um zurückgegebene Produkte aus dem Bestand zu nehmen und um zu verhindern, dass sie verkauft werden.

    > [!NOTE]
    > Wenn für einen Artikel eine Rückgabeortrichtlinie verwendet wird, der Rückgabegrund, den ein Kassierer auswählt, jedoch mit keinem Code übereinstimmt, der auf dem Inforegister **Einzelhandel-Infocodes** oder **Vertriebs- und Marketingursachencodes** angegeben ist, wird der Artikel an den Standardrückgabeort gesendet, der auf der Seite **Lagerort** definiert ist. Außerdem bestimmt die Einstellung des Kontrollkästchens **Lagerbestand sperren** auf dem Inforegister **Allgemein** der Seite **Rückgabeorte**, ob der zurückgegebene Artikel im Bestand gesperrt werden soll.

1. Gehen Sie zu **Einzelhandel und Handel \> Handelsprodukthierarchie**.
1. Wählen Sie auf dem Inforegister **Bestandskategorieeigenschaften verwalten** im Feld **Rückgabeort** einen Rückgabeort aus. Da für dasselbe Geschäft mehrere Rückgabeortrichtlinien definiert werden können, bestimmt der Wert, den Sie hier auswählen, die verwendete Rückgabeortrichtlinie.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Seriennummergesteuerte Produkte am Point of Sale (POS) zurückgeben](POS-serial-returns.md)

[Verknüpfte Rückerstattungen von zuvor genehmigten und bestätigten Transaktionen](dev-itpro/linked-refunds.md)

[Retouren- und Rückerstattungsrichtlinie für einen Kanal erstellen und aktualisieren](refund_policy_returns.md)

[Visuelle Konfigurationen der POS-Benutzeroberfläche](pos-screen-layouts.md)
