---
title: Steuerintegration für Commerce-Kanäle einrichten
description: Dieser Artikel enthält Richtlinien zum Einrichten der Steuerintegrationsfunktionen für Commerce-Kanäle.
author: EvgenyPopovMBS
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 9fd801395f2ba04c703734a1de7998d6a53b6462
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276131"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Steuerintegration für Commerce-Kanäle einrichten

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Richtlinien zum Einrichten der Steuerintegrationsfunktionen für Commerce-Kanäle. Weitere Informationen zur Steuerintegration finden Sie unter [Übersicht der Steuerintegration für Commerce-Kanäle](fiscal-integration-for-retail-channel.md).

## <a name="enable-features-in-commerce-headquarters"></a>Funktionen in der Commerce-Zentralverwaltung aktivieren

Führen Sie die folgenden Schritte aus, um Funktionen zu aktivieren, die sich auf die Steuerintegrationsfunktionalität für Commerce-Kanäle beziehen.

1. Gehen Sie in der Commerce headquarters zu **Systemadministration \> Arbeitsbereiche \> Funktionen verwalten**.
1. Finden und aktivieren Sie die folgenden Funktionen:

    - **Direkte Steuerintegration über POS-Kassen** – Die Funktion erweitert das Steuerintegrationsspektrum durch die Möglichkeit, Steuerkonnektoren zu erstellen, die in der Verkaufsstelle (POS) ausgeführt werden. Diese Art von Konnektor kommuniziert mit einem Finanzgerät oder -dienst, das bzw. der eine HTTP-API bereitgestellt. So muss für das Geschäft kein separates Gerät angeschafft werden. Die Funktion erlaubt die Nutzung von Mobilgeräten zur Steuerintegration, ohne dass eine gemeinsame Hardwarestation erforderlich ist.
    - **Überschreibungen für technisches Profil der Steuerintegration** – Diese Funktion ermöglicht die Erweiterung der Konfiguration der Steuerintegration und fügt die Möglichkeit hinzu, Verbindungsparameter auf der Einstellungsseite einer POS-Kasse zu überprüfen. Wenn diese Funktion aktiviert ist, können Sie die Parameter eines technischen Profils überschreiben.
    - **Status der Steuerregistrierung von POS-Kassen** – Wenn diese Funktion aktiviert ist, können Sie die Steuerregistrierung für bestimmte POS-Kassen deaktivieren. In diesem Fall können an der POS-Kasse keine Verkaufsbuchungen erfolgen.
    - **Lokaler Datenspeicher-Backup für Finanzverflechtung** – Diese Funktion erweitert die Fehlerbehandlungsfunktionen des Steuerintegrationsframework. Sie ermöglicht auch eine automatische Sicherung von Steuerregistrierungsdaten im Falle eines Datenverlusts, sodass die Daten im lokalen Speicher wiederhergestellt werden, während ein Gerät aktiviert wird.

## <a name="set-up-commerce-parameters"></a>Commerce-Parameter festlegen

Gehen Sie zum Einrichten von Commerce-Parametern folgendermaßen vor.

1. Setzen Sie auf der Seite **Freigegebene Commerce-Parameter** auf der Registerkarte **Allgemein** die Option **Steuerintegration aktivieren** auf **Ja**.
1. Definieren Sie auf der Registerkarte **Nummernkreise** die Nummernkreise der folgenden Referenzen:

    - Nummer des technischen Steuerprofils
    - Nummer der Steuerconnectorgruppe
    - Registrierungsprozessnummer

1. Definieren Sie auf der Seite **Commerce-Parameter** die Nummernfolge für die Nummer des funktionalen Steuerprofils.

> [!NOTE]
> Nummernkreise sind optional. Nummern für alle Entitäten der Steuerintegration können entweder aus Zahlenreihen oder manuell generiert werden.

## <a name="set-up-a-fiscal-registration-process"></a>Einrichten eines Steuerregistrierungsprozesses

Der Prozess der Einrichtung der Steuerintegration umfasst die folgenden allgemeinen Aufgaben:

