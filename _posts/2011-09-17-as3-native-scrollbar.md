---
id: 2011017
title: AS3 native scrollbar 
date: 2011-09-17T11:27:07+00:00
author: Gorka
layout: post
permalink: /2011/09/as3-native-scrollbar/
categories:
  - Ideas
---
<img style="margin: auto;" src="/public/img/2011/09/as3-scrollbar.png" alt="AS3 scrollbar" />

Para uno de mis proyectos (y lo más seguro es que para todos eventualmente) me encontré con la necesidad de poner un texto en un espacio más chico del total del texto, esto simple y sencillamente se soluciona habilitando un scrollbar.

La onda fue que al hacer uso del Componente que ya existe en flash de scrollbar me vino la duda si a la hora de enviarlo al iphone se vería de manera “nativa” o si mantendría el aspecto de flash. Al hacer las pruebas ví que mantenía el aspecto típico, y eso no me gustó nada porque le quita “usabilidad” (al no usar controles nativos a los que los usuarios ya se van acostumbrando – OJO gracias al desarrollo de apps para ios en flash y as3 se pueden recrear TODOS los controles que se quiera y a veces es bueno para innovar, pero en este caso es algo tan sencillo que no valía la pena recrearlo todo).

Busqué un rato en web y no encontré nada para iOS, hay muchos sí para AS3 pero simplemente para aplicaciones o web nada para mobile. Intenté trucar el componente que viene con flash y no sirvió de mucho, así que tuve que ponerme a hacer esto por código propio desde cero.

Resultó algo muy fácil, es una simple clase que al instanciar se le tienen que dar dos parametros: 1.- el movieclip origen (esto para que tenga acceso al stage y así pueda usar addChild) y 2.- la caja de texto a la que se le va a poner el scrollbar.

**Notas**
- Es deficiente en el sentido que no tiene animaciones fluídas para moverse ni para hacer fade in o fade out según su uso.
- Nada más funciona en sentido vertical (con unos pocos cambios se puede hacer horizontal, pero en mobile nunca he visto eso).
- Por ahora sólo funciona con TextField’s (con otros pocos cambios se le puede hacer funcionar con cualquier control/componente/movieclip).
- Seguramente se puede eficientar el proceso y agregar un par de listeners para que se integre aún mejor, pero con lo que es funciona y funciona muy bien.
- Desde el constructor se puede controlar toda la “vista” o aspecto del scrollbar.

```as3
package {
  import flash.display.MovieClip;
  import flash.display.Shape;
  import flash.events.*;
  import flash.text.TextField;

  public class ComponentVerticalScrollbar {
    // ——- Constructor ——-
    public function ComponentVerticalScrollbar(obj_home:MovieClip, obj_text_field:TextField, num_width:Number=5, num_round_w:Number=2, num_round_h=2, num_alpha:Number=.5, num_color:Number=0xCCCCCC) {
      referencia_home = obj_home;
      objeto_text_field = obj_text_field;
      var number_position_x:Number = objeto_text_field.x + objeto_text_field.width ;
      objeto_text_field.width -= 10;
      var number_position_y:Number = objeto_text_field.y;
      var num_height:Number = Math.floor(objeto_text_field.height / objeto_text_field.maxScrollV);
      if(num_height < 20){
        num_height = 20;
      }
      round_square_trackbar = new Shape();
      round_square_trackbar.graphics.lineStyle(0, num_color, 0, false);
      round_square_trackbar.graphics.beginFill(num_color);
      round_square_trackbar.graphics.drawRoundRect(number_position_x, number_position_y, num_width, num_height, 10, 10); round_square_trackbar.graphics.endFill();
      round_square_trackbar.alpha = num_alpha;
      referencia_home.addChild(round_square_trackbar);
      objeto_text_field.addEventListener(Event.SCROLL, handler_scroll);
    }
    // ——- Properties ——-
    private var referencia_home:MovieClip;
    private var objeto_text_field:TextField;
    private var round_square_trackbar:Shape;
    // ——- Methods ——-
    private function handler_scroll(event:Event):void{
      // hago el indice actual basados en cero
      var number_actual:Number = objeto_text_field.scrollV – 1;
      var number_total:Number = objeto_text_field.maxScrollV – 1;
      round_square_trackbar.y = ((number_actual) / (number_total) * objeto_text_field.height) – (number_actual / number_total * round_square_trackbar.height);
    }
  }
}
```

En fin espero que a alguien le sirva o ayude.

Saludos,<br />
Gorka
