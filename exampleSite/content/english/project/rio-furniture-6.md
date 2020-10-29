---
title: Espejo Alpha
description: el modelo más popular
image: "/images/s-l1600.jpg"
bg_image: "/images/espejos-de-maquillaje.jpg"
category: Professional
information:
- label: Dimensiones
  info: 60X80cm
- label: Precio
  info: 89€
- label: Materiales
  info: Madera y cristal
- label: Tiempo de elaboración
  info: 2 días
- label: 'Iluminación '
  info: LED
- label: Iluminación total
  info: 2000 lumens

---
## Espejo Modelo Alpha categoría profesional

Este espejo es el más versátil de la tienda, tiene dimensiones que se ajustan a prácticamente cualquier tocador y su pesjo ligero hace que podamos transportarlo con facilidad si hace falta.

Por estas características se convierte en una herramienta tanto para profesionales como amateurs del maquillaje, ya que te lo puedes llevar a trabajar en una boda y es lo suficientemente grande como para tenerlo en el baño o la mesa de tocador de la habitación.

[![](/images/boton.png)](https://espejosdemaquillaje.netlify.app/contact/ "Pedir")

#### Galería fotos del producto:

<!-- Portfolio Start -->
<section class="portfolio-work">
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <div class="block">
          <div class="portfolio-menu">
            <div class="btn-group btn-group-toggle justify-content-center" data-toggle="buttons">
              <label class="btn btn-sm btn-primary active">
                <input type="radio" name="shuffle-filter" value="all" checked="checked">{{ i18n "all" }}
              </label>
              {{ $categories := slice }}
              {{ range .Data.Pages }}
              {{ $categories = $categories | append .Params.Category }}
              {{ end }}
              {{ range ( $categories | uniq ) }}
              <label class="btn btn-sm btn-primary">
                <input type="radio" name="shuffle-filter" value="{{ . | urlize }}">{{ . | humanize }}
              </label>
              {{ end }}
            </div>
          </div>
          <div class="row shuffle-wrapper">
            {{ range .Data.Pages }}
            <div class="col-md-4 portfolio-item shuffle-item" data-groups="[&quot;{{ .Params.Category | urlize }}&quot;]">
              <img src="{{ .Params.Image | relURL }}" alt="{{ .Title }}">
              <div class="portfolio-hover">
                <div class="portfolio-content">
                  <a href="{{ .Params.Image | relURL }}" class="portfolio-popup"><i class="icon ion-search"></i></a>
                  <a class="h3" href="{{ .Permalink }}">{{ .Title }}</a>
                  <p>{{ .Params.Description }}</p>
                </div>
              </div>
            </div>
            {{ end }}
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
