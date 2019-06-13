<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="orderexchanges.md" target-language="de-DE">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>orderexchanges.ba78aa.43571099727830e81c41416b6fe250dba398b3f8.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>43571099727830e81c41416b6fe250dba398b3f8</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\orderexchanges.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Configure and process an exchange on a return order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfigurieren und Verarbeiten eines Austausch für eine Rücklieferung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to configure an exchange on a return in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In diesem Thema wird erläutert, wie Sie einen Austausch für eine Rücklieferung im Microsoft Dynamics 365 for Retail konfigurieren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Configure and process an exchange on a return order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfigurieren und Verarbeiten eines Austausch für eine Rücklieferung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In previous versions of Microsoft Dynamics 365 for Retail, returns against customer orders were processed by using the return order document in Retail Headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In älteren Versionen von Microsoft Dynamics 365 for Retail werden Rücklieferungen für Kundenaufträge mithilfe des Rücklieferungsdokuments in Retail Headquarters verarbeitet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>However, the return order document can be used to process only products that are being returned.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Doch das Rücklieferungsdokument kann auch ausschließlich für die Bearbeitung von Produkten verwendet werden, die zurückgegeben werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The returned products are indicated by a negative quantity on the return order lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die zurückgelieferten Produkte werden durch eine negative Menge in den Rücklieferungspositionen angegeben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>By contrast, sales are indicated by a positive quantity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dagegen wird im Umsatz eine positive Menge angegeben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>However, the return order document doesn't support positive quantities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Das Rücklieferungsdokument unterstützt jedoch keine positiven Mengen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Because of this limitation, previous versions of Retail didn't support scenarios where product exchanges are done by using the return order document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aufgrund dieser Einschränkung wurden in früheren Versionen von Retail keine Szenarien unterstützt, in denen Produktumtauschaktivitäten mithilfe des Rücklieferungsdokuments durchgeführt wurden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>However, functionality has been added to support scenarios where exchanges are done on return orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Allerdings wurden Funktionen hinzugefügt, die Szenarien unterstützen, in denen der Umtausch mithilfe von Rücklieferungen erfolgt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Retail now uses the sales order document instead of the return order document to process these types of transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail verwendet nun das Auftragsdokument anstelle des Rücklieferungsdokuments, um die Transaktionsarten zu verarbeiten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Configure Retail to support exchanges on return orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfigurieren von Retail für die Unterstützung von Rücklieferungen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Follow these steps to configure the system to support exchanges on return orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gehen Sie folgendermaßen vor, um das System so zu konfigurieren, dass Umtausch mit Rücklieferungen unterstützt wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Headquarters setup <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Retail parameters<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gehen Sie zu <bpt id="p1">**</bpt>Einzelhandel <ph id="ph1">\&gt;</ph> Zentralverwaltungseinrichtung <ph id="ph2">\&gt;</ph> Parameter <ph id="ph3">\&gt;</ph> Retail-Parameter<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>On the <bpt id="p1">**</bpt>Customer orders<ept id="p1">**</ept> FastTab, set the <bpt id="p2">**</bpt>Process return orders as sales orders<ept id="p2">**</ept> option to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Legen Sie im Inforegister <bpt id="p1">**</bpt>Kundenaufträge<ept id="p1">**</ept> die Option <bpt id="p2">**</bpt>Rücklieferungen als Aufträge verarbeiten<ept id="p2">**</ept> auf <bpt id="p3">**</bpt>Ja<ept id="p3">**</ept> fest.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Run the <bpt id="p1">**</bpt>Global configuration distribution schedule<ept id="p1">**</ept> job (<bpt id="p2">**</bpt>1110<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Führen Sie den Auftrag <bpt id="p1">**</bpt>Globaler Konfigurationsverteilungszeitplan<ept id="p1">**</ept> (<bpt id="p2">**</bpt>1110<ept id="p2">**</ept>) aus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Make an exchange</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Durchführen eines Umtauschs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn das System wie im vorigen Abschnitt beschrieben konfiguriert ist, wählt der Verkaufsstellen (POS)-Benutzer immer noch einen Auftrag oder eine Verkaufsrechnung aus, um eine Rücklieferung zu verarbeiten. Dies hat sich seit den vorherigen Versionen von Retail nicht geändert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn jedoch die Rückgabeartikel in den Einkaufskorb gelegt wurden, kann der Benutzer dem Einkaufskorb neue Auftragspositionen hinzuzufügen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Für diese neuen Auftragspositionen muss der Benutzer alle Attribute definieren, die für die Verarbeitung von Kundenauftragsposition erforderlich sind.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>These attributes include the delivery method and fulfillment location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Diese Attribute enthalten die Lieferarten und den Erfüllungsstandort.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The payment that is due for the transaction will be a net of the return order lines and sales order lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Zahlung, die für die Transaktion fällig ist, ist der Nettobetrag der Rücklieferungspositionen und Auftragspositionen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>When payment is tendered for the transaction, the return order will be posted as a sales order document in Retail Headquarters, and the system will immediately invoice the return lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Erfolgt die Zahlung für die Transaktion, wird die Rücklieferung in Retail Headquarters als Auftragsdokument gebucht, und das System erstellt sofort eine Rechnung für die Rückgabepositionen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zur besseren Übersicht über die unterschiedlichen Mengen für den Einkaufskorb wurden dem Einkaufskorb drei neue Betragsfelder hinzugefügt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>You can use the screen designer to make these new fields available in the POS user interface (UI).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mithilfe des Bildschirmdesigners können Sie diese neuen Felder in der POS-Benutzeroberfläche (UI) bereitstellen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Deposit applied<ept id="p1">**</ept> – The deposit amount that is applied on a transaction when the user does a customer order pickup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Einzahlung angewendet<ept id="p1">**</ept> – Der Einzahlungsbetrag, der in einer Transaktion verwendet wird, wenn der Benutzer einen Kundenauftrag auswählt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn die Einzahlung nicht überschrieben wird und eine Einzahlung von 10 Prozent konfiguriert wurde, beläuft sich der Betrag in diesem Feld auf 90 Prozent des Gesamtbetrags des Kundenauftrags.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>Carry out amount<ept id="p1">**</ept> – The total amount for lines where the delivery mode was set to <bpt id="p2">**</bpt>Carry out<ept id="p2">**</ept> when the customer order was created or edited, or during a customer order exchange.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Betrag ausführen<ept id="p1">**</ept> – Der Gesamtbetrag für Positionen, in denen die Lieferart bei der Erstellung oder Bearbeitung des Kundenauftrags oder bei einem Umtausch eines Kundenauftrags auf <bpt id="p2">**</bpt>Ausführen<ept id="p2">**</ept> festgelegt wurde.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The amount in this field includes taxes and charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Betrag in diesem Feld enthält die Steuern und Belastungen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Return amount<ept id="p1">**</ept> – The total amount for lines that have negative quantities during the customer order exchange.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Rückgabebetrag<ept id="p1">**</ept> – Der Gesamtbetrag für Positionen, die negative Mengen für den Kundenauftragsumtausch haben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The amount in this field includes taxes and charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Betrag in diesem Feld enthält die Steuern und Belastungen.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>