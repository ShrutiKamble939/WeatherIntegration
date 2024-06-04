


1. Have jdk 11 installed on the machine
2. run the spring boot project using spring boot application
3. using postman hit the following curl commands
Note - just  import the curl command and trigger it



Curl command 1-- 

OkHttpClient client = new OkHttpClient().newBuilder()
  .build();
MediaType mediaType = MediaType.parse("application/json");
RequestBody body = RequestBody.create(mediaType, "{\r\n    \"cityname\":\"London\"\r\n}");
Request request = new Request.Builder()
  .url("http://localhost:9090/weather")
  .method("POST", body)
  .addHeader("Content-Type", "application/json")
  .build();
Response response = client.newCall(request).execute();


Curl command 2-- 

OkHttpClient client = new OkHttpClient().newBuilder()
  .build();
MediaType mediaType = MediaType.parse("application/json");
RequestBody body = RequestBody.create(mediaType, "{\r\n    \"cityname\":\"\"\r\n}");
Request request = new Request.Builder()
  .url("http://localhost:9090/weather")
  .method("POST", body)
  .addHeader("Content-Type", "application/json")
  .build();
Response response = client.newCall(request).execute();


