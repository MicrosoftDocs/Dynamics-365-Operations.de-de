---
title: Neuerungen oder Änderungen in Dynamics 365 for Operations Version 1611 (1611. November 2016)
description: In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 for Operations Version 1611 entweder neu oder geändert sind.
author: sericks007
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 221294
ms.assetid: 357931ed-f843-4bf5-bc85-0da3de0619ec
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4b0397b7120769969c4c7aae16dd2a2b3ec97371
ms.sourcegitcommit: 4d6ec2b1a9674712e1efb8c46b919d554f21a2b3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2019
ms.locfileid: "2627587"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-operations-version-1611-november-2016"></a>Neuerungen oder Änderungen in Dynamics 365 for Operations Version 1611 (1611. November 2016)

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 for Operations Version 1611 entweder neu oder geändert sind.

## <a name="cost-accounting"></a>Kostenrechnung

<table>
<thead>
<tr>
<th>Wie Sie vorgehen können</th>
<th>Warum dies wichtig ist</th>
</tr>
</thead>
<tbody>
<tr>
<td>Definieren Sie Kostenelementdimensionen und importieren Sie Kostenelement-Dimensionsmitglieder.</td>
<td>Kostenelemente werden in der Kostenrechnung verwendet, um Kosten zu kategorisieren und den Kostenfluss zu dokumentieren. Die primären Kostenelemente werden entweder importiert, indem Sie einen Microsoft Dynamics 365 for Operations-Datenkonnektor verwenden, um die Hauptkonten direkt aus Operations abzurufen, oder indem Sie einen allgemeinen Datenkonnektor verwenden, mit dem Sie Hauptkonten in Microsoft Excel von jedem anderen Quellsystemtyp abrufen. Nachdem die Hauptkonten in die Kostenrechnung importiert wurden, werden sie als Kostenfaktordimensionsmitglieder verwendet. Die sekundären Kostenfaktoren sind benutzerdefiniert und werden in Zuweisungen zum Dokumentieren des Kostenflusses verwendet.</td>
</tr>
<tr>
<td>Zuordnen von Kostenelementdimensionen.</td>
<td>Wenn die Hauptkonten der juristischen Personen aufgrund der gesetzlichen Kostenrechnungsrichtlinien nicht freigegeben werden können, können Sie sie zuordnen, nachdem Sie sie in die Kostenrechnung importiert haben, um eine holistische Ansicht der Organisation zu erhalten.</td>
</tr>
<tr>
<td>Definieren Sie Kostenobjektdimensionen und importieren Sie Kostenobjekt-Dimensionsmitglieder.</td>
<td>Kostenträger sind alle Typen von Objekten, denen Kosten zugewiesen werden. Typische Kostenträger sind unter Anderem Produkte, Projekte, Ressourcen, Abteilungen, Kostenstellen und geografische Regionen. Sie können entweder einen Microsoft Dynamics 365 for Operations-Datenkonnektor verwenden, um Finanzdimensionen und Werte von Operations abzurufen, oder einen allgemeinen Datenkonnektor, mit dem Sie Dimensionen und Werte per Excel aus einem anderen Quellsystemtyp abrufen. Wenn Sie beispielsweise die Kostenstellenfinanzdimension als die Objektdimension verwenden, sind alle Kostenstellen, die importiert werden, die Dimensionswerte für den Kostenträger.</td>
</tr>
<tr>
<td>Definieren oder Importieren von statistischen Dimensionen.</td>
<td>Statistische Dimensionselemente werden in den nicht-monetären Einheiten, beispielsweise Maschinenstunden, Mitarbeiteranzahl und Quadrat gemessen. Sie werden in Aufstellungen oder als Basis für Verteilungen und Zuweisungen verwendet.</td>
</tr>
<tr>
<td>Anbietervorlagen für statistische Maßnahmen erstellen.</td>
<td>Eine statistische Kennzahl-Anbietervorlage wird verwendet, um Dynamics 365 for Operations-Daten in statistische Kennzahlen umzuwandeln. Die Vorlage wird dann einem bestimmten statistischen Dimensionsmitglied zugeordnet. Die Vorlagen sind vorgefiltert, sodass sie nur die Tabellen anzeigen, denen Finanzdimensionen zugeordnet sind.</td>
</tr>
<tr>
<td>Kostenrechnungs-Sachkonten erstellen.</td>
<td>Ein Kostenrechnungs-Sachkonto ist ein agnostisches Sachkonto, das einen eigenen Kalender und eine eigene Währung verwendet. Es spielt eine wichtige Rolle im Verarbeiten aller Kostenbuchungen. Beispiel: Für ein Kostenrechnungssachkonto werden Kosten basierend auf eigenen Kostenfaktoren klassifiziert und basierend auf eigenen Objektdimensionen aggregiert. Sie können beliebig viele Kostenrechnungssachkonten erstellen, um Verwaltungsberichte aus verschiedenen Perspektiven zu erstellen.</td>
</tr>
<tr>
<td>Kostensteuerungseinheiten erstellen.</td>
<td>Kostenkontrollsteuereinheiten bilden die Kostenstruktur und definieren den Kostenfluss in einem Kostenrechnungssachkonto. Sie müssen einer Kostenträgerdimension zugeordnet werden, um die Kostenträgerdimensionen im Sachkonto darzustellen.</td>
</tr>
<tr>
<td>Hauptbucheinträge verarbeiten.</td>
<td>Um die tatsächliche Leistung zu messen, benötigen Sie Daten. Die Daten werden importiert, indem die Konnektoren verwendet werden, die für das Kostenrechnungssachkonto definiert sind. Wenn Sie die Hauptbucheinträge verarbeiten, werden die Daten inkrementell importiert.</td>
</tr>
<tr>
<td>Budgeteinträge verarbeiten.</td>
<td>Um die budgetierte Leistung zu messen, benötigen Sie Daten. Die Daten werden importiert, indem die Konnektoren verwendet werden, die für das Kostenrechnungssachkonto definiert sind. Wenn Sie die Budgeteinträge verarbeiten, werden die Daten inkrementell importiert.</td>
</tr>
<tr>
<td>Erstellen und Anwenden von Kostenverhaltensregeln.</td>
<td>Sie können eine Kostenverhaltensregel verwenden, um Kosten als Fixkosten, variable Kosten oder halbvariable Kosten zu klassifizieren. Eine Richtlinie ist regelbasiert und datumsbezogen. Standardmäßig werden alle Kosten als nicht klassifiziert markiert, bis Sie eine Kostenverhaltensrichtlinie anwenden und die Auswirkungen der Regel berechnen. Nach der Berechnung werden die Kosten klassifiziert.</td>
</tr>
<tr>
<td>Ablaufverfolgungskosten.</td>
<td>Zum einfachen Verständnis der Auswirkungen von Kostenrichtlinien können Sie mit der Kostenrechnung Kosten bis zu den Quellwerten und den angewendeten Regeln am Ursprung verfolgen. Diese Funktionen bieten vollständige Nachverfolgbarkeit zu auftretenden Kosten, den Kostenarten und den angewendeten Kostenverhaltensregeln.</td>
</tr>
<tr>
<td>Dimensionshierarchien definieren.</td>
<td>Dimensionshierarchien können Sie entweder zu Kategorisierungs- oder Klassifizierungszwecken erstellen. So können Sie eine Kategorisierungshierarchie definieren, die auf einer Kostenfaktordimension und den Mitgliedern basiert. Wahlweise können Sie eine Klassifizierungshierarchie definieren, die auf einer Kostenobjektdimension und den Mitgliedern basiert. Die Berichterstellungsstrukturen werden in den folgenden Situationen verwendet:
<ul>
<li>Definieren Sie Zuweisungen, Kostensätze und Kostenrollupregeln.</li>
<li>Sie zeigen Auszüge an, indem Sie den Arbeitsbereich verwenden.</li>
<li>Sie definieren den Zugriff, um aggregierte Daten anzuzeigen.</li>
<li>Sie zeigen Daten in Excel an.</li>
</ul></td>
</tr>
<tr>
<td>Erstellen Sie Auszüge, die im Arbeitsbereich angezeigt werden können.</td>
<td>Verwenden Sie den Arbeitsbereich, um sich schnell einen Überblick über die tatsächlichen und budgetierten Kosten und die Abweichungen zu verschaffen. Sie können die Daten nach Zeitraum oder Kostenebene filtern. Der Arbeitsbereich ist für Manager vorgesehen, die für Kostensteuerung zuständig sind. Er unterliegt den Zugriffsregeln, die für die Dimensionshierarchien definiert werden.</td>
</tr>
<tr>
<td>Erstellen Sie Berichte mit Excel.
<blockquote>[!NOTE] Führen Sie die Stapelverarbeitung Microsoft Excel 2016.</blockquote>
</td>
<td>Sie können Kostenrechnungsdaten direkt als Excel-Datenentitäten exportieren und Microsoft-PivotTable verwenden, um Berichte zu erstellen.</td>
</tr>
</tbody>
</table>

## <a name="expense-management"></a>Spesenverwaltung

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| Kreditkartenbuchungen des ausgeschiedenen Mitarbeiters neu zuweisen. | Wenn ein Mitarbeiter gekündigt wird, kann es vorkommen, dass dessen Konto der Active Directory-Domänendienste (AD DS) deaktiviert wird, wenn aktive Kreditkartenbuchungen importiert werden, die als Aufwand gebucht werden müssen. Bisher konnten Sie keinen Stellvertreter für Speseneinträge zuweisen oder die Kreditkartenbuchungen zu Spesenabrechnung zuordnen. Sie können nun die Seite **Kreditkartenbuchungen** verwenden, um den Mitarbeiter für eine Kreditkartenbuchung neu zuzuweisen, wo der zugeordnete Mitarbeiter ausgeschieden ist. Nachdem die Kreditkartenbuchung neu zugewiesen wurde, kann die Buchung für eine Spesenabrechnung ausgewählt werden und über den regulären Prozess für Spesenabrechnungsrückerstattung bezahlt werden. |
| Ändern Sie die Kreditkarteninformationen für Ausgaben für ausstehende und ehemalige Mitarbeiter. | Sie können die Kreditkarteninformationen für die Spesenverwaltung für ausstehende Arbeitskräfte und ehemalige Arbeitskräfte ändern. Bisher konnten Sie die Ausgabenenkreditkarteninformationen nur ändern, wenn die Arbeitskraft ein aktiver Mitarbeiter war. |
| Kopieren Sie einen Ausgabenbericht. | Sie können vorhandene Ausgaben jetzt kopieren, wenn Sie neue Kosten auf derselben Spesenabrechnung erstellen. Sie können eine Spesenabrechnung und alle zugeordneten Ausgaben, die nicht über eine Kreditkarte erfolgten, in eine neue Spesenabrechnung kopieren. Sie müssen alle erforderlichen Einzelaufzählungen noch ausführen und obligatorische Zugänge auf Grundlage definierter Ausgabenrichtlinien und Kategorien zuordnen. Sie können Kreditkartenbuchungen zur Spesenabrechnung hinzufügen, indem Sie auswählen, dass nicht abgestimmte Ausgaben hinzugefügt werden. |
| Massenbearbeitung von Spesen. | Einige Kreditkartenbuchungen können nicht zu einer Ausgabenkategorie zugeordnet werden, oder sie sind möglicherweise falsch zugeordnet, wenn diese importiert werden. In diesem Fall müssen Mitarbeiter die zugeordneten Ausgabenkategorie manuell ändern. Wenn Sie die nicht abgestimmten Ausgaben verwalten, können Sie die Ausgabenkategorie für die ausgewählten jetzt per Massenbearbeitung ändern. Wenn Sie darüber hinaus die für eine bestimmte Ausgabe ausgewählte Spesenabrechnung verwalten, können Sie das Projekt und die zusätzlichen Informationen per Massenbearbeitung ändern. |
| Ändern des Wechselkurses für Kreditkartenbuchungen. | Der tatsächliche Wechselkurs, der für eine Kreditkartenbuchung verwendet wird, unterscheidet sich möglicherweise vom Wechselkurs, der im System eingerichtet ist. Bisher konnten Mitarbeiter den Wechselkurs für eine Kreditkartenbuchung nicht ändern, die in die Ausgabenverwaltung importiert wurde. Sie können den Parameter jetzt auf der Seite **Ausgabenverwaltungsparameter** festlegen, um den für Kreditkartenbuchungen zu ändernden Kurs zuzulassen. |
| Korruptionsbekämpfungs-Bescheinigung für Ausgaben einrichten. | Einige Mitarbeiter einer Organisation arbeiten möglicherweise zusammen mit Regierungsbeamten, und einige Ausgaben, die als Teil dieser Arbeit auftreten, könnten als Bestechung angesehen werden. In der Ausgabenverwaltung können Sie jetzt eine Korruptionsbekämpfungs-Bescheinigung einrichten, die für ausgewählte Ausgabenkategorien angezeigt wird, wie z. B. Verpflegung und Präsente. Mitarbeiter müssen auswählen, ob Ausgaben, die für die Korruptionsbekämpfungs-Bescheinigung eingerichtet sind, den Kriterien entsprechen, die anhand der Richtlinien der Organisation definiert werden. |
| Verhindern Sie die manuelle Eingabe von Ausgaben für bestimmte Ausgabenkategorien. | Eine Ausgabenkategorie kann so eingerichtet werden, dass sie eine Kreditkartenbuchung angibt, für die die Kategorie nicht geändert werden kann. Ein Beispiel ist eine Gebühr können Mahngebühren der Kreditkarte sein. Sie können nun eine Ausgabenkategorie einrichten, die nur zulässt, dass Ausgaben durch den Import erstellt werden. Diese Funktion hindert Mitarbeiter daran, Ausgaben für die Kategorie manuell zu erstellen. Sie können auch die Kategorie nicht für Buchungen ändern, die importiert wurden und die angegebenen Kategorie verwenden. |
| Fügen Sie einen Beleg an mehrere Ausgaben an. | Eine Empfangsbestätigung, die zur Spesenverwaltung hochgeladen wurde, kann mehreren Ausgaben zugeordnet sein. Bisher musste ein Beleg, der mehreren Ausgaben zugeordnet wurde, einmal für jede Ausgabe hochgeladen werden. Sie können jetzt eine Empfangsbestätigung zu Ausgaben zuordnen, die bereits zu einer anderen Ausgabe auf derselben Spesenabrechnung hochgeladen und zugeordnet wurde. Wenn Sie darüber hinaus einen Zugang in die Kopfzeile der Spesenabrechnung hochladen, können Sie eine oder mehrere Positionen auswählen, die dem Beleg zugeordnet werden sollen. |
| Zukünftige Ausgaben erstellen. | Wenn Sie eine Spesenabrechnung kopieren, kann beispielsweise das Buchungsdatum für Ausgaben ein zukünftiges Datum haben. Vorherige Versionen lassen keine zukünftige Ausgaben zu. Sie können nun Ausgaben erstellen und speichern, die ein zukünftiges Datum aufweisen. Sie können jedoch zukünftige Ausgaben nicht übermitteln. |
| Konfigurieren Sie Ausgabenensteuern für ein Bundesland/Kanton. | In einigen Ländern/Regionen sind in möglicherweise Ausgaben, die in verschiedenen Bundesländern bzw. in den Kantonen anfallen, abhängig von verschiedenen Mehrwertsteuersätzen. Sie können jetzt die Ausgabenensteuerkonfigurationen auf Bundeslands-/Kantonsebene Kantonsebene einrichten und nicht nur auf Landes-/Regionsebene. Wenn Sie das Feld **Bundesland** auf der Seite **Steuerkonfiguration** leer lassen, wird die Mehrwertsteuergruppe auf alle Bundesländer/Kantone angewendet, die für die Länder/Regionen angegeben wurden. |
| Kreditkartentypen für Ausgaben einrichten. | Bisher gab es keine Seite, auf der Sie neue Kreditkartentypen, beispielsweise Visa, MasterCard oder Amex erstellen können, die mit der Spesenverwaltung verwendet werden können. Sie können nun Kreditkartentypen erstellen, um sie mit der Ausgabenverwaltung zu verwenden. Die Seite befindet sich im Bereich **Einstellungen** im Abschnitt **Berechnungen und Codes**. |
| Definieren eines mehrstufigen Genehmigungsworkflows für Spesenabrechnungen. | Ein neuer Workflow für Spesenabrechnungen unterstützt einen mehrstufigen Genehmigungsprozess. Mitarbeiter können die Zwischengenehmiger und den letzten Genehmiger eingeben, wenn sie die Spesenabrechnung erstellen. Der Workflow leitet dann die Spesenabrechnung zuerst zum Zwischengenehmiger. Nachdem die Spesenabrechnung auf dieser Ebene genehmigt wurde, leitet der Workflow sie an den letzten Genehmiger für die endgültige Zustimmung weiter. |
| Erstellen und verwalten Sie Ausgaben, die keiner Spesenabrechnung zugeordnet sind. | Der Benutzer kann nun Ausgaben erstellen und diese Ausgaben (beispielsweise über das Zuweisen oder das Aufschlüsseln von Belegen oder das Zuweisen von Gästen) verwalten, ohne zunächst eine Spesenabrechnung erstellen zu müssen. Eine oder mehrere Ausgaben können ausgewählt und einer neuen Spesenabrechnung hinzugefügt werden, sodass sie zur Genehmigung übermittelt werden kann. Eine neue Seite für die Verwaltung von Ausgaben ist verfügbar unter **Ausgabenverwaltung** &gt; **Eigene Ausgaben** &gt; **Ausgaben**. |