- Konfigurieren Sie Steuerkonnectoren , die steuerbezogene Geräten oder Dienste repräsentieren, die zur Steuerregistrierung verwendet werden, wie beispielsweise Belegdrucker.
- Konfigurieren Sie Dokumentenanbieter, die Steuerdokumente generieren, die von Steuerkonnektoren in steuerbezogenen Geräten oder Diensten registriert werden.
- Konfigurieren Sie den Steuerregistrierungsprozess, der eine Reihe von Schritten der Steuerregistrierung definiert, und die Steuerkonnektoren und Steuerdokumentanbieter, die für jeden Schritt verwendet werden.
- Weisen Sie den steuerlichen Registrierungsprozess POS-Funktionsprofilen zu.
- Ordnen Sie die technischen Profile des Konnektors den Hardwareprofilen zu.
- Weisen Sie den Konnektoren technische Profile für die POS-Hardware oder Funktionsprofile zu.

### <a name="upload-configurations-of-fiscal-document-providers"></a>Konfigurationen von Anbietern von Fiskalbelegen hochladen

Ein Steuerdokumentanbieter ist für die Erstellung von Steuerdokumenten verantwortlich, die Transaktionen und Ereignisse darstellen, die am POS in einem Format registriert sind, das auch für die Interaktion mit einem steuerbezogenen Gerät oder Dienst verwendet wird. So kann beispielsweise ein Steuerdokumentanbieter eine Darstellung eines Steuerbelegs in einem XML-Format erzeugen.

Um Konfigurationen von fiskalischen Belegen hochzuladen, führen Sie diese Schritte aus.

1. Gehen Sie in der Commerce-Zentralverwaltung auf die Seite **Fiskalische Belege** (**Retail und Commerce \> Channel-Einrichtung \> Fiskalische Integration \> Fiskalische Belege**).
1. Laden Sie für jedes Gerät oder jeden Dienst, den Sie verwenden möchten, eine XML-Konfiguration hoch.

> [!TIP]
> Durch Auswahl von **Ansicht** können Sie alle funktionalen und technischen Profile anzeigen, die sich auf den aktuellen Steuerdokumentanbieter beziehen.

> [!NOTE]
> Die Datenabbildung wird als Teil eines Steuerdokumentanbieters betrachtet. Wenn Sie andere Datenenzuordnungen für den gleichen Konnektor einrichten (beispielsweise besondere Bestimmungen für ein Bundesland), sollten Sie verschiedene Steuerdokumentanbieter erstellen.

### <a name="upload-configurations-of-fiscal-connectors"></a>Hochladen von Konfigurationen für Fiskalkonnektoren

