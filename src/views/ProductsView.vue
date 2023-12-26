<template>
   <Table />
</template>


<script>
import Table from '../components/Table.vue'


export default {
    name:'Products',

    components:{
        Table,
    },
    created(){
        this.getProductos()
    },
    methods:{
        getProductos: async function(){
            try {
                const setting= {
                    method: 'GET',
                }
                const url =  'http://localhost:3000/api';
                const data =await fetch(url, setting);
                const json =await data.json();
                console.log(json)
            } catch (error) {
                
            }
        }
    }

}
</script>