## <a name="financial-management"></a>Finanzverwaltung

<table>
<thead>
<tr>
<th>Wie Sie vorgehen können</th>
<th>Warum dies wichtig ist</th>
</tr>
</thead>
<tbody>
<tr>
<td>Hier können Sie Anlagenbewertungen verfolgen, indem Sie ein einzelnes "Buch"-Konzept verwenden.</td>
<td>Bisher wurden zwei verschiedene Bewertungstypen verwendet, um Anlagenwerte zu verfolgen: Wertmodelle und Abschreibungsbücher. In der aktuellen Version wurden diese beiden Konzepte in einem einzelnen Bewertungskonzept mit dem Namen "Bücher" zusammengeführt. Bücher haben alle Funktionen von Wertmodellen und Abschreibungsbüchern. Beispielsweise können Sie Buchungen im Hauptbuch deaktivieren. Bücher, die im Hauptbuch buchen, werden in der Regel für Unternehmensfinanzberichte verwendet. Bücher, die nicht im Hauptbuch buchen, können für die Steuererklärung verwendet werden.</td>
</tr>
<tr>
<td>Führen Sie den Hauptbuchjahresabschluss für mehrere juristische Personen aus.</td>
<td>Wenn Sie den Jahresabschlussprozess beschleunigen möchten, können Sie den Jahresabschluss jetzt für mehrere juristische Personen auf einer freigegebenen Jahresabschlussseite ausführen. Gruppen juristischer Personen können gemeinsam mit Einstellungen definiert werden, die von einem Jahr zum nächsten beibehalten werden sollen. Andere Benutzerfreundlichkeitserweiterungen sind ebenfalls in den Jahresabschlussprozess eingegangen.</td>
</tr>
<tr>
<td>Nutzen Sie Erweiterungen der Hauptbuchneubewertung der Fremdwährung.</td>
<td>Die folgenden Erweiterungen wurden am Hauptbuchprozess für eine Neubewertung der Fremdwährung vorgenommen:
<ul>
<li>Ein Wechselkurstyp wurde zum Hauptkonto hinzugefügt. Dieser Wechselkurstyp wird verwendet, um den Wechselkurs für die Währungsaufwertung zu bestimmen. Wenn kein Wechselkurstyp definiert ist, wird der Prozess fortgesetzt, um den Wechselkurstyp zu verwenden, der für das Sachkonto festgelegt wird.</li>
<li>Es ist nun einfacher, einen Bereich von Hauptkonten und Währungen auszuwählen, für die die Neubewertung durchgeführt wird.</li>
<li>Neubewertung kann für mehrere juristische Personen ausgeführt werden.</li>
<li>Das System behält jetzt den Verlauf jedes Neubewertungsprozesses bei, der ausgeführt wurde, sowie für Debitor-(AR)- und Kreditor-(AP)-Neubewertungen.</li>
<li>Wenn Sie den Prozess ausführen, können Sie die Ergebnisse der Neubewertung in einer Vorschau anzeigen. Die Vorschau zeigt die Ergebnisse für alle juristischen Personen an, für die der Prozess ausgeführt wurde. Sie können dann alle oder einige juristischen Personen aus der Vorschau buchen. Sie können die Ergebnisse der Vorschau auch nach Excel exportieren.</li>
</ul></td>
</tr>
<tr>
<td>Transaktionen für zusätzliche Buchungsebenen anzeigen.</td>
<td>Auf der Listenseite <strong>Zwischenbilanz</strong> und im Bericht <strong>Dimensionsaufstellung</strong> können Sie die zusätzlichen Buchungsebenen jetzt auswählen, die im Hauptbuch hinzugefügt wurden. Wenn Sie die zusätzlichen Buchungsebenen auswählen, werden die Regulierungen für diese Buchungsebenen in Salden auf der Listenseite oder im Bericht einbezogen.</td>
</tr>
<tr>
<td>Fügen Sie Anleitungsdokumentation zur Finanzperiodenabschlussvorlage hinzu.</td>
<td>Bisher konnten Sie Dokumentation anfügen, nachdem eine Aufgabe abgeschlossen wurde. So können Sie beispielsweise einen Bericht anfügen, der generiert wurde. Sie können jetzt auch ein Anleitungsdokument an die Vorlage anfügen. Dieses Anleitungsdokument wird anschließend in jede Aufgabe im Finanzperiodenzeitplan kopiert, damit der Aufgabeneigentümer Anweisungen zum Abschluss der Aufgabe anzeigen.</td>
</tr>
<tr>
<td>Definieren Sie die Verrechnungseinrichtung auf einer gemeinsamen Seite.</td>
<td>Die <strong>Verrechnungseinstellungsseite</strong> wird nun gemeinsam genutzt, sodass eine Organisation alle Paare von juristischen Personen definieren kann, die miteinander Transaktionen abwickeln können. Darüber hinaus können Sie eine Buchung zur ursprünglichen juristischen Person eingeben, jedoch nicht von der juristischen Zielperson. Wenn jede juristische Person eine Verrechnungsbuchung initiieren kann, muss das reziproke Paar definiert werden. Daher wird die juristische Zielperson auch als ursprüngliche juristische Person eingerichtet.</td>
</tr>
<tr>
<td>Begründungsdokumente für Budgetpläne übermitteln.</td>
<td>Sie können eine Begründungsvorlage als zusätzliche Dokumentation für die angeforderten Beträge erstellen. Benutzer können die Details der Vorlage ausfüllen und die Vorlage an den Budgetplan anfügen, damit er während des Genehmigungsprozesses verwendet werden kann.</td>
</tr>
<tr>
<td>Aktivieren Sie erweiterte Regeln für Budgetregistereinträge.</td>
<td>Wenn erweiterte Regeln im Hauptbuch konfiguriert sind, können die Regeln für neue Einträge und Umbuchungen ins Budgetregister verwendet werden.</td>
</tr>
<tr>
<td>Nutzen Sie die erweiterte Sichtbarkeit der Vorauszahlungsrechnungsstellungsaktivität.</td>
<td>Eine neue Liste <strong>Offene Vorauszahlungen</strong> enthält eine Momentaufnahme des Status der Vorauszahlungsrechnungsstellungsaktivität. Die Seite stellt der Kreditoren-Abteilung Informationen zu Bestellungen zur Verfügung, die verbleibende Vorauszahlungswerte haben, die noch fakturiert werden müssen, fakturierte Werte, die gezahlt werden müssen, und bezahlte Rechnungswerte, die auf die Standardrechnungen angewendet werden müssen. Darüber helfen Erweiterungen für die automatische Anwendung von entlohnten Vorauszahlungsrechnungen bei Standardrechnungen den Zahlungsbearbeitern bei der effizienteren Dateneingabe.</td>
</tr>
<tr>
<td>Verwenden Sie den <strong>Arbeitsbereich für Kreditor-Kooperationsrechnungen</strong>.</td>
<td>Mit dem neuen Arbeitsbereich <strong>Rechnungsstellung</strong> im Bereich <strong>Kreditor-Kooperation</strong> können externe Kreditoren auf ihre eigenen Rechnungsdaten zugreifen. Kreditoren können beispielsweise sehen, ob eine Rechnung bezahlt wurde, und ihre eigene Rechnung senden. Diese Änderung bietet eine effizientere und fristgerechtere Kommunikation mit externen Kreditoren. Deshalb haben die Zahlungsbearbeiter weniger Unterbrechungen.</td>
</tr>
<tr>
<td>Juristische Personen während der Rechnungseingabe wechseln.</td>
<td>Verbesserungen lassen Zahlungsbearbeiter, die Rechnungen für mehrere juristische Personen eingeben müssen, schnelle Änderungen an der juristischen Person über die Rechnungsstellungsseiten vornehmen. Diese Funktion erspart den Zahlungsbearbeitern Zeit, da sie sich nicht mehr bei der aktuellen juristischen Person abmelden und bei einer anderen juristischen Person anmelden müssen. Sowohl die Seite <strong>Globale Rechnungserfassung</strong> als auch die Seite <strong>Kreditorenrechnungen</strong> ermöglicht es Benutzern, die juristische Person bei der Dateneingabe zu ändern.</td>
</tr>
<tr>
<td>Unterstützung für elektronische Dateien beim Internal Revenue Service (IRS) 1099 kombinierten Bundes-/Landeseinreichungsprogramm</td>
<td>Wenn der Konfigurationsschlüssel für die <strong>USA</strong> aktiviert ist, bietet der Prozess zur elektronischen 1099-Übermittlung zusätzliche Funktionen, die mit IRS-Bestimmungen für das kombinierte Bundes-/Landeseinreichungsprogramm übereinstimmen. Dieses Programm wurde vom IRS eingerichtet, damit Informationensrücklieferungen zu den elektronischen Teilnahmebundesländern weitergeleitet werden können.</td>
</tr>
<tr>
<td>Ausgleichserweiterungen</td>
<td>Erweiterungen unterstützen Zahlungsmitarbeiter beim effizienteren Ausgleich, da die Sekretäre für die gleiche Rechnung mehrere nicht gebuchte Zahlungen zum Ausgleich verwenden können.</td>
</tr>
<tr>
<td>Unternehmensübergreifende Ansicht</td>
<td>Mitarbeiter für zentralisierte Zahlungen können jetzt unternehmensübergreifend überfällige Rechnungen anzeigen. Die Arbeitsbereiche <strong>Kreditorenzahlungen</strong> und <strong>Debitorenzahlungen</strong> bieten jetzt eine bessere Transparenz und Kontrolle bei überfälligen Rechnungen, indem Sie eine Möglichkeit zur Anzeige und Filterung von Unternehmen bieten, die Teil einer Organisationshierarchie für zentralisierte Zahlung sind.</td>
</tr>
<tr>
<td>Verwenden Sie den <strong>Bankwesen</strong>-Arbeitsbereich.</td>
<td>Ein neuer <strong>Bankwesen</strong>-Arbeitsbereichs hilft beim Verfolgen von Bankkonten und Salden für die juristischen Personen. Laufende und ausstehende Salden sind umgehend für alle Konten verfügbar, und Sie können von den Salden in tiefer die detaillierten Buchungsbelege gelangen. Sie können die historischen Saldodaten für jedes Bankkonto oder eine Zusammenfassung für alle Bankkonten des Unternehmens in sowohl kurzfristigen als auch Langzeitansichten anzeigen. Sie können bessere Einblicke in Bankkontoabstimmung erhalten, da das Datum der letzten Abstimmung für jedes Bankkonto gemeldet wird, und es gibt einen Indikator für Abstimmungen, die sich in Bearbeitung befinden.</td>
</tr>
<tr>
<td>Elektronischen Bankauszug für alle juristischen Personen in einem einzelnen Schritt importieren.</td>
<td>Sie können jetzt elektronische Bankauszüge für alle juristischen Personen in einem einzelnen Schritt importieren. Bankauszugsdateien können Auszüge vielen Bankkonten und juristischen Personen enthalten, und ZIP-Dateien können mehrere Bankauszugsdateien enthalten. Mithilfe eines einzelnen Importprozess können Sie die Abstimmung für alle gemeldeten Bankkonten für alle juristischen Personen starten. Durch dieses Feature können Sie Zeit sparen, da Sie nicht zwischen Unternehmen und mehrere Auszugsimporten wechseln müssen. Sie können außerdem Übereinstimmungsregeln für alle importierten Auszüge in jedem Unternehmen automatisch ausführen.</td>
</tr>
<tr>
<td>Bewertungsnachverfolgung</td>
<td>Eine einzelne Anlage kann mehrere Bewertungen für unterschiedliche Buchungsstandards haben und kann optional die zugehörigen Buchungen im Hauptbuch buchen. Bisher wurden diese Bewertungen nachverfolgt, indem entweder Wertmodelle oder Abschreibungsbücher verwendet werden. Sie können dieser Bewertungen, die jetzt als Bücher bezeichnet werden, erfassen indem Sie einen gemeinsamen Satz von Erfassungen, Abfragen und Berichten verwenden. Die einheitliche Umgebung vereinfacht die Implementierung und verringert die Anzahl von Schnittstellen, die die periodischen Verfahren benötigen.</td>
</tr>
<tr>
<td>Nutzen Sie Erweiterungen für unternehmensübergreifende Abschreibungsausführungen.</td>
<td>Sie können nun eine Abschreibungsausführung für Anlagen aller juristischen Personen über eine einzelne Seite beginnen. Sie können die Erfassungen auch automatisch buchen, nachdem diese erstellt wurden. Sie können die Erstellung und die Buchung von Erfassungen zur Stapelverarbeitung senden, damit die Abschreibungsausführung im Hintergrund ausgeführt wird. Diese Erweiterungen reduzieren ineffiziente Verfahren, da Sie keine einzelnen Abschreibungsausführungen separat für jedes Unternehmen starten müssen. Die Erweiterung ermöglicht auch eine bessere zentralisierte Verwaltung von Anlagen.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Human Capital Management

