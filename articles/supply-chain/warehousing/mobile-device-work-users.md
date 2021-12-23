---
title: Benutzerkonten für mobile Geräte
description: In diesem Thema wird beschrieben, wie Benutzerkonten eingerichtet und verwaltet werden, die es Mitarbeitern ermöglichen, sich anzumelden und die Warehouse-App zu verwenden.
author: Mirzaab
ms.date: 09/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-09-15
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f3a930814a1fb98e3b1611adf309c10e66b49b9d
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902096"
---
# <a name="mobile-device-user-accounts"></a>Benutzerkonten für mobile Geräte

[!include [banner](../includes/banner.md)]

Jedes Mal, wenn ein Mitarbeiter beginnt, die Warehouse-App zu verwenden, muss er sich mit einem Benutzernamen und einem Kennwort anmelden. Jedem Mitarbeiter im System kann eine beliebige Anzahl von Warehouse-App-Benutzern zugeordnet werden, und Lagerorte sind normalerweise jedem dieser Lagerort-App-Benutzer zugeordnet. Außerdem werden für jeden Arbeiter verschiedene Optionen konfiguriert, um Standardeinstellungen und andere Einstellungen festzulegen, die für die Verwendung der Lagerort-App relevant sind.

## <a name="set-up-the-required-worker-and-employee-records"></a>Einrichten der erforderlichen Arbeiter- und Mitarbeiterdatensätze

Bevor Sie Lagerort-App-Benutzer einrichten können, muss jede Arbeitskraft bereits als Supply Chain Management-Mitarbeiter oder Arbeitskraft im **Human Resources**-Modul vorhanden sein.

## <a name="set-up-mobile-device-user-accounts"></a><a name="set-wma-users"></a>Benutzerkonten für mobile Geräte einrichten

Nachdem die erforderlichen Arbeitskräfte und Mitarbeiter in Human Resources eingerichtet wurden, können Sie jedem von ihnen Lagerort-App-Benutzer zuweisen und andere Optionen einrichten, die sich auf die Verwendung der App auswirken.

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Arbeitskraft**.
1. Um eine vorhandene Arbeitskraft zu bearbeiten, wählen Sie sie im Listenbereich aus. Um einen neuen Datensatz hinzuzufügen, wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wenn Sie eine neue Arbeitskraft einrichten, gehen Sie folgendermaßen vor:

    1. Wählen Sie im Feld **Arbeitskraft** den Zielbenutzer in der Liste der Mitarbeiter aus.
    1. Wählen Sie **Auswählen**.
    1. Wählen Sie im Aktionsbereich **Speichern** aus.

1. Ein Standardprofil kann verwendet werden, um den Lagerortmitarbeiter am Packplatz durch den dort erforderlichen Prozess zu führen. Alternativ kann das Standardprofil verwendet werden, um die bevorzugten Profileinstellungen für die Arbeitskraft zu speichern. Legen Sie im Inforegister **Profil** die folgenden Felder fest:

    - **Verpackungsrichtlinie für Container** – Wählen Sie eine Containerpackrichtlinie aus, die definiert, wie Container an der Packstation verarbeitet werden sollen. Die hier ausgewählte Containerpackrichtlinie wird für die Arbeitskraft beim Öffnen der Packstation vorausgewählt. Weitere Informationen finden Sie im folgenden Blogbeitrag: [Verbesserte Verpackungsfunktionalität](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611),
    - **Verpackungsprofil-ID** – Wählen Sie eine Verpackungsprofil-ID aus, die die verwendeten Verpackungsrichtlinien und Containereinstellungen definiert. Wenn die ausgewählte Verpackungsprofil-ID mit einer Containerverpackungsrichtlinie verknüpft ist, können Sie die **Verpackungsrichtlinie für Container**-Einstellung auf dieser Seite nicht verwenden.

1. Legen Sie im Inforegister **Standard-Packstation** die folgenden Felder fest, um die Standardpackstation zu definieren, die angewendet wird, wenn sich die Arbeitskraft anmeldet. Bei Bedarf kann die Arbeitskraft noch eine andere Packstation auswählen.

    - **Seite** – Wählen Sie den Standort aus, an dem sich die Standardpackstation befindet.
    - **Lagerort** – Wählen Sie den Lagerort aus, an dem sich die Standardpackstation befindet.
    - **Standort** – Wählen Sie den Standort der Standardpackstation aus.

