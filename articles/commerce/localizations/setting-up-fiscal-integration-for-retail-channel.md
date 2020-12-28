---
title: Steuerintegration für Commerce-Kanäle einrichten
description: Dieses Thema enthält Richtlinien zum Einrichten der Steuerintegrationsfunktionen für Commerce-Kanäle.
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b221bfede5d1db8d7970e1efede85e8dba7fe017
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412445"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Steuerintegration für Commerce-Kanäle einrichten

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Einführung

Dieses Thema enthält Richtlinien zum Einrichten der Steuerintegrationsfunktionen für Commerce-Kanäle. Weitere Informationen zur Steuerintegration finden Sie unter [Übersicht der Steuerintegration für Commerce-Kanäle](fiscal-integration-for-retail-channel.md).

Der Prozess der Einrichtung der Steuerintegration umfasst die folgenden allgemeinen Aufgaben:

1. Konfigurieren Sie Steuerkonnectoren , die steuerbezogene Geräten oder Dienste repräsentieren, die zur Steuerregistrierung verwendet werden, wie beispielsweise Belegdrucker.
2. Konfigurieren Sie Dokumentenanbieter, die Steuerdokumente generieren, die von Steuerkonnektoren in steuerbezogenen Geräten oder Diensten registriert werden.
3. Konfigurieren Sie den Steuerregistrierungsprozess, der eine Reihe von Schritten der Steuerregistrierung definiert, und die Steuerkonnektoren und Steuerdokumentanbieter, die für jeden Schritt verwendet werden.
4. Ordnen Sie den Steuerregistrierungsprozess den Funktionsprofilen der Verkaufsstellen (POS) zu.
5. Ordnen Sie die technischen Profile des Konnektors den Hardwareprofilen zu.

## <a name="set-up-a-fiscal-registration-process"></a>Einrichten eines Steuerregistrierungsprozesses

Vor der Verwendung der Steuerintegrationsfunktionen müssen Sie die folgenden Einstellungen konfigurieren.

1. Commerce-Parameter aktualisieren.

    1. Setzen Sie auf der Seite **Freigegebene Commerce-Parameter** auf der Registerkarte **Allgemein** die Option **Steuerintegration aktivieren** auf **Ja**. Definieren Sie auf der Registerkarte **Nummernkreise** die Nummernkreise der folgenden Referenzen:

        - Nummer des technischen Steuerprofils
        - Nummer der Steuerconnectorgruppe
        - Registrierungsprozessnummer

    2. Definieren Sie auf der Seite **Commerce-Parameter** die Nummernfolge für die Nummer des funktionalen Steuerprofils.

    > [!NOTE]
    > Nummernkreise sind optional. Nummern für alle Entitäten der Steuerintegration können entweder aus Zahlenreihen oder manuell generiert werden.

