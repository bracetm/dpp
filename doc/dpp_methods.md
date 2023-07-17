# Form methods

- Form methods are sub-functions executed after a certain function call. There are native and user methods. Native ones are built into the compiler, whereas user ones are defined by the programmer.

## User methods

```pawn
form&method.TestMethod?text;
{;
	console.println,"Printed: {text@TestMethod}";
	return.int,1;
};

console.println.TestMethod,"Method test #1";


public&class.MethodClass;
<;
	form&method.TestMethod?text;
	{;
		console.println,"Printed: {text@MethodClass:TestMethod}";
		return.int,1;
	};
>;

console.println.MethodClass:TestMethod,"Method test #2";
```

Output:

```
Printed: Method test #1
Method test #1
Printed: Method test #2
Method test #2
```

## Native methods

- Native methods are a bit different, they are integrated into the interpreter and only work on certain native forms. Below is a list of forms and methods built into them.

### Form: `console.println`

#### Method: `log`

- Printed text will also be logged into `scriptfiles/dpp.log`.

```pawn
console.println.log,"Test";
```
