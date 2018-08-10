---
title: "Erstellen von Regeln für Optimierungsratgeber"
description: "In diesem Thema wird erläutert, wie dem Optimierungsratgeber neue Regeln hinzufügt werden."
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 83648a93f367510d7b04bbd04a9f37689ecfaa59
ms.openlocfilehash: a18fac31b5acb7d2a1ec40203122d4eb9d94a439
ms.contentlocale: de-de
ms.lasthandoff: 05/23/2018

---

# <a name="create-rules-for-optimization-advisor"></a>Erstellen von Regeln für Optimierungsratgeber

[!include [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie neue Regeln für den **Optimierungsratgeber** erstellt werden. Sie können beispielsweise eine neue Regel erstellen, die angibt, welche Angebotsanforderungsanfragen einen leeren Titel haben. Durch das Verwenden von Titeln bei Anfragen können sie leicht identifiziert und gesucht werden. Während es ziemlich einfach ist, zeigt dieses Beispiel, was mit Optimierungsregeln erreicht werden kann. 

Eine *Regel* ist eine Prüfung von Anwendungsdaten. Wenn die Bedingung, nach der die Regel bewertet, erfüllt ist, werden Verkaufschancen zum Optimieren von Prozessen oder zum Verbessern von Daten erstellt. Auf die Verkaufschancen hin kann gehandelt werden oder optional kann die Auswirkung der Aktivitäten auch gemessen werden. 

Um eine neue Regel für den **Optimierungsratgeber** zu erstellen, eine neue Klasse hinzuzufügen die die abstrakte Klasse **SelfHealingRule** erweitert, die Schnittstelle **IDiagnosticsRule** implementiert und durch das **DiagnosticRule** ausgestattet wird. Bei der Klasse muss auch eine Methode mit dem Attribut **DiagnosticsRuleSubscription** ausgestattet werden. Gewöhnlich erfolgt dies bei der Methode **opportunityTitle**, die später behandelt wird. Diese neue Klasse kann einem benutzerdefinierten Modell mit einer Abhängigkeit vom Modell **SelfHealingRules** hinzugefügt werden. Im folgenden Beispiel wird die Regel, die implementiert wird, **RFQTitleSelfHealingRule** genannt.

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

Die abstrakte Klasse **SelfHealingRule** hat abstrakte Methoden, die in erbenden Klassen implementiert werden müssen. Der Kern ist die Methode **evaluate**, die eine Liste von Verkaufschancen zurückgibt, die von der Regel identifiziert werden. Verkaufschancen können pro juristische Person sein oder das gesamte System betreffen.

```
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

Die oben gezeigt Methode umfasst Unternehmen und wählt Angebotsanforderungsanfragen mit leeren Titeln in der Methode **findRFQCasesWithEmptyTitle** aus. Wenn mindestens eine solche Anfrage gefunden wird, wird eine unternehmensspezifische Verkaufschance mit der Methode **getOpportunityForCompany** erstellt. Beachten Sie, dass das Feld **Daten** in der Tabelle **SelfHealingOpportunity** vom Typ **Container** ist, und es kann daher jegliche Daten enthalten, die relevant für die Logik sind, die für diese Regel spezifisch ist. Durch Festlegen von **OpportunityDate** mit dem aktuellen Zeitstempel wird die Uhrzeit der letzten Bewertung der Verkaufschance registriert.  

Verkaufschancen können auch unternehmensübergreifend sein. In diesem Fall ist die Schleife um Unternehmen nicht notwendig und die Verkaufschance muss mit der Methode **getOpportunityAcrossCompanies** erstellt werden. 

Der folgende Code zeigt die Methode **findRFQCasesWithEmptyTitle**, die die Kennungen der Angebotsanforderungsanfragen zurückgibt, die leere Titel haben.

```
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

Zwei Methoden, die implementiert werden müssen, sind **opportunityTitle** und **opportunityDetails**. Erstere gibt einen kurzen Titel für die Verkaufschance zurück, letztere gibt eine detaillierte Beschreibung der Verkaufschance zurück, die auch Daten umfassen kann.

Der Titel, der durch **opportunityTitle** zurückgegeben wird, wird unter der Spalte **Optimierungsverkaufschance** im Arbeitsbereich **Optimierungsratgeber** angezeigt. Er wird zudem als der Kopf des Seitenbereichs angezeigt, der mehr Informationen zu der Verkaufschance anzeigt. Ordnungsgemäß ist diese Methode mit dem Attribut **DiagnosticRuleSubscription** ausgestattet, das die folgenden Argumente bezieht: 

* **Diagnosebereich** – Eine Aufzählung des Typs **DiagnosticArea**, der beschreibt, zu welchem Bereich der Anwendung die Regel gehört, wie beispielsweise **DiagnosticArea::SCM**. 

* **Regelname** – Eine Zeichenfolge mit dem Regelname. Diese wird unter der Spalte **Regelname** im Formular **Diagnoseüberprüfungsregel** (**DiagnosticsValidationRuleMaintain**) angezeigt. 

* **Ausführungshäufigkeit** – Eine Aufzählung des Typs **DiagnosticRunFrequency**, die beschreibt, wie oft die Regel ausgeführt werden soll, wie beispielsweise **DiagnosticRunFrequency::Daily**. 

* **Regelbeschreibung** – Eine Zeichenfolge mit einer ausführlicheren Beschreibung der Regel. Diese wird unter der Spalte **Regelbeschreibung** im Formular **Diagnoseüberprüfungsregel** (**DiagnosticsValidationRuleMaintain**) angezeigt. 

> [!NOTE]
> Das Attribut **DiagnosticRuleSubscription** ist erforderlich, damit die Regel funktioniert. Normalerweise wird es bei **opportunityTitle** verwendet, mit ihm kann jedoch jede Methode oder Klasse ausgestattet werden.

Hier folgt ein Beispiel einer Implementierung. Rohzeichenolgen werden der Einfachheit halber verwendet, aber eine korrekte Implementierung erfordert Beschriftungen. 

```
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

Die Beschreibung, die von **opportunityDetails** zurückgegeben wird, wird im Seitenbereich angezeigt, dabei zeigt sie weitere Informationen zur Verkaufschance an. Sie nimmt das Argument **SelfHealingOpportunity**, das das Feld **Daten** ist, das verwendet werden kann, um weitere Informationen zur Verkaufschance bereitzustellen. Im Beispiel gibt die Methode die Kennungen der Angebotsanforderungsanfragen mit einem leeren Titel zurück. 

```
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

Die beiden verbleibenden zu implementierenden abstrakten Methoden sind **provideHealingAction** und **securityMenuItem**. 

**provideHealingAction** gibt „true” zurück, wenn eine Reparaturaktivität bereitgestellt wird, ansonsten gibt sie „false” zurück. Wenn „true” zurückgegeben wird, muss die Methode **performAction** implementierte werden, oder ein Fehler wird ausgelöst. Die Methode **performAction** nimmt ein **SelfHealingOpportunity**-Argument, in dem die Daten für die Aktivität verwendet werden können. Im Beispiel öffnet die Aktivität die **PurchRFQCaseTableListPage**, für die manuelle Korrektur. 

```
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

Abhängig von den Angaben der Regel kann es nicht möglich, von einer automatischen Aktivität mithilfe der Verkaufschancendaten Gebrauch zu machen. In diesem Beispiel könnte das System Titel für Angebotsanforderungsanfragen automatisch generieren. 

**securityMenuItem** gibt den Namen einer Aktivitätsmenüoption zurück, sodass die Regel nur für Benutzer sichtbar ist, die auf die Aktivitätsmenüoption zugreifen können. Die Sicherheit kann es unter Umständen erfordern, dass auf bestimmte Regeln und Verkaufschancen nur durch autorisierte Benutzer zugegriffen werden kann. Im Beispiel können nur Benutzer mit Zugriff auf **PurchRFQCaseTitleAction** die Verkaufschance anzeigen. Beachten Sie, dass diese Aktivitätsmenüoption für dieses Beispiel erstellt wurde und als Einstiegspunkt für das Sicherheitsrecht **PurchRFQCaseTableMaintain** hinzugefügt wurde. 

> [!NOTE]
> Die Menüoption muss eine Aktivitätsmenüoption sein, damit die Sicherheit ordnungsgemäß funktioniert. Andere Menüoptionstypen, wie **Anzeigemenüartikel** funktionieren nicht korrekt.

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

Nachdem die Regel kompiliert wurde, führen Sie den folgenden Einzelvorgang aus, damit die Anzeige in der Benutzeroberfläche (UI) erfolgt.

```
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

Die Regel wird im Formular **Diagnoseüberprüfungsregel** angezeigt, das von **Systemverwaltung** > **Periodische Aufgaben** > **Diagnoseüberprüfungsregel verwalten** verfügbar ist. Damit sie bewertet wird, wechseln Sie zu **Systemverwaltung** > **Periodische Aufgaben** > **Diagnoseüberprüfungsregel planen**, wählen Sie die Häufigkeit der Regel aus, wie beispielsweise **Täglich**. Klicken Sie auf **OK**. Wechseln Sie zu **Systemverwaltung** > **Optimierungsratgeber**, um die neue Verkaufschance anzuzeigen. 

Das folgende Beispiel ist ein Codeausschnitt mit dem Skelett einer Regel einschließlich aller erforderlichen Attribute und Methoden. Es ermöglicht, mit dem schreiben neuer Regeln zu beginnen. Die Beschriftungen und die Aktivitätsmenüoptionen, die im Beispiel verwendet werden, gelten nur zu Vorführungszwecken.

```
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

Weitere Informationen finden Sie im kurzen YouTube-Video: [Optimierungsratgeber in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)

