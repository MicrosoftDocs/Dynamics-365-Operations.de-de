---
title: Implementieren benutzerdefinierter Felder für die mobile Microsoft Dynamics 365 Project Timesheet-App auf iOS und Android
description: Dieses Thema enthält allgemeine Muster zur Verwendung von Erweiterungen, um benutzerdefinierte Felder zu implementieren.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174872"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="d8fad-103">Implementieren benutzerdefinierter Felder für die mobile Microsoft Dynamics 365 Project Timesheet-App auf iOS und Android</span><span class="sxs-lookup"><span data-stu-id="d8fad-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8fad-104">Dieses Thema enthält allgemeine Muster zur Verwendung von Erweiterungen, um benutzerdefinierte Felder zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="d8fad-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="d8fad-105">Folgende Themen werden behandelt:</span><span class="sxs-lookup"><span data-stu-id="d8fad-105">The following topics are covered:</span></span>

- <span data-ttu-id="d8fad-106">Die verschiedenen Datentypen, die das benutzerdefinierte Feldframework unterstützt</span><span class="sxs-lookup"><span data-stu-id="d8fad-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="d8fad-107">Vorgehensweise beim Anzeigen schreibgeschützter oder bearbeitbarer Felder in Arbeitszeittabelleneinträgen und Speichern von vom Benutzer bereitgestellten Werten zurück in die Datenbank</span><span class="sxs-lookup"><span data-stu-id="d8fad-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="d8fad-108">Vorgehensweise beim Anzeigen schreibgeschützter Felder in der Arbeitszeittabellen-Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="d8fad-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="d8fad-109">Vorgehensweise beim Integrieren anderer benutzerdefinierter Geschäftslogik, um Standardwerte in Felder einzugeben und zusätzliche Auswertung vorzunehmen</span><span class="sxs-lookup"><span data-stu-id="d8fad-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="d8fad-110">Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="d8fad-110">Audience</span></span>

