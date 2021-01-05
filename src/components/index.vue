<template>
    <div class="root">
        <kinesis-container class="container">
            <kinesis-element :strength="10">
                <h1 class="title1">CONTINENTAL GT </h1>
            </kinesis-element>
            <kinesis-element :strength="20">
                <p class="content1">With its 6.0 litre, twin-turbocharged W12 engine, a step-change in technology<br> 
                and a truly stunning design language, the Continental GT is unmatched<br>
                in its class. This Bentley GT* coupé is the quintessential grand<br>
                tourer – phenomenally powerful, beautifully<br>
                designed and exquisitely crafted.</p>
            </kinesis-element>
            <!-- <img class="car" src="../../static/car2.png"/> -->
        </kinesis-container>
    </div>
</template>

<script>
export default {
    name: 'index',
    data: () => ({

    })
}
</script>

<style scoped>
    .container {
        position: absolute;
        top: 150px;
        left: 200px;
        color: black;
        padding: 20px;
    }
    .car {
        max-width: 800px;
        max-height: 600px;
        position: absolute;
        top: 10px;
        left: 450px;
    }
</style>