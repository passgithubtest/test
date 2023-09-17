# tested

<a href="https://go.8x8.vc['go.vc.vc']/support">Contact support</a>
<script>
const ipAddress = 'your-ip-address'; // Replace with the desired IP address
const url = `http://${ipAddress}/path/to/resource`; // Construct the URL

// Construct custom headers
const customHeaders = new Headers();
customHeaders.append('Host', 'custom-host-header.com'); // Add your custom Host header
// Add other custom headers as needed

// Create the request object
const request = new Request(url, {
  method: 'GET', // Adjust the HTTP method as needed
  headers: customHeaders,
});

// Send the request
fetch(request)
  .then(response => {
    if (!response.ok) {
      throw new Error(`Network response was not ok: ${response.status}`);
    }
    return response.text(); // You can also use .json() for JSON data
  })
  .then(data => {
    // Handle the response data here
    console.log(data);
  })
  .catch(error => {
    // Handle any errors that occurred during the fetch
    console.error('Fetch error:', error);
  });
</script>
