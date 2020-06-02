<template>
  <div>
    <b-field id="animationTwo">
      <b-input
        placeholder="Search for a specific movie"
        type="search"
        icon="magnify"
        icon-clickable
        @icon-click="searchIconClick"
      ></b-input>
    </b-field>
    <br />
    <div class="tile is-ancestor">
      <div class="tile is-vertical is-8">
        <div class="tile">
          <div class="tile is-parent is-vertical">
            <article id="animationOne" class="tile is-child notification is-warning">
              <p class="title">{{ MoviesIndex.movieOne.nome }}</p>
              <p class="subtitle">{{ MoviesIndex.movieOne.sinopse }}</p>
            </article>
            <article id="animationTwo" class="tile is-child notification is-warning">
              <p class="title">{{ MoviesIndex.movieTwo.nome }}</p>
              <p class="subtitle">{{ MoviesIndex.movieTwo.sinopse }}</p>
            </article>
          </div>
          <div class="tile is-parent">
            <article id="animationTwo" class="tile is-child notification is-warning">
              <p class="title">{{ MoviesIndex.movieThree.nome }}</p>
              <p class="subtitle">{{ MoviesIndex.movieThree.sinopse }}</p>
              <figure class="image is-4by3">
                <img src="https://bulma.io/images/placeholders/640x480.png" />
              </figure>
            </article>
          </div>
        </div>
        <div id="animationOne" class="tile is-parent">
          <article class="tile is-child notification is-warning">
            <p class="title">{{ MoviesIndex.movieFour.nome }}</p>
            <p class="subtitle">{{ MoviesIndex.movieFour.sinopse }}</p>
            <div class="content">
              <!-- Content -->
            </div>
          </article>
        </div>
      </div>
      <div id="animationOpacity" class="tile is-parent">
        <article class="tile is-child notification is-warning">
          <div class="content">
            <p class="title">{{ MoviesIndex.movieFive.nome }}</p>
            <p class="subtitle">{{ MoviesIndex.movieFive.sinopse }}</p>
            <figure class="image is-4by3">
              <img src="https://bulma.io/images/placeholders/640x480.png" />
            </figure>
            <div class="content">
              <!-- Content -->
            </div>
          </div>
        </article>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      listOfMovies: [
        {
          nome: "Um Sonho de Liberdade",
          ano: 1994,
          nota: 9.3,
          genero: "Drama",
          sinopse:
            "Two imprisoned men bond over a number of years, finding solace and eventual redemption through acts of common decency.",
          diretor: "Frank Darabont",
          atores: ["Bob Gunton", "Morgan Freeman", "Tim Robbins"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi3877612057?playlistId=tt0111161&ref_=tt_ov_vi"
        },
        {
          nome: "O Poderoso Chefão",
          ano: 1972,
          nota: 9.2,
          genero: "Crime",
          sinopse:
            "The aging patriarch of an organized crime dynasty transfers control of his clandestine empire to his reluctant son.",
          diretor: "Francis Ford Coppola",
          atores: ["James Caan", "Al Pacino", "Marlon Brando"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi1348706585?playlistId=tt0068646&ref_=tt_ov_vi"
        },
        {
          nome: "O Poderoso Chefão II",
          ano: 1974,
          nota: 9,
          genero: "Crime",
          sinopse:
            "The early life and career of Vito Corleone in 1920s New York City is portrayed, while his son, Michael, expands and tightens his grip on the family crime syndicate.",
          diretor: "Francis Ford Coppola",
          atores: ["Robert Duvall", "Robert De Niro", "Al Pacino"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi696162841?playlistId=tt0071562&ref_=tt_ov_vi"
        },
        {
          nome: "Batman: O Cavaleiro das Trevas",
          ano: 2008,
          nota: 9,
          genero: "Action",
          sinopse:
            "When the menace known as the Joker wreaks havoc and chaos on the people of Gotham, Batman must accept one of the greatest psychological and physical tests of his ability to fight injustice.",
          diretor: "Christopher Nolan",
          atores: ["Aaron Eckhart", "Heath Ledger", "Christian Bale"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi324468761?playlistId=tt0468569&ref_=tt_ov_vi"
        },
        {
          nome: "12 Homens e uma Sentença",
          ano: 1957,
          nota: 8.9,
          genero: "Crime",
          sinopse:
            "A jury holdout attempts to prevent a miscarriage of justice by forcing his colleagues to reconsider the evidence.",
          diretor: "Sidney Lumet",
          atores: ["Martin Balsam", "Lee J. Cobb", "Henry Fonda"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi3452609817?playlistId=tt0050083&ref_=tt_ov_vi"
        },
        {
          nome: "A Lista de Schindler",
          ano: 1993,
          nota: 8.9,
          genero: "Biography",
          sinopse:
            "In German-occupied Poland during World War II, industrialist",
          diretor: "Steven Spielberg",
          atores: ["Ben Kingsley", "Ralph Fiennes", "Liam Neeson"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi1158527769?playlistId=tt0108052&ref_=tt_ov_vi"
        },
        {
          nome: "O Senhor dos Anéis: O Retorno do Rei",
          ano: 2003,
          nota: 8.9,
          genero: "Adventure",
          sinopse:
            "Gandalf and Aragorn lead the World of Men against Sauron's army to draw his gaze from Frodo and Sam as they approach Mount Doom with the One Ring.",
          diretor: "Peter Jackson",
          atores: ["Ian McKellen", "Viggo Mortensen", "Elijah Wood"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi2073101337?playlistId=tt0167260&ref_=tt_ov_vi"
        },
        {
          nome: "Pulp Fiction: Tempo de Violência",
          ano: 1994,
          nota: 8.9,
          genero: "Crime",
          sinopse:
            "The lives of two mob hitmen, a boxer, a gangster and his wife, and a pair of diner bandits intertwine in four tales of violence and redemption.",
          diretor: "Quentin Tarantino",
          atores: ["Samuel L. Jackson", "Uma Thurman", "John Travolta"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi2620371481?playlistId=tt0110912&ref_=tt_ov_vi"
        },
        {
          nome: "Três Homens em Conflito",
          ano: 1966,
          nota: 8.8,
          genero: "Western",
          sinopse:
            "A bounty hunting scam joins two men in an uneasy alliance against a third in a race to find a fortune in gold buried in a remote cemetery.",
          diretor: "Sergio Leone",
          atores: ["Lee Van Cleef", "Eli Wallach", "Clint Eastwood"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi2789278233?playlistId=tt0060196&ref_=tt_ov_vi"
        },
        {
          nome: "O Senhor dos Anéis: A Sociedade do Anel",
          ano: 2001,
          nota: 8.8,
          genero: "Action",
          sinopse:
            "A meek Hobbit from the Shire and eight companions set out on a journey to destroy the powerful One Ring and save Middle-earth from the Dark Lord Sauron.",
          diretor: "Peter Jackson",
          atores: ["Orlando Bloom", "Ian McKellen", "Elijah Wood"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi2073101337?playlistId=tt0120737&ref_=tt_ov_vi"
        },
        {
          nome: "Clube da Luta",
          ano: 1999,
          nota: 8.8,
          genero: "Drama",
          sinopse:
            "An insomniac office worker and a devil-may-care soapmaker form an underground fight club that evolves into something much, much more.",
          diretor: "David Fincher",
          atores: ["Meat Loaf", "Edward Norton", "Brad Pitt"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi781228825?playlistId=tt0137523&ref_=tt_ov_vi"
        },
        {
          nome: "Forrest Gump: O Contador de Histórias",
          ano: 1994,
          nota: 8.8,
          genero: "Drama",
          sinopse:
            "The presidencies of Kennedy and Johnson, the events of Vietnam, Watergate and other historical events unfold through the perspective of an Alabama man with an IQ of 75, whose only desire is to be reunited with his childhood sweetheart.",
          diretor: "Robert Zemeckis",
          atores: ["Gary Sinise", "Robin Wright", "Tom Hanks"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi3567517977?playlistId=tt0109830&ref_=tt_ov_vi"
        },
        {
          nome: "A Origem",
          ano: 2010,
          nota: 8.8,
          genero: "Action",
          sinopse:
            "A thief who steals corporate secrets through the use of dream-sharing technology is given the inverse task of planting an idea into the mind of a C.E.O.",
          diretor: "Christopher Nolan",
          atores: ["Ellen Page", "Joseph Gordon-Levitt", "Leonardo DiCaprio"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi4219471385?playlistId=tt1375666&ref_=tt_ov_vi"
        },
        {
          nome: "Star Wars, Episódio V: O Império Contra-Ataca",
          ano: 1980,
          nota: 8.7,
          genero: "Action",
          sinopse:
            "After the Rebels are brutally overpowered by the Empire on the ice planet Hoth, Luke Skywalker begins Jedi training with Yoda, while his friends are pursued by Darth Vader and a bounty hunter named Boba Fett all over the galaxy.",
          diretor: "Irvin Kershner",
          atores: ["Carrie Fisher", "Harrison Ford", "Mark Hamill"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi221753881?playlistId=tt0080684&ref_=tt_ov_vi"
        },
        {
          nome: "O Senhor dos Anéis: As Duas Torres",
          ano: 2002,
          nota: 8.7,
          genero: "Adventure",
          sinopse:
            "While Frodo and Sam edge closer to Mordor with the help of the shifty Gollum, the divided fellowship makes a stand against Sauron's new ally, Saruman, and his hordes of Isengard.",
          diretor: "Peter Jackson",
          atores: ["Viggo Mortensen", "Ian McKellen", "Elijah Wood"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi2073101337?playlistId=tt0167261&ref_=tt_ov_vi"
        },
        {
          nome: "Matrix",
          ano: 1999,
          nota: 8.7,
          genero: "Action",
          sinopse:
            "A computer hacker learns from mysterious rebels about the true nature of his reality and his role in the war against its controllers.",
          diretor: "Lana Wachowski",
          atores: ["Carrie-Anne Moss", "Laurence Fishburne", "Keanu Reeves"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi1032782617?playlistId=tt0133093&ref_=tt_ov_vi"
        },
        {
          nome: "Os Bons Companheiros",
          ano: 1990,
          nota: 8.7,
          genero: "Biography",
          sinopse: "The story of",
          diretor: "Martin Scorsese",
          atores: ["Joe Pesci", "Ray Liotta", "Robert De Niro"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi2673654553?playlistId=tt0099685&ref_=tt_ov_vi"
        },
        {
          nome: "Um Estranho no Ninho",
          ano: 1975,
          nota: 8.7,
          genero: "Drama",
          sinopse:
            "A criminal pleads insanity and is admitted to a mental institution, where he rebels against the oppressive nurse and rallies up the scared patients.",
          diretor: "Milos Forman",
          atores: ["Will Sampson", "Louise Fletcher", "Jack Nicholson"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi3943282969?playlistId=tt0073486&ref_=tt_ov_vi"
        },
        {
          nome: "Os Sete Samurais",
          ano: 1954,
          nota: 8.6,
          genero: "Action",
          sinopse:
            "A poor village under attack by bandits recruits seven unemployed samurai to help them defend themselves.",
          diretor: "Akira Kurosawa",
          atores: ["Keiko Tsushima", "Takashi Shimura", "Toshirô Mifune"],
          linkTrailer: "https://www.imdb.comundefined"
        },
        {
          nome: "Seven: Os Sete Crimes Capitais",
          ano: 1995,
          nota: 8.6,
          genero: "Crime",
          sinopse:
            "Two detectives, a rookie and a veteran, hunt a serial killer who uses the seven deadly sins as his motives.",
          diretor: "David Fincher",
          atores: ["Kevin Spacey", "Brad Pitt", "Morgan Freeman"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi2508831257?playlistId=tt0114369&ref_=tt_ov_vi"
        },
        {
          nome: "A Vida é Bela",
          ano: 1997,
          nota: 8.6,
          genero: "Comedy",
          sinopse:
            "When an open-minded Jewish librarian and his son become victims of the Holocaust, he uses a perfect mixture of will, humor, and imagination to protect his son from the dangers around their camp.",
          diretor: "Roberto Benigni",
          atores: ["Giorgio Cantarini", "Nicoletta Braschi", "Roberto Benigni"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi2332801561?playlistId=tt0118799&ref_=tt_ov_vi"
        },
        {
          nome: "Cidade de Deus",
          ano: 2002,
          nota: 8.6,
          genero: "Crime",
          sinopse:
            "In the slums of Rio, two kids' paths diverge as one struggles to become a photographer and the other a kingpin.",
          diretor: "Fernando Meirelles",
          atores: [
            "Matheus Nachtergaele",
            "Leandro Firmino",
            "Alexandre Rodrigues"
          ],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi1783208985?playlistId=tt0317248&ref_=tt_ov_vi"
        },
        {
          nome: "O Silêncio dos Inocentes",
          ano: 1991,
          nota: 8.6,
          genero: "Crime",
          sinopse:
            "A young F.B.I. cadet must receive the help of an incarcerated and manipulative cannibal killer to help catch another serial killer, a madman who skins his victims.",
          diretor: "Jonathan Demme",
          atores: ["Lawrence A. Bonney", "Anthony Hopkins", "Jodie Foster"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi3377380121?playlistId=tt0102926&ref_=tt_ov_vi"
        },
        {
          nome: "A Felicidade Não se Compra",
          ano: 1946,
          nota: 8.6,
          genero: "Drama",
          sinopse:
            "An angel is sent from Heaven to help a desperately frustrated businessman by showing him what life would have been like if he had never existed.",
          diretor: "Frank Capra",
          atores: ["Lionel Barrymore", "Donna Reed", "James Stewart"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi1101988121?playlistId=tt0038650&ref_=tt_ov_vi"
        },
        {
          nome: "Guerra nas Estrelas",
          ano: 1977,
          nota: 8.6,
          genero: "Action",
          sinopse:
            "Luke Skywalker joins forces with a Jedi Knight, a cocky pilot, a Wookiee and two droids to save the galaxy from the Empire's world-destroying battle station, while also attempting to rescue Princess Leia from the mysterious Darth Vader.",
          diretor: "George Lucas",
          atores: ["Carrie Fisher", "Harrison Ford", "Mark Hamill"],
          linkTrailer:
            "https://www.imdb.com/video/imdb/vi1317709849?playlistId=tt0076759&ref_=tt_ov_vi"
        }
      ],
      MoviesIndex: {
        movieOne: null,
        movieTwo: null,
        movieThree: null,
        movieFour: null,
        movieFive: null
      }
    };
  },
  methods: {},
  created() {
    this.MoviesIndex.movieOne = this.listOfMovies[
      Math.floor(Math.random() * this.listOfMovies.length)
    ];
    this.MoviesIndex.movieTwo = this.listOfMovies[
      Math.floor(Math.random() * this.listOfMovies.length)
    ];
    this.MoviesIndex.movieThree = this.listOfMovies[
      Math.floor(Math.random() * this.listOfMovies.length)
    ];
    this.MoviesIndex.movieFour = this.listOfMovies[
      Math.floor(Math.random() * this.listOfMovies.length)
    ];
    this.MoviesIndex.movieFive = this.listOfMovies[
      Math.floor(Math.random() * this.listOfMovies.length)
    ];
  }
};
</script>
<style>
#animationOne {
  animation-name: ItemsOne;
  animation-duration: 3s;
}

@keyframes ItemsOne {
  0% {
    right: 500px;
  }
  100% {
    right: 0px;
  }
}
#animationOpacity {
  animation-name: ItemsOne;
  animation-duration: 3s;
}

@keyframes ItemsOne {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
#animationTwo {
  animation-name: ItemsTwo;
  animation-duration: 2s;
}

@keyframes ItemsTwo {
  0% {
    top: 500px;
  }

  55% {
    top: 0px;
  }
}
</style>