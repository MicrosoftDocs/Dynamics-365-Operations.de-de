---
title: Entitätsdaten in Excel öffnen und sie mithilfe des Excel-Add-Ins aktualisieren
description: In diesem Thema wird erläutert, wie Entitätsdaten in Microsoft Excel geöffnet und anschließend mit dem Microsoft Dynamics Office-Add-in für Excel angezeigt, aktualisiert und bearbeitet werden.
author: ChrisGarty
manager: AnnBe
ms.date: 04/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26d5f165648c1553745e3061cc89bcba42f9636a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688466"
---
# <a name="open-entity-data-in-excel-and-update-it-by-using-the-excel-add-in"></a>Entitätsdaten in Excel öffnen und sie mithilfe des Excel-Add-Ins aktualisieren

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Entitätsdaten in Microsoft Excel geöffnet und anschließend mit dem Microsoft Dynamics Office-Add-in für Excel angezeigt, aktualisiert und bearbeitet werden. Um die Entitätsdaten zu öffnen, können Sie entweder mit Excel oder Finance and Operations beginnen.

Durch das Öffnen der Entitätsdaten in Excel können Sie die Daten mit dem Add-in für Excel schnell und einfach anzeigen und bearbeiten. Dieses Add-In erfordert Microsoft Excel 2016.

> [!NOTE]
> Wenn Ihr Microsoft Azure Active Directory (Azure AD)-Mandant für die Verwendung von Active Directory Federation Services (AD FS) konfiguriert ist, müssen Sie sicherstellen, dass das Update von Mai 2016 für Office eingespielt wurde, sodass Sie über das Excel-Add-In korrekt angemeldet werden können.

