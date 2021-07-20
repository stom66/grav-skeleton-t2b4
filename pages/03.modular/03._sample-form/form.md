---
column: col-6
image_align: left
custom_classes: text-right
process:
    markdown: true
    twig: true
title: Sample Form
form:
    name: contact
    rounded: 2
    label_width: 3
    row_margin: my-3
    fields:
        checkbox1:
          label: "Checkbox!"
          type: checkbox
        checkboxes:
          type: checkboxes
          label: Checkboxes
          default:
              - option1
              - option2
          options:
              option1: Option 1
              option2: Option 2
              option3: Option 3
              option4: Option 4
              option5: Option 5
        date:      
          type: date
          label: Enter a date
          validate.min: "2014-01-01"
          validate.max: "2018-12-31"
        email:
          label: Email
          placeholder: Enter your email address
          type: email
          validate:
            required: true
        message:
          label: Message
          placeholder: Enter your message
          type: textarea
          validate:
            required: true
        name:
          label: Name
          placeholder: Enter your name
          autocomplete: on
          type: text
          validate:
            required: true
        password:
          type: password
          label: Password
        radio:
          type: radio
          label: Radios
          default: option1
          options:
            option1: Option 1
            option2: Option 2
            option3: Option 3
            option4: Option 4
        selection:
          type: select
          label: Selector
          default: title
          help: 'Pages in a list will render using this order unless it is overridden'
          options:
            default: 'Default - based on folder name'
            folder: 'Folder - based on prefix-less folder name'
            title: 'Title - based on title field in header'
            date: 'Date - based on date field in header'
        upload1:
          label: Upload
          type: file
          multiple: false
          destination: @self
          accept: []
        g-recaptcha-response:
          label: Captcha
          type: captcha
          recaptcha_not_validated: 'Captcha not valid!'
    buttons:
        submit:
          type: submit
          value: Submit
          classes: btn btn-primary
        reset:
          type: reset
          value: Reset
          classes: btn btn-primary
    process:
        captcha: true
        save:
            fileprefix: contact-
            dateformat: Ymd-His-u
            extension: txt
            body: "{% include 'forms/data.txt.twig' %}"
        email:
            subject: "[Site Contact Form] {{ form.value.name|e }}"
            body: "{% include 'forms/data.html.twig' %}"
        message: Thank you for getting in touch!
        display: thankyou
---