<span data-ttu-id="d8fad-111">Dieses Thema richtet sich an Entwickler, die ihre benutzerdefinierten Felder in die mobile Microsoft Dynamics 365 Project Timesheet-Anwendung integrieren, die für Apple iOS und Google Android verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d8fad-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="d8fad-112">Es wird davon ausgegangen, dass Leser mit der X++-Entwicklung und Projektarbeitszeittabellen-Funktion vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="d8fad-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="d8fad-113">Datenvertrag – TSTimesheetCustomField X++-Klasse</span><span class="sxs-lookup"><span data-stu-id="d8fad-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="d8fad-114">Die Klasse **TSTimesheetCustomField** ist die X++-Datenvertragsklasse, die Informationen zu einem benutzerdefinierten Feld für die Arbeitszeittabellen-Funktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="d8fad-115">Listen der benutzerdefinierten Feldobjekte werden sowohl im TSTimesheetDetails-Datenvertrag als auch im TSTimesheetEntry-Vertrag weitergegeben, um benutzerdefinierte in der mobilen App anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="d8fad-116">**TSTimesheetDetails** – Der Arbeitszeittabellen-Kopfzeilen-Vertrag</span><span class="sxs-lookup"><span data-stu-id="d8fad-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="d8fad-117">**TSTimesheetEntry** – Der Arbeitszeittabellen-Buchungsvertrag.</span><span class="sxs-lookup"><span data-stu-id="d8fad-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="d8fad-118">Gruppen dieser Objekte, die dieselben Projektinformationen und denselben **timesheetLineRecId**-Wert haben, stellen eine Position dar.</span><span class="sxs-lookup"><span data-stu-id="d8fad-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="d8fad-119">fieldBaseType (Typen)</span><span class="sxs-lookup"><span data-stu-id="d8fad-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="d8fad-120">Die Eigenschaft **FieldBaseType** im Objekt **TsTimesheetCustom** bestimmt den Typ des Felds, das in der App angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8fad-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="d8fad-121">Die folgenden **Typen**-Werte, die unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="d8fad-122">Typenwert</span><span class="sxs-lookup"><span data-stu-id="d8fad-122">Types value</span></span> | <span data-ttu-id="d8fad-123">Typ</span><span class="sxs-lookup"><span data-stu-id="d8fad-123">Type</span></span>              | <span data-ttu-id="d8fad-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8fad-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="d8fad-125">0</span><span class="sxs-lookup"><span data-stu-id="d8fad-125">0</span></span>           | <span data-ttu-id="d8fad-126">Zeichenfolge und (Enumeration)</span><span class="sxs-lookup"><span data-stu-id="d8fad-126">String (and Enum)</span></span> | <span data-ttu-id="d8fad-127">Das Feld wird als Textfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="d8fad-128">1</span><span class="sxs-lookup"><span data-stu-id="d8fad-128">1</span></span>           | <span data-ttu-id="d8fad-129">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="d8fad-129">Integer</span></span>           | <span data-ttu-id="d8fad-130">Der Wert wird als Anzahl ohne Dezimalstellen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="d8fad-131">2</span><span class="sxs-lookup"><span data-stu-id="d8fad-131">2</span></span>           | <span data-ttu-id="d8fad-132">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="d8fad-132">Real</span></span>              | <span data-ttu-id="d8fad-133">Der Wert wird als Anzahl mit Dezimalstellen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="d8fad-134">Zum Anzeigen des realen Werts als Währung in der App, verwenden Sie die Eigenschaft **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="d8fad-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="d8fad-135">Sie können die Eigenschaft **numberOfDecimals** verwenden, um die Anzahl von Dezimalstellen festzulegen, die angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="d8fad-136">3</span><span class="sxs-lookup"><span data-stu-id="d8fad-136">3</span></span>           | <span data-ttu-id="d8fad-137">Datum</span><span class="sxs-lookup"><span data-stu-id="d8fad-137">Date</span></span>              | <span data-ttu-id="d8fad-138">Datumsformate werden durch die Einstellung **Datum, Uhrzeit und Zahlenformat** des Benutzers bestimmt, die unter **Einstellung von Sprache und Land/Region** unter **Benutzeroptionen** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d8fad-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="d8fad-139">4</span><span class="sxs-lookup"><span data-stu-id="d8fad-139">4</span></span>           | <span data-ttu-id="d8fad-140">Aktiv</span><span class="sxs-lookup"><span data-stu-id="d8fad-140">Boolean</span></span>           | |
| <span data-ttu-id="d8fad-141">15</span><span class="sxs-lookup"><span data-stu-id="d8fad-141">15</span></span>          | <span data-ttu-id="d8fad-142">GUID</span><span class="sxs-lookup"><span data-stu-id="d8fad-142">GUID</span></span>              | |
| <span data-ttu-id="d8fad-143">16</span><span class="sxs-lookup"><span data-stu-id="d8fad-143">16</span></span>          | <span data-ttu-id="d8fad-144">Int64</span><span class="sxs-lookup"><span data-stu-id="d8fad-144">Int64</span></span>             | |

