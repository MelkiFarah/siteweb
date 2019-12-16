# siteweb
<!DOCTYPE html>
<html>
    <head>
<meta charset="utf-8">
<link rel="stylesheet" href="rev.css"/>
</head>
<body>
  <div></div>
    <header>
        <h1>This is a heading</h1>
    </header>
    <div class="clearfix">
            <nav>
            <div class="column menu">
              <h2>I.Introduction</h2>
              <ul>
                <li>1.Objectif ></li>
                <li>2.Déclaration</li>
                <li>3.Type des variables</li>
                <li>4.L’instruction d’affectation</li>
              </ul>
              <h2>II.Les structures de contrôle</h2>
              <ul>
                  <li>1.Objectif></li>
                  <li>2.Les structures de contrôle</li>
                  <li>3.Les structures itératives</li>
                  
                </ul>
                <h2>III.Les tableaux à une dimension </h2>
                <ul>
                    <li>1.Objectif></li>
                    <li>2.Définition</li>
                    <li>3.Exemple</li>
                  </ul>
            </div>
        </nav>
      
        <section>
            <div class="column content">
                    
              <h1 class="h">Introduction</h1>
    <p>L’objectif  de  ce  document  est  de  présenter  aux  étudiants  un  résumé  du  cours 
        algorithmique et structures de données.  
         
        Par la suite, une sélection d’exercices sera proposée. Les exercices sont choisis de sorte 
        à  aider  les  étudiants  à  développer  une  solution  algorithmique  qui  résout  un  problème 
        proposé.  
         
        Le document propose la solution de quelques exercices. La solution est destinée aux 
        étudiants qui n’ont pas pu assister à une séance de Travaux Dirigés (TD), elle permet de les 
        aider pour se rattraper…</p>
        <hr>
          <h2>CHAPITRE I</h2>
          <article>
  <h2>1.Objectif</h2>
