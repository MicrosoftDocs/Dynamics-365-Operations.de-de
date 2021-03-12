---
title: Bestandsausgangsoperation in POS
description: Dieses Thema beschreibt die Möglichkeiten des Bestandsausgangs am Point of Sale (POS).
author: hhaines
manager: annbe
ms.date: 07/30/2020
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
ms.openlocfilehash: b8f0daf96e782e5ba6c985847bad81312e48d30b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976613"
---
# <a name="outbound-inventory-operation-in-pos"></a>Bestandsausgangsoperation in POS

[!include [banner](includes/banner.md)]


In Microsoft Dynamics 365 Commerce Version 10.0.10 und höher ersetzen Ein- und Ausgangsvorgänge am POS (Point of Sale) den Kommissionier- und Empfangsvorgang.

> [!NOTE]
> In Version 10.0.10 und später werden alle neuen Funktionen in der POS-Anwendung, die mit dem Empfang von Filialbeständen gegen Bestellungen und Transportaufträge zusammenhängen, zum Vorgang der Eingangsvorgänge hinzugefügt. Wenn Sie derzeit den Kommissionier- und Empfangsvorgang in der POS-Anwendung verwenden, empfehlen wir Ihnen, eine Strategie für den Übergang von diesem Vorgang zu den neuen Eingangs- und Ausgangsvorgängen zu entwickeln. Obwohl der Kommissionier- und Wareneingangsvorgang nicht aus dem Produkt entfernt wird, werden ab Version 10.0.9 keine weiteren Investitionen in das Produkt getätigt, weder aus funktionaler noch aus leistungsbezogener Sicht.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Voraussetzung: Konfigurieren Sie ein asynchrones Dokumenten-Framework.

Die ausgehende Operation umfasst Leistungsverbesserungen, um sicherzustellen, dass Benutzer, die ein hohes Volumen an Eingangsbuchungen in vielen Geschäften oder Unternehmen sowie große Bestandsdokumente haben, diese Dokumente ohne Zeitverzögerungen oder Ausfälle an Commerce Headquarters (HQ) weiterleiten können. Diese Verbesserungen erfordern die Verwendung eines asynchronen Dokumenten-Frameworks.

Wenn ein asynchrones Belegframework verwendet wird, können Sie Änderungen an ausgehenden Belegen von der Kasse an Commerce Headquarters (HQ) übertragen und dann zu anderen Aufgaben übergehen, während die Verarbeitung an Commerce Headquarters (HQ) im Hintergrund erfolgt. Sie können den Status des Belegs über die **Ausgangsoperation**-Dokumentliste in POS überprüfen, um sicherzustellen, dass die Buchung erfolgreich war. In der POS-Anwendung können Sie auch die Belegliste der Ausgangsoperation aktiv verwenden, um alle Belege zu sehen, die nicht an Commerce Headquarters (HQ) gebucht werden konnten. Wenn ein Beleg fehlschlägt, können POS-Benutzer Korrekturen an ihm vornehmen und dann erneut versuchen, ihn an Commerce Headquarters (HQ) zu verarbeiten.

> [!IMPORTANT]
> Das asynchrone Belegframework muss konfiguriert werden, bevor ein Unternehmen versucht, die Ausgangsoperation im POS zu verwenden.

Um ein asynchrones Belegframework zu konfigurieren, führen Sie die folgenden Verfahren durch.

### <a name="create-and-configure-a-number-sequence"></a>Erstellen und konfigurieren Sie eine Zahlenfolge

1. Gehen Sie zu **Organisationsverwaltung \> Nummernkreis \> Nummernkreis**.
2. Erstellen Sie auf der Seite **Nummernkreise** einen Nummernkreis.
3. Geben Sie in die Felder **Nummernkreiscode** und **Name** benutzerdefinierte Werte ein.
4. Wählen Sie auf dem Inforegister **Referenzen** **Hinzufügen**.
5. Im Feld **Bereich** wählen Sie **Commerce-Parameter**.
6. Wählen Sie im Feld **Referenz** **Dokumentvorgangskennung**.
7. Setzen Sie im Inforegister **Allgemein** im Abschnitt **Einrichten** die Option **Kontinuierlich** auf **Nein**, um sicherzustellen, dass es keine Leistungsprobleme gibt.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Erstellen und planen Sie zwei Batch-Jobs für die Dokumentverarbeitung und die Überwachungsaufgaben

