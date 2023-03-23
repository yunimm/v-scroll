<template>
    <div class="hello">
        <h1>{{ msg }}</h1>
        <p>
            For a guide and recipes on how to configure / customize this
            project,<br />
            check out the
            <a href="https://cli.vuejs.org" target="_blank" rel="noopener"
                >vue-cli documentation</a
            >.
        </p>
        <h3>Installed CLI Plugins</h3>
        <!-- <button  type="button">刪除</button> -->
        <h1 class="debug">{{ this.y }}/{{ this.section }}</h1>
        <nav>
            <ul class="fixed">
                <li v-for="(item, index) in nav" :key="item.id">
                    <button
                        @click="click(index, item.yAxisHeight)"
                        :class="{
                            active: section === index,
                        }"
                        type="button"
                    >
                        {{ item.name }}
                    </button>
                </li>
            </ul>
        </nav>
        <div class="menu-wrapper">
            <div
                ref="listItems"
                v-for="item in nav"
                :key="item.id"
                :class="`section${item.id}`"
            >
                <h2>{{ `yAxisHeight:${item.yAxisHeight}` }}</h2>
                <h3>{{ item.name }}</h3>
                <p>
                    {{ item.text }}
                </p>
            </div>
        </div>
        <footer>
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Laboriosam excepturi repellat error fugiat alias debitis ipsam
                quaerat adipisci iure, repellendus sapiente veritatis ab
                consectetur saepe! Quam aspernatur veritatis accusantium in.
            </p>
        </footer>
    </div>
</template>

<script>
export default {
    name: 'HelloWorld',
    props: {
        msg: String,
    },
    data() {
        return {
            item_y: 0,
            y: 0,
            section: 0,
            active: 0,
            nav: [
                {
                    isScroll: false,
                    id: 0,
                    name: 'fruit',
                    text: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendis?Lorem ipsum dolor sit, aepellendus perspiciatis delectus opquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendisLorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendis?Lorem ipsum dolor sit, aepellendus perspiciatis delectus opquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendisLorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendis?Lorem ipsum dolor sit, aepellendus perspiciatis delectus opquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendisLorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendis?Lorem ipsum dolor sit, aepellendus perspiciatis delectus opquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendisLorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendis?Lorem ipsum dolor sit, aepellendus perspiciatis delectus opquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendisLorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendis?Lorem ipsum dolor sit, aepellendus perspiciatis delectus opquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendisLorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendis?Lorem ipsum dolor sit, aepellendus perspiciatis delectus opquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendisLorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendis?Lorem ipsum dolor sit, aepellendus perspiciatis delectus opquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendis',
                },
                {
                    isScroll: false,
                    id: 1,
                    name: 'tea',
                    text: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendis?Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendisLorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendisLorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendis?Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendisLorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendis',
                },
                {
                    isScroll: false,
                    id: 2,
                    name: 'drink',
                    text: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendis?Lorem ipsum dolor siterspiciatis delectus optio. In minima quam reiciendis?Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendisLorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat, maiores! Aliquid fugit nam sunt iusto! Ut commodi dolor error expedita dicta sed repellendus perspiciatis delectus optio. In minima quam reiciendis',
                },
            ],
        };
    },
    created() {
        window.addEventListener('scroll', this.handleScroll);
    },
    mounted() {
        this.addYData();
        // setTimeout(() => {
        //     this.nav.shift();
        // }, 1000);
    },
    methods: {
        handleScroll() {
            this.y = window.scrollY;
            this.calculateSection();
        },
        calculateSection() {
            this.nav.forEach((item, index) => {
                if (this.y >= item.yAxisHeight) {
                    this.section = index;
                }
            });
        },
        click(index, y) {
            this.addStyle(index);

            window.scrollTo({
                top: y + 160,
                behavior: 'smooth',
            });
        },
        addStyle(index) {
            this.active = index;
        },
        addYData() {
            if (this.$refs.listItems && this.$refs.listItems.length) {
                this.$refs.listItems.forEach((element, index) => {
                    const yAxisHeight = element.offsetTop;
                    this.$set(this.nav[index], 'yAxisHeight', yAxisHeight);
                    console.log(
                        `Item ${index + 1} 的 Y 軸高度：${yAxisHeight}`,
                    );
                });
            }
        },
    },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.debug {
    position: fixed;
    top: 0;
    left: 0;
    z-index: 9999;
}
h3 {
    margin: 40px 0 0;
}

button {
    color: #42b983;
    cursor: pointer;
}
nav {
    position: relative;
}
ul {
    position: fixed;
    top: 0;
    background-color: bisque;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 2rem;
}

.menu-wrapper {
    padding: 1rem;
}
.active {
    background-color: red;
}
footer {
    margin-top: 50rem;
    background-color: grey;
}
</style>
