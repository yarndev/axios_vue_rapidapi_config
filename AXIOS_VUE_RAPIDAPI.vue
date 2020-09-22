<template>

</template>

<script>
import axios from 'axios'

export default {
    data: function () {
        return {

            result: null,

        };
    },
    methods: {
        autofill() {
            axios({
                    'method': 'GET',
                    'url': 'https://vindecoder.p.rapidapi.com/decode_vin',
                    'headers': {
                        'content-type': 'application/octet-stream',
                        "x-rapidapi-host": "vindecoder.p.rapidapi.com",
                        "x-rapidapi-key": "YOUR_API_KEY"
                    },
                    'params': {
                        'YOUR_PARAMETER_KEY': 'YOUR_PARAMETER_KEY',
                    },
                })
                .then((response) => {
                    console.log(response.data);

                });
        },
    },
};
</script>
