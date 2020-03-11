---
title: Iteración de punto fijo
linktitle: Punto fijo
toc: true
type: docs
publishDate: "2020-02-25T10:30:00-06:00"
draft: false
menu:
  analisis:
    parent: Algoritmos
    weight: 2

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
# weight: 2
---

El método de iteración de punto fijo requiere el siguiente teorema para garantizar la convergencia a un resultado

{{% alert note %}}
Sea $g\in C[a,b]$ tal que $g(x)\in[a,b]$ para todas las $x$ en $[a,b]$. Suponga, además, que existe $g'$ en $(a,b)$ y que existe una constante $0<k<1$ con 
$$
|g'(x)|\leq k, \text{ para toda }x\in (a,b).
$$
Entonces, para cualquier número $p_0$ en $[a,b]$, la sucesión definida por 
$$
p_n=g(p_{n-1}), \qquad n\geq 1,
$$
converge al único punto fijo $p$ en $[a,b]$.
{{% /alert %}}

Bajo las condiciones del teorema el algoritmo siempre converge. Las cotas de error al aproximar $p_n$ al punto fijo están dadas por
$$
|p_n-p|\leq k^n \max\\{p_0-a,b-p_0\\}
$$
y
$$
|p_n-p| \leq \dfrac{k^n}{1-k}|p_1-p_0|, \text{  para toda }n\geq 1.
$$

## Diagrama de flujo

