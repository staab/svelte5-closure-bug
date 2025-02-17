<script lang="ts">
  import Component1 from '../lib/Component1.svelte'

  const setState = newState => {
    state = newState
  }

  let state = $state({
    component: Component1,
    props: {
      value: 1,
      setState,
    },
  })
</script>

<state.component {...state.props} />
