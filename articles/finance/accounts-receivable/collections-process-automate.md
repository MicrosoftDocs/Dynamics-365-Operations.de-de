---
title: Automatisierung des Inkasso-Prozesses
description: In diesem Thema wird das Einrichten von Inkassoprozessstrategien beschrieben, mit denen Debitorenrechnungen automatisch identifiziert werden, für die eine E-Mail-Erinnerung, eine Inkassoaktivität (z. B. ein Telefonanruf) oder ein Mahnschreiben an den Debitoren gesendet werden müssen.
author: panolte
manager: AnnBe
ms.date: 08/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: a63058904df72a7fda5a67ed1e6a846eed393ce0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969700"
---
# <a name="collections-process-automation"></a>Automatisierung des Inkasso-Prozesses

[!include [banner](../includes/banner.md)]

In diesem Thema wird das Einrichten von Inkassoprozessstrategien beschrieben, mit denen Debitorenrechnungen automatisch identifiziert werden, für die eine E-Mail-Erinnerung, eine Inkassoaktivität (z. B. ein Telefonanruf) oder ein Mahnschreiben an den Debitoren gesendet werden müssen. 

Unternehmen verbringen viel Zeit damit, alte Kontostandberichte, Debitorenkonten und offene Rechnungen zu recherchieren, um festzustellen, welche Debitoren wegen einer offenen Rechnung oder eines offenen Kontostands kontaktiert werden müssen. Diese Recherche nimmt Zeit in Anspruch, die ein Inkassobüro für die Kommunikation mit Debitoren benötigt, um überfällige Salden einzuziehen oder Rechnungsstreitigkeiten beizulegen. Mit der Automatisierung von Inkassoprozessen können Sie einen strategiebasierten Ansatz für Ihren Inkassoprozess festlegen. Auf diese Weise können Sie Inkassoaktivitäten konsistent anwenden, indem Sie benutzerdefinierte E-Mail-Erinnerungen oder einen programmierten Prozess zum Senden von Mahnschreiben bereitstellen. 

## <a name="collections-process-setup"></a>Inkassoprozesseinrichtung
Sie können die **Inkassoprozesseinrichtung**-Seite (**Kredit und Inkasso > Einrichtung > Inkassoprozesseinrichtung**) verwenden, um einen automatisierten Inkassoprozess zu erstellen, der Aktivitäten plant, E-Mail-Nachrichten sendet und Debitorenmahnschreiben erstellt und veröffentlicht. Die Prozessschritte basieren auf der führenden oder ältesten offenen Rechnung. Jeder Schritt verwendet diese Rechnung, um zu bestimmen, welche Kommunikation oder Aktivität mit einem bestimmten Debitor stattfinden soll.  

### <a name="process-hierarchy"></a>Prozesshierarchie
Jeder Debitorenpool kann nur einer Prozesshierarchie zugeordnet werden. Der Hierarchierang dieses Schritts gibt an, welcher Prozess Vorrang hat, wenn ein Debitor in mehr als einem Pool enthalten ist, dem eine Prozesshierarchie zugewiesen ist. Die Pool-ID bestimmt, welche Debitoren dem Prozess zugewiesen werden. 

Die Ruhetage werden verwendet, um sicherzustellen, dass ein Debitor durch den automatisierten Prozess nicht zu häufig kontaktiert wird.  Wenn beispielsweise die Ruhetage auf zwei festgelegt sind, wird ein Debitor mindestens zwei Tage lang nicht durch den automatisierten Prozess kontaktiert, selbst wenn die ursprüngliche Hauptrechnung vollständig beglichen wurde. 

Um Debitoren von der Prozessautomatisierung auszuschließen, wenn der Kontostand oder der Rechnungssaldo unter einem definierten Wert liegt, legen das Feld **Vom Prozess ausschließen** auf **Ja** fest und geben Sie den Betragswert ein.

## <a name="process-details"></a>Prozessdetails
**Beschreibung** wird verwendet, um den Zweck oder Namen des Schritts in der Hierarchie zu identifizieren.

**Aktionstyp** definiert, ob der Schritt eine Aktivität erstellt, eine E-Mail sendet oder ein Mahnschreiben erstellt.

**Geschäftsdokument** definiert die Vorlage, die zum Erstellen des Aktionstyps verwendet wird.  Dies kann eine Aktivitätsvorlage, eine E-Mail-Vorlage oder ein Mahnschreiben pro Debitor sein. 

Die Aktionstypen können entweder vor oder nach dem Fälligkeitsdatum der Rechnung erstellt werden, basierend auf der Einstellung, die in der Spalte **Tage in Bezug auf das Fälligkeitsdatum der Rechnung** angezeigt wird.

Wenn Sie einen E-Mail-Aktionstyp auswählen, wird anhand des Empfängers definiert, ob es sich um einen Debitor-, Verkaufsgruppen- oder Inkassovermittler handelt. Der Wert im Feld **Kontakt zu Geschäftszwecken** bestimmt dann, welcher Kontakt von diesem Debitorenkonto die Mitteilung erhält.

## <a name="business-document-details"></a>Einzelheiten des Geschäftsdokuments
Die Einzelheiten des Geschäftsdokuments variieren je nach Aktionstyp, der in den Prozessdetails ausgewählt wurde.  Wenn der Aktionstyp eine Aktivität ist, werden die Details der Aktivitätsvorlage angezeigt.  Zu diesen Details gehören der Name der Aktivitätsvorlage, die Art der zu erstellenden Aktivität, der Zweck der Aktivität, die Anzahl der Tage, die für den Abschluss der Aktivität geplant sind, und die Details der Aktivität.  Diese Aktivität wird dann mit der führenden Rechnung verknüpft, die den Empfänger die Aktion mitteilt, die zum Abschließen der Aktivität erforderlich ist.

Wenn der Aktionstyp eine E-Mail in den Prozessdetails ist, enthält dieser Abschnitt zwei Inforegister.  Die erste wird verwendet, um die Vorlagen-ID, die E-Mail-Beschreibung, die Standardsprache, den Benutzernamen, der automatisch gesendeten E-Mail-Nachrichten zugewiesen wird, und die E-Mail-Adresse des zugeordneten Absenders zu definieren. Mit der zweiten Option kann der Text der E-Mail nach den Werten in den Feldern **Sprache** und **Betreff** der E-Mail durch Auswahl von **Bearbeiten** gespeichert werden.  Dies öffnet ein Fenster, in dem HTML-Inhalte hochgeladen werden können. Sie können die manuell erstellte Nachricht auch in das Feld unten links im Fenster eingeben.  

> [!Note]
> Eine Outlook-E-Mail kann mit dem gewünschten Textkörper der Kommunikation im HTML-Format gespeichert werden. Dies kann dann hochgeladen werden, um die Vorlage zu implementieren. <br> <br> Wenn der Aktionstyp des Mahnschreibens ausgewählt ist, wird im Einrichtungsformular kein Abschnitt mit Geschäftsdokumentdetails angezeigt.


## <a name="fasttab-reference"></a>Inforegister-Referenz
In den folgenden Tabellen sind die Seiten und Felder aufgeführt, über die auf die angegebenen Inforegister zugegriffen werden kann, sowie eine Beschreibung der Informationen auf dieser Registerkarte. 

### <a name="process-hierarchy"></a>Prozesshierarchie

|     Seite                                                  |     Feld                         |     Beschreibung                           |
| --------------------------------------------------------  |-------------------------------    |---------------------------------------    |
|     Inkassoprozesseinrichtung <br> Prozessautomatisierung       |                                   |     Erstellen und Verwalten von Inkassoprozessen basierend auf Debitorpoolzuweisungen.                                                                                                                             |
|     Inkassoprozesseinrichtung <br> Prozessautomatisierung       |     Hierarchie                     |     Definiert die Priorität der Prozessautomatisierung, um einen Debitor zuzuweisen, wenn er zu mehreren Pools gehört.                                                                                                   |
|     Inkassoprozesseinrichtung <br> Prozessautomatisierung       |     Poolkennung                       |     Abfragen, die eine Gruppe von Debitorendatensätzen definieren.                                                                                                                                                        |
|     Inkassoprozesseinrichtung <br> Prozessautomatisierung       |     Ruhige Tage                    |     Begrenzen Sie, wie oft ein Prozessschritt ausgeführt werden kann. Wenn beispielsweise zwei Ruhetage festgelegt sind, wird der nächste Prozessschritt mindestens zwei Tage lang nicht ausgeführt, wenn sich die führende Rechnung ändert.     |
|     Inkassoprozesseinrichtung <br> Prozessautomatisierung       |     Aus dem Prozess ausschließen        |     Die Auswahl von entweder **Guthaben der Debitorenfälligkeit kleiner als** oder **Rechnungsbetrag kleiner als** wird schließt einen Debitor von der Prozessautomatisierung aus, wenn die Wertkriterien nicht erfüllt sind.                                   |

### <a name="process-details"></a>Prozessdetails
|     Seite                                                  |     Feld                                         |      Beschreibung                  |
|--------------------------------------------------------   |-----------------------------------------------    |----------------------------   |
|     Inkassoprozesseinrichtung <br> Prozessautomatisierung       |                                                   |     Definieren Sie die Schritte basierend auf der führenden Rechnung.                                                                                                |
|                                                           |     Beschreibung                                   |     Freitextfeld zur Angabe eines Namens und/oder einer Beschreibung des Schritts.                                                                           |
|                                                           |     Vorgangstyp                                   |     Aktivität, E-Mail oder Mahnschreiben, das vom Prozessschritt erstellt wird.                                                                     |
|                                                           |     Geschäftsdokument                           |     Definiert die Aktivität oder E-Mail-Vorlage, die während des Prozessschritts verwendet wird.                                                                        |
|                                                           |     Wenn                                          |     Legt fest, ob der Prozessschritt vor oder nach dem Fälligkeitsdatum der führenden Rechnung zusammen mit dem **Tage in Bezug auf das Fälligkeitsdatum der Rechnung**-Feld auftritt.        |
|                                                           |     Tage in Bezug auf das Fälligkeitsdatum der Rechnung        |     Zusammen mit dem **Wann**-Feld gibt dies den Zeitpunkt des Prozessschritts an.                                                                          |
|                                                           |     Auftragsbearbeiter                                     |     Gibt an, ob eine E-Mail an einen Debitor, eine Verkaufsgruppe oder einen Inkassoagent-Kontakt gesendet wird.                                                   |
|                                                           |     Kontakt für Geschäftszweck                    |     Bestimmt, welche Empfänger-E-Mail-Adresse für die E-Mail-Kommunikation verwendet wird.                                                                                 |

### <a name="business-process-activity-template-details"></a>Details zur Vorlage für Geschäftsprozessaktivitäten 
|     Seite                                                  |     Feld                     |      Beschreibung                  |
|--------------------------------------------------------   |----------------------------   |-------------------------  |
|     Inkassoprozesseinrichtung <br> Prozessautomatisierung       |                               |     Abschnitt des Einrichtungsprozesses, in dem die Details der Aktivitätsvorlage angegeben sind.                                                                      |
|     Inkassoprozesseinrichtung <br> Prozessautomatisierung       |     Aktivitätsvorlage       |     Identifiziert den Typ, den Zweck und die Anzahl der Tage für das Abschließen und enthält Details zu der Aktivität, die während eines Aktivitätsprozessschritts erstellt wird.       |

### <a name="business-document-email-template-details"></a>Details der Geschäftsdokument-E-Mailvorlagen 
|     Seite                                                  |     Feld     |      Beschreibung                  |
|--------------------------------------------------------   |-------------- |-----------------------------  |
|     Inkassoprozesseinrichtung <br> Prozessautomatisierung       |               |     Identifiziert die E-Mail-Beschreibung, die Standardsprache, den Absendernamen und die E-Mail-Adresse, die während eines E-Mail-Prozessschritts erstellt werden.        |


### <a name="collections-history"></a>Inkassohistorie 
|     Seite                              |     Feld     |      Beschreibung                                                          |
|------------------------------------   |-------------- |---------------------------------------------------------------------  |
|     Inkassoprozesseinrichtung       |               |     Zeigen Sie den aktuellen Verlauf für die ausgewählte Prozesshierarchie an.     |

### <a name="collection-process-assignment"></a>Inkassoprozesszuweisung
|     Seite                              |     Feld     |      Beschreibung                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|     Inkassoprozesseinrichtung       |               |     Zeigen Sie die einem Inkassoprozess zugeordneten Debitoren an.  
|     Manuelle Zuweisung               |               |     Zeigen Sie Debitoren an, die einem Prozess manuell zugewiesen wurden, oder wählen Sie Debitoren aus, die einem Prozess zugewiesen werden sollen. |
|     Vorschau der Prozesszuweisung      |               |     Zeigen Sie eine Vorschau der Debitoren an, die einer Strategie zugewiesen werden, wenn sie ausgeführt wird.   |
|     Vorschau der Debitorenzuweisung     |               |     Zeigen Sie die Strategie an, die einem bestimmten Debitoren zugewiesen ist.    |
 
### <a name="parameters"></a>Parameter
|     Seite                                                                  |     Feld                                             |      Beschreibung                              |
|-------------------------------------------------------------------------- |------------------------------------------------------ |-------------------------------------  |
|     Debitorenkontenparameter> Automatisierung von Inkassoprozessen     |     Anteil der Debitoren pro Stapelverarbeitungsaufgabe          |     Einstellung zum Bestimmen der Anzahl der Stapelaufgaben pro Automatisierungsprozess.                                          |
|     Debitorenkontenparameter> Automatisierung von Inkassoprozessen     |     Mahnschreiben automatisch buchen           |     Aktionstypen für Mahnschreiben werden den Brief während der Automatisierung buchen.                                      |
|     Debitorenkontenparameter> Automatisierung von Inkassoprozessen     |     Erstellen von Aktivitäten für Automatisierung                |     Erstellen und schließen Sie Aktivitäten für Aktionstypen ohne Aktivität, um alle automatisierten Schritte anzuzeigen, die für ein Konto ausgeführt wurden.        |
|     Debitorenkontenparameter> Automatisierung von Inkassoprozessen     |     Inkassoprozessautomatisierung für aufzubewahrende Tage     |     Definiert die Anzahl der Tage, an denen der Inkassoverlauf gespeichert wird.                                                       |
