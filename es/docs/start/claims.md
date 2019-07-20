# Como obtener KSM

La red Kusama es la red de investigación y desarrollo de Polkadot. Esta guía lo guiará a través de cómo proceder con la reclamación de KSM (tokens de Kusama).

Para alinear a Kusama con los propietarios y la comunidad de DOT existentes, si usted es un titular de la asignación de DOT, puede reclamar la cantidad equivalente de tokens de Kusama (ticker: KSM). Hay dos formas de reclamar antes de génesis enviando una transacción en Ethereum o después de génesis firmando un mensaje usando su clave de asignación y realizando una transacción en Kusama.

## Paso 1. Crea una cuenta en Kusama.

Necesitará una cuenta de Kusama para reclamar el KSM. Hay algunas formas en que puedes crear una. Para la mayoría de los usuarios, recomendamos el uso de la [interfaz de usuario de Polkadot,](https://polkadot.js.org/apps/#/explorer) ya que le permitirá almacenar su archivo de clave cifrado localmente.

> AVISO: Lamentablemente, en este momento, las cadenas Kusama y Substrate no tienen soporte de billetera de hardware utilizando los productos Ledger o Trezor. Esperemos que pronto esto cambie!

Otra opción que puede considerar usar es la utilidad de línea de comandos de `subkey` que le permitirá estar más seguro y generar su clave en un dispositivo con espacio de aire. Algunas otras opciones incluyen el uso de la billetera Enzyme en el navegador (como MetaMask) o la billetera móvil Polkawallet.

### Uso de Polkadot UI

1. Vaya a la [pestaña de la cuenta de Polkadot UI](https://polkadot.js.org/apps/#/accounts) y haga clic en el botón `Add account` .

<img src="../../../img/polkadotui-find-the-accounts-page.png" width="50%">

1. Ingrese un nombre para su cuenta y cree una contraseña segura. Esta contraseña se utilizará para descifrar su cuenta.

<img src="../../../img/polkadotui-create-your-account.png" width="50%">

1. Ignore las opciones avanzadas a menos que desee cambiar el tipo de criptografía que se usa para sus claves (ya sea sr25519 o ed25519).

2. Haga clic en `Save` y `Create and backup account` .

3. Guarde su almacén de claves cifrado localmente.

4. La cuenta ahora aparece en la pestaña Cuentas y está respaldada en el almacén de claves que acaba de guardar.

5. Haga clic en el identicon DOT para copiar la dirección al portapapeles.

<img src="../../../img/polkadotui-copy-account-address.png" width="50%">

### Usando `subkey`

1. Siga las instrucciones de construcción para el [sustrato](https://github.com/paritytech/substrate#6-building) .
2. Al compilar, en lugar de compilar todos los binarios, construya una `subkey` escribiendo la `cargo build subkey` .
3. Puede crear / usar la subclave en una computadora que no esté conectada a Internet para mayor seguridad.
4. El comando `subkey generate` generará un nuevo par de claves.

### Uso de la billetera del navegador Enzyme (solo Chrome)

1. Instale la billetera del navegador Enzyme desde la [tienda Chrome](https://chrome.google.com/webstore/detail/enzyme/amligljifngdnodkebecdijmhnhojohh) . Haga clic en `Add to Chrome` y confirme haciendo clic en `Add extension` en la ventana emergente.

2. Acepte los términos de uso.

<img src="../../../img/enzyme-open-the-extension.png" width="50%">

1. Cree una contraseña segura y asegúrese de escribirla en otro lugar, luego haga clic en `Create` .

<img src="../../../img/enzyme-choose-a-password.png" width="50%">

1. Copia la frase semilla y guárdala en un lugar seguro. No comparta la frase semilla con nadie, puede usarla para acceder a su cuenta si olvida su contraseña o pierde su almacén de claves.

<img src="../../../img/enzyme-generate-seed-phrase.png" width="50%">

1. Haga clic en `Dashboard` .

2. Haga clic en el identicon DOT para copiar su dirección al portapapeles.

<img src="../../../img/enzyme-copy-your-address.png" width="50%">

### Utilizando polkawallet

1. Instale [Polkawallet](https://polkawallet.io) . Haga clic en Descargar y seleccione el enlace correspondiente a la plataforma que está utilizando. En Android es posible que deba permitir la instalación de aplicaciones desde fuentes externas. En iOS, es posible que deba "confiar" en Polkawallet en General> Perfiles y administración de dispositivos> Sección de aplicaciones empresariales antes de ejecutar la aplicación.

2. Una vez que abra la aplicación, copie la frase semilla y guárdela en un lugar seguro, no la comparta con nadie, puede usarla para acceder a su cuenta si olvida su contraseña o pierde su almacén de claves.

<img src="../../../img/polkawallet-create-account.jpg" width="50%">

1. Asigne un nombre a su cuenta y cree una contraseña segura, asegúrese de escribirla en otro lugar y luego haga clic en Guardar.

2. Se le pedirá que confirme su frase inicial: esto es para asegurarse de que la haya copiado en un lugar seguro.

3. Haga clic en el símbolo rosado del Código QR y seleccione Copiar dirección para copiar su dirección al portapapeles.

<img src="../../../img/polkawallet-accounts-page.jpg" width="50%">
<img src="../../../img/polkawallet-copy-address.jpg" width="50%">

## Paso 2. Consigue los tokens KSM

Hay dos métodos para reclamar KSM.

1. **Titulares de DOT** aquellos que participaron en las ventas de Polkadot pueden reclamar una cantidad proporcional de KSM antes del lanzamiento de la red.

Puede hacerlo a través de [este proceso de reclamaciones](https://claim.kusama.network/) .

Puede consultar [esta guía detallada](./dot-holders.md) para conocer paso a paso cómo hacerlo.

¿Teniendo problemas? Obtenga ayuda en el [chat de reclamaciones de](https://riot.im/app/#/room/#KSMAClaims:polkadot.builders) KSM.

**2. Faucet:** para aquellos que no participaron en la venta de Polkadot, KSM está disponible públicamente después de la génesis a través de un faucet. Descubre más [aquí](./faucet.md) .

Los proyectos públicos que necesitan más KSM pueden solicitarlos enviando un correo electrónico a projects@kusama.network.