1. Im Inforegister **Benutzer** können Sie eine beliebige Anzahl von Lagerort-App-Benutzerkonten für die ausgewählte Arbeitskraft erstellen. Jedes Konto ist einem oder mehreren bestimmten Lagerorten zugeordnet. Verwenden Sie die Symbolleiste, um Benutzerkonten hinzuzufügen oder zu entfernen, das Kennwort für ein ausgewähltes Konto zurückzusetzen oder einem ausgewählten Konto Lagerorte zuzuweisen. Für jedes Benutzerkonto können Sie die folgenden Felder festlegen:

    - **Benutzer-ID** – Geben Sie eine eindeutige ID ein.
    - **Benutzername** – Geben Sie einen Namen für die ID ein.
    - **Standardlagerort** – Legen Sie den Standardlagerort fest, in dem die Arbeitskraft normalerweise arbeitet. Sie können die Symbolleiste verwenden, um zusätzliche Lagerorte zuzuweisen, und die Arbeitskraft kann zwischen den Lagerorten wechseln, indem Sie die indirekte Aktivität **Lagerort wechseln** des Menüelements Mobiles Gerät verwenden.
    - **Menüname** – Wählen Sie das Stammmenü aus, das die Startseite für die Arbeitskraft sein wird. Die Möglichkeit, für jede Arbeitskraft ein Stammmenü einzurichten, ist nützlich, da Sie damit die Menüstruktur steuern können, die jede Arbeitskraft verwenden kann. Beispielsweise kann das Menü für Arbeitskräfte, die nur im Ausgangsbereich aktiv sind, auf Aufgaben zugeschnitten werden, die sich auf Ausgangsvorgänge für diesen Bereich beziehen.
    - **Inaktiv** – Ein aktiviertes Kontrollkästchen zeigt an, dass das Benutzerkonto inaktiv ist. Das Benutzerkonto wird automatisch deaktiviert, wenn eine Arbeitskraft in der Lagerort-App fünfmal hintereinander das falsche Kennwort eingibt. Dieses Kontrollkästchen kann allerdings auch manuell aktiviert werden. Deaktivieren Sie das Kontrollkästchen, um den Benutzer wieder zu aktivieren.