> [!NOTE]
> In Commerce Version 10.0.13 und höher müssen Sie die Stapeljobs nicht über das Stapeljob-Framework konfigurieren. Die Stapelverarbeitungsvorgänge können über das Menü **Retail and Commerce >Retail and Commerce IT** konfiguriert werden. Verwenden Sie die Menüoptionen **Überwachung für den Betrieb von Einzelhandelsdokumenten** und **Verarbeitung von Einzelhandelsdokumenten** zum Konfigurieren der Stapeljobs.

Die von Ihnen erstellten Batch-Jobs werden zur Verarbeitung von Dokumenten verwendet, die fehlschlagen oder ein Time-Out aufweisen. Sie werden auch verwendet, wenn die Anzahl der aktiven Bestandsbelege, die von der Kasse aus verarbeitet werden, einen vom System konfigurierten Wert überschreitet.

1. Gehen Sie zu **Systemverwaltung \> Anfragen \> Batch-Jobs**.
2. Legen Sie auf der Seite **Batch-Job** zwei Batch-Jobs an:

    - Konfigurieren Sie einen Job für die Ausführung der Klasse **RetailDocumentOperationMonitorBatch**.
    - Konfigurieren Sie den anderen Job so, dass er die Klasse **RetailDocumentOperationProcessingBatch** ausführt.

3. Planen Sie die neuen Batch-Jobs so ein, dass sie wiederkehrend ausgeführt werden. Stellen Sie den Zeitplan z.B. so ein, dass die Jobs alle fünf Minuten ausgeführt werden.

## <a name="prerequisite-add-outbound-operation-to-the-pos-screen-layout"></a>Dies ist eine Voraussetzung: Fügen Sie dem POS-Bildaufbau den Ausgang hinzu.

Bevor Ihr Unternehmen die Funktionalität des Ausgangsvorgangs nutzen kann, muss es den **Ausgangsvorgang** POS-Vorgang auf einem oder mehreren Ihrer [POS-Bildschirmbilder](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) konfigurieren. Bevor Sie den neuen Vorgang in einer Produktionsumgebung einsetzen, sollten Sie ihn gründlich testen und Ihre Benutzer in der Verwendung schulen.

## <a name="overview"></a>Übersicht

Die Ausgangsoperation ermöglicht es den POS-Benutzern, die folgenden Aufgaben durchzuführen:

- Buchen von Sendungen für Transportauftragsbelege in Fällen, in denen die Filiale des Benutzers das vorgesehene Auslieferungslager ist.
- Informationen über historische Transportauftragssendungen anzeigen, die von der Filiale gebucht wurden.
- Neue ausgehende Transportauftragsanforderungen erstellen.

Wenn der Ausgangsvorgang aus der POS-Anwendung heraus gestartet wird, erscheint eine Listenseitenansicht. Diese Ansicht zeigt offene Transportauftragsbelege mit Bestandszeilen, die die aktuelle Filiale des Benutzers versenden und erfüllen soll. Um einen ausgewählten Beleg zu finden, können Benutzer die Liste durchblättern oder die Suchfunktion verwenden.

Die Liste der ausgehenden Bestandsbelege hat drei Registerkarten.

- **Aktiv** - Diese Registerkarte zeigt Transportaufträge mit dem Status **Anforderlich** oder **Teilweise versandt**. Die Aufträge enthalten Zeilen oder Mengen auf Zeilen, die von der aktuellen Filiale des Benutzers versandt werden müssen. Diese Registerkarte zeigt auch Bestellungen mit dem Status **Verarbeitung in HQ** (d. h. sie warten auf die Bestätigung der erfolgreichen Buchung von Commerce Headquarters [HQ]) oder **Verarbeitung fehlgeschlagen** (d. h. die Buchung in Commerce Headquarters (HQ) war nicht erfolgreich, und der Benutzer muss die Daten korrigieren und erneut versuchen, die Bestellungen einzureichen).
- **Entwurf** - Diese Registerkarte zeigt neue ausgehende Transportauftragsanforderungen, die von der Filiale des Benutzers erstellt wurden. Die Belege wurden jedoch nur lokal gespeichert. Sie wurden noch nicht zur Bearbeitung an Commerce Headquarters (HQ) übermittelt.
- **Ausführlich** - Diese Registerkarte zeigt eine Liste der Transportauftragsbelege, die die Filiale in den letzten sieben Tagen vollständig versandt hat. Diese Registerkarte dient nur zu Informationszwecken. Alle Informationen zu den Belegen sind schreibgeschützte Daten für die Filiale.

