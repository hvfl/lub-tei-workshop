### TEI

> «Die Text Encoding Initiative (TEI) ist eine 1987 gegründete Organisation (seit 2000 als TEI‐ Konsortium organisiert) und ein gleichnamiges Dokumentenformat zur Kodierung und zum Austausch von Texten, das diese entwickelt hat und weiterentwickelt. In der aktuellen Version P5 basiert das Format auf XML ...» (Wikipedia)

%-- 
### TEI Guidelines

- [http://www.tei-c.org](http://www.tei-c.org)  

%--
### TEI Das minimale Skelett

```xml
<TEI>
   <teiHeader>
      <fileDesc>
         <titleStmt><title>Title</title></titleStmt>
         <publicationStmt><p>Publication Information</p></publicationStmt>
         <sourceDesc><p>Information about the source</p></sourceDesc>
      </fileDesc>
   </teiHeader>
   <text>
      <body>
         <p>Some text here.</p>
      </body>
   </text>
</TEI>
```
%--

Rootelement mit Namespaceangabe: 

```<TEI xmlns="http://www.tei-c.org/ns/1.0">```

Dann `<teiHeader>` und `<text>`.


%--
### TEI weitere Infos

- [https://teibyexample.org/](https://teibyexample.org/)
- [https://www.ssrq-sds-fds.ch/wiki/Transkriptionsrichtlinien](https://www.ssrq-sds-fds.ch/wiki/Transkriptionsrichtlinien)

https://www.ssrq-sds-fds.ch/wiki/Spezial:Benutzerkonto_beantragen

%-- 
### Beispiele

- SG Missive
https://gitlab.com/andreas_kraenzle/missive-data

- SSRQ 
https://github.com/eeditiones/tei-examples/issues

%--
### Register: Personen, Organisationen, Familien
#### Elemente
- `<rs>`
- `<name>`
- `<persName>`
- `<orgName>`

#### Attribute
- `@ref` 
- `@role`

[Guidelines](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ND.html#NDNA)

%--
### Register: Orte

#### Elemente
- `<placeName>`
- `<geogName>`
- `<origPlace>`

#### Attribute
- `@ref`
- `@role`
[Guidelines](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ND.html#NDPLAC)
%-- 
### Register:Schlagworte und Begriffe

#### Elemente
- `<term>` 

#### Attribute
- `@ref` 

### Datierungen
#### Elemente
- `<date>`
- `<origDate>`

#### Attribute
- `@when` 
- ...

### Abkürzungen

```xml
<choice>
   <abbr>c.</abbr>
   <expan>cum</expan>
</choice>
```

### Masse, Gewichte, Währungen

komplex: 
- https://www.ssrq-sds-fds.ch/wiki/Masse_und_Gewichte
- https://www.ssrq-sds-fds.ch/wiki/W%C3%A4hrungen

%--
### Sachanmerkungen
#### Elemente
- `<note>`

%--
### ODD (One Document does it all)

- Möglichkeit Verwendung von TEI zu dokumentieren, einzuschränken und anzupassen
- ODD ist selbst wieder TEI, es lassen sich auch Schemata für die Arbeit mit der TEI erzeugen
