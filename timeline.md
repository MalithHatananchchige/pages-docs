# Timeline

Pages timeline has been adapted from [CodyHouse Timeline example](http://codyhouse.co/gem/vertical-timeline/).

**Step one**

Start by creating the markup for the timeline. We recommend that you use the same card elements which were introduced in [Pages Social app](http://pages.revox.io/dashboard/3.0.0/docs/partials/social.html) for each post of the timeline

```markup
<div class="timeline-container">
    <section class="timeline">
        <div class="timeline-block">
            <div class="timeline-point success">
                <i class="pg-map"></i>
            </div>
            <!-- timeline-point -->
            <div class="timeline-content">
                <!-- START CARD ELEMENT -->
                <div class="card share full-width">
                    <div class="circle" data-toggle="tooltip" title="Label">
                    </div>
                    <div class="card-header clearfix">
                        <div class="user-pic">
                            <img alt="Profile Image" width="33" height="33" data-src-retina="assets/img/profiles/8x.jpg" data-src="assets/img/profiles/8.jpg" src="assets/img/profiles/8x.jpg">
                        </div>
                        <h5>Jeff Curtis</h5>
                        <h6>Shared a Tweet
                                <span class="location semi-bold"><i class="fa fa-map-marker"></i> SF, California</span>
                            </h6>
                    </div>
                    <div class="card-description">
                        <p>What you think, you become. What you feel, you attract. What you imagine, you create - Buddha. <a href="#">#quote</a> </p>
                        <div class="via">via Twitter</div>
                    </div>
                </div>
                <!-- END CARD ELEMENT -->
                <div class="event-date">
                    <h6 class="font-montserrat all-caps hint-text m-t-0">Apple Inc</h6>
                    <small class="fs-12 hint-text">15 January 2015, 06:50 PM</small>
                </div>
            </div>
            <!-- timeline-content -->
        </div>
        
        <div class="timeline-block">
          ...
        </div>

    </section>
    <!-- timeline -->
</div>
```

**Step one**

Add the following snippet to make the posts appear on scroll with a nice fade in effect.

```javascript
jQuery(document).ready(function($){
    var $timeline_block = $('.timeline-block');

    //hide timeline blocks which are outside the viewport
    $timeline_block.each(function(){
        if($(this).offset().top > $(window).scrollTop()+$(window).height()*0.75) {
            $(this).find('.timeline-point, .timeline-content').addClass('is-hidden');
        }
    });

    //on scolling, show/animate timeline blocks when enter the viewport
    $(window).on('scroll', function(){
        $timeline_block.each(function(){
            if( $(this).offset().top <= $(window).scrollTop()+$(window).height()*0.75 && $(this).find('.timeline-point').hasClass('is-hidden') ) {
                $(this).find('.timeline-point, .timeline-content').removeClass('is-hidden').addClass('bounce-in');
            }
        });
    });
});
```

**Aligning elements**

By default the posts will be spread on both sides of a vertical axis for larger screens. For small/medium screens the posts will be aligned to left automatically. Explicity specifying either `left` or `center` classes in the `timeline-container` element, posts will be forced not to change the layout type relevant to screen size.

```markup
<!-- ALIGN timeline-block ITEMS TO LEFT -->
    <div class="timeline-container left">
    <section class="timeline">
        
        <div class="timeline-block">
          ...
        </div>
    </section>
    <!-- timeline -->
</div>
```

