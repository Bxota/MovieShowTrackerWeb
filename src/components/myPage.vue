<template>
    <div id="page">
        <div v-show="data == 'Download'" class="content-download">
            <div class="download-file disable">Download for Linux</div> 
            <div class="download-file">Download for Windows</div> 
            <div class="download-file disable">Download for MacOs</div> 
        </div>
        <div v-show="data == 'Accueil'" class="content-accueil">
            <img src="@/assets/img/ic_launcher-playstore.png" alt="logo"/>
        </div>
        <div v-show="data == 'Information'" class="content-information">
            <div>
                <p class="center"><strong>Movie&ShowTracker</strong></p>
                <p>
                    Tout projet vient avec la naissance d’une idée, d’un besoin. En ce qui nous concerne, c’est un besoin simple et situationnel ayant toute sa part de contrainte. Ne vous êtes-vous jamais retrouvé lors de discussions amicales à parler films ou bien séries et que certaines informations vous échappent ? Est-ce la date de parution ? le casting ? ou la plateforme qui le propose ? Movie&ShowTracker en est la solution.
                    <br/>
                    <br/>
                    MST est né d’un manque d’application relatives à ce sujet. Il y a des règles d’or qui ont été établi : simplicité et fiabilité. En effet cette application est 100% française ce qui évite le problème des différentes plateformes de streaming selon les pays. Un choix a aussi été pris pour ne pas établir de comptes utilisateurs, ce qui permet aux clients de ne pas s’engager et de rendre l’accessibilité encore plus importante. Cette idée de rendre les utilisateurs complètements anonymes est venu grâce à mes grands-parents, ils n’ont pas grandi avec cette technologie et elle leur est de rude épreuve. J’ai donc constaté que le fait d’aller à l’essentiel avec peu d’interactions possibles était une manière de rendre une application accessible à tous. Une inscription nécessite implicitement une adresse électronique, un pseudo, un mot de passe, etc. Tout cela nous est inutile. 
                    <br/>
                    <br/>
                    MST vous permet donc de rechercher un film ou une série, avoir ses infos et l’ajouter à deux listes possibles : « déjà vu » ou « à voir ». Simple.
                    Chronologiquement, nous avons établis les maquettes du projet, composé d’une application web simple, d’une application mobile. L’interface de type desktop permet uniquement de rechercher des contenus et voir leurs informations, alors que l’application mobile a la fonctionnalité de mettre dans les listes dites ci-dessus.
                    L’objectif de cette application n’est pas de gagner de l’argent mais de rendre service. En espérant qu’elle vous plaira.
                </p>
                <p class="center"><strong>Hubitech – Reemo</strong></p>
                <p>
                    En parallèle de mes cours au sein de l’école 89, je suis en alternance au sein de l’entreprise Hubitech, une entreprise spécialisée dans le cloud computing entre autres avec leur produit : Reemo. Leur service étant de type web, j’ai donc eu des missions de type interface web et de base de données.
                    En ce qui me concerne, je trouve l’expérience professionnelle beaucoup plus immersive et intéressante qu’un projet fictif, c’est donc pour cela que j’ai essayé de mettre au maximum en avant mes expériences professionnelles dans mon dossier.
                    Les modules traités au sein de mon entreprise sont les parties front et back end utilisateur web, les trois modules traitant de la base de données ainsi que la collaboration à un projet informatique. J’ai eu comme projet de faire un site de documentation, de refaire la partie support du site vitrine pour les parties front-end utilisateur. En ce qui concerne la partie back-end utilisateur, j’ai participé à une mission où le but était de mettre en place des routes d’appels API. En complément de tous ces projets/missions, nous utilisons des outils collaboratifs pour mener à bien à nos travaux, ce qui serai détaillé dans la partie « Collaborer à la gestion d’un projet informatique et à l’organisation de l’environnement de développement ».
                </p> 
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                data: "Accueil"
            }
        },
        mounted() {
            this.emitter.on("event", data => {
                this.data = data
            })
        },
    }
</script>

<style lang="stylus">
  @import '@/assets/page.styl'
</style>