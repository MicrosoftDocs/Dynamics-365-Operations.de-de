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
ms.reviewer: yuyus
ms.search.scope: Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: e64d4fc1a7425d38d728b11e503d3e7289312495
ms.contentlocale: de-de
ms.lasthandoff: 02/07/2018

---

# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="f9635-103">Erstellen von Regeln für Optimierungsratgeber</span><span class="sxs-lookup"><span data-stu-id="f9635-103">Create rules for Optimization advisor</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f9635-104">In diesem Thema wird erklärt, wie neue Regeln für den **Optimierungsratgeber** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f9635-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="f9635-105">Sie können beispielsweise eine neue Regel erstellen, die angibt, welche Angebotsanforderungsanfragen einen leeren Titel haben.</span><span class="sxs-lookup"><span data-stu-id="f9635-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="f9635-106">Durch das Verwenden von Titeln bei Anfragen können sie leicht identifiziert und gesucht werden.</span><span class="sxs-lookup"><span data-stu-id="f9635-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="f9635-107">Während es ziemlich einfach ist, zeigt dieses Beispiel, was mit Optimierungsregeln erreicht werden kann.</span><span class="sxs-lookup"><span data-stu-id="f9635-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="f9635-108">Eine *Regel* ist eine Prüfung von Anwendungsdaten.</span><span class="sxs-lookup"><span data-stu-id="f9635-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="f9635-109">Wenn die Bedingung, nach der die Regel bewertet, erfüllt ist, werden Verkaufschancen zum Optimieren von Prozessen oder zum Verbessern von Daten erstellt.</span><span class="sxs-lookup"><span data-stu-id="f9635-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="f9635-110">Auf die Verkaufschancen hin kann gehandelt werden oder optional kann die Auswirkung der Aktivitäten auch gemessen werden.</span><span class="sxs-lookup"><span data-stu-id="f9635-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="f9635-111">Um eine neue Regel für den **Optimierungsratgeber** zu erstellen, eine neue Klasse hinzuzufügen die die abstrakte Klasse **SelfHealingRule** erweitert, die Schnittstelle **IDiagnosticsRule** implementiert und durch das **DiagnosticRule** ausgestattet wird.</span><span class="sxs-lookup"><span data-stu-id="f9635-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="f9635-112">Bei der Klasse muss auch eine Methode mit dem Attribut **DiagnosticsRuleSubscription** ausgestattet werden.</span><span class="sxs-lookup"><span data-stu-id="f9635-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="f9635-113">Gewöhnlich erfolgt dies bei der Methode **opportunityTitle**, die später behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="f9635-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="f9635-114">Diese neue Klasse kann einem benutzerdefinierten Modell mit einer Abhängigkeit vom Modell **SelfHealingRules** hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f9635-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="f9635-115">Im folgenden Beispiel wird die Regel, die implementiert wird, **RFQTitleSelfHealingRule** genannt.</span><span class="sxs-lookup"><span data-stu-id="f9635-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="f9635-116">Die abstrakte Klasse **SelfHealingRule** hat abstrakte Methoden, die in erbenden Klassen implementiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f9635-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="f9635-117">Der Kern ist die Methode **evaluate**, die eine Liste von Verkaufschancen zurückgibt, die von der Regel identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f9635-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="f9635-118">Verkaufschancen können pro juristische Person sein oder das gesamte System betreffen.</span><span class="sxs-lookup"><span data-stu-id="f9635-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

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

<span data-ttu-id="f9635-119">Die oben gezeigt Methode umfasst Unternehmen und wählt Angebotsanforderungsanfragen mit leeren Titeln in der Methode **findRFQCasesWithEmptyTitle** aus.</span><span class="sxs-lookup"><span data-stu-id="f9635-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="f9635-120">Wenn mindestens eine solche Anfrage gefunden wird, wird eine unternehmensspezifische Verkaufschance mit der Methode **getOpportunityForCompany** erstellt.</span><span class="sxs-lookup"><span data-stu-id="f9635-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="f9635-121">Beachten Sie, dass das Feld **Daten** in der Tabelle **SelfHealingOpportunity** vom Typ **Container** ist, und es kann daher jegliche Daten enthalten, die relevant für die Logik sind, die für diese Regel spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="f9635-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="f9635-122">Durch Festlegen von **OpportunityDate** mit dem aktuellen Zeitstempel wird die Uhrzeit der letzten Bewertung der Verkaufschance registriert.</span><span class="sxs-lookup"><span data-stu-id="f9635-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="f9635-123">Verkaufschancen können auch unternehmensübergreifend sein.</span><span class="sxs-lookup"><span data-stu-id="f9635-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="f9635-124">In diesem Fall ist die Schleife um Unternehmen nicht notwendig und die Verkaufschance muss mit der Methode **getOpportunityAcrossCompanies** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f9635-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="f9635-125">Der folgende Code zeigt die Methode **findRFQCasesWithEmptyTitle**, die die Kennungen der Angebotsanforderungsanfragen zurückgibt, die leere Titel haben.</span><span class="sxs-lookup"><span data-stu-id="f9635-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

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