2. Laden Sie Konfigurationen der Steuerkonnectoren und Steuerdokumentanbieter hoch.

    Ein Steuerdokumentanbieter ist für die Erstellung von Steuerdokumenten verantwortlich, die Transaktionen und Ereignisse darstellen, die am POS in einem Format registriert sind, das auch für die Interaktion mit einem steuerbezogenen Gerät oder Dienst verwendet wird. So kann beispielsweise ein Steuerdokumentanbieter eine Darstellung eines Steuerbelegs in einem XML-Format erzeugen.

    Ein Steuerkonnektor ist für die Kommunikation mit einem steuerbezogenen Gerät oder Dienst verantwortlich. So kann beispielsweise ein Steuerkonnektor einen Steuerbeleg, den ein Steuerdokumentanbieter in einem XML-Format erstellt hat, an einen Belegdrucker senden. Genauere Informationen zu Ateuerintegrationskomponenten finden Sie unter [Steuerregistrierungsprozess und Steuerintegrationsbeispiele für steuerbezogene Geräte](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

    1. Laden Sie auf der Seite **Steuerkonnektoren** (**Retail und Commerce \> Kanaleinrichtung \> Steuerintegration \> Steuerkonnektoren**) eine XML-Konfiguration für jedes Gerät oder jeden Dienst hoch, den Sie für Zwecke der Steuerintegration verwenden möchten.

        > [!TIP]
        > Durch Auswahl von **Ansicht** können Sie alle funktionalen und technischen Profile anzeigen, die sich auf den aktuellen Steuerkonnektor beziehen.

    2. Laden Sie auf der Seite **Steuerdokumentanbieter** (**Retail und Commerce \> Kanaleinrichtung \> Steuerintegration \> Steuerdokumentanbieter**) eine XML-Konfiguration für jedes Gerät oder jeden Dienst hoch, den Sie verwenden möchten.

        > [!TIP]
        > Durch Auswahl von **Ansicht** können Sie alle funktionalen und technischen Profile anzeigen, die sich auf den aktuellen Steuerdokumentanbieter beziehen.

    Beispiele für die Konfiguration von Steuerkonnektoren und Steuerdokumentanbieter finden Sie unter [Steuerintegrationsbeispiele im Retail SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk).

    > [!NOTE]
    > Die Datenabbildung wird als Teil eines Steuerdokumentanbieters betrachtet. Wenn Sie andere Datenenzuordnungen für den gleichen Konnektor einrichten (beispielsweise besondere Bestimmungen für ein Bundesland), sollten Sie verschiedene Steuerdokumentanbieter erstellen.

3. Erstellen Sie funktionale Profile und technische Profile des Konnektors.

    1. Erstellen Sie auf der Seite **Funktionale Connector-Profile** (**Retail und Commerce \> Kanaleinrichtung \> Steuerintegration \> Funktionale Connector-Profile**) ein funktionales Connector-Profil für jede Kombination aus einem Steuerkonnektor und einem Steuerdokumentanbieter, der mit diesem Steuerkonnektor verbunden ist.

        1. Wählen Sie einen Verbindungsnamen.
        2. Wählen Sie einen Dokumentenanbieter.

        Sie können die Datenenzuordnungsparameter in ein funktionales Profil des Konnektors ändern. Um die Standardparameter wiederherzustellen, die in der Konfiguration des Steuerdokumentanbieters definiert sind, wählen Sie **Aktualisierung**.

        **Beispiele**

        |   | Formate | Beispiel |
        |---|--------|---------|
        | **MwSt-Satzeinstellungen** | Wert: MwSt-Satz | 1 : 2000, 2 : 1800 |
        | **Zuordnung von MwSt.-Codes** | MwSt-Code: Wert | vat20: 1, vat18: 2 |
        | **Zahlungsmitteltyp-Zuordnung** | TenderTyp: Wert | Bargeld: 1, Karte : 2 |

        > [!NOTE]
        > Funktionale Profile des Konnektors sind unternehmensspezifisch. Wenn Sie planen, die gleiche Kombination aus einem Steuerkonnektor und einem Steuerdokumentanbieter in verschiedenen Unternehmen zu verwenden, sollten Sie für jedes Unternehmen ein funktionales Profil des Konnektors anlegen.

    2. Erstellen Sie auf der Seite **Technische Connector-Profile** (**Retail und Commerce \> Kanaleinrichtung \> Steuerintegration \> Technische Connector-Profile**) ein technisches Profil für jeden Steuerkonnektor.

        1. Wählen Sie einen Verbindungsnamen.
        2. Wählen Sie einen Konnektortyp aus. Für Geräte, die mit einer Hardwarestation verbunden sind, wählen Sie **Lokal**.

            > [!NOTE]
            > Nur lokaler Konnektoren werden derzeit unterstützt.

        Parameter auf den Registerkarten **Gerät** und **Einstellungen** in einem technischen Profil des Konnektors können geändert werden. Um die Standardparameter wiederherzustellen, die in der Konfiguration des Steuerkonnektors definiert sind, wählen Sie **Aktualisierung**. Während eine neue Version einer XML-Konfiguration geladen wird, erhalten Sie eine Nachricht, durch die angegeben wird, dass der aktuelle Konnektor oder Steuerdokumentanbieter bereits verwendet wird. Dieses Verfahren überschreibt keine manuellen Änderungen, die zuvor in den funktionalen Profilen und in den technischen Profilen des Konnektors vorgenommen wurden. Um den Standardparametersatz aus einer neuen Konfiguration anzuwenden, wählen Sie auf der Seite **Funktionale Profile des Connectors** oder der Seite **Technische Profile des Konnektors** **Aktualisieren**.

4. Erstellen Sie Steuerkonnektorgruppen.

    Eine Steuerkonnektorgruppe ist eine Teilmenge funktionaler Profile des Konnektors, die mit steuerlichen Verbindungen verknüpft werden, um identische Funktionen auszuführen und im gleichen Schritt innerhalb eines Steuerregistrierungsprozesses verwendet zu werden. Wenn beispielsweise mehrere Modelle eines Belegdruckers in einem Shop verwendet werden können, können Steuerkonnektoren für diese Belegdrucker in einer Steuerkonnektorengruppe kombiniert werden.

    1. Auf der Seite **Steuerkonnektorgruppe** (**Retail und Commerce \> Kanaleinrichtung \> Steuerintegration \> Steuerkonnektorgruppen**) erstellen Sie eine neue Steuerkonnektorgruppe.
    2. Hier können Sie funktionale Profile der Konnektorgruppe hinzufügen Klicken Sie auf der Seite **Funktionale Profile** auf **Hinzufügen** und wählen Sie eine Profilnummer aus. jeder Steuerkonnektor innerhalb einer Konnektorgruppe kann nur ein funktionales Profil haben.
    3. Wenn Sie die Nutzung des funktionalen Profils unterbrechen möchten, stellen Sie die Option **Deaktivieren** auf **Ja** ein. Diese Änderung betrifft nur die aktuelle Konnektorgruppe. Sie können das selbe funktionale Profil in anderen Konnektorgruppen weiter nutzen.

5. Erstellen eines Steuerregistrierungsprozesses.

    Ein Steuerregistrierungsprozess wird durch den Nummernkreis der Erfassungsschritte und der Konnektorgruppe definiert, die für jeden Schritt verwendet werden.

    1. Erstellen Sie auf der Seite **Steuerregistrierungsprozess** (**Retail und Commerce \> Kanal einrichten \> Steuerintegration \> Steuerregistrierungsprozesse**) für jeden eindeutigen Prozess der Steuerintegration einen neuen Datensatz.
    2. Fügen Sie Erfassungsschritte dem Prozess hinzu:

        1. Wählen Sie **Hinzufügen** aus.
        2. Wählen Sie einen Steuerkonnektortyp aus:
        3. Wählen Sie im Feld **Gruppennummer** eine entsprechende Steuerkonnektorgruppe aus.

6. Ordnen Sie Entitäten des Steuerregistrierungsprozess den POS-Profilen zu.

    1. Auf der Seite **POS-Funktionsprofile** (**Retail und Commerce \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \>-Funktionsprofile**) weisen Sie den Steuerregistrierungsprozess einem POS-Funktionsprofil zu. Wählen Sie **Bearbeiten**, und wählen Sie dann auf der Registerkarte **Steuerregistrierungsprozess** im Feld **Prozessnummer** einen Prozess aus.
    2. Weisen Sie auf der Seite **POS-Hardwareprofil** (**Retail und Commerce \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Hardwareprofile**) die technischen Connector-Profile einem Hardwareprofil zu. Wählen Sie **Bearbeiten**, fügen Sie eine Zeile auf der Registerkarte **Peripheriegeräte für die Steuerverwaltung** hinzu und wählen Sie dann im Feld **Profilnummer** ein technisches Profil des Connectors aus.

    > [!NOTE]
    > Sie können mehrere technische Profile dem gleichen Hardwareprofil hinzufügen. Ein Hardwareprofil oder POS-Funktionalitätsprofil sollte jedoch nur einen Schnittpunkt mit einer beliebigen Steuerkonnektorgruppe aufweisen.

    Der Ablauf der Steuerregistrierung wird durch den steuerlichen Registrierungsprozess und auch durch einige Parameter von Komponenten der Steuerintegration definiert: die Commerce-Laufzeiterweisterung für den Steuerdokumentanbieter und die Hardwarestationserweiterung für den Steuerkonnektor.

    - Der Dauerauftrag für Ereignisse und Transaktionen der Steuererfassung ist im Steuerdokumentanbieter vordefiniert.
    - Die Steuerdokumentanbieter ist auch für das Identifizieren des Steuerkonnektors zuständig, der zur Steuerregistrierung verwendet wird. Es stimmt die funktionalen Profile des Konnektors, die in der Steuerkonnektorgruppe enthalten sind, die für den aktuellen Schritt des Steuerregistrierungsprozess spezifiziert ist, mit dem dem Profil des Konnektors ab, das dem Hardwareprofil der Hardwarestation zugeordnet ist, mit der der POS gekoppelt ist.
    - Der Steuerdokumentanbieter verwendet die Datenmapping-Einstellungen aus der Konfiguration des Steuerdokumentanbieters, um Transaktions-/Ereignisdaten wie Steuern und Zahlungen zu transformieren, während ein Steuerdokument erzeugt wird.
    - Wenn der Steuerdokumentanbieter ein Steuerdokument erzeugt, kann der Steuerkonnektor es entweder unverändert an das Fiskalgerät senden oder es analysieren und in eine Folge von Befehlen der API (Device Application Programming Interface) umwandeln, je nachdem, wie die Kommunikation gehandhabt wird.

7. Wählen Sie auf der Seite **Steuerregistrierungsprozess** (**Retail und Commerce \> Kanaleinrichtung \> Steuerintegration \> Steuerregistrierungsprozesse**) **Prüfen**, um den steuerlichen Registrierungsprozess zu validieren.

    Es wird empfohlen, diese Art der Überprüfung in den folgenden Fällen ausführen:

    - Nachdem Sie alle Einstellungen für einen neuen Registrierungsprozess vorgenommen haben, auch wenn Sie Registrierungsprozesse POS-Funktionsprofilen und Hardwareprofilen zuordnen.
    - Nachdem Sie Änderungen an einem bestehenden Steuerregistrierungsprozess vorgenommen haben, können diese Änderungen dazu führen, dass zur Laufzeit ein anderer Steuerkonnektor ausgewählt wird (z.B. wenn Sie die Konnektorgruppe für einen Schritt des Steuerregistrierungsprozesses ändern, ein Konnektorfunktionsprofil in einer Konnektorgruppe aktivieren oder ein neues Konnektorfunktionsprofil zu einer Konnektorgruppe hinzufügen).
    - Nachdem Sie Änderungen in der Zuordnung der technischen Profile des Konnektors in Hardwareprofilen vorgenommen haben.

8. Führen Sie auf der Seite **Distributionsplan** die Aufträge **1070** und **1090** aus, um Daten in die Kanaldatenbank zu übertragen.

## <a name="set-up-fiscal-texts-for-discounts"></a>Steuertexte für Rabatte einrichten

In einigen Fällen muss ein spezieller Text auf einem Steuerbeleg gedruckt werden, wenn ein Rabatt gewährt wird. Sie können Steuertexte auf der Seite **Steuerkonnektorgruppe** (**Retail und Commerce \> Kanaleinrichtung \> Steuerintegration \> Steuerkonnektorgruppen**) einrichten.

- Für manuelle Rabatte, die am POS angewendet werden, sollten Sie einen Steuertext für den Infocode oder die Infocode-Gruppe einstellen, der im POS-Funktionalitätsprofil als Infocode **Produktrabatt** angegeben ist.

    1. Wählen Sie auf der Seite **Steuerkonnektorgruppe** **Text für Steuerbeleg** aus.
    2. Auf der Registerkarte **Infocodes** wählen Sie **Hinzufügen** und wählen einen Infocode oder eine Infocodegruppe aus.
    3. Wählen Sie unter **Infocodenummer** einen Wert aus.
    4. Im Feld **Untercodenummer** wählen Sie einen Wert aus, wenn ein Untercode für den ausgewählten Infocode erforderlich ist.
    5. Wählen Sie im Feld **Text für Steuerbeleg** einen Steuertext an, der auf einen Steuerbeleg gedruckt werden soll.
    6. Setzen Sie die Option **Benutzereingabe beim Steuerbeleg** auf **Ja**, um den Text auf einem Steuerbeleg mit Informationen zu überschreiben, die ein Benutzer manuell am POS eingibt. Diese Option gilt nur für Infocodes, die einen Eingabetyp **Text**  haben.

    > [!NOTE]
    > Sie können einen Steuertext für mehrere Info-Codes angeben, um Szenarien zu unterstützen, in denen Info-Codegruppen, verknüpfte Info-Codes und ausgelöste Info-Codes verwendet werden. In diesen Szenarien enthält der Steuerbeleg die Steuertexte aller Infocodes, die mit der Transaktionszeile verknüpft sind, in der der Rabatt gewährt wurde.

- Für kanalbezogene Rabatte sollten Sie einen Steuertext für die Rabattkennung definieren.

    1. Wählen Sie auf der Seite **Steuerkonnektorgruppe** **Text für Steuerbeleg** aus.
    2. Wählen Sie auf der Registerkarte **Rabatte** **Hinzufügen** und wählen Sie eine Rabattkennung.
    3. Wählen Sie im Feld **Text für Steuerbeleg** einen Steuertext an, der auf einen Steuerbeleg gedruckt werden soll.

    > [!NOTE]
    > Wenn mehrere Rabatte auf dieselbe Buchungszeile angewendet werden, enthält der Steuerbeleg Steuertexte von allen Rabatten, die mit dieser Buchungszeile verknüpft sind.

## <a name="set-error-handling-settings"></a>Einstellungen zur Fehlerbehandlung festlegen

Die Optionen für die Fehlerbehandlung, die in der Steuerintegration zur Verfügung stehen, werden im Prozess der Steuerregistrierung festgelegt. Weitere Informationen zur Fehlerbehandlung in der Steuerintegration finden Sie unter [Fehlerbehandlung](fiscal-integration-for-retail-channel.md#error-handling).

1. Auf der Seite **Steuerregistrierungsprozess** (**Retail und Commerce \> Kanaleinrichtung \> Steuerintegration \> Steuerregistrierungsprozesse**) können Sie die folgenden Parameter für jeden Schritt des Steuerregistrierungsprozesses einstellen:

    - **Überspringen erlauben** - Dieser Parameter aktiviert die Option **Überspringen** im Dialogfenster zur Fehlerbehandlung.
    - **Als registriert markieren erlauben** - Dieser Parameter aktiviert die Option **Als registriert markieren** im Dialogfenster zur Fehlerbehandlung.
    - **Bei Fehler fortsetzen** – Wenn dieser Parameter aktiviert ist, kann der steuerlichen Registrierungsprozess im POS-Register fortgesetzt werden, wenn bei der Transaktion einer Steuererfassung oder eines Ereignisses ein Fehler auftritt. Um die Steuererfassung der nächsten Transaktion oder des Ereignisses sonst auszuführen, muss der Mitarbeiter die fehlerhafte Steuererfassung erneut ausführen, sie überspringen, oder die Buchung oder das Ereignis als erfasst markieren. Weitere Informationen finden Sie unter [Optionale Steuererfassung](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Wenn der Parameter **Bei Fehler fortsetzen** aktiviert wird, sind die Parameter **überspringen zulassen** und **als erfasst markieren** automatisch deaktiviert.

2. Die Optionen **Überspringen** und **Als registriert markieren** im Dialogfenster zur Fehlerbehandlung benötigen die Berechtigung **überspringen oder als registriert markiert zulassen**. Aktivieren Sie daher auf der Seite **Berechtigungsgruppen** (**Retail und Commerce \> Mitarbeiter \> Berechtigungsgruppen**) die Berechtigung **Überspringen der Registrierung zulassen oder als registriert markieren**.
3. Die Optionen **Überspringen** und **Als registriert markieren** ermöglichen es den Operatoren, zusätzliche Informationen einzugeben, wenn die Steuerregistrierung fehlschlägt. Um diese Funktionalität zur Verfügung zu stellen, sollten Sie die **Überspringen** und **Als registriert markieren** Infocodes auf einer Steuerkonnektorgruppe angeben. Die von den Bedienern eingegebenen Informationen werden dann als Infocodetransaktion gespeichert, die mit dem Steuertransaktion verknüpft ist. Weitere Informationen zu Infocodes, finden Sie unter [Infocodes und Infocodegruppen](../info-codes-retail.md).

    > [!NOTE]
    > Die Auslösefunktion **Produkt** wird für die Infocodes, die für **Überspringen** und **Als registriert markieren** in Steuerkonnektorgruppen verwendet werden, nicht unterstützt.

    - Wählen Sie auf der Seite **Steuerkonnektorgruppe** auf der Registerkarte **Infocodes** Infocodes oder Infocodegruppen in den Feldern **Überspringen** und **Als registriert markieren** aus.

    > [!NOTE]
    > Ein Steuerdokument und ein nicht-steuerliches Dokument können in jedem Schritt eines Steuerregistrierungsprozesses erzeugt werden. Eine Erweiterung des Steuerdokumentanbieters identifiziert jede Art von Transaktion oder Ereignis als steuerliches oder nicht steuerliches Dokument. Die Fehlerbehandlung gilt nur für Steuerdokumente.
    >
    > - **Steuerdokument** - Ein obligatorisches Dokument, das erfolgreich registriert werden sollte (z.B. ein Steuerbeleg).
    > - **Nicht-steuerliches Dokument** – Ein ergänzender Beleg für die Transaktion oder das Ereignis (z.B. ein Geschenkgutschein).

4. Wenn der Operator in der Lage sein muss, den aktuellen Arbeitsgang zu verarbeiten (beispielsweise zur Erstellung oder zum Abschluss einer Transaktion), nachdem ein Integritätsprüfungsfehler auftritt, sollten Sie die Berechtigung **Überspringen des Integritätsprüfungsfehler zulassen** auf der Seite **Berechtigungsgruppen** (**Retail und Commerce \> Mitarbeiter \> Berechtigungsgruppen**) aktivieren. Weitere Informationen zur Integritätsprüfungsprozedur finden Sie unter[Steuerliche Erfassungsintegritätsprüfung](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Einrichten von steuerlichen X/Z-Berichten von der POS aus

Um die Ausführung von X/Z-Berichten aus der POS heraus zu ermöglichen, sollten Sie einem POS-Layout neue Schaltflächen hinzufügen.

- Folgen Sie auf der Seite **Schaltflächenraster** den Anweisungen unter [POS-Operationen zu POS-Layouts hinzufügen, indem Sie den Button Grid Designer](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) verwenden, um den Designer zu installieren und ein POS-Layout zu aktualisieren.

    1. Wählen Sie das zu aktualisierende Layout aus. 
    2. Fügen Sie eine neue Schaltfläche hinzu und legen Sie die Eigenschaft der Schaltfläche **Steuer X drucken** fest.
    3. Fügen Sie eine neue Schaltfläche hinzu und legen Sie die Eigenschaft der Schaltfläche **Steuer Z drucken** fest.
    4. Führen Sie auf der Seite **Distributionszeitplan** den Auftrag **1090** aus, um Änderungen in die Kanaldatenbank zu übertragen.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Aktivieren Sie die manuelle Ausführung der verschobenen steuerlichen Erfassung.

Um die manuelle Ausführung einer aufgeschobenen steuerlichen Erfassung zu aktivieren, können Sie einer Schaltfläche ein neues POS-Layout hinzufügen.

- Folgen Sie auf der Seite **Schaltflächenraster** den Anweisungen unter [POS-Operationen zu POS-Layouts hinzufügen, indem Sie den Button Grid Designer](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) verwenden, um den Designer zu installieren und ein POS-Layout zu aktualisieren.

    1. Wählen Sie das zu aktualisierende Layout aus.
    2. Fügen Sie eine neue Schaltfläche hinzu und legen Sie die Eigenschaft der Schaltfläche  auf **Steuererlicher Registrierungsprozess abschliessen**
    3. Führen Sie auf der Seite **Distributionszeitplan** den Auftrag **1090** aus, um Ihre Änderungen in die Kanaldatenbank zu übertragen.
