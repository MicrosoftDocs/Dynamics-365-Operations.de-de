<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="work-with-store-inventory.md" target-language="de-DE">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>work-with-store-inventory.418f90.551a8408aa730bc1916f1c57b7cfd773966ce8bf.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>551a8408aa730bc1916f1c57b7cfd773966ce8bf</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\work-with-store-inventory.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Store inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bestandsverwaltung im Laden</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the types of documents that you can use to manage inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dieser Artikel beschreibt die Dokumentarten, die Sie zum Verwalten des Bestands verwenden können.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Store inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bestandsverwaltung im Laden</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>When working with inventory in Dynamics 365 for Retail and using the POS application, it is important to note that POS provides limited support for inventory dimensions and certain inventory item types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bei der Arbeit mit dem Bestand in Dynamics 365 for Retail und der Verwendung der POS-Anwendung ist zu beachten, dass der POS nur begrenzte Unterstützung für Bestandsdimensionen und bestimmte Bestandsartikelarten bietet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The POS solution does not support the following item configurations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die POS-Lösung unterstützt die folgenden Artikelkonfigurationen nicht:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>BOM items (except kit products, which utilize some components of the BOM framework)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stücklistenpositionen (außer Kitprodukten, die einige Komponenten des Stücklistenrahmens verwenden)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Catch weight items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Artikelgewichtsartikel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Batch-controlled items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Chargengesteuerte Artikel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The POS application currently does not support the following tracking dimensions in the POS:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die POS-Anwendung unterstützt derzeit die folgenden Tracking-Dimensionen am POS nicht:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Batch tracking dimension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dimension der Chargenverfolgung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Owner dimension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eigentümerdimension</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The POS solution provides limited support for the following dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die POS-Lösung bietet begrenzte Unterstützung für die folgenden Dimensionen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Limited support indicates that the POS may default some of these dimensions into inventory transactions automatically based on warehouse/store setup configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eingeschränkte Unterstützung deutet darauf hin, dass der POS einige dieser Dimensionen automatisch in Bestandstransaktionen einbinden kann, basierend auf der Konfiguration von Lager/Geschäft.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>POS will not fully support the dimensions in the way they are supported if a sales transaction is manually entered into the ERP.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">POS unterstützt die Dimensionen nicht vollständig in der Art und Weise, wie sie unterstützt werden, wenn ein Verkaufsvorgang manuell in das ERP eingegeben wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>Warehouse Location<ept id="p1">**</ept> – Users will not have the ability to manage the receiving warehouse location for items received into a store warehouse when the store has not been configured to use the warehouse management process.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Lagerortstandort<ept id="p1">**</ept> – Benutzer können den Standort des empfangenden Lagerorts für Artikel nicht verwalten, die für einen Filiallagerort eingehen, wenn die Filiale nicht so konfiguriert wurde, dass der Lagerortverwaltungsprozess verwendet wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>A default receiving location defined on the store warehouse will be used for these items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ein Standardstandort für den Empfang, der im Filiallagerort definiert wird, wird für diese Artikel verwendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>If the warehouse management process has been enabled for the store, limited support that prompts the user to choose a receiving location for the entire receipt will be triggered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn der Lagerortverwaltungsprozess für die Filiale aktiviert wurde, wird begrenzter Unterstützung ausgelöst, der den Benutzer auffordert, einen Empfangsstandort für den gesamten Eingang auswählen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Items sold from the store will always be sold out of the default retail location as defined on the store warehouse setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Artikel, die von der Filiale verkauft werden, werden immer aus dem Standardeinzelhandelsstandort verkauft, wie bei der Einrichtung des Filiallagerorts definiert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The location for managing return inventory can be controlled through default return location definition on the store warehouse or based on return reason codes as defined in the return location policy.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Der Standort zum Verwalten des Rückholbestands kann nach über die Definition des Standardrücklieferungsstandort im Filiallagerort oder auf Grundlage von den in der Rückholstandortrichtlinie definierten Rückholursachencodes gesteuert werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>License plate<ept id="p1">**</ept> – License plates are only applicable when <bpt id="p2">**</bpt>Use warehouse management process<ept id="p2">**</ept> has been enabled on the item and the store warehouse.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Ladungsträger<ept id="p1">**</ept> – Ladungsträger gelten nur, wenn <bpt id="p2">**</bpt>Prozess der Lagerverwaltung verwenden<ept id="p2">**</ept> für den Artikel und den Filiallagerort aktiviert wurde.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>In POS, if inventory is received into a store warehouse where the warehouse management process has been enabled, and the location chosen to receive the item into is tied to a location profile that requires license plate control, the POS application will systematically apply a license plate to the receiving line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Im POS: wenn Bestand in einen Filiallagerort eingeht, in dem der Lagerortverwaltungsprozess aktiviert wurde, und der Standort, der für den Empfang der Artikel ausgewählt wurde, mit einen Lagerplatzprofil verknüpft ist, für das Kennzeichensteuerung erforderlich, wendet die POS-Anwendung systematisch ein Kennzeichen für die empfangende Position an.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Users in POS will not have the ability to change or manage this license plate data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Benutzer im POS können diese Kennzeichendaten nicht ändern oder verwalten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>If full management of license plates is required, it is suggested the store use the WMS mobile application or the back office ERP client to manage the receipt of these items.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Wenn die vollständige Verwaltung von Kennzeichen erforderlich ist, sollte die Filiale die mobile WMS-Anwendung oder den Backoffice-ERP-Client verwenden, um den Eingang dieser Artikel zu verwalten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Serial number<ept id="p1">**</ept> – The POS application has limited support for single serial number to be registered on a transaction sales line for orders created in POS with serialized items.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Seriennummer<ept id="p1">**</ept> – Die POS-Anwendung hat begrenzte Unterstützung für die Registrierung einzelner Seriennummern in einer Transaktionsverkaufsposition für Aufträge, die in POS mit serialisierten Artikeln erstellt werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>This serial number is not validated against registered serial numbers already in inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Seriennummer wird nicht gegen registrierte Seriennummern geprüft, die bereits im Bestand sind.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>If a sales order is created in the call center channel or fulfilled through the ERP and multiple serial numbers are registered to a single sales line during the fulfillment process in the ERP, these serial numbers will not be able to be applied or validated if a return is processed in POS for these orders.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Wenn ein Auftrag in Callcenterkanal erstellt oder durch das ERP erfüllt wird und während des Erfüllungsprozesses im ERP mehrere Seriennummern für eine einzelne Auftragsverkaufsposition erfasst werden, können diese Seriennummern nicht angewendet oder geprüft werden, wenn eine Rücklieferung im POS für diese Aufträge verarbeitet wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">**</bpt>Inventory status<ept id="p1">**</ept> – For items that use the warehouse management process and require an inventory status, this status field is not able to be set or modified through the POS application.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Bestandstatus<ept id="p1">**</ept> – Für Artikel, die den Lagerortverwaltungsprozess verwenden und einen Bestandsstatus benötigen, kann dieses Statusfeld nicht durch die POS-Anwendung festgelegt oder geändert werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The default inventory status as defined on the store warehouse configuration will be used when items are received into inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der wie in der Filiallagerortkonfiguration definierte Standardbestandsstatus wird verwendet, wenn Artikel im Bestand entgegengenommen werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>All organizations must test item configurations through POS in development or test environments before deploying them to production.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Alle Unternehmen müssen Artikelkonfigurationen über den POS in Entwicklungs- oder Testumgebungen testen, bevor sie in der Produktion eingesetzt werden können.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Test your items by performing regular cash and carry sales transacting and creating customer orders (if applicable) through the POS with your items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Testen Sie Ihre Artikel, indem Sie regelmäßige Cash and Carry-Verkaufstransaktionen durchführen und Kundenaufträge (falls vorhanden) über die POS mit Ihren Artikeln erstellen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Testing must include running a full statement posting processes in your test environment and verifying that there are no issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Das Testen muss die Durchführung eines vollständigen Buchungsprozesses in Ihrer Testumgebung und die Überprüfung, ob es keine Probleme gibt, beinhalten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Configuring items in a way that is not supported by the POS application, without proper testing, can result in your statement posting process failing in production without an easy way to correct the issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn Sie Artikel ohne ordnungsgemäße Tests so konfigurieren, dass sie nicht von der POS-Anwendung unterstützt werden, kann dies dazu führen, dass Ihr Prozess der Rechnungsbuchung in der Produktion fehlschlägt, ohne dass Sie die Probleme einfach beheben können.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Partner or customer customizations to the application may optionally be considered to allow these posting processes to successfully complete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Partner- oder Kundenanpassungen an die Anwendung können optional in Betracht gezogen werden, damit diese Buchungsprozesse erfolgreich abgeschlossen werden können.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>If customizations are not needed, the organization must ensure that the product configuration of your products has been done in a way that is supported by the standard POS application/order creation/statement posting process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn keine Anpassungen erforderlich sind, muss das Unternehmen sicherstellen, dass die Produktkonfiguration Ihrer Produkte in einer Weise erfolgt ist, die vom Standard-POS-Anwendungs-/Auftragserstellungs-/Anlagenbuchungsprozess unterstützt wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Purchase orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bestellungen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Purchase orders are created at the head office.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bestellungen werden in der Zentrale erstellt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail through the <bpt id="p1">**</bpt>Picking/Receiving<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn ein Einzelhandelslagerort im Bestellkopf enthalten ist, kann der Auftrag im Shop mithilfe von Modern POS (MPOS) oder Cloud POS in Microsoft Dynamics 365 for Retail durch die Operation <bpt id="p1">**</bpt>Entnahme-/Empfangskennung<ept id="p1">**</ept> empfangen werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>After the quantities that are received at the store are entered in the <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> field in POS for the purchase order document, they can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nachdem die in der Filiale eingehenden Mengen im Feld <bpt id="p1">**</bpt>Aktuelle Lieferung<ept id="p1">**</ept> im POS für das Bestellungsdokument eingegeben wurden, können sie lokal gespeichert oder zugesagt werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Saving this data locally has no effect on in-stock inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Das lokale Speichern dieser Daten hat keine Auswirkungen auf den Lagerbestand.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Saving should be done only if the user is not ready to post the receipt to HQ and just needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Es sollte nur gespeichert werden, wenn der Benutzer nicht bereit ist, den Empfang in der Hauptniederlassung zu buchen und nur eine Möglichkeit benötigt, die zuvor eingegebenen <bpt id="p1">**</bpt>Aktuelle Lieferung<ept id="p1">**</ept>-Daten vorübergehend zu speichern.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>This saves the receive now data locally to the user's channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dies speichert die Daten der aktuellen Lieferung lokal auf der Kanaldatenbank des Benutzers.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>After the document is processed using the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option, the <bpt id="p2">**</bpt>Receive Now<ept id="p2">**</ept> data is sent to HQ and the purchase order receipt will be posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nachdem das Dokument mit der Option <bpt id="p1">**</bpt>Zusagen<ept id="p1">**</ept> verarbeitet wurde, werden die <bpt id="p2">**</bpt>Aktuelle Lieferung<ept id="p2">**</ept>-Daten an die Hauptniederlassung gesendet und der Bestellungszugang wird gebucht.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Transfer orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Umlagerungsaufträge</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>A transfer order can specify that a particular store is the location that items can be shipped from or the location the inventory will be received into.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mit einem Umlagerungsauftrag kann angegeben werden, dass eine bestimmte Filiale der Standort ist, von dem Artikel versendet werden können, oder der Standort, an dem der Bestand eingeht.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the POS user is the shipping warehouse for a transfer order, they will be able to enter <bpt id="p1">**</bpt>Ship Now<ept id="p1">**</ept> quantities from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn der POS-Benutzer der Versandlagerort für einen Umlagerungsauftrag ist, kann er <bpt id="p1">**</bpt>Jetzt liefern<ept id="p1">**</ept>-Mengen aus POS eingeben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The data entered by the shipping store can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Daten, die durch die Versandfiliale eingegeben werden, können lokal gespeichert oder zugesagt werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>When saved locally, no updates are made to the transfer order document in HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bei lokaler Speicherung werden keine Aktualisierungen des Umlagerungsauftragsdokuments in der Hauptniederlassung vorgenommen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Saving should be done only if the user is not ready to post the shipment to HQ and needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Ship Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Es sollte nur gespeichert werden, wenn der Benutzer nicht bereit ist, die Lieferung in der Hauptniederlassung zu buchen und eine Möglichkeit benötigt, die zuvor eingegebenen <bpt id="p1">**</bpt>Jetzt liefern<ept id="p1">**</ept>-Daten vorübergehend zu speichern.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>After the store is ready to confirm shipment, the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option should be selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nachdem die Filiale bereit ist, die Lieferung zu bestätigen, sollte die Option <bpt id="p1">**</bpt>Zusagen<ept id="p1">**</ept> ausgewählt werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>This posts the shipment of the transfer order in HQ so that the receiving warehouse will now be able to receive against it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dadurch wird die Lieferung der Umlagerungsauftrags in der Hauptniederlassung gebucht, sodass das empfangenden Lagerort nun für den Empfang bereit ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>If the POS user is the receiving warehouse for a transfer order, they will be able to enter the <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> quantities from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn der POS-Benutzer der Empfangslagerort für einen Umlagerungsauftrag ist, kann er <bpt id="p1">**</bpt>Aktuelle Lieferung<ept id="p1">**</ept>-Mengen aus POS eingeben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The data entered by the receiving store can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Daten, die durch die Empfangsfiliale eingegeben werden, können lokal gespeichert oder zugesagt werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Saving should be done only if the user is not ready to post the receipt to HQ and needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Es sollte nur gespeichert werden, wenn der Benutzer nicht bereit ist, den Empfang in der Hauptniederlassung zu buchen und eine Möglichkeit benötigt, die zuvor eingegebenen <bpt id="p1">**</bpt>Aktuelle Lieferung<ept id="p1">**</ept>-Daten vorübergehend zu speichern.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>This saves the receive now data locally to the user's channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dies speichert die Daten der aktuellen Lieferung lokal auf der Kanaldatenbank des Benutzers.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>After the document is processed using the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option, the <bpt id="p2">**</bpt>Receive Now<ept id="p2">**</ept> data is sent to HQ and the transfer order receipt will be posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nachdem das Dokument mit der Option <bpt id="p1">**</bpt>Zusagen<ept id="p1">**</ept> verarbeitet wurde, werden die <bpt id="p2">**</bpt>Aktuelle Lieferung<ept id="p2">**</ept>-Daten an die Hauptniederlassung gesendet und der Umlagerungsauftrag wird gebucht.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>It's important to note that the receiving store will be restricted to only being able to commit receive quantities that are equal to or less than shipped quantities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beachten Sie unbedingt, dass die empfangende Filiale darauf beschränkt wird, nur Eingangsmengen zuzusagen, die gleich oder kleiner der gelieferten Mengen sind.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>An attempt to receive quantities on a transfer order that have not previously shipped will result in errors and the receipt will not be confirmed in HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ein Versuch, Mengen für einen Umlagerungsauftrag zu empfangen, die zuvor nicht versendet wurden, ergibt Fehler und der Zugang wird in der Hauptniederlassung nicht bestätigt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Stock counts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bestandsmengen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Stock counts can be either scheduled or unscheduled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bestandsmengen können entweder geplant oder ungeplant sein.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Geplante Bestandszählungen werden in der Zentrale veranlasst, die die zu zählenden Artikel vorgibt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Von der Zentrale wird ein Inventurdokument erstellt, das im Shop empfangen werden kann und in dem die tatsächlich verfügbaren Mengen in MPOS oder Cloud POS eingegeben werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ungeplante Bestandsmengen werden in einem Shop initiiert, und die Mengen des tatsächlich verfügbaren Lagerbestands werden in MPOS oder Cloud POS aktualisiert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Im Gegensatz zu geplanten Bestandsmengen haben ungeplante Bestandsmengen keine vordefinierte Liste mit Artikeln.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>When a stock count of either type is completed, it is committed and sent to the head office.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn eine Bestandsmenge eines beliebigen Typs abgeschlossen wurde, wird sie kommissioniert und an die Zentrale gesendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>At the head office, the count is validated and posted as a separate step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In der Zentrale wird die Anzahl als getrennter Schritt geprüft und gebucht.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Inventory lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bestandsuche</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The current product quantity on hand for multiple stores and warehouses can be viewed on the <bpt id="p1">**</bpt>Inventory lookup<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die aktuelle Produktmenge für Mehrfachshops und Lagerorte kann auf der <bpt id="p1">**</bpt>Bestandssuchen<ept id="p1">**</ept>-Seite angezeigt werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Neben der aktuellen verfügbaren Menge können auch künftige Verfügbarkeitszusagen-Mengen (ATP) für jede einzelne Filiale angezeigt werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>To do so, select the store that you want to view the ATP for and then click <bpt id="p1">**</bpt>Show store availability<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Klicken Sie hierfür auf die Filiale, für die Sie die VfZ für anzeigen möchten, und klicken Sie auf <bpt id="p1">**</bpt>Verfügbarkeit in Filiale anzeigen<ept id="p1">**</ept>.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>