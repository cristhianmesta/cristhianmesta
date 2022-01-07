<template>
  <article class="sobre-mi container">
      <section class="hero">
        <h1>Cristhian Mesta</h1>
        <p>
          En el 2011, empecé en el mundo del desarrollo de software. A largo de estos años he trabajado principalmente con tecnologías .NET y JavaScript, desarrollando aplicaciones tanto para plataformas web y desktop.
        </p>
        <p>
          Me he desempeñado en diferentes industrias como gobierno, investigación de mercados, banca y esporádicamente como freelancer.
        </p>
        <p>
          <b>Actualmente me encuentro trabajando desde casa.</b>🏠
        </p>
      </section>

      <section class="sobre-mi-section">
        <Experience :experiences="experiences" />
      </section>

      <section class="sobre-mi-section">
        <Studies :studies="studies" />
      </section>

      <section class="sobre-mi-section">
        <Tecnologies :tecnologies="tecnologies" />
      </section>

      <section class="sobre-mi-section">
        <Tools :tools="tools" />
      </section>    

      <section class="sobre-mi-section">
        <Hobbies :hobbies="hobbies" />
      </section>        

  </article>
</template>

<script>
import Hobbies from '~/components/sobre-mi/Hobbies.vue'
export default {
  components: { Hobbies },
 data(){
   return {
     experiences: [
       {
         period       : 'sept. 2021 - actualidad',
         position     : 'NET DEVELOPER SR',
         company      : 'Softtek',
         company_url  : 'https://www.softtek.com/',
         company_logo : '',
         location     : 'Lima, Perú'
       },
       {
         period       : 'ago. 2018 - ago. 2021',
         position     : 'JEFE DE PROGRAMACIÓN',
         company      : 'Ipsos Perú',
         company_url  : 'https://www.ipsos.com/es-pe',
         company_logo : '',
         location     : 'Lima, Perú'
       },
       {
         period       : 'mar. 2014 - jul. 2018',
         position     : 'PROGRAMADOR',
         company      : 'Ipsos Perú',
         company_url  : 'https://www.ipsos.com/es-pe',
         company_logo : '',
         location     : 'Lima, Perú'
       },
       {
         period       : 'jul 2011 - jun 2013',
         position     : 'DESARROLLADOR',
         company      : 'Municipalidad Provincial de Ferreñafe',
         company_url  : 'http://www.muniferrenafe.gob.pe/',
         company_logo : '',
         location     : 'Ferreñafe, Perú'
       }
     ],
     studies: [
       {
         year            : '2016',
         title           : 'VISUAL STUDIO DEVELOPER',
         institution     : 'Cibertec',
         institution_url : 'https://www.cibertec.edu.pe/',
         institution_logo: '',
       },
      {
         year            : '2013',
         title           : 'INGENIERO DE SISTEMAS',
         institution     : 'Universidad Nacional Pedro Ruiz Gallo',
         institution_url : 'http://www.unprg.edu.pe/',
         institution_logo: '',
       }
     ],
     tecnologies: [
       {
         section: '⚡Lenguajes',
         items: [
           { name : 'C#'        , image: 'logo_csharp.svg'},
           { name : 'VB.NET'    , image: 'logo_vbnet.svg'},
           { name : 'JavaScript', image: 'logo_javascript.svg'},
           { name : 'TypeScript', image: 'logo_typescript.svg'},
           { name : 'Python'    , image: 'logo_python.svg'},
           { name : 'SQL'       , image: 'logo_sql.svg'},
           { name : 'HTML'      , image: 'logo_html.svg'},
           { name : 'CSS'       , image: 'logo_css.svg'},
           { name : 'SASS'      , image: 'logo_sass.svg'}
         ]
       },
       {
         section: '📦 Frameworks',
         items: [
           { name : '.NET'          , image: 'logo_net.svg'},
           { name : '.NET Framework', image: 'logo_netframework.svg'},
           { name : 'Angular'       , image: 'logo_angular.svg'},
           { name : 'Vue'           , image: 'logo_vue.svg'},
           { name : 'Bootstrap'     , image: 'logo_bootstrap.svg'},
         ]
       },
       {
         section: '💻 Otros',
         items: [
           { name : 'SQL Server', image: 'logo_sqlserver.svg'},
           { name : 'MySql'     , image: 'logo_mysql.svg'},
           { name : 'Git'       , image: 'logo_git.svg'},
         ]
       }
     ],
     tools: [
       {
         section: '✨Favoritas',
         items: [
           { name : 'VS Code'         , image: 'logo_visualstudiocode.svg' },
           { name : 'Visual Studio'   , image: 'logo_visualstudio.svg' },
           { name : 'GitHub'          , image: 'logo_github.svg' },
           { name : 'Postman'         , image: 'logo_postman.svg' },
           { name : 'Notion'          , image: 'logo_notion.svg' },
         ]
       },
       {
         section: '🧰 Otras',
         items: [
           { name : 'Jira'          , image: 'logo_jira.svg' },
           { name : 'Bitbucket'     , image: 'logo_bitbucket.svg' },
           { name : 'Figma'         , image: 'logo_figma.svg' },
         ]
       },
     ],
     hobbies: [
         '🤓 Mi formación profesional continua.',
         '👨‍🍳 Un entusiasta de la buena cocina.',
         '📚 Lectura sobre diversos temas.',
         '🎨 El dibujo y la pintura',
         '🏃‍♂️ Realizar algo de deporte.',
         '🌱 Cuidar mis plantas.',
         '👪 Lo más importante, mi familia.',
     ]
   }
 },
 head() {
    return{
      title: 'Sobre mí | Cristhian Mesta',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Información sobre mi, mis estudios, experiencia, intereses.'
        }
      ],
    }
 },
}
</script>

<style lang="scss" scoped>

.sobre-mi{

  .sobre-mi-section{
    margin-bottom: 2rem;
  }
  
}
</style>