<table>
<thead>
<tr>
<th>Wie Sie vorgehen können</th>
<th>Warum dies wichtig ist</th>
</tr>
</thead>
<tbody>
<tr>
<td>Leistungserfassung erstellen.</td>
<td>Vor dem Abschluss einer Prüfung sammeln Sie häufig Informationen zu Aktivitäten oder Ereignissen, die Ihnen während der Überprüfungsperiode bei Ihrer Arbeit geholfen haben. Sie können einen Eintrag zur Leistungserfassung hinzufügen, um diese Aktivitäten und Ereignisse zu dokumentieren. Sie können die Aktivitäten und Ereignisse mit einem Ziel oder einer Leistungsbeurteilung verbinden, um weitere Informationen für den Prüfer bereitzustellen.</td>
</tr>
<tr>
<td>Erstellen Sie weitere ausführliche Ziele.</td>
<td>Sie haben mehr Kontrolle über den Inhalt der Ziele, die Sie festgelegt haben. Sie können Messungen für die Ziele erstellen, Leistungsjournaleinträge mit Messungen verknüpfen und Dokumente anfügen und anzeigen. Sie können Ziele als Vorlagen speichern und sie für die schnelle Einrichtung wieder verwenden.</td>
</tr>
<tr>
<td>Erstellen Sie ausführliche Leistungsbeurteilungen.</td>
<td>Leistungsbeurteilungen, die formal als Diskussionen bekannt sind, sind nun so flexibel, dass fortlaufende Rückmeldungen und formellere Prüfungen unterstützt werden. Sie können aktive Ziele einbeziehen und Kommentare dazu abgeben sowie Abschnitte für eine Prüfung der Kompetenzen hinzufügen. Es werden zusätzliche Abschnitte bereitgestellt, in denen Sie Messungen, Leistungsjournaleinträge, Anhänge und Abzeichnungen hinzufügen oder anzeigen können, die in Verbindung mit der Genehmigung stehen.</td>
</tr>
<tr>
<td>Ordnen Sie zusätzliche Positionshierarchien zu Workflows zu.</td>
<td>Sie können einen Workflow einer Positionshierarchie zuordnen. Sie können auch die Workflowschritte ändern, um den Genehmigungsprozess zu optimieren, damit er Ihren geschäftlichen Anforderungen entspricht. Daher können Sie eine effektive Genehmigungsstruktur definieren, die für die verschiedenen Berichtsbeziehungsinformationen passt, die in Ihrer Organisation verwendet werden.</td>
</tr>
<tr>
<td>Workflowsupport zum Eingeben von Geheimzahlen (PINs) im Mitarbeiter-Self-Service.</td>
<td>Die Workflowfunktionen für die Personalverwaltung (HR) wurden erweitert und bieten jetzt Unterstützung für PINs. Mitarbeiter können Ihre PIN zur Effizienzsteigerung hinzufügen und bearbeiten. Allerdings können diese Informationen von Personalverwaltungsarbeitskräften hinsichtlich der Genauigkeit und Vollständigkeit geprüft werden, bevor sie dem Datensatz des Mitarbeiters hinzugefügt werden.</td>
</tr>
<tr>
<td>Erstellen Sie Zielvorlagen, und verwenden Sie diese, um neue Ziele hinzufügen.</td>
<td>Sie können Zielvorlagen für Zielsetzungen erstellen, die von vielen Mitarbeitern im Unternehmen verwendet werden. Mitarbeiter können über eigene Vorlagen Ziele hinzufügen, Manager können Ziele für ihr Team aus einer Vorlage hinzufügen, und Personalverwaltungsteammitglieder können Ziele für Mitarbeiter im Unternehmen hinzufügen.</td>
</tr>
<tr>
<td>Erstellen Sie Zielgruppen, und verwenden Sie diese, um neue Ziele hinzufügen.</td>
<td>Sie können Zielvorlagen einer Gruppe hinzufügen und die Gruppe verwenden, um ein oder mehrere Ziele für einen Mitarbeiter, ein Team, eine Position, eine Abteilung oder das Unternehmen zu erstellen.</td>
</tr>
<tr>
<td>Mehr Kontrolle über das Überprüfungsverfahren.</td>
<td>Sie können einen Workflow zur Steuerung des Überprüfungsverfahrens verwenden. Sie können Prüfungsvorlagen erstellen und diese verwenden, um Prüfungen erstellen. Darüber hinaus können Sie auch Bewertungen zu einer Prüfung hinzufügen.</td>
</tr>
<tr>
<td>Verwenden Sie Berichtszeiträumen, um den Zeitrahmen für die Prüfung zu definieren.</td>
<td>Sie können eine Zeitperiode für eine Leistungsbeurteilung definieren, und Start- und Enddatum der Prüfung werden automatisch eingegeben. Sie können diese Standarddaten nach Bedarf ändern.</td>
</tr>
<tr>
<td>Zugriff auf fünf neue Power BI-Inhaltspakete für die Personalverwaltung</td>
<td>Die neuen Inhaltspakete aktivieren die Personalverwaltungsorganisation und Personalverwaltungsmanager, um Folgendes zu analysieren:
<p>Arbeitskraftkennzahlen</p>
<ul>
<li>Demographische Aufschlüsselungen nach Alter und Geschlecht, Familienstand</li>
<li>Vergleichen Sie Abgangsraten über die Jahre und finden Sie eine Liste der Gründe, warum Mitarbeiter die Organisation verlassen.</li>
<li>Hier wird eine Liste der offenen Stellen sowie einen Vergleich von den offenen zu den geschlossenen Positionen angezeigt</li>
</ul>
<p>Vergütungen/Vorteile</p>
<ul>
<li>Vergleichen Sie Mitarbeiter im Stundenlohn und mit Fixlohn</li>
<li>Hier wird die Anzahl der Mitarbeiter angezeigt, die für Vorteile registriert sind</li>
<li>Hiermit werden Mitarbeiter angezeigt nach Beschäftigungstyp</li>
</ul>
<p>Personalbeschaffung</p>
<ul>
<li>Analysieren Sie Bewerber auf Basis der Anzahl von Bewerbern, , woher sie kommen und für welche Position sie sich bewerben</li>
</ul>
<p>Organisationsschulungen</p>
<ul>
<li>Kurserfassung nach elektronischer Adresse</li>
<li>Kursanwesenheit nach Status</li>
<li>Liste von Mitarbeitern, die Kurse angemeldet sind</li>
</ul>
<p>Mitarbeiterkompetenzen und -entwicklung</p>
<ul>
<li>Liste der Fähigkeiten nach Mitarbeitern</li>
<li>Aufschlüsselung von Fähigkeitstypen nach Teammitglied</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="localizations"></a>Lokalisierungen

