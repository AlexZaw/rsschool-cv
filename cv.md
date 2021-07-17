# **Alexandr Zawgorodniy**

<img src="./img/email.svg" width="24" valign="middle"> <alexandr.zawgorodniy@gmail.com>

 <img src="./img/telegram.svg" width="24" valign="middle"> <https://t.me/Alex_Zaw>

## Professional skills

* _HTML_
* _CSS (SCSS)_
* _JS_
* _Git_
* _Gulp_
* _BEM_
* _Figma_
* _Photoshop_
* _Adobe XD_

## Experience

* _Implementation of educational projects on layout and javascript_
* _Code refactoring and error correction in someone else's code_

## Sample code

```javascript
const filterForm = document.querySelector('.map__filters');
const ANY_RANGE = 'any';
const PRICE_RANGE = {
  LOW: {
    MIN: 0,
    MAX: 10000,
  },
  MIDDLE: {
    MIN: 10000,
    MAX: 50000,
  },
  HIGH: {
    MIN: 50000,
    MAX: Infinity,
  },
};

const FILTERS ={
  TYPE: filterForm['housing-type'],
  PRICE: filterForm['housing-price'],
  ROOMS: filterForm['housing-rooms'],
  GUESTS: filterForm['housing-guests'],
};

const adFilter = (adsArray) => {
  const filtersValue = {
    type: FILTERS.TYPE.value,
    price: FILTERS.PRICE.value.toUpperCase(),
    rooms: Number(FILTERS.ROOMS.value) ||
      FILTERS.ROOMS.value.toLowerCase(),
    guests: Number(FILTERS.GUESTS.value) ||
      FILTERS.GUESTS.value.toLowerCase(),
  };
  const filterKeys = Object.keys(filtersValue);
  const filteredAds = adsArray.slice()
    .filter((currentAd) => filterKeys.every((key) => {
      if (key === 'price') {
        if (Object.prototype.hasOwnProperty.call(PRICE_RANGE, filtersValue[key])) {
          const min = PRICE_RANGE[filtersValue[key]].MIN;
          const max = PRICE_RANGE[filtersValue[key]].MAX;
          return (currentAd.offer[key] >= min && currentAd.offer[key] <= max);
        }
        return true;
      }
      return currentAd.offer[key] === filtersValue[key] || filtersValue[key] === ANY_RANGE;
    }));
  return filteredAds;
};
```

## Projects

Project type      | Project Name       | Tech used
------------------|:------------------:|----------:
Training project  | [Keksobooking][1]  | JS
Training project  | [Cat Energy][2]    | HTML, CSS, JS
Browser extension | [SelectCode][3]    | JS

## Education

* **Tomsk Radio Mechanical College** 
    * _Faculty of Radio Electronics and Equipment_

* **Courses**
    * _[HTML Academy Frontend developer](https://htmlacademy.ru/profession/frontender)_

* **Self-education**

    * _[The Modern JavaScript Tutorial](https://learn.javascript.ru/)_
    * _[CSS-TRICKS](https://css-tricks.com/)_
    * _[WEB Standards](https://web-standards.ru/)_
    * _Different YouTube channels_
    * _etc_

## Languages

* _Russian - native_
* _English - Pre-Intermediate_

[1]: [https://github.com/AlexZaw/397481-keksobooking-23]
[2]: [https://github.com/AlexZaw/397481-cat-energy-22]
[3]: [https://github.com/AlexZaw/SelectCode]