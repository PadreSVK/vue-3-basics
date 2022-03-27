<template>
    <input id="Search" type="text" v-model="query" placeholder="Search" />
    <ul>
        <li v-for="item in items" :key="item.id">
            {{ item.label }} : {{ item.age }}
            <br />
        </li>
    </ul>
</template>

<script setup lang="ts">
import { ref, watch } from 'vue';

const data = [
    { id: "40e63dc3f0fd478ebd1086272dce4af6", label: "Katelynn Leclerc", age: 2 },
    { id: "b512c82b5d3a45bca4a085f4ce085ef5", label: "Michale Vasseur", age: 26 },
    { id: "c2719496015b4a3a9267f210a944c784", label: "Leatha Renault", age: 61 },
    { id: "ee95eafe84ac47c9ad5d04254611fe27", label: "Karlee Le roux", age: 72 },
    { id: "79c426bad5144503a9b3c5617909b96d", label: "Henri Picard", age: 76 },
    { id: "7661be436f2541e384d72cf08d138182", label: "Katelynn", age: 78, },
    { id: "2c4637d276704b818d035b34476d01f3", label: "Larry", age: 70, },
    { id: "3f303720783b4684a7a9df821cb287a6", label: "Michale", age: 6, },
    { id: "49039479239f41539bae99a5585bdc21", label: "Rosalind", age: 22, },
    { id: "1884c7fc319e4303afce89a1de2234d5", label: "Leatha", age: 43, },
    { id: "588b5f6e6b0c426cbdc86b4d76402192", label: "Ruthie", age: 65, },
    { id: "fee2c34cfa134478a54f1085cdfddf97", label: "Karlee", age: 55, },
    { id: "ec67f6edaf114efd9ebc35b724f41512", label: "Roselyn", age: 97, },
    { id: "6fecf2680f68407bb320455bad7cfcf1", label: "Henri", age: 63, },
    { id: "a8cb3c90160b426e8cd1dc76c78f5492", label: "Linda", age: 16, },
    { id: "7c37a1a9c3094a04a8b11037dbd1f862", label: "Luna", age: 11, },
    { id: "5e5affd2a85f47b59a6e2a59a0713352", label: "Gerard", age: 3, },
    { id: "425018d9d7544a369b806daf7baf93e2", label: "Humberto", age: 29, },
    { id: "3ccdd84eec8e4a88b3880ae8e33e6f55", label: "Eli", age: 98, },
    { id: "03e9d63bdd0a41a591ec16c3aab9b2a3", label: "Sim", age: 86, },
    { id: "76abf76250294a09847e70a320c437fd", label: "Anahi", age: 94, },
    { id: "1f6fe321d9654c6792413c8c93007fcf", label: "Vincenzo", age: 10, },
    { id: "79c137a0d3174e2aa2741f2cfdfafd6a", label: "Donny", age: 45, },
    { id: "e01ee9e5fbaf455f89e6db23efbd48e1", label: "Gerald", age: 66, },
    { id: "0ad5384c212b484d9fce8c0625a7d0e7", label: "Jason", age: 94, },
    { id: "3375427ead3b4805a234ea65fb142842", label: "Pauline", age: 92, },
    { id: "88a252cd61f9428998938971315a4b27", label: "Randy", age: 47, },
    { id: "da51a685fa154492a0e7cea6f7e29848", label: "June", age: 89, },
];

const items = ref(data)
const query = ref("")

watch(query, q => {
    console.log({ query: q });
    items.value = data.filter(i => i.label.includes(q))
})

</script>
