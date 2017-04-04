---
title: Verwenden Sie das Excel-Add-In
description: "In diesem Thema wird erläutert wie Daten der offenen Entität in Microsoft Excel und dann zeigt, aktualisiert und verarbeitet die Daten, indem das Add-In Microsoft Dynamics für Office Excel verwendet. Um die Entitätsdaten zu öffnen, können Sie aus Excel oder von Microsoft Dynamics 365 beginnen entweder für Arbeitsgänge."
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

# <a name="use-the-excel-add-in"></a>Verwenden Sie das Excel-Add-In

In diesem Thema wird erläutert wie Daten der offenen Entität in Microsoft Excel und dann zeigt, aktualisiert und verarbeitet die Daten, indem das Add-In Microsoft Dynamics für Office Excel verwendet. Um die Entitätsdaten zu öffnen, können Sie aus Excel oder von Microsoft Dynamics 365 beginnen entweder für Arbeitsgänge.

Per Öffnen von Entitätsdaten in Microsoft Excel, Sie, kann die Daten mithilfe der Addins Microsoft Dynamics für Office Excel schnell und einfach anzeigen und bearbeiten. Dies erfordert Add-In Microsoft Excel 2016. ** Hinweis: ** Wenn Ihr Mandant Microsoft Azures Active Directory "Azure ANZEIGE) konfiguriert wird, um AD FS Active Directory-Verbunddiensten () verwendet werden soll, müssen Sie prüfen, ob die Aktualisierung im Mai 2016 angewendet wurde, für das Sie Excel-Add-In ordnungsgemäß in signieren kann.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Daten der offenen Entität in Excel, wenn Sie von Microsoft Dynamics 365 für Arbeitsgänge von
1.  Auf eine Seite in Microsoft Dynamics 365 für Arbeitsgänge, auf ** geöffnet in Microsoft Office **. Wenn die Stammdatenquelle (Tabelle) zur Seite die gleich ist, die die Stammdatenquelle für beliebige Entitäten, Standard ** offen in Excel ** Optionen für Seite die generiert werden. ** Offen in Excel ** Optionen kann auf häufig verwendeter Seiten, z befinden ** alle Kreditoren ** ** ** und alle Debitoren.
2.  Klicken Sie auf Erneut öffnen eine ** in Excel ** Option, und öffnen Sie die Arbeitsmappe, die generiert wird. Diese Arbeitsmappe besitzt verbindliche Informationen für die Entität, den Mauszeiger in Ihrer Umgebung und einen Excel-Add-In Mauszeiger an.
3.  In Excel auf ** aktivieren Bearbeiten ** um das Excel-Add-Ins zu aktivieren, die ausgeführt werden. Das übertreffungs-Add-In ausgeführt wird in einen Bereich auf der rechten Seite des Excel-Fensters.
4.  Wenn Sie das Excel-Add-In zum ersten Mal ausgeführt, auf ** vertrauen Sie diesem Add-In **.
5.  Wenn Sie aufgefordert werden, in zu signieren, klicken Sie in ** ** signieren Sie, und unterzeichnet Sie den in fest, indem Sie die gleichen Anmeldeinformationen verwenden, die Sie verwenden, um zu Dynamics 365 für Arbeitsgänge in zu signieren. Das übertreffungs-Add-In verwendet einen vorherigen Anmeldungskontext von Internet Explorer und signiert Sie automatisch in, wenn es kann. Daher müssen Sie unbedingt den Benutzernamen in der oberen rechten Ecke des Excel-Add-Ins.

