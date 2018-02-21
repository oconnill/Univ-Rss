<template>
    <div class="text-center animated zoomInDown" v-if="user.quote">
        <div class="col-sm-12">
            <div class="panel panel-default">
                <div class="panel-body">
                    <div>
                        <h4><b>" {{quote.quote}} "</b></h4>
                    </div>
                    <div>
                        <h5>-{{quote.author}}-</h5>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'quote',
        data() {
            return {}
        },
        computed: {
            quote() {
                return this.$store.state.quote
            },
            user() {
                return this.$store.state.user
            }
        }
    }

</script>

<style scoped>

    .panel-body{
        padding: 0px;
    }
    .panel {
        background-color:rgba(0, 0, 0, 0.2);
        color: white;
        border: none
    }
</style>