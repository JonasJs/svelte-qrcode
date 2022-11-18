<script>
  import { onMount } from "svelte";
  import QRious from 'qrious';

  let elementRef;
  let qrCodeRef;
  let element = "img";
  let imageData = null;

  // Props
  export let value = "";
  export let level = "H";
  export let background = "#fff";
  export let color= "#000";
  export let size = 200;
  export let padding = 0;
  export let className = "qrcode";
  export let errorCorrection = "L";

  function generateQrCode() {
    const qrcode = new QRious({
      element: elementRef,
      value,
      level,
      background,
      foreground: color,
      size,
      padding,
      level: errorCorrection,
    });

    qrCodeRef = qrcode;
  }

  export function getImage({ type = "image/png", quality = 1 }) {
    return qrCodeRef?.toDataURL(type, quality);
  }

  $: {
    if(value && qrCodeRef) {
      generateQrCode();
    }
  }

  onMount(() => {
    generateQrCode();
  });

</script>

<svelte:element class={className} this={element} bind:this={elementRef} {...$$props} />
