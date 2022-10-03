<template>
    <div class="hero">
        <!-- Desktop -->
        <div class="d-none d-md-block">
            <div class="row mt-4 mb-2">
                <div class="col-md">
                    <div class="d-flex h-100">
                        <div class="justify-content-center align-self-center">
                            <h2><strong>Readily Available</strong> <br />Shopping Made Easy!</h2>
                            <p>Do your groceries from the palm of your hands</p>
                            <button class="btn btn-lg btn-primary">
                                <b-icon-arrow-right></b-icon-arrow-right> Order
                            </button>
                        </div>
                    </div>
                </div>
                <div class="col-md">
                    <img src="@/assets/images/undraw_shopping_app_flsj.png" alt="@/assets/images/default.png"
                        width="100%">
                </div>
            </div>
        </div>


        <!-- Mobile -->
        <div class="d-sm-block d-md-none">
            <div class="row mt-4 mb-2">
                <div class="col-md mb-3">
                    <img src="@/assets/images/undraw_shopping_app_flsj.png" alt="@/assets/images/default.png"
                        width="100%">
                </div>
                <div class="col-md">
                    <div class="d-flex h-100">
                        <div class="justify-content-center align-self-center">
                            <h2><strong>Readily Available</strong> <br />Shopping Made Easy!</h2>
                            <p>Groceries from the palm of your hands</p>
                            <button class="btn btn-lg btn-primary">
                                <b-icon-arrow-right></b-icon-arrow-right> Order
                            </button>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </div>

</template>

<script>
export default {
    name: 'HeroBanner'
}
</script>

<style>

</style>