---
title: Schritttitel und Anweisungen für die mobile Warehouse Management-App anpassen
description: Dieses Thema beschreibt, wie Sie angepasste Anweisungen für jeden Schritt jedes Task Flows erstellen und anzeigen, den Sie für die Mobile-App von Warehouse Management festgelegt haben.
author: MarkusFogelberg
ms.date: 08/11/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-08-11
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 112f4ab1d4ed6081ca14e93c3767139ccf95c9f7
ms.sourcegitcommit: 3d05bb2a423fe130700686ff73daa355d15b0e09
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386146"
---
# <a name="customize-step-titles-and-instructions-for-the-warehouse-management-mobile-app"></a>Schritttitel und Anweisungen für die mobile Warehouse Management-App anpassen

> [!IMPORTANT]
> Die Funktionen, die in diesem Thema beschrieben werden, gelten nur für die neue Warehouse Management Mobile-App. Sie betreffen nicht die alte Lager-App, die jetzt außer Betrieb genommen ist.

Dieses Thema beschreibt, wie Sie angepasste Anweisungen für jeden Schritt jedes Task Flows erstellen und anzeigen, den Sie für die Warehouse Management Mobile-App festgelegt haben. Wenn die Arbeitskräfte im Lager gut geschriebene Anweisungen erhalten, können sie sofort mit der Verwendung neuer Flows beginnen, ohne dass eine vorherige Schulung erforderlich ist. Diese Funktion bietet die folgenden Vorteile:

- **Beschleunigen Sie die Einarbeitung der Arbeitskräfte, indem Sie sie einfache Anweisungen für jeden Aufgabenschritt befolgen lassen.** Jeder Schritt eines Flows enthält Anweisungen, die es den Arbeitskräften an der Front ermöglichen, die Aufgabe zu verstehen.
- **Bieten Sie Anweisungen an, die zu Ihren eigenen Prozessen passen.** Schreiben Sie Ihre eigenen Anweisungen, die zu Ihren Geschäfts- und Lagerprozessen passen. Zum Beispiel können Sie die Terminologie an Ihre räumlichen Gegebenheiten und lokalen Abkürzungen anpassen.

## <a name="turn-on-the-warehouse-app-step-instructions-feature"></a>Aktivieren Sie die Funktion "Schrittanweisungen" der App Lager

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Admins können die Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu prüfen und sie einzuschalten. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Name der Funktion:** *Schrittanweisungen für die App "Lager"*

## <a name="step-titles-and-step-instructions-in-the-app"></a>Schritttitel und Schrittanweisungen in der App

Jeder Schritt in einem Task Flow in der Mobile-App von Warehouse Management wird durch eine Schritt-ID identifiziert. Zusätzlich hat jeder Schritt einen Titel, ein Symbol und eine Anweisung. (Weitere Informationen finden Sie unter [Schritt-Symbole und -Titel für die Mobile-App von Warehouse Management zuweisen](step-icons-titles.md)).

### <a name="step-titles"></a>Schritt-Titel

Ein *Schritttitel* ist eine kurze Beschreibung dessen, was eine Arbeitskraft während eines Schritts tun soll. Er erscheint als großer Text am oberen Rand des Bildschirms, wie in der folgenden Abbildung gezeigt.

![Beispiel für einen Schritttitel in der Mobile-App Warehouse Management](media/wma-step-title.png "Beispiel für einen Schritttitel in der Mobile-App Warehouse Management")

> [!TIP]
> Aufgrund der großen Textgröße sollten Sie versuchen, Schritttitel so kurz wie möglich zu halten. Andernfalls könnte der Text abgeschnitten werden. Bei langen Titeln können die Arbeitskräfte jedoch immer noch den Titel drücken und halten, um ein Dialogfeld zu öffnen, das den vollständigen Text anzeigt.

### <a name="step-instructions"></a>Schrittanweisungen

Eine *Schrittanweisung* ist eine längere Beschreibung, die mehr Informationen darüber liefert, was eine Arbeitskraft während eines Schritts tun sollte. Sie erscheint in einem Popup-Dialogfeld, wie in der folgenden Abbildung gezeigt.

![Beispiel für eine Schrittanweisung in der Mobile-App Warehouse Management](media/wma-step-instructions.png "Beispiel für eine Schrittanweisung in der Mobile-App Warehouse Management")

