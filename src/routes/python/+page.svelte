<script>
    export let frameworks = [
        { name: "Django", description: "Framework web Python de alto nível que incentiva o desenvolvimento rápido.", link: "https://www.djangoproject.com/", image: "https://static.djangoproject.com/img/logos/django-logo-negative.png" },
       {name:   "CherryPy", description:"CherryPy é um framework web python, orientado a objetos herryPy permite que desenvolvedores criem aplicativos web da mesma forma que criariam qualquer outro programa Python orientado a objetos. ", link:"https://cherrypy.dev/", image:"https://cherrypy.dev/images/cherrypy.png"} ,
       { 
            name: "Bottle", 
            description: "Framework Python minimalista para a criação de aplicativos web simples e rápidos.", 
            link: "https://bottlepy.org/", 
            image: "https://avatars.githubusercontent.com/u/1019799?s=280&v=4"
        },
        { 
            name: "Kivy", 
            description: "Framework Python para o desenvolvimento de aplicações multitouch, com suporte a interfaces gráficas ricas e interativas.", 
            link: "https://kivy.org/", 
            image: "https://upload.wikimedia.org/wikipedia/commons/5/58/Kivy_logo.png"
        },
        { 
            name: "Flask", 
            description: "Microframework para Python, projetado para ser simples e fácil de usar, ideal para aplicativos menores e mais rápidos.", 
            link: "https://flask.palletsprojects.com/", 
            image: "https://www.twilio.com/content/dam/twilio-com/global/en/blog/legacy/2017/building-python-web-apps-with-flask-html/flask-oauth.png"
        }
    ];
  
  </script>
  
  <style>
    .framework-card {
        display: flex;
        align-items: center;
        border: 1px solid #ddd;
        border-radius: 12px;
        padding: 16px;
        margin: 16px 0;
        box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
        transition: transform 0.3s, box-shadow 0.3s;
        background-color: #fff;
    }
      .maior {
  font-size: 20px;
  
  
  
      }
  
  
    .framework-card:hover {
        transform: translateY(-6px);
        box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
    }
  
    .framework-image {
        width: 80px;
        height: 80px;
        margin-right: 16px;
    }
  
    .framework-title {
        font-size: 1.8rem;
        font-weight: bold;
        color: #34495e;
    }
  
    .framework-description {
        margin: 12px 0;
        color: #666;
        line-height: 1.5;
    }
  
    .framework-link {
        color: #196ac7;
        text-decoration: none;
        font-weight: bold;
    }
  
    .framework-link:hover {
        text-decoration: underline;
    }
  </style>
  
  <div class="container">
    
  
    {#each frameworks as framework}
        <div class="framework-card">
            <img class="framework-image" src={framework.image} alt={framework.name}>
            <div>
                <h2 class="framework-title">{framework.name}</h2>
                <p class="framework-description">{framework.description}</p>
                <a class="framework-link" href={framework.link} target="_blank">Saiba mais</a>
            </div>
        </div>
    {/each}
  </div>
  