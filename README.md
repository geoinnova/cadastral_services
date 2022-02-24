# cadastral_services

## Sistema de referencia Parámetro Código EPSG

**Longitud/ Latitud**

Geográficas WGS84 4326 EPSG:4326
Geográficas ETRS89 4258 EPSG:4258

**UTM x/y**

ETRS89 / UTM zone 29N 25829 EPSG:25829
ETRS89 / UTM zone 30N 25830 EPSG:25830
ETRS89 / UTM zone 31N 25831 EPSG:25831 **

**Openlayers**

Web Mercator 3785 EPSG:3785
Web Mercator 3857 EPSG:3857 

## Organización datos catatso

### Manzana-Zona 
Para Urbana: 12 digitos (manzana(5) + PCAT2(7))
Para rústica: 9 dígitos (del,mun, sector,polígono)

52270DE7052N
52250DE7052N

## Parcela
Referencia catastral de 14 posiciones para Urbana y para Rústica
5225043DE7052N

## Inmueble
5225043DE7052N0001PQ

# Servicios Catastro Inspire
- https://www.catastro.minhap.es/webinspire/index.html

**Manzana (GetZoning - cod_zona) Catastro por identificador común**

http://ovc.catastro.meh.es/INSPIRE/wfsCP.aspx?
service=wfs&
version=2&
request=storedqueries&
STOREDQUERIE_ID=GetZoning&
cod_zona=5225043DE7052N&
srsname=EPSG::4326

[https://ovc.catastro.meh.es/INSPIRE/wfsCP.aspx?service=wfs&version=2&request=storedqueries&STOREDQUERIE_ID=GetZoning&cod_zona=52250DE7052N&srsname=EPSG::3785](https://ovc.catastro.meh.es/INSPIRE/wfsCP.aspx?service=wfs&version=2&request=storedqueries&STOREDQUERIE_ID=GetZoning&cod_zona=52250DE7052N&srsname=EPSG::3785)


**Parcela (GetParcel-REFCAT)**

Parcela por identificador
Ejemplo Parcela

http://ovc.catastro.meh.es/INSPIRE/wfsCP.aspx?
service=wfs&
version=2&
request=storedqueries&
STOREDQUERIE_ID=GetParcel&
REFCAT=5225043DE7052N&
srsname=EPSG::4326

http://ovc.catastro.meh.es/INSPIRE/wfsCP.aspx?service=wfs&version=2&request=storedqueries&STOREDQUERIE_ID=GetParcel&REFCAT=5225043DE7052N&srsname=EPSG::4326

**Edicidicio (descarga)**
http://ovc.catastro.meh.es/INSPIRE/wfsBU.aspx?service=wfs&version=2&request=getfeature&STOREDQUERIE_ID=GETBUILDINGBYPARCEL&refcat=5225043DE7052N&srsname=EPSG::4326

- Foto fachada de edificio

https://ovc.catastro.meh.es/OVCServWeb/OVCWcfLibres/OVCFotoFachada.svc/RecuperarFotoFachadaGet?ReferenciaCatastral=5225043DE7052N

- Dirección edicio
http://ovc.catastro.meh.es/INSPIRE/wfsAD.aspx?service=wfs&version=2&request=GetFeature&STOREDQUERIE_ID=GetadByRefcat&refcat=5225043DE7052N&srsname=EPSG::4326

CL MAR, DE SA 119
SOLLER (ILLES BALEARS)
1.287 m2

Ejemplo de datos del inmueble en la web del Catastro

https://www1.sedecatastro.gob.es/CYCBienInmueble/OVCListaBienes.aspx?RC1=5225043&RC2=DE7052N&RC3=&RC4=&esBice=&RCBice1=&RCBice2=&DenoBice=&pest=rc&final=&RCCompleta=5225043DE7052N&from=OVCBusqueda&tipoCarto=nuevo&ZV=NO&ZR=NO&anyoZV=&strFechaVR=&tematicos=&anyotem=


## URL Y PARÁMETROS:

https://www.catastro.minhap.es/webinspire/documentos/inspire-cp-WFS.pdf


### Parcelas Catastrales por referencia catastral ###

http://ovc.catastro.meh.es/INSPIRE/wfsCP.aspx?service=wfs&version=2&request=getfeature&STOREDQUERIE_ID=GetParcel&refcat=3662001TF3136S&srsname=EPSG::25830

3662001TF3136S

* Longitud Ref: **14**
* Identificador (STOREDQUERIE_ID): **GetParcel**
* Parámetros: **REFCAT**
* Retorno: **CP:CadastralParcel**


### Parcelas catastrales, propia y colindantes por referencia catastral ###

http://ovc.catastro.meh.es/INSPIRE/wfsCP.aspx?service=wfs&version=2&request=getfeature&STOREDQUERIE_ID=GETNEIGHBOURPARCEL&refcat=3662001TF3136S&srsname=EPSG::25830

3662001TF3136S

* Longitud Ref: **14**
* Identificador (STOREDQUERIE_ID): **GetNeighbourParcel**
* Parámetros: **REFCAT**
* Retorno: **CP:CadastralParcel**


### Zonas Catastrales por código de zona ### 

http://ovc.catastro.meh.es/INSPIRE/wfsCP.aspx?service=wfs&version=2&request=getfeature&STOREDQUERIE_ID=GetZoning&cod_zona=41624TF3146S&srsname=EPSG::25830

41624TF3146S

* Longitud Ref: **12**
* Identificador (STOREDQUERIE_ID): **GetZoning**
* Parámetros: **COD_ZONA**
* Retorno: **CP:CadastralZoning **


### Parcelas catastrales de una zona por su código de zona ###
http://ovc.catastro.meh.es/INSPIRE/wfsCP.aspx?service=wfs&version=2&request=getfeature&STOREDQUERIE_ID=Getparcelsbyzoning&cod_zona=36620TF3136S&srsname=EPSG::25830

* Longitud Ref: **12**
* Identificador (STOREDQUERIE_ID): **GetParcelsByZoning**
* Parámetros: **COD_ZONA**
* Retorno: **CP:CadastralParcel**



url= "http://ovc.catastro.meh.es/INSPIRE/wfsCP.aspx?service=wfs&version=2&request=getfeature&STOREDQUERIE_ID="
+identificador+"&"
+paremetros+"="+referencia_catastral
+"&srsname=EPSG::"+sistema_referencia 