Wenn Sie Dokumente auf einer der Registerkarten anzeigen, kann das Feld **Status** Ihnen helfen, den Status des Dokuments zu verstehen.

- **Entwurf** - Das Transportauftragsdokument wurde nur lokal in der Kanaldatenbank der Filiale gespeichert. Es wurden noch keine Informationen über den Transportauftragsantrag an Commerce Headquarters (HQ) übermittelt.
- **Anforderung** – Die Bestellung oder der Transportauftrag wurde in Commerce Headquarters (HQ) angelegt und ist vollständig geöffnet. Der aktuelle Speicher des Benutzers hat noch keine Sendungen gegen das Dokument verarbeitet.
- **Teilweise versandt** - Der Transportauftragsbeleg hat eine oder mehrere Zeilen oder Teilzeilenmengen, die als vom Ausgangslager versandt gebucht wurden. Diese versandten Zeilen können über den Eingangsvorgang empfangen werden.
- **Vollständig versandt** - Der Transportauftrag wurde mit allen Zeilen und vollen Zeilenmengen als vom Auslieferungslager versandt gebucht.
- **In Bearbeitung** - Dieser Status wird verwendet, um Gerätebenutzer darüber zu informieren, dass der Beleg von einem anderen Benutzer aktiv bearbeitet wird.
- **Pausiert** - Dieser Status wird angezeigt, nachdem **Empfang pausieren** gewählt wurde, um den Empfangsvorgang vorübergehend zu stoppen.
- **Bearbeitung in HQ** – Das Dokument wurde von der POS-Anwendung an Commerce Headquarters (HQ) übermittelt, aber es wurde noch nicht erfolgreich an Commerce Headquarters (HQ) gesendet. Der Beleg durchläuft gerade den asynchronen Belegverbuchungsprozess. Nachdem der Beleg erfolgreich an Commerce Headquarters (HQ) gebucht wurde, sollte sein Status auf **Vollständig erhalten** oder **Teilweise erhalten** aktualisiert werden.
- **Verarbeitung fehlgeschlagen** - Das Dokument wurde an Commerce Headquarters (HQ) gebucht und abgelehnt. Der Bereich **Details** zeigt den Grund für das Fehlschlagen der Buchung. Der Beleg muss bearbeitet werden, um Datenprobleme zu beheben, und dann erneut zur Verarbeitung an Commerce Headquarters (HQ) geschickt werden.

Wenn Sie eine Belegzeile in der Liste auswählen, erscheint ein Fenster **Details**. Dieser Bereich zeigt zusätzliche Informationen über den Beleg an, wie z.B. Transport- und Datumsinformationen. Ein Fortschrittsbalken zeigt an, wie viele Positionen noch bearbeitet werden müssen. Wenn der Beleg nicht erfolgreich an Commerce Headquarters (HQ) verarbeitet wurde, zeigt der Bereich **Details** auch Fehlermeldungen an, die mit dem Fehler zusammenhängen.

In der Seitenansicht der Dokumentliste können Sie in der Anwendungsleiste **Details** wählen, um die Dokumentdetails anzuzeigen. Sie können auch die Eingangsverarbeitung für berechtigte Belegzeilen aktivieren.

In der Seitenansicht der Belegliste können Sie auch einen neuen ausgehenden Transportauftrag für eine Filiale anlegen.

## <a name="transfer-order-shipping-process"></a>Versandprozess für Transportaufträge

