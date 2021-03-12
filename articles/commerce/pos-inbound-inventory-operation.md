---
title: Eingangsbestandsvorgang in POS
description: Dieses Thema beschreibt die Möglichkeiten des POS-Eingangsbestandsvorgangs (POS).
author: hhaines
manager: annbe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: f3dd442f979c23a87ae4b7e69a37de65d5d9bd70
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972629"
---
# <a name="inbound-inventory-operation-in-pos"></a>Eingangsbestandsvorgang in POS

[!include [banner](includes/banner.md)]

In Microsoft Dynamics 365 Commerce Version 10.0.10 und höher ersetzen Ein- und Ausgangsvorgänge am POS (Point of Sale) den Kommissionier- und Empfangsvorgang.

> [!NOTE]
> In der Commerce-Version 10.0.10 und später werden alle neuen Funktionen in der POS-Anwendung, die sich auf den Empfang von Filialbeständen gegen Bestellungen und Transportaufträge beziehen, zum **Eingangsvorgang** POS-Vorgang hinzugefügt. Wenn Sie derzeit den Kommissionier- und Empfangsvorgang in der POS-Anwendung verwenden, empfehlen wir Ihnen, eine Strategie für den Übergang von diesem Vorgang zu den neuen Eingangs- und Ausgangsvorgängen zu entwickeln. Obwohl der Kommissionier- und Wareneingangsvorgang nicht aus dem Produkt entfernt wird, werden ab Version 10.0.9 keine weiteren Investitionen in das Produkt getätigt, weder aus funktionaler noch aus leistungsbezogener Sicht.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Voraussetzung: Konfigurieren Sie ein asynchrones Dokumenten-Framework.

Der Eingangsvorgang umfasst Leistungsverbesserungen, um sicherzustellen, dass Benutzer, die ein hohes Volumen an Eingangsbuchungen in vielen Filialen oder Unternehmen und große Bestandsbelege haben, diese Belege ohne Zeitüberschreitungen oder Ausfälle an Commerce Headquarters verarbeiten können. Diese Verbesserungen erfordern die Verwendung eines asynchronen Dokumenten-Frameworks.

Wenn ein asynchrones Belegframework verwendet wird, können Sie Eingangsbelegänderungen vom POS an Commerce Headquarters übergeben und dann zu anderen Aufgaben übergehen, während die Verarbeitung an Commerce Headquarters im Hintergrund erfolgt. Sie können den Status eines Belegs über die **Eingangsvorgang**-Belegliste in der POS-Abteilung überprüfen, um sicherzustellen, dass die Buchung erfolgreich war. In der POS-Anwendung können Sie auch die Belegliste der Eingangsoperation aktiv verwenden, um alle Belege zu sehen, die nicht an Commerce Headquarters gebucht werden konnten. Wenn ein Beleg fehlschlägt, können POS-Benutzer Korrekturen an ihm vornehmen und dann erneut versuchen, ihn an Commerce Headquarters zu verarbeiten.

> [!IMPORTANT]
> Das asynchrone Belegframework muss konfiguriert werden, bevor ein Unternehmen versucht, die Eingangsoperation in der POS-Anwendung zu verwenden.

Um ein asynchrones Belegframework zu konfigurieren, führen Sie die folgenden Verfahren durch.

### <a name="create-and-configure-a-number-sequence"></a>Erstellen und konfigurieren Sie eine Zahlenfolge

1. Gehen Sie zu **Organisationsverwaltung \> Nummernkreis \> Nummernkreise**.
2. Erstellen Sie auf der Seite **Nummernkreise** einen Nummernkreis.
3. Geben Sie in die Felder **Nummernkreiscode** und **Name** benutzerdefinierte Werte ein.
4. Wählen Sie auf dem Inforegister **Referenzen** **Hinzufügen**.
5. Im Feld **Bereich** wählen Sie **Commerce-Parameter**.
4. Wählen Sie im Feld **Referenz** **Dokumentvorgangskennung**.
5. Setzen Sie im Inforegister **Allgemein** im Abschnitt **Einrichten** die Option **Kontinuierlich** auf **Nein**, um sicherzustellen, dass es keine Leistungsprobleme gibt.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Erstellen und planen Sie zwei Batch-Jobs für die Dokumentverarbeitung und die Überwachungsaufgaben

