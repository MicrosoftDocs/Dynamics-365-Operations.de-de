<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="cost.md" target-language="de-DE">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>cost.4e88df.80e7a033467c3d94d55f06daa05f99bd27e19a29.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>80e7a033467c3d94d55f06daa05f99bd27e19a29</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\cost.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Cost configuration for distributed order management (DOM)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kostenkonfiguration für die verteilte Auftragsverwaltung (DOM)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes cost configuration for the distributed order management (DOM) functionality in Microsoft Dynamics 365 for Retail.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Dieses Thema behandelt die Kostenkonfiguration für die Funktion zur verteilten Auftragsverwaltung (DOM) in Microsoft Dynamics 365 for Retail.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Cost configuration for distributed order management (DOM)</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Kostenkonfiguration für die verteilte Auftragsverwaltung (DOM)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Um den optimalen Standort zur Erledigung von Aufträgen zu ermitteln, berücksichtigen Organisationen mehrere Kostenkomponenten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Some of these cost components are shipping cost, handling cost, and packaging cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dazu gehören unter anderem Kosten für Versand, Bearbeitung und Verpackung.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>A combination of these costs is calculated to determine the fulfillment location.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Anhand einer berechneten Kombination dieser Kosten wird der Erfüllungslagerplatz bestimmt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When the first iteration of distributed order management (DOM) in Microsoft Dynamics 365 for Retail optimized the assignment of orders to fulfillment locations, it factored in distance only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bei der Verbesserung der Zuweisung von Aufträgen zu Erfüllungslagerplätzen durch die erste Iteration der verteilten Auftragsverwaltung (DOM) in Microsoft Dynamics 365 for Retail wurde nur die Entfernung als Faktor berücksichtigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Although distance can be correlated with cost, it isn't the same as cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Auch wenn diese ggf. mit Kosten korreliert, ist sie nicht mit Kosten identisch.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">So kann ein Übernachtversand über dieselbe Entfernung mehr als ein Drei- oder Sieben-Tage-Versand kosten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Mit der Funktion zur Kostenkonfiguration können Einzelhändler zusätzliche Kostenkomponenten anlegen und konfigurieren, die zur Ermittlung des besten Standortes zur Erfüllung von Auftragspositionen berechnet und berücksichtigt werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sind Kostenkomponenten konfiguriert, verwendet der DOM-Solver bei der Ermittlung des besten Erfüllungslagerplatzes nur diese Kostendefinitionen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>It doesn't consider the distance component as a cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Entfernungskomponente wird nicht als Kosten berücksichtigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Sind keine Kostenkomponenten konfiguriert, verwendet der DOM-Solver bei der Ermittlung des besten Erfüllungslagerplatzes die Entfernungskomponente als Kosten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Set up cost components</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Kostenkomponenten einrichten</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Two major cost component types can be defined in the system: <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Other<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">In System können zwei maßgebliche Kostenkomponenten festgelegt werden: <bpt id="p1">**</bpt>Versand<ept id="p1">**</ept> und <bpt id="p2">**</bpt>Sonstiges<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Both cost component types support multiple calculation bases, as shown in the following table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wie in der folgenden Tabelle dargestellt, unterstützen beide Typen von Kostenkomponenten mehrere Berechnungsgrundlagen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Cost component type</source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match">Typ der Kostenkomponente</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Calculation basis</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Berechnungsbasis</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Shipping</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Versand</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Simple</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Einfach</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Tiered</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Mehrstufig</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Other</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Sonstiges</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Sales order</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Auftrag</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Sales line</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Verkaufsposition</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Location</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Ort</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Shipping cost component type</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Kostenkomponententyp „Versand“</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and a calculation basis for shipping costs.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">In diesem Abschnitt wird beschrieben, wie die einzelnen Kombinationen des Kostenkomponententyps <bpt id="p1">**</bpt>Versand<ept id="p1">**</ept> und eine Berechnungsgrundlage für Versandkosten eingerichtet werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>It also explains how the DOM solver uses each combination.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ferner wird erläutert, wie der DOM-Solver die einzelnen Kombinationen verwendet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Cost component type = Shipping and Calculation basis = Simple</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kostenkomponententyp = Versand und Berechnungsgrundlage = Einfach</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Simple<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wird eine Kombination aus dem Kostenkomponententyp <bpt id="p1">**</bpt>Versand<ept id="p1">**</ept> und der Berechnungsgrundlage <bpt id="p2">**</bpt>Einfach<ept id="p2">**</ept> verwendet, beruhen die Versandkosten einer Lieferart entweder auf einer Kostenpauschale oder auf der Entfernung.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must set up the following fields for this combination:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Für diese Kombination müssen die folgenden Felder eingerichtet werden:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Kostenfaktor<ept id="p1">**</ept>: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source><target logoport:matchpercent="78" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Beschreibung<ept id="p1">**</ept>: Geben Sie Name und Beschreibung des Kostenfaktors ein.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Startdatum<ept id="p1">**</ept> und <bpt id="p2">**</bpt>Enddatum<ept id="p2">**</ept>: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Aktiv<ept id="p1">**</ept>: Gibt an, ob der Kostenfaktor aktiv ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Unternehmen<ept id="p1">**</ept>: Geben Sie die juristische Person an, für die Kostenfaktor konfiguriert wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>All lines of the calculation criteria must be for the same legal entity.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Alle Positionen der Berechnungskriterien müssen sich auf dieselbe juristische Person beziehen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Lieferarten<ept id="p1">**</ept>: Geben Sie die Lieferarten an, für die die Kosten konfiguriert werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Berechnungstyp<ept id="p1">**</ept>: Geben Sie an, wie die Kosten für die einzelnen Lieferarten berechnet werden sollen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Two calculation types are supported:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Es werden zwei Berechnungsarten unterstützt:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Fest<ept id="p1">**</ept>: Für die Lieferart wird eine Pauschale verwendet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bei Auswahl dieser Berechnungsart bestimmt das Feld <bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept> die Kostenpauschale.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Per-distance unit<ept id="p1">**</ept> – The cost for the mode of delivery is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Pro Entfernungseinheit<ept id="p1">**</ept>: Die Kosten für die Lieferart werden berechnet, indem der im Feld <bpt id="p2">**</bpt>Kosten<ept id="p2">**</ept> angegebene Wert mit der Entfernung zwischen Lieferadresse und Standorten multipliziert wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept>: Geben Sie den Wert an, der im Zusammenhang mit dem Feld <bpt id="p2">**</bpt>Berechnungstyp<ept id="p2">**</ept> verwendet wird, um die Kosten für eine Lieferart zu berechnen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Cost component type = Shipping and Calculation basis = Tiered</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Kostenkomponententyp = Versand und Berechnungsgrundlage = Mehrstufig</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Tiered<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match">Wird eine Kombination aus dem Kostenkomponententyp <bpt id="p1">**</bpt>Versand<ept id="p1">**</ept> und der Berechnungsgrundlage <bpt id="p2">**</bpt>Mehrstufig<ept id="p2">**</ept> verwendet, beruhen die Versandkosten einer Lieferart entweder auf einer Kostenpauschale oder auf der Entfernung.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>However, in this combination, the distance is based on a tiered range of distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Allerdings beruht die Entfernung bei dieser Kombination auf einer mehrstufigen Entfernungsskala.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Für diese Kombination müssen die folgenden Felder eingerichtet werden:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kostenfaktor<ept id="p1">**</ept>: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Beschreibung<ept id="p1">**</ept>: Geben Sie Name und Beschreibung des Kostenfaktors ein.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>Default cost<ept id="p1">**</ept> – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Standardkosten<ept id="p1">**</ept>: Geben Sie die Kosten an, die für eine Lieferart verwendet werden sollen, wenn die Entfernung zwischen der Lieferadresse und dem Standort nicht in eine der mehrstufigen Entfernungen der Lieferart fällt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Startdatum<ept id="p1">**</ept> und <bpt id="p2">**</bpt>Enddatum<ept id="p2">**</ept>: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktiv<ept id="p1">**</ept>: Gibt an, ob der Kostenfaktor aktiv ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Unternehmen<ept id="p1">**</ept>: Geben Sie die juristische Person an, für die Kostenfaktor konfiguriert wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>All lines of the calculation criteria must be for the same legal entity.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Alle Positionen der Berechnungskriterien müssen sich auf dieselbe juristische Person beziehen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Lieferarten<ept id="p1">**</ept>: Geben Sie die Lieferarten an, für die die Kosten konfiguriert werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Distance type<ept id="p1">**</ept> – Specify whether the tiered distance definition is an aerial distance or a road distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Entfernungstyp<ept id="p1">**</ept>: Geben Sie an, ob die mehrstufige Entfernungsdefinition Luftlinie oder Straßenentfernung ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Distance units<ept id="p1">**</ept> – Specify the unit that the tiered distance is measured in.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Entfernungseinheiten<ept id="p1">**</ept>: Geben Sie die Einheit an, in der die Entfernung gemessen wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Distance from<ept id="p1">**</ept> – Specify the start range for the tiered distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Entfernung von<ept id="p1">**</ept>: Geben Sie den Startpunkt der mehrstufigen Entfernung an.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>Distance to<ept id="p1">**</ept> – Specify the end range for the tiered distance.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Entfernung bis<ept id="p1">**</ept>: Geben Sie den Zielpunkt der mehrstufigen Entfernung an.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Berechnungstyp<ept id="p1">**</ept>: Geben Sie an, wie die Kosten für die einzelnen Lieferarten und die mehrstufige Entfernung berechnet werden sollen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Two calculation types are supported:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Es werden zwei Berechnungsarten unterstützt:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Fest<ept id="p1">**</ept>: Für die Lieferart wird eine Pauschale verwendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Bei Auswahl dieser Berechnungsart bestimmt das Feld <bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept> die Kostenpauschale.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Per distance unit<ept id="p1">**</ept> – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Pro Entfernungseinheit<ept id="p1">**</ept>: Die Kosten für die Lieferart und die mehrstufige Entfernung werden berechnet, indem der im Feld <bpt id="p2">**</bpt>Kosten<ept id="p2">**</ept> angegebene Wert mit der Entfernung zwischen Lieferadresse und Standorten multipliziert wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept>: Geben Sie den Wert an, der im Zusammenhang mit dem Feld <bpt id="p2">**</bpt>Berechnungstyp<ept id="p2">**</ept> verwendet wird, um die Kosten für eine Lieferart zu berechnen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>When you define tiered distances, the system validates that there are no missing or overlapping distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bei Angaben mehrstufiger Entfernungen prüft das System, ob Entfernungen fehlen oder überlappen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The distance type that is used for a mode of delivery must be the same across all the tiered distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Der für eine Lieferart verwendete Entfernungstyp muss für alle mehrstufigen Entfernungen identisch sein.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Other cost component type</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Kostenkomponententyp „Sonstiges“</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and an other cost type for non-shipping costs.</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">In diesem Abschnitt wird beschrieben, wie die einzelnen Kombinationen des Kostenkomponententyps <bpt id="p1">**</bpt>Sonstiges<ept id="p1">**</ept> und eines weiteren Kostentyps bei nicht versandbezogenen Kosten berechnet werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>It also explains how the DOM solver uses each combination.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Ferner wird erläutert, wie der DOM-Solver die einzelnen Kombinationen verwendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Cost component type = Other and Other cost type = Sales order</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kostenkomponententyp = Sonstiges und anderer Kostentyp = Auftrag</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales order<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Eine Kombination aus dem Kostenkomponententyp <bpt id="p1">**</bpt>Sonstiges<ept id="p1">**</ept> und dem anderen Kostentyp <bpt id="p2">**</bpt>Auftrag<ept id="p2">**</ept> wird verwendet, um auf Auftragsebene Kosten ohne Versandbezug zu definieren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Für diese Kombination müssen die folgenden Felder eingerichtet werden:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kostenfaktor<ept id="p1">**</ept>: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Beschreibung<ept id="p1">**</ept>: Geben Sie Name und Beschreibung des Kostenfaktors ein.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Startdatum<ept id="p1">**</ept> und <bpt id="p2">**</bpt>Enddatum<ept id="p2">**</ept>: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktiv<ept id="p1">**</ept>: Gibt an, ob der Kostenfaktor aktiv ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept>: Geben Sie den Wert für nichtversandbezogene Kosten auf Auftragsebene ein.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Cost component type = Other and Other cost type = Sales line</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Kostenkomponententyp = Sonstiges und anderer Kostentyp = Auftragsposition</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales line<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order line level.</source><target logoport:matchpercent="93" state="translated" state-qualifier="fuzzy-match">Eine Kombination aus dem Kostenkomponententyp <bpt id="p1">**</bpt>Sonstiges<ept id="p1">**</ept> und dem anderen Kostentyp <bpt id="p2">**</bpt>Auftragsposition<ept id="p2">**</ept> wird verwendet, um auf Auftragspositionsebene Kosten ohne Versandbezug zu definieren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Für diese Kombination müssen die folgenden Felder eingerichtet werden:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kostenfaktor<ept id="p1">**</ept>: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Beschreibung<ept id="p1">**</ept>: Geben Sie Name und Beschreibung des Kostenfaktors ein.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Startdatum<ept id="p1">**</ept> und <bpt id="p2">**</bpt>Enddatum<ept id="p2">**</ept>: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktiv<ept id="p1">**</ept>: Gibt an, ob der Kostenfaktor aktiv ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order line level.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept>: Geben Sie den Wert für nichtversandbezogene Kosten auf Auftragspositionsebene ein.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Cost component type = Other and Other cost type = Location</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Kostenkomponententyp = Sonstiges und anderer Kostentyp = Standort</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Location<ept id="p2">**</ept> other cost type is used to define non-shipping costs for a group of locations or an individual location.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Eine Kombination aus dem Kostenkomponententyp <bpt id="p1">**</bpt>Sonstiges<ept id="p1">**</ept> und dem anderen Kostentyp <bpt id="p2">**</bpt>Standort<ept id="p2">**</ept> wird verwendet, um für eine Gruppe von Standorten oder für einen einzelnen Standort nichtversandbezogene Kosten zu berechnet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Für diese Kombination müssen die folgenden Felder eingerichtet werden:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kostenfaktor<ept id="p1">**</ept>: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Beschreibung<ept id="p1">**</ept>: Geben Sie Name und Beschreibung des Kostenfaktors ein.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Startdatum<ept id="p1">**</ept> und <bpt id="p2">**</bpt>Enddatum<ept id="p2">**</ept>: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktiv<ept id="p1">**</ept>: Gibt an, ob der Kostenfaktor aktiv ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>Fulfillment group<ept id="p1">**</ept> – Specify the group of locations that the non-shipping cost is defined for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Erfüllungsgruppe<ept id="p1">**</ept>: Geben Sie die Gruppe der Standorte an, für die die Kosten ohne Versandbezug definiert werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>Fulfillment location<ept id="p1">**</ept> – Specify the location that the non-shipping cost is defined for.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Erfüllungslagerplatz<ept id="p1">**</ept>: Geben Sie den Ort an, für den die Kosten ohne Versandbezug definiert werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bei standortbasierten Berechnungskriterien können keine Erfüllungsgruppe und kein Erfüllungslagerplatz angegeben werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept>: Geben Sie den Wert für die Kosten ohne Versandbezug auf Ebene der Erfüllungsgruppe oder auf Ebene des Erfüllungslagerplatzes an.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Damit diese Kosten bei der DOM berücksichtigt werden, muss der Kostenfaktor im jeweiligen Erfüllungsprofil ergänzt werden.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>