Nachdem Sie einen Transportauftragsbeleg auf der Registerkarte **Aktiv** ausgewählt haben, können Sie **Auftragsdetails** wählen, um den Erfüllungsprozess zu beginnen. Die Ansicht **Komplette Bestellliste** erscheint. Diese Seite zeigt alle Belegzeilen an, die die Position enthalten. Sie zeigt auch Details zur bestellten Menge an.

Jeder Scan eines Barcodes aktualisiert die Menge im Feld **Versand jetzt** um eine Einheit. Alternativ können Sie eine Versandmenge eingeben, indem Sie in der Anwendungsleiste **Produkt versenden** wählen, eine Artikel-ID eingeben und dann die Menge eingeben. Wenn die Position ortsgesteuert ist, können Sie den Versandort für die Belegposition bestätigen oder festlegen.

In der Ansicht **Vollständige Auftragsliste** können Sie eine Zeile in der Liste manuell auswählen und dann die **Versandmenge jetzt** für die ausgewählte Zeile im Bereich **Details** aktualisieren.

### <a name="over-delivery-shipping-validations"></a>Überlieferungs-Versandvalidierungen

Validierungen erfolgen während des Empfangsprozesses für die Belegzeilen. Dazu gehören auch Validierungen für Überlieferungen. Wenn ein Benutzer versucht, mehr Bestand zu erhalten, als in einer Bestellung bestellt wurde, aber entweder keine Überlieferung konfiguriert ist oder die erhaltene Menge die Überlieferungstoleranz überschreitet, die für die Bestellzeile konfiguriert ist, erhält der Benutzer einen Fehler und darf die überschüssige Menge nicht erhalten.

### <a name="underdelivery-close-lines"></a>Unterlieferung schließen-Positionen

In Commerce Version 10.0.12 wurde eine Funktion hinzugefügt, mit der POS-Benutzer verbleibende Mengen während des Versandes ausgehender Bestellungen schließen oder stornieren können, wenn das ausgehende Lager feststellt, dass nicht die angeforderte volle Menge versendet werden kann. Mengen können auch später geschlossen oder storniert werden. Um diese Funktion nutzen zu können, muss das Unternehmen so konfiguriert sein, dass eine Unterlieferung von Transportaufträgen möglich ist. Zusätzlich muss ein Unterlieferungsprozentsatz für die Transportauftragsposition definiert werden.

Um das Unternehmen so zu konfigurieren, dass eine Unterlieferung von Umlagerungsaufträgen möglich ist, wechseln Sie in Commerce Headquarters (HQ) zu **Bestandsverwaltung \> Einrichtung \> Bestands- und Lagerverwaltungsparameter**. Auf der Seite **Bestands- und Lagerverwaltungsparameter**, auf der Registerkarte **Umlagerungsaufträge** aktivieren Sie die Option **Unterlieferung akzeptieren**. Dann führen Sie den Verteilungszeitplanvorgang **1070** zum Synchronisieren der Parameteränderungen mit Ihrem Geschäftskanal aus.

Unterlieferungsprozentsätze für eine Transportauftragsposition können für Produkte als Teil der Produktkonfiguration in der Commerce-Zentrale vordefiniert werden. Alternativ können sie über Commerce Headquarters (HQ) in einer bestimmten Überweisungsauftragsposition festgelegt oder überschrieben werden.

Nachdem eine Organisation die Konfiguration der Unterlieferung von Umlagerungsaufträgen abgeschlossen hat, wird den POS-Benutzern eine neue Option **Restmenge schließen** im Bereich **Details** angezeigt, wenn sie eine ausgehende Umlagerungsauftragsposition über die Funktion **Ausgangsvorgang** auswählen. Wenn der Benutzer die Lieferung mit dem Vorgang **Erfüllung abschließen** abschließt, können sie eine Anforderung an Commerce Headquarters (HQ) senden, um die verbleibende nicht versendete Menge zu stornieren. Wenn ein Benutzer die verbleibende Menge schließt, führt Commerce eine Prüfung durch, ob die stornierte Menge innerhalb der prozentualen Toleranz für die Unterlieferung liegt, die in der Überweisungsauftragsposition definiert ist. Wenn die Toleranz für Unterlieferung überschritten wird, wird eine Fehlermeldung angezeigt und der Benutzer kann die verbleibende Menge erst schließen, wenn die zuvor versendete Menge und die Menge „Jetzt versenden“ die Toleranz für Unterlieferung erfüllt oder überschreitet.