<table>
<thead>
<tr>
<th>Wie Sie vorgehen können</th>
<th>Warum dies wichtig ist</th>
</tr>
</thead>
<tbody>
<tr>
<td>Lokalisierungen sind für weitere 18 Länder verfügbar:
<ul>
<li>Österreich</li>
<li>Belgien</li>
<li>Brasilien</li>
<li>China</li>
<li>Tschechische Republik</li>
<li>Estland</li>
<li>Finnland</li>
<li>Ungarn</li>
<li>Italien</li>
<li>Lettland</li>
<li>Litauen</li>
<li>Norwegen</li>
<li>Polen</li>
<li>Saudi-Arabien</li>
<li>Spanien</li>
<li>Schweden</li>
<li>Schweiz</li>
<li>Thailand</li>
</ul>
<p>Die folgenden Länder benötigen auch Lokalisierung. Die Lokalisierung für diese Länder ist noch nicht abgeschlossen und für H1 2017 geplant:</p>
<ul>
<li>Brasilien</li>
<li>Tschechische Republik</li>
<li>Estland</li>
<li>Ungarn</li>
<li>Lettland</li>
<li>Litauen</li>
<li>Malaysia</li>
<li>Polen</li>
<li>Schweden</li>
</ul>
</td>
<td>Dynamics 365 for Operations ist in zusätzlichen 18 Ländern verfügbar. Im Rahmen unserer Bemühungen, die Lokalisierung zu vereinfachen und konfigurierbarer zu machen, wurden gesetzliche elektronische Berichterstellungsfeatures zu ER-Konfigurationen (Electronic reporting) umgewandelt, und einige gesetzlich vorgeschriebene Microsoft SQL Server Reporting Services (SSRS)-Berichte wurden zu ER-Konfigurationen umgewandelt, die Excel-Vorlagen verwenden. Diese konvertierten Funktionen werden speziell weiter unten in dieser Tabelle angegeben.</td>
</tr>
<tr>
<td>Japan – Gruppieren von Anlagen, wenn Sie das Formular 26 und zugeordnete Tabellen drucken.</td>
<td>Das Formular 26 muss an jeden Ort gesendet werden, in dem das Unternehmen arbeitet. Zum Speichern der Arbeit, wenn Sie das Formular 26 drucken, können Anlagen automatisch nach Standort gruppiert und sortiert werden.</td>
</tr>
<tr>
<td>Japan – Anzeige der Beträge für schnellere und zusätzliche Abschreibung im Profil.</td>
<td>Das Profil kann eine genaue Vorkalkulation der Beträge für beschleunigte und zusätzliche Abschreibungen bereitstellen.</td>
</tr>
<tr>
<td>Japan – Progressive Berechnung der Quellensteuer.</td>
<td>Die japanische Regierung fordert, dass Sie die Quellensteuer progressiv basierend auf dem Zahlungsbetrag berechnen.</td>
</tr>
<tr>
<td>Japan – Importieren Sie die Postleitzahlendatei für bestimmte große Unternehmensgebäude.</td>
<td>Die Postleitzahlendatei, die von der Behörde für bestimmte große Unternehmensgebäude bereitgestellt wird, kann in das System importiert werden. Die Adresse kann dann aus den Postleitzahlen berechnet werden.</td>
</tr>
<tr>
<td>Japan – Konfigurieren eines Leerlaufzeitraums für Anlagen.</td>
<td>Leerlaufzeiträume gestatten dem Benutzer die Anlagenabschreibung während eines angegebenen Zeitraums. Diese Funktionalität ist gesetzlich erforderlich.</td>
</tr>
<tr>
<td>Europa – Konfigurieren Sie eine Mehrwertsteuer (VAT)-Registrierungsnummer für die Adresse einer Partei, indem Sie das Registrierungskennungs-Framework verwenden.</td>
<td>Sie können eine MwSt.-Registrierungsnummer für die Adresse einer Partei mithilfe des Registrierungskennungs-Frameworks und der neuen Registrierungskategorie <strong>MwSt-Kennung</strong> konfigurieren.</td>
</tr>
<tr>
<td>Finnland – Konfigurieren Sie eine Zoll-Debitorennummer für die Adresse einer Partei, indem Sie das Registrierungskennungs-Framework verwenden.</td>
<td>Sie können eine Zoll-Debitorennummer für die Adresse einer Partei mithilfe des Registrierungskennungs-Frameworks und einer neuen Registrierungskategorie <strong>Zolldebitorkennung</strong> konfigurieren.</td>
</tr>
<tr>
<td>Frankreich – Drucken von Debitorenrechnungen in einem für Frankreich spezifischen Layout.</td>
<td>Der Debitorenrechnungsausdruck wird angepasst, um französische Besonderheiten zu erfüllen.</td>
</tr>
<tr>
<td>Frankreich – Erzwingen von chronologischer Nummerierung von Dokumenten nach Finanzzeiträumen.</td>
<td>Um spezifische französische Anforderungen bei der Nummerierung von Debitorenrechnungen zu ermöglichen, können Sie Nummernkreise für Debitorenrechnungen pro Finanzzeitraum einrichten.</td>
</tr>
<tr>
<td>Lokalisierung Österreich – ER-Konfigurationen</td>
<td>
<ul>
<li>XML-Format der zusammenfassenden Meldung für Österreich</li>
<li>Intrastat-Format für Österreich</li>
<li>ISO20022 Kredittransferzahlungsformat für Österreich</li>
<li>ISO20022 Lastschriftzahlungsformat für Österreich</li>
<li>EDIFACT-PAYMUL-Format für Österreich</li>
<li>Mehrwertsteuererklärung für Österreich</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung Belgien – ER-Konfigurationen</td>
<td>
<ul>
<li>BLWI-Format für Belgien</li>
<li>XML-Format der zusammenfassenden Meldung für Belgien</li>
<li>Bericht 'Anlagen' für Belgien</li>
<li>Intervat-Format für Belgien</li>
<li>Intrastat-Format für Belgien</li>
<li>Rechnungsumsatzbericht für Belgien</li>
<li>Sachkontobuchungsexportformat für Belgien</li>
<li>SWIFT-Kreditorenzahlungsformat für Belgien</li>
<li>Importformat für CODA-Bankauszug für Belgien</li>
<li>ISO20022 Kredittransferzahlungsformat für Belgien</li>
<li>ISO20022 Lastschriftzahlungsformat für Belgien</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung Brasilien – ER-Konfigurationen</td>
<td>
<ul>
<li>GIA SP für Brasilien</li>
<li>GIA-ST für Brasilien</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung Tschechische Republik – ER-Konfigurationen</td>
<td>
<ul>
<li>XML-Format der zusammenfassenden Meldung für die Tschechische Republik</li>
<li>Intrastat-Format für die Tschechische Republik</li>
<li>Mehrwertsteuererklärung für die Tschechische Republik</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung China – ER-Konfigurationen</td>
<td>
<ul>
<li>Format "Debitorenfälligkeitsbericht" für China</li>
<li>Analyse-Berichtsformat für fälligen Betrag des Debitors für China</li>
<li>Format "Kreditorenfälligkeitsbericht" für China</li>
<li>Analyse-Berichtsformat für fälligen Betrag des Kreditors für China</li>
<li>Format 'Fälligkeitsanalyse für Debitorenzahlung' für China</li>
<li>Format "Debitorensaldenbericht" für China</li>
<li>Format "Sachkontosaldenbericht" für China</li>
<li>Format "Kreditorensaldenbericht" für China</li>
<li>GBT-Datei für China</li>
<li>Format für Golden-Steuerexportdatei</li>
<li>Produktionsverbrauchs-Abweichungsberichtsformat für China</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung Estland – ER-Konfigurationen</td>
<td>
<ul>
<li>XML-Format der zusammenfassenden Meldung für Estland</li>
<li>Intrastat-Format für Estland</li>
<li>Bestandsreklassifikationsauszug für Estland</li>
<li>ISO20022 Kredittransferzahlungsformat für Estland</li>
<li>Debitorenkreditorensaldo-Begriffsbericht für Estland</li>
<li>Mehrwertsteuererklärung für Estland</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung Finnland – ER-Konfigurationen</td>
<td>
<ul>
<li>Zusammenfassende Meldung TXT-Format für Finnland</li>
<li>Intrastat-Format für Finnland</li>
<li>ISO20022 Kredittransferzahlungsformat für Finnland</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung Ungarn – ER-Konfigurationen</td>
<td>
<ul>
<li>XML-Format der zusammenfassenden Meldung für Ungarn</li>
<li>Intrastat-Format für Ungarn</li>
<li>Vereinfachtes Intrastat-Format für Ungarn</li>
<li>Exportformat für Rechnungsliste für Ungarn</li>
<li>Mehrwertsteuererklärung für Ungarn</li>
<li>Aufgeschlüsselte Mehrwertsteuererklärung für Ungarn</li>
<li>Bestandsauszug für Ungarn</li>
<li>MultiCash-Zahlungsformat für Ungarn</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung Italien – ER-Konfigurationen</td>
<td>
<ul>
<li>Intrastat-Format für Italien</li>
<li>Projektrechnungsformat für Italien</li>
<li>Verkaufsrechnungsformat für Italien</li>
<li>ISO20022 Kredittransferzahlungsformat für Italien</li>
<li>ISO20022 Lastschriftzahlungsformat für Italien</li>
<li>RIBA-Inkassoüberweisungsformat für Italien</li>
<li>Buchungsbericht für Inlandssteuer für Italien</li>
<li>Bericht mit der schwarzen Liste für Italien</li>
<li>Modello770-Bericht für Italien</li>
<li>Bericht zur jährlichen Steuermitteilung für Italien</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung Lettland – ER-Konfigurationen</td>
<td>
<ul>
<li>Bericht zur Barbelegnutzung (LV)</li>
<li>Zusammenfassende Meldung XML-Format für Lettland</li>
<li>Korrekturen für zusammenfassende Meldung XML-Format für Lettland</li>
<li>Intrastat (A)-Format für Lettland</li>
<li>Intrastat (B)-Format für Lettland</li>
<li>Bestandsinventurliste für Lettland</li>
<li>Bestandsinventuraufstellung für Lettland</li>
<li>Lagerumlagerung für Lettland</li>
<li>Lieferschein für interne Umlagerung für Lettland</li>
<li>Bestandsumgliederungsdokument für Lettland</li>
<li>ISO20022 Kredittransferzahlungsformat für Lettland</li>
<li>Mehrwertsteuererklärung für Lettland</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung Litauen – ER-Konfigurationen</td>
<td>
<ul>
<li>XML-Format der zusammenfassenden Meldung für Litauen</li>
<li>Intrastat-Format für Litauen</li>
<li>Bestandsauszug für Litauen</li>
<li>Kredittransferzahlungsformat ISO20022 für Litauen</li>
<li>Interner Debitoren/Kreditoren-Abstimmungsbericht für Litauen</li>
<li>Mehrwertsteuererklärung für Litauen</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung Norwegen – ER-Konfigurationen</td>
<td>
<ul>
<li>Mahnschreibenformat für Norwegen</li>
<li>AutoGiro-Zahlungsformat für Norwegen</li>
<li>AvtaleGiro-Debitorenzahlungsformat für Norwegen</li>
<li>eFaktura-Debitorenzahlungsformat für Norwegen</li>
<li>ISO20022 Kredittransferzahlungsformat für Norwegen</li>
<li>NETS-Zahlungsformat für Norwegen</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung Polen – ER-Konfigurationen</td>
<td>
<ul>
<li>Intrastat-Format für Polen</li>
<li>Lagerortdokumente für Polen</li>
<li>Bestandsumgliederungsdokument für Polen</li>
<li>MultiCash-Zahlungsformat für Polen</li>
<li>MultiCash-Fremdwährungs-Zahlungsformat für Polen</li>
<li>Debitorenkreditorensaldo-Bestätigungsbericht für Polen</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung Saudi-Arabien – ER-Konfigurationen</td>
<td>Bank-Kreditbrief sonst. Zuschlags-Zuweisungsformat für Saudi-Arabien</td>
</tr>
<tr>
<td>Lokalisierung Spanien – ER-Konfigurationen</td>
<td>
<ul>
<li>Zusammenfassende Meldung TXT-Format für Spanien</li>
<li>Intrastat-Format für Spanien</li>
<li>Projektrechnungsformat für Spanien</li>
<li>Verkaufsrechnungsformat für Spanien</li>
<li>ISO20022 Kredittransferzahlungsformat für Spanien</li>
<li>ISO20022 Lastschriftzahlungsformat für Spanien</li>
<li>Format "Spanisches MwSt.-Registrierbuch"</li>
<li>Format "Zusammenfassung des Spanischen MwSt.-Registrierbuchs"</li>
<li>Meldung 347-ASCII-Export für Spanien</li>
<li>Bericht zur Meldung 347 für Spanien</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung Schweden – ER-Konfigurationen</td>
<td>
<ul>
<li>Intrastat-Format für Schweden</li>
<li>Bankgirot Autogiro-Debitorenzahlungsformat für Schweden</li>
<li>Bankgirot-Kreditorenzahlungsformat für Schweden</li>
<li>SWIFT-Kreditorenzahlungsformat für Schweden</li>
<li>SIE-Exportformat für Schweden</li>
<li>ISO20022 Kredittransferzahlungsformat für Schweden</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisierung Schweiz – ER-Konfigurationen</td>
<td>
<ul>
<li>DebitDirect-Zahlungsformat für die Schweiz</li>
<li>LSV-Direktbelastungs-Zahlungsformat für die Schweiz</li>
<li>ISO20022 Kredittransferzahlungsformat für die Schweiz</li>
<li>ISO20022-Direktbelastungs-Zahlungsformat für die Schweiz</li>
<li>Importformat für ESR-Bankauszug für die Schweiz</li>
</ul>
</td>
</tr>
<tr>
<td>Deutschland – Exportkreditorenzahlungen im DTAZV-Format</td>
<td>Deutschland erforderlich DTAZV mit fremder Formatspezifikation, durch die eine Meldung der Banküberweisung (Kreditorenzahlung) gemäß Angabe grenzüberschreitende Zahlungen von Deutschland an ein Konto bei einer Auslandsbank oder an eine inländische Bank in einer Fremdwährung darstellt.</td>
</tr>
</tbody>
</table>