> [!NOTE]
> In Commerce Version 10.0.13 und höher müssen Sie diese Stapeljobs nicht über das Stapeljob-Framework konfigurieren. Die Stapelverarbeitungsvorgänge können über das Menü **Retail and Commerce >Retail and Commerce IT** konfiguriert werden. Verwenden Sie die Menüoptionen **Überwachung für den Betrieb von Einzelhandelsdokumenten** und **Verarbeitung von Einzelhandelsdokumenten** zum Konfigurieren der Stapeljobs.

Die von Ihnen erstellten Batch-Jobs werden zur Verarbeitung von Dokumenten verwendet, die fehlschlagen oder ein Time-Out aufweisen. Sie werden auch verwendet, wenn die Anzahl der aktiven Bestandsbelege, die von der Kasse aus verarbeitet werden, einen vom System konfigurierten Wert überschreitet.

1. Gehen Sie zu **Systemverwaltung \> Anfragen \> Batch-Jobs**.
2. Legen Sie auf der Seite **Batch-Job** zwei Batch-Jobs an:

    - Konfigurieren Sie einen Job für die Ausführung der Klasse **RetailDocumentOperationMonitorBatch**.
    - Konfigurieren Sie den anderen Job so, dass er die Klasse **RetailDocumentOperationProcessingBatch** ausführt.

2. Planen Sie die neuen Batch-Jobs so ein, dass sie wiederkehrend ausgeführt werden. Stellen Sie den Zeitplan z.B. so ein, dass die Jobs alle fünf Minuten ausgeführt werden.

## <a name="prerequisite-add-inbound-operation-to-the-pos-screen-layout"></a>Voraussetzung: Hinzufügen des Eingangsvorgangs zum POS-Bildaufbau

Bevor Ihr Unternehmen die Eingangsoperationsfunktionalität nutzen kann, muss es die **Eingangsoperation** POS-Operation auf einem oder mehreren Ihrer [POS-Bildlayouts](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) konfigurieren. Bevor Sie den neuen Vorgang in einer Produktionsumgebung einsetzen, sollten Sie ihn gründlich testen und Ihre Benutzer in der Verwendung schulen.

## <a name="overview"></a>Übersicht

Die Eingangsoperation ermöglicht es den POS-Benutzern, die folgenden Aufgaben durchzuführen:

- Empfang von Bestand in den Filialbestand entweder aus bestätigten Bestellbelegen oder aus versandten Transportauftragsbelegen.
- Informationen über historische Bestandszugänge für einen Zeitraum von sieben Tagen nach dem vollständigen Eingang des Belegs anzeigen.
- Neue eingehende Transportauftragsanforderungen erstellen.

Wenn der Eingangsvorgang von der POS-Anwendung aus gestartet wird, erscheint eine Listenseitenansicht. Diese Ansicht zeigt offene Bestell- und Transportauftragsbelege mit Bestandszeilen, die für den Eingang in der aktuellen Filiale vorgesehen sind. Um einen bestimmten Beleg zu finden und auszuwählen, können Benutzer die Liste durchblättern oder die Suchfunktion verwenden.

Die Liste der eingehenden Bestandsbelege hat drei Registerkarten:

- **Aktiv** - Auf dieser Registerkarte werden Belege angezeigt, die ganz oder teilweise geöffnet sind und Zeilen oder Mengen auf Zeilen enthalten, die noch empfangen werden müssen.
- **Entwurf** - Auf dieser Registerkarte werden neue eingehende Transportauftragsanforderungen angezeigt, die die Filiale erstellt hat. Die Belege wurden jedoch nur lokal gespeichert. Sie wurden noch nicht zur Bearbeitung an Commerce Headquarters übermittelt.
- **Abschließen** - Diese Registerkarte zeigt eine Liste von Bestell- oder Transportauftragsbelegen, die die Filiale in den letzten sieben Tagen vollständig erhalten hat. Diese Registerkarte dient nur zu Informationszwecken. Alle Informationen zu den Belegen sind schreibgeschützte Daten für die Filiale.

Wenn Sie Dokumente auf einer der Registerkarten anzeigen, kann das Feld **Status** Ihnen helfen, den Status des Dokuments zu verstehen.

