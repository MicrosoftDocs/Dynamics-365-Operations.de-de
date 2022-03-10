---
title: Kleinpaketlieferung
description: Dieses Thema enthält Informationen zur Kleinpaketlieferung. Diese Funktion aktiviert Microsoft Dynamics 365 Supply Chain Management, um Details zu einem gepackten Container an den Spediteur zu senden und dann ein Adressetikett, einen Frachtsatz und eine Sendungsverfolgungsnummer von diesem Spediteur zu erhalten.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: cb5a4195d94750fcbee00e7301bd250f653cb347
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576087"
---
# <a name="small-parcel-shipping"></a>Kleinpaketlieferung

[!include [banner](../../includes/banner.md)]

Die Kleinpaketlieferung ermöglicht Microsoft Dynamics 365 Supply Chain Management die direkte Interaktion mit Spediteuren durch die Bereitstellung eines Frameworks für die Kommunikation über Spediteur-APIs. Diese Funktion ist nützlich, wenn Sie einzelne Aufträge über kommerzielle Spediteure versenden, anstatt sich für den Containerversand oder den Versand mit weniger als Wagenladung zu entscheiden.

Die Kleinpaketlieferung interagiert mit Ihrem Spediteur über ein dediziertes *Tarifmodul*. Ihre Organisation muss dieses Tarifmodul in Zusammenarbeit mit dem Spediteur oder dem Spediteurnetzwerk entwickeln. Dieses Tarifmodul aktiviert Supply Chain Management, um Details zu einem gepackten Container an den Spediteur zu senden und dann ein Adressetikett, einen Frachtsatz und eine Sendungsverfolgungsnummer von diesem Spediteur zu erhalten.

Der übermittelte Frachtsatz wird dem zugehörigen Auftrag als sonstige Gebühr hinzugefügt. Das Adressetikett kann dann automatisch mit einem ZPL-Drucker (Zebra Programming Language) ausgedruckt und an der Lieferung angebracht werden. Der Spediteur scannt dieses Adressetikett, wenn er die Päckchen an Ihrem Lagerort abholt.

## <a name="prepare-your-system-to-support-sps"></a>Vorbereiten Ihres System auf die Kleinpaketlieferung

Bevor Sie die Kleinpaketlieferung verwenden können, müssen Sie sie in der Funktionsverwaltung aktivieren, Ihr Traifmodul hinzufügen und die Module **Transportverwaltung** und **Lagerortverwaltung** entsprechend einrichten.

### <a name="turn-on-the-sps-feature"></a>Aktivieren der Kleinpaketlieferung

Bevor Sie die Kleinpaketlieferung nutzen können, muss sie in Ihrem System aktiviert werden. Administratoren können den Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu prüfen und sie bei Bedarf einzuschalten. Dort wird die Funktion folgendermaßen aufgelistet:

- **Modul:** *Transportverwaltung*
- **Funktionsname:** *Kleinpaketlieferung*

### <a name="deploy-and-set-up-rate-engines"></a>Bereitstellen und Einrichten von Tarifmodulen

Supply Chain Management umfasst keine Tarifmodule. Die benötigten Tarifmodule müssen bezogen oder erstellt und dann zu Ihrem System hinzugefügt werden. Microsoft bietet jedoch eine Demotarifmodule an, die Sie zum Testen verwenden könnten.

#### <a name="download-and-deploy-the-demo-rate-engine"></a>Herunterladen und Bereitstellen des Demotarifmoduls

Befolgen Sie diese Schritte, um das Demotarifmodul zu erhalten.

1. Laden Sie auf GitHub die [Dynamic Link Library (DLL) für das Demotarifmodul](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS) herunter.
1. Speichern Sie die DLL auf Ihrem Supply Chain Management-Server im Ordner **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.

#### <a name="create-and-deploy-functional-rate-engines"></a>Erstellen und Bereitstellen funktionsfähiger Tarifmodule

Informationen zum Erstellen und Bereitstellen funktionsfähiger Tarifmodule, die in einer Produktions- oder Testumgebung verwendet werden können, finden Sie in den folgenden Themen:

