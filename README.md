**Description** 

Get following information by IP address:

ipVersion
ipAddress
latitude
longitude
countryName
countryCode
cityName
regionName

**API:** 

[https://rapidapi.com/zilinskivan/api/recipe64/](https://rapidapi.com/zilinskivan/api/ip-geolocation23)

**Code Samples:** 

**-HTTP**

<pre>
GET / HTTP/1.1
X-Rapidapi-Key: Your API Key
X-Rapidapi-Host: ip-geolocation23.p.rapidapi.com
Host: ip-geolocation23.p.rapidapi.com
</pre>

**-NodeJS**

<pre>
const http = require('https');

const options = {
	method: 'GET',
	hostname: 'ip-geolocation23.p.rapidapi.com',
	port: null,
	path: '/',
	headers: {
		'X-RapidAPI-Key': 'Your API Key',
		'X-RapidAPI-Host': 'ip-geolocation23.p.rapidapi.com'
	}
};

const req = http.request(options, function (res) {
	const chunks = [];

	res.on('data', function (chunk) {
		chunks.push(chunk);
	});

	res.on('end', function () {
		const body = Buffer.concat(chunks);
		console.log(body.toString());
	});
});

req.end();
</pre>

**-PHP**

<pre>
<?php

$curl = curl_init();

curl_setopt_array($curl, [
	CURLOPT_URL => "https://ip-geolocation23.p.rapidapi.com/",
	CURLOPT_RETURNTRANSFER => true,
	CURLOPT_ENCODING => "",
	CURLOPT_MAXREDIRS => 10,
	CURLOPT_TIMEOUT => 30,
	CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
	CURLOPT_CUSTOMREQUEST => "GET",
	CURLOPT_HTTPHEADER => [
		"X-RapidAPI-Host: ip-geolocation23.p.rapidapi.com",
		"X-RapidAPI-Key: Your API Key"
	],
]);

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
	echo "cURL Error #:" . $err;
} else {
	echo $response;
}
</pre>

