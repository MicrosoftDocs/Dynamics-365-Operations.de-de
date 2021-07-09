---
title: Was ist neu oder geändert in der Warehouse Management Mobile-App
description: Dieses Thema listet die neuen und geänderten Funktionen für jede freigegebene Version der Warehouse Management Mobile-App für Microsoft Dynamics 365 Supply Chain Management auf.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261778"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="7f39b-103">Was ist neu oder geändert in der Warehouse Management Mobile-App</span><span class="sxs-lookup"><span data-stu-id="7f39b-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f39b-104">Dieses Thema listet neue Funktionen, Korrekturen, Verbesserungen und bekannte Probleme für jede freigegebene Version der Warehouse Management Mobile-App für Microsoft Dynamics 365 Supply Chain Management auf.</span><span class="sxs-lookup"><span data-stu-id="7f39b-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="7f39b-105">Version 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="7f39b-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="7f39b-106">Neue Funktionen, Fehlerbehebungen und Verbesserungen in Version 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="7f39b-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="7f39b-107">Diese Version führt die folgenden neuen Funktionen, Korrekturen und Verbesserungen ein:</span><span class="sxs-lookup"><span data-stu-id="7f39b-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="7f39b-108">Im Demomodus werden jetzt alle Labels in der Gerätesprache angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f39b-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="7f39b-109">Die Wahrscheinlichkeit, dass Sie die folgende Fehlermeldung erhalten, ist geringer: „Es konnte keine passende Ansicht für die angegebene Größe gefunden werden.“</span><span class="sxs-lookup"><span data-stu-id="7f39b-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="7f39b-110">Die Mindesthöhe für Arbeitskarten wurde erhöht (für Fälle, in denen drei oder weniger Felder konfiguriert sind, die in der Arbeitsliste erscheinen sollen).</span><span class="sxs-lookup"><span data-stu-id="7f39b-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="7f39b-111">Die Ränder (Ausblendung) am unteren Rand von Detailkarten wurden verbessert.</span><span class="sxs-lookup"><span data-stu-id="7f39b-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="7f39b-112">Ungültige Symbole in XML-Dateien, die mit dem Server ausgetauscht werden, werden nun korrekt behandelt.</span><span class="sxs-lookup"><span data-stu-id="7f39b-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="7f39b-113">(Zum Beispiel werden nicht druckbare Zeichen jetzt korrekt behandelt und führen nicht mehr dazu, dass die App nicht mehr reagiert).</span><span class="sxs-lookup"><span data-stu-id="7f39b-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="7f39b-114">HTTP-Fehler (z. B. „Fehler 503“) beim Senden einer Serveranforderung werden jetzt korrekt behandelt.</span><span class="sxs-lookup"><span data-stu-id="7f39b-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="7f39b-115">Während ein Fehler angezeigt wird, wird die Optionsliste für Steuerelemente in Kombinationsfeldern nicht mehr automatisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f39b-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="7f39b-116">Die App reagiert nicht mehr aufgrund der Anzeigeausrichtung, die in den Benutzereinstellungen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7f39b-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="7f39b-117">Produktbilder werden jetzt in Self-Service-Umgebungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f39b-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="7f39b-118">(Diese Änderung gilt nur für Versionen mit niedriger Auflösung.</span><span class="sxs-lookup"><span data-stu-id="7f39b-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="7f39b-119">Der Dateiverwaltungsdienst unterstützt keine Bilder in voller Größe in Self-Service-Umgebungen.)</span><span class="sxs-lookup"><span data-stu-id="7f39b-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="7f39b-120">Ein Problem, das das Kommissionieren von Null-Mengen betraf, wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="7f39b-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="7f39b-121">Die App reagiert nicht mehr, wenn eine Detailkarte mehrere identische Felder anzeigt.</span><span class="sxs-lookup"><span data-stu-id="7f39b-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="7f39b-122">Bekannte Probleme in Version 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="7f39b-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="7f39b-123">Die folgenden bekannten Probleme sind in dieser Version vorhanden:</span><span class="sxs-lookup"><span data-stu-id="7f39b-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="7f39b-124">Die App (insbesondere die Arbeitsliste) wird mit der Zeit langsamer.</span><span class="sxs-lookup"><span data-stu-id="7f39b-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="7f39b-125">**Windows-Version:** Wenn eine USB-Pistole zum Scannen unter Windows verwendet wird, werden durch inkonsistente Ergebnisse gescannte Symbole vertauscht.</span><span class="sxs-lookup"><span data-stu-id="7f39b-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="7f39b-126">Version 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="7f39b-126">Version 2.0.5.0</span></span>

