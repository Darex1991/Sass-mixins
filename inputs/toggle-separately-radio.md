# Sass

	.radio
	  &--primary
	    &__input
	      display: none
	      &:checked ~ .radio--primary__text
	        background-color: $color-gray-dark
	        color: $color-white
	
	    &__text
	      @extend %btn-base
	      @extend %btn
	      +truncate
	      +font-smooth
	      background-color: $color-white
	      border-color: $color-gray-dark
	      color: $color-gray-dark
	      font-size: $font-size-base
	      max-width: 100%
	
	      &:hover
	        background-color: $color-gray-dark
	        color: $color-white

# HAML

	.row
	  label.radio--primary.col-xs-5 for='Private'
	    input.radio--primary__input type='radio' checked='true' id='Private' name='radio2'
	    .radio--primary__text Private
	
	  label.radio--primary.col-xs-5 for='Public'
	    input.radio--primary__input type='radio' id='Public' name='radio2'
	    .radio--primary__text Public
