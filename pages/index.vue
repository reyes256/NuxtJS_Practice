<template>
    <div>
        <!-- <h1>VUE JS HDTPM</h1>

        <h3>A {{ precio }} EL PUTO DOCE DE TECATE MAMON</h3>

        <button v-on:click="increment">Subele al doce</button>

        <br><br>
        <hr>
        <br> -->

        <table>
            <tr>
                <th>Name</th>
                <th>Id</th>
                <th>Value</th>
            </tr>
            <tr v-for="device in devices">
                <td>{{ device.name }}</td>
                <td>{{ device.id }}</td>
                <td>{{ device.value }}</td>
            </tr>
        </table>

        <br><hr><br>
        
        Name: {{ newDevice.name.toUpperCase() }}<br>
        Id: {{ newDevice.id.toUpperCase() }}<br>
        Value: {{ newDevice.value.toUpperCase() }}<br>
        
        <br><hr><br>
        
        <label for="">Name: <input type="text" v-model="newDevice.name"></label><br>
        <label for="">Id: <input type="text" v-model="newDevice.id"></label><br>
        <label for="">Value: <input type="text" v-model="newDevice.value"></label><br>
        <label for="">User Id: <input type="text" v-model="newDevice.userId"></label><br>
        
        <button @click="addDevice">Add Device</button>
        <br><hr><br>

        <pre>{{ newDevice }}</pre>
    </div>
</template>

<script>
    export default{
        data(){
            return {
                precio: 200,
                devices: [],
                newDevice: {
                    name: "",
                    id: "",
                    value: "",
                    userId: "",
                }
            }
        },

        created(){
        },
        mounted(){
            setTimeout(() => {
                this.getDevices();
            }, 800);
        },

        methods: {
            increment(){
                this.precio++;
            },
            addDevice(){
                this.devices.push(this.newDevice)
            },
            getDevices(){
                var response = [
                    {
                        name: "Home",
                        id: "2222",
                        userId: "conchudo",
                        value: 7
                    },
                    {
                        name: "Kitchen",
                        id: "3333",
                        userId: "Martina",
                        value: 69
                    },
                    {
                        name: "Patio",
                        id: "4444",
                        userId: "Carlota",
                        value: 111
                    },
                ];

                this.devices = response;
            }
        }
    }
</script>

<style>
    table, th, td{
        border-collapse: collapse;
        border: 1px solid black;
        padding: 10px;
    }
</style>