Das automatisch die übertreffungs-Add-In liest Daten für die Entität, die Sie ausgewählt haben. Beachten Sie, dass keine Daten in der Arbeitsmappe wird, bis sie in das Excel-Add-In liest.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Daten der offenen Entität in Excel, wenn aus Excel von
1.  In Excel auf der Registerkarte, Einfügen ** ** ** Add-Ins ** in der Gruppe auf, ** Shop ** um das Office-Shops zu öffnen.
2.  Im Office-Shop, Suche im Schlüsselwort "Dynamics," und auf ** Hinzufügen ** neben ** Add-In Microsoft Dynamics Public-Vorlage Office ** (das Excel-Add-In).
3.  Wenn Sie das Excel-Add-In zum ersten Mal ausführen, klicken Sie ** vertrauen Sie diesem Add-In ** um das Excel-Add-In zu aktivieren, die ausgeführt werden. Das übertreffungs-Add-In ausgeführt wird in einen Bereich auf der rechten Seite des Excel-Fensters.
4.  ** Auf fügen Sie Serverinformationen hinzu ** ** Optionen ** um das Fenster zu öffnen.
5.  Kopieren Sie die URL Browser vom Ziel Dynamics 365 für Arbeitsgangsinstanz, ordnen Sie sie im ** Server URL ** Feld ein, und löschen Sie anschließend alle nach den Hostnamen (z, Löschen **/? cmp=usmf&mi=CustTableListPage **). Die resultierende URL soll derzeit den Hostnamen haben (z **, https://xxx.dynamics.com**).
6.  ** Der auf OK ** und klicken dann ** Ja ** um die Änderung zu bestätigen. Die übertreffungs-hinzugefügteNeustarts und die Auslastungsmetadaten. ** Entwurf ** Die Schaltfläche ist jetzt zur Verfügung. Wenn das Excel-Add-In eine Auslastungsapplets ** ** Schaltfläche hat, werden Sie vermutlich in nicht zur Der richtige Benutzer signiert. Weitere Informationen finden Sie, ob "die Auslastungsappletschaltfläche " in" Problembehandlungs" Abschnitt dieses Themas wird angezeigt.
7.  ** Entwurf ** auf. Das übertreffungs-Add-In ruft Entitätsmetadaten ab.
8.  ** Auf fügen Sie Tabelle hinzufügen **. Eine Liste von Entitäten wird. Die Entitäten werden in "Name - Beschriftungs" Format angezeigt.
9.  Wählen Sie eine Entität in der Liste, wie Debitor ** - Debitoren ** und klicken Sie dann auf Weiter ** ** aus.
10. Um ein Feld von der ** verfügbare Felder ** ** der Liste ausgewählte Felder ** Liste hinzuzufügen, klicken Sie auf das Feld, und klicken Sie dann ** Hinzufügen **. Alternativ Doppelklicken Sie auf das Feld.
11. Nachdem Sie die gewünschten Felder der ** ausgewählte Felder ** Liste hinzugefügt sind, überprüfen Sie, ob den Cursor im richtigen Ort im Arbeitsblatt (beispielsweise Gesamtlayout, Zelle A1), und klicken Sie dann ** getan **. Klicken Sie anschließend auf dem ausgeführt ** ** Designer zu beenden.
12. ** Aktualisierung auf ** um eines Satzes Daten in zu ziehen.

## <a name="view-and-update-entity-data-in-excel"></a>Dient zum Anzeigen und Aktualisierungsentitätsdaten in Excel
Nachdem das Excel-Add-In Entitätsdaten in die Arbeitsmappe liest, können Sie die Daten jederzeit aktualisieren, indem Sie im Excel-Add-In ** Aktualisierung ** klicken.

## <a name="edit-entity-data-in-excel"></a>Bearbeiten Sie Entitätsdaten in Excel
Sie können Entitätsdaten ändern, wie Sie benötigen und diese dann nach veröffentlichen, indem Sie ** Veröffentlichen ** im Excel-Add-In klicken. Wenn Sie einen Datensatz zu bearbeiten, aktivieren Sie eine Zelle im Arbeitsblatt, und ändern Sie anschließend den Zellenwert. Wenn Sie einen neuen Datensatz hinzufügen möchten, führen Sie die folgenden Schritte aus:

-   Klicken Sie auf eine beliebige Stelle im Arbeitsblatt, und klicken Sie dann im Excel-Add-In ** ** neu.
-   Klicken Sie in der letzten Zeile des Arbeitsblatts, und drücken Sie dann die TAB-Taste, bis der Cursor aus der letzten Spalte dieser Zeile Auschecken durchläuft und eine neue Position erstellt wird.
-   Klicken Sie in der Zeile des Arbeitsblatts und sofort unterhalb des Starts, Daten in einer Zelle einzugeben. Wenn Sie das Ziel aus der Zelle bewegen, erweitert dem Arbeitsblatt, um die neue Zeile anzuzeigen.

Wenn Sie einen Datensatz zu löschen, führen Sie die folgenden Schritte aus:

-   Klicken Sie auf die Arbeitsblattzeile Zeilennummer neben der xxxx_1, die gelöscht werden soll, und klicken Sie dann auf Löschen ** **.
-   Klicken Sie in der Arbeitsblattzeile xxxx_1, die gelöscht werden soll, und klicken Sie dann auf Löschen ** ** ** &gt; auf Tabellen- **.

## <a name="add-or-remove-columns"></a>Spalten hinzufügen oder entfernen
Sie können den Designer verwenden, um die Spalten anzupassen, die automatisch mit Arbeitsblatt hinzugefügt werden.

1.  Starten Sie den Datenquellendesigner des Excel-Add-Ins, indem Sie auf die Schaltfläche (** Optionen ** das Gangsymbol) klicken und dann das ** aktivieren Sie den Entwurf ** Kontrollkästchen aktivieren.
2.  ** Entwurf ** auf im Excel-Add-In. Alle Datenquellen werden aufgelistet.
3.  Rechts bei der Datenquelle ** klicken Sie auf die Schaltfläche (Bearbeiten ** das Bleistiftsymbol).
4.  Passen Sie die in der Liste ausgewählte Felder ** ** Liste, wie Sie benötigen:
    -   Um ein Feld von der ** verfügbare Felder ** ** der Liste ausgewählte Felder ** Liste hinzuzufügen, klicken Sie auf das Feld, und klicken Sie dann ** Hinzufügen **. Alternativ Doppelklicken Sie auf das Feld.
    -   Um ein Feld von der ** ausgewählte Felder ** Liste zu entfernen, klicken Sie auf das Feld, und klicken Sie dann ** entfernen Sie sicher **. Alternativ Doppelklicken Sie auf das Feld.
    -   Um die Reihenfolge der Felder zu ändern, klicken Sie auf das Feld in der ausgewählten Felder ** ** Liste, und klicken Sie dann oben ** ** ** ** oder unten.

5.  Wenden Sie Ihre Änderungen mit der Datenquelle, indem Sie auf klicken ** ** Aktualisierung. Klicken Sie anschließend auf dem ausgeführt ** ** Designer zu beenden. Wenn Sie ein Feld (Spalte) haben, klicken Sie ** Aktualisierung ** aktualisierten um einen Satz Daten in zu ziehen.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Troubleshooting
Es gibt mehrere Probleme, die durch mehrere einfache Schritte behoben werden können.

-   ** Die Auslastungsappletschaltfläche wird angezeigt. ** Wenn das Excel-Add-In eine Auslastungsapplets ** ** Schaltfläche nach Anmeldung hat, werden Sie vermutlich in nicht zur Der richtige Benutzer signiert. Zur Behebung dieses Problems, sollten Sie sicherstellen dass der korrekte Benutzername in der oberen rechten Ecke des Excel-Add-Ins wird. Wenn ein falscher Benutzername wird, klicken Sie auf dieses Symbol, signieren Sie in und unterzeichnet Sie sich dann wieder in.
-   ** Sie erhalten eine Meldung "verbotene". ** Wenn Sie eine verbotene "" Meldung erhalten, für das Excel-Add-In Metadaten werden, ist das Konto, das in das Excel-Add-In signiert wurde, nicht berechtigt, den, die Service gezielten Instanz oder die Datenbank verwendet werden soll. Zur Behebung dieses Problems, sollten Sie sicherstellen dass der korrekte Benutzername in der oberen rechten Ecke des Excel-Add-Ins wird. Wenn ein falscher Benutzername wird, klicken Sie auf dieses Symbol, signieren Sie in und unterzeichnet Sie sich dann wieder in.
-   ** Eine leere Webseite wird über Excel angezeigt. ** Wenn eine leere Webseite während des Anmeldungsprozesses geöffnet wird, benötigt das Konto AD FS, doch die Version aus Excel, das das Add-In ausführt, ist nicht erstattungsfähig genug neu, das Anmeldungsdialogfeld zu laden. Zur Behebung dieses Problems, aktualisieren Sie die Version aus Excel die Sie verwenden. Sie können die Version aus Excel aktualisieren wenn Sie auf in einem Unternehmen werden das auf dem Schema Kanal ist, können Sie Office-Bereitstellungstool []( https://technet.microsoft.com/library/jj219422.aspx) [Verschiebung vom dem aktuellen Schema Kanal Kanal]( https://technet.microsoft.com/library/mt455210.aspx).