1. Legen Sie auf dem Inforegister **Arbeit** die folgenden Felder fest:

    - **Außerkraftsetzen des Entnahmeorts zulassen** – Setzen Sie diese Option auf *Ja*, um es der Arbeitskraft zu ermöglichen, den Standort für die Entnahmeschritte zu überschreiben. Diese Funktion kann nützlich sein, wenn die physische Bestandsaufnahme nicht mit dem vom System vorgeschlagenen Standort übereinstimmt.
    - **Außerkraftsetzen des Einlieferungslagerplatzes zulassen** – Setzen Sie diese Option auf *Ja*, um es der Arbeitskraft zu ermöglichen, den Standort für der Einlieferungsschritte zu überschreiben. Diese Funktion kann nützlich sein, wenn der vorgeschlagene Einlieferungslagerplatz derzeit voll oder nicht verfügbar ist oder sich die Bereitstellungsstandorte geändert haben.
    - **Zu hohe Entnahme für Auftrag zulassen:** – Setzen Sie diese Option auf *Ja*, um es der Arbeitskraft zu ermöglichen, bei der Kommissionierung von Verkaufsaufträgen zu viel zu kommissionieren. Weitere Informationen finden Sie unter [Überkommissionierung bei Aufträgen und Umlagerungsaufträgen](over-picking-for-sales-and-transfer-orders.md).
    - **Zu hohe Entnahme für Umlagerungsauftrag zulassen:** – Setzen Sie diese Option auf *Ja*, um es der Arbeitskraft zu ermöglichen, bei der Kommissionierung von Umlagerungsaufträgen zu viel zu kommissionieren. Weitere Informationen finden Sie unter [Überkommissionierung bei Aufträgen und Umlagerungsaufträgen](over-picking-for-sales-and-transfer-orders.md).
    - **Bewegung von Bestand mit zugeordneter Arbeit zulassen** – Setzen Sie diese Option auf *Ja*, um es der Arbeitskraft zu ermöglichen, Inventar zu verschieben, das bereits reserviert oder bereits mit anderen Arbeiten verknüpft ist. Weitere Informationen finden Sie unter [Bewegung von Bestand mit zugeordneter Arbeit in der Warehouse Management](move-inventory-associated-work.md).
    - **Manuelle Artikelneuzuordnung zulassen** – Setzen Sie diese Option auf *Ja*, um eine manuelle Umverteilung für deie Arbeitskraft bei der Kurzkommissionierung zu ermöglichen. Die Neuzuweisung von Artikeln führt die Arbeitskräfte dazu, Inventar von einem anderen Standort zu kommissionieren. Obwohl die automatische Neuzuweisung für alle Arbeitskräfte verfügbar ist, erfordert die manuelle Neuzuweisung eine explizite Einrichtung für eine Arbeitskraft. Die Möglichkeit, die manuelle Neuzuweisung für jede Arbeitskraft zu steuern, kann hilfreich sein, da Sie damit die Sichtbarkeit jeder Arbeitskraft steuern können, wenn beispielsweise die Artikelentnahme aus dem Quarantäne- oder Massenbereich auf vertrauenswürdige Arbeitskräfte beschränkt ist. Weitere Informationen finden Sie im folgenden Blogbeitrag: [Automatische und manuelle Artikelzuordnung bei der Kurzkommissionierung](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/11/07/automatic-and-manual-item-reallocation-during-the-short-picking-dynamics-365-for-operations-1611/).
    - **Ist ein Zykluszählungs-Supervisor** – Setzen Sie diese Option auf *Ja*, um die Arbeitskraft zu einem Supervisor für die Zykluszählung zu machen. In diesem Fall werden alle Zykluszählungen, die der Mitarbeiter in der Lagerort-App durchführt, sofort genehmigt. Die Felder **Maximale Prozentgrenze**, **Höchstmengenbegrenzung** und **Maximalwertgrenze** werden für Arbeitskräfte nicht berücksichtigt, für die diese Option auf *Ja* eingestellt ist.
    - **Maximale Prozentgrenze** – Geben Sie die höchsten Prozentsatzgrenze ein, um den eine Inventur von der erwarteten Zahl abweichen kann, ohne dass eine Genehmigung durch den Supervisor der permanenten Inventur erforderlich ist.
    - **Höchstmengenbegrenzung** – Geben Sie die Gesamtmenge ein, um die die eingegebene Menge von der erwarteten Menge abweichen kann (in Einheiten), ohne dass eine Genehmigung durch einen Zykluszähler-Supervisor erforderlich ist.
    - **Maximale Wertgrenze** – Geben Sie den Maximalbetrag ein, um den die Kosten der Inventur von den erwarteten Kosten abweichen kann, ohne dass eine Genehmigung durch den Supervisor der permanenten Inventur erforderlich ist.

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wenn Sie einen neues Benutzerkonto hinzugefügt haben, wird das Dialogfeld **Passwort festlegen** angezeigt, in dem Sie ein einfaches Kennwort erstellen können, mit dem sich der Benutzer bei der mobilen App anmelden kann. Geben Sie das einfache Kennwort zweimal ein, und wählen Sie dann **Kennwort speichern** aus, um fortzusetzen.

## <a name="set-the-language-number-formats-and-time-zone-for-each-warehouse-app-user"></a>Legen Sie die Sprache, das Zahlenformat und die Zeitzone für jeden Lagerort-App-Benutzer fest

