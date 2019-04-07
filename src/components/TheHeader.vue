<template>
  <header>
    <FontAwesomeIcon :icon="icon('bomb')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('bong')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('heart')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('laugh')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('meh')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('acorn')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('axeBattle')"></FontAwesomeIcon>
    <FontAwesomeIcon :icon="icon('dagger')"></FontAwesomeIcon>
  </header>
</template>

<script>
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { faBomb, faBong } from "@fortawesome/pro-light-svg-icons";
import {
  faHeart,
  faLaughBeam,
  faMeh,
  faFutbol as farFutbol
} from "@fortawesome/pro-regular-svg-icons";

import {
  faAcorn,
  faAxeBattle,
  faDagger
} from "@fortawesome/pro-solid-svg-icons";

export default {
  components: {
    FontAwesomeIcon
  },
  methods: {
    icon(i) {
      const fa = {
        bomb: faBomb,
        bong: faBong,
        heart: faHeart,
        laugh: faLaughBeam,
        meh: faMeh,
        acorn: faAcorn,
        axeBattle: faAxeBattle,
        dagger: faDagger
      };
      return fa[`${i}`];
    }
  }
};
</script>
