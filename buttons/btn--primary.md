# SASS

	$btn-padding-side: $m
	$btn-height: 45px
	$btn-sm-height: 35px
	
	@mixin btn-small
	  height: $btn-sm-height
	  line-height: $btn-sm-height
	  min-width: $btn-sm-height
	
	%btn-base
	  +animate(background-color, border-color, color)
	  border: 1px solid $brand-primary
	    radius: 30px
	  cursor: pointer
	  display: inline-block
	  font:
	    family: $font-family-base
	    size: $font-size-sm
	    weight: $font-weight-light
	  text-align: center
	
	  &:hover
	    text-decoration: none
	
	  &:focus
	    outline: none
	    
	%btn, .btn
	  line-height: $btn-height
	  padding:
	    left: $btn-padding-side
	    right: $btn-padding-side
	  min-width: 70px
	
	  /* ----- size ----- */
	  &--xs
	    height: $m
	    min-width: $m
	    &:before
	      font-size: $font-size-base
	      line-height: $m - 2
	      padding-left: 1px
	
	  &--sm
	    +btn-small
	
	  &--md
	    font-size: $font-size-base
	    line-height: 1
	    padding: $m-half $m
	
	  /* ----- primary ----- */
	  &--primary
	    @extend %btn-base
	    @extend %btn
	    background-color: $brand-primary
	    color: $color-white
	
	    &:hover
	      background-color: $color-white
	      color: $brand-primary
	
	    &--border
	      @extend %btn-base
	      @extend %btn
	      background-color: $color-transparent
	      color: $brand-primary
	
	      &:hover
	        background-color: $brand-primary
	        color: $color-white
	
	    &--icon
	      @extend %btn-base
	      @extend %btn-icon
	      color: $brand-primary
	
	      &:hover
	        background-color: $brand-primary
	        color: $color-white

# HAML
	
	.btn--primary Test
	.btn--primary--border Test
	
## or

	.btn--primary.icon-[type]
	.btn--primary--border.icon-[type]
