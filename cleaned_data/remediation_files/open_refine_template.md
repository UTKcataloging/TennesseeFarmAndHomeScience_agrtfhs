# Open Refine Template for Tennessee Farm and Home Science


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells["adminDB"].value}}</identifier>
<identifier type="pid"><{{cells['PID'].value}}</identifier>
{{if(isBlank(cells['identifier'].value), '', '<identifier type="extension">' + cells['identifier'].value + '</identifier>')}}
<titleInfo><title>{{cells["title"].value}}</title></titleInfo> 
{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}
<tableOfContents>{{cells['Table_of_Contents'].value}}</tableOfContents>
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><extent>{{cells['extent'].value}}</extent></physicalDescription>
{{if(isBlank(cells['date_year'].value), '', '<originInfo><dateIssued>' + cells['date_year'].value + '</dateIssued><dateIssued encoding="edtf" keyDate="yes">' + cells['date_year'].value + '</dateIssued><publisher>' + cells['publisher'].value + '</publisher><place><placeTerm valueURI="http://id.loc.gov/authorities/names/n79109786">Knoxville (Tenn.)</placeTerm>
</place><issuance>serial</issuance></originInfo>')}}
<note>{{cells['note'].value}}</note>
<subject authority="lcsh" valueURI="http://id.loc.gov/authorities/subjects/sh2009114481"><topic>Agriculture--Tennessee</topic></subject>
<subject authority="lcsh" valueURI="http://id.loc.gov/authorities/subjects/sh85047223"><topic>Farm management</topic></subject>
{{if(isBlank(cells['subject3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject4'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject4_URI'].value + '"><topic>' + cells['subject4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject5'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject5_URI'].value + '"><topic>' + cells['subject5'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject' + if(isBlank(cells['subject_name_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name_URI'].value + '"') + '><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
<subject authority="naf" valueURI="http://id.loc.gov/authorities/names/n79060965"><geographic>Tennessee</geographic><cartographics><coordinates>{{cells['subject_geo_coord'].value}}</coordinates></cartographics></subject>
<classification authority="lcc">{{cells['classification'].value}}</classification>
<typeOfResource>{{cells['item_type'].value}}</typeOfResource>
<language><languageTerm type="text" authority="iso639-2b">English</languageTerm></language>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['digital_collection'].value}}</title></titleInfo></relatedItem>
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```