Die Schrittanweisung wird automatisch angezeigt, wenn ein Schritt geöffnet wird. Arbeitskräfte können sie ausblenden, indem sie auf eine beliebige Stelle außerhalb des Popup-Dialogfelds tippen. Zusätzlich enthält das Dialogfeld ein **Nicht mehr anzeigen**-Kontrollkästchen, das Arbeitskräfte aktivieren können, um zu verhindern, dass die Anweisung beim nächsten Mal, wenn sie dieselbe Aufgabe ausführen, angezeigt wird.

## <a name="load-the-default-setup"></a>Laden der Standardeinrichtung

Wenn Sie die Funktion *Schrittanweisungen für Apps im Lager* zum ersten Mal einschalten, enthält Ihr System keine anpassbaren Schritttitel oder Anweisungen. Daher sollten Sie als erstes die Standardeinrichtung laden. Die Standardeinrichtung bietet Texte für alle verfügbaren Schritt-IDs in jeder unterstützten Sprache. Um die Standardeinrichtung zu laden, gehen Sie wie folgt vor.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> Mobiles Gerät \> Mobiles Gerät Schritte**.
1. Wählen Sie im Aktionsbereich **Standardsetup erstellen** aus. Die Seite wird mit den Standardschritten ausgefüllt.

## <a name="customize-step-titles-and-instructions"></a>Anpassen von Schritttiteln und Anweisungen

Um den Titel und/oder die Anleitung für einen Schritt in einer beliebigen Anzahl von Sprachen anzupassen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> Mobiles Gerät \> Mobiles Gerät Schritte**.

    Die Seite **Mobilgeräteschritte** listet jeden Schritt auf, der für Ihr System verfügbar ist. Jede Schritt-ID kann von einer beliebigen Anzahl von Menüelementen des mobilen Geräts gemeinsam genutzt werden. Wenn eine Schritt-ID von mehreren Menüpunkten gemeinsam genutzt wird, werden derselbe Titel und dieselbe Anweisung für alle diese Menüpunkte angezeigt. Sie können jedoch Überschreibungen erstellen, um den Titel und die Anweisung für bestimmte Menüpunkte anzupassen. (Weitere Informationen finden Sie im nächsten Abschnitt.)

    Das Raster enthält die folgenden Spalten:

    - **Menüelementname** - Zeilen, in denen diese Spalte leer ist, verwenden den Standard-Schritttitel und die Anweisung, die für alle Menüelemente auf mobilen Geräten gelten, für die keine Überschreibung definiert ist. Zeilen, in denen diese Spalte auf den Namen eines Menüelements festgelegt ist, haben Überschreibungen, die nur für das angegebene Menüelement gelten.
    - **Schritt-ID** - Die eindeutige ID des Schritts.
    - **Titel für Eingabe** - Der Titel, der angezeigt wird, wenn die App neue Informationen anfordert. Normalerweise sind die Felder auf der Seite leer (d.h. sie haben keine voreingestellten Werte).
    - **Titel für Bestätigung** - Der Titel, der angezeigt wird, wenn die App die Bestätigung eines Wertes anfordert, der bereits im System gespeichert ist. Typischerweise haben die Felder auf der Seite voreingestellte Werte.

