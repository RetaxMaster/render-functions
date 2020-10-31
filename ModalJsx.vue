<script>
export default {

    name: "ModalJsx",

    props: {

        show: {
            type: Boolean,
            default: false,
        },

    },

    render() {
        return (this.show) ? <div class="modal">
            <p>{this.$slots.default}</p>
            <button onClick={this.clickCancelHandler}>Cancelar</button>
            <button onClick={this.clickOkHandler}>Ok</button>
        </div> : null
    },

    methods: {

        clickCancelHandler() {
            console.log("Click on Cancel");
        },

        clickOkHandler() {
            console.log("Click on Ok");
        },

    }

}
</script>