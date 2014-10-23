<!DOCTYPE HTML>
<html>
<head>
    <link rel="stylesheet/less" href="/themes/ribbit/css/style.less">
    <script src="/themes/ribbit/js/less.js"></script>
</head>
<body>
    <header>
        <div class="wrapper">
            <img src="/assets/images/logo.png">
            <span>Twitter Clone</span>

            <?php if ($this->auth->is_logged_in()) : ?>
              <a href="<?= site_url('logout') ?>">Logout</a>
            <?php else: ?>

              <?= form_open(LOGIN_URL, 'class="login"') ?>
                <input type="hidden" name="redirect_url" value="/">

                <input type="email" name="login" placeholder="Email">
                <input type="password" name="password" placeholder="Password">
                <input type="submit" name="log-me-in" value="Login">
              <?= form_close(); ?>

            <?php endif; ?>
            </p>
      </div>
   </header>
   <div id="content">
      <div class="wrapper">
        <?= Template::content(); ?>
      </div>
   </div>
   <footer>
      <div class="wrapper">
         Ribbit - A Twitter Clone Tutorial<img src="/assets/images/logo-nettuts.png">
      </div>
   </footer>
</body>
</html>