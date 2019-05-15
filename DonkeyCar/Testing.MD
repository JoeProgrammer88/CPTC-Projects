# Testing DonkeyCar

## Discovering the IP Addresses

```
    ping <carname>
```
When a the Raspberry PI is configured with a name you can ping it (while on the same network) to discover the IP address. Alternatively, if you are using a HotSpot in Windows 10, it will show the IP of every device connected through the hotspot.

## Connecting Remotely
Rather than directly connecting to the Raspberry PI you can ssh into it.

```
    ssh pi@<DonkeyCar IP>
```
It should prompt for the pi user password after and connect successfully

## Starting DonkeyCar
On the DonkeyCar itself run

```
    cd mycar
    python manage.py drive
```
You must navigate to the directory with the script. The second command executes it in Python and starts the DonkeyCar server which will allow you to remote in from a web browser. You must open a separate terminal for each car to start the manage.py script to keep it executing.


## Connecting in the browser

Open a browser and navigate to the cars IP address. The output in the command line will also giv eyou a port number. The default is 8887

```
    In the browser navigate to:
    <DonkeyCar IP>:8887
```

Using your phone browser by hand, or using an Xbox Controller through a browser, drive the car to take pictures and collect data.

## Xbox Controller Support (May 2019)
- Works with Edge on desktop
- Does not work with Chrome on desktop
- Mobile browsers/other browsers untested