---
title: Virtuelle Dataverse-Tabellenabfragen optimieren
description: Optimieren und Behandeln von Leistungsproblemen bei virtuellen Dataverse-Tabellenabfragen
author: twheeloc
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f379cd7783cc984666582d2c680a1db013627ce
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070171"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>Virtuelle Dataverse-Tabellenabfragen optimieren


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



## <a name="issue"></a>Abgang

### <a name="overview"></a>Übersicht

Beim Benutzen von virtuellen Dataverse-Tabellen zum Entwickeln von Integrationen und anderen Datenverbindungen mit Dynamics 365 Human Resources können bei Abfragen der virtuellen Tabellen Leistungsprobleme auftreten. Die langsame Abfrageausführung kann über verschiedene Clients oder Schnittstellen hinweg erfolgen. Beispielsweise kann das Problem in den folgenden Umständen auftreten:

- Bei der Abfrage einer virtuellen Tabelle über die Dataverse-Web-API
- Beim Erstellen einer Power-App für eine virtuelle Tabelle
- Beim Erstellen eines Power BI-Berichts über eine virtuelle Tabelle

Alle diese Schnittstellen können das Leistungsproblem auslösen.

Eine Ursache für eine langsame Leistung mit virtuellen Dataverse-Tabellen für die Personalabteilung sind die Fremdschlüsselspalten der virtuellen Tabelle, die sich auf die [Navigationseigenschaften](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) der Tabelle beziehen. Wenn Navigationseigenschaften für eine virtuelle Tabelle erstellt werden, wird der Tabelle automatisch eine Fremdschlüsselspalte hinzugefügt, um den Wert des Schlüssels für die Schlüsselspalte der zugehörigen virtuellen Tabelle darzustellen. Die Spalte **_mshr_fk_Person_id_value** wird zum Beispiel der Entität **mshr_hcmworkerbaseentity** mit der Fremdschlüsseleigenschaft aus der **mshr_dirpersonentity**-Entität hinzugefügt. Aufgrund der Art und Weise, wie die Werte für diese Fremdschlüsselspalten in einer Tabelle verwaltet werden, kann sich das Abrufen der Werte negativ auf die Leistung einer Abfrage für die virtuelle Tabelle auswirken.

### <a name="potential-symptoms"></a>Mögliche Symptome

Diese Auswirkungen treten zum Beispiel möglicherweise bei Abfragen an die Arbeitskraft- Entität (**mshr_hcmworkerentity**) oder Basisarbeitskraft-Entität (**mshr_hcmworkerbaseentity**) auf. Möglicherweise tritt das Leistungsproblem auf verschiedene Arten auf:

- **Langsame Abfrageausführung**: Die Abfrage für die virtuelle Tabelle gibt möglicherweise die erwarteten Ergebnisse zurück, es dauert jedoch länger als erwartet, bis die Ausführung der Abfrage abgeschlossen ist.
- **Abfragezeitüberschreitung**: Die Abfrage kann eine Zeitüberschreitung verursachen und den folgenden Fehler zurückgeben: „Es wurde ein Token erhalten, um Finanzen und Betrieb aufzurufen, aber Finanzen und Betrieb hat einen Fehler vom Typ InternalServerError zurückgegeben.“
- **Unerwarteter Fehler**: Die Abfrage gibt möglicherweise einen Fehler vom Typ 400 mit der folgenden Meldung zurück: „Ein unerwarteter Fehler ist aufgetreten.“

  ![Fehler vom Typ 400 bei der HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType400.png)

