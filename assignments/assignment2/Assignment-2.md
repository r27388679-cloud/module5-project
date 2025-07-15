<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Maquette Responsive Module 2</title>
  <link rel="stylesheet" href="css/style.css" />
</head>
<body>
  <h1>Maquette Responsive</h1>

  <div class="container">
    <section class="box box1">
      <div class="title">Poulet</div>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum sit amet.</p>
    </section>
    <section class="box box2">
      <div class="title">Bœuf</div>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt.</p>
    </section>
    <section class="box box3">
      <div class="title">Sushi</div>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur lobortis leo et.</p>
    </section>
  </div>
</body>
</html>

/* Reset et base */
*,
*::before,
*::after {
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  margin: 20px;
}

/* Container général */
.container {
  overflow: hidden; /* Pour clear floats */
}

/* Styles communs aux sections */
.box {
  position: relative;
  border: 1px solid black;
  padding: 40px 20px 20px 20px;
  margin-bottom: 20px;
  color: #000;
  min-height: 150px;
}

/* Titres positionnés en haut à droite */
.title {
  position: absolute;
  top: 5px;
  right: 5px;
  border: 1px solid black;
  padding: 5px 10px;
  font-weight: bold;
  font-size: 120%;
  color: white;
}

/* Couleurs des sections */
.box1 {
  background-color: #f9c74f; /* Jaune */
}
.box1 .title {
  background-color: #f9844a; /* Orange */
}

.box2 {
  background-color: #90be6d; /* Vert clair */
}
.box2 .title {
  background-color: #43aa8b; /* Vert foncé */
}

.box3 {
  background-color: #577590; /* Bleu */
  color: white;
}
.box3 .title {
  background-color: #277da1; /* Bleu foncé */
}

/* -------- Desktop - ≥992px --------- */
@media (min-width: 992px) {
  .box {
    float: left;
    width: 32%;
    margin-right: 2%;
  }
  /* Supprimer marge droite sur dernière box */
  .box3 {
    margin-right: 0;
  }
}

/* -------- Tablette 768px à 991px --------- */
@media (min-width: 768px) and (max-width: 991px) {
  .box1, .box2 {
    float: left;
    width: 48%;
    margin-right: 4%;
  }
  .box2 {
    margin-right: 0;
  }
  .box3 {
    float: none;
    width: 100%;
    margin-right: 0;
  }
}

/* -------- Mobile ≤ 767px --------- */
@media (max-width: 767px) {
  .box {
    float: none;
    width: 100%;
  }
}

/* Taille police relative */
body {
  font-size: 16px;
}
.title {
  font-size: 1.25rem; /* 25% plus grande que base */
}
.box p {
  font-size: 0.875rem; /* 75% de base */
  margin-top: 1em;
}

/* Espacement supplémentaire pour que texte ne chevauche pas le titre */
.box p {
  padding-top: 20px;
}
