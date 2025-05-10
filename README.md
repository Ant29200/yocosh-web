<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no" />
    <title>YOCOSH - Yogurt Natural Peruano</title>
    <style>
        /* Reset and base */
        * {
            margin: 0; padding: 0; box-sizing: border-box;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #f2ebe3, #fff);
            color: #3a3a3a;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            user-select: none;
        }
        header {
            background: #d52b1e; /* Peruvian red */
            color: white;
            padding: 1.6rem 1rem;
            text-align: center;
            box-shadow: 0 4px 10px rgba(213,43,30,0.6);
            position: sticky;
            top: 0;
            z-index: 100;
            font-family: 'Georgia', serif;
        }
        header h1 {
            font-weight: 900;
            font-size: 2.8rem;
            letter-spacing: 0.15em;
            font-family: 'Arial Black', Arial, sans-serif;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.3);
            user-select: none;
            text-transform: uppercase;
        }
        header p {
            font-weight: 600;
            margin-top: 0.3rem;
            font-size: 1.1rem;
            font-style: italic;
            text-shadow: 1px 1px 1px rgba(0,0,0,0.2);
        }
        main {
            flex: 1;
            padding: 1.2rem 1.5rem 3rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            max-width: 620px;
            margin: 0 auto;
        }
        .hero-image {
            width: 100%;
            max-width: 420px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(213,43,30,0.3);
            margin-bottom: 1.8rem;
            object-fit: cover;
            user-select: none;
        }
        .intro-text {
            font-size: 1.15rem;
            line-height: 1.68;
            text-align: center;
            padding: 0 1rem;
            margin-bottom: 2.2rem;
            color: #4a4a4a;
            font-weight: 500;
        }
        .features {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            gap: 1.25rem;
            width: 100%;
            margin-bottom: 2.6rem;
        }
        .feature {
            background: #fff8f6;
            border: 2px solid #d52b1e;
            border-radius: 18px;
            box-shadow: 0 6px 20px rgba(213,43,30,0.18);
            padding: 1.3rem 1.6rem;
            flex: 1 1 230px;
            min-width: 230px;
            user-select: none;
            transition: transform 0.35s cubic-bezier(0.49, 0.03, 0, 1);
            cursor:pointer;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .feature:hover,
        .feature:focus {
            transform: translateY(-8px);
            box-shadow: 0 12px 30px rgba(213,43,30,0.35);
            outline: none;
        }
        .feature-icon {
            width: 48px;
            height: 48px;
            margin-bottom: 0.8rem;
            user-select: none;
        }
        .feature h3 {
            color: #d52b1e;
            margin-bottom: 0.6rem;
            font-size: 1.35rem;
            text-align: center;
            font-weight: 800;
            letter-spacing: 0.03em;
            user-select: none;
        }
        .feature p {
            color: #66504a;
            font-size: 1rem;
            text-align: center;
            font-weight: 500;
            line-height: 1.4;
        }
        .order-section {
            width: 100%;
            background: #d52b1e;
            border-radius: 25px;
            padding: 1.3rem 1.5rem;
            color: white;
            box-shadow: 0 9px 30px rgba(213,43,30,0.6);
            user-select: none;
            text-align: center;
            font-weight: 700;
        }
        .order-section h2 {
            margin-bottom: 0.7rem;
            font-size: 2rem;
            font-family: 'Georgia', serif;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.25);
        }
        .order-section p {
            margin-bottom: 1.3rem;
            font-size: 1.25rem;
            font-weight: 600;
            letter-spacing: 0.03em;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.15);
        }
        .btn-order {
            background: #fff8f6;
            color: #d52b1e;
            font-weight: 800;
            font-size: 1.2rem;
            border: none;
            border-radius: 50px;
            padding: 0.75rem 2.6rem;
            cursor: pointer;
            box-shadow: 0 6px 18px rgba(213,43,30,0.5);
            transition: background-color 0.32s ease, color 0.32s ease, box-shadow 0.3s ease;
            user-select: none;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            text-transform: uppercase;
        }
        .btn-order:hover,
        .btn-order:focus {
            background: #ab1e14;
            color: white;
            outline: none;
            box-shadow: 0 15px 36px rgba(171,30,20,0.85);
        }
        footer {
            background: #d52b1e;
            color: white;
            text-align: center;
            padding: 1rem 1rem;
            font-size: 0.95rem;
            font-family: 'Georgia', serif;
            user-select: none;
        }
        /* Responsive */
        @media (max-width: 650px) {
            main {
                padding: 1rem 1rem 2rem;
                max-width: 100%;
            }
            .features {
                flex-direction: column;
                align-items: center;
            }
            .feature {
                min-width: 88%;
            }
            .hero-image {
                max-width: 100%;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>YOCOSH</h1>
        <p>El yogurt natural peruano que refresca y nutre</p>
    </header>
    <main>
        <img class="hero-image" src="https://images.unsplash.com/photo-1615486360939-b45aabed60ec?auto=format&fit=crop&w=700&q=80" alt="Vasos de yogurt peruano Yocosh decorados con frutas" />
        <p class="intro-text">
            Descubre YOCOSH, el yogurt natural peruano elaborado con ingredientes frescos y saludables de nuestras tierras. Perfecto para empezar tu día con energía o para un snack delicioso y nutritivo. Sin aditivos, con probióticos vivos y el sabor auténtico del Perú.
        </p>
        <section class="features" aria-label="Características del yogurt YOCOSH">
            <article class="feature" tabindex="0" aria-describedby="desc-natural">
                <img class="feature-icon" src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/64/d52b1e/natural-food.png" alt="Icono de alimento natural" aria-hidden="true" />
                <h3>100% Natural</h3>
                <p id="desc-natural">Solo ingredientes frescos de nuestra tierra peruana, sin conservantes ni químicos.</p>
            </article>
            <article class="feature" tabindex="0" aria-describedby="desc-probioticos">
                <img class="feature-icon" src="https://img.icons8.com/ios-filled/50/d52b1e/intestines.png" alt="Icono de intestinos salud" aria-hidden="true" />
                <h3>Probióticos</h3>
                <p id="desc-probioticos">Con bacterias vivas que mejoran tu salud digestiva y defienden tu sistema inmune.</p>
            </article>
            <article class="feature" tabindex="0" aria-describedby="desc-sabor">
                <img class="feature-icon" src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/64/d52b1e/cream.png" alt="Icono de crema y sabor" aria-hidden="true" />
                <h3>Sabor Auténtico</h3>
                <p id="desc-sabor">Cremoso, fresco y con ese toque peruano que te hará volver por más.</p>
            </article>
        </section>

        <section class="order-section" aria-label="Sección para realizar pedidos de yogurt YOCOSH">
            <h2>Realiza tu pedido</h2>
            <p>Contáctanos y recibe la frescura del yogurt YOCOSH directo a tu hogar, ¡rápido y fácil!</p>
            <button class="btn-order" id="orderBtn" aria-label="Hacer un pedido de YOCOSH">¡Pedir ahora!</button>
        </section>
    </main>
    <footer>
        &copy; 2025 YOCOSH - Inspirado por Perú. Todos los derechos reservados.
    </footer>
<script>
    const orderBtn = document.getElementById('orderBtn');
    orderBtn.addEventListener('click', () => {
        const phone = prompt("Para hacer tu pedido, por favor ingresa tu número telefónico (WhatsApp):");
        if (phone && phone.trim()) {
            const message = encodeURIComponent("Hola, quiero hacer un pedido de yogurt YOCOSH.");
            const whatsappUrl = `https://wa.me/${phone.replace(/\\D/g, '')}?text=${message}`;
            window.open(whatsappUrl, '_blank');
        } else {
            alert("Número inválido. Intenta de nuevo.");
        }
    });
</script>
</body>
</html>

