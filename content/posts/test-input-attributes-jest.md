---
title: 'Test Input Attributes in Jest'
date: 2020-03-03T08:51:00+02:00
draft: false
---

** How to test a required input field of a React Component in Jest **

```javascript
it.only('title field of the form is required', () => {
  const wrapper = mount(<Topic state={fetchedState} />);
  expect(
    wrapper.find('input').filterWhere((item) => {
      return item.prop('required') === true;
    })
  ).toHaveLength(1);
});
```

[source](https://github.com/enzymejs/enzyme/issues/669)