- <span data-ttu-id="d8fad-145">Wenn die Eigenschaft **stringOptions** nicht im Objekt **TSTimesheetCustomField** angegeben ist, wird dem Benutzer ein Freitextfeld bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="d8fad-146">Die Eigenschaft **stringLength** kann verwendet werden, um die maximale Zeichenfolgenlänge festzulegen, die Benutzer eingeben können.</span><span class="sxs-lookup"><span data-stu-id="d8fad-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="d8fad-147">Wenn die Eigenschaft **stringOptions** im Objekt **TSTimesheetCustomField** bereitgestellt wird, sind diese Listenelemente die einzigen Werte, die Benutzer auswählen können, indem sie Optionsfelder (Optionsfelder) verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="d8fad-148">In diesem Fall kann das Zeichenfolgenfeld als ein Enumerationswert für den Zweck des Benutzereintrags dienen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="d8fad-149">Um den Wert in der Datenbank als Enumeration zu speichern, weisen Sie den Zeichenfolgenwert manuell dem Enumerationswert zurück zu, bevor Sie ihn in der Datenbank mithilfe einer Befehlskette speichern (im Abschnitt „Verwenden einer Befehlskette in der TSTimesheetEntryService-Klasse, um einen Arbeitszeittabelleneintrag aus der App wieder in der Datenbank zu speichern“ später in diesem Thema finden Sie ein Beispiel).</span><span class="sxs-lookup"><span data-stu-id="d8fad-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="d8fad-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="d8fad-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="d8fad-151">Sie können diese Eigenschaft verwenden, um tatsächliche Werte als Währung zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="d8fad-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="d8fad-152">Dieser Ansatz ist nur anwendbar, wenn der **fieldBaseType**-Wert **Tatsächlich** ist.</span><span class="sxs-lookup"><span data-stu-id="d8fad-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="d8fad-153">**TSCustomFieldExtendedType:None** – Keine Formatierung wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="d8fad-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="d8fad-154">**TSCustomFieldExtendedType::Currency** – Formatieren Sie den Wert als Währung.</span><span class="sxs-lookup"><span data-stu-id="d8fad-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="d8fad-155">Wenn die Währungsformatierung aktiv ist, kann das Feld **stringValue** verwendet werden, um den Währungscode weiterzugeben, der in der App angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8fad-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="d8fad-156">Der Wert ist ein schreibgeschützter Wert.</span><span class="sxs-lookup"><span data-stu-id="d8fad-156">The value is a read-only value.</span></span>

    <span data-ttu-id="d8fad-157">Das Feld **realValue** enthält den Geldbetrag, der in der Datenbank gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8fad-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="d8fad-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="d8fad-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="d8fad-159">Sie können diese Eigenschaft verwenden, um anzugeben, wo das benutzerdefinierte Feld in der App angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8fad-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="d8fad-160">**TSCustomFieldSection::Header** – Das Feld wird im Abschnitt **Weitere Details anzeigen** in der App angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="d8fad-161">Diese Felder sind immer schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-161">These fields are always read-only.</span></span>
- <span data-ttu-id="d8fad-162">**TSCustomFieldSection::Line** – Das Feld wird nach den gesamten vorkonfigurierten Positionsfeldern in Zeittabelleneinträgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="d8fad-163">Diese Felder können entweder bearbeitbar oder schreibgeschützt sein.</span><span class="sxs-lookup"><span data-stu-id="d8fad-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="d8fad-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="d8fad-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="d8fad-165">Diese Eigenschaft identifiziert das Feld, wenn Werte, die die App bereitstellt, wieder in der Datenbank gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="d8fad-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="d8fad-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="d8fad-167">Diese Eigenschaft identifiziert das Feld, wenn Werte, die die App bereitstellt, wieder in der Datenbank gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="d8fad-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="d8fad-168">isEditable (NoYes)</span></span>

<span data-ttu-id="d8fad-169">Legen Sie diese Eigenschaft auf **Ja** fest, um anzugeben, dass das Feld im Arbeitszeittabellen-Eintragsabschnitt von Benutzern bearbeitbar sein soll.</span><span class="sxs-lookup"><span data-stu-id="d8fad-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="d8fad-170">Legen Sie die Eigenschaft auf **Nein** fest, damit das Feld schreibgeschützt wird.</span><span class="sxs-lookup"><span data-stu-id="d8fad-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="d8fad-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="d8fad-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="d8fad-172">Legen Sie diese Eigenschaft auf **Ja** fest, um anzugeben, dass das Feld im Arbeitszeittabellen-Eintragsabschnitt obligatorisch sein soll.</span><span class="sxs-lookup"><span data-stu-id="d8fad-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="d8fad-173">Bezeichnung (str)</span><span class="sxs-lookup"><span data-stu-id="d8fad-173">label (str)</span></span>

<span data-ttu-id="d8fad-174">Diese Eigenschaft gibt die Bezeichnung an, die neben dem Feld in der App angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8fad-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="d8fad-175">stringOptions (Liste der Zeichenfolgen)</span><span class="sxs-lookup"><span data-stu-id="d8fad-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="d8fad-176">Diese Eigenschaft ist nur anwendbar, wenn **fieldBaseType** auf **Zeichenfolge** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d8fad-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="d8fad-177">Wenn **stringOptions** festgelegt ist, werden die Zeichenfolgenwerte, die zur Auswahl mittels Optionsfelder (Optionsfelder) verfügbar sind, durch die Zeichenfolgen in der Liste angegeben.</span><span class="sxs-lookup"><span data-stu-id="d8fad-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="d8fad-178">Wenn keine Zeichenfolgen bereitgestellt werden, ist der Freitexteintrag im Zeichenfolgenfeld zulässig (im Abschnitt „Verwenden von Befehlskette in der TSTimesheetEntryService-Klasse, um einen Arbeitszeittabellen-Eintrag aus der App wieder in der Datenbank zu speichern“ später in diesem Thema finden Sie ein Beispiel).</span><span class="sxs-lookup"><span data-stu-id="d8fad-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="d8fad-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="d8fad-179">stringLength (int)</span></span>

