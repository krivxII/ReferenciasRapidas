# Codigo implementado de useState

Uso Simple

```javascript
const [varState, setVarState] = useState( 'valor inicial' );
```

Si el valor inicial se calcula con un proceso pesado

```javascript
const [varState, setVarState] = useState( () => expensiveComputation() );
```

---

## Usando el valor previo en la funcion setVarState()

```javascript
setVar( (prev) => {/* la variable prev tendra el valor antiguo del estado*/} ) 
```

---

## Creando objetos complejos como variable de estado.

```javascript
//se actualiza el atributo count sumandole 1 al viejo valor
const [varObj, setVarObj] = useState({
  atributo1: '',
  count:0,
  objeto1: {
    id: 1,
    text: ''
  },
  objeto2: {
    id: 1,
    text: ''
  },
});

//actualizando un objeto no anidado
 setVarObj((prev)=>{return {...prev, count: prev.count+1}}

//Actualizando objeto anidado
 setCount((prev)=>{return {...prev, objeto1:{...prev.objeto1,count:prev.objeto1.count+1}}})
```
