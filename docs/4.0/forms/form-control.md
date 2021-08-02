---
title: Vue Form Controls
name: Form control
description: Vue input and textarea components. Give textual form controls like `<input>`s and `<textarea>`s an upgrade with custom styles, sizing, focus states, and more.
---

## Example

::: demo
<CForm>
  <div class="mb-3">
    <CFormLabel for="exampleFormControlInput1">Email address</CFormLabel>
    <CFormInput type="email" id="exampleFormControlInput1" placeholder="name@example.com"/>
  </div>
  <div class="mb-3">
    <CFormLabel for="exampleFormControlTextarea1">Example textarea</CFormLabel>
    <CFormTextarea id="exampleFormControlTextarea1" rows="3"></CFormTextarea>
  </div>
</CForm>
:::
```vue
<CForm>
  <div class="mb-3">
    <CFormLabel for="exampleFormControlInput1">Email address</CFormLabel>
    <CFormInput type="email" id="exampleFormControlInput1" placeholder="name@example.com"/>
  </div>
  <div class="mb-3">
    <CFormLabel for="exampleFormControlTextarea1">Example textarea</CFormLabel>
    <CFormTextarea id="exampleFormControlTextarea1" rows="3"></CFormTextarea>
  </div>
</CForm>
```

## Sizing

Set heights using `size` property like `size="lg"` and `size="sm"`.

::: demo
<CFormInput type="text" size="lg" placeholder="Large input" aria-label="lg input example"/>
<br/>
<CFormInput type="text" placeholder="Default input" aria-label="default input example"/>
<br/>
<CFormInput type="text" size="sm" placeholder="Small input" aria-label="sm input example"/>
:::
```vue
<CFormInput type="text" size="lg" placeholder="Large input" aria-label="lg input example"/>
<br/>
<CFormInput type="text" placeholder="Default input" aria-label="default input example"/>
<br/>
<CFormInput type="text" size="sm" placeholder="Small input" aria-label="sm input example"/>
```

## Disabled

Add the `disabled` boolean attribute on an input to give it a grayed out appearance and remove pointer events.

::: demo
<CFormInput type="text" placeholder="Disabled input" aria-label="Disabled input example" disabled/>
<br/>
<CFormInput type="text" placeholder="Disabled readonly input" aria-label="Disabled input example" disabled readOnly/>
<br/>
:::
```vue
<CFormInput type="text" placeholder="Disabled input" aria-label="Disabled input example" disabled/>
<br/>
<CFormInput type="text" placeholder="Disabled readonly input" aria-label="Disabled input example" disabled readOnly/>
<br/>
```

## Readonly

Add the `readOnly` boolean attribute on an input to prevent modification of the input's value. Read-only inputs appear lighter (just like disabled inputs), but retain the standard cursor.

::: demo
<CFormInput type="text" placeholder="Readonly input here..." aria-label="readonly input example" readOnly/>
:::
```vue
<CFormInput type="text" placeholder="Readonly input here..." aria-label="readonly input example" readOnly/>
```

## Readonly plain text

If you want to have `<input readonly>` elements in your form styled as plain text, use the `plainText` boolean property to remove the default form field styling and preserve the correct margin and padding.

::: demo
<CRow class="mb-3">
  <CFormLabel for="staticEmail" class="col-sm-2 col-form-label">Email</CFormLabel>
  <div class="col-sm-10">
    <CFormInput type="text" id="staticEmail" defaultValue="email@example.com" readOnly plainText/>
  </div>
</CRow>
<CRow class="mb-3">
  <CFormLabel for="inputPassword" class="col-sm-2 col-form-label">Password</CFormLabel>
  <div class="col-sm-10">
    <CFormInput type="password" id="inputPassword"/>
  </div>
