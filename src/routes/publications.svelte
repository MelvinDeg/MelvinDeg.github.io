<script>
    import { fly, fade, slide, draw } from "svelte/transition";
    import { quintOut } from 'svelte/easing';
    import {currentPage} from "$lib/components/stores.js"
    $currentPage = "publications"
</script>

<svelte:head>
    <title>Publications</title>
</svelte:head>

<div class="container w-11/12 lg:3/4 text-center mb-40">

    <p class="my-6">The full list of publications can be found at <a class="underline decoration-blue-600 " href="https://www.umu.se/en/staff/sofie-degerman/">https://www.umu.se/en/staff/sofie-degerman/</a>  
    </p>

    <h1 class="underline text-xl italic font-bold ">Ten selected publications</h1>

    <ul class="text-left">

        <li in:slide="{{delay: 250, duration: 600, easing: quintOut }}" out:fade><span>“Aging of preleukemic thymocytes drives CpG island hypermethylation in T-cell acute lymphoblastic leukemia”</span>, Roels J*, Thénoz M*, Szarzyńska-Zawadzka B, Landfors M, De Coninck S, Demoen L, Provez L, Kuchmiy A, Strubbe S, Reunes L, Pieters T, Matthijssens P, Van Loocke W, Erarslan‐Uysa B, Richter-Pechańska P, Declerck K, Lammens T, De Moerloose B, Deforce D, Van Nieuwerburgh F, C Cheung L, S Kotecha R, Mansour MR, Ghesquière B, Van Camp G, Vanden Berghe W, Kowalczyk JR, Szczepański T, Davé UP, Kulozik AE, Goossens S, Curtis DJ, Taghon T, Dawidowska M, Degerman  S and Van Vlierberghe P.  Blood Cancer Discov. 2020 Nov;1(3):274-289. <a class="underline decoration-blue-600" href="https://doi.org/10.1182/blood-2020-138501" target="_blank">https://doi.org/10.1182/blood-2020-138501</a></li>
        <li in:slide="{{delay: 250, duration: 600, easing: quintOut }}" out:fade><span>“DNA methylation and copy number variation profiling of T-cell lymphoblastic leukemia and lymphoma”</span>, Haider Z, Landfors M, Golovleva I, Erlanson M , Schmiegelow K, Flaegstad T, Kanerva J, Noren-Nyström U, Hultdin M and Degerman S. Blood Cancer J. 2020 Apr 28;10(4):45. <a class="underline decoration-blue-600" href="https://doi.org/10.1038/s41408-020-0310-9" target="__blank">https://doi.org/10.1038/s41408-020-0310-9</a> </li>
        <li in:slide="{{delay: 250, duration: 600, easing: quintOut }}" out:fade><span>“Cell-of-origin determined by both gene expression profiling and immunohistochemistry is the strongest predictor of survival in patients with diffuse large B-cell lymphoma”</span>.Abdulla M, Hollander P, Pandzic T, Mansouri L, Ednersson SB, Andersson PO, Hultdin M, Fors M, Erlanson M, Degerman S, Petersen HM, Asmar F, Grønbaek K, Enblad G, Cavelier L, Rosenquist R, Amini RM. Am J Hematol. 2020 Jan;95(1):57-67.  <a href="https://doi.org/10.1002/ajh.25666" class="underline decoration-blue-600" target="_blank">https://doi.org/10.1002/ajh.25666</a>  </li>
        <li in:slide="{{delay: 250, duration: 600, easing: quintOut }}" out:fade><span>“An integrated transcriptome analysis in T-cell acute lymphoblastic leukemia links DNA methylation subgroups to dysregulated TAL1 and ANTP homeobox gene expression.”</span> Haider Z, Landfors M, Larsson P, Köhn L, Schmiegelow K, Flaegstad T, Kanerva J, Heyman M, Hultdin M and Degerman S, 2019, Cancer medicine, 8(1), pp. 311-324. I  <a href="https://doi.org/10.1002/cam4.1917" class="underline decoration-blue-600" target="_blank">https://doi.org/10.1002/cam4.1917</a></li>
        <li in:slide="{{delay: 250, duration: 600, easing: quintOut }}" out:fade><span>“DNA methylation holds prognostic information in relapsed precursor B-cell acute lymphoblastic leukemia"</span>, Borssén M, Nordlund J, Haider Z, Landfors M, Larsson P, Norén-Nyström U, Schmiegelow K, Åsberg AE, Kanerva J, Palle J, Frost BM, Forestier E, Heyman M,  Hultdin M, Lönnerholm G, and Degerman S,  Clinical Epigenetics, 2018, Mar 5;10:31. <a href="https://doi.org/10.1186/s13148-018-0466-3" class="underline decoration-blue-600" target="_blank">https://doi.org/10.1186/s13148-018-0466-3</a> </li>
        <li in:slide="{{delay: 250, duration: 600, easing: quintOut }}" out:fade><span>“DNA methylation adds prognostic value to minimal residual disease status in pediatric T-cell acute lymphoblastic leukemia.”</span>, Borssén M *, Haider Z*, Landfors M, Hultdin M, Norén Nyström U, Schmiegelow K, Åsberg A E, Kanerva J, Madsen H O, Heyman M, Roos G, Forestier E, and Degerman S. *contributed equally. Pediatr Blood Cancer. 2016 Feb 29. <a href="https://doi.org/10.1002/pbc.25958" class="underline decoration-blue-600" target="_blank">https://doi.org/10.1002/pbc.25958</a>  </li>
        <li in:slide="{{delay: 250, duration: 600, easing: quintOut }}" out:fade><span>"Combining epigenetic and clinicopathological variables improves specificity in prognostic prediction in clear cell renal cell carcinoma”</span> Andersson-Evelönn E, Vidman*L, Källberg D, Landfors M, Liu X, Ljungberg B, Hultdin M, Rydén P*, Degerman S*. ", *contributed equally, J Transl Med. 2020 Nov 13;18(1):435. <a href="https://doi.org/10.1186/s12967-020-02608-1" class="underline decoration-blue-600" target="_blank">https://doi.org/10.1186/s12967-020-02608-1</a> </li>
        <li in:slide="{{delay: 250, duration: 600, easing: quintOut }}" out:fade><span>“Immortalization of T-cells is accompanied by gradual changes in CpG methylation resulting in a profile resembling a subset of T-cell leukemias.”</span>, Degerman S, Landfors M, Siwicki JK, Revie J, Borssén M, Andersson E, Forestier E, Chrzanowska KH, Ryden P, Keith WN and Roos G.  Neoplasia. 2014 Jul;16(7):606-15. <a href="https://doi.org/10.1016/j.neo.2014.07.001" class="underline decoration-blue-600" target="_blank">https://doi.org/10.1016/j.neo.2014.07.001</a></li>
        <li in:slide="{{delay: 250, duration: 600, easing: quintOut }}" out:fade><span>“Prognostic implications of mutations in NOTCH1 and FBXW7 in childhood T-ALL treated according to the NOPHO ALL-1992 and ALL-2000 protocols.”</span> Fogelstrand L, Staffas A, Wasslavik C, Sjögren H, Söderhäll S, Frost BM, Forestier E, Degerman S, Behrendtz M, Heldrup J, Karrman K, Johansson B, Heyman M, Abrahamsson J, Palmqvist L., , Pediatr Blood Cancer. 2014 Mar;61(3):424-30. <a href="https://doi.org/10.1002/pbc.24803" class="underline decoration-blue-600" target="_blank">https://doi.org/10.1002/pbc.24803</a>  </li>
        <li in:slide="{{delay: 250, duration: 600, easing: quintOut }}" out:fade><span>“Promoter DNA methylation pattern identifies prognostic subgroups of childhood T-ALL”</span>, Borssen M, Palmqvist L, Karrman K, Abrahamsson J, Behrendtz M, Heldrup J, Forestier R, Roos G and Degerman S., PLoS One. 2013 Jun 6;8(6):e65373. <a href="https://doi.org/10.1371/journal.pone.0065373" class="underline decoration-blue-600" target="__blank">https://doi.org/10.1371/journal.pone.0065373</a> </li>
    </ul>


</div>

<style>
    ul > li{
        margin: 20px 0; 
        border-width: 1px;
        border-radius: 10px;
        border-color: black;
        padding: 15px;
        box-shadow: 2px 2px 2px grey;
        overflow: hidden;
    }
    span {
        font-weight: 800;
    }

    .container {
        margin-bottom: 75px;
        margin-top: 100px;
    }


</style>