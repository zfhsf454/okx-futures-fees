# OKX comisiones futuros: cuánto se paga al abrir y cerrar un perpetuo, cómo se calcula el 0,02%/0,05% y qué otros cargos aparecen en la cuenta (con ejemplos y tarifas por región)

En el nivel Regular de la plataforma global, OKX cobra **0,02% maker y 0,05% taker** en perpetuos y futuros con vencimiento. El porcentaje se aplica sobre el valor nominal de la operación, no sobre el margen, y se paga dos veces: al abrir y al cerrar. Una posición de 20.000 USDC que entra y sale con órdenes a mercado deja 20 USDC en comisiones, que es el 1% del margen comprometido si operaste con 10x.

Aquí está el desglose completo: la fórmula exacta para futuros denominados en USDC/USDT y para futuros denominados en cripto, los dos ejemplos numéricos que publica el propio OKX, el resto de cargos que se suman al trading (funding, liquidación forzosa, 0,01% de liquidación al vencimiento) y las diferencias de tarifa entre la plataforma global, la EEE, Estados Unidos y Australia.

> **Para decidir en un minuto.** Fuera de la EEE y de EE. UU., la tarifa de futuros es 0,02% maker / 0,05% taker hasta que subas de nivel. Un ciclo completo taker entra y sale por 0,10% del nominal; con órdenes límite que descansan en el libro, 0,04%. 👉 [Abrir cuenta en OKX con el enlace de registro y ver la tarifa que asigna a tu cuenta](https://okx.com/join/CASH20).

## Tarifas de futuros de OKX según el tipo de cuenta y la región

La tarifa que aparece en tu panel depende del esquema al que pertenece tu cuenta, no solo del producto que operas. OKX mantiene tablas separadas para la plataforma global, para el Espacio Económico Europeo y para Estados Unidos, y la filial australiana publica la suya. La tabla de la página estadounidense, por ejemplo, muestra 0,2000% maker y 0,3500% taker para el usuario Regular, cifras que no deben compararse con el 0,08%/0,10% de spot global porque son mercados distintos con estructuras de comisiones distintas.

| Tipo de cuenta | Spot (maker / taker) | Futuros (maker / taker) | Qué implica |
| --- | --- | --- | --- |
| Global, usuario Regular | 0,08% / 0,10% | **0,02% / 0,05%** | Tarifa base más baja; VIP 1 desde 100.000 USD en activos o 1.000.000 USD de volumen spot a 30 días |
| EEE con cuenta de derivados (X-Perps) | 0,08% / 0,10% | 0,02% / 0,05% | Es la cuenta que te habilita a operar derivados en Europa |
| EEE solo spot | 0,10% / 0,20% según una fuente; 0,20% / 0,35% según otra | Sin acceso a futuros | Dos lecturas en conflicto, ver nota |
| EE. UU. (OKX INC., marco vigente desde el 1 de febrero de 2026) | 0,20% / 0,35% en la tabla oficial estadounidense | Derivados restringidos para residentes | No mezclar con la tabla global |
| Australia | 0,70% Regular; VIP 1 baja a 0,45% / 0,50% desde 150.000 AUD en activos o 200.000 AUD de volumen a 30 días | Restringidos | Dato de una sola fuente, tómalo como referencia |

Dos advertencias sobre esa tabla. La primera: hay dos fuentes terciarias, publicadas con tres días de diferencia en noviembre de 2026, que dan cifras distintas para la cuenta europea que solo tiene spot. Una habla de 0,10%/0,20%; otra, de 0,20%/0,35%, la misma que el esquema estadounidense. La página oficial europea no permite zanjar la discrepancia con los datos disponibles, así que lo práctico es revisar la tabla que aparece al iniciar sesión, que es la que se aplica a tus operaciones. La segunda: la cuenta europea sin derivados no puede operar futuros; para eso hace falta abrir la cuenta de X-Perps, que en la EEE sustituye al perpetuo clásico con contratos a cinco años para cumplir con MiFID II y admite hasta 10x de apalancamiento.

En cualquier caso, cada fila de la tabla se consulta desde el mismo registro: 👉 [comprobar la tarifa vigente de tu tipo de cuenta en OKX](https://okx.com/join/CASH20).

Sobre los niveles VIP: no hay una tabla oficial pública con el detalle de futuros para cada nivel en el momento de escribir esto, así que conviene desconfiar de las tablas de terceros que circulan con cifras cerradas. Lo que sí está documentado es el mecanismo: el nivel se calcula con el volumen a 30 días y el snapshot diario de activos de la cuenta principal **y todas sus subcuentas**, las subcuentas comparten el nivel de la principal, el volumen se contabiliza a las 16:00 UTC y OKX actualiza el nivel de comisiones entre las 20:00 y las 22:00 UTC. El nivel VIP 1 de la plataforma global arranca en 100.000 USD de activos o 1.000.000 USD de volumen spot a 30 días. A partir del VIP 6 la comisión maker de spot baja a cero y desde el VIP 7 se cobra un rebate al maker, que en el escalón más alto ronda el 0,005%.

## Cómo se calcula la comisión de un futuro en OKX

OKX usa dos fórmulas, una por tipo de margen. La diferencia no es cosmética: cambia la base de cálculo y la moneda en la que te cobran.

**Futuros con margen en USDC o USDT (U-margined):**

> Comisión = tasa × (número de contratos × multiplicador × tamaño del contrato × precio de ejecución)

Se liquida en USDC y se descuenta en el momento de la ejecución.

**Futuros con margen en cripto (coin-margined):**

> Comisión = tasa × (número de contratos × multiplicador × valor nominal por contrato ÷ precio de ejecución)

Se liquida en la cripto que estás operando, también al ejecutarse la orden.

Los dos ejemplos que publica el centro de ayuda de OKX sirven para verlo con números reales:

| Ejemplo | Orden | Cálculo | Comisión |
| --- | --- | --- | --- |
| Perpetuo BTCUSDC (tamaño 0,01 BTC, multiplicador 1), 100 contratos = 1 BTC a 20.000 USDC, 10x, margen 2.000 USDC | A mercado (taker) | 0,05% × (100 × 1 × 0,01 × 20.000) | **10 USDC** |
| La misma posición | Límite que descansa en el libro (maker) | 0,02% × (100 × 1 × 0,01 × 20.000) | **4 USDC** |
| Perpetuo BTCUSD (tamaño 100 USD, multiplicador 1), 100 contratos = 10.000 USD a 20.000 USD | A mercado (taker) | 0,05% × (100 × 1 × 100 ÷ 20.000) | **0,00025 BTC** |
| La misma posición | Límite (maker) | 0,02% × (100 × 1 × 100 ÷ 20.000) | **0,0001 BTC** |

La lectura importante del primer par de filas: el margen eran 2.000 USDC, pero la comisión se calculó sobre 20.000 USDC de nominal. Diez USDC de entrada representan el 0,5% del margen; abrir y cerrar a mercado deja 20 USDC, es decir, el 1% del colateral. El apalancamiento no cambia la tasa, cambia el tamaño de la base sobre la que se aplica.

La comisión se descuenta del propio llenado, no existe un saldo aparte para pagarla ni puedes abonarla con otra moneda. En una compra el cargo se hace sobre la cripto recibida; en una venta, sobre el importe obtenido. Si alguna vez el número de la comisión no coincide con tu cálculo, el sitio para revisarlo es el historial de órdenes, donde cada llenado trae su propia línea de fee.

👉 [Crear la cuenta y revisar la tarifa antes de enviar la primera orden](https://okx.com/join/CASH20)

## Cuánto cuesta un ciclo completo: abrir y cerrar

OKX cobra la misma tasa al abrir y al cerrar, siempre sobre el tamaño ejecutado. Eso permite reducir el coste de una operación a una escalera de tres combinaciones:

- **Taker entra, taker sale:** 0,05% + 0,05% = **0,10%** del nominal. Sobre 10.000 USD son 10 USD.
- **Maker entra, taker sale (o al revés):** 0,02% + 0,05% = **0,07%**.
- **Maker entra, maker sale:** 0,02% + 0,02% = **0,04%**.

Ese 0,10% hay que leerlo como el coste mínimo de operar antes de contar el funding, y es la razón por la que un scalper que hace diez ciclos diarios de 10.000 USD con órdenes a mercado paga unos 100 USD al día solo en comisiones. Para quien abre una posición y la mantiene semanas, 0,10% es irrelevante frente al movimiento del precio; para quien hace muchas entradas y salidas, es el gasto principal.

No se cobra nada por ajustar el apalancamiento ni por añadir margen a una posición abierta. Esos movimientos no generan comisión.

## Los cargos que no son comisión de trading (y los que no existen)

Aquí es donde se mezclan conceptos. Una cuenta de futuros puede recibir cuatro cargos distintos, y solo el primero es la comisión de la que habla la tabla de tarifas.

**1. Comisión de trading.** 0,02% / 0,05% en el nivel base global, dos veces por posición.

**2. Funding o tasa de financiación.** Solo en perpetuos. No es un ingreso de OKX: es una transferencia directa entre largos y cortos, y la plataforma no cobra servicio por moverla.

**3. Comisión de liquidación forzosa.** Se calcula con la tasa **taker** de tu nivel actual. Si te liquidan, pagas un 0,05% extra en el peor momento posible, cuando la cuenta ya está absorbiendo una pérdida que no elegiste.

**4. Comisión de liquidación al vencimiento.** 0,01% para todos los usuarios, sin importar el nivel. Aplica a los futuros con fecha de vencimiento; los perpetuos no la pagan.

Fuera de eso, hay costes que pertenecen a otra parte de la cuenta: la comisión de red al retirar cripto (desde 0,0022 USDT en X Layer hasta alrededor de 2 USDT en Tron), el spread implícito de Convert y de la compra rápida, y el 0% de P2P, cuyo volumen además no cuenta para subir de nivel. Nada de eso es comisión de futuros.

## Funding: el coste que aparece cada 8 horas

El funding se calcula como valor de la posición multiplicado por la tasa de financiación. En un perpetuo con margen en USDT, el valor de la posición es número de contratos × tamaño × multiplicador × precio de marca. Con tasa positiva, los largos pagan a los cortos; con tasa negativa, ocurre al revés.

La mayoría de los contratos liquidan a las 00:00, 08:00 y 16:00 UTC, y solo paga o cobra quien tiene posición abierta exactamente en ese instante. Algunos contratos lo hacen cada 4, 2 o 1 hora. El componente de interés de referencia es del 0,03% diario, o 0,01% por cada ciclo de ocho horas, y la prima del futuro sobre el índice empuja la tasa arriba o abajo.

Desde abril de 2026 hay una regla adicional que afecta a quien mantiene posiciones en momentos de estrés: si la tasa toca su límite superior o inferior, OKX sube la frecuencia de liquidación un escalón cada vez (de 8 a 4, de 4 a 2, de 2 a 1 hora). Solo vuelve al horario por defecto cuando todas las liquidaciones de las 12 horas previas se mantuvieron dentro de ±0,20%. En la práctica, un mercado muy desequilibrado puede pasar de cobrarte tres veces al día a cobrarte veinticuatro.

Para dimensionarlo: 10.000 USDT en largo con una tasa de 0,01% por liquidación cuestan unos 3 USDT al día, alrededor de 90 USDT al mes. Es un orden de magnitud inferior al 0,10% de ida y vuelta de una operación taker, pero se acumula justo en las posiciones que más tiempo aguantan. Los futuros con vencimiento no pagan funding; su coste vive en la base, el momento del roll y la liquidación.

## Cómo bajar la tarifa (y qué no funciona)

**Usa órdenes límite que se queden en el libro.** La diferencia entre maker y taker en futuros es de 2,5x: 0,02% frente a 0,05%. Es la palanca más directa que existe y no depende de tu volumen. Una orden límite que cruza el spread se ejecuta al instante y paga taker, así que la condición es que quede esperando.

**Sube de nivel con volumen real.** El nivel se recalcula a diario con el volumen a 30 días y el snapshot de activos. Si operas con frecuencia, el escalón superior llega solo; si no, forzarlo con operaciones de relleno cuesta más en comisiones de lo que ahorra.

**Cuidado con los pares de comisión cero.** USDC/USDT y PYUSD/USDT cotizan al 0% en la plataforma global, y en la EEE lo hacen USDC/EUR y tres pares en zloty polaco. Son útiles para moverte entre stablecoins, pero su volumen **no cuenta** para el volumen de 30 días ni para la evaluación de niveles. Si los usas para hacer volumen, no avanzas.

**Lo que no rebaja la comisión:** mantener OKB y usar un código de referido. El propio centro de ayuda de OKX indica que ninguna de las dos cosas reduce la tarifa de trading. Existen programas de devolución gestionados por afiliados, pero son acuerdos externos con sus propias condiciones; no los cuentes como un descuento oficial de la casa.

👉 [Abrir la cuenta con el registro de OKX y empezar a operar con la tarifa que te corresponda](https://okx.com/join/CASH20)

## OKX frente a otras plataformas: cuándo la tarifa base no decide nada

Con la misma operación de 1.000 USD, las comisiones de futuros cambian bastante según dónde la ejecutes. Estas son las cifras verificadas de los competidores que más se comparan:

| Plataforma | Futuros maker | Futuros taker | 1.000 USD, abrir y cerrar como taker |
| --- | --- | --- | --- |
| OKX, Regular global | 0,02% | 0,05% | 1,00 USD |
| MEXC, contrato estándar | 0,010% | 0,040% | 0,80 USD |
| MEXC, perpetuo BTCUSDT (tarifa especial) | 0,000% | 0,020% | 0,20 USD |

MEXC sale más barato en esa comparación, con una advertencia que importa: no atiende a residentes de Estados Unidos, Reino Unido ni del Espacio Económico Europeo, así que para esas tres regiones la comparación no aplica. En volumen sostenido la brecha se nota: 100.000 USD mensuales de taker durante un año son 1.200 USD en OKX, 960 USD en contratos estándar de MEXC y 240 USD con la tarifa especial de BTCUSDT.

Como referencia de mercado, las tarifas base de OKX coinciden con el nivel regular de futuros de Binance y quedan por debajo del 0,055% taker de Bybit. Hyperliquid, en cadena, arranca más abajo: 0,045% taker y 0,015% maker.

La conclusión práctica no es que una plataforma sea mejor en abstracto. Si haces pocas operaciones al mes, 0,05% frente a 0,04% son céntimos y pesan más la liquidez, la disponibilidad de pares y el acceso legal desde tu país. Si haces volume alto como taker, la diferencia de una décima de punto se convierte en tres cifras al año y merece cambiar de venue o pasarse a órdenes maker.

## Preguntas frecuentes sobre las comisiones de futuros de OKX

**¿La liquidación forzosa se cobra aparte de la comisión normal?**
Sí. Además de las comisiones de apertura y cierre, la liquidación tiene su propio cargo calculado con tu tasa taker vigente.

**¿El funding se lo queda OKX?**
No. Es una transferencia entre traders: los largos pagan a los cortos o al contrario según el signo de la tasa. OKX no cobra servicio por ese movimiento.

**¿Una orden a mercado siempre paga taker?**
En la práctica sí, porque se ejecuta contra el libro. Una orden límite también paga taker si su precio cruza el spread y se llena de inmediato; solo paga maker si espera en el libro. Las órdenes de stop loss y take profit suelen llenarse como taker.

**¿Por qué me cobraron taker si puse una orden límite?**
Porque se ejecutó al entrar, sin llegar a descansar en el libro. El historial de órdenes muestra el rol de cada llenado y la comisión aplicada.

**¿Pago lo mismo operando en USDC que en BTC?**
La tasa es la misma, pero la moneda y la fórmula no. En U-margined la comisión se liquida en USDC o USDT sobre el nominal; en coin-margined se liquida en la cripto operada y el cálculo divide por el precio de ejecución.

**¿Los futuros con vencimiento pagan funding?**
No. En su lugar pagas un 0,01% de liquidación al vencimiento, igual para todos los niveles.

## Cómo elegir según tu caso

Si abres y cierras posiciones de forma ocasional, el nivel Regular global con 0,02%/0,05% es suficiente y no hay nada que optimizar: el coste de ida y vuelta es 0,10% del nominal y se diluye en cualquier movimiento relevante.

Si operas como taker varias veces por semana, el objetivo es bajar a la ruta maker-taker (0,07%) o maker-maker (0,04%). Eso significa trabajar con órdenes límite y aceptar el riesgo de no ser llenado. En volumen alto, comparar venues también tiene sentido, siempre que la plataforma alternativa opere legalmente en tu jurisdicción.

Si estás en la EEE, el primer paso no es mirar la tarifa sino confirmar que tienes abierta la cuenta de derivados (X-Perps). Sin ella no hay futuros, y la tabla de spot que aplica a tu cuenta puede ser distinta según la fuente que consultes.

Antes de enviar la primera orden, confirma dos cosas en tu panel: la tarifa maker/taker que aparece asociada a tu cuenta (no la de la tabla pública, que puede corresponder a otra región) y el horario de la próxima liquidación de funding del contrato que vas a operar. Con esos dos datos, el número que veas en el historial de órdenes cuadrará con lo que calculaste aquí.

👉 [Registrarte en OKX y comprobar tu tarifa real de futuros antes de operar](https://okx.com/join/CASH20)