</CRow>
:::
```vue
<CRow class="mb-3">
  <CFormLabel for="staticEmail" class="col-sm-2 col-form-label">Email</CFormLabel>
  <div class="col-sm-10">
    <CFormInput type="text" id="staticEmail" defaultValue="email@example.com" readOnly plainText/>
  </div>
</CRow>
<CRow class="mb-3">
  <CFormLabel for="inputPassword" class="col-sm-2 col-form-label">Password</CFormLabel>
  <div class="col-sm-10">
    <CFormInput type="password" id="inputPassword"/>
  </div>
</CRow>
```

::: demo
<CForm class="row g-3">
  <div class="col-auto">
    <CFormLabel for="staticEmail2" class="visually-hidden">Email</CFormLabel>
    <CFormInput type="text" id="staticEmail2" defaultValue="email@example.com" readOnly plainText/>
  </div>
  <div class="col-auto">
    <CFormLabel for="inputPassword2" class="visually-hidden">Password</CFormLabel>
    <CFormInput type="password" id="inputPassword2" placeholder="Password"/>
  </div>
  <div class="col-auto">
    <CButton type="submit" class="mb-3">Confirm identity</CButton>
  </div>
</CForm>
:::
```vue
<CForm class="row g-3">
  <div class="col-auto">
    <CFormLabel for="staticEmail2" class="visually-hidden">Email</CFormLabel>
    <CFormInput type="text" id="staticEmail2" defaultValue="email@example.com" readOnly plainText/>
  </div>
  <div class="col-auto">
    <CFormLabel for="inputPassword2" class="visually-hidden">Password</CFormLabel>
    <CFormInput type="password" id="inputPassword2" placeholder="Password"/>
  </div>
  <div class="col-auto">
    <CButton type="submit" class="mb-3">Confirm identity</CButton>
  </div>
</CForm>
```

## File input

::: demo
<div class="mb-3">
  <CFormLabel for="formFile">Default file input example</CFormLabel>
  <CFormInput type="file" id="formFile"/>
</div>
<div class="mb-3">
  <CFormLabel for="formFileMultiple">Multiple files input example</CFormLabel>
  <CFormInput type="file" id="formFileMultiple" multiple/>
</div>
<div class="mb-3">
  <CFormLabel for="formFileDisabled">Disabled file input example</CFormLabel>
  <CFormInput type="file" id="formFileDisabled" disabled/>
</div>
<div class="mb-3">
  <CFormLabel for="formFileSm">Small file input example</CFormLabel>
  <CFormInput type="file" size="sm" id="formFileSm"/>
</div>
<div>
  <CFormLabel for="formFileLg">Large file input example</CFormLabel>
  <CFormInput type="file" size="lg" id="formFileLg"/>
</div>
:::
```vue
<div class="mb-3">
  <CFormLabel for="formFile">Default file input example</CFormLabel>
  <CFormInput type="file" id="formFile"/>
</div>
<div class="mb-3">
  <CFormLabel for="formFileMultiple">Multiple files input example</CFormLabel>
  <CFormInput type="file" id="formFileMultiple" multiple/>
</div>
<div class="mb-3">
  <CFormLabel for="formFileDisabled">Disabled file input example</CFormLabel>
  <CFormInput type="file" id="formFileDisabled" disabled/>
</div>
<div class="mb-3">
  <CFormLabel for="formFileSm">Small file input example</CFormLabel>
  <CFormInput type="file" size="sm" id="formFileSm"/>
</div>
<div>
  <CFormLabel for="formFileLg">Large file input example</CFormLabel>
  <CFormInput type="file" size="lg" id="formFileLg"/>
</div>
```

## Color

::: demo
<CFormLabel for="exampleColorInput">Color picker</CFormLabel>
<CFormInput type="color" id="exampleColorInput" defaultValue="#563d7c" title="Choose your color" />
:::
```vue
<CFormLabel for="exampleColorInput">Color picker</CFormLabel>
<CFormInput type="color" id="exampleColorInput" defaultValue="#563d7c" title="Choose your color" />
```

## API

!!!include(./docs/api/form/CFormInput.api.md)!!!

!!!include(./docs/api/form/CFormTextarea.api.md)!!!