<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="optimal-combination-overlapping-discounts.md" target-language="de-DE">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>optimal-combination-overlapping-discounts.e4f3cd.e327f652855f898e50f1dd853ae20f3a0ff41d9e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>e327f652855f898e50f1dd853ae20f3a0ff41d9e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\optimal-combination-overlapping-discounts.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ermittelt die optimale Kombination von überlappenden Rabatten</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn Rabatte überlappen, müssen Sie die Kombination von Rabatten überlappenden bestimmen, die Buchungssumme niedrigsten oder höchsten den Rechnungsrabatt erzeugen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common 'Buy 1, get 1 X percent off' (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn der Rabattbetrag gemäß dem Preis der gekauften Produkte schwankt, wie bei üblichen Aktionen wie „kaufen 1 günstiger erhalten“ (BOGO), wird dieser Prozess ein Thema der kombinatorischen Optimierung.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ermittelt die optimale Kombination von überlappenden Rabatten</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn Rabatte überlappen, müssen Sie die Kombination von Rabatten überlappenden bestimmen, die Buchungssumme niedrigsten oder höchsten den Rechnungsrabatt erzeugen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common "Buy 1, get 1 X percent off" (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn der Rabattbetrag gemäß dem Preis der gekauften Produkte schwankt, wie bei üblichen Aktionen wie „kaufen 1 günstiger erhalten“ (BOGO), wird dieser Prozess ein Thema der kombinatorischen Optimierung.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This article applies to Microsoft Dynamics AX 2012 R3 with KB 3105973 (released November 2, 2015) or later, and to Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dieser Artikel gilt für Microsoft Dynamics AX 2012 R3 mit KB 3105973 (veröffentlicht am 2. November 2015) oder höher und für Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To determine the combination overlapping discounts to apply in a timely manner, we have introduced a method for applying overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Damit die Kombination sich überschneidender Rabatte zeitnah angewendet werden kann, haben wir eine Methode zum Anwenden sich überschneidender Rabatte eingeführt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>We call this new method <bpt id="p1">**</bpt>marginal value ranking<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Es erhalten diese neue Methode angezeigt <bpt id="p1">**</bpt>Schwellenwertklassifizierung<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Marginal value ranking is used when the time that is required in order to evaluate the possible combinations of overlapping discounts exceeds a threshold that is configurable on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Schwellenwertklassifizierung wird verwendet, wenn die Zeit, die erforderlich ist, um die möglichen Kombinationen von sich überschneidenden Rabatten zu bewerten, einen Schwellenwert überschreitet, der auf der Seite <bpt id="p1">**</bpt>Einzelhandelsparameter<ept id="p1">**</ept> konfigurierbar ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In the marginal value ranking method, a value is calculated for each overlapping discount by using the discount's value on the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In der Schwellenwertklassifizierungsmethode wird ein Wert für jeden überlappenden Rabatt berechnet, indem der Wert des Rabatts auf den freigegebenen Produkten verwendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The overlapped discounts are then applied from the highest relative value to the lowest relative value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die überlappenden Rabatte werden dann dem höchsten relativen Wert der niedrigste relativen Wert angewendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For details about the new method, see the "Marginal value" section, later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Einzelheiten über die neue Methode, lesen Sie den Abschnitt "Schwellenwert", später in diesem Artikel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Marginal value ranking isn't used when the discount amounts for a product aren't affected by another product in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Schwellenwertklassifizierung wird nicht verwendet, wenn Skontobeträgen für das Produkt nicht durch unterschiedliche Produkt in der Buchung betroffen sind.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For example, this method isn't used for two simple discounts, or for a simple discount and a single product quantity discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beispielsweise kann diese Methode nicht für zwei einfache Rabatte oder einen einfachen Rabatt und einen einzelnen Produktmengenrabatt verwendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Discount examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rabattbeispiele</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can create an unlimited number of retail discounts on a common set of products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sie können eine unbegrenzte Anzahl an Einzelhandelsrabatten für eine allgemeines Set an Produkten erstellen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>However, because there is no limit, performance issues can occur when you try to calculate the discounts that should be used on the various products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Da jedoch kein Limit festgelegt ist, können Leistungsprobleme auftreten, wenn Sie versuchen, die Rabatte zu berechnen, die auf den verschiedenen Produkten verwendet werden sollen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The following examples illustrate this issue in more detail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die folgenden Beispiele veranschaulichen dieses Problem genauer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In example 1, we start with two products and two overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In Beispiel 1 beginnen, wir mit zwei Produkten und zwei überlappenden Rabatten.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Then, in example 2, we show how the issue evolves as more products are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Im Beispiel 2, zeigen wir, wie das Problem, entwickelt für weitere Produkte hinzugefügt werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Example 1: Two products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beispiel 1: Zwei beiden Rabatte und Produkte</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>In this example, two products are required in order to qualify for each discount, and the discounts can't be combined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In diesem Beispiel wurden zwei Produkte erforderlich, das für jeden Rabatt zu erlangen, und Rabatte können nicht zusammengefasst werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The discounts in this example are <bpt id="p1">**</bpt>Best price<ept id="p1">**</ept> discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die in Rabatte diesem Beispiel sind <bpt id="p1">**</bpt>Bester Preis<ept id="p1">**</ept> Rabatte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Both products qualify for both discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Beide Produkte qualifizieren der beiden Rabatte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Here are the two discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Hierbei gelten die beiden Rabatte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Example of two Best price discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Beispiel zweiter bester Preisrabatte</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>For any two products, the better of these two discounts depends on the prices of the two products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Bei zwei Produkten hängt der bessere der beiden Rabatte vom Preis der beiden Produkte ab.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>When the price of both products is equal or almost equal, discount 1 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn der Preis beider Produkte oder gleich fast gleich ist besser, Skonto 1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>When the price of one product is significantly less than the price of the other product, discount 2 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn der Preis aus einem Produkt bei geringer als der anderen Preis des Produkts ist besser, Rabatt ist 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Here is the mathematical rule for evaluating these two discounts against each other.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Hier ist die mathematischen Regel zur Abwägung der beiden Rabatte gegeneinander.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Rule for evaluating the discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Regel für die Bewertung der Rabatte</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>When the price of product 1 is equal to two-thirds of the price of product 2, the two discounts are equal.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Wenn der Preis von Produkt 1 gleich Zweidrittel des Preises von Produkt 2 beträgt, sind die beiden Rabatte identisch.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In this example, the effective discount percentage for discount 1 varies from a few percent (when the prices of the two products are far apart) to a maximum of 25 percent (when the two products have the same price).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In diesem Beispiel ist der zum Diskont effektive Rabattprozentsatz 1 von einigen Prozent (wenn die Preise der beiden Produkte weites getrennt sind), bis zu maximal 25 Prozent (wenn die Produkte zwei denselben Preis haben).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The effective discount percentage for discount 2 is fixed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Rabattprozentsatz für den Skonto 2 ist fest.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>It's always 20 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Es ist immer 20 Prozent.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Because the effective discount percentage for discount 1 has a range that can be more than or less than discount 2, the best discount depends on the prices of the two products that must be discounted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Da der gültigen Rabattprozentsatz für Skonto 1 einen Bereich hat, der mehr als Rabatt oder kleiner als 2 sein kann, hängt der beste Rabatt von Preisen der beiden Produkte aus, die für den Rabatt gewährt werden müssen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In this example, the calculation is completed quickly, because only two discounts are applied on only two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In diesem Beispiel wird die Berechnung schnell ausgefüllt, da nur beiden Rabatte auf nur zwei Produkten angewendet werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>There are only two possible combinations: one application of discount 1 or one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Es gibt lediglich zwei mögliche Kombinationen: eine Bewerbung der Anwendung des Rabatts 1 oder einen Rabatt. 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>There are no permutations to calculate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Es sind keine zuzuteilenden Belastungen vorhanden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The value of each discount is calculated by using both products, and the best discount is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Wert jedes Rabatt wird berechnet, indem das sowohl Produkte verwendet, und der beste Rabatt wird verwendet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Example 2: Four products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Beispiel 2: Vier beiden Rabatte und Produkte</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Next, we will use four products and the same two discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Danach verwenden Sie vier Produkte und dieselben beiden Rabatte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>All four products qualify for both discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Alle vier Produkte qualifizieren der beiden Rabatte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>There are twelve possible combinations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Es gibt zwölf mögliche Kombinationen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>In the end, two discounts will be applied to the transaction in one of three combinations: two applications of discount 1, two applications of discount 2, or one application of discount 1 and one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Am Ende der Buchung werden beiden Rabatte auf drei verschiedene Kombinationen verwendet: Anwendungen zwei von Skonto 1, zwei Bewerbungen der Anwendung des Rabatts 2 oder einer der Anwendung des Rabatts 1 und einer von Rabatt. 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To illustrate the possible combinations, we will look at two different sets of four products that have different prices:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Um die möglichen Kombinationen zum Demonstrieren, beachten Sie zwei verschiedene Gruppen der Produkte die vier verschiedene Preise haben:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>All four products have the same price, $15.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Alle vier Produkte denselben Preis haben, €15,00.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In this case, the best discount combination is two applications of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In diesem Fall ist die beste Rabattkombination zwei Bewerbungen von Rabatt. 1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Two products will be full price, and two will be 50 percent off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zwei Produkte sind voller Preis, und sind zwei heruntergesetzt 50 Prozent.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The discounted total for the transaction is $45 (15 + 15 + 7.50 + 7.50), which is $15 (25 percent) off the undiscounted total of $60.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die rabattierte Summe für die Buchung ist €45 (15 + 15 + 7,50 + 7,50), die €15 (25 Prozent) die zur Abrundung der nicht-rabattierten Summe von €60 ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Discount 2 is only $12 (20 percent).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skonto 2 ist nur €12 (20 Prozent).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Two products are $20 each, one product is $15, and one product is $5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zwei Produkte sind €20 je, ist ein Produkt €15, und das Produkt ist €5.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In this case, the best discount combination is one application of discount 2 and one application of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In diesem Fall ist die beste Rabattkombination eine Bewerbung der Anwendung des Rabatts 2 und einer erweiterten Rabatts. 1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The following tables illustrates the discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die folgenden Tabellen wird gezeigt Rabatte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>To read the tables, use one product from a row and one product from a column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Um die Tabellen gelesen, verwenden Sie ein Produkt aus einer Zeile und ein Produkt aus einer Spalte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For example, in the table for discount 1, when you combine the two $20 products, you get $10 off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In der Tabelle für Skonto 1, wenn Sie mit den beiden €20 Produkte kombinieren, werden Sie bei €10 ab.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the table for discount 2, when you combine the $15 product and the $5 product, you get $4 off.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">In der Tabelle für Skonto 2, wenn Sie mit den €15 Produkt und dem €5 Produkt kombinieren, erhalten Sie €4 Rabatt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Example that uses four products for the same two discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Beispiel, das vier Produkte für dieselben zwei Rabatte verwendet</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>First, we find the largest discount that is available from any two products by using either discount.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Zunächst suchen wir den höchsten Rabatt, der für einen der beiden Produkte verfügbar ist, in dem wir einen der Rabatte anwenden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The two tables show the discount amount for all combinations of the two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die beiden Tabellen zeigen den Rabattbetrag für alle Kombinationen der beiden Produkte angezeigt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The shaded portions of the tables represent either cases where a product is paired with itself, which we can't do, or a reverse pairing of two products that produces the same discount amount and can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die schattierten Teile der Tabellen finden jeden Fälle, in denen ein Produkt mit dem zugeordnet ist, das von uns nicht ausführen können, oder ein Rückzuordnen zweier Produkten dar, weshalb dieselbe Rabattbetrag hergestellt und ignoriert werden kann.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>By looking at the tables, you can see that discount 1 for the two $20 items is the largest discount that is available for either discount on all four products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Durch Festlegen der Tabellen einmal genauer anschauen, werden Sie sehen, dass Skonto 1 für die zwei €20 Artikel der größten Rabatt ist, für jeden der Rabatt auf alle vier Produkte verfügbar ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>(This discount is highlighted in green in the first table.) That leaves only the $15 product and the $5 product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Dieser Rabatt wird in grün in der ersten Tabelle. Markieren) Dadurch lassen nur das Produkt €15 und das Produkt €5.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>By looking at the two tables again, you can see that, for these two products, discount 1 gives a $2.50 discount, whereas discount 2 gives a $4 discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wenn Sie erneut die beiden Tabellen einmal genauer anschauen, werden Sie sehen, dass, für diese beiden Produkte, Skonto 1 einen Rabatt €2,50 gibt, für Skonto 2 einen Rabatt €4 gibt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Therefore, we select discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Daher wird Skonto 2 aus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The total discount is $14.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Rechnungsrabatt beträgt €14.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>To make this discussion easier to visualize, here are two additional tables that show the effective discount percentage for all possible two-product combinations for both discount 1 and discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Um diese Diskussion zu vereinfachen visualisiert werden, sollten Sie hier zwei zusätzliche Tabellen die der eigentliche Rabattprozentsatz für alle möglichen Zwei-Produktkombinationen für Skonto 1 Skonto 2 und anzeigen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Only half the list of combinations is included, because, for these two discounts, the order in which the two products are put into the discount doesn't matter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nur ist Hälfte Liste mit Kombinationen eingeschlossen, weil, für diese beiden Rabatte, den Auftrag, in der zwei die Produkte in den Rabatt angewendet werden, noch ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The highest effective discount (25 percent) is highlighted in green, and the lowest effective discount (10 percent) is highlighted in red.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Der höchste effektive Rabatt (25 Prozent) wird in grün und niedrigsten im tatsächlichen Rabatt (10 Prozent) markiert wird rot hervorgehoben.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Effective discount percentage for all two-product combinations for both discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Effektiver Rabattprozentsatz für alle Zwei-Produkt-Kombinationen für beide Rabatte</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>When prices vary, and two or more discount compete, the only way to guarantee the best combination of discounts is to evaluate both discounts and compare them.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Wenn Preise variieren, und zwei oder mehr Rabatte miteinander konkurrieren, besteht die einzige Möglichkeit, die beste Rabattkombination zu garantieren, darin, beide Rabatte zu bewerten und miteinander zu vergleichen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Total possible combinations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Insgesamt mögliche Kombinationen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section continues the example from the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dieser Abschnitt wird das beispielsweise von vorherigen Abschnitt fort.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>We will add more products and another discount, and see how many combinations must be calculated and compared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Es können weitere Produkte und einen anderen Rabatt hinzu und finden, wie viele Kombinationen berechnet und verglichen werden müssen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The following table shows the number of possible discount combinations as the product quantity increases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">In der folgenden Tabelle wird die Anzahl für mögliche Rabattkombinationen als die Produktmengenerhöhungen angezeigt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>The table shows what happens both when there are two overlapping discounts, as in the previous example, and when there are three overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die Tabelle ist angegeben, was einerseits, wenn zwei überlappende Rabatte gibt, wie im vorherigen Beispiel erfolgt, und wenn es drei überlappende Rabatte gibt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The number of possible discount combinations that must be evaluated soon exceeds what even a fast computer can calculate and compare quickly enough to be acceptable for retail transactions.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Die Anzahl für mögliche Rabattkombinationen, die demnächst ausgewertet werden müssen, überschreitet, was auch ein Computer schneller berechnen sowie Vergleichen kann schnell genug, um für Einzelhandelstransaktionen akzeptiert werden sollen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Number of possible discount combinations as the product quantity increases</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Anzahl für mögliche Rabattkombinationen bei Erhöhung der Produktmenge</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>When even larger quantities or more overlapping discounts are applied, the total number of possible discount combinations quickly goes into the millions, and the time that is required in order to evaluate and select the best possible combination quickly becomes noticeable.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Werden sogar größere Mengen oder mehr sich überschneidende Rabatte angewendet, geht die gesamte Anzahl möglicher Rabattkombinationen schnell in die Millionen. Und die Zeit, die erforderlich ist, die bestmögliche Kombination zu bewerten und auszuwählen, wird schnell spürbar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Some optimizations have been done in the retail price engine to reduce the total number of combinations that must be evaluated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Einige Optimierungen sind im Kleineinzelhandelspreismodul fertig, aktualisiert die Gesamtanzahl von Kombinationen zu reduzieren, die überprüft werden müssen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>However, because the number overlapping discounts and the quantities in a transaction aren't limited, a large number of combinations will always have to be evaluated whenever there are overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Da jedoch die überlappenden Rabatte der Nummer und Mengen in einer Buchung nicht eingeschränkt werden, müssen mehrere Kombinationen immer ausgewertet werden, sobald sich überlappende Rabatte gibt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This issue is the issue that the marginal value ranking method addresses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dieses Problem wird der Abgang die Schwellenwertklassifizierungs-Methodenadressen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Marginal value method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Schwellenwertmethode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>To resolve the issue of an exponentially increasing number of combinations that must be evaluated, an optimization exists that calculates the value per shared product of each discount on the set of products that two or more discounts can be applied to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Um den Abgang einer exponential zunehmenden Anzahl von Kombinationen die Behebung ausgewertet werden müssen, ist eine Optimierung die den Wert pro freigegebenes Produkt jedes Rabatts im Satz von Produkten berechnet die zwei oder mehr Rabatte angewendet werden kann.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>We refer to this value as the <bpt id="p1">**</bpt>marginal value<ept id="p1">**</ept> of the discount for the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Wir bezeichnen diesen Wert als <bpt id="p1">**</bpt>Schwellenwert<ept id="p1">**</ept> des Rabatts für die freigegebene Produkte angezeigt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>The marginal value is the average per product increase in the total discount amount when the shared products are included in each discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Der Schwellenwert ist der Durchschnitt pro Produkterhöhung im freigegebenen Gesamtrabattbetrag, wenn die Produkte in den Rabattzeitraum einbezogen werden sollen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The marginal value is calculated by taking the total discount amount (DTotal), subtracting the discount amount without the shared products (DMinus<ph id="ph1">\\</ph> Shared), and dividing that difference by the number of shared products (ProductsShared).</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Der Schwellenwert wird berechnet, indem der Gesamtrabattbetrag (DTotal), den Rabattbetrag ohne die freigegebene Produkte (DMinus<ph id="ph1">\\</ph>Shared) abgezogen, und die Differenz von der Anzahl von freigegebenen Produkten (ProductsShared) geteilt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Formula for calculating marginal value</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Formel für die Berechnung des Schwellenwerts</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>After the marginal value of each discount on a shared set of products is calculated, the discounts are applied to the shared products in order, exhaustively, from highest marginal value to lowest marginal value.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Nachdem der Schwellenwert eines jeden Rabatts auf einem freigegebenen Produktsatz berechnet wurde, werden die Rabatte auf die freigegebenen Produkten angewendet, und zwar in der Reihenfolge vom höchsten Schwellenwert bis zu niedrigsten Schwellenwert.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For this method, all remaining discount possibilities aren't compared every time after a single instance of a discount is applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bei dieser Methode werden alle restlichen Rabattmöglichkeiten nicht jedes Mal verglichen, nachdem eine einzelne AOS-Instanz einen Rabatt angewendet wurde.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Instead, the overlapping discounts are compared one time and then applied in order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stattdessen werden einmal verglichen überlappenden die Rabatte angewendet und dann im Auftrag.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>No additional comparisons are done.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Keine weiteren Vergleiche durchgeführt werden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>You can configure the threshold to switch to the marginal value method on the <bpt id="p1">**</bpt>Discount<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sie können den Schwellenwert konfigurieren, die der auf der Schwellenwertmethode <bpt id="p1">**</bpt>Rabatt<ept id="p1">**</ept> Registerkarte der <bpt id="p2">**</bpt>Einzelhandelsparameter<ept id="p2">**</ept> Seite zu wechseln.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>The acceptable time to calculate the total discount varies across retail industries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Die akzeptierte Zeit, den Rechnungsrabatt zu berechnen variiert zu Einzelhandel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>However, this time generally falls in the range of tens of milliseconds to one second.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Allerdings liegt diese Zeit im Allgemeinen im Bereich der zehnten Millisekunden auf einer Sekunde.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>