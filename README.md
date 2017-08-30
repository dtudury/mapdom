# mapdom

mapping language (and code) to transform dom to a regular object and back

each module has methods:
.couple(el?, obverse?) //multiple el okay?
.toObj() //from el
.toHTML(indent?) //from el
.render() //to el

-----

<ul id="example">
    <li>1</li>
    <li>2</li>
    <li>3</li>
</ul>

h('ul', ARRAY,
    h('li', NUMBER)
)("#example")

// returns: [1,2,3]

-----

<ul id="example">
    <li>1</li>
    <li>2</li>
    <li>3</li>
</ul>

h('ul', OBJECT,
    h('li', NAME("a"), NUMBER),
    h('li', NAME("b"), NUMBER),
    h('li', NAME("c"), NUMBER)
)("#example")

// returns: {a:1, b:2, c:3}

-----
