<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="valid-checker.md" target-language="de-DE">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>valid-checker.125a66.1fc894206f9d90fce1e2eab292ac241e9d943e23.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1fc894206f9d90fce1e2eab292ac241e9d943e23</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\valid-checker.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konsistenzprüfung für Einzelhandelstransaktionen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the retail transaction consistency checker functionality in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In diesem Thema werden die Funktionen der Konsistenzprüfung für Einzelhandelstransaktionen in Microsoft Dynamics 365 for Retail beschrieben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konsistenzprüfung für Einzelhandelstransaktionen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In diesem Thema werden die in Version 8.1.3 von Microsoft Dynamics 365 for Finance and Operations eingeführten Funktionen der Konsistenzprüfung für Einzelhandelstransaktionen beschrieben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Die Konsistenzprüfung ermittelt und isoliert inkonsistente Transaktionen, bevor sie im Auszugsbuchungsprozess verarbeitet werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When a statement is posted in Microsoft Dynamics 365 for Retail, posting can fail due to inconsistent data in the retail transaction tables.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Wird ein Auszug in Microsoft Dynamics 365 for Retail gebucht, kann die Buchung aufgrund der inkonsistenten Daten in den Einzelhandelstransaktionstabellen fehlschlagen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The data issue may be caused by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Die Datenfehler können durch unvorhergesehene Probleme in der Verkaufsstellenanwendung oder durch Fehler beim Importieren von Buchungen aus POS-Systemen von Drittanbietern auftreten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Examples of how these inconsistencies may appear include:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Im Folgenden sind Beispiele für diese Inkonsistenzen aufgeführt:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The transaction total on the header table does not match the transaction total on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Transaktionsgesamtbetrag in der Kopftabelle entspricht nicht dem Transaktionsgesamtbetrag der Positionen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The line count on the header table does not match with the number of lines in the transaction table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Positionsanzahl in der Kopftabelle entspricht nicht der Anzahl von Positionen in der Transaktionstabelle.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Taxes on the header table do not match the tax amount on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Steuern in der Kopftabelle stimmen nicht mit dem Steuerbetrag in den Positionen überein.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn inkonsistente Transaktionen durch den Aufstellungsbuchungsprozess verarbeitet werden, werden inkonsistente Verkaufsrechnungen und Zahlungserfassungen erstellt, und der gesamte Aufstellungsbuchungsprozess schlägt anschließend fehl.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Das Wiederherstellen der Aufstellungen aus einem solchen Zustand umfasst komplexe Datenkorrekturen in mehreren Transaktionstabellen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The retail transaction consistency checker prevents such issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Konsistenzprüfung für Einzelhandelstransaktionen verhindert solche Probleme.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The following chart illustrates the posting process with the transaction consistency checker.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Das folgende Diagramm veranschaulicht den Buchungsprozess mit Transaktionskonsistenzprüfung.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">![</bpt>Statement posting process with retail transaction consistency checker<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>Statement posting process with retail transaction consistency checker<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>Aufstellungsbuchungsprozess mit der Konsistenzprüfung für Einzelhandelstransaktionen<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>Aufstellungsbuchungsprozess mit der Konsistenzprüfung für Einzelhandelstransaktionen<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The <bpt id="p1">**</bpt>Validate store transactions<ept id="p1">**</ept> batch process checks the consistency of the retail transaction tables for the following scenarios.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Der Stapelverarbeitungsvorgang <bpt id="p1">**</bpt>Geschäftsbuchungen überprüfen<ept id="p1">**</ept> prüft die Konsistenz der Einzelhandelstransaktionstabellen in folgenden Szenarien.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Customer account<ept id="p1">**</ept> – Validates that the customer account in the retail transaction tables exists in the HQ customer master.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Debitorenkonto<ept id="p1">**</ept>: Überprüft, dass das Debitorenkonto in den Einzelhandelstransaktionstabellen in den HQ-Debitorenmasterdaten vorhanden ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Line count<ept id="p1">**</ept> – Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Positionsanzahl<ept id="p1">**</ept>: Prüft, ob die Positionsanzahl, wie in der Tabelle in der Transaktionskopfzeile angegeben, mit der Anzahl der Positionen in den Verkaufstransaktionstabellen übereinstimmt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Price includes tax<ept id="p1">**</ept> – Validates that the <bpt id="p2">**</bpt>Price includes tax<ept id="p2">**</ept> parameter is consistent across transaction lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Preis enthält Steuern<ept id="p1">**</ept>: Prüft, ob der Parameter <bpt id="p2">**</bpt>Preis enthält Steuern<ept id="p2">**</ept> über alle Transaktionspositionen konsistent ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>Gross amount<ept id="p1">**</ept> – Validates that the gross amount on the header is the sum of the net amounts on the lines plus the tax amount.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Bruttobetrag<ept id="p1">**</ept>: Prüft, ob der Bruttobetrag in der Kopfzeile mit der Summe der Nettobeträge der Positionen zuzüglich des Steuerbetrags identisch ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Net amount<ept id="p1">**</ept> – Validates that the net amount on the header is the sum of the net amounts on the lines.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Nettobetrag<ept id="p1">**</ept>: Prüft, ob der Nettobetrag in der Kopfzeile mit der Summe der Nettobeträge der Positionen identisch ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Under / Over payment<ept id="p1">**</ept> – Validates that the difference between the gross amount on the header and the payment amount doesn't exceed the maximum underpayment/overpayment configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Unter-/Überzahlung<ept id="p1">**</ept>: Prüft, ob die Differenz zwischen dem Bruttobetrag in der Kopfzeile und dem Zahlungsbetrag nicht die maximale Unter- bzw. Überzahlungskonfiguration übersteigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Discount amount<ept id="p1">**</ept> – Validates that the discount amount on the discount tables and the discount amount on the retail transaction line tables are consistent, and that the discount amount on the header is the sum of the discount amounts on the lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Rabattbetrag<ept id="p1">**</ept>: Prüft, ob der Rabattbetrag in den Rabatttabellen und der Rabattbetrag in den Tabellen mit den Einzelhandelstransaktionspositionen konsistent ist, und ob der Rabattbetrag aus der Kopfzeile der Summe der Rabattbeträge in den Positionen entspricht.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Line discount<ept id="p1">**</ept> – Validates that the line discount on the transaction line is the sum of all the lines in the discount table that corresponds to the transaction line.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Positionsrabatt<ept id="p1">**</ept>: Prüft, ob der Positionsrabatt der Transaktionsposition der Summe aller Positionen in der Rabatttabelle entspricht, die sich auf die Transaktionsposition beziehen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Gift card item<ept id="p1">**</ept> – Retail doesn't support the return of gift card items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Geschenkkartenartikel<ept id="p1">**</ept>: Retail unterstützt nicht die Rückgabe von Geschenkkartenartikeln.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>However, the balance on a gift card can be cashed out. Any gift card item that is processed as a return line instead of a cash-out line fails the statement posting process.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Allerdings kann der Wert einer Geschenkkarte bar ausgezahlt werden. Bei allen Geschenkkartenartikeln, die anstelle einer Barauszahlungsposition als Rückgabeposition verarbeitet werden, schlägt der Auszugsbuchungsprozess fehl.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The validation process for gift card items helps guarantee that the only return gift card line items on the retail transaction tables are gift card cash-out lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bei der Validierung von Geschenkkartenartikeln wird sichergestellt, dass die einzigen Rückgabepositionsartikel der Geschenkkarte in den Einzelhandelstransaktionstabellen Barauszahlungspositionen sind.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>Negative price<ept id="p1">**</ept> – Validates that there are no negative price transaction lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Negativer Preis<ept id="p1">**</ept>: Überprüft, dass es keine Transaktionspositionen mit negativen Preisen gibt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Item &amp; Variant<ept id="p1">**</ept> – Validates that items and variants on the transaction lines exist in the item and variant master file.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Artikel und Variante<ept id="p1">**</ept>: Prüft, ob Artikel und Varianten aus den Transaktionspositionen in der Masterdatei mit Artikeln und Varianten vorhanden sind.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Set up the consistency checker</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Konsistenzprüfung einrichten</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Configure the "Validate store transactions" batch process, at <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> POS posting<ept id="p1">**</ept>, for periodic runs.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Konfigurieren Sie den Stapelverarbeitungsvorgang „Geschäftsbuchungen überprüfen“ unter <bpt id="p1">**</bpt>Einzelhandel <ph id="ph1">\&gt;</ph> IT für den Einzelhandel <ph id="ph2">\&gt;</ph> POS-Buchung<ept id="p1">**</ept>, sodass er regelmäßig ausgeführt wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Stapelverarbeitungsauftrag kann basierend auf der Shoporganisationshierarchie in ähnlicher Weise wie die Funktionen zum Berechnen und Buchen im Stapel geplant werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Es wird empfohlen, diesen Stapelverarbeitungsauftrag so zu konfigurieren, dass mehrmals am Tag ausgeführt wird, und ihn so zu planen, dass er am Ende jeder P-Auftragsausführung ausgeführt wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Results of validation process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ergebnisse des Überprüfungsprozesses</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The results of the validation check by the batch process are tagged on the appropriate retail transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Ergebnisse der Überprüfung durch den Stapelverarbeitungsauftrag werden in der entsprechenden Einzelhandelstransaktion markiert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The <bpt id="p1">**</bpt>Validation status<ept id="p1">**</ept> field on the retail transaction record is either set to <bpt id="p2">**</bpt>Successful<ept id="p2">**</ept> or <bpt id="p3">**</bpt>Error<ept id="p3">**</ept>, and the date of the last validation run appears on the <bpt id="p4">**</bpt>Last validation time<ept id="p4">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Das Feld <bpt id="p1">**</bpt>Überprüfungsstatus<ept id="p1">**</ept> im Einzelhandelstransaktionsdatensatz wird entweder auf <bpt id="p2">**</bpt>Erfolgreich<ept id="p2">**</ept> oder <bpt id="p3">**</bpt>Fehler<ept id="p3">**</ept> festgelegt und das Datum der letzten Prüfungsausführung wird im Feld <bpt id="p4">**</bpt>Uhrzeit der letzten Überprüfung<ept id="p4">**</ept> angezeigt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the <bpt id="p1">**</bpt>Validation errors<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Um eine ausführlichere Fehlerbeschreibung in Bezug auf einen Validierungsfehler zu erhalten, wählen Sie den entsprechenden Shoptransaktionsdatensatz aus und klicken auf die Schaltfläche <bpt id="p1">**</bpt>Überprüfungsfehler<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Transaktionen mit Überprüfungsfehlern und noch nicht validierte Transaktionen werden nicht in Aufstellungen einbezogen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Während des Prozesses „Auszug berechnen“ werden Benutzer darüber informiert, wenn Transaktionen vorliegen, die in die Aufstellung aufgenommen hätten werden können, wo dies jedoch nicht der Fall war.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>If a validation error is found, the only way to fix the error is to contact Microsoft Support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn ein Überprüfungsfehler gefunden wird, können Sie ihn nur beheben, indem Sie sich an den Microsoft Support wenden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In a future release, capability will be added so that users can fix the records that failed through the user interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In einer zukünftigen Version werden Funktionen hinzugefügt, mit denen Benutzer die Fehler, die in der Benutzeroberfläche erfolgten, in den Datensätzen selbst beheben können.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Logging and auditing capabilities will also be made available to trace the history of the modifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Es werden außerdem Protokollierungs- und Überwachungsfunktionen zur Nachverfolgung des Änderungsverlaufs bereitgestellt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Additional validation rules to support more scenarios will be added in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In zukünftigen Versionen werden zudem zusätzliche Validierungsregeln zur Unterstützung weiterer Szenarien hinzugefügt.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>