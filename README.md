# PHPHandlingObjectInsideArrayFunc
PHP execute data in object inside the array function 


```PHP

  Class Person {
 	
   public function name( $name) { return $name; }	
   
   public function cc() { return 123; }
   
  }
 
 function data() {
 	
   return [
 	
 	 'request' => function( ) { 
 	 	
 	 	$name = new Person();
 	  
 		return implode('', [ $name->name('na') , $name->cc() ]);
 		
 	 },
 	 'get' => function() : int { return (int) 1230; }
 	
 	];
 	
 }

  var_dump( data()["request"]());

 // Result: string(5) "na123"

```


<br /> Reference: 
<br /> https://github.com/PHPWine/PHPVanilla/blob/main/Crud/Vanilla.php
<br /> https://github.com/PHPWine/PHPVanilla/tree/main