- [Erstellen eines neuen Transportverwaltungsmoduls](../transportation/create-new-transportation-management-engine.md)
- [Einrichten von Transportverwaltungsmodulen](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

Weitere Informationen zum Erstellen eines Tarifmoduls für die Kleinpaketlieferung finden Sie im folgenden Blogbeitrag: [Kleinpaketlieferung: Nutzung der Kleinpaketlieferung in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a>Einrichten eines Tarifmoduls in Supply Chain Management

Führen Sie die folgenden Schritte aus, nachdem Sie ein Tarifmodul für die Kleinpaketlieferung erstellt und bereitgestellt haben.

1. Wechseln Sie zu **Transportverwaltung \> Einrichten \> Module \> Tarifmodul**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Felder fest.

    - **Tarifmodul** – Geben Sie einen eindeutigen Namen für das Tarifmodul ein. Wenn Sie das Demotarifmodul verwenden, geben Sie *Demotarifmodul* ein.
    - **Name** – Geben Sie eine kurze Beschreibung des Tarifmoduls ein. Wenn Sie das Demotarifmodul verwenden, geben Sie *Demotarifmodul* ein.
    - **Bewertungs-Metadaten-ID** – Wählen Sie die Basis aus, auf der Ihr Tarif berechnet werden soll. Zum Beispiel könnte Ihr Tarif basierend auf der Entfernung berechnet werden. Wenn Sie das Demotarifmodul verwenden, können Sie dieses Feld leer lassen.
    - **Modulassembly** – Geben Sie den Dateinamen des von Ihnen bereitgestellten DLL-Pakets ein. Wenn Sie das Demotarifmodul verwenden, geben Sie *TMSSmallParcelShippingEngine.dll* ein.
    - **Modulklasse** – Geben Sie den Klassennamen ein, der für Ihr Tarifmodul festgelegt wurde. Wenn Sie das Demotarifmodul verwenden, geben Sie *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine* ein.

## <a name="example-scenario"></a>Beispielszenario

Dieses Beispielszenario zeigt, wie Sie die Kleinpaketlieferung einrichten und verwenden, nachdem Sie Ihr System wie zuvor in diesem Thema beschrieben vorbereitet haben. In diesem Szenario wird das zuvor erwähnte Demotarifmodul verwendet.

### <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Um dieses Szenario mit den hier angegebenen Demodatensätzen und -werten durchzuarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

### <a name="set-up-the-scenario"></a>Szenario einrichten

In diesem Beispielszenario müssen Sie über einen Demospediteur, eine Spediteurgruppe, eine Verpackungsrichtlinie und ein Verpackungsprofil verfügen. In den folgenden Unterabschnitten wird erläutert, wie Sie die für das Szenario erforderlichen Datensätze vorbereiten. In einem Produktionsszenario ähnelt der Einrichtungsprozess normalerweise dem hier beschriebenen Prozess. Sie werden jedoch andere Werte einstellen.

#### <a name="set-up-carriers"></a>Einrichten von Spediteuren

Gehen Sie folgendermaßen vor, um einen Spediteur einzurichten.

1. Wechseln Sie zu **Transportverwaltung \> Einstellungen \> Spediteure \> Spediteure**.
1. Wählen Sie im Aktionsbereich **Neu** aus, um einen Spediteur hinzuzufügen.
1. Legen Sie in der Kopfzeile die folgenden Werte fest:

    - **Spediteur:** *Demospediteur*
    - **Name:** *Demospediteur*
    - **Modus:** *Boden*

1. Legen Sie im Inforegister **Übersicht** die folgenden Werte fest:

    - **Spediteur aktivieren:** *Ja*
    - **Spediteur-Rating aktivieren:** *Ja*

1. Wählen Sie im Inforegister **Dienstleistungen** die Option **Neu** aus, um dem Raster eine Dienstleistung hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Dienstleistung fest.

    - **Spediteurdienstleistung:** *Demospediteurdienstleistung*
    - **Name:** *Demospediteurdienstleistung*
    - **Transportmethode:** *Boden*

    Geben Sie nach Bedarf beliebige Werte für alle anderen Felder ein. (Wenn Sie den neuen Spediteurdatensatz speichern, wird eine neue Lieferart erstellt und das Feld **Lieferart** wird automatisch festgelegt.)

1. Wählen Sie im Inforegister **Bewertungsprofile** die Option **Neu** aus, um ein Bewertungsprofil zum Raster hinzuzufügen.
1. Legen Sie die folgenden Werte für das neue Profil fest:

    - **Bewertungsprofil:** *Demospediteurdienstleistung*
    - **Name:** *Demospediteurdienstleistung*
    - **Tarifmodul:** *Demotarifmodul*

    Geben Sie nach Bedarf beliebige Werte für alle anderen Felder ein.

1. Wählen Sie im Aktionsbereich **Speichern** aus.

Weitere Informationen zum Einrichten von Spediteuren finden Sie unter [Spediteure einrichten](../transportation/tasks/set-up-shipping-carriers.md).

#### <a name="set-up-carrier-service-accounts"></a>Einrichten von Spediteurdienstleistungskonten

Gehen Sie folgendermaßen vor, um ein Spediteurdienstleistungskonto einzurichten.

1. Wechseln Sie zu **Transportverwaltung \> Einrichten \> Bewertung \> Spediteurdienstleistungskonto**.
1. Wählen Sie im Aktionsbereich **Neu** aus, um ein Spediteurdienstleistungskonto hinzuzufügen.
1. Legen Sie die folgenden Werte für das neue Konto fest:

    - **Spediteur:** *Demospediteur*
    - **Spediteurdienstleistung:** *Demospediteurdienstleistung*
    - **Kundenkontonummer des Spediteurs:** Die Kundenkontonummer des Spediteurs, mit der die Verbindung zum Spediteur überprüft und authentifiziert wird. Ihr Spediteur wird diesen Wert bereitstellen. Wenn Sie die Demodienstleistung verwenden, können Sie einen beliebigen Wert eingeben.
    - **Standort:** *6*
    - **Lagerort:** *62*

    > [!NOTE]
    > Oft ist die **Kundenkontonummer des Spediteurs** der einzige Wert, der zur Authentifizierung der Verbindung erforderlich ist. Wenn Ihr Spediteur jedoch zusätzliche Authentifizierungsparameter benötigt, sollte Ihre Organisation diese Seite anpassen, um gegebenenfalls zusätzliche Felder hinzuzufügen.

#### <a name="set-up-a-container-packing-policy"></a>Einrichten einer Containerverpackungsrichtlinie

Gehen Sie zum Einrichten einer Containerverpackungsrichtlinie folgendermaßen vor.

1. Wenn Sie noch keine ZPL-Druckerdefinition eingerichtet haben, richten Sie sie mit der Anwendung Document Routing Agent ein. Weitere Informationen finden Sie unter [Übersicht zum Dokumentendruck](../../fin-ops-core/dev-itpro/analytics/print-documents.md) und verwandten Themen.
1. Wechseln Sie zu **Lagerortverwaltung \> Einrichten \> Container \> Containerverpackungsrichtlinien**.
1. Wählen Sie im Aktionsbereich **Neu** aus, um eine Containerverpackungsrichtlinie hinzuzufügen.
1. Legen Sie in der Kopfzeile der neuen Richtlinie die folgenden Werte fest:

    - **Containerverpackungsrichtlinie:** *Demoverpackungsrichtlinie*
    - **Beschreibung:** Eine Beschreibung der Richtlinie.

1. Legen Sie im Inforegister **Übersicht** die folgenden Werte fest:

    - **Lagerort:** *62*
    - **Standardlagerplatz für letzte Lieferung:** *Ladebereichstor*
    - **Gewichtseinheit:** *KG*
    - **Richtlinie zum Containerabschluss:** *Automatische Freigabe*
    - **Richtlinien zur Containerfreigabe:** *Am endgültigen Versandort zur Verfügung stellen*

1. Legen Sie im Inforegister **Containermanifestierung** die folgenden Werte fest:

    - **Automatisch manifestieren beim Schließen des Containers:** *Ja*
    - **Manifestanforderungen für Container:** *Transportverwaltung*
    - **Containerinhalt drucken:** *Nein*

1. Legen Sie im Inforegister **Containerbeschriftungsdruck** die folgenden Werte fest:

    - **Adressetikett für Container drucken:** *Immer*
    - **Druckername:** Der Name des ZPL-Druckers, der Adressetiketten drucken soll.

#### <a name="set-up-a-packing-profile"></a>Einrichten eines Verpackungsprofils

Gehen Sie zum Einrichten eines Verpackungsprofils folgendermaßen vor.

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichten \> Verpackung \> Verpackungsprofile**.
1. Wählen Sie im Aktionsbereich **Neu** aus, um ein Verpackungsprofil zum Raster hinzuzufügen.
1. Legen Sie die folgenden Werte für das neue Profil fest:

    - **Verpackungsprofilkennung:** *Demoverpackungsprofil*
    - **Beschreibung:** Eine Beschreibung des Profils.
    - **Containerverpackungsrichtlinie:** *Demoverpackungsrichtlinie*
    - **Containerkennungsmodus:** *Auto*
    - **Containertyp:** *Kleiner Karton*

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a>Einrichten eines Kunden zurVerwendung des Spediteurs für Kleinpaketlieferungen

Führen Sie die folgenden Schritte aus, um einen Kunden so einzurichten, dass er den von Ihnen erstellten Spediteur verwenden kann.

1. Wechseln Sie zu **Debitoren \> Kunden \> Alle Kunden**.
1. Suchen Sie im Raster den Kunden *US-027* und wählen Sie ihn aus.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Allgemein** in der Gruppe **Einrichten** die Option **Kundenkonten des Spediteurs** aus.
1. Wählen Sie auf der Seite **Kundenkonten des Spediteurs** im Aktionsbereich **Neu** aus, um ein Konto zum Raster hinzuzufügen.
1. Legen Sie die folgenden Werte für das neue Konto fest:

    - **Spediteur:** *Demospediteur*
    - **Kundenkontonummer des Spediteurs:** *12345* (Der Wert ist für dieses Szenario nicht wichtig, wird jedoch im nächsten Abschnitt referenziert.)

### <a name="go-through-the-example-scenario"></a>Durchgehen des Beispielszenarios

Nachdem Sie alle Beispieldaten wie im vorherigen Abschnitt beschrieben eingerichtet haben, können Sie das Beispielszenario durchgehen.

#### <a name="create-a-sales-order-and-process-the-work"></a>Erstellen eines Auftrags und bearbeiten der Arbeit

Gehen Sie folgendermaßen vor, um einen Auftrag zu erstellen.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** das Feld **Debitorenkonto** auf *US-027* fest.
1. Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.
1. Der neue Auftrag wird geöffnet. Legen Sie im Inforegister **Auftragskopf** das Feld **Kundenkontonummer des Spediteurs** auf den Wert fest, den Sie zuvor für diesen Kunden ausgewählt haben (*12345*).
1. Fügen Sie im Abschnitt **Auftragspositionen** eine Verkaufsposition hinzu und legen Sie die folgenden Werte dafür fest:

    - **Artikelnummer:** *A0002*
    - **Menge** *1*
    - **Standort:** *6*
    - **Lagerort:** *62*

1. Wechseln Sie zur Ansicht **Kopfzeile**.
1. Legen Sie im Inforegister **Lieferung** die folgenden Werte fest:

    - **Spediteur:** *Demospediteur*
    - **Spediteurdienstleistung:** *Demospediteurdienstleistung*

1. Wechseln Sie zurück zur Ansicht **Positionen**. Wenn Sie aufgefordert werden, die Lieferart für die Verkaufspositionen zu aktualisieren, wählen Sie **Ja** aus.
1. Wählen Sie im Abschnitt **Auftragspositionen** die Auftragsposition aus, die Sie zuvor eingerichtet haben, und wählen Sie dann **Bestand \> Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.
1. Schließen Sie die Seite **Reservierung**, um zum Auftrag zurückzukehren.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.

    Es wird Arbeit erstellt, um Artikel vom Kommissionierort zur Verpackungsstation zu bewegen.

1. Wechseln Sie im Abschnitt **Auftragspositionen** zu **Lagerort \> Lieferdetails**.
1. Notieren Sie sich auf der Seite **Lieferdetails** die Lieferungs-ID. Sie benötigen sie, wenn Sie das Paket an der Verpackungsstation verpacken.
1. Schließen Sie die Seite **Lieferdetails**, um zum Auftrag zurückzukehren.
1. Notieren Sie sich die Auftragsnummer und wechseln Sie dann zu **Lagerortverwaltung \> Arbeit \> Alle Arbeit**.
1. Verwenden Sie die Auftragsnummer, um die Arbeit zu finden und auszuwählen, die für den Auftrag erstellt wurde.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Arbeit** die Option **Arbeit abschließen** aus.
1. Wählen Sie auf der Seite **Arbeitsabschluss** im Feld **Benutzer-ID** eine Benutzer-ID aus. Wählen Sie im Aktionsbereich **Arbeit überprüfen** aus.
1. Bei einer erfolgreichen Prüfung wählen Sie im Aktionsbereich **Arbeit abschließen** aus.

    Die Arbeit wird als abgeschlossen markiert, um die Bewegung von Artikeln zur Verpackungsstation zu simulieren.

#### <a name="pack-the-shipment"></a>Verpacken der Lieferung

Gehen Sie folgendermaßen vor, um die Lieferung zu verpacken.

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichten \> Arbeitskraft** und stellen Sie sicher, dass Ihr Benutzerkonto einem Arbeitskraftkonto für die Lagerortverwaltung zugeordnet ist.
1. WechselnWarehouse Management Solution Sie zu **Lagerortverwaltung \> Kommissionierung und Containerisierung \> Paket**.
1. Legen Sie im Dialogfeld **Verpackungsstation auswählen** die folgenden Werte fest:

    - **Standort:** *6*
    - **Lagerort:** *62*
    - **Lagerplatz:** *Verpackung*
    - **Verpackungsprofilkennung:** *Demoverpackungsprofil*

1. Wählen Sie **OK**.
1. Die Seite **Paket** wird angezeigt. In einem Produktionsszenario scannt eine Arbeitskraft ein Kennzeichen oder eine Lieferungs-ID. Öffnen Sie für dieses Szenario jedoch die Seite **Alle Lieferungen** und suchen Sie die Liefernummer für die Lieferung, die Sie gerade erstellt haben. Geben Sie dann diesen Wert in das Feld **Kennzeichen oder Lieferung** auf der Seite **Paket** ein. Geben Sie alternativ die Lieferungs-ID ein, die Sie zuvor notiert haben.
1. Wählen Sie im Aktivitätsbereich **Neuer Container** aus.
1. Das angezeigte Dialogfeld zeigt Details zum neuen Container an. Behalten Sie die Standardwerte bei und wählen Sie dann **OK** aus.
1. Wählen Sie auf der Seite **Paket** im Inforegister **Artikelverpackung** im Feld **Kennung** den Wert *A0002* aus, um den Artikel zu verpacken. Der Artikel wird dem Container hinzugefügt.
1. Wählen Sie im Aktionsbereich **Container für Lieferung** aus.

    Die angezeigte Seite **Container für Lieferung** enthält eine Zeile für den Container, den Sie gerade erstellt haben. Das Feld **Containermanifestierungs-ID** in dieser Zeile ist derzeit jedoch leer, da Sie das Adressetikett und die Sendungsverfolgungsnummer noch nicht vom Spediteur erhalten haben.

1. Wählen Sie im Aktivitätsbereich **Container schließen** aus.
1. Legen Sie im Dialogeld **Container schließen** das Feld **Bruttogewicht** auf *1 kg* fest und wählen Sie dann **OK** aus.

    Das Adressetikett sollte jetzt auf dem zuvor ausgewählten ZPL-Drucker gedruckt werden. Es sollte dem folgenden Beispiel ähneln.

    ![Beispieladressetikett.](media/sps-label-example.png "Beispieladressetikett")

1. Beachten Sie, dass die Werte für **Containermanifestierungs-ID** und **Gesamtfracht** als vom Spediteur erhalten hinzugefügt wurden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]