1. Suchen Sie die Kombination der Werte **Schritt-ID** und **Name des Elements**, die Sie bearbeiten wollen, und wählen Sie den Wert in der Spalte **Schritt-ID**. Die Seite, die geöffnet wird, listet alle verfügbaren Übersetzungen für den Titel und die Anweisung des ausgewählten Schritts auf.
1. Führen Sie einen dieser Schritte aus, um den Text für eine beliebige Sprache anzupassen. Mit beiden Optionen können Sie Texte für vorhandene Sprachen bearbeiten. Allerdings können Sie nur mit der ersten Option Texte für neue Sprachen hinzufügen, während Sie nur mit der zweiten Option Texte für alle vorhandenen menüspezifischen Überschreibungen der ausgewählten Sprache anzeigen und bearbeiten können.

    - Wählen Sie in der Symbolleiste **Hinzufügen**, um ein Dialogfeld zu öffnen, in dem Sie Texte für jede unterstützte Sprache hinzufügen oder bearbeiten können. Legen Sie das Feld **Referenzsprache** auf die Sprache fest, für die Sie Werte anzeigen möchten. Die Werte werden in der linken Spalte angezeigt. Legen Sie das Feld **Sprache der Übersetzungen** auf die Sprache fest, die Sie hinzufügen oder anpassen wollen. Bearbeiten Sie in der rechten Spalte die Werte der Felder **Titel für Eingabe**, **Anweisung für Eingabe**, **Titel für Bestätigung** und **Anweisung für Bestätigung** wie gewünscht. Wählen Sie dann **OK** aus.
    - Suchen Sie im Raster die Zeile, in der das Feld **Sprache** auf die Sprache festgelegt ist, die Sie bearbeiten wollen, und wählen Sie sie aus. Wählen Sie in der Symbolleiste **Übersetzungen &lt;Sprache&gt; dieses Schritts anzeigen**, um ein Dialogfeld zu öffnen, in dem Sie Texte für alle verfügbaren Überschreibungen für die ausgewählte Sprache bearbeiten können. Das Dialogfeld enthält ein Raster mit Zeilen sowohl für die Standardtexte (bei denen das Feld **Name des Menüelements** leer ist) als auch für jeden verfügbaren Überschreibungs-Text (bei dem das Feld **Name des Menüelements** auf den Namen des Menüelements festgelegt ist, für den die Überschreibung gilt). Bearbeiten Sie die Werte der Felder **Titel für Eingabe**, **Anweisung für Eingabe**, **Titel für Bestätigung** und **Anweisung für Bestätigung** wie gewünscht. Wählen Sie dann **OK** aus.

1. Fahren Sie fort, bis Sie jeden gewünschten Titel und jede gewünschte Anweisung für jede gewünschte Sprache definiert haben.

## <a name="add-menu-specific-overrides"></a>Hinzufügen von menüspezifischen Überschreibungen

Wie bereits im vorigen Abschnitt erwähnt, können Sie für jede Schritt-ID eine beliebige Anzahl von menüspezifischen Überschreibungen erstellen. Sie können diese Funktionalität verwenden, um die Anweisung so zu bearbeiten und zu ändern, dass sie besser zu Ihrem lokalen Geschäftsprozess für einen bestimmten Menüpunkt passt. Wenn Ihre Firma z.B. bei der Verkaufskommissionierung den Arbeitskräften normalerweise Arbeits-IDs auf einem gedruckten Beleg zur Verfügung stellt, können Sie einen Hinweis geben, dass die Arbeitskräfte mit dem Scannen einer Arbeits-ID beginnen sollen.

Jede Überschreibung gilt für einen bestimmten Menüpunkt auf einem mobilen Gerät und kann eine beliebige Anzahl von Übersetzungen enthalten. Wenn für einen Menüpunkt keine Überschreibung existiert, verwendet der Menüpunkt die Standardtexte. Wenn für eine Sprache keine Überschreibungsübersetzung definiert ist, werden die Standardtexte verwendet, auch für Menüelemente, für die eine Überschreibung für andere Sprachen definiert ist.

Führen Sie die folgenden Schritte aus, um eine Außerkraftsetzung zu erstellen und zu konfigurieren.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> Mobiles Gerät \> Mobiles Gerät Schritte**.
1. Suchen Sie im Raster die Zeile, für die Sie eine Außerkraftsetzung erstellen wollen, und wählen Sie sie aus.
1. Wählen Sie im Aktionsbereich **Schrittkonfiguration hinzufügen**.
1. Legen Sie im Dropdown-Dialogfeld **Schrittkonfiguration hinzufügen** das Feld **Menüelement** auf den Namen des Menüelements des mobilen Geräts fest, für das Ihre Außerkraftsetzung gilt. Wählen Sie dann **OK** aus.
1. Die erscheinende Seite zeigt alle Texte an, die für die neue Überschreibung verfügbar sind. Zu Beginn wird nur eine Sprache erstellt. Alle anderen Sprachen werden weiterhin die Standardtexte verwenden, es sei denn, Sie fügen diese Sprachen hier hinzu. Bearbeiten Sie die Texte und fügen Sie bei Bedarf neue Sprachen hinzu, wie im vorherigen Abschnitt beschrieben.
