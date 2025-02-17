<script lang="ts>
  import Component2 from './Component2.svelte'

  const {value, setState} = $props()

  let closure = () => console.log('value is undefined:', value)

  // Uncomment to fix the bug
  // const valueCopy = value
  // closure = () => console.log('value is undefined:', valueCopy)

  const next = () => setState({component: Component2, props: {closure}})

  $inspect(value)
</script>

<button onclick={next}>Next</button>