Nachdem die Sendung mit Commerce Headquarters (HQ) synchronisiert wurde, werden die Mengen, die im Feld **Jetzt versenden** für die Transportauftragsposition im POS definiert sind, in Commerce Headquarters (HQ) auf den Versandstatus aktualisiert. Alle nicht versendeten Mengen, die zuvor als „Lieferrückstand“ angesehen wurden (d.h. Mengen, die später versendet werden), gelten stattdessen als stornierte Mengen. Der „Lieferrückstand“ für die Transportauftragsposition ist eingestellt auf **0** (Null), und die Position gilt als vollständig versendet.

### <a name="shipping-location-controlled-items"></a>Versandortsgesteuerter Artikel

Wenn die zu versendenden Artikel standortgesteuert sind, können die Benutzer während des Versandprozesses den Ort wählen, von dem aus sie den Bestand ausgeben möchten. Wir empfehlen Ihnen, einen Standardausgabestandort für Ihr Filiallager zu konfigurieren, um diesen Prozess effizienter zu gestalten. Selbst wenn ein Standardort konfiguriert ist, können Benutzer den Ausgabeort in ausgewählten Zeilen nach Bedarf überschreiben.

Der Vorgang respektiert die Konfiguration **Leerbeleg zulässig** Konfiguration auf der Lagerdimension **Lagerort** und erfordert keine Eingabe einer Ortsdimension, wenn ein leerer Beleg konfiguriert ist. Wenn leere Belegpositionen für einen Artikel nicht erlaubt sind, zeigt die POS-Anwendung einen Fehler an und verlangt die Eingabe einer Position, bevor der Beleg gebucht werden kann.

### <a name="ship-all"></a>Alles versenden

Bei Bedarf können Sie in der Anwendungsleiste **Alle versenden** wählen, um die **Jetzt versenden** Menge für alle Belegzeilen schnell auf den maximalen Wert zu aktualisieren, der für diese Zeilen zur Verfügung steht.

### <a name="cancel-fulfillment"></a>Erfüllung stornieren

Benutzen Sie die Funktion **Erfüllung abbrechen** in der Anwendungsleiste nur dann, wenn Sie aus dem Dokument zurückkehren und keine Änderungen speichern möchten. Sie haben z.B. zunächst den falschen Beleg selektiert und möchten keine der bisherigen Versanddaten speichern.

### <a name="pause-fulfillment"></a>Erfüllung anhalten

Wenn Sie den Transportauftrag erfüllen, können Sie die Funktion **Erfüllung pausieren** verwenden, wenn Sie eine Pause vom Prozess machen wollen. Sie möchten beispielsweise einen anderen Vorgang vom POS aus durchführen, wie z. B. einen Kundenverkauf anrufen oder die Verbuchung der Sendung in Commerce Headquarters (HQ) verzögern.

Wenn Sie **Erfüllung pausieren** wählen, wird der Status des Belegs auf **Pausiert** geändert. Daher weiß der Benutzer, dass Daten in den Beleg eingegeben wurden, der Beleg aber noch nicht bestätigt wurde. Wenn Sie bereit sind, den Erfüllungsprozess wieder aufzunehmen, markieren Sie das angehaltene Dokument und wählen Sie dann **Auftragsdetails**. Alle **Versand jetzt** Mengen, die zuvor gespeichert wurden, bleiben erhalten und können in der Ansicht **Vollständige Bestellliste** eingesehen werden.

### <a name="review"></a>Überprüfen

Vor dem endgültigen Eingang der erfüllten Mengen in Commerce Headquarter (HQ) können Sie die Funktion **Überprüfung** verwenden, um das ausgehende Dokument zu überprüfen. Diese Funktion macht Sie auf mögliche fehlende oder falsche Daten aufmerksam, die zu Verarbeitungsfehlern führen können, und bietet Ihnen die Möglichkeit, Probleme zu beheben, bevor Sie die Empfangsanforderung senden. Um die Funktion **Überprüfen** in der App-Symbolleiste zu aktivieren, aktivieren Sie die Funktion **Prüfung eingehender und ausgehender Bestandsvorgänge am POS** über die Funktionsverwaltung im Commerce Headquarters (HQ).