<span data-ttu-id="d8fad-180">Diese Eigenschaft gibt die maximale Länge für ein Zeichenfolgenfeld an.</span><span class="sxs-lookup"><span data-stu-id="d8fad-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="d8fad-181">Sie ist nur anwendbar, wenn **fieldBaseType** auf **Zeichenfolge** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d8fad-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="d8fad-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="d8fad-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="d8fad-183">Diese Eigenschaft gibt die Anzahl von Dezimalstellen an, die für ein tatsächliches Feld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="d8fad-184">Sie ist nur anwendbar, wenn **fieldBaseType** auf **Tatsächlich** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d8fad-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="d8fad-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="d8fad-185">orderSequence (int)</span></span>

<span data-ttu-id="d8fad-186">Diese Eigenschaft steuert die Reihenfolge, in der benutzerdefinierte Felder in der App angezeigt werden, wenn mehr als ein benutzerdefiniertes Feld angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d8fad-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="d8fad-187">Felder, die niedrigere Zahlen besitzen, werden zuerst angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="d8fad-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="d8fad-188">booleanValue (boolean)</span></span>

<span data-ttu-id="d8fad-189">Für Felder des Typs **Boolesch** gibt diese Eigenschaft den booleschen Wert des Felds zwischen dem Server und der App weiter.</span><span class="sxs-lookup"><span data-stu-id="d8fad-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="d8fad-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="d8fad-190">guidValue (guid)</span></span>

<span data-ttu-id="d8fad-191">Für Felder des Typs **GUID** gibt diese Eigenschaft den Wert des global eindeutigen Bezeichners (GUID) des Felds zwischen dem Server und der App weiter.</span><span class="sxs-lookup"><span data-stu-id="d8fad-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="d8fad-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="d8fad-192">int64Value (int64)</span></span>

<span data-ttu-id="d8fad-193">Für Felder des Typs **Int64** gibt diese Eigenschaft den int64-Wert des Felds zwischen dem Server und der App weiter.</span><span class="sxs-lookup"><span data-stu-id="d8fad-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="d8fad-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="d8fad-194">intValue (int)</span></span>

<span data-ttu-id="d8fad-195">Für Felder des Typs **Int** gibt diese Eigenschaft den int-Wert des Felds zwischen dem Server und der App weiter.</span><span class="sxs-lookup"><span data-stu-id="d8fad-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="d8fad-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="d8fad-196">realValue (real)</span></span>

<span data-ttu-id="d8fad-197">Für Felder des Typs **Tatsächlich** gibt diese Eigenschaft den tatsächlichen Wert des Felds zwischen dem Server und der App weiter.</span><span class="sxs-lookup"><span data-stu-id="d8fad-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="d8fad-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="d8fad-198">stringValue (str)</span></span>

<span data-ttu-id="d8fad-199">Für Felder des Typs **Zeichenfolge** gibt diese Eigenschaft den Zeichenfolgenwert des Felds zwischen dem Server und der App weiter.</span><span class="sxs-lookup"><span data-stu-id="d8fad-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="d8fad-200">Sie wird auch für Felder des Typs **Tatsächlich** verwendet, die als Währung formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="d8fad-201">Für diese Felder wird die Eigenschaft verwendet, um den Währungscode an die App weiterzugeben.</span><span class="sxs-lookup"><span data-stu-id="d8fad-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="d8fad-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="d8fad-202">dateValue (date)</span></span>

