<div class="row mx-0 g-0">
  <div class="col-lg-9 fw-content-wrapper mb-16 mb-lg-0">
    <div class="fw-content fw-content--single-article line-numbers">
      {{ article.body }}
      {{ article | attachments }}
    </div>
      {{ article | solution_article_feedback }}
  </div>
  <section class="col-lg-3 fw-sidebar-wrapper">
    <div class="print mb-20">
      <a href="javascript:print()"><span class="icon-print pe-8"></span>Print</a>
    </div>
      {% if article.tags.size >= 1 %}
      <aside class="bg-grey fw-sidebar">
      </aside>
      {% endif %}
  </section>

  .mb-20 a{
  color: #12344d;
}

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
  <script type="text/javascript">
    var ToC =
    "<nav role='navigation' class='table-of-contents'>" +
    "<h5>On this page:</h5>" +
    "<ul>";

    var newLine, el, title, link;

    $(".fw-wrapper-shadow .fw-content--single-article h2").each(function() {

    el = $(this);
    title = el.text();
    link = "#" + el.attr("id");

    newLine =
      "<li>" +
        "<a href='" + link + "'>" +
          title +
        "</a>" +
      "</li>";

    ToC += newLine;

  });
  ToC +=
    "</ul>" +
    "</nav>";

  $(".fw-sidebar").prepend(ToC);
        
  window.addEventListener('DOMContentLoaded', () => {

    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        const id = entry.target.getAttribute('id');
        if (entry.intersectionRatio > 0) {
          document.querySelector(`nav li a[href="#${id}"]`).parentElement.classList.add('active');
        } else {
          document.querySelector(`nav li a[href="#${id}"]`).parentElement.classList.remove('active');
        }
      });
    });

    // Track all sections that have an `id` applied
    document.querySelectorAll('h2[id]').forEach((section) => {
      observer.observe(section);
    });
    
  });
  </script>

{% if  portal.current_page != "csat_survey" %}
 <footer class="container-fluid px-0">
   <section class="fw-contact-info">
     <p class="fw-contacts">
       {{ portal | footer_contact_info }}
     </p>
   </section>
   <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
   <section class= "fw-credit">
   <div class="container">
  	 	<div class="row">
          	<div class="footer-col">
			<a title="LeapXpert - Link to main page" href="https://www.leap.expert/" target="_blank"><img src="https://www.leap.expert/wp-content/themes/leapexpert/images/leapxpert.svg" width="135" alt="LeapXpert"></a>
              <h4>follow us</h4>
              <div class="social-links">
                <a href="https://www.linkedin.com/company/leapxpert" target="_blank" title="LeapXpert on Linkedin"><i class="fa fa-linkedin"></i></a>
                <a href="https://twitter.com/leapxpert" target="_blank" title="LeapXpert on Twitter"><i class="fa fa-twitter"></i></a>
              </div>
  	 		</div>
  	 		<div class="footer-col">
  	 			<h4>Solutions</h4>
  	 			<ul class="footer__items clean-list">
  	 				<li><a class ="footer_link" href="https://www.leap.expert/the-responsible-business-communication-platform-to-talk-and-chat/" target="_blank">Enterprise</a></li>
  	 				<li><a class ="footer_link" href="https://www.leap.expert/archive-text-messages-for-compliance-and-security-in-minutes/" target="_blank">Small business</a></li>
  	 				<li><a class ="footer_link" href="https://www.leap.expert/leapxpert-for-microsoft-teams/" target="_blank">LeapXpert for Microsoft Teams</a></li>
  	 				<li><a class ="footer_link" href="https://www.leap.expert/pricing/" target="_blank">Pricing</a></li>
  	 			</ul>
  	 		</div>
  	 		<div class="footer-col">
  	 			<h4>Resources</h4>
  	 			<ul class="footer__items clean-list">
  	 				<li><a class ="footer_link" href="https://www.leap.expert/category/blog/" target="_blank">Blog</a></li>
  	 				<li><a class ="footer_link" href="https://www.leap.expert/category/news/" target="_blank">News</a></li>
  	 				<li><a class ="footer_link" href="https://www.leap.expert/category/press-release/" target="_blank">Press Releases</a></li>
  	 				<li><a class ="footer_link" href="https://www.leap.expert/category/white-paper/" target="_blank">White Papers</a></li>
  	 				<li><a class ="footer_link" href="https://www.leap.expert/category/ebook/" target="_blank">eBooks</a></li>
  	 				<li><a class ="footer_link" href="https://www.leap.expert/glossary/" target="_blank">Glossary</a></li>
  	 				<li><a class ="footer_link" href="https://www.leap.expert/category/webinar/" target="_blank"</a></li>
  	 				<li><a class ="footer_link" href="https://www.leap.expert/category/brochure/" target="_blank">Brochures</a></li>
  	 				<li><a class ="footer_link" href="https://www.leap.expert/category/customer-story/" target="_blank">Customer Stories</a></li>
  	 			</ul>
  	 		</div>
  	 		<div class="footer-col">
  	 			<h4>Company</h4>
  	 			<ul class="footer__items clean-list">
  	 				<li><a class ="footer_link" href="https://www.leap.expert/about-us/" target="_blank">About Us</a></li>
  	 				<li><a class ="footer_link" href="https://www.leap.expert/about-us/#partners" target="_blank">Partners</a></li>
  	 				<li><a class ="footer_link" href="https://www.leap.expert/about-us/#awards" target="_blank">Awards</a></li>
  	 			</ul>
  	 		</div>
  	 		<div class="footer-col">
  	 			<h4>follow us</h4>
  	 			<div class="social-links">
					<a href="https://www.linkedin.com/company/leapxpert" target="_blank" title="LeapXpert on Linkedin"><i class="fa fa-linkedin"></i></a>
  	 				<a href="https://twitter.com/leapxpert" target="_blank" title="LeapXpert on Twitter"><i class="fa fa-twitter"></i></a>
  	 			</div>
  	 		</div>
  	 	</div>
  	 </div>
	<nav class="fw-laws">
    <span class="fw-branding">@ 2023 LeapXpert</span><a id="" href="https://www.leap.expert/terms-of-use/" class="copyright-text" target="_blank">Terms of Use</a>
    <a id="" href="https://www.leap.expert/privacy-policy/" class="cookie-policy">Privacy Policy</a>
 	</nav>
     </section>
 </footer>
{% endif %}