<template>
    <div class="container-fluid">
        <h1>The kiss of heaven</h1>
        <div class="row-fluid">
            <div>
                <menu1></menu1>
            </div>
            <div>
                <main1></main1>
            </div>     
        </div>    
    </div>
</template>

<script>
import Menu1 from "./menu/Menu1";
import homeMain from "./menu/homeMain";
export default {
    components: {
        menu1: Menu1,
        main1: homeMain,
    },
}
</script>