<span data-ttu-id="f9635-126">Zwei Methoden, die implementiert werden müssen, sind **opportunityTitle** und **opportunityDetails**.</span><span class="sxs-lookup"><span data-stu-id="f9635-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="f9635-127">Erstere gibt einen kurzen Titel für die Verkaufschance zurück, letztere gibt eine detaillierte Beschreibung der Verkaufschance zurück, die auch Daten umfassen kann.</span><span class="sxs-lookup"><span data-stu-id="f9635-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="f9635-128">Der Titel, der durch **opportunityTitle** zurückgegeben wird, wird unter der Spalte **Optimierungsverkaufschance** im Arbeitsbereich **Optimierungsratgeber** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f9635-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="f9635-129">Er wird zudem als der Kopf des Seitenbereichs angezeigt, der mehr Informationen zu der Verkaufschance anzeigt.</span><span class="sxs-lookup"><span data-stu-id="f9635-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="f9635-130">Ordnungsgemäß ist diese Methode mit dem Attribut **DiagnosticRuleSubscription** ausgestattet, das die folgenden Argumente bezieht:</span><span class="sxs-lookup"><span data-stu-id="f9635-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="f9635-131">**Diagnosebereich** – Eine Aufzählung des Typs **DiagnosticArea**, der beschreibt, zu welchem Bereich der Anwendung die Regel gehört, wie beispielsweise **DiagnosticArea::SCM**.</span><span class="sxs-lookup"><span data-stu-id="f9635-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="f9635-132">**Regelname** – Eine Zeichenfolge mit dem Regelname.</span><span class="sxs-lookup"><span data-stu-id="f9635-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="f9635-133">Diese wird unter der Spalte **Regelname** im Formular **Diagnoseüberprüfungsregel** (**DiagnosticsValidationRuleMaintain**) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f9635-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="f9635-134">**Ausführungshäufigkeit** – Eine Aufzählung des Typs **DiagnosticRunFrequency**, die beschreibt, wie oft die Regel ausgeführt werden soll, wie beispielsweise **DiagnosticRunFrequency::Daily**.</span><span class="sxs-lookup"><span data-stu-id="f9635-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="f9635-135">**Regelbeschreibung** – Eine Zeichenfolge mit einer ausführlicheren Beschreibung der Regel.</span><span class="sxs-lookup"><span data-stu-id="f9635-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="f9635-136">Diese wird unter der Spalte **Regelbeschreibung** im Formular **Diagnoseüberprüfungsregel** (**DiagnosticsValidationRuleMaintain**) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f9635-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="f9635-137">Das Attribut **DiagnosticRuleSubscription** ist erforderlich, damit die Regel funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f9635-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="f9635-138">Normalerweise wird es bei **opportunityTitle** verwendet, mit ihm kann jedoch jede Methode oder Klasse ausgestattet werden.</span><span class="sxs-lookup"><span data-stu-id="f9635-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="f9635-139">Hier folgt ein Beispiel einer Implementierung.</span><span class="sxs-lookup"><span data-stu-id="f9635-139">The following is an example implementation.</span></span> <span data-ttu-id="f9635-140">Rohzeichenolgen werden der Einfachheit halber verwendet, aber eine korrekte Implementierung erfordert Beschriftungen.</span><span class="sxs-lookup"><span data-stu-id="f9635-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

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

<span data-ttu-id="f9635-141">Die Beschreibung, die von **opportunityDetails** zurückgegeben wird, wird im Seitenbereich angezeigt, dabei zeigt sie weitere Informationen zur Verkaufschance an.</span><span class="sxs-lookup"><span data-stu-id="f9635-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="f9635-142">Sie nimmt das Argument **SelfHealingOpportunity**, das das Feld **Daten** ist, das verwendet werden kann, um weitere Informationen zur Verkaufschance bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f9635-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="f9635-143">Im Beispiel gibt die Methode die Kennungen der Angebotsanforderungsanfragen mit einem leeren Titel zurück.</span><span class="sxs-lookup"><span data-stu-id="f9635-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

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