- **Entwurf** - Das Transportauftragsdokument wurde nur lokal in der Kanaldatenbank der Filiale gespeichert. Es wurden noch keine Informationen über den Transportauftragsantrag an Commerce Headquarters übermittelt.
- **Anforderung** - Die Bestellung oder der Transportauftrag wurde in Commerce Headquarters angelegt und ist vollständig geöffnet. Es wurden noch keine Belege für den Beleg verarbeitet. Für Dokumente der Belegart Bestellung kann der Empfang jederzeit beginnen, solange der Status **Beantragt** ist.
- **Teilweise versandt** - Der Transportauftragsbeleg hat eine oder mehrere Zeilen oder Teilzeilenmengen, die als vom Ausgangslager versandt gebucht wurden. Diese versandten Zeilen können über den Eingangsvorgang empfangen werden.
- **Vollständig versandt** - Der Transportauftrag wurde mit allen Zeilen und vollen Zeilenmengen als vom Auslieferungslager versandt gebucht. Das gesamte Dokument steht für den Empfang über den Eingangsvorgang zur Verfügung.
- **Teilweise empfangen** - Einige der Zeilen oder Zeilenmengen auf dem Bestell- oder Transportauftragsbeleg sind in der Filiale eingegangen, aber einige Zeilen bleiben offen.
- **Vollständig empfangen** - Alle Zeilen und Mengen auf dem Bestell- oder Transportauftragsbeleg sind vollständig empfangen worden. Die Belege sind nur auf der Registerkarte **Vollständig** zugänglich und für Filialbenutzer schreibgeschützt.
- **In Bearbeitung** - Dieser Status wird verwendet, um Gerätebenutzer darüber zu informieren, dass der Beleg von einem anderen Benutzer aktiv bearbeitet wird.
- **Pausiert** - Dieser Status wird angezeigt, nachdem **Empfang pausieren** gewählt wurde, um den Empfangsvorgang vorübergehend zu stoppen.
- **Bearbeitung in HQ** - Das Dokument wurde von der POS-Anwendung an Commerce Headquarters übermittelt, aber es wurde noch nicht erfolgreich an Commerce Headquarters gesendet. Der Beleg durchläuft gerade den asynchronen Belegverbuchungsprozess. Nachdem der Beleg erfolgreich an Commerce Headquarters gebucht wurde, sollte sein Status auf **Vollständig erhalten** oder **Teilweise erhalten** aktualisiert werden.
- **Verarbeitung fehlgeschlagen** - Das Dokument wurde an Commerce Headquarters gebucht und abgelehnt. Der Bereich **Details** zeigt den Grund für das Fehlschlagen der Buchung. Der Beleg muss bearbeitet werden, um Datenprobleme zu beheben, und dann erneut zur Verarbeitung an Commerce Headquarters geschickt werden.

Wenn Sie eine Belegzeile in der Liste auswählen, erscheint ein Fenster **Details**. Dieser Bereich zeigt zusätzliche Informationen über den Beleg an, wie z.B. Transport- und Datumsinformationen. Ein Fortschrittsbalken zeigt an, wie viele Positionen noch bearbeitet werden müssen. Wenn der Beleg nicht erfolgreich an Commerce Headquarters verarbeitet wurde, zeigt der Bereich **Details** auch Fehlermeldungen an, die mit dem Fehler zusammenhängen.

In der Seitenansicht der Dokumentliste können Sie in der Anwendungsleiste **Details** wählen, um die Dokumentdetails anzuzeigen. Sie können auch die Eingangsverarbeitung für berechtigte Belegzeilen aktivieren.

In der Seitenansicht der Belegliste können Sie auch eine neue eingehende Transportauftragsanforderung für eine Filiale anlegen. Die Belege bleiben im Status **Entwurf** und können angepasst oder gelöscht werden, bis sie zur Bearbeitung an Commerce Headquarters übermittelt werden. Nachdem sie an Commerce Headquarters übermittelt wurden, können die Transportauftragszeilen nicht mehr von der POS-Anwendung aus geändert werden.

## <a name="receiving-process"></a>Eingangsprozess

Nachdem Sie eine Bestellung oder einen Transportauftragsbeleg auf der Registerkarte **Aktiv** ausgewählt haben, können Sie **Bestelldetails** wählen, um den Empfangsvorgang zu starten.

Standardmäßig wird die Ansicht **Empfang jetzt** angezeigt. Diese Ansicht ist für das Scannen von Barcodes optimiert. Sie kann verwendet werden, um eine Liste der gescannten Artikel zu erstellen, sodass diese Artikel empfangen werden können. Um den Empfangsvorgang zu beginnen, können Sie mit dem Scannen von Artikel-Barcodes beginnen.

