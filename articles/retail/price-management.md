<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="price-management.md" target-language="de-DE">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>price-management.9d0b0e.afa553fd0562b306f720f2a30c7f901db7ad1b3a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>afa553fd0562b306f720f2a30c7f901db7ad1b3a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>0fbfb9b0ab78c804f3931a083028d2ce313d6521</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/21/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\price-management.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail sales price management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Einzelhandelspreisverwaltung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the concepts for creating and managing sales prices in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In diesem Thema werden die Konzepte für das Erstellen und Verwalten von Verkaufspreisen in Microsoft Dynamics 365 for Retail behandelt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail sales price management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verwaltung von Einzelhandelsverkaufspreisen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides information about the process of creating and managing sales prices in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dieses Thema enthält Informationen über den Prozess der Berichterstellung und Verwaltung von Verkaufspreisen in Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>It focuses on the concepts that are involved in this process, and on the effects of the various configuration options for sales prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Es bezieht sich auf die Konzepte, die an diesem Prozess beteiligt sind, und auf die Auswirkungen der verschiedenen Konfigurationsoptionen für Verkaufspreise.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Terminology</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Terminologie</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The following terms are used in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die folgenden Begriffe werden in diesem Thema erläutert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Term</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zeitdauer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Definition, usage, and notes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Definition, Verwendung und Hinweise</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preis</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The single unit amount that a product sells for in a point of sale (POS) client or on a sales order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der einzelne Einheitenbetrag, der ein Produkt in einem Verkaufsstellen (POS)- Client oder einem Auftrag verkauft.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In this topic, the term <bpt id="p1">*</bpt>price<ept id="p1">*</ept> always refers to the sales price, not the inventory price or cost price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In diesem Thema bezieht sich <bpt id="p1">*</bpt>Preis<ept id="p1">*</ept> immer den Verkaufspreis, nicht des Lagerpreises oder den Einstandspreis an.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Base price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Basispreis</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The price that is set in the <bpt id="p1">**</bpt>Price<ept id="p1">**</ept> field on a released product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Preis, der im Feld <bpt id="p1">**</bpt>Preis<ept id="p1">**</ept> auf einen gemeinsam verwendete Produktdimensionsgruppe festgelegt wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Trade agreement price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preisgestaltung für Handelsvereinbarung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The price that is set on a product or variant by using a trade agreement of the <bpt id="p1">**</bpt>Price (sales)<ept id="p1">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Preis, der auf ein Produkt oder eine Variante festgelegt wird, indem eine Handelsvereinbarung des Typs <bpt id="p1">**</bpt>Preis (Verkauf)<ept id="p1">**</ept> verwendet wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Best price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bester Preis</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>When more than one price or discount can be applied to a product, the smallest price amount and/or the largest discount amount that produces the lowest possible net amount that the customer must pay.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn mehr als ein Preis oder Rabatt auf ein Produkt angewendet wird, der kleinste oder Preisbetrag und/oder der größte Rabattbetrag, der den niedrigsten Nettobetrag produziert, den der Debitor bezahlen muss, wird angewendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In this topic, the concept of best price is always referred to as "the best price."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In diesem Thema gilt das Konzept des besten Preises immer als der beste "Preis".</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This best price differs from and should not be confused with the <bpt id="p1">**</bpt>Best price<ept id="p1">**</ept> enumeration value for a discount's concurrency mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dieser beste Preis unterscheidet sich vom und sollte nicht mit dem <bpt id="p1">**</bpt>Besten Preis<ept id="p1">**</ept> Optionswert für einen Rabattmodus verwechselt werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Price groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preisgruppen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Price groups are at the heart of price and discount management in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preisgruppen sind zentral in der Preis- und Rabattverwaltung in Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Price groups are used to assign prices and discounts to retail entities (that is, channels, catalogs, affiliations, and loyalty programs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preisgruppen werden verwendet, um Rabatte und Handelsvereinbarungen zu den Einzelhandelskanälen, Zugehörigkeiten, Katalogen und Treueprogrammen zuzuweisen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Because price groups are used for all pricing and discounts, it's very important that you plan how you will use them before you start.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Da Preisgruppen für alle Preise und Rabatte verwendet werden, ist es sehr wichtig, dass Sie planen, wie Sie diese verwenden, bevor Sie beginnen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>By itself, a price group is just a name, a description, and, optionally, a pricing priority.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">An sich ist eine Preisgruppe derzeit ein Name, Beschreibung und optional eine Preiskalkulationspriorität.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The main point to remember about price groups is that they are used to manage the many-to-many relationships that discounts and prices have with retail entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Hauptpunkt, an den man sich bei Preisgruppen erinnern soll ist, dass sie verwendet werden, um die m:n-Beziehungen zu verwalten, die Rabatte und Preise mit Kleinentitäten haben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The following illustration shows how price groups are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die folgende Abbildung zeigt, wie Preisgruppen verwendet werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In this illustration, notice that "Price group" is literally at the center of pricing and discount management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In dieser Grafik beachten Sie, dass "Preisgruppe" buchstäblich in der Mitte der Preiskalkulations- und Rabattverwaltung ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The retail entities that you can use to manage differential prices and discounts are on the left, and the actual price and discount records are on the right.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Kleinentitäten, die Sie verwenden können, um differenzielle Preise und Rabatte zu verwalten, sind auf der linken Seite und die Effektivpreis- und Rabattdatensätze sind auf der rechten Seite.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">![</bpt>Price groups<ept id="p1">]</ept><bpt id="p2">(./media/PriceGroups.png "</bpt>Price groups<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>Preisgruppen<ept id="p1">]</ept><bpt id="p2">(./media/PriceGroups.png "</bpt>Preisgruppen<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>When you create price groups, you should not use a single price group for multiple types of retail entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn Sie Preisgruppen erstellen, sollten Sie eine Gruppe des Uniform Preises für mehrere Arten von Kleinentitäten nicht verwenden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Otherwise, it can be difficult to determine why a specific price or discount is being applied to a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Andernfalls kann es schwierig sein zu ermitteln, warum ein bestimmter Preis oder ein Rabatt auf eine Buchung angewendet wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>As the red dashed line in the illustration shows, Retail does support the core Microsoft Dynamics 365 functionality of a price group that is set directly on a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wie die rot gestrichelte Linie in der Abbildung zeigt, unterstützt Retail die zentralen Microsoft Dynamics 365-Funktionen einer Preisgruppe, die direkt auf einen Kunden festgelegt wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>However, in this case, you get only sales price trade agreements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jedoch in diesem Fall erhalten Sie nur Handelsvereinbarungen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you want to apply customer-specific prices, we recommend that you not set price groups directly on the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Falls Sie benutzerdefinierte Preise anwenden möchten, sollten Sie nicht festgelegte Preisgruppen direkt für den Debitor definieren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Instead, you should use affiliations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stattdessen können Sie Zuordnungen verwenden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The following sections provide more information about the retail entities that you can use to set distinct prices when the price groups are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die folgenden Abschnitte enthalten weitere Informationen zur Kleinentitäten, die Sie verwenden können, wenn Preise festgelegt werden, wenn eindeutige Preisgruppen verwendet werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The configuration of prices and discounts for all these entities is a two-step process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Variante von Preisen und Rabatten für alle diese Entitäten ist ein Prozess in zwei Schritten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>These steps can be done in either order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Diese Schritte können in jedem Auftrag vorgenommen werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>However, the logical order is to set the price groups on the entities first, because this step is likely to be a one-time setup that is done during implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Allerdings besteht die logische Reihenfolge darinm, Preisgruppen auf die Entitäten zuerst festzulegen, da dieser Schritt nicht wahrscheinlich eine einmalige Einstellung ist, die bei der Implementierung geleistet wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Then, as prices and discounts are created, you can set the price groups on those prices and discounts individually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Anschließend wenn Preise und Rabatte erstellt werden, können Sie Preisgruppen die auf diesen Preisen und Rabatten basieren, einzeln festlegen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Channels</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Benachrichtigungskanäle</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the retail industry, it's very typical to have different prices in different channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Im Einzelhandel ist es sehr typisch, verschiedene Preise in verschiedenen Kanälen zu haben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The two primary factors that affect channel-specific prices are costs and local market conditions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die primären zwei Faktoren, die Kanal spezifische Preise beeinflusse, sind Kosten, und lokale Marktlagen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Costs<ept id="p1">**</ept> – The farther away a channel is from the product source, the more it costs to stock a product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Kosten<ept id="p1">**</ept> – Je weiter weg ein Kanal von der Produktquelle ist, desto mehr kostet der Bestand eines Produktes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>For example, fresh produce has a limited shelf life and specific production requirements (for example, a growing season).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">So verfügt beispielsweise Frischware eine begrenzte Haltbarkeit und besondere Produktionsanforderungen (beispielsweise eine Vegetationsperiode).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>During the winter, fresh lettuce likely costs more in northern climates than in southern climates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Während des Winters kostet frischer Kopfsalates in den Nordklimata vermutlich mehr als in den südlichen. Klimata</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If you're setting prices for channels over a large geographical area, you will probably want to set different prices in different channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn Preise für Kanäle in einem großen geografischen Bereich festgelegt werden soll, müssen Sie wahrscheinlich verschiedene Preise in verschiedenen Kanälen festlegen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">**</bpt>Local market conditions<ept id="p1">**</ept> – A store that has a direct competitor across the street will be much more price-sensitive than a store that doesn't have a direct competitor nearby.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Lokale Marktlagen<ept id="p1">**</ept> – Ein Shop, der über einen direkten Mitbewerber in der gleichen Straße hat ist vermutlich Preis sensitiver als ein Geschäft, dass keinen unmittelbaren Mitbewerber hat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Affiliations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zugehörigkeiten</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The general definition of an affiliation is a link to or association with a group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bei einer Definition einer allgemeinen Zugehörigkeit ist ein Link die Zuordnung zu einer Gruppe.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>In Retail, affiliations are groups of customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In Retail sind Zuordnungen Gruppen von Debitoren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Affiliations are a much more flexible tool for customer pricing and discounts than the core Microsoft Dynamics 365 concept of customer groups and discount groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zuordnungen sind ein wesentlich flexibleres Tool für Kundenpreiskalkulation und -Rabatte als das Microsoft Dynamics 365 Kernkonzept von Debitorengruppen und Rabattgruppen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>First, an affiliation can be used for both prices and discounts, whereas non-retail pricing has a different group for each type of discount and price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zuerst kann eine Zugehörigkeit für beide Preise und Rabatte verwendet werden, während Nicht-Einzelhandelpreiskalkulation eine andere Gruppe für jeden Typ Rabatt und Preis ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Next, a customer can belong to multiple affiliations but can belong to only one non-retail pricing group of each type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Danach kann ein Debitor mehrere Zuordnungen haben, jedoch kann nur eine Nicht-Einzelhandelpreiskalkulationsgruppe dem jeweiligen Typ angehören.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Finally, although affiliations can be set up so that they are linked to a customer, they don't have to be.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Schließlich obwohl Zuordnungen verwendet werden, damit sie einem Debitor zugeordnet sind, müssen beide nicht zwangsläufig zugeordnet sein.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>An ad-hoc affiliation can be used for anonymous customers at the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eine ad hoc Zugehörigkeit kann für die anonyme Debitoren am POS verwendet werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>A typical example of an anonymous affiliation discount is a senior or student discount, where a customer can receive a discount just by showing a group membership card.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ein typisches Beispiel eines anonymen Zugehörigkeitsrabatts ist ein Senior- oder Studierenderrabatt, wobei der Kunde einen Rabatt erhält, der momentan durch die Auswahl einer Gruppenmitgliedschaftskarte anzeigt wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Although affiliations are most often associated with discounts, you can also use them to set differential pricing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Obwohl Zuordnungen am häufigsten Rabatten zugeordnet sind, können diese auch verwendet werden, um verschiedene Preisgestaltung festzulegen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For example, when a retailer sells to an employee, it might want to change the selling price instead of applying a discount on top of the regular price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn beispielsweise ein Einzelhändler für einen Mitarbeiter verkauft, sollte der der Verkaufspreis ändern, anstatt einen Rabatt zu übernehmen in den normalen Preis.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>As another example, a retailer that sells to both consumer customers and business customers might offer business customers better prices, based on their purchasing volume.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ein anderes Beispiel ist, ein Einzelhändler, der Einzelkunden und Firmenkunden Preise der Firmenkunden auf Grundlage der Einkaufsvolumen anbietet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Affiliations enable both these scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zuordnungen aktivieren diese beiden Szenarien.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Loyalty programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Treueprogramme</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>In relation to prices and discounts, loyalty programs are basically just an affiliation that has a special name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hinsichtlich Preise und Rabatte sind Treueprogramme im Allgemeinen derzeit eine Zugehörigkeit, die einen bestimmten Namen hat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Both prices and discounts can be set for a loyalty program, just as they can be set for an affiliation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preise und Rabatte können für ein Treueprogramm festgelegt werden, während sie derzeit für eine Zugehörigkeit festgelegt werden können.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>However, the way that customers get loyalty pricing during a transaction or order differs from the way that they get affiliation pricing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Allerdings unterscheidet sich die Möglichkeit, dass Kunden Loyalitätspreiskalkulation während einer Buchung oder eines Auftrags zugewiesen wird, von der Methode, mit der sie Zugehörigkeitspreiskalkulation abrufen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Customers can get loyalty pricing only if a loyalty card is added to a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Debitoren können die angegebenen Treuepreis abrufen, wenn eine Treuekart einer Buchung hinzugefügt wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>When a loyalty card is added to a transaction, the loyalty program is also added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn eine Treuekarte einer Buchung hinzugefügt wird, wird das Treueprogramm auch hinzugefügt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The loyalty program then enables special prices and discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Das Treueprogramm aktiviert dann Sonderpreise und Rabatte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Loyalty programs can have multiple tiers, and the discounts can differ for different tiers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ein Treueprogramm kann mehrere Ebenen besitzen, und Rabatte können sich für verschiedene Ebenen unterscheiden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>In this way, retailers can give frequent customers larger rewards without having to manually put those customers into a special group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Auf diese Weise können Einzelhändler rasch Debitoren größere Belohnungen geben, ohne dass diese Debitoren in einer speziellen Gruppe manuell zugeordnet werden müssen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Loyalty programs have additional functionality besides prices and discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ein Treueprogramm hat zusätzliche Funktionen mit Ausnahme von Preisen und Rabatten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>However, from the perspective of pricing and discounts, they are the same as affiliations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Allerdings sind sie aus der Perspektive der Preiskalkulation und der Rabatte die gleichen wie Zuordnungen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Catalogs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kataloge</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Some retailers use physical or virtual catalogs to market products to, and price them for, focused groups of customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Einige Einzelhändler werden die physischen oder virtuellen Kataloge nutzen und diese Preise für fokussierte Debitorengruppen festlegen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>As part of their business model to target marketing via a catalog, these retailers can set differential prices on their various catalogs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Im Rahmen des Geschäftsmodells zum zielgruppenorientierten Marketing zu einem Katalog können diese differenzielle Einzelhändler Preise auf ihren verschiedenen Katalogen festlegen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Microsoft Dynamics 365 supports this capability by letting you define catalog-specific discounts and prices, just as you can define channel-specific or affiliation-specific discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 unterstützt diese Funktion und erlaubt Ihnen, katalogspezifische Rabatte und -Preise zu definieren, ebenso wie kanalspezifische oder zuordnungsspezifische Rabatte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>When you edit a catalog, you can associate price groups with the catalog, just as you can associate them with a channel, affiliation, or loyalty program.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn Sie einen Katalog ändern, können Sie Preisgruppen dem Katalog, als Sie zuordnen können sie einem Kanal, einer Zugehörigkeit oder einem Treueprogramm zuordnen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Best practices for price groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Optimale Verfahren für Preisgruppen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Don't use a price group for multiple retail entity types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verwenden Sie keine Preisgruppe für mehrere Kleinentitätstypen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Instead, use one set of price groups for channels, a different set of price groups for affiliations or loyalty programs, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verwenden Sie stattdessen einen Satz Preisgruppen für Kanäle, einen anderen Satz Zuordnungen oder Preisgruppen für Treueprogramme, usw.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>You can use a prefix or suffix in the name of the price group to visually group the various types of price groups that you're using.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sie können ein Präfix oder ein Suffix im Auftrag der Preisgruppe verwendet, um die unterschiedlichen Arten von Preisgruppen visuell zu gruppieren, die Sie verwenden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Avoid setting price groups directly on a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vermeiden Sie es, Preisgruppen direkt auf einem Debitor festzulegen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Instead, use an affiliation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verwenden Sie stattdessen eine Zugehörigkeit.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>In this way, you can assign all types of prices and discounts to customers, not just sales price trade agreements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Auf diese Weise können Sie alle Typen von Preisen und Rabatten zuweisen für Debitoren, nicht nur Handelsvereinbarungen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Pricing priority</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preisgestaltungspriorität</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>By itself, a pricing priority is just a number and a description.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">An sich ist eine Preiskalkulationspriorität derzeit eine Nummer sowie eine Beschreibung.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Pricing priorities can be applied to price groups, or they can be applied directly to discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preiskalkulationsprioritäten können den Preisgruppen angewendet werden, oder sie können direkt auf Rabatte angewendet werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>When pricing priorities are used, they let a retailer override the principle of the best price by controlling the order in which prices and discounts are applied to products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn dieser für Preis Prioritäten angegebenen, werden verwendet, wenn sie den Einzelhändler das Prinzip des besten Preis überschreiben, indem die Reihenfolge steuern, in dem die Preise und Rabatte zu Produkten angewendet werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>A larger pricing priority number is evaluated before a lower pricing priority number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eine höhere Preiskalkulationsprioritätsnummer wird vor einer unteren Preiskalkulationsprioritätsnummer ausgewertet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Additionally, if a price or discount is found at any priority number, all prices or discounts that have lower priority numbers are ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Darüber hinaus wenn ein Preis oder eines Rabatts an irgendeinem Prioritätsnummer, in allen oder an Preisen Rabatte gefunden wird, die untere Prioritätsnummern haben, werden ignoriert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The price and a discount can come from two different pricing priorities, because pricing priorities apply to prices and discounts independently.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preis und Rabatt können von zwei unterschiedlichen Preiskalkulationsprioritäten stammen, da Preisprioritäten für Preise und Rabatte unabhängig gelten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>To use pricing priority for prices, you must assign a pricing priority to a price group and then create a sales price trade agreement for that price group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Um Preiskalkulationspriorität für Preise zu verwenden, müssen Sie eine Preiskalkulationspriorität einer Preisgruppe zuweisen und eine Verkaufspreis-Handelsvereinbarung Preisgruppe für diese erstellt werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The pricing priority feature was introduced to support the scenario where a retailer wants to apply higher prices in a specific set of stores.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Preiskalkulationsprioritätsfunktion wurde eingegeben, um das Szenario zu unterstützen, in dem ein Einzelhändler höhere Preise in einem bestimmten Geschäft übernehmen möchte, das aus den Shops festgelegt wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>For example, a retailer has defined regional prices for the east coast of the United States but wants higher prices for some products in New York City stores, because it costs more to sell some products in the city, and/or because the local market will bear a higher price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">So verfügt beispielsweise ein Einzelhändler definiert regionale Preise für die Ostküste der USA aber möchte höhere Preise für mehrere Produkte in New York Cityshops, da es mehr kostet, um mehrere Produkte im Ort zu verkaufen und/oder weil der lokale Markt einen höheren Preis verträgt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>As was described in the "Best price" section of this topic, the retail pricing engine typically selects the lower of two prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wie im Abschnitt "Bester Preis" beschrieben wurde, wählt das Einzelhandelspreismodul in der Regel den tieferen der zwei Preise aus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Therefore, the retailer is usually prevented from using the higher of two prices in a store that has both the East coast and New York price groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Daher wird der Einzelhändler normalerweise daran gehindert, den höheren der beiden Preisen in einem Shop zu verwenden, der die Ostküste und New York als Preisgruppen hat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>To resolve this issue before the pricing priority feature was introduced, the retailer had to define prices for every product two times and not assign both price groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zur Behebung dieses Problems muss der Einzelhändler Preise für jedes Produkt zweimal definieren und Preisgruppen nicht beiden zuweisen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Alternatively, the retailer had to create extra price groups to isolate the products that have higher prices from products that have the usual, lower prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Alternativ musste der Einzelhändler zusätzliche Preisgruppen erstellen, um die Produkte zu suchen, die höhere Preise von Produkten verfügen, die die üblichen, niedrigeren Preisen haben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>However, the pricing priority feature lets the retailer create a pricing priority for store prices that is higher than the pricing priority for regional prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Allerdings ermöglicht die Preiskalkulationsfunktion es zu, dass der Einzelhändler eine Preiskalkulationspriorität für Shop-Preise erstellt, die höher als die Preiskalkulationspriorität regionaler Preise ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Alternatively, the retailer can create a pricing priority just for store prices and leave regional prices at the default pricing priority, which is 0 (zero).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Alternativ kann der Einzelhändler eine Preiskalkulationspriorität für Shop-Preise regionaler Preise erstellen und die Standardpreiskalkulationspriorität lassen, die 0 (null )ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Both setups help guarantee that store prices will always be used before regional prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beide Einstellungen stellen sicher, dass Shop-Preise immer vor regionalen Preise verwendet werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Pricing priority example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beispiel der Preisgestaltungspriorität</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Let's look at an example where store prices override other prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Schauen wir ein Beispiel an, bei dem Shop-Preise andere Preise überschreiben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>A national retailer sets most prices per region, and it has four regions: North east, South east, Mid-west and West.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ein nationaler Einzelhändler legt die meisten Preise pro Region fest, und besitzt vier Regionen: Nordosten, Südosten, Mittlerer Westen und Westen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>It has identified several high-cost markets that can support higher prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Er hat mehrere Märkte mit hohen Kosten bestimmt, die höhere Preise unterstützen können.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>These markets are in New York City, Chicago, and the San Francisco Bay area.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Diese Märkte sind in New York City, in Chicago und im San-Francisco Baybereich.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>For this example, we will drill into the North east region.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In vorliegenden Beispiel schauen wir die Region Nordosten an.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Store 1 is in Boston, and store 2 is in Manhattan.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Shop 1 ist in Boston, und Shop 2 ist in Manhattan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>For the Boston store, two price groups are linked to the channel: North East and Store 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Für den Boston-Shop werden zwei Preisgruppen mit dem Kanal verknüpft: Nordosten und Shop 1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>For the Manhattan store, three price groups are linked to the channel: North East, NYC, and Store 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Für den Manhatten-Shop werden drei Preisgruppen mit dem Kanal verknüpft: Nordosten, NYC und Shop 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>The retailer sets up two pricing priorities: High cost has a priority number of 5, and Store prices has a priority number of 10.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Einzelhändler legt zwei Preisprioritäten fest: Hohe Kosten besitzen eine Prioritätsnummer von 5, und Shop-Preise hat eine Prioritätsnummer von 10.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>(Remember that, by default, the pricing priority is 0 <ph id="ph1">\[</ph>zero<ph id="ph2">\]</ph>, and a price or discount that has a higher priority number is used before a price or discount that has a lower priority number.) For the North East price group, the pricing priority is left at the default value of <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Bedenken Sie, dass standardmäßig die Preiskalkulationspriorität 0 <ph id="ph1">\[</ph>Null<ph id="ph2">\]</ph>und ein Preis oder Rabatt eine höhere Nummer hat, bevor ein Preis oder einen Rabatt verwendet wird, der eine niedrigere Prioritätsnummer hat). Für die Nordostpreisgruppe wird die Preiskalkulationspriorität am Standardwert <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (Null) sein.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>For the NYC price group, the pricing priority is set to <bpt id="p1">**</bpt>5<ept id="p1">**</ept>, because New York City is a high-cost market.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Für die NYC-Preisgruppe wird die Preiskalkulationspriorität auf <bpt id="p1">**</bpt>5<ept id="p1">**</ept> festgelegt, da New York ein Markt mit hohen Kosten ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>For the Store 1 and Store 2 price groups, the pricing priority is set to <bpt id="p1">**</bpt>10<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Für die Shop 1 und Shop 2 Preisgruppen, wird die Preiskalkulationspriorität auf <bpt id="p1">**</bpt>10<ept id="p1">**</ept> festgelegt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Two products that the retailer sells are product 1, a commodity T-shirt, and product 2, brand-specific fashion jeans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zwei Produkte, die der Einzelhändler als Produkt 1 verkauft, eine Ware T-Shirt und ein Produkt 2, makrenspezifische Jeans.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Product</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Produkt</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>North East price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preise Nordosten</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>NYC price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NYS Preis:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Store price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Shoppreise</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>T-shirt</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">T-Shirt</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>$15</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Not set</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nicht festgelegt</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Not set</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nicht festgelegt</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Fashion jeans</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modische Jeans</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>$50</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$50</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>$70</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$70</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Not set</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nicht festgelegt</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The T-shirt sells for the same price (that is, $15) at both the Boston and Manhattan stores, because only one price is set in the North East price group that is linked to both channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Das T-Shirt verkauft sich für denselben Preis (das heißt, $15) in den Boston- und Manhattan-Shops, da nur ein Preis in der Nordostpreisgruppe festgelegt wurde, die beide Kanäle verknüpft.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The fashion jeans sell for $50 in the Boston store, because that price is the only price that is available in that store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die modischen Jeans verkaufen sich im Boston-Shop für $50, weil dies der einzige verfügbare Preis im Shop ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>However, in the Manhattan store, two prices are available: $50 and $70.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jedoch im Manhattan-Shop, stehen zwei Preise zu Verfügung: $50 und $70.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Because the pricing priority of 5 for the NYC price group is higher than the pricing priority of 0 (zero) for the North East price group, the price will be rung up as $70 in the POS system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Da die Preiskalkulationspriorität von 5 für die NYC-Preisgruppe höher ist als die Preiskalkulationspriorität von 0 (null )für die Nordostpreisgruppe ist, wird der Preis im POS-System als Rollup für beide Artikel bezeichnet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>For each pricing priority, a full pass through the logic for the retail pricing engine is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Für jede Preiskalkulationspriorität ist ein vollständiger Durchlauf für die Verkaufslogik des Einzelhandelspreismoduls erforderlich.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Therefore, to help maintain the performance of the price and discount calculation, you should use pricing priorities sparingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Um die Leistung der Rabattberechnung der Preis und Rapatte zu verwalten, sollten Sie Preiskalkulationsprioritäten kaum verwenden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Types of prices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Arten von Preisen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>In Microsoft Dynamics 365, you can set the price of a product in three places:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In Microsoft Dynamics 365 können Sie den Preis eines Produkts an drei Stellen festlegen:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Directly on the product (base price)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Direkt auf dem Produkt (Basispreis)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In a sales price trade agreement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In einer Verkaufspreis-Handelsvereinbarung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>In a price adjustment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In einer Preisregulierung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The base price and trade agreement price are part of core Microsoft Dynamics 365, and are available even if you don't use Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Handelsvereinbarungs-Basispreis und der Basispreis sind Teil des zentralen Microsoft Dynamics 365 und sind verfügbar, wenn Sie nicht Einzelhandel verwenden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>The price adjustment functionality is available only in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Preisregulierungsfunktionen sind nur im Einzelhandel verfügbar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>The next section provides more information about each of these options for setting prices and explains how the options work together.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der nächste Abschnitt enthält weitere Informationen zu diesen Optionen für das Einrichten von Preisen und beschreibt, wie die Optionen zusammenarbeiten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Setting prices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preisfestlegung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Base price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Basispreis</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The easiest place to set the price for a product is directly on the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der einfachste Ort, um Preis für ein Produkt festzulegen ist direkt im Produkt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>The value that you set directly on a product is often referred to as the base price for the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Wert, den Sie direkt auf ein Produkt festsetzen, ist häufig als Basispreis für das Produkt gekennzeichnet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>You set the base price in the <bpt id="p1">**</bpt>Price<ept id="p1">**</ept> field on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab of the <bpt id="p3">**</bpt>Released product details<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sie legen den Basispreis auf dem Feld <bpt id="p1">**</bpt>Preis<ept id="p1">**</ept> auf der Registerkarte <bpt id="p2">**</bpt>Verkaufen<ept id="p2">**</ept> der Seite <bpt id="p3">**</bpt>Details für freigegebene Produkte<ept id="p3">**</ept> fest.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>The value that you enter is in the company currency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Wert, den Sie eingeben, ist in der Unternehmenswährung.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>By default, the price is for a quantity of 1 of the unit of measure (UoM) that is set in the <bpt id="p1">**</bpt>Unit<ept id="p1">**</ept> field on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab. The actual price per unit of a product is based on the UoM, the price quantity, and the currency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Standardmäßig ist der Preis für die Menge " 1 der Maßeinheit (UoM), die im Feld <bpt id="p1">**</bpt>Einheit<ept id="p1">**</ept> auf der Registerkarte <bpt id="p2">**</bpt>Verkaufen<ept id="p2">**</ept> festgelegt wird. Der tatsächliche Preis je Einheit eines Fertigprodukts basiert auf dem UoM, die Preismenge und die Währung.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If a product has one price for everyone, the base price offers the most efficient way to manage the price of that product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn ein Produkt einen Preis für den aufweist, bietet der Basispreis effizienteste Weise an, Preis dieses Produkts zu verwalten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Even if you use trade agreements to set prices, you might also set the base price on a product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Auch wenn Sie Handelsvereinbarungen zum Festlegen der Preise nutzen, können Sie auch den Basispreis auf einem Produkt festlegen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Then, if you don't use an <bpt id="p1">**</bpt>All<ept id="p1">**</ept> trade agreement, you have a fallback price that is used when no trade agreement applies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn Sie keine Handelsvereinbarung <bpt id="p1">**</bpt>Alle<ept id="p1">**</ept> verwenden, haben Sie einen Fallback-Preis, der verwendet wird, wenn keine Handelsvereinbarung gilt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>If a retail channel's currency differs from the company currency, the base price in that retail channel is determined by using currency conversion on the price that is set on the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn sich die Währung eines Einzelhandelskanals von der Unternehmenswährung unterscheidet, wird der Einzelhandelskanal-Basispreis ermittelt, indem Währungskonvertierung für den Preis verwendet, die für das Produkt festgelegt wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Although the price unit isn't a common retail scenario, the retail pricing engine supports it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Obgleich die Preiseinheit kein allgemeines Kleinszenario ist, unterstützt es das Einzelhandelspreismodul,</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>If the price unit is set to a value other than <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero), the price per unit equals Price ÷ Price unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn die Preiseinheit auf einen anderen Wert als <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (Null) festgelegt ist, ergibt der Preis pro Einheit Preis ÷ Preiseinheit.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>For example, if a product's price is $10.00, and the price unit is 50, the price for a quantity of 1 is $0.20 (= $10.00 ÷ 50).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn der Preis eines Produkts $ 10,00 ist und die Preiseinheit ist 50, ist der Preis für eine Menge von 1 ist $0,20 (= $10.00 ÷ 50).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Sales price trade agreement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verkaufspreis-Handelsvereinbarung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>By using the trade agreement journal, you can create sales price trade agreements for each product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mit der Handelsvereinbarungserfassung verwenden, können Sie Handelsvereinbarungen für jedes Produkt erstellen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>In Microsoft Dynamics 365, there are three customer scopes for sales price trade agreements: <bpt id="p1">**</bpt>Table<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Group<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>All<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In Microsoft Dynamics 365 gibt es drei Debitorenumfänge für Handelsvereinbarungen: <bpt id="p1">**</bpt>Tabelle<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Gruppe<ept id="p2">**</ept> und <bpt id="p3">**</bpt>Alle<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The customer scope determines the customers that a given sales price trade agreement applies to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Debitorenumfang bestimmt die Debitoren, die eine bestimmte Verkaufspreis-Handelsvereinbarung gilt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>A <bpt id="p1">**</bpt>Table<ept id="p1">**</ept> sales price trade agreement is for a single customer that is set directly on the trade agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eine Handelsvereinbarung zu Verkaufspreisen <bpt id="p1">**</bpt>Tabelle<ept id="p1">**</ept> gilt für einen einzelnen Debitor, der direkt in der Handelsvereinbarung festgelegt ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>This scenario isn't a typical retail business-to-consumer (B2C) scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dieses Szenario ist kein typisches Einzelhandels-Konsumenten-Szenario (B2C).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>However, if it occurs, the retail pricing engine uses <bpt id="p1">**</bpt>Table<ept id="p1">**</ept> trade agreements when it determines price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn es der Fall ist, verwendet das Einzelhandelspreismodul Handelsvereinbarungen <bpt id="p1">**</bpt>Tabelle<ept id="p1">**</ept>, wenn der Preis bestimmt wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>A <bpt id="p1">**</bpt>Group<ept id="p1">**</ept> sales price trade agreement is the type that is most often used with retail functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eine Handelsvereinbarung zu Verkaufspreisen <bpt id="p1">**</bpt>Gruppe<ept id="p1">**</ept> ist der Typ, der mit Kleinfunktionen häufig an das benutztesten ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Outside Retail, <bpt id="p1">**</bpt>Group<ept id="p1">**</ept> sales price trade agreements are for a simple customer group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Außerhalb des Einzelhandels sind <bpt id="p1">**</bpt>Gruppe<ept id="p1">**</ept> Handelsvereinbarungen für eine einfache Debitorengruppe.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>However, in Retail, the concept of a customer group has been extended so that it's a more generic retail price group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Allerdings ist im Einzelhandel das Konzept einer Debitorengruppe erweitert worden, damit er eine allgemeine Einzelhandelspreisgruppe ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>A price group can be linked to a retail channel, affiliation, loyalty program, or catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bei einer Preisgruppe kann einem Einzelhandelskanal, einer Zugehörigkeit, einem Treueprogramm oder einem Katalog zugeordnet werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>For detailed information about price groups, see the "Price groups" section earlier in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Detaillierte Informationen zu Preisgruppen finden Sie im Abschnitt "Preisgruppen" oben in diesem Thema.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>A trade agreement price is always used before the base price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ein Handelsvereinbarungs-Preis wird immer vor dem Basispreis verwendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Price adjustment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preisregulierung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>As the name implies, a price adjustment is used to modify the price that was either set directly on the product or set by using a trade agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wie der Name sagt, steht er für eine Preisregulierung und wird verwendet, um den Preis zu ändern, der entweder für die Gruppe direkt oder durch eine Handelsvereinbarung festgelegt wurde.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>A price adjustment can be used only to lower the price, not raise it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eine Preisregulierung kann verwendet werden, um nur den Preis zu senken, nicht zu erhöhen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>A price adjustment is the recommended way for retailers to create, track, and manage price markdowns for their products over time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eine Preisregulierung ist der empfohlene Weg für Einzelhändler, um Nachverfolgen zu erstellen und Preisabschläge für seine Produkte über die Zeit zu verwalten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>There are three types of price adjustments: percentage off, amount off, and price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Es gibt drei Typen Preisregulierungen: Prozentsatz, der Betrag und der Preis.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>A price adjustment of the percentage off or amount off type is always applied to a sale transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eine Preisregulierung des Prozentsatzes des Importprozesses oder Betrags auf dem Typ wird immer in einer Verkaufstransaktion angewendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>However, a price adjustment of the price type is applied only if the adjusted price is less than the price that was set by using the base price or trade agreement price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Es wird jedoch eine Preisregulierung des Preistyps angewendet, wenn der angepasste Preis kleiner ist als der Preis, der festgelegt wurde, indem der Handelsvereinbarungs-Preis oder der Basispreis erfasst wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Therefore, if the price that is set in a price adjustment is more than the unadjusted price, the price adjustment isn't used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn der Preis, der in eine Preisregulierung festgelegt ist, höher ist als der nicht angepasste Preis, wird die Preisregulierung nicht verwendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Determining price for a product in a transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bestimmen des Preises für ein Produkt in einer Buchung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>The calculation of the price and discount on a transaction uses the principle of finding the best price for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Berechnung des Preises und des Rabatts in einer Buchung verwendet das Prinzip des besten Findens für den besten Preis für den Debitor.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>According to this principle, if more than one price is found, the lowest price is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Entsprechend dieses Prinzip, wenn mehr als ein Preis gefunden wird, wird der niedrigste Preis verwendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Additionally, the combination of discounts that produces the largest discount amount for the whole transaction is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Darüber hinaus wird die Kombination von Rabatten, die den größten Rabattbetrag für die gesamte Buchung erzeugt, verwendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>In some cases, a smaller discount must be used on a single product, so that additional discounts can be applied to other products in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In einigen Fällen muss ein kleinerer Rabatt auf einem einzelnen Produkt verwendet werden, sodass zusätzliche Rabatte für andere Produkte in der Buchung angewendet werden können.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>The only exception to the principle of finding the best price for the customer is an option for mix-and-match least-expensive discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die einzige Ausnahme des Prinzips für den besten Preis für den Debitor fungiert in eine Option für wenig teure Rabatte des Angebots-Sortiments.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>This option enables least-expensive discounts that favor the retailer when products are selected and grouped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Diese Option ermöglicht wenig-teure Rabatte, die den Einzelhändler bevorzugen, wenn Produkte ausgewählt und gruppiert werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Therefore, when a transaction includes more products than are required to qualify for the least-expensive discount, the retail pricing engine selects the products that produce the smallest possible discount amount for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn eine Buchung mehr Produkte enthält, als benötigt werden, um einen Anspruch auf den günstigsten Rabatt zu erlangen, wählt das Einzelhandelspreismodul die Produkte aus, die einen möglichen Skontobetrag für den Debitor erstellen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The retail pricing engine returns three prices for every product: the base price, the trade agreement price, and the active price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Das Einzelhandelspreismodul gibt drei Preisen für jedes Produkt zurück: Basispreis, der aktive Handelsvereinbarungs-Preis und der aktive Preis.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>The base price is just the property on the product and is the same for everyone everywhere.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Basispreis ist nur die Eigenschaft im Produkt und entspricht dem gleichen überall.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>On the sales price trade agreement, if the <bpt id="p1">**</bpt>Find next<ept id="p1">**</ept> option is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>, the lowest price that is found for applicable sales price trade agreements is used as the trade agreement price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Auf der Verkaufspreis-Handelsvereinbarung wenn die Option <bpt id="p1">**</bpt>Weitersuchen<ept id="p1">**</ept> festgelegt wurde, wird der tiefste Preis auf <bpt id="p2">**</bpt>Ja<ept id="p2">**</ept> festgelegt, der für die gültige Artikelverkaufspreis-Handelsvereinbarungen gefunden wird, und als Handelsvereinbarungs-Preis verwendet wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Trade agreements can be found by using price groups or the <bpt id="p1">**</bpt>ALL<ept id="p1">**</ept> account code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Handelsvereinbarungen können gefunden werden, indm Sie Preisgruppen oder den Kontocode <bpt id="p1">**</bpt>ALLE<ept id="p1">**</ept> verwenden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Alternatively, trade agreements can be assigned directly to a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Alternativ können Handelsvereinbarungen direkt einem Debitor zugewiesen werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>If the <bpt id="p1">**</bpt>Find next<ept id="p1">**</ept> option is set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>, the first trade agreement price that is found is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn die Option <bpt id="p1">**</bpt>Weitersuchen<ept id="p1">**</ept> auf <bpt id="p2">**</bpt>Nein<ept id="p2">**</ept> festgelegt wurde, wird der erste Handelsvereinbarungs-Preis, der gefunden wird, verwendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>If no sales price trade agreements are found, then the trade agreement price is set equal to the base price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn keine Handelsvereinbarungen zu Verkaufspreisen enthalten sind, wird der Handelsvereinbarungs-Preis gleich dem Basispreis festgelegt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>The active price is calculated by taking the trade agreement price and applying the largest price adjustment that applies to the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der aktive Preis wird berechnet, indem der Handelsvereinbarungs-Preis genommen wird und auf die größte Preisanpassung angewendet wird, die für das Produkt gilt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>If no price adjustments are found, or if the calculated active price is more than the trade agreement price, the active price is set equal to the trade agreement price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn keine Preisregulierungen gefunden werden oder wenn die berechnete Preis höher ist als der Handelsvereinbarungs-Preis, wird der aktive Preis gleich dem Handelsvereinbarungs-Preis festgelegt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Remember that you can't raise the price of a product by using a price adjustment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bedenken Sie, dass Sie den Preis eines Produkts nicht erhöhen können, indem Sie eine Preisregulierung verwenden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>The applicable price adjustments can be found only by using price groups that are assigned to a channel, catalog, affiliation, or loyalty program.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die gültigen Preisregulierungen können Sie nur ermitteln, indem Preisgruppen verwendet werden, die einem Kanal, einem Katalog, einer Zugehörigkeit oder einem Treueprogramm zugewiesen werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Category price rules</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kategoriepreisregeln</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>The category price rules feature in Retail gives you an easy way to create new trade agreements for all the products in a category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Kategorie-Preisregelfunktion im Einzelhandel gibt Ihnen eine einfache Möglichkeit, neue Handelsvereinbarungen für alle Produkte in einer Kategorie zu erstellen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>This feature also lets you automatically find existing trade agreements for the products in the category and expire them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Diese Funktion kann auch automatisch vorhandene Handelsvereinbarungen für die Produkte in der Kategorie finden und sie ablaufen lassen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>When you select the option to expire existing trade agreements, the system creates a new trade agreement journal for the products in the category that have an active trade agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn Sie die Option auswählen, vorhandene Handelsvereinbarungen auslaufen zu lassen, erstellt das System eine neue Handelsvereinbarungserfassung für die Produkte in der Kategorie, die eine aktive Handelsvereinbarung haben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>However, the journal must be manually posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zuvor muss die Erfassung manuell gebucht werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Additionally, the category price rules can find existing trade agreements only if you're using the same price rule (that is, if you create a new price rule that uses the same category that was before).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Darüber hinaus können die Kategorie-Preisregeln vorhandene Handelsvereinbarungen finden, wenn Sie die gleiche Preisregel verwenden (das heißt, wenn Sie eine neue Preisregel erstellen, für die die gleiche Kategorie verwendet wird, die eingerichtet wurde).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>If you aren't using the same price rule, the existing trade agreements won't be expired.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn Sie dieselbe Preisregel verwenden, werden die vorhandenen Handelsvereinbarungen nicht ablaufen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>The prices can be increased or decreased by using the <bpt id="p1">**</bpt>Price rule<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Price basis<ept id="p2">**</ept> fields of the category price rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Preise können erhöht oder verringert werden, indem Sie die Felder <bpt id="p1">**</bpt>Preisregel<ept id="p1">**</ept> und <bpt id="p2">**</bpt>Preisgrundlage<ept id="p2">**</ept> der Kategorie-Preisregeln verwenden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>In the <bpt id="p1">**</bpt>Price rule<ept id="p1">**</ept> field, select the type of price change to use:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wählen Sie im Feld <bpt id="p1">**</bpt>Preisregel<ept id="p1">**</ept> aus, welchen Typ der Preisänderung zu verwenden ist:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source><bpt id="p1">**</bpt>Markup<ept id="p1">**</ept> – A percentage of the price basis is used to calculate the sales price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Aufschlag<ept id="p1">**</ept> - ein Prozentsatz der Preisbasis wird verwendet, um den Verkaufspreis zu berechnen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>For example, a product that costs 10.00 and sells for 15.00 has a markup of 50 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beispiel: Ein Produkt, das 10,00 kostet und für 15,00 verkauft wird, hat einen Aufschlag von 50 Prozent.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source><bpt id="p1">**</bpt>Margin<ept id="p1">**</ept> – A percentage of the sales price is used to calculate the amount of profit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Gewinn<ept id="p1">**</ept> - Ein Prozentsatz des Verkaufspreises, der verwendet wird, um den Gewinn zu berechnen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>For example, a product that costs 10.00 and sells for 15.00 has a margin of 33.3 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beispiel: Ein Produkt, das 10,00 kostet und für 15,00 verkauft wird, hat einen Gewinn von 33,3 Prozent.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source><bpt id="p1">**</bpt>Fixed amount<ept id="p1">**</ept> – An amount that is added to the price basis is used to calculate the sales price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Fester Betrag<ept id="p1">**</ept> - Ein Betrag, der der Preisbasis hinzugefügt wird, die verwendet wird, um den Verkaufspreis zu berechnen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>For example, a product that costs 10.00 and sells for 15.00 has a fixed amount of 5.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beispiel: Ein Produkt, das 10,00 kostet und für 15,00 verkauft wird, hat einen festen Betrag von 5,00.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>In the <bpt id="p1">**</bpt>Price basis<ept id="p1">**</ept> field, select the type of price to modify:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wählen Sie im Feld <bpt id="p1">**</bpt>Preisbasis<ept id="p1">**</ept> den Typ des zu ändernden Preises aus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source><bpt id="p1">**</bpt>Base cost<ept id="p1">**</ept> – The amount that the retailer paid to the supplier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Grundkosten<ept id="p1">**</ept> - Der Betrag, den der Einzelhändler an den Lieferanten zahlt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source><bpt id="p1">**</bpt>Base price<ept id="p1">**</ept> – The sales price before trade agreements and price adjustments are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Grundpreis<ept id="p1">**</ept> - Der Verkaufspreis, bevor Handelsvereinbarungen und Preisregulierungen angewendet werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source><bpt id="p1">**</bpt>Current price<ept id="p1">**</ept> – The sales price after trade agreements and price adjustments are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Aktueller Preis<ept id="p1">**</ept> - Der Verkaufspreis, nachdem Handelsvereinbarungen und Preisregulierungen angewendet werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>To easily update the prices of various products from different product categories, you can use the supplemental product categories together with the category price rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Um die Preise von verschiedenen Produkten und von verschiedenen Produktkategorien leicht zu aktualisieren, können Sie die ergänzenden Produktkategorien zusammen mit den Kategorie-Preisregeln verwenden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Best practices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Optimale Verfahren</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Microsoft SQL Server Express is often used for channel databases because of the cost (free).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server Express wird häufig für Kanaldatenbanken verwendet, um Kosten einzusparen (kostenlos).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Keep in mind that SQL Server Express has hardware limitations and limits on data size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beachten Sie, dass SQL Server Express Hardwareeinschränkungen und Grenzen auf Datenvolumen hat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>If you don't plan correctly, you can quickly reach the data size limits of SQL Server Express.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn Sie nicht ordnungsgemäß planen, können Sie die Datengrößenbeschränkungen von SQL Server Express schnell erreichen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>This consideration applies not only to pricing but also to other areas of the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Diese Überlegung gilt nicht nur der Preiskalkulation sondern auch auf andere Bereiche des Produkts auf.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Here are a few best practices that can help you reduce the size of your data:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nachfolgend sind einige Verfahren, die Ihnen beim Erfüllen der Auflagen, Größe zu reduzieren bei Ihren Daten, helfen kann:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>If you're using trade agreements, and your prices change, you should expire the old trade agreements by setting an end date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn Sie Handelsvereinbarungen verwenden, sollten Sie die alten Handelsvereinbarungen ablaufen lassen, indem Sie ein Enddatum festlegen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Over time, this approach helps reduce the number of trade agreements that are kept in channel databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Im Laufe der Zeit hilft dieser Ansatz, die Anzahl der Handelsvereinbarungen zu reduzieren, die in den Kanaldatenbanken aufbewahrt werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>It also helps reduce the amount of data that the price calculation algorithm must work with.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Er hilft zudem, die Datenmenge zu verringern, von denen der Herstellkostenkalkulationsalgorithmus mit arbeiten muss.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>If your prices vary by product variant, consider using the product base price as the price of the most common variant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn die Preise sich mit Nebenproduktvarianten unterscheiden, nehmen Sie den Produktbasispreis der allgemeinsten Variante.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Then use trade agreements only for the variant prices that are exceptions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nutzen Sie dann nur Handelsvereinbarungen für verschiedene Preise, die Ausnahmen sind.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>This approach helps reduce the number of trade agreement records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Durch diesen Ansatz können Sie die Anzahl der Handelsvereinbarungsdatensätze reduzieren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Because it's so easy to import data into Microsoft Dynamics 365, you might be tempted to import a trade agreement for every variant of every product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Da es so einfach ist, Daten in Microsoft Dynamics 365 zu importieren, könnten Sie versucht sein, für jede Variante jedes Produkts eine Handelsvereinbarung zu importieren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>However, that approach can produce many trade agreements that have the same value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Allerdings kann dieser Ansatz dazu führen, viele Handelsvereinbarungen zu produzieren, die denselben Wert besitzen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Therefore, it can needlessly increase the size of your data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Daher kann die Größe der Daten leicht erhöht werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Retail processes variant-specific prices in order from most specific to least specific.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Einzelhandel verarbeitet Varianten spezifische Preise von dem mit den meisten Angaben zu dem mit den wenigsten Angaben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>If a product dimension doesn't affect the price, you don't have to define trade agreements for it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn eine Produktdimension den Preis nicht beeinträchtigt, müssen Sie keine Handelsvereinbarungen definieren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>For example, a product is available in three colors and four sizes, but the price varies only by size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beispielsweise ist ein Produkt in drei Farben und vier Größen verfügbar, aber der Preis unterscheidet sich von Größe zu Größe.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>If you define a trade agreement for every variant, you create 12 records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn eine Handelsvereinbarung für jede Variante definieren wird, erstellen Sie 12 Datensätze.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Instead, you can define a trade agreement just for each size and leave the Color dimension blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stattdessen können Sie eine Handelsvereinbarung nur für jede Kombination von Größe definieren und das Farbdimensionsleerzeichen lassen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>In this case, you produce only four records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In diesem Fall erstellen Sie nur vier Datensätze.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Alternatively, if not every value of a dimension produces a different price, you can define one trade agreement for the product master and leave all product dimensions blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Falls nicht jeder Wert einer Dimension einen anderen Preis erzeugt, können Sie eine Handelsvereinbarung für den Produktmaster definieren und alle Produktdimensionen lassen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Then define a separate trade agreement just for each dimension value that produces a different price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Definieren Sie dann eine separate Handelsvereinbarung für jeden Dimensionswert, der einen anderen Preis erzeugt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>For example, if the XXL size has a higher price, but all other sizes have the same price, you require only two trade agreements: one for the product master and one for the XXL size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn beispielsweise die XXL-Größe einen höheren Preis hat, aber für alle anderen Größen haben Sie denselben Preis, müssen Sie nur zwei Handelsvereinbarungen haben: eine für den Produktmaster und eine für die XXL-Größe.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Prices that include tax vs. prices that exclude tax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preise, die Preise für Steuer enthalten und solche, die keine Steuer enthalten</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>When you set sales prices in Microsoft Dynamics 365, you don't specify whether the price value that you're setting includes or excludes tax.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn Sie Verkaufspreise in Microsoft Dynamics 365 festlegen, definieren Sie nicht, ob der Preis den Sie festlegen, Mehrwersteuer einschließt oder nicht.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>The value is just the price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Wert ist nur der Preis.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>However, the <bpt id="p1">**</bpt>Price includes sales tax<ept id="p1">**</ept> setting on retail channels lets you configure retail channels so that they either include or exclude tax from prices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Allerdings können Sie mit der Einstellung <bpt id="p1">**</bpt>Preis enthält Mehrwertsteuer<ept id="p1">**</ept> Einzelhandelskanälen so konfigurieren, sodass sie entweder Steuer von Preisen einbeziehen oder ausschließen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>This setting is set on the channel and can change even in a single company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Diese Einstellung wird für den Kanal festgelegt und kann auch in einem bestimmten Unternehmen ändern.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>If you work with both inclusive and exclusive types of tax, it's very important that you set prices correctly, because the total amount that the customer pays will change if the <bpt id="p1">**</bpt>Price includes sales tax<ept id="p1">**</ept> setting on the channel is changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn Sie mit den Arten der inklusiven und exklusive Steuern arbeiten, ist es für Sie für Preise ordnungsgemäß außerordentlich wichtig, da der Gesamtbetrag, der vom Debitor bezahlt wird, ändert, wenn die Einstellung <bpt id="p1">**</bpt>Preis enthält Mehrwertsteuer<ept id="p1">**</ept> im Kanal geändert wird.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Differences between retail pricing and non-retail pricing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Unterschiede zwischen der Festsetzung von Enzelhandelspreisen und Nicht-Einzelhandelpreiskalkulation</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>A single pricing engine is used to calculate retail prices across all channels: Call center, Retail store, and Online stores.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eine einzelne Modul-Preiskalkulation wird verwendet, um Einzelhandelspreise über alle Kanäle zu berechnen: Callcenter, auf Shop Lagermanagement und Onlineshops.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>This helps in enabling the unified commerce scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Das hilft bei der Aktivierung der einheitlichen Geschäftsszenarien.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Retail pricing is designed to work with retail entities instead of non-retail entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retailpreise wurde so entworfen, dass mit Retailentitäten anstelle der Nicht-Retailentitäten gearbeitet werden kann.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Specifically, it's designed to set prices by store, not by warehouse.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Speziell wurde diese so entworfen, dass Preise nach Filiale, nicht nach Lagerort festgelegt werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>The retail pricing engine doesn't support the following pricing features:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Das Einzelhandelsmodul unterstützt nicht die folgenden Preiskalkulationsfunktionen:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Setting price by using the Site and Warehouse storage dimensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Preisfestlegung mithilfe der Standort- und Lagerortlagerdimensionen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>Attribute-based pricing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Auf Attributen basierte Preiskalkulationskennung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Vendor discount pass-through</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kreditorenrabatt-Pass-Through</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>In addition, <bpt id="p1">**</bpt>only<ept id="p1">**</ept> the retail pricing engine supports the following pricing features:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Das Einzelhandelsmodul unterstützt zudem <bpt id="p1">**</bpt>nur<ept id="p1">**</ept> die folgenden Preiskalkulationsfunktionen:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>The price is based on product dimensions, in order from the most-specific variant price to the least-specific variant price to the product master price.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Preis wird auf Grundlage der Produktdimensionen im Auftrag der verschiedenen Preis von der spezifischsten Preisvariante bis zur am wenigsten spezifischen Preisvariante im Produktmaster-Preis festgelegt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>A price that is set by using two product dimensions (for example, Color and Size) is used before a price that is set by using only one product dimension (for example, Size).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ein Preis, der festgelegt wird, indem zwei Produktdimensionen verwendet werden (beispielsweise Gesamtlayout, Farbe und Größe), die vor einem Preis verwendet werden, der festgelegt wird, indem nur eine Produktdimension verwendet wird (beispielsweise Gesamtlayout, Größe).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>The same price group can be used to control pricing and discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Dieselbe Preisgruppe kann verwendet werden, um Preiskalkulation und Rabatte zu steuern.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Pricing API enhancements</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Preisberechnung für API-Erweiterungen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Price is one of the most important factors that govern the buying decisions of many customers, and many customers compare prices on various sites before they make a purchase.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Der Preis ist einer der wichtigsten Faktoren, die bei der Einkaufsentscheidung vieler Kunden entscheidend sind. Viele Kunden vergleichen Preise auf verschiedenen Websites, bevor sie einen Kauf tätigen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>To help guarantee that they provide competitive prices, retailers keep a close eye on their competitors and often run promotions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Zur Sicherstellung dass sie konkurrenzfähige Preise bereitstellen, behalten Einzelhändler ihre Konkurrenten genau im Blick und führen oft Verkaufsförderungsmaßnahmen durch.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Therefore, to help these retailers attract customers, it's very important that product search, the browse feature, lists, and the product details page show the most accurate prices.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Um diese Einzelhändler bei ihrer Kundengewinnung zu unterstützen, ist es sehr wichtig, dass die Produktsuche, die Funktion fürs Durchsuchen und die Seite für Produktdetails die genauesten Preise anzeigen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>In an upcoming release of Retail, the <bpt id="p1">**</bpt>GetActivePrices<ept id="p1">**</ept> application programming interface (API) will return prices that include simple discounts (for example, single-line discounts that don't depend on other items in the cart).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">In einer bevorstehenden Version von Retail, wird die Anwendungsprogrammierungsschnittstelle (API) <bpt id="p1">**</bpt>GetActivePrices<ept id="p1">**</ept> Preise zurückgeben, die einfache Rabatte enthalten (z. B. Einzelpositionsrabatte, die nicht von anderen Artikeln im Warenkorb abhängen).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>In this way, the prices that are shown are close to the actual amount that customers will pay for items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Auf diese Weise sind die Preise, die angezeigt werden, dem tatsächlichen Betrag ziemlich nahe, den Kunden für Artikel bezahlen werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>This API will include all the types of simple discounts: affiliation-based, loyalty-based, catalog-based, and channel-based discounts.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese API wird alle Typen einfacher Rabatte umfassen: zugehörigkeitsbasierte, treuebasierte, katalogbasierte sowie kanalbasierte Rabatte.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Additionally, the API will return the names and validity information for the applied discounts, so that retailers can provide a more detailed description of the price and create a sense of urgency if the discount's validity will expire soon.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Darüber hinaus wird die API die Namen und Gültigkeitsinformationen für die angewendeten Rabatte zurückgeben, sodass Einzelhändler eine ausführlichere Beschreibung des Preises bereitstellen können und einen Eindruck der Dringlichkeit vermitteln können, wenn die Gültigkeit des Rabatts bald abläuft.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>