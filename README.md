
{% load static %}
<!DOCTYPE html>
<html lang="en">

<head>
<title>Travello</title>
<meta charset="utf-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="description" content="Travello template project">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" type="text/css" href="{% static 'styles/bootstrap4/bootstrap.min.css' %}">
<link href="{% static 'plugins/font-awesome-4.7.0/css/font-awesome.min.css' %}" rel="stylesheet" type="text/css">
<link rel="stylesheet" type="text/css" href="{% static 'plugins/OwlCarousel2-2.2.1/owl.carousel.css' %}">
<link rel="stylesheet" type="text/css" href="{% static 'plugins/OwlCarousel2-2.2.1/owl.theme.default.css' %}">
<link rel="stylesheet" type="text/css" href="{% static 'plugins/OwlCarousel2-2.2.1/animate.css' %}">
<link rel="stylesheet" type="text/css" href="{% static 'styles/main_styles.css' %}">
<link rel="stylesheet" type="text/css" href="{% static 'styles/responsive.css' %}">
</head>
<body>

<div class="super_container">
	
	<!-- Header -->

	<header class="header">
		<div class="container">
			<div class="row">
				<div class="col">
					<div class="header_content d-flex flex-row align-items-center justify-content-start">
						<div class="header_content_inner d-flex flex-row align-items-end justify-content-start">
							<div class="logo"><a href="">Travel World</a></div>
							<nav class="main_nav">
								<ul class="d-flex flex-row align-items-start justify-content-start">
									<li class="active"><a href="">Home</a></li>
									<li><a href="accounts/about">About Us</a></li>
									<li><a href="accounts/packages">Packages</a></li>
									<li><a href="accounts/news">News</a></li>
									<li><a href="accounts/contact">Contact</a></li>
									  <li><a href="accounts/cart">Cart</a></li>


									{% if user.is_authenticated %}
										<li><a href="accounts/logout">Logout</a></li>
									{% else %}
										<li><a href="accounts/register">Register</a></li>
										<li><a href="accounts/login">Login</a></li>

									{% endif %}
								</ul>
							</nav>
							{% if user.is_authenticated %}
								<div class="header_phone ml-auto">Welcome, {{user.first_name}}</div>
							{% else %}
								<div class="header_phone ml-auto">
									<a style="color: white; font-size:xx-large;" href="https://www.instagram.com/priyanka_chowdary123/" target="_blank">
										<i class="fa fa-instagram" aria-hidden="false"></i>
									</a>
								</div>
							{% endif %}

							<!-- Hamburger -->

							<div class="hamburger ml-auto">
								<i class="fa fa-bars" aria-hidden="true"></i>
							</div>

						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="header_social d-flex flex-row align-items-center justify-content-start">
			<ul class="d-flex flex-row align-items-start justify-content-start">
				<li><a href="#"><i class="fa fa-pinterest" aria-hidden="true"></i></a></li>
				<li><a href="#"><i class="fa fa-facebook" aria-hidden="true"></i></a></li>
				<li><a href="#"><i class="fa fa-twitter" aria-hidden="true"></i></a></li>
				<li><a href="#"><i class="fa fa-dribbble" aria-hidden="true"></i></a></li>
				<li><a href="#"><i class="fa fa-behance" aria-hidden="true"></i></a></li>
				<li><a href="#"><i class="fa fa-linkedin" aria-hidden="true"></i></a></li>
			</ul>
		</div>
	</header>

	<!-- Menu -->

	<div class="menu">
		<div class="menu_header d-flex flex-row align-items-center justify-content-start">
			<div class="menu_logo"><a href="">Travel World</a></div>
			<div class="menu_close_container ml-auto"><div class="menu_close"><div></div><div></div></div></div>
		</div>
		<div class="menu_content">
			<ul>
				<li class="active"><a href="">Home</a></li>
				<li><a href="accounts/about">About Us</a></li>
				<li><a href="accounts/news">News</a></li>
				<li><a href="accounts/contact">Contact</a></li>

				{% if user.is_authenticated %}
					<li><a href="accounts/logout">Logout</a></li>
				{% else %}
					<li><a href="accounts/register">Register</a></li>
					<li><a href="accounts/login">Login</a></li>
				{% endif %}
			</ul>
		</div>
		<div class="menu_social">
			{% if user.is_authenticated %}
				<div class="menu_phone ml-auto">Logged in: {{user.first_name}} {{user.last_name}}</div>
			{% else %}
				<div class="menu_phone ml-auto">Call us: 00-56 445 678 33</div>
				<ul class="d-flex flex-row align-items-start justify-content-start">
					<li><a href="#"><i class="fa fa-pinterest" aria-hidden="true"></i></a></li>
					<li><a href="#"><i class="fa fa-facebook" aria-hidden="true"></i></a></li>
					<li><a href="#"><i class="fa fa-twitter" aria-hidden="true"></i></a></li>
					<li><a href="#"><i class="fa fa-dribbble" aria-hidden="true"></i></a></li>
					<li><a href="#"><i class="fa fa-behance" aria-hidden="true"></i></a></li>
					<li><a href="#"><i class="fa fa-linkedin" aria-hidden="true"></i></a></li>
				</ul>
			{% endif %}
		</div>
	</div>
	
	<!-- Home -->

	<div class="home">
		
		<!-- Home Slider -->
		<div class="home_slider_container">
			<div class="owl-carousel owl-theme home_slider">
				
				<!-- Slide -->
				<div class="owl-item">
					<div class="background_image" style="background-image:url({% static 'images/home_slider.jpg' %})"></div>
					<div class="home_slider_content_container">
						<div class="container">
							<div class="row">
								<div class="col">
									<div class="home_slider_content">
										<div class="home_title"><h2>Let us take you away</h2></div>
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>

				<!-- Slide -->
				<div class="owl-item">
					<div class="background_image" style="background-image:url({% static 'images/home_slider.jpg' %})"></div>
					<div class="home_slider_content_container">
						<div class="container">
							<div class="row">
								<div class="col">
									<div class="home_slider_content">
										<div class="home_title"><h2>Let us take you away</h2></div>
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>

				<!-- Slide -->
				<div class="owl-item">
					<div class="background_image" style="background-image:url({% static 'images/home_slider.jpg' %})"></div>
					<div class="home_slider_content_container">
						<div class="container">
							<div class="row">
								<div class="col">
									<div class="home_slider_content">
										<div class="home_title"><h2>Let us take you away</h2></div>
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>

			</div>

			<div class="home_page_nav">
				<ul class="d-flex flex-column align-items-end justify-content-end">
					<li><a href="#" data-scroll-to="#destinations">Offers<span>01</span></a></li>
					<li><a href="#" data-scroll-to="#testimonials">Testimonials<span>02</span></a></li>
					<li><a href="#" data-scroll-to="#news">Latest<span>03</span></a></li>
				</ul>
			</div>
		</div>
	</div>

	<!-- Search -->

