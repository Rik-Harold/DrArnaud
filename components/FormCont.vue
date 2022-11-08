<template>
    <div class="contpro">
         <Conpro >
        <template v-slot:date>
            <span>DOCTORAT (Ph.D)</span>
        </template>
        <template v-slot:annee>
            <span>2011</span>
        </template>
        <template v-slot:matiere>
            <span>EN HYDROLOGIE ET GESTION INTEGRÉE DES RESSOURCES EN EAU</span>
        </template>
        <template v-slot:mention>
            <span>(MENTION TRÈS HONORABLE AVEC FÉLICITATIONS DU JURY)</span>
        </template>
    </Conpro>

    <Conpro>
        <template v-slot:date>
            <span>MASTER</span>
        </template>
        <template v-slot:annee>
            <span>2006</span>
        </template>
        <template v-slot:matiere>
            <span>EN EAU ET ENVIRONNEMENT</span>
        </template>
        <template v-slot:mention>
            <span>(MENTION BIEN)</span>
        </template>
    </Conpro>

    <Conpro>
        <template v-slot:date>
            <span>DIPLÔME D’INGÉNIEUR AGRONOME</span>
        </template>
        <template v-slot:annee>
            <span>2004</span>
        </template>
        <template v-slot:matiere>
            <span>EN SPÉCIALITÉ HYDRAULIQUE, EAUX ET FÔRETS, GÉNIE <br> ET AMÉNAGEMENT RURAL</span>
        </template>
        <template v-slot:mention>
            <span>(TRÈS BIEN AVEC FÉLICITATIONS DU JURY)</span>
        </template>
    </Conpro>

    <Conpro>
        <template v-slot:date>
            <span >DIPLÔME D’ÉTUDES UNIVERSITAIRES DU PREMIER CYCLE  (DEUPC)</span>
        </template>
        <template v-slot:annee>
            <span>2001</span>
        </template>
        <template v-slot:matiere>
            <span>EN SCIENCES DE LA VIE ET DE LA TERRE</span>
        </template>
        <template v-slot:mention>
            <span>(MENTION BIEN)</span>
        </template>
    </Conpro>
    <Conpro>
        <template v-slot:date>
            <span>BACCALAURÉAT</span>
        </template>
        <template v-slot:annee>
            <span>1998</span>
        </template>
        <template v-slot:matiere>
            <span>SÉRIE « C » (MATHÉMATIQUES ET SCIENCES PHYSIQUES)</span>
        </template>
        <template v-slot:mention>
            <span>(MENTION BIEN)</span>
        </template>
    </Conpro>

  
    </div>
   

</template>

<script>
    import Conpro from './Conpro.vue';
    export default{
    name: "FormCont",
    components: { Conpro }
}
</script>

<style>
.contpro{
    width: auto;
}
</style>