- **Drosselung**: Die Abfrage kann die Serverressourcen überbeanspruchen, sodass es zu einer Drosselung kommt. In diesem Fall gibt die Abfrage den folgenden Fehler zurück: „Es wurde ein Token erhalten, um Finanzen und Betrieb aufzurufen, aber Finanzen und Betrieb hat einen Fehler vom Typ 429 zurückgegeben.“ Weitere Informationen zur Drosselung in Humen Resources finden Sie unter [Drosselung – Häufig gestellte Fragen](./hr-admin-integration-throttling-faq.md).

  ![Fehler vom Typ 429 bei der HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>Lösung

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>Begrenzen Sie die Anzahl der Spalten, die in Ihrer Datenabfrage enthalten sind

Bei virtuellen Tabellen ist eine der Methoden mit dem größten Potenzial zur Verbesserung der Abfrageleistung die Begrenzung der Anzahl der für die Abfrage ausgewählten Spalten. Die allgemeine Anleitung zur Optimierung der Abfrageleistung besteht darin, die in Ihrer Abfrage zurückgegebenen Spalten nur auf die Eigenschaften zu beschränken, die Sie benötigen. Dies gilt insbesondere für die Fremdschlüsselspalten in virtuellen Tabellen. Wenn Sie die Werte in den Fremdschlüsselspalten für Ihre Integration oder Ihren Bericht nicht benötigen, strukturieren Sie die Abfrage so, dass nur die Spalten ausgewählt werden, die Sie benötigen, und die Fremdschlüsselspalten ausschließen.

#### <a name="selecting-columns-in-an-odata-query"></a>Spalten in einer OData-Abfrage auswählen

Bei der Abfrage einer virtuellen Tabelle über Dataverse-Web-API können Sie die Anzahl der in der Abfrage enthaltenen Spalten mithilfe der **$select**-Systemabfrageoption begrenzen und die Spalten definieren, für die Ergebnisse zurückgegeben werden sollen. Um die Leistung zu maximieren, schließen Sie Fremdschlüsselspalten aus der Abfrage aus (mit dem Präfix **_mshr_FK_**).

Die folgende Abfrage der **mshr_hcmworkerbaseentity**-Entität enthält zum Beispiel nur die Spalten, die in der **$select**-Abfrageoptionsklausel enthalten sind; die Fremdschlüsselwerte sind ausgeschlossen. Dies bietet eine erhebliche Leistungsverbesserung gegenüber einer Abfrage, die alle Tabellenspalten enthält.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Die Empfehlung, die Anzahl der ausgewählten Spalten zu begrenzen, gilt auch bei Verwendung der Abfrageoption **$expand** zum Erweitern der Abfrage auf dazugehörige virtuelle Tabellen über Navigationseigenschaften. Die folgende Abfrage enthält beispielsweise Spalten aus der **mshr_hcmworkerbaseentity**-Entität mit erweiterten Spalten aus der **mshr_dirpersonentity**-Entität. Bitte beachten Sie, dass die **$select**-Abfrageoption auch in der **$expand**-Abfrageoptionsklausel enthalten ist.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Wenn Sie diese Methode zum Abrufen von Daten mit der Abfrageoption **$select** in der Abfrageoptionsklausel **$expand** verwenden, werden in der Regel größere Leistungsverbesserungen festgestellt, wenn die Navigationseigenschaft zwischen den Entitäten eine n:1-Beziehung ist. Eventuell stellen Sie beim Erweitern einer 1:n-Beziehung nicht dieselbe Verkürzung der Ausführungszeit für Abfragen fest. Weitere Informationen zur Beziehungsdefinition für virtuelle Dataverse-Tabellen finden Sie unter [Tabellenbeziehungen](/powerapps/maker/data-platform/create-edit-entity-relationships).

Weitere Informationen zur Verwendung der Systemabfrageoptionen **$select** und **$expand** in der Dataverse-Web-API finden Sie unter [Dazugehörige Entitätsdatensätze mit einer Abfrage abrufen](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).

#### <a name="selecting-columns-in-power-bi"></a>Spalten in Power BI auswählen

Wenn Sie beim Erstellen eines Power BI-Bericht für eine virtuelle Dataverse-Tabelle eines der oben genannten Anzeichen einer langsamen Leistung feststellen, können Sie die Leistung verbessern, indem Sie Fremdschlüsselspalten von den Spalten ausschließen, die in der Tabelle für den Bericht ausgewählt wurden. Wenn Sie zum Beispiel Power BI Desktop verwenden, um einen Bericht für die Entität **mshr_hcmworkerbaseentity** zu erstellen, können Sie die folgenden Schritte ausführen, um die Spalten auszuwählen, die in die Berichtsabfrage enthalten sein sollen.

1. Wählen Sie im Power BI Desktop **Mehr ...** in der Dropdownliste auf dem Aktionsband **Daten abrufen** aus.
2. Geben Sie in dem Fenster **Daten abrufen** **Common Data Service** in das Suchfeld ein, wählen Sie den Connector **Common Data Service** und dann **Verbinden** aus.
3. Geben Sie im Feld **Server-URL** des Common Data Service-Fensters die Organisations-URI für Ihre Dataverse-Umgebung ein und wählen Sie **OK**.
  
   ![Die URI für Ihre Dataverse-Umgebung eingeben.](./media/PowerBIDataverseURLSetup.png)
  
4. Erweitern Sie im Navigator-Fenster den Knoten **Entitäten** aus.
5. Geben Sie im Suchfeld **mshr_hcmworkerbaseentity** ein und wählen Sie die Entität aus.
6. Wählen Sie **Daten transformieren** aus.
7. Wählen Sie im Fenster Power Query Editor **Erweiterter Editor**.
8. Aktualisieren Sie im **Erweiterten Editor** die Abfrage so, dass sie wie folgt aussieht, und fügen Sie dem Array Spalten nach Bedarf hinzu oder entfernen Sie sie.

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Aktualisieren Sie die Abfrage im Advanced Editor für den Power Query-Editor.](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. Wählen Sie **Fertig**.

   > [!NOTE]
   > Wenn Sie vor dem Aktualisieren einen Fehler vom Typ 429 von der Abfrage erhalten haben, müssen Sie möglicherweise die Wiederholungsperiode abwarten, bevor Sie die Abfrage aktualisieren, damit sie erfolgreich abgeschlossen wird.

10. Klicken Sie auf **Schließen & Anwenden** auf dem Menüband Power Query Editor Aktion.

Sie können dann mit dem Aufbau Ihres Power BI-Berichts für die aus der virtuellen Tabelle ausgewählten Spalten beginnen.

#### <a name="selecting-columns-in-power-apps"></a>Spalten in Power Apps auswählen

Ähnlich wie bei Dataverse Web-API-Abfragen und Power BI können Sie die Abfrageleistung für Power Apps basierend auf virtuellen Dataverse-Tabellen verbessern, indem Sie Spalten dazugehöriger Tabellen aus Ihrer App ausschließen. Wenn Spalten aus einer dazugehörigen Tabelle auf einer Seite enthalten sind, enthält die zum Abrufen der Daten erstellte Anforderungs-URL Fremdschlüsseleigenschaften der zugehörigen Tabelle. Wie in den Beispielen von [Spalten in einer OData-Abfrage auswählen](#selecting-columns-in-power-apps) oben, reduziert dies die Leistung, indem zusätzliche Datensuchen durchgeführt werden.

Um dies zu umgehen, können Sie sicherstellen, dass in keinem Datenformular Ihrer Power App Datenfelder aus dazugehörigen Tabellen enthalten sind.

1. Wählen Sie im Bereich der Strukturansicht das Datenformular für die Anzeige aus.
2. Wählen Sie im Bereich **Eigenschaften** **Bearbeiten** in der Eigenschaft **Felder** aus.
3. Stellen Sie im Bereich **Daten** sicher, dass keines der ausgewählten Felder zur virtuellen Tabelle der Datenquelle gehört.

Wenn beispielsweise eines der auf einer Seite in der App enthaltenen Datenfelder auf eine andere Tabelle, wie **ThisItem.Worker.Name** verweist, wo **Arbeitskraft** die dazugehörige Tabelle ist, besteht die Möglichkeit, dass die Leistung beim Abrufen der Daten geringer ist.

Sie können den [Power Apps-Monitor](/powerapps/maker/monitor-overview) benutzen, um sicherzustellen, dass nur die Spalten, die Sie benötigen, in die Abfrage aufgenommen werden, um die Daten für die Power App abzurufen. Sie können die für den getRows-Vorgang erstellte URL anzeigen lassen, um sicherzustellen, dass die für Ihre App ausgewählten Spalten für das Abrufen der Daten optimal sind.

![Den Power Apps-Monitor benutzen, um den getData-Vorgang zu analysieren.](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>Die Datenabfrage filtern

Eine andere Methode zur Verbesserung der Leistung der Abfrageausführung besteht darin, die Anzahl der in den Abfrageergebnissen zurückgegebenen Datensätze zu begrenzen. Sie können dazu die Ergebnisse filtern, um sicherzustellen, dass Sie nur die Datensätze erhalten, die Sie benötigen.

Weitere Informationen zum Filtern von Abfragedaten finden Sie unter [Ergebnisse filtern](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results).

### <a name="limiting-the-page-size-of-the-query"></a>Die Seitengröße der Abfrage begrenzen

Wenn Sie mit großen Datenmengen arbeiten, können Sie die Abfrageergebnisse auf mehrere Seiten aufteilen, indem Sie die `odata.maxpagesize`-Präferenzkopfzeile zu Datenabfragen hinzufügen.

Weitere Informationen zur Seitenverwaltung finden Sie unter [Anzahl der Entitäten festlegen, die auf einer Seite zurückgegeben werden sollen](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).

## <a name="see-also"></a>Siehe auch

- [Virtuelle Dataverse-Tabellen konfigurieren](hr-admin-integration-common-data-service-virtual-entities.md)
- [Virtuelle Human Resources-Tabellen – Häufig gestellte Fragen](hr-admin-virtual-entity-faq.md)
- [Drosselung – Häufig gestellte Fragen](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