<span data-ttu-id="d8fad-203">Für Felder des Typs **Datum** gibt diese Eigenschaft den Datumswert des Felds zwischen dem Server und der App weiter.</span><span class="sxs-lookup"><span data-stu-id="d8fad-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="d8fad-204">Anzeigen und Speichern eines benutzerdefinierten Felds im Abschnitt Arbeitszeittabellen-Eintrag</span><span class="sxs-lookup"><span data-stu-id="d8fad-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="d8fad-205">Unten befindet sich ein Bildschirmfoto von der mobilen App. Es zeigt eine Arbeitszeittabellen-Eintragserstellung</span><span class="sxs-lookup"><span data-stu-id="d8fad-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="d8fad-206">Er zeigt die vorkonfigurierten Felder und ein benutzerdefiniertes Feld im Abschnitt „Zeiteintrag“, der „Testzeichenfolge“ bezeichnet wird, bei dem ein Enumerationswert „Zweite Option“ bereits festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d8fad-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Benutzerdefiniertes Testzeichenfolgen-Feld in der App](media/timesheet-entry.jpg)



<span data-ttu-id="d8fad-208">Unten ist ein Bildschirmfoto der mobilen App des Benutzers, der eine der Enumerationsoptionen auswählt, die für das benutzerdefinierte Feld „Testzeichenfolge“ verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d8fad-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="d8fad-209">Die zwei Optionen sind „Erste Option“ und „Zweite Option“, die als Optionsfelder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="d8fad-210">Die zweite Option ist derzeit ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-210">The second option is currently selected.</span></span>

