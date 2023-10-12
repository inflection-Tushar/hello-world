<script>
	import Nested from './component/Nested.svelte';
  import Grreting from './component/grreting.svelte';
  import Firstcomponent from './component/firstcomponent.svelte';
  
// let fname="jay shree ram";
// let th="hello"
// const hello=()=>{
//     th="jay shree ram"
// }
// const reset=(a)=>{
//  if(a=="db"){
//     fname="Jay Shree ram"
//  }
//  else{
//     fname="Hare krisha"
//  }
    
// }
let f1=0;
let f2=0;
let sum=0;
let mul=0;
let div=0;
let sub=0;
const calculator=(a)=>{
    if(a=="sc"){
    f1+=1
    f2+=2
    sum=f1 + f2;
    div=f1/f2;
    mul=f1*f2;
    sub=f1-f2;
    alert(`your table is updated ${f1} times`)
}else{
    f1=0
    f2=0
    sum=0
    div=0
    mul=0
    sub=0
    alert(`your table is reset`)
}
}
</script>


<main>

    <!-- props example -->
    <!-- <h1 class="">{fname}</h1>
    <button on:click={()=>reset("sc")} on:contextmenu={()=>reset("db")} on:click={()=>hello()} >click</button> -->
	<!-- <Grreting {th}></Grreting>
<Firstcomponent {fname}></Firstcomponent> -->


<!-- reactivity example -->
<h1>reactivity</h1>
<button on:click={()=>calculator("sc")} on:contextmenu={()=>calculator()}>click to see changes</button>
<table>
    <tr>
    <th>firstnumber</th>
    <th>secondnumber</th>
    <th>sum</th>
    <th>multiplication</th>
    <th>division</th>
    <th>subtraction</th>    
</tr>
<tr>
    <td>{f1}</td>
    <td>{f2}</td>
    <td>{sum}</td>
    <td>{mul}</td>
    <td>{div}</td>
    <td>{sub}</td>
</tr>
</table>
</main> 

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
        background-color: cyan;
        

	}
table{
    border: 3px solid black;
    margin-left: 30%;
}
tr{
    border: 3px solid black;
    margin: 10px;
}
td,th{
    border:2px solid black
}
	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}

	
	
</style>