<center>
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" width="223px" viewBox="-0.5 -0.5 223 552" content="&lt;mxfile host=&quot;www.draw.io&quot; modified=&quot;2020-02-26T23:59:28.905Z&quot; agent=&quot;Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.130 Safari/537.36&quot; etag=&quot;TjKyIJgBL7D5mPuq8Ywl&quot; version=&quot;12.7.8&quot; type=&quot;onedrive&quot;&gt;&lt;diagram id=&quot;C5RBs43oDa-KdzZeNtuy&quot; name=&quot;Page-1&quot;&gt;7Vtbd+I2EP41Pqd9CMe2fOMxQLLZ3TRn26TN5lHYAlxsyzVmA/n1HWEZX8YBQjEkdPMA1kgaSTOf5yaikH64+JTQePIb91ig6Kq3UMhA0XXHMuFTEJYZwXC0jDBOfC8jqQXh3n9hGVHLqXPfYzNJy0gp50Hqx1Wiy6OIuWmFRpOEP1eHjXjgVQgxHTNEuHdpgKmPvpdOMipR1YJ+w/zxRK5s5R0hzcdKwmxCPf5cIpErhfQTztPsKVz0WSBEl4vl8fPyMbidWp++/D77h/7Z+/pw99dFxuz6LVPWJ0hYlO7NWvPvZuHo6x/JA/s+f3n4cju4eZZT1B80mEtxfY581+fyxOkyl2LC55HHBCtNIb3niZ+y+5i6ovcZYAO0SRoGsnvEo1QCQQMx9cYBnQktqvA8SxM+XWtCjF7LVXSP/CDo84Anq2WJR5kzctfTSj2W67DhCHrkCViSskVN41vkpa2VCNhnPGRpsoR5kktXykbCPkfBc4Gh/M2YlOBD5DAqUTte8y1UAw9SO2/QlIY0dctn4rWkqfi2AthAb5jA01g8+dE4YTMQrOijoVBQNJyJrxmPFHGY+gzqMXe+mkCusfonPBzOZ9tVX1Um4OCahn4gZHjDgh8s9V3aABAa+OMIGi4ojCXNKIEl4VDQsorWA4flBxfGuwKOpXfMCnQ0C2NHy/FUBo/TFnh0BJ46KjJIVEhXUZpQD9R1Kbak6LC0Olx91aFTnxnPo5SLPQlbQsXuYrxenQkDW59kq4R00RHTAQugZh6B+6gDEnAWi0fQFQ0CFvBxQkOxNEt8kJkAUbXvW9Gx1Xy9HyiRjkYqWHJ2hJLVFpRsBKUpfE0VvadtcBrqR5K649SlrttY7HaD1Nuz/thR3yt9olwOkNBBGGlVssi6CpGBIQ4uZUfoe56Y3gOX4b/Q4YqVUFnM/ShdncXsKeZA8JqDu5GWu03na3ZUtVv6q6rDwOogDerQW1MH9sZi4+Nf4l/P5SXoqps0QJrCIadjHzUiwl5tunYzK+cyBUey2vNW56PY/cVFDJ/roZlPirHn2TkUej+6tK2OVlVfgz3rGh2THNGR5Ca2pL5rP0LiBk6QKbKPJG6HdCynIm+TNPiPbofYWN5Ga/I2G4LAurAj71Kk3MJZiJzNd6syZgs//V56fhJWDaLdrDVYSCO3aixlI1uEeShL30XGsDs+T1y26VzNuihJ2mxwDTktYQFN/R/VvTXJXq7wTXjEQtWagYJ9u6bA7AByXjk/r7PS66zqr15KkzFLESfQGF2Whkmn/eqeYaXaQrqqbtwanmFVJsBDtokCnWtN/AfAWgiwd7gwcRbhjmbXQNQQ5h83wMFh/t7GojAQT6We0xgLKa/sTdowTn9nRqUeRO1sVLp1VvUawytG5WAvsXMaIAFckmVpkmg+lfuKaavWsQCo7wjAs/FqCIBa3Wi1jEDdaEAgKn5drapUsm418v8WXwzVThc4cxADI/Hh8ggcA+Bme6VLFGBlbhLTGS7Rojfkf1LtqlbcDRM7QU1vyDDNtrygfsCQ+QMYr61GyT6pUdJRMRQlSztbJRvz0o5slg4bYcFpyilZ19qclJUQZnRJBWMdVdW24GzVKpmYNf86rW1vau/qTU/rTk2ENrJ3QKcbiNexHerPkK6xGLwdhafNKroIhca+KISZCIVHTizyrf9EYbUavj21NU6KQoJRuHdu4WBeR7aFBCcX51qj2nwhZDRUuI9asTLwlZz4bcgCKeOD3sfhGixxTCTyY9/BGfrhrPBbLhUKK1yNXc2PYoWNk0akOqrKGOqeRpigWhGp5+Mt22CjqcBzkEhA3YjBtrF0NhDBN1uoZHOoqy3DemWlVm+qDFwnOutf59Svq8ipr6sMfFV4IBNw2uuqvHa9PbUk78tWmPW76/3diXmwwhw0i1/rZ8OL/3ggV/8C&lt;/diagram&gt;&lt;/mxfile&gt;" onclick="(function(svg){var src=window.event.target||window.event.srcElement;while (src!=null&amp;&amp;src.nodeName.toLowerCase()!='a'){src=src.parentNode;}if(src==null){if(svg.wnd!=null&amp;&amp;!svg.wnd.closed){svg.wnd.focus();}else{var r=function(evt){if(evt.data=='ready'&amp;&amp;evt.source==svg.wnd){svg.wnd.postMessage(decodeURIComponent(svg.getAttribute('content')),'*');window.removeEventListener('message',r);}};window.addEventListener('message',r);svg.wnd=window.open('https://www.draw.io/?client=1&amp;lightbox=1&amp;edit=_blank');}}})(this);" style="cursor:pointer;max-width:100%;max-height:552px;"><defs/><g><rect x="30" y="0" width="65" height="30" rx="4.5" ry="4.5" fill="#dae8fc" stroke="#6c8ebf" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 63px; height: 1px; padding-top: 15px; margin-left: 31px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: all; white-space: normal; word-wrap: normal; ">Inicio</div></div></div></foreignObject><text x="63" y="19" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">Inicio</text></switch></g><path d="M 62.5 140 L 122.5 180 L 62.5 220 L 2.5 180 Z" fill="#dae8fc" stroke="#6c8ebf" stroke-miterlimit="10" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 110px; height: 1px; padding-top: 178px; margin-left: 8px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: all; white-space: normal; word-wrap: normal; ">Los datos<br />ingresados son <br />adecuados?</div></div></div></foreignObject><text x="63" y="182" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">Los datos...</text></switch></g><path d="M 3.13 120 L 27.13 60 L 123.13 60 L 99.13 120 Z" fill="#dae8fc" stroke="#6c8ebf" stroke-miterlimit="10" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 118px; height: 1px; padding-top: 90px; margin-left: 4px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: all; white-space: normal; word-wrap: normal; ">   Entrada: a, b,<br /> punto inicial p <br />error, max. iteraciones</div></div></div></foreignObject><text x="63" y="94" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">Entrada: a, b,...</text></switch></g><rect x="28.13" y="250" width="70" height="30" fill="#dae8fc" stroke="#6c8ebf" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 68px; height: 1px; padding-top: 265px; margin-left: 29px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: all; white-space: normal; word-wrap: normal; ">k=k+1</div></div></div></foreignObject><text x="63" y="269" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">k=k+1</text></switch></g><rect x="35.01" y="220" width="30" height="20" fill="none" stroke="none" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 230px; margin-left: 50px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: all; white-space: nowrap; ">Sí</div></div></div></foreignObject><text x="50" y="234" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">Sí</text></switch></g><rect x="30.01" y="300" width="68.75" height="30" fill="#dae8fc" stroke="#6c8ebf" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 67px; height: 1px; padding-top: 315px; margin-left: 31px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: all; white-space: normal; word-wrap: normal; ">x=g(p)</div></div></div></foreignObject><text x="64" y="319" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">x=g(p)</text></switch></g><path d="M 63.37 350 L 110.63 380 L 63.37 410 L 16.1 380 Z" fill="#dae8fc" stroke="#6c8ebf" stroke-miterlimit="10" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 93px; height: 1px; padding-top: 380px; margin-left: 17px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: all; white-space: normal; word-wrap: normal; ">k&lt;kmax y <br />|x-p|&gt;eps</div></div></div></foreignObject><text x="63" y="384" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">k&lt;kmax y...</text></switch></g><ellipse cx="63.37" cy="530" rx="39.685" ry="20" fill="#dae8fc" stroke="#6c8ebf" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 77px; height: 1px; padding-top: 530px; margin-left: 25px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: all; white-space: normal; word-wrap: normal; ">Fin</div></div></div></foreignObject><text x="63" y="534" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">Fin</text></switch></g><path d="M 122.5 180 L 142.5 180 Q 152.5 180 152.5 170 L 152.5 50 Q 152.5 40 142.5 40 L 68.87 40" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 63.62 40 L 70.62 36.5 L 68.87 40 L 70.62 43.5 Z" fill="#000000" stroke="#000000" stroke-miterlimit="10" pointer-events="all"/><rect x="115" y="160" width="30" height="20" fill="none" stroke="none" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 170px; margin-left: 130px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: all; white-space: nowrap; ">No</div></div></div></foreignObject><text x="130" y="174" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">No</text></switch></g><path d="M 62.5 30 L 62.75 53.63" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 62.8 58.88 L 59.23 51.92 L 62.75 53.63 L 66.23 51.85 Z" fill="#000000" stroke="#000000" stroke-miterlimit="10" pointer-events="all"/><path d="M 63.13 120 L 62.7 133.64" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 62.54 138.88 L 59.26 131.78 L 62.7 133.64 L 66.25 132 Z" fill="#000000" stroke="#000000" stroke-miterlimit="10" pointer-events="all"/><path d="M 0 480 L 25 430 L 125 430 L 100 480 Z" fill="#dae8fc" stroke="#6c8ebf" stroke-miterlimit="10" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 123px; height: 1px; padding-top: 455px; margin-left: 1px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: all; white-space: normal; word-wrap: normal; ">  El punto fijo es x<br />o no converge <br />en kmax pasos </div></div></div></foreignObject><text x="63" y="459" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">El punto fijo es x...</text></switch></g><path d="M 63.13 220 L 63.13 243.63" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 63.13 248.88 L 59.63 241.88 L 63.13 243.63 L 66.63 241.88 Z" fill="#000000" stroke="#000000" stroke-miterlimit="10" pointer-events="all"/><path d="M 64.04 278.95 L 63.94 293.66" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 63.91 298.91 L 60.46 291.89 L 63.94 293.66 L 67.46 291.93 Z" fill="#000000" stroke="#000000" stroke-miterlimit="10" pointer-events="all"/><path d="M 64.38 330 L 63.69 343.64" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 63.42 348.88 L 60.28 341.71 L 63.69 343.64 L 67.27 342.07 Z" fill="#000000" stroke="#000000" stroke-miterlimit="10" pointer-events="all"/><path d="M 63.37 410 L 62.78 423.64" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 62.55 428.88 L 59.35 421.74 L 62.78 423.64 L 66.35 422.04 Z" fill="#000000" stroke="#000000" stroke-miterlimit="10" pointer-events="all"/><rect x="30.01" y="410" width="30" height="20" fill="none" stroke="none" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 420px; margin-left: 45px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: all; white-space: nowrap; ">No</div></div></div></foreignObject><text x="45" y="424" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">No</text></switch></g><rect x="152.5" y="365" width="68.75" height="30" fill="#dae8fc" stroke="#6c8ebf" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 67px; height: 1px; padding-top: 380px; margin-left: 154px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: all; white-space: normal; word-wrap: normal; ">p=x</div></div></div></foreignObject><text x="187" y="384" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">p=x</text></switch></g><path d="M 110.63 380 L 146.13 380" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 151.38 380 L 144.38 383.5 L 146.13 380 L 144.38 376.5 Z" fill="#000000" stroke="#000000" stroke-miterlimit="10" pointer-events="all"/><path d="M 186.88 365 L 186.53 240 Q 186.5 230 176.5 230 L 68.87 230" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 63.62 230 L 70.62 226.5 L 68.87 230 L 70.62 233.5 Z" fill="#000000" stroke="#000000" stroke-miterlimit="10" pointer-events="all"/><rect x="115" y="360" width="30" height="20" fill="none" stroke="none" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject style="overflow: visible; text-align: left;" pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 370px; margin-left: 130px;"><div style="box-sizing: border-box; font-size: 0; text-align: center; "><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: #000000; line-height: 1.2; pointer-events: all; white-space: nowrap; ">Sí</div></div></div></foreignObject><text x="130" y="374" fill="#000000" font-family="Helvetica" font-size="12px" text-anchor="middle">Sí</text></switch></g><path d="M 62.5 480 L 62.92 503.63" fill="none" stroke="#000000" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 63.01 508.88 L 59.39 501.95 L 62.92 503.63 L 66.39 501.82 Z" fill="#000000" stroke="#000000" stroke-miterlimit="10" pointer-events="all"/></g><switch><g requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"/><a transform="translate(0,-5)" xlink:href="https://desk.draw.io/support/solutions/articles/16000042487" target="_blank"><text text-anchor="middle" font-size="10px" x="50%" y="100%">Viewer does not support full SVG 1.1</text></a></switch></svg>
</center>