<!--	<div class="home_search">-->
<!--		<div class="container">-->
<!--			<div class="row">-->
<!--				<div class="col">-->
<!--					<div class="home_search_container">-->
<!--						<div class="home_search_title">Search for your trip</div>-->
<!--						<div class="home_search_content">-->
<!--							<form action="#" class="home_search_form" id="home_search_form">-->
<!--								<div class="d-flex flex-lg-row flex-column align-items-start justify-content-lg-between justify-content-start">-->
<!--									<input type="text" class="search_input search_input_1" placeholder="City" required="required">-->
<!--									<input type="text" class="search_input search_input_2" placeholder="Departure" required="required">-->
<!--									<input type="text" class="search_input search_input_3" placeholder="Arrival" required="required">-->
<!--									<input type="text" class="search_input search_input_4" placeholder="Budget" required="required">-->
<!--									<button class="home_search_button">search</button>-->
<!--								</div>-->
<!--							</form>-->
<!--						</div>-->
<!--					</div>-->
<!--				</div>-->
<!--			</div>-->
<!--		</div>-->
<!--	</div>-->

<!--	&lt;!&ndash; Intro &ndash;&gt;-->

	<div class="intro">
		<div class="intro_background" style="background-image:url({% static 'images/intro.png' %})"></div>
		<div class="container">
			<div class="row">
				<div class="col">
					<div class="intro_container">
						<div class="row">

							<!-- Intro Item -->
							<div class="col-lg-4 intro_col">
								<div class="intro_item d-flex flex-row align-items-end justify-content-start">
									<div class="intro_icon"><img src="{% static 'images/beach.svg' %}" alt=""></div>
									<div class="intro_content">
										<div class="intro_title">Top Destinations</div>
										<div class="intro_subtitle"><p>Enjoy the journey as much as the destination.</p></div>
									</div>
								</div>
							</div>

							<!-- Intro Item -->
							<div class="col-lg-4 intro_col">
								<div class="intro_item d-flex flex-row align-items-end justify-content-start">
									<div class="intro_icon"><img src="{% static 'images/wallet.svg' %}" alt=""></div>
									<div class="intro_content">
										<div class="intro_title">The Best Prices</div>
										<div class="intro_subtitle"><p>Don't be slow! Our prices are low.The best for less.</p></div>
									</div>
								</div>
							</div>

							<!-- Intro Item -->
							<div class="col-lg-4 intro_col">
								<div class="intro_item d-flex flex-row align-items-end justify-content-start">
									<div class="intro_icon"><img src="{% static 'images/suitcase.svg' %}" alt=""></div>
									<div class="intro_content">
										<div class="intro_title">Amazing Services</div>
										<div class="intro_subtitle"><p>Make a customer, not a sale. Make the customer the hero of your story.</p></div>
									</div>
								</div>
							</div>

						</div>
					</div>
				</div>		
			</div>
		</div>
	</div>

	<!-- Destinations -->

	<div class="destinations" id="destinations">
		<div class="container">
			<div class="row">
				<div class="col text-center">
					<div class="section_subtitle">simply amazing places</div>
					<div class="section_title"><h2>Popular Destinations</h2></div>
				</div>
			</div>
			<div class="row destinations_row">
				<div class="col">
					<div class="destinations_container item_grid">

						<!-- Destination -->
						
						{% for dest in dests %}
						<div class="destination item">
							<div class="destination_image">
								<img src="{{dest.img.url}}" alt="">
								{% if dest.offer %}
								<div class="spec_offer text-center"><a href="#">Special Offer</a></div>
								{% endif %}
							</div>
							<div class="destination_content">
								<div class="destination_title"><a href="accounts/destinations">{{dest.name}}</a></div>
								<div class="destination_subtitle"><p>{{dest.desc}}</p></div>
								<div class="destination_price">From ${{dest.price}}</div>
							</div>
						</div>

						{% endfor %}

					</div>
				</div>
			</div>
		</div>
	</div>

	<!-- Testimonials -->

	<div class="testimonials" id="testimonials">
		<div class="parallax_background parallax-window" data-parallax="scroll" data-image-src="{% static 'images/testimonials.jpg' %}" data-speed="0.8"></div>
		<div class="container">
			<div class="row">
				<div class="col text-center">
					<div class="section_subtitle">simply amazing places</div>
					<div class="section_title"><h2>Testimonials</h2></div>
				</div>
			</div>
			<div class="row testimonials_row">
				<div class="col">

					<!-- Testimonials Slider -->
					<div class="testimonials_slider_container">
						<div class="owl-carousel owl-theme testimonials_slider">
							
							<!-- Slide -->
							<div class="owl-item text-center">
								<div class="testimonial">Booking through you was very easy and made our lives so much easier.
									I have nothing bad to say! Thank you for giving us tips and guidance before we left on
									what to bring and such, that was very helpful! </div>
								<div class="testimonial_author">
									<div class="testimonial_author_content d-flex flex-row align-items-end justify-content-start">
										<div>,</div>
										<div>client</div>
									</div>
								</div>
							</div>

							<!-- Slide -->
							<div class="owl-item text-center">
								<div class="testimonial">Booking through you was very easy and made our lives so much easier.
									I have nothing bad to say! Thank you for giving us tips and guidance before we left on what to bring and such,
									that was very helpful! </div>
								<div class="testimonial_author">
									<div class="testimonial_author_content d-flex flex-row align-items-end justify-content-start">
										<div>john turner,</div>
										<div>client</div>
									</div>
								</div>
							</div>

							<!-- Slide -->
							<div class="owl-item text-center">
								<div class="testimonial">Booking through you was very easy and made our lives so much easier.
									I have nothing bad to say! Thank you for giving us tips and guidance before we left on what to bring and such,
									that was very helpful! </div>
								<div class="testimonial_author">
									<div class="testimonial_author_content d-flex flex-row align-items-end justify-content-start">
										<div>john turner,</div>
										<div>client</div>
									</div>
								</div>
							</div>

						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="test_nav">
			<ul class="d-flex flex-column align-items-end justify-content-end">
				<li><a href="#">City Breaks Clients<span>01</span></a></li>
				<li><a href="#">Cruises Clients<span>02</span></a></li>
				<li><a href="#">All Inclusive Clients<span>03</span></a></li>
			</ul>
		</div>
	</div>

	<!-- News -->

	<div class="news" id="news">
		<div class="container">
			<div class="row">
				<div class="col-xl-8">
					<div class="news_container">
						
						<!-- News Post -->
						<div class="news_post d-flex flex-md-row flex-column align-items-start justify-content-start">
							<div class="news_post_image"><img src="{% static 'images/news_1.jpg' %}" alt=""></div>
							<div class="news_post_content">
								<div class="news_post_date d-flex flex-row align-items-end justify-content-start">
									<div>02</div>
									<div>june</div>
								</div>
								<div class="news_post_title"><a href="#">Best tips to travel light</a></div>
								<div class="news_post_category">
									<ul>
										<li><a href="#">lifestyle & travel</a></li>
									</ul>
								</div>
								<div class="news_post_text">
									<p>Think innovative. Think what all will be your activities during the holiday.</p>
								</div>
							</div>
						</div>

						<!-- News Post -->
						<div class="news_post d-flex flex-md-row flex-column align-items-start justify-content-start">
							<div class="news_post_image"><img src="{% static 'images/news_2.jpg' %}" alt=""></div>
							<div class="news_post_content">
								<div class="news_post_date d-flex flex-row align-items-end justify-content-start">
									<div>01</div>
									<div>june</div>
								</div>
								<div class="news_post_title"><a href="#">Best tips to travel light</a></div>
								<div class="news_post_category">
									<ul>
										<li><a href="#">lifestyle & travel</a></li>
									</ul>
								</div>
								<div class="news_post_text">
									<p>Decide Where You Want to Go.Narrow It down to a Specific Destination.Find the Perfect Amount of Time Away.</p>
								</div>
							</div>
						</div>

						<!-- News Post -->
						<div class="news_post d-flex flex-md-row flex-column align-items-start justify-content-start">
							<div class="news_post_image"><img src="{% static 'images/news_3.jpg' %}" alt=""></div>
							<div class="news_post_content">
								<div class="news_post_date d-flex flex-row align-items-end justify-content-start">
									<div>29</div>
									<div>may</div>
								</div>
								<div class="news_post_title"><a href="#">Best tips to travel light</a></div>
								<div class="news_post_category">
									<ul>
										<li><a href="#">lifestyle & travel</a></li>
									</ul>
								</div>
								<div class="news_post_text">
									<p>India is home to some charming hill stations that are counted as the best places to go for honeymoon in summer.</p>
								</div>
							</div>
						</div>

					</div>
				</div>

				<!-- News Sidebar -->
				<div class="col-xl-4">
					<div class="travello">
						<div class="background_image" style="background-image:url({% static 'images/travello.jpg' %})"></div>
						<div class="travello_content">
							<div class="travello_content_inner">
								<div></div>
								<div></div>
							</div>
						</div>
						<div class="travello_container">
							<a href="#">
								<div class="d-flex flex-column align-items-center justify-content-end">
									<span class="travello_title">Get a 20% Discount</span>
									<span class="travello_subtitle">Buy Your Vacation Online Now</span>
								</div>
							</a>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>

	<!-- Footer -->

	<footer class="footer">
		<div class="parallax_background parallax-window" data-parallax="scroll" data-image-src="{% static 'images/footer_1.jpg' %}" data-speed="0.8"></div>
		<div class="container">
			<div class="row">
				<div class="col">
					<div class="newsletter">
						<div class="newsletter_title_container text-center">
							<div class="newsletter_title">Subscribe to our newsletter to get the latest trends & news</div>
						</div>
						<div class="newsletter_form_container">
							<form action="#" class="newsletter_form d-flex flex-md-row flex-column align-items-start justify-content-between" id="newsletter_form">
								<div class="d-flex flex-md-row flex-column align-items-start justify-content-between">
									<div><input type="text" class="newsletter_input newsletter_input_name" id="newsletter_input_name" placeholder="Name" required="required"><div class="input_border"></div></div>
									<div><input type="email" class="newsletter_input newsletter_input_email" id="newsletter_input_email" placeholder="Your e-mail" required="required"><div class="input_border"></div></div>
								</div>
								<div><button style="background-color: brown;" class="newsletter_button">subscribe</button></div>
							</form>
						</div>
					</div>
				</div>
			</div>
			<div class="row footer_contact_row">
				<div class="col-xl-10 offset-xl-1">
					<div class="row">

						<!-- Footer Contact Item -->
						<div class="col-xl-4 footer_contact_col">
							<div class="footer_contact_item d-flex flex-column align-items-center justify-content-start text-center">
								<div class="footer_contact_icon"><img src="{% static 'images/sign.svg' %}" alt=""></div>
								<div class="footer_contact_title">give us a call</div>
								<div class="footer_contact_list">
									<ul>
										<li>Office Landline: 2571126</li>
										<li>Mobile: 0866 666 1000</li>
									</ul>
								</div>
							</div>
						</div>

						<!-- Footer Contact Item -->
						<div class="col-xl-4 footer_contact_col">
							<div class="footer_contact_item d-flex flex-column align-items-center justify-content-start text-center">
								<div class="footer_contact_icon"><img src="{% static 'images/trekking.svg' %}" alt=""></div>
								<div class="footer_contact_title">come & drop by</div>
								<div class="footer_contact_list">
									<ul style="max-width:190px">
										<li>40-13-6, behind Varun Bajaj, Chandra Mouli Puram, Benz Circle, Vijayawada, Andhra Pradesh</li>
									</ul>
								</div>
							</div>
						</div>

						<!-- Footer Contact Item -->
						<div class="col-xl-4 footer_contact_col">
							<div class="footer_contact_item d-flex flex-column align-items-center justify-content-start text-center">
								<div class="footer_contact_icon"><img src="{% static 'images/around.svg' %}" alt=""></div>
								<div class="footer_contact_title">send us a message</div>
								<div class="footer_contact_list">
									<ul>
										<li>travelagency@gmail.com</li>
									</ul>
								</div>
							</div>
						</div>

					</div>
				</div>
			</div>
		</div>
		<div style="background-color: black;" class="col text-center"><!-- Link back to Colorlib can't be removed. Template is licensed under CC BY 3.0. -->