Die Funktion **Überprüfen** überprüft die folgenden Probleme in einem ausgehenden Dokument:
- **Zu viel versendet**: Die versendete Menge ist größer als die bestellte Menge. Der Schweregrad dieses Problems wird durch die Konfiguration der Mehrlieferung des Commerce Headquarters (HQ) bestimmt.
- **Zu wenig versendet**: Die versendete Menge ist niedriger als die bestellte Menge. Der Schweregrad dieses Problems wird durch die Konfiguration der Unterlieferung des Commerce Headquarters (HQ) bestimmt.
- **Seriennummer**: Die Seriennummer wird für einen serialisierten Artikel, für den die Seriennummer im Bestand registriert werden muss, nicht angegeben oder steht nicht zur Verfügung.
- **Standort nicht festgelegt**: Der Standort ist für standortgesteuerte Artikel nicht angegeben, wenn ein Standort nicht leer bleiben darf.
- **Gelöschte Zeilen**: In dem Auftrag wurden Zeilen von einem Benutzer des Commerce Headquarters (HQ) gelöscht, der der POS-Anwendung nicht bekannt ist.

Wenn Sie den Parameter **Automatische Prüfung aktivieren** auf **Ja** unter **Handelsparameter** > **Bestand** > **Bestandsvorgänge speichern** stellen, wird die Prüfung automatisch ausgeführt, wenn die Funktion **Erfüllung abschließen** ausgewählt wurde.

### <a name="finish-fulfillment"></a>Erfüllung abschließen

Wenn Sie die Eingabe aller **Jetzt versenden** Mengen für Produkte abgeschlossen haben, müssen Sie **Ausführung beenden** in der Anwendungsleiste wählen.

Bei der asynchronen Belegverarbeitung wird der Beleg über ein asynchrones Dokumenten-Framework eingereicht. Die Zeit, die für die Verbuchung des Belegs benötigt wird, hängt von der Größe des Belegs (Anzahl der Zeilen) und dem allgemeinen Verarbeitungsverkehr, der auf dem Server stattfindet, ab. Normalerweise erfolgt dieser Vorgang in wenigen Sekunden. Wenn die Buchung des Dokuments fehlschlägt, wird der Benutzer über die **Ausgangsoperation**-Dokumentenliste auf der Registerkarte **Aktiv** benachrichtigt, wo der Dokumentstatus auf **Verarbeitung fehlgeschlagen** aktualisiert wird. Der Benutzer kann dann den fehlgeschlagenen Beleg in POS auswählen, um die Fehlermeldungen und den Grund für den Fehlschlag im Bereich **Details** anzuzeigen. Ein fehlgeschlagener Beleg bleibt ungebucht und erfordert, dass der Benutzer zu den Belegzeilen zurückkehrt, indem er **Bestelldetails** in POS wählt. Der Benutzer muss dann das Dokument mit Korrekturen auf der Grundlage der Fehler aktualisieren. Nachdem ein Beleg korrigiert wurde, kann der Benutzer erneut versuchen, ihn zu verarbeiten, indem er in der Anwendungsleiste **Erfüllung beenden** wählt.

## <a name="create-an-outbound-transfer-order"></a>Erstellen Sie einen ausgehenden Transportauftrag

Vom POS aus können Benutzer neue Transportauftragsbelege erstellen. Um den Prozess zu beginnen, wählen Sie **Neu** in der Anwendungsleiste, während Sie sich in der Hauptmenüleiste **Ausgangsvorgang** Belegliste befinden. Sie werden dann aufgefordert, ein **Transfer an** Lager oder Filiale zu wählen, an die Ihre aktuelle Filiale Bestand senden wird. Die Werte sind auf die Auswahl beschränkt, die in der Konfiguration der Erfüllungsgruppe der Filiale definiert ist. Bei einem ausgehenden Transportauftrag ist Ihre aktuelle Filiale immer die **Transfer von** Lager für den Transportauftrag. Dieser Wert kann nicht geändert werden.