## Código

El siguiente codigo implementa el método de punto fijo en C++:

```cpp
///////////////////////////////////////////////////////////////////////////////////
// Programa para hallar el punto fijo de una función g entre a y b.		 //
// El programa requiere un subprograma para la función g, los puntos 		 //
// a y b, la tolerancia de error eps, y el máximo número 			 //
// de iteraciones permitidas, kmax. 						 //
// El programa muestra una tabla con los valores de x y su evaluación en g.	 //
///////////////////////////////////////////////////////////////////////////////////
# include <iomanip>
# include <math.h> // para log x
using namespace std; // Para usar cout

long double f(long double x); // Declara la función f

int main(){
    int kmax;
    long double a, b, p, eps;
    cout << "Ingrese a, b, p, eps, kmax\n";
    cin >> a >> b >> p >> eps >> kmax;
    // Verificamos que los valores ingresados permitan usar el algoritmo
    while(b<a || isnan(f(a)) || isnan(f(b)) || f(a)<a || f(b)>b){
        if(b<a)
            cout << "Ingrese un intervalo de la forma (a,b) con a<b\n";
        else if(isnan(f(a)))
            cout << "La evaluacion en " << a << " no esta definida\n";
        else if(isnan(f(b)))
            cout << "La evaluacion en " << b << " no esta definida\n";
        else if(f(a)<a || f(b)>b)
            cout << "La funcion no satisface el Teorema  b\n";
        cout << "Ingrese nuevamente valores para a y b\n";
        cin >> a >> b;
    }
    cout << "Los valores ingresados son \n";
    cout << "a= " << a << "  b= " << b << " p= " <<p;
    cout << " eps = " << eps << "  kmax = " << kmax << endl;
    cout << "Los resultados son\n"; // Muestra el encabezado de la tabla
    cout << "k" << setw(16) << "x" << setw(22) << "f(x)\n";
    int k=1;
    cout.setf(ios::fixed);
    while ((k<=kmax) && (fabs(f(p)-p)>eps)){
        // Muestra los valores de k, x, y, a, b
        cout << k << setprecision(9) << setw(20) << p << setw(20) << f(p)
             << endl;
        k++; // incrementa el contador del ciclo
        p=f(p);
    };
    if (fabs(f(p)-p)<=eps) cout << "El punto fijo de f es " << f(p); 
    else if (k>kmax) cout << "no converge";
    return 0;
}
// El subprograma para ingresar la función f
long double f(long double x){
    return x-(x*x*x+4*x*x-10)/(3*x*x+8*x);
}
```


