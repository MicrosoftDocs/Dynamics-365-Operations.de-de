---
title: "Externen Katalog für PunchOut eProcurement einrichten"
description: "In diesem Thema wird die Verwendung eines externen Katalogs oder des Punchoutkatalogs beschrieben, um Angebotsinformationen von einem Kreditor zu erhalten und einer Bestellanforderung hinzuzufügen."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a20bb97e451ac59ba23c7f767b5feb336278dcd1
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-an-external-catalog-for-punchout-eprocurement"></a>Externen Katalog für PunchOut eProcurement einrichten

[!include[banner](../includes/banner.md)]

Mithilfe des externen Katalogs können Sie sicherstellen, dass das Produkt und die Preisangaben, die Sie dann in Dynamics 365 for Finance and Operations, Enterprise Edition, Juli 2017 verarbeiten, auf dem aktuellen Stand sind. Die Anforderung kann anschließend genehmigt und in eine Bestellung konvertiert und ein Auftrag kann an den Kreditor erteilt werden.

Wenn der externe Katalog eingerichtet ist und ein Mitarbeiter eine Anforderung vorbereitet, gibt es eine Option zur Weiterleitung an einen externen Standort, den externen Katalog, und zum Einkaufskorb zurückzukehren, der auf der externen Website erstellt wurde. Die Kommunikation basiert auf dem cXML Protokoll und sie muss zwischen Systemen der kaufenden und verkaufenden Organisation eingerichtet werden.

Um die Kommunikation einzurichten, muss Ihr Kreditor Informationen für Sie zur Verwendung in der Konfiguration des externen Katalogs bereitstellen, wie Kennung, Domäne des Käufers, zum Beispiel "DUNS" und "Duns-Nummer", Anmeldeinformationen und die URL für den Kreditorenkatalog bereitstellen.

## <a name="setting-up-an-external-catalog"></a>Einrichten eines externen Katalogs

Der externe Katalog sollte einem Mitarbeiter, der eine Bestellanforderung eingibt, ermöglichen, auf einer externen Website die Produkte auszuwählen. Die Produkte, die der Mitarbeiter im externen Katalog auswählen, werden zu Dynamics 365 for Finance and Operations mit aktuellen Preisangaben zurückgegeben und von hier können sie der Bestellanforderung hinzugefügt werden. Die Absicht ist es, Mitarbeiter nicht dazu zu berechtigen, einen Auftrag auf einer externen Website zu erteilen. Wird der externe Katalog eingerichtet, müssen Sie prüfen, ob der Zweck der Seite, die auf den externen Lieferantenkatalog zugreifen kann, so ist, dass Angebotsinformationen gesammelt werden und kein tatsächlicher Auftrag erteilt wird.

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>Führen Sie zum Einrichten eines externen Lieferantenkatalogs die folgenden Aufgaben aus:

