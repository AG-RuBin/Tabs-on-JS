# Tabs on JS (EN)

Creating tabs on JavaScript language.

#### HTML

```
<div id="tabs">
    <div class="tab whiteborder">Tab 1</div>
    <div class="tab">Tab 2</div>
    <div class="tab">Tab 3</div>
    <div class="tabContent">Вкладка 1</div>
    <div class="tabContent">Вкладка 2</div>
    <div class="tabContent">Вкладка 3</div>
</div>
```

#### CSS

```
#tabs .tab {
    display: inline-block;
    padding: 5px 10px;
    cursor: pointer;
    position: relative;
    z-index: 5;
}

#tabs .whiteborder {
    border: 1px solid #707070;
    border-bottom: 1px solid #fff;
    border-radius: 3px 3px 0 0;
}

#tabs .tabContent {
    width: 300px;
    height: 60px;
    border: 1px solid #707070;
    position: relative;
    top: -1px;
    z-index: 1;
    padding: 10px;
    border-radius: 0 0 3px 3px;
}

#tabs .hide {
    display: none;
}

#tabs .show {
    display: block;
}
```

#### JavaScript

```
var tab
var tabContent

window.onload = function () {
    tabContent = document.getElementsByClassName('tabContent')
    tab = document.getElementsByClassName('tab')
    hideTabsContent(1)
}

function hideTabsContent(a) {
    for (var i = a; i < tabContent.length; i++) {
        tabContent[i].classList.remove('show')
        tabContent[i].classList.add('hide')
        tab[i].classList.remove('whiteborder')
    }
}

document.getElementById('tabs').onclick = function (event) {
    var target = event.target
    if (target.className == 'tab') {
        for (var i = 0; i < tab.length; i++) {
            if (target == tab[i]) {
                showTabsContent(i)
                break
            }
        }
    }
}

function showTabsContent(b) {
    if (tabContent[b].classList.contains('hide')) {
        hideTabsContent(0)
        tab[b].classList.add('whiteborder')
        tabContent[b].classList.remove('hide')
        tabContent[b].classList.add('show')
    }
}
```

# Ползунок на JS (RU)

Создание вкладок на языке JavaScript.

#### HTML

```
<div id="tabs">
    <div class="tab whiteborder">Tab 1</div>
    <div class="tab">Tab 2</div>
    <div class="tab">Tab 3</div>
    <div class="tabContent">Вкладка 1</div>
    <div class="tabContent">Вкладка 2</div>
    <div class="tabContent">Вкладка 3</div>
</div>
```

#### CSS

```
#tabs .tab {
    display: inline-block;
    padding: 5px 10px;
    cursor: pointer;
    position: relative;
    z-index: 5;
}

#tabs .whiteborder {
    border: 1px solid #707070;
    border-bottom: 1px solid #fff;
    border-radius: 3px 3px 0 0;
}

#tabs .tabContent {
    width: 300px;
    height: 60px;
    border: 1px solid #707070;
    position: relative;
    top: -1px;
    z-index: 1;
    padding: 10px;
    border-radius: 0 0 3px 3px;
}

#tabs .hide {
    display: none;
}

#tabs .show {
    display: block;
}
```

#### JavaScript

```
var tab
var tabContent

window.onload = function () {
    tabContent = document.getElementsByClassName('tabContent')
    tab = document.getElementsByClassName('tab')
    hideTabsContent(1)
}

function hideTabsContent(a) {
    for (var i = a; i < tabContent.length; i++) {
        tabContent[i].classList.remove('show')
        tabContent[i].classList.add('hide')
        tab[i].classList.remove('whiteborder')
    }
}

document.getElementById('tabs').onclick = function (event) {
    var target = event.target
    if (target.className == 'tab') {
        for (var i = 0; i < tab.length; i++) {
            if (target == tab[i]) {
                showTabsContent(i)
                break
            }
        }
    }
}

function showTabsContent(b) {
    if (tabContent[b].classList.contains('hide')) {
        hideTabsContent(0)
        tab[b].classList.add('whiteborder')
        tabContent[b].classList.remove('hide')
        tabContent[b].classList.add('show')
    }
}
```