Wenn Artikel-Barcodes in der Ansicht **Empfang jetzt** gescannt werden, validiert die Anwendung die Artikel gegen den ausgewählten Einkaufs- oder Transportauftragsbeleg, um sicherzustellen, dass jeder gescannte Artikel einem gültigen Artikel auf dem Beleg entspricht. In der Ansicht **Empfang jetzt** wird bei jedem Scannen eines Barcodes davon ausgegangen, dass es sich um den Empfang einer Menge von einer Einheit handelt, es sei denn, im Barcode ist eine Menge eingebettet. Sie können in dieser Ansicht wiederholt Strichcodes scannen, um eine Liste aller Artikel und Mengen für den Empfang zu erstellen.

### <a name="example-scenario"></a>Beispielszenario

Ein Benutzer erhält eine Bestellung, die 10 Einheiten des Barcodes 5657900266 enthält. Der Benutzer kann diesen Barcode 10 Mal scannen, um das Feld **Jetzt empfangen** um eine Einheit pro Scan zu aktualisieren. Wenn der Benutzer die Scans abgeschlossen hat, zeigt das Feld **Jetzt empfangen** für die Zeile des Artikels an, dass eine Menge von 10 Stück eingegangen ist.

In einem Szenario, in dem die Artikelmenge groß ist, kann der Benutzer es alternativ vorziehen, die Menge manuell einzugeben, anstatt den Strichcode für jeden eingegangenen Artikel zu scannen. In diesem Fall kann der Benutzer den Barcode einmal einscannen, um den Artikel der Liste **Empfang jetzt** hinzuzufügen. Der Benutzer kann dann die zugehörige Zeile in der Ansicht **Jetzt empfangen** auswählen und dann im Fenster **Details**, das auf der rechten Seite der Seite erscheint, das Feld **Empfangsmenge** für den Artikel aktualisieren.

Obwohl die Ansicht **Jetzt empfangen** für das Scannen von Barcodes optimiert ist, können Benutzer auch **Produkt empfangen** in der Anwendungsleiste auswählen und dann die Artikel-ID oder die Barcodedaten über ein Dialogfenster eingeben. Nachdem der eingegebene Artikel validiert wurde, wird der Benutzer aufgefordert, die Empfangsmenge einzugeben.

Die Ansicht **Jetzt empfangen** bietet eine gezielte Möglichkeit für Benutzer, zu sehen, welche Produkte sie erhalten. Alternativ kann die Ansicht **Vollständige Auftragsliste** verwendet werden. Diese Ansicht zeigt die gesamte Liste der Belegzeilen für den ausgewählten Einkaufs- oder Transportauftragsbeleg. Benutzer können Zeilen manuell in der Liste auswählen und dann im Bereich **Details** das Feld **Empfangsmenge** für die ausgewählte Zeile aktualisieren. In der Ansicht **Vollständige Auftragsliste** können die Benutzer Barcodes einscannen oder sie können die Funktion **Produkt empfangen** verwenden, um die Artikel-ID oder den Barcode und Daten über die empfangene Menge einzugeben, ohne zuerst die entsprechende Artikelzeile in der Liste auswählen zu müssen.

### <a name="over-receiving-validations"></a>Übereingangsvalidierungen

Validierungen erfolgen während des Empfangsprozesses für die Belegzeilen. Dazu gehören auch Validierungen für Überlieferungen. Wenn ein Benutzer versucht, mehr Bestand zu erhalten, als in einer Bestellung bestellt wurde, aber entweder keine Überlieferung konfiguriert ist oder der erhaltene Betrag die für die Bestellposition konfigurierte Überlieferungstoleranz überschreitet, erhält der Benutzer einen Fehler und darf die überschüssige Menge nicht erhalten.

Für Transportauftragsbelege ist der Überempfang nicht zulässig. Benutzer erhalten immer Fehler, wenn sie versuchen, mehr zu erhalten, als für die Transportauftragsposition geliefert wurde.

### <a name="close-purchase-order-lines"></a>Bestellpositionen schließen

Sie können die verbleibende Menge einer eingehenden Bestellung während des Empfangsprozesses schließen, wenn der Versender bestätigt hat, dass er die angeforderte volle Menge nicht versenden kann. Um diese Funktion nutzen zu können, muss das Unternehmen so konfiguriert sein, dass eine Unterlieferung von Bestellungen möglich ist. Zusätzlich muss ein Unterlieferungstoleranzprozentsatz für die Bestellung definiert werden.

