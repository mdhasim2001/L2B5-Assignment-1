*** What are some differences between interfaces and types in TypeScript?
1.
// type alias
type Parsion {
  name : string;
  age : number
}

// interface type
interface {
  name : string;
  age : number
}

2. When we use another interface to create an interface, we have to use extend
   example :
   interface Parson {
     name : string;
     age : number;
   }
   interface Student extend Parson {
     class : number;
   }

   and When we use another type alias to create an type alias, we have to use intersection (&)
   example :
   type Parson = {
     name : string;
     age : number;
   }
   type Student = Parson & {
     class : number;
   }


   *** Provide an example of using union and intersection types in TypeScript.

   A variable can have multiple types, so the union type is used
   example :
   
   type Status = string | number | boolen;

   function userType(value: Status) : Status {
      console.log(`Status set to: ${value}`);
    }

    userType("I am Hasim"); 
    userType(2001);
    userType(true)

   We use intersection type to combine all properties of multiple types
   example :
   type Status = string & number & boolen;

   function userType(value: Status) : Status {
      console.log(value);
    }

    userType("Hasim", 2001, true); 
   
