## Indice
- [Cosas a recordar](#Cosas-a-recordar)
- [Propiedades por defecto](#Propiedades-por-defecto)

--------------------------
## Cosas a recordar
- Las propiedades no se pueden crear dentro de la funcion.
- Las propiedades no se pueden modificar dentro de la funcion.

[Indice](#Indice)

---------------------------
## Propiedades por defecto
Las propiedades no se pueden ni crear ni cambiar. Esto limita la forma en la que se pueden trabajar con ellas.

Una buena solucion es crear dentro de a funcion variables locales que almacenen el valor temporal de la propiedad y de no existir la propiedad se le asigna el valor por defecto

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