Um das Unternehmen so zu konfigurieren, dass eine Unterlieferung von Bestellungen in der Commerce-Zentrale möglich ist, gehen Sie zu **Beschaffung** > **Einstellungen** > **Beschaffungsparameter**. Aktivieren Sie auf der Registerkarte **Lieferung** den Parameter **Unterlieferung akzeptieren**. Führen Sie dann den Verteilungsplan-Einzelvorgang **1070** (**Kanalkonfiguration**) aus, um die Einstellungsänderungen mit den Kanälen zu synchronisieren.

Unterlieferungstoleranzprozentsätze für eine Bestellungsposition können für Produkte als Teil der Produktkonfiguration in der Commerce-Zentrale vordefiniert werden. Alternativ können sie für eine bestimmte Bestellung in der Commerce-Zentrale festgelegt oder überschrieben werden.

Nachdem eine Organisation die Konfiguration der Unterlieferung von Bestellungen abgeschlossen hat, wird den POS-Benutzern eine neue Option **Restmenge schließen** im Bereich **Details** angezeigt, wenn sie eine eingehende Bestellungsposition über den Vorgang **Eingehender Bestand** auswählen. Wenn ein Benutzer die verbleibende Menge schließt, führt POS eine Prüfung durch, ob die geschlossene Menge innerhalb der prozentualen Toleranz für die Unterlieferung liegt, die in der Bestellungsposition definiert ist. Wenn die Unterlieferungstoleranz überschritten wurde, wird eine Fehlermeldung angezeigt, und der Benutzer kann die Restmenge erst dann abschließen, wenn die zuvor eingegangene Menge zuzüglich der Menge **Jetzt empfangen** die Mindestmenge erreicht oder überschreitet, die auf der Grundlage des Unterlieferungstoleranzprozentsatzes empfangen werden muss. 

Wenn die Option **Restmenge schließen** für eine Bestellposition aktiviert ist und der Benutzer den Empfang mit der Aktion **Empfang abschließen** abschließt, wird auch eine Abschlussanforderung an die Commerce-Zentrale gesendet, und alle nicht erhaltenen Mengen dieser Bestellposition werden storniert. Zu diesem Zeitpunkt gilt die Position als vollständig empfangen. 

### <a name="receiving-location-controlled-items"></a>Empfangen von standortgesteuerten Positionen

Wenn die empfangenen Artikel ortsgesteuert sind, können die Benutzer den Ort auswählen, an dem sie die Artikel während des Empfangsprozesses erhalten möchten. Wir empfehlen Ihnen, einen Standard-Empfangsort für Ihr Filiallager zu konfigurieren, um diesen Prozess effizienter zu gestalten. Selbst wenn ein Standardort konfiguriert ist, können Benutzer den Empfangsort auf ausgewählten Zeilen nach Bedarf überschreiben.

Der Vorgang respektiert die Konfiguration **Leerbeleg zulässig** Konfiguration auf der Lagerdimension **Lagerort** und erfordert keine Eingabe einer Ortsdimension, wenn ein leerer Beleg konfiguriert ist. Wenn leere Belegpositionen für einen Artikel nicht erlaubt sind, zeigt die POS-Anwendung einen Fehler an und verlangt die Eingabe einer Position, bevor der Beleg gebucht werden kann.

### <a name="receive-all"></a>Alle empfangen

Bei Bedarf können Sie in der Anwendungsleiste **Alles empfangen** wählen, um die **Jetzt empfangen** Menge für alle Belegzeilen schnell auf den maximalen Wert zu aktualisieren, der für diese Zeilen zum Empfang verfügbar ist.

### <a name="receipt-of-unplanned-items-on-purchase-orders"></a>Erhalt ungeplanter Artikel bei Bestellungen

In Commerce Version 10.0.14 und höher können Benutzer ein Produkt erhalten, das ursprünglich nicht in der Bestellung enthalten war. Um diese Funktion zu aktivieren, aktivieren Sie **Der Bestellung des Verkaufsstellenzugangs Positionen hinzufügen**.  

Diese Funktion funktioniert nur für den Zugang von Bestellungen. Es ist nicht möglich, Artikel bei Umlagerungsaufträgen zu erhalten, wenn die Artikel zuvor nicht bestellt und aus dem Ausgangslager versendet wurden.

