<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { library } from '@fortawesome/fontawesome-svg-core';
import { fab } from '@fortawesome/free-brands-svg-icons';
import { fas } from '@fortawesome/free-solid-svg-icons';

export default {
components: {
    FontAwesomeIcon,
},
  mounted() {
    library.add(fab, fas);
  }
}
</script>

<template>
  <font-awesome-icon :icon="['fab', 'github']" />
    
    <!-- Ikon 2 -->
    <font-awesome-icon :icon="['fab', 'whatsapp']" />

    <!-- Ikon 3 -->
    <font-awesome-icon :icon="['fab', 'instagram']" />

    <font-awesome-icon :icon="['fas', 'envelope']" />
</template>
