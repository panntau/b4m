<template>
  <header class="header-black" id="header-section2">
    <!-- nav -->
    <b-navbar togglable="sm" class="bg-black tz-header-bg no-margin alt-font dark-header  shrink-transparent-header-dark header-border-light">
        <div class="container navigation-menu">
            <b-row>
                <!-- logo -->
                <b-col md="3" sm="4" xs="9">
                    <a href="#home" class="inner-link">
                        <img alt="" src="~/assets/images/logoB4M_big.png">
                    </a>
                </b-col>
                <!-- end logo -->
                <b-col md="9"  sm="8" xs="3" class="position-inherit">
                    <b-navbar-toggle target="bs-example-navbar-collapse-1">
                      <div class="burger">
                          <span class="icon-bar"></span>
                          <span class="icon-bar"></span>
                          <span class="icon-bar"></span>
                      </div>
                      <div class="icon-name">Menu</div>
                    </b-navbar-toggle>
                    <!-- <button data-target="#" data-toggle="collapse" class="navbar-toggle collapsed" type="button">
                    </button> -->
                    <b-collapse id="bs-example-navbar-collapse-1" is-nav class="pull-right">
                        <b-nav>
                            <b-nav-item class="propClone" href="#content-section39" id="ui-id-28">
                              <span class="inner-link text-white" >
                                O nás
                              </span>
                            </b-nav-item>
                            <b-nav-item class="propClone">
                                <a class="inner-link text-white" href="#content-section21" id="ui-id-31">Služby</a>
                            </b-nav-item>
                            <b-nav-item class="propClone">
                                <a class="inner-link text-white" href="#portfolios-section3" id="ui-id-32">Portfolio</a>
                            </b-nav-item>
                            <b-nav-item class="propClone">
                                <a class="inner-link text-white" href="#title-section2" id="ui-id-33">Reference</a>
                            </b-nav-item>
                            <b-nav-item class="propClone">
                                <a class="inner-link text-white" href="#clients-section1" id="ui-id-34">Partneři</a>
                            </b-nav-item>
                            <b-nav-item class="propClone sm-no-border">
                                <a class="inner-link text-white" href="#contact-section9" id="ui-id-35">Kontakt</a>
                            </b-nav-item>
                            <!-- <b-nav-item class="nav-button propClone sm-no-margin-tb float-left btn-medium"><a href="#contact-section9" class="inner-link btn btn-small propClone bg-deep-red text-black border-radius-0 font-weight-300 sm-padding-nav-btn sm-display-inline-block" style="color: #fff; font-size: 14px; font-weight: 500; font-family: 'Montserrat', sans-serif; text-transform: none;" id="ui-id-15">Začít projekt</a></b-nav-item> -->
                        </b-nav>
                    </b-collapse>
                </b-col>
            </b-row>
        </div>
    </b-navbar>
    <!-- end nav -->
  </header>
</template>

<style scoped>
/* ===================================
    Navbar
====================================== */

.navbar {
  padding: 15px 0;
  z-index: 999;
  width: 100%;
  border-radius: 0;
  border: 0;
}
.navbar img {
  max-height: 45px;
}
.navbar li {
  margin: 13px 20px;
}
.navbar li:last-child {
  margin-right: 0;
}
.navbar li a {
  font-size: 12px;
  padding: 0;
  cursor: pointer !important;
  border-bottom: 1px solid transparent;
}
.navbar li a:hover {
  opacity: 0.8;
}
.navbar li a.active {
  opacity: 0.8;
}
.navbar .nav-button {
  margin: 10px 0 8px 30px;
}
.navbar .nav-button i {
  margin-right: 5px;
}
.navbar .nav-button a {
  padding: 3px 17px 2px !important;
  border: 1px solid transparent;
  font-size: 10px;
}
.navbar-collapse {
  padding: 0;
}
header .container {
  position: relative;
  min-height: 0;
}
header .row {
  align-items: center;
  display: flex;
  height: auto;
}
.header-margin-top {
  margin-top: 86px;
}
.navbar.shrink-nav {
  position: fixed !important;
  top: 0;
}
.navbar.shrink-nav.shrink {
  padding: 11px 0;
  background: rgba(0, 0, 0, 0.7);
}
.header-margin-top-big {
  margin-top: 134px;
}
.header-margin-top-medium {
  margin-top: 138px;
}
.navbar.shrink-nav.shrink .header-bottom {
  padding: 11px 0;
}

/* transparent header */
.shrink-transparent-header-dark.shrink {
  background: #000000 !important;
}
.shrink-transparent-header-light.shrink {
  background: #ffffff !important;
}
.shrink-transparent-header-light.shrink.navbar li a {
  color: #282828;
}
.shrink-transparent-header-light.shrink.navbar .nav-button a {
  border: 2px solid #000;
  color: #fff;
}

/* header border bottom */
.header-border-light {
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}
.header-border-dark {
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
}
.light-header.navbar li.active a {
  border-bottom: 1px solid rgba(0, 0, 0, 0.3);
}
.dark-header.navbar li.active a {
  border-bottom: 1px solid rgba(255, 255, 255, 0.3);
}
.icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
  background: #fff;
}
.burger {
  margin: 0 10px;
}
.navbar-toggler {
  display: flex;
  color: #fff;
}
.navbar-toggler .icon-bar + .icon-bar {
  margin-top: 4px;
}
</style>
