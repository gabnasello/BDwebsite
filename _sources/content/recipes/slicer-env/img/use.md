# How to use the slicer-env container

## Open the Docker container

1. Run the command:

`bdstart slicer-env`

2. Click on the `Slicer GUI` link
3. Open the `X11 Session` and you will see Slicer app running
4. *Optional* - Click on the computer icon (up-left) to adjust the screen resolution   

## Remote desktop clipboard

Text copied in the remote desktop will appear in the clipboard box in noVNC's interface. 

![](img/noVNC_clipboard.png)

You can then copy the text from that box to access it in your local clipboard. 

Any text put into the clipboard box will be sent to the remote clipboard as well.

## Run Jupyter Lab server

1. Inside the Slicer app, go to the `Modules` -> `Developer Tool` -> `JupyterKernel`
2. Select the home folder in `Notebook directory` (important: `/home/researcher/mounted_volume` is your local `$HOME` folder in the BD center)
3. Click `Start Jupyter server`
4. Move to the Python Interactor window (up-right Python button) and run the command:

Remember to [copy the command via the remote desktop clipboard](#remote-desktop-clipboard)

```slicer.util._executePythonModule("jupyter", ["server", "list"])```

6. Copy the code after `token=` [via the remote desktop clipboard](#remote-desktop-clipboard)
7. Open the `Slicer Jupyter (ONLY after activation from Slicer GUI)` link from the terminal you used to start the container
8. Insert the token and JupyterLab will start 
