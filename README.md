java-json-rpc
=============
{ 
  "method"  : "accounts.addUser",
  "params"  : { "name" : "Jason Remote", "age" : 25, "email" : "jason@remote.com" },
  "id"      : 123,
  "jsonrpc" : "2.0"
}

output:
{
  "result" : "uid-001",
  "id"     : 123,
  "jsonrpc":"2.0"
}


// The remote method to call
String method = "makePayment";

// The required named parameters to pass
Map<String,Object> params = new HashMap<String,Object>();
params.put("recipient", "Penny Adams");
params.put("amount", 175.05);

// The mandatory request ID
String id = "req-001";

// Create a new JSON-RPC 2.0 request
JSONRPC2Request reqOut = new JSONRPC2Request(method, params, id);

// Serialise the request to a JSON-encoded string
String jsonString = reqOut.toString();

// jsonString can now be dispatched to the server...

output:
{ 
  "id"      : "req-001",
  "method"  : "makePayment",
  "params"  : { "amount" : 175.05, "recipient" : "Penny Adams" },
  "jsonrpc" : "2.0"
}

Suppose you have a method "makePayment" which takes three parameters specified by name. Its signature looks like this:
method: "makePayment"
named parameters:
	"recipient"    : string, mandatory
	"amount"       : number, mandatory
	"confirmation" : boolean, optional (defaults to false)
	
	output:
	
	


