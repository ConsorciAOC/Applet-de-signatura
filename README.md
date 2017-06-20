# Applet de Signatura

En aquest repositori podeu trobar els *JARs* de l'útlima versió alliberada de l'applet. 

Aquesta versió és només per als integradors que han fet ús de versions antigues de l'applet que encara no han pogut integrar-se amb el [servei del Signador](https://signador-pre.aoc.cat/signador/init) 
però tenen la necessitat de filtrar els certificats seleccionables per l'usuari entre els de signatura i els d'autenticació.

No s'adjunta documentació, aquesta és pot trobar [al portal del Consorci AOC](https://www.aoc.cat/knowledge-base/manual-dusuari-integracio-applet-de-signatura/idservei/integracio/). L'únic canvi que incorpora aquesta versió *2.6.7* respecte l'anterior és el paràmetre `keyUsage` que es descriu a continuació:

- keyUsage: Permet filtrar per l'ús de la clau del certificat, de signatura o d'autenticació. Els possibles valors d'aquest atribut són:

  - FD : Firma digital.
  - NR : Non repudiation.

Es poden indicar múltiples entrades separades per punts i comes `;`. El filtre es case insensitive. Per defecte filtra per les dues opcions. Exemple: `"NR; FD"`.

# End of life
El *EOL* del Applet es va decidir que fos a principis d'any a data _31 de Maig de 2017_. 

Això és degut a la caiguda en desús dels applets java, degut al seu funcionament poc user-friendly i als coneguts i continus problemes de seguretat. 

La aparició del _HTML5_ i la migració de moltes funcionalitats dels applets a la web gracies a les noves funcionalitats del _HTML5_ han acabat de rematar-ho. 

A més ja fa un temps que el [*Chrome* va descontinuar](https://www.chromium.org/developers/npapi-deprecation) el suport del plugin de Java, recentment *Firefox* en la seva
versió 52, s'ha sumat també a deixar de donar suport als plugin Java, i el nou navegador *Edge* de Microsoft ja no li ha donat suport des de bon principi.

L'alternativa que s'ofereix des del Consorci és la integració amb el [servei del Signador](https://signador-pre.aoc.cat/signador/init). 
Del qual podeu trobar [aqui la documentació](https://github.com/ConsorciAOC/signador).



