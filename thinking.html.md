<!DOCTYPE html>

<html lang="en">

<head>

  <meta charset="UTF-8" />

  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <title>Thinking - Foci Capital</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500&display=swap" rel="stylesheet">

  <style>

    @font-face {

      font-family: 'CP Company';

      src: url('fonts/CPCompany-Light.woff2') format('woff2'),

           url('fonts/CPCompany-Light.woff') format('woff');

      font-weight: 300;

      font-style: normal;

      font-display: swap;

    }

    * {

      box-sizing: border-box;

    }



    body {

      margin: 0;

      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;

      color: #1a1a1a;

      background-color: #FBF7F0;

      line-height: 1.6;

    }



    /* HEADER */

    header {

      width: 100%;

      max-width: 100%;

      height: 81px;

      padding: 24px 40px;

      font-size: 14px;

      font-weight: 400;

      letter-spacing: 0.5px;

      border-bottom: 1px solid #e5e5e5;

      background-color: #FBF7F0;

      display: flex;

      justify-content: space-between;

      align-items: center;

      box-sizing: border-box;

      text-align: right;

    }



    header .logo {

      font-size: 20px;

      font-weight: 400;

      letter-spacing: 0.5px;

      color: #1a1a1a;

      text-decoration: none;

      display: inline-block;

    }

    header .logo:hover {

      opacity: 0.7;

    }



    header nav {

      display: flex;

      align-items: center;

      gap: 32px;

      margin-left: auto;

    }



    header nav a {

      color: #1a1a1a;

      text-decoration: none;

      font-size: 14px;

      font-weight: 400;

      letter-spacing: 2px;

      text-transform: uppercase;

      transition: opacity 0.2s ease;

      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;

    }



    header nav a:hover {

      opacity: 0.7;

    }



    /* CONTENT SECTION */

    .content-section {

      max-width: 1000px;

      margin: 0 auto;

      padding: 100px 40px 100px;

      text-align: left;

    }



    .content-section h1 {

      font-size: 64px;

      font-weight: 400;

      line-height: 1.2;

      margin-top: 0px;

      margin-bottom: 0px;

      box-sizing: content-box;

      letter-spacing: 0;

      color: #1a1a1a;

      font-family: Georgia, "Times New Roman", Times, serif;

      text-align: left;

    }



    .content-section p {

      font-size: 18px;

      margin-bottom: 24px;

      color: #1a1a1a;

      font-weight: 400;

      line-height: 1.8;

    }



    /* FOOTER */

    footer {

      display: grid;

      text-align: center;

      padding: 30px 10px;

      font-size: 13px;

      color: #ffffff;

      background-color: #007354;

      border-top: none;

      margin-top: 0;

      letter-spacing: 0.2px;

      border-style: solid;

      border-width: 1px;

      border-color: rgba(0, 0, 0, 1);

      box-shadow: 0px 4px 12px 0px rgba(0, 0, 0, 0.15);

      flex-wrap: wrap;

    }



    /* ===== RESPONSIVE STYLES ===== */

    @media (max-width: 768px) {

      header {

        padding: 20px 24px;

        font-size: 13px;

        flex-wrap: wrap;

        gap: 16px;

      }



      header .logo {

        font-size: 18px;

      }



      header nav {

        gap: 20px;

      }



      header nav a {

        font-size: 12px;

      }



      .content-section {

        padding: 50px 24px 50px;

      }



      .content-section h1 {

        font-size: 64px;

      }



      .content-section p {

        font-size: 16px;

      }

    }



    @media (max-width: 480px) {

      header {

        padding: 18px 20px;

        flex-direction: column;

        align-items: flex-start;

      }



      header .logo {

        font-size: 16px;

      }



      header nav {

        width: 100%;

        justify-content: flex-end;

        gap: 16px;

        margin-top: 8px;

      }



      header nav a {

        font-size: 11px;

      }



      .content-section {

        padding: 60px 20px 40px;

      }



      .content-section h1 {

        font-size: 36px;

      }



      .content-section p {

        font-size: 15px;

      }

    }

  </style>

</head>



<body>



  <!-- HEADER -->

  <header>

    <a href="index.html" class="logo">FOCI CAPITAL</a>

    <nav>

      <a>ABOUT US</a>

      <a href="thinking.html">THINKING</a>

      <a href="mailto:darda.samkeet@gmail.com">CONTACT US</a>

    </nav>

  </header>



  <!-- CONTENT -->

  <section class="content-section">

    <h1>Thinking</h1>

    <p>Welcome to our thinking section. Here we share insights, perspectives, and ideas that shape our approach to building the future together.</p>

    <p>This page is a space for our thoughts, reflections, and strategic considerations as we navigate the evolving landscape of capital and innovation.</p>

  </section>



  <!-- FOOTER -->

  <footer>

    © 2025 Foci Capital. All rights reserved.

  </footer>



</body>

</html>
