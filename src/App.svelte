<script>
    let name =" ";
    let result =''
    $: show = `${name + result}`
	const namechanger= (y)=>{
   name += y
   result= ""
}
const total =()=>{
    result= eval(name)
    name=" "
}
const cancel= (y)=>{
   name = " "
   result = ""
}
</script>

<main>
 <table>
  <tr>
     <td colspan="4"><input type="text"  bind:value ={show}  readonly="true">  </td>      
</tr>
  <tr>
       <td><button on:click= {()=>{namechanger('1')}}>1</button></td>
        <td> <button on:click= {()=>{namechanger('2')}}>2</button></td>
        <td> <button on:click= {()=>{namechanger('3')}}>3</button></td>
        <td><button on:click= {()=>{namechanger('+')}}>+</button></td> 
        
</tr>
   
    <tr>
        <td> <button on:click= {()=>{namechanger('4')}}>4</button></td>
       <td> <button on:click= {()=>{namechanger('5')}}>5</button></td>
        <td> <button on:click= {()=>{namechanger('6')}}>6</button></td>
        <td><button on:click= {()=>{namechanger('*')}}>x</button></td> 
     </tr> 
     <tr> 
        <td> <button on:click= {()=>{namechanger('7')}}>7</button></td>
         <td> <button on:click= {()=>{namechanger('8')}}>8</button></td>
        <td> <button on:click= {()=>{namechanger('9')}}>9</button></td>
        <td><button on:click= {()=>{namechanger('/')}}>/</button></td> 
    </tr>
   
    <tr>
       <td> <button on:click= {()=>{cancel('')}}>c</button></td>
        <td> <button on:click= {()=>{namechanger('0')}}>0</button></td>
         <td> <button on:click= {total}>=</button></td>
        <td> <button on:click= {()=>{namechanger('-')}}>-</button></td>
    </tr>
   

</table>
</main>

<style>
	main{
    position: absolute;
    top: 40%;
    left: 50%;
    transform: translate(-50%, -50%);
    }
    table{
       margin: auto;
  background-color: black;

  max-width: 29.5rem;
  height: 32.5rem;
  text-align: center;
  border-radius: 0.4rem;
  padding-right: 1rem;
    }
button{
  outline: 0;
  position: relative;
  left: 0.5rem;
  top: 0.5rem;
  border: 0;
  color: gray;
  background-color: #fff;
  border-radius: 0.4rem;
  width: 6rem;
  height: 5rem;
  float: left;
  margin: 0.5rem;
  font-size: 2rem;
  box-shadow: 0 0.4rem rgba(0,0,0,0.2);
  margin-bottom: 1.5rem;
}
button:active {
  top: 0.4rem;
  border: 0 solid #000;
  color: #495069;
  background-color: #fff;
  border-radius: 0.4rem;
  width: 6rem;
  height: 5rem;
  float: left;
  margin: 0.5rem;
  font-size: 2rem;
  box-shadow: none;
}
input{
    width: 26.5rem;
  max-width: 27rem;
  font-size: 26px;
  text-align: right;
  background-color: #bcbd95;
  float: left;
}

</style>