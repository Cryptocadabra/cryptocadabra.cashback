<template>
  <section class="faq" id="faq">
    <div class="container">
      <article class="page" itemscope="" itemtype="https://schema.org/FAQPage">
        <header class="page-header">
          <h1 class="page-title">Frequently Asked Questions</h1>
        </header>
        <div class="faq-search"></div>
        <div class="faq display-desktop">
          <div class="row">
            <div class="col-75">
              <ul id="faqContainer" class="faq__container">
                <li class="faq__content _mPS2id-t" id="99">
                  <ul>
                    <li
                      v-for="a in answerQueistion"
                      :key="a"
                      @click="isVisible(a)"
                      class="faq__text"
                      itemscope=""
                      itemprop="mainEntity"
                      itemtype="https://schema.org/Question"
                    >
                      <div class="faq__input">
                        <span class="faq-icon faq-icon--close">+</span>
                        <span class="faq-icon faq-icon--open">-</span>
                        <span itemprop="name"> {{ a.question }} </span>
                      </div>
                      <div
                        v-if="a.visible"
                        class="faq__reply faq-show"
                        itemscope=""
                        itemprop="acceptedAnswer"
                        itemtype="https://schema.org/Answer"
                      >
                        <div itemprop="">
                          <p>
                            <span
                              data-sheets-value='{"1":2,"2":"At first you sign up for a XX-hour/week plan with Lemon.io. Your project’s developer will report the amount of hours spent on your projects on a weekly basis. "}'
                              data-sheets-userformat='{"2":769,"3":{"1":0},"11":4,"12":0}'
                            >
                              {{ a.answear }}
                            </span>
                          </p>
                        </div>
                      </div>
                    </li>
                  </ul>
                </li>
              </ul>
            </div>
          </div>
          <div class="faq__bottom">
            <a href="" class="btn" data-wpel-link="internal"
              >I have another question</a
            >
          </div>
        </div>
      </article>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      isAnswerVisible: false,

      answerQueistion: [
        {
          question: "How does your business work?",
          answear:
            "The money comes into our account from the Binance affiliate program. Then we reback you a major amount (80%) of money. It's easy and profitable for everyone!",
          visible: false,
        },
        {
          question: "Is it legal?",
          answear:
            "In connection with partnerships agreements, we have the right to manage the money at our mind. That's why everything is fair!",
          visible: false,
        },
        {
          question: "What if I'm already an account?",
          answear:
            "Not a problem, you can re-create it. Please contact our support for a more detailed explanation.",
          visible: false,
        },
        {
          question: "What if you deceive me?",
          answear:
            "It's not in our best interest. The longer we cooperate, the more we will earn.",
          visible: false,
        },
        {
          question: "How much % cryptocadabra takes for itself?",
          answear:
            "The affiliate payout rate for Binance Spot trading is 40%. We give you 30% and keep 10% for the development of our service. We keep one quarter.",
          visible: false,
        },
      ],
    };
  },

  methods: {
    isVisible(q) {
      if (q.visible === true) {
        q.visible = false;
      } else {
        q.visible = true;
      }
    },
  },
};
</script>

