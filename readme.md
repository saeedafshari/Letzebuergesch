# Words.lu Luxembourgish Dictionary Dataset

Parsed by Saeed Afshari - NeatCapital OU (sa@neatcapital.ee)

Based on the LOD Dataset

Data is stored in the Realm format. More information: https://realm.io

License: Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International Public License

### Conjugation (31006 entries)
```
[Key] public int Id { get; set; }
public string IdItemAdresse { get; set; }
public string P1 { get; set; }
public string P2 { get; set; }
public string P3 { get; set; }
public string P4 { get; set; }
public string P5 { get; set; }
public string P6 { get; set; }
public LodConjugationTypes Type { get; set; }
```

### TextValue (234650 entries)
```
[Key] public int Id { get; set; }
public string IdItemAdresse { get; set; }
public string IdUniteDeSens { get; set; } //LOD Unit ID ID-UNITE-DE-SENS
public string Text { get; set; } //TEXTE-EX, just flatten all values
public LodTextTypes Type { get; set; }
```

### Translation (108673 entries)
```
[Key] public int Id { get; set; }

public string UniqueItemId { get; set; }
public string IdItemAdresse { get; set; }

public LodLanguages SourceLanguageId { get; set; }

[Column(TypeName = "ntext")]
[MaxLength]
public string Lu { get; set; }

[Column(TypeName = "ntext")]
[MaxLength]
public string Fr { get; set; }

[Column(TypeName = "ntext")]
[MaxLength]
public string De { get; set; }

[Column(TypeName = "ntext")]
[MaxLength]
public string En { get; set; }

[Column(TypeName = "ntext")]
[MaxLength]
public string Po { get; set; }
```

### Unit (32315 entries)
```
[Key] public int Id { get; set; }
public string IdItemAdresse { get; set; } //LOD Unique ID ID-ITEM-ADRESSE
public string IdUniteDeSens { get; set; } //LOD Unit ID ID-UNITE-DE-SENS
```

### Word (26221 entries)
```
[Key] public int Id { get; set; }
public string Title { get; set; }
public string IdItemAdresse { get; set; } //LOD Unique ID
public double? Latitude { get; set; } //See SCHWANENTHAL, lod:tag lod:typ="WGS84"
public double? Longitude { get; set; }
public string Genre { get; set; } //Gender
public bool CityName { get; set; } //NOM-DE-LOCALITE
public string PluralForm { get; set; } //FORME-PLURIEL
public string RenvoiSubstIdItemAdresse { get; set; } //see KARDIOLOGIN1 - KARDIOLOG1
public string RenvoiSubstIdUnitesDeSens { get; set; } //see KARDIOLOGIN1 - KARDIOLOG1
public string CitizenMaleIdItemAdresse { get; set; } //CITOYEN see KATARERIN1
public string CitizenFemaleIdItemAdresse { get; set; } //CITOYENNE see KATARERIN1
public string CountryIdItemAdresse { get; set; } //PAYS see KATARERIN1
public string AdjCorrespItemAdresse { get; set; } //ADJ-CORRESP see KATARERIN1 -> KATARESCH1ITE
public bool IsVerb { get; set; } //MS-TYP-VRB
public string VerbAux { get; set; } //VRB-AUXILIAIRE, see OPFLEIEN1
public string Infinitive { get; set; } //INFINITIF
public string PastParticiple { get; set; } //PARTICIPLE-PASSE
public bool HasAudio { get; set; }
```