<script>
  import { onMount } from 'svelte';
  import { default as QRious } from 'qrious';

  export let errorCorrection = "L";
  export let background = "#fff";
  export let color = "#000";
  export let size = "200";
  export let value = "";
  export let padding = 0;
  export let className = "qrcode";

  let image = '';

  function generateQrCode() {
    const QRCode = new QRious();
    QRCode.set({
      background,
      foreground: color,
      level: errorCorrection,
      padding,
      size,
      value,
    });

    image = QRCode.toDataURL('image/jpeg');
  }

  // (!) Plugin svelte: $: has no effect outside of the top-level
  $: {
    if (typeof document != 'undefined' && value) {
      generateQrCode();
    }
  }

  export function getImage() {
    return image;
  }

  onMount(() => {
    generateQrCode();
  });
</script>

<img src={image} alt={value} class={className} />