<style scoped>
/**handles:slick-style,slick-theme,faq-style**/
.slick-slider {
  position: relative;
  display: block;
  box-sizing: border-box;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  -webkit-touch-callout: none;
  -khtml-user-select: none;
  -ms-touch-action: pan-y;
  touch-action: pan-y;
  -webkit-tap-highlight-color: transparent;
}
.slick-list {
  position: relative;
  display: block;
  overflow: hidden;
  margin: 0;
  padding: 0;
}
.slick-list:focus {
  outline: 0;
}
.slick-list.dragging {
  cursor: pointer;
  cursor: hand;
}
.slick-slider .slick-list,
.slick-slider .slick-track {
  -webkit-transform: translate3d(0, 0, 0);
  -moz-transform: translate3d(0, 0, 0);
  -ms-transform: translate3d(0, 0, 0);
  -o-transform: translate3d(0, 0, 0);
  transform: translate3d(0, 0, 0);
}
.slick-track {
  position: relative;
  top: 0;
  left: 0;
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.slick-track:after,
.slick-track:before {
  display: table;
  content: "";
}
.slick-track:after {
  clear: both;
}
.slick-loading .slick-track {
  visibility: hidden;
}
.slick-slide {
  display: none;
  float: left;
  height: 100%;
  min-height: 1px;
}
[dir="rtl"] .slick-slide {
  float: right;
}
.slick-slide img {
  display: block;
}
.slick-slide.slick-loading img {
  display: none;
}
.slick-slide.dragging img {
  pointer-events: none;
}
.slick-initialized .slick-slide {
  display: block;
}
.slick-loading .slick-slide {
  visibility: hidden;
}
.slick-vertical .slick-slide {
  display: block;
  height: auto;
  border: 1px solid transparent;
}
.slick-arrow.slick-hidden {
  display: none;
}
.slick-next,
.slick-prev {
  font-size: 0;
  line-height: 0;
  position: absolute;
  top: 50%;
  display: block;
  width: 20px;
  height: 20px;
  padding: 0;
  -webkit-transform: translate(0, -50%);
  -ms-transform: translate(0, -50%);
  transform: translate(0, -50%);
  cursor: pointer;
  color: transparent;
  border: none;
  outline: 0;
  background: 0 0;
}
.slick-next:focus,
.slick-next:hover,
.slick-prev:focus,
.slick-prev:hover {
  color: transparent;
  outline: 0;
  background: 0 0;
}
.slick-next:focus:before,
.slick-next:hover:before,
.slick-prev:focus:before,
.slick-prev:hover:before {
  opacity: 1;
}
.slick-next.slick-disabled:before,
.slick-prev.slick-disabled:before {
  opacity: 0.25;
}
.slick-next:before,
.slick-prev:before {
  font-size: 20px;
  line-height: 1;
  opacity: 0.75;
  color: #fff;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.slick-prev {
  left: -25px;
}
[dir="rtl"] .slick-prev {
  right: -25px;
  left: auto;
}

[dir="rtl"] .slick-prev:before {
  content: "â†’";
}
.slick-next {
  right: -25px;
}
[dir="rtl"] .slick-next {
  right: auto;
  left: -25px;
}
.slick-next:before {
  content: "â†’";
}

.slick-dotted.slick-slider {
  margin-bottom: 30px;
}
.slick-dots {
  position: absolute;
  bottom: -25px;
  display: block;
  width: 100%;
  padding: 0;
  margin: 0;
  list-style: none;
  text-align: center;
}
.slick-dots li {
  position: relative;
  display: inline-block;
  width: 20px;
  height: 20px;
  margin: 0 5px;
  padding: 0;
  cursor: pointer;
}
.slick-dots li button {
  font-size: 0;
  line-height: 0;
  display: block;
  width: 20px;
  height: 20px;
  padding: 5px;
  cursor: pointer;
  color: transparent;
  border: 0;
  outline: 0;
  background: 0 0;
}
.slick-dots li button:focus,
.slick-dots li button:hover {
  outline: 0;
}
.slick-dots li button:focus:before,
.slick-dots li button:hover:before {
  opacity: 1;
}
.slick-dots li button:before {
  font-size: 6px;
  line-height: 20px;
  position: absolute;
  top: 0;
  left: 0;
  width: 20px;
  height: 20px;
  content: "â€¢";
  text-align: center;
  opacity: 0.25;
  color: #000;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.slick-dots li.slick-active button:before {
  opacity: 0.75;
  color: #000;
}
/*! normalize.css v8.0.1 | MIT License | github.com/necolas/normalize.css */
html {
  line-height: 1.15;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
main {
  display: block;
}
h1 {
  font-size: 45em;
  margin: 0.67em 0;
}
hr {
  -webkit-box-sizing: content-box;
  box-sizing: content-box;
  height: 0;
  overflow: visible;
}
pre {
  font-size: 1em;
}
a {
  background-color: transparent;
}
abbr[title] {
  border-bottom: none;
  text-decoration: underline;
  -webkit-text-decoration: underline dotted;
  text-decoration: underline dotted;
}
b,
strong {
  font-weight: bolder;
}
code,
kbd,
samp {
  font-size: 1em;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sub {
  bottom: -0.25em;
}
sup {
  top: -0.5em;
}
img {
  border-style: none;
}
button,
input,
optgroup,
select,
textarea {
  font-size: 100%;
  line-height: 1.15;
  margin: 0;
}
button,
input {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
[type="button"],
[type="reset"],
[type="submit"],
button {
  -webkit-appearance: button;
}
[type="button"]::-moz-focus-inner,
[type="reset"]::-moz-focus-inner,
[type="submit"]::-moz-focus-inner,
button::-moz-focus-inner {
  border-style: none;
  padding: 0;
}
[type="button"]:-moz-focusring,
[type="reset"]:-moz-focusring,
[type="submit"]:-moz-focusring,
button:-moz-focusring {
  outline: 0.0625rem dotted ButtonText;
}
fieldset {
  padding: 0.35em 0.75em 0.625em;
}
legend {
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  color: inherit;
  display: table;
  max-width: 100%;
  padding: 0;
  white-space: normal;
}
progress {
  vertical-align: baseline;
}
textarea {
  overflow: auto;
}
[type="checkbox"],
[type="radio"] {
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  padding: 0;
}
[type="number"]::-webkit-inner-spin-button,
[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
[type="search"] {
  -webkit-appearance: textfield;
  outline-offset: -0.125rem;
}
[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
::-webkit-file-upload-button {
  -webkit-appearance: button;
  font: inherit;
}
details {
  display: block;
}
summary {
  display: list-item;
}
[hidden],
template {
  display: none;
}
*,
:after,
:before,
html {
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
}
body {
  background: #000;
  overflow-x: hidden;
}
p {
  margin: 0;
}
hr {
  background-color: #ccc;
  border: 0;
  height: 0.0625rem;
  margin-bottom: 1.5em;
}
img {
  height: auto;
  max-width: 100%;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
}
figure {
  margin: 1em 0;
}
ol,
ul {
  margin: 0;
  padding: 0;
  list-style-position: inside;
}
ul {
  list-style: none;
  list-style-position: inside;
}
ol {
  list-style: decimal;
  list-style-position: inside;
}
li > ol,
li > ul {
  margin-bottom: 0;
  margin-left: 0;
}
dt {
  font-weight: 700;
}
dd {
  margin: 0 1.5em 1.5em;
}
table {
  margin: 0 0 1.5em;
  width: 100%;
}
p {
  margin-bottom: 0;
}
cite,
dfn,
em,
i {
  font-style: italic;
}
blockquote {
  margin: 0;
}
address {
  margin: 0 0 1.5em;
}
pre {
  background: #eee;
  line-height: 1.6;
  margin-bottom: 1.6em;
  max-width: 100%;
  overflow: auto;
  padding: 1.6em;
}
code,
kbd,
pre,
tt,
var {
  font-size: (0.9375 * 16) * 0.0625rem;
  font-size: 0.9375 * 1rem;
}
abbr,
acronym {
  border-bottom: 1px dotted #666;
  cursor: help;
}
ins,
mark {
  background: #fff9c0;
  text-decoration: none;
}
big {
  font-size: 125%;
}
:focus {
  outline: 0;
}
b,
strong {
  font-weight: 400;
}
h1,
h2,
h3,
h4,
h5,
h6 {
  clear: both;
  color: #fff;
  font-weight: 700;
  margin: 0;
}
h2,
h3,
h4,
h5,
h6 {
  max-width: 45rem;
}
h1 {
  font-size: 45px;
  font-weight: 700;
  text-transform: uppercase;
}
@media screen and (max-width: 600px) {
  h1 {
    font-size: 3.25rem;
    letter-spacing: 0.28125rem;
  }
}
h2 {
  font-size: 3.25rem;
}
h2,
h3 {
  line-height: 1.15;
  letter-spacing: 0.0625rem;
}
h3 {
  font-size: 2.5rem;
}
h4 {
  font-size: 2rem;
  line-height: 1.25;
  letter-spacing: 0.05rem;
}
h5 {
  font-size: 1.625rem;
  line-height: 1.31;
  letter-spacing: 0.04063rem;
}
body,
button,
input,
optgroup,
select,
textarea {
  color: #fff;
  font-weight: 300;
  font-size: 1.125rem;
  line-height: 1.56;
  text-transform: lowercase;
}
.blog-nav {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
}
@media screen and (max-width: 600px) {
  .blog-nav {
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -ms-flex-direction: column;
    flex-direction: column;
  }
}
.blog-nav li a {
  text-decoration: none;
  border: none;
}
.blog-nav li.focus > a,
.blog-nav li:hover > a {
  color: #dcff02;
}
.blog-nav li.focus > a:after,
.blog-nav li:hover > a:after {
  position: absolute;
  display: inline;
  content: "/";
}
.blog-nav li.current-menu-item,
.blog-nav li.current-menu-item a {
  color: #dcff02;
}
.blog-nav li.current-menu-item:after {
  position: absolute;
  display: inline;
  content: "/";
}
.footer-navigation {
  width: 100%;
}
.footer-navigation ul {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
  width: 100%;
  padding: 0;
  margin: 0;
  list-style: none;
}
@media screen and (max-width: 600px) {
  .footer-navigation ul {
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -ms-flex-direction: column;
    flex-direction: column;
  }
}
.footer-navigation ul a {
  text-decoration: none;
  color: #fff;
  font-size: 1rem;
  font-weight: 300;
  line-height: 1.65;
  border: none;
}
@media screen and (max-width: 600px) {
  .footer-navigation ul li {
    margin-bottom: 1.5625rem;
  }
}
.footer-navigation--black ul a {
  color: #000;
}
.footer-navigation .menu > li {
  padding: 1.25rem 0;
}
@media screen and (max-width: 600px) {
  .footer-navigation .menu > li {
    padding: 0.3125rem 0;
  }
}
.footer-navigation .sub-menu {
  position: absolute;
  right: 0;
  bottom: 4.0625rem;
  display: none;
  opacity: 0;
  width: 90vw;
  max-width: 51.25rem;
  padding: 1.5625rem 2.8125rem;
  -webkit-column-count: 3;
  -moz-column-count: 3;
  column-count: 3;
  background-color: #aa75e3;
}
.footer-navigation .sub-menu li {
  margin-bottom: 0.625rem;
}
.footer-navigation .sub-menu:after {
  position: absolute;
  display: block;
  content: "";
  width: 1.5625rem;
  height: 1.5625rem;
  right: 1.5625rem;
  bottom: -0.625rem;
  -webkit-transform: rotate(45deg);
  transform: rotate(45deg);
  background-color: #aa75e3;
}
@media screen and (max-width: 600px) {
  .footer-navigation .sub-menu {
    -webkit-column-count: 1;
    -moz-column-count: 1;
    column-count: 1;
    left: 1.5625rem;
    right: auto;
  }
}
.footer-navigation .menu-item-has-children {
  position: relative;
}
.footer-navigation .menu-item-has-children:hover .sub-menu {
  display: block;
  opacity: 1;
}
a {
  color: inherit;
  text-decoration: none;
}
a:active,
a:focus,
a:hover {
  outline: 0;
}
.main-navigation {
  clear: both;
  display: block;
  margin-left: auto;
}

.main-navigation ul {
  display: none;
  list-style: none;
  margin: 0;
  padding-left: 0;
}
.main-navigation ul li.focus > ul,
.main-navigation ul li:hover > ul {
  left: auto;
  right: 0;
}
.main-navigation ul a {
  position: relative;
  color: #fff;
  text-transform: lowercase;
  border: none;
}
.main-navigation ul#primary-menu > li {
  float: left;
  position: relative;
  padding: 1.25rem;
}
.main-navigation ul#primary-menu > li.focus > a,
.main-navigation ul#primary-menu > li:hover > a {
  color: #dcff02;
}
.main-navigation ul#primary-menu > li.focus > a:after,
.main-navigation ul#primary-menu > li:hover > a:after {
  position: absolute;
  display: inline;
  content: "/";
}
.main-navigation ul > li {
  float: left;
  margin-left: 0.625rem;
  padding: 1.25rem;
}
.main-navigation ul > li:first-child {
  margin-left: 0;
}
.main-navigation ul ul {
  float: left;
  position: absolute;
  top: 100%;
  left: -999em;
  z-index: 99999;
  width: 21.5625rem;
  padding: 1.25rem 1.25rem 1.25rem 2.1875rem;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  background: #1a1a1a;
}
.main-navigation ul ul li {
  max-width: 100%;
  padding: 0;
  margin-left: 0;
  margin-bottom: 1.25rem;
}
.main-navigation ul ul li:hover > a {
  color: #c58fff;
}
.main-navigation ul ul a {
  text-decoration: none;
  border: none;
}
.main-navigation ul ul li.menu-item-has-children {
  cursor: pointer;
}
.main-navigation ul ul li.menu-item-has-children > a:after {
  display: inline-block;
  content: "+";
  margin-left: 0.4375rem;
}
.main-navigation ul ul li.menu-item-has-children ul {
  position: static;
  height: 0;
  overflow: hidden;
  max-width: 100%;
  padding: 0;
}
.main-navigation ul ul li.menu-item-has-children ul li {
  float: none;
  max-width: 100%;
  margin: 0;
  padding: 0.4375rem 0 0.4375rem 1.25rem;
  font-size: 0.95em;
}
.main-navigation ul ul li.menu-item-has-children ul li:first-child {
  padding-top: 0.9375rem;
}
.main-navigation ul ul li.menu-item-has-children.open > a:after {
  content: "-";
}
.main-navigation ul ul li.menu-item-has-children.open ul {
  height: auto;
}
.main-navigation a {
  display: block;
  text-decoration: none;
  border: none;
}
.main-navigation .current-menu-ancestor > a,
.main-navigation .current-menu-item > a,
.main-navigation .current_page_ancestor > a,
.main-navigation .current_page_item > a {
  color: #dcff02;
}
.main-navigation .current-menu-ancestor > a:after,
.main-navigation .current-menu-item > a:after,
.main-navigation .current_page_ancestor > a:after,
.main-navigation .current_page_item > a:after {
  position: absolute;
  display: inline;
  content: "/";
}
.main-navigation ul#primary-menu > li > ul.sub-menu {
  top: 4.375rem;
}
.main-navigation ul#primary-menu > li > ul.sub-menu:before {
  position: absolute;
  top: -0.625rem;
  right: 1.25rem;
  display: block;
  content: "";
  width: 1.25rem;
  height: 1.25rem;
  background: #1a1a1a;
  -webkit-transform: rotate(45deg);
  transform: rotate(45deg);
}
.menu-main-menu-container {
  float: right;
}
.main-navigation.toggled ul,
.menu-toggle {
  display: block;
}
@media screen and (min-width: 37.5em) {
  .menu-toggle {
    display: none;
  }
  .main-navigation ul {
    display: block;
  }
}
.site-main .comment-navigation,
.site-main .post-navigation,
.site-main .posts-navigation {
  margin: 0 0 1.5em;
  overflow: hidden;
}
.comment-navigation .nav-previous,
.post-navigation .nav-previous,
.posts-navigation .nav-previous {
  float: left;
  width: 50%;
}
.comment-navigation .nav-next,
.post-navigation .nav-next,
.posts-navigation .nav-next {
  float: right;
  text-align: right;
  width: 50%;
}
#responsive-menu-container {
  padding-top: 2.5rem !important;
}
.blogsearch {
  padding-right: 1.25rem;
}
.blogsearch__wrapper {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  width: 100%;
}
.blogsearch__wrapper input[type="text"],
.blogsearch__wrapper__field {
  background-color: transparent;
  border-color: transparent;
  color: #fff;
  -webkit-box-flex: 10;
  -ms-flex-positive: 10;
  flex-grow: 10;
}
.blogsearch__wrapper input[type="submit"] {
  width: 3.75rem;
  font-size: 0;
  background-color: transparent;
  border-color: transparent;
  background: url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='30' height='30' fill='transparent'%3E%3Cg fill-rule='evenodd'%3E%3Cpath d='M0 0h30v30H0z'/%3E%3Cpath d='M21.374 13.187a8.187 8.187 0 11-16.374 0 8.187 8.187 0 0116.374 0zm-2.398 5.789l5.932 5.932' stroke='%23FFF' stroke-width='2'/%3E%3C/g%3E%3C/svg%3E")
    100% no-repeat;
  background-size: 1.875rem;
  cursor: pointer;
}
.blogsearch__wrapper input[type="submit"]:hover {
  border-color: transparent;
}
.blogsearch--active {
  background-color: #c58fff;
}
.blogsearch--active input[type="text"] {
  outline: 0;
}
.blogsearch--active input[type="submit"] {
  cursor: pointer;
  background: url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='30' height='30' fill='%23c58fff'%3E%3Cg fill-rule='evenodd'%3E%3Cpath d='M0 0h30v30H0z'/%3E%3Cpath d='M21.374 13.187a8.187 8.187 0 11-16.374 0 8.187 8.187 0 0116.374 0zm-2.398 5.789l5.932 5.932' stroke='%23FFF' stroke-width='2'/%3E%3C/g%3E%3C/svg%3E")
    100% no-repeat;
}
button,
input[type="button"],
input[type="reset"],
input[type="submit"] {
  padding: 1.25rem;
  border: 1px solid #a9ff03;
  border-radius: 0;
  background: #a9ff03;
  font-size: 1.0625rem;
  line-height: 1;
  font-weight: 500;
  text-align: center;
  color: #000;
}
button.btn-disabled,
button.btn-disabled:hover,
button:disabled,
button:disabled:hover,
input[type="button"].btn-disabled,
input[type="button"].btn-disabled:hover,
input[type="button"]:disabled,
input[type="button"]:disabled:hover,
input[type="reset"].btn-disabled,
input[type="reset"].btn-disabled:hover,
input[type="reset"]:disabled,
input[type="reset"]:disabled:hover,
input[type="submit"].btn-disabled,
input[type="submit"].btn-disabled:hover,
input[type="submit"]:disabled,
input[type="submit"]:disabled:hover {
  background-color: #272727;
  border-color: #272727;
}
.btn {
  display: inline-block;
  padding: 1.25rem;
  min-width: 15rem;
  font-weight: 500;
  color: #000;
  text-align: center;
  line-height: 1;
  font-size: 1.0625rem;
  background: #dcff02;
  cursor: pointer;
  text-decoration: none;
  text-transform: lowercase;
  border: 1px solid #dcff02;
  -webkit-transition: all 0.5s ease-out;
  transition: all 0.5s ease-out;
}
.btn--small {
  min-width: 10rem;
}
.btn--disabled,
.btn--disabled:hover {
  background-color: #272727;
  border-color: #272727;
}
.btn:hover {
  background-color: #a9ff03;
}
.btn--transparent {
  background: 0 0;
  color: #dcff02;
}
.btn--simple-black {
  background: #000;
  color: #fff;
  border-color: #000;
}
.btn--image {
  min-width: 17.8125rem;
  min-height: 4.375rem;
  line-height: 4.375rem;
  white-space: nowrap;
  padding: 0 2.5rem;
  background: url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='285' height='70' fill='%23dcff02'%3E%3Cpath fill-rule='evenodd' d='M284.508 21.976l-1.474-14.734c-.041-.404-.31-1.205-.692-1.984V4.81h-.237c-.455-.813-1.013-1.505-1.53-1.534l-14.703-.84c-3.422-.196-6.816-.552-10.236-.31l-17.987 1.275c-1.122.08-2.273.243-3.398.21-2.097-.064-4.21-.33-6.3-.493-5.49-.43-10.981-.948-16.478-1.289-4.164-.258-8.405-.036-12.577-.04-3.871-.004-7.845-.279-11.707.038l-17.091 1.4c-3.26.266-6.347.448-9.61.39l-17.888-.33c-3.585-.067-7.174.09-10.758.166-4.661.096-9.407.466-14.067.29-5.028-.19-10.091-.915-15.101-1.37-3.382-.307-6.758-.779-10.155-.7-9.305.216-18.606.331-27.897.886-5.491.327-10.982.708-16.476.983-4.132.206-8.296.126-12.433.182-9.693.13-19.367.074-29.061-.016-1.538-.013-3.075-.028-4.612-.043-.024.048-.05.095-.072.142L.614 16.302c-.316 2.917-.74 5.724-.58 8.648.434 7.933 1 15.823.9 23.766l-.18 14.41c-.011.875.583 1.853 1.008 2.575.276.468.829 1.66 1.468 1.668 4.918.066 9.837.132 14.755.2 3.522.047 7.054.201 10.575.047 9.295-.41 18.574-.975 27.879-.907 5.588.041 11.179.023 16.765.124 4.145.076 8.303.48 12.44.726l8.996.54c.957.056 1.9.172 2.854.065 5.738-.64 11.476-1.283 17.212-1.925 1.807-.202 3.66-.553 5.479-.614 1.408-.045 2.876.182 4.28.274 5.927.39 11.855.777 17.782 1.165 8.207.538 16.493-.18 24.714.046 8.609.237 17.2 1.208 25.816 1.213l18.218.011c3.434.002 6.813-.382 10.235-.692l9.769-.882c1.924-.174 3.88-.47 5.814-.525 1.337-.037 2.703.115 4.038.178l9.664.448c9.662.448 19.3.556 28.974.664 1.516.016 3.03.034 4.545.051.059.001.075-.066.073-.158.07-7.23-.007-14.477.238-21.704l.52-15.354c.1-2.88-.07-5.509-.357-8.384'/%3E%3C/svg%3E")
    50% / contain no-repeat;
  border: none;
  font-size: 1.125rem;
  font-weight: 600;
  -webkit-transition: all 0.5s ease-out;
  transition: all 0.5s ease-out;
}
.btn--image:hover {
  background: url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='285' height='70' fill='%23a9ff03'%3E%3Cpath fill-rule='evenodd' d='M284.508 21.976l-1.474-14.734c-.041-.404-.31-1.205-.692-1.984V4.81h-.237c-.455-.813-1.013-1.505-1.53-1.534l-14.703-.84c-3.422-.196-6.816-.552-10.236-.31l-17.987 1.275c-1.122.08-2.273.243-3.398.21-2.097-.064-4.21-.33-6.3-.493-5.49-.43-10.981-.948-16.478-1.289-4.164-.258-8.405-.036-12.577-.04-3.871-.004-7.845-.279-11.707.038l-17.091 1.4c-3.26.266-6.347.448-9.61.39l-17.888-.33c-3.585-.067-7.174.09-10.758.166-4.661.096-9.407.466-14.067.29-5.028-.19-10.091-.915-15.101-1.37-3.382-.307-6.758-.779-10.155-.7-9.305.216-18.606.331-27.897.886-5.491.327-10.982.708-16.476.983-4.132.206-8.296.126-12.433.182-9.693.13-19.367.074-29.061-.016-1.538-.013-3.075-.028-4.612-.043-.024.048-.05.095-.072.142L.614 16.302c-.316 2.917-.74 5.724-.58 8.648.434 7.933 1 15.823.9 23.766l-.18 14.41c-.011.875.583 1.853 1.008 2.575.276.468.829 1.66 1.468 1.668 4.918.066 9.837.132 14.755.2 3.522.047 7.054.201 10.575.047 9.295-.41 18.574-.975 27.879-.907 5.588.041 11.179.023 16.765.124 4.145.076 8.303.48 12.44.726l8.996.54c.957.056 1.9.172 2.854.065 5.738-.64 11.476-1.283 17.212-1.925 1.807-.202 3.66-.553 5.479-.614 1.408-.045 2.876.182 4.28.274 5.927.39 11.855.777 17.782 1.165 8.207.538 16.493-.18 24.714.046 8.609.237 17.2 1.208 25.816 1.213l18.218.011c3.434.002 6.813-.382 10.235-.692l9.769-.882c1.924-.174 3.88-.47 5.814-.525 1.337-.037 2.703.115 4.038.178l9.664.448c9.662.448 19.3.556 28.974.664 1.516.016 3.03.034 4.545.051.059.001.075-.066.073-.158.07-7.23-.007-14.477.238-21.704l.52-15.354c.1-2.88-.07-5.509-.357-8.384'/%3E%3C/svg%3E")
    50% / contain no-repeat;
}
@media screen and (max-width: 600px) {
  .btn--image {
    min-height: 3.75rem;
    line-height: 3.75rem;
    padding: 0 1.25rem;
    font-size: 1.0625rem;
  }
}
.btn--image-small {
  width: 4.375rem;
  height: 2.1875rem;
  line-height: 2.1875rem;
  white-space: nowrap;
  padding: 0 0.3125rem;
  background: url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='285' height='70' fill='%23dcff02'%3E%3Cpath fill-rule='evenodd' d='M284.508 21.976l-1.474-14.734c-.041-.404-.31-1.205-.692-1.984V4.81h-.237c-.455-.813-1.013-1.505-1.53-1.534l-14.703-.84c-3.422-.196-6.816-.552-10.236-.31l-17.987 1.275c-1.122.08-2.273.243-3.398.21-2.097-.064-4.21-.33-6.3-.493-5.49-.43-10.981-.948-16.478-1.289-4.164-.258-8.405-.036-12.577-.04-3.871-.004-7.845-.279-11.707.038l-17.091 1.4c-3.26.266-6.347.448-9.61.39l-17.888-.33c-3.585-.067-7.174.09-10.758.166-4.661.096-9.407.466-14.067.29-5.028-.19-10.091-.915-15.101-1.37-3.382-.307-6.758-.779-10.155-.7-9.305.216-18.606.331-27.897.886-5.491.327-10.982.708-16.476.983-4.132.206-8.296.126-12.433.182-9.693.13-19.367.074-29.061-.016-1.538-.013-3.075-.028-4.612-.043-.024.048-.05.095-.072.142L.614 16.302c-.316 2.917-.74 5.724-.58 8.648.434 7.933 1 15.823.9 23.766l-.18 14.41c-.011.875.583 1.853 1.008 2.575.276.468.829 1.66 1.468 1.668 4.918.066 9.837.132 14.755.2 3.522.047 7.054.201 10.575.047 9.295-.41 18.574-.975 27.879-.907 5.588.041 11.179.023 16.765.124 4.145.076 8.303.48 12.44.726l8.996.54c.957.056 1.9.172 2.854.065 5.738-.64 11.476-1.283 17.212-1.925 1.807-.202 3.66-.553 5.479-.614 1.408-.045 2.876.182 4.28.274 5.927.39 11.855.777 17.782 1.165 8.207.538 16.493-.18 24.714.046 8.609.237 17.2 1.208 25.816 1.213l18.218.011c3.434.002 6.813-.382 10.235-.692l9.769-.882c1.924-.174 3.88-.47 5.814-.525 1.337-.037 2.703.115 4.038.178l9.664.448c9.662.448 19.3.556 28.974.664 1.516.016 3.03.034 4.545.051.059.001.075-.066.073-.158.07-7.23-.007-14.477.238-21.704l.52-15.354c.1-2.88-.07-5.509-.357-8.384'/%3E%3C/svg%3E")
    50% / contain no-repeat;
  border: none;
  font-weight: 600;
  -webkit-transition: all 0.5s ease-out;
  transition: all 0.5s ease-out;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
}
.btn--image-small:hover {
  background: url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='285' height='70' fill='%23a9ff03'%3E%3Cpath fill-rule='evenodd' d='M284.508 21.976l-1.474-14.734c-.041-.404-.31-1.205-.692-1.984V4.81h-.237c-.455-.813-1.013-1.505-1.53-1.534l-14.703-.84c-3.422-.196-6.816-.552-10.236-.31l-17.987 1.275c-1.122.08-2.273.243-3.398.21-2.097-.064-4.21-.33-6.3-.493-5.49-.43-10.981-.948-16.478-1.289-4.164-.258-8.405-.036-12.577-.04-3.871-.004-7.845-.279-11.707.038l-17.091 1.4c-3.26.266-6.347.448-9.61.39l-17.888-.33c-3.585-.067-7.174.09-10.758.166-4.661.096-9.407.466-14.067.29-5.028-.19-10.091-.915-15.101-1.37-3.382-.307-6.758-.779-10.155-.7-9.305.216-18.606.331-27.897.886-5.491.327-10.982.708-16.476.983-4.132.206-8.296.126-12.433.182-9.693.13-19.367.074-29.061-.016-1.538-.013-3.075-.028-4.612-.043-.024.048-.05.095-.072.142L.614 16.302c-.316 2.917-.74 5.724-.58 8.648.434 7.933 1 15.823.9 23.766l-.18 14.41c-.011.875.583 1.853 1.008 2.575.276.468.829 1.66 1.468 1.668 4.918.066 9.837.132 14.755.2 3.522.047 7.054.201 10.575.047 9.295-.41 18.574-.975 27.879-.907 5.588.041 11.179.023 16.765.124 4.145.076 8.303.48 12.44.726l8.996.54c.957.056 1.9.172 2.854.065 5.738-.64 11.476-1.283 17.212-1.925 1.807-.202 3.66-.553 5.479-.614 1.408-.045 2.876.182 4.28.274 5.927.39 11.855.777 17.782 1.165 8.207.538 16.493-.18 24.714.046 8.609.237 17.2 1.208 25.816 1.213l18.218.011c3.434.002 6.813-.382 10.235-.692l9.769-.882c1.924-.174 3.88-.47 5.814-.525 1.337-.037 2.703.115 4.038.178l9.664.448c9.662.448 19.3.556 28.974.664 1.516.016 3.03.034 4.545.051.059.001.075-.066.073-.158.07-7.23-.007-14.477.238-21.704l.52-15.354c.1-2.88-.07-5.509-.357-8.384'/%3E%3C/svg%3E")
    50% / contain no-repeat;
}
.btn--image-wide {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  width: 22.5rem;
  height: 4.375rem;
  padding: 0 0.3125rem;
  background: url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='360' height='71' fill='%23dcff02'%3E%3Cpath d='M358.016 21.977L356.17 7.243c-.051-.404-.388-1.205-.867-1.984v-.448h-.297c-.57-.813-1.27-1.505-1.916-1.534l-18.425-.841c-4.288-.195-8.541-.551-12.827-.31l-22.54 1.276c-1.405.08-2.847.243-4.257.209-2.628-.063-5.274-.33-7.895-.492-6.88-.43-13.76-.948-20.648-1.29-5.218-.257-10.532-.035-15.76-.04-4.851-.003-9.83-.278-14.67.039L214.65 3.227c-4.084.267-7.953.449-12.04.39-7.472-.11-14.944-.22-22.417-.328-4.493-.067-8.99.09-13.481.166-5.84.096-11.788.466-17.627.29-6.3-.191-12.645-.915-18.923-1.371-4.238-.306-8.469-.778-12.725-.7-11.66.217-23.315.332-34.958.887-6.88.327-13.761.708-20.646.983-5.178.206-10.395.126-15.58.182-12.146.129-24.268.074-36.416-.016a5545.97 5545.97 0 01-5.779-.043l-.09.142c-.565 4.165-1.13 8.33-1.697 12.494-.396 2.917-.927 5.724-.727 8.648.544 7.933 1.254 15.823 1.13 23.766l-.226 14.409c-.015.876.73 1.854 1.262 2.576.346.468 1.039 1.659 1.84 1.668 6.162.066 12.326.132 18.489.2 4.413.047 8.839.2 13.251.047 11.648-.41 23.275-.975 34.935-.907 7.002.04 14.008.023 21.008.124 5.194.076 10.405.479 15.589.726l11.272.539c1.2.057 2.383.173 3.577.066l21.568-1.925c2.264-.202 4.588-.553 6.866-.614 1.764-.045 3.604.182 5.363.274l22.282 1.165c10.284.538 20.668-.18 30.97.046 10.787.237 21.554 1.208 32.35 1.213l22.828.01c4.303.003 8.537-.381 12.825-.691l12.242-.882c2.41-.174 4.863-.471 7.285-.525 1.676-.037 3.387.115 5.06.178l12.11.448c12.107.448 24.186.556 36.307.664l5.695.05c.074.002.094-.065.092-.157.088-7.23-.009-14.477.298-21.704l.653-15.354c.124-2.88-.088-5.51-.449-8.384' stroke='%23000' stroke-width='2' fill-rule='evenodd'/%3E%3C/svg%3E")
    50% / contain no-repeat;
  border: none;
  font-size: 1.125rem;
  line-height: 1.2;
  font-weight: 600;
  text-align: center;
  -webkit-transition: all 0.5s ease-out;
  transition: all 0.5s ease-out;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
}
.btn--image-wide:hover {
  background: url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='360' height='71' fill='%23a9ff03'%3E%3Cpath d='M358.016 21.977L356.17 7.243c-.051-.404-.388-1.205-.867-1.984v-.448h-.297c-.57-.813-1.27-1.505-1.916-1.534l-18.425-.841c-4.288-.195-8.541-.551-12.827-.31l-22.54 1.276c-1.405.08-2.847.243-4.257.209-2.628-.063-5.274-.33-7.895-.492-6.88-.43-13.76-.948-20.648-1.29-5.218-.257-10.532-.035-15.76-.04-4.851-.003-9.83-.278-14.67.039L214.65 3.227c-4.084.267-7.953.449-12.04.39-7.472-.11-14.944-.22-22.417-.328-4.493-.067-8.99.09-13.481.166-5.84.096-11.788.466-17.627.29-6.3-.191-12.645-.915-18.923-1.371-4.238-.306-8.469-.778-12.725-.7-11.66.217-23.315.332-34.958.887-6.88.327-13.761.708-20.646.983-5.178.206-10.395.126-15.58.182-12.146.129-24.268.074-36.416-.016a5545.97 5545.97 0 01-5.779-.043l-.09.142c-.565 4.165-1.13 8.33-1.697 12.494-.396 2.917-.927 5.724-.727 8.648.544 7.933 1.254 15.823 1.13 23.766l-.226 14.409c-.015.876.73 1.854 1.262 2.576.346.468 1.039 1.659 1.84 1.668 6.162.066 12.326.132 18.489.2 4.413.047 8.839.2 13.251.047 11.648-.41 23.275-.975 34.935-.907 7.002.04 14.008.023 21.008.124 5.194.076 10.405.479 15.589.726l11.272.539c1.2.057 2.383.173 3.577.066l21.568-1.925c2.264-.202 4.588-.553 6.866-.614 1.764-.045 3.604.182 5.363.274l22.282 1.165c10.284.538 20.668-.18 30.97.046 10.787.237 21.554 1.208 32.35 1.213l22.828.01c4.303.003 8.537-.381 12.825-.691l12.242-.882c2.41-.174 4.863-.471 7.285-.525 1.676-.037 3.387.115 5.06.178l12.11.448c12.107.448 24.186.556 36.307.664l5.695.05c.074.002.094-.065.092-.157.088-7.23-.009-14.477.298-21.704l.653-15.354c.124-2.88-.088-5.51-.449-8.384' stroke='%23000' stroke-width='2' fill-rule='evenodd'/%3E%3C/svg%3E")
    50% / contain no-repeat;
}
@media screen and (max-width: 600px) {
  .btn--image-wide {
    width: 17.5rem;
    height: 3.75rem;
    margin: 0 auto;
    background: url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='281' height='60' fill='%23dcff02'%3E%3Cpath d='M279.62 18.837l-1.448-12.63c-.04-.346-.305-1.032-.68-1.7v-.384h-.234c-.447-.697-.995-1.29-1.502-1.315l-14.452-.72c-3.363-.168-6.698-.473-10.06-.265l-17.678 1.092c-1.102.069-2.234.209-3.34.18-2.06-.054-4.136-.282-6.191-.422-5.396-.369-10.792-.813-16.195-1.105-4.092-.221-8.26-.03-12.36-.034-3.805-.004-7.71-.24-11.507.032l-16.797 1.2c-3.203.228-6.238.384-9.444.334-5.86-.095-11.72-.188-17.581-.281-3.524-.058-7.051.077-10.574.142-4.58.082-9.245.4-13.825.248-4.941-.163-9.917-.784-14.841-1.175-3.324-.262-6.642-.667-9.98-.599-9.146.185-18.287.284-27.419.76-5.396.28-10.793.606-16.192.842-4.061.177-8.154.108-12.22.156-9.526.11-19.034.064-28.561-.014-1.512-.01-3.023-.024-4.533-.036l-.07.121-1.332 10.71c-.31 2.5-.727 4.906-.57 7.412.427 6.8.983 13.563.886 20.37L.743 54.108c-.012.751.572 1.59.99 2.208.27.402.814 1.422 1.442 1.43 4.834.057 9.668.113 14.502.172 3.461.04 6.933.172 10.393.04 9.135-.352 18.255-.836 27.4-.778 5.492.036 10.987.02 16.477.107 4.074.065 8.16.41 12.226.622l8.842.462c.94.049 1.868.148 2.805.057l16.916-1.65c1.776-.174 3.598-.474 5.385-.527 1.384-.038 2.826.156 4.206.235 5.825.334 11.652.666 17.477.999 8.066.46 16.21-.155 24.289.04 8.461.202 16.905 1.035 25.372 1.039l17.905.01c3.375.001 6.696-.328 10.06-.594l9.6-.756c1.892-.149 3.815-.404 5.715-.45 1.314-.032 2.656.099 3.968.153l9.498.384c9.496.384 18.97.476 28.476.569l4.467.044c.058 0 .074-.057.072-.136.069-6.197-.007-12.409.234-18.603l.512-13.16c.097-2.47-.069-4.723-.352-7.187' fill-rule='evenodd'/%3E%3C/svg%3E")
      50% / contain no-repeat;
    font-size: 1.0625rem;
  }
}
.btn--image-wider {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  width: 27.25rem;
  height: 4.375rem;
  padding: 0 0.3125rem;
  background: url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='436' height='71' fill='%23dcff02'%3E%3Cpath d='M431.417 23.31l-2.225-14.733c-.062-.404-.468-1.205-1.044-1.984v-.448h-.358c-.687-.813-1.53-1.505-2.308-1.534L403.29 3.77c-5.165-.195-10.288-.551-15.45-.31l-27.148 1.276c-1.693.08-3.43.243-5.128.209-3.166-.063-6.353-.33-9.51-.492-8.285-.43-16.573-.948-24.87-1.29-6.285-.257-12.686-.035-18.983-.04-5.842-.003-11.84-.278-17.67.039L258.736 4.56c-4.92.267-9.58.449-14.503.39-8.999-.11-18-.22-27-.328-5.412-.067-10.829.09-16.238.166-7.035.096-14.198.466-21.232.29-7.589-.191-15.23-.915-22.792-1.371-5.105-.306-10.2-.778-15.327-.7-14.045.217-28.083.332-42.106.887-8.288.327-16.575.708-24.868.983-6.236.206-12.521.126-18.765.182-14.63.129-29.231.074-43.863-.016-2.32-.013-4.64-.028-6.96-.043-.037.048-.075.095-.11.142-.68 4.165-1.36 8.33-2.043 12.494-.477 2.917-1.117 5.724-.875 8.648.655 7.933 1.509 15.823 1.36 23.766L3.14 64.46c-.018.876.878 1.854 1.52 2.576.416.468 1.251 1.659 2.216 1.668 7.422.066 14.847.132 22.27.2 5.315.047 10.646.2 15.96.047 14.03-.41 28.035-.975 42.08-.907 8.433.04 16.872.023 25.303.124 6.256.076 12.532.479 18.776.726l13.578.539c1.444.057 2.87.173 4.308.066l25.978-1.925c2.727-.202 5.526-.553 8.27-.614 2.125-.045 4.34.182 6.46.274l26.838 1.165c12.388.538 24.894-.18 37.302.046 12.994.237 25.962 1.208 38.965 1.213l27.497.01c5.183.003 10.283-.381 15.448-.691l14.744-.882c2.904-.174 5.858-.471 8.775-.525 2.018-.037 4.08.115 6.095.178l14.586.448c14.583.448 29.132.556 43.731.664l6.86.05c.09.002.114-.065.11-.157.106-7.23-.01-14.477.36-21.704l.786-15.354c.15-2.88-.106-5.51-.54-8.384' stroke='%23000' stroke-width='2' fill-rule='evenodd'/%3E%3C/svg%3E")
    50% / contain no-repeat;
  border: none;
  font-size: 1.125rem;
  line-height: 1.2;
  font-weight: 600;
  text-align: center;
  -webkit-transition: all 0.5s ease-out;
  transition: all 0.5s ease-out;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
}
.btn--image-wider:hover {
  background: url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='436' height='71' fill='%23a9ff03'%3E%3Cpath d='M431.417 23.31l-2.225-14.733c-.062-.404-.468-1.205-1.044-1.984v-.448h-.358c-.687-.813-1.53-1.505-2.308-1.534L403.29 3.77c-5.165-.195-10.288-.551-15.45-.31l-27.148 1.276c-1.693.08-3.43.243-5.128.209-3.166-.063-6.353-.33-9.51-.492-8.285-.43-16.573-.948-24.87-1.29-6.285-.257-12.686-.035-18.983-.04-5.842-.003-11.84-.278-17.67.039L258.736 4.56c-4.92.267-9.58.449-14.503.39-8.999-.11-18-.22-27-.328-5.412-.067-10.829.09-16.238.166-7.035.096-14.198.466-21.232.29-7.589-.191-15.23-.915-22.792-1.371-5.105-.306-10.2-.778-15.327-.7-14.045.217-28.083.332-42.106.887-8.288.327-16.575.708-24.868.983-6.236.206-12.521.126-18.765.182-14.63.129-29.231.074-43.863-.016-2.32-.013-4.64-.028-6.96-.043-.037.048-.075.095-.11.142-.68 4.165-1.36 8.33-2.043 12.494-.477 2.917-1.117 5.724-.875 8.648.655 7.933 1.509 15.823 1.36 23.766L3.14 64.46c-.018.876.878 1.854 1.52 2.576.416.468 1.251 1.659 2.216 1.668 7.422.066 14.847.132 22.27.2 5.315.047 10.646.2 15.96.047 14.03-.41 28.035-.975 42.08-.907 8.433.04 16.872.023 25.303.124 6.256.076 12.532.479 18.776.726l13.578.539c1.444.057 2.87.173 4.308.066l25.978-1.925c2.727-.202 5.526-.553 8.27-.614 2.125-.045 4.34.182 6.46.274l26.838 1.165c12.388.538 24.894-.18 37.302.046 12.994.237 25.962 1.208 38.965 1.213l27.497.01c5.183.003 10.283-.381 15.448-.691l14.744-.882c2.904-.174 5.858-.471 8.775-.525 2.018-.037 4.08.115 6.095.178l14.586.448c14.583.448 29.132.556 43.731.664l6.86.05c.09.002.114-.065.11-.157.106-7.23-.01-14.477.36-21.704l.786-15.354c.15-2.88-.106-5.51-.54-8.384' stroke='%23000' stroke-width='2' fill-rule='evenodd'/%3E%3C/svg%3E")
    50% / contain no-repeat;
}
@media screen and (max-width: 600px) {
  .btn--image-wider {
    width: 17.5rem;
    height: 5.625rem;
    margin: 0 auto;
    background: url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='281' height='90' fill='%23dcff02'%3E%3Cpath d='M279.62 28.237l-1.448-19.448c-.04-.533-.305-1.59-.68-2.619v-.591h-.234c-.447-1.073-.995-1.987-1.502-2.025l-14.452-1.11c-3.363-.258-6.698-.728-10.06-.408l-17.678 1.683c-1.102.105-2.234.32-3.34.276-2.06-.083-4.136-.435-6.191-.65-5.396-.567-10.792-1.251-16.195-1.701-4.092-.34-8.26-.048-12.36-.053-3.805-.005-7.71-.368-11.507.05l-16.797 1.847c-3.203.352-6.238.592-9.444.515-5.86-.146-11.72-.29-17.581-.433-3.524-.089-7.051.118-10.574.219-4.58.126-9.245.615-13.825.383-4.941-.253-9.917-1.208-14.841-1.81-3.324-.404-6.642-1.027-9.98-.923-9.146.285-18.287.437-27.419 1.17-5.396.431-10.793.934-16.192 1.297-4.061.272-8.154.167-12.22.24-9.526.17-19.034.098-28.561-.02-1.512-.018-3.023-.038-4.533-.057-.024.063-.048.125-.07.187-.444 5.498-.887 10.995-1.332 16.492-.31 3.85-.727 7.555-.57 11.415.427 10.47.983 20.885.886 31.37L.743 82.552c-.012 1.156.572 2.447.99 3.4.27.618.814 2.19 1.442 2.202 4.834.087 9.668.174 14.502.264 3.461.062 6.933.265 10.393.062 9.135-.541 18.255-1.287 27.4-1.197 5.492.054 10.987.03 16.477.163 4.074.1 8.16.633 12.226.959l8.842.711c.94.075 1.868.228 2.805.087l16.916-2.54c1.776-.267 3.598-.73 5.385-.811 1.384-.06 2.826.24 4.206.362l17.477 1.537c8.066.71 16.21-.237 24.289.061 8.461.313 16.905 1.595 25.372 1.601l17.905.015c3.375.002 6.696-.505 10.06-.914l9.6-1.164c1.892-.23 3.815-.622 5.715-.693 1.314-.049 2.656.152 3.968.235l9.498.591c9.496.592 18.97.734 28.476.877 1.49.02 2.978.045 4.467.067.058.001.074-.087.072-.208.069-9.544-.007-19.11.234-28.649l.512-20.266c.097-3.802-.069-7.272-.352-11.067' fill-rule='evenodd'/%3E%3C/svg%3E")
      50% / contain no-repeat;
    font-size: 1.0625rem;
  }
}
.btn--badge {
  position: relative;
}
.btn--dark {
  min-width: 8.125rem;
  padding: 0.8125rem 0.625rem 0.9375rem;
  color: grey;
}
.btn--dark,
.btn--dark:hover {
  background-color: hsla(0, 0%, 100%, 0.1);
  border-color: hsla(0, 0%, 100%, 0.1);
}
.btn--dark:hover {
  color: #fff;
}
.btn--header {
  min-width: 10.9375rem;
  margin-left: 2.5rem;
  padding: 0.3125rem 0.9375rem;
  background-color: #a9ff03;
  border-color: #a9ff03;
  font-size: 0.9375rem;
  font-weight: 500;
  line-height: 1.87;
  text-align: center;
  color: #000;
}
@media screen and (max-width: 768px) {
  .btn--header {
    -webkit-box-ordinal-group: 4;
    -ms-flex-order: 3;
    order: 3;
    margin-top: 1.875rem;
  }
}
.btn-badge {
  position: absolute;
  right: -6.5625rem;
}
@media screen and (max-width: 600px) {
  .btn-badge {
    width: 5.3125rem;
    top: 1.5625rem;
    right: -3.4375rem;
  }
}
.btn-wrapper {
  width: 100%;
}
.btn-wrapper--centered {
  text-align: center;
}
.toggle-btn {
  padding: 0.9375rem 1.4375rem;
  border: 1px solid #444;
  background-color: transparent;
  font-size: 1.125rem;
  line-height: 1.67;
  color: #b3b3b3;
}
.toggle-btn--small {
  padding: 0 0.3125rem;
  font-size: 1rem;
  line-height: 1.75;
}
.btn-wrapper {
  margin-top: 2.5rem;
  margin-bottom: 3.75rem;
}
@media screen and (max-width: 600px) {
  .btn-wrapper {
    margin-top: 1.875rem;
    margin-bottom: 2.5rem;
  }
}
input[type="color"],
input[type="date"],
input[type="datetime-local"],
input[type="datetime"],
input[type="email"],
input[type="month"],
input[type="number"],
input[type="password"],
input[type="range"],
input[type="search"],
input[type="tel"],
input[type="text"],
input[type="time"],
input[type="url"],
input[type="week"],
textarea {
  height: 3.75rem;
  border: 1px solid #fff;
  border-radius: 0;
  padding: 1.25rem;
  font-size: 1rem;
  font-weight: 500;
  line-height: 1.75;
  color: rgba(0, 0, 0, 0.4);
}
input[type="submit"] {
  width: 11.25rem;
  height: 3.75rem;
  padding: 0;
  background-color: #dcff02;
  font-size: 1.0625rem;
  font-weight: 500;
  text-align: center;
  color: #000;
  border-radius: 0;
  border: 1px solid #dcff02;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
}
textarea {
  width: 100%;
}
.form-row {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
}
@media screen and (max-width: 600px) {
  .form-row {
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -ms-flex-direction: column;
    flex-direction: column;
  }
}
.form-input {
  margin-right: 0.625rem;
}
@media screen and (max-width: 600px) {
  .form-input {
    width: 100%;
    margin-right: 0;
    margin-bottom: 0.625rem;
  }
}
@media screen and (max-width: 600px) {
  .form-input input,
  .form-submit input {
    width: 100%;
  }
}
::-webkit-input-placeholder {
  color: #000;
  opacity: 1;
}
::-moz-placeholder {
  color: #000;
  opacity: 1;
}
:-ms-input-placeholder {
  opacity: 1;
}
::-ms-input-placeholder {
  opacity: 1;
}
::placeholder {
  color: #000;
  opacity: 1;
}
:-ms-input-placeholder {
  color: #000;
}
::-ms-input-placeholder {
  color: #000;
}
input:focus::-webkit-input-placeholder {
  opacity: 0.35;
}
input:focus::-moz-placeholder {
  opacity: 0.35;
}
input:focus::placeholder {
  opacity: 0.35;
}
input:focus:-ms-input-placeholder {
  opacity: 0.35;
}
input:focus::-ms-input-placeholder {
  opacity: 0.35;
}
.sticky {
  display: block;
}
article.page,
article.post {
  margin: 0 0 12.5rem;
  padding: 3.75rem 0 0;
}
@media screen and (max-width: 600px) {
  article.page,
  article.post {
    padding-top: 0.625rem;
    margin-bottom: 3.125rem;
  }
}
.updated:not(.published) {
  display: none;
}
.entry-content,
.entry-summary,
.page-content {
  margin: 1.5em 0 0;
}
.page-links {
  clear: both;
  margin: 0 0 1.5em;
}
.site {
  overflow-x: hidden;
}
.container {
  width: 66.5625rem;
  max-width: 100%;
  padding: 0 1.25rem;
  margin: 0 auto;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
}
.row {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
}
.col-100,
.row {
  width: 100%;
}
.col-50 {
  width: 49%;
}
@media screen and (max-width: 600px) {
  .col-50 {
    width: 100%;
  }
}
.col-25 {
  width: 25%;
}
@media screen and (max-width: 600px) {
  .col-25 {
    width: 100%;
  }
}
.col-30 {
  width: 29%;
}
@media screen and (max-width: 600px) {
  .col-30 {
    width: 100%;
  }
}
.col-70 {
  width: 69%;
}
@media screen and (max-width: 600px) {
  .col-70 {
    width: 100%;
  }
}
.col-75 {
  width: 75%;
}
@media screen and (max-width: 600px) {
  .col-75 {
    width: 100%;
  }
}
.display-desktop {
  display: block;
}
@media screen and (max-width: 768px) {
  .display-desktop {
    display: none;
  }
}
.display-mobile {
  display: none;
}
@media screen and (max-width: 768px) {
  .display-mobile {
    display: block;
  }
}
.site-header {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  width: 100%;
  padding: 1.25rem 0;
}
@media screen and (max-width: 768px) {
  .site-header {
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
  }
}
.site-branding {
  width: 12.1875rem;
}
@media screen and (max-width: 600px) {
  .site-branding {
    max-width: 50%;
    margin: 0 auto;
  }
}
.site-footer__top {
  background: #c58fff;
}
.site-footer__info {
  padding: 3.75rem 0;
}
.site-footer__nav {
  padding: 2.5rem 0;
  border-top: 2px solid #b785ee;
}
.site-footer__bottom {
  height: 3.75rem;
  padding: 0.9375rem 0;
  background: #aa75e3;
}
@media screen and (max-width: 600px) {
  .site-footer__bottom {
    height: auto;
  }
}
.site-footer__socials {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: end;
  -ms-flex-pack: end;
  justify-content: flex-end;
}
@media screen and (max-width: 600px) {
  .site-footer__socials {
    -webkit-box-pack: start;
    -ms-flex-pack: start;
    justify-content: flex-start;
  }
}
@media screen and (max-width: 600px) {
  .site-footer__logo {
    margin-bottom: 1.25rem;
  }
}
.copyright {
  font-size: 1rem;
  opacity: 0.6;
  text-align: right;
}
@media screen and (max-width: 600px) {
  .copyright {
    text-align: left;
  }
}
.socials {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  width: auto;
  list-style: none;
}
.socials a {
  text-decoration: none;
}
.socials li {
  width: 3.125rem;
  height: 3.125rem;
  margin-left: 1.5625rem;
}
.socials li:first-child {
  margin-left: 0;
}
.socials span {
  font-size: 0;
}
@media screen and (max-width: 600px) {
  .subscription-widget {
    margin-bottom: 2.5rem;
  }
}
.subscription-widget h3 {
  max-width: 38.75rem;
  margin-bottom: 0.625rem;
  font-size: 2.5rem;
  font-weight: 400;
  letter-spacing: 0.1625rem;
  line-height: 1.2;
  text-transform: uppercase;
}
.subscription-widget h3 span {
  color: #dcff02;
}
@media screen and (max-width: 600px) {
  .subscription-widget h3 {
    font-size: 1.75rem;
    line-height: 1.21;
    letter-spacing: 0.1rem;
  }
}
.subscription-widget h4 {
  margin-bottom: 1.875rem;
  font-style: normal;
  font-weight: 400;
  font-size: 2rem;
  line-height: 1.25;
  letter-spacing: 0.01875rem;
  color: #fff;
  text-transform: none;
}
@media screen and (max-width: 600px) {
  .subscription-widget h4 {
    font-size: 1.625rem;
    line-height: 1.15;
    letter-spacing: 0.00625rem;
  }
}
.subscription-widget input[type="email"] {
  width: 21.25rem;
}
@media screen and (max-width: 600px) {
  .subscription-widget input[type="email"] {
    width: 100%;
  }
}
.top-banner {
  position: relative;
  z-index: 9999999;
  width: 100%;
  padding: 0.375rem 0;
  background: #c58fff;
}
@media screen and (max-width: 600px) {
  .top-banner {
    padding: 0.625rem 1.25rem 0.375rem;
  }
}
.top-banner__container {
  position: relative;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  justify-content: center;
}
@media screen and (max-width: 600px) {
  .top-banner__container.container {
    padding: 0 1.875rem 0 0;
  }
}
@media screen and (max-width: 600px) {
  .top-banner__container {
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -ms-flex-direction: column;
    flex-direction: column;
    -webkit-box-align: start;
    -ms-flex-align: start;
    align-items: flex-start;
  }
}
.top-banner__slogan {
  margin-right: 1.25rem;
  font-size: 1.3125rem;
  font-weight: 400;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.02813rem;
  text-align: center;
  color: #000;
  text-transform: none;
}
@media screen and (max-width: 600px) {
  .top-banner__slogan {
    margin-right: 0;
    margin-bottom: 0.625rem;
    text-align: left;
  }
}
.top-banner__close {
  position: absolute;
  top: 50%;
  right: 0;
  color: #000;
  font-size: 1.5625rem;
  font-weight: 600;
  cursor: pointer;
  -webkit-transform: translateY(-50%);
  transform: translateY(-50%);
}
@media screen and (max-width: 600px) {
  .top-banner__close {
    top: 0;
    right: 0;
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }
}
.faq-search {
  margin-top: 3.75rem;
  margin-bottom: 6.875rem;
}
@media screen and (max-width: 600px) {
  .faq-search {
    margin: 1.875rem 0 2.5rem;
  }
}
.input-container {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  width: 100%;
  background-color: #c58fff;
  padding: 0.625rem 1.875rem;
}
@media screen and (max-width: 600px) {
  .input-container {
    padding: 0.3125rem 0.9375rem;
  }
}
.input-container input {
  -webkit-box-flex: 10;
  -ms-flex-positive: 10;
  flex-grow: 10;
  padding: 0.3125rem;
  background-color: #c58fff;
  border-color: #c58fff;
  color: #000;
}
.input-container input:focus {
  outline: 0;
  border-color: #c58fff;
}
.input-icon {
  margin-left: 0.625rem;
  cursor: pointer;
}
.input-icon--reset,
.input-icon--search-active {
  display: none;
}
.faq {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  text-transform: lowercase;
}
.faq__category {
  margin-bottom: 1.875rem;
  line-height: 1.4;
}
.faq__category a:after {
  display: none;
  content: "/";
}
.faq__category a:hover:after {
  display: inline;
}
.faq__category a.highlight:after {
  display: inline;
  content: "/";
}
.faq__category:nth-child(3n + 1) a:hover {
  color: #c58fff;
}
.faq__category:nth-child(3n + 2) a:hover {
  color: #5cffe4;
}
.faq__category:nth-child(3n + 3) a:hover {
  color: #a9ff03;
}
.faq__category:nth-child(3n + 1) a.highlight {
  color: #c58fff;
}
.faq__category:nth-child(3n + 2) a.highlight {
  color: #5cffe4;
}
.faq__category:nth-child(3n + 3) a.highlight {
  color: #a9ff03;
}
.faq__search-results {
  display: none;
}
.faq__filter {
  padding-top: 0.9375rem;
}
.faq__filter.fixed {
  position: fixed;
  top: 1.25rem;
  max-width: 15.625rem;
}
.faq__content {
  margin-bottom: 3.125rem;
}
@media screen and (max-width: 600px) {
  .faq__content {
    margin-bottom: 0;
  }
}
.faq__content li {
  margin-bottom: 1.875rem;
}
.faq__content:nth-child(3n + 1) {
  color: #c58fff;
}
.faq__content:nth-child(3n + 1) .faq__reply {
  border-color: #c58fff;
}
.faq__content:nth-child(3n + 2) {
  color: #5cffe4;
}
.faq__content:nth-child(3n + 2) .faq__reply {
  border-color: #5cffe4;
}
.faq__content:nth-child(3n + 3) {
  color: #a9ff03;
}
.faq__content:nth-child(3n + 3) .faq__reply {
  border-color: #a9ff03;
}
.faq__input {
  cursor: pointer;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
}
@media screen and (max-width: 600px) {
  .faq__input {
    -webkit-box-align: start;
    -ms-flex-align: start;
    align-items: flex-start;
  }
}
.faq__input .faq-icon--close {
  display: inline;
}
.faq__input .faq-icon--open,
.faq__input.faq-show .faq-icon--close {
  display: none;
}
.faq__input.faq-show .faq-icon--open {
  display: inline;
}
.faq__reply {
  margin-left: 4.375rem;
  padding-left: 2.5rem;
  border-left: 1px solid;
  color: #fff;
  line-height: 2;
  height: 0;
  opacity: 0;
  overflow: hidden;
  -webkit-transition: all 0.3s ease-in;
  transition: all 0.3s ease-in;
}
.faq__reply p {
  margin-bottom: 0.9375rem;
}
@media screen and (max-width: 600px) {
  .faq__reply {
    margin-left: 0;
    border-left-width: 0;
    padding-left: 2.375rem;
  }
}
.faq__reply.faq-show {
  height: auto;
  margin-top: 1.875rem;
  opacity: 1;
}
.faq__bottom {
  width: 100%;
  margin-top: 5rem;
  text-align: center;
}
.faq__category-name {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
  -ms-flex-item-align: center;
  align-self: center;
  margin-bottom: 1.875rem;
  color: #fff;
}
.faq__category-name.faq-show {
  color: inherit;
}
.faq__category-name.faq-show span {
  -webkit-transform: rotate(180deg);
  transform: rotate(180deg);
}
.faq__category-container {
  height: 0;
  opacity: 0;
  overflow: hidden;
  -webkit-transition: all 0.3s ease-in;
  transition: all 0.3s ease-in;
}
.faq__category-container.faq-show {
  height: auto;
  opacity: 1;
}
.faq-icon {
  margin-right: 1.25rem;
  font-size: 2em;
  font-weight: 300;
}
@media screen and (max-width: 600px) {
  .faq-icon {
    line-height: 1.6875rem;
  }
}
.faq-active {
  color: red;
}
</style>