Copyright &copy;<script>document.write(new Date().getFullYear());</script> All rights reserved | This template is made with <i class="fa fa-heart-o" aria-hidden="true"></i> by <a href="https://instagram.com/kmranrg" target="_blank">Kumar Anurag</a> | Credits:<a href="https://colorlib.com/" target="_blank"> Colorlib</a>
<!-- Link back to Colorlib can't be removed. Template is licensed under CC BY 3.0. --> </div>
	</footer>
</div>

<script src="{% static 'js/jquery-3.2.1.min.js' %}"></script>
<script src="{% static 'styles/bootstrap4/popper.js' %}"></script>
<script src="{% static 'styles/bootstrap4/bootstrap.min.js' %}"></script>
<script src="{% static 'plugins/OwlCarousel2-2.2.1/owl.carousel.js' %}"></script>
<script src="{% static 'plugins/Isotope/isotope.pkgd.min.js' %}"></script>
<script src="{% static 'plugins/scrollTo/jquery.scrollTo.min.js' %}"></script>
<script src="{% static 'plugins/easing/easing.js' %}"></script>
<script src="{% static 'plugins/parallax-js-master/parallax.min.js' %}"></script>
<script src="{% static 'js/custom.js' %}"></script>

<!-- Global site tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-23581568-13"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'UA-23581568-13');
</script>


</body>

</html>
