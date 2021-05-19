
# props

Referencias rapidas para las propiedades en react

# Indice

- [Cosas a recordar](#Cosas-a-recordar)
- [Propiedades por defecto](#Propiedades-por-defecto)
- [Propiedades a variables de estado](#Propiedades-a-variables-de-estado)

--------------------------

## Cosas a recordar

- Las propiedades no se pueden crear dentro de la funcion.
- Las propiedades no se pueden modificar dentro de la funcion.

--------------------------

## Propiedades por defecto

```javascript
function ComponenteSuma(props) {
    let n1 = props.n1;
    if (typeof props.n1 === 'undefined') {
        n1 = 0
    }
    let n2 = props.n2;
    if (typeof props.n2 === 'undefined') {
        n2 = 0
    }
    return (<p>{n1+n2}</p>)
}
```

Mucha gente prefiere la ´destructuring syntax´ para hacer el codigo mas elegante

```javascript
function Add({n1=0, n2 = 0}) {
  return (
    <div>
      {n1} + {n2} = {n1 + n2}
    </div>
  )
}
```
[Indice](#Indice)

---

## Propiedades a variables de estado

```javascript
function AddWithInput({n1=0, n2 = 0}) {

  const [n22, setN22] = React.useState(n2)

  function handleInputChange(event) {
    const input = event.target
    setN22(Number(input.value));
    setN22(newN2)
  }

  return (
    <div>
      {n1} + <input type="number" value={n2} onChange={handleInputChange} /> ={' '}
      {n1 + n2}
    </div>
  )
}
```

[Indice](#Indice)
