# Testing DonkeyCar

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
You must navigate to the directory with the script. The second command executes it in Python and starts the DonkeyCar server which will allow you to remote in from a web browser.


## Connecting in the browser

Open a browser and navigate to the cars IP address. The output in the command line will also giv eyou a port number. The default is 8887

```
    In the browser navigate to:
    <DonkeyCar IP>:8887
```