### <a name="electronic-reporting"></a>Elektronische Berichterstellung

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| Konfigurieren Sie ER-Berichte, um Daten in mehreren Formaten vom Dokumentverwaltungsspeicher in generierte elektronische Nachrichten einzufügen. | ER-Berichte können Daten in vom Dokumentverwaltungsspeicher generierte elektronische Nachrichten einfügen. Daher können die Anhänge eines Geschäftsdokuments in Übereinstimmung mit den gesetzlichen Anforderungen zu elektronischen Nachrichten hinzugefügt werden, die für dieses Dokument generiert wurden. Diese Anlagen können derzeit im MIME-Format zu einer XML-Nachricht hinzugefügt werden, die generiert wurde. Alternativ können die Anhänge in einer binären Nachricht im Base64-Format hinzugefügt werden, die generiert wurde. |
| Konfigurieren Sie ER-Berichte, um elektronische Dokumente in Excel, Microsoft Word oder im PDF-Format zu generieren. | Eine Konfiguration aktiviert ER-Berichte, um elektronische Dokumente in drei verschiedenen Formaten zu generieren: OpenXML-Arbeitsblatt (Excel), Word und XML-Formulardatenformat (XFDF) (PDF). Benutzer können ein Format auswählen, indem sie eine Formatvorlage zu einem ER-Bericht als Excel-, PDF- oder Word-Dokument hinzufügen. |
| Konfigurieren Sie ER-Berichte, um Daten in Kopf-und Fußzeilen elektronischer Dokumente einzufügen, die im OpenXML-Arbeitsblattformat generiert werden, und um Seitenumbrüche zu steuern. | Er-Berichte können Geschäftsdaten in Kopf-und Fußzeilen einfügen und bestimmen auch, wo Seitenumbrüche auftreten. Daher können die Berichte über statische obere und untere Bereiche für Seiten der elektronischen Dokumente verfügen, die generiert wurden. Sie können auch spezifisches Paging dieser Dokumente unterstützen, damit sie gesetzlichen Anforderungen entsprechen. |
| Konfigurieren Sie das Ziel der ER-Berichte so, dass die Ausgabe als E-Mail gesendet wird und dass Daten sowie ER-Logik (Ausdrücke) verwendet werden können, um zur Laufzeit die zu verwendende E-Mail-Adresse anzugeben. | Wenn Sie bisher ein ER-Ziel konfigurierten, konnte die E-Mail-Adresse des Empfängers der Ausgabe zur Entwurfszeit definiert werden. Sie können jetzt einen Ausdruck im ER-Format konfigurieren. Dieser Ausdruck kann anschließend in einem Ziel als Quelle der E-Mail-Adresse für jede Formatkonfiguration und jede Ausgabekomponente separat ausgewählt werden (Ordner oder Datei). Wenn daher ein ER-Bericht ausgeführt wird, kann jede Datei, die erzeugt wird, an einen anderen Empfänger gesendet werden, und die E-Mail-Adresse kann auf Grundlage von ER-Logik und Geschäftsdaten definiert werden. |
| Konfigurieren Sie das Ziel der ER-Berichte, sodass die Ausgabe entweder als benannte neue Datei oder eine neue Version der vorhandenen Datei an den Microsoft SharePoint-Ordner gesendet wird und dass die Daten im Microsoft Power BI-Framework entweder als Datensatz oder als Bericht verwendet werden können. | Wenn Sie ER-Berichte konfigurieren, können Sie jetzt problemlos (ohne programmieren zu müssen) die angeforderten Daten vorbereiten, damit diese im Power BI-Framework verwendet werden können. Wenn Sie diese ER-Berichte ausführen, können Sie das Power BI-Framework mit entsprechenden Geschäftsdaten und/oder Excel-Berichten versorgen, die bereits zur Verfügung stehen. Wenn Sie die Berichtsausführung im regelmäßigen Modus planen, können Sie den geplanten Push der Geschäftsdaten von Dynamics 365 for Operations zu Power BI so einrichten, dass der Aktualisierungszeitplan der Power BI-Berichte unterstützt wird. |
| Konfigurieren Sie ER-Berichte, um einen Teil des elektronischen Dokuments zu verwenden, das bereits als Datenquelle generiert wurde, um den Rest des Dokuments zu generieren. | Sie können ER-Berichte konfigurieren, die die Ausgabe im Textformat erstellen, um die Zeilenzählung des Dokuments zu verwenden. Diese Informationen können dann in anderen Teilen des Dokuments verwendet werden, um Positionen zu erstellen, die zusammenfassende Details enthalten. Die zusammengefassten Informationen (Summen und Nummern) können in den generierten elektronischen Dokumenten berechnet und gedruckt werden, ohne dass zusätzliche Umwandlungen der Daten erforderlich sind. Daher kann diese Funktion die Leistung der Berichtsausführung verbessern und hilft bei der zukünftigen Wartung des konfigurierten ER-Formats. |
| Konfigurieren Sie ER-Berichte, um die Dateinamenerweiterung für elektronische Dokumente anzugeben, die im Textformat generiert wurden. | Sie können ER-Berichte konfigurieren, um die Ausgabe im Textformat zu erstellen, sodass sie als Datei mit einer bestimmten Erweiterung gespeichert werden können. Neben der TXT-Standarderweiterung können Sie Erweiterungen wie CSV und PRN entsprechend den Formatspezifikationen konfigurieren. |
| Erstellen Sie neue ER-Berichte, die auf einer bestimmten Version eines ER-Modells basieren. | Wenn Sie bisher ein neues ER-Format erstellt haben, konnte nur die aktuelle Version des ausgewählten ER-Modells als Datenquellenspeicherort für das Format verwendet werden. Sie können jetzt jede verfügbare Version des ausgewählten ER-Modells auswählen. Durch diese Funktion können Sie ER-Berichte während des aktuellen Jahres verwalten und parallel dazu eine neue Version des ER-Modells für das nächste Jahr entwerfen. |
| Durchsuchen Sie Datenquellen und Formate/Modelle nach Text oder einem ausgewähltem Artefakt mit einem Mausklick. Lösen Sie Rebasierungskonflikte proaktiv, und lösen Sie Konflikte zwischen Konfigurationen. Konfigurieren Sie ER-Berichte, um mehrere Prüfungsnachrichten für Fehler zu erstellen, die gesucht werden, bis die Berichtsausführung beendet ist. | Einige Verbesserungen der Benutzerfreundlichkeit (UX) in den helfen ER-Frameworkbenutzern beim effizienteren und einfacheren Arbeiten mit ER. |
| Zeigt den **ER**-Arbeitsbereich in Power BI-Berichten an. | Benutzer können die Seite **ER-Arbeitsbereich** konfigurieren, sodass diese neue Menüoptionen und Live-Kacheln umfasst, die die Power BI-basierten Berichte ausführen. |

## <a name="payroll"></a>Lohnabrechnung

<table>
<thead>
<tr>
<th>Wie Sie vorgehen können</th>
<th>Warum dies wichtig ist</th>
</tr>
</thead>
<tbody>
<tr>
<td>Konfigurieren Sie Lohndatensätze und verarbeiten Sie Lohnzahlungen, indem Sie Funktionen verwenden, die den Funktionen des Moduls <strong>Lohn</strong> in Microsoft Dynamics AX 2012 R3 entsprechen.</td>
<td>Sie können nun US-Lohnzahlungen konfigurieren und verarbeiten, indem Sie eine Reihe von Funktionen verwenden, die dem Funktionsumfang von AX 2012 R3 entsprechen.
<ul>
<li>Sie können Lohnzyklen und Lohnperioden, Arbeitszyklen und Arbeitsperioden, Einkommenscodes und Einkommenscodegruppen, Zeitpläne, Sonderurlaubstypen und Vorteilsabgrenzungspläne konfigurieren.</li>
<li>Sie können erforderliche Abzüge für Vorteile und Steuern einrichten und Lohndaten für Positionen sowie Arbeitskräfte für die Berichterstellung und zu Analysezwecken erfassen.</li>
<li>Sie können Abzüge für Pfändungen und Steuerabgaben und für alle zugeordneten Verwaltungsgebühren einrichten und verwalten.</li>
</ul>
</td>
</tr>
<tr>
<td>Überwachen und verarbeiten Sie den Lohnperiodenprozess, indem Sie den neuen Arbeitsbereich <strong>Lohnverwaltung</strong> verwenden.</td>
<td>Sie können nun die Lohnverarbeitung problemlos überwachen. Lohnadministratoren können auf einen Blick Einnahmen- und Zahlungsaufstellungen anzeigen, die Aufmerksamkeit erfordern, sodass der Zahlungslauf genau und vollständig verläuft. Im Arbeitsbereich <strong>Lohnverwaltung</strong> können Benutzer End-to-End-Prozesse von einem einzigen Arbeitsbereich überwachen und ausführen.</td>
</tr>
<tr>
<td>Datei für positive Lohnzahlungsschecks generieren.</td>
<td>Es gibt eine neue Erweiterung für die positive Lohnabrechnungsfunktionen von "Bargeld- und Bankverwaltung". Es wurden separate Menüoptionen im Kernprozess hinzugefügt, um eine eigene Konfiguration für Lohnzahlungen zu ermöglichen. Die Funktionen sind identisch mit der Kernfunktion für positive Lohnzahlungen, die in Anwendungsversion 7.0.1 von Microsoft Dynamics AX (Mai 2016) enthalten ist. Aufgrund dieser Erweiterung, werden Lohnabrechnungsdaten vollständig aus den restlichen positiven Lohnbuchungen separiert. Durch diese Isolation wird sichergestellt, dass Lohnzahlungsbenutzer nur auf Daten in Verbindung mit der Lohnkomponente zugreifen und diese anzeigen können.</td>
</tr>
<tr>
<td>Importieren Sie Gewinnaufteilungspositionen aus einer externen Quelle, indem Sie die neue Gewinnaufstellungspositionen-Entität verwenden.</td>
<td>Eine wichtige neue Daten-Entität ermöglicht Integration in externe Zeit- und Einnahmeberechnungssysteme. Die Datenentität importiert Gewinnaufteilungspositionen und führt die gesamte Standardlogik aus, die der Benutzer direkt in der Gewinnaufstellung eingegeben hat. Nach dem Importieren werden diese Positionen automatisch dem entsprechenden Gewinnaufteilungsdokument zugeordnet. Wenn kein geeignetes Gewinnaufteilungsdokument vorhanden ist, wird automatisch ein Dokument erstellt.</td>
</tr>
</tbody>
</table>

## <a name="planning-and-scheduling"></a>Zeitplanung

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| Legen Sie Standardauftragseinstellungen für Verkäufe und Käufe basierend auf beliebigen aktiven Produktdimensionen im Produktmaster fest. Sie können deshalb Standardauftragseinstellungen für die Lagermengeneinheit (SKU) oder eine teilweise SKU definieren. | Sie können Standard-Auftragseinstellungsregeln für eine Produktdimension oder eine Kombination aus Produktdimensionen definieren.<p>**Beispiel**</p><p>Sie verkaufen ein Produkt namens "Polo-T-Shirt". Das Produkt ist in zwei Farben verfügbar: "Grün" und "Blau". Es ist auch in zwei Größen verfügbar: "Small" und "Medium". Farbe und Größe sind aktive Produktdimensionen für "Polo-T-Shirt". Sie können Einkäufe aller grünen Polo-T-Shirts unabhängig von deren Größe blockieren.</p> |

## <a name="product-master-data"></a>Produktmasterdaten

<table>
<thead>
<tr>
<th>Wie Sie vorgehen können</th>
<th>Warum dies wichtig ist</th>
</tr>
</thead>
<tbody>
<tr>
<td>Richten Sie alle Standardauftragseinstellungen und standortspezifischen Auftragseinstellungen gleichzeitig auf einer Seite ein.</td>
<td>Diese Funktion bietet einen besseren Überblick über Artikeleinstellungen.</td>
</tr>
<tr>
<td>Erstellen Sie eine Bezeichnung für Produktvariantennummern.</td>
<td>Sie können Elemente wie Produktdimensionen, Attribute und Zeichen in die Produktvariantennummern einbeziehen. Sie können schnell die bestimmte Produktvariante suchen, wenn Sie einen Auftrag oder eine Bestellung erstellen.</td>
</tr>
<tr>
<td>Suche nach Produkten und Produktvarianten in Verkaufs- und Einkaufszenarien.</td>
<td>Wenn Sie eine Bestellposition oder eine Auftragsposition erstellen, können Sie nach Produkten suchen, indem Sie Produktdimensionen und beliebige Produktnummern mit Ausnahme der globalen Geschäftsartikelnummern (GTINs) und Strichcodes verwenden. Diese Suche ist eine Volltextsuche, die die vorhandene "Beginnt mit"-Suche ersetzt, die in der Auftrags- und Einkaufssuchliste verwendet wird. Mit dieser Funktion suchen Sie nach Produktgruppen, die vergleichbare Eigenschaften, oder einem einzelnen Produkt, das eindeutige Merkmale hat. Um diese Funktion zu aktivieren, wählen Sie den Parameter <strong>Produktsuche über die Suche ermöglichen</strong> auf der Seite <strong>Suchparameter</strong> aus.</td>
</tr>
<tr>
<td>Geben Sie die Produktvariante direkt an, wenn Sie eine Verkaufs- oder Einkaufstransaktion erstellen. Alternativ können Sie aus einer Liste mit zulässigen Dimensionskombinationen auswählen.</td>
<td>Diese Funktion ist eine Produktivitätserweiterung.
<p><strong>Beispiel</strong></p>
<p>Sie verkaufen ein Produkt namens "Polo-T-Shirt". Das Produkt ist in zwei Farben verfügbar: "Grün" und "Blau". Es ist auch in zwei Größen verfügbar: "Small" und "Medium". Farbe und Größe sind aktive Produktdimensionen für "Polo-T-Shirt". Wenn Sie eine Auftragsposition für "Polo-T-Shirt" mit der Farbe "Grün" und der Größe "Small" eingeben, müssen Sie keine Daten in den Feldern <strong>Artikelnummer</strong>, <strong>Farbe</strong> und <strong>Größe</strong> eingeben. Sie können die Position erstellen, indem Sie einen der folgenden Schritte verwenden:</p>
<ul>
<li>Geben Sie im Feld <strong>Artikelnummer</strong> die Produktvariantennummer, den Wert einer Farbe oder die Größe ein. In der Suche finden Sie die spezifische Variante, die Sie verkaufen möchten, und erstellen Sie die Auftragsposition.</li>
<li>Geben Sie im Feld <strong>Artikelnummer</strong> die Artikelnummer ein. Wechseln Sie zu einem beliebigen Produktdimensionsfeld. In der Suche <strong>Produktdimension</strong> finden Sie alle in Frage kommenden Dimensionskombinationen, die für Polo-T-Shirt gelten. In einem Schritt können Sie die Produktvariante auswählen, die Sie verkaufen möchten.</li>
</ul>
</td>
</tr>
<tr>
<td>Geben Sie an, ob auf buchungsbezogenen Seiten Produktnummern angezeigt werden.</td>
<td>Die buchungsbezogenen Seiten, beispielsweise "Aufträge" und "Bestellungen", zeigen nur die Felder <strong>Artikelnummer</strong> und <strong>Produktname</strong> an. Um das Feld <strong>Produktnummer</strong> anzuzeigen, legen Sie den <strong>Produktnummern in Formularen anzeigen</strong>-Parameter unter <strong>Parameter für Produktinformationsverwaltung</strong> fest.</td>
</tr>
</tbody>
</table>

