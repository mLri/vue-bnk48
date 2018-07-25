<template>
    <div class="slides">
        <div :style="{ width: innerWidth + 'px', marginLeft: '-' + slideInnerMarginLeft + 'px' }" class="slides-inner">
            <Slide 
                v-for="(image, i) in images" :key="i" 
                :style="{ width: singleWidth + 'px' }" 
                :image="image.src">
            </Slide>
        </div>
        <div class="navigation">
            <span @click="prev">Prev</span>
            <span class="nav-number" 
                v-for="(num, i) in images" 
                :key="i"
                @click="goToIndex(i)">
                {{ i + 1 }}
            </span>
            <span @click="next">Next</span>
        </div>
    </div>
    
</template>

<script>
import Slide from '@/components/Slide'

export default {
    props: {
        images: {
            require: true,
            type: Array
        },
        itemSlide: {
            type: null,
            default: 1
        }
    },
    components: {
        Slide
    },
    data () {
        return {
            innerWidth: 0,
            singleWidth: 0,
            curentIndex: 0,
            windowWidth: 0,
            txt: ''
        }
    },
    watch: {
        // windowWidth(newHeight, oldHeight) {
        //     this.txt = `it changed to ${newHeight} from ${oldHeight}`;
        //     console.log('in watch')
        //     console.log('newWidth', newHeight)
        //     console.log('oldWidth', oldHeight)
        // }
    },
    mounted() {
        // this.$nextTick(() => {
        //     window.addEventListener('resize', () => {
        //         this.windowWidth = window.innerWidth
        //         console.log('in mounted')
        //     });
        // })
        this.$nextTick(() => {
            window.addEventListener('resize', () => {
                this.singleWidth = this.$el.clientWidth / this.itemSlide
                this.innerWidth = this.singleWidth * this.images.length
            });
        })
    },
    computed: {
        slideInnerMarginLeft(){
            return this.curentIndex * this.singleWidth
        }
    },
    created(){
        this.setVar()
    },
    methods: {
        setVar(){
            this.$nextTick(() => {
                console.log('clientWidth ->', this.$el.clientWidth)
                console.log(this.$el.clientWidth / this.itemSlide)
                let singleWidth = this.$el.clientWidth / this.itemSlide
                this.singleWidth = singleWidth
                this.innerWidth = singleWidth * this.images.length
            })
        },
        next(){
            if(this.curentIndex === this.images.length - 1)
                return
            this.curentIndex++
        },
        prev(){
            if(this.curentIndex === 0)
                return
            this.curentIndex--
        },
        goToIndex(index){
            this.curentIndex = index
        }
    }
    
}
</script>

<style scoped>
    .slides {
        overflow: hidden;
        text-align: center;
    }

    .slides-inner {
        transition: margin 0.6s ease-out;
    }

    .nav-number {
        margin: 0 5px;
        background-color: white;
        padding: 0 5px;
        border: 1px solid black;
        cursor: pointer;
    }
</style>