1. Richten Sie eine Beschaffungskategoriehierarchie ein. Weitere Informationen finden Sie unter [Einrichten einer Beschaffungskategoriehierarchie](tasks/set-up-policies-procurement-category-hierarchies.md).
2. Registrieren Sie den Kreditor im Bereich Finance and Operations. Bevor Sie Konfigurationen für den Zugriff auf einen externen Lieferantenkatalog einrichten können, müssen Sie zuerst den Kreditor und den Kreditorkontakt in Microsoft Dynamics 365 einrichten. Der externe Lieferantenkatalog muss auch der ausgewählten Beschaffungskategorie zugeordnet werden. Weitere Informationen zum Registrieren von Kreditoren in Microsoft Dynamics 365, finden Sie unter [Verwalten Sie Kreditorenzusammenarbeitbenutzer](manage-vendor-collaboration-users.md). Informationen zum Einrichten einer Beschaffungskategoriehierarchie und zum Zuordnen der Warencodes zu einer Beschaffungskategorie finden Sie unter [Lieferanten bestimmten Beschaffungskategorien zuweisen](tasks/approve-vendors-specific-procurement-categories.md).
3. Stellen Sie sicher, dass die Maßeinheiten und die Währung, die vom Lieferanten verwendet werden, eingerichtet werden. Informationen darüber, wie Sie eine Maßeinheit erstellen, finden Sie unter [Maßeinheit verwalten](../pim/tasks/manage-unit-measure.md).
4. Konfigurieren Sie den externen Lieferantenkatalog anhand der Anforderungen an die externe Katalogwebsite des Kreditors. Genauere Informationen zu dieser Aufgabe finden Sie unter [Konfigurieren des externen Lieferantenkataloge](#configure-the-external-vendor-catalog).
5. Testen Sie die Konfigurationen des externen Lieferantenkatalogs. Überprüfen Sie dabei, ob die Einstellungen funktionieren und Sie auf den Katalog zugreifen können. Verwenden Sie die Aktion **Einstellungen überprüfen**, um die angeforderte Nachricht aufzusetzen. Diese Nachricht soll Kreditorendie auf die externe Katalogwebsite leiten, die in einem Browserfenster geöffnet wird. Während der Prüfungs können Sie keine Artikel und Dienstleistungen beim Lieferanten bestellen. Zum Bestellen von Artikeln oder Dienstleistungen müssen Sie auf die Bestellanforderung des Lieferanten zugreifen.
6. Aktivieren Sie den externen Katalog, indem Sie die Schaltfläche **Katalog aktivieren** auf der Seite **Externe Kataloge** verwenden. Der externe Katalog muss aktiviert werden, bevor ihn Mitarbeiter verwenden können. Sie können jederzeit den externen Katalog deaktivieren.


## <a name="configure-the-external-vendor-catalog"></a>Konfigurieren Sie den externen Lieferantenkatalog

Dieser Abschnitt spezifiziert Informationen zur Aufgabe 4 im vorherigen Abschnitt.

1. Geben Sie einen Namen und eine Beschreibung für den externen Katalog des Lieferanten ein. Der Name, den Sie eingeben, wird im Einkaufskorb, der den externen Katalog darstellt, dem Mitarbeiter angezeigt, der eine Bestellanforderung erstellt. Mitarbeiter können auf den Einkaufskorb klicken, um den Katalog auf der externen Lieferantenkatalogseite zu öffnen.
2. Hier können Sie ein Bild hinzufügen, indem Sie die Aktivität **Bild für externen Katalog** verwenden. Das Bild erscheint im Einkaufskorb, der den externen Katalog darstellt und wird dem Mitarbeiter angezeigt, der eine Bestellanforderung erstellt. Beachten Sie, dass die Breite und Höhe des Bilds gleich sein müssen. Andernfalls wird das Bild nicht ordnungsgemäß angezeigt.
3. Wählen Sie aus, ob auf der Website die externe Katalogwebsite des Kreditors im selben Browserfenster erscheinen soll, in dem der Mitarbeiter die Anforderung erstellt hat oder ob sie in einem neuen Fenster geöffnet wird.
4. Wählen Sie den Lieferant für den Katalog aus. In der Liste **Juristische Personen** gibt es eine Zeile für jede juristische Person, in der der Kreditor eingerichtet wurde. Um Benutzer zu erlauben, Produkte direkt aus dem Lieferantenkatalog von gewissen juristischen Personen zu bestellen aber nicht von allen, können Sie die Schaltfläche **Zugriff sperren** oder **Zugriff ermöglichen** für jede juristische Person verwenden, für den der Katalog verfügbar oder nicht verfügbar sein soll.
5. Geben Sie im Feld **Standardvervall (Tage)** ein, wie viele Tage ein Angebot gültig ist und beim externen Kreditor erworben werden kann. Wird ein Angebot erstellt und von der externen Katalogwebsite des Kreditors abgerufen, gilt das Angebot ab dem aktuellen Systemdatum und bleibt für die in diesem Feld eingegebene Anzahl an Tagen gültig.
6. Klicken Sie auf die Schaltfläche **Hinzufügen**, um die Zuordnung der Beschaffungskategorien dem externen Katalog zu starten. Wählen Sie anschließend aus der Kategorieliste eine Kategorie aus. Die Liste der Kategorien ist eine Obermenge der Beschaffungskategorien, die dem Lieferant in allen juristischen Personen zugeordnet wurde, die für den Kreditor eingerichtet werden.
[!NOTE]
Beschaffungspolitische Richtlinien werden verwendet, um den Zugriff zu den Kategorien für die kaufende juristische Person oder Empfangsorganisationseinheit zuzulassen oder einzuschränken. Punchout auf einem externen Katalog setzt voraus, dass der Zugriff mit mindestens einer Beschaffungskategorien zulässig ist, die dem Katalog zugeordnet ist.
7. Richten Sie die cXML Einstellungs-Anforderungsnachricht ein, die an den Kreditor gesendet wird. Das automatisch generierte Nachrichtenformat ist die Mindest-Vorlage, die erforderlich ist, um eine Sitzung zu starten. Geben Sie Werte für die Markierungen aus.

Sie könnne jederzeit die vom System generierte Nachrichtenvorlage erneut laden, indem Sie auf **Nachrichtenformat wiederherstellen** klicken. Beachten Sie, dass, wenn Sie das Nachrichtenformat wiederherstellen, die aktuelle Meldung durch die automatisch generierte Nachricht ersetzt wird, die leere Markierungen hat.

### <a name="cxml-setup-message"></a>cXML Nachricht einrichten
Unten finden Sie eine Beschreibung der Tags, die in der Vorlage enthalten sind:

| Feld | Beschreibung | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|Di Domäne des Unternehmens des Käufers.|
|< Header >< From >< Credential>< Identity >< /Identity > | Die ID des Unternehmen des Käufers.|
|< Header >< To >< Credential domain=”” > | Die Domäne des Unternehmens des Lieferanten.|
|< Header >< To >< Credential>< Identity >< /Identity> | Die Indentität des Unternehmens des Lieferanten.|
|< Header >< Sender >< Credential domain=”” > | Di Domäne des Unternehmens des Käufers.|
|< Header >< Sender >< Credential >< Identity >< /Identity> | Die ID des Unternehmen des Käufers.|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|Das freigegebene Geheimnis für das Unternehmen des Käufers.|
|< Request deploymentMode=”” >|Die Test- oder Produktionsbereitstellung.|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|Die URL des Punchout-Enpunkt des Lieferanten.|

### <a name="extrinsic-elements"></a>Äußere Elemente

Ein systeminternes Element sind zusätzliche Informationen, wie beispielsweise Benutzername, die auf dem Benutzer basieren, der ein PunchOut durchführt. Das systeminterne Element wird festgelegt, wenn der PunchOut erfolgt, und es kann in der Anforderungseinstellungsnachricht gesendet werden.
Ihr Kreditor kann eine Anforderung für den Erhalt eines äußeren Elements in der Einstellungsanforderung haben. In diesem Fall sollten Sie das äußeren Elementen der Liste der äußeren Elemente im Abschnitt **Nachrichtenformat** der Seite **Externer Katalog** hinzufügen. Geben Sie einen Namen für das äußere Element an, das der Lieferant erkennen und einem Wert zuordnen kann. Die Optionen für Werte: Benutzernamen-, Benutzer--E-Mail oder Zufallswert.
Weitere Informationen zum cXML Protokoll, finden Sie hier: http://cxml.org/

## <a name="post-back-message"></a>Nachricht zurückbuchen
Die zurückgebuchte Nachricht ist die Meldung, die der Kreditor erhält, wenn der Benutzer sich von der externen Website abmeldet und zu Finance and Operations zurückkehrt. Rückmeldungsnachrichten können nicht konfiguriert werden. Die Meldungen basieren auf den cXML Protokolldefinition. Hierbei gelten die Informationen, die Teil der Rückmeldungsnachricht werden können, die auf einer Bestellanforderungsposition basieren:

| Meldung vom Kreditor empfangen | Kopiert die Bestellanforderungsposition nach Finance and Operations|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |Leistung|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|Externe Artikelkennung|
|< ItemDetail>< UnitPrice >< Money currency=”” >| Währung|
|< ItemDetail >< UnitPrice >< Money >< /Money >| Preis je Einheit|
|< ItemDetail >< Description ShortName=”” >|Produktname|
|< ItemDetail >< Description >< /Description >|In der Artikelbeschreibung eingeschlossen; Produktname, wenn Kurzname nicht angegeben wird.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Einheit|
|< ItemDetail >< Classification >< /Classification >|In der Artikelbeschreibung eingeschlossen|
|< ItemDetail >< Classification domain=”” >|In der Artikelbeschreibung eingeschlossen|

## <a name="delete-an-external-catalog"></a>Löschen eines externen Katalogs
Löschen eines externen Katalogs mit der Löschaktion auf der Seite.

Wenn ein Produkt aus dem externen Lieferantenkatalog angefordert wurde, kann der externe Lieferantenkatalog nicht gelöscht werden. Stattdessen wird der Status des externen Lieferantenkatalogs auf "Inaktiv" gesetzt. Wenn Sie den Zugriff auf die Katalogwebsite des externen Lieferanten entfernen möchten, ändern Sie den Status des externen Katalogs auf "Inaktiv".


