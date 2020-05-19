<script>
  import QRious from 'qrious';

  const QRcode = new QRious();


  export let errorCorrection = "H";
  export let background = "#fff";
  export let color = "#000";
  export let size = "400";
  export let value = ""
  export let padding = 0;

  export let className = "qrcode"

  QRcode.set({
    background,
    foreground: color,
    level: errorCorrection,
    padding,
    size,
    value,
  });
  
  const image = QRcode.toDataURL('image/jpeg')

</script>

<img src={image} alt="" class={className} />