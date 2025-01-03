# Parkplätze in Baden

## Öffentliche Parkplätze
Interaktive Karte: [Öffentliche Parkplätze in der Stadt Baden](https://overpass-turbo.eu/map.html?Q=%2F*%0APUBLIC+PARKING+IN+BADEN%0A*%2F%0A%0A%5Bout%3Ajson%5D%5Btimeout%3A25%5D%3B%0A%0A%2F%2F+Search+Area%0Aarea%28id%3A3601684261%29-%3E.Baden%3B%0A%28%0A++area%28id%3A3601684261%29%3B%0A++area%28id%3A3601684458%29%3B%0A++%29-%3E.BadenWettingen%3B%0A%0A%0A%2F%2F+1%29+Publicly+accessible+street+parking+%28operated+by+city+of+Baden%29%0Anwr%5B%22amenity%22%3D%22parking%22%5D%5B%22access%22%3D%22yes%22%5D%5B%22parking%22%7E%22%5E%28street_side%7Clane%7Con_kerb%7Chalf_on_kerb%29%24%22%5D%28area.Baden%29%3B%0Aout+geom%3B%0A%0Amake+stats+streetParking%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%2F%2F+2%29+Surface+parkings+operated+by+city+of+Baden%0A%2F%2F+Note%3A+Parking+Schwimmbad+is+located+in+Wettingen%0A%0A%28%0A++nwr%5B%22amenity%22%3D%22parking%22%5D%5B%22access%22%3D%22yes%22%5D%0A++%5B%22parking%22%3D%22surface%22%5D%5B%22operator%22%3D%22Stadt+Baden%22%5D%28area.BadenWettingen%29%3B%0A%29%3B%0Aout+geom%3B%0A%0Amake+stats+surfaceParking%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%2F%2F+3.1%29+Garages+%28%22Parkh%C3%A4user%22%29+operated+by+city+of+Baden%0A%2F%2F+Garages+can+be+maped+with+amenity%3Dparking_entrance+and%2For+amenity%3Dparking.+To+avoid+doublecounting%2C+only+items+with+a+name+are+shown.%0Anwr%5B%22amenity%22%7E%22%5E%28parking%7Cparking_entrance%29%24%22%5D%5B%22access%22%3D%22yes%22%5D%5B%22name%22%7E%22.%22%5D%5B%22parking%22%7E%22%5E%28multi-storey%7Cunderground%7Crooftop%29%24%22%5D%5B%22operator%22%3D%22Stadt+Baden%22%5D%28area.Baden%29%3B%0A%0Aout+geom%3B%0Amake+stats+garageParkingCity%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%2F%2F+3.2%29+Garages+%28%22Parkh%C3%A4user%22%29+operated+by+Parkhaus+L%C3%A4ndli+AG+and+Grand+Casino+Baden+AG%0A%2F%2F+Garages+can+be+maped+with+amenity%3Dparking_entrance+and%2For+amenity%3Dparking.+To+avoid+doublecounting%2C+only+items+with+a+name+are+shown.%0A+nwr%5B%22amenity%22%7E%22%5E%28parking%7Cparking_entrance%29%24%22%5D%5B%22access%22%3D%22yes%22%5D%5B%22name%22%7E%22.%22%5D%5B%22parking%22%7E%22%5E%28multi-storey%7Cunderground%7Crooftop%29%24%22%5D%5B%22operator%22%7E%22%5E%28Parkhaus+L%C3%A4ndli+AG%7CGrand+Casino+Baden+AG%29%24%22%5D%28area.Baden%29%3B%0A%0Aout+geom%3B%0Amake+stats+garageParkingLaendliCasino%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%0A%2F%2F+4%29+Public+parking+%28surface+or+garages%29+operated+by+privates%0A++%0A++++nwr%5B%22amenity%22%7E%22%5E%28parking%7Cparking_entrance%29%24%22%5D%5B%22access%22%3D%22yes%22%5D%5B%22parking%22%7E%22%5E%28surface%7Cmulti-storey%7Cunderground%7Crooftop%29%24%22%5D%5B%22operator%3Atype%22%21%3D%22government%22%5D%5B%22operator%3Atype%22%5D%5B%22operator%22%21%3D%22Parkhaus+L%C3%A4ndli+AG%22%5D%5B%22operator%22%21%3D%22Grand+Casino+Baden+AG%22%5D%28area.Baden%29%3B%0Aout+geom%3B%0Amake+stats+publicParkingByPrivate%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%2F%2F+MAP+STYLE%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%2F%2F+Best+use+with+Tile+Server%3A+http%3A%2F%2F%7Bs%7D.basemaps.cartocdn.com%2Flight_all%2F%7Bz%7D%2F%7Bx%7D%2F%7By%7D.png%7B%7Bstyle%3A+%0A%0A*%5Bparking%3Dlane%5D%0A%7B+color%3A+steelblue%3B+fill-color%3Asteelblue%3B+%7D%0A*%5Bparking%3Dstreet_side%5D%0A%7B+color%3A+steelblue%3B+fill-color%3Asteelblue%3B+%7D%0A*%5Bparking%3Don_kerb%5D%0A%7B+color%3A+steelblue%3B+fill-color%3Asteelblue%3B+%7D%0A*%5Bparking%3Dhalf_on_kerb%5D%0A%7B+color%3A+steelblue%3B+fill-color%3Asteelblue%3B+%7D%0A%0A*%5Bparking%3Dsurface%5D%0A%7B+color%3A+%236646b4%3B+fill-color%3A%236646b4%3B+%7D%0A%0A*%5Bparking%3Dmulti-storey%5D%0A%7B+color%3A+%23b446a7%3B+fill-color%3A%23b446a7+%7D%0A*%5Bparking%3Dunderground%5D%0A%7B+color%3A+%23b446a7%3B+fill-color%3A%23b446a7%3B+%7D%0A*%5Bparking%3Drooftop%5D%0A%7B+color%3A+%23b446a7%3B+fill-color%3A%23b446a7%3B+%7D%0A%0A*%5Boperator%3DParkhaus+L%C3%A4ndli+AG%5D%0A%7B+color%3A+%23b446a7%3B+fill-color%3A%23b446a7%3B+dashes%3A1%2C3%3B%7D%0A*%5Boperator%3DGrand+Casino+Baden+AG%5D%0A%7B+color%3A+%23b446a7%3B+fill-color%3A%23b446a7%3B+dashes%3A1%2C3%3B%7D%0A%0A*%5Boperator%3Atype%5D%5Boperator%21%3DStadt+Baden%5D%5Boperator%21%3DParkhaus+L%C3%A4ndli+AG%5D%5Boperator%21%3DGrand+Casino+Baden+AG%5D%0A%7B+color%3A+red%3B+fill-color%3Ared%3B%7D%0A%7Btext%3A+eval%28%22tag%28%27name%27%29%22%29%3B%7D%0A%0A*%5Bcapacity%3E25%5D%0A%7Btext%3A+eval%28%22tag%28%27name%27%29+.+%27+%28%27+.+tag%28%27capacity%27%29+.+%27%29%27%22%29%3B%7D%0A%0A%0A+%7D%7D)

Karte mit Abfragequery: [Link](https://overpass-turbo.eu/s/1WxE)

| | Typ | Anzahl Parkfelder[^3] |
|--|--|--|
| $`\textcolor{steelblue}{\text{●}}`$ |  Öffentliche Parkplätze auf und entlang von Strassen | 909
| $`\textcolor{#6646b4}{\text{●}}`$ | Oberirdische Parkierungsanlagen, im Besitz der Stadt Baden | 688
| | **Total öffentliche oberirdische Parkplätze** | **1'597**
| $`\textcolor{#b446a7}{\text{●}}`$ | Öffentliche Parkhäuser, im Besitz der Stadt Baden | 1'053
| $`\textcolor{#b446a7}{\text{◌}}`$ | Öffentliche Parkhäuser, 50% im Besitz der Stadt Baden [^1] | 948
| | **Total Parkplätze in Parkhäusern im (Teil-) Eigentum der Stadt Baden** | **2'001**
| $`\textcolor{red}{\text{●}}`$ | Öffentliche Parkplätze im privaten Besitz | min. 3'093 [^2]
| | **Total öffentliche Parkplätze in Baden** | **min. 6'691**

[![parkingMap](https://github.com/user-attachments/assets/5425308f-0b49-418a-8a22-af085cf9a5d9)](https://overpass-turbo.eu/map.html?Q=%2F*%0APUBLIC+PARKING+IN+BADEN%0A*%2F%0A%0A%5Bout%3Ajson%5D%5Btimeout%3A25%5D%3B%0A%0A%2F%2F+Search+Area%0Aarea%28id%3A3601684261%29-%3E.Baden%3B%0A%28%0A++area%28id%3A3601684261%29%3B%0A++area%28id%3A3601684458%29%3B%0A++%29-%3E.BadenWettingen%3B%0A%0A%0A%2F%2F+1%29+Publicly+accessible+street+parking+%28operated+by+city+of+Baden%29%0Anwr%5B%22amenity%22%3D%22parking%22%5D%5B%22access%22%3D%22yes%22%5D%5B%22parking%22%7E%22%5E%28street_side%7Clane%7Con_kerb%7Chalf_on_kerb%29%24%22%5D%28area.Baden%29%3B%0Aout+geom%3B%0A%0Amake+stats+streetParking%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%2F%2F+2%29+Surface+parkings+operated+by+city+of+Baden%0A%2F%2F+Note%3A+Parking+Schwimmbad+is+located+in+Wettingen%0A%0A%28%0A++nwr%5B%22amenity%22%3D%22parking%22%5D%5B%22access%22%3D%22yes%22%5D%0A++%5B%22parking%22%3D%22surface%22%5D%5B%22operator%22%3D%22Stadt+Baden%22%5D%28area.BadenWettingen%29%3B%0A%29%3B%0Aout+geom%3B%0A%0Amake+stats+surfaceParking%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%2F%2F+3.1%29+Garages+%28%22Parkh%C3%A4user%22%29+operated+by+city+of+Baden%0A%2F%2F+Garages+can+be+maped+with+amenity%3Dparking_entrance+and%2For+amenity%3Dparking.+To+avoid+doublecounting%2C+only+items+with+a+name+are+shown.%0Anwr%5B%22amenity%22%7E%22%5E%28parking%7Cparking_entrance%29%24%22%5D%5B%22access%22%3D%22yes%22%5D%5B%22name%22%7E%22.%22%5D%5B%22parking%22%7E%22%5E%28multi-storey%7Cunderground%7Crooftop%29%24%22%5D%5B%22operator%22%3D%22Stadt+Baden%22%5D%28area.Baden%29%3B%0A%0Aout+geom%3B%0Amake+stats+garageParkingCity%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%2F%2F+3.2%29+Garages+%28%22Parkh%C3%A4user%22%29+operated+by+Parkhaus+L%C3%A4ndli+AG+and+Grand+Casino+Baden+AG%0A%2F%2F+Garages+can+be+maped+with+amenity%3Dparking_entrance+and%2For+amenity%3Dparking.+To+avoid+doublecounting%2C+only+items+with+a+name+are+shown.%0A+nwr%5B%22amenity%22%7E%22%5E%28parking%7Cparking_entrance%29%24%22%5D%5B%22access%22%3D%22yes%22%5D%5B%22name%22%7E%22.%22%5D%5B%22parking%22%7E%22%5E%28multi-storey%7Cunderground%7Crooftop%29%24%22%5D%5B%22operator%22%7E%22%5E%28Parkhaus+L%C3%A4ndli+AG%7CGrand+Casino+Baden+AG%29%24%22%5D%28area.Baden%29%3B%0A%0Aout+geom%3B%0Amake+stats+garageParkingLaendliCasino%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%0A%2F%2F+4%29+Public+parking+%28surface+or+garages%29+operated+by+privates%0A++%0A++++nwr%5B%22amenity%22%7E%22%5E%28parking%7Cparking_entrance%29%24%22%5D%5B%22access%22%3D%22yes%22%5D%5B%22parking%22%7E%22%5E%28surface%7Cmulti-storey%7Cunderground%7Crooftop%29%24%22%5D%5B%22operator%3Atype%22%21%3D%22government%22%5D%5B%22operator%3Atype%22%5D%5B%22operator%22%21%3D%22Parkhaus+L%C3%A4ndli+AG%22%5D%5B%22operator%22%21%3D%22Grand+Casino+Baden+AG%22%5D%28area.Baden%29%3B%0Aout+geom%3B%0Amake+stats+publicParkingByPrivate%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%2F%2F+MAP+STYLE%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%2F%2F+Best+use+with+Tile+Server%3A+http%3A%2F%2F%7Bs%7D.basemaps.cartocdn.com%2Flight_all%2F%7Bz%7D%2F%7Bx%7D%2F%7By%7D.png%7B%7Bstyle%3A+%0A%0A*%5Bparking%3Dlane%5D%0A%7B+color%3A+steelblue%3B+fill-color%3Asteelblue%3B+%7D%0A*%5Bparking%3Dstreet_side%5D%0A%7B+color%3A+steelblue%3B+fill-color%3Asteelblue%3B+%7D%0A*%5Bparking%3Don_kerb%5D%0A%7B+color%3A+steelblue%3B+fill-color%3Asteelblue%3B+%7D%0A*%5Bparking%3Dhalf_on_kerb%5D%0A%7B+color%3A+steelblue%3B+fill-color%3Asteelblue%3B+%7D%0A%0A*%5Bparking%3Dsurface%5D%0A%7B+color%3A+%236646b4%3B+fill-color%3A%236646b4%3B+%7D%0A%0A*%5Bparking%3Dmulti-storey%5D%0A%7B+color%3A+%23b446a7%3B+fill-color%3A%23b446a7+%7D%0A*%5Bparking%3Dunderground%5D%0A%7B+color%3A+%23b446a7%3B+fill-color%3A%23b446a7%3B+%7D%0A*%5Bparking%3Drooftop%5D%0A%7B+color%3A+%23b446a7%3B+fill-color%3A%23b446a7%3B+%7D%0A%0A*%5Boperator%3DParkhaus+L%C3%A4ndli+AG%5D%0A%7B+color%3A+%23b446a7%3B+fill-color%3A%23b446a7%3B+dashes%3A1%2C3%3B%7D%0A*%5Boperator%3DGrand+Casino+Baden+AG%5D%0A%7B+color%3A+%23b446a7%3B+fill-color%3A%23b446a7%3B+dashes%3A1%2C3%3B%7D%0A%0A*%5Boperator%3Atype%5D%5Boperator%21%3DStadt+Baden%5D%5Boperator%21%3DParkhaus+L%C3%A4ndli+AG%5D%5Boperator%21%3DGrand+Casino+Baden+AG%5D%0A%7B+color%3A+red%3B+fill-color%3Ared%3B%7D%0A%7Btext%3A+eval%28%22tag%28%27name%27%29%22%29%3B%7D%0A%0A*%5Bcapacity%3E25%5D%0A%7Btext%3A+eval%28%22tag%28%27name%27%29+.+%27+%28%27+.+tag%28%27capacity%27%29+.+%27%29%27%22%29%3B%7D%0A%0A%0A+%7D%7D)

## Private Parkplätze
> [!WARNING]
> Die Zahlen zu den privaten Parkplätzen in Baden sind auf OpenStreetMap noch sehr unvollständig. Unterirdische Parkierungsanlagen fehlen praktisch komplett, die oberirdischen sind unvollständig. Bei der Aktualisierung im Dezember 24/Januar 25 lag der Fokus auf den öffentlichen Parkplätzen.

Interaktive Karte: [Private Parkplätze in der Stadt Baden](https://overpass-turbo.eu/map.html?Q=%2F%2F+%40name+Private+Parking+Stadt+Baden%0A%0A%2F*%0APRIVATE+PARKING+IN+BADEN+%28incomplete+data%21%29%0A*%2F%0A%0A%5Bout%3Ajson%5D%5Btimeout%3A25%5D%3B%0A%0A%2F%2F+Search+Area%0Aarea%28id%3A3601684261%29-%3E.Baden%3B%0A%28%0A++area%28id%3A3601684261%29%3B%0A++area%28id%3A3601684458%29%3B%0A++%29-%3E.BadenWettingen%3B%0A%0A%0A%2F%2F+1%29+Private+street+parking+%0Anwr%5B%22amenity%22%3D%22parking%22%5D%5B%22access%22%5D%5B%22access%22%21%3D%22yes%22%5D%5B%22parking%22%7E%22%5E%28street_side%7Clane%7Con_kerb%7Chalf_on_kerb%29%24%22%5D%28area.Baden%29%3B%0Aout+geom%3B%0A%0Amake+stats+streetParking%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%2F%2F+2%29+Private+surface+parking+%0Anwr%5B%22amenity%22%3D%22parking%22%5D%5B%22access%22%5D%5B%22access%22%21%3D%22yes%22%5D%5B%22parking%22%3D%22surface%22%5D%28area.Baden%29%3B%0Aout+geom%3B%0A%0Amake+stats+surfaceParking%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%2F%2F+3%29+Private+garage+parking%0A%0Anwr%5B%22amenity%22%7E%22%5E%28parking%7Cparking_entrance%29%24%22%5D%5B%22access%22%5D%5B%22access%22%21%3D%22yes%22%5D%5B%22parking%22%7E%22%5E%28multi-storey%7Cunderground%7Crooftop%29%24%22%5D%28area.Baden%29%3B%0A%0Aout+geom%3B%0Amake+stats+garageParking%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%2F%2F+MAP+STYLE%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%2F%2F+Best+use+with+Tile+Server%3A+http%3A%2F%2F%7Bs%7D.basemaps.cartocdn.com%2Flight_all%2F%7Bz%7D%2F%7Bx%7D%2F%7By%7D.png%7B%7Bstyle%3A+%0A%0A*%5Bparking%3Dlane%5D%0A%7B+color%3A+gold%3B+fill-color%3Agold%3B+%7D%0A*%5Bparking%3Dstreet_side%5D%0A%7B+color%3A+gold%3B+fill-color%3Agold%3B+%7D%0A*%5Bparking%3Don_kerb%5D%0A%7B+color%3A+gold%3B+fill-color%3Agold%3B+%7D%0A*%5Bparking%3Dhalf_on_kerb%5D%0A%7B+color%3A+gold%3B+fill-color%3Agold%3B+%7D%0A%0A*%5Bparking%3Dsurface%5D%0A%7B+color%3A+goldenrod%3B+fill-color%3Agoldenrod+%7D%0A%0A*%5Bparking%3Dmulti-storey%5D%0A%7B+color%3A+darkorange%3B+fill-color%3Adarkorange+%7D%0A*%5Bparking%3Dunderground%5D%0A%7B+color%3A+darkorange%3B+fill-color%3Adarkorange+%7D%0A*%5Bparking%3Drooftop%5D%0A%7B+color%3A+darkorange%3B+fill-color%3Adarkorange+%7D%0A%0A*%5Bcapacity%3E25%5D%0A%7Btext%3A+eval%28%22tag%28%27name%27%29+.+%27+%28%27+.+tag%28%27capacity%27%29+.+%27%29%27%22%29%3B%7D%0A%0A+%7D%7D)

Karte mit Abfragequery: [Link](https://overpass-turbo.eu/s/1WxG)

| | Typ | Anzahl Parkfelder[^3][^7] |
|--|--|--|
| $`\textcolor{gold}{\text{●}}`$ |  Private Parkplätze entlang von Strassen | min. 1'530
| $`\textcolor{goldenrod}{\text{●}}`$ | Private oberirdische Parkierungsanlagen | min. 2'781
| | **Total oberirdische private Parkplätze** | **min. 4'311**
| $`\textcolor{darkorange}{\text{●}}`$ | Private Parkhäuser | zu wenig Daten

[![privateParkingMap](https://github.com/user-attachments/assets/1cf6daed-059a-4121-bc6e-91d716e464eb)](https://overpass-turbo.eu/map.html?Q=%2F%2F+%40name+Private+Parking+Stadt+Baden%0A%0A%2F*%0APRIVATE+PARKING+IN+BADEN+%28incomplete+data%21%29%0A*%2F%0A%0A%5Bout%3Ajson%5D%5Btimeout%3A25%5D%3B%0A%0A%2F%2F+Search+Area%0Aarea%28id%3A3601684261%29-%3E.Baden%3B%0A%28%0A++area%28id%3A3601684261%29%3B%0A++area%28id%3A3601684458%29%3B%0A++%29-%3E.BadenWettingen%3B%0A%0A%0A%2F%2F+1%29+Private+street+parking+%0Anwr%5B%22amenity%22%3D%22parking%22%5D%5B%22access%22%5D%5B%22access%22%21%3D%22yes%22%5D%5B%22parking%22%7E%22%5E%28street_side%7Clane%7Con_kerb%7Chalf_on_kerb%29%24%22%5D%28area.Baden%29%3B%0Aout+geom%3B%0A%0Amake+stats+streetParking%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%2F%2F+2%29+Private+surface+parking+%0Anwr%5B%22amenity%22%3D%22parking%22%5D%5B%22access%22%5D%5B%22access%22%21%3D%22yes%22%5D%5B%22parking%22%3D%22surface%22%5D%28area.Baden%29%3B%0Aout+geom%3B%0A%0Amake+stats+surfaceParking%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%2F%2F+3%29+Private+garage+parking%0A%0Anwr%5B%22amenity%22%7E%22%5E%28parking%7Cparking_entrance%29%24%22%5D%5B%22access%22%5D%5B%22access%22%21%3D%22yes%22%5D%5B%22parking%22%7E%22%5E%28multi-storey%7Cunderground%7Crooftop%29%24%22%5D%28area.Baden%29%3B%0A%0Aout+geom%3B%0Amake+stats+garageParking%3Dsum%28is_tag%28%22capacity%22%29+%3F+number%28t%5B%22capacity%22%5D%29+%3A+0%29%3B%0Aout%3B%0A%0A%2F%2F+MAP+STYLE%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%0A%2F%2F+Best+use+with+Tile+Server%3A+http%3A%2F%2F%7Bs%7D.basemaps.cartocdn.com%2Flight_all%2F%7Bz%7D%2F%7Bx%7D%2F%7By%7D.png%7B%7Bstyle%3A+%0A%0A*%5Bparking%3Dlane%5D%0A%7B+color%3A+gold%3B+fill-color%3Agold%3B+%7D%0A*%5Bparking%3Dstreet_side%5D%0A%7B+color%3A+gold%3B+fill-color%3Agold%3B+%7D%0A*%5Bparking%3Don_kerb%5D%0A%7B+color%3A+gold%3B+fill-color%3Agold%3B+%7D%0A*%5Bparking%3Dhalf_on_kerb%5D%0A%7B+color%3A+gold%3B+fill-color%3Agold%3B+%7D%0A%0A*%5Bparking%3Dsurface%5D%0A%7B+color%3A+goldenrod%3B+fill-color%3Agoldenrod+%7D%0A%0A*%5Bparking%3Dmulti-storey%5D%0A%7B+color%3A+darkorange%3B+fill-color%3Adarkorange+%7D%0A*%5Bparking%3Dunderground%5D%0A%7B+color%3A+darkorange%3B+fill-color%3Adarkorange+%7D%0A*%5Bparking%3Drooftop%5D%0A%7B+color%3A+darkorange%3B+fill-color%3Adarkorange+%7D%0A%0A*%5Bcapacity%3E25%5D%0A%7Btext%3A+eval%28%22tag%28%27name%27%29+.+%27+%28%27+.+tag%28%27capacity%27%29+.+%27%29%27%22%29%3B%7D%0A%0A+%7D%7D)

## Gedanken dazu

1. Die von der Stadt für 2025 **budgetierten 1'500 Oberflächenparkplätze stimmen ziemlich gut**. Trotz des "Abbaus" im 2024 (AZ-Hochhaus, Parkstrasse) sind es noch immer rund 1'600 oberirdische Parkplätze.
2. Die knapp 900 Parkplätze entlang von Strassen sind nicht unerheblich. **Viel wichtiger sind aber die grösseren Parkierungsanlagen (oberirdisch und in Parkhäusern)**. Im (Teil-) Besitz der Stadt Baden sind das rund 1'700 Parkplätze, zählt man die öffentlich zugänglichen privaten Anlagen dazu, sind es sogar mindestens rund 5'800; da fallen die 900 wenig ins Gewicht (15 %).
3. Die **Zahl der privaten öffentlichen Parkplätze ist nicht vollständig**. Es fehlen noch einige Anlagen (z.B. Bareggcenter). Auch wenn einige dieser Anlagen oft einen primären Zweck haben (z.B. Parkplatz bei der Boulderhalle), können diese allgemein benutzt werden und sollten daher mitberücksichtigt werden.
4. **Baden hat mit total mindestens rund 6'700 öffentlich zugänglichen Parkplätzen sehr viele Parkplätze**. Es macht daher sicher keinen Sinn, über die Aufhebung einzelner weniger Parkplätze (z.B. entlang Oberstadtstrasse) lange zu diskutieren.
5. Die Haltung des Stadrats, oberirdische Parkplätze entlang von Strassen in (unterirdische) Parkierungsanlagen zu verschieben macht grundsätzlich Sinn. Dies ist aber nicht überall gleich dringend. Es gibt viele Stellen, wo diese Parkplätze wenig stören und teilweise auch notwendig sind; z.B. weil Private auf ihrem Grundstück keine Parkplätze erstellen konnten und dafür eine Abgabe bezahlt haben ("planungsrechtlich notwendige Dauerparkierung"). **Eine Aufhebung/Verschiebung oberirdischer Parkplätze ist m.E. aus folgenden Gründen dringend**:
   - Städtebauliche Gründe: Strassenraum ist öffentlicher Raum. Statt ihn mit Autos zu besetzen, kann er begrünt oder belebt werden. Beispiel: Bereich ums AZ-Hochhaus.
   - Wichtige Infrastrukturen: Beispielsweise Veloinfrastruktur. Beispiel: Veloschnellroute Zürcherstrasse.
   - Klimawirksame Massnahmen: Begrünung oder Entsiegelung. Beispiel: Bereich ums AZ-Hochhaus.
6. Als Argument für Notwendigkeit von Strasenparkplätzen werden oft gehbehinderte Personen ins Feld geführt, welche auf Parkplätze angewiesen sind, die nahe am Ziel liegen. Von den rund 1'500 Oberflächenparkplätzen im Eigentum der Stadt Baden sind aber **nur gerade 8 Parkplätze für Behinderte** reserviert ([Link zur Analyse](https://overpass-turbo.eu/s/1WxI)). Mehr Behindertenparkplätze würden hier wohl mehr helfen. 
7. Der Fokus liegt hier auf den öffentlichen Parkplätzen. Aber man darf die **privaten Parkplätze** (Bewohnende, Besuchende, Angestellte, etc.) nicht vergessen! Die Zahlen dazu sind auf OSM noch sehr unvollständig. Es fehlen etliche Parkplätze, vor allem unterirdische Parkierungen fehlen praktisch komplett.
   - Trotz den unvollständigen Zahlen sind schon jetzt **sehr viele oberirdische private Parkplätze** in der OSM Datenbank vorhanden: **Total über 4'300**! Das sind weit mehr als die öffentlich zugänglichen oberirdischen Parkplätze. Davon liegen rund 1'500 entlang oder neben Strassen und prägen somit das öffentliche Strassenbild. 
   - Die Anzahl privater Parkplätze wird über die BNO gesteuert. In Baden sind heute bis zu 1 Parkplatz pro Wohnung möglich - auch im Zentrum. Das ist weit mehr, als beispielsweise Winterthur zulässt[^4]. Daher ist es wichtig, dass die BNO in diesem Bereich überarbeitet wird und weniger Parkplätze zulässt.
8. Insgesamt sind in der OSM Datenbank in Baden 10'504 Parkplätze vorhanden. Da noch etliche unterirdische private Parkierungsanlagen sowie Garagen und Vorplätze fehlen, wird die totale Anzahl weit höher ausfallen. In der Schweiz werden etwa ein Parkplatz pro EinwohnerIn geschätzt[^5], in Baden dürfte dieser Wert mindestens ähnlich gross sein. Eine Grössenordnung von 25'000 Parkplätzen ist durchaus realistisch. Bei 20 m² pro Parkplatz (inkl. Platz für Zufahrt etc.) wären das 500'000 m² Parkfpläche, das entspricht etwa 70 Fussballfeldern und würde die gesamte Badener Innenstadt inkl. Baden Nord und Martinsberg abdecken!
9. Eine Studie der Credit Suisse aus dem Jahr 2020 stellt in der Schweiz generell ein Überangebot an Parkplätzen fest. [^6]

Die meisten der oben aufgeführten Punkte werden im **Konzept öffentliche Parkierung Innenstadt Baden (September 2024)** gestützt und detailliert erläutert. Wichtige Punkte des Konzepts:
- Kreise Modell: Die Stadt wird in 3 Kreise unterteilt, worin die Parkplätze für unterschiedliche Zielgruppen zur verfügung stehen sollen. Im Zentrum primär planungsrechtlich notwendige Dauerparkieruende und Kurzzeitparkierende, in peripheren Lagen auch "planungsrechtlich nicht notwendige" Dauerparkierende. Die Begriffe werden im Bericht erläutert.
- Oberirdische Parkplätze sollen aufgehoben werden, prioritär in den Kreisen 1 und 2. In den öffentlichen Parkhäusern (der Stadt und von Privaten) hat es noch Platz, um diese Parkplätze aufzunehmen.
- Um in den Parkhäusern mehr Platz für Kurzzeitparkierende und planungsroechtlich notwendige Dauerparkierende zu schaffen, müssen die Dauerparkkarten restriktiver ausgegeben werden.

## Datenquelle
Die Daten stammen von [OpenStreetMap](https://www.openstreetmap.org/) und wurden vom team baden anhand von Luftbildern (August 2024) sowie Begehungen im Dezember 24/Januar 25 aktualisiert. OpenStreetMap ist eine öffentliche Datenplattform, jede:r kann die Karte bearbeiten. Es besteht kein Anspruch auf Vollständigkeit.
Fehler bitte direkt auf OpenStreetMap korrigieren oder melden an: till.schmid@teambaden.ch.

[^1]: Parkhaus Ländli AG und Grand Casino Baden AG
[^2]: Zahlen auf OSM unvollständig. Die Zahl hier beinhaltet zudem das sich im Bau befindliche Parkhaus Brown-Boveri-Platz (498 Parkplätze), welches auf OSM noch fehlt.
[^3]: Stand 2.1.2025
[^4]: [GVK Raum Baden und Umgebung, Konferenz 25.5.24, Folie 68](https://www.ag.ch/media/kanton-aargau/bvu/mobilitaet-und-verkehr/gesamtverkehrsplanung/gvk-region-ostaargau/raum-baden-und-umgebung/projektdokumentation/20240525-gvk-raum-baden-uu-mok4a-vollst-ndig-1.pdf)
[^5]: https://www.tagesanzeiger.ch/parkplatz-land-schweiz-661473879811
[^6]: [Schweizer Immobilienmarkt 2020, Credit Suisse, Seite 31 ff.](./schweizer-immobilienmarkt-2020.pdf)
[^7]: Zahlen sehr unvollständig, siehe Warnung oben.
