---
title: "226309 PV Grundlagen sozialer Netzwerkanalyse"
subtitle: "Codebuch"
author: "Anika Geiger, ag172"
output: md_document
variant: markdown_github
---

# Datensatz Testat #
Codebuch Stand 2022-02,
erstellt von Anika Geiger (ag172@hdm-stuttgart.de)
## Inhalt
- Edges.csv (Edgelist)
- Nodes.csv (Nodelist)
- Codebuch.md (Codierung der Datensätze)

## Ursprung und Datenerhebung
Ich habe den Datensatz der Politiker*innen im Kurs Netzwerkanalyse erhoben.
Das Netzwerk ist ein *gerichtetes two-mode Akteursnetzwerk*. 

**Umgang mit fehlgenden Werten**
  Fehlende Werte werden nicht erfasst.
  

# EDGE-Attribute

**id**  
  eindeutige Identifikation jedes einzelnen Knotens (vertex), der erfasst wird

**from**
  definiert den Sender in gerichteten Netzwerken. Entspricht ID in der Nodelist. 

**to**
  
  definiert den Empfänger in ungerichteten Netzwerken. Entspricht ID in der Nodelist. 

**relationship**
definiert Verbindungen zwischen Politiker*innen und dem Organisationen

1 = *Ministerium*   
2 = *politische Funktion* in Gremien oder der Partei
3 = *Ehrenamt* Mitgliedschaften in NGOs, Stiftungen, Gedenkstätten
4 = *Unternehmen und Aufsichtsräte* Beteiligung an Unternehmen
5 = *Stipendien*
6 = *Berufstätigkeiten*
7 = *Studienort in In- und Ausland* Studien- und längere Aufenthalte im In- und Ausland


1 = Achtung: Regierung umfasst auch Staatsekretäre und das
Bundeskanzleramt, etc. hier sollte als Knoten das entsprechende
Ministerium angegeben werden.

2 = aktuelle und ehemalige politische Funktionen in politischen
Ausschüssen, Gremien und der Partei. etc. Das können auch frühere
Stationen gewesen sein, z.B. Geschäftsführer:in einer Partei, etc.

3 = umfasst alle Mitgliedschaften in NGOs, Stiftungen, Gedenkstätten,
etc: werden im Bundestagsprofil als Körperschaften öffentlichen Rechts
bezeichnet.

4 = Beteiligung an Unternehmen durch Mandate, etwa Aufsichtsratsmandate,
Gremien, etc.

5 = erhalten Stipendien (egal wann), etwa Deutsche Studienstiftung,
Parteinahe Stiftungen, Internationale Organisationen im In- und Ausland
etc.

6 = ausgeübte Berufstätigkeiten, falls vorhanden

7 = Studien- bzw. (längere) Aufenthaltsort(e) in In- und Ausland

**year**  
Jahr, in dem die Variable relationship erhoben wurde


# NODE-Attribute  
  
**id**  
eindeutige Identifikation jedes einzelnen Knotens (vertex), der erfasst wird.  

**name_short**
Nachnahme des/der Politiker/in 

**name**
Vollständiger Name  des/der Politiker/in 

**type**
Art des Knoten 
0 = Person
1 = Organisation/Ort/Verband

**sex**    
Geschlecht  
1 = female 
2 = male  
  
**birth**    
Geburtsjahr

**position**  
jetzige Position
1 = Staatssekretär/in
2 = Minister/in 

**education**  
höchster Bildungsabschluss
1 = Diplom
2 = Promotion
3 = Staatsexamen
4 = Magister 

**subject**   
Fachrichtung bei Studium/Promotion
1= Politik
2 = Rechtswissenschaften
3 = Wirtschaft
4 = Soziales 

**party**   
Parteizugehörigkeit
gruene = Bündnis 90/Die Grünen
spd = SDP
fdp = FPD

**religion**    
Religion, 
1 = evangelisch
2 = römisch-katholisch
  
**kids**    
Anzahl der Kinder

**twitter**  
Anzahl der Twitter-Follower
  
**instagram**    
Anzahl der Instagram-Follower

**facebook**  
Anzahl der Facebook-Follower

**youtube** 
Anzahl der Youtube-Abonnenten 

##
