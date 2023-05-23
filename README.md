import time

def focus_timer(minutes):
    """A function to create a timer for focusing on work or studying."""
    
    seconds = minutes * 60
    
    while seconds:
        mins, secs = divmod(seconds, 60)
        timer = '{:02d}:{:02d}'.format(mins, secs)
        print(timer, end="\r")
        time.sleep(1)
        seconds -= 1
        
    print('Time is up! Good job.')