![Optionsfelder (Optionsfelder) für benutzerdefinierte Feld „Testzeichenfolge“](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="d8fad-212">Erweitern der TSTimesheetLine-Tabelle, sodass sie ein benutzerdefiniertes Feld hat</span><span class="sxs-lookup"><span data-stu-id="d8fad-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="d8fad-213">In typischen Szenarien ist es wahrscheinlich, dass die Daten für ein benutzerdefiniertes Feld im Abschnitt Arbeitszeittabelleneintrag in der Tabelle TSTimesheetLine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="d8fad-214">Allerdings können andere Tabellen verwendet werden, wenn die Daten auf Basis eines TSTimesheetTrans-Datensatzes abgerufen werden können, oder wenn sie keinen spezifischen Datensatzkontext haben (beispielsweise wenn das Feld in den Projektparametern als schreibgeschützt festgelegt wird).</span><span class="sxs-lookup"><span data-stu-id="d8fad-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="d8fad-215">Beachten Sie, dass benutzerdefinierte Felder keine unterstützenden Datenbank-Datensätze haben müssen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="d8fad-216">Sie können auf Grundlage der X++-Logik dynamisch generiert werden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="d8fad-217">Dieser Ansatz kann bei schreibgeschützten Szenarien nützlich sein (im Abschnitt „Befehlskettenbefehl in der TSTimesheetDetails class-Klasse, buildCustomFieldListForHeader-Methode verwenden, um Arbeitszeittabellendetails auszufüllen“ finden Sie ein Beispiel dynamisch generierter benutzerdefinierter Feldwerte.)</span><span class="sxs-lookup"><span data-stu-id="d8fad-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="d8fad-218">Unten ist ein Bildschirmfoto von Visual Studio, das die Entwicklungsumgebung zeigt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="d8fad-219">Er zeigt eine Erweiterung der TSTimesheetLine-Tabelle mit dem Feld TestLineString an, das als benutzerdefiniertes Feld hinzugefügt ist.</span><span class="sxs-lookup"><span data-stu-id="d8fad-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Positionszeichenfolge](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="d8fad-221">Verwenden der Befehlskette in der Methode buildCustomFieldList der Klasse TSTimesheetSettings zum Anzeigen eines Felds im Arbeitszeittabelleneintrags-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d8fad-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="d8fad-222">Dieser Code steuert die Anzeigeeinstellungen für das Feld in der App.</span><span class="sxs-lookup"><span data-stu-id="d8fad-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="d8fad-223">Er steuert beispielsweise den Feldtyp, die Bezeichnung, ob das Feld ein Pflichtfeld ist und in welchem Abschnitt das Feld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8fad-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="d8fad-224">Im folgenden Beispiel wird ein Zeichenfolgenfeld in Zeiteinträgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="d8fad-225">Dieses Feld enthält zwei Optionen, **Erste Option** und **Zweite Option**, die über Optionsfelder (Optionsfelder) verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d8fad-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="d8fad-226">Das Feld in der App ist dem Feld **TestLineString** zugeordnet, das der Tabelle TSTimesheetLine-Tabelle hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d8fad-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="d8fad-227">Beachten Sie die Verwendung der **TSTimesheetCustomField::newFromMetatdata()**-Methode, um die Initialisierung der Eigenschaften benutzerdefinierter Felder zu vereinfachen: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** und **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="d8fad-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="d8fad-228">Sie können diese Parameter auch manuell festlegen, wenn Sie dies bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-228">You can also set these parameters manually, as you prefer.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="d8fad-229">Verwenden der Befehlskette in der Methode buildCustomFieldListForEntry der Klasse TSTimesheetEntry zum Eingeben von Werten in einem Arbeitszeittabelleneintrag</span><span class="sxs-lookup"><span data-stu-id="d8fad-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="d8fad-230">Die Methode **buildCustomFieldListForEntry** wird verwendet, um Werte in den gespeicherten Arbeitszeittabellen-Positionen in der mobilen App einzugeben.</span><span class="sxs-lookup"><span data-stu-id="d8fad-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="d8fad-231">Sie übernimmt einen TSTimesheetTrans-Datensatz als Parameter.</span><span class="sxs-lookup"><span data-stu-id="d8fad-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="d8fad-232">Felder aus diesem Datensatz können verwendet werden, um den benutzerdefinierten Feldwert in der App auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="d8fad-233">Verwenden von Befehlskette in der Klasse TSTimesheetEntryService zum erneuten Speichern eines Arbeitszeittabellen-Eintrags aus der App in der Datenbank</span><span class="sxs-lookup"><span data-stu-id="d8fad-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="d8fad-234">Um ein benutzerdefiniertes Feld in typischer Verwendung wieder in die Datenbank zu speichern, müssen Sie mehrere Methoden erweitern:</span><span class="sxs-lookup"><span data-stu-id="d8fad-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="d8fad-235">Die Methode **timesheetLineNeedsUpdating** wird verwendet, um zu bestimmen, ob der Positionsdatensatz vom Benutzer in der App geändert wurde und in der Datenbank gespeichert werden muss.</span><span class="sxs-lookup"><span data-stu-id="d8fad-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="d8fad-236">Wenn Leistung keine Rolle spielt, kann diese Methode vereinfacht werden, damit sie immer **true** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="d8fad-237">Die Methoden **populateTimesheetLineFromEntryDuringCreate** und **populateTimesheetLineFromEntryDuringUpdate** können auch erweitert werden, sodass sie Werte im Datenbank-Datensatz TSTimesheetLine aus dem bereitgestellten TSTimesheetEntry-Datenvertrags-Datensatz eingeben.</span><span class="sxs-lookup"><span data-stu-id="d8fad-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="d8fad-238">Beachten Sie im folgenden Beispiel, wie die Zuordnung zwischen dem Datenbankfeld und dem Eingabefeld manuell über den X++-Code erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="d8fad-239">Die Methode **populateTimesheetWeekFromEntry** kann auch erweitert werden, wenn das benutzerdefinierte Feld, das dem Objekt **TSTimesheetEntry** zugeordnet ist, erneut in die Datenbanktabelle TSTimesheetLineweek schreiben muss.</span><span class="sxs-lookup"><span data-stu-id="d8fad-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="d8fad-240">Das folgende Beispiel speichert die Werte **firstOption** oder **secondOption**, die der Benutzer auswählt, in der Datenbank als unformatierter Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="d8fad-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="d8fad-241">Wenn das Datenbankfeld ein Feld vom Typ **Enumeration** ist, können diese Werte manuell einem Enumerationswwert zugeordnet werden und dann in einem Enumerationsfeld in der Datenbanktabelle gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="d8fad-242">Anzeigen eines benutzerdefinierten Felds im Abschnitt Arbeitszeittabellen-Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="d8fad-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="d8fad-243">Unten befindet sich ein Bildschirmfoto von der mobilen App. Es zeigt einen Benutzer, der die Arbeitszeittabelle anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="d8fad-244">Die Schaltfläche „Weitere Informationen“ in der rechten oberen Ecke ist ausgewählt worden, um die Option „Weitere Details anzeigen“ anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Weitere Details anzeigen – Befehl](media/show-more.png)



<span data-ttu-id="d8fad-246">Unten befindet sich ein Bildschirmfoto von der mobilen App. Es zeigt den Abschnitt „Mehr“ in der Arbeitszeittabelle.</span><span class="sxs-lookup"><span data-stu-id="d8fad-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="d8fad-247">Ein benutzerdefiniertes Feld mit der Bezeichnung „Benutzungsrate der Arbeitszeittabelle (berechnetes benutzerdefiniertes Feld)“ ist dem Arbeitszeittabellen-Kopfzeilenabschnitt hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="d8fad-248">Ein schreibgeschützter Wert „0,667“ ist im benutzerdefinierten Feld festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Weiterer Abschnitt](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="d8fad-250">Erweitern der TSTimesheetTable-Tabelle, sodass sie ein benutzerdefiniertes Feld hat</span><span class="sxs-lookup"><span data-stu-id="d8fad-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="d8fad-251">In typischen Szenarien ist es wahrscheinlich, dass die Daten für ein benutzerdefiniertes Feld im Kopfzeilenabschnitt aus der TSTimesheetHeader-Tabelle entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="d8fad-252">Allerdings können andere Tabellen verwendet werden, wenn die Daten auf Basis eines TSTimesheetTable-Datensatzes abgerufen werden können, oder wenn sie keinen spezifischen Datensatzkontext haben (beispielsweise wenn das Feld in den Projektparametern als schreibgeschützt festgelegt wird).</span><span class="sxs-lookup"><span data-stu-id="d8fad-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="d8fad-253">Beachten Sie, dass benutzerdefinierte Felder keine unterstützenden Datenbank-Datensätze haben müssen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="d8fad-254">Sie können auf Grundlage der X++-Logik dynamisch generiert werden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="d8fad-255">Das Beispiel, das folgt, zeigt diesen Ansatz.</span><span class="sxs-lookup"><span data-stu-id="d8fad-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="d8fad-256">Felder im Kopfzeilenabschnitt sind immer in der App immer schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="d8fad-257">Verwenden der Befehlskette in der Methode buildCustomFieldList der Klasse TSTimesheetSettings zum Anzeigen eines Felds im Kopfzeilenabschnitt</span><span class="sxs-lookup"><span data-stu-id="d8fad-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="d8fad-258">Dieser Code steuert die Anzeigeeinstellungen für das Feld in der App.</span><span class="sxs-lookup"><span data-stu-id="d8fad-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="d8fad-259">Er steuert beispielsweise den Feldtyp, die Bezeichnung, ob das Feld ein Pflichtfeld ist und in welchem Abschnitt das Feld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8fad-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="d8fad-260">Das folgende Beispiel zeigt einen berechneten Wert im Kopfzeilenabschnitt in der App an.</span><span class="sxs-lookup"><span data-stu-id="d8fad-260">The following example shows a computed value in the header section in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="d8fad-261">Verwenden der Befehlskette in der Methode buildCustomFieldListForHeader der Klasse TSTimesheetDetails zum Eingeben von Werten in Arbeitszeittabellen-Details</span><span class="sxs-lookup"><span data-stu-id="d8fad-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="d8fad-262">Die Methode **buildCustomFieldListForHeader** wird verwendet, um die Arbeitszeittabellen-Kopfzeilendetails in der mobilen App einzugeben.</span><span class="sxs-lookup"><span data-stu-id="d8fad-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="d8fad-263">Sie übernimmt einen TSTimesheetTable-Datensatz als Parameter.</span><span class="sxs-lookup"><span data-stu-id="d8fad-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="d8fad-264">Felder aus diesem Datensatz können verwendet werden, um den benutzerdefinierten Feldwert in der App auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="d8fad-265">Im folgenden Beispiel werden keine Werte aus der Datenbank gelesen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="d8fad-266">Stattdessen wird eine X++-Logik verwendet, um einen berechneten Wert zu generieren, der dann in der App angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8fad-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="d8fad-267">Andere Konfigurierberkeits-/Erweiterbarkeits-Verkaufschancen</span><span class="sxs-lookup"><span data-stu-id="d8fad-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="d8fad-268">Zusätzliche Überprüfung für die App hinzufügen</span><span class="sxs-lookup"><span data-stu-id="d8fad-268">Adding additional validation for the app</span></span>

<span data-ttu-id="d8fad-269">Vorhandene Logik für die Arbeitszeittabellen-Funktion auf der Datenbankebene funktioniert noch wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="d8fad-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="d8fad-270">Um den Abschluss der Speicher- oder Sendevorgänge zu unterbrechen und eine spezifische Fehlermeldung anzuzeigen, können Sie dem Code **throw error("message to user")** über eine Befehlskettenerweiterung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="d8fad-271">Nachfolgend finden Sie drei Beispiele von nützlichen erweiterbaren Methoden:</span><span class="sxs-lookup"><span data-stu-id="d8fad-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="d8fad-272">Wenn **validateWrite** in der TSTimesheetLine-Tabelle **false** während eines Speichervorgangs für eine Arbeitszeittabellen-Position zurückgibt, wird eine Fehlermeldung in der mobilen App angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="d8fad-273">Wenn **validateSubmit** in der TSTimesheetTable-Tabelle **false** während der Arbeitszeittabellen-Übermittlung in der App zurückgibt, wird dem Benutzer eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="d8fad-274">Logik die Felder ausfüllt (zum Beispiel **Positionseigenschaft**) während die **insert**-Methode in der Tabelle TSTimesheetLine immer noch ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8fad-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="d8fad-275">Ausblenden und Markieren vorkonfigurierter Felder als schreibgeschützt über eine Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d8fad-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="d8fad-276">Von den Projektparametern aus können Sie vorkonfigurierte Felder in der mobilen App mit einem Schreibschutz versehen oder ausblenden.</span><span class="sxs-lookup"><span data-stu-id="d8fad-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="d8fad-277">Legen Sie die Optionen im Abschnitt **Mobile Arbeitszeittabellen** unter der Registerkarte **Arbeitszeittabelle** der Seite **Projektverwaltungs- und Buchhaltungsparameter** fest.</span><span class="sxs-lookup"><span data-stu-id="d8fad-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projektparameter](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="d8fad-279">Die Aktivitäten ändern, die zur Auswahl über Erweiterungen verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="d8fad-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="d8fad-280">Die Aktivitäten, die zur Auswahl für ein Projekt verfügbar sind, werden über die Methoden **getActivitiesForProject()** und **getActivityQuery()** in der Klasse **TsTimesheetProjectService** eingegeben.</span><span class="sxs-lookup"><span data-stu-id="d8fad-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="d8fad-281">Sie können eine Befehlskette verwenden, um dieses Verhalten zu ändern, damit es Ihrem Geschäftsszenario entspricht. Das gilt für die Aktivitäten, die für ein bestimmtes Projekt zur Auswahl stehen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="d8fad-282">Eingeben einer Standardprojektkategorie in Arbeitszeittabellen-Einträge</span><span class="sxs-lookup"><span data-stu-id="d8fad-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="d8fad-283">Eingabe einer standardmäßigen Projektkategorie in Arbeitszeittabellen-Einträgen erfolgt auf drei Ebenen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="d8fad-284">Sie können Befehlsketten verwenden, um das Verhalten auf irgendeine oder alle dieser Ebenen auszudehnen, um das gewünschte Verhalten zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="d8fad-285">Die folgende Hierarchie wird verwendet:</span><span class="sxs-lookup"><span data-stu-id="d8fad-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="d8fad-286">Die App versucht, die Standardkategorie aus der Projektressource zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="d8fad-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="d8fad-287">Diese Standardkategorie wird in den Methoden **getCurrentUserResource** und **getDelegatedResourcesForCurrentUser** in der Klasse **TSTimesheetSettingsService** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="d8fad-288">Wenn die Standardkategorie nicht auf der Projektressourcenebene bereitgestellt wird, versucht die App, sie aus der Projektaktivität zu beziehen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="d8fad-289">Diese Standardkategorie wird in der Methode **getActivitiesForProject** in der Klasse **TSTimesheetProjectService** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="d8fad-290">Wenn die Standardkategorie nicht auf der Projektaktivitätsebene bereitgestellt wird, wird die Standardkategorie aus den Projektparametern bezogen.</span><span class="sxs-lookup"><span data-stu-id="d8fad-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="d8fad-291">Diese Standardkategorie wird in der Methode **getProjectDetailsbyRule** in der Klasse **TSTimesheetProjectService** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d8fad-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