## <a name="project-management-and-accounting"></a>Projektverwaltung und -verrechnung

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| Verwenden Sie späte Auswahl, wenn Sie Rechnungsvorschläge in einem Stapel buchen. | Projektbuchhalter können einen Stapelverarbeitungsauftrag einrichten, um Rechnungsvorschläge für die Buchung automatisch aufzuheben, wenn die Vorschläge Kriterien entsprechen, die im Stapelverarbeitungsauftrag angegeben werden. Diese Funktion verbessert die Automatisierung der Rechnungsbuchung, da der Stapelverarbeitungsauftrag fortlaufend ausgeführt werden kann und automatisch Vorschläge für die Buchung aufnimmt. |
| Erstellen Sie Analysen in Power BI-Desktop. | Business Intelligence (BI)-Inhalte für projekt- und ressourcenbezogene Daten können in Power BI-Desktop einfach erstellt werden. |
| Verwenden Sie Bestellungsvorauszahlungen und schließen Sie sie ordnungsgemäß im Projektvorkalkulationsprozess ein. | Bei Projektbestellungen müssen Vorauszahlungen verarbeitet werden, bevor eine Zahlung an die Kreditoren freigegeben werden kann. Diese Vorauszahlungsrechnungen werden jetzt in der Projektvorkalkulation/Anerkennungsprozess für Projekte des Typs **Festpreis** angezeigt. |
| Greifen Sie auf Kosten- und Umsatzerlösschätzungen sowie Artikelbedarf direkt aus einer Projektstrukturplanaufgabe (PSP) zu. | Sie können Vorkalkulationen, Umsatzerlösschätzungen und Artikelbedarf für eine PSP-Aufgabe im Detaildialogfeld für diese Aufgabe im PSP-Planungsfenster verwalten. |
| Entnehmen Sie eine Finanzierungsquelle für Gebührenerfassungen. | Wenn der Vertrag für ein Projekt mehrere Finanzierungsquellen enthält, können Sie eine bestimmte Finanzierungsquelle auswählen, wenn Gebühren gebucht werden. Wenn Sie keine bestimmte Finanzierungsquelle auswählen, werden die Finanzierungsregeln verwendet, die im Vertrag angegeben sind, um die Gebühren zuzuteilen. |
| Öffnen Sie Projektaufstellungen in Excel. | Mit neuen Datenentitäten für Sachkontoaktualisierungen und Budgetaktualisierungen können Sie Projektaufstellungsdaten in Excel öffnen und Analysen mittels Excel-Funktionen erstellen. |
| Verwenden Sie nur einen Konfigurationsschlüssel, um die Funktionalität für die Projektverwaltung und Buchhaltung (PMA) zu aktivieren. | Die projektbezogenen Konfigurationsschlüssel wurden durch eine interne Projektkonfiguration ersetzt, die PMA-Funktionen aktiviert. |

## <a name="retail-and-commerce"></a>Einzelhandel und Handel

### <a name="advanced-warehouse-management-in-a-retail-store"></a>Erweiterte Lagerortverwaltung in einem Einzelhandelsgeschäft

Einzelhändler können die erweiterte Lagerortverwaltung (WHS)-Lösung in ihren Geschäften verwenden und die zur Unterstützung erforderlichen Aktualisierungen an den aktuellen Verkaufsstellen-Funktionen (POS) vornehmen. Die Verfahren der Handheldlösung sollten in einem Geschäft funktionieren wie in einem beliebigen anderen Lagerort. Alle aktuellen in Ladengeschäfts-Lagerbestands-Prozesse und alle POS-Prozesse, die Lagerbuchungen erstellen oder aktualisieren, werden aktualisiert, sodass sie die bestimmten Anforderungen für WHS-aktivierte Lagerorte nutzen.

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| Verwenden Sie den POS, um nach verfügbarem Lagerbestand in WHS-aktivierten Geschäften zu suchen. | Wenn Sie Bestand suchen, sollte der Prozess wie bisher funktionieren. Die Suche sollte den verfügbaren Lagerbestand auf Lagerortebene anzeigen und sollte die Lagerort-, Bestandsstatus- oder Ladungsträger-Dimensionen nicht berücksichtigen. |
| Verwenden Sie den POS, um einen Produktzugang für einen Umlagerungsauftrag in einem WHS-aktivierten Geschäft zu verarbeiten. | Sie können Umlagerungsaufträge am POS für ein WHS-aktiviertes Geschäft und Artikel erhalten. Der Benutzer sollte in der Lage sein, die empfangenden Lagerplätze auszuwählen, und er sollte in der Lage sein, Ladungsträger-IDs einzugeben, um die empfangenden Positionen automatisch auszufüllen. |
| Verwenden Sie den POS, um einen Produktzugang für einen Bestellungsauftrag in einem WHS-aktivierten Geschäft zu verarbeiten. | Sie können Bestellungsaufträge am POS für ein WHS-aktiviertes Geschäft und Artikel erhalten. Der Benutzer sollte in der Lage sein, die empfangenden Lagerplätze auszuwählen, und er sollte in der Lage sein, Ladungsträger-IDs einzugeben, um die empfangenden Positionen automatisch auszufüllen. |
| Verwenden Sie den POS, um die Lieferung von Produkten von einem WHS-aktivierten Geschäft zu verarbeiten. | Sie können Umlagerungen des POS für ein WHS-aktiviertes Geschäft und Artikel erfassen. Der Benutzer sollte in der Lage sein, die liefernden Lagerplätze auszuwählen, der Bestandsstatus sollte automatisch generiert werden, und die Ladungsträger sollten ignoriert werden. |

### <a name="enable-seamless-omni-channel-commerce"></a>Aktivieren Sie nahtlosen Mehrkanalhandel

Nahtloser Mehrkanalhandel bezieht sich auf die Verwaltung und Auftragsverarbeitung in physischen Geschäften, Online-Schaufenstern, Callcentern und mobilen Handelsumgebungen. In dieser Version wurden folgende Investitionen in diesem Bereich ausgeführt:

- Verbesserungen beim Veröffentlichen von E-Commerce-Schaufenstern
- Eine neue mobile App für Endverbraucher, die Produkterfassung, Kontoverwaltung und Onlineeinkauf ermöglicht

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| Verbraucher: Die aktuelle Version der App für Endverbraucher aktiviert die folgenden Merkmale – Produktsuche, Kategoriesuche, Einkaufswagen und Auschecken als Gast. Einzelhändler können das Branding des Unternehmens auf die App anwenden und dann als Paket für die App-Stores für Android iOS veröffentlichen. | Einzelhändler können auf einfache Weise eine Endverbraucher-App erstellen, mit der Kunden als Gast über ihre Mobilgeräte Produkte suchen und liefern lassen können. |
| Kundenwunschzettel für E-Commerce-Online-Schaufenster | Unabhängige Softwarehersteller (ISVs) können das Wunschzettelsteuerelement verwenden, um Benutzer mehrere Listen in ihrem Online-Schaufenster erstellen und verwalten zu lassen und diese Listen am POS anzuzeigen. |
| Asynchrone Kundenerstellung über E-Commerce-Online-Schaufenster | ISVs können jetzt Kundenkonten erstellen, auch wenn der Commerce Data Exchange-Echtzeitservice nicht verfügbar ist. |
| Veröffentlichen Sie Kanalprodukte vom Retail Server in Schaufenstern von Drittanbietern. | Retail Server unterstützt nun Service-zu-Service-Authentifizierung. ISVs können jetzt die Kanalproduktveröffentlichung von Retail Server in Schaufenstern von Drittanbietern nutzen. |

### <a name="extensibility"></a>Erweiterbarkeit

- Handelsablaufprojekte werden jetzt vom Retail SDK versiegelt.
- Einfachere Bereitstellung und Verwaltung von Microsoft-Komponentenpaketen sowie ISV-Paketen für den POS, Retail Server, Datenbanken, Zahlungen und Hardwarestationen.

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| CRT/Retail Server: Einzelhändler oder ISVs können das CRT durch Erweiterungshooks erweitern. Inlinecodeänderungen werden nicht mehr unterstützt. | Um fortlaufende Integration und fortlaufende Bereitstellung zu aktivieren, sollten Sie Inlinecodeänderungen vollständig vermeiden. Dies dient außerdem einer einfachen Implementierung von Hotfixes ohne Codezusammenführungen sowie der Bereitstellung von CRT-Komponenten. |

### <a name="personalized-product-recommendations"></a>Personalisierte Produktempfehlungen

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| Zeigen Sie personalisierte Produktempfehlungen an mehreren Touchpoints an POS an, um festzustellen, woran ein Kunde möglicherweise aufgrund seiner Einkaufshistorie, seiner Elemente auf der Wunschliste, anderer Elemente, die von anderen Kunden online und in Filialen eingekauft wurden, interessiert ist. | Im Falle von Einzelhändlern mit großen Katalogen helfen personalisierte Empfehlungen dem Kunden dabei, Produkte zu entdecken. Den Shopmitarbeitern stehen dadurch informierte Kunden gegenüber. Indem Produkte zur Schau gestellt werden, die sich an den Interessen und Kaufgewohnheiten eines Kunden orientieren, erhalten Einzelhändler Upsell-Möglichkeiten und die Kundenbindung wird gestärkt. In Retail werden die Produktempfehlungen durch kognitive Dienste und Microsoft Azure Machine Learning unterstützt. |

### <a name="pos-task-recorder"></a>POS-Aufgabenaufzeichnung

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| Einzelhändler können POS-Aufgabenaufzeichnung verwenden, um Trainingsmaterial, Geschäftsprozessmodellierer (BPM)-Diagramme und Hilfeinhalt für eine Erhöhung der Produktivität und für bessere Analysen sowie Anwendungsentwürfe zu generieren. | Um fortlaufende Integration und fortlaufende Bereitstellung zu aktivieren, sollten Sie Inlineänderungen vollständig vermeiden. Dies dient außerdem einer einfachen Implementierung von Hotfixes ohne Codezusammenführungen sowie der Bereitstellung von CRT-Komponenten. |
| Echtzeithilfe im POS. | Kassierer/Manager können Echtzeithilfe von POS für Geschäftsprozesse abrufen, ohne den Kontext zu wechseln. |

### <a name="store-system-providing-a-seamless-on-premises-store-experience"></a>Shopsystem: Bereitstellen einer nahtlosen lokalen Shoperfahrung

Das Shopsystem ist eine Bereitstellungs-Auswahl für Einzelhändler, mit deren Hilfe eine Reihe von Geschäftsvorgängen in einem lokalen Shop, in der öffentlichen Microsoft-Cloud oder der eigenen privaten Cloud des Kunden unterstützt werden. In dieser Version ist der Bereich nur ladenintern. Um die Unterstützung für Umgebungen zu verbessern, die langsame unzuverlässige Netzwerkkonnektivität haben, müssen wir eine Option für Einzelhändler zur Bereitstellung der Kanaldatenbank und von Retail Server im Shop zur Verfügung stellen. Anschließend können sie fortfahren, ihre Kerngeschäftsszenarien auszuführen, auch wenn keine Konnektivität mit der Zentralverwaltung besteht. Basierend auf den unterschiedlichen Datenpunkten, die Technikteamdiskussionen, Marktstudienergebnisse und Mitbewerberanalyse umfassen, haben wir den folgenden Lösungsumfang als Idealangebot für unsere Zielkunden identifiziert:

- Ein Self-Service-Paket ist für Shopsystem verfügbar.
- Die Standardinstallation ist eine One-Box-Bereitstellung, benutzerdefinierte Bereitstellung ist jedoch zulässig.
- Aktivieren Sie einfache Bereitstellung/Selbstwartung.
- Retail Server und die Shopdatenbank sind im Shop zusammen mit dem Async Client-Service enthalten.
- Retail Server kommuniziert im Shop direkt mit Application Object Server (AOS) in der Shopsystem-Hauptniederlassung.
- Unterstützt terminalübergreifende Szenarien, in denen keine Hauptniederlassungskonnektivität besteht.
- Retail Modern POS und Cloud POS kommunizieren immer mit Retail Server im Shop.
- Unterstützt Retail Modern POS und Cloud POS, wenn keine Hauptniederlassungskonnektivität besteht.
- Unterstützt eine Retail Modern POS-spezifische Offline-Datenbank (isoliert für jede Retail Modern POS-Instanz), wenn keine Hauptniederlassungskonnektivität besteht.
- Authentifizierung basiert ausschließlich auf Service-zu-Service für das Shopsystem.
- Echtzeitserviceanrufe werden nicht unterstützt, wenn keine Internet-Konnektivität besteht.
- Direkte Datenbankkonnektivität von Retail Modern POS mit der Kanaldatenbank wird nicht unterstützt.
- Aktivieren Sie Telemetrie/Überwachung.

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| Ein Einzelhändler lädt das Shopsystem-Self-Service-Installationsprogramm von der Kanaldatenbankseite in der Dynamics AX-Hauptniederlassung und die Konfigurationsdatei herunter. | Der Einzelhändler kann das Self-Service-Paket nahtlos herunterladen. |
| Ein Einzelhändler installiert das Shopsystem, indem er das Self-Service-Installationsprogramm verwendet. | Der Einzelhändler kann das Shopsystem installieren, indem er das Self-Service-Paket verwendet. |
| Der IT-Manager konfiguriert das Shopsystem in Dynamics 365 for Operations (Kanaldatenbank, Kanalprofil, Shop und Bereitstellungspaket). | Der IT-Manager kann das Shopsystem einfach und effizient konfigurieren. |
| Ein Einzelhändler betreibt Retail Modern POS im lokalen Shop und kann Echtzeitvorgänge ausführen, wie die Ausgabe von Geschenkkarten, wenn Konnektivität besteht. | Der Einzelhändler kann Echtzeitaktivitäten aus dem Shopsystem ausführen, sofern Konnektivität besteht. |
| Ein Einzelhändler kann Daten vom lokalen Shopsystem mit der Hauptniederlassung synchronisieren, wenn eine Verbindung besteht. | Der Einzelhändler kann in beide Richtungen mit dem Shopsystem synchronisieren, sofern Konnektivität besteht. |
| Ein Einzelhändler kann sichere Kommunikation zwischen dem lokalen Shopsystem und Hauptniederlassung nutzen. | Der Einzelhändler kann sicher vom Shopsystem kommunizieren, sofern Konnektivität besteht. |
| Der IT-Manager und Microsoft Operations können das lokale Shopsystem überwachen und Berichte erstellen (Diagnose- und Berichterstellungsänderungen). | Die IT-Manager und Microsoft Operations können das Shopsystem überwachen und Probleme effizient beheben. |