Sie können in den Feldern **Versanddatum**, **Empfangsdatum** und **Lieferart** je nach Bedarf Werte eingeben. Sie können auch eine Notiz hinzufügen, die zusammen mit dem Transportauftragskopf als Anlage zum Dokument in Commerce Headquarters (HQ) gespeichert wird.

Nachdem die Kopfinformationen erstellt wurden, können Sie dem Transportauftrag Produkte hinzufügen. Um den Prozess des Hinzufügens von Artikeln und angeforderten Mengen zu starten, scannen Sie Barcodes oder wählen Sie **Produkt hinzufügen**.

Nachdem die Zeilen im ausgehenden Transportauftrag eingegeben wurden, müssen Sie **Speichern** wählen, um die Belegänderungen lokal zu speichern, oder **Anfrage senden**, um die Auftragsdetails zur weiteren Bearbeitung an Commerce Headquarters (HQ) zu senden. Wenn Sie **Speichern** wählen, wird der Belegentwurf in der Kanaldatenbank gespeichert, und das Ausgangslager kann den Beleg erst dann ausführen, wenn er erfolgreich über **Anfrage senden** verarbeitet wurde. Wählen Sie **Speichern** nur dann, wenn Sie nicht bereit sind, die Anforderung zur Verarbeitung an Commerce Headquarters (HQ) zu übergeben.

Wenn ein Dokument lokal gespeichert wird, finden Sie es auf der Registerkarte **Entwürfe** der Dokumentenliste **Eingangsvorgang**. Solange sich ein Dokument im Status **Entwurf** befindet, können Sie es bearbeiten, indem Sie **Bearbeiten** wählen. Sie können Zeilen nach Bedarf aktualisieren, hinzufügen oder löschen. Sie können auch das gesamte Dokument löschen, während es sich im Status **Entwurf** befindet, indem Sie **Löschen** auf der Registerkarte **Entwürfe** wählen.

Nachdem der Dokumententwurf erfolgreich bei Commerce Headquarters (HQ) eingereicht wurde, erscheint er auf der Registerkarte **Aktiv** und hat den Status **Beantragt**. Zu diesem Zeitpunkt können nur Benutzer im Ausgangslager den Beleg bearbeiten, indem sie in der POS-Anwendung **Ausgangsvorgang** wählen. Benutzer im Eingangslager können den Transportauftrag auf der Registerkarte **Aktiv** der Belegliste **Eingangsvorgang** anzeigen, aber nicht bearbeiten oder löschen. Die Bearbeitungssperre stellt sicher, dass keine Konflikte auftreten, weil ein eingehender Anforderer den Transportauftrag zur gleichen Zeit ändert, zu der der ausgehende Verlader den Auftrag aktiv kommissioniert und versendet. Wenn nach der Übermittlung des Transportauftrags Änderungen aus dem eingehenden Lager oder dem Lager erforderlich sind, sollte der ausgehende Verlader kontaktiert und aufgefordert werden, die Änderungen einzugeben.

Nachdem sich der Beleg im Status **Anforderung** befindet, ist er für die Erfüllungsbearbeitung durch das Ausgangslager bereit. Da der Transport mit Hilfe des Ausgangsvorgangs bearbeitet wird, wird der Status der Transportauftragsbelege von **Anforderung** auf **Vollständig versandt** oder **Teilweise versandt** fortgeschrieben. Nachdem sich die Belege im Status **Vollständig versandt** oder **Teilweise versandt** befinden, kann das Eingangslager oder das Lager mit Hilfe des Empfangsprozesses für den Eingangsvorgang Eingänge gegen sie buchen.

Vollständig versandte Transportaufträge werden auf die Registerkarte **Vollständig** der Belegliste **Ausgangsvorgang** verschoben. Dort bleiben sie für Benutzer im ausgehenden Lager oder im Lager im Nur-Lese-Modus sieben Tage lang sichtbar.

## <a name="related-topics"></a>Verwandte Themen

[Eingangsbestandsvorgang in POS](pos-inbound-inventory-operation.md)
