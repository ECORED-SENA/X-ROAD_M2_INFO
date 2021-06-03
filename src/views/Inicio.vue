<template lang="pug">
section
  BannerPrincipal.mb-5

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 1. Presentación

    p El programa Configurar Escenario de Interoperabilidad mediante X-ROAD, introducirá a los participantes en el diseño e implementación de escenarios de interoperabilidad entre diferentes tipos de sistemas de información y conocimiento, con el propósito de facilitar la entrega de servicios digitales a ciudadanos, empresas y otras entidades. Todo esto, a través, del intercambio de datos entre sus sistemas TIC y los elementos y características de la plataforma X-ROAD, que permitirá brindar una solución de software en un escenario común de interoperabilidad.

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
        
    .titulo__template--a.mb-4
      span.h6 2. Justificación<br>del programa
  
    .row
      .col-12.col-md-8.col-lg-9
        p.mb-4 El programa Configurar Escenario de Interoperabilidad mediante X-ROAD, introducirá a los participantes en el diseño e implementación de escenarios de interoperabilidad entre diferentes tipos de sistemas de información y conocimiento, con el propósito de facilitar la entrega de servicios digitales a ciudadanos, empresas y otras entidades. Todo esto, a través, del intercambio de datos entre sus sistemas TIC y los elementos y características de la plataforma X-ROAD, que permitirá brindar una solución de software en un escenario común de interoperabilidad.

        p Es así como el SENA, a través de la formación que imparte, permite mantener actualizado el recurso humano con las competencias técnicas y sociales que permiten impactar al sector productivo positivamente, suministrando el conocimiento requerido para el cumplimiento de los planes de Gobierno Nacional a través del programa Configurar escenario de interoperabilidad mediante X-ROAD

      .col-4.col-lg-3.d-none.d-md-block
        figure
          img(src='@/assets/curso/05.png', alt='X-Road mintic')    


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 3. Competencias<br>a desarrollar

    p  
      span.colorText01
        strong • 
      | Operar herramientas informáticas y digitales de acuerdo con protocolos y manuales técnicos.
  
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 4. Perfil<br>de ingreso
    
    p.mb-4 El público objetivo deberá corresponder a los funcionarios públicos del país (funcionarios y contratistas), los cuales estarán principalmente priorizados por:
    
    ul.lista-ul
      li.d-flex  
        i.fas.fa-angle-right
        | Servidores Públicos (Funcionarios y Contratistas). 
      li.d-flex  
        i.fas.fa-angle-right
        | CIOs, Lideres TI, Servidores de oficinas TI. 
      li.d-flex  
        i.fas.fa-angle-right
        | Personas que han manifestado el desarrollo de proyectos TI bajo el enfoque de interoperabilidad. 
      li.d-flex  
        i.fas.fa-angle-right
        | Priorizar servidores del ente Territorial sobre ente Nacional de Bogotá. 
      li.d-flex  
        i.fas.fa-angle-right
        | Priorizar funcionarios sobre contratistas.

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 5. Estrategia<br>metodológica

    p.mb-4 Centrada en la construcción de autonomía para garantizar la calidad de los procesos formativos   en el marco de la formación por competencias, el aprendizaje por proyectos y el  uso de  técnicas didácticas activas que estimulan el pensamiento para la resolución de problemas simulados y reales; soportadas en el utilización de las tecnologías de la información y la comunicación, integradas, en ambientes abiertos y pluri tecnológicos, que en todo caso recrean el contexto productivo y vinculan al aprendiz con la realidad cotidiana y el desarrollo de las competencias.

    p.mb-4 Igualmente, debe estimular de manera permanente la autocrítica y la reflexión del aprendiz sobre el que hacer y los resultados de aprendizaje que logra a través de la vinculación activa de las cuatro fuentes de información para la construcción de conocimiento.

    .row.g-4.justify-content-center
      .col-5.col-sm-3.col-md-2
        figure.mb-2
          img.w-75.mx-auto(src='@/assets/curso/01.svg', alt='El instructor - tutor')
        p.text-center
          strong El instructor - tutor
      .col-5.col-sm-3.col-md-2
        figure.mb-2
          img.w-75.mx-auto(src='@/assets/curso/02.svg', alt='El instructor - tutor')
        p.text-center
          strong El entorno
      .col-5.col-sm-3.col-md-2
        figure.mb-2
          img.w-75.mx-auto(src='@/assets/curso/03.svg', alt='El instructor - tutor')
        p.text-center
          strong Las TIC

  //- Créditos
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 Créditos

    CreditosComp

  Footer
  

</template>
<script>
import { menuPrincipal } from '../config/global'
import BannerPrincipal from '../components/plantilla/BannerPrincipal'
import CreditosComp from '../components/plantilla/CreditosComp'
import Footer from '../components/plantilla/Footer'
export default {
  name: 'Inicio',
  components: {
    BannerPrincipal,
    CreditosComp,
    Footer,
  },
  data: () => ({
    menuPrincipalData: menuPrincipal,
  }),
  computed: {
    desarrolloContenidosData() {
      const allMenuData = [
        ...this.menuPrincipalData.menu,
        ...this.menuPrincipalData.subMenu,
      ]
      return allMenuData.filter(item => item.desarrolloContenidos)
    },
  },
}
</script>