### <a name="universal-windows-platform-app-for-retail-modern-pos"></a>Universal Windows Platform-App für Retail Modern POS

Derzeit ist Retail Modern POS nur als Windows 8.1-Anwendung für Desktopcomputer und Tablets sowie als Cloud POS für Desktop- oder Tabletbrowser verfügbar. In dieser Version wurde Retail Moderns POS in einer Universelle Windows-Plattform-App konvertiert. Durch diese Änderung kann Retail Modern POS auf jedem Windows 10-Gerät Desktop (Desktop, Tablet oder Smartphone) ausgeführt werden und auf Geräten mit Continuum-Unterstützung sogar zwischen Ansichten wechseln.

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| Aktivieren Sie wichtige POS-Funktionen für kleinformatige Geräte. | Retail POS-Funktionen sind für Smartphones und andere kleinformatige Geräte verfügbar, auf denen Windows 10 ausgeführt wird. |

## <a name="supply-chain-management"></a>Lieferkettenverwaltung

### <a name="consignment-inventory"></a>Lieferbestand

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| Als Kreditor können Sie Rohmaterialien am Lagerort des Debitors lagern. Als Kunde können Sie den tatsächlichen Einkauf verschieben, bis das Rohmaterial für die Produktion erforderlich ist. | Ein Lagerbestand an Rohmaterialien kann erhebliche Kosten verursachen. Indem Lieferungsbestand verwendet wird, kann ein Kreditor Rohmaterialien am Lagerort des Debitors lagern. Der Kunde kann den tatsächlichen Einkauf verschieben, bis das Rohmaterial für die Produktion erforderlich ist. Rohmaterialien werden mit einem Unterlieferungs-Wiederbeschaffungsauftrag bestellt und empfangen. Der Wiederbeschaffungsauftrag zeichnet physische Transaktionen auf, wirkt sich jedoch nicht im Hauptbuch aus. Um zwischen Lagerartikeln im Debitorenbesitz und Kreditorenbesitz zu unterscheiden, können Sie die Bestandseigentümerdimension verwenden. Eigentümeränderungen für Lagerbestand werden von einem Erfassungsprozess verarbeitet, der die Eigentümerschaft vom Kreditorenbesitz in den Debitorenbesitz ändert. Dieser Prozess löst die Erstellung einer Bestellung und eines Produktzugangs aus.<blockquote>[!NOTE] Diese Funktion wurde auf eingehende Lieferung von Rohmaterialien für die Produktion beschränkt. Sie ist nicht in die Lagerortverwaltung (WHS) und die Transportverwaltung (TMS) integriert.</blockquote> |
| Als Kreditor erhalten Sie Informationen zur Menge des überlieferten Lagerbestands, der an den Debitor übergeben wird. | Um eine Rechnung für den Debitor zu erstellen, benötigt der Kreditor Informationen zu den Rohmaterialien, die vom Lieferungsbestand gekauft wurden, und zum Kaufdatum. Der Kreditor kann auch den verfügbaren Lagerbestand am Standort des Debitors mithilfe der Kreditoren-Zusammenarbeitsschnittstelle überwachen. |
| Verschieben Sie Lagerbestand im Kreditorenbesitz mit einer Umlagerungserfassung. | Wenn Sie die physische Position des Lagerbestands im Kreditorenbesitz nachverfolgen möchten, muss es möglich sein, die Position im System zu erfassen. Durch die Verwendung einer Umlagerungserfassung können Sie die Bewegung des physischen Bestands erfassen, wie z. B. die Bewegung von einem Lagerplatz an einem Lagerort zu einem anderen. |
| Passen Sie Lagerbestand im Kreditorenbesitz mit einer Inventurerfassung an. | Es ist wichtig, dass Sie den im System verfügbaren Lagerbestand konsistent mit dem tatsächlichen physischen Bestand synchron halten. Der Lagerbestand im Kreditorenbesitz kann mithilfe von Zählverfahren wie Mengenanpassungs- und in Inventurerfassungsprozessen angepasst werden. |
| Finden Sie sich über Lieferungssupport in Dynamics 365 for Operations | Weitere Informationen zur Unterstützung von Lieferungsprozessen erhalten Sie unter [Lieferung](../../../supply-chain/inventory/consignment.md), [Lieferung einrichten](../../../supply-chain/inventory/set-up-consignment.md), [Erstellen eines neuen Unterlieferungs-Wiederbeschaffungsauftrags (Aufgabenleitfaden)](../../../supply-chain/inventory/tasks/create-consignment-replenishment-order.md) und [Ändern des Besitzes des Lieferungsbestandes auf Grundlage des Produktionsbedarfs (Aufgabenleitfaden)](../../../supply-chain/inventory/tasks/change-ownership-consignment.md). |

### <a name="vendor-collaboration-previously-known-as-the-vendor-portal"></a>Kreditorenzusammenarbeit (bisher als Kreditorenportal bezeichnet)

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| Ermöglichen Sie Kreditoren, auf jede Bestellposition zu reagieren und Änderungen vorzuschlagen. | In einigen Fällen möchten Kreditoren mehrere Bestellpositionen akzeptieren und andere ablehnen. Kreditoren können Bestellpositionen nun einzeln verwalten. Jede Position kann abgelehnt, übernommen oder mit Änderungen akzeptiert werden. So können Kreditoren das Lieferdatum ändern, die Lieferung und die Menge aufteilen oder einen anderen Artikel vorschlagen. |
| Ermöglichen Sie Kreditoren die Verwaltung von Kontaktpersoneninformationen. | Kreditoren können Kontaktpersoneninformationen für das Unternehmen verwalten. Diese Informationen umfassen Namen, E-Mail-Adressen und Telefonnummern. Zugriff auf diese Funktion wird durch eine dedizierte Sicherheitsrolle gewährt. |
| Geben Sie Dokumente frei, die sich auf Bestellungen mit Kreditoren beziehen. | Wenn Sie ein Dokument für einen Kreditor freigeben müssen, wie z. B. ein Dokument über Anforderungen, ist es von Vorteil, das Dokument mit der relevanten Bestellung zu verknüpfen. Der Kreditor kann anschließend Hinweise und Anlagen mit dem Debitor gemeinsam nutzen, indem er das Dokument mit der Antwort auf die Bestellung verknüpft. Dokumentverwaltung ist das grundlegende Framework, und es können nur Hinweise und Anhänge, die als "extern" klassifiziert werden, für Kreditoren freigegeben werden. |
| Neue Kreditorenbenutzer bereitstellen. | Wenn Ihre Kreditoren die Kreditorenzusammenarbeitsschnittstelle verwenden, können diese auf nahtlose Weise neue Benutzerkonten anfordern, wenn neue Kontakte Zugriff auf die Kreditorenzusammenarbeit erfordern. Beschaffungsspezialisten können eine Anforderung für ein Benutzerkonto für eine Kontaktperson in der Organisation des Kreditors senden. Eine Kontaktperson des Kreditors, die bereits ein Benutzer der Kreditorenzusammenarbeit ist, kann diesen Typ der Anforderung auch senden. Diese Anforderung erstellt schließlich einen neuen Benutzer in Dynamics 365 for Operations, der über kreditorenspezifische Sicherheitsrollen verfügt. Sie vereinfacht auch eine Anforderung zum Portal Microsoft Azure B2B der Rücklage der Benutzer unter einem neuen Benutzerkontos Azure Active Directory (Azure AD). Kreditoren können auch anfordern, dass bestimmte Kreditorenbenutzerkonten deaktiviert werden oder dass Sicherheitsrollen geändert werden. |
| Erfahren Sie mehr über die Kreditorenzusammenarbeit in Dynamics 365 for Operations. | Weitere Informationen zu Kreditorenzusammenarbeit finden Sie unter [Kreditorenzusammenarbeit mit externen Kreditoren](../../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md), [Kreditorenzusammenarbeit mit Debitoren](../../../supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations.md), [Benutzer für Kreditor-Kooperationen verwalten](../../../supply-chain/procurement/manage-vendor-collaboration-users.md), [Einrichten und Verwalten von Kreditorenzusammenarbeit](../../../supply-chain/procurement/set-up-maintain-vendor-collaboration.md) und [Arbeitsbereich für Kreditor-Kooperationsrechnungen](../../../finance/accounts-payable/vendor-portal-invoicing-workspace.md). |

### <a name="intercompany-order-processing"></a>Verarbeiten von Intercompany-Aufträgen

<table>
<thead>
<tr>
<th>Wie Sie vorgehen können</th>
<th>Warum dies wichtig ist</th>
</tr>
</thead>
<tbody>
<tr>
<td>Definieren Sie direkt auf Auftragspositionen, wo der Bedarfsursprung liegt und wie er genutzt wird.
<p><strong>Beispiel</strong></p>
<p>Erstellen Sie eine Auftragsposition und geben Sie Direktlieferung als Lieferart an. Der primäre Kreditor wird der Auftragsposition als Beschaffungspunkt hinzugefügt.</p>
</td>
<td>Der Ablauf für die Auftragsannahme wurde deutlich verbessert. Sie können jetzt direkt auf Auftragspositionen definieren, wo der Bedarfsursprung liegt und wie er genutzt wird. Sie müssen nicht mehr warten, bis alle Positionen zum Auftrag hinzugefügt wurden. Durch neue Optionen auf Auftragspositionen können Sie den Liefertyp angeben, wenn Sie einen Kreditor angeben. Wenn Sie einen Kreditor zu Auftragspositionen zuordnen, werden Auftragsketten für die Lieferung vom Kreditor erstellt.
<ul>
<li>Der Kreditor kann ein Intercompany-Lieferant sein, der eine interne Bestellung und einen internen Auftrag verwendet, oder er kann ein externer Kreditor sein, der eine externe Bestellung verwendet.</li>
<li>Der Liefertyp kann <strong>Direktlieferung</strong> oder <strong>Bestand</strong> sein. Die Lieferart <strong>Bestand</strong> gibt an, dass der Kreditor an den lokalen Bestand beliefern soll, bevor er an den Debitor versendet.</li>
</ul>
</td>
</tr>
<tr>
<td>Erstellen Sie eine Lieferterminzusagen direkt aus den Auftragspositionen.
<p><strong>Beispiel</strong></p>
<p>Erstellen Sie eine Auftragsposition, die von einem Intercompany-Kreditor stammt. Verlassen Sie die Position. Die Lieferdaten werden entsprechend der Verfügbarkeit im Beschaffungsunternehmen berechnet.</p>
</td>
<td>Wenn Sie Auftragspositionen erstellen, die die neuen Beschaffungsinformationen verwenden, werden die Lieferdaten dem Steuerelement <strong>Lieferdatum</strong> entsprechend berechnet. Wenn beispielsweise ein Intercompany-Lieferant ausgewählt wurde, wird die Verfügbarkeit im Beschaffungsunternehmen berechnet. Auf diese Weise werden automatisch Auftragsketten zusammen mit Auftragspositionen erstellt. Durch diese Funktion wird sichergestellt, dass im Beschaffungsunternehmen Lieferdaten angezeigt werden, damit die Profile "VfZ - Verfügbar für Zusage" den voraussichtlichen Bedarf direkt verarbeiten können, während Aufträge erstellt werden.</td>
</tr>
<tr>
<td>Prüfen Sie die Produktverfügbarkeit in allen Beschaffungslagerplätzen, und wählen Sie die beste Beschaffungsoption aus.</td>
<td>Die Seite <strong>Lieferungsalternativen</strong> wurde neu gestaltet und bietet nun wertvolle Informationen über alle genehmigten internen und externen Kreditoren. Dazu gehören Beschaffungsoptionen für die Kreditorenbeschaffung. Wenn Sie eine Lieferart auswählen, berechnet das System durchführbare Lieferdaten. Sie können die beste Option für den Debitoren auswählen und diese Option auf jede Auftragsposition anwenden.</td>
</tr>
</tbody>
</table>

