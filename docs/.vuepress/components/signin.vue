<template>
    <div class="counter ">
        <h1>{{number}}</h1>

        <button class="va-btn va-btn-md va-btn-primary" @click = "increment">Increment</button>
        <button class="va-btn va-btn-md va-btn-primary" @click = "decrement">Decrement</button>
        <br>
        <va-button @click.native="showCustom">Open</va-button>
        <va-modal :width="width" :backdrop-clickable="backdropclickable" ref="customModal">
            <div slot="header" />
            <div slot="body" style="height:120px;text-align:center;">
                <img src="https://placekitten.com/300/120"/>
            </div>
            <div slot="footer">
                <div style="text-align: center;">
                    <va-button @click.native="$refs.customModal.close()">Woof</va-button>
                    <va-button type="primary" @click.native="$refs.customModal.close()">Meow</va-button>
                </div>
            </div>
        </va-modal>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                number: 0,
                loading: false,
                size: 'md',
                active: false,
                round: true,
                disabled: false,
                width: 600,
                backdropclickable: true

            }
        },
        methods:{
            increment(){
                if(this.number >= 0){
                    this.number++
                }
            },
            decrement(){
                if(this.number > 0){
                    this.number --
                }
            },
            showCustom () {
                    this.$refs.customModal.open()
                }

        }
    }
</script>
