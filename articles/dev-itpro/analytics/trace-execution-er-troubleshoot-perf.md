<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="trace-execution-er-troubleshoot-perf.md" target-language="de-DE">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>trace-execution-er-troubleshoot-perf.773b92.aa71db2752889bc905c22bab1cf2fa46d7ee07c7.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>aa71db2752889bc905c22bab1cf2fa46d7ee07c7</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>67d00b95952faf0db580d341249d4e50be59119c</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\trace-execution-er-troubleshoot-perf.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Trace execution of ER format to troubleshoot performance issues</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ausführung des EB-Formats nachverfolgen, um Leistungsprobleme zu behandeln</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to use the performance trace feature in Electronic reporting (ER) to troubleshoot performance issues.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dieses Thema bietet Informationen darüber, wie die Leistungsnachverfolgungsfunktion in der Elektronischen Berichterstellung (EB) verwendet werden kann, um Leistungsprobleme zu behandeln.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Trace the execution of ER formats to troubleshoot performance issues</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">Ausführung von EB-Formaten nachverfolgen, um Leistungsprobleme zu behandeln</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Im Rahmen des Prozesses, Elektronische Berichterstellungs-(EB)-Konfigurationen zu entwerfen, um elektronische Dokumente zu generieren, definieren Sie die Methode, mit der Daten von Microsoft Dynamics 365 for Finance and Operations abgerufen werden und in der Ausgabe, die generiert wird, eingegeben werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die EB-Leistungsablaufverfolgungfunktion hilft dabei, die Zeit und Kosten zu verringern, die durch das Sammeln der Details der EB-Formatausführung und bei deren Verwendung zur Behandlung von Leistungsproblemen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dieses Tutorial bietet Richtlinien dazu, wie Leistungsnachverfolgungen für ausgeführte EB-Formate in Finance and Operations gewonnen werden und wie die Informationen aus diesen Nachverfolgungen zur Verbesserung der Leistung verwendet werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Voraussetzungen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To complete the examples in this tutorial, you must have the following access:</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Um die Beispiele in diesem Tutorial abzuschließen, müssen Sie den folgenden Zugriff haben:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Access to Finance and Operations for one of the following roles:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Zugriff auf Finance and Operations für eine der folgenden Rollen:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Entwickler für elektronische Berichterstellung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Funktionaler Berater für elektronische Berichterstellung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Systemadministrator</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Zugriff auf die Instanz des Regulatory Configuration Service (RCS), der für denselben Mandanten wie Finance and Operations bereitgestellt wurde, für eine der folgenden Rollen:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Entwickler für elektronische Berichterstellung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Funktionaler Berater für elektronische Berichterstellung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Systemadministrator</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You must also download and locally store the following files.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie müssen auch die folgenden Dateien herunterladen und lokal speichern.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>File</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Datei</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Content</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Inhalt</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Performance trace model.version.1</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Leistungsnachverfolgung model.version.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">[</bpt>Sample ER data model configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>Beispiel-EB-Datenmodell-Konfiguration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Performance trace metadata.version.1</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Leistungsnachverfolgung metadata.version.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">[</bpt>Sample ER metadata configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>Beispiel-EB-Metadatenkonfiguration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Performance trace mapping.version.1.1</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Leistungsnachverfolgung mapping.version.1.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">[</bpt>Sample ER model mapping configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>Beispiel-EB-Modellzuordnungskonfiguration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Performance trace format.version.1.1</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Leistungsnachverfolgung format.version.1.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt>Sample ER format configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>Beispiel-EB-Formatkonfiguration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Configure ER parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Parameter der elektronischen Berichterstellung konfigurieren</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jede EB-Leistungsablaufverfolgung, die in Finance and Operations generiert wird, wird als Anhang des Ausführungsprotokoll-Datensatzes gespeichert.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The Document management (DM) framework of Finance and Operations is used to manage these attachments.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Das Dokumentenverwaltungs-(DM)-Framework von Finance and Operations wird verwendet, um diese Anhänge zu verwalten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie müssen EB-Parameter im Voraus konfigurieren, um den DM-Dokumenttyp anzugeben, der verwendet werden soll, um Leistungsnachverfolgungen anzufügen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In Finance and Operation, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">In Finance and Operation im Arbeitsbereich <bpt id="p1">**</bpt>Elektronische Berichterstellung<ept id="p1">**</ept> wählen Sie <bpt id="p2">**</bpt>Elektronische Berichterstellungsparameter<ept id="p2">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wählen Sie anschließend auf der Seite <bpt id="p1">**</bpt>Elektronische Berichterstellungsparameter<ept id="p1">**</ept> unter der Registerkarte <bpt id="p2">**</bpt>Anhänge<ept id="p2">**</ept> im Feld <bpt id="p3">**</bpt>Andere<ept id="p3">**</ept> den DM-Dokumenttyp aus, der für Leistungsnachverfolgungen zu verwenden ist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Electronic reporting parameters page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Elektronische Berichterstellungsparameterseite in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Um im Suchfeld <bpt id="p1">**</bpt>Andere<ept id="p1">**</ept> verfügbar zu sein, muss ein DM-Dokumenttyp in folgender Weise auf der Seite <bpt id="p2">**</bpt>Dokumenttypen<ept id="p2">**</ept> konfiguriert sein (<bpt id="p3">**</bpt>Organisationsverwaltung <ph id="ph1">\&gt;</ph> Dokumentenverwaltung <ph id="ph2">\&gt;</ph> Dokumenttypen<ept id="p3">**</ept>):</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Klasse:<ept id="p1">**</ept> Datei anfügen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Gruppe:<ept id="p1">**</ept> Datei</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Document types page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dokumenttypenseite in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Der ausgewählte Dokumenttyp muss in jedem Unternehmen der aktuellen Finance and Operations-Instanz verfügbar sein, da DM-Anhänge unternehmensspezifisch sind.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Configure RCS parameters</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">RCS-Parameter konfigurieren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">EB-Leistungsnachverfolgungen, die in Finance and Operations generiert werden, werden in RCS zur Analyse importiert, indem der EB-Format-Designer und der EB-Zuordnungs-Designer verwendet wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Da EB-Leistungsnachverfolgungen als Anlagen des Ausführungsprotokoll-Datensatzes gespeichert werden, der dem EB-Format zugeordnet ist, müssen Sie RCS-Parameter im Voraus konfigurieren, um den DM-Dokumenttyp anzugeben, der verwendet werden soll, um Leistungsablaufverfolgungen anzufügen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the instance of RCS that has been provisioned for your company, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">In der Instanz von RCS, der für Ihr Unternehmen im Arbeitsbereich <bpt id="p1">**</bpt>Elektronische Berichterstellung<ept id="p1">**</ept> bereitgestellt wurde, wählen Sie <bpt id="p2">**</bpt>Elektronische Berichterstellungsparameter<ept id="p2">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Wählen Sie anschließend auf der Seite <bpt id="p1">**</bpt>Elektronische Berichterstellungsparameter<ept id="p1">**</ept> unter der Registerkarte <bpt id="p2">**</bpt>Anhänge<ept id="p2">**</ept> im Feld <bpt id="p3">**</bpt>Andere<ept id="p3">**</ept> den DM-Dokumenttyp aus, der für Leistungsnachverfolgungen zu verwenden ist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Electronic reporting parameters page in RCS</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">Seite der elektronischen Berichterstellungsparameter in RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Um im Suchfeld <bpt id="p1">**</bpt>Andere<ept id="p1">**</ept> verfügbar zu sein, muss ein DM-Dokumenttyp in folgender Weise auf der Seite <bpt id="p2">**</bpt>Dokumenttypen<ept id="p2">**</ept> konfiguriert sein (<bpt id="p3">**</bpt>Organisationsverwaltung <ph id="ph1">\&gt;</ph> Dokumentenverwaltung <ph id="ph2">\&gt;</ph> Dokumenttypen<ept id="p3">**</ept>):</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>Klasse:<ept id="p1">**</ept> Datei anfügen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>Gruppe:<ept id="p1">**</ept> Datei</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Design an ER solution</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">Eine EB-Lösung entwerfen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Nehmen Sie an, Sie haben mit dem Entwurf einer neuen EB-Lösung begonnen, um einen neuen Bericht zu generieren, der Kreditorentransaktionen darstellt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Currently, you can find the transactions for a selected vendor on the <bpt id="p1">**</bpt>Vendor transactions<ept id="p1">**</ept> page (go to <bpt id="p2">**</bpt>Account payable <ph id="ph1">\&gt;</ph> Vendors <ph id="ph2">\&gt;</ph> All vendors<ept id="p2">**</ept>, select a vendor, and then, on the Action Pane, on the <bpt id="p3">**</bpt>Vendor<ept id="p3">**</ept> tab, in the <bpt id="p4">**</bpt>Transactions<ept id="p4">**</ept> group, select <bpt id="p5">**</bpt>Transactions<ept id="p5">**</ept>).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Aktuell können Sie die Transaktionen für einen ausgewählten Kreditor auf der Seite <bpt id="p1">**</bpt>Kreditorenbuchungen<ept id="p1">**</ept> suchen (wechseln Sie zu <bpt id="p2">**</bpt>Kreditor <ph id="ph1">\&gt;</ph> Kreditoren <ph id="ph2">\&gt;</ph> Alle Kreditoren<ept id="p2">**</ept>, wählen Sie einen Kreditor aus, und dann, im Aktivitätsbereich unter der Registerkarte <bpt id="p3">**</bpt>Kreditor<ept id="p3">**</ept> in der Gruppe <bpt id="p4">**</bpt>Transaktionen<ept id="p4">**</ept> wählen Sie <bpt id="p5">**</bpt>Transaktionen<ept id="p5">**</ept>).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>However, you want to have all vendor transaction at the same time in one electronic document in XML format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie möchten jedoch alle Kreditorenbuchungen gleichzeitig in einem elektronischen Dokument im XML-Format haben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese Lösung besteht aus mehreren EB-Konfigurationen, die das erforderliche Datenmodell, die Metadaten, die Modellzuordnung und Formatkomponenten enthalten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Sign in to the instance of RCS that has been provisioned for your company.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Melden Sie sich bei der Instanz von RCS an, die für Ihr Unternehmen bereitgestellt wurde.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In this tutorial, you will create and modify configurations for the <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept> sample company.</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">In diesem Tutorial erstellen und modifizieren Sie Konfigurationen für das Beispielunternehmen <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Therefore, make sure that this configuration provider has been added to RCS and selected as active.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Stellen Sie daher sicher, dass dieser Konfigurationsanbieter RCS hinzugefügt wurde und als aktiv ausgewählt wurde.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For instructions, see the <bpt id="p1">[</bpt>Create configuration providers and mark them as active<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept> procedure.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Anweisungen finden Sie unter der Prozedur <bpt id="p1">[</bpt>Konfigurationsanbieter erstellen und als aktiv markieren<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Im Arbeitsbereich <bpt id="p1">**</bpt>Elektronische Berichterstellung<ept id="p1">**</ept> wählen Sie die Kachel <bpt id="p2">**</bpt>Berichterstellungskonfigurationen<ept id="p2">**</ept> aus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Auf der Seite <bpt id="p1">**</bpt>Konfigurationen<ept id="p1">**</ept> importieren Sie die EB-Konfigurationen, die Sie als Voraussetzung nach RCS heruntergeladen haben, in der folgenden Reihenfolge: Datenmodell, Metadaten, Modellzuordnung, Format.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For each configuration, follow these steps:</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Führen Sie für jede Konfiguration die folgenden Schritte aus:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Exchange <ph id="ph1">\&gt;</ph> Load from XML file<ept id="p1">**</ept>.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Wählen Sie im Aktivitätsbereich <bpt id="p1">**</bpt>Austausch <ph id="ph1">\&gt;</ph> Aus XML-Datei laden<ept id="p1">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the appropriate file for the required ER configuration in XML format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wählen Sie <bpt id="p1">**</bpt>Durchsuchen<ept id="p1">**</ept> aus, um die entsprechende Datei für die erforderliche EB-Konfiguration im XML-Format auszuwählen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Wählen Sie <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Configurations page in RCS</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Konfigurationsseite in RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Run the ER solution to trace execution</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ausführen der EB-Lösung, um Ausführung nachzuverfolgen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Assume that you've finished designing the first version of the ER solution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Gehen Sie davon aus, dass Sie das Entwerfen der ersten Version der EB-Lösung beendet haben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>You now want to test it in your Finance and Operations instance and analyze execution performance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jetzt möchten Sie sie in Ihrer Finance and Operations-Instanz testen und die Ausführungsleistung analysieren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import an ER configuration from RCS into Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Importieren einer EB-Konfiguration aus RCS nach Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Sign in to your Finance and Operations instance.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Bei Finance and Operations-Instanz anmelden.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Für dieses Tutorial importieren Sie Konfigurationen aus Ihrer RCS-Instanz (wo Sie Ihre EB-Komponenten entwerfen) in Ihre Finance and Operations-Instanz (wo Sie sie testen und schließlich benutzen).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Therefore, you must make sure that all the required artifacts have been prepared.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Daher müssen Sie sicherstellen, dass alle erforderlichen Artefakte vorbereitet wurden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>For instructions, see the <bpt id="p1">[</bpt>Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept> procedure.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Anweisungen finden Sie unter der Prozedur <bpt id="p1">[</bpt>Importieren von elektronischen Berichtstellungskonfigurationen (EB) aus Regulatory Configuration Services (RCS)<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Follow these steps to import the configurations from RCS into Finance and Operations:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Gehen Sie folgendermaßen vor, um die Konfigurationen von RCS nach Finance and Operations zu importieren:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, on the tile for the <bpt id="p2">**</bpt>Litware, Inc.<ept id="p2">**</ept> configuration provider, select <bpt id="p3">**</bpt>Repositories<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Im Arbeitsbereich <bpt id="p1">**</bpt>Elektronische Berichterstellung<ept id="p1">**</ept> in der Kachel für den Konfigurationsanbieter <bpt id="p2">**</bpt>Litware, Inc.<ept id="p2">**</ept> wählen Sie <bpt id="p3">**</bpt>Repositorys<ept id="p3">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>On the <bpt id="p1">**</bpt>Configuration repository<ept id="p1">**</ept> page, select the repository of the <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> type, and then select <bpt id="p3">**</bpt>Open<ept id="p3">**</ept>.</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match">Wählen Sie auf de Seite <bpt id="p1">**</bpt>Konfigurationsrepository<ept id="p1">**</ept> das Repository des Typs <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> aus und wählen Sie dann <bpt id="p3">**</bpt>Öffnen<ept id="p3">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> FastTab, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Im Inforegister <bpt id="p1">**</bpt>Konfigurationen<ept id="p1">**</ept> wählen Sie die Konfiguration <bpt id="p2">**</bpt>Leistungsnachverfolgungsformat<ept id="p2">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>On the <bpt id="p1">**</bpt>Versions<ept id="p1">**</ept> FastTab, select version <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> of the selected configuration, and then select <bpt id="p3">**</bpt>Import<ept id="p3">**</ept>.</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Wählen Sie im Inforegister <bpt id="p1">**</bpt>Versionen<ept id="p1">**</ept> die Version <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> der ausgewählten Konfiguration aus, und wählen Sie dann <bpt id="p3">**</bpt>Importieren<ept id="p3">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Configuration repository page in Finance and Operations</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">Konfigurationsrepositoryseite in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die entsprechenden Versionen der Datenmodell- und Modellzuordnungskonfigurationen werden automatisch als Voraussetzungen für die importierte EB-Formatkonfiguration importiert.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Turn on the ER performance trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Aktivieren der EB-Leistungsnachverfolgung</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">In Finance and Operations gehen Sie zu <bpt id="p1">**</bpt>Organisationsverwaltung <ph id="ph1">\&gt;</ph> Elektronische Berichterstellung <ph id="ph2">\&gt;</ph> Konfigurationen<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Auf der Seite <bpt id="p1">**</bpt>Konfigurationen<ept id="p1">**</ept> im Aktivitätsbereich, auf der Registerkarte <bpt id="p2">**</bpt>Konfigurationen<ept id="p2">**</ept> in der Gruppe <bpt id="p3">**</bpt>Erweiterte Einstellungen<ept id="p3">**</ept> wählen Sie <bpt id="p4">**</bpt>Benutzerparameter<ept id="p4">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, follow these steps:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Im Dialogfeld <bpt id="p1">**</bpt>Benutzerparameter<ept id="p1">**</ept> im Abschnitt <bpt id="p2">**</bpt>Ausführungsnachverfolgung<ept id="p2">**</ept> führen Sie die folgenden Schritte aus:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Debug trace format<ept id="p2">**</ept> to start to collect the details of ER format execution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wählen Sie im Feld <bpt id="p1">**</bpt>Ausführungsnachverfolgungsformat<ept id="p1">**</ept> die Option <bpt id="p2">**</bpt>Nachverfolgungsformat debuggen<ept id="p2">**</ept> aus, um mit dem Sammeln der Details der EB-Formatausführung zu beginnen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wenn dieser Wert ausgewählt wurde, dann sammelt die Leistungsnachverfolgung Informationen zu der Zeit, die für die folgenden Aktivitäten aufgewendet wird:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Running each data source in the model mapping that is called to get data</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ausführen jeder Datenquelle in der Modellzuordnung, die aufgerufen wird, um Daten abzurufen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Processing each format item to enter data in the output that is generated</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Verarbeitung jedes Formatelements, um Daten in der Ausgabe einzugeben, die generiert wird</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You use the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie verwenden das Feld <bpt id="p1">**</bpt>Ausführungsnachverfolgungsformat<ept id="p1">**</ept>, um das Format der generierten Leistungsnachverfolgung anzugeben, in der die Ausführungsdetails für das EB-Format und Zuordnungselemente gespeichert werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>By selecting <bpt id="p1">**</bpt>Debug trace format<ept id="p1">**</ept> as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Indem Sie <bpt id="p1">**</bpt>Nachverfolgungsformat debuggen<ept id="p1">**</ept> als Wert auswählen, sind Sie in der Lage, den Inhalt der Nachverfolgung im EB-Arbeitsgang-Designer zu analysieren und das EB-Format oder die Zuordnungselemente, die in der Nachverfolgung aufgeführt werden, anzuzeigen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Set the following options to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to collect specific details of the execution of the ER model mapping and ER format components:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Legen Sie die folgenden Optionen auf <bpt id="p1">**</bpt>Ja<ept id="p1">**</ept> fest, um bestimmte Details der Ausführung der EB-Modellzuordnung und EB-Formatkomponenten zu sammeln:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Collect query statistics<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect the following information:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Abfragestatistiken sammeln<ept id="p1">**</ept> – Wenn diese Option aktiviert ist, wird die Leistungsnachverfolgung die folgenden Informationen sammeln:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The number of database calls that were made by data sources</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Anzahl von Datenbankaufrufen, die nach Datenquellen vorgenommen wurden</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The number of duplicate calls to the database</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Anzahl der Doppeltaufrufe der Datenbank</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Details of the SQL statements that were used to make database calls</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Details der SQL-Anweisungen, die verwendet wurden, um Datenbankaufrufe vorzunehmen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Trace access of caching<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Zugriff der Zwischenspeicherung nachverfolgen<ept id="p1">**</ept> – Wenn diese Option aktiviert ist, sammelt die Leistungsnachverfolgung Informationen über die Cacheverwendung durch die EB-Modellzuordnung.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source><bpt id="p1">**</bpt>Trace data access<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Datenzugriff nachverfolgen<ept id="p1">**</ept> – Wenn diese Option aktiviert ist, sammelt die Leistungsnachverfolgung Informationen zur Anzahl der Aufrufe der Datenbank für ausgeführte Datenquellen des Datensatz-Listentyps.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">**</bpt>Trace list enumeration<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Listenenumeration nachverfolgen<ept id="p1">**</ept> – Wenn diese Option aktiviert ist, sammelt die Leistungsnachverfolgung Informationen zur Anzahl der Datensätze, die von Datenquellen des Datensatz-Listentyps angefordert werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The parameters in the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box are specific to the user and the current company.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Parameter im Dialogfeld <bpt id="p1">**</bpt>Benutzerparameter<ept id="p1">**</ept> sind für den Benutzer und das aktuelle Unternehmen spezifisch.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>User parameters dialog box in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Benutzerparameter-Dialogfeld in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Run the ER format</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Das EB-Format ausführen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>In Finance and Operations, select the <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept> company.</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match">Wählen Sie in Finance and Operations das Unternehmen <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Wechseln Sie zu <bpt id="p1">**</bpt>Organisationsverwaltung <ph id="ph1">\&gt;</ph> Elektronische Berichterstellung <ph id="ph2">\&gt;</ph> Konfigurationen<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> item.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Auf der Seite <bpt id="p1">**</bpt>Konfigurationen<ept id="p1">**</ept> in der Konfigurationsstruktur wählen Sie das Element <bpt id="p2">**</bpt>Leistungsnachverfolgungsformat<ept id="p2">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Run<ept id="p1">**</ept>.</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Wählen Sie im Aktivitätsbereich auf <bpt id="p1">**</bpt>Ausführen<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Notice that the file that is generated presents information about 265 transactions for six vendors.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Beachten Sie, dass die Datei, die generiert wird, Informationen über 265 Transaktionen für sechs Kreditoren präsentiert.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Review the execution trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Überprüfen der Ausführungsnachverfolgung</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Export the generated trace from Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Die generierte Nachverfolgung aus Finance and Operations exportieren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Leistungsnachverfolgungen werden vom Quell-EB-Format entkoppelt und können in eine externe ZIP-Datei serialisiert werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configuration debug logs<ept id="p1">**</ept>.</source><target logoport:matchpercent="88" state="translated" state-qualifier="fuzzy-match">In Finance and Operations gehen Sie zu <bpt id="p1">**</bpt>Organisationsverwaltung <ph id="ph1">\&gt;</ph> Elektronische Berichterstellung <ph id="ph2">\&gt;</ph> Konfigurationsdebug-Protokolle<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Electronic reporting run logs<ept id="p1">**</ept> page, in the left pane, in the <bpt id="p2">**</bpt>Configuration name<ept id="p2">**</ept> field, select <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> to find the log records that have been generated by the execution of the <bpt id="p4">**</bpt>Performance trace format<ept id="p4">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Auf der Seite <bpt id="p1">**</bpt>Elektronische Berichterstellungs-Ausführungsprotokolle<ept id="p1">**</ept> im linken Bereich im Feld <bpt id="p2">**</bpt>Konfigurationsname<ept id="p2">**</ept> wählen Sie <bpt id="p3">**</bpt>Leistungsnachverfolgungsformat<ept id="p3">**</ept> aus, um die Protokolldatensätze zu suchen, die durch die Ausführung der Konfiguration <bpt id="p4">**</bpt>Leistungsnachverfolgungsformat<ept id="p4">**</ept> generiert wurden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Select the <bpt id="p1">**</bpt>Attachments<ept id="p1">**</ept> button (the paper clip symbol) in the upper-right corner of the page, or press <bpt id="p2">**</bpt>Ctrl+Shift+A<ept id="p2">**</ept>.</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Wählen Sie die Schaltfläche <bpt id="p1">**</bpt>Anhänge<ept id="p1">**</ept> aus (das Büroklammersymbol) in der oberen rechten Ecke der Seite, oder drücken Sie <bpt id="p2">**</bpt>Strg+Umschalt+A<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Attachments button on the Electronic reporting run logs page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Anhangschaltfläche auf der Seite für Elektronische Berichterstellungsausführungsprotokolle in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>On the <bpt id="p1">**</bpt>Attachments for Electronic reporting run logs<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Open<ept id="p2">**</ept> to get the performance trace as a zip file and store it locally.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Auf der Seite <bpt id="p1">**</bpt>Anhänge für elektronische Berichterstellungsausführungsprotokolle<ept id="p1">**</ept> im Aktivitätsbereich wählen Sie <bpt id="p2">**</bpt>Öffnen<ept id="p2">**</ept> aus, um die Leistungsnachverfolgung als ZIP-Datei abzurufen und sie lokal zu speichern.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Attachments for Electronic reporting run logs page in Finance and Operations</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Anhänge für auf der Seite für Elektronische Berichterstellungsausführungsprotokolle in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The trace that is generated has a reference to the source ER report via a unique report identifier in <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> format only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Nachverfolgung, die generiert wird, hat eine Referenz auf den Quell-EB-Bericht über einen eindeutigen Berichtsbezeichner ausschließlich im <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept>-Format.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The version numbering of the format isn't considered.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Versionsnummerierung des Formats wird nicht berücksichtigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Beachten Sie, dass die Zuordnung zwischen der Leistungsnachverfolgung, die für das ausgeführte EB-Format generiert wurde, und der EB-Modellzuordnung auf dem Stammdeskriptor basiert, der verwendet wurde, sowie dem allgemeinen Datenmodell.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>The version numbering of the format and model mapping isn't considered.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Die Versionsnummerierung des Formats und der Modellzuordnung wird nicht berücksichtigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The setting of the <bpt id="p1">**</bpt>Default for model mapping<ept id="p1">**</ept> flag for the model mapping also isn't considered.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Einstellung der Markierung <bpt id="p1">**</bpt>Standard für Modellzuordnung<ept id="p1">**</ept> für die Modellzuordnung wird ebenfalls nicht berücksichtigt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import the generated trace into RCS</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Generierte Nachverfolgung nach RCS importieren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>In RCS, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match">Im RCS, im Arbeitsbereich <bpt id="p1">**</bpt>Elektronische Berichterstellung<ept id="p1">**</ept> wählen Sie die Kachel <bpt id="p2">**</bpt>Berichterstellungskonfigurationen<ept id="p2">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, expand the <bpt id="p2">**</bpt>Performance trace model<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Erweitern Sie auf der Seite <bpt id="p1">**</bpt>Konfigurationen<ept id="p1">**</ept> in der Konfigurationsstruktur das Element <bpt id="p2">**</bpt>Leistungsnachverfolgungsmodell<ept id="p2">**</ept>, und wählen Sie das Element <bpt id="p3">**</bpt>Leistungsnachverfolgungsformat<ept id="p3">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Wählen Sie im Aktivitätsbereich <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>On the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Auf der Seite <bpt id="p1">**</bpt>Format-Designer<ept id="p1">**</ept> im Aktivitätsbereich wählen Sie <bpt id="p2">**</bpt>Leistungsnachverfolgung<ept id="p2">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>In the <bpt id="p1">**</bpt>Performance trace result settings<ept id="p1">**</ept> dialog box, select <bpt id="p2">**</bpt>Import performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Im Dialogfeld <bpt id="p1">**</bpt>Leistungsnachverfolgungs-Ergebniseinstellungen<ept id="p1">**</ept> wählen Sie <bpt id="p2">**</bpt>Leistungsnachverfolgung importieren<ept id="p2">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the zip file that you exported from Finance and Operations earlier.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wählen Sie <bpt id="p1">**</bpt>Durchsuchen<ept id="p1">**</ept> aus, um die ZIP-Datei auszuwählen, die Sie zuvor aus Finance and Operations exportiert haben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Wählen Sie <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Performance trace result settings dialog box in RCS</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Leistungsnachverfolgungsergebnis-Einstellungen-Dialogfeld in RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use the performance trace for analysis in RCS – Format execution</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Verwenden Sie die Leistungsnachverfolgung zur Analyse in RCS – Formatausführung</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>In RCS, on the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>Expand/collapse<ept id="p2">**</ept> to expand the content of all format items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">In RCS auf der Seite <bpt id="p1">**</bpt>Format-Designer<ept id="p1">**</ept> wählen Sie <bpt id="p2">**</bpt>Erweitern/Reduzieren<ept id="p2">**</ept> aus, um den Inhalt aller Formatelemente zu erweitern.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Notice that additional information is shown for some items of the current format:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Beachten Sie, dass zusätzliche Informationen für einige Artikel des aktuellen Formats angezeigt werden:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>The actual time that was spent entering data in the generated output by using the format item</source><target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-mt">Tatsächlicher Zeitaufwand für die Eingabe von Daten in der generierten Ausgabe mithilfe des Formatelements</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>The same time expressed as a percentage of the total time that was spent generating the whole output</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die gleiche Zeit, ausgedrückt als Prozentsatz der gesamten Zeit, die für das Generieren der gesamten Ausgabe aufgewendet wurde</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Format designer page in RCS</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Format-Designer-Seite in RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Close <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Seite <bpt id="p1">**</bpt>Format-Designer<ept id="p1">**</ept> schließen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Use the performance trace for analysis in RCS – Model mapping</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Verwenden Sie die Leistungsnachverfolgung zur Analyse in RCS – Modellzuordnung</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> item.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">In RCS, auf der Seite <bpt id="p1">**</bpt>Konfigurationen<ept id="p1">**</ept> in der Konfigurationsstruktur wählen Sie das Element <bpt id="p2">**</bpt>Leistungsnachverfolgungszuordnung<ept id="p2">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="85" state="translated" state-qualifier="leveraged-inherited">Wählen Sie im Aktivitätsbereich <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept> aus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Wählen Sie <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept> aus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>On the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Auf der Seite <bpt id="p1">**</bpt>Modellzuordnungsdesigner<ept id="p1">**</ept> im Aktivitätsbereich wählen Sie <bpt id="p2">**</bpt>Leistungsnachverfolgung<ept id="p2">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Select the trace that you imported earlier.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wählen Sie die Nachverfolgung aus, die Sie zuvor importierten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Wählen Sie <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Notice that new information becomes available for some data source items of the current model mapping:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Beachten Sie, dass neue Informationen für einige Datenquellelemente der aktuellen Modellzuordnung verfügbar werden:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The actual time that was spent getting data by using the data source</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tatsächlicher Zeitaufwand für das Abrufen von Daten mithilfe der Datenquelle</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The same time expressed as a percentage of the total time that was spent running the whole model mapping</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Die gleiche Zeit, ausgedrückt als Prozentsatz der gesamten Zeit, die für das Ausführen der gesamten Modellzuordnung aufgewendet wurde</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source is run.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Beachten Sie, dass EB Sie informiert, dass die aktuelle Modellzuordnung Datenbankanforderungen dupliziert, während die Datenquelle VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum ausgeführt wird.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese Duplizierung findet statt, weil die Liste von Kreditorentransaktionen zweimal für jeden iterierten Kreditorendatensatz aufgerufen wird:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>One call is made to enter details of each transaction in the data model, based on configured bindings.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ein Aufruf wird vorgenommen, um Details jeder Transaktion in das Datenmodell einzugeben, basierend auf konfigurierten Bindungen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>One call is made to enter the calculated number of transactions per vendor in the data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ein Aufruf wird vorgenommen, um die berechnete Anzahl von Transaktionen pro Kreditor im Datenmodell einzugeben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Message about duplicate database requests on the Model mapping designer page in RCS</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Meldung zu doppelten Datenbankanforderungen auf der Seite Modellzuordnungsdesigner in RCS.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Der Wert <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> gibt an, dass die Tabelle VendTrans 530 Mal aufgerufen wurde, um einen Datensatz von dieser Tabelle an die Datenquelle VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum zurückzugeben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Der Wert <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> gibt an, dass die Datenquelle VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum 530 Mal aufgerufen wurde, um einen Datensatz aus dieser Datenquelle zurückzugeben und die Details daraus in das Datenmodell einzugeben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>We recommend that you use caching for the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Es wird empfohlen, dass Sie das Zwischenspeichern für die Datenquelle VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum verwenden, um die Anzahl von Aufrufen zu verringern, die vorgenommen werden, um die Details für 265 Transaktionen abzurufen und die Leistung der Modellzuordnung zu verbessern.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Es kann außerdem hilfreich sein, die Anzahl von Aufrufen zu reduzieren, die an die Datenquelle LedgerTransTypeList vorgenommen werden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>This data source is used to associate each value of the <bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> enumeration with its label.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese Datenquelle wird verwendet, um jeden Wert der Enumeration <bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> seiner Beschriftung zuzuordnen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Indem Sie diese Datenquelle verwenden, können Sie eine entsprechende Beschriftung finden und sie in das Datenmodell für jede Kreditorentransaktion eingeben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>The current number of calls to this data source (9,027) is quite high for 265 transactions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die aktuelle Anzahl von Aufrufen an diese Datenquelle (9.027) ist ziemlich hoch für 265 Buchungen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Model mapping designer page in RCS, showing 9,027 calls to the data source</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Modellzuordnungsdesigner-Seite in RCS, die 9.027 Aufrufe an die Datenquelle zeigt</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Improve the model mapping based on information from the execution trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Verbessern der Modellzuordnung auf der Grundlage von Informationen aus der Ausführungsnachverfolgung</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Modify the logic of the model mapping</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Die Logik der Modellzuordnung ändern</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Follow these steps to use caching, to help prevent duplicate calls to the database:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Gehen Sie folgendermaßen vor, um Zwischenspeicherung zu verwenden, um doppelte Aufrufe an die Datenbank zu verhindern:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>In RCS, on the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Data sources<ept id="p2">**</ept> pane, select the <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">In RCS auf der Seite <bpt id="p1">**</bpt>Modellzuordnungsdesigner<ept id="p1">**</ept> im Bereich <bpt id="p2">**</bpt>Datenquellen<ept id="p2">**</ept> wählen Sie das Element <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wählen Sie <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Expand the <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept> item, expand the list of one-to-many relations for the VendTable data source (the <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p2">**</ept> item), and select the <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Erweitern Sie das Element <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept>, erweitern Sie die Liste der 1:n-Beziehungen für die Datenquelle VendTable (das Element <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p2">**</ept>), und wählen Sie das Element <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Wählen Sie <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Caching setup to help prevent duplicate calls</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Zwischenspeicherungseinstellung, um doppelte Aufrufe zu verhindern</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Gehen Sie folgendermaßen vor, um die Datenquelle LedgerTransTypeList in den Bereich der Datenquelle VendTable zu bringen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>In the <bpt id="p1">**</bpt>Data source types<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>Functions<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Calculated field<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Erweitern Sie im Bereich <bpt id="p1">**</bpt>Datenquellentypen<ept id="p1">**</ept> das Element <bpt id="p2">**</bpt>Funktionen<ept id="p2">**</ept>, und wählen Sie das Element <bpt id="p3">**</bpt>Berechnetes Feld<ept id="p3">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, select the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wählen Sie im Bereich <bpt id="p1">**</bpt>Datenquellen<ept id="p1">**</ept> das Element <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Select <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Wählen Sie <bpt id="p1">**</bpt>Hinzufügen<ept id="p1">**</ept> aus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept>.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Geben Sie im Feld <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> die Bezeichnung <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept> ein.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Wählen Sie <bpt id="p1">**</bpt>Formel bearbeiten<ept id="p1">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept>.</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match">Geben Sie im Feld <bpt id="p1">**</bpt>Formel<ept id="p1">**</ept> die Bezeichnung <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept> ein.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Wählen Sie <bpt id="p1">**</bpt>Speichern<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Schließen Sie die Seite <bpt id="p1">**</bpt>Formel-Editor<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Klicken Sie auf <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Follow these steps to do caching of the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> field:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Gehen Sie folgendermaßen vor, um die Zwischenspeicherung des Felds <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> auszuführen:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Select the <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept> item.</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Wählen Sie das Element <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Wählen Sie <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Select the <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wählen Sie das Element <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Wählen Sie <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Caching setup for the $TransType field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Zwischenspeicherungseinstellung für das Feld $TransType</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Follow these steps to change the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept> field so that it starts to use the cached <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept> field:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Gehen Sie folgendermaßen vor, um das Feld <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept> zu ändern, sodass es damit beginnt, das zwischengespeicherte Feld <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept> zu verwenden:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item, expand the <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p3">**</ept> item, expand the <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept> item, and select the <bpt id="p5">**</bpt>VendTable. VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Erweitern Sie im Bereich <bpt id="p1">**</bpt>Datenquellen<ept id="p1">**</ept> das Element <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept>, erweitern Sie das Element <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p3">**</ept>, erweitern Sie das Element <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept>, und wählen Sie das Element <bpt id="p5">**</bpt>VendTable. VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Select <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Wählen Sie <bpt id="p1">**</bpt>Bearbeiten<ept id="p1">**</ept> aus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Wählen Sie <bpt id="p1">**</bpt>Formel bearbeiten<ept id="p1">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, find the following expression:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Suchen Sie im Feld <bpt id="p1">**</bpt>Formel<ept id="p1">**</ept> den folgenden Ausdruck:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter the following expression:</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Geben Sie im Feld <bpt id="p1">**</bpt>Formel<ept id="p1">**</ept> den folgenden Ausdruck ein:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Wählen Sie <bpt id="p1">**</bpt>Speichern<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Schließen Sie die Seite <bpt id="p1">**</bpt>Formel-Editor<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Wählen Sie <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Wählen Sie <bpt id="p1">**</bpt>Speichern<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Close the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Schließen Sie die Seite <bpt id="p1">**</bpt>Modellzuordnungsdesigner<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Close the <bpt id="p1">**</bpt>Model mappings<ept id="p1">**</ept> page.</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match">Schließen Sie die Seite <bpt id="p1">**</bpt>Modellzuordnungen<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Complete the modified version of the ER model mapping</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die geänderte Version der EB-Modellzuordnung abschließen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Versions<ept id="p2">**</ept> FastTab, select version <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept> of the <bpt id="p4">**</bpt>Performance trace mapping<ept id="p4">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">In RCS auf der Seite <bpt id="p1">**</bpt>Konfigurationen<ept id="p1">**</ept> im Inforegister <bpt id="p2">**</bpt>Versionen<ept id="p2">**</ept> wählen Sie die Version <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept> der Konfiguration <bpt id="p4">**</bpt>Leistungsnachverfolgungszuordnung<ept id="p4">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Select <bpt id="p1">**</bpt>Change status<ept id="p1">**</ept>.</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match">Wählen Sie <bpt id="p1">**</bpt>Status ändern<ept id="p1">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Select <bpt id="p1">**</bpt>Complete<ept id="p1">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Wählen Sie <bpt id="p1">**</bpt>Abgeschlossen<ept id="p1">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Import the modified ER model mapping configuration from RCS into Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Importieren der geänderten EB-Modellzuordnungskonfiguration von RCS nach Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import an ER configuration from RCS into Finance and Operations<ept id="p1">](#import-configuration)</ept> section earlier in this topic to import version 1.2 of the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> configuration into Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wiederholen Sie die Schritte im Abschnitt <bpt id="p1">[</bpt>Importieren einer EB-Konfiguration von RCS nach Finance and Operations<ept id="p1">](#import-configuration)</ept> weiter oben in diesem Thema, um Version 1.2 der Konfiguration <bpt id="p2">**</bpt>Leistungsnachverfolgungszuordnung<ept id="p2">**</ept> nach Finance and Operations zu importieren. </target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Run the modified ER solution to trace execution</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Ausführen der geänderten EB-Lösung, um Ausführung nachzuverfolgen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Run the ER format</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Das EB-Format ausführen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wiederholen Sie die Schritte im Abschnitt <bpt id="p1">[</bpt>Das EB-Format ausführen<ept id="p1">](#run-format)</ept> weiter oben in diesem Thema, um eine neue Leistungsnachverfolgung zu generieren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Review the execution trace</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Überprüfen der Ausführungsnachverfolgung</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Export the generated trace from Finance and Operations</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Die generierte Nachverfolgung aus Finance and Operations exportieren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Export the generated trace from Finance and Operations<ept id="p1">](#export-trace)</ept> section earlier in this topic to save a new performance trace locally.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wiederholen Sie die Schritte im Abschnitt <bpt id="p1">[</bpt>Die generierte Nachverfolgung aus Finance and Operations exportieren<ept id="p1">](#export-trace)</ept> weiter oben in diesem Thema, um eine neue Leistungsnachverfolgung lokal zu speichern.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Import the generated trace into RCS</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Generierte Nachverfolgung nach RCS importieren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import the generated trace into RCS<ept id="p1">](#import-trace)</ept> section earlier in this topic to import the new performance trace into RCS.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wiederholen Sie die Schritte im Abschnitt <bpt id="p1">[</bpt>Importieren der generierten Nachverfolgung nach RCS<ept id="p1">](#import-trace)</ept> weiter oben in diesem Thema, um die neue Leistungsnachverfolgung nach RCS zu importieren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Use the performance trace for analysis in RCS – Model mapping</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Verwenden Sie die Leistungsnachverfolgung zur Analyse in RCS – Modellzuordnung</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Use the performance trace for analysis in RCS – Model mapping<ept id="p1">](#use-trace)</ept> section earlier in this topic to analyze the latest performance trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wiederholen Sie die Schritte im Abschnitt <bpt id="p1">[</bpt>Verwenden der Leistungsnachverfolgung zur Analyse in RCS – Modellzuordnung<ept id="p1">](#use-trace)</ept> weiter oben in diesem Thema, um die aktuellste Leistungsnachverfolgung analysieren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Beachten Sie, dass die Regulierungen, die Sie an der Modellzuordnung vorgenommen haben, doppelte Abfragen an eine Datenbank beseitigt haben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>The number of calls to database tables and data sources for this model mapping has been also reduced.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Die Anzahl der Aufrufe an Datenbanktabellen und Datenquellen für diese Modellzuordnung ist auch reduziert worden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Therefore, the performance of the whole ER solution has improved.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Daher wurde die Leistung der gesamten EB-Lösung verbessert.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Trace information for the VendTable data source on the Model mapping designer page in RCS</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Nachverfolgungsinformationen für die VendTable-Datenquelle auf der Seite Modellzuordnungsdesigner in RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>In the trace information, the value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> for the VendTable data source indicates that this data source was called 12 times.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">In den Nachverfolgungsinformationen gibt der Wert <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> für die Datenquelle VendTable an, dass diese Datenquelle 12 Mal aufgerufen wurde.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that six calls were translated to database calls to the VendTable table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Der Wert <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> gibt an, dass sechs Aufrufe in Datenbankaufrufe an die Tabelle VendTable übersetzt wurden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Der Wert <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> gibt an, dass die Datensätze, die aus der Datenbank abgerufen wurden, zwischengespeichert wurden, und sechs weitere Aufrufe wurden mithilfe des Cache verarbeitet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Beachten Sie, dass die Anzahl der Aufrufe an die LedgerTransTypeList-Datenquelle von 9.027 auf 240 verringert wurde.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Trace information for the LedgerTransTypeList data source on the Model mapping designer page in RCS</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Nachverfolgungsinformationen für die LedgerTransTypeList-Datenquelle auf der Seite Modellzuordnungsdesigner in RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Review the execution trace in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Überprüfung der Ausführungsnachverfolgung in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Neben RCS bieten manche Versionen von Finance and Operations möglicherweise Funktionen für die Funktionalität eines EB-Framework-Designers.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>These versions of Finance and Operations have an <bpt id="p1">**</bpt>Enable design mode<ept id="p1">**</ept> option that can be turned on.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese Versionen von Finance and Operations haben eine Option <bpt id="p1">**</bpt>Entwurfsmodus aktivieren<ept id="p1">**</ept>, die aktiviert werden kann.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>You can find this option on the <bpt id="p1">**</bpt>General<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept> page, which you can open from the <bpt id="p3">**</bpt>Electronic reporting<ept id="p3">**</ept> workspace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie können diese Option unter der Registerkarte <bpt id="p1">**</bpt>Allgemein<ept id="p1">**</ept> der Seite <bpt id="p2">**</bpt>Elektronische Berichterstellungsparameter<ept id="p2">**</ept> finden, die Sie vom Arbeitsbereich <bpt id="p3">**</bpt>Elektronische Berichterstellung<ept id="p3">**</ept> aus öffnen können.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Enable design mode option on the Electronic reporting parameters page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Entwurfsmodusoption auf der Seite „Elektronische Berichterstellungsparameter“ in Finance and Operations aktivieren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Wenn Sie eine dieser Versionen von Finance and Operations verwenden, können Sie die Details von generierten Leistungsnachverfolgungen direkt in Finance and Operations analysieren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>You don't have to export them from Finance and Operation and import them into RCS.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie müssen sie nicht aus Finance and Operations exportieren und nach RCS importieren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Review the execution trace by using external tools</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Überprüfung der Ausführungsnachverfolgung mithilfe externer Tools</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Configure user parameters</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Benutzerparameter konfigurieren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="72" state="translated" state-qualifier="leveraged-inherited">In Finance and Operations gehen Sie zu <bpt id="p1">**</bpt>Organisationsverwaltung <ph id="ph1">\&gt;</ph> Elektronische Berichterstellung <ph id="ph2">\&gt;</ph> Konfigurationen<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="72" state="translated" state-qualifier="leveraged-inherited">Auf der Seite <bpt id="p1">**</bpt>Konfigurationen<ept id="p1">**</ept> im Aktivitätsbereich, auf der Registerkarte <bpt id="p2">**</bpt>Konfigurationen<ept id="p2">**</ept> in der Gruppe <bpt id="p3">**</bpt>Erweiterte Einstellungen<ept id="p3">**</ept> wählen Sie <bpt id="p4">**</bpt>Benutzerparameter<ept id="p4">**</ept> aus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, in the <bpt id="p3">**</bpt>Execution trace format<ept id="p3">**</ept> field, select <bpt id="p4">**</bpt>PerfView XML<ept id="p4">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Im Dialogfeld <bpt id="p1">**</bpt>Benutzerparameter<ept id="p1">**</ept> im Abschnitt <bpt id="p2">**</bpt>Ausführungsnachverfolgung<ept id="p2">**</ept> im Feld <bpt id="p3">**</bpt>Ausführungsnachverfolgungsformat<ept id="p3">**</ept> wählen Sie <bpt id="p4">**</bpt>PerfView XML<ept id="p4">**</ept> aus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Run the ER format</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Das EB-Format ausführen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Wiederholen Sie die Schritte im Abschnitt <bpt id="p1">[</bpt>Das EB-Format ausführen<ept id="p1">](#run-format)</ept> weiter oben in diesem Thema, um eine neue Leistungsnachverfolgung zu generieren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Notice that the web browser offers a zip file for download.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Beachten Sie, dass der Webbrowser eine ZIP-Datei zum Herunterladen anbietet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>This file contains the performance trace in PerfView format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Diese Datei beinhaltet die Leistungsnachverfolgung im PerfView-Format.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sie können dann das PerfView-Leistungsanalysetool verwenden, um die Details der EB-Formatausführung zu analysieren.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>