Benutzer können der Bestellung während des POS-Zugangs keine neuen Produkte hinzufügen, wenn der [Änderungsverwaltungsworkflow](https://docs.microsoft.com/dynamics365/supply-chain/procurement/purchase-order-approval-confirmation) für die Bestellung in der Commerce-Zentrale (HQ) aktiviert ist. Um die Änderungsverwaltung zu aktivieren, müssen alle Änderungen an einer Bestellung zuerst genehmigt werden, bevor der Zugang zulässig ist. Da dieser Prozess es einem Empfänger ermöglicht, der Bestellung neue Positionen hinzuzufügen, schlägt der Zugang fehl, wenn der Änderungsverwaltungs-Workflow aktiviert ist. Wenn die Veränderungsverwaltung für alle Bestellungen oder für den Lieferanten aktiviert ist, der mit der Bestellung verknüpft ist, die aktiv am POS zugeht, kann der Benutzer der Bestellung während des Zugangs am POS keine neuen Produkte hinzufügen.

Die Funktion zum Hinzufügen von Positionen kann nicht als Problemumgehung für den Zugang zusätzlicher Mengen von Produkten verwendet werden, die bereits in der Bestellung enthalten sind. Überhöhter Zugang wird über den Standard verwaltet [Überhöhter Zugang](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation#over-receiving-validations)-Einstellungen für die Produktposition in der Bestellung.

Wenn **Der Bestellung während des Zugangs an der Verkaufsstelle Positionen hinzufügen** aktiviert ist und ein Benutzer mit dem **Eingehender Vorgang** in POS empfängt, die nicht als Artikel in der aktuellen Bestellung erkannt wird, aber als gültiger Artikel erkannt wird, erhält der Benutzer eine Nachricht über das Hinzufügen des Artikels zur Bestellung. Wenn der Benutzer den Artikel zur Bestellung hinzufügt, wird die in **Jetzt zugegangen** eingegebene Menge als bestellte Menge für die Bestellposition betrachtet.

Wenn der Bestellzugang vollständig ist und zur Bearbeitung an die Zentrale übermittelt wurde, werden die hinzugefügten Positionen im Bestellungszentraldokument erstellt. In der Bestellposition in der Zentrale befindet sich eine Kennzeichnung **Hinzugefügt von POS** in der Registerkarte **Allgemein** der Bestellposition. Die Kennzeichnung **Hinzugefügt von POS** zeigt an, dass die Bestellposition durch den POS-Zugangsprozess hinzugefügt wurde und keine Position war, die sich vor dem Zugang in der Bestellung befand.

### <a name="cancel-receiving"></a>Empfang stornieren

Sie sollten die Funktion **Empfang abbrechen** in der Anwendungsleiste nur dann verwenden, wenn Sie aus dem Dokument aussteigen und keine Änderungen speichern möchten. Sie haben z.B. zunächst das falsche Dokument ausgewählt und möchten keine der bisherigen Empfangsdaten speichern.

### <a name="pause-receiving"></a>Empfang anhalten

Wenn Sie eine Bestandsaufnahme erhalten, können Sie die Funktion **Empfang unterbrechen** verwenden, wenn Sie eine Pause vom Empfangsvorgang einlegen möchten. Sie können beispielsweise eine andere Operation vom POS aus durchführen, wie z.B. einen Kundenverkauf anrufen oder die Buchung des Bons verzögern.

Wenn Sie **Empfang pausieren** wählen, wird der Status des Belegs auf **Pausiert** geändert. Daher wissen die Benutzer, dass Daten für den Beleg eingegeben wurden, der Beleg aber noch nicht bestätigt wurde. Wenn Sie bereit sind, den Empfangsvorgang fortzusetzen, wählen Sie das angehaltene Dokument aus und wählen Sie dann **Auftragsdetails**. Alle **Jetzt empfangen** Mengen, die zuvor gespeichert wurden, bleiben erhalten und können in der Ansicht **Vollständige Auftragsliste** angezeigt werden.

### <a name="review"></a>Überprüfen

Vor des endgültigen Eingang der empfangenen Mengen im Commerce Headquaraters (HQ) können Sie die Überprüfungsfunktion verwenden, um das eingehende Dokument zu validieren. Die Überprüfung macht Sie auf fehlende oder falsche Daten aufmerksam, die zu Verarbeitungsfehlern führen können, und bietet Ihnen die Möglichkeit, Probleme zu beheben, bevor Sie die Empfangsanforderung senden. Um die Funktion **Überprüfen** in der App-Symbolleiste zu aktivieren, aktivieren Sie die Funktion **Prüfung eingehender und ausgehender Bestandsvorgänge am POS aktivieren** über den Arbeitsbereich **Funktionsverwaltung** im Commerce Headquarters (HQ).

Die Funktion **Überprüfen** überprüft die folgenden Probleme in einem eingehenden Dokument:

- **Zu viel empfangen**: Die Empfangsmenge ist größer als die bestellte Menge. Der Schweregrad dieses Problems wird durch die Konfiguration der Mehrlieferung des Commerce Headquarters (HQ) bestimmt.
- **Zu wenig empfangen**: Die Empfangsmenge ist kleiner als die bestellte Menge. Der Schweregrad dieses Problems wird durch die Konfiguration der Unterlieferung des Commerce Headquarters (HQ) bestimmt.
- **Seriennummer**: Die Seriennummer wird für einen serialisierten Artikel, für den die Seriennummer im Bestand registriert werden muss, nicht angegeben oder überprüft.
- **Standort nicht festgelegt**: Der Standort ist für standortgesteuerte Artikel nicht angegeben, wenn ein leerer Standort nicht zulässig ist.
- **Gelöschte Zeilen**: In dem Auftrag wurden Zeilen von einem Benutzer des Commerce Headquarters (HQ) gelöscht, der der POS-Anwendung nicht bekannt ist.

Stellen Sie den Parameter **Automatische Prüfung aktivieren** auf **Ja** unter **Commerce-Parameter** > **Bestand** > **Bestand speichern**, um die Prüfung automatisch ausführen zu lassen, wenn **Empfang abschließen** ausgewählt wurde.

### <a name="finish-receiving"></a>Empfang abschließen

Wenn Sie die Eingabe aller **Jetzt empfangen** Mengen für Produkte abgeschlossen haben, müssen Sie **Empfang beenden** in der Anwendungsleiste wählen, um den Beleg zu bearbeiten.

Wenn Benutzer einen Bestelleingang abschließen, werden sie aufgefordert, einen Wert in das Feld **Belegnummer** einzugeben, wenn diese Funktion konfiguriert ist. In der Regel entspricht dieser Wert der Kennung des Lieferantenpackzettels. Die Daten **Quittungsnummer** werden im Wareneingangsjournal in Commerce Headquarters gespeichert. Belegnummern werden nicht für Transportauftragseingänge erfasst.

Bei der asynchronen Belegverarbeitung wird der Beleg über ein asynchrones Dokumenten-Framework eingereicht. Die Zeit, die für die Verbuchung des Belegs benötigt wird, hängt von der Größe des Belegs (Anzahl der Zeilen) und dem allgemeinen Verarbeitungsverkehr, der auf dem Server stattfindet, ab. Normalerweise erfolgt dieser Vorgang in wenigen Sekunden. Wenn die Belegbuchung fehlschlägt, wird der Benutzer über die Liste **Eingangsvorgang** Belege benachrichtigt, wobei der Belegstatus auf **Verarbeitung fehlgeschlagen** aktualisiert wird. Der Benutzer kann dann den fehlgeschlagenen Beleg in POS auswählen, um die Fehlermeldungen und den Grund für den Fehlschlag im Bereich **Details** anzuzeigen. Ein fehlgeschlagener Beleg bleibt ungebucht und erfordert, dass der Benutzer zu den Belegzeilen zurückkehrt, indem er **Bestelldetails** in POS wählt. Der Benutzer muss dann das Dokument mit Korrekturen auf der Grundlage der Fehler aktualisieren. Nachdem ein Beleg korrigiert wurde, kann der Benutzer erneut versuchen, ihn zu verarbeiten, indem er in der Anwendungsleiste **Erfüllung beenden** wählt.

## <a name="create-an-inbound-transfer-order"></a>Einen eingehenden Transportauftrag erstellen

Vom POS aus können Benutzer neue Transportauftragsbelege erstellen. Um den Prozess zu beginnen, wählen Sie **Neu** in der Anwendungsleiste, während Sie sich in der Hauptmenüleiste befinden **Eingangsvorgang**-Dokumentenliste. Sie werden dann aufgefordert, ein **Umlagerung von**-Lager oder Filiale auszuwählen, die den Bestand an Ihrem Filialstandort bereitstellen wird. Die Werte sind auf die Auswahl beschränkt, die in der Konfiguration der Erfüllungsgruppe der Filiale definiert ist. Bei einem eingehenden Transportauftrag ist Ihre aktuelle Filiale immer das **Transfer an**-Lager für den Transportauftrag. Dieser Wert kann nicht geändert werden.

Sie können in den Feldern **Versanddatum**, **Empfangsdatum** und **Lieferart** je nach Bedarf Werte eingeben. Sie können auch eine Notiz hinzufügen, die zusammen mit dem Transportauftragskopf als Anlage zum Dokument in Commerce Headquarters gespeichert wird.

Nachdem die Kopfinformationen erstellt wurden, können Sie dem Transportauftrag Produkte hinzufügen. Um den Prozess der Hinzufügung von Artikeln und angeforderten Mengen zu starten, wählen Sie **Produkt hinzufügen**. Im Bereich **Details** können Sie auch eine zeilenspezifische Notiz zu den Journalzeilen hinzufügen. Diese Notizen werden als Zeilenanhang gespeichert.

Nachdem die Zeilen auf dem eingehenden Transportauftrag eingegeben wurden, müssen Sie **Sichern** wählen, um die Belegänderungen lokal zu speichern, oder **Anfrage senden**, um die Auftragsdetails zur weiteren Bearbeitung an Commerce Headquarters zu senden. Wenn Sie **Speichern** wählen, wird der Belegentwurf in der Kanaldatenbank gespeichert, und das Ausgangslager kann den Beleg erst dann ausführen, wenn er erfolgreich über **Anfrage senden** verarbeitet wurde. Sie sollten **Speichern** nur dann wählen, wenn Sie nicht bereit sind, die Anforderung zur Verarbeitung an Commerce Headquarters zu übergeben.

Wenn ein Dokument lokal gespeichert wird, finden Sie es auf der Registerkarte **Entwürfe** der Dokumentenliste **Eingangsvorgang**. Solange sich ein Dokument im Status **Entwurf** befindet, können Sie es bearbeiten, indem Sie **Bearbeiten** wählen. Sie können Zeilen nach Bedarf aktualisieren, hinzufügen oder löschen. Sie können auch das gesamte Dokument löschen, während es sich im Status **Entwurf** befindet, indem Sie **Löschen** auf der Registerkarte **Entwürfe** wählen.

Nachdem der Dokumententwurf erfolgreich bei Commerce Headquarters eingereicht wurde, erscheint er auf der Registerkarte **Aktiv** und hat den Status **Beantragt**. Zu diesem Zeitpunkt können Benutzer in der Eingangsfiliale oder im Lager den angeforderten eingehenden Transportauftragsbeleg nicht mehr bearbeiten. Nur Benutzer im Ausgangslager können den Beleg bearbeiten, indem sie in der POS-Anwendung **Ausgangsvorgang** wählen. Die Bearbeitungssperre stellt sicher, dass keine Konflikte auftreten, weil ein eingehender Anforderer den Transportauftrag zur gleichen Zeit ändert, zu der der ausgehende Verlader den Auftrag aktiv kommissioniert und versendet. Wenn nach der Übermittlung des Transportauftrags Änderungen aus dem eingehenden Lager oder dem Lager erforderlich sind, sollte der ausgehende Verlader kontaktiert und aufgefordert werden, die Änderungen einzugeben.

Nachdem sich der Beleg im Status **Anforderung** befindet, ist er auf der Registerkarte **Aktiv** sichtbar. Er kann jedoch noch nicht von der Eingangsfiliale oder dem Lager empfangen werden. Nachdem das Ausgangslager einen Teil oder den gesamten Transportauftrag versendet hat, kann die eingehende Filiale oder das Lager Belege in POS buchen. Wenn die Ausgangsseite die Transportauftragsbelege verarbeitet, wird ihr Status von **Anforderung** auf **Versandt** oder **Teilweise versandt** fortgeschrieben. Nachdem sich die Belege im Status **Versandt** oder **Teilweise versandt** befinden, kann die eingehende Filiale oder das Lager über den Eingangsvorgangs-Empfangsprozess Eingänge gegen sie buchen.

## <a name="related-topics"></a>Verwandte Themen

[Bestandsaufnahme am Ausgang in POS](pos-outbound-inventory-operation.md)