Wenn sich eine Arbeitskraft bei der mobilen Warehouse Management-App anmeldet, ändern sich die Sprache, das Zahlenformat und die Zeitzone entsprechend den Präferenzen dieser Arbeitskraft. Die Kontoeinstellungen für die Arbeitskraft, die in Schritt 3 im [Einrichten von Benutzerkonten für Mobilgeräte](#set-wma-users)-Abschnitt ausgewählt wurde, bestimmt die verwendeten Einstellungen. Wenn Sie für jeden Benutzer separate Einstellungen benötigen, verwenden Sie unterschiedliche Arbeitskonten. Das folgende Verfahren zeigt, wie Sie die Sprache, das Zahlenformat und die Zeitzone für jeden Lagerort-App-Benutzer ändern.

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Arbeitskraft**.
1. Suchen Sie hier den Namen der Arbeitskraft, die Sie einrichten möchten. Stellen Sie sicher, dass die Arbeitskraft über alle erforderlichen Lagerort-App-Benutzerkonten verfügt, die auf dem Inforegister **Benutzer** aufgeführt sind. Erstellen Sie nach Bedarf einen neue Arbeitskraft und/oder fügen Sie Benutzerkonten für die Lagerort-App hinzu, indem Sie die Schritte im Abschnitt [Einrichten von Benutzerkonten für Mobilgeräte](#set-wma-users) befolgen.
1. Wechseln Sie zu **Systemverwaltung \> Benutzer \> Benutzer**.
1. Wählen Sie das Benutzerkonto aus, in dem die **Person**-Spalte den Namen der Arbeitskraft zeigt, die Sie in Schritt 2 gefunden haben.

    > [!IMPORTANT]
    > Die Werte **Benutzer-ID**, die auf der Seite **Benutzer** aufgeführt sind, beziehen sich *nicht* auf den Wert, der auf dem Inforegister **Benutzer** der **Arbeitskraft**-Seite angezeigt wird, die Sie in Schritt 1 geöffnet haben.

1. Wählen Sie im Aktivitätsbereich **Benutzeroptionen**.
1. Legen Sie auf der Registerkarte **Voreinstellungen** die folgenden Felder fest:

    - **Sprache** – Wählen Sie die Sprache aus, die die Arbeitskraft bevorzugt. Dieses Feld steuert auch das Datumsformat, das in der Lagerort-App angezeigt wird.
    - **Datums-, Uhrzeit- und Zahlenformat** – Wählen Sie die Sprache aus, die die Zahlenformate bestimmt, die in der Lagerort-App angezeigt werden. Beachten Sie, dass die Datums- und Uhrzeitformate, die in der Lagerort-App angezeigt werden, tatsächlich vom **Sprache** Feld bestimmt werden, nicht durch dieses Feld.
    - **Zeitzone** – Wählen Sie die Zeitzone aus, in der die Arbeitskraft arbeitet. Dieses Feld wirkt sich auf den Zeitstempel für alle Registrierungen aus, die der Mitarbeiter über die App vornimmt.

> [!NOTE]
> In einigen Fällen kann die Lagerort-App bestimmte Mitarbeitereinstellungen nicht finden, die die Sprache, das Zahlenformat und die Zeitzone festlegen. Dabei gelten folgende Regeln:
>
> - Wenn die App nicht mit einer Supply Chain Management-Umgebung verbunden ist (z. B. beim ersten Start der App nach der Installation), wird die Sprache des lokalen Geräts verwendet. Wenn sich die Gerätesprache ändert, ändert sich auch die App-Sprache. Weitere Informationen zum Konfigurieren der Sprache für das lokale Gerät finden Sie in der Dokumentation zu Ihrem Gerät und/oder Betriebssystem.
> - Wenn die App mit einer Supply Chain Management-Umgebung verbunden ist, aber keine Einstellungen für den angemeldeten Mitarbeiter festgelegt sind, werden Sprache, Zahlenformat und Zeitzone basierend auf dem Konto ausgewählt, das der Client-ID zugeordnet ist, die das Gerät verwendet, um sich mit dem Supply Chain Management zu verbinden. Weitere Informationen finden Sie unter [Erstellen und Konfigurieren eines Benutzerkontos in Supply Chain Management](install-configure-warehouse-management-app.md#user-azure-ad).

> [!TIP]
> Wenn Sie feststellen, dass für Registrierungen, die über die Lagerort-App vorgenommen wurden, falsche Zeitstempel angezeigt werden, müssen Sie möglicherweise die Zeitzone anpassen, die für das Benutzerkonto festgelegt ist, mit dem sich Mitarbeiter bei Supply Chain Management anmelden und/oder authentifizieren. Wie bereits erwähnt, kann die Zeitzoneneinstellung aus dem Benutzerkonto stammen, das zum Anmelden bei der Lagerort-App verwendet wird, wie es auf der Seite **Arbeitskraft** eingerichtet wurde. Wenn das Benutzerkonto nicht auf der **Arbeitskraft**-Seite eingerichtet ist, stammt die Zeitzone alternativ aus dem Benutzerkonto, das mit der Client-ID verknüpft ist, die für die Authentifizierung verwendet wird, wie es auf der Seite **[Azure Active Directory Anwendungen](install-configure-warehouse-management-app.md)** eingerichtet ist.