### <a name="warehouse-enhancements-for-high-volume-distribution-centers"></a>Lagerorterweiterungen für Großserienabsatzzentren

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| Erstellen Sie Arbeit, nachdem Waren in einer Verpackungsanlage verpackt wurden. | Diese Funktion ist hilfreich, wenn es weitere Prozesse nach der manuellen Verpackungsarbeit gibt (wie z. B. Palettierung, Qualitätsprüfung, Konsolidierung von Lieferungen oder Änderungen an den Verladedocks). Mit dem neuen Arbeitstyp **Entnahme aus gepacktem Container** können Sie diese Aufgaben modellieren, indem Sie separate Arbeitspositionen verwenden. Sie können nun Verpackungsanlagen modellieren, um Arbeit nach dem Verpacken zu generieren. Dieser Vorgang kann verwendet werden, um die Aktivität des verpackten Bestands zu organisieren. |
| Gruppencontainer in der Verpackungsstation. | Diese Funktion ermöglicht die Gruppierung mehrerer Pakete in einen Container oder Ladungsträger in der Verpackungsanlage. So kann beispielsweise ein E-Commerce-/Großhandelsbetreiber 100 einzeln verpackte Pakete in einen einzelnen Container gruppieren (beispielsweise eine Palette oder einen Käfig). Dieser Container kann dann in einer einzelnen Arbeitsanweisung verschoben, bereitgestellt oder verladen werden, die von einer einzelnen Arbeitskraft generiert wird, indem sie den einzelnen Strichcode (Ladungsträger) für den gruppierten Container scannt. Diese Funktion minimiert die Arbeitsbuchungen zum Verschieben vieler kleinerer verpackter Container. Weitere Informationen finden Sie unter [Erstellen einer Menüoption des mobilen Geräts für die Ladungsträger-Konsolidierung (Aufgabenleitfaden)](../../../supply-chain/warehousing/tasks/create-mobile-device-license-plate-consolidation.md). |
| Erstellen Sie eine Freigaberichtlinie für verpackte Container. | Arbeit, die nach Containerfreigabe ausgelöst wird, kann sowohl automatisch als auch manuell erstellt werden. Bei automatischer Erstellung wird die Arbeit beim Schließen des Containers generiert, indem das Lagerplatzrichtlinien- und Arbeitsvorlagen-Framework dazu verwendet wird. Bei manueller Freigabe kann der Verpacker entscheiden, ob die Arbeiten für einen einzelnen Container oder für eine Containergruppe generiert werden soll. Diese Funktion verringert das Risiko, dass die geschlossenen Container entnommen und verschoben werden, bevor sie bereit sind, von der Verpackungsanlage verschoben zu werden. Dadurch ist auch eine nicht-systemgesteuerte gruppierte Freigabe möglich. |
| Neuzuordnung für Entnahme mit unzureichender Menge | Es wurde Unterstützung für Entnahmeverfahren mit unzureichender Menge hinzugefügt, um einem Mitarbeiter die Möglichkeit zu geben, an einem anderen Standort verfügbare Artikel zu verwenden, wenn die Waren nicht entnommen werden können und er den Auftrag erfüllen möchte. Sie können einen automatischen Neuzuordnungsprozess verwenden, der dieselben Lagerplatzrichtlinien verwendet, um Waren zu erhalten, wenn sie an einem anderen Standort verfügbar sind. Wenn stattdessen manuelle Neuzuordnung verwendet wird, zeigt das mobile Geräts eine Liste der Standorte in Verbindung mit der verfügbaren Menge an. Der Lagerarbeiter kann wählen, aus welchem Lagerplatz Lagerbestand entnommen werden soll. Diese beiden Methoden können einzeln festgelegt werden oder in einem einzelnen Befehl im Lagerarbeitermenü kombiniert werden. Wenn die manuelle Neuzuordnung verwendet wird, kann der Lagerarbeiter die unzureichende Artikelmenge von verschiedenen Orten entnehmen. Weitere Informationen finden Sie unter [Einrichtung der Artikelneuzuordnung für Entnahme mit unzureichender Menge (Aufgabenleitfaden)](../../../supply-chain/warehousing/tasks/set-up-short-picking-item-reallocation.md). |
| Bewegen von Bestand mit zugeordneter Arbeit. | Sie können jetzt Bestand mit zugeordneter Arbeit bewegen. Diese Funktion ist hilfreich, wenn z. B. eine Arbeitskraft einen Eingangsrampenplatz freimachen und erfasste Paletten bewegen möchte, die sich noch im Wartezustand befinden, um an einen anderen eingehenden Lagerplatz verlegt zu werden. Die Rampe wird freigemacht und kann eine zusätzlich mit Waren beladen werden, und der Lagerbestand, der verschoben wurde, wird mit neuen Einlagerungsinformationen aktualisiert. Diese Funktion kann auch verwendet werden, um Platz an den Entnahmeorten freizumachen, indem Sie den Lagerbestand verschieben, dem Arbeit zugeordnet ist, um Platz für die Neubefüllung zu machen. Sie können damit auch Ladung von einem Staginglagerplatz zu einem anderen bewegen, ohne die Ladearbeit zu verlieren, die dadurch generiert wurde. Auf diese Weise kann die Funktion dazu beitragen, die Arbeitszeit zu optimieren, die benötigt wird, um LKWs zu beladen, wenn diese eintreffen. Sie können den Lagerbestand verschieben, der für Aufträge, Umlagerungsauftragsabgänge, Umlagerungsauftragszugänge und Bestellungen reserviert wurde. Die Bewegung wird verhindert, wenn dadurch durch die Positionen aufgeteilt werden. Wenn Sie beispielsweise eine Arbeitsposition für 100 Einheiten eines Artikels haben, können Sie nur 30 Stück dieses Artikels nicht an einen anderen Speicherort verschieben. |
| Führen Sie Ladungsträger zusammen, denen Arbeit zugeordnet wurde. | Sie können Ladungsträger zusammenführen, denen ausgehende Arbeit zugeordnet wurde. Wenn eine Entnahme beispielsweise in mehrere Arbeiten unterteilt wurde, kann es hilfreich sein, die Zusammenführung der Ladungsträger zuzulassen, nachdem sie zum Staginglagerplatz geliefert werden. Ladungsträger können nur konsolidiert werden, wenn sie sich am gleichen Lagerort befinden, Mitglieder der gleichen Ladung sind und dieselben Lieferinformationen haben. |
| Einfrieren von Entnahmearbeit, die einer Auffüllung auf Positionsebene zugeordnet ist. | Sie können Arbeit jetzt auch auf Positionsebene anstatt auf Kopfebene einfrieren, sodass Arbeitskräfte Entnahmepositionen erfüllen können, die nicht mit Bedarfswiederbeschaffung eingefroren wurden. Daher können Großhändler oder Einzelhändler mit großen Aufträgen oder Wiederbeschaffungsumlagerungsaufträgen den Start der Entnahmearbeit für alle Positionen ermöglichen, die nicht unter Wiederbeschaffungsarbeit fallen. Die Entnahme- und Wiederbeschaffungsarbeit kann anschließend parallel ausgeführt werden. Diese Funktion kann so konfiguriert werden, dass Sie wählen können, ob auf Kopf- oder Positionsebene eingefroren wird. Sie können auch beide Methoden verwenden und eine Arbeitsvorlage für die einzelnen Methoden erstellen. Die Kopf-/Positionskonfiguration wird auf Arbeitsvorlagen festgelegt, Sie können sie jedoch direkt in der generierten Arbeit ändern. |
| Stornieren von Arbeit mit einem mobilen Gerät. | Sie können jetzt Arbeit über ein mobiles Gerät mit oder ohne Bedarfswiederbeschaffung stornieren. Bisher mussten Sie den Rich-Client verwenden. Um diese Funktion zu aktivieren, erstellen Sie eine Menüoption auf dem mobilen Gerät, in der der Modus auf **Indirekt** und der Aktivitätscode auf **Arbeit stornieren** festgelegt ist. |

### <a name="warehouse-operation-enhancements"></a>Lagerortarbeitsgangserweiterungen

| Wie Sie vorgehen können | Warum dies wichtig ist |
|-----------------|-----------------------|
| Modellieren verschiedener Containertypen. | Sie können verschiedene Containertypen im Lagerort verwenden, um die Lagerung aus anderen Gründen zu optimieren. Die neue Containertypentität hat die physischen Merkmale von Containertypen. Sie können jetzt Ladungsträgern einen bestimmten Containertyp zuordnen und Lagerplatzbeschränkungen verwenden. Sie können diese Funktion beispielsweise verwenden, um zu steuern, wie viele Paletten (oder andere Containertypen) Sie an einem bestimmten Ort zulassen. Containertypen wurden außerdem zu Einheitennummernkreisgruppen hinzugefügt, um Standardcontainertypen für den Empfangsvorgang hinzuzufügen. Containertypen können mit ein- und ausgehenden Lagerplatzrichtlinien verwendet werden. Sie können auch in der Ansicht für verfügbaren Bestand verwendet werden, um zu bestimmen, wie viele Containertypen derzeit im Lager vorliegen. Weitere Informationen finden Sie im Blogbeitrag [Verwenden von Ladungsträgern mit Containertyp-Zuordnung zur Steuerung des Lagerortverwaltungsprozesses](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/20/use-of-license-plates-associated-with-a-container-type-to-drive-warehouse-management-processes/). Obwohl in diesem Blogbeitrag eine Aktualisierung auf Microsoft Dynamics AX 2012 beschrieben wird, wurde die gleiche Unterstützung jetzt zu Dynamics 365 for Operations hinzugefügt. |
| Stornieren von Lieferungen. | In einem Lagerort muss es möglich sein, verspätete Änderungen zu verarbeiten. Beispielsweise können mehrere Waren beschädigt werden, sodass Sie sie nicht versenden können. Außerdem kann es vorkommen, dass ein Debitor möglicherweise eine verspätete Anfrage auf Stornierung oder Änderung eines Auftrags übermittelt. Mit Dynamics 365 for Operations können nun eine Lieferung stornieren. Daher können Sie einen ein Lieferschein stornieren, sodass Sie ihn mit den korrekten Mengen später aktualisieren können. Außerdem können Sie Produktzugänge beim Zugang stornieren, damit eine aktualisierte Version erstellt werden kann. |
| Verwenden von Paletten mit gemischten Artikeln. | Sie können nun "gemischte" Paletten empfangen und erfassen. Eine gemischte Palette besteht aus verschiedenen Artikeln, die auf einer Palette für eine oder mehrere Bestellungen oder Positionen zusammengelegt wurden. Alle Erfassungen können in einem Ladungsträger zusammengefasst werden. Dieser Prozess wird durch das mobilen Geräts am Lagerort ermöglicht. Wenn beispielsweise die Palette von Mischartikeln am Lagerort eingeht, identifiziert der empfangende Mitarbeiter die Artikel und Mengen auf der Palette, bevor die Palette zu dedizierten Einlagerungsplätzen verschoben wird. Die Einlagerungsplätze werden durch Arbeitsvorlagen und Lagerplatzrichtlinien gekennzeichnet. Wenn die Einlagerungsplätze auf mehrere Artikel mit festen Lagerplätzen verteilt sind, erstellt diese Funktion so viele Einlagerungsarbeitspositionen, wie verschiedene Artikel auf der Mischpalette vorhanden sind. Diese Funktion ermöglicht eine schnellere und flexiblere Erfassung und Einlagerung der empfangenen Mischartikelpaletten. Weitere Informationen finden Sie im Blogbeitrag [Erhalten und Registrieren eine Palette mit gemischten Quelldokumentzeilen unter Verwendung des Ladungsträger 1-Bestellungsabgleichs](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/13/receive-and-register-a-pallet-with-mixed-source-document-lines-using-1-license-plate-purchase-order-matching/) und im Abschnitt zu Mischpalettenunterstützung in der [Ankündigung des neuen kumulativen Updates](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/30/whats-new-in-cu11-for-wms-and-tms/). Obwohl in diesem Blogbeitrag eine Aktualisierung auf AX 2012 beschrieben wird, wurde die gleiche Unterstützung jetzt zu Dynamics 365 for Operations hinzugefügt. |

### <a name="minor-feature-enhancements-in-supply-chain-management"></a>Kleinere Funktionserweiterungen in der Lieferkettenverwaltung

<table>
<thead>
<tr>
<th>Wie Sie vorgehen können</th>
<th>Warum dies wichtig ist</th>
</tr>
</thead>
<tbody>
<tr>
<td>Verwenden Sie neue Datenentitäten, um Daten zu importieren und exportieren.</td>
<td>Sie können Daten importieren und exportieren, indem Sie diese Datenentitäten verwenden:
<ul>
<li>Frachtrechnung</li>
<li>Aggregat des verfügbaren Bestands nach Lagerort und Bestandsstatus</li>
<li>Bestandsbelastung</li>
<li>Angebot</li>
</ul>
</td>
</tr>
<tr>
<td>Verwenden Sie das erweiterte Gantt-Steuerelement, um interaktive Planungsszenarien zu entwickeln.</td>
<td>Mit dem erweiterten Gantt-Steuerelement lassen sich neue interaktive Planungsszenarien entwickeln und es enthält erweiterte APIs, die verwendet werden können, um die Darstellungsweise von Aktivitäten anzupassen. Im Folgenden finden Sie einige der neuen APIs:
<ul>
<li>Vertikales Drag & Drop der Aktivitäten</li>
<li>Aktivitäten hinzufügen/entfernen</li>
<li>Vorschau der gebuchten Perioden in der Zusammenfassungsleiste</li>
<li>Änderung von Farbe und Stil der Aktivitätsrahmen</li>
<li>Ändern von Farbe, Stil und Hintergrund des Texts im Raster</li>
</ul>
</td>
</tr>
<tr>
<td>Verbesserte Material- und Ressourcenplanung.</td>
<td>Es wurden einige Erweiterungen an der Material- und Ressourcenplanung vorgenommen:
<ul>
<li>Der Sicherheitszuschlag für Warenabgang wird jetzt verarbeitet, wenn ein Artikel verfügbar ist.</li>
<li>Überschreiben Sie das Lieferdatum bei fest geplanten Aufträge.</li>
<li>Priorisieren Sie Auftragserfüllung vor Sicherheitslagerbestand.</li>
<li>Verhindern Sie die Planung von Bestellvorschlägen in der Vergangenheit.</li>
</ul>
</td>
</tr>
<tr>
<td>Melden des tatsächlichen Verbrauchs für Produktion und Anzeigen des Bestandsstatus.</td>
<td>Sie können den tatsächlichen Verbrauch für die Produktion anzeigen. Darüber hinaus ermöglicht ein neues Kontrollkästchen <strong>Bestandsstatus anzeigen</strong>, das zur Option <strong>Bewegung</strong> im Menüelement <strong>Arbeitserstellung</strong> hinzugefügt wurde, die Anzeige des Bestandsstatus.</td>
</tr>
<tr>
<td>Berechnen Sie Raumgewicht, wenn die Gebühren für den Spediteur auf dem Raumgewicht basieren.</td>
<td>Ein neues TMS-Tarifmodul, das auf dem Raumgewicht basiert, wurde hinzugefügt, damit Sie das Raumgewicht berechnen können.</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Neuheiten und Änderungen](whats-new-changed.md)
