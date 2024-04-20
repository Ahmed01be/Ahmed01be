import requests

# Replace 'YOUR_API_KEY' with your actual API key
API_KEY = 'YOUR_API_KEY'

# Example endpoint URL for retrieving live streams
endpoint_url = 'https://api.bigolive.com/v1/live?access_token=' + API_KEY

def get_live_streams():
    try:
        # Sending GET request to the API endpoint
        response = requests.get(endpoint_url)
        # Checking if the request was successful
        if response.status_code == 200:
            # Parsing the JSON response
            live_streams = response.json()
            return live_streams
        else:
            print('Failed to retrieve live streams. Status code:', response.status_code)
            return None
    except Exception as e:
        print('An error occurred:', e)
        return None

def main():
    # Getting live streams using the API
    live_streams = get_live_streams()
    if live_streams:
        # Displaying information about each live stream
        for stream in live_streams:
            print('Stream ID:', stream.get('id'))
            print('Title:', stream.get('title'))
            print('Broadcaster:', stream.get('broadcaster').get('nickname'))
            print('Viewer count:', stream.get('viewer_count'))
            print('---------------------------------------------')

if __name__ == "__main__":
    main()