<span data-ttu-id="7f39b-127">Diese Version führt die folgenden neuen Funktionen, Korrekturen und Verbesserungen ein:</span><span class="sxs-lookup"><span data-stu-id="7f39b-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="7f39b-128">Das Client-Geheimnis wird beim Einrichten der Verbindungseinstellungen nicht mehr versteckt.</span><span class="sxs-lookup"><span data-stu-id="7f39b-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="7f39b-129">Sie können jetzt lange auf einen beliebigen Text drücken, um ihn vollständig zu sehen.</span><span class="sxs-lookup"><span data-stu-id="7f39b-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="7f39b-130">Die Fehlermeldung beim Fehlen von Speicherberechtigungen wurde verbessert.</span><span class="sxs-lookup"><span data-stu-id="7f39b-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="7f39b-131">Es wurden neue Steuerelemente für einige Flows hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7f39b-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="7f39b-132">Die Schaltfläche „Senden“ wird nicht mehr fälschlicherweise aufgrund der Fenstergröße verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7f39b-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="7f39b-133">Schieberegler können jetzt auf kleineren Bildschirmen weiterlaufen, wenn größere Schaltflächen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f39b-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="7f39b-134">Das Overlay mit vier Schaltflächen wird nicht mehr abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="7f39b-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="7f39b-135">Die Tastatur unterstützt jetzt die DELETE-Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="7f39b-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="7f39b-136">Ein Problem mit der Helligkeit, das beim Drücken der Tastatur auftreten konnte, wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="7f39b-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="7f39b-137">Verschiedene Probleme mit Demo-Daten wurden behoben.</span><span class="sxs-lookup"><span data-stu-id="7f39b-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="7f39b-138">Ein Problem, das numerische Felder auf der Detailseite betraf, wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="7f39b-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="7f39b-139">Die Bildschirmtastatur wird nicht mehr gelegentlich auf einigen Geräten ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="7f39b-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="7f39b-140">Verschiedene Fehler in der Benutzeroberfläche (UI) wurden behoben, z. B. Fehler, die die Hintergrundfarbe und -positionierung betrafen.</span><span class="sxs-lookup"><span data-stu-id="7f39b-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="7f39b-141">Die russischsprachige Benutzeroberfläche wurde verbessert.</span><span class="sxs-lookup"><span data-stu-id="7f39b-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="7f39b-142">Verschiedene Probleme, die dazu führten, dass das System nicht mehr reagierte, wurden behoben.</span><span class="sxs-lookup"><span data-stu-id="7f39b-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="7f39b-143">Ein Problem, das mit dem erneuten Öffnen des Taschenrechners zusammenhing, wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="7f39b-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="7f39b-144">**Android Version:** Ein Problem, das dazu führte, dass Android 4.4 beim Starten nicht mehr reagierte, wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="7f39b-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="7f39b-145">**Android Version:** Die minimale Skalierung wurde auf 50 Prozent reduziert.</span><span class="sxs-lookup"><span data-stu-id="7f39b-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="7f39b-146">Version 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="7f39b-146">Version 2.0.4.0</span></span>

<span data-ttu-id="7f39b-147">Version 2.0.4.0 war die erste allgemein verfügbare Version der Warehouse Management Mobile-App.</span><span class="sxs-lookup"><span data-stu-id="7f39b-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="7f39b-148">Neue Funktionen, Korrekturen und Verbesserungen in Version 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="7f39b-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="7f39b-149">Diese Version führt die folgenden neuen Funktionen, Korrekturen und Verbesserungen ein, die in der Vorschau-Version nicht verfügbar waren:</span><span class="sxs-lookup"><span data-stu-id="7f39b-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="7f39b-150">Wenn eine Detailkarte zwei Labels enthält, die identische Daten haben, wird eines der Labels ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="7f39b-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="7f39b-151">Sonderzeichen werden jetzt standardmäßig angezeigt, und die Option, sie auszublenden, wurde aus den Benutzereinstellungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="7f39b-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="7f39b-152">Deaktivierte Schaltflächen zum Senden werden jetzt in der kompakten Armansicht als nicht verfügbar angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f39b-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="7f39b-153">Eine Änderung der Sequenz-Logik für Steuerelemente sorgt für eine reibungslosere Skalierung über Geräte hinweg.</span><span class="sxs-lookup"><span data-stu-id="7f39b-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="7f39b-154">Daher ist es weniger notwendig, die Skalierung von Schriftarten oder Schaltflächen anzupassen.</span><span class="sxs-lookup"><span data-stu-id="7f39b-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="7f39b-155">Das Standard-Farbdesign wurde auf *Dunkel* geändert.</span><span class="sxs-lookup"><span data-stu-id="7f39b-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="7f39b-156">Das fehlende Symbol für die deaktivierte Schaltfläche „Senden“ wurde in der Menüband-Ansicht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7f39b-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="7f39b-157">Timeout-Ausnahmen führen nun zur Verbindungsseite, anstatt einen Inline-Fehler anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7f39b-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="7f39b-158">Wenn keine Sendeaktion verfügbar ist (wie **OK**, **Ja**, **Akzeptieren**, **Erledigt** oder **Fertig**), wird die Schaltfläche Senden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7f39b-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="7f39b-159">Die Stabilität der Apps wurde verbessert.</span><span class="sxs-lookup"><span data-stu-id="7f39b-159">App stability has been improved.</span></span>
- <span data-ttu-id="7f39b-160">Es gibt einen Fix für die Sicherheitslücke [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span><span class="sxs-lookup"><span data-stu-id="7f39b-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="7f39b-161">**Windows-Version:** Ein Problem unter Windows, bei dem die Menüs nach der Größenänderung des Fensters nicht mehr reagierten, wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="7f39b-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="7f39b-162">Bekanntes Problem in Version 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="7f39b-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="7f39b-163">Das folgende bekannte Problem ist in dieser Version vorhanden:</span><span class="sxs-lookup"><span data-stu-id="7f39b-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="7f39b-164">Diese Version hat ein Problem mit Geräten, die Android 4.4 verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f39b-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="7f39b-165">Es kann zu Problemen kommen, wenn Sie die App auf dieser Android-Version verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f39b-165">You might experience issues when you use the app on this Android version.</span></span>