Weitere Informationen zur Verwendung des Excel-Add-Ins finden Sie unter [Erstellen Sie Vorlage für Kopf- und Positionsmuster in Dynamics 365 for Finance and Operations](https://youtu.be/RTicLb-6dbI) Video.

## <a name="open-entity-data-in-excel-when-you-start-from-finance-and-operations"></a>Öffnen von Entitätsdaten in Excel beim Start von Finance and Operations
1. Wählen Sie auf einer Seite in Finance and Operations die Option **In Microsoft Office öffnen** aus.

    Wenn die Stammdatenquelle (Tabelle) der Seite dieselbe ist wie die Stammdatenquelle für beliebige Entitäten, werden standardmäßige **In Excel öffnen**-Optionen für die Seite generiert. **In Excel öffnen**-Optionen finden Sie auf häufig verwendeten Seiten wie **Alle Kreditoren** und **Alle Debitoren**.
 
2. Klicken Sie auf eine **In Excel öffnen**-Option, um die generierte Arbeitsmappe zu öffnen. Diese Arbeitsmappe besitzt Bindungsinformationen für die Entität, einen Mauszeiger auf Ihre Umgebung und einen Zeiger auf das Excel-Add.
3. Klicken Sie in Excel auf die Option zum **Bearbeiten aktiveren**, damit das Excel Add-In ausgeführt werden kann. Das Excel-Add-In wird in einem Bereich auf der rechten Seite des Excel-Fensters ausgeführt.
4. Wenn Sie das Excel-Add-In zum ersten Mal ausführen, klicken Sie auf **Diesem Add-In vertrauen**.
5. Klicken Sie nach Aufforderung auf **Anmelden** und melden Sie sich mit den Anmeldeinformationen an, mit denen Sie sich bei Finance and Operations angemeldet haben. Das Excel-Add-In verwendet einen vorherigen Anmeldungskontext von Internet Explorer und meldet Sie automatisch an, wenn dies möglich ist. Daher müssen Sie unbedingt den Benutzernamen in der oberen rechten Ecke des Excel-Add-Ins überprüfen.

Das Excel-Add-In liest automatisch die Daten für die Entität, die Sie ausgewählt haben. Beachten Sie, dass keine Daten in der Arbeitsmappe sind, bis sie vom Excel-Add-In eingelesen werden.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Öffnen von Entitätsdaten in Excel beim Start von Excel
1. Klicken Sie in Excel auf der Registerkarte **Einfügen** in der Gruppe **Add-Ins** auf **Shop**, um den Office Store zu öffnen.
2. Suchen Sie im Office Store nach dem Schlüsselwort **Dynamics**, und klicken Sie auf **Hinzufügen** neben dem **Microsoft Dynamics Office Add-in** (dem Excel-Add-In).
3. Wenn Sie das Excel-Add-In zum ersten Mal ausführen, klicken Sie auf **Diesem Add-In vertrauen**, damit das Excel-Add-In ausgeführt werden kann. Das Excel-Add-In wird in einem Bereich auf der rechten Seite des Excel-Fensters ausgeführt.
4. Klicken Sie auf **Serverinformationen hinzufügen**, um den Bereich **Optionen** zu öffnen.
5. Kopieren Sie die Browser-URL der Finance and Operations-Instanz, fügen Sie sie in das Feld **Server-URL** ein, und löschen Sie dann alles nach dem Hostnamen. Die resultierende URL soll derzeit nur den Hostnamen haben.

    Wenn beispielsweise die URL `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage` ist, löschen Sie alles außer `https://xxx.dynamics.com`.

6. Klicken Sie auf **OK** und dann auf **Ja**, um die Änderung zu bestätigen. Das Excel-Add-In wird neu gestartet und lädt die Metadaten.

    Die Schatfläche für den **Entwurf** ist jetzt verfügbar. Verfügt das Excel-Add-In über eine Schaltfläche **Applets laden**, sind Sie möglicherweise nicht als der korrekte Benutzer angemeldet. Weitere Informationen finden Sie unter "Die 'Applets laden'-Schaltfläche wird angezeigt" im Abschnitt [Problembehandlung](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#troubleshooting) in diesem Thema.

7. **Design** auswählen. Das Excel-Add-In ruft die Entitätsmetadaten ab.
8. **Tabelle hinzufügen** auswählen. Eine Liste von Entitäten wird angezeigt. Die Entitäten werden in "Name - Beschriftungs"-Format angezeigt.
9. Wählen Sie eine Entität in der Liste aus, beispielsweise **Kunden - Kunden**, und klicken Sie dann auf **Weiter**.
10. Um ein Feld von der Liste **Verfügbare Felder** zur Liste **Ausgewählte Felder** hinzuzufügen, klicken Sie auf das Feld und dann auf **Hinzufügen**. Alternativ doppelklicken Sie auf das Feld in der Liste **Verfügbare Felder**.
11. Nachdem Sie die gewünschten Felder der Liste **Ausgewählte Felder** hinzugefügt haben, stellten Sie sicher, dass sich der Cursor auf der korrekten Position in der Arbeitsmappe befindet (beispielsweise Zelle A1) und klicken dann auf **Fertig**. Klicken Sie anschließend auf **Fertig**, um den Designer zu beenden.
12. Klicken Sie auf **Aktualisieren**, um Daten zu laden.

## <a name="view-and-update-entity-data-in-excel"></a>Anzeigen und Aktualisieren von Entitätsdaten in Excel
Nachdem das Excel-Add-In die Entitätsdaten in die Arbeitsmappe eingelesen hat, können Sie die Daten jederzeit aktualisieren, indem Sie im Excel-Add-In auf **Aktualisieren** klicken.

## <a name="edit-entity-data-in-excel"></a>Bearbeiten von Entitätsdaten in Excel
Sie können Entitätsdaten bei Bedarf ändern und anschließend wieder veröffentlichen, indem Sie im Excel-Add-In auf **Veröffentlichen** klicken. Wenn Sie einen Datensatz bearbeiten möchten, wählen Sie eine Zelle im Arbeitsblatt und ändern anschließend den Zellenwert. Wenn Sie einen neuen Datensatz hinzufügen möchten, führen Sie die folgenden Schritte aus:

- Klicken Sie auf eine beliebige Datenquelle im Arbeitsblatt, und klicken Sie dann im Excel-Add-In auf **Neu**.
- Klicken Sie irgendwo in die letzte Zeile der Datenquelle im Arbeitsblatt, und drücken Sie dann die TAB-Taste, bis der Cursor die letzten Spalte dieser Zeile verlässt und eine neue Zeile erstellt wird.
- Klicken Sie irgendwo in die Zeile direkt unterhalb der Datenquelle im Arbeitsblatt und geben Sie Daten in eine Zelle ein. Wenn Sie den Fokus aus der Zelle heraus bewegen, wird die Tabelle um die neue Zeile erweitert.
- Für Feldbindungen von Überschriftendatensätzen, klicken Sie auf eines der Felder, und klicken Sie dann . Excel-Add-In **Neu**.

Beachten Sie, dass ein neuer Datensatz erstellt werden kann, wenn alle Schlüssel und Pflichtfelder im Arbeitsblatt gebunden werden oder wenn Standardwerten ausgefüllt wurden, indem die Filterbedingungen verwendet werden.

Wenn Sie einen Datensatz löschen möchten, führen Sie die folgenden Schritte aus:

- Klicken Sie mit der rechten Maustaste auf die Zeilennummer neben der zu löschenden Arbeitsblattzeile, und klicken Sie dann auf **Löschen**.
- Klicken Sie mit der rechten Maustaste irgendwo in der zu löschenden Arbeitsblattzeile, und klicken Sie dann auf **Löschen** &gt; **Tabellenzeilen**.

Wenn Datenquellen als zugeordnete Datenquellen hinzugefügt wurden, wird die Überschrift vor den Positionen veröffentlicht. Sind Abhängigkeiten zwischen anderen Datenquellen vorhanden, müssen Sie möglicherweise den Standard-Veröffentlichen-Auftrag ändern. Um den Veröffentlichungsauftrag, im Excel-Add-In zu ändern, wählen die **Optionen** (das Gangsymbol), und klicken Sie dann auf dem Inforegister auf **Datenkonnektor**, wählen Sie **Veröffentlichungsreihenfolge konfigurieren**

## <a name="add-or-remove-columns"></a>Spalten hinzufügen oder entfernen
Sie können den Designer verwenden, um die Spalten anzupassen, die automatisch zum Arbeitsblatt hinzugefügt wurden.

> [!NOTE]
> Wenn die Schaltfläche **Entwurf** nicht unter der Schaltfläche **Filtern** im Excel-Add-In angezeigt wird, müssen Sie den Datenquellendesigner aktivieren. Wählen Sie die **Optionen** (Schaltfläche das Gangsymbol) aus, und aktivieren Sie anschließend das Kontrollkästchen **Aktivieren von Entwicklungen**.

1. Klicken Sie auf die Option für **Design**. Alle Datenquellen werden aufgelistet.
2. Klicken Sie neben der Datenquelle auf **Bearbeiten** (Bleistiftsymbol).
3. Passen Sie die Liste in der Liste **Ausgewählte Felder** die Liste der Felder Ihren Bedürfnissen an:

    - Um ein Feld von der Liste **Verfügbare Felder** zur Liste **Ausgewählte Felder** hinzuzufügen, klicken Sie auf das Feld und dann auf **Hinzufügen**. Alternativ doppelklicken Sie auf das Feld in der Liste **Verfügbare Felder**.
    - Zum Entfernen eines Felds aus der Liste **Ausgewählte Felder** klicken Sie auf das Feld und dann auf **Entfernen**. Sie können auch einen Doppelklick auf das Feld ausführen.
    - Um die Reihenfolge der Felder zu ändern, klicken Sie auf das Feld in der Liste **Ausgewählte Felder** und klicken dann auf die Option für **Nach oben** oder **Nach unten**.

4. Klicken Sie auf **Aktualisieren**, um die Änderungen der Datenquelle zu übernehmen. Klicken Sie anschließend auf **Fertig**, um den Designer zu beenden.
5. Wenn Sie ein Feld (Spalte) hinzugefügt haben, klicken Sie auf **Aktualisieren**, um aktualisierte Datensätze zu laden.

## <a name="copy-environment-data"></a>Umgebungsdaten kopieren

Die Daten, die in die Arbeitsmappe in einer Umgebung eingelesen werden, können in eine andere Umgebung kopiert werden. Sie können jedoch die Verbindungs-URL derzeit nicht ändern, da der Datencache in der Arbeitsmappe weiterhin die Daten als vorhandene Daten behandelt. Stattdessen müssen Sie die Copy Environment Data-Funktionen verwenden, um die Daten in einer neuen Umgebung als neue Daten zu veröffentlichen.

1. Wählen Sie die **Optionen**-Schaltfläche (Gangsymbol), und klicken Sie dann auf den FastTab **Datenkonnektor**, wählen Sie **Umgebungsdaten kopieren**. 
2. Geben Sie die Server-URL für die neue Umgebung an. 
3. Klicken Sie auf **OK** und dann auf **Ja**, um die Aktion zu bestätigen. Das Excel-Add-In wird neu gestartet und verbindet sich mit der neuen Umgebung. Alle vorhandenen Daten in der Arbeitsmappe werden als neue Daten behandelt.

    Nachdem das Excel-Add-In neugestartet wurde, zeigt ein Meldungsfeld an, dass die Arbeitsmappe im Umgebungskopiemodus ist.

4. Um die Daten in die neue Umgebung als neue Daten zu kopieren, wählen Sie **Veröffentlichen** aus. Um den Umgebungskopiervorgang abzubrechen und die vorhandenen Daten in der neuen Umgebung zu prüfen, wählen Sie **Aktualisieren**.

## <a name="troubleshooting"></a>Problembehandlung
Es gibt mehrere Probleme, die ganz einfach behoben werden können.

- **Die "Applets laden"-Schaltfläche wird angezeigt.** – Verfügt das Excel-Add-In nach der Anmeldung über eine Schaltfläche Applets laden, sind Sie möglicherweise nicht als der korrekte Benutzer angemeldet. **Applets laden**, sind Sie möglicherweise nicht als der korrekte Benutzer angemeldet. Zur Behebung dieses Problems sollten Sie sicherstellen, dass der korrekte Benutzername in der oberen rechten Ecke des Excel-Add-Ins angezeigt wird. Wenn ein falscher Benutzername angezeigt wird, klicken Sie auf dieses Symbol, melden Sie sich ab, und melden Sie sich dann wieder an.
- **Sie erhalten eine "Nicht zulässig"-Meldung.** – Wenn Sie eine "Nicht zulässig"-Meldung erhalten, während das Excel-Add-In die Metadaten lädt, dann verfügt das Konto, mit dem Sie beim Excel-Add-In angemeldet sind, nicht über die Berechtigungen, den gewünschten Dienst, die gewünschte Instanz oder die gewünschte Datenbank zu verwenden. Zur Behebung dieses Problems sollten Sie sicherstellen, dass der korrekte Benutzername in der oberen rechten Ecke des Excel-Add-Ins angezeigt wird. Wenn ein falscher Benutzername angezeigt wird, klicken Sie auf dieses Symbol, melden Sie sich ab, und melden Sie sich dann wieder an.
- **Eine leere Webseite wird über Excel angezeigt** – Wenn eine leere Webseite während des Anmeldungsprozesses geöffnet wird, benötigt das Konto AD FS, aber die Excel-Version, mit der das Excel-Add-In ausgeführt wird, ist veraltet und reicht für das Laden des Anmeldedialogs nicht aus. Zur Behebung dieses Problems aktualisieren Sie die Excel-Version, die Sie verwenden. Zum Aktualisieren der Excel-Version, während Sie sich in einem Unternehmen mit einem verzögerten Kanal befinden, nutzen Sie das [Office-Bereitstellungstool](https://technet.microsoft.com/library/jj219422.aspx) um [vom verzögerten Kanal zum aktuellen Kanal zu wechseln](https://technet.microsoft.com/library/mt455210.aspx).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]