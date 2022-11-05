# BlockchainVotingSystem

One of the requirements with regard to the integrity of an online election is that the election result must be checked in the end. However, the necessary confidentiality in the event of a choice makes it difficult to develop a procedure that is easy to handle on the one hand for voters and voting observers and on the other hand ensures that individual voices and the election result can be checked as a whole. This requirement is called End-To-End Verifiability (E2E-V).

The verification objectives can be summarized with the catchphrase, “Cast as intended;
recorded as cast; and counted as recorded.” 

Das bedeutet, dass überprüfbar sein muss:
1. Wurde der beabsichtigte Kandidat gewählt. Wenn beispielsweise die Kandidaten
auf den Listen vertauscht würden, könnte ein Wähler unbeabsichtigt die falsche
Wahl treffen.
2. Wurde die Stimme so übermittelt und gespeichert, wie gewählt. Durch
Manipulationen bei der Übermittlung oder Speicherung können bei einem Online-
Wahlsystem Stimmen verloren gehen, oder doppelt gespeichert werden.
3. wurde die Stimme auch so gewertet wie gespeichert.

## Authentifizierung und Anonymität
Für eine demokratische Wahl muss auch gewährleistet werden, dass nur berechtigte
Wählerinnen ihre Stimme abgeben können und dass jeder die gleiche Anzahl von
Stimmen hat. Gleichzeitig muss die Anonymität der abgegebenen Stimmen gewahrt
bleiben. Bei einem Peer-To-Peer-Netzwerk auf Basis des Bitcoin-Protokolls ist eine
Authentifizierung nicht vorgesehen, jeder kann Teilnehmer in dem Netzwerk werden
und alle Transaktionen beobachten. 

## Geheimhaltung und Mechanismus gegen Erpressungen
Ein Online-Wahlsystem muss eine geheime Wahl garantieren. Da eine Online-Wahl
unter „unkontrollierten“ Bedingungen stattfindet (nicht im Wahllokal sondern zuhause
auf unsicheren Endgeräten), muss außerdem sichergestellt werden, dass kein
massenhafter Stimmenkauf, Erpressung etc. technisch ermöglicht wird, ohne dass dies
entdeckt wird. Das bedeutet, dass das System beispielsweise nicht offenbaren darf, wie
ein bestimmter Wähler gewählt hat.

Das Problem der potentiellen Erpressbarkeit erweitert die Anforderung der bloßen
Geheimhaltung: Die Gefahr, dass Stimmen gekauft oder erpresst werden, lässt sich nur
verhindern, wenn eine Wählerin nicht die Möglichkeit hat, zu beweisen, wie sie gewählt
hat. Wäre sie dazu in der Lage, könnte ein Erpresser diesen Beleg fordern und sie wäre
erpressbar. Eine Anforderung, die deswegen an elektronische Wahlsysteme gestellt
wird, wird in der Literatur als „Coercion resistance“ - zu Deutsch etwa
„Widerstandsfähigkeit gegen Erpressung“ bezeichnet. Ein möglicher Erpresser darf
außerdem auch ohne Kooperation der Wählerin keine Möglichkeit haben, eine
Verbindung zwischen der Wählerin und ihrer Wahlentscheidung herstellen können
dürfen. Um die Anforderungen betreffs der Geheimhaltung und Widerstandsfähigkeit zu
erfüllen, ist es notwendig, die Wahlentscheidungen bei der Übertragung in die
Blockchain so zu verschlüsseln, dass ein Erpresser keine Möglichkeit hat, vom Opfer
oder dem Computer des Opfers einen Schlüssel zur Entschlüsselung der Daten zu
bekommen, um Kenntnis über die tatsächliche Wahlentscheidung der Wählerin zu
erlangen – sei es mit oder ohne Kooperation der Wählerin.

## Blockchain-basierte Netzwerke zur Durchführung von Online-Wahlen

Bei konventionellen Kryptowährungen, wie zum Beispiel dem Bitcoin-Netzwerk, ist die Geheimhaltung der
Informationen und der Metadaten nicht vorgesehen. Jede Transaktion läßt sich bis zu den Addressen der Absenderinnen und Empfänger verfolgen.
Techniken wie zum Beispiel Ring-Signaturen ermöglichen den Schutz der Privatssphäre, da sie die Adressen der Teilnehmerinnen einer Transaktion geheim halten.

## Entwicklung von Prototypen

Für das BVS werden verschiedene Applikationen benötigt, die jeweils die Funktionalitäten für die jeweiligen Rollen bei einer Wahl abdecken. Als erster Prototyp wird eine Webserver-basierte Anwendung "BVS-Wahl" entwickelt, mit der die Funktionalitäten für die Rolle Wähler/-in getestet werden kann. Als Basis dient dabei eine Node,js (Javascript) Laufzeit-Umgebung und das Testnet von Avalanche, einem Blockchain-Projekt, das wie Ethereum dApps (Verteilte Anwendungen) und SmartContracts unterstützt.

## Installation der Wahl-Applikation für Wählerinnen

### Prerequitsites
- NodeJS >= 10.16 and npm >= 5.6 installed.
- Truffle, which can be installed globally with npm install -g truffle
- Metamask extension added to the browser.
