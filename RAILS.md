# Rails snippets
### Simple form
To add a wrapper for label use `boolean_style: :inline`

To change the tag that wraps the whole element use `item_wrapper_tag: 'div'`

`= f.association :choice, label_method: :text, as: :radio_buttons, boolean_style: :inline, wrapper_html: { class: 'hot-question' }, item_wrapper_tag: 'div'`
