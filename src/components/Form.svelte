<script>
  export let current;
</script>

<form class="field has-addons">
  <div class="control">
    <input
      class="input username"
      type="text"
      placeholder="enter github username"
      required />
  </div>
  <div class="control">
    <button
      type="submit"
      class="button is-info load-username has-tooltip-right
      has-tooltip-multiline"
      data-tooltip="username can only contain characters: `a-z`, `0-9`, `-`, `_`">
      Load
    </button>
  </div>
</form>