Ein Steuerkonnektor ist für die Kommunikation mit einem steuerbezogenen Gerät oder Dienst verantwortlich. So kann beispielsweise ein Steuerkonnektor einen Steuerbeleg, den ein Steuerdokumentanbieter in einem XML-Format erstellt hat, an einen Belegdrucker senden. Weitere Einzelheiten zu den Komponenten der Fiskalintegration finden Sie unter [Fiskalischer Registrierungsprozess und Fiskalintegrationsmuster für Fiskalgeräte und -dienste](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

Um Konfigurationen von fiskalischen Konnektoren hochzuladen, führen Sie diese Schritte aus.

1. Gehen Sie in der Commerce-Zentralverwaltung auf die Seite **Fiskalische Konnektoren** (**Retail und Commerce \> Channel-Einrichtung \> Fiskalische Integration \> Fiskalische Konnektoren**).
1. Laden Sie eine XML-Konfiguration für jedes Gerät oder jeden Dienst hoch, den Sie für die steuerliche Integration verwenden möchten.

> [!TIP]
> Durch Auswahl von **Ansicht** können Sie alle funktionalen und technischen Profile anzeigen, die sich auf den aktuellen Steuerkonnektor beziehen.

Beispiele für Konfigurationen von fiskalischen Konnektoren und Anbietern von fiskalischen Belegen finden Sie unter [Beispiele für die fiskalische Integration im Commerce SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-commerce-sdk).

### <a name="create-connector-functional-profiles"></a>Erstellen Sie funktionale Profile für Konnektoren

Um funktionale Profile für Konnektoren zu erstellen, folgen Sie diesen Schritten.

1. Gehen Sie in der Commerce-Zentralverwaltung auf die Seite **Funktionsprofile für Konnektoren** (**Handel und Commerce \> Einrichtung des Channels \> Fiscal Integration \> Funktionsprofile für Konnektoren**).
1. Erstellen Sie für jede Kombination aus einem fiskalischen Konnektor und einem Anbieter von fiskalischen Belegen, die mit diesem fiskalischen Konnektor verbunden ist, ein Konnektor-Funktionsprofil, indem Sie diese Schritte ausführen:

    1. Wählen Sie einen Verbindungsnamen.
    1. Wählen Sie einen Dokumentenanbieter.

#### <a name="change-data-mapping-parameters-in-a-connector-functional-profile"></a>Ändern Sie die Parameter für die Datenzuordnung in einem Funktionsprofil des Konnektors

Sie können die Datenenzuordnungsparameter in ein funktionales Profil des Konnektors ändern. Die folgende Tabelle enthält einige Beispiele für Parameter der Datenzuordnung in einem Funktionsprofil des Konnektors.

| Parameter | Formatieren | Beispiel |
|-----------|--------|---------|
| MwSt-Satzeinstellungen | Wert: MwSt-Satz | 1 : 2000, 2 : 1800 |
| Zuordnung von MwSt.-Codes | MwSt-Code: Wert | vat20: 1, vat18: 2 |
| Zahlungsmitteltyp-Zuordnung | TenderTyp: Wert | Bargeld: 1, Karte : 2 |

Um die Standardparameter wiederherzustellen, die in der Konfiguration des Anbieters von fiskalischen Belegen definiert sind, wählen Sie **Aktualisieren** auf der Seite **Konnektor Funktionsprofile**.

> [!NOTE]
> Funktionale Profile des Konnektors sind unternehmensspezifisch. Wenn Sie dieselbe Kombination aus einem Konnektor und einem Anbieter von fiskalischen Belegen für verschiedene Firmen verwenden möchten, sollten Sie für jede Firma ein Funktionsprofil für den Konnektor erstellen.

### <a name="create-connector-technical-profiles"></a>Erstellen Sie technische Profile für Konnektoren

Um technische Profile für Konnektoren zu erstellen, folgen Sie diesen Schritten.

1. Gehen Sie in der Commerce-Zentralverwaltung auf die Seite **Technische Profile des Konnektors** (**Handel und Commerce \> Channel Einrichtung \> Fiskalische Integration \> Technische Profile des Konnektors**).
1. Erstellen Sie für jeden fiskalischen Konnektor ein technisches Profil, indem Sie die folgenden Schritte ausführen:

    1. Wählen Sie einen Verbindungsnamen.
    1. Wählen Sie einen Konnektor-Typ:

        - Für Geräte oder Dienste, die mit einer Hardware-Station verbunden oder im lokalen Netzwerk vorhanden sind, wählen Sie **Lokal**.
        - Für externe Dienste wählen Sie **Extern**.
        - Für interne Konnektoren in der Commerce Runtime (CRT) wählen Sie **Intern**. 

    1. Wählen Sie einen Konnektor Standort:

        - Wenn sich der Konnektor auf der Hardwarestation befindet, wählen Sie **Hardwarestation**.
        - Wenn sich der Konnektor auf der POS-Kasse befindet, wählen Sie **Kasse**.

Parameter auf den Registerkarten **Gerät** und **Einstellungen** in einem technischen Profil des Konnektors können geändert werden. Um die Standardparameter wiederherzustellen, die in der Konfiguration des Steuerkonnektors definiert sind, wählen Sie **Aktualisierung**. Während eine neue Version einer XML-Konfiguration geladen wird, erhalten Sie eine Nachricht, die besagt, dass der aktuelle Fiskalkonnektor oder Fiskalbeleg-Anbieter bereits verwendet wird. Dieses Verfahren überschreibt keine manuellen Änderungen, die zuvor in den funktionalen Profilen und in den technischen Profilen des Konnektors vorgenommen wurden. Um die Standardparameter einer neuen Konfiguration festzulegen, wählen Sie **Aktualisieren** entweder auf der Seite **Funktionsprofile des Konnektors** oder auf der Seite **Technische Profile des Konnektors**.

Wenn Sie spezifische Parameter für eine einzelne Kasse oder einen Store festlegen müssen, gehen Sie wie folgt vor.

1. Wählen Sie den Menüpunkt **Aufheben**.
1. Erstellen Sie auf der Seite **Aufheben** einen neuen Datensatz.
1. Wählen Sie einen Store oder eine POS-Kasse. Sie können die Parameter des ausgewählten technischen Profils für eine einzelne Kasse oder alle Kassen in einer einzelnen Filiale außer Kraft setzen.
1. Auf der Registerkarte **Gerät** geben Sie die Parameter für die ausgewählte Kasse oder den Store ein.

### <a name="create-fiscal-connector-groups"></a>Erstellen Sie fiskalische Konnektorengruppen

Eine Steuerkonnektorgruppe ist eine Teilmenge funktionaler Profile des Konnektors, die mit steuerlichen Verbindungen verknüpft werden, um identische Funktionen auszuführen und im gleichen Schritt innerhalb eines Steuerregistrierungsprozesses verwendet zu werden. Wenn beispielsweise mehrere Modelle eines Belegdruckers in einem Shop verwendet werden können, können Steuerkonnektoren für diese Belegdrucker in einer Steuerkonnektorengruppe kombiniert werden.

Um eine Gruppe fiskalischer Konnektoren zu erstellen, folgen Sie diesen Schritten.

1. Gehen Sie auf die Seite **Fiskalische Konnektoren** (**Einzelhandel und Commerce \> Einrichtung der Kanäle \> Fiskalische Integration \> Fiskalische Konnektoren**).
1. Erstellen Sie eine neue fiskalische Konnektor-Gruppe.
1. Hier können Sie funktionale Profile der Konnektorgruppe hinzufügen Klicken Sie auf der Seite **Funktionale Profile** auf **Hinzufügen** und wählen Sie eine Profilnummer aus. Jeder fiskalische Konnektor in einer Konnektorgruppe kann nur ein Funktionsprofil haben.
1. Wenn Sie die Nutzung des funktionalen Profils unterbrechen möchten, stellen Sie die Option **Deaktivieren** auf **Ja** ein. Diese Änderung betrifft nur die aktuelle Konnektorgruppe. Sie können das selbe funktionale Profil in anderen Konnektorgruppen weiter nutzen.

### <a name="create-a-fiscal-registration-process"></a>Erstellen Sie einen steuerlichen Registrierungsprozess

Ein Steuerregistrierungsprozess wird durch den Nummernkreis der Erfassungsschritte und der Konnektorgruppe definiert, die für jeden Schritt verwendet werden.

Um einen fiskalischen Registrierungsprozess zu erstellen, führen Sie diese Schritte aus.

1. Gehen Sie in der Commerce-Zentralverwaltung auf die Seite **Fiskalische Registrierungsprozesse** (**Retail und Commerce \> Channel-Einrichtung \> Fiskalische Integration \> Fiskalische Registrierungsprozesse**).
1. Erstellen Sie einen neuen Datensatz für jeden einzelnen fiskalischen Registrierungsprozess.
1. Fügen Sie dem Prozess Registrierungsschritte hinzu, indem Sie diese Schritte befolgen:

    1. Wählen Sie **Hinzufügen** aus.
    1. Wählen Sie einen Steuerkonnektortyp aus:
    1. Wählen Sie im Feld **Gruppennummer** eine entsprechende Steuerkonnektorgruppe aus.

### <a name="assign-entities-of-the-fiscal-registration-process-to-pos-profiles"></a>Weisen Sie Entitäten des steuerlichen Registrierungsprozesses POS-Profilen zu

Um Entitäten des fiskalischen Registrierungsprozesses POS-Profilen zuzuordnen, führen Sie diese Schritte aus.

1. Gehen Sie in der Commerce-Zentralverwaltung auf die Seite **POS-Funktionsprofile** (**Retail und Commerce \> Channel Einrichtung \> POS Einrichtung \> POS Profile \> Funktionsprofile**). 
1. Weisen Sie den steuerlichen Registrierungsprozess einem POS-Funktionsprofil zu.
1. Wählen Sie **Bearbeiten**, und wählen Sie dann auf der Registerkarte **Steuerregistrierungsprozess** im Feld **Prozessnummer** einen Prozess aus.
1. Auf der Registerkarte **Steuerliche Dienste** wählen Sie technische Profile des Konnektors mit dem Konnektorstandort **Registrieren**.
1. Gehen Sie auf die Seite **POS-Hardwareprofil** (**Retail und Commerce \> Einrichtung der Kanäle \> Einrichtung der Kassen \> POS-Profile \> Hardwareprofile**).
1. Weisen Sie einem Hardwareprofil technische Profile für Konnektoren zu. 
1. Wählen Sie **Bearbeiten** und fügen Sie dann auf der Registerkarte **Steuerliche Peripheriegeräte** eine Zeile hinzu. 
1. Wählen Sie im Feld **Profilnummer** ein technisches Profil für den Konnektor aus.
1. Wählen Sie auf der Registerkarte **Steuerliche Peripheriegeräte** technische Profile für Konnektoren mit dem Standort des Konnektors **Hardware Station**.

> [!NOTE]
> Sie können mehrere technische Profile dem gleichen Hardwareprofil hinzufügen. Ein Hardwareprofil oder POS-Funktionalitätsprofil sollte jedoch nur einen Schnittpunkt mit einer beliebigen Steuerkonnektorgruppe aufweisen.

Der Flow der Fiskalregistrierung wird durch den Prozess der Fiskalregistrierung und auch durch einige Parameter der Fiskalintegrationskomponenten definiert: die Erweiterung CRT für den Anbieter von Fiskalbelegen und die Erweiterung Hardware-Station für den Fiskalkonnektor.

- Der Dauerauftrag für Ereignisse und Transaktionen der Steuererfassung ist im Steuerdokumentanbieter vordefiniert.
- Die Steuerdokumentanbieter ist auch für das Identifizieren des Steuerkonnektors zuständig, der zur Steuerregistrierung verwendet wird. Es stimmt die funktionalen Profile des Konnektors, die in der Steuerkonnektorgruppe enthalten sind, die für den aktuellen Schritt des Steuerregistrierungsprozess spezifiziert ist, mit dem dem Profil des Konnektors ab, das dem Hardwareprofil der Hardwarestation zugeordnet ist, mit der der POS gekoppelt ist.
- Der Steuerdokumentanbieter verwendet die Datenmapping-Einstellungen aus der Konfiguration des Steuerdokumentanbieters, um Transaktions-/Ereignisdaten wie Steuern und Zahlungen zu transformieren, während ein Steuerdokument erzeugt wird.
- Wenn der Steuerdokumentanbieter ein Steuerdokument erzeugt, kann der Steuerkonnektor es entweder unverändert an das Fiskalgerät senden oder es analysieren und in eine Folge von Befehlen der Geräte-API umwandeln, je nachdem, wie die Kommunikation gehandhabt wird.

### <a name="set-up-registers-with-fiscal-registration-restrictions"></a>Register mit steuerlichen Registrierungsbeschränkungen festlegen

Sie können Register auswählen, bei denen die fiskalische Registrierung verboten ist, z.B. in Fällen, in denen Sie auf diesen Geräten nur nicht-fiskalische Vorgänge wie die Suche im Produktkatalog, das Nachschlagefeld für Kunden oder die Erstellung von Transaktionsentwürfen anbieten möchten.

Um Register mit fiskalischen Registrierungsbeschränkungen festzulegen, folgen Sie diesen Schritten.

1. Gehen Sie in der Commerce headquarters zu **Einzelhandel und Commerce \> Channel-Einrichtung \> Steuerliche Integration \> Steuerliche Registrierungsprozesse**.
1. Wählen Sie den gewünschten Prozess.
1. Wählen Sie die Registerkarte **POS-Register mit fiskalischen Verarbeitungsbeschränkungen**.
1. Fügen Sie nach Bedarf Register mit fiskalischen Prozessbeschränkungen hinzu.

### <a name="validate-the-fiscal-registration-process"></a>Validieren Sie den Prozess der steuerlichen Registrierung

Es wird empfohlen, den fiskalischen Registrierungsprozess in den folgenden Fällen zu validieren:

- Sie haben alle Einstellungen für einen neuen Registrierungsprozess festgelegt. Diese Einstellungen umfassen die Zuordnung von Registrierungsprozessen zu POS-Funktionsprofilen und Hardwareprofilen.
- Sie haben Änderungen an einem bestehenden fiskalischen Registrierungsprozess vorgenommen, und diese Änderungen können dazu führen, dass zur Laufzeit ein anderer fiskalischer Konnektor ausgewählt wird. (Sie haben z.B. die Konnektorgruppe für einen Prozessschritt der steuerlichen Registrierung geändert, ein Konnektor-Funktionsprofil in einer Konnektorgruppe aktiviert oder ein neues Konnektor-Funktionsprofil zu einer Konnektorgruppe hinzugefügt.)
- Sie haben Änderungen an der Zuordnung von technischen Profilen des Konnektors zu Hardwareprofilen vorgenommen.

Führen Sie diese Schritte aus, um den Prozess der Fiskalregistrierung zu bestätigen.

1. Gehen Sie in der Commerce-Zentralverwaltung auf die Seite **Fiskalische Registrierungsprozesse** (**Retail und Commerce \> Channel-Einrichtung \> Fiskalische Integration \> Fiskalische Registrierungsprozesse**).
1. Wählen Sie **Validieren**, um den Prozess der steuerlichen Registrierung zu validieren.
1. Führen Sie auf der Seite **Distributionsplan** die Aufträge **1070** und **1090** aus, um Daten in die Kanaldatenbank zu übertragen.

## <a name="set-up-fiscal-texts-for-discounts"></a>Steuertexte für Rabatte einrichten

In einigen Fällen muss ein spezieller Text auf einem Steuerbeleg gedruckt werden, wenn ein Rabatt gewährt wird. Sie können Steuertexte auf der Seite **Steuerkonnektorgruppe** (**Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuerkonnektorgruppen**) einrichten.

- Für manuelle Rabatte, die am POS angewendet werden, sollten Sie einen Steuertext für den Infocode oder die Infocode-Gruppe einstellen, der im POS-Funktionalitätsprofil als Infocode **Produktrabatt** angegeben ist.

    1. Wählen Sie auf der Seite **Steuerkonnektorgruppe** **Text für Steuerbeleg** aus.
    1. Auf der Registerkarte **Infocodes** wählen Sie **Hinzufügen** und wählen einen Infocode oder eine Infocodegruppe aus.
    1. Wählen Sie im Feld **Info-Code-Nummer** einen Wert aus.
    1. Im Feld **Untercodenummer** wählen Sie einen Wert aus, wenn ein Untercode für den ausgewählten Infocode erforderlich ist.
    1. Wählen Sie im Feld **Text für Steuerbeleg** einen Steuertext an, der auf einen Steuerbeleg gedruckt werden soll.
    1. Setzen Sie die Option **Benutzereingabe beim Steuerbeleg** auf **Ja**, um den Text auf einem Steuerbeleg mit Informationen zu überschreiben, die ein Benutzer manuell am POS eingibt. Diese Option gilt nur für Infocodes, die einen Eingabetyp **Text** haben.

    > [!NOTE]
    > Sie können einen Steuertext für mehrere Info-Codes angeben, um Szenarien zu unterstützen, in denen Info-Codegruppen, verknüpfte Info-Codes und ausgelöste Info-Codes verwendet werden. In diesen Szenarien enthält der Steuerbeleg die Steuertexte aller Infocodes, die mit der Transaktionszeile verknüpft sind, in der der Rabatt gewährt wurde.

- Für kanalbezogene Rabatte sollten Sie einen Steuertext für die Rabattkennung definieren.

    1. Wählen Sie auf der Seite **Steuerkonnektorgruppe** **Text für Steuerbeleg** aus.
    1. Wählen Sie auf der Registerkarte **Rabatte** **Hinzufügen** und wählen Sie eine Rabattkennung.
    1. Wählen Sie im Feld **Text für Steuerbeleg** einen Steuertext an, der auf einen Steuerbeleg gedruckt werden soll.

    > [!NOTE]
    > Wenn mehrere Rabatte auf dieselbe Buchungszeile angewendet werden, enthält der Steuerbeleg Steuertexte von allen Rabatten, die mit dieser Buchungszeile verknüpft sind.

## <a name="set-error-handling-settings"></a>Einstellungen zur Fehlerbehandlung festlegen

Die Optionen für die Fehlerbehandlung, die in der Steuerintegration zur Verfügung stehen, werden im Prozess der Steuerregistrierung festgelegt. Weitere Informationen zur Fehlerbehandlung in der Steuerintegration finden Sie unter [Fehlerbehandlung](fiscal-integration-for-retail-channel.md#error-handling).

Um die Einstellungen für die Fehlerbehandlung festzulegen, gehen Sie folgendermaßen vor.

1. Auf der Seite **Steuerregistrierungsprozess** (**Einzelhandel und Handel \> Kanaleinrichtung \> Steuerintegration \> Steuerregistrierungsprozesse**) können Sie die folgenden Parameter für jeden Schritt des Steuerregistrierungsprozesses einstellen:

    - **Überspringen erlauben** - Dieser Parameter aktiviert die Option **Überspringen** im Dialogfenster zur Fehlerbehandlung.
    - **Als registriert markieren erlauben** - Dieser Parameter aktiviert die Option **Als registriert markieren** im Dialogfenster zur Fehlerbehandlung.
    - **Aufschieben zulassen** - Dieser Parameter aktiviert die Option **Aufschieben** im Dialogfeld zur Fehlerbehandlung.
    - **Bei Fehler fortsetzen** – Wenn dieser Parameter aktiviert ist, kann der steuerlichen Registrierungsprozess im POS-Register fortgesetzt werden, wenn bei der Transaktion einer Steuererfassung oder eines Ereignisses ein Fehler auftritt. Um die Steuererfassung der nächsten Transaktion oder des Ereignisses sonst auszuführen, muss der Mitarbeiter die fehlerhafte Steuererfassung erneut ausführen, sie überspringen, oder die Buchung oder das Ereignis als erfasst markieren. Weitere Informationen finden Sie unter [Optionale Steuererfassung](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Wenn der Parameter **Bei Fehler fortsetzen** aktiviert wird, sind die Parameter **überspringen zulassen** und **als erfasst markieren** automatisch deaktiviert.

1. Die Optionen **Überspringen** und **Als registriert markieren** im Dialogfenster zur Fehlerbehandlung erfordern, dass die Berechtigung **Registrierung überspringen oder als registriert markieren zulassen** aktiviert ist. Um diese Berechtigung zu aktivieren, gehen Sie auf die Seite **Berechtigungsgruppen** (**Einzelhandel und Commerce \> Mitarbeiter \> Berechtigungsgruppen**) und legen Sie die Option **Zulassen, dass Registrierung übersprungen oder als registriert markiert wird** auf **Ja** fest.
1. Die Option **Aufschieben** im Dialogfenster für die Fehlerbehandlung erfordert, dass die Berechtigung **Aufschieben zulassen** aktiviert ist. Um die Berechtigung zu aktivieren, gehen Sie auf die Seite **Berechtigungsgruppen** (**Retail und Commerce \> Mitarbeiter \> Berechtigungsgruppen**) und legen Sie die Option **Verschiebung zulassen** auf **Ja** fest.
1. Mit den Optionen **Überspringen**, **Als registriert markieren** und **Verschieben** können Operatoren zusätzliche Informationen eingeben, wenn die Fiskalregistrierung fehlschlägt. Um diese Funktion verfügbar zu machen, sollten Sie die Info-Codes **Auslassen**, **Als registriert markieren** und **Aufschieben** auf einer fiskalischen Konnektor-Gruppe angeben. Die von den Bedienern eingegebenen Informationen werden dann als Infocodetransaktion gespeichert, die mit dem Steuertransaktion verknüpft ist. Weitere Informationen zu Infocodes, finden Sie unter [Infocodes und Infocodegruppen](../info-codes-retail.md).

    > [!NOTE]
    > Die Auslösefunktion **Produkt** wird für die Infocodes, die für **Überspringen** und **Als registriert markieren** in Steuerkonnektorgruppen verwendet werden, nicht unterstützt.

    - Wählen Sie auf der Seite **Steuerlicher Konnektor** auf der Registerkarte **Infocodes** Infocodes oder Infocodegruppen in den Feldern **Überspringen**, **Als registriert markieren** und **Aufschieben**.

    > [!NOTE]
    > Ein Steuerdokument und ein nicht-steuerliches Dokument können in jedem Schritt eines Steuerregistrierungsprozesses erzeugt werden. Eine Erweiterung des Steuerdokumentanbieters identifiziert jede Art von Transaktion oder Ereignis als steuerliches oder nicht steuerliches Dokument. Die Fehlerbehandlung gilt nur für Steuerdokumente.
    >
    > - **Steuerdokument** - Ein obligatorisches Dokument, das erfolgreich registriert werden sollte (z.B. ein Steuerbeleg).
    > - **Nicht-steuerliches Dokument** – Ein ergänzender Beleg für die Transaktion oder das Ereignis (z.B. ein Geschenkgutschein).

1. Wenn der Operator in der Lage sein muss, den aktuellen Arbeitsgang zu verarbeiten (beispielsweise zur Erstellung oder zum Abschluss einer Transaktion), nachdem ein Integritätsprüfungsfehler auftritt, sollten Sie die Berechtigung **Überspringen des Integritätsprüfungsfehler zulassen** auf der Seite **Berechtigungsgruppen** (**Einzelhandel und Handel \> Mitarbeiter \> Berechtigungsgruppen**) aktivieren. Weitere Informationen zur Integritätsprüfungsprozedur finden Sie unter[Steuerliche Erfassungsintegritätsprüfung](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Einrichten von steuerlichen X/Z-Berichten von der POS aus

Um die Ausführung von X/Z-Berichten aus der POS heraus zu ermöglichen, sollten Sie einem POS-Layout neue Schaltflächen hinzufügen.

- Folgen Sie auf der Seite **Schaltflächenraster** den Anweisungen unter [POS-Operationen zu POS-Layouts hinzufügen, indem Sie den Button Grid Designer](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) verwenden, um den Designer zu installieren und ein POS-Layout zu aktualisieren.

    1. Wählen Sie das zu aktualisierende Layout aus. 
    1. Fügen Sie eine neue Schaltfläche hinzu und legen Sie die Eigenschaft der Schaltfläche **Steuer X drucken** fest.
    1. Fügen Sie eine neue Schaltfläche hinzu und legen Sie die Eigenschaft der Schaltfläche **Steuer Z drucken** fest.
    1. Führen Sie auf der Seite **Distributionszeitplan** den Auftrag **1090** aus, um Änderungen in die Kanaldatenbank zu übertragen.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Aktivieren Sie die manuelle Ausführung der verschobenen steuerlichen Erfassung.

Um die manuelle Ausführung einer aufgeschobenen steuerlichen Erfassung zu aktivieren, können Sie einer Schaltfläche ein neues POS-Layout hinzufügen.

- Folgen Sie auf der Seite **Schaltflächenraster** den Anweisungen unter [POS-Operationen zu POS-Layouts hinzufügen, indem Sie den Button Grid Designer](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) verwenden, um den Designer zu installieren und ein POS-Layout zu aktualisieren.

    1. Wählen Sie das zu aktualisierende Layout aus.
    1. Fügen Sie eine neue Schaltfläche hinzu und legen Sie die Eigenschaft der Schaltfläche auf **Steuererlicher Registrierungsprozess abschliessen**
    1. Führen Sie auf der Seite **Distributionszeitplan** den Auftrag **1090** aus, um Ihre Änderungen in die Kanaldatenbank zu übertragen.


## <a name="view-connection-parameters-and-other-information-in-pos"></a>Verbindungsparameter und andere Informationen in POS anzeigen

Gehen Sie wie folgt vor, um Verbindungsparameter und andere Informationen in POS anzuzeigen.

1. Öffnen Sie das Modern POS (MPOS) oder Cloud POS (CPOS).
1. Wählen Sie **Einstellungen**. Wenn die Steuerintegration aktiviert ist, zeigt der Abschnitt **Steuerintegration** auf der rechten Seite die folgenden Informationen:

    - Der Status der Steuerregistrierung
    - Der Status der letzten Steuertransaktion
    - Die Anzahl ausstehender Überwachungsereignisse

1. Wählen Sie **Details**, um die folgenden Informationen anzuzeigen:

    - Registrierungsprozessschritte
    - Verbindungsparameter
    - Überwachungsereignisdetails
 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
