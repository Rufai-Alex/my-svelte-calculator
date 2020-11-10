<script>
    let name =" "
	const namechanger= (y)=>{
   name += y
}
const total =()=>{
    name= eval(name)
}
const cancel= (y)=>{
   name = " "
}
</script>

<main>
 <table>
  
    <tr> 
       <td><input type="text"  bind:value ={name} colspan="4" readonly="true"></td>        

  <tr>
        <td> <button on:click= {()=>{namechanger('1')}}>1</button></td>
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
	
</style>