<p>Maitriser les notions : variable, type et valeur.
</p>
<h2>2.Déclaration</h2>
<p>Un  programme  a  besoin  de  stocker  provisoirement  des  valeurs  (information).  Ces 
    valeurs  peuvent  être de plusieurs  types :  elles peuvent être des nombres, du texte,  etc. 
    Toujours est-il que dès que l’on a besoin de stocker une information dans un programme, 
    on utilise une variable. 
    Pour la schématiser, une variable est une boîte, repérée par une étiquette. Pour avoir 
    accès au contenu de la boîte, il suffit de la désigner par son étiquette.
    NB: Dans la mémoire vive de l’ordinateur, cette boîte et cette étiquette collée dessus 
    n’existent pas. Il y a plutôt un emplacement de mémoire, désigné par une adresse binaire. 
    La  compilation  d’un  langage  informatique  se  charge  de  nous  épargner  la  gestion 
    fastidieuse de ces emplacements mémoire et de leurs adresses. En affectant une étiquette 
    choisie par le programmeur pour chaque adresse binaire. 
    La première chose  à faire  avant de pouvoir  utiliser une variable est  de préparer son 
    emplacement mémoire : nous allons alors créer la boîte et lui coller une étiquette. Ceci se 
    fait (pour les variables globales) au début de l’algorithme, avant même les instructions 
    proprement dites. C’est ce qu’on appelle la déclaration des variables. </p>
    <h2>3.Type des variables</h2>
    <p>Pour créer une boîte (réserver un emplacement mémoire) nous devons préciser sa taille. 
        Elle  doit  correspondre  à  ce  que  l’on  voudra  mettre dedans.  Ça  sera  un gaspillage  de 
        mémoire de créer une boite plus grande par rapport à notre besoin. Et notre boite ne pourra 
        pas stocker l’information dont nous avons besoin si elle n’a pas une taille suffisante.
        C’est comme l’exemple de construire un château pour stocker un oiseau ou construire une petite 
        cage pour stocker un éléphant. </p>
        <h3>Types numériques classiques</h3>
        <table border="0">
            <tr>
              <td>Type Numérique</td>
              <td>Plage</td>
            </tr>
            <tr>
              <td>Byte(Octet)</td>
              <td>
              <span>0 à 255</span></td>
            </tr>
            <tr>
              <td>Entier Simple</td>
              <td>
              <span>-32 768 à 32 767</span></td>
            </tr>
            <tr>
              <td rowspan="3">Entier Long
              <p>Réel Simple</td>
              <td>
              <span>-2 147 483 648 à 2 147</span>
              <span>483 647</span></td>
            </tr>
            <tr>
              <td>
              <span>
              -3,40E38 à -1,40E-45 pour les valeurs négatives</span></td>
            </tr>
            <tr>
              <td>
              <span>
              1,40E-45 à 3,40E38 pour les valeurs positives
              </span></td>
            </tr>
            <tr>
              <td rowspan="2">Réel Double</td>
              <td>
              <span>
              1,79E308 à -4,94E-324 pour les valeurs négatives</span></td>
            </tr>
            <tr>
              <td>
              <span>4,94E-324 à 1,79E308 pour les valeurs positives</span></td>
            </tr>
          </table>
          <p>Question : Pourquoi ne pas  déclarer toutes  les variables numériques en réel  double? 
              (Réponse : pour éviter un gaspillage de mémoire réservée.) 
              Une déclaration algorithmique de variables aura ainsi cette forme : 
              Variable g en Entier Long 
              Variables PrixHT, TauxTVA, PrixTTC en Réel Simple</p>
              <h2>Types non numériques</h2>
              <p>Nos  boîtes peuvent contenir une  information  autre que des  nombres.  Sans cela, on 
                  serait un peu embêté dès que l’on devrait stocker un nom de famille, par exemple. 
                  On dispose donc du type alphanumérique (également appelé type caractère) : dans 
                  une variable de ce type, on  stocke des caractères, qu’il  s’agisse de lettres, de  signes de 
                  ponctuation, d’espaces, ou de chiffres.  
                  Une  série  de  caractères  forme  une  chaîne  de  caractères.  Et  une  telle  chaîne  de 
                  caractères est toujours  notée entre  guillemets. Comme 2010 peut  représenter le  nombre 
                  2010, ou la suite de caractères 2, 0, 1 et 0.  
                  Un autre type est le type booléen : on y stocke uniquement les valeurs logiques VRAI 
                  et FAUX.</p>
                  <h2>4. L’instruction d’affectation</h2>
                  <p>Comme nous l’avons déjà  présenté une variable permet  de stocker  une information, 
                      cette opération de stockage se fait à travers l’affectation, c’est-à-dire lui attribuer une 
                      valeur. En algorithmique, cette instruction se note avec le signe ←
                      Exemple : 
                      Variable Boite en Entier  
                      //Cette ligne permet de réserver un espace mémoire suffisant pour contenir un entier au 
                      //niveau de la déclaration notre boite est vide. 
                      Boite ←12
                      //Cette instruction affecte la valeur 12 dans notre boite
                      Boite ←20 
                      //Cette nouvelle instruction écrase l’ancienne valeur 12 et affecte la nouvelle valeur 20 
                      //dans notre boite.</p>
        </article>
        <h1>CHAPITRE II </h1>
        <article>
          <h2>1. Objectif</h2>
          <p>Définir, maitriser et manipuler les structures de contrôle.</p>
          <h2>2. Les structures de contrôle:</h2>
          <p>Il n’y a que deux formes possibles pour un test ; 
              L’instruction conditionnelle Si : 
              Si expression logique Alors  
                 Instructions 
              [Sinon  
              Instructions] 
              FinSi  
               Si l’expression logique (condition) prend la valeur vrai, le premier bloc d’instructions 
              est exécuté; si elle prend la valeur faux, le second bloc est exécuté (s’il est présent, sinon 
              rien). 
               
              Les conditionnelles emboîtées:  
              Si expression1(test1) Alors  
                Instructions 1 
              Sinon 
               Si expression2(test2) Alors 
                  Instructions 2 
                Sinon  
                  Instructions 3  
                FinSi  
              FinSi  
              On peut remplacer la suite de si par l’instruction selon (permet une facilité d’écriture) 
              Syntaxe: 
                selon <identificateur> 
                  (liste de) valeur(s): instructions 
                  (liste de) valeur(s): instructions  </p>
                  <h2>3. Les structures itératives</h2>
                  <p>La boucle pour:  
                      C’est  l’instruction pour  qui permet  de faire  des boucles  déterministes.  Il s’agit  de 
                      répéter une suite d’instructions un certain nombre de fois.  
                      Syntaxe:  
                        pour <var> de valinit à valfin [par <pas>]  faire 
                          Instructions à exécuter à chaque boucle 
                        Finpour  
                       
                      La boucle tant que:  
                      Syntaxe:  
                        initialisation des variables de condition  
                      Tantque expression logique est vraie(test) faire  
                        Instructions à exécuter à chaque boucle 
                         réaffectation des variables de condition  
                      FinTantque 
                       Fonction: signifie répéter une suite d’instructions tant que la condition est remplie 
                       
                      La boucle répéter…tantque…  
                      Syntaxe:  
                       répéter 
                          (ré)affectation des variables de condition  
                          Instructions à exécuter à chaque boucle 
                          Tantque  <expression logique est vraie>  
                       Fonction: les instructions sont exécutées au  moins une  fois et répétées  tant que  la 
                      condition est remplie. </p>
  
        </article>
        <h1>CHAPITRE III </h1>
        <article>
          <h2>1. Objectif</h2>
          <p>Maitriser la définition et la manipulation des tableaux à une dimension. 
              Maitriser les algorithmes de tri.</p>
              <h2>2. Définition </h2>
              <p>Un  tableau  est  une  variable  de  type  complexe,  elle  peut  être  définie  comme  un 
                  ensemble de variables (de type simple) de même types. Chaque cellule dans un tableau est 
                  considérée comme une variable (de type simple). On peut accéder à cette cellule à travers 
                  son indice.</p>
                  <h2>3. Exemple</h2>
                  <p>Soit un tableau Table de type entier et qui est composé de 10 éléments. 
                      Déclaration du tableau : 
                       
                        Types : 
                          Tab : Tableau[1..50] d’Entiers 
                        Variables : 
                        Table : Tab 
                         
                        //Pour affecter la valeur x à la cellule de Table d’indice k il suffit de faire 
                        Table[k]x 
                        //k est l’indice de la kième cellule de Table.</p>
                        <h2>4. Algorithmes de tri</h2>
                        <p>Trier  un tableau  c'est  le fait  d'organiser  l'ensemble  de  ses éléments  selon un  ordre 
                            déterminé. 
                            Les algorithmes de tri ne sont pas tous identiques. En effet, ils peuvent être différenciés 
                            par la  complexité algorithmique (fixer une borne supérieure  du nombre d'opérations  qui 
                            seront  nécessaires  pour  trier  un  ensemble  de  n  éléments),  les  ressources  nécessaires 
                            (notamment en termes d'espace mémoire utilisé) et le caractère stable (garder l'ordre relatif 
                            des quantités égales). </p>
        </article>
        <h1>CHAIPTRE III.2</h1>
        <article>
          <h2>1. Objectif</h2>
          <p>Maitriser la définition et la manipulation des tableaux à deux dimensions.</p>
          <h2>2. Définition</h2>
          <p>Une matrice est un tableau à deux dimensions. Chaque ligne d’une matrice est un 
              tableau à une dimension.</p>
              <h2>3. Exemple</h2>
              <p>Soit une matrice MaMatrice de type entier et qui est composé de 10 lignes et 10 
                  colonnes. 
                  Déclaration du tableau : 
                    Types : 
                      Tab : MaMatrice[1..50 ; 1..50] d’Entiers 
                    Variables : 
                   Table : Tab 
                     
                    //Pour affecter la valeur x à la cellule de la ligne l et la colonne c de la matrice 
                    // il suffit de faire 
                   Matrice[l][c] 
                   //l est l’indice de la lième ligne de MaMatrice. 
                    ////c est l’indice de la cième colonne de MaMatrice.</p>
        </article>
          </div>
        </section>
            
          </div>
        
          
<footer>
    <h1>Merci de visiter notre page</h1>
</footer>
</body>
</html>

