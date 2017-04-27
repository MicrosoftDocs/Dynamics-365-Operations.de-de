---
title: Excel-Add-In verwenden
description: "In diesem Thema wird erläutert, wie Entitätsdaten in Microsoft Excel geöffnet und anschließend mit dem Microsoft Dynamics Office-Add-in für Excel angezeigt, aktualisiert und bearbeitet werden. Sie können die Entitätsdaten über Excel oder Microsoft Dynamics 365 for Operations öffnen."
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 8af663b47117759ed3b2e2ed8eee85ae4df100d1
ms.lasthandoff: 03/31/2017


---

# <a name="use-the-excel-add-in"></a>Excel-Add-In verwenden

In diesem Thema wird erläutert, wie Entitätsdaten in Microsoft Excel geöffnet und anschließend mit dem Microsoft Dynamics Office-Add-in für Excel angezeigt, aktualisiert und bearbeitet werden. Sie können die Entitätsdaten über Excel oder Microsoft Dynamics 365 for Operations öffnen.

Durch das Öffnen der Entitätsdaten in Microsoft Excel können Sie die Daten mit dem Microsoft Dynamics Office-Add-in für Excel schnell und einfach anzeigen und bearbeiten. Das Add-In erfordert Microsoft Excel 2016. **Hinweis:** Wenn Ihr Microsoft Azure Active Directory (Azure AD)-Mandant für die Verwendung von Active Directory Federation Services (AD FS) konfiguriert ist, müssen Sie sicherstellen, dass das Update von Mai 2016 eingespielt wurde, sodass Sie über das Excel-Add-In korrekt angemeldet werden können.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Öffnen von Entitätsdaten in Excel beim Start von Dynamics 365 for Operations
1.  Klicken Sie in Microsoft Dynamics 365 for Operations auf einer Seite auf **In Microsoft Office öffnen**. Wenn die Stammdatenquelle (Tabelle) der Seite dieselbe ist wie die Stammdatenquelle für beliebige Entitäten, werden standardmäßige **In Excel öffnen**-Optionen für die Seite generiert. **In Excel öffnen**-Optionen finden Sie auf häufig verwendeten Seiten wie **Alle Kreditoren** und **Alle Debitoren**.
2.  Klicken Sie auf eine **In Excel öffnen**-Option, um die generierte Arbeitsmappe zu öffnen. Diese Arbeitsmappe besitzt Bindungsinformationen für die Entität, einen Mauszeiger auf Ihre Umgebung und einen Zeiger auf das Excel-Add.
3.  Klicken Sie in Excel auf die Option zum **Bearbeiten aktiveren**, damit das Excel Add-In ausgeführt werden kann. Das Excel-Add-In wird in einem Bereich auf der rechten Seite des Excel-Fensters ausgeführt.
4.  Wenn Sie das Excel-Add-In zum ersten Mal ausführen, klicken Sie auf **Diesem Add-In vertrauen**.
5.  Klicken Sie nach Aufforderung auf **Anmelden**, und melden Sie sich mit den Anmeldeinformationen an, mit denen Sie sich bei Dynamics 365 for Operations angemeldet haben. Das Excel-Add-In verwendet einen vorherigen Anmeldungskontext von Internet Explorer und meldet Sie automatisch an, wenn dies möglich ist. Daher müssen Sie unbedingt den Benutzernamen in der oberen rechten Ecke des Excel-Add-Ins überprüfen.

Das Excel-Add-In liest automatisch die Daten für die Entität, die Sie ausgewählt haben. Beachten Sie, dass keine Daten in der Arbeitsmappe sind, bis sie vom Excel-Add-In eingelesen werden.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Öffnen von Entitätsdaten in Excel beim Start von Excel
1.  Klicken Sie in Excel auf der Registerkarte **Einfügen** in der Gruppe **Add-Ins** auf **Shop**, um den Office Store zu öffnen.
2.  Suchen Sie im Office Store nach dem Schlüsselwort "Dynamics", und klicken Sie auf **Hinzufügen** neben dem **Microsoft Dynamics Office Add-In** (dem Excel-Add-In).
3.  Wenn Sie das Excel-Add-In zum ersten Mal ausführen, klicken Sie auf **Diesem Add-In vertrauen**, damit das Excel-Add-In ausgeführt werden kann. Das Excel-Add-In wird in einem Bereich auf der rechten Seite des Excel-Fensters ausgeführt.
4.  Klicken Sie auf **Serverinformationen hinzufügen**, um den Bereich **Optionen** zu öffnen.
5.  Kopieren Sie die Browser-URL der Dynamics 365 for Operations-Zielinstanz, fügen Sie sie in das Feld **Server-URL** ein, und löschen Sie dann alles nach dem Hostnamen (löschen Sie beispielsweise **/?cmp=usmf&mi=CustTableListPage**). Die resultierende URL sollte nur den Hostnamen enthalten (beispielsweise **https://xxx.dynamics.com**).
6.  Klicken Sie auf **OK** und dann auf **Ja**, um die Änderung zu bestätigen. Das Excel-Add-In wird neu gestartet und lädt die Metadaten. Die Schatfläche für den **Entwurf** ist jetzt verfügbar. Verfügt das Excel-Add-In über eine Schaltfläche **Applets laden**, sind Sie möglicherweise nicht als der korrekte Benutzer angemeldet. Weitere Informationen finden Sie unter "Die 'Applets laden'-Schaltfläche wird angezeigt" im Abschnitt "Problembehandlung".
7.  Klicken Sie auf die Schaltfläche für **Entwurf**. Das Excel-Add-In ruft die Entitätsmetadaten ab.
8.  Klicken Sie auf **Tabelle hinzufügen**. Eine Liste von Entitäten wird angezeigt. Die Entitäten werden in "Name - Beschriftungs"-Format angezeigt.
9.  Wählen Sie eine Entität in der Liste aus, beispielsweise **Kunden - Kunden**, und klicken Sie dann auf **Weiter**.
10. Um ein Feld von der Liste **Verfügbare Felder** zur Liste **Ausgewählte Felder** hinzuzufügen, klicken Sie auf das Feld und dann auf **Hinzufügen**. Sie können auch einen Doppelklick auf das Feld ausführen.
11. Nachdem Sie die gewünschten Felder der Liste **Ausgewählte Felder** hinzugefügt haben, stellten Sie sicher, dass sich der Cursor auf der korrekten Position in der Arbeitsmappe befindet (beispielsweise Zelle A1) und klicken dann auf **Fertig**. Klicken Sie anschließend auf **Fertig**, um den Designer zu beenden.
12. Klicken Sie auf **Aktualisieren**, um Daten zu laden.

## <a name="view-and-update-entity-data-in-excel"></a>Anzeigen und Aktualisieren von Entitätsdaten in Excel
Nachdem das Excel-Add-In die Entitätsdaten in die Arbeitsmappe eingelesen hat, können Sie die Daten jederzeit aktualisieren, indem Sie im Excel-Add-In auf **Aktualisieren** klicken.

## <a name="edit-entity-data-in-excel"></a>Bearbeiten von Entitätsdaten in Excel
Sie können Entitätsdaten bei Bedarf ändern und anschließend wieder veröffentlichen, indem Sie im Excel-Add-In auf **Veröffentlichen** klicken. Wenn Sie einen Datensatz bearbeiten möchten, wählen Sie eine Zelle im Arbeitsblatt und ändern anschließend den Zellenwert. Wenn Sie einen neuen Datensatz hinzufügen möchten, führen Sie die folgenden Schritte aus:

-   Klicken Sie auf eine beliebige Stelle im Arbeitsblatt, und klicken Sie dann im Excel-Add-In auf **Neu**.
-   Klicken Sie in die letzte Zeile des Arbeitsblatts, und drücken Sie dann die TAB-Taste, bis der Cursor die letzten Spalte dieser Zeile verlässt und eine neue Zeile erstellt wird.
-   Klicken Sie in die Zeile direkt unterhalb des Arbeitsblatts und geben Sie Daten in eine Zelle ein. Wenn Sie den Fokus aus der Zelle heraus bewegen, wird das Arbeitsblatt um die neue Zeile erweitert.

Wenn Sie einen Datensatz löschen möchten, führen Sie die folgenden Schritte aus:

-   Klicken Sie mit der rechten Maustaste auf die Zeilennummer neben der zu löschenden Arbeitsblattzeile, und klicken Sie dann auf **Löschen**.
-   Klicken Sie mit der rechten Maustaste auf die zu löschende Arbeitsmappenzeile, und klicken Sie dann auf **Löschen** &gt; und die Option für **Tabellenzeilen**.

## <a name="add-or-remove-columns"></a>Spalten hinzufügen oder entfernen
Sie können den Designer verwenden, um die Spalten anzupassen, die automatisch zum Arbeitsblatt hinzugefügt wurden.

1.  Starten Sie den Datenquellendesigner des Excel-Add-Ins, indem Sie auf die Schaltfläche **Optionen** (Zahnradsymbol) klicken und anschließend das Kontrollkästchen **Entwurf aktivieren** aktivieren.
2.  Klicken Sie auf die Option für **Entwurf** im Excel-Add-In. Alle Datenquellen werden aufgelistet.
3.  Klicken Sie neben der Datenquelle auf **Bearbeiten** (Bleistiftsymbol).
4.  Passen Sie die Liste in der Liste **Ausgewählte Felder** Ihren Bedürfnissen an:
    -   Um ein Feld von der Liste **Verfügbare Felder** zur Liste **Ausgewählte Felder** hinzuzufügen, klicken Sie auf das Feld und dann auf **Hinzufügen**. Sie können auch einen Doppelklick auf das Feld ausführen.
    -   Zum Entfernen eines Felds aus der Liste **Ausgewählte Felder** klicken Sie auf das Feld und dann auf **Entfernen**. Sie können auch einen Doppelklick auf das Feld ausführen.
    -   Um die Reihenfolge der Felder zu ändern, klicken Sie auf das Feld in der Liste **Ausgewählte Felder** und klicken dann auf die Option für **Nach oben** oder **Nach unten**.

5.  Klicken Sie auf **Aktualisieren**, um die Änderungen der Datenquelle zu übernehmen. Klicken Sie anschließend auf **Fertig**, um den Designer zu beenden. Wenn Sie ein Feld (Spalte) hinzugefügt haben, klicken Sie auf **Aktualisieren**, um aktualisierte Datensätze zu laden.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Problembehandlung
Es gibt mehrere Probleme, die ganz einfach behoben werden können.

-   **Die "Applets laden"-Schaltfläche wird angezeigt.** Verfügt das Excel-Add-In nach der Anmeldung über eine Schaltfläche **Applets laden**, sind Sie möglicherweise nicht als der korrekte Benutzer angemeldet. Zur Behebung dieses Problems sollten Sie sicherstellen, dass der korrekte Benutzername in der oberen rechten Ecke des Excel-Add-Ins angezeigt wird. Wenn ein falscher Benutzername angezeigt wird, klicken Sie auf dieses Symbol, melden Sie sich ab, und melden Sie sich dann wieder an.
-   **Sie erhalten eine "Nicht zulässig"-Meldung.** Wenn Sie eine "Nicht zulässig"-Meldung erhalten, während das Excel-Add-In die Metadaten lädt, dann verfügt das Konto, mit dem Sie beim Excel-Add-In angemeldet sind, nicht über die Berechtigungen, den gewünschten Dienst, die gewünschte Instanz oder die gewünschte Datenbank zu verwenden. Zur Behebung dieses Problems sollten Sie sicherstellen, dass der korrekte Benutzername in der oberen rechten Ecke des Excel-Add-Ins angezeigt wird. Wenn ein falscher Benutzername angezeigt wird, klicken Sie auf dieses Symbol, melden Sie sich ab, und melden Sie sich dann wieder an.
-   **Eine leere Webseite wird über Excel angezeigt.** Wenn eine leere Webseite während des Anmeldungsprozesses geöffnet wird, benötigt das Konto AD FS, aber die Excel-Version, mit der das Add-In ausgeführt wird, ist veraltet und reicht für das Laden des Anmeldedialogs nicht aus. Zur Behebung dieses Problems aktualisieren Sie die Excel-Version, die Sie verwenden. Zum Aktualisieren der Excel-Version, während Sie sich in einem Unternehmen mit einem verzögerten Kanal befinden, nutzen Sie das [Office-Bereitstellungstool](https://technet.microsoft.com/library/jj219422.aspx) um [vom verzögerten Kanal zum aktuellen Kanal zu wechseln](https://technet.microsoft.com/library/mt455210.aspx).



