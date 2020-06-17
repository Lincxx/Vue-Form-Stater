<template>
    <div>
        <app-header/>
        <div class="container">
           <form>
               <div class="row">
                   <div class="col-xs-12">
                        <h1>Contact us</h1>
                        <hr>

                        <div class="form-group">
                            <label for="name">Name</label>
                            <input 
                                type="text" 
                                id="name"
                                class="form-control"  
                            >     
                        </div>

                   </div>
               </div>
           </form>
        </div>
        <app-footer/>
    </div>
</template>

<script>
    export default {
        data(){
            return {
                countries:[
                    'EEUU',
                    'India',
                    'UK',
                    'Russia'
                ],
                formdata:{
                    name:'',
                    lastname:'',
                    subject:'',
                    message:'Some default content',
                    extras:[],
                    gender:'alien',
                    country:'India'
                }
            }
        },
        methods:{
            submitForm(){
                console.log(this.formdata);
                console.log(JSON.stringify(this.formdata))
            }
        }
    }
</script>


<style>
    body {
        padding:0;
        margin:0;
        font-family: 'Roboto', sans-serif;
    }

    .container {
        min-height: 84vh;
        box-sizing: border-box;
        padding: 20px;
    }



</style>