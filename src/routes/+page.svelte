
<script>
  import QrCode from "$lib/index";
  let qrCodeRef;

  let inputValue = "";

  function handleGetImage() {
    const imageUrl = qrCodeRef?.getImage();

    console.log(imageUrl);
  }
</script>

<h1>{inputValue}</h1>
<input type="text" bind:value={inputValue} >

<button on:click={handleGetImage}>Export Image</button>
<QrCode value={inputValue} bind:this={qrCodeRef} />
