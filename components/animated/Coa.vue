<template>
  <svg xmlns="http://www.w3.org/2000/svg" width="199" height="222" viewBox="0 0 149 222">
    <g id="Coa" transform="translate(-1246 -332)" opacity="1">
      <rect
        id="Rectangle_23"
        class="account"
        data-name="Rectangle 23"
        width="43"
        height="9"
        rx="4.5"
        transform="translate(1246 332)"
        fill="#ebebeb"
      ></rect>
      <rect
        id="Rectangle_23-2"
        class="account"
        data-name="Rectangle 23"
        width="121"
        height="9"
        rx="4.5"
        transform="translate(1257 347)"
        fill="#ebebeb"
      ></rect>
      <rect
        id="Rectangle_23-3"
        class="account"
        data-name="Rectangle 23"
        width="61"
        height="9"
        rx="4.5"
        transform="translate(1257 362)"
        fill="#ebebeb"
      ></rect>
      <rect
        id="Rectangle_23-4"
        class="account"
        data-name="Rectangle 23"
        width="91"
        height="9"
        rx="4.5"
        transform="translate(1260 377)"
        fill="#ebebeb"
      ></rect>
      <rect
        id="Rectangle_23-5"
        class="account"
        data-name="Rectangle 23"
        width="126"
        height="9"
        rx="4.5"
        transform="translate(1269 392)"
        fill="#ebebeb"
      ></rect>
      <rect
        id="Rectangle_23-6"
        class="account"
        data-name="Rectangle 23"
        width="61"
        height="9"
        rx="4.5"
        transform="translate(1269 407)"
        fill="#ebebeb"
      ></rect>
      <rect
        id="Rectangle_23-7"
        class="account"
        data-name="Rectangle 23"
        width="79"
        height="9"
        rx="4.5"
        transform="translate(1246 422)"
        fill="#ebebeb"
      ></rect>
      <rect
        id="Rectangle_23-8"
        class="account"
        data-name="Rectangle 23"
        width="97"
        height="9"
        rx="4.5"
        transform="translate(1257 437)"
        fill="#ebebeb"
      ></rect>
      <rect
        id="Rectangle_23-9"
        class="account"
        data-name="Rectangle 23"
        width="56"
        height="9"
        rx="4.5"
        transform="translate(1269 452)"
        fill="#ebebeb"
      ></rect>
      <rect
        id="Rectangle_23-10"
        class="account"
        data-name="Rectangle 23"
        width="85"
        height="9"
        rx="4.5"
        transform="translate(1257 467)"
        fill="#ebebeb"
      ></rect>
      <rect
        id="Rectangle_23-11"
        class="account"
        data-name="Rectangle 23"
        width="57"
        height="9"
        rx="4.5"
        transform="translate(1246 482)"
        fill="#ebebeb"
      ></rect>
      <rect
        id="Rectangle_23-12"
        class="account"
        data-name="Rectangle 23"
        width="69"
        height="9"
        rx="4.5"
        transform="translate(1269 513)"
        fill="#ebebeb"
      ></rect>
      <rect
        id="Rectangle_23-13"
        class="account"
        data-name="Rectangle 23"
        width="91"
        height="9"
        rx="4.5"
        transform="translate(1282 529)"
        fill="#ebebeb"
      ></rect>
      <rect
        id="Rectangle_23-14"
        class="account"
        data-name="Rectangle 23"
        width="67"
        height="9"
        rx="4.5"
        transform="translate(1269 545)"
        fill="#ebebeb"
      ></rect>
      <rect
        id="Rectangle_39"
        class="account"
        data-name="Rectangle 39"
        width="116"
        height="9"
        rx="4.5"
        transform="translate(1257 498)"
        fill="#ebebeb"
      ></rect>
    </g>
  </svg>
</template>

<script>
export default {
  name: 'Coa',
  mounted() {
    let scene = new this.$scrollmagic.Scene({
      triggerElement: '#Coa'
    })
    let timeline1 = new this.$gsap.TimelineMax({
      paused: false,
      defaultEase: Linear.easeNone,
      onComplete: () => this.$emit('completed', 2)
    })
    timeline1
      .from('.account', 1.5, { scaleX: 0, opacity: 0 })
      .to('.card-title', 1.5, { opacity: 1 }, '-=1')
      .to('.card-description', 1.5, { opacity: 1 }, '-=1.5')

    scene.setTween(timeline1)
    this.$ksvuescr.$emit('addScene', 'scene1', scene)
  },
  destroyed() {
    this.$ksvuescr.$emit('destroyScene', 'scene1')
  }
}
</script>
