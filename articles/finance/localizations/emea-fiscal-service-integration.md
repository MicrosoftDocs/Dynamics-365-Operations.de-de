---
title: Integration von steuerlichem Dienst (ESR)
description: Dieses Thema enthält Informationen zur Integration eines steuerlichen Diensts für Österreich und die Tschechische Republik.
author: Anasyash
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashRegister_W
audience: Application user
ms.reviewer: kfend
ms.search.region: Austria, Czech Republic
ms.author: Anasyash
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 7740ae9af85efc7ba91048d436c6f5eca9fef4cb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226197"
---
# <a name="fiscal-service-esr-integration"></a>Integration von steuerlichem Dienst (ESR)

[!include [banner](../includes/banner.md)]

In Österreich sollten alle Barzahlungen durch ein externes Gerät oder einen externen Dienst signiert werden, und sie sollten sicher gespeichert werden. In der Tschechischen Republik sollten alle Barzahlungen an das Behördenportal für eine steuerliche Signatur übermittelt werden. In beiden Ländern sollte ein Barbeleg ausgestellt werden, auf dem die Signatur, bzw. Unterschrift gedruckt wird.

Um diese landesspezifischen Anforderungen zu unterstützen, ermöglicht Dynamics 365 Finance Ihnen, eine Integration mit dem steuerlichen Dienst eines Drittanbieters herzustellen, der bestimmte Anforderungen für die Barzahlungskontrolle in verschiedenen Ländern oder Regionen erfüllt.

> [!NOTE]
> Es wird vorausgesetzt, dass der steuerliche Dienst des Drittanbieters alle anderen landesspezifischen gesetzlichen Anforderungen bezüglich registrierter Transaktionen erfüllt. Sie sind für die ordnungsgemäße Einrichtung und Verwaltung des steuerlichen Diensts verantwortlich.

## <a name="available-configurations"></a>Verfügbare Konfigurationen

Die Formate des Barbelegs, die XML-Anforderung des steuerlichen Diensts und die XML-Antwort vom steuerlichen Dienst werden als Konfigurationen zur elektronischen Berichterstellung (EB) konfiguriert, die in der Bibliothek freigegebener Anlagen in Microsoft Dynamics Lifecycle Services (LCS) gespeichert werden. Die folgenden Konfigurationen sind verfügbar.

| Konfigurationsname | Konfigurationsbeschreibung | Kommentar | EB-Konfigurationsdatei in der LCS-Bibliothek freigegebener Anlagen |
|---|---|---|---|
| **Barbelegmodell** | | **Datenmodell für das Barbelegformat** | **Barbeleg Model.version.1.xml** |
| Barbelegformat | | Grundlegendes Format für einen Barbeleg | Barbeleg Format.version.1.1.xml |
| Barbelegformat (AT) | | Format für ein Barbeleg in Österreich (Dieses Format enthält einen Quick Response Code \[QR-Code\]) | Barbelegformat (AT).version.1.1.1.xml |
| Barbelegformat (CZ) | | Format für einen Barbeleg in der Tschechischen Republik (Dieses Format enthält die ID der Geschäftsräumlichkeiten \[BP\].) | Barbelegformat (CZ).version.1.1.1.xml |
| **Kassenmodell** | | **Datenmodell für Kassenintegration** | **Kasse Model.version.1.xml** |
| ESR-Anforderungsbeispiel | Beispiel einer einfachen Beleganforderung (ESR) gemäß der European Fiscal Standards Association (EFSTA) | Grundformat für eine Beispiel-XML-Anforderung an den steuerlichen Dienst der EFSTA (Dieses Format kann in Österreich verwendet werden.) | ESR-Anforderung example.version.1.1.xml |
| ESR-Anforderungsbeispiel (CZ) | Beispiel einer ESR-Anforderung für die Tschechische Republik | Format für eine Beispiel-XML-Anforderung an den steuerlichen Dienst der EFSTA in der Tschechischen Republik | ESR-Anforderungsbeispiel (CZ).version.1.1.1.xml |
| ESR-Antwortbeispiel | Beispiel einer ESR-Antwort | Grundformat für eine Beispiel-XML-Antwort an den steuerlichen Dienst der EFSTA (Dieses Format kann in Österreich verwendet werden.) | ESR-Antwort example.version.1.1.xml |
| ESR-Antwortbeispiel (CZ) | Beispiel einer ESR-Antwort für die Tschechische Republik | Format für eine Beispiel-XML-Antwort an den steuerlichen Dienst der EFSTA in der Tschechischen Republik | ESR-Antwortbeispiel (CZ).version.1.1.1.xml |