<span data-ttu-id="f9635-144">Die beiden verbleibenden zu implementierenden abstrakten Methoden sind **provideHealingAction** und **securityMenuItem**.</span><span class="sxs-lookup"><span data-stu-id="f9635-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="f9635-145">**provideHealingAction** gibt „true” zurück, wenn eine Reparaturaktivität bereitgestellt wird, ansonsten gibt sie „false” zurück.</span><span class="sxs-lookup"><span data-stu-id="f9635-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="f9635-146">Wenn „true” zurückgegeben wird, muss die Methode **performAction** implementierte werden, oder ein Fehler wird ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="f9635-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="f9635-147">Die Methode **performAction** nimmt ein **SelfHealingOpportunity**-Argument, in dem die Daten für die Aktivität verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f9635-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="f9635-148">Im Beispiel öffnet die Aktivität die **PurchRFQCaseTableListPage**, für die manuelle Korrektur.</span><span class="sxs-lookup"><span data-stu-id="f9635-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

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

<span data-ttu-id="f9635-149">Abhängig von den Angaben der Regel kann es nicht möglich, von einer automatischen Aktivität mithilfe der Verkaufschancendaten Gebrauch zu machen.</span><span class="sxs-lookup"><span data-stu-id="f9635-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="f9635-150">In diesem Beispiel könnte das System Titel für Angebotsanforderungsanfragen automatisch generieren.</span><span class="sxs-lookup"><span data-stu-id="f9635-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="f9635-151">**securityMenuItem** gibt den Namen einer Aktivitätsmenüoption zurück, sodass die Regel nur für Benutzer sichtbar ist, die auf die Aktivitätsmenüoption zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="f9635-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="f9635-152">Die Sicherheit kann es unter Umständen erfordern, dass auf bestimmte Regeln und Verkaufschancen nur durch autorisierte Benutzer zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f9635-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="f9635-153">Im Beispiel können nur Benutzer mit Zugriff auf **PurchRFQCaseTitleAction** die Verkaufschance anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f9635-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="f9635-154">Beachten Sie, dass diese Aktivitätsmenüoption für dieses Beispiel erstellt wurde und als Einstiegspunkt für das Sicherheitsrecht **PurchRFQCaseTableMaintain** hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f9635-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

> [!NOTE]
> <span data-ttu-id="f9635-155">Die Menüoption muss eine Aktivitätsmenüoption sein, damit die Sicherheit ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f9635-155">The menu item must be an action menu item for security to work correctly.</span></span> <span data-ttu-id="f9635-156">Andere Menüoptionstypen, wie **Anzeigemenüartikel** funktionieren nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="f9635-156">Other menu item types, such as **Display menu items** will not work correctly.</span></span>

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="f9635-157">Nachdem die Regel kompiliert wurde, führen Sie den folgenden Einzelvorgang aus, damit die Anzeige in der Benutzeroberfläche (UI) erfolgt.</span><span class="sxs-lookup"><span data-stu-id="f9635-157">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

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

<span data-ttu-id="f9635-158">Die Regel wird im Formular **Diagnoseüberprüfungsregel** angezeigt, das von **Systemverwaltung** > **Periodische Aufgaben** > **Diagnoseüberprüfungsregel verwalten** verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f9635-158">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="f9635-159">Damit sie bewertet wird, wechseln Sie zu **Systemverwaltung** > **Periodische Aufgaben** > **Diagnoseüberprüfungsregel planen**, wählen Sie die Häufigkeit der Regel aus, wie beispielsweise **Täglich**.</span><span class="sxs-lookup"><span data-stu-id="f9635-159">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="f9635-160">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9635-160">Click **OK**.</span></span> <span data-ttu-id="f9635-161">Wechseln Sie zu **Systemverwaltung** > **Optimierungsratgeber**, um die neue Verkaufschance anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f9635-161">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="f9635-162">Das folgende Beispiel ist ein Codeausschnitt mit dem Skelett einer Regel einschließlich aller erforderlichen Attribute und Methoden.</span><span class="sxs-lookup"><span data-stu-id="f9635-162">The following example is a code snippet with the skeleton of a rule including all the required methods and attributes.</span></span> <span data-ttu-id="f9635-163">Es ermöglicht, mit dem schreiben neuer Regeln zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="f9635-163">It helps you get started with writing new rules.</span></span> <span data-ttu-id="f9635-164">Die Beschriftungen und die Aktivitätsmenüoptionen, die im Beispiel verwendet werden, gelten nur zu Vorführungszwecken.</span><span class="sxs-lookup"><span data-stu-id="f9635-164">The labels and action menu items that are used in the example are only used for demonstration purpose.</span></span>

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

<span data-ttu-id="f9635-165">Weitere Informationen erhalten Sie in einem kurzen YouTube-Video:</span><span class="sxs-lookup"><span data-stu-id="f9635-165">For more information, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/MRsAzgFCUSQ]

