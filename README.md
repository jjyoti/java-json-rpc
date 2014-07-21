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