## <a name="setup"></a>Einrichten

### <a name="cash-registers"></a>Kassen

Jede Kasse muss so eingerichtet werden, dass sie mit dem steuerlichen Dienst kommuniziert. Sie können Kassen auf der Seite **Kassen** (**Debitoren** &gt; **Setup** &gt; **Kassen** &gt; **Kassen**) einrichten. In der folgenden Tabelle werden weitere Informationen über die Einrichtung beschrieben, die erforderlich ist.

<table>
<thead>
<tr>
<th>Einrichten</th>
<th>Details</th>
<th>Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr>
<td>Kasseneinstellungen</td>
<td>Geben Sie die URL der Kasse, den Namen der Instanz von Microsoft Azure Key Vault und den Klassennamen an.</td>
<td><ul>
<li><strong>Kassen-URL</strong> – Geben Sie die URL des steuerlichen Diensts ein.
<p><strong>Warnung:</strong> Drittanbieterdienste oder andere Dienste, die Sie hier konfigurieren, benötigen keine Zertifizierung, und sie erfüllen möglicherweise nicht die Datenschutzstandards von Microsoft. Sie sollten die Datenschutzdokumentation jedes Diensts überprüfen und mit jedem Dienstanbieter zusammenarbeiten, um mehr über die Konformitätsstufe zu erfahren, die jeder Dienst bietet. Sie sind dafür verantwortlich, sicherzustellen, dass diese Dienste ihre sicherheitsbezogenen, datenschutzbezogenen und gesetzlichen Standards erfüllen. Sie tragen das Risiko der Verwendung dieser Dienste. Microsoft gewährt keine ausdrücklichen Gewährleistungen, Garantien oder Bedingungen. Es wird dringend empfohlen, dass Sie nur Diensten verwenden, die sichere und autorisierte Verbindungen verwenden (das heißt, Dienste, die das HTTPS-Protokoll verwenden).</p>
</li>
<li><strong>Key Vault-Name</strong> – Wenn auf den steuerlichen Dienst über eine sichere Verbindung zugegriffen werden kann (dass heißt, die URL beginnt mit https://), sollten Sie Zertifikate einrichten und sie korrekt auf beiden Seiten speichern (bei der Finance-App und beim steuerlichen Dienst des Drittanbieters). In diesem Feld wählen Sie den Namen der Azure Key Vault-Instanz aus, in der das Finance-Zertifikat gespeichert ist. Weitere Informationen finden Sie unter <a href="https://support.microsoft.com/help/4040305/setting-up-a-key-vault-client">Einen Azure Key Vault-Client einrichten</a>.</li>
<li><strong>Klassenname</strong> – Wählen Sie die Klasse aus, in der Eigenschaften der Integration mit dem steuerlichen Dienst implementiert werden. Die verfügbare Klasse ist <strong>CashRegisterProcessingEFSTA_W</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>Varianten</td>
<td>Wählen Sie für jede Kasse die EB-Formate aus, die verwendet werden müssen, um Belege auszudrucken, Anforderungen an den steuerlichen Dienst zu senden und Antworten vom steuerlichen Dienst zu empfangen. Die EB-Formate, die Sie auswählen, müssen für die primäre Adresse der juristischen Person geeignet sein.</td>
<td>Für das Belegformat wählen Sie beispielsweise <strong>Barbelegformat (AT)</strong> für Österreich und <strong>Barbelegformat (CZ)</strong> für die Tschechische Republik aus.

Wenn Sie kein Format in der Liste finden, können Sie aktuelle elektronische Formate von LCS herunterladen. Weitere Informationen finden Sie unter <a href="https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs">Elektronische Berichtskonfigurationen aus Lifecycle Service herunterladen</a>.</td>
</tr>
<tr>
<td>Kassenzertifikatseinstellungen</td>
<td>Aktivieren Sie die Verwendung selbstsignierter Zertifikate.</td>
<td>
<ul>
<li><strong>Verwenden eines selbstsignierten Zertifikats</strong> – Legen Sie diese Option auf <strong>Ja</strong> fest, wenn Sie ein selbstgeneriertes, selbstsigniertes Zertifikat verwenden, das sie nicht der Liste vertrauenswürdiger Zertifikate hinzufügen können.</li>
<li><strong>Kassenzertifikats-Fingerabdruck</strong> – Geben Sie den Fingerabdruck des selbst signierten Zertifikats ein, das in einem steuerlichen Dienst gespeichert ist und das verwendet wird, um das Zertifikat des steuerlichen Diensts zu überprüfen.</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="cash-register-locations"></a>Kassenstandorte

Sie können Standorte von Kassen auf der Seite **Kassenstandorte** (**Debitoren** &gt; **Setup** &gt; **Kassen** &gt; **Kassenstandorte**) einrichten.

#### <a name="prerequisites-for-the-czech-republic"></a>Voraussetzungen für die Tschechische Republik

Bevor Sie Kassenstandorte für eine juristische Person einrichten, deren primäre Adresse in der Tschechischen Republik liegt, müssen Sie diese Schritte befolgen.

1. Erstellen Sie einen Steuerregistrierungstyp für die Geschäftsraumkennung, indem Sie **Organisationsverwaltung** &gt; **Globales Adressbuch** &gt; **Registrierungstypen** &gt; **Registrierungstypen** auswählen.

    Dieser Registrierungstyp sollte auf **Organisation** eingeschränkt werden.

2. Ordnen Sie den Registrierungstyp der Registrierungskategorie **Geschäftsraumkennung** zu:

    1. Wählen Sie **Organisationsverwaltung** &gt; **Globales Adressbuch** &gt; **Registrierungstypen** &gt; **Registrierungskategorien** aus.
    2. Wählen Sie den Registrierungstyp aus, den Sie zuvor erstellt haben, und wählen Sie anschließend im Feld **Registrierungskategorie** die **Geschäftsraumkennung** aus.

3. Ordnen Sie die Geschäftsraumkennung der Organisationseinheitsadresse der Organisationseinheit zu, die für den Kassenstandort verwendet wird.

    1. Wählen Sie **Organisationsverwaltung** &gt; **Gemeinsam** &gt; **Organisationen** &gt; **Interne Organisationen** aus.
    2. Wählen Sie die Organisation aus, die der Geschäftsraumkennung zuzuordnen ist.
    3. Wählen Sie im Inforegister **Adressen** die Option **Weitere Optionen** &gt; **Erweitert** aus.
    4. Wählen Sie im Inforegister **Registrierungskennung** die Option **Hinzufügen** aus.
    5. Wählen Sie den Registrierungstyp aus, den Sie zuvor erstellt haben.
    6. Geben Sie die Registrierungsnummer ein.

### <a name="create-cash-register-terminals"></a>Kassenterminals erstellen

Sie können die Kassenterminals erstellen, die für den Standort verfügbar sind, und anschließend weisen Sie die Kasse dem Terminal hinzu, auf der Seite **Kassenterminals** (**Debitoren** &gt; **Setup** &gt; **Kassen** &gt; **Kassenterminals**).

### <a name="assign-the-user-to-a-person"></a>Den Benutzer einer Person zuweisen

Der Benutzer, der als Bargeldoperator fungiert und der Bargeldtransaktionen protokollieren darf, die in der Kasse registriert sind, muss einer Person zugewiesen sein. Sie können einen Benutzer einer Person zuweisen, indem Sie **Systemverwaltung** &gt; **Benutzer** auswählen.

### <a name="set-up-cash-register-operators"></a>Kassenbediener einrichten

Sie können Kassenoperatoren einrichten, diese dem Kassenstandort zuweisen, und ein Standardterminal zuweisen, indem Sie **Debitoren** &gt; **Setup** &gt; **Kasse** &gt; **Kassenoperatoren** auswählen.

### <a name="set-up-methods-of-payment-that-require-fiscal-registration"></a>Zahlungsmethoden einrichten, für die eine steuerliche Registrierung erforderlich ist

Sie können Zahlungsmethoden einrichten, die in einer Kasse registriert werden müssen. Wählen Sie **Debitoren** &gt; **Setup** &gt; **Kassen** &gt; **Kassenzahlungsmethoden** aus, und legen Sie dann die folgenden Felder fest.

| Feld | Beschreibung |
|---|---|
| Zahlungsmethode | Wählen Sie eine Zahlungsmethode aus, die in der Kasse registriert werden muss und dem steuerlichen Dienst gesendet werden muss. |
| Kassensteuerbetrag | Aktivieren Sie das Kontrollkästchen, um anzugeben, dass die Steuerbeträge, die dem Barzahlungsbetrag zugeordnet sind, im steuerlichen Dienst registriert werden müssen. |

#### <a name="important-notices"></a>Wichtige Hinweise

In den folgenden Szenarios können die Steuerbeträge, die dem Zahlungsbetrag zugeordnet sind, zuverlässig anhand der gebuchten Transaktionen identifiziert werden:

- Für die Barzahlung, die automatisch gebucht wird, wenn eine Rechnung für Zahlung bei Lieferung (Zahlungsbedingungen für Zahlung bei Lieferung) gebucht wird. In diesem Fall sind Steuerbeträge, die übermittelt werden, gleich den Steuerbeträgen, die durch eine Rechnungsbuchung erzeugt werden.
- Für die Bargeldvorauszahlung, die manuell aus der Debitorenzahlungserfassung gebucht wird, wenn Mehrwertsteuerbeträge aus der Zahlungserfassung berechnet und gebucht werden. (Steuerbeträge, die aus einer Vorauszahlung gebucht werden, werden immer gesendet, unabhängig von der Einstellung des Kontrollkästchens **Steuerbetrag registrieren**.)

Sie sollten sich bei der lokalen Steuerbehörden erkundigen, um die Anforderungen für die Registrierung von Steuerbeträgen zu identifizieren, die einer Barzahlung in der Kasse zugeordnet sind. Sie sollten Zahlungsmethoden bei Bedarf auch aufteilen.

In den folgenden Szenarios können die Steuerbeträge, die dem Zahlungsbetrag zugeordnet sind, nicht zuverlässig anhand der gebuchten Transaktionen identifiziert werden:

- Für die Barzahlung, die manuell aus der Debitorenzahlungserfassung gebucht wird und gegenüber der zuvor gebuchten Rechnung beglichen wird, die einen gebuchten Steuerbetrag enthält.

Wenn die Kassenzahlungsmethode konfiguriert wird, um Steuerbeträge zu erfassen, berechnet eine bestimmte Betragverteilungslogik ungefähre Steuerbeträge, basierend auf dem Zahlungsbetrag in diesem Szenario.

In diesen Szenarien werden die korrekten Steuerbeträge nur in der gebuchten Rechnung dargestellt, die beglichen ist. Erkundigen Sie sich bei der lokalen Steuerbehörden, um die korrekte Methode zum Übermitteln der fakturierten Steuerbeträge für Steuerbehördenüberprüfungen für diese Szenarien zu identifizieren.

### <a name="create-terms-of-payment-for-a-cod-scenario"></a>Erstellen von Zahlungsbedingungen für ein Szenario mit Zahlung bei Lieferung

Wenn eine Barzahlung empfangen werden kann, wenn eine Rechnung gebucht wird, können Sie Zahlungsbedingungen erstellen, die die Zahlungsmethode **Zahlung bei Lieferung** haben. Wählen Sie **Debitoren** &gt; **Zahlung** &gt; **Zahlungsbedingungen** aus, und legen Sie dann die folgenden Felder fest.

| Feld | Beschreibung |
|---|---|
| Zahlungsart | Wählen Sie **Zahlung bei Lieferung** aus. |
| Barzahlung | Legen Sie die Option auf **Ja** fest, um eine automatische Zahlungstransaktion zu erstellen. |
| Bargeld | Wählen Sie das Hauptbuchkonto aus, das verwendet wird, um Barzahlungen zu buchen, die automatisch generiert werden. |

## <a name="example"></a>Beispiel

In diesem Abschnitt werden Sie Schritt für Schritt durch die folgenden Geschäftsprozesse geführt, und es wird der steuerliche Dienst [EFSTA Fiscal Register (EFR)](https://public.efsta.net/efr/) als Beispiel verwendet:

- Nachdem Sie eine Barzahlung buchen, für die die Registrierung ansteht, wird eine Kassentransaktion erstellt, die zu signierende Daten hat. Diese Transaktion wird dann im angegebenen XML-Format an den steuerlichen Dienst zur Registrierung übermittelt.
- Sie empfangen eine Antwort vom steuerlichen Dienst. Diese Antwort hat eine Signatur und Steuercodes, die der steuerliche Dienst gemäß landes-/regionenspezifischer Regeln generiert. Diese Antwort wird in einer steuerlichen Kassentransaktion gespeichert.
- Der Barbeleg wird gedruckt. Dieser Beleg umfasst die Buchungsdaten, Signaturen und Steuercodes.

### <a name="register-an-automatically-posted-cod-payment-for-a-free-text-invoice-and-print-a-cash-receipt"></a>Registrieren einer automatisch gebuchten Zahlung bei Lieferung für eine Freitextrechnung und Drucken eines Barbelegs

1. Wählen Sie **Debitoren** &gt; **Freitextrechnungen** &gt; **Alle Freitextrechnungen** aus.
2. Dient zum Erstellen einer Freitextrechnung. Weitere Informationen finden Sie unter [Erstellen von Freitextrechnungen](../accounts-receivable/create-free-text-invoice-new.md). 
3. Wählen Sie im Inforegister **Zahlung** eine Zahlungsmethode aus, die als Zahlungsmethode für die Kasse eingerichtet ist.
4. Wählen Sie Zahlungsbedingungen aus, die für die Zahlung bei Lieferung eingerichtet sind.
5. Wählen Sie **Buchen** aus.
6. Folgen Sie im Dialogfeld **Freitextrechnung buchen** diesen Schritten:

    1. Aktivieren Sie im Inforegister **Parameter** das Kontrollkästchen **Beleg drucken**, damit ein Barbeleg gedruckt wird, nachdem die Rechnung gebucht wurde.
    2. Überprüfen Sie im Inforegister **Kasse** den Standort, das Terminal, die Kasse und die Operatorcodes. Der Terminalcode wird automatisch aus dem Feld **Standardkassenterminal** auf der Seite **Kassenoperatoren** eingegeben. Ändern Sie den Terminalcode nur, wenn die Barzahlung an einem anderen Kassenterminal empfangen wurde, die für den aktuellen Operator verfügbar ist.
    3. Wählen Sie **OK**.

7. Überprüfen Sie den Barbeleg, der für die gebuchte Rechnung generiert ist. Standardmäßig ist der generierte Barbeleg als Datei verfügbar. Informationen dazu, wie andere Ziele eingerichtet werden, die Sie für Barbelege verwenden können, finden Sie unter [Ziele für die elektronische Berichterstellung](../../dev-itpro/analytics/electronic-reporting-destinations.md).


### <a name="register-an-automatically-posted-cod-payment-for-a-sales-order-invoice-and-print-a-cash-receipt"></a>Registrieren einer automatisch gebuchten Zahlung bei Lieferung für eine Auftragsrechnung und Drucken eines Barbelegs

1. Wählen Sie **Debitoren** &gt; **Aufträge** &gt; **Alle Aufträge** aus.
2. Erstellen Sie einen Auftrag. Weitere Informationen finden Sie unter [Aufträge erstellen](../../supply-chain/sales-marketing/tasks/create-sales-orders.md).
3. Wählen Sie im Inforegister **Preis und Rabatt** eine Zahlungsmethode aus, die als Zahlungsmethode für die Kasse eingerichtet ist.
4. Wählen Sie im Feld **Zahlung** die Zahlungsbedingungen aus, die für Zahlung bei Lieferung eingerichtet sind.
5. Wählen Sie **Rechnung** &gt; **Rechnung** aus.
6. Legen Sie im Inforegister **Parameter** die Option **Beleg drucken** auf **Ja** fest, damit ein Barbeleg gedruckt wird, nachdem die Rechnung gebucht wurde.
7. Überprüfen Sie im Inforegister **Kasse** den Standort, das Terminal, die Kasse und die Operatorcodes. Ändern Sie die Informationen nach Bedarf. Der Terminalcode wird automatisch aus dem Feld **Standardkassenterminal** auf der Seite **Kassenoperatoren** eingegeben. Ändern Sie den Terminalcode nur, wenn die Barzahlung an einem anderen Kassenterminal empfangen wurde, die für den aktuellen Operator verfügbar ist.

### <a name="register-a-customer-payment-from-the-customer-payment-journal-and-print-a-cash-receipt"></a>Registrieren einer Debitorenzahlung aus der Debitorenzahlungserfassung und Drucken eines Barbelegs

1. Wählen Sie **Debitoren** &gt; **Erfassungen** &gt; **Zahlungen** &gt; **Zahlungserfassung** aus, um die Debitorenzahlungserfassung zu öffnen. (Alternativ wählen Sie **Hauptbuch** &gt; **Erfassungen** &gt; **Allgemeine Erfassung** aus, um die allgemeine Erfassung zu öffnen.)
2. Erstellen Sie die Erfassungspositionen, die eine Debitorenbarzahlung haben.
3. Wählen Sie auf der Registerkarte **Zahlung** eine Zahlungsmethode aus, die als Zahlungsmethode für die Kasse eingerichtet ist.
4. Aktivieren Sie das Kontrollkästchen **Erfassungsbeleg für Vorauszahlung**, wenn die Zahlung eine Vorauszahlung ist.
5. Überprüfen Sie auf der Registerkarte **Zahlung** den Standort, das Terminal, die Kasse und die Operatorcodes. Ändern Sie die Informationen nach Bedarf. Der Terminalcode wird automatisch aus dem Feld **Standardkassenterminal** auf der Seite **Kassenoperatoren** eingegeben. Ändern Sie den Terminalcode nur, wenn die Barzahlung an einem anderen Kassenterminal empfangen wurde, die für den aktuellen Operator verfügbar ist.
6. Wählen Sie **Buchen** &gt; **Buchen** aus.
7. Wählen Sie **Drucken** &gt; **Barbeleg** aus, um einen Beleg zu drucken, der Steuercodes enthält.

### <a name="register-a-customer-payment-from-the-slip-journal-and-print-a-cash-order-that-includes-cash-receipt-information-czech-republic-only"></a>Registrieren einer Debitorenzahlung aus der Belegerfassung und Drucken eines Barauftrags, der Barbeleginformationen enthält (nur Tschechische Republik)

1. Wählen Sie **Bargeld- und Bankverwaltung** &gt; **Erfassungen** &gt; **Belegerfassung** aus.
2. Erstellen Sie die Erfassungspositionen, die eine Debitorenbarzahlung haben.
3. Überprüfen Sie auf der Registerkarte **Zahlung** die Felder im Abschnitt **Kasse**. Der Terminalcode wird automatisch aus dem Feld **Standardkassenterminal** auf der Seite **Kassenoperatoren** eingegeben. Ändern Sie den Terminalcode nur, wenn die Barzahlung an einem anderen Kassenterminal empfangen wurde. 
4. Wählen Sie **Dokumentgenehmigung** &gt; **Genehmigen** aus. Die Barauftragsnummer, die der Zahlung zugewiesen ist.
5. Wählen Sie **Buchen** &gt; **Buchen** aus.
6. Wählen Sie **Drucken** &gt; **Barauftrag** aus, um einen Barauftrag zu drucken, der Steuercodes enthält.

### <a name="cancel-a-payment"></a>Zahlung stornieren

Wenn eine Barbelegnummer für eine Zahlung in der Kasse registriert wurde und Sie dann die Zahlung stornieren, wird eine neue Barbelegnummer in derselben Kasse erfasst. Der Zahlungsstornierungsbarbeleg enthält genau dieselben Mengen wie der ursprüngliche Beleg, aber die Beträge haben ein negatives Vorzeichen.

1. Öffnen Sie die Seite **Kundentransaktionen**:

    1. Wählen Sie **Debitoren** &gt; **Kunden** &gt; **Alle Kunden** aus.
    2. Wählen Sie einen Debitor aus.
    3. Wählen Sie im Aktivitätsbereich **Kunde** &gt; **Transaktionen** aus.

2. Wählen Sie die zu stornierende Zahlungstransaktion.
3. Wählen Sie **Stornieren** &gt; **Zahlung stornieren** aus.
3. Geben Sie die erforderlichen Informationen ein, und wählen Sie dann **OK** aus, um die Zahlungsstornierungstransaktion zu erstellen und zur Seite **Kundentransaktionen** zurückzukehren.
4. Wählen Sie die neue Zahlungsstornierungstransaktion aus, und wählen Sie anschließend **Drucken** &gt; **Barbeleg** aus, um einen Barbeleg zu drucken, der Steuercodes enthält.

### <a name="review-cash-register-fiscal-transactions-and-resend-a-transaction-to-the-cash-register"></a>Überprüfen Sie die Kassensteuerbuchungen und übermitteln Sie erneut eine Buchung an die Kasse

Sie können die Barzahlungen überprüfen, die registriert wurden, und Sie können auch das Barbelegoriginal oder eine Kopie des Barbelegs erneut drucken, indem Sie **Drucken** unter **Debitoren** &gt; **Anfragen** &gt; **Kassensteuerbuchungen** auswählen.

Das Gesetz beschreibt Ausnahmeszenarien, die der steuerliche Dienst richtig handhaben soll. Wenn eine Barzahlung aus irgendeinem Grund, der nicht mit einem dieser Ausnahmeszenarien zusammenhängt, nicht erfolgreich registriert wurde, wird eine Fehlermeldung angezeigt, nachdem Sie eine Barzahlung buchen. Die Kassentransaktion, die den Status **Erstellt** hat, wird auf der Seite **Steuerbezogene Kassenbuchungen** verfügbar sein. Sie müssen die Probleme beheben und die Bartransaktionen, die für die Kasse erstellt werden, manuell erneut senden. Andernfalls kann ein Barbeleg nicht gedruckt werden, der Steuercodes enthält. Wenn eine Barzahlung ordnungsgemäß registriert ist, hat sie den Status **Registriert**.

In der folgenden Tabelle werden die Felder für Kassenzahlungsbuchungen beschrieben.

<table>
<thead>
<tr>
<th>Feld</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr>
<td>Kasse</td>
<td>Die Kennung der Kasse.</td>
</tr>
<tr>
<td>Buchungskennung</td>
<td>Die Kennung der Transaktion in der Kasse. Dieser Wert wird aus dem steuerlichen Dienst empfangen.</td>
</tr>
<tr>
<td>Kassen-URL</td>
<td>Die URL des Ortes, in dem sich der steuerliche Dienst befindet.</td>
</tr>
<tr>
<td>Status</td>
<td>Der Status der Buchung. Folgende Werte werden verwendet:
<ul>
<li><strong>Erstellt</strong> – Die Zahlungstransaktion ist gebucht, aber nicht registriert worden.</li>
<li><strong>Registriert</strong> – Die Zahlungstransaktion ist gebucht und registriert worden. (Somit haben Sie die Zahlungstransaktion an den steuerlichen Dienst übermittelt, und Sie haben eine Antwort empfangen, die Steuercodes enthält.)</li>
</ul></td>
</tr>
<tr>
<td>(CZ/Tschechische Republik) Offline</td>
<td>Ein Indikator, dass die Bartransaktion offline registriert wurde (zugelassene Ausnahme) und ein PKP (Unterzeichnungscode) empfangen wurde.</td>
</tr>
<tr>
<td>Terminal</td>
<td>Der Code des Kassenterminals.</td>
</tr>
<tr>
<td>Operator</td>
<td>Der Code des Kassenoperators.</td>
</tr>
<tr>
<td>Beleg</td>
<td>Die Belegnummer der gebuchten Bartransaktion.</td>
</tr>
<tr>
<td>Termin</td>
<td>Das Datum der Buchung.</td>
</tr>
<tr>
<td>Belegsnummer</td>
<td>Die Nummer des Barbelegs.</td>
</tr>
<tr>
<td>Datum und Uhrzeit der Buchung</td>
<td>Datum und Uhrzeit der registrierten Transaktion. Dieser Wert wird aus dem steuerlichen Dienst empfangen.</td>
</tr>
<tr>
<td>Belegsbetrag</td>
<td>Der Zahlungsbetrag.</td>
</tr>
<tr>
<td>Währung</td>
<td>Die Währung der Zahlung.</td>
</tr>
<tr>
<td>Name</td>
<td>Der Name des Steuercodes, der vom steuerlichen Dienst empfangen ist. Folgende Werte können verwendet werden:
<ul>
<li><strong>Info</strong> – Zusätzliche Informationen</li>
<li>(AT/Österreich) <strong>Code</strong> – Signatur</li>
<li>(AT/Österreich) <strong>Link</strong> – Link, der von Signatur abhängt</li>
</ul>
</td>
</tr>
<tr>
<td>Beschriftung</td>
<td>Die Bezeichnung des Steuercodes, der vom steuerlichen Dienst empfangen ist. Folgende Werte können verwendet werden:
<ul>
<li>(CZ/Tschechische Republik) <strong>FIK</strong> – Steuerlicher Kennungscode</li>
<li>(CZ/Tschechische Republik) <strong>BKP</strong> – Sicherheitscode</li>
<li>(CZ/Tschechische Republik) <strong>PKP</strong> – Unterzeichnungscode (Dieser Code wird im Fall einer Offlineregistrierung zurückgegeben.)</li>
</ul>
</td>
</tr>
<tr>
<td>Wert</td>
<td>Der Wert des Steuercodes, der vom steuerlichen Dienst empfangen ist.</td>
</tr>
<tr>
<td>Wert</td>
<td>Der Prozentsatz der registrierten Steuer.</td>
</tr>
<tr>
<td>Mehrwertsteuerbetrag</td>
<td>Der Betrag der registrierten Steuer.</td>
</tr>
<tr>
<td>Bruttobetrag</td>
<td>Der Betrag der